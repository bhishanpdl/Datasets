# Description
IMDB dataset having 50K movie reviews for natural language processing or Text analytics.
This is a dataset for binary sentiment classification containing substantially more data than previous benchmark datasets. We provide a set of 25,000 highly polar movie reviews for training and 25,000 for testing. So, predict the number of positive and negative reviews using either classification or deep learning algorithms.
For more dataset information, please go through the following link, http://ai.stanford.edu/~amaas/data/sentiment/

Kaggle: https://www.kaggle.com/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews

# Reading data using pandas
```python
ifile = "https://github.com/bhishanpdl/Datasets/blob/master/Kaggle/IMDB/imdb.zip?raw=true"
df = pd.read_csv(ifile,compression='zip')
print(f"df {df.shape}")
display(df.head(2).append(df.tail(2)))
```

# Reading tar data from stanford
``
Files:
folder: aclImdb
files: 
imdbEr.txt
imdb.vocab
README

subfolders:
test
train

files inside train:
labeledBow.feat
unsupBow.feat
urls_neg.txt
urls_pos.txt
urls_unsup.txt

subfolders:
neg
pos
unsup

Command: ls aclImdb/train/pos/ | head
0_9.txt
10000_8.txt
10001_10.txt

Command: ls aclImdb/train/neg/ | head
0_3.txt
10000_4.txt
10001_4.txt

Command:
head -2 aclImdb/train/neg/0_3.txt

Story of a man who has unnatural feelings for a pig. Starts out with a opening scene that is a terrific example of absurd comedy. A formal orchestra audience is turned into an insane, violent mob by the crazy chantings of it's singers. Unfortunately it stays absurd the WHOLE time with no general narrative eventually making it just too off putting. Even those from the era should be turned off. The cryptic dialogue would make Shakespeare seem easy to a third grader. On a technical level it's better than you might think with some good cinematography by future great Vilmos Zsigmond. Future stars Sally Kirkland and Frederic Forrest can be seen briefly.
```



```python
import requests

url = 'http://ai.stanford.edu/~amaas/data/sentiment/aclImdb_v1.tar.gz'
target_path = 'aclImdb_v1.tar.gz'

response = requests.get(url, stream=True)
if response.status_code == 200:
    with open(target_path, 'wb') as f:
        f.write(response.raw.read())
        
import tarfile
tar = tarfile.open('aclImdb_v1.tar.gz')
tar.extractall()
tar.close()

import glob 
classes = {'pos':1, 'neg':0}

def read_txt(file_path):
  with open(file_path, 'r') as file:
    text = file.read()
  file.close()
  return text

def populate(main_folder):
  all_txts, all_sentiments = [], []
  for class_ in classes:
    directory = "aclImdb/{}/{}".format(main_folder, class_)
    file_paths = glob.glob(directory + '/*.txt')
    txts = [read_txt(path) for path in file_paths]
    sentiments = [classes[class_] for _ in range(len(txts))]
    all_txts.extend(txts)
    all_sentiments.extend(sentiments)
  return all_txts, all_sentiments
  
X_train, y_train = populate('train')
X_test, y_test = populate('test')

print(len(X_train))
print(len(X_test))
```
