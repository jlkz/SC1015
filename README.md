# Analysis of Plays in the NFL 🏈
## About
This is a SC1015 Mini Project about the factors that affect the outcome of a play in an NFL game. Data of pbp-2020 and pbp-2021 was taken from (http://nflsavant.com/about.php)

In 2021 alone, 1 team on offense will call over 1200 plays across 17 games averaging 70 plays per game.
Time is of the essence as information needs to be relayed to all players involved within 40s between plays.

Coaches therefore face a lot of stress due to the importance of good play calling. They also face tight time constraints. By finding out factors that most affect the outcome of a play, we can aid coaches in making better decisions. 
## Overview
### Data Extraction and Cleaning 
- Concatenating of pbp-2020 and pbp-2021 datasets
- Focusing on Baltimore (BAL) games
- Renaming Categories
- Dropping Rows and Columns that do not contribute to yardage gained
- Reformatting and Combining categories into CombinedPlayType
### EDA and Data Visualisation
- Displaying counts of the variables
- Plotting variables against each other
- Observing initial patterns and anomalies
### Machine Learning
- Encoding Categorical variables
- Applying Random Forest Classifier and intepreting with Treeinterpreter
- Applying XGBoost and interpreting with SHAP explainer
- Interpreting the models and their accuracy
### Data Driven Insights
- Finding features with high importance
- Drawing conclusions
## Contributors
- @Owie963
- @comgood
- @jlkz
## Requirements
The NFL-Plays notebook requires the following to run:
- treeinterpreter
```sh
pip install treeinterpreter
```
- xgboost
```sh
pip install xgboost
```
- shap
```sh
pip install shap
```
## Problem Definition
- Can we help NFL coaches make more informed decisions with various stressors?
- How do different factors affect the outcome of a play?
## Models / Algorithms Used
- Pandas
- Plotly
- Treeinterpreter
- One-Hot Encoding
- Random Forest Classifier
- XGBoost
- SHAP 
## Conclusion
- YardLine, Time, ToGo seem to be of greater importance in affecting the outcome of a failed / decent / great play
- But these factors are too insignificant (low SHAP score) to provide a reliable influence on importance
- Data before upsampling did not perform well
- XGBoost with upsampled data is the most accurate (75.46 %)
- Useful to a certain extent to evaluate which factor is important in affecting the outcome of play
- Although we are able to find the important factors, more has to be done to look into their usefulness to help the coaches decide better
## Learning Outcomes of this Project
- Handling imbalanced datasets using upsampling
- Encoding categorical variables
- Concepts about Precision, Recall, and F1 Score
- Accuracy and reliability of various models
- Understanding of the new XGBoost model
- Finding new visualization methods through TreeInterpreter and SHAP
- Acquiring insights into comparing models
## References
* https://www.baeldung.com/cs/multi-class-f1-score
* https://medium.com/analytics-vidhya/evaluating-a-random-forest-model-9d165595ad56
* https://coderzcolumn.com/tutorials/machine-learning/treeinterpreter-interpreting-tree-based-models-prediction-of-individual-sample
* https://towardsdatascience.com/interpretable-machine-learning-with-xgboost-9ec80d148d27
* https://slundberg.github.io/shap/notebooks/Census%20income%20classification%20with%20XGBoost.html
* https://www.analyticsvidhya.com/blog/2021/06/understanding-random-forest/
* https://xgboost.readthedocs.io/en/stable/python/python_api.html
* https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html
* https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.OneHotEncoder.html
* https://pypi.org/project/treeinterpreter/
* https://xgboost.readthedocs.io/en/stable/parameter.html
* https://shap-lrjball.readthedocs.io/en/latest/generated/shap.summary_plot.html
* https://towardsdatascience.com/explainable-ai-xai-with-shap-multi-class-classification-problem-64dd30f97cea
* https://xgboost.readthedocs.io/en/stable/tutorials/model.html
