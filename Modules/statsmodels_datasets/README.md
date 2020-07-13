# Statsmodels Built-in Datasets
```python
import statsmodels.api as sm

# built-in datasets
excludes = ['PytestTester', 'test', 'utils','webuse',
            'get_data_home', 'get_rdataset','check_internet','clear_data_home',]
fnames = [i for i in dir(sm.datasets) if i[0]!='_' if i not in excludes ]
print(fnames)
# ['anes96', 'cancer', 'ccard', 'china_smoking', 'co2', 'committee',
# 'copper', 'cpunish', 'elnino', 'engel', 'fair', 'fertility', 'grunfeld',
# 'heart', 'interest_inflation', 'longley', 'macrodata', 'modechoice', 'nile',
# 'randhie', 'scotland', 'spector', 'stackloss', 'star98', 'statecrime', 'strikes', 'sunspots']

for fname in fnames:
    print()
    print(fname)
    df = getattr(sm.datasets,fname).load_pandas().data
    display(df.head(2))
```

# Getting Rdatasets from stasmodels
Statsmodels provides access to 1173 datasets from the [Rdatasets project](https://github.com/vincentarelbundock/Rdatasets).

```python
df_iris = sm.datasets.get_rdataset('iris').data
dataset_iris = sm.datasets.get_rdataset(dataname='iris', package='datasets')
print(dataset_iris.title) # "Edgar Anderson's Iris Data"
print(dataset_iris.__doc__)
```

# Statsmodels Built-in datasets sample
- anes96:  [American National Election Survey 1996](http://www.statsmodels.org/dev/datasets/generated/anes96.html)
- cancer: [Breast Cancer Data](http://www.statsmodels.org/dev/datasets/generated/cancer.html)
- ccard: [Bill Greene’s credit scoring data.](http://www.statsmodels.org/dev/datasets/generated/ccard.html)
- china_smoking: [Smoking and lung cancer in eight cities in China.](http://www.statsmodels.org/dev/datasets/generated/china_smoking.html)
- co2: [Mauna Loa Weekly Atmospheric CO2 Data](http://www.statsmodels.org/dev/datasets/generated/co2.html)
- committee: [First 100 days of the US House of Representatives 1995](http://www.statsmodels.org/dev/datasets/generated/committee.html)
- copper: [World Copper Market 1951-1975 Dataset](http://www.statsmodels.org/dev/datasets/generated/copper.html)	
- cpunish: [US Capital Punishment dataset](http://www.statsmodels.org/dev/datasets/generated/cpunish.html)
- elnino: [El Nino - Sea Surface Temperatures	](http://www.statsmodels.org/dev/datasets/generated/elnino.html)
- engel: [Engel (1857) food expenditure data](http://www.statsmodels.org/dev/datasets/generated/engel.html)
- fair: [Affairs dataset](http://www.statsmodels.org/dev/datasets/generated/fair.html)
- fertility: [World Bank Fertility Data](http://www.statsmodels.org/dev/datasets/generated/fertility.html)
- grunfeld: [Grunfeld (1950) Investment Data](http://www.statsmodels.org/dev/datasets/generated/grunfeld.html)
- heart: [Transplant Survival Data](http://www.statsmodels.org/dev/datasets/generated/heart.html)
- longley: [Longley dataset](http://www.statsmodels.org/dev/datasets/generated/longley.html)
- macrodata: [United States Macroeconomic data](http://www.statsmodels.org/dev/datasets/generated/macrodata.html)
- modechoice: [Travel Mode Choice](http://www.statsmodels.org/dev/datasets/generated/modechoice.html)
- nile: [Nile River flows at Ashwan 1871-1970](http://www.statsmodels.org/dev/datasets/generated/nile.html)
- randhie: [RAND Health Insurance Experiment Data](http://www.statsmodels.org/dev/datasets/generated/randhie.html)
- scotland: [Taxation Powers Vote for the Scottish Parliamant 1997](http://www.statsmodels.org/dev/datasets/generated/scotland.html)
- spector: [Spector and Mazzeo (1980) - Program Effectiveness Data](http://www.statsmodels.org/dev/datasets/generated/spector.html)
- stackloss: [Stack loss data](http://www.statsmodels.org/dev/datasets/generated/stackloss.html)
- star98: [Star98 Educational Dataset](http://www.statsmodels.org/dev/datasets/generated/star98.html)
- statecrime: [Statewide Crime Data 2009](http://www.statsmodels.org/dev/datasets/generated/statecrime.html)
- strikes: [U.S. Strike Duration Data](http://www.statsmodels.org/dev/datasets/generated/strikes.html)
- sunspots: [Yearly sunspots data 1700-2008](http://www.statsmodels.org/dev/datasets/generated/sunspots.html)

```
anes96
popul	TVnews	selfLR	ClinLR	DoleLR	PID	age	educ	income	vote	logpopul
0	0.0	7.0	7.0	1.0	6.0	6.0	36.0	3.0	1.0	1.0	-2.302585
1	190.0	1.0	3.0	3.0	5.0	1.0	20.0	4.0	1.0	0.0	5.247550

cancer
cancer	population
0	1.0	445.0
1	0.0	559.0

ccard
AVGEXP	AGE	INCOME	INCOMESQ	OWNRENT
0	124.98	38.0	4.52	20.4304	1.0
1	9.85	33.0	2.42	5.8564	0.0

china_smoking
smoking_yes_cancer_yes	smoking_yes_cancer_no	smoking_no_cancer_yes	smoking_no_cancer_no
Location				
Beijing	126	100	35	61
Shanghai	908	688	497	807

co2
co2
1958-03-29	316.1
1958-04-05	317.3

committee
BILLS104	SIZE	SUBS	STAFF	PRESTIGE	BILLS103
0	6.0	58.0	13.0	109.0	1.0	9.0
1	23.0	42.0	0.0	39.0	1.0	101.0

copper
WORLDCONSUMPTION	COPPERPRICE	INCOMEINDEX	ALUMPRICE	INVENTORYINDEX	TIME
0	3173.0	26.56	0.70	19.76	0.98	1.0
1	3281.1	27.31	0.71	20.78	1.04	2.0

cpunish
EXECUTIONS	INCOME	PERPOVERTY	PERBLACK	VC100k96	SOUTH	DEGREE
0	37.0	34453.0	16.7	12.2	644.0	1.0	0.16
1	9.0	41534.0	12.5	20.0	351.0	1.0	0.27

elnino
YEAR	JAN	FEB	MAR	APR	MAY	JUN	JUL	AUG	SEP	OCT	NOV	DEC
0	1950.0	23.11	24.20	25.37	23.86	23.03	21.57	20.63	20.15	19.67	20.03	20.02	21.80
1	1951.0	24.19	25.28	25.60	25.37	24.79	24.69	23.86	22.32	21.44	21.77	22.33	22.89

engel
income	foodexp
0	420.157651	255.839425
1	541.411707	310.958667

fair
rate_marriage	age	yrs_married	children	religious	educ	occupation	occupation_husb	affairs
0	3.0	32.0	9.0	3.0	3.0	17.0	2.0	5.0	0.111111
1	3.0	27.0	13.0	3.0	1.0	14.0	3.0	4.0	3.230769

fertility
Country Name	Country Code	Indicator Name	Indicator Code	1960	1961	1962	1963	1964	1965	1966	1967	1968	1969	1970	1971	1972	1973	1974	1975	1976	1977	1978	1979	1980	1981	1982	1983	1984	1985	1986	1987	1988	1989	1990	1991	1992	1993	1994	1995	1996	1997	1998	1999	2000	2001	2002	2003	2004	2005	2006	2007	2008	2009	2010	2011	2012	2013
0	Aruba	ABW	Fertility rate, total (births per woman)	SP.DYN.TFRT.IN	4.82	4.655	4.471	4.271	4.059	3.842	3.625	3.417	3.226	3.054	2.908	2.788	2.691	2.613	2.552	2.506	2.472	2.446	2.425	2.408	2.392	2.377	2.364	2.353	2.342	2.332	2.32	2.307	2.291	2.272	2.249	2.221	2.187	2.149	2.108	2.064	2.021	1.979	1.94	1.905	1.874	1.848	1.825	1.805	1.786	1.769	1.754	1.739	1.726	1.713	1.701	1.69	NaN	NaN
1	Andorra	AND	Fertility rate, total (births per woman)	SP.DYN.TFRT.IN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	1.240	1.180	1.250	1.190	1.220	NaN	NaN	NaN

grunfeld
invest	value	capital	firm	year
0	317.6	3078.5	2.8	General Motors	1935.0
1	391.8	4661.7	52.6	General Motors	1936.0

heart
survival	censors	age
0	15.0	1.0	54.3
1	3.0	1.0	40.4

interest_inflation
year	quarter	Dp	R
0	1972.0	2.0	-0.003133	0.083
1	1972.0	3.0	0.018871	0.083

longley
TOTEMP	GNPDEFL	GNP	UNEMP	ARMED	POP	YEAR
0	60323.0	83.0	234289.0	2356.0	1590.0	107608.0	1947.0
1	61122.0	88.5	259426.0	2325.0	1456.0	108632.0	1948.0

macrodata
year	quarter	realgdp	realcons	realinv	realgovt	realdpi	cpi	m1	tbilrate	unemp	pop	infl	realint
0	1959.0	1.0	2710.349	1707.4	286.898	470.045	1886.9	28.98	139.7	2.82	5.8	177.146	0.00	0.00
1	1959.0	2.0	2778.801	1733.7	310.859	481.301	1919.7	29.15	141.7	3.08	5.1	177.830	2.34	0.74

modechoice
individual	mode	choice	ttme	invc	invt	gc	hinc	psize
0	1.0	1.0	0.0	69.0	59.0	100.0	70.0	35.0	1.0
1	1.0	2.0	0.0	34.0	31.0	372.0	71.0	35.0	1.0

nile
year	volume
0	1871.0	1120.0
1	1872.0	1160.0

randhie
mdvis	lncoins	idp	lpi	fmde	physlm	disea	hlthg	hlthf	hlthp
0	0	4.61512	1	6.907755	0.0	0.0	13.73189	1	0	0
1	2	4.61512	1	6.907755	0.0	0.0	13.73189	1	0	0

scotland
YES	COUTAX	UNEMPF	MOR	ACT	GDP	AGE	COUTAX_FEMALEUNEMP
0	60.3	712.0	21.0	105.0	82.4	13566.0	12.3	14952.0
1	52.3	643.0	26.5	97.0	80.2	13566.0	15.3	17039.5

spector
GPA	TUCE	PSI	GRADE
0	2.66	20.0	0.0	0.0
1	2.89	22.0	0.0	0.0

stackloss
STACKLOSS	AIRFLOW	WATERTEMP	ACIDCONC
0	42.0	80.0	27.0	89.0
1	37.0	80.0	27.0	88.0

star98
NABOVE	NBELOW	LOWINC	PERASIAN	PERBLACK	PERHISP	PERMINTE	AVYRSEXP	AVSALK	PERSPENK	PTRATIO	PCTAF	PCTCHRT	PCTYRRND	PERMINTE_AVYRSEXP	PERMINTE_AVSAL	AVYRSEXP_AVSAL	PERSPEN_PTRATIO	PERSPEN_PCTAF	PTRATIO_PCTAF	PERMINTE_AVYRSEXP_AVSAL	PERSPEN_PTRATIO_PCTAF
0	452.0	355.0	34.39730	23.29930	14.235280	11.411120	15.91837	14.70646	59.15732	4.445207	21.71025	57.03276	0.0	22.22222	234.102872	941.68811	869.9948	96.50656	253.52242	1238.1955	13848.8985	5504.0352
1	144.0	40.0	17.36507	29.32838	8.234897	9.314884	13.63636	16.08324	59.50397	5.267598	20.44278	64.62264	0.0	0.00000	219.316851	811.41756	957.0166	107.68435	340.40609	1321.0664	13050.2233	6958.8468

statecrime
violent	murder	hs_grad	poverty	single	white	urban
state							
Alabama	459.9	7.1	82.1	17.5	29.0	70.0	48.65
Alaska	632.6	3.2	91.4	9.0	25.5	68.3	44.46

strikes
duration	iprod
0	7.0	0.01138
1	9.0	0.01138

sunspots
YEAR	SUNACTIVITY
0	1700.0	5.0
1	1701.0	11.0
```
