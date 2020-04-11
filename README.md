# Project 2 - Ames Housing Data and Kaggle Challenge

### Problem Statement

As a real estate agent, for what reasons would I recommend a 1-story over 2-story house to first-time home buyers?

---

### Overview

For this project, I analyzed housing data from Ames, Iowa in 2010. This data included reports of garage size, lot size, kitchen quality, amount of bedrooms and bathrooms, foundation type, etc., and associated price. I wanted to get a better understanding of the differences in house features between single story and double story homes. I cleaned this data and explored it to get try to identify the highest and practical correlations between housing features and sale price.

### Dataset Features

Full dataset features: https://www.kaggle.com/c/dsi-us-11-project-2-regression-challenge/data

### Model Features
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


### Procedure / Methodology
For this project, I began by looking through the data dictionary and the associated columns in the train.csv data set to get an idea of the possible features I could use for a Linear Regression model.  I started with general data cleaning; I dropped the item with Id 2182, and I checked for missing values and corrupt datatype columns. I found that over 80% of values were missing for the 'Pool QC', 'Fence', 'Misc Feature', and 'Alley', so I decided to drop those columns completely. Next, to account for any foreclosures, I dropped all rows where the Sale Type was labelled as Other.

After cleaning the data, I started my EDA. I decided that I wanted to explore differences in single and double story homes, so I began my analysis with that in mind.  After exploring or engineering a feature, I checked the correlation to SalePrice to assess if the feature was significant enough to be added as a model paramater. I started by engineering a new feature called total_baths that was a sum of the half baths and total baths of a house so that I could more easily compare amount of bathrooms between different houses. I then looked at Street Type to explore price differecens in houses based on paved streets. I then looked at lot area and created a feature called 'big_house' to see if there was a significant price difference in houses with a lot size of over 9,000sqft. I then explored some categorical variables by converting 'Exter Qual', 'House Style', 'Central Air', and 'Kitchen Qual' to numeric variables, comparing their correlation with Sale Price. I then eliminated some rows from the dataset that had outlier numbers for the amount of bedrooms to ensure my model would seem more accurate. After all of this analysis, I decided on the features in the data dictionary above due to their high correlation and relevance to my problem statement. I then log transformed the Sale Price column to normalize its distribution before fitting to my model.

For the modelling process, I began by splitting my 'train' data set into a training set and testing set. I then fit a linear regression model, scored the model and looked at the cross validation score. Unsatisfied with the model, I scaled the data and fit it into a Lasso cv, Ridge, cv, and Elastic Net cv to compare the difference in scores of each regularization technique. I found Lasso to be the most balanced model, but the model was slightly underfit. To create an even better model, I created interaction terms using PolynomialFeatures. I then rescaled and regularized my model, and using Lasso, I ended up with nearly identical training and testing r2 scores of about 0.85. 

I then transformed and scaled the 'test' dataset in the same way that I did for the 'train' set and predicted the Sale Price for each home using my final Lasso Model.

### Conclusion
After analyzing the data and looking for differences between single and double story homes, I found that there were no significant differences between single and double story homes. In fact, single story homes were on average $35,000 less expensive with marginal decreases in garage size and amounts of bathrooms. However, there was a noticeable increase in lot and basement size for single story homes, providing home owners with larger, warmer basement spaces for the winter and larger amounts of land around their home. This was especially noteworthy due to outside research that suggested that home lot areas have been steadily decresing over time, indicating that bigger lot sizes were starting to become a welcomed luxury. With these factors in mind, I would recommend single story homes to potential new home owners.


### Outside Data Sources

https://www.desmoinesregister.com/story/money/business/development/2015/06/20/bigger-homes-smaller-lots-prairie-trail/29010087/

