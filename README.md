# README

## Project Overview
This project involves performing data cleaning and preprocessing, conducting both basic and advanced exploratory data analysis (EDA), and building a model to forecast temperature. The dataset contains 41 features and 60218 rows, which provides information about weather conditions, locations, and other environmental factors. 

### Key Tasks:
1. **Data Cleaning and Preprocessing**
2. **Exploratory Data Analysis (EDA)**
3. **Model Building and Evaluation**

---

## Data Cleaning and Preprocessing

### Key Observations:
- **Total number of features (columns)**: 41
- **Total number of rows**: 60218 
- **Number of numerical columns**: 31
- **Number of categorical columns**: 10
- **Missing values**: There are no missing values in the dataset.
- **Duplicates**: There are no duplicate rows present in the dataset.

### Outlier Detection:
As the data is multivariate, **Isolation Forest** was used to detect outliers. This method is well-suited for high-dimensional datasets and helps identify data points that significantly differ from the majority of the data.

---

## Exploratory Data Analysis (EDA)

### Key Observations:
1. **Countries and Locations**:
   - **Unique countries**: 210
   - **Unique locations**: 248
   - **Top 10 countries by count**: 
     - Bulgaria, Indonesia, Sudan, Iran, Thailand, Madagascar, Belgium, Turkey, Bolivia, Vietnam.

2. **Temperature and Latitude**:
   - The **USA** has the highest latitude difference among all countries and contains 308 instances.
   - However, no strong correlation was observed between **temperature** and **latitude** in the data.

### Data Distribution:
- **Pie Charts**: 
  - Pie charts were plotted to visualize the distribution of values in the **categorical columns** such as `moon_phase`, `condition_text`, and `wind_direction`.

- **Correlation Heatmap**:
  - A correlation matrix heatmap was generated to identify relationships between numerical features and visualize their interdependencies.

- **Temperature and Precipitation Distributions**:
  - Distribution plots for temperature (`temperature_celsius`) and precipitation (`precipitation_mm`) were created to understand their spread and central tendencies.

---

## Model Building

### Forecasting Model:
- A **basic ARIMA** model was used for forecasting the `temperature_celsius` variable based on historical data.
- The ARIMA model was evaluated using the following metrics:

  - **Mean Absolute Error (MAE)**: 2.8862
  - **Root Mean Squared Error (RMSE)**: 3.6178

These evaluation metrics provide an understanding of the model’s accuracy in forecasting future temperatures.

### Results:
The ARIMA model shows relatively good performance for temperature forecasting. The low MAE and RMSE values suggest that the model can reasonably predict future temperature values, though further fine-tuning or more advanced models may improve accuracy.

---

## Conclusion:
This project demonstrates the process of cleaning, analyzing, and modeling a weather-related dataset. The ARIMA model provides a basic but effective approach to forecasting temperature. For future improvements, experimenting with more advanced models such as SARIMA, LSTM, or XGBoost could help enhance forecasting accuracy.

---

## Dependencies:
- pandas
- numpy
- matplotlib
- seaborn
- statsmodels
- scikit-learn

---

## How to Run:
1. Clone this repository to your local machine.
2. Install the required dependencies listed above.
3. Run the Python script to perform data cleaning, EDA, and model building.
