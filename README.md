# **Prediction of Stroke**
- **Author:** Evan Yeslow
- **Email** evany24@gmail.com
- **LinkedIn** https://www.linkedin.com/in/evan-yeslow-093388248/

Using different modeling techniques we can try to predict the instance of stroke in patients.

## **[Link to Dataset]

!(https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset/download?datasetVersionNumber=1)
## **Source of Data:**

!(https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset))

## **Data Dictionary:**
- 1) id: unique identifier
- 2) gender: "Male", "Female" or "Other"
- 3) age: age of the patient
- 4) hypertension: 0 if the patient doesn't have hypertension, 1 if the patient has hypertension
- 5) heart_disease: 0 if the patient doesn't have any heart diseases, 1 if the patient has a heart disease
- 6) ever_married: "No" or "Yes"
- 7) work_type: "children", "Govt_jov", "Never_worked", "Private" or "Self-employed"
- 8) Residence_type: "Rural" or "Urban"
- 9) avg_glucose_level: average glucose level in blood
- 10) bmi: body mass index
- 11) smoking_status: "formerly smoked", "never smoked", "smokes" or "Unknown"*
 - *Note: "Unknown" in smoking_status means that the information is unavailable for this patient
- 12) stroke: 1 if the patient had a stroke or 0 if not


## **Stroke Distribution**

![Stroke Instance](https://github.com/evany24/Stroke-Prediction/blob/main/stroke%20distribution.png)

 - The number of people who have strokes is small in comparison to those who do not

## **Stroke by Age**

![Stroke by Age](https://github.com/evany24/Stroke-Prediction/blob/main/stroke%20by%20age.png)

 - Strokes appear to be more common in people who are aged 40 and above

## **Stroke by Smoking Status**

![Stroke by Smoking Status](https://github.com/evany24/Stroke-Prediction/blob/main/smoking%20status%20stroke.png)

- Strokes appear to be evenly distributed among people with different smoking status.
- While it appears there may be more in people who never smoked that may be due to the fact there are more people in the never smoked category

## **BMI vs Age**

![BMI by Age](https://github.com/evany24/Stroke-Prediction/blob/main/bmi%20vs%20age.png)

- There is a minor positive correlation between BMI and Age
- This could mean that as age tends to go up so does BMI and because of this so do instances of stroke

## **Avg Glucose Lvl by Age**

![Average Glucose Level by Age](https://github.com/evany24/Stroke-Prediction/blob/main/glucose%20by%20age.png)

- There is a minor positive correlation between Avg Glucose Level and Age
- Just like BMI with the minor positive correlation avg glucose level appears to go up and so do instances of stroke

## **Model Evaluation**

- The best overall model remained the tuned under sampled logistic regression model.
 -  The model made true positive predictions at a rate of 83% and true negative predictions at 71%. The model is making the correct predictions 72% of the time. While that is not a wonderful score most of the incorrect predictions are stemming from false positives which are less costly.
- Recall for the positive class is at 83% which is close to the highest number from all models. While there were some models that were slightly higher at 85% those other models had more false negatives which are more costly.
