# Hostel Wi-Fi Speed Prediction  

## Problem Statement  
Hostel Wi-Fi often becomes very slow during certain times of the day due to heavy usage by students.  
The aim of this project is to analyze hostel internet usage data and predict when Wi-Fi will be slow, so that students can choose better time for downloading files, watching videos and submitting assignments.

## Dataset  
Internetusage_Beginnertask03.csv  

The dataset contains internet session logs including:
- Session start time  
- Usage duration  
- Total data transferred  

## Approach  

1. The raw session data was converted into hour-wise internet usage.
2. Total data used per hour was taken as an indicator of Wi-Fi slowness.
3. New features were created such as:
   - Hour of day  
   - Previous 1, 3, 6 and 12 hour usage  
   - Daily average usage  
   - Weekend indicator  
4. A Wi-Fi Load Index (WLI) was created as a smoothed version of congestion to represent how slow Wi-Fi actually feels.
5. A Random Forest regression model was trained to predict the Wi-Fi Load Index.

## Results  

- Model R² Score ≈ 0.67  
- Worst Wi-Fi time: 3 PM – 8 PM  
- Best time for downloading files and watching videos: 2 AM – 6 AM  

## Conclusion  

From this project it was observed that hostel Wi-Fi becomes slow mainly in the evening when most students use the internet for streaming, gaming and online classes.  
The model can reasonably predict Wi-Fi slowness and can help students choose better time for heavy internet usage.
