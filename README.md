# Indigo_Block_Hours_Model
This project analyzes flight On-Time Performance (OTP) for the DEL-BOM sector using synthetic data. It calculates block hour overrun, identifies key influencing factors like departure delays, weather, and ATC congestion, and builds a Logistic Regression model to predict on-time arrivals. Visualizations aid in understanding these impacts.

Exploratory Data Analysis (EDA):

EDA is performed to gain deeper insights into the factors affecting OTP. The distribution of block_hour_overrun is visualized and statistically summarized, clearly demonstrating how this metric differs significantly between on-time and delayed flights. This highlights the immediate impact of operational efficiency on punctuality. Further, a correlation analysis is conducted across various flight-related features, including dep_delay_min (departure delay in minutes), weather_index, atc_congestion_index, and load_factor, against the target variable otp_arrival_15m (on-time arrival within 15 minutes). This step helps identify which variables have the strongest linear relationships with flight punctuality.

Predictive Modeling:

A Logistic Regression model is implemented to predict the otp_arrival_15m status. The chosen features for the model include block_hour_overrun, dep_delay_min, aircraft_type, weather_index, and atc_congestion_index. The aircraft_type categorical variable is one-hot encoded to be suitable for the model. The dataset is split into training and testing sets to ensure robust model evaluation. After training, the model's performance is assessed using accuracy score and a detailed classification report, which provides metrics like precision, recall, and F1-score for both on-time and delayed predictions. The model achieved an accuracy of 88%.

Feature Importance and Visualization:

The coefficients from the Logistic Regression model are examined to understand the impact of each feature on the likelihood of a flight being on-time. This reveals that block_hour_overrun has the most significant negative influence on OTP, while certain aircraft types appear to have a positive association with punctuality. The analysis is further supported by visualizations, including a box plot that illustrates the distribution of departure delays across on-time and delayed flights, and a bar chart showing the average OTP for different aircraft types. These visualizations provide clear, actionable insights into the drivers of flight punctuality, which can inform operational improvements and decision-making for airlines and air traffic control.


