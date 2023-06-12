# **Prediction of Stroke**
- **Author:** Evan Yeslow
- **Email** evany24@gmail.com
- **LinkedIn** https://www.linkedin.com/in/evan-yeslow-093388248/

Using different modeling techniques we can try to predict the instance of stroke in patients.

## **Source of Data:**
![sales_prediction-2023.csv](https://github.com/evany24/Predictions-of-Product-Sales/blob/main/sales_predictions_2023.csv)

## **Data Dictionary:**

![data dictionary](https://github.com/evany24/Predictions-of-Product-Sales/blob/main/data%20dictionary.png)

# **Exploratory Data Analysis**:
- An exploratory data analysis was done on the data. Boxplots and histograms were created to help understand distributions of numeric data, while barplots were created for categoric data
- Both univariate and multivariate graphs were created for EDA.

![Item Fat Content Distribution](https://github.com/evany24/Predictions-of-Product-Sales/blob/main/Item%20Fat%20Content%20Distribution.png)

 - This plot shows the distribution of items sold by their fat content. The items were grouped into 2 categories, Low Fat and Regular.

# **Explanatory Data Analysis**:

## **Questions:**

**How does Item MRP affect Item Outlet Sales?**

![Item MRP vs Item Outlet Sales](https://github.com/evany24/Predictions-of-Product-Sales/blob/main/Item%20MRP%20vs%20Item%20Outlet%20Sales.png)

 - There is a postive correlation between Item MRP and Item Outlet Sales which means as Item MRP increases so do Item Outlet Sales.

**Is there a correlation between Item Visibility and Item Outlet Sales?**

![Item Visibility vs Item Outlet Sales](https://github.com/evany24/Predictions-of-Product-Sales/blob/main/Item%20Visibility%20vs%20Item%20Outlet%20Sales.png)

 - There is a slightly negative correlation between Item Visibilty and Item Outlet Sales. This means that as Item Visibility increases the Item Outlet Sales decrease. This correlation is opposite but much smaller in comparison to the correlation of Item MRP on Item Outlet Sales.

### **Correlation can be visualized using this heat map:**

![Product Sales Correlations.png](https://github.com/evany24/Predictions-of-Product-Sales/blob/main/Product%20Sales%20Correlations.png)

**What Item Types have the highest and lowest sales?**

![Item Outlet Sales by Item Type](https://github.com/evany24/Predictions-of-Product-Sales/blob/main/Item%20Outlet%20Sales%20by%20Item%20Type.png)

 - Fruits and vegetables have the highest Item Outlet Sales and are 15.17% of all sales followed by Snack Foods at 14.70% and Household items at 11.06%. Breakfast items and Seafood items have the lowest Item Outlet Sales with 1.25% and 0.80% respectively.

**Which Outlet Size has the highest and lowest sales?**

![Item Outlet Sales by Outlet Size](https://github.com/evany24/Predictions-of-Product-Sales/blob/main/Item%20Outlet%20Sales%20by%20Outlet%20Size.png)

 - Medium size stores have the highest item sales accounting for 40.29% of all sales. Next are small stores with 24.56% followed by uncategorized stores at 23.63%. The large stores account for only 11.52% of total item sales.

**What Outlet Types having the highest and lowest sales?**

![Item Outlet Sales by Outlet Type](https://github.com/evany24/Predictions-of-Product-Sales/blob/main/Item%20Outlet%20Sales%20by%20Outlet%20Type.png)

 - Supermarket Type 1 stores have the highest item sales accounting for 69.48% of total sales. There is a large drop off with Supermarket Type 3 store sales at 18.58%, Supermarket Type 2 store sales at 9.96% and lastly grocery store sales at 1.98%

**What is the comparison of Item Outlet Sales when looking at Item Fat Content?**

![Item Outlet Sales by Item Fat Content](https://github.com/evany24/Predictions-of-Product-Sales/blob/main/Item%20Outlet%20Sales%20by%20Item%20Fat%20Content.png)

 - Low Fat item sales are almost double that of regular fat items. Low Fat items account for 64.03% of total item sales while Regular items account for only 35.97%

## **Summary of analysis.**

- Low Fat items are selling much better than Regular Fat items.
- Item MRP has a very strong link to higher total item sales
- Item visibility does not have a strong effect on total item sales
- Fruits and vegetables and snack food have the highest sales. Breakfast and Seafood items may need restructering techniques to bring sales up.

## **Machine Learning:**
- A linear regression model and a decision tree model were used to predict Item Outlet Sales.

## **Model evaluations and metrics**

- Linear Regression Model on testing data:
  - MAE: 804.2645 
  - MSE: 1,194,403.5311 
  - RMSE: 1,092.8877 
  - R2: 0.5671
  
- Final Decision Tree Model on testing data:
  - MAE: 738.3556 
  - MSE: 1,118,187.9463 
  - RMSE: 1,057.4441 
  - R2: 0.5947

## **Model Recommendations:**

  - The Decison Tree is the better model to predict Item Outlet Sales.
  - The mean value for Item Outlet Sales was ₹2,181.29.
  - The MAE for Item Outlet Sales was ₹738.36 which makes the error 33.85%.
  - THE MSE and RMSE are slightly lower for the decision tree model, meaning that the decision tree model may be handling any higher outliers in check.
  - The R2 score of close to 60 percent for the decision tree model also beats out the 55 percent R2 score for the linear regression model. This higher score while not a great way to explain the decision tree model being much better helps its validity.
