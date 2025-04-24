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
**1. Descriptive Statistics**: 

![image](https://github.com/user-attachments/assets/02ca931c-1496-49d7-903e-930aa6fdef07)
The average number of daily accidents in Istanbul 2024 was 37.63 In a day minimum 11, maximum 87 accidents had happened. The standard deviation is 10.95 which means that the daily accident amounts vary. 
Temperature was minimum 35.9 Fahrenheit and maximum 86.4 Fahrenheit in Istanbul with a mean of 62.59 and standard deviation of 12.97. This shows that Istanbul lived many seasons. 
Windgust was between 8.90 and 74.30 mph with a mean of 22.62 and standard deviation of 7.22.
Humidity was between 44.50% to 92.00% with a mean of 71.96% and standard deviation of 9.37%. We can say that Istanbul was a humid place.


**2. Correlation Matrix**:

![image](https://github.com/user-attachments/assets/65126c47-e2f8-4281-9da3-f1e994e68063)
Accident count and windgust tend to have a negative correlation. As windgust decreases, accident counts increase slightly. 
During windy days, drivers can be more careful due to the increasing tendency of accidents.
Accident count and humdity have a negative weak correlation. As humidity decreases, accidents occur slightly more. 
Accident count and temperature have a extremely weak positive correlation. As temperature increases, accidents may occur very slightly more.


**3. Line Plot**:
![image](https://github.com/user-attachments/assets/c90097ac-f500-4589-94c6-3e41adaedadf)
In 2024, there is no clear trend, lots of variation is going on most of the accidents occur 20 to 60 daily. This supports H0 as there cannot be seen a clear distinct relationship between weather and accidents.

**4. Histograms**:
![image](https://github.com/user-attachments/assets/4225c2cd-34a8-4dd1-a453-7b5e23e43c3b)

The x axis shows the number of accidents in a day and y axis shows the number of days that had many accidents. Accident amount is lightly skewed to the right. The majority is between 20 and 50. There are some outliers.
Then x axis shows the daily average temperature in Fahrenheit and the y axis shows the number of days with that temperature range. It is bimodal, has 2 peak points which are 60 and 80 Fahrenheit. The range is wide. This indicates date Istanbul experienced many seasons in a year.
The x axis shows the windgust speed in mph and the y axis shows the number of days with that windgust range. The histogram is left-skewed the wind was mostly low. The x axis shows humidity percentage and the y axis shows the number of days with that humidity. It looks like it is normally distributed but has more density on the right side. The humidity is centered around 70%.


**5. Bar Charts**:

![image](https://github.com/user-attachments/assets/b878b96d-1a67-4eac-a8af-1f0c9a9f939c)
![image](https://github.com/user-attachments/assets/df31bd09-9254-4596-a89a-ea112956a360)
![image](https://github.com/user-attachments/assets/baf5c868-ddd8-49dd-9328-5fe9fb74f944)

**6. Boxplot**:

![image](https://github.com/user-attachments/assets/275a265e-6988-4d33-94ad-4eb988e1bdd0)
![image](https://github.com/user-attachments/assets/a752196d-dc19-4a68-a977-6cafcf44b56f)
![image](https://github.com/user-attachments/assets/9d2a8e2c-d130-4f60-8411-8f2fa434b19a)








