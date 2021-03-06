# Weather or Not? - An Analysis of Weather &amp; Traffic Flow in Pasig City

Open the `DMW_Final_Weather_or_Not.html` file to view the report.

### Executive Summary

The Philippines is one of the countries where autos are widely used as a form of travel. With roughly 154 thousand passenger cars sold in 2020, the Philippines is placed 11th among Asia and Pacific countries in terms of passenger car sales. With the increasing number of cars sold in the Philippines and the country's climate change, traffic is unavoidable and will increase over time. We try to address how the traffic flow in different areas of Pasig City responds to wet weather using data from the Waze Connected Citizens Program and weather data.

To help us investigate our problem, we examined both the weather and traffic data of Pasig City. For the weather data, we scraped both the TimeandDate weather API and WorldWeatherOnline website to derive weather features. On the other hand, we obtained externally-sourced Waze data to extract transport-related features such as traffic and location with help of Thinking Machines and the Waze Connected Citizens Program. To aid our analysis, we used vector representation to segment the Pasig City Waze Traffic into 700 square blocks with derived on traffic features (average speed, number of traffic jams, portions of road). Feature engineering was done to derive additional features such as the amount of rainfall in a certain span of of day/week/month/year to examine the effect of weather features for each block at different times. Each block was then grouped through the help of clustering. Additionally, dimensionality reduction was done to extract significant features.

Upon clustering we were able to identify 3 main clusters according to their traffic volume and road type, and we decided to label them as routes:

- **Cluster 1: Major Highways** includes roads guarantee you the fastest route with the highest potential speed, however because to the high volume of traffic and the route's length, most people will be significantly delayed along this route. This group includes major roadways. The Pasig City LGU and MMDA need to improve infrastructural capacity and traffic control in these locations, especially during severe weather.
- **Cluster 2: Intracity Routes** contains roads that are ranked second in terms of weather-related delays, congestion, and speed. The majority of Pasig's areas fall into this category which indicates high urban congestion within the roads.
- **Cluster 3: Hidden Routes** upon initial glance has roads which have the lowest maximum speed in the area that make them appear unpromising. However, they seem to be the smoothest and least congested routes. The majority of these are located in the outskirts of Pasig City. In times of congestion or inclement weather, the MMDA and Waze should guide drivers to these locations.

When we grouped clusters this way, we were able to reveal the city's various congested locations. The number of jams, maximum speed, and normalized delay for each block were the three most relevant characteristics in the clusters. All three are traffic characteristics that may be used to explain traffic congestion during different times of the day. As a consequence, we were able to decipher the clustering findings and glean useful information from the data.

Finally, we want to recommended the following to the relevant stakeholders of Pasig City and the National Government. First, we suggest increasing infrastructure capacity especially in Cluster 1 (Major Highways) to help in decreasing overall congestion among these roads especially since these are main thoroughfares. In the short-term, rerouting some of the traffic volume in the Main Highways to less-traversed roads such as those found in the third cluster (the Hidden Routes) may help in augmenting the congestion within the city during the rush hour. Lastly, for Cluster 2 (Intracity Routes), we suggest taking a closer a look at these areas for the crafting of long-term urban planning policies since points of interests such as commercial and public spaces are included here. In the process, this may improve the prospects of public transportation as well as route optimization and help in the overall traffic situation of Pasig in the future.

Recommendations to improve this study include expanding the dataset by integrating flood and accident reports, as well as possibly including non-jammed roads for a more complete picture of the traffic situation. This limitation could be augmented through twitter as well through NLP.


In partial fulfillment of the requirements for AIM MSDS 2022 Data Mining and Wrangling under Prof. Christian Alis.
