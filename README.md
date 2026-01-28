# Student Performance Prediction

## 📌 Project Overview

This project applies **Linear Regression** to predict the **Average Student Score**. The goal is to understand how personal and academic factors—such as parental education, test preparation course completion, and gender—influence a student's performance.

This analysis provides insights that can help educators identify at-risk students and understand the impact of socio-economic factors on education.

## 📊 Problem Statement

Student academic performance is influenced by various internal and external factors. By analyzing these variables, we aim to build a predictive model that estimates a student's average score based on their background information.

## 📂 Dataset Description

The dataset (`StudentsPerformance.csv`) contains the following attributes:

- **gender**: Male / Female
- **race/ethnicity**: Types A, B, C, D, E
- **parental level of education**: e.g., High School, Bachelor's, Master's
- **lunch**: Standard / Free or Reduced
- **test preparation course**: None / Completed
- **math score, reading score, writing score**: Individual subject scores

## 🛠️ Tools & Technologies

- **Python**: Core programming language
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical operations
- **Matplotlib & Seaborn**: Data visualization
- **Scikit-learn**: Machine learning (Linear Regression, Model Evaluation)

## 🔄 Project Workflow

1. **Data Collection**: Loaded dataset from `data/` folder.
2. **Data Cleaning**: Checked for missing values and consistencies.
3. **Feature Engineering**: Created a new target variable `AverageScore` = (Math + Reading + Writing) / 3.
4. **Data Preprocessing**: Converted categorical variables (like gender, race) into numerical form using One-Hot Encoding.
5. **Model Training**: Trained a Linear Regression model on 80% of the data.
6. **Evaluation**: Tested on 20% of unseen data using R² Score and Mean Absolute Error (MAE).

## 📈 Model & Results

| Metric         | Description                                                                       |
| :------------- | :-------------------------------------------------------------------------------- |
| **Model Used** | Linear Regression                                                                 |
| **R² Score**   | Measures how well the independent variables explain the variance in the score.    |
| **MAE**        | Mean Absolute Error - The average difference between predicted and actual scores. |

_Note: Specific result values can be seen by running the notebook._

## 🚀 How to Run the Project

### 1. Locally (VS Code / Jupyter)

1.  **Clone the repository:**

    ```bash
    git clone https://github.com/yourusername/student-performance-analysis.git
    cd student-performance-analysis
    ```

2.  **Launch Jupyter Notebook:**

    ```bash
    jupyter notebook
    ```

3. **Install dependencies:**
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
   ```
4. **Open the notebook:**
Open `notebook/student_performance_prediction.ipynb` and run all cells.

### 2. On Google Colab

Run the notebook directly in your browser (no installation required):

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1wxyuxUOJaaU_QHK6C3ZVLWUQuiqBA7Y1?usp=sharing)

## 🔮 Future Improvements

- Test other algorithms like Decision Trees or Random Forest for potentially better accuracy.
- Perform hyperparameter tuning.
- Add more extensive feature engineering (e.g., binning parental education).

## 🤝 Contributing

Contributions are welcome! If you have suggestions for further analysis or visualizations, please feel free to fork the repo and submit a pull request.

## ✍️ Author

**Shivank Singh**
_Data Science Enthusiast_

## 📄 License

This project is open source and available under the [MIT License](LICENSE).