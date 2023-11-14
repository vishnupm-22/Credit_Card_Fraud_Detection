
## **BREAST CANCER CLASSIFICATION**

**Problem Statement**:
* The primary objective of this problem is to develop an accurate and efficient credit card fraud detection system that can distinguish between legitimate and fraudulent transactions in real-time.

**Steps** :
* Understanding the data
* EDA
* Handling Imbalanced dataset 
* Model Building and Evaluation

**The dataset contains transactions made by credit card users in 2 days**.
 * It contains only numerical input variables which are the result of a PCA transformation.Features V1, V2, … V28 are the principal components obtained with PCA .
 * Time and Amount are the features that are not transformed by PCA.

**Did exploratory data analysis to gain some insights on data**:
 * **Class Distribution**: bar and pie plot shows that data is highly Imbalanced.
 * **Feature Distribution** : from heat map ,wrt to target column v17,v14,v11 are highly correlated .Visualizing the distribution plots of V17,V14,V11 shows thatthese feature have minimal overlap which significantly helps in classifying the fraud and legit transactions. 
 * **Time-based Analysis** :
    * From both dist plot and hourly-based transactions plot  we can observe the peak hours.
    * daily basis transactions : Unfortunately as data contains only  transactions of 2 days ,there is no much significant difference in No of fraud transactions in 2 days.
* **Amount based Analysis**:
   * Average amount value of fraud transactions in both the days are significantly high as compared to legit transactions.
   * Dist plot : shows that it is right skewed distribution for both transactions.

 Handled Imbalanced dataset using Under-Sampling technique to address the issue of Biased Model & Overfitting.

**Model Building and Evaluation**:
 * Created a pipeline which is a series of data preprocessing steps and models chained together in a specific sequence
 * Preprocessing steps include Normalization technique such as  Robust Scaling which handles outliers.
 * Implemented Multiple Models such as LogisticRegression,SVM &RandomForestClassifier and also evaluated these models by Precision , recall & F1 score.
 * cross-validation of these scores provides a more robust estimate of the model's performance.
 * RFC performes with an accuracy: ,Precision: ,F1 : 


