# Improving Low Cost Air Quality Sensor Accuracy with a Simple Machine Learning Model

## Introduction: 
In this project, I wanted to see if a simple machine learning model could make low cost air quality sensor readings more accurate. I used data that compares PM2.5 readings from a low cost sensor with readings from a more accurate reference instrument. Then, I used a simple linear regression model to learn the pattern between their readings and correct the low cost sensor results.

## Dataset:
 I used the SingleSensor_CalibData.csv dataset from Mendeley Data. The data contains hourly readings from a low cost PurpleAir sensor and a more accurate reference instrument collected at the American University of Beirut in Beirut, Lebanon. 
Dataset: [Low cost air quality sensors "PurpleAir" calibration and inter-calibration dataset in the context of Beirut, Lebanon](https://data.mendeley.com/datasets/rh2z7s7btj/2)

## What I did:
First, I loaded and explored the datset to understand what information it contained and checked if there was any missing data. Then, I compared the low cost sensor readings with the reference readings and calculated how inaccurate the low cost sensor was. After that, I split the data into training and testing groups and trained a simple linear regression model to learn the pattern between the low cost and reference readings. Finally, I tested the model on data it had not seen before and compared the original sensor error with the error after using the model.

## Results:
The original low cost sensor had an average error (MAE) of 11.58 uq/m^3 on the test data. After usingthe machine learning model, the MAE decreased to 3.56 uq/m^3, which is about 69% reduction in error. The model also had an RMSE of 4.45 uq/m^3 and R^2 of about 0.80. These results shows that simple ml model was able to make the low cost sensor readings much closer to the refernce readings in this dataset.

## Limitations:
The model was trained using data from specific sensors, so it might not work the same way with the other low cost sensors because different sensors can have different sensors can have different error patterns. Environmental conditions, such as humidity and temperature, might also affect sensors readings. My model only uses the original PM2.5 reading and does not include these environmental factors. Because of this, the results of this project are specific to the sensors and conditions represented in this dataset and might not apply to other sensors or environments.