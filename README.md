# Customer-Relationship-Prediction
The KDD cup 2009 is a marketing problem with the goal of identifying
data mining techniques. The task was to build upon Customer
Relationship Management (CRM) which is a key element of modern
marketing strategies. The large marketing databases from the French
Telecom company Orange had three main targets: to predict the
propensity of customers to switch provider (churn), buy new products or
sale services (appetency), or buy upgrades or add-ons proposed to them
to make the sales more profitable (up-selling).

## Data
The dataset consisted of 50000 values in the small dataset. It consisted
of a subset of 230 variables, 40 of which were categorical. The key
challenges in this dataset were its heterogeneity, large missing values
and a large number of unique categories for each categorical variable.
The ROC AUC score was used as the scoring parameter to test all
models against.

## Models Used
- XGBoostClassifier
- GradientBoostClassifier
- RandomForestClassifier
- ExtraTreesClassifier
- Neural Network With Entity Embedding

## Results
From the above classification algorithms, it is evident that Cost weighted
XGBoost did the best job on comparing the ROC AUC scores. The score
is still lower than the winners’ score of 0.84. But it must be noted that
they worked on the large dataset which was a lot easier to handle than
the smaller one in terms of feature engineering and selection.
![roc and prc curves](https://github.com/Wangsherpa/Customer-Relationship-Prediction/blob/main/image/roc_prc_image.png)

## Conclusion:
We successfully trained three baseline models and 4 classification
models on the KDD Cup 2009 challenge dataset. While the dataset was
challenging in terms of pre-processing and model hyper parameter
tuning, it gave us the opportunity to work on multiple facets of data
analysis that one can ask for in just a single dataset. We do believe that
several other things could have been done such as discretization of the
data as seen in the histogram plots, downsampling of the majority class,
rigorous feature selection using backward/forward feature selection and
the use of boosting algorithms such as AdaBoost and CatBoost. We also
believe that training on the data with just the selected features from
feature importance could have given us a better idea about the
underlying collinearity and if our models even took care of it. There is
much to be done but alas, time is never enough!

## References
References
1. The 2009 Knowledge Discovery in Data Competition (KDD Cup
2009)Challenges in Machine Learning, Volume 3
http://www.mtome.com/Publications/CiML/CiML-v3-book.pdf

## About the repository files:
There are four important files:
- [KDD_2009_data_preprocessing.ipynb](https://github.com/Wangsherpa/Customer-Relationship-Prediction/blob/main/KDD_2009_data_preprocessing.ipynb) - contains all preprocessing steps
- [BaselineModels.ipynb](https://github.com/Wangsherpa/Customer-Relationship-Prediction/blob/main/BaselineModels.ipynb) - contains all baseline models
- [model_training_and_evaluation.ipynb](https://github.com/Wangsherpa/Customer-Relationship-Prediction/blob/main/model_training_and_evaluation.ipynb) - contains training and evaluation of different models
- [requirements.txt](https://github.com/Wangsherpa/Customer-Relationship-Prediction/blob/main/requirements.txt): specifies what python packages are required to run this project.

There are also data and models folder which contains preprocessed data and trained model weights.

