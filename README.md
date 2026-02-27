
[Portfolio Project 1 .docx](https://github.com/user-attachments/files/25615418/Portfolio.Project.1.docx)



Abe Epstein 

INFO 3401 

Portfolio Project 1 

2 March 2026



__Project Overview__

This project is interested in studying how different factors influence health outcomes at the state level (in Colorado) and the national level. All data analysis was done in MySQL, with queries attached to GitHub. In this project, there are three questions that we are seeking to answer: 
1.  Are there sex differences in the prevalence of heart disease mortality in 2021? 
2.  What are the top 5 regions in Colorado with the highest age-adjusted incidence rate of lung and bronchus cancer from 2018 to 2020?
3.  How did socioeconomic status influence the prevalence of chronic obstructive pulmonary disease (COPD) in 2021? 
To improve data analysis, only the 2021 CDC and economic data were used. 













__Question 1: Sex Differences in Coronary Heart Disease Mortality__

*Overview*

The first thing that I was interested in looking at was the sex differences in the prevalence of heart disease mortality by state. To do this, I filtered the data to show only the disease we are interested in and its crude rate (to obtain the disease's prevalence by gender). I then grouped the data by gender (under the stratification1 variable) and used the most recent data from 2021. The results are as follows:

<img width="499" height="144" alt="image" src="https://github.com/user-attachments/assets/29a54c5a-2d50-4fa0-9eee-1280287b87fe" />

 
*Interpretation*


The resulting data shows, on average, 54 more cases per 100,000 of coronary heart disease mortalities in males than there are in females in 2021. There are a multitude of reasons that may explain these findings. In a review by Maas & Appelman (2010), findings suggest that cardiovascular disease develops later in women, as well as differences in clinical presentation in women, leading to an under-recognition of heart disease and less aggressive treatment strategies. 



__Question 2: Lung and Bronchus Cancer__

*Overview*

The second question that I am seeking to answer with this data is: What are the top 5 counties in Colorado that have the highest incidence (new cases) of lung and bronchus cancer when adjusting for age differences across counties? The first thing I did was isolate the data I was looking for and remove the counties that did not report any values (Costilla, Gilpin, Hinsdale, Jackson, Kiowa, Mineral, San Juan). I then converted the values to numbers using CONVERT because the data was read in as text. I then ordered the data from highest to lowest to find the top 5 counties. The results are below: 

<img width="499" height="112" alt="image" src="https://github.com/user-attachments/assets/718abd68-ea6f-4a6f-a6c4-e4d4e22f9497" />

 
*Interpretation*

The top 5 counties with the highest incidence of lung and bronchus cancer were Cheyenne, Baca, Lincoln, Prowers, and Fremont. The most striking incidence of lung cancer is in Cheyenne, with 67 more cases than the state average of 37. Though there are numerous risk factors associated with developing lung and bronchus cancer, additional research into these county’s allowed for a couple of theories. Firstly, elevated tobacco use in frontier counties such as Baca, Prowers, and Lincoln in comparison to the state average may explain the higher incidence rates. Secondly, rural counties also have fewer opportunities for early lung cancer screenings due to a lack of access to specialized healthcare facilities. Lastly, these five counties share lower median household incomes and higher poverty rates than the state average. Socioeconomic status is deeply intertwined with tobacco use, health insurance, and increased occupational exposures to carcinogens. Future solutions include an increase in screening programs and greater healthcare equality in these areas. 







__Question 3: Socioeconomic Status and COPD__

*Overview*

Using economic data from the U.S. Census and disease data from the CDC, question 3 investigates how socioeconomic status influences the prevalence of chronic obstructive pulmonary disease (COPD). The first thing that I did was create a subquery that filtered the economic data to isolate per capita data, and created another subquery that filtered the CDC data to isolate COPD data. I joined the two tables using an inner join on the state variable. Attempting to extrapolate findings from this data was difficult, so I added how each state ranks in per capita income and disease prevalence so that the data would be easier to interpret. Results are below:  

 <img width="499" height="249" alt="image" src="https://github.com/user-attachments/assets/59dd9688-416b-45bf-a822-a132d9c9a6ee" />

 
*Interpretation*

Overall, there appears to be a strong correlation between lower SES and higher rates of COPD. By sorting to find the top 10 states with the highest COPD prevalence, we see that every single state on this list falls in the bottom third of the country for per capita income. We also see that West Virginia has the highest COPD rate and the second lowest per capita income, and Mississippi has the lowest per capita income in the country and the sixth highest COPD prevalence. States with the highest COPD and lowest per capita income ranks are also concentrated in the South and Midwest. These regions have historically faced both socioeconomic and public health challenges, which may partly explain this trend. 




__References__


Centers for Disease Control and Prevention. U.S. Chronic disease indicators (CDI). Data.gov. Published March 9, 2024. Accessed February 27, 2026. https://catalog.data.gov/dataset/u-s-chronic-disease-indicators


Colorado Department of Public Health and Environment. (n.d.). Colorado Central Cancer Registry (CCCR) data. Accessed February 27, 2026. https://cdphe.colorado.gov/colorado-central-cancer-registry


Maas, A. H., & Appelman, Y. E. (2010). Gender differences in coronary heart disease. Netherlands heart journal: monthly journal of the Netherlands Society of Cardiology and the Netherlands Heart Foundation, 18(12), 598–602. https://doi.org/10.1007/s12471-010-0841-y


U.S. Census Bureau. (n.d.). American Community Survey (ACS). U.S. Department of Commerce. https://www.census.gov/programs-surveys/acs/




