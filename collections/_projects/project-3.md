---
layout: project-right
title: "Analysis of Electric Vehicle Infrastructure in the DFW Metroplex"
description: "Is the DFW EV charging station infrastructure sustainable?"
date: 2021-04-08
weight: 1
thumbnail: "/assets/images/gen/projects/Dallas_Driveshed_Mile-3-3-thumbnail.jpg"
image: "/assets/images/gen/projects/Dallas_Driveshed_Mile-3-3.jpg"
client: false
categories: ["Infrastructure", "Case Study", "Research", "Energy", "Geospatial", "GIS"]
role: false
gallery_limit: 15
gallery:
  - image: "/assets/images/gen/projects/Charging_stations_DFW.jpg"
    caption: "<strong>Figure 1:</strong> Map of charging stations across the DFW Metroplex."
  - image: "/assets/images/gen/projects/pop_poverty_DFW.jpg"
    caption: "<strong>Figure 2:</strong> Map of the percentage of population below or at poverty level in DFW based of 12-month income in 2019."
  - image: "/assets/images/gen/projects/pop_black_DFW.jpg"
    caption: "<strong>Figure 3:</strong> Map of the percentage of black or African American population in DFW in 2019."
  - image: "/assets/images/gen/projects/5mile_DFW_driveshed.jpg"
    caption: "<strong>Figure 4:</strong> Map of 5-mile driveshed in DFW Metroplex"
  - image: "/assets/images/gen/projects/1mile_DFW_driveshed.jpg"
    caption: "<strong>Figure 5:</strong> Map of 1-mile driveshed across the DFW Metroplex."
  - image: "/assets/images/gen/projects/1mile_dallas_driveshed.jpg"
    caption: "<strong>Figure 6:</strong> Map of 1-mile driveshed across the city of Dallas"
  - image: "/assets/images/gen/projects/1mile_fortworth_driveshed.jpg"
    caption: "<strong>Figure 7:</strong> Map of 1-mile driveshed across the city of Fort Worth."
  - image: "/assets/images/gen/projects/1mile_denton_driveshed.jpg"
    caption: "<strong>Figure 8:</strong> Map of 1-mile driveshed across the city of Denton."
  - image: "/assets/images/gen/projects/1mile_northcentralTX_driveshed.jpg"
    caption: "<strong>Figure 9:</strong> Map of 1-mile driveshed across North Central Texas."
  - image: "/assets/images/gen/projects/1mile_driveshed_stats.png"
    caption: "<strong>Table 1:</strong> Statistics of 1-mile driveshed intersection poverty status in DFW."
  - image: "/assets/images/gen/projects/1mile_driveshed_race_stats.png"
    caption: "<strong>Table 2:</strong> Statistics of 1-mile driveshed intersection race & ethnicity status in DFW."
---

## Summary:

The success of electric vehicle market growth relies heavily on the ability for people to transition from gas powered to electric powered transportation. Dallas-Fort Worth is one of the leaders in charging station infrastructure according to Nicholas et al. 2019, however, significantly more charging infrastructure will be needed to sustain the transition to electric vehicles by 2025. While there is sufficient availability of charging stations throughout the Dallas and Fort Worth area, the surrounding metroplex may lack enough charging stations for those wanting to make the transition to electric powered transportation. Furthermore, electric vehicle companies and legislators should consider addressing certain social and economic barriers throughout the DFW Metroplex.

## Introduction:

Electric Vehicles (EV’s) have had a long history within the United States dating back to the early 1900s. However, EV’s at the time couldn’t gain significant traction due to better performing gasoline powered vehicles. Additionally, there were substantial barriers plaguing the development of a sustainable electric vehicle market. Technology has come a long way over the years and continues to improve, pushing the interest in electric vehicles across many states. 

Overall, an eco-friendlier environment remains the common goal amongst the majority of those pushing to further the electric vehicle market. Many researchers suggest the best opportunities to cut carbon emissions and reshape the United States transportation sector, is dependent upon the electric vehicle potential (Glandorf, 2020). Throughout the last decade, data from the U.S. Department of Energy shows that electric vehicle sales have increased and are on a trend to continue to do so. As a result, the demand has created the need for proper infrastructure to be put in place across many metropolitan areas in the United States (Nicholas, 2019). 

