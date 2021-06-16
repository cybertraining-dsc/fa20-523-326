---
date: 2021-03-15
title: Analysis of Future of Buffalo Breeds and Milk Production Growth in India
linkTitle: Milk Production
tags: ["project", "ai", "environment", "finance"]
description: "Water buffalo (**Bubalus bubalis**) is also called *Domestic Water Buffalo* or *Asian Water Buffalo*. It is large bovid originating in Indian subcontinent, Southeast Asia, and China and today found in other regions of world - Europe, Australia, North America, South America and some African countries. There are two extant types recognized based on morphological and behavioral criteria: 1. River Buffalo - Mostly found in Indian subcontinent and further west to the Balkans, Egypt, and Italy. 2. Swamp Buffalo - Found from west of Assam through Southeast Asia to the Yangtze valley of China in the east. India is the largest milk producer and consumer compared to other countries in the world and stands unique in terms of the largest share of milk being produced coming from buffaloes. The aim of this academic project is to study the livestock census data of buffalo breeds in India and their milk production using Empirical Benchmarking analysis method at state level. Looking at the small sample of data, our analysis indicates that we have been seeing increasing trends in past few years in livestock and milk production but there are considerable opportunities to increase production using combined interventions."
author: Gangaprasad Shahapurkar
resources:
- src: "**.{png,jpg}"
  title: "Image #:counter"
---

# 

