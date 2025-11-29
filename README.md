🚁 UAV Vibration Analysis After PID Tuning

A complete analysis of UAV vibration patterns using Mission Planner log files, Python (Pandas, SciPy, Matplotlib), and Tableau dashboards.
Old vs New logs were compared to quantify vibration reduction after optimizing PID values.

📌 Key Outcomes
✨ 50% Overall Reduction in Vibration

X-axis: 49% reduction

Y-axis: 43% reduction

Z-axis: 58% reduction

🎯 What Improved?

Reduced frame resonance

Lower IMU noise

Smoother roll/pitch/yaw output

Stabilized acceleration & gyroscope signals

Cleaner altitude vs speed profile

📊 Dashboards & Visualizations
Before PID Tuning (Old Log File)
<img width="1521" height="857" alt="image" src="https://github.com/user-attachments/assets/3398cdc6-f8ed-4648-9ccc-c213f1158ecf" />
<img width="1520" height="855" alt="image" src="https://github.com/user-attachments/assets/9a3ae58c-58f0-4bdc-9f4b-6e9d59be0cc7" />
<img width="1774" height="751" alt="image" src="https://github.com/user-attachments/assets/7a98be71-3cf0-454c-a79a-c9e9d640ea9a" />

After PID Tuning (New Log File)
<img width="1520" height="856" alt="image" src="https://github.com/user-attachments/assets/907ca88b-6de4-4448-bb33-7a9aa3c1740e" />
<img width="1520" height="856" alt="image" src="https://github.com/user-attachments/assets/05f769d5-90bf-439a-9d4d-6ef4feb0a51e" />
<img width="1778" height="749" alt="image" src="https://github.com/user-attachments/assets/591a160d-09fb-4219-ba71-2ff8ce89b89c" />

🔬 Data Processing Workflow
1. Extract Logs (Mission Planner)

FC log files: .bin

Converted to .mat and .csv

2. Clean & Process (Python)

Tools used:

Pandas  | Filtering, cleaning, grouping  
SciPy   | Smoothing, signal processing  
Matplotlib/Seaborn | Plotting  


Processing steps:
Removed outliers
Normalized timestamps
Merged IMU, PID, GPS, and Altitude data
Computed average X-Y-Z vibration metrics

3. Vibration Metrics Computed

accX, accY, accZ
gyrX, gyrY, gyrZ
VibeX, VibeY, VibeZ
RDES, YDES, PDES
Roll, Pitch, Yaw outputs

4. Dashboard (Tableau)

Vibration vs Time
Acceleration vs Speed
Gyro vs Speed
Altitude vs Vibration
PID Response Plots

📐 Percentage Reduction Calculation

Using averages of old vs new:

<img width="310" height="71" alt="image" src="https://github.com/user-attachments/assets/58b509a0-529c-4a46-980d-11d38d756014" />

Axis	Old	New	% Reduction
X	17.17	8.76	49%
Y	9.65	5.46	43%
Z	25.86	10.94	58%
🛠️ Tech Stack

Python: Pandas, SciPy, Matplotlib

Excel: Cleaning & pivot exploration

Tableau: Dashboard and final visual analysis

IMU Data: accX/Y/Z, gyrX/Y/Z, vibration values
