# Scrape the data
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
