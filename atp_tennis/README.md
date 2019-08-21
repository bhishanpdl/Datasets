# Data Source
Association of Tennis Professionals Matches
ATP tournament results from 2000 to 2017

Web: https://www.kaggle.com/gmadevs/atp-matches-dataset/kernels

There are 48 commas (48+1 column names in 0th row) and first row has 116 commas.

```
tourney_id,tourney_name,surface,draw_size,tourney_level,tourney_date,match_num,winner_id,winner_seed,winner_entry,winner_name,winner_hand,winner_ht,winner_ioc,winner_age,winner_rank,winner_rank_points,loser_id,loser_seed,loser_entry,loser_name,loser_hand,loser_ht,loser_ioc,loser_age,loser_rank,loser_rank_points,score,best_of,round,minutes,w_ace,w_df,w_svpt,w_1stIn,w_1stWon,w_2ndWon,w_SvGms,w_bpSaved,w_bpFaced,l_ace,l_df,l_svpt,l_1stIn,l_1stWon,l_2ndWon,l_SvGms,l_bpSaved,l_bpFaced
2016-M020,Brisbane,Hard,32,A,20160104,300,105683,4,,Milos Raonic,R,196,CAN,25.0212183436,14,2170,103819,1,,Roger Federer,R,185,SUI,34.4065708419,3,8265,6-4 6-4,3,F,87,6,6,60,34,28,14,10,1,1,7,3,61,34,25,14,10,3,5,,,,,,,,,,,,,,,,,,,,
2016-M020,Brisbane,Hard,32,A,20160104,299,103819,1,,Roger Federer,R,185,SUI,34.4065708419,3,8265,106233,8,,Dominic Thiem,R,,AUT,22.3353867214,20,1600,6-1 6-4,3,SF,60,6,0,49,27,23,12,9,0,1,2,4,55,31,18,9,8,2,6,,,,,,,,,,,,,,,,,,,,
```


# Reading dataframe with unequal commas in csv file

```python
# checking
!head -3 /Users/poudel/Datasets/atp_tennis/atp_matches_2016.csv
!head -1 /Users/poudel/Datasets/atp_tennis/atp_matches_2016.csv | tr -cd , | wc -c  # headers are 48+1
!head -2 /Users/poudel/Datasets/atp_tennis/atp_matches_2016.csv | tr -cd , | wc -c  # first row has 116 commas


# file
csv = '/Users/poudel/Datasets/atp_tennis/atp_matches_2016.csv'

# skip header line
df = pd.read_csv(csv, skiprows=[0], header = None)

# drop columns that only have NaNs
df = df.dropna(axis=1, how='all')

# get header from first row
df.columns = pd.read_csv(csv, nrows=0).columns
print(df.shape)
df.head().T
```
