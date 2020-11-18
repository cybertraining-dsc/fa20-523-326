# Analysis of Future of Buffalo Breeds and Milk Production Growth in India


[![Check Report](https://github.com/cybertraining-dsc/fa20-523-326/workflows/Check%20Report/badge.svg)](https://github.com/cybertraining-dsc/fa20-523-326/actions)


Gangaprasad Shahapurkar, fa20-523-326, [Edit](https://github.com/cybertraining-dsc/fa20-523-326/blob/main/project/project.md)

{{% pageinfo %}}

## Abstract

Water buffalo (**Bubalus bubalis**) is also called *Domestic Water Buffalo* or *Asian Water Buffalo*. It is large bovid originating in Indian subcontinent, Southeast Asia, and China and today found in other regions of world - Europe, Australia, North America, South America and some African countries. There are two extant types recognized based on morphological and behavioral criteria:

1. River Buffalo - Mostly found in Indian subcontinent and further west to the Balkans, Egypt, and Italy
2. Swamp Buffalo - Found from west of Assam through Southeast Asia to the Yangtze valley of China in the east

India is the largest milk producer and consumer compared to other countries in the world and stands unique in terms of the largest share of milk being produced coming from buffaloes. The aim of this academic project is to study the livestock census data of buffalo breeds in India and their milk production using Empirical Benchmarking analysis method at state level. Looking at the small sample of data, our analysis indicates that we have been seeing increasing trends in past few years in livestock and milk production but there are considerable opportunities to increase production using combined interventions.

Contents

{{< table_of_contents >}}

{{% /pageinfo %}}


**Keywords:** hid 326, i532, buffalo, milk production, livestock, benchmarking, in-milk yield, agriculture, India, analysis.

## 1. Introduction

Indian Agriculture sector has been playing a vital role in overall contribution to Indian Economy. Most of the rural community in the nation still make their livelihood on Dairy Farming or Agriculture Farming. Dairy Farming itself has been on its progressive stage from past few years and it is contributing to almost more than 25% of Agriculture Gross Domestic Product (GDP) [^3]. Livestock rearing has been integral part of the nation's rural community and this sector is leveraging the economy in a big way considering the growth seen. It not only provides food, income, employment but also plays major role in life of farmers. It also does other contributions to the overall rural development of the nation. The output of livestock rearing such as milk, egg, meat, and wool provides everyday income to the farmers on daily basis, it provides nutrition to consumers and indirectly it helps in contributing to the overall economy and socio-economic development of the country.

The world buffalo population is estimated at 185.29 million, spread in some 42 countries, of which 179.75 million (97%) are in Asia (Source: Fao.org/stat 2008). Hence major share of buffalo milk production in world comes from Asia (see Figure 1). India has 105.1 million and they comprise approximately 56.7 percent of the total world buffalo population. During the last 10 years, the world buffalo population increased by approximately 1.49% annually, by 1.53% in India, 1.45% in Asia and 2.67% in the rest of the world. Figure 1 shows worldwide share of milk production from buffalo breed. Figure 2 highlights percentage contribution of Asia including other top 2 contributors to world milk production.

![Milk Production World](https://github.com/cybertraining-dsc/fa20-523-326/raw/main/project/images/milk_production_world.png)

**Figure 1:** Production of Milk, whole fresh buffalo in World + (Total), Average 2013 - 2018

![Milk Production Share](https://github.com/cybertraining-dsc/fa20-523-326/raw/main/project/images/milk_production_by_region.png)

**Figure 2:** Production share of Milk, whole fresh buffalo by region, Average 2013 - 2018

## 2. Background Research and Previous Work

Production of milk and meat from buffaloes in Asian countries over the last decades has shown a varying pattern: in countries such as India, Sri Lanka, Pakistan and China. Buffaloes are known to be better at converting poor-quality roughage into milk and meat. They are reported to have 5% higher digestibility of crude fibre than high-yielding cows; and a 4% to 5% higher efficiency of utilization of metabolic energy for milk production [^5], [^7]. 

After studying literatures and researches it was noticed that there has been some research around to quantify livestock yield gaps. There is no standard methodology, but multiple methods were combined for research. Researchers were able to calculate relative yield gaps for the dairy production in India and Ethiopia [^20]. There was analysis based on attainable yields using Empirical Benchmarking and Stochastic Frontier Analysis and evaluate possible interventions to increase production (household modelling). It was noticed that large yield gaps exist for dairy production in both countries, and packages of interventions are required to bridge these gaps rather than single interventions. Part of the research was borrowed to analyze the limited dataset chosen as part of this project. 

## 3. Choice of Datasets

Number of online literatures and datasets were checked to find out suitable dataset required for this project analysis. Below dataset were found promising:

1. [DAHD Data](https://dahd.nic.in/about-us/divisions/statistics) [^6], [^14], [^15], [^16] (**20th Livestock Census Data**)

The Animal Husbandry Statistics Division of the Department of Animal Husbandry & Dairying Division (DAHD) is responsible for the generation of Animal Husbandry Statistics through the schemes of Livestock Census and Integrated Sample Surveys [^3]. Survey is defined by Indian Agriculture Statistics Research Institute (IASRI) [^18]. This is the only scheme through which considerable data, particularly on the production estimate of major livestock products, is being generated for policy formulation in the livestock sector. It is mandate for this division to

-   Conduct quinquennial livestock census
-   Conduct annual sample survey through integrated sample survey
-   Publish annual production estimates of milk, eggs, meat, wool and other related animal husbandry statistics based on survey

2. [FAO Data](http://www.fao.org/faostat/en/#data) [^4], [^17]

Food and Agriculture Organization of United Nation (FAO) publishes worldwide data on the aspects of dairy farming which can also be visualized online with the options provided. Some of the data from this source was used to extract useful summary needed in analysis.

## 4. Methodology 

### 4.1 Software Components

This project has been implemented in Python 3.7 version. Jupyter Notebook application was used to develop the code and produce a notebook document. Jupyter Notebook is a Client-Server architecture-based application which allows modification and execution of code through web browser. Jupyter Notebook can be installed locally and accessed through localhost browser or it can be installed on a remote machine and accessed via Internet [^10], [^11].     

Following python libraries were used in overall code development. Before running the code, one must make sure that these libraries are installed.

- **Pandas** This is a high performance and easy to use library. It was used for data cleaning, data analysis, & data preparation.
- **NumPy** NumPy is python core library used for scientific computing. Some of the basic functions were used in this project.
- **Matplotlib** This is a comprehensive library used for static, animated and interactive visualization. 
- **OS** This is another standard library of Python which provides miscellaneous operating system interface functions.

### 4.2 Data Processing

The raw data retrieved from the source was in excel format. The data was pre-processed and stored back in csv format for the purpose of this project and to easily process it. This dataset was further processed through various stages via EDA, feature engineering and modelling.

#### 4.2.1 EDA 

Preprocessed dataset selected for this analysis contains information at the state level. Below is the nature of the attributes in the dataset:

- **State Name:** Name of each state in India. One record for each state.
- **Buffalo count:** Total number of male and female buffaloes. Data recorded for 14 types of buffalo breeds. One attribute for each type of female and male breeds.
- **In Milk animals:** Number of In-Milk animals per state (figures in 000 no's) recorded each year from 2013 to 2019. One attribute per year
- **Yield per In-Milk animal:** Yield per In-Milk animals per state (figures in kg/day) recorded each year from 2013 to 2019. One attribute per year.
- **Milk production:** - Milk production per state (figures in 000 tones) recorded each year from 2013 to 2019. One attribute per year.

Figure 3 shows top 10 states from livestock census having total number of buffalo counts. Uttar Pradesh is the state which reported a greater number of buffalos compared to any other states in the country. 

![Milk Production Share](https://github.com/cybertraining-dsc/fa20-523-326/raw/main/project/images/top10states.png)

**Figure 3:** Top 10 state with buffalo counts compared to others

 There are a greater number of female buffalos reported in country (80%) compared to male buffalo breeds.

![Milk Production Share](https://github.com/cybertraining-dsc/fa20-523-326/raw/main/project/images/buffaloshare.png)

**Figure 4:** Percentage of Female vs Male buffalo reported

#### 4.2.2 Feature Engineering

Murrah buffalo shown in Figure 5 is the most productive and globally famous breed [^19], [^1]. This breed is resistant to diseases and can adjust to various Indian climate conditions. 

![Murrah buffalo](https://github.com/cybertraining-dsc/fa20-523-326/raw/main/project/images/murrah_buffalo.jpeg)

**Figure 5:** Murrah buffalo (Bubalus bubalis), globally famous local breed of Haryana, were exported to many nations [^12], [^13]

In Feature engineering multiple attributes were derived needed in modelling or for analysis. From survey data total number of Murrah buffalo count from top 10 states and their percentage share were derived and listed in Table 1. Though Uttar Pradesh is top state in India in terms of total number of buffalos but percentage share of Murrah buffalo is more in state of Punjab. 

**Table 1:** Murrah buffalo percent share in top 10 state with buffalo count 

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

Survey dataset had three primary attributes reported at the state level. Data reported from 2013 to 2019 for in-milk animals, yield per in-milk animals and milk production per state were averaged for analysis purpose. Total number of buffalos per breed type were calculated from the data provided in the dataset. Following list of breeds were identified from dataset [^2].

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

### 4.3 Modelling

#### 4.3.1 Benchmarking 

There are two dominant approach of economic modelling to estimate the production behavior - Empirical Benchmarking and Stochastic Frontier Analysis [^8], [^9]. Empirical Benchmarking is simple modelling method, and it is one of the two dominant approach. This method was used to analyze past 6 years of data points available in the livestock dataset. In this approach milk yield data and milk production data of past 6 years was averaged. Top 10 states with most yield in-milk and milk production reported were compared with average of the whole sample. The comparison did not consider all possible characteristics for modelling. The problem analyzed as part of this project was relatively small. With the given small dataset only two parameters, average yield in-milk and average milk production was analyzed. 

We created two models, one for analyzing average yield in-milk animals and second one was to analyze the average milk production. Data showed that Uttar Pradesh had highest average milk production of 17810 tonne compared to whole sample. Punjab state had highest average yield per in-milk animals which as 8.39 kg per day. As we analyzed common attributes between two states that contributed to highest numbers in their respective area, we noticed that both the states have highest number of Murrah breed buffalos compared to other breeds. Figure 5 shows the share of top 3 breeds in both the state.  

![TOP TWO States](https://github.com/cybertraining-dsc/fa20-523-326/raw/main/project/images/punjab_up_state.png)

**Figure 5:** Top 3 types of buffalo breeds of Uttar Pradesh and Punjab

In this study we presented result of the two models analyzed. Based on the trends of yield in-milk and milk production from 20th livestock census data we were able to analyze patterns.


## 5. Results

Based on simple Empirical Benchmarking Analysis and trends noticed in data it appears that it is possible to increase production past currently attainable yields. The current scale of the yield does indicate that, leading states have best breeds of buffalos. Different methods of analyzing yield gaps can be combined to give estimates of attainable yields. It will also help to evaluate possible interventions to increase production and profits. 

## 6. Discussion

The biggest probable limitation here was availability of good quality data. Correct relation of census data with other socioeconomic factors like population information, climate information, agriculture information could not be established as part of this project since the data would not be matched to satisfactory level and covariate analysis results would be inconsistent due to nature of rollup census data at state level. It would have been possible to conduct the analysis at finer level. Our analysis had to be done state level rather than at district level or specific area. 

## 7. Conclusion

The analysis done above with the limited dataset showed that there are considerable gaps in the average yield per in-milk buffalo of state Punjab and Uttar Pradesh, compared to other states in top 10 list. These states have larger share of Murrah breed buffalos. Based on the data trends it appears that it is possible to increase the production past current attenable numbers. However, this would need to combine different methods and multiple strategies.
  
## 8. Acknowledgements

The author would like to thank Dr. Gregor Von Laszewski, Dr. Geoffrey Fox, and the associate instructors in the *FA20-BL-ENGR-E534-11530: Big Data Applications* course (offered in the Fall 2020 semester at Indiana University, Bloomington) for their continued assistance and suggestions with regard to exploring this idea and also for their aid with preparing the various drafts of this article.

## 9. References

[^1]: Water Buffalo. Accessed: Oct 26, 2020. [Online]. Available: <https://en.wikipedia.org/wiki/Water_buffalo> 

[^2]: List of Water Buffalo Breeds. Accessed: Oct 26, 2020. [Online]. Available: <https://en.wikipedia.org/wiki/List_of_water_buffalo_breeds>

[^3]: PIB Delhi. (2019). "Department of Animal Husbandry & Dairying releases 20th Livestock Census", 16 (Oct 2019).
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

[^20]: Mayberry, Dianne (07/2017). "Yield gap analyses to estimate attainable bovine milk yields and evaluate options to increase production in Ethiopia and India". Agricultural systems (0308-521X), 155 , p. 43.
