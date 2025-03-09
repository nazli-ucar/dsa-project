# Weather Impact on Traffic Accidents in Istanbul in 2024

### Motivation
As a driver in İstanbul, traffic safety is one of my biggest concerns. Many factors affect the situation in traffic: how the drivers act, the comfort of the roads, the density of the traffic... One of the less direct factors to affect the drivers' comfort is the weather. Rainy days, the wind and sometimes the snow decreases the driving comfort and indirectly causes traffic accidents. This project's aim to examine the relationship between weather conditions and traffic accidents in İstanbul. To make the project more relevant, I am using the 2024 data.

### Data Sources
This project relies on the following databases:
1. **Weather Data**: Collected from sources like **Turkish State Meteorological Service (MGM)**, OpenWeather API, or historical weather datasets.
2. **Traffic Announcements Data**: İBB’s database where the reported traffic accidents are shown with the date of the announcements, the topic of the announcements, the intervention time and how many lanes are closed temporarily because of the accident.

### Data Collection & Preparation
- The accident dataset will be filtered by **date, time, location, and severity**.
- Weather data will be merged based on **date, time, and location**.
- Data will be cleaned to remove inconsistencies and missing values.
- Additional preprocessing steps like handling outliers and normalizing variables will be applied.

### Analysis Methods
1. **Exploratory Data Analysis (EDA)**:
   - Identify accident frequency across different weather conditions (rain, fog, snow, clear skies).
   - Compare accident rates between dry and wet road conditions.
2. **Statistical Analysis & Correlation Tests**:
   - Conduct hypothesis testing to determine the significance of weather's impact on accident rates.
   - Correlation analysis between accident severity and weather parameters (temperature, humidity, precipitation).
3. **Machine Learning Models (Optional)**:
   - Train predictive models (e.g., logistic regression, random forests) to predict accident probability based on weather.
4. **Visualization**:
   - Create accident heatmaps based on weather conditions.
   - Time-series plots showing accident frequency during extreme weather events.

### Expected Findings
- Identification of the most dangerous weather conditions for traffic in Istanbul.
- Understanding the impact of temperature, rain intensity, and visibility on accident rates.
- Predictive insights that could help authorities issue warnings or adjust speed limits on certain roads during risky weather.

### Limitations & Future Work
- **Data Availability**: Weather data might not always match accident records perfectly.
- **Causal vs. Correlational Issues**: Bad weather may correlate with accidents, but other factors (driver behavior, road conditions) might be at play.
- **Scalability**: The study could be extended to other cities or regions in Turkey.

### Timeline
- **March 10**: Submit project proposal on GitHub.
- **April 18**: Collect data, perform exploratory analysis, and run correlation tests.
- **May 23**: Apply machine learning methods for predictive modeling.
- **May 30**: Final submission with a well-documented report and visualizations.

### Tools & Technologies
- **Programming Language**: Python (Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn)
- **Data Sources**: TÜİK, İBB Open Data Portal, OpenWeather API, MGM
- **Version Control**: GitHub for project tracking and documentation

### Submission Guidelines
- The project will be maintained in a GitHub repository.
- Regular commits will be made to document progress.
- A final report with insights and recommendations will be included.

---

This project aims to provide valuable insights into how weather conditions impact traffic accidents in Istanbul, with potential applications for road safety improvements and smart city planning.
