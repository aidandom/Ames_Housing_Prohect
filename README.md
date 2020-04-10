# Project 2 - Ames Housing Data and Kaggle Challenge

### Problem Statement

As a real estate agent, for what reasons would I recommend a 1-story over 2-story house to first-time home buyers?

---

### Overview

For this project, I analyzed housing data from Ames, Iowa in 2010. This data included reports of garage size, lot size, kitchen quality, amount of bedrooms and bathrooms, foundation type, etc., and associated price. I wanted to get a better understanding of the differences in house features between single story and double story homes. I cleaned this data and explored it to get try to identify the highest and practical correlations between housing features and sale price.

### Dataset Features

Full dataset features: https://www.kaggle.com/c/dsi-us-11-project-2-regression-challenge/data

### Model Dataset Features
|Feature|Type|Dataset|Description|
|---|---|---|---|
|**Overall Qual**|*int*|train/test|Overall material and finish quality on scale 1-10|
|**Gr Liv Area**|*int*|train/test|Above grade (ground) living area square feet|
|**Exter Qual**|*int*|trai/test|Exterior material quality|
|**Kitchen Qual**|*int*|train/test|Kitchen quality|
|**Garage Area**|*float*|train/test|Size of garage in square feet|
|**Garage Cars**|*float*|train/test|Size of garage in car capacity|
|**Total Bsmt SF**|*float*|train/test|Total square feet of basement area|
|**1st Flr SF**|*int*|train/test|First Floor square feet|
|**Year Built**|*int*|train/test|Original construction date|
|**total_bath**|*int*|train/test|Amount of total bathrooms|
|**Bedroom AbvGr**|*int*|train/test|Number of bedrooms above basement level|
|**floors**|*int*|train/test|Whether a house is 2 stories or not|
|**Lot Area**|*int*|train/test|The lot size in square feet|
|**Central Air_Y**|*int*|train/test|Central air conditioning present of not|
|**SalePrice**|*int*|train/test|The property's sale price in dollars|


I found that **Michigan**, **Connecticut**, and **Delaware** had the highest SAT participation for both 2017 and 2018, and **North Dakota** consistently had the lowest participation rate. However, I did also discover that despite having consistently the lowest participation rate, **North Dakota** did have the third highest mean SAT total score in 2018.

Through this data I discovered that there was a pretty high but negative correlation between 2018 SAT Participation and 2017 ACT Participation. This is to say, that decreases in ACT Participation in 2017 were fairly correlated with increases in SAT Participation in 2018. I then used outside research to look for reasons why this could be. I analyzed Colorado and Illinois who were greatly affected by this correlation, and discovered that the change in Colorado's and Illinois's SAT and ACT participation can be attributed to the new state contracts with the College Board, incentivizing states to promote the SAT to students.

Given all this information, for the lowest SAT participatory state, **North Dakota**, I would reccommend that College Board seek to increase participation by initiating a state contract, allowing the state schools to administer the exam for free and providing the school with free SAT preparatory resources. I would also recommend advertising SAT competitive rates for local universities as both North Dakota State University and Minot State University, two of the largest universities in North Dakota, are reportedly less competitive to get into when using SAT scores vs using ACT scores.

### Outside Data Sources

 https://blog.prepscholar.com/which-states-require-the-sat
 https://www.adn.com/alaska-news/education/2016/06/30/students-no-longer-need-national-tests-to-graduate/
 https://www.prepscholar.com/sat/s/colleges/North-Dakota-State-University-SAT-scores-GPA 
 https://www.prepscholar.com/sat/s/colleges/Minot-State-University-admission-requirements
