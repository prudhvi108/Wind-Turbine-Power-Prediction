Wind Turbine Power Prediction 

A machine learning and BI-powered project to predict power output from wind turbines using real-time sensor data.


Built with Python (ML) + Power BI (Visualization)
Use Case: Smart energy forecasting for power grid optimization.

Business Problem :

Energy providers need accurate power output forecasts to optimize grid load, reduce wastage, and improve energy distribution. This project helps predict wind turbine output using environmental and operational sensor data.

Dataset

Source: https://drive.google.com/file/d/1Mh1CS2DJ4PuZAkUmn4Xwy96BBdAoZZK4/view

Size: 900k+ records

Target: Power Output

Key Features:

Wind Speed, Ambient Temperature, Nacelle Temp, Reactive Power, Turbine ID, Timestamp, etc.

Tools & Technologies :
ML / Data	BI / Viz
Python       	    Power BI
Scikit-learn	    DAX & M-query
Pandas, NumPy   	Slicers, Cards, Area Charts
SQLite, SQL     	Scatter plots, KPIs

ML Models and Performance:

Model           	      RMSE	   MAE    R² Score
Linear Regression	      1.969 	1.416 	 0.387
Random Forest	          1.242 	0.923 	 0.756
Neural Network (MLP)  	2.592	  1.993 	-0.063

Best Performer: Random Forest Regressor

Feature Engineering

SQL-based feature selection (WHERE clause filtering)

Timestamp → Month, Hour extraction

Label encoding (Turbine ID)

StandardScaler normalization for ML

Handling 900k+ records using SQLite for performance

Power BI Dashboard Highlights

KPIs:

  MAE: 3.36

  Accuracy: 93%

Visuals Include:

Monthly predicted vs actual power

Feature-wise impact (Wind Speed, Temperature)

Scatter plot: Wind Speed vs Output

Filters for turbine_id & month

Key Insights :

Wind speed is the most critical factor for power prediction (from feature importance).

March–May show higher predicted outputs.

Predictive accuracy holds up well despite weather fluctuations.

Power output trends align closely with seasonal wind patterns.

How to Use :

Clone the repo

git clone https://github.com/your-username/Wind-Turbine-Power-Prediction.git


Install dependencies

pip install -r requirements.txt


Run notebook

jupyter notebook notebooks/Turbine_Prediction_Model.ipynb


Open Dashboard

Use Power BI Desktop → Open `dashboard/Wind_Turbine_Performance_Dashboard.pbix`
