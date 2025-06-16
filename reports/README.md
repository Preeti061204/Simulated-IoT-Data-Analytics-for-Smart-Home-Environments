Here are the key **deductions and insights** drawn from the outputs in the two PDF files:<br><br>

### ✅ **ML Models Evaluation & Forecasting (Output #1)**

1. **Model Performance Varies**:

   * Among all models, ensemble methods like **Random Forest** and **Gradient Boosting** outperformed simpler models like Linear Regression, achieving higher accuracy and better generalization (higher R² values), indicating they capture non-linear patterns in energy consumption more effectively.

2. **Feature Importance**:

   * The most influential features contributing to total energy consumption were identified. Typically, rooms such as the **Kitchen** and **Living Room** had higher feature importance scores, indicating they play a significant role in driving overall energy usage.


3. **Residual Analysis**:

   * Residual plots show how well each model fits the data. Models with **residuals close to zero and evenly scattered** are better. Any systematic pattern or outliers suggest model weaknesses or anomalies in the data.

4. **Forecast Trends**:

   * **Prophet's 7-day forecast** displays expected future energy consumption trends and seasonality. The model captures **daily and weekly cycles**, which can help plan energy-saving strategies during peak usage times.

5. **Anomalies in Forecast**:

   * Points where actual values fall outside the confidence interval in Prophet plots indicate **unexpected behavior or outliers**, which may need further investigation.<br><br>



### ⚠️ **Anomaly Detection (Output #2)**

1. **Z-Score Detection**:

   * A few energy readings are identified as statistical outliers, often corresponding to **extremely high or low energy usage**. These may be due to faulty sensors, unusual appliance use, or external conditions.

2. **Isolation Forest Detection (Unsupervised ML)**:

   * Detects anomalies based on **multivariate patterns** across all rooms. It can capture more complex and subtle abnormal behaviors that Z-Score might miss.

3. **Prophet Residual-Based Detection**:

   * Flags anomalies when there’s a large deviation between actual and forecasted values. Useful for identifying **time-based anomalies** (e.g., unexpected spikes during low-usage periods).

4. **Consensus-Based Detection**:

   * The final combined plot marks anomalies detected by **at least two methods**, increasing confidence in the results. These **consensus anomalies** are most reliable and should be prioritized for action or inspection.
