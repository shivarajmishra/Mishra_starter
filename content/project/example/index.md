---
slides: example
url_pdf: ""
title: eTutorial. Ideas, codes and worked examples for creating Forrest Plot and
  Gap Minder Visualization in SAS 9.4
summary: >-
  <!--StartFragment-->


  This visualization shows the gender difference in cardiovascular disease rates by socio-economic status. For that, I used the data from the global burden of disease data. In this tutorial/blog, I will briefly explain the steps in creating such vitalization and try explaining some of the findings’ nuances, which might be interesting.


  <!--EndFragment-->
url_video: ""
date: 2016-04-27T00:00:00Z
external_link: https://shivarajmishra.tumblr.com/post/638934132740718592/etutorial-ideas-codes-and-worked-examples-for
url_slides: ""
subtitle: Viz
tags:
  - Deep Learning
links:
  - icon: twitter
    icon_pack: fab
    name: Follow
    url: https://twitter.com/georgecushen
image:
  caption: Photo by rawpixel on Unsplash
  focal_point: Smart
url_code: ""
---
<!--StartFragment-->

## eTutorial. Ideas, codes and worked examples for creating Forrest Plot and Gap Minder Visualization in SAS 9.4

**Shiva Raj Mishra,** Brisbane, Australia 

This visualization shows the gender difference in cardiovascular disease rates by socio-economic status. For that, I used the data from the global burden of disease data. In this tutorial/blog, I will briefly explain the steps in creating such vitalization and try explaining some of the findings’ nuances, which might be interesting.

**Background**

The cardiovascular disease (CVD) has increased continually over the past two decades due to population growth, aging as well as improvement in treatment and management of disease. This study aims to examine the gendered impact of poverty in the risk of cardiovascular disease among women.



> **STEPS in analysis**
>
> STEP 1: Familiarize yourself with the literature\
> Before jumping into data analysis, I conducted a scoping review around the literatures examining the independent and interactive association between socioeconomic status, gender and cardiovascular disease. Doing these analyses, I was able to demonstrate that there is gendered differences in rates of cardiovascular disease (e.g. incidence, hospitalizations rates) between men and women. However, I found that not lot of studies has considered such differences in the context of socio-economic status. Such differences could be pronounced among women from the low socio-economic status compared to their counterparts.
>
> STEP 2: define the study variables and methods
>
> In the proposed analysis, the ‘gender difference in rates’ is defined as the difference between male and female rates. The p-trend values were calculated using the Jonckheere-Terpstra Test for the trend of the continuous outcome variable (2). The figures were created using the standard methodology for creating Forrest plot in SAS using graphic template language (1). Sample codes are provided in *supplementary appendix*.
>
> Further, the gross domestic product (GDP) per capita (inflation-adjusted) are plotted in x-axis and corresponding values of gender difference in age-standardized CVD rates (male rates minus female rates) are plotted in the y-axis. The size of bubble represents the size of population of the country. The definition of cardiovascular disease includes all eleven CVD types and is described elsewhere (4). The map on the left are annotation and shows the world region (America, East Asia & Pacific, Europe & Central Asia, Middle east & north Africa, South Asia, Sub-Saharan Africa). The data on cardiovascular diseases rates were obtained from Global Burden of Disease (4) and population data from World Bank (5). These figures were created using graphic template language in SAS following a procedure developed by Robert (2019) (3). Sample codes are provided in *supplementary appendix*.
>
> When considering cardiovascular disease types, I reduced the number of CVD types from eleven to eight (Rheumatic heart disease, Ischemic heart disease, Stroke, Hypertensive heart disease, Cardiomyopathy and myocarditis, Peripheral heart disease, Endocarditis, Other cardiovascular diseases). The ‘other cardiovascular diseases’ here includes non-rheumatic valvular heart disease plus atrial fibrillation and flutter plus other cardiovascular diseases which were displayed separately in earlier visualizations.

**Findings**

Burden of cardiovascular diseases disaggregated by sociodemographic index

> *I displayed DALYs rates, deaths rates and prevalence rates in the same figure for each CVD types. This way, it might help to improve the clarity in the findings.*

**(A)**   **Rheumatic heart disease**

Female had higher DALYs (per 100,000 population), deaths (per 100,000) and prevalence (per 100,000) from rheumatic heart disease (RHD) and this gap narrowed across the SDI quintiles. In low SDI region, female witnessed 99 more DALYs from RHD (per 100,000 population) than male which narrowed down to <7 more DALYs in higher SDI regions. These findings suggest statistically significant relationship between SDI quintiles and gender-specific DALYs, deaths and prevalence RHD rates (all *P-trend* = 0.0143).

