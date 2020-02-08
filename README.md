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
- Reduce the features
- Dataset without identity file information
