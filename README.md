# King’s County Home Sales dataset analysis

Author: GROUP 1

## Project Overview

This project utilizes linear regression analysis to uncover the key features that significantly impact home sale prices and quantify their respective influences.

### Business Problem

A family intending to settle down in King’s County has approached G-One Limited to help them settle on a home that will have the highest resale value. G-One Limited will analyze data on housing prices in King's County to identify key factors impacting housing prices and help our client choose a home. Insights from the analysis will provide our client with valuable guidance for making informed decisions in the housing market in King’s County.

### Data understanding

This project uses the King County House Sales dataset obtained from  `kc_house_data.csv` in the data folder [in this project's GitHub repository](https://github.com/NazraJN/dsc-phase-2-project-v2-3/tree/main/data). The dataset includes comprehensive information on 21,597 residential properties, covering 21 distinct features including the `date a house was sold`, `sale price (prediction target)`, `number of bedrooms`, `number of bathrooms`, `square footage of living space in the home`, `square footage of the lot`, `number of floors (levels) in house`, `whether the house is on a waterfront`, `quality of the view from the house`, `how good the overall condition of the house is`, `overall grade of the house`, among others. Further information on the features of the houses can be found in `column_names.md` and on [King County Assessor Website](https://info.kingcounty.gov/assessor/esales/Glossary.aspx?type=r#g).


### Modelling

To prepare the data for analysis, we follow a systematic approach. First, we import the dataset and the necessary libraries to facilitate the analysis. We then carefully examine the dataset's contents and perform data cleaning procedures to eliminate any missing values and log-transform the price variable to make it more suitable for our analysis.
The project thereafter employs linear regression methods to develop a comprehensive model for predicting house prices. To begin, we create a baseline model using simple linear regression to examine the relationship between `price` and `square foot living` since it has the highest correlation to price.

![correlation](https://github.com/NazraJN/dsc-phase-2-project-v2-3/blob/main/correlation_matrix.JPG)

Subsequent iterations of the model build upon this baseline, gradually incorporating additional feature variables. The final model utilizes multiple linear regression to examine the relationship between price and `sqft_living`, `bedrooms`, `bathrooms`, `waterfront`, `sqft_lot`, `floors`, `yr_built`, `condition`, `grade`, `view`, and `Renovated`. 

By iteratively refining the model, we aim to achieve improved accuracy and robustness in predicting housing prices based on the selected set of features.

### Regression results 

The analysis reveals that certain features have a significant impact on the prices of houses in the dataset. Notably:

* A one-unit increase in square foot living corresponds to a price increase of 0.02%.
* A one-unit increase in the number of bathrooms results in a price increase of 7.91%.
* A one-unit increase in the number of floors corresponds to a price increase of 7.74%.
* Higher grading is associated with higher prices. An excellent grade leads to an 11.94% price increase, while a luxury grade results in a 21.27% increase, and a mansion grade leads to a 22.91% increase.
* A better condition is linked to higher prices. A "good" condition results in a price increase of 1.9%, while a "very good" condition corresponds to an 8.63% increase.
* Houses with better views command higher prices. A good view leads to a 3.52% price increase, a fair view corresponds to an 8.33% increase, and an excellent view results in a 16.55% increase.
* Houses with a waterfront location experience a substantial price increase of 31.51%.

Significantly, the `waterfront`, `grade`, and `view` features contribute the most to higher sales prices.


## Conclusions

The family should consider the following features: 
* Waterfront, as waterfront properties exhibit the highest price values, suggesting their exclusivity and attractiveness to potential buyers
* Higher grading as houses graded as excellent, luxury, or mansion tend to command higher prices, indicating the importance of the overall quality and prestige of a property
* View, as houses with a good view exhibit higher price values compared to those without, emphasizing the desirability of scenic views
* The condition of a house as this plays a crucial role, with houses in “good” or “very good” condition attracting higher prices
* The number of bathrooms and floors, as these features have a notable influence on the price of a house


## Next steps

Our model accurately fits only 65.1% percent of the data. While this is sufficient enough to make observations and insights, it would be beneficial to explore techniques to improve the model's performance and enhance its predictive capabilities. This could involve incorporating additional features or using more advanced modeling techniques. 

Additionally, since the current model does not meet the assumptions of normality and homoscedasticity, further exploration into the normalization and scaling of features might help pass these assumptions. Addressing these assumptions can improve the model's reliability and interpretability.

Finally, further investigation into other potential influential factors affecting housing prices could be valuable. This might include analyzing neighborhood characteristics, proximity to amenities, or economic factors. By incorporating such variables, a more comprehensive understanding of housing price dynamics can be obtained.

Addressing these aspects in future analysis and modeling can yield a more refined and accurate understanding of the factors influencing housing prices.

