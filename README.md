# Development of Mobile Application For Daily Air Quality Assessment In Bangkok ---Model Part
City Air แอปพลิเคชันประเมินคุณภาพอากาศรายวันในกรุงเทพมหานคร โดยใช้แบบจำลอง LSTM ในการทำนาย PM2.5 ล่วงหน้า 7 วัน และใช้เทคโนโลยี GIS ในการแสดงผลเชิงแผนที่บน Application
<p align="center"><img src = "https://github.com/user-attachments/assets/f09fc8b2-e8d5-420c-b5b0-d78d04cc42ea"></p>


<p align="center" >
  <a href="#Overview">Overview</a> •
  <a href="#Features">Features</a> •
  <a href="#Knowledge">Knowledge</a> •
  <a href="#Operation">Operation</a> •
  <a href="#getting-started">Getting Started</a> •
  <a href="#Conclusion">Conclusion</a> •
</p>


## Overview
Air is essential for all living beings, but PM2.5 pollution has become a major issue, especially in Bangkok, due to urban expansion, population growth, and changing weather conditions.  The objective of this research is to propose the fine-tune machine learning models which able to forecast 7-Day PM2.5 in Bangkok. 
The model could determine appropriate measures to cope with the haze problem in the future. The Long Short Term Memory models (LSTM), one of the Deep Learning models, was trained using hourly air pollution data from the Pollution Control Department, Thailand, and The Meteorological Department, Thailand. 

## Features
1. Display air quality and PM2.5 levels in Bangkok using data from the Pollution Control Department, presented via ArcGIS software in an Android application.
2. Show daily PM2.5 levels for the user's current location and surrounding areas in Bangkok.
3. Provide detailed health information on how different air pollution levels impact public health.
4. Display PM2.5 trend forecasts for the next 7 days.
5. Allow users to report garbage burning sites or other pollution sources to be displayed on the application's map.

## Knowledge
1. Basic information about PM2.5 dust concentration
2. Deep learning techniques
3. Neural network structure
4. Long-term short-term memory model
5. Long short-Term memory optimizer
6. Theories relating to model occuracy assessment

## Operation
- STEP 1 : **Select Data** (PM2.5, PM10, Wind speed, Pressure, Humidity,Temperature, and traffic )
- STEP 2 : **Manage Data** (Clean Data/Interpolation)
- STEP 3 : **Select Modes** (Compare and Select models GRU and LSTM)
- STEP 4 : **Create App** (Desige and Develop on Android studio)
- STEP 5 : **Connect server** (Database with Android studio and ArcGis Server with Android)
> [!NOTE]
> Steps 4-5 will be included in the content of the GitHub repository: [https://github.com/m/AirCity-FinalProject.]



## Getting Started
To run this app on your jupyter notebook or Google Colab, follow these steps:
1. **Select Data** (PM2.5, PM10, Wind speed, Pressure, Humidity,Temperature, and traffic ) and calculate the daily average <p align="center"><img width = "600" src = "https://github.com/user-attachments/assets/50b8f9ba-0604-44d5-ad16-b4f3b0fe80e2"></p>
2. **Exploratory Data Analysis(EDA) and Clean Data** is the initial step in examining data to select features and clean data.
<p align="center"><img width = "327" src = "https://github.com/user-attachments/assets/93106841-8d4b-4ed6-aeca-447bdacbec1b">  <img width = "250" src = "https://github.com/user-attachments/assets/029617f0-be63-4e35-9404-779dcaea2543"></p>

3. **Data Preparation for Model**
   - method shift : It involves shifting feature values + past target values, Since the feature used in the model is 30 days of historical data to Forecast PM2.5 levels for the next 7 days.
<p align="center"><img src = "https://github.com/user-attachments/assets/f9909dd5-f2b7-43ba-9736-2b69057674a8">

   - scaling : Data transformation using Min-Max Scaler, Since the data range is quite wide, scaling is applied to normalize the values within the range of 0 to 1.
   - Split Data: Train Data 90% , test Data 10%
5. **Create Model** :
We will use the LSTM model from the Keras library, a deep learning framework that runs on top of Google’s TensorFlow. In Keras, the Sequential class is used to create deep learning models, serving as a blank framework where various layers can be added.
6. **Model Evaluation** (Root Mean Squared Error: RMSE, Mean Absolute Error: MAE, Mean absolute percentage error: MAPE)
<p align="center"><img width = "350" src = "https://github.com/user-attachments/assets/e26a8287-c3bd-4aed-bb1a-564908893a82"></p>


## Conclusion
The Long Short-Term Memory models (LSTM), one of the Deep Learning models, was trained using hourly air pollution dato from the Pollution Control Department, Thailand, and The Meteorological Deportment, Thailand. From the experiment results
show that Long shot-Term Memory (LSTM) has the best performance in predictions of AM 25 in 7 days. The best results include PM2.5, PM10, wind speed, Pressure, Humidity, and Temperature. The model performance values are RMSE 8.47, MAE 6.37 and MAPE 25.19%
This research has improved the efficiency of the model to forecast more accurately by choosing Adam optimizer.




