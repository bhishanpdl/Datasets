# Data Description
Reference: https://www.kaggle.com/c/web-traffic-time-series-forecasting/data

train_1.csv:
```
rows = 145,063
columns = 551

first column = Page	
date columns = 2015-07-01, 2015-07-02, ..., 2016-12-31 (550 columns)

file size: 284.6 MB

Date columns:
------------------
Jul/2015 - 31 days
Aug/2015 - 31 days
Sep/2015 - 30 days
Oct/2015 - 31 days
Nov/2015 - 30 days
Dec/2015 - 31 days

Total     : 184 days
Year 2016 : 366 days (leap year)
Total     : 550 days

NOTE:
For this dataset, missing data is represented by 0.

```

The training dataset consists of approximately 145k time series. Each of these time series represent a number of daily views of a different Wikipedia article, starting from July, 1st, 2015 up until December 31st, 2016. The leaderboard during the training stage is based on traffic from January, 1st, 2017 up until March 1st, 2017.

The second stage will use training data up until September 1st, 2017. The final ranking of the competition will be based on predictions of daily views between September 13th, 2017 and November 13th, 2017 for each article in the dataset. You will submit your forecasts for these dates by September 12th.

For each time series, you are provided the name of the article as well as the type of traffic that this time series represent (all, mobile, desktop, spider). You may use this metadata and any other publicly available data to make predictions. Unfortunately, the data source for this dataset does not distinguish between traffic values of zero and missing values. A missing value may mean the traffic was zero or that the data is not available for that day.

To reduce the submission file size, each page and date combination has been given a shorter Id. The mapping between page names and the submission Id is given in the key files.

# Read the dataset
```bash
%%bash
cd ../data/
rm -rf train_1.csv

# download the data
wget https://github.com/bhishanpdl/Datasets/blob/master/Projects/Web_Traffic_Timeseries_Forecast/raw/train_1_01?raw=true > /dev/null 2>&1

wget https://github.com/bhishanpdl/Datasets/blob/master/Projects/Web_Traffic_Timeseries_Forecast/raw/train_1_02?raw=true > /dev/null 2>&1

wget https://github.com/bhishanpdl/Datasets/blob/master/Projects/Web_Traffic_Timeseries_Forecast/raw/train_1_03?raw=true > /dev/null 2>&1

cat train_1_01?raw=true train_1_02?raw=true train_1_03?raw=true > train_1.csv.zip
# unzip train_1.csv.zip
# I dont have to delete zip file, it is ignored by github

echo ""
echo ""
ls
cd -
```

```python
train = pd.read_csv('../data/train_1.csv.zip',compression='zip')
print(train.shape)

display(train.head())
```