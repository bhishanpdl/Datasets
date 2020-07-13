# Sklearn datasets
```python
from sklearn import datasets

fnames = [ i for i in dir(datasets) if 'load_' in i]
print(fnames)
# 'load_boston', 'load_breast_cancer','load_diabetes', 'load_digits', 'load_files'
# 'load_iris', 'load_linnerud','load_mlcomp','load_sample_image','load_sample_images',
# 'load_svmlight_file', 'load_svmlight_files', 'load_wine'

iris = datasets.load_iris()
iris_df = pd.DataFrame(iris.data, columns=iris.feature_names)
print(datasets.load_iris().DESCR)

X,y = datasets.load_iris(return_X_y=True) # numpy arrays
dic_data = datasets.load_iris(as_frame=True)
print(dic_data.keys())
df = dic_data['frame']
df_X = dic_data['data']
ser_y = dic_data['target']
dic_data['target_names'] # numpy array



from sklearn import datasets

fnames_and_others = [ i for i in dir(datasets) if 'load_' in i]
fnames = ['load_boston', 'load_breast_cancer', 'load_diabetes',
          'load_digits', 'load_iris', 'load_wine']
print(fnames)

fname = 'load_boston'
loader = getattr(datasets,fname)()
df = pd.DataFrame(loader['data'],columns= loader['feature_names'])
df['target'] = loader['target']
df.head(2)

for fname in fnames:
    print()
    print(fname)
    loader = getattr(datasets,fname)()
    df = pd.DataFrame(loader['data'],columns= loader['feature_names'])
    df['target'] = loader['target']
    display(df.head(2))
```

# Datasets
```
load_boston
CRIM	ZN	INDUS	CHAS	NOX	RM	AGE	DIS	RAD	TAX	PTRATIO	B	LSTAT	target
0	0.00632	18.0	2.31	0.0	0.538	6.575	65.2	4.0900	1.0	296.0	15.3	396.9	4.98	24.0
1	0.02731	0.0	7.07	0.0	0.469	6.421	78.9	4.9671	2.0	242.0	17.8	396.9	9.14	21.6

load_breast_cancer
mean radius	mean texture	mean perimeter	mean area	mean smoothness	mean compactness	mean concavity	mean concave points	mean symmetry	mean fractal dimension	radius error	texture error	perimeter error	area error	smoothness error	compactness error	concavity error	concave points error	symmetry error	fractal dimension error	worst radius	worst texture	worst perimeter	worst area	worst smoothness	worst compactness	worst concavity	worst concave points	worst symmetry	worst fractal dimension	target
0	17.99	10.38	122.8	1001.0	0.11840	0.27760	0.3001	0.14710	0.2419	0.07871	1.0950	0.9053	8.589	153.40	0.006399	0.04904	0.05373	0.01587	0.03003	0.006193	25.38	17.33	184.6	2019.0	0.1622	0.6656	0.7119	0.2654	0.4601	0.11890	0
1	20.57	17.77	132.9	1326.0	0.08474	0.07864	0.0869	0.07017	0.1812	0.05667	0.5435	0.7339	3.398	74.08	0.005225	0.01308	0.01860	0.01340	0.01389	0.003532	24.99	23.41	158.8	1956.0	0.1238	0.1866	0.2416	0.1860	0.2750	0.08902	0

load_diabetes
age	sex	bmi	bp	s1	s2	s3	s4	s5	s6	target
0	0.038076	0.050680	0.061696	0.021872	-0.044223	-0.034821	-0.043401	-0.002592	0.019908	-0.017646	151.0
1	-0.001882	-0.044642	-0.051474	-0.026328	-0.008449	-0.019163	0.074412	-0.039493	-0.068330	-0.092204	75.0

load_digits
pixel_0_0	pixel_0_1	pixel_0_2	pixel_0_3	pixel_0_4	pixel_0_5	pixel_0_6	pixel_0_7	pixel_1_0	pixel_1_1	pixel_1_2	pixel_1_3	pixel_1_4	pixel_1_5	pixel_1_6	pixel_1_7	pixel_2_0	pixel_2_1	pixel_2_2	pixel_2_3	pixel_2_4	pixel_2_5	pixel_2_6	pixel_2_7	pixel_3_0	pixel_3_1	pixel_3_2	pixel_3_3	pixel_3_4	pixel_3_5	pixel_3_6	pixel_3_7	pixel_4_0	pixel_4_1	pixel_4_2	pixel_4_3	pixel_4_4	pixel_4_5	pixel_4_6	pixel_4_7	pixel_5_0	pixel_5_1	pixel_5_2	pixel_5_3	pixel_5_4	pixel_5_5	pixel_5_6	pixel_5_7	pixel_6_0	pixel_6_1	pixel_6_2	pixel_6_3	pixel_6_4	pixel_6_5	pixel_6_6	pixel_6_7	pixel_7_0	pixel_7_1	pixel_7_2	pixel_7_3	pixel_7_4	pixel_7_5	pixel_7_6	pixel_7_7	target
0	0.0	0.0	5.0	13.0	9.0	1.0	0.0	0.0	0.0	0.0	13.0	15.0	10.0	15.0	5.0	0.0	0.0	3.0	15.0	2.0	0.0	11.0	8.0	0.0	0.0	4.0	12.0	0.0	0.0	8.0	8.0	0.0	0.0	5.0	8.0	0.0	0.0	9.0	8.0	0.0	0.0	4.0	11.0	0.0	1.0	12.0	7.0	0.0	0.0	2.0	14.0	5.0	10.0	12.0	0.0	0.0	0.0	0.0	6.0	13.0	10.0	0.0	0.0	0.0	0
1	0.0	0.0	0.0	12.0	13.0	5.0	0.0	0.0	0.0	0.0	0.0	11.0	16.0	9.0	0.0	0.0	0.0	0.0	3.0	15.0	16.0	6.0	0.0	0.0	0.0	7.0	15.0	16.0	16.0	2.0	0.0	0.0	0.0	0.0	1.0	16.0	16.0	3.0	0.0	0.0	0.0	0.0	1.0	16.0	16.0	6.0	0.0	0.0	0.0	0.0	1.0	16.0	16.0	6.0	0.0	0.0	0.0	0.0	0.0	11.0	16.0	10.0	0.0	0.0	1

load_iris
sepal length (cm)	sepal width (cm)	petal length (cm)	petal width (cm)	target
0	5.1	3.5	1.4	0.2	0
1	4.9	3.0	1.4	0.2	0

load_wine
alcohol	malic_acid	ash	alcalinity_of_ash	magnesium	total_phenols	flavanoids	nonflavanoid_phenols	proanthocyanins	color_intensity	hue	od280/od315_of_diluted_wines	proline	target
0	14.23	1.71	2.43	15.6	127.0	2.80	3.06	0.28	2.29	5.64	1.04	3.92	1065.0	0
1	13.20	1.78	2.14	11.2	100.0	2.65	2.76	0.26	1.28	4.38	1.05
```
