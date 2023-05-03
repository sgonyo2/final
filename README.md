**Description**  
The purpose of this project is to create an interactive [shiny app](https://www.shinyapps.io/admin/#/application/9020621) to understand attitudes towards gender roles and immigration using data from the European Value Study (EVS) from 2017. The EVS is a large-scale, cross-national and longitudinal survey research on how Europeans think about family, work, religion, politics, and society. Visit [European Value Study](https://search.gesis.org/research_data/ZA7500#variables|exploredata-ZA7500_Varv80|0|variable_order|asc|v80) for more information.

Specifically, we are interested in understanding the relationships between age, education, and sex on agreement with the following statements:  
 * When a mother works for pay, the children suffer
 * When jobs are scarce, employers should give priority to [NATIONALITY] people over immigrants
 
Two tabs are shown in the app. The first tab shows graphs exploring the relationship between the selected outcome variable and three controls: age, education, and sex. The second tab shows the coefficients and residuals plot of a regression analysis between the selected outcome variable and selected control variables.

Four inputs are required to use this app. First, select a country from the drop-down menu below. Next, select between two outcome variables. Then, select sex and/or education as your control variables (age is included by default). Finally, select the number of age polynomials you would like to include in the regression (e.g., selecting 3 includes age, age^2, and age^3).
 
**Organization**  
[data_prep](https://github.com/sgonyo2/hw2/blob/main/data_prep.Rmd) prepares the data by retaining, renaming, and cleaning the variables of interest.  
[dashboard](https://github.com/sgonyo2/final/blob/main/dashboard.Rmd) creates an interactive [shiny app](https://www.shinyapps.io/admin/#/application/9020621) to explore the data.
[data_subset](https://github.com/sgonyo2/final/blob/main/data_subset.rds) is the processed data.
[output](https://github.com/sgonyo2/final/tree/main/output) contains examples of the output created by the shiny app.

**Main Findings**  
Generally speaking, men, older people, and those with lower educations tend to agree more that children suffer when a mother works for pay (Figure 1). Opinions do not appear to change with age for woman as much as for men, and opinions do not appear to change with education as much for men as for women. Alternatively, education appears to be the primary driver of agreement that employers should give priority to nationals over immigrants When jobs are scarce (Figure 2), where those with higher educations are more likely to disagree.

Figure 1: Relationship between age, education, and sex and the statement "When a mother works for pay, the children suffer"
![](https://github.com/sgonyo2/final/blob/main/output/fig/child_suffer.jpeg)

Figure 2: Relationship between age, education, and sex and the statement "When jobs are scarce, employers should give priority to [NATIONALITY] people over immigrants"
![](https://github.com/sgonyo2/final/blob/main/output/fig/job_priority.jpeg)

**Session Info**  
R version 4.2.3 (2023-03-15 ucrt)  
Platform: x86_64-w64-mingw32/x64 (64-bit)  
Running under: Windows 10 x64 (build 19044)  

Matrix products: default  

locale:  
[1] LC_COLLATE=English_United States.utf8  LC_CTYPE=English_United States.utf8   
[3] LC_MONETARY=English_United States.utf8 LC_NUMERIC=C                          
[5] LC_TIME=English_United States.utf8    

attached base packages:  
[1] stats     graphics  grDevices utils     datasets  methods   base     

other attached packages:  
 [1] rio_0.5.29            shinythemes_1.2.0     shinycssloaders_1.0.0
 [4] caret_6.0-94          lattice_0.20-45       corrplot_0.92        
 [7] plotly_4.10.1         DT_0.27               leaflet_2.1.2        
[10] maps_3.4.1            stargazer_5.2.3       broom_1.0.4          
[13] shinydashboard_0.7.2  shiny_1.7.4           labelled_2.11.0      
[16] haven_2.5.2           knitr_1.42            texreg_1.38.6        
[19] lubridate_1.9.2       forcats_1.0.0         stringr_1.5.0        
[22] purrr_1.0.1           readr_2.1.4           tidyr_1.3.0          
[25] tibble_3.2.1          ggplot2_3.4.2         tidyverse_2.0.0      
[28] dplyr_1.1.1  
