# Project 2 - Ames Housing Data and Kaggle Challenge

### Problem Statement

As a real estate agent, for what reasons would I recommend a 1-story over 2-story house to first-time home buyers?

---

### Overview

For this project, I analyzed 2017 and 2018 SAT and ACT data. This data included reports of participation levels, mean individual test subject scores and total/composite scores per state. I wanted to get a better understanding of which states had the lowest SAT participation and possible explanations for the statistics. I cleaned this data and explored it to get try to identify any possible correlations involving these states.

### Dataset Features
|Feature|Type|Dataset|Description|
|---|---|---|---|
|**state**|*object*|ACT/SAT|The 50 states of the U.S. (including the entire Nation)|
|**sat_participation_17**|*float*|SAT|The percentage of the state that took the SAT in 2017|
|**sat_english_17**|*int*|SAT|The mean SAT Evidence-Based Reading and Writing score for each state in 2017|
|**sat_math_17**|*int*|SAT|The mean SAT Math score for each state in 2017|
|**sat_total_17**|*int*|SAT|The mean SAT total score for each state in 2017|
|**act_participation_17**|*float*|ACT|The percentage of the state that took the ACT in 2017|
|**act_english_17**|*float*|ACT|The mean ACT English score for each state in 2017|
|**act_math_17**|*float*|ACT|The mean ACT Math score for each state in 2017|
|**act_reading_17**|*float*|ACT|The mean ACT Reading score for each state in 2017|
|**act_science_17**|*float*|ACT|The mean ACT Science score for each state in 2017|
|**act_composite_17**|*float*|ACT|The mean ACT composite score for each state in 2017|


I found that **Michigan**, **Connecticut**, and **Delaware** had the highest SAT participation for both 2017 and 2018, and **North Dakota** consistently had the lowest participation rate. However, I did also discover that despite having consistently the lowest participation rate, **North Dakota** did have the third highest mean SAT total score in 2018.

Through this data I discovered that there was a pretty high but negative correlation between 2018 SAT Participation and 2017 ACT Participation. This is to say, that decreases in ACT Participation in 2017 were fairly correlated with increases in SAT Participation in 2018. I then used outside research to look for reasons why this could be. I analyzed Colorado and Illinois who were greatly affected by this correlation, and discovered that the change in Colorado's and Illinois's SAT and ACT participation can be attributed to the new state contracts with the College Board, incentivizing states to promote the SAT to students.

Given all this information, for the lowest SAT participatory state, **North Dakota**, I would reccommend that College Board seek to increase participation by initiating a state contract, allowing the state schools to administer the exam for free and providing the school with free SAT preparatory resources. I would also recommend advertising SAT competitive rates for local universities as both North Dakota State University and Minot State University, two of the largest universities in North Dakota, are reportedly less competitive to get into when using SAT scores vs using ACT scores.

### Outside Data Sources

 https://blog.prepscholar.com/which-states-require-the-sat
 https://www.adn.com/alaska-news/education/2016/06/30/students-no-longer-need-national-tests-to-graduate/
 https://www.prepscholar.com/sat/s/colleges/North-Dakota-State-University-SAT-scores-GPA 
 https://www.prepscholar.com/sat/s/colleges/Minot-State-University-admission-requirements
