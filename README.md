# Weather Impact on Traffic Accidents in Istanbul in 2024

This project's aim is to examine the relationship between weather conditions and traffic accidents in İstanbul. To make the project more relevant, the data will be limited to 2024 and İstanbul province.

### Motivation
As a driver in İstanbul, traffic safety is one of my biggest concerns. Many factors affect the situation in traffic: how the drivers act, the comfort of the roads, the density of the traffic... One of the less direct factors to affect the drivers' comfort is the weather. Rainy days, the wind and sometimes the snow decreases the driving comfort and indirectly causes traffic accidents. To become a more conscious driver, the relationship must be realized. 

### Data Sources
This project relies on the following databases:
1. **Weather Data**: Collected from Visual Crossing website where Istanbul's daily weather conditions were displayed for every day in 2024. (https://www.visualcrossing.com/weather-query-builder/%C4%B0stanbul,%20T%C3%BCrkiye/us/2024-01-01/2024-12-31/#)
2. **Traffic Announcements Data**: İBB’s database where the reported traffic accidents are shown with the date of the announcements, the topic of the announcements, the intervention time and how many lanes are closed temporarily because of the accident. https://data.ibb.gov.tr/tr/dataset/ulasim-yonetim-merkezi-trafik-duyuru-verisi/resource/1c043914-8a76-4793-bae9-c60a68c7d389

### Data Collection & Preparation
- The accident dataset will be filtered by **date, time, location, and severity**. The data will be focused on accidents happened in İstanbul, 2024.
- Weather data will be observed based on **date, time, and location**. The location will be narrowed to İstanbul and the days when accidents happen. 


### Expected Findings
- Detecting the weather conditions which make the traffic in Istanbul more dangerous.
- Finding the effect of weather conditions and their consequences such as rainfall density, glaciation and temperature on drivers in Istanbul and their cars.
- Predictions of the danger of the roads during specific weather event and creating precautions for decreasing the chance of accidents.


### Tools & Technologies
- **Programming Language**: Python (Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn)
- **Data Sources**: İBB Open Data Portal, OpenWeather API, MGM
- **Version Control**: GitHub for project tracking and documentation

### Data Cleaning
**Raw Data**
- **Weather Data**: The weather data was already in the form of csv, so it was well structured and could be cleared. Additionally, it was daily reported for ever day in 2024. On the other hand, some of the data were unnecessary. The data was contained in a text file named 'raw data weather text.txt'.
- **Traffic Accident Data**: The accident data was separated with semi columns and it was from 2013 to 2025, so it needed to be fixed. Additionally, there were many unnecessary information such as the amount of closed lanes, the reported location, etc. The data was contained in a comma-separated-value file named 'traffic_announcement.csv'.

**Coding**: First, the weather file was read and loaded as a dataframe. Then, the unnecessary datas were erased. Only date, temperature, humdity and windgust were remaining. After that, the traffic accident file was read by noticing the delimiter as semicolon. Then, groups all the occurences by date and amount. The accident data was filtered by 2024 to match with the weather data. Finally, the weather and accident data were merged by the date and only three columns stayed: Date, accident amount, temperature, windgust and humidity. The result was saved in an excel file named "final_numeric_weather_accidents.xlsx".

### Exploratory Data Analysis (EDA)
**1.Descriptive Statistics**: 
![image](https://github.com/user-attachments/assets/02ca931c-1496-49d7-903e-930aa6fdef07)

