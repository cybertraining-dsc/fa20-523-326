# Analysis of Future of Buffalo Breeds and Milk Production Growth in India

[![Check Report](https://github.com/cybertraining-dsc/fa20-523-326/workflows/Check%20Report/badge.svg)](https://github.com/cybertraining-dsc/fa20-523-326/actions)


Gangaprasad Shahapurkar, fa20-523-326, [Edit](https://github.com/cybertraining-dsc/fa20-523-326/blob/master/project/project.md)

{{% pageinfo %}}

## Abstract

Water buffalo (Bubalus bubalis) also called domestic water buffalo or Asian water buffalo is a large bovid originating in the Indian subcontinent, Southeast Asia, and China. Today, it is also found in Europe, Australia, North America, South America and some African countries. Two extant types of water buffalo are recognized, based on morphological and behavioural criteria. One is river buffalo of the Indian subcontinent and further west to the Balkans, Egypt, and Italy, and other one is swamp buffalo, found from Assam in the west through Southeast Asia to the Yangtze valley of China in the east. India has the highest level of milk production and consumption of all countries. The dairy industry in India is unique among large-scale milk producing countries in terms of its large share of buffalo milk. The aim of this academic project is to study the livestock census data of buffalo breeds in India and their milk production using emphirical benchmarking analysis method at state level. Looking at small sample of data, our analysis indicates that we have been seeing increasing trends in past few years in livestock and milk production but there are considerable opportunities to increase production using combined interventions.

Contents

{{< table_of_contents >}}

{{% /pageinfo %}}


**Keywords:** hid 326, i532, buffalo, milk production, livestock, benchmarking, in-milk yield, argriculture, india, analysis.

## 1. Introduction

Indian Agriculture sector has been playing a vital role in overall contribution to Indian Economy. Most of the rural community in the nation still make their livelihood on Dairy Framing or Agriculture farming. Dairy framing itself has been on its progressive stage from past few years and it is contributing to almost more than 25% of agriculture GDP [^3]. Livestock rearing has been integral part of rural community of the nation and this sector is leveraging the economy in big way considering the growth we can see. Livestock production plays major role in life of farmers. It provides food, income, employment. It also does other contributions to the overall rural development of the nation. The output of livestock rearing such as milk, egg, meat, and wool provides everyday income to the farmers on daily basis, it provides nutrition to consumers and indirectly it helps in contributing to overall national economy and socio-economic development of the country.

![Milk Production World](https://github.com/cybertraining-dsc/fa20-523-326/raw/master/project/images/milk_production_world.png)

**Figure 1:** Production of Milk, whole fresh buffalo in World + (Total), Average 2013 - 2018

![Milk Production Share](https://github.com/cybertraining-dsc/fa20-523-326/raw/master/project/images/milk_production_by_region.png)

**Figure 2:** Production share of Milk, whole fresh buffalo by region, Average 2013 - 2018

India is the highest buffalo milk producer in the world. The world buffalo population is estimated at 185.29 million, spread in some 42 countries, of which 179.75 million (97%) are in Asia (Source: Fao.org/stat 2008). India has 105.1 million and they comprise approximately 56.7 percent of the total world buffalo population. During the last 10 years, the world buffalo population increased by approximately 1.49% annually, by 1.53% in India, 1.45% in Asia and 2.67% in the rest of the world.

## 2. Background Research and Previous Work

The production of milk and meat from buffaloes in Asian countries over the last decades has shown a varying pattern: in countries such as India, Sri Lanka, Pakistan and China. Buffaloes are known to be better at converting poor-quality roughage into milk and meat. They are reported to have a 5 percent higher digestibility of crude fibre than high-yielding cows; and a 4-5 percent higher efficiency of utilization of metabolic energy for milk production [^5].

## 3. Choice of Datasets

Number of online literatures and datasets were checked to find out suitable dataset required for this project analysis. Below dataset were found promising:

1. [DAHD Data](https://dahd.nic.in/about-us/divisions/statistics) [^6], [^14], [^15], [^16]
2. [FAO Data](http://www.fao.org/faostat/en/#data) [^17]
  
The Animal Husbandry Statistics Division of the Department of Animal Husbandry & Dairying division (DAHD) is responsible for generation of
Animal Husbandry Statistics through the schemes of Livestock Census and Integrated Sample Surveys [^3]. Survey is defined by Indian Agriculture Statistics Research Institute (IASRI) [^18]. This is the only scheme through which considerable data, particularly on the production estimate of major livestock products, is being generated for policy formulation in the livestock sector. It is mandate for this division to

-   Conduct quinquennial livestock census.
-   Conduct annual sample survey through Integrated Sample Survey.
-   Publish of annual estimates of production of milk, eggs, meat, wool and other related Animal Husbandry Statistics based on Integrated 	Sample Survey conducted through State and Union Territories.

Food and Agriculture Organization of United Nation (FAO) publishes world wide data on aspects of dairy farming which can also be visualized online with the options provided. Some of the data from this source was used to extract useful summary needed in analysis.

## 4. Methodology 

### 4.1 Software Components

This project has been implemented in Python 3.7 version. Jupyter Notebook Application was used to develop the code and produce a notebook document. Jupyter Notebook is a client server architecture based application which allows modification and execution of code through web browser. Jupyter Notebook can be installed locally and accessed through localhost browser or it can be installed on a remote machine and accessed via Internet [^10], [^11].     

Following python libraries were used in overall code development. Before running the code one must make sure that these libraries are installed.
-   **Pandas** This is an high performence and easy to use library. It was used for data cleaning, data analysis, & data preperatin.
-   **Numpy** Numerical Python or Numpy is the python core library used for scientific computing. Some of the basic functions were used in 		this project
-   **Matplotlib** This is an comprehensive library used for static, animated and interactive visualization. 
-   **OS** This is another standard library of Python which provides which provides miscellaneous operating system interface functions

### 4.2 Data Processing

The raw data retrived from the source was in excel format. The data was pre-processed and stored back in csv formaat for the purpose of this project to easily process it. This data set was further processed through various stages via EDA, feature engineering and Modelling

#### 4.2.1 EDA 

Preprossed dataset selected for this analysis contians information at state level. Below are the nature of the attributes in the dataset:

- **State Name** Name each of the state in India. One record for each state
- **Buffalo count** Total number of male and female buffalo. Data recorded for 14 types of buffalo breeds. One attribute for each type of female and male breed
- **In Milk** Number of In-Milk animals per state (figures in 000 nos) recorded each year from 2013 to 2019. One attribute per year
- **Yeild In-Milk** Yield per In-Milk animals per state (figures in kg/day) recorded each year from 2013 to 2019. One attribute per year
- **Milk production** - Milk production per state (figures in 000 tones) recorded each year from 2013 to 2019. One attribute per year

Livestock census shows that Uttar Pradesh is the state which reported more number buffalos compared to any other states in country. 

![Milk Production Share](https://github.com/cybertraining-dsc/fa20-523-326/raw/master/project/images/top10states.png)

**Figure 3:** Top 10 state with buffalo counts compared to others

Apart from the total number of buffalo state wise, overall we can see more than 80 % of the buffalo breeds reported in census were female breeds 

![Milk Production Share](https://github.com/cybertraining-dsc/fa20-523-326/raw/master/project/images/buffaloshare.png)

**Figure 4:** Percentage of Female vs Male buffalo reported

#### 4.2.2 Feature Engineering


![Murrah buffalo](https://github.com/cybertraining-dsc/fa20-523-326/raw/master/project/images/murrah_buffalo.jpeg)

**Figure 5:** Murrah buffalo (Bubalus bubalis), globally famous local breed of Haryana, were exported to many nations [^12], [^13]

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

### 4.3 Modelling

#### 4.3.1 Benchmarking 

This is a simple modelling method and it is one of the two dominant approach of economic modelling to estimate the production behaviour [^4]. This method was used to estimate the potential of increase in milk yeild. In this approach milk yeild data of past 6 years was averaged. Top 10 states most yeild reported were compared with average of the whole sample and used to estimate the yeild for year 2020

![TOP TWO States](https://github.com/cybertraining-dsc/fa20-523-326/raw/master/project/images/punjab_up_state.png)

**Figure 5:** Top 3 types of buffalo breeds of Uttar Pradesh and Punjab

## 5. Results

NOTE: This section will continue to be updated until project completion.

## 6. Discussion

NOTE: This section will continue to be updated until project completion.

The biggest probabal limitation here was availability of good quality data. It would be possible to conduct the analyses at finer level. Our analyses had to be done state level rather than at district level or specific area. 

## 7. Conclusion

NOTE: This section will continue to be updated until project completion.

The analysis done above with the limited dataset showed that there are considerable gaps in avg yeild in per in-milk buffalo of state Punjab and Haryana compared to other states in top 10 list. Based on the data trends it appears possible to increase the production past current number attended. Though this would need to combine different methods and multiple strategies.
  

## 8. Acknowledgements

The author would like to thank Dr. Gregor Von Laszewski, Dr. Geoffrey Fox, and the associate instructors in the *FA20-BL-ENGR-E534-11530: Big Data Applications* course (offered in the Fall 2020 semester at Indiana University, Bloomington) for their continued assistance and suggestions with regard to exploring this idea and also for their aid with preparing the various drafts of this article.

## 9. References

[^1]: TEXT MISSING Accessed: Oct 26, 2020. [Online]. Available: <https://en.wikipedia.org/wiki/Water_buffalo> 

[^2]: TEXT MISSING. Accessed: Oct 26, 2020. [Online]. Available: <https://en.wikipedia.org/wiki/List_of_water_buffalo_breeds>

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

[^17]: FAO - Food and Agriculture Organization of United Nation, Accessed: Nov, 2020, <http://www.fao.org/faostat/en/#data>

[^18]: IASRI - Indian Agriculture Statistics Research Institute. <https://iasri.icar.gov.in/>

[^19]: Bharathi Dairy Farm. <http://www.bharathidairyfarm.com/about-murrah.php>

