# Resources
- kaggle github: https://github.com/Kaggle/kaggle-api

# Installing kaggle module
- Create Kaggle account
- Click on logo > Account > Create API Token
- Copy downloaded json to `~/.kaggle/kaggle.json`
- Change permissions `chmod 600 ~/.kaggle/kaggle.json`
- Go to conda env and install the module `pip install kaggle`

# Getting  dataset
```python
# -c is competition
!kaggle competitions files -c web-traffic-time-series-forecasting
!kaggle competitions download -c web-traffic-time-series-forecasting -f train_1.csv.zip

# project data download
!kaggle datasets files zillow/zecon
!kaggle datasets download zillow/zecon -f State_time_series.csv

# search data with -s
!kaggle datasets list -s health
```