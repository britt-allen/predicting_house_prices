Problem Statement
----
Create a regression model with the [Ames Housing Dataset](http://jse.amstat.org/v19n3/decock/DataDocumentation.txt) to accurately predict the price of a house at sale. There’s been an increase in user traffic to properties with 3-star accuracy Zestimates. Our goal is to improve [Zestimate accuracy (star rating)](https://www.zillow.com/howto/DataCoverageZestimateAccuracyIA.htm) for areas with 3 stars (Good Zestimate).


## Executive Summary
We cleaned and analyzed 81 features which we engineered by way of dummying, mapping, and Polynomial features. This resulted in a final, 20,706 features which we fed into our LassoCV model. We chose a Lasso model because we knew a large number of features would have the potential of overfitting, therefore, we wanted the harshest method of regularization. 

Our model achieved an R squared of 94% on training data and 86% on unseen data. This means two things: 86% of the variability in the data is explained by our model and our model is overfit. Our final model was not our best model. We, unfortunately, overwrote the features from our best model as the assumption was made that converting all features to numeric and using Polynomial Features would yield even better results which was not the case.

## Recommendations
* Continue to test/learn to improve the model by:
   * Revisiting my initial forward selection process
   * Selecting features highly correlated with Sale Price
   * Creating new ones and checking their correlation
   * Feeding the model and checking the results
   * Keeping track of the features that improve the model and discard (but also track) the features that don't
* We believe more time and the meeting of diverse minds to test and learn will yield better results.
* We also would like more data from other cities in Story county and more data on the neighborhood (e.g. number of schools, school types, prisons/jails in the area, etc.)
   
#### Our presentation can be found [here.](https://docs.google.com/presentation/d/18HFR4V_COfimNcqGskrFQk7IxSU8_tn7iLrRXwrEkTg/edit#slide=id.g49c05edb3f_1_97) I also have [an article featured on Towards Data Science](https://towardsdatascience.com/using-machine-learning-to-predict-home-prices-d5d534e42d38) that walks you through my data science process.
