Documentation  
# Reference percentiles for carotid measures of subclinical atherosclerosis in children and adolescents – Data from the KiGGS study  

[**Robert Koch-Institut | RKI**](http://www.rki.de)  
Nordufer 20   
13353 Berlin   

<br>  

[**Julia Büschges**](https://orcid.org/0000-0002-5669-2427)&sup1;&sup2;, [**Angelika Schaffrath Rosario**](https://orcid.org/0000-0001-7777-8070)&sup1;, [**Giselle Sarganas Margolis**](https://orcid.org/0000-0002-6296-3174)&sup1;&sup2;, [**Karsten Königstein**](https://orcid.org/0000-0002-2994-8570)&sup2;&sup3;, **Dieter Schweizer**&#8308;, [**Arno Schmidt-Trucksäss**](https://orcid.org/0000-0002-4662-3911)&sup3;, [**Hannelore Neuhauser**](https://orcid.org/0000-0002-6605-6221)&sup1;&sup2;


&emsp;&sup1; Robert Koch Institute | Department of Epidemiology and Health Monitoring, Berlin  
&emsp;&sup2; German Centre for Cardiovascular Research (DZHK) | partner site Berlin  
&emsp;&sup3; University of Basel | Department of Sport, Exercise and Health, Division Sports and Exercise Medicine  
&emsp;&#8308; Fukuda Denshi Switzerland AG, Basel  

---

**Cite**  

Büschges J, Schaffrath Rosario A, Sarganas Margolis G, Königstein K, Schweizer D, Schmidt-Trucksäss A and Neuhauser H (**2022**): Reference percentiles for carotid measures of subclinical atherosclerosis in children and adolescents – Data from the KiGGS study. Berlin: Zenodo. [DOI:10.5281/zenodo.7048174](https://doi.org/10.5281/zenodo.7048174)  


## General information

This dataset presents reference centile data for carotid intima-media thickness as well as four carotid stiffness parameters. Further details can be found in previously published articles [[1](https://doi.org/10.1016/j.ultrasmedbio.2020.10.015), [2](https://doi.org/10.1161/hypertensionaha.121.18521)].

The reference percentiles presented in this publication are based on data from the German Health Interview and Examination Survey for Children and Adolescents 2003-2006 (KiGGS). A number of more detailed papers have been published on individual parameters [[1](https://doi.org/10.1016/10.1161/HYPERTENSIONAHA.121.18521),[2](https://doi.org/10.1161/hypertensionaha.121.18521),[3](https://doi.org/10.1016/j.ultrasmedbio.2020.10.015)]. KiGGS started as a cross-sectional study conducted between 2003 and 2006 which was based on a nationally representative sample and aimed at obtaining comprehensive data on the health of children and adolescents aged 0 to 17 years living in Germany. Detailed information on study design and conduct has been published elsewhere [[4](https://doi.org/10.1186/1471-2458-8-196)]. 11 years later, KiGGS Wave 2 (2014-2017) was conducted as an interview and examination survey. 

Carotid sonography was attempted at follow-up (KiGGS2) in all 4,798 participants of the KiGGS cohort aged 14 to 28 years. Carotid intima-media thickness (CIMT) was successfully measured in 4,709 participants. Reference centiles for the distensibility coefficient, stiffness index ß, Young's elastic modulus and Peterson's elastic modulus were computed using data on 4,305 adolescents and young adults aged 14 to 28.

## Measurement of carotid intima-media thickness

At follow-up, the distal common carotid artery was examined with high-resolution B-mode ultrasound, using a 5 to 12 MHz linear array transducer (UF—760AG, Fukuda Denshi Co. Ltd, Tokyo, Japan) in examination participants from age 14. Examinations were standardized following current recommendations [[5](https://doi.org/10.1016/j.echo.2007.11.011), [6](https://doi.org/10.1159/000343145)]. A snake algorithm together with subpixel interpolation was used to automatically detect contours of the vascular layers [[7](https://doi.org/10.1016/s0169-2607(00)00149-8)].
 Carotid intima-media thickness (CIMT) and lumen diameter (LD) were measured bilaterally on the ear-to-ear and horizontal planes over 6 heart cycles on a 10 mm segment, 10-15 mm from the carotid bulb. Over each heart cycle, up to 266 point-to-point measurements were obtained. Using software-based ECG-gated real-time quality control algorithm, valid heart cycles were identified. Successful CIMT measurement was defined as ≥1 valid CIMT value over ≥2 valid heart cycles in ≥1 plane. The final CIMT was calculated as a mean value from all valid measurements. A detailed description of the sonographic procedure, automatic detection, real-time, and postprocedural quality control is provided elsewhere [[1](https://doi.org/10.1016/j.ultrasmedbio.2020.10.015)].


## Calculation of carotid stiffness

Various parameters of carotid stiffness can be computed by combining information on BP and LD as well as CIMT, namely the distensibility coefficient (DC), ß stiffness index (ß), Young's elastic modulus (YEM) and Peterson's elastic modulus (Ep). The equations used for calculating arterial stiffness can be found elsewhere [[1](https://doi.org/10.1016/j.ultrasmedbio.2020.10.015)]. An increase in Ep, YEM or β indicates increased arterial stiffness, while an increase in DC reflects increased elasticity and therefore a decrease in stiffness. Measurements of DC, Ep and YEM are given in kilopascal (1 kPa = 7.6 mmHg)


## Statistical Data analysis

As a first step, extreme values in the sample were replaced by their next neighbours counting inwards from the extreme (winsorizing). For all parameters, smoothing techniques were applied in order to balance random fluctuations in the observed data. To test the goodness of fit of the models, Q-tests [[8](https://doi.org/10.1002/sim.1692), [9](https://doi.org/10.1002/1097-0258(20001115)19:21%3C2943::aid-sim559%3E3.0.co;2-5)] and wormplots [[10](https://doi.org/10.1002/sim.746)] were applied within age groups. Percentiles for all parameters were estimated separately by sex. Sampling weights were used in all analyses to account for unequal sampling probabilities and to better represent the population structure in Germany regarding age, sex and region [[4](https://doi.org/10.1186/1471-2458-8-196)]. In the analysis of the parameters for subclinical atherosclerosis measured at follow-up, the weights also corrected for longitudinal drop-out.

To model the centiles, an extension of the LMS method for two covariates was used, namely the generalized additive models for location, scale and shape (GAMLSS) fitted with the GAMLSS package version 1.9-4 in the free statistical software R 2.8.0 ([www.cran.r-project.org](https://www.cran.r-project.org/)). In GAMLLS, the parameter L is called Nu, M is called Mu, and S is called Sigma. Either the Box-Cox-Cole-Green (with the three parameters L, M and S as described above) or the Box-Cox-Power-Exponential distribution family were used to fit the models in R.

### Calculation of additional percentiles

The data sets published here contain selected percentiles as well as the parameters M, L and S, by sex and age. For example, P90, the 90th percentile, and P95, the 95th percentile, are published. If other percentiles are required, e.g. P80, any (100α) percentile, Pα, at a given age can be calculated as:

```
Pα = M · (1 + L · S · zα)^1/L            for L ≠ 0  
Pα = M · exp(S · zα)                    for L = 0  
Pα = M · (1 + S · zα)                   for L = 1  
```

where exp() is the exponential function and zα the α-quantile of a standard normal distribution, which can be found in quantile tables or calculated within the common statistical packages or spreadsheet applications. Note that extreme percepercentilesntiles (say lower than P1 or higher than P99) are subject to larger modelling uncertainties.

### Calculation of z-scores and  for an individual data point

The other way around, a given value x of an indicator can be transformed into the so-called z-score or standard deviation score (SDS). The z-score transforms the original values to the scale of a standard normal distribution for each age. The z-scores are thus age- and sex-standardized values of the original indicator. A z-score of 1 means that a value is 1 standard deviation above the median (recall that about 68% of the values of a standard normal distribution are within ± 1 standard deviation of the median, so a z-score of 1 corresponds to the 84th percentile). The z-scores correspond to zα in the formula above. They can be calculated by applying the following formula:

```
z = [(x/M)^L – 1] / (S · L)             for L ≠ 0   
z = 1/S · log (x/M)                    for L = 0  
z = 1/S · [(x/M) – 1]                  for L = 1  
```

where log() denotes the natural logarithm. The z-score can  be transformed into a percentile P via:

```
P = 100 · Φ (z)
```

Here, Φ() is the cumulative probability function of a standard normal distribution, which can be found in tables or calculated in a statistics package or spreadsheet application. Again, extreme z-scores and percentiles are subject to larger modelling uncertainties.

### Percentile estimation for carotid measures of subclinical atherosclerosis

CIMT percentiles were modelled as a function of age and height simultaneously. The parameters L, M and S were first modelled by natural cubic splines. However, often the model could be simplified to a parametric (linear or quadratic) formula. Thus, the values in the reference data sets published here can be generated according to the following regression formulas. These formulas can also be used to generate values for L, M and S for combinations of age and height not included in the reference data sets.

CIMT was modelled by age and height in cm. The values in the reference data sets can be generated according to the following regression formulas:

#### CIMT in males
```
L = 0.0477  
M = exp {−0.85287 + 0.78411 · age + 0.3977 · age² + 0.00141 · height}  
S = exp {−2.58624 + 0.0104 · age}  
```

#### CIMT in females
```
L = - 0.0578  
M = exp {−0.75941 + 0.00563 · age + 0.55674 · height – 0.39676 · height²}  
S = 0.0876
```

### Indicators of carotid stiffness

Percentiles for measures of carotid stiffness were calculated with GAMLSS as well. Percentiles for females were modelled using age only, while percentiles for males were modelled as a function of both age and height. Either the Box-Cox-Cole-Green (with the three parameters L, M and S as described above) or the Box-Cox-Power-Exponential distribution family (with an additional parameter Tau which describes whether the distribution is heavy-tailed) were used to fit the models. At the present time, no formulae are available for these models. A detailed description of the estimation of these models has been previously published [2].

## Structure and content of this data set 

The data set contains aggregated data, namely the results of the GAMLSS model for each indicator. The data set contains:

- reference percentile data for all indicators
- LMS data for CIMT
- Data set documentation
- Metadata for export to other repositories
- License information in German und English

### Reference percentile data

For selected values of age, height and stratified by sex, the reference percentile data contain the values of selected percentiles as predicted by the GAMLSS model.

The data is contained in the following files:

> Percentiles/KiGGS2-2014-2017_Percentiles_Subclinical_Atherosclerosis.csv
> Percentiles/KiGGS2-2014-2017_Percentiles_Subclinical_Atherosclerosis.xlsx

The naming scheme of the files, “KiGGSx-YYYY-YYYY", indicates the respective KiGGS wave "x" and the respective data collection years “YYYY-YYYY”. 

#### Variables

| Variable | Type | Expressions | Description | 
| -------- | -------- | -------- | -------- | 
| indicator | string  | `cimt`, `dc`, `Ep`, `yem`, `beta` | KiGGS indicator meassured |
| sex   	| string  | `f`: female <br> `m`: male| Sex  |
| ageY		| float   |          | Age in years |
| height 	| integer |          | Height in cm |
| P$   		| float  | 			 | KiGGS $% reference percentile, specific on modeled variables  |

#### Data formats 

In order to meet the community's needs, the data is provided in two formats, .csv and .xlsx. The .csv file is formatted according to the international standard:

- Character set: UTF-8
- .csv separator: comma “,”

The .xlsx file provides a German decimal separator for the reference data sets.

### Statistical core data

The Statistical core datafiles contain the values of the three parameters L, M and S estimated in the GAMLSS models. All parameters are provided for selected values of age (and height) and stratified by sex.

These data can be used for calculating additional percentiles not included in the reference percentile data sets. The necessary formula are described in Section: Statistical Data analysis.

The data is contained in the following files:

> KiGGS2-2014-2017_GAMLSS_Subclinical_Atherosclerosis.csv
> KiGGS2-2014-2017_GAMLSS_Subclinical_Atherosclerosis.xlsx

The naming scheme of the files, “KiGGSx-YYYY-YYYY”, indicates the respective data collection years “YYYY-YYYY”. 

#### Variables

| Variable | Type | Expressions | Description | 
| -------- | -------- | -------- | -------- | 
| indicator | string  | `cimt`   | KiGGS indicator measured |
| sex   	| string  | `f`: female <br> `m`: male| Sex  |
| ageY		| float   |          | Age in years |
| height 	| integer |          | Height in cm |
| mu   		| Integer  | | GAMLSS model parameter: Median (50th centile)  |
| sigma 	| Integer  | | GAMLSS model parameter: Approximate coefficient of variation|
| lambda   	| Integer  | | GAMLSS model parameter: Skewness/ Box-Cox Power Transformation|

#### Data formats 

In order to meet the community's needs, the data is provided in two formats, .csv and .xlsx. The .csv file is formatted according to the international standard:

- Character set: UTF-8
- .csv separator: comma “,”

The .xlsx file provides a German decimal separator for the reference data sets.

### Metadata

To increase findability, the provided data is described with metadata. Metadata is distributed to the corresponding platforms via GitHub Actions. A specific metadata file exists for each platform and is stored in the metadata folder: 

> [Metadata/](/Metadata/)  

Versioning and DOI assignment is done via [Zenodo.org](https://zenodo.org). The metadata provided for import into Zenodo is stored in [zenodo.json](/metadata/zenodo.json). Documentation of the individual metadata variables can be found at https://developers.zenodo.org/#representation.

> [Metadaten/zenodo.json](/Metadaten/zenodo.json)  

## Notes on continued use of these data

Open research data of the RKI are made available on [GitHub.com](http://GitHub.com/), [Zenodo.org](http://Zenodo.org/) und [Edoc.rki.de](http://Edoc.rki.de/):

- [https://github.com/robert-koch-institut](https://github.com/robert-koch-institut)
- [https://zenodo.org/communities/robertkochinstitut](https://zenodo.org/communities/robertkochinstitut)
- [https://edoc.rki.de](https://edoc.rki.de/) 

### Value of the data

- These data provide reference tables carotid measures of subclinical atherosclerosis ranging from early childhood and adolescence to young adulthood.
- These reference percentiles were derived from a large general population sample of German children and adolescents.
- These data contribute to understanding the natural development of arterial structure and function from childhood and adolescence to young adulthood.

Access restrictions apply to the raw data underlying the centile estimation. The raw data set cannot be made publicly available because informed consent from study participants did not cover public deposition of data. However, the minimal data set underlying the findings is archived in the ‘Health Monitoring’ Research Data Centre at the Robert Koch Institute (RKI) and can be accessed by researchers on reasonable request. On-site access to the data set is possible at the Secure Data Center of the RKI’s ‘Health Monitoring’ Research Data Centre. Requests should be submitted to the ‘Health Monitoring’ Research Data Centre, Robert Koch Institute, Berlin, Germany fdz@rki.de.

### License

The data set "Reference percentiles for carotid measures of subclinical atherosclerosis in children and adolescents – Data from the KiGGS study" is licensed under the [Creative Commons Attribution 4.0 International Public License | CC-BY 4.0 International](https://creativecommons.org/licenses/by/4.0/deed.en)

The data provided in the data set are freely available under the condition that the Robert Koch Institute is credited as the source. This means that any person has the right to process and to modify the data, to create derivatives of the data set and to use them for commercial or non-commercial purposes. Further information on the license can be found in the [LICENSE](https://github.com/robert-koch-institut/SARS-CoV-2_Infektionen_in_Deutschland/blob/master/LICENSE) file of the data set.


## Literature

1. Neuhauser HK, Büschges J, Schaffrath Rosario A, Schienkiewitz A, Sarganas G, Königstein K, Schweizer D, Schmidt-Trucksäss A. Carotid Intima-Media Thickness Percentiles in Adolescence and Young Adulthood and Their Association With Obesity and Hypertensive Blood Pressure in a Population Cohort. Hypertension. 2022 Jun;79(6):1167-1176. [DOI: 10.1161/HYPERTENSIONAHA.121.18521](https://doi.org/10.1016/10.1161/HYPERTENSIONAHA.121.18521).

2. Büschges J, Schaffrath Rosario A, Schienkiewitz A, Königstein K, Sarganas G, Schmidt-Trucksäss A, Neuhauser H. Vascular aging in the young: New carotid stiffness centiles and association with general and abdominal obesity - The KIGGS cohort. Atherosclerosis. 2022 Aug;355:60-67. [DOI: 10.1016/j.atherosclerosis.2022.05.003](https://doi.org/10.1016/j.atherosclerosis.2022.05.003). 

3.  Königstein K, von Schenck U, Büschges JC, Schweizer D, Vogelgesang F, Damerow S, Sarganas G, Dratva J, Schmidt-Trucksäss A, Neuhauser H. Carotid IMT and Stiffness in the KiGGS 2 National Survey: Third-Generation Measurement, Quality Algorithms and Determinants of Completeness. Ultrasound Med Biol. 2021 Feb;47(2):296-308. [DOI: 10.1016/j.ultrasmedbio.2020.10.015](https://doi.org/10.1016/j.ultrasmedbio.2020.10.015).

4.	Kurth, B.M., et al., The challenge of comprehensively mapping chil- dren's health in a nation-wide health survey: design of the German KiGGS-Study. BMC Public Health, 2008. 8: p. 196. [DOI: 10.1186/1471-2458-8-196](https://doi.org/10.1186/1471-2458-8-196)

5. Stein JH, Korcarz CE, Hurst RT, Lonn E, Kendall CB, Mohler ER, Najjar SS, Rembold CM, Post WS; American Society of Echocardiography Carotid Intima-Media Thickness Task Force. Use of carotid ultrasound to identify subclinical vascular disease and evaluate cardiovascular disease risk: a consensus statement from the American Society of Echocardiography Carotid Intima-Media Thickness Task Force. Endorsed by the Society for Vascular Medicine. J Am Soc Echocardiogr. 2008 Feb;21(2):93-111; quiz 189-90. [DOI: 10.1016/j.echo.2007.11.011](https://doi.org/10.1016/j.echo.2007.11.011).

6. Touboul PJ, Hennerici MG, Meairs S, Adams H, Amarenco P, Bornstein N, Csiba L, Desvarieux M, Ebrahim S, Hernandez Hernandez R, Jaff M, Kownator S, Naqvi T, Prati P, Rundek T, Sitzer M, Schminke U, Tardif JC, Taylor A, Vicaut E, Woo KS. Mannheim carotid intima-media thickness and plaque consensus (2004-2006-2011). An update on behalf of the advisory board of the 3rd, 4th and 5th watching the risk symposia, at the 13th, 15th and 20th European Stroke Conferences, Mannheim, Germany, 2004, Brussels, Belgium, 2006, and Hamburg, Germany, 2011. Cerebrovasc Dis. 2012;34(4):290-6. [DOI: 10.1159/000343145](https://doi.org/10.1159/000343145). 

7. Cheng DC, Schmidt-Trucksäss A, Cheng KS, Burkhardt H. Using snakes to detect the intimal and adventitial layers of the common carotid artery wall in sonographic images. Comput Methods Programs Biomed. 2002 Jan;67(1):27-37. [DOI: 10.1016/s0169-2607(00)00149-8](https://doi.org/10.1016/s0169-2607(00)00149-8).

8.	Pan, H. and T.J. Cole, A comparison of goodness of fit tests for age- related reference ranges. Stat Med, 2004. 23(11): p. 1749-65. [DOI: 10.1002/sim.1692](https://doi.org/10.1002/sim.1692) 

9.	Royston, P. and E.M. Wright, Goodness-of-fit statistics for age-specific reference intervals. Stat Med, 2000. 19(21): p. 2943-62. [ DOI: 10.1002/1097-0258(20001115)19:21<2943::aid-sim559>3.0.co;2-5](https://doi.org/10.1002/1097-0258(20001115)19:21%3C2943::aid-sim559%3E3.0.co;2-5)

10.	van Buuren, S. and M. Fredriks, Worm plot: a simple diagnostic device for modelling growth reference curves. Stat Med, 2001. 20(8): p. 1259-77. [DOI: 10.1002/sim.746](https://doi.org/10.1002/sim.746)
