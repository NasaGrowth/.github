# High level Summary

Farmers need support to face the issues of climate change, by means of improved weather data and predictions. There is a wealth of information, but we will publish that information in a way which is accessible and understandable to farmers, by means of an app. It will run on:
- smartphones
- tablets
- web browsers

With:
- user-friendly interface
- visual dashboard
- sourcing data from two directions: from the Space Agencies and the farmers as well.

The app addresses the challenge by focusing on the Critical Success Factors we identified:
- Farmer centric design
- Data presented in a clear and understandable way
- With timely updates as well as offline capability for remote areas with little or no connectivity.

It is essential that we focus on the farmers, which are the ones who will be using the app and may have reduced literacy and / or limited means to afford hardware.

# Demo Link
[Intended app behaviour (Youtube)](https://www.youtube.com/watch?v=cKN6QTTM4XQ)

# Detailed project screens
[Open it at figma online ](Https://www.figma.com/community/file/1424843421858850351/nasagrowth)

# WHY? 
Farmers need support against these issues of climate change, by means of improved weather data and predictions (more precise, timely, adapted to their specific crops / livestock) 
This will enable farmers to: 

+ Make informed decisions based on relevant, useful, actual data. 
+ Manage the risks of drought and floodings and use water efficiently. 
+ Improve their farming practices. 
+ Optimize production.
   
In turn, this contributes to a steady supply of food, which benefits farmers and consumers (predictable deliveries, stable prices). 

 # WHO? 
 
Smallholders are small-scale farmers managing areas varying from less than one hectare to 10 hectares. 

Women comprise up to almost 50 percent of the agricultural labor force. 

Smallholders provide up to 80 percent of the food supply in Asian and sub-Saharan Africa. 
 
There are an estimated 500 million smallholder farms in developing countries of the world alone, supporting almost two billion people. 

Additional users for the app could be:

+ Agronomists 
+ Soil scientists 
+ Laborers 
+ Agricultural communities 

In the developing world, according to Huebler & Lu (2013) adult literacy rates were reported to be below the global average especially in South and West Asia (63%) and sub-Saharan Africa (59%), where more than one-third of adults cannot read and write.

# WHAT? 
 
Historic rainfall, moisture and temperature conditions related to the current season would help smallholders to plan water requirements or variety selection. 
 
Those data are recorded by NASA satellites. 
We want to bring to the smallholder’s farm such information. 
The farmer defines the season’s init/end according to the crop he plans for the plot.  
The app provides the farmer with: 

+ A Season-to-day rainfall of current year compared with previous ones 
+ A Season-to-day rainfall of current year in perspective of previous full seasons 
+ A quadrant will express the current season compared with historical data. 
+ A k-means clustering off previous years and current year. 
+ A forecast of yield (Only if Farmer introduces in the app, yields obtained in previous years)

  
### A Season-to-day rainfall of current year compared with previous ones 
![image](https://github.com/NasaGrowth/Docs_and_refs/blob/main/Season-to-day.png)

 In areas with scare bandwidth, a table with colors will be enough to hint farmer about current year’s rainfall rank 

### A Season-to-day rainfall of current year in perspective of previous full seasons 
![image](https://github.com/NasaGrowth/Docs_and_refs/blob/main/Full%20season%20rainfall.png)


### A quadrant will express current season compared with historical data  
![image](https://github.com/NasaGrowth/Docs_and_refs/blob/main/Quadrant.png)

This quadrant will support water management decisions: 
 
+ Scenario 1: is the best scenario for the farmer. The current season rainfall is above average as well as soil moisture. Water care can relax a little bit. 
+ Scenario 2: Soil moisture is still under the average for the season time, but as rainfall is above average, probably farmer will not require additional water reserves. 
+ Scenario 3: Despite moisture soil is above average, the season has scare rainfall. A close follow-up is a must. 
+ Scenario 4: is the worst case for the farmer. He must check if has enough water reserves to finish a successful crop or choose a variety with less water requirements. 

# HOW?

We use three data sources
+ [**For rainfall**:Huffman, G.J., A. Behrangi, D.T. Bolvin, E.J. Nelkin (2022), GPCP Version 3.2 Satellite-Gauge (SG) Combined Precipitation Data Set, Edited by Huffman, G.J., A. Behrangi, D.T. Bolvin, E.J. Nelkin, Greenbelt, Maryland, USA, Goddard Earth Sciences Data and Information Services Center (GES DISC), Accessed: [2024-10-06], 10.5067/MEASURES/GPCP/DATA304 with a spatial resolution 0.5 ° x 0.5 ° and temporal resolution 1 month](https://disc.gsfc.nasa.gov/datasets/GPCPMON_3.2/summary)
+ [**For temperature**: Global Modeling and Assimilation Office (GMAO) (2015), MERRA-2 statD_2d_slv_Nx: 2d,Daily,Aggregated Statistics,Single-Level,Assimilation,Single-Level Diagnostics V5.12.4, Greenbelt, MD, USA, Goddard Earth Sciences Data and Information Services Center (GES DISC), Accessed: [2024-10-06], 10.5067/9SC1VNTWGWV3 with a spatial resolution 0.5 ° x 0.625 ° and temporal resolution 1 day](https://disc.gsfc.nasa.gov/datasets/M2S)
+ [**For moisture**: Vrije Universiteit Amsterdam (Richard de Jeu) and NASA GSFC (Manfred Owe) (2014), AMSR2/GCOM-W1 surface soil moisture (LPRM) L3 1 day 10 km x 10 km ascending V001, Edited by Goddard Earth Sciences Data and Information Services Center (GES DISC) (Bill Teng), Greenbelt, MD, USA, Goddard Earth Sciences Data and Information Services Center (GES DISC), Accessed: [2024-10-06], 10.5067/B0GHODHJLDA8 with a spatial resolution 10 km x 10 km and temporal resolution 1 month](https://disc.gsfc.nasa.gov/datasets/LPRM_AMSR2_DS_A_SOILM3_001/summary?keywords=moisture%20soil)

Data sources were available at NASA earth data. We created one profile there.

When farmer device gets plot geo location from GPS sensor,  the right polygon for each data source is calculated.

When farmer introduces the season windows for the crop, the app queries data sources for the right time frame for current and previous seasons. 

The data summary for  the plot is saved in the farmer device for further usage. Run conversions for fields (type, length, unit of measure, decimals, check values,...) has been executed on the flight accordingly to farmer locale. data summary are limited to running totals. maximums, minimums, or averages on season windows bases.

As long as time goes on, incremental download with updated data will occur when device has wireless communications.

The aim is that farmer could visualize charts and quadrants with minimal dependency on telecommunications. 

we have to identify others sources of NASA data to add more functionalities such as sunlight exposure, flood risk, chemical soil status, and so on. 




# CRITICAL SUCCESS FACTORS 
Some developing countries do not enjoy the best telecommunications infrastructure. 
The app will download historical data for NASA data sources for each plot the smallholders want to include. 
As far as new current rainfall and moisture data is available, that app will download it when a good signal is available. 
 Illiteracy conditions how the app renders the information. 

# MONETIZATION
Free for farmers monitoring less than 10 hectares. 3rd sector entities pushing FAO programs would deliver app to farmers in developing countries.


# APP

Preview the mobile application design created using Figma. Check it out on our [public file](https://www.figma.com/community/file/1424843421858850351/nasagrowth)

<img width="739" alt="Captura de Pantalla 2024-10-06 a las 22 14 15" src="https://github.com/user-attachments/assets/22842754-001f-463f-8128-8c91baff4706">

<img width="739" alt="Captura de Pantalla 2024-10-06 a las 22 14 39" src="https://github.com/user-attachments/assets/92353564-07aa-41ec-a28e-c52302c52439">


