# Seaborn datasets
```python
import seaborn as sns
iris = sns.load_dataset('iris')

print(sns.get_dataset_names())
'anscombe', 'attention', 'brain_networks', 'car_crashes', 'diamonds', 'dots', 'exercise', 'flights', 'fmri', 
'gammas', 'iris', 'mpg', 'planets', 'tips', 'titanic'
```

# Datasets
```
Dataset:  anscombe
dataset	x	y
0	I	10.0	8.04
1	I	8.0	6.95
2	I	13.0	7.58
3	I	9.0	8.81
4	I	11.0	8.33

Dataset:  attention
Unnamed: 0	subject	attention	solutions	score
0	0	1	divided	1	2.0
1	1	2	divided	1	3.0
2	2	3	divided	1	3.0
3	3	4	divided	1	5.0
4	4	5	divided	1	4.0

Dataset:  brain_networks
network	1	1.1	2	2.1	3	3.1	4	4.1	5	5.1	6	6.1	6.2	6.3	7	7.1	7.2	7.3	7.4	7.5	8	8.1	8.2	8.3	8.4	8.5	9	9.1	10	10.1	11	11.1	12	12.1	12.2	12.3	12.4	13	13.1	13.2	13.3	13.4	13.5	14	14.1	15	15.1	16	16.1	16.2	16.3	16.4	16.5	16.6	16.7	17	17.1	17.2	17.3	17.4	17.5	17.6
0	node	1	1	1	1	1	1	1	1	1	1	1	1	2	2	1	1	2	2	3	3	1	1	2	2	3	3	1	1	1	1	1	1	1	1	2	2	3	1	1	2	2	3	4	1	1	1	1	1	1	2	2	3	3	4	4	1	1	2	2	3	3	4
1	hemi	lh	rh	lh	rh	lh	rh	lh	rh	lh	rh	lh	rh	lh	rh	lh	rh	lh	rh	lh	rh	lh	rh	lh	rh	lh	rh	lh	rh	lh	rh	lh	rh	lh	rh	lh	rh	lh	lh	rh	lh	rh	rh	rh	lh	rh	lh	rh	lh	rh	lh	rh	lh	rh	lh	rh	lh	rh	lh	rh	lh	rh	lh
2	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN
3	0	56.05574417114258	92.03103637695312	3.391575574874878	38.65968322753906	26.203819274902344	-49.71556854248047	47.4610366821289	26.746612548828125	-35.898860931396484	-1.8891807794570925	5.898688316345215	-43.69232177734375	-47.66426467895508	12.2841215133667	1.5665380954742432	-13.042585372924805	-1.8552596569061282	-39.80590057373047	-30.831512451171875	-61.13700866699219	-25.82785606384277	39.02416229248047	-29.97164535522461	-6.1323723793029785	-56.75698852539063	0.2101360559463501	-33.01984405517578	2.9784927368164062	-8.327313423156737	15.077152252197266	-10.35627269744873	18.01881599426269	-63.29214477539063	-75.9951171875	-35.44591522216797	-99.3927230834961	-73.01741790771484	-18.968013763427734	14.880836486816404	-47.75459671020508	14.73847484588623	-16.853010177612305	-34.217819213867195	-66.33069610595703	-5.723308563232423	-32.08142852783203	-76.85454559326172	13.468185424804688	68.45629119873047	19.31100845336914	30.17892837524414	60.526405334472656	0.6079040169715881	-70.27054595947266	77.36577606201172	-21.73455047607422	1.0282527208328247	7.7917842864990225	68.90372467041016	-10.520872116088867	120.49046325683594	-39.686431884765625
4	1	55.5472526550293	43.6900749206543	-65.49598693847656	-13.974522590637207	-28.27496337890625	-39.05012893676758	-1.2106596231460571	-19.012897491455078	19.568010330200195	15.902982711791992	-23.231822967529297	-10.745866775512695	10.269545555114746	31.27583122253418	-26.30948829650879	-18.0770263671875	-10.259323120117188	-43.488677978515625	-63.96562957763672	47.78985595703125	-7.910674571990968	37.951271057128906	-9.677253723144533	-52.37350845336914	6.007475852966309	9.637691497802734	7.8559889793396	-1.527979016304016	6.175285816192628	-16.031373977661133	5.727298259735107	72.07283020019531	-40.54705810546875	-38.19401168823242	-56.60818481445313	-98.99261474609376	-82.66967010498047	-64.5064697265625	4.3486294746398935	-84.35491943359375	23.79228210449219	8.927006721496582	-19.73240089416504	25.67934989929199	22.786357879638672	-13.500933647155762	-12.818994522094727	58.72330093383789	73.05491638183594	72.22550201416016	89.64704895019531	73.12434387207031	57.49507141113281	-76.39321899414062	127.26136016845705	-13.035799026489258	46.3818244934082	-15.752449989318848	31.00033187866211	-39.607521057128906	24.76401138305664	-36.7710075378418

Dataset:  car_crashes
total	speeding	alcohol	not_distracted	no_previous	ins_premium	ins_losses	abbrev
0	18.8	7.332	5.640	18.048	15.040	784.55	145.08	AL
1	18.1	7.421	4.525	16.290	17.014	1053.48	133.93	AK
2	18.6	6.510	5.208	15.624	17.856	899.47	110.35	AZ
3	22.4	4.032	5.824	21.056	21.280	827.34	142.39	AR
4	12.0	4.200	3.360	10.920	10.680	878.41	165.63	CA

Dataset:  diamonds
carat	cut	color	clarity	depth	table	price	x	y	z
0	0.23	Ideal	E	SI2	61.5	55.0	326	3.95	3.98	2.43
1	0.21	Premium	E	SI1	59.8	61.0	326	3.89	3.84	2.31
2	0.23	Good	E	VS1	56.9	65.0	327	4.05	4.07	2.31
3	0.29	Premium	I	VS2	62.4	58.0	334	4.20	4.23	2.63
4	0.31	Good	J	SI2	63.3	58.0	335	4.34	4.35	2.75

Dataset:  dots
align	choice	time	coherence	firing_rate
0	dots	T1	-80	0.0	33.189967
1	dots	T1	-80	3.2	31.691726
2	dots	T1	-80	6.4	34.279840
3	dots	T1	-80	12.8	32.631874
4	dots	T1	-80	25.6	35.060487

Dataset:  exercise
Unnamed: 0	id	diet	pulse	time	kind
0	0	1	low fat	85	1 min	rest
1	1	1	low fat	85	15 min	rest
2	2	1	low fat	88	30 min	rest
3	3	2	low fat	90	1 min	rest
4	4	2	low fat	92	15 min	rest

Dataset:  flights
year	month	passengers
0	1949	January	112
1	1949	February	118
2	1949	March	132
3	1949	April	129
4	1949	May	121

Dataset:  fmri
subject	timepoint	event	region	signal
0	s13	18	stim	parietal	-0.017552
1	s5	14	stim	parietal	-0.080883
2	s12	18	stim	parietal	-0.081033
3	s11	18	stim	parietal	-0.046134
4	s10	18	stim	parietal	-0.037970

Dataset:  gammas
timepoint	ROI	subject	BOLD signal
0	0.0	IPS	0	0.513433
1	0.0	IPS	1	-0.414368
2	0.0	IPS	2	0.214695
3	0.0	IPS	3	0.814809
4	0.0	IPS	4	-0.894992

Dataset:  geyser
duration	waiting	kind
0	3.600	79	long
1	1.800	54	short
2	3.333	74	long
3	2.283	62	short
4	4.533	85	long

Dataset:  iris
sepal_length	sepal_width	petal_length	petal_width	species
0	5.1	3.5	1.4	0.2	setosa
1	4.9	3.0	1.4	0.2	setosa
2	4.7	3.2	1.3	0.2	setosa
3	4.6	3.1	1.5	0.2	setosa
4	5.0	3.6	1.4	0.2	setosa

Dataset:  mpg
mpg	cylinders	displacement	horsepower	weight	acceleration	model_year	origin	name
0	18.0	8	307.0	130.0	3504	12.0	70	usa	chevrolet chevelle malibu
1	15.0	8	350.0	165.0	3693	11.5	70	usa	buick skylark 320
2	18.0	8	318.0	150.0	3436	11.0	70	usa	plymouth satellite
3	16.0	8	304.0	150.0	3433	12.0	70	usa	amc rebel sst
4	17.0	8	302.0	140.0	3449	10.5	70	usa	ford torino

Dataset:  penguins
species	island	culmen_length_mm	culmen_depth_mm	flipper_length_mm	body_mass_g	sex
0	Adelie	Torgersen	39.1	18.7	181.0	3750.0	MALE
1	Adelie	Torgersen	39.5	17.4	186.0	3800.0	FEMALE
2	Adelie	Torgersen	40.3	18.0	195.0	3250.0	FEMALE
3	Adelie	Torgersen	NaN	NaN	NaN	NaN	NaN
4	Adelie	Torgersen	36.7	19.3	193.0	3450.0	FEMALE

Dataset:  planets
method	number	orbital_period	mass	distance	year
0	Radial Velocity	1	269.300	7.10	77.40	2006
1	Radial Velocity	1	874.774	2.21	56.95	2008
2	Radial Velocity	1	763.000	2.60	19.84	2011
3	Radial Velocity	1	326.030	19.40	110.62	2007
4	Radial Velocity	1	516.220	10.50	119.47	2009

Dataset:  tips
total_bill	tip	sex	smoker	day	time	size
0	16.99	1.01	Female	No	Sun	Dinner	2
1	10.34	1.66	Male	No	Sun	Dinner	3
2	21.01	3.50	Male	No	Sun	Dinner	3
3	23.68	3.31	Male	No	Sun	Dinner	2
4	24.59	3.61	Female	No	Sun	Dinner	4

Dataset:  titanic
survived	pclass	sex	age	sibsp	parch	fare	embarked	class	who	adult_male	deck	embark_town	alive	alone
0	0	3	male	22.0	1	0	7.2500	S	Third	man	True	NaN	Southampton	no	False
1	1	1	female	38.0	1	0	71.2833	C	First	woman	False	C	Cherbourg	yes	False
2	1	3	female	26.0	0	0	7.9250	S	Third	woman	False	NaN	Southampton	yes	True
3	1	1	female	35.0	1	0	53.1000	S	First	woman	False	C	Southampton	yes	False
4	0	3	male	35.0	0	0	8.0500	S	Third	man	True	NaN	Southampton	no	True

```
