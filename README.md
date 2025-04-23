# Weather Impact on Traffic Accidents in Istanbul in 2024

This project's aim is to examine the relationship between weather conditions and traffic accidents in İstanbul. To make the project more relevant, the data will be limited to 2024 and İstanbul province.

### Motivation
As a driver in İstanbul, traffic safety is one of my biggest concerns. Many factors affect the situation in traffic: how the drivers act, the comfort of the roads, the density of the traffic... One of the less direct factors to affect the drivers' comfort is the weather. Rainy days, the wind and sometimes the snow decreases the driving comfort and indirectly causes traffic accidents. To become a more conscious driver, the relationship must be realized. 

### Data Sources
This project relies on the following databases:
1. **Weather Data**: Collected from sources like **Turkish State Meteorological Service (MGM)**, OpenWeather API, or historical weather datasets. https://www.mgm.gov.tr/
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

###Data Process
**Data Cleaning**: The weather data was already in the form of csv, so it was well structured and could be cleared. The accident data was separated with semi columns, so it needed to be fixed.
