# 🏡 RealtyScope
### Advanced Real Estate Analytics & California Housing Price Prediction

**Transforming Housing Data into Meaningful Insights Through Machine Learning**

![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Machine Learning](https://img.shields.io/badge/Machine-Learning-00BFA6?style=for-the-badge)
![Scikit Learn](https://img.shields.io/badge/Scikit--Learn-Regression-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![Data Science](https://img.shields.io/badge/Data-Science-2563EB?style=for-the-badge)

---

## 🌟 Project Overview

**RealtyScope** is an end-to-end Data Science and Machine Learning project designed to analyze California housing data, uncover influential housing characteristics, and predict median house values through statistical modeling and intelligent analytics.

Rather than focusing exclusively on conventional regression, RealtyScope combines **exploratory data analysis, automated data quality assessment, feature engineering, regression model comparison, explainable machine learning, interactive dashboards, and live predictions** into a unified Jupyter Notebook experience.

The project demonstrates how raw housing data can be transformed into interpretable insights and predictive models using a structured machine learning workflow.

> **Our Vision:** Make housing data easier to explore, understand, and predict through transparent, data-driven intelligence.

---

## 🚀 Key Features

###  1. Interactive Real Estate Analytics Dashboard

Explore California housing data through interactive visualizations and dynamic filters.

- Interactive Plotly visualizations
- Ocean proximity filtering
- Median income filtering
- Housing value distribution analysis
- Dynamic housing statistics
- Interactive charts with zoom and hover functionality

###  2. Intelligent Data Quality Analyzer

Automatically examine dataset quality before model development.

- Missing value detection
- Duplicate record analysis
- Data type inspection
- IQR-based outlier detection
- Dataset completeness scoring
- Automated data quality recommendations

###  3. ML Model Battle Arena

Compare multiple regression algorithms through a visual model leaderboard.

**Models implemented:**

- Ordinary Least Squares (OLS) Regression
- Ridge Regression — L2 Regularization
- Lasso Regression — L1 Regularization

**Performance metrics:**

- Root Mean Squared Error (RMSE)
- Mean Absolute Error (MAE)
- R² Score

Includes interactive model comparison charts and performance rankings.

###  4. Explainable AI (XAI)

Understand how different housing characteristics influence predictions.

- Regression coefficient analysis
- Feature importance visualization
- Positive and negative feature contributions
- Interpretable linear model explanations

The explanations describe model behavior and do not establish causal relationships.

###  5. California Housing Intelligence Map

Explore geographical housing patterns through interactive mapping.

- Latitude and longitude visualization
- Geographic housing value distribution
- Population-based marker sizing
- Interactive location exploration
- Ocean proximity insights

###  6. Live Housing Price Prediction Simulator

Generate predictions using a trained regression model.

**User-controlled inputs include:**

- Median income
- Housing median age
- Total rooms and bedrooms
- Population and households
- Latitude and longitude
- Ocean proximity

The simulator automatically applies feature engineering and preprocessing before producing a predicted median house value.

**Note:** Predictions represent historical district-level median house values rather than current individual property prices.

---

##  Dataset Information

**Dataset:** California Housing Dataset

**Source:** [California Housing CSV — GitHub](https://raw.githubusercontent.com/ageron/handson-ml2/master/datasets/housing/housing.csv)

| Attribute | Details |
|---|---|
| Dataset file | `housing.csv` |
| Total records | 20,640 |
| Original columns | 10 |
| Prediction target | `median_house_value` |
| Problem type | Supervised Regression |
| Data format | CSV |

### Dataset Features

| Feature | Description |
|---|---|
| `longitude` | Geographic longitude |
| `latitude` | Geographic latitude |
| `housing_median_age` | Median housing age |
| `total_rooms` | Total rooms in the district |
| `total_bedrooms` | Total bedrooms in the district |
| `population` | District population |
| `households` | Number of households |
| `median_income` | Median income in dataset units |
| `ocean_proximity` | Location relative to the ocean |
| `median_house_value` | Target median house value |

---

##  Machine Learning Workflow

```text
               CALIFORNIA HOUSING DATASET
                          |
                          v
                DATA QUALITY ANALYSIS
                          |
                          v
               EXPLORATORY DATA ANALYSIS
                          |
                          v
                  FEATURE ENGINEERING
                          |
                          v
                 TRAIN / TEST SPLIT
                          |
                          v
              PREPROCESSING PIPELINE
              |                   |
       Median Imputation     One-Hot Encoding
       Standard Scaling      Categorical Features
              |                   |
              +---------+---------+
                        |
                        v
                REGRESSION MODELS
              /         |         \
             v          v          v
            OLS       RIDGE       LASSO
             \          |          /
              +---------+---------+
                        |
                        v
                  GRIDSEARCHCV
                        |
                        v
                 MODEL EVALUATION
                RMSE | MAE | R²
                        |
                        v
               EXPLAINABLE ANALYTICS
                        |
                        v
                LIVE PRICE PREDICTION
```

---

##  Technology Stack

| Category | Technologies |
|---|---|
| Programming | Python |
| Development Environment | Jupyter Notebook |
| Data Manipulation | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn, Plotly |
| Machine Learning | Scikit-learn |
| Statistical Analysis | Statsmodels |
| Interactive Controls | ipywidgets |
| Model Optimization | GridSearchCV |

---

##  Feature Engineering

RealtyScope creates additional housing characteristics to improve the model's representation of the dataset.

**Engineered features:**

1. Rooms per Household
2. Bedrooms per Room
3. Population per Household
4. Income × Housing Age Interaction

These features capture additional relationships between housing characteristics.

Missing values and infinite ratios are handled through preprocessing.

---

##  Model Training & Evaluation

The dataset is divided into:

- **80% Training Data:** 16,512 records
- **20% Testing Data:** 4,128 records

### Regression Algorithms

**OLS Regression**

Establishes a baseline linear relationship between housing characteristics and median house values.

**Ridge Regression**

Uses L2 regularization to reduce coefficient magnitude and improve stability when predictors are correlated.

**Lasso Regression**

Uses L1 regularization, allowing some feature coefficients to become zero.

### Hyperparameter Optimization

GridSearchCV performs five-fold cross-validation to tune Ridge and Lasso regularization strengths.

### Model Evaluation

Models are assessed using RMSE, MAE, and R².

Additional diagnostics include:

- Actual vs Predicted visualization
- Residual distribution
- Residuals vs Predicted Values
- Housing price cap investigation

Model selection should use training-set cross-validation, with the held-out test set reserved for final performance reporting.

---

##  Installation & Setup

### Step 1 — Clone the Repository

```bash
git clone https://github.com/rohanbhowm25308/RealtyScope.git
cd RealtyScope
```

### Step 2 — Create a Virtual Environment (Optional)

```bash
python -m venv venv
```

Activate on Windows:

```bash
venv\Scripts\activate
```

Activate on macOS/Linux:

```bash
source venv/bin/activate
```

### Step 3 — Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn plotly ipywidgets statsmodels notebook
```

### Step 4 — Download the Dataset

Download [housing.csv](https://raw.githubusercontent.com/ageron/handson-ml2/master/datasets/housing/housing.csv) and place it in the project directory.

### Step 5 — Launch Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
RealtyScope.ipynb
```

Execute the notebook cells sequentially using **Run All**.

---

##  Project Highlights

- End-to-end machine learning pipeline
- Automated data quality analysis
- Exploratory statistical analysis
- Correlation and VIF-based multicollinearity analysis
- Advanced housing feature engineering
- Leakage-aware preprocessing pipelines
- Three regression algorithms
- Five-fold cross-validation and GridSearchCV
- Model performance leaderboard
- Explainable regression coefficients
- Interactive analytics dashboard
- Geographic housing intelligence map
- Live housing value prediction simulator

---

##  Limitations

RealtyScope uses a historical California Housing dataset, so its predictions should not be interpreted as current market valuations.

The dataset contains aggregated housing district information rather than individual property listings.

Some target values are capped near the upper recorded housing value, which can affect model performance.

The project is intended for educational, analytical, and machine learning demonstration purposes.

---

## 👨‍💻 Developed By

**Rohan Bhowmik**

*AI/ML | Data Science | Generative AI | AI Agents | Web Development*

- **GitHub:** [rohanbhowm25308](https://github.com/rohanbhowm25308)
- **LinkedIn:** [Rohan Bhowmik](https://www.linkedin.com/in/rohan-bhowmik-b014473a1)
- **Portfolio:** [Personal Portfolio](https://venerable-lamington-90daf4.netlify.app/)

---

### ⭐ Support the Project

If you find RealtyScope useful, consider giving the repository a star!

**RealtyScope — Explore Data. Understand Patterns. Predict Housing Values.**

*Built with Python • Powered by Machine Learning • Driven by Data Science*

**Developed by Rohan Bhowmik**
