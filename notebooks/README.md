This project focuses on analyzing and optimizing energy consumption in a smart IoT-enabled home using a combination of **Power BI dashboards**, **machine learning models**, and **advanced anomaly detection techniques**.<br><br>


### 📈 Power BI Dashboard Insights

* **Room-wise Consumption Patterns**:

  * **Bedrooms** show peak energy usage at night, primarily due to AC or fan usage.
  * **Kitchen** sees spikes in the morning and evening aligned with cooking times.
  * **Living Room** consumption rises during weekends and evenings, likely linked to entertainment systems.
  * **Bathrooms** have low but predictable usage, mainly from geysers and exhaust fans.

* **Environmental Impact**:

  * Indoor conditions (temperature, humidity) are generally stable and better than outdoor AQI, indicating good insulation or air filtration.
  * These environmental factors influence appliance operation, particularly cooling systems.

* **Optimization Opportunities**:

  * Aligning appliance use with occupancy
  * Reducing idle power drain
  * Implementing smart scheduling or sensor-triggered automation<br><br>
    

### 🤖 Model-Based Energy Prediction (Python Code #1)

A machine learning pipeline was developed to predict total energy consumption using features from all rooms. Key steps:

* **Preprocessing**:

  * Cleaned and standardized room-wise energy data
  * Generated a correlation heatmap to assess feature relationships

* **Models Used**:

  * Linear Regression, Random Forest, Gradient Boosting
  * Support Vector Regressor, K-Nearest Neighbors
  * MLP Neural Network

* **Evaluation Metrics**:

  * **R² Score**, **Mean Squared Error**, and **Accuracy (based on MAPE)**
  * Visualization of actual vs. predicted, feature importance, and residuals

* **Forecasting with Prophet**:

  * Time series forecast for next 30 days
  * Anomaly detection using confidence interval breaches<br><br>



### ⚠️ Anomaly Detection (Python Code #2)

Three techniques were applied for robust anomaly detection in energy consumption:

1. **Z-Score Method**

   * Flags outliers in `Total_Energy_kWh` beyond ±2.5 standard deviations.

2. **Isolation Forest**

   * Identifies multivariate anomalies using unsupervised learning over all room features.

3. **Prophet-Based Residual Detection**

   * Forecasted energy trends using Prophet
   * Detected anomalies from residuals (error z-score > ±2)

* **Consensus Detection**:
  Points flagged by at least two methods were marked as final anomalies for higher reliability.

* **Visualization**:
  Plots were generated for each method and a combined consensus anomaly chart.
