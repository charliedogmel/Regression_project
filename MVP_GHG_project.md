# Analysis of Greenhouse Gas Emissions

#### Melissa Cooper

The goal of this project is to analyze and interpret greenhouse gas emissions by countries over ten years and to see how factors like area, population, poverty level, and energy production/consumption relate to emissions.

To start, I used web scraping to gather country data from 2018. I downloaded emissions data in csv format. 

Initial modeling on training data shows ridge regression performing best.

`Linear Regression val R^2: 0.847
 Ridge Regression val R^2: 0.852
 Degree 2 polynomial regression val R^2: -55.928`

Cross-validation confirms this:

`Linear Regression cross validation R^2:  0.8875504801582187
 Ridge Regression cross validation R^2:  0.8917781738718029`

However, the test data scores much lower:

`Linear Regression test R^2: 0.692
 Ridge Regression test R^2: 0.690`

Although, these values change with different random states on the train/test split. The values shown imply overfitting while previous values (with a much lower random state) imply that there are some outliers. Feature engineering, scaling, and hyperparameter tuning will be utilized moving forward, as well as filling in nine more years of data.














