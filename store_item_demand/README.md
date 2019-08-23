# Data source
https://www.kaggle.com/c/demand-forecasting-kernels-only/data

# Data fields
date - Date of the sale data. There are no holiday effects or store closures.
store - Store ID
item - Item ID
sales - Number of items sold at a particular store on a particular date.

# Sample data
```
url = "https://github.com/bhishanpdl/Datasets/blob/master/store_item_demand/train_store_item_demand.csv?raw=true"
df = pd.read_csv(url)
print(df.shape)
df.head()

(913000, 4)
         date  store  item  sales
0  2013-01-01      1     1     13
1  2013-01-02      1     1     11
2  2013-01-03      1     1     14
3  2013-01-04      1     1     13
4  2013-01-05      1     1     10
```
