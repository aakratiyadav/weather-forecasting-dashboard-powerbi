# weather-forecasting-dashboard-powerbi
This Power BI Weather Forecasting Dashboard uses historical data (1990–2022) from Indian cities to visualize key metrics like temperature, humidity, wind, and rainfall. With Power Query cleaning and DAX KPIs, it offers dynamic insights to compare trends across cities for smart weather analysis. 
<img width="1337" height="731" alt="image" src="https://github.com/user-attachments/assets/3e8451fe-4f5f-4761-b1ed-66e4324897e2" />
🔍 Overview of the Weather Forecasting Project
This project uses historical weather data (1990–2022) from various Indian cities (e.g., Mumbai, Delhi, etc.). It offers an interactive dashboard built in Power BI using:

Power Query for data transformation and appending

Data modeling and relationships

DAX measures for KPIs

Visuals for temperature, humidity, wind, and precipitation insights

Forecasting and slicers for dynamic analysis

📊 Data Preparation and Power Query
In Power Query Editor:

✅ Applied Steps:
1.Imported multiple city CSV files (e.g., Mumbai, Delhi).
2.Renamed columns:
  >tavg → Avg Temperature (°C)
  >tmin → Min Temperature (°C)
  >tmax → Max Temperature (°C)
  >prcp → Precipitation (mm)
  >wspd → Wind Speed (km/h)
  >hum → Humidity (%)
3.Added 'City' column manually to each dataset before appending.
4.Appended datasets into a single table called weatherdata
5.Removed null rows and unnecessary columns.
6.Ensured data types (e.g., date, decimal) were correctly assigned.

📐 Data Modeling
1. Single table model: weatherdata
2. Time-based analysis is possible through the Date column
3. No relationships needed since the dataset is already consolidated


🎯 Key KPIs Created (Using DAX)
Below are some important KPIs used in the dashboard:

1. Average Temperature (°C)-Shows average temperature across the selected city/date range. 
   AvgTemperature = AVERAGE(weatherdata[Avg Temperature (°C)])

2. Maximum Temperature (°C)-Highlights extreme temperatures useful for summer pattern analysis.
   MaxTemperature = MAX(weatherdata[Max Temperature (°C)])

3. Minimum Temperature (°C)-Useful for detecting cold weather trends.
   AvgHumidity = AVERAGE(weatherdata[Humidity (%)])

4. Average Humidity (%)-Helps understand how humid a region was during a time frame.
   AvgHumidity = AVERAGE(weatherdata[Humidity (%)])

5. Total Precipitation (mm)-Assesses rainfall patterns, monsoon trends, and drought potential.
   TotalRainfall = SUM(weatherdata[Precipitation (mm)])

6. Average Wind Speed (km/h)-Useful in understanding weather instability and storm potential.
   AvgWind = AVERAGE(weatherdata[Wind Speed (km/h)])


   📈 Visualizations Used
🔹 1. Line Chart with Forecasting
Axis: Date
Values: Avg Temperature
Forecasting Enabled in analytics pane
Forecast Length: e.g., 6 months
Confidence Interval: 95%
Purpose: To visualize future weather trends using historical data.

🔹 2. Clustered Column Charts
Compared Avg/Max/Min Temperature, Humidity, or Rainfall
Grouped by City or Year

🔹 3. Cards
Displayed KPIs like:
1.Avg Temp
2.Min Temp
3.Max Temp
4.Total Rainfall
5.Avg Wind Speed

These cards are dynamic based on slicers.

🔹 4. Slicers
City Slicer: Select specific cities
Date Slicer: Filter by year or month
Both slicers affect every visual on the dashboard

🔹 5. Area Chart or Stacked Chart (Optional)
Used to show rainfall accumulation over time
Helps compare how monsoon intensity varied across years


✅ Conclusion
This project demonstrates how data-driven approaches can enhance weather monitoring and provide a clear view of long-term climate shifts in India.




