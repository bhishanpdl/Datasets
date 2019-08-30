Table of Contents
=================
   * [web scrape top 250 imdb movies](#web-scrape-top-250-imdb-movies)
   * [web scrape comedy shows transcripts](#web-scrape-comedy-shows-transcripts)

# web scrape top 250 imdb movies
```python
import numpy as np
import pandas as pd

import re
import time

import requests
from bs4 import BeautifulSoup

from IPython.display import display
from ipywidgets import FloatProgress

t0 = time.time()

# url
url = 'http://www.imdb.com/chart/top?ref_=nv_mv_250_6'

# get soup
result = requests.get(url)
c = result.content
soup = BeautifulSoup(c,"lxml")

# Create empty lists to append the extracted data.
moviename = []
cast = []
description = []
rating = []
ratingoutof = []
year = []
genre = []
movielength = []
rot_audscore = []
rot_avgrating = []
rot_users = []

# Extracting the required data from the html soup.
rgx = re.compile('[%s]' % '()')
f = FloatProgress(min=0, max=200)
display(f)

# summary
summary = soup.find('div',{'class':'article'})

for row, i in zip(summary.find('table').findAll('tr'),
                  range(len(summary.find('table').findAll('tr')))):
    
    # get year
    for sitem in row.findAll('span', {'class': 'secondaryInfo'}):
        s = sitem.find(text=True)
        year.append(rgx.sub("", s))
        
    # get ratings
    for ritem in row.findAll('td', {'class': "ratingColumn imdbRating"}):
        for iget in ritem.findAll('strong'):
            rating.append(iget.find(text=True))
            ratingoutof.append(iget.get('title').split(' ', 4)[3])

    # tmdb items             
    for item in row.findAll('td',{'class':'titleColumn'}):
        for href in item.findAll('a',href=True):
            moviename.append(href.find(text=True))
            rurl = 'https://www.rottentomatoes.com/m/'+ href.find(text=True)

            # get rotten url
            try:
                rresult = requests.get(rurl)
            except requests.exceptions.ConnectionError:
                status_code = "Connection refused"

            # rc
            rc = rresult.content
            rsoup = BeautifulSoup(rc)
                
            # 
            try:
                raud = rsoup.find('div', {'class':'meter-value'})
                raud = raud.find('span',{'class':'superPageFontColor'})
                raud = raud.text
                rot_audscore.append(raud)

                ravg = rsoup.find('div',{'class':'audience-info hidden-xs superPageFontColor'})
                ravg = ravg.find('div')
                ravg = ravg.contents[2].strip()
                rot_avgrating.append(ravg)

                ru = rsoup.find('div', {'class':'audience-info hidden-xs superPageFontColor'})
                ru = ru.contents[3].contents[2].strip()
                rot_users.append(ru)

            except AttributeError:
                rot_audscore.append("")
                rot_avgrating.append("")
                rot_users.append("")

            cast.append(href.get('title'))
            imdb = "http://www.imdb.com" + href.get('href')

            try:
                iresult = requests.get(imdb)
                ic = iresult.content
                isoup = BeautifulSoup(ic)
                #print(isoup,file=open('isoup.html','w'))
                
                # desc
                #
                # <div class="summary_text">
                #    The early life and career of Vito Corleone 
                # </div>
                #
                desc = isoup.find('div', {'class':'summary_text'})
                desc = desc.find(text=True).strip()
                description.append(desc)


                # genre
                # <a href="/search/keyword?keywords=mafia"> <span class="itemprop">
                # mafia</span></a><span>|</span>
                #
                # genre = mafia
                gen = isoup.find('span',{'class':'itemprop'})
                gen = gen.find(text=True)
                genre.append(gen)
                

                # duration
                #
                # <time datetime="PT175M">
                #        2h 55min
                #   </time>
                #
                dt = isoup.find('time')
                dt = dt.find(text=True).strip()
                movielength.append(dt)


            except requests.exceptions.ConnectionError:
                description.append("")
                genre.append("")
                movielength.append("")
        # sleep  
        time.sleep(.1)
        f.value = i

t1 = time.time() - t0
print('Time taken {:.0f} min {:.0f} secs: '.format(*divmod(t1,60)))
# 10 min 22 secs

#====================================
# create dataframe
imdb = pd.DataFrame({'rank': range(1, len(year)+1),
                     'moviename': moviename,
                     'year': year,
                     'imdb_rating': rating,
                     'cast': cast,
                     'description': description,
                     'genre': genre,
                     'movielength': movielength,
                     'cast': cast,
                     'imdb_ratingbasedon': ratingoutof,
                     'tomatoes_audscore': rot_audscore,
                     'tomatoes_rating': rot_avgrating,
                     'tomatoes_ratingbasedon': rot_users})

print(imdb.shape)
imdb.head()

```

# web scrape comedy shows transcripts
```python

# Imports
import requests
from bs4 import BeautifulSoup
import pickle

# Scrape the data
def url_to_transcript(url):
    '''Returns transcript data specifically from scrapsfromtheloft.com.'''
    page = requests.get(url).text
    soup = BeautifulSoup(page, "lxml")
    
    # here, for this page the transcript class is post-content
    # (can be seen in google chrome: View > Developer > Inspect Elements)
    text_lst = [p.text for p in soup.find(class_="post-content").find_all('p')]
    return text_lst

# get list of data
url = "https://scrapsfromtheloft.com/2019/08/26/brazil-corruption-amazon-hasan-minhaj/"
text_lst = url_to_transcript(url)

# save as text file
with open('hasan.txt','w') as fo:
    fo.write('\n'.join(text))
    
# save as pickle file
with open("hasan.pkl", "wb") as fo:
        pickle.dump(text_lst, fo)

# load pickle file
with open("hasan.pkl", "rb") as fi:
   data_lst = pickle.load(fi)

# create dataframe
import pandas as pd
pd.set_option('max_colwidth',150)

data_dict = {'hasan': ' '.join(data_lst)}
data_df = pd.DataFrame(data_dict,index=data_dict.keys())
```
