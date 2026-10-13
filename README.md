# 🏠 Bengaluru House Price Prediction Using Machine Learning

## 📌 Project Overview

This project uses Machine Learning to predict house prices in Bengaluru, India, based on property-related features such as location, total square footage, number of bedrooms (BHK), bathrooms, balcony count, area type, and availability.

The project follows a complete data analysis and machine learning workflow, including data cleaning, feature engineering, Exploratory Data Analysis (EDA), model training, evaluation, and feature importance analysis.

## 🎯 Project Objectives

- Clean and preprocess Bengaluru housing data.
- Analyze property prices and location-based trends.
- Explore the relationship between house prices and property features.
- Perform feature engineering to improve data quality.
- Train multiple regression models to predict house prices.
- Compare model performance using standard evaluation metrics.
- Identify the most influential factors affecting property prices.

## 🛠️ Technologies Used

- **Programming Language:** Python
- **Environment:** Jupyter Notebook / Google Colab
- **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn

## 📊 Dataset Features

The project uses the following property-related features:

- `area_type` — Type of property area
- `availability` — Property availability status
- `location` — Location of the property
- `total_sqft` — Total property area in square feet
- `bhk` — Number of bedrooms, halls, and kitchens
- `bath` — Number of bathrooms
- `balcony` — Number of balconies
- `price` — House price in lakhs

**Target Variable:** `price`

## 🧹 Data Cleaning and Preprocessing

The notebook includes the following data preparation steps:

- Dataset inspection and summary statistics
- Missing-value analysis and treatment
- Removal of the `society` column
- Extraction of BHK values from the `size` column
- Conversion of square footage ranges into numerical values
- Handling missing bathroom and balcony values using median imputation
- Removal of the original `size` column
- Filtering properties with very small total areas
- Feature engineering using `sqft_per_bhk`
- Calculation of `price_per_sqft`
- Removal of derived features from the model inputs to avoid direct target leakage
- One-hot encoding of categorical features

## 📈 Exploratory Data Analysis (EDA)

The project explores housing patterns through visualizations such as:

- House price distribution
- House price versus total square footage
- Price comparison by BHK
- Price comparison by number of bathrooms
- Top 15 locations by property count
- Top 15 locations by average house price
- Price per square foot distribution
- Correlation heatmap of numerical features
- Actual versus predicted house prices
- Comparison of regression model RMSE scores
- Feature importance analysis

These visualizations help understand how property characteristics and location relate to house prices.

## 🤖 Machine Learning Models

Three regression algorithms are implemented:

### 1. Linear Regression
Used as a baseline model to estimate the relationship between property features and house prices.

### 2. Decision Tree Regressor
Uses decision-tree rules to model nonlinear relationships between property characteristics and prices.

### 3. Random Forest Regressor
Combines multiple decision trees to generate predictions and capture more complex patterns in the housing data.

## 📏 Model Evaluation

The models are evaluated using:

- **MAE (Mean Absolute Error):** Average absolute difference between actual and predicted prices.
- **RMSE (Root Mean Squared Error):** Penalizes larger prediction errors more heavily.
- **R² Score:** Measures how much variation in house prices the model explains.

The notebook uses an 80/20 train-test split and compares the three models using these metrics.

## 🏆 Results

According to the recorded notebook results, **Random Forest Regressor** performed best among the three evaluated models.

| Metric | Random Forest |
|---|---:|
| MAE | 31.996 |
| RMSE | 86.945 |
| R² Score | 0.6356 |

The model achieved an R² score of approximately **63.56%**, indicating that it explained around 63.56% of the variation in house prices in the test dataset.

Feature importance analysis identified total square footage as the most influential feature, followed by location, number of bathrooms, BHK, and availability status.

*Note: These results are based on the notebook's recorded outputs and may vary when the notebook is rerun.*

## ⚙️ Installation and Setup

### 1. Clone the repository

```bash
git clone <YOUR_REPOSITORY_URL>
cd <YOUR_REPOSITORY_FOLDER>
```

### 2. Install the required libraries

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### 3. Prepare the dataset

Place `Bengaluru_House_Data.csv` in your project directory.

Update the dataset-loading code to use a relative path:

```python
import pandas as pd

df = pd.read_csv("Bengaluru_House_Data.csv")
```

### 4. Run the notebook

```bash
jupyter notebook
```

Open `Bengaluru_House_Data.ipynb` and execute the cells in order.

## 📁 Repository Structure

```text
Bengaluru-House-Price-Prediction/
│
├── Bengaluru_House_Data.ipynb
├── Bengaluru_House_Data.csv
└── README.md
```

## 🚀 Future Improvements

- Hyperparameter tuning for improved model performance
- Cross-validation for more reliable evaluation
- Outlier detection and location-based price analysis
- Feature selection and explainability
- A web application for interactive house price predictions
- Deployment using Flask or Streamlit
- Testing on new and unseen housing data

## ⚠️ Disclaimer

This project is intended for educational and analytical purposes. Predicted prices are estimates and should not be treated as guaranteed market values or professional property valuations.

## 👨‍💻 Author

**Ariyan Khan**

B.Tech — Computer Science Engineering

Interested in Data Science, Machine Learning, and Artificial Intelligence.
