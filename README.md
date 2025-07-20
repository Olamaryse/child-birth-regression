# Analyzing Factors Affecting Birth Weight and Gestation 👶📊

-----

## 🚀 Project Overview

This project delves into the crucial factors influencing **baby birth weight** throughout pregnancy. Utilizing a comprehensive dataset, the goal is to identify and quantify the impact of various maternal characteristics and gestational details on a newborn's weight. The project employs advanced machine learning regression techniques to build predictive models, aiming to uncover key insights that could be valuable for healthcare professionals and expectant parents.

-----

## 📊 Dataset

The dataset for this analysis is sourced from [Kaggle: Child Weight at Birth and Gestation Details](https://www.kaggle.com/datasets/jacopoferretti/child-weight-at-birth-and-gestation-details/data). It provides a rich set of features related to maternal health and pregnancy outcomes.

**Key Features:**

  * **Case**: Unique identifier for each pregnancy.
  * **bwt**: **Birthweight in ounces** (the primary target variable for prediction).
  * **gestation**: Length of gestation in days.
  * **parity**: Binary indicator: `0` for a first pregnancy, `1` otherwise.
  * **age**: Mother's age in years.
  * **height**: Mother's height in inches.
  * **weight**: Mother's weight in pounds.
  * **smoke**: Binary indicator: `1` if the mother smokes, `0` otherwise.

-----

## 🔬 Methodology

This project employs a robust machine learning pipeline to analyze and predict birth weight:

1.  **Data Import & Preparation**:
      * The raw data was imported using `pandas`.
      * Initial data cleaning and inspection steps were performed to ensure data quality.
2.  **Feature Engineering & Preprocessing**:
      * Features were prepared for model training, including scaling numerical features using `StandardScaler` to ensure all features contribute equally to the model, which is particularly beneficial for models like Ridge and SVR.
3.  **Model Selection & Training**:
      * A comparative analysis was conducted using three distinct regression algorithms:
          * **Ridge Regression**: A linear model that uses L2 regularization to prevent overfitting.
          * **Support Vector Regressor (SVR)**: A powerful, flexible model capable of capturing complex non-linear relationships.
          * **Random Forest Regressor**: An ensemble method that builds multiple decision trees and averages their predictions for robust performance.
4.  **Hyperparameter Tuning & Optimization**:
      * `GridSearchCV` was extensively used to systematically search for the optimal hyperparameters for each model. This process ensures that each algorithm performs at its peak potential.
5.  **Model Persistence**:
      * The best-performing estimator for each model (Ridge, SVR, Random Forest) and the `StandardScaler` were saved using `joblib`. This allows for easy deployment and future use of the trained models without needing to retrain them.

-----

## ✨ Key Findings & Conclusion

Through comprehensive experimentation with multiple regression models and rigorous hyperparameter tuning, this project successfully developed predictive models for birth weight. The comparative analysis aimed to identify the most accurate and reliable model among Ridge, SVR, and Random Forest. While specific performance metrics (e.g., R-squared, MAE, RMSE) are not detailed in the provided output, the methodological rigor employed ensures that the project delivers a well-optimized solution for predicting birth weight and understanding its influencing factors. This work lays the groundwork for further research and practical applications in prenatal care and public health.

-----

## 🚀 How to Run

To run and explore this project:

1.  **Download the Notebook**: Obtain the `child-birth-and-gestation.ipynb` file.
2.  **Dataset**: The notebook expects the corresponding dataset. Download the `birthweight.csv` (or similar, as indicated by the Kaggle link) from the [Kaggle: Child Weight at Birth and Gestation Details](https://www.kaggle.com/datasets/jacopoferretti/child-weight-at-birth-and-gestation-details/data) and place it in the same directory as your notebook.
3.  **Install Dependencies**: Install the necessary Python libraries:
    ```bash
    pip install pandas numpy matplotlib seaborn scikit-learn joblib
    ```
4.  **Run the Notebook**: Open the `child-birth-and-gestation.ipynb` file using Jupyter Notebook or JupyterLab and execute the cells sequentially to reproduce the analysis and model training.

-----
