
## **CREDIT CARD FRAUD DETECTION**

**Problem Statement**:
* The primary objective of this problem is to develop a credit card fraud detection system that can distinguish between legitimate and fraudulent transactions in real-time.

**Steps** :
* Understanding the data
* EDA & feature selection
* Handling Imbalanced dataset 
* Model Building and Evaluation

**You can find the dataset from below link** :  [credit_card_dataset](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)

**The dataset contains transactions made by the credit card users in 2 days**.
 * It contains only numerical input variables which are the result of a PCA transformation.Features V1, V2, … V28 are the principal components obtained with PCA .
 * Time and Amount are the only features that are not transformed by PCA.

Then checked for both null and duplicate values, and found no null values are present. But there are 1000 duplicate values, which were deleted from the dataset in order to overcome the disadvantage of overfitting if handeled not properly.


**Did exploratory data analysis to gain some insights on data**:
 * **Class distribution**: plotted bar and pie plot to show that data is highly Imbalanced.
 * **Correlation Analysis** :
   Plotted the correlation heatmap to know any columns are highly correlated. Found out that there are around 11 columns which are having pearson's correation index minimum of 0.80. Then deleted all of them and left with only those which are highly correlated.

Analyzed time and amount feature to identify any patterns and behaviours associated with fraud.plotted the count plot by simply grouping data by hour and count transactions for legitimate and fraudulent cases & observed the peak hours where fraud transactions are more at that specific time.
Also,Plotted the average transaction value for both legitimate and fraudulent cases by grouping the data by days and found avg transaction value for fraudulent cases are significantly high than in legitimate cases.


Handled Imbalanced dataset using Under-Sampling technique to address the issue of Biased Model & Overfitting.

Checked for any outliers present in each of the columns and found out that there are significant number of outliers in most of the columns, so we can use Robustscaler for feature Scaling before the model training

**Model Building and Evaluation**:
 * Created a pipeline which is a series of data preprocessing steps such as robust scaler and models chained together in a specific sequence
 * Implemented Multiple Models such as LogisticRegression,SVM &RandomForestClassifier and also evaluated these models by Precision , recall & F1 score.
 * cross-validation of these scores provides a more robust estimate of the model's performance.
 * RFC performs better  with an average scores of : _Accuracy: _0.9368, _Precision: _0.9613, _Recall score: _0.9094, _F1 score: _0.9326
 * LogisticRegression performed with an average scores of : _Accuracy: _0.9275, _Precision: _0.9696, _Recall score: _0.8796, _F1 score: _0.9208 
 * Support Vector Machine performed with an average scores of : _Accuracy: _0.9171, _Precision: _0.9613, _Recall score: _0.9094, _F1 score: _0.9326