California, Florida, and Texas have the greatest number of electric vehicles as of December 2020. These three states lead the charge, no pun intended, when it comes to the need for proper charging infrastructure; However, they lack the necessary charging infrastructure installed, based off their electric vehicle growth. Why might this be? There is research suggesting the adoption of electric vehicles may not come easy due to the substantial economic, social, and technical barriers (Glandorf, 2020). This is important because, as states began to make the transition to electric powered transportation, these questions must be answered.

The study focused directly on the charging infrastructure in the Dallas-Fort Worth Metroplex. This study used a geospatial approach to illustrate and address the common barriers as noted above. Some of those barriers include:
- electric vehicle market growth
- charging times
- charger compatibility
- availability of charging stations
- charging station ease-of-use
- associated costs 

However, this study sepcifically focused on the potential impact that the availability of charging stations and ease-of-use has on the transition over to electric vehicles. To achieve a better understanding of why these barriers, create such an obstacle, this study also used data from the U.S. Census Bureau to help explain some of the social and economic barriers. Through geospatial analysis, we are able to explain and illustrate the issues Dallas-Fort Worth Metroplex faces regarding charging station infrastructure and compare the findigs in the DFW Metroplex to other states. Lastly, these results should provide insight into the pros and cons of electric vehicles.

## Method:

Given this focuses on the charging infrastructure in the Dallas-Fort Worth Metroplex, the unit of analysis for this project was at both the county and census tract levels. To account for both, the geographically large scale and high population density, it will be easier and more sufficient to use county and census tract data rather than census block data. Both poverty status and demographic related data had limitations as the data has poor aggregation. Additionally, using county and census tract levels as the unit of analysis will be beneficial while looking at such as large area.

To answer the different questions throughout the study, there will be multiple data types and sources. First the county polygon boundaries, highway (2019) line feature layer, and city streets line feature layer will come from the North Central Texas Council of Governments Regional Data Center. Then for charging stations, this study uses an Alternative Fueling Stations dataset which contains point data from the Bureau of Transportation Statistics Geospatial Portal. Lastly, for demographic data it will be a combination of polygon data from the United States Census Bureau and the North Central Texas Council of Governments containing information about population, economics, and other associated variables.

To look at the charging station infrastructure in the DFW Metroplex we will first need to look at how many charging stations there are across all counties. Both the charging station and county TIGER/Line feature layers will be added to a blank ArcMap. Additionally, the Highway (2019) feature layer will be added so that the Clip geoprocessing analysis can be carried out. This method allows for a more focused view on the study area by excluding data outside of the desired counties. Once those steps are carried out, census tract data for poverty status and demographics can be added to the map. The census tract TIGER/Line feature layer attributes can be joined with the census tract poverty status and demographic attribute tables. This method provides the opportunity to view data in a way that illustrates the distribution of the total population with the associated variables by creating choropleth maps using a technique called geodemography.

Perhaps the most important method of analysis in this study is the network analysis of charging stations by using a drivingshed technique. The network analysis takes into account all drivable roads throughout the Dallas-Fort Worth Metroplex. The streets feature layer from the North Central Texas Council of Governments Regional Data set is used. Additionally, the analysis considers one-way streets, to, and from endpoints. Then once those network analysis factors are identified, a 1-mile and 5-mile driveshed can be solved, showing the availability of charging stations.  From this we are able to determine drive times, address range anxiety, determine best routes, and ease-of-use. Lastly, we can then compare the results of the DFW Metroplex vs. other metropolitan areas.

## Findings and Discussion:

