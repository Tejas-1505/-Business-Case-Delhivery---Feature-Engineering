# -Business-Case-Delhivery---Feature-Engineering
My Case studies with Scaler Academy

## About Delhivery

Delhivery is the largest and fastest-growing fully integrated player in India by revenue in Fiscal 2021. They aim to build the operating system for commerce, through a combination of world-class infrastructure, logistics operations of the highest quality, and cutting-edge engineering and technology capabilities.

The Data team builds intelligence and capabilities using this data that helps them to widen the gap between the quality, efficiency, and profitability of their business versus their competitors.



## Problem Statement

The company wants to understand and process the data coming out of data engineering pipelines:

• Clean, sanitize and manipulate data to get useful features out of raw fields

• Make sense out of the raw data and help the data science team to build forecasting models on it



## Dataset

**Column Profiling:**

**data** - tells whether the data is testing or training data

**trip_creation_time** – Timestamp of trip creation

**route_schedule_uuid** – Unique Id for a particular route schedule

**route_type** – Transportation type

**FTL** – Full Truck Load: FTL shipments get to the destination sooner, as the truck is making no other pickups or drop-offs along the way

**Carting**: Handling system consisting of small vehicles (carts)

**trip_uuid**- Unique ID given to a particular trip (A trip may include different source and destination centers)

**source_center** - Source ID of trip origin

**source_name** - Source Name of trip origin

**destination_cente**– Destination ID

**destination_name** – Destination Name

**od_start_time** – Trip start time

**od_end_time** – Trip end time

**start_scan_to_end_scan** – Time taken to deliver from source to destination

**is_cutoff** – Unknown field

**cutoff_factor** – Unknown field

**cutoff_timestamp** – Unknown field

**actual_distance_to_destination** – Distance in Kms between source and destination warehouse

**actual_time** – Actual time taken to complete the delivery (Cumulative)

**osrm_time** – An open-source routing engine time calculator which computes the shortest path between points in a given map (Includes usual traffic, distance through major and minor roads) and gives the time (Cumulative)

**osrm_distance** – An open-source routing engine which computes the shortest path between points in a given map (Includes usual traffic, distance through major and minor roads) (Cumulative)

**factor** – Unknown field

**segment_actual_time** – This is a segment time. Time taken by the subset of the package delivery

**segment_osrm_time** – This is the OSRM segment time. Time taken by the subset of the package delivery

**segment_osrm_distance** – This is the OSRM distance. Distance covered by subset of the package delivery

**segment_factor** – Unknown field

## Insights
 - The data is given from the period '2018-09-12 00:00:16' to '2018-10-08 03:00:24'.
 - There are about 14817 unique trip IDs, 1508 unique source centers, 1481 unique destination_centers,
   690 unique source cities, 806 unique destination cities.
   
 - Most of the data is for testing than for training.
 - Most common route type is Carting.
 - The names of 14 unique location ids are missing in the data.
 - The number of trips start increasing after the noon, becomes maximum at 10 P.M and then start decreasing.
 - Maximum trips are created in the 38th week.
 - Most orders come mid-month. That means customers usually make more orders in the mid of the month.
 - Most orders are sourced from the states like Maharashtra, Karnataka, Haryana, Tamil Nadu, Telangana
 - Maximum number of trips originated from Mumbai city followed by Gurgaon  Delhi, Bengaluru and Bhiwandi. That means that the seller base is strong in these cities.
 - Maximum number of trips ended in Maharashtra state followed by Karnataka, Haryana, Tamil Nadu and Uttar Pradesh. That means that the number of orders placed in these states is significantly high.
 - Maximum number of trips ended in Mumbai city followed by Bengaluru, Gurgaon, Delhi and Chennai. That means that the number of orders placed in these cities is significantly high.
 - Most orders in terms of destination are coming from cities like bengaluru, mumbai, gurgaon, bangalore, Delhi.

 - Features start_scan_to_end_scan and od_total_time(created feature) are statistically similar.

 - Features actual_time & osrm_time are statitically different.

 - Features start_scan_to_end_scan and segment_actual_time are statistically similar.

 - Features osrm_distance and segment_osrm_distance are statistically different from each other.

 - Both the osrm_time & segment_osrm_time are not statistically same.

## Recommendations
 - The OSRM trip planning system needs to be improved. Discrepancies need to be catered to for transporters, if the routing engine is configured for optimum results.

 - osrm_time and actual_time are different. Team needs to make sure this difference is reduced, so that better delivery time prediction can be made and it becomes convenient for the customer to expect an accurate delivery time.

 - The osrm distance and actual distance covered are also not same i.e. maybe the delivery person is not following the predefined route which may lead to late deliveries or the osrm devices is not properly predicting the route based on distance, traffic and other factors. Team needs to look into it.
 - Most of the orders are coming from/reaching to states like Maharashtra, Karnataka, Haryana and Tamil Nadu. The existing corridors can be further enhanced to improve the penetration in these areas.

 - Customer profiling of the customers belonging to the states Maharashtra, Karnataka, Haryana, Tamil Nadu and Uttar Pradesh has to be done to get to know why major orders are coming from these atates and to improve customers' buying and delivery experience.

 - From state point of view, we might have very heavy traffic in certain states and bad terrain conditions in certain states. This will be a good indicator to plan and cater to demand during peak festival seasons.