![image](https://64.media.tumblr.com/bf53f25f789c989e02334a373fab478e/0c961475975a797c-63/s500x750/cad03f5495df9027da8467e2efcf32039e1bcb18.png)

**(B)**    **Ischemic heart disease**

Females had lower DALYs (per 100,000 population), deaths (per 100,000), and prevalence (per 100,000) from ischemic heart disease (IHD), and this gap was not affected by SDI quintiles (p-trend >0.05). In the low SDI region, females witnessed 1180 less DALYs from IHD (per 100,000 population) than males, which narrowed down to 863 per 100,000 DALYs in the higher SDI region. However, these findings show no evidence of a relationship between gender and SDI quintiles.

![image](https://64.media.tumblr.com/840f370f90cb0ad7948a8776193d553e/0c961475975a797c-14/s500x750/6a02d451b83490527ee02833f939321d6e2303cf.png)

**©**    **Stroke**

Females had lower DALYs (per 100,000 population), deaths (per 100,000), and but higher prevalence (per 100,000) from stroke than males, and this gap remained unchanged across the SDI quintiles (p-trend >0.05). In the low SDI region, females witnessed 101 less DALYs from stroke (per 100,000 population) than males, which moderately increased to 185 DALYs per 100,000 in higher SDI regions. These findings suggest no evidence of a relationship between DALYs rate (per 100,000 population) and SDI quintiles. There was some evidence suggesting a relationship between SDI quintiles and gender-specific RHD prevalence rates (*P-trend* = 0.05).

![image](https://64.media.tumblr.com/22ae65531a8e20cfdea23fce8ec00aa5/0c961475975a797c-8d/s500x750/c51bc7a9eddfb1b4830b6c5882d4526c8f57b4d6.png)

> *I spent quite a bit of time exploring different visualization methods. I have always been fascinated by Gap minder’s graphical presentation – which I tried to re-create in SAS using graphic template language. It was a good learning experience.*

**Burden of cardiovascular disease from 1990-2017 by countries and region**

These figures were created using graphic template language in SAS following a procedure developed by Robert (2019) (3). The GDP per capita (inflation-adjusted) are plotted in x-axis and corresponding values of gender difference in age-standardized cardiovascular disease (CVD) rates (male rates minus female rates) are plotted in y-axis. The size of bubble corresponds to the size of the population of the country. The definition of cardiovascular disease includes all eleven CVD types and is described elsewhere (4). The left map is for annotation and shows the world’s region (America, East Asia & Pacific, Europe & Central Asia, Middle east & North Africa, South Asia, Sub-Saharan Africa). The data on cardiovascular disease rates were obtained from the Global Burden of Disease (4) and population data from World Bank (5). *Sample codes are provided in supplementary appendix.*

*(A)* **Age-standardized DALYs rate of cardiovascular disease per 100,000 population from 1990 to 2017 by country’s GDP/capita**

![image](https://64.media.tumblr.com/b29cfb46acdffed7bc50d12ca517a225/0c961475975a797c-d2/s500x750/e662bde85a967261a971701459aec0c65828e990.gifv)

*(B)* **Age- standardized deaths rate of cardiovascular disease per 100,000 population from 1990 to 2017 by country’s GDP/capita** 

![image](https://64.media.tumblr.com/18d382305bbd4d14deb1dfaf96ca46fe/0c961475975a797c-6d/s500x750/fa0a213bff3dc0689692e401741ceb8199695821.gifv)

*©* **Age- standardized prevalence rate of cardiovascular disease per 100,000 population on from 1990 to 2017 by country’s GDP/capita**  

![image](https://64.media.tumblr.com/08894ff6b4266715141fdf71a9178438/0c961475975a797c-1a/s500x750/cd3ad95ac221aa3ce4f7a0373b7efaa5f4db66f0.gifv)

**Summary**

As the GDP goes up from 1990 to 2017, countries gradually shift from having higher CVD DALYs rates to lower CVD DALYs among women. Many countries were in the negative quadrant in 1990. These changes support our ealier findings that the gender difference has been continuously narrowing down for rheumatic heart disease and widening for stroke, across the SDI quintiles. 

Factors contributing to these shifts in CVD rates may include literary, income, and empowerment in women. Also, these changes should be interpreted in the context of existing data limitations. Further studies are needed to untangle the gendered impact of poverty in cardiovascular disease.

**[Supplementary appendix](https://href.li/?https://drive.google.com/file/d/18yYKbFipPT0ouKk3veCpgyk3gjUjqa5Z/view?usp=sharing) (click here)**

**References**

1. O’Leary JR. How to Create a Journal Quality Forest Plot with SAS® 9.4. Available from [https://www.pharmasug.org/proceedings/2017/QT/PharmaSUG-2017-QT15.pdf](https://href.li/?https://www.pharmasug.org/proceedings/2017/QT/PharmaSUG-2017-QT15.pdf) (accessed 7 May, 2020)

2. Park C, Hsiung JT, Soohoo M, Streja, E. Choosing Wisely: Using the Appropriate Statistical Test for Trend in SAS. Available from [https://www.lexjansen.com/wuss/2019/175_Final_Paper_PDF.pdf (accessed 7 May 2020)](<https://href.li/?https://www.lexjansen.com/wuss/2019/175_Final_Paper_PDF.pdf%20(%0d3>)

[3](<https://href.li/?https://www.lexjansen.com/wuss/2019/175_Final_Paper_PDF.pdf%20(%0d3>). Robert A. Available from [https://blogs.sas.com/content/sastraining/2019/01/24/re-creating-a-hans-rosling-graph-animation-with-sas/](https://href.li/?https://blogs.sas.com/content/sastraining/2019/01/24/re-creating-a-hans-rosling-graph-animation-with-sas/) (accessed 7 May 2020)

4. Global Burden of Disease Collaborative Network. Global Burden of Disease Study 2017 (GBD 2017) Results. Seattle, United States: Institute for Health Metrics and Evaluation (IHME), 2018. Available from. Available from [http://ghdx.healthdata.org/gbd-results-tool](https://href.li/?http://ghdx.healthdata.org/gbd-results-tool) (accessed 5 May 2020)

5. World Bank. Population Total. Available from [http://wdi.worldbank.org/table/2.1#](https://href.li/?http://wdi.worldbank.org/table/2.1) (accessed 5 May 2020)

<!--EndFragment-->