# Project Background

Ford India, established in 1995, a critical transportation alternative in the San Francisco Bay Area, offering a convenient and eco-friendly way to travel. 


The company has significant amount of **data on its trip data for a continuous period of 31 days, spanning the entire month of January 2018.**
This project dives deep into the trip data to uncover patterns in user behavior and trip characteristics, with a focus on how long trips typically last, and whether trip duration is influenced by time of year or user type.

To guide the analysis, we explore the following key questions:

- **How long does the average trip take?**

- **Is the trip duration affected by weather or seasons (inferred through months)?**

- **Does trip duration vary significantly between subscribers and customers?**

The analysis journey follows a structured path:

- **Introduction of the topic and dataset** to set the stage.
- **Preliminary data investigation and wrangling** to clean and understand the dataset.

- Further **data wrangling** to shape the data for analysis.

- **Univariate analysis** to summarize key features like trip duration and user demographics.

- **Bivariate and multivariate exploration** to examine how trip duration relates to months and user types.

- **Conclusions and answers** to provide actionable insights and summarize key findings.

Through this exploration, we aim to provide data-backed recommendations that could enhance service delivery, improve customer satisfaction, and support future infrastructure planning for the GoBike system.


# Data Structure and Initial Checks

Ford GoBike's database Structure as seen below consists of total row count of **94802** records of both user type subscribers and customers.

| Column Name               | Description                                                                 |
|---------------------------|-----------------------------------------------------------------------------|
| `duration_sec`            | Trip duration in seconds (key for identifying short vs long trips).         |
| `start_time`, `end_time`  | Timestamp of trip start and end (used for seasonal, hourly, and weekday trends). |
| `start_station_id`, `end_station_id` | Unique identifiers of start and end stations.                |
| `start_station_name`, `end_station_name` | Names of start and end stations (great for mapping popular routes). |
| `start_station_latitude`, `start_station_longitude` | GPS coordinates for start locations.       |
| `end_station_latitude`, `end_station_longitude`     | GPS coordinates for end locations.         |
| `bike_id`                 | Unique identifier for each bike (can be used to analyze bike usage frequency). |
| `user_type`               | Either **Subscriber** or **Customer**. Subscribers are regular users.       |
| `member_birth_year`       | Birth year of the user (used to calculate age and understand demographics). |
| `member_gender`           | Gender of the user (can be used to study usage trends across genders).     |
| `bike_share_for_all_trip` | Indicates whether the user opted for bike sharing for all trips (Yes/No).  |

Prior to beginning the analysis, a variety of check were conducted for quality control and familiarization with the dataset. 

# Executive Summary

In the course of the exploration, I found that the **average duration for all trips** is approximately **871 seconds** (~**14.5 minutes**).  
Most trips occurred on **Wednesdays** and **Tuesdays**, while **weekends** had the **fewest trip records**, although trip durations tended to be **longer** on weekends compared to weekdays.

An interesting pattern observed was the **peak usage around 8 AM to 9 AM** and again between **5 PM to 6 PM**.  
These periods align with typical **morning and evening rush hours**, indicating strong commuter usage.

More than **87% of the rides** were taken by **Subscribers**, and over **75.3%** of the total rides were completed by **male riders**.

Further findings revealed that:
- **Customers** tend to spend **more time per trip** compared to **Subscribers**.
- **Female subscriber riders** tend to have **slightly longer ride durations** compared to **male subscriber riders**.

Additionally:
- **User type** does **not significantly affect** the number of rides taken on any specific day.
- However, for any given day, **Customers** consistently tend to have **longer trip duration**

To meet the business objectives of **increasing ridership, enhancing user engagement, and boosting revenue**, it is **recommended** that the company:

- Develop targeted strategies aimed at **converting high-engagement Customers into long-term Subscribers** by offering subscription incentives and loyalty programs.

- **Launch marketing initiatives** focused on weekend and leisure riders, such as special offers, partnership deals, and bundled ride packages.

- **Optimize bike distribution** and resource allocation based on user behavior:

- **Prioritize availability** in business hubs during weekdays for Subscribers.

- **Enhance availability in tourist areas** and parks during weekends for Customers.

By aligning operational strategies with the distinct usage patterns of each user segment, the company can **maximize utilization, increase customer lifetime value, and strengthen market position.**
