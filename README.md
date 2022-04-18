# Project - Standardized Test Analysis


### Problem Statement

California is the largest state in population with many school districts - some that are top in the nation, others pale significantly in comparison. We hypothesize that school funding contributes positively to standardized test performances. This project aims to identify California school districts with comparatively weak standardized testing performances and explore how factors such as __school expenditures__, __household incomes__, and __student-to-faculty ratios__ affect __standardized test scores__ in each school district. We hope to provide recommendations as to how to help improve standardized test performances for these districts in need, whether through fund allocations or other means.

### Dataset Used
* [`sat_2019_ca.csv`](../data/sat_2019_ca.csv): 2019 SAT Scores in California by School  ([*source*](https://www.cde.ca.gov/re/pr/satactapdatareports.asp))
* [`act_2019_ca.csv`](../data/act_2019_ca.csv): 2019 ACT Scores in California by School ([*source*](https://www.cde.ca.gov/re/pr/satactapdatareports.asp))
* [`pubschls.csv`](../data/pubschls.csv): All Public School Records in California ([*source*](https://www.cde.ca.gov/ds/si/ds/pubschls.asp))
* [`ncesdata_expend_ca.csv.csv`](../data/ncesdata_expend_ca.csv): 2019 Expenditures in California by School District ([*source*](https://nces.ed.gov/edfin/search/peergroupdata.asp?dataid=2&subdataid=1&mt=0&pagenumber=1&bleaid=&jobid={A2629B56-1758-4ED8-AE7A-7157DBA157E6}))
* [`ncesdata_charac_ca.csv`](../data/ncesdata_charac_ca.csv):  2019 Other Characteristics in California by School District ([*source*](https://nces.ed.gov/edfin/search/peergroupdata.asp?dataid=2&subdataid=1&mt=0&pagenumber=1&bleaid=&jobid={A2629B56-1758-4ED8-AE7A-7157DBA157E6}))
* [`ncesdata_kids_poverty_ca.csv`](../data/ncesdata_kids_poverty_ca.csv): 2008 Student Poverty ACT Scores in California by School Ditrict ([*source*](https://nces.ed.gov/edfin/search/peergroupdata.asp?dataid=2&subdataid=1&mt=0&pagenumber=1&bleaid=&jobid={A2629B56-1758-4ED8-AE7A-7157DBA157E6}))
* [`ca_avg_income_by_school_district.csv`](../data/ca_avg_income_by_school_district.csv): 2019 Average Household Income by School District ([*source*](https://nces.ed.gov/))


### Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|cds|object|sat_2019_ca_cleaned|County/District/School Code| 
|LEAID|object|sat_2019_ca_cleaned, act_2019_ca_cleaned|Local Education Agency ID Number| 
|district_codes|object|sat_2019_ca_cleaned, act_2019_ca_cleaned|District Code| 
|county|object|sat_2019_ca_cleaned, act_2019_ca_cleaned|County name| 
|participation_rate_11|float|sat_2019_ca_cleaned|Total participation rate for 11th-grade SAT takers| 
|participation_rate_12|float|sat_2019_ca_cleaned|Total participation rate for 12th-grade SAT takers| 
|participation_rate_total|float|sat_2019_ca_cleaned|Total participation rate for both 11th and 12th grade SAT takers| 
|total_enroll|float|sat_2019_ca_cleaned|Total enrollment for Grade 11 and 12 students| 
|school_district|object|sat_2019_ca_cleaned, act_2019_ca_cleaned|School District| 
|participation_rate_12_act|float|act_2019_ca_cleaned|Total participation rate for 12th-grade ACT takers| 
|enrollment_12|float|act_2019_ca_cleaned|Total enrollment for Grade 12 students| 
|avg_comp_act|float|act_2019_ca_cleaned|Average ACT composite score| 
|avg_english_act|float|act_2019_ca_cleaned|Average ACT english score| 
|avg_reading_act|float|act_2019_ca_cleaned|Average ACT reading score| 
|avg_math_act|float|act_2019_ca_cleaned|Average ACT math score|
|avg_science_act|float|act_2019_ca_cleaned|Average ACT science score| 
|%act_testers>21|float|act_2019_ca_cleaned|Percentage of ACT testers who scored 22 or higher in composite score| 
|#erw_12|float|sat_2019_ca_cleaned|The number meeting the Evidence-Based Reading & Writing (ERW) benchmark established by the College Board based on the New 2016 SAT test format as of March 2016 for Grade 12.| 
|%erw_12|float|sat_2019_ca_cleaned|The percent of students who met or exceeded the benchmark for Evidence-Based Reading & Writing (ERW) test for Grade 12.| 
|#math_12|float|sat_2019_ca_cleaned|The number of students who met or exceeded the benchmark for the New SAT Math test format as of March 2016 for Grade 12.| 
|%math_12|float|sat_2019_ca_cleaned|The percent of students who met or exceeded the benchmark for SAT Math test for Grade 12.| 
|enrollment_11|float|sat_2019_ca_cleaned|Total Enrollment of Grade 11| 
|total_tester_11|float|sat_2019_ca_cleaned|Number of Test Takers Grade 11| 
|#erw_11t|float|sat_2019_ca_cleaned|The number meeting the Evidence-Based Reading & Writing (ERW) benchmark established by the College Board based on the New 2016 SAT test format as of March 2016 for Grade 11.| 
|%erw_11|float|sat_2019_ca_cleaned|The percent of students who met or exceeded the benchmark for Evidence-Based Reading & Writing (ERW) test for Grade 11.| 
|#math_11|float|sat_2019_ca_cleaned|The number of students who met or exceeded the benchmark for the New SAT Math test format as of March 2016 for Grade 11.| 
|%math_11|float|sat_2019_ca_cleaned|The percent of students who met or exceeded the benchmark for SAT Math test for Grade 11.| 
|#both_12|float|sat_2019_ca_cleaned|The total number of students who met the benchmark of both Evidence-Based Reading & Writing (ERW) and Math Grade 12.| 
|%both_12|float|sat_2019_ca_cleaned|The percent of students who met the benchmark of both Evidence-Based Reading & Writing (ERW) and Math Grade 12.| 
|#both_11|float|sat_2019_ca_cleaned|The total number of students who met the benchmark of both Evidence-Based Reading & Writing (ERW) and Math Grade 11.| 
|%both_11|float|sat_2019_ca_cleaned|The percent of students who met the benchmark of both Evidence-Based Reading & Writing (ERW) and Math Grade 11.| 
|student_teacher_ratio|float|sat_2019_ca_cleaned, act_2019_ca_cleaned|The Student-to-Faculty ratio for the district| 
|total_cur_exp|float|sat_2019_ca_cleaned, act_2019_ca_cleaned|The total current expenditure per student for the district in fiscal year 2019| 
|instructional_exp|float|sat_2019_ca_cleaned, act_2019_ca_cleaned|The total instructional expenditure per student for the district in fiscal year 2019| 
|student_staff_support_exp|float|sat_2019_ca_cleaned, act_2019_ca_cleaned|The total student-staff-support expenditure per student for the district in fiscal year 2019| 
|operations_exp|float|sat_2019_ca_cleaned, act_2019_ca_cleaned|The total operational expenditure per student for the district in fiscal year 2019| 
|%kids_poverty|float|sat_2019_ca_cleaned, act_2019_ca_cleaned|The percentage of students in poverty for the district in year 2008| 
|locale_type|object|sat_2019_ca_cleaned, act_2019_ca_cleaned|The types of environment the school district in classified in: suburban, rural, city, town|
|avg_household_income|float|sat_2019_ca_cleaned, act_2019_ca_cleaned|The average household income for the district in fiscal year 2019| 


### Summary of Analysis

We identified school districts with weaker standardized test performances with aggregatiion and masking on the originally provided SAT and ACT datasets. 
To explore relationships between school fundings, income, and test performance, we obtained, cleaned, and combined datasets containing relevant information on school expenditure and student-faculty ratio, and average household income.
To help identify how various factors contribute / relate to standardized test performances, we computed pairwise correlations on all pairs of features and visualized with heatmap. 
We used scatter and regression plots to visualize the pairs of our target features to confirm the correlations, or lack thereof.

Our findings are as follow:

- School districts of Golden Plains Unified, Compton Unified, Reef-Sunset Unified, Fontana Unified, and Ravenswood City Elementary are the 5 districts that have the lowest composite SAT/ACT scores.
- Student-Teacher-Ratio and Instructional Expenditures both have little-to-no correlation wiith SAT/ACT test performances.
- As student poverty rate decreases, standardized test performances tend to increase.
- As average household income increases, standardized test performances tend to increase.
- School districts with high average income / low student poverty rate and high standardized test performances tend to be in cities or suburbs.

### Conclusions and Recommendations

Based on our exploration of the data, we find that school districts of Golden Plains Unified, Compton Unified, Reef-Sunset Unified, Fontana Unified, and Ravenswood City Elementary are the 5 districts that have the lowest composite ACT scores. 
In terms of reccomendations, we find that it is not as simple as allocating more funding to these districts in need. 
This is because we find there to be little-to-no correlation between standardized test performances and educational expenditures or student-teacher ratio. 

While there is little correlation between the test performances and school expenditures, we find that as average household income increases,  standardized test scores also tend to increase. 
Thus our initial assumption that allocating more funds to school districts with weaker performances helps improve standardize test performances may not be true. 

Along with the postive correlation between test scores and average household income, we infer that school teaching may not have a huge impact on standardized test scores, and that private standardize testing preperations may play a role in students' standardized test performance.
This illustrates the potential inequity inherent in standardized testing practices, and begs for closer examination from educators and researchers to address and improve such issues of inequity.


