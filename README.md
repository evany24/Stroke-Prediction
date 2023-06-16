# **Prediction of Stroke**
- **Author:** Evan Yeslow
- **Email** evany24@gmail.com
- **LinkedIn** https://www.linkedin.com/in/evan-yeslow-093388248/

Using different modeling techniques we can try to predict the instance of stroke in patients.

## **[Link to Dataset]**

(https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset/download?datasetVersionNumber=1)

## **[Source of Data]**

(https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset))

## **Data Dictionary:**
1. id: unique identifier
2. gender: "Male", "Female" or "Other"
3. age: age of the patient
4. hypertension: 0 if the patient doesn't have hypertension, 1 if the patient has hypertension
5. heart_disease: 0 if the patient doesn't have any heart diseases, 1 if the patient has a heart disease
6. ever_married: "No" or "Yes"
7. work_type: "children", "Govt_jov", "Never_worked", "Private" or "Self-employed"
8. Residence_type: "Rural" or "Urban"
9. avg_glucose_level: average glucose level in blood
10. bmi: body mass index
11. smoking_status: "formerly smoked", "never smoked", "smokes" or "Unknown"*
12. stroke: 1 if the patient had a stroke or 0 if not 
 *Note: "Unknown" in smoking_status means that the information is unavailable for this patient

# **Exploratory Data Analysis**:
- An exploratory data analysis was done on the data. Countplots and histograms were created to help understand distributions of numeric data. Countplots were used for categorical data as well.
- The exploratory data analysis allowed us to remove the 'other' feature from the gender column and the 'never_worked' feature in the work type column.
  
## **Stroke Distribution**

![Stroke Instance](https://github.com/evany24/Stroke-Prediction/blob/main/stroke%20distribution.png)

 - The number of people who have strokes is small in comparison to those who do not

# **Explanatory Data Analysis**:

- Plots were made to explain the data before modeling some insights and visuals are as follows:
  
![Stroke by Age, Avg Glucose and bmi](https://github.com/evany24/Stroke-Prediction/blob/main/strokekernelplot.png)

 - As age increases so does instance of stroke. It is occuring mostly in people aged 40 and above.
 - For average glucose level it appears that a large majority of the non stroke class have avg glucose levels between 50 and 150. People who are having stroked have a wide distribution of avg glucose level. There isn't much correlation.
 - For bmi the plot is telling us that there is almost no correlation between this feature and instance of stroke.

## **Stroke by Smoking Status**

![Stroke Distribution over Different Features](https://github.com/evany24/Stroke-Prediction/blob/main/violinplotstroke.png)

- The violin plot allows us to see the distribution of certain features that are having and not having strokes.
 - The first plot shows us that gender does not have much difference in stroke instance.
 - The second plot tells us that hypertension is not occuring in most people who do not have strokes. For stroke patients hypertension is more common but only slightly.
 - The third plot shows heart disease is very similar to hypertension distribution.
 - The fourth plot shows that gender plays a small role in stroke instance, slightly more in males.
 - The 5th plot shows that stroke is occuring in all work types similarly but in children it is occuring at a very small rate.
 - The 6 plot shows us that residence type distribution is extremely similar for rural and urban areas

## **BMI vs Age**

![BMI by Age](https://github.com/evany24/Stroke-Prediction/blob/main/bmi%20vs%20age.png)

- There is a minor positive correlation between BMI and Age
- This could mean that as age tends to go up so does BMI and because of this so do instances of stroke

## **Avg Glucose Lvl by Age**

![Average Glucose Level by Age](https://github.com/evany24/Stroke-Prediction/blob/main/glucose%20by%20age.png)

- There is a minor positive correlation between Avg Glucose Level and Age
- Just like BMI with the minor positive correlation avg glucose level appears to go up and so do instances of stroke

## **Machine Learning:**

- Three main models were used to predict the instance of stroke.
  - Logistic Regression
  - KNN
  - Random Forest
 - These models were tuned using gridsearchcv, SMOTE and by under sampling.

## **Model Evaluation**

![Under Sampled Tuned Logistic Regression Confusion Matrix and False Positive AUC](https://github.com/evany24/Stroke-Prediction/blob/main/tunedlogregmodel.png)
- The best overall model remained the tuned under sampled logistic regression model.
 -  The model made true positive predictions at a rate of 83% and true negative predictions at 71%. The model is making the correct predictions 72% of the time. While that is not a wonderful score most of the incorrect predictions are stemming from false positives which are less costly.
- Recall for the positive class is at 83% which is close to the highest number from all models. While there were some models that were slightly higher at 85% those other models had more false negatives which are more costly.