[![Check Report](https://github.com/cybertraining-dsc/fa20-523-326/workflows/Check%20Report/badge.svg)](https://github.com/cybertraining-dsc/fa20-523-326/actions)
[![Status](https://github.com/cybertraining-dsc/fa20-523-326/workflows/Status/badge.svg)](https://github.com/cybertraining-dsc/fa20-523-326/actions)
Status: final, Type: Project


Gangaprasad Shahapurkar, fa20-523-326, [Edit](https://github.com/cybertraining-dsc/fa20-523-326/blob/main/project/project.md) [Python Notebook](https://github.com/cybertraining-dsc/fa20-523-326/blob/main/project/code/project.ipynb)

{{% pageinfo %}}

## Abstract

Water buffalo (**Bubalus bubalis**) is also called *Domestic Water Buffalo* or *Asian Water Buffalo*. It is large bovid originating in Indian subcontinent, Southeast Asia, and China and today found in other regions of world - Europe, Australia, North America, South America and some African countries. There are two extant types recognized based on morphological and behavioral criteria:

1. River Buffalo - Mostly found in Indian subcontinent and further west to the Balkans, Egypt, and Italy
2. Swamp Buffalo - Found from west of Assam through Southeast Asia to the Yangtze valley of China in the east

India is the largest milk producer and consumer compared to other countries in the world and stands unique in terms of the largest share of milk being produced coming from buffaloes. The aim of this academic project is to study the livestock census data of buffalo breeds in India and their milk production using Empirical Benchmarking analysis method at state level. Looking at the small sample of data, our analysis indicates that we have been seeing increasing trends in past few years in livestock and milk production but there are considerable opportunities to increase production using combined interventions.

Contents

{{< table_of_contents >}}

{{% /pageinfo %}}


**Keywords:** hid 326, i532, buffalo, milk production, livestock, benchmarking, in-milk yield, agriculture, india, analysis

## 1. Introduction

Indian agriculture sector has been playing a vital role in overall contribution to Indian economy. Most of the rural community in the nation still make their livelihood on dairy farming or agriculture farming. Dairy farming itself has been on its progressive stage from past few years and it is contributing to almost more than 25% of agriculture Gross Domestic Product (GDP) [^3]. Livestock rearing has been integral part of the nation's rural community and this sector is leveraging the economy in a big way considering the growth seen. It not only provides food, income, employment but also plays major role in life of farmers. It also does other contributions to the overall rural development of the nation. The output of livestock rearing such as milk, egg, meat, and wool provides everyday income to the farmers on daily basis, it provides nutrition to consumers and indirectly it helps in contributing to the overall economy and socio-economic development of the country.

The world buffalo population is estimated at 185.29 million, spread in some 42 countries, of which 179.75 million (97%) are in Asia (Source: Fao.org/stat 2008). Hence major share of buffalo milk production in world comes from Asia (see Figure 1). India has 105.1 million and they comprise approximately 56.7 percent of the total world buffalo population. During the last 10 years, the world buffalo population increased by approximately 1.49% annually, by 1.53% in India, 1.45% in Asia and 2.67% in the rest of the world. Figure 1 shows worldwide share of milk production from buffalo breed. Figure 2 highlights percentage contribution of Asia including other top 2 contributors to world milk production.

![Milk Production World](https://github.com/cybertraining-dsc/fa20-523-326/raw/main/project/images/milk_production_world.png)

**Figure 1:** Production of Milk, whole fresh buffalo in World + (Total), Average 2013 - 2018 [^17]

![Milk Production Share](https://github.com/cybertraining-dsc/fa20-523-326/raw/main/project/images/milk_production_by_region.png)

**Figure 2:** Production share of Milk, whole fresh buffalo by region, Average 2013 - 2018 [^17]

## 2. Background Research and Previous Work

Production of milk and meat from buffaloes in Asian countries over the last decades has shown a varying pattern: in countries such as India, Sri Lanka, Pakistan and China. Buffaloes are known to be better at converting poor-quality roughage into milk and meat. They are reported to have 5% higher digestibility of crude fibre than high-yielding cows; and a 4% to 5% higher efficiency of utilization of metabolic energy for milk production [^5], [^7].

After studying literatures and researches it was noticed that there has been some research around to quantify livestock yield gaps. There is no standard methodology, but multiple methods were combined for research. Researchers were able to calculate relative yield gaps for the dairy production in India and Ethiopia [^20]. There was analysis based on attainable yields using Empirical Benchmarking, and Stochastic Frontier Analysis to evaluate possible interventions for increasing production (household modelling). It was noticed that large yield gaps exist for dairy production in both countries, and packages of interventions are required to bridge these gaps rather than single interventions. Part of the research was borrowed to analyze the limited dataset chosen as part of this project.

## 3. Choice of Datasets

Number of online literatures and datasets were checked to find out suitable dataset required for this project analysis. Below dataset were found promising:

1. [DAHD Data](https://dahd.nic.in/about-us/divisions/statistics) [^6], [^14], [^15], [^16] (**20th India Livestock Census Data**)

The Animal Husbandry Statistics Division of the Department of Animal Husbandry & Dairying Division (DAHD) is responsible for the generation of animal husbandry statistics through the schemes of livestock census and integrated sample surveys [^3]. Survey is defined by Indian Agriculture Statistics Research Institute (IASRI) [^18]. This is the only scheme through which considerable data, particularly on the production estimate of major livestock products, is being generated for policy formulation in the livestock sector. It is mandate for this division to

-   Conduct quinquennial livestock census
-   Conduct annual sample survey through integrated sample survey
-   Publish annual production estimates of milk, eggs, meat, wool and other related animal husbandry statistics based on survey

2. [FAO Data](http://www.fao.org/faostat/en/#data) [^4], [^17]

Food and Agriculture Organization (FAO) of United Nation publishes worldwide data on the aspects of dairy farming which can also be visualized online with the options provided. Some of the data from this source was used to extract useful summary needed in analysis.

3. [UIDAI Data] (https://uidai.gov.in) [^21]

Unique Identification Authority of India (UIDAI) was created with the objective to issue Unique Identification numbers (UID), named as **Aadhaar**, to all residents of India. Projected population data of 2020 was extracted from this source. 

In addition to above, other demographics information such as area of each state, district count was extracted from OpenStreetMap [^22]. Agricultural zone information was extracted from report of Food and Nutrition Security Analysis, India, 2019 [^23].

## 4. Methodology

### 4.1 Software Components

This project has been implemented in Python 3.7 version. Jupyter Notebook application was used to develop the code and produce a notebook document. Jupyter notebook is a Client-Server architecture-based application which allows modification and execution of code through web browser. Jupyter notebook can be installed locally and accessed through localhost browser or it can be installed on a remote machine and accessed via internet [^10], [^11].

Following python libraries were used in overall code development. Before running the code, one must make sure that these libraries are installed.

- **Pandas** This is a high performance and easy to use library. It was used for data cleaning, data analysis, & data preparation.
- **NumPy** NumPy is python core library used for scientific computing. Some of the basic functions were used in this project.
- **Matplotlib** This is a comprehensive library used for static, animated and interactive visualization.
- **OS** This is another standard library of Python which provides miscellaneous operating system interface functions.
- **Scikit-learn (Sklearn)**  Robust library that provides efficient tools for machine learning and statistical modelling.
- **Seaborn** Python data visualization library based on matplotlib.


### 4.2 Data Processing

The raw data retrieved from various sources was in excel or report format. The data was pre-processed and stored back in csv format for the purpose of this project and to easily process it. This dataset was further processed through various stages via EDA, feature engineering and modelling.

#### 4.2.1 EDA 

Preprocessed dataset selected for this analysis contained information at the state level. There were two seperate pre-processed dataset used.  Below was the nature of the attributes in the main dataset which had buffalo information:

- **State Name:** Name of each state in India. One record for each state.
- **Buffalo count:** Total number of male and female buffaloes. Data recorded for 14 types of buffalo breeds. One attribute for each type of female and male breeds.
- **In Milk animals:** Number of In-Milk animals per state (figures in 000 no's) recorded each year from 2013 to 2019. One attribute per year
- **Yield per In-Milk animal:** Yield per In-Milk animals per state (figures in kg/day) recorded each year from 2013 to 2019. One attribute per year.
- **Milk production:** - Milk production per state (figures in 000 tones) recorded each year from 2013 to 2019. One attribute per year.

Below was the nature of the attributes in the secondary dataset which had demographic information:

- **Geographic information:** features captured at state level where each feature represented - projected population of 2020, total districts in each state, total villages in each state, official area of each state in square kilometer. 
- **Climatic information:** One of attribute for each zone highlighted in Table 1

**Table 1:** Agro climatic regions in India

| Zones   | Agro-Climatic Regions    | States |
|---------|--------------------------|--------|
| Zone 1 | Western Himalayan Region | Jammu and Kashmir, Himachal Pradesh, Uttarakhand |
| Zone 2 | Eastern Himalayan Region | Assam, Sikkim, West Bengal, Manipur, Mizoram, Andhra Pradesh, Meghalaya, Tripura |
| Zone 3 | Lower Gangetic Plains Region | West Bengal |
| Zone 4 | Middle Gangetic Plains Region | Uttar Pradesh, Bihar, Jharkhand |
| Zone 5 | Upper Gangetic Plains Region | Uttar Pradesh |
| Zone 6 | Trans-Gangetic Plains Region | Punjab, Haryana, Delhi and Rajasthan |
| Zone 7 | Eastern Plateau and Hills Region | Maharashtra, Chhattisgarh, Jharkhand, Orissa and West Bengal |
| Zone 8 | Central Plateau and Hills Region | Madhya Pradesh, Rajasthan, Uttar Pradesh, Chhattisgarh |
| Zone 9 | Western Plateau and Hills Region | Maharashtra, Madhya Pradesh, Chhattisgarh and Rajasthan |
| Zone 10 | Southern Plateau and Hills Region | Andhra Pradesh, Karnataka, Tamil Nadu, Telangana, Chhattisgarh |
| Zone 11 | East Coast Plains and Hills Region | Orissa, Andhra Pradesh, Tamil Nadu and Pondicherry |
| Zone 12 | West Coast Plains and Ghat Region | Tamil Nadu, Kerala, Goa, Karnataka, Maharashtra, Gujarat |
| Zone 13 | Gujarat Plains and Hills Region | Gujarat, Madhya Pradesh, Rajasthan, Maharashtra |
| Zone 14 | Western Dry Region | Rajasthan |
| Zone 15 | The Islands Region | Andaman and Nicobar, Lakshadweep |

Figure 3 shows top 10 states from livestock census having total number of buffalo counts. Uttar Pradesh was the state which reported a greater number of buffaloes compared to any other states in the country.

![Milk Production Share](https://github.com/cybertraining-dsc/fa20-523-326/raw/main/project/images/top10states.png)

**Figure 3:** Top 10 state by buffalo counts

There were greater number of female buffaloes reported in country (80%) compared to male buffalo breeds.

![Milk Production Share](https://github.com/cybertraining-dsc/fa20-523-326/raw/main/project/images/buffaloshare.png)

**Figure 4:** Buffalo breeds ratio by male and female 

#### 4.2.2 Feature Engineering

Murrah buffalo shown in Figure 5 is the most productive and globally famous breed [^19], [^1]. This breed is resistant to diseases and can adjust to various Indian climate conditions.

![Murrah buffalo](https://github.com/cybertraining-dsc/fa20-523-326/raw/main/project/images/murrah_buffalo.jpeg)

**Figure 5:** Murrah buffalo (Bubalus bubalis), globally famous local breed of Haryana, were exported to many nations [^12], [^13]

In feature engineering multiple attributes were derived needed for modelling or during analysis. Table 2 shows percentage share of Murrah buffalo breed in top 10 states having highest number of total buffaloes. Though Uttar Pradesh was top state in India in terms of total number of buffaloes but percentage share of Murrah buffalo was more in state of Punjab.

**Table 2:** Murrah buffalo percent share in top 10 state with buffalo count

| State Name | Murrah Buffalo Count | Total Buffalo Count | % Murrah Breed |
|------------|----------------------|---------------------|----------------|
| UTTAR PRADESH |	20110852 | 30625334 | 65.67 |
| RAJASTHAN | 6448563 | 12976095 | 49.70 |
| ANDHRA PRADESH | 5227270 | 10622790 | 49.21 |
| HARYANA | 5011145 | 6085312 | 82.35 |
| PUNJAB | 4116508 | 5159734 | 79.78 |
| BIHAR | 2419952 | 7567233 | 31.98 |
| MADHYA PRADESH | 1446078 | 8187989 | 17.66 | 
| MAHARASHTRA | 986981 | 5594392 | 17.64 |
| TAMIL NADU | 435634 | 780431 | 55.82 |
| UTTARAKHAND | 378917 | 987775 | 38.36 |

Survey dataset had three primary attributes reported at the state level. Data reported from 2013 to 2019 for in-milk animals, yield per in-milk animals and milk production per state were averaged for analysis purpose. Total number of buffaloes per breed type were calculated from the data provided in the dataset. Following list of breeds were identified from dataset [^2].

- Banni
- Bhadawari
- Chilika
- Jaffarabadi
- Kalahandi
- Marathwadi
- Mehsana
- Murrah
- Nagpuri
- Nili Ravi
- Non-Descript
- Pandharpuri
- Surti
- Toda

Data showed that Uttar Pradesh had highest average milk production with in the top 10 states whereas Punjab state had highest average yield per in-milk animals. Figure 6 shows the share of top 3 breeds in both the state. Common attribute seen between two states was highest number of Murrah breed buffaloes compared to other breeds. 

![TOP TWO States](https://github.com/cybertraining-dsc/fa20-523-326/raw/main/project/images/punjab_up_state.png)

**Figure 6:** Top 3 types of buffalo breeds of Uttar Pradesh and Punjab


### 4.3 Modelling

#### 4.3.1 Data Preperation

Data from main dataset and supplementary dataset which was demographics data was merged into one dataset. This dataset was not labelled and it was small dataset. We considered average milk production as our target label for analysis. The rest of the features were divided based on categorical and numerical nature. Our dataset did not had any categorical features except state name which was used as index column so no futher processing was considered for this attribute. All the features were of numerical nature and all the data points were not on same scale. Hence datapoints were normalized for further processing.

#### 4.3.2 Empirical Benchmarking Model

There are two dominant approach of economic modelling to estimate the production behavior - Empirical Benchmarking and Stochastic Frontier Analysis [^8], [^9]. Empirical Benchmarking is simple modelling method, and it is one of the two dominant approach. This method was used to analyze past 6 years of data points available in the livestock dataset. In this approach milk production data of past 6 years was averaged. Top 10 states with most milk production reported were compared with average of the whole sample. The problem analyzed as part of this project was relatively small. The comparison did not consider all possible characteristics for modelling. 

Correlation of target variable with various demographics features available in the dataset was calculated. Table 3 and Table 4 shows the positive and negative coorelation with target variable average milk production respectively. We noticed from Table 3 that average milk production contribution was getting affected by number of in-milk animals reported in the particular year census data and their was also factor of climatic conditions affecting the milk production. India is divided into 15 Agro climate zones. Agro zone 6 is Trans-Gangetic Plains region. Indian states Chandigarh, Delhi, Haryana, Punjab, Rajasthan (some parts) falls under this zone. Agricultural development has shown phenomenal growth in overall productivity and in providing better environment for dairy farming in this zone [^24].

**Table 3:** Positive coorelation of target with demographics features

| Feature | % |
|---------|---|
| avg_milk_production | 1.00 |
| avg_in_milk | 0.95 |
| total_female| 0.90 |
| total_male | 0.71 |
| agro_climatic_zone6 | 0.50 | 

**Table 4:** Negative coorelation of target with demographics features

| Feature | % |
|---------|---|
| official_area_sqkm | -0.17 |
| agro_climatic_zone2 | -0.19 |
| avg_yield_in_milk | -0.23 |
| district_count | -0.34 |
| proj_population_2020 | -0.94 |

#### 4.3.3 Linear Regression

Our target variable considered was a continous variable. In an attempt to perform dimension reduction, Principal Component Analysis (PCA) was applied to available limited dataset. In the example presented, an pipeline was constructed that had dimension reduction followed by Linear regression classifier. Grid search cross validation was applied (GridSearchCV) to find the best parameters and score. Linear regression was applied with default parameter settings whereas parameter range was passed for PCA. Below is snapshot of pipeline implemented.

```python
# Define a pipeline to search for the best combination of PCA truncation
# and classifier regularization.
pca = PCA()

# Linear Regression without parameters
linear = LinearRegression()

full_pipeline_with_predictor = Pipeline([
        ("preparation", num_pipeline),
        ("pca",pca),
        ("linear", linear)
    ])

# Parameters of pipelines:
param_grid = {
    'pca__n_components': [5, 15, 30, 45, 64]
}
```

## 5. Results

Based on simple Empirical Benchmarking Analysis and trends noticed in data it appears that it is possible to increase production past currently attainable yields (see Figure 7). The current scale of the yield does indicate that, leading states have best breeds of buffaloes. Different methods of analyzing yield gaps can be combined to give estimates of attainable yields. It will also help to evaluate possible interventions to increase production and profits.

![TOP 10 States](https://github.com/cybertraining-dsc/fa20-523-326/raw/main/project/images/avgmilkproduction.png)

**Figure 7:** Average milk production in top 10 state with benchmark

The best parameter came out of the pipeline implemented are highlighted here. The results were not promising due the limited dataset so further experimentation was not attempted, but one thing was noticed that cross validated score came out to 0.28 and dimension reduction to 5 components.

```python
Best parameter (CV score=0.282):
{'pca__n_components': 5}

PCA(copy=True, iterated_power='auto', n_components=None, random_state=None,
    svd_solver='auto', tol=0.0, whiten=False) 
```

![COV Analysis](https://github.com/cybertraining-dsc/fa20-523-326/raw/main/project/images/covariance.png)

**Figure 8:** Covariance Heat Map

We were able to calculate correlation of census data with other socioeconomic factors like population information, climate information (see Figure 8). The biggest probable limitation here was availability of good quality data. It would have been possible to conduct the analysis at finer level if more granular level data would have been available. Our analysis had to be done state level rather than at district level or specific area.

## 6. Conclusion

The analysis done above with the limited dataset showed that there are considerable gaps in the average yield per in-milk buffalo of state Punjab and Uttar Pradesh, compared to other states in top 10 list. These states have larger share of Murrah breed buffaloes. Based on the data trends it appears that it is possible to increase the production past current attenable numbers. However, this would need to combine different methods and multiple strategies.

## 7. Acknowledgements

The author would like to thank Dr. Gregor von Laszewski, Dr. Geoffrey Fox, and the associate instructors in the *FA20-BL-ENGR-E534-11530: Big Data Applications* course (offered in the Fall 2020 semester at Indiana University, Bloomington) for their continued assistance and suggestions with regard to exploring this idea and also for their aid with preparing the various drafts of this article.

## 8. References

[^1]: Water Buffalo. Accessed: Oct 26, 2020. [Online]. Available: <https://en.wikipedia.org/wiki/Water_buffalo> 

[^2]: List of Water Buffalo Breeds. Accessed: Oct 26, 2020. [Online]. Available: <https://en.wikipedia.org/wiki/List_of_water_buffalo_breeds>

[^3]: PIB Delhi. (2019). Department of Animal Husbandry & Dairying releases 20th Livestock Census, 16 (Oct 2019).
<https://pib.gov.in/PressReleasePage.aspx?PRID=1588304>

[^4]: F.A.O. (2008). Food and Agriculture Organization. Rome Italy. STAT <http://database.www.fao.org>

[^5]: Mudgal, V.D. (1988). "Proc. of the Second World Buffalo Congress, New Delhi, India", 12 to 17 Dec.:454.

[^6]: Department of Animal Husbandry and Dairying. <http://dahd.nic.in/about-us/divisions/statistics>

[^7]: Alessandro, Nardone. (2010). "Buffalo Production and Research". Italian Journal of Animal Science. 5. 10.4081/ijas.2006.203.

[^8]: Bogetoft P., Otto L. (2011) Stochastic Frontier Analysis SFA. In: Benchmarking with DEA, SFA, and R. International Series in Operations Research & Management Science, vol 157. Springer, New York, NY. <https://doi.org/10.1007/978-1-4419-7961-2_7>

[^9]: Aigner, Dennis (07/1977). "Formulation and estimation of stochastic frontier production function models". Journal of econometrics (0304-4076), 6 (1), p. 21. <https://doi.org/10.1016/0304-4076(77)90052-5>

[^10]: Corey Schafer. Jupyter Notebook Tutorial: Introduction, Setup, and Walkthrough. (Sep. 22, 2016). Accessed: Nov. 07, 2020. [Online Video]. Available: <https://www.youtube.com/watch?v=HW29067qVWk>

[^11]: *The Jupyter Notebook*. Jupyter Team. Accessed: Nov. 07, 2020. [Online]. Available: <https://jupyter-notebook.readthedocs.io/en/stable/notebook.html>

[^12]: Kleomarlo. Own work, CC BY-SA 3.0. [Online]. Available: <https://commons.wikimedia.org/w/index.php?curid=4349862>

[^13]: ICAR - Central Institute for Research on Buffaloes. <https://cirb.res.in/>

[^14]: Department of Animal Husbandry and Dairying, Accessed: Oct. 2020, <http://dadf.gov.in/sites/default/filess/20th%20Livestock%20census-2019%20All%20India%20Report.pdf>

[^15]: Department of Animal Husbandry and Dairying, Accessed: Oct. 2020, <http://dadf.gov.in/sites/default/filess/Village%20and%20Ward%20Level%20Data%20%5BMale%20%26%20Female%5D.xlsx>

[^16]: Department of Animal Husbandry and Dairying, Accessed: Oct. 2020, <http://dadf.gov.in/sites/default/filess/District-wise%20buffalo%20population%202019_0.pdf>

[^17]: FAO - Food and Agriculture Organization of United Nation, Accessed: Nov. 2020, <http://www.fao.org/faostat/en/#data>

[^18]: IASRI - Indian Agriculture Statistics Research Institute. <https://iasri.icar.gov.in/>

[^19]: Bharathi Dairy Farm. <http://www.bharathidairyfarm.com/about-murrah.php>

[^20]: Mayberry, Dianne (07/2017). Yield gap analyses to estimate attainable bovine milk yields and evaluate options to increase production in Ethiopia and India. Agricultural systems (0308-521X), 155 , p. 43.

[^21]: Unique Identification Authority of India, Accessed: Nov. 2020, <https://uidai.gov.in/images/state-wise-aadhaar-saturation.pdf>

[^22]: OpenStreetMap, Accessed: Nov. 2020, <https://wiki.openstreetmap.org/wiki/Main_Page>

[^23]: Food and Nutrition Security Analysis, India, 2019, Accessed: Nov. 2020, <http://mospi.nic.in/sites/default/files/publication_reports/document%281%29.pdf>

[^24]: Farm Mechanization-Department of Agriculture and Cooperation, India, Accessed: Nov. 2020, <http://farmech.gov.in/06035-04-ACZ6-15052006.pdf>
