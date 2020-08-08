# USA States latitude and longitude
Data from [google developer data](https://developers.google.com/public-data/docs/canonical/states_csv)

```python
df_lat_lon = pd.read_html("https://developers.google.com/public-data/docs/canonical/states_csv")[0]

df_lat_lon.to_csv('../data/usa_lat_lon.csv',index=False)
```
