# 🏠 House Rent Prediction

## 📌 Project Overview
House Rent Prediction is a machine learning project that estimates rental prices of houses based on features such as location, size, furnishing status, and tenant preferences.

The project builds and compares multiple regression models to determine the most accurate approach for predicting rent, making the process more data-driven, transparent, and reliable for both landlords and tenants.

---

## 📊 Dataset
The dataset is loaded from:
data/House_Rent_Dataset.csv


### Key Features:
- BHK (number of bedrooms)
- Rent (target variable)
- City
- Area Type
- Furnishing Status
- Tenant Preferred
- Point of Contact
- Area Locality

### Data Preprocessing:
- Removed irrelevant columns: Area Locality, Posted On, Floor
- Standardized categorical inconsistencies (e.g., Bachelors/Family → Both)

---

##  Exploratory Data Analysis (EDA)
The dataset was explored using:
- `.info()` and `.describe()` for structure understanding
- Null value analysis
- Visualizations:
  - Bar plots (Rent vs Furnishing Status)
  - Scatter plots (Rent vs City, BHK)
  - Correlation heatmap

###  Insights from Correlation Heatmap
- BHK and Bathroom show strong correlation (**0.73**) → indicates larger houses tend to have more bathrooms
- Size is strongly related to BHK (**0.68**) and Bathroom (**0.66**)
- Type and Contact also show moderate correlation (**0.55**)
- City has weak to moderate relationships with most features

---

##  Data Preprocessing
- Label Encoding for categorical variables
- Outlier removal using IQR method
- Feature scaling using StandardScaler
- Train-test split: 80% training, 20% testing

---

## 🤖 Machine Learning Models Used
- Linear Regression
- Support Vector Regressor (SVR - Linear Kernel)
- Decision Tree Regressor
- Random Forest Regressor

---

## 📈 Model Evaluation Results

|         Model            | R² Score |    MSE      |    MAE   |
|--------------------------|--------|---------------|----------|
| Linear Regression        | 0.4964 | 84,569,840.17 | 6,728.35  |
| Support Vector Regressor | 0.1055 | 150,218,091.32| 7,630.68  |
| Decision Tree Regressor  | 0.7039 | 49,733,988.91 | 4,707.83  |
| Random Forest Regressor  | 0.7191 | 47,179,993.48 | 4,558.07  |

---

## 🏆 Best Model
The **Random Forest Regressor** performed the best with:
- Highest R² Score: **0.7191**
- Lowest error values (MSE & MAE)

---

## 🧰 Tech Stack
- Python 🐍
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---

## 🚀 How to Run

### 1. Install Dependencies
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
