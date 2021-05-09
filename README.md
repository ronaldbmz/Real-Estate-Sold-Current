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
- Number of Beds
- Number of Baths
- Square Ft. Area
- Address
- City
- ZipCode

Once extracted, the data was cleaned and transformed into json and csv format in order to load in JavaScript query to build webpages.

## Visualization
To analyze the extracted real estate data, I have built the following visualizations using JavaScipt Plotly and D3:

### 1. Cluter Map Chart
The objective of this visualization to provide user the flexibity to review the number of sold and currently avaialble properties using actual geographic map view. Following are the features available in the map chart:
- Sold properties are shown in "green" color with different gradients based on the number of properties being sold. The more the properties sold, the darker the color is.
- Current available properties are shown in "red" color, with same different gradients based on number of properties being available.
- User can zoom-in or zoom-out in order to split or cluster the points respectively. 

#### Insights
- At higher level, we can observe that Frisco and Irving are the hotspot areas as there are more than 100 properties being currently avaialble and more than 100 properties being sold in the past 6 months.
- On the other hand, we can notice that in the past 6 months only ~20 properties being sold in Fort Worth area and around same number of properties are currently available as well.

![map_chart](Images/map_chart.png)
