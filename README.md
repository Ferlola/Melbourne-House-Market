# Melbourne House Market 🏡📊

This project focuses on the analysis,visualization, and prediction of house prices using **data science techniques**, including exploratory data analysis, statistical visualization, and predictive modeling.

The project is divided into **two main files**:
1. **Price prediction and model evaluation**
2. **Exploratory data analysis and visualizations**

---

## 📂 Project Structure
```
├── melbourne_predictions.ipynb # Modeling, training, and evaluation
├── melbourne_graphics.ipynb # Exploratory analysis and visualizations
├── README.md
```
---

## 🔮 Predictive Modeling

This file contains the complete data science workflow, including data preprocessing, feature engineering, model training, hyperparameter optimization, evaluation, and interpretation.

### 1️⃣ Exploratory Model Benchmarking
LazyPredict was used as a **preliminary exploratory benchmarking tool** to quickly evaluate multiple regression models and identify strong candidates for further analysis.

> ⚠️ *LazyPredict is not included directly in the file*, as it was only used during the exploratory phase.

The **top three models** identified were:
1. **LGBMRegressor**
2. **HistGradientBoostingRegressor**
3. **XGBRegressor**

### 2️⃣ Inclusion of CatBoostRegressor
LazyPredict does not include **CatBoostRegressor**. However, after training it with default parameters, it showed **strong performance**, so it was included in the project.

### 3️⃣ Compatibility Issues
During the optimization of **CatBoostRegressor**, compatibility issues appeared because recent versions of CatBoost are **not compatible with Python 3.13**.

👉 **Solution:**  
The environment was downgraded to **Python 3.11**, ensuring full compatibility and stability.

### 4️⃣ Model Optimization and Validation
Hyperparameter optimization was performed as part of the data science workflow to improve generalization and reduce overfitting.

### 5️⃣ Results and Visual Outputs
The predictions file includes:

- 📊 **Metrics comparison table** (Train RMSE, Test RMSE, Test RMSE std, Gap RMSE, Gap RMSE %, Train R², Test R², Gap R²)
- 📈 **Model benchmark plot**:
  - Test RMSE vs Gap % vs Test R²
- 📉 **Learning curve** of the selected best model:
  - **HistGradientBoostingRegressor**
- 🏠 **Final prediction table**, including:
  - Actual prices
  - Predicted prices
  - Minimum, maximum, and average prices of similar houses  
    (based on *suburb* and *number of rooms*)

---

## 📊 Graphics File

This file focuses on **Exploratory Data Analysis (EDA)** as a core step of the data science process, using visualizations to understand patterns, distributions, relationships, and anomalies in the data.

### Included Visualizations

- Sales per day of the week
- House prices depending on the number of rooms
- Total houses sold by number of rooms
- House prices depending on the number of bedrooms
- Total houses sold by number of bedrooms
- Top 10 suburbs with the highest number of house sales
- Top 10 councils with the highest number of house sales
- Houses sold by regions
- House prices by geographical coordinates (Latitude & Longitude)
- Houses sold by sales method
- Houses sold by type of housing
- Outlier detection
- Data frequency distributions
- Price–feature correlation analysis

These visualizations help identify key patterns, trends, anomalies, and relationships between variables.

---

## 🧰 Data Science Stack

### Language
- **Python 3.11.14**

### Main Libraries
- numpy: `2.4.1`
- pandas: `3.0.0`
- scikit-learn: `1.4.2`
- Optuna: `4.7.0`
- CatBoost: `1.2.8`
- XGBoost: `3.1.3`
- LightGBM: `4.6.0`
- matplotlib: `3.10.8`
- seaborn: `0.13.2`

---

## 📌 Conclusions

- **HistGradientBoostingRegressor** was selected as the best overall model due to its balance between performance and generalization.
- The exploratory data analysis provided valuable insights into the structure and behavior of the Melbourne housing market, supporting the modeling decisions.

---

## 📎 Additional Notes

- LazyPredict was used only as an exploratory tool and is not a required dependency.
- The project emphasizes **model stability, interpretability, and predictive performance**.



