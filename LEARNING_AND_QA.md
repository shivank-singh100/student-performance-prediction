# Learning & Interview Q/A

## SECTION 1: What I Learned From This Project

- **Data Preprocessing**:
  - Learned importance of checking for null values and duplicated records.
  - Understood how to handle categorical data using pandas `get_dummies` (One-Hot Encoding) to make it suitable for machine learning models.

- **Feature Engineering**:
  - Created a new feature `AverageScore` to simplify the prediction target from three separate scores (math, reading, writing) into a single representative metric.
  - Recognized that creating meaningful features can often improve model interpretability.

- **Regression Modeling**:
  - Applied **Linear Regression** as a baseline model for regression tasks.
  - Learned how to split data into training and testing sets to evaluate performance objectively.

- **Model Evaluation**:
  - Used **R² Score** to determine the "goodness of fit" – i.e., how much of the variance in student scores is explained by the demographic features.
  - Used **MAE (Mean Absolute Error)** to understand the average error in points, which is easier to interpret for non-technical stakeholders.

- **Real-World Understanding**:
  - realized that socio-economic factors (like lunch type and parental education) often have visible correlations with academic performance, highlighting the importance of domain knowledge in data science.

---

## SECTION 2: Interview Q&A (Based on This Project)

### Q1: Why did you choose AverageScore as the target variable?

**Answer**: "Instead of predicting math, reading, and writing scores separately, I aggregated them into a single 'AverageScore' metric. This provides a holistic view of a student's overall academic performance and simplifies the modeling process. In a business context, this is similar to predicting a 'Customer Health Score' based on multiple interaction metrics."

### Q2: Why did you choose Linear Regression?

**Answer**: "I started with Linear Regression because it is simple, interpretable, and computationally efficient. It allows us to easily see the relationship between input features (like 'test preparation course') and the target variable. It serves as an excellent baseline model before trying more complex algorithms like Random Forest or Gradient Boosting."

### Q3: What challenges did you face?

**Answer**: "One challenge was handling categorical variables. The dataset has multiple categorical features like 'race/ethnicity' and 'parental level of education'. I had to ensure they were properly encoded using One-Hot Encoding to avoid the model misinterpreting them as ordinal (ranked) data. Another consideration was feature selection—deciding which features were actually relevant to the prediction."

### Q4: How did you evaluate the model?

**Answer**: "I used two main metrics:

1. **R² Score**: To measure how well the model explains the variance in the data.
2. **Mean Absolute Error (MAE)**: To get a concrete idea of how far off the predictions are on average. For example, an MAE of 5 would mean my prediction is typically off by about 5 points, which is easy to explain to a client."

### Q5: How would you improve this project?

**Answer**: "To improve prediction accuracy, I would try non-linear models like **Random Forest** or **XGBoost**, which might capture complex interactions between features better than a linear model. I could also perform more improved feature engineering, such as grouping 'parental education' into broader categories to reduce noise."

### Q6: What did this project teach you about real data?

**Answer**: "It taught me that data is rarely just numbers—it represents real-world behaviors. For instance, seeing the correlation between 'completed test preparation' and higher scores reinforced that some features have strong causal predictive power. It also emphasized the need to avoid 'Data Leakage'—for example, I had to ensure I didn't verify the model using the individual math/reading scores as inputs since they directly make up the target variable."
