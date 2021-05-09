# Real Estate Analysis Sold vs. Current

## Objetive
Most of the real estate websites provide an option of analyzing current and sold properties but individually not together. At a time, user either can view the currently listed properties or sold properties. In this app, I have built the functionality for the user to review & analyze both current and sold properties together which could help in making better decision.

## ETL (Data Extraction Transform and Load)
 For this project the data has been scrapped from Redfin real estate website. In order to have sufficient amount of data, I have extracted Sold and Currently listed properties of following 10 cities in Texas using BeautifulSoup in Python:
- Dallas
- Fort Worth
- Plano
- Frisco
- Arlington
- Irving
- Southlake
- McKinney
- Colleyville
- Coppell

Also, to have data consistency, following key attributes are being extracted from the Sold & Currently listed properties:
- Coordinates of property located (Latitude & Longitude extracted using GeoCod API)
- Price
- # of Beds
- # of Baths
- Square Ft. Area
- Address
- City
- ZipCode

Once extracted, the data was cleaned and transformed into json and csv format in order to load in JavaScript query to build webpages.

## Visualization
To analyze the extracted real estate data, I have built the following visualizations using JavaScipt Plotly and D3:

### 1. Map Chart
![map_chart](Images/map_chart.png)
