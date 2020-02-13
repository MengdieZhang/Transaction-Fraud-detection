# Transaction-Fraud-detection
#####     By Mengdie Zhang

### Abstract
Anomaly detection can identify of rare items or suspicions, widely applied for fraud detection, structural defect, medical problems detection, and sensor networks detection. In this project, the real-world transactions data from Vesta will be used to fix with dozens of models to obtain an optimized model with high accuracy and low false fraud prediction, which will not just reduce business fraud loss, but also improve the user experience with low false alerts. 

### Introduction
Anomaly detection is a very important topic in data science, which addresses a variety issues in nowadays industries, such as fraud detection in business, fault detection in manufacturing, medical monitoring in health industry, ecosystem disturbance detection and sensor detection.  

For many business owners, how to protect their company from fraudulent activity is one of the greatest concerns. Whether it be from customers or third-party organisations, a good fraud detection will prevent company loss the money, and make the company can be more trusted. 

To build a model for detecting frauds, we need to find the strange patterns of frauds in the data that are against the norm. Anomaly detection is the study of applying different statistical and machine learning techniques to these areas to identify the suspicions by differing significantly from the majority of data.



### Environment 
- Python version: 3.7.4 
- Numpy version: 1.16.4
- Pandas version: 0.25.0 
- Seaborn version: 0.9.0 
- Scikit-learn version: 0.21.2 
- Lightgbm version: 2.2.3
- Xgboost version: 0.90 

### Content:
#### details seen in [Fraud detection](https://github.com/MengdieZhang/Transaction-Fraud-detection/blob/master/Fraud%20detection_final.ipynb)

##### A) Data Source

##### B) Model Selection

##### C) Feature engineering & Model Improvement

##### D) Results and discussion
In this project, the feature engineering is an important part of the job. After EDA, cleaning&wrangling data, three different models were used to fit the data. And LightGBM is choosen as the final model.

After optimising several important parameters and conducting feature engineering, the AUC score for test data reached 0.961 with a very low false positive rate as 0.00116.

While there still have some issues need to be discussed:

- The balance of fn and fp
The issue of this problem: According to the confusion matrix, the recall is little low just 0.5786, which means only 57.86% of total real frauds have been detected in this model. To deal with this problem, we can reduce our threshold to 0.4. The balance of fn and fp is important. If the company prefers to reduce money loss from detection, so the fn should be low. If the company wants improve customer experience, so the fp should be reduced.

when threshold dropped to 0.2, the recall score is increased to 0.6826, while the precision decreased with a higher false positive rate


- Reduce the features
The feature_importance in this project is measured by the numbers of times the feature is used in a model to split. We will selected top 100 features as selected feature. With only top 100 features, the computation time of this model is much faster with a little lower AUC score.

- Dataset without identity file information

Since the model has a very high AUC score before feature engineering, it may cause by including the file named "train_identity" which contains the information from collected by Vesta’s fraud protection system and digital security partners. Thus, we can fit this model with the dataset only from "train_transaction" file to check the performance.

From the above results, we can find there is nearly no change in AUC score and a little difference in confusion matrix. It seems that the data in "train_identity" file nearly has no influence to our model.
