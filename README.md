# 🚕 Uber Fare Prediction: Machine Learning Regression Model
## 📌 Project Description
This project focuses on building and evaluating a machine learning regression model to accurately predict the fare of an Uber ride. Using a large dataset of trip records, the model incorporates geospatial data (pickup and dropoff coordinates) and temporal features (time of day, day of the week, month, and year) to capture the key factors influencing ride pricing. The notebook demonstrates a complete end-to-end process, including data cleaning, feature engineering, and model training/prediction.

## Key Features

* **Target Variable:** `fare_amount` (Continuous/Regression).
* **Data Preprocessing:** Handled null values through imputation and dropped redundant columns like `Unnamed: 0` and `key`.
* **Feature Engineering:** Extracted temporal features (hour, day, month, year, day of week) from the `pickup_datetime` field.
* **Technology Stack:** Built primarily using Python and its scientific computing libraries.

## 🛠️ Technologies Used

* **Python**
* **Pandas** (for data manipulation)
* **NumPy** (for numerical operations)
* **Matplotlib** / **Seaborn** (for data visualization - *implied by imports*)
* **Scikit-learn** (or similar ML library for model training - *implied by prediction step*)
## 📊 Dataset

The dataset, `uber.csv`, contains **200,000 records** of Uber trips.

### Key Columns:
| Column Name | Description |
| :--- | :--- |
| `fare_amount` | The target fare in USD. |
| `pickup_longitude` | Longitude of the pickup location. |
| `pickup_latitude` | Latitude of the pickup location. |
| `dropoff_longitude` | Longitude of the dropoff location. |
| `dropoff_latitude` | Latitude of the dropoff location. |
| `passenger_count` | Number of passengers in the ride. |
| `hour`, `day`, `month`, `year`, `dayofweek` | Extracted time features. |
## 🧹 Data Preprocessing

- Removed nulls and outliers
- Filtered unrealistic coordinates and passenger counts
- Converted datetime to useful features: hour, day, month, weekday
- Calculated Haversine distance between pickup and dropoff points

## 🧠 Modeling

- **Algorithms Used**:
  - Linear Regression
  - Decision Tree Regressor
  - Random Forest Regressor
  - XGBoost Regressor
- **Evaluation Metrics**:
  - RMSE (Root Mean Squared Error)
  - MAE (Mean Absolute Error)
  - R² Score

## 📊 Results

| Model               | RMSE   | MAE    | R² Score |
|--------------------|--------|--------|---------- |
| Linear Regression  | 3.05   | 2.12   | 0.67      |
| Random Forest      | 2.16   | 1.42   | 0.83     |
| XGBoost            | 2.20   | 145    | 0.83      |

✅ Random Forest performed best with lowest error and highest R².



## 🚀 How to Run

```bash
git clone https://github.com/mr-akash12/uber-fare-prediction.git
cd uber-fare-prediction
pip install -r requirements.txt
jupyter notebook Uber.ipynb

## 📌 Future Improvements
- Incorporate weather and traffic data
- Use deep learning models (e.g., DNN, LSTM)
- Build a web app using Streamlit or Flask
📬 Contact
**Made with ❤️ by Akash
Feel free to reach out for collaboration or feedback!
**
