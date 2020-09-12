# Reading the data
```python
path_pro = 'https://github.com/bhishanpdl/Datasets/blob/master/Projects/All_State_Insurance/processed'

df_train = pd.read_csv(f'{path_pro}/train_cleaned_encoded.csv.zip?raw=true',compression='zip')

df_test = pd.read_csv(f'{path_pro}/test_cleaned_encoded.csv.zip?raw=true',compression='zip')

print(df_train.shape) # (188318, 816)
df_train.head(2).append(df_train.tail(2))
```