Overall, the results and findings from this study followed those of previous scientific literature and research. The overarching issue that electric vehicle companies and legislators face is lack of charging station infrastructure. Additionally, available space, charger type, ease-of-use, and distance all play a role in current charging station infrastructure. Figure 1, shows the current charging station infrastructure across the Dallas-Fort Worth Metroplex. In Dallas County, we see the majority of charging stations particularly throughout Dallas proper. Then to the north along the North Dallas Tollway a consistent cluster of charging stations remain until you cross the Dallas-Collin County lines. Aside from Dallas County, as we move outward from the center of Dallas, the amount of available charging stations decrease and become more sparce. This finding highlights the issue of available charging stations and the distance between other charging stations throughout a 1 to 5 mile radius.

In Figure 2. 6.8% or less of the total population that is at or below the poverty line reside in the suburbs or in what could be consider a wealthier part of the overall area. On the contrary, the other 94% of the population at or below the poverty line reside near a city center. For example, more than 37% of the total population at or below the poverty line live near or south of the City of Dallas. The same can be said for the percentage of the population that lives near Fort Worth. What may be interesting about this is there is strong concentration of charging stations within these cities. However, many electric vehicle owners own personal charging ports at their own homes, but it comes at an additional cost. Furthermore, those who live in apartment housing, are at a disadvantage due to the lack of equipped charging infrastructure present at these types of locations (Glandorf, 2020). Without proper charging infrastructure, the percentage of population at or below the poverty line probably won’t have an equal opportunity at transitioning over to electric powered transportation. Figure 3. which shows the percentage of black or African American population across the DFW metroplex, also suggests the same result. The pattern in both Figure 2 and Figure 3 are similar and may be where electric vehicle companies and legislators need to focus their strategic planning in order to achieve a more successful and equal outcome. See Tables 1 and 2 in for additional statistics.

Given the large number of charging station locations, performing a network analysis for drivesheds was more complex. However, the results shown in Figures 4 and 5 provide some information on the available roads that can be traveled to reach a charging station location. Additionally in Figures 4 and 5, we see that it can be difficult to interpret the results given such a large study area. Therefore, this study found that focusing on three metropolitan cities and one smaller region would be more beneficial to view the results. The result in Figure 6 explains that there are many options for finding a route within a one-mile radius to the nearest charging station location. In fact, all the charging stations in the Dallas proper area are easily accessible by road. However, while these charging stations may be easily accessible, there still may be a few issues that counteract the access. Those issues include charger type, ease-of use, home charging ports, and range anxiety. 

For Figures 7 and 8, we look at two other metropolitan cities aside from Dallas. Their results look similar to what is seen in Dallas, however, there are less charging station locations, and they are spread out more unevenly. Another interesting thing to point out is how the results in Figures 7 and 8 compared to that of what is shown in Figure 1. While the charging stations are accessible near each city center, as people plan to travel out of town, the number of charging stations becomes extremely small and charging station infrastructure in general is almost nonexistent. The result shown in Figure 9 validates this and the theme remains consistent throughout this region, ultimately in any direction that people travel. 

The charging station infrastructure across the DFW metroplex certainly reflects a good starting place given the current number of electric vehicles on the road today. However, throughout this study it is evident that there are some gaps regarding current infrastructure that needs to be addressed moving forward if electric powered transportation is to survive. If this can be accomplished, then it could spark the interest of more consumers.

## Conclusion:

The demand for electric vehicles will continue to grow as vehicle technology improves. However, the overall success of electric vehicle adoption will depend on the ability for electric vehicle companies and local politicians to pass the needed legislation to account for the substantial barriers facing electric vehicle growth. States, such as California, will require all new cars and passenger trucks sold in the state to be zero-emission vehicles by 2035. Similar states, that are leading in electric vehicle infrastructure, need to follow in those footsteps for proper charging infrastructure to be addressed sooner rather than later. This study highlighted how charging station availability, distance, and certain demographic barriers could affect the transition to electric vehicle transportation, and the challenges that could be present for future growth. Additionally, as this study focused specifically on the DFW Metroplex, we were able to see how the charging infrastructure in the DFW metroplex compares to other metropolitan areas. Lastly, the hope of this study was to shed light on the need for proper charging station infrastructure to achieve the common goal of becoming an eco-friendlier environment.



