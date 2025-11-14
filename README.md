# Hospitality Booking and Revenue Analysis

## Overview
This project utilizes Power BI to analyze hospitality booking patterns and revenue metrics. It offers interactive dashboards and visualizations to help stakeholders gain insights into booking trends, revenue streams, and customer behavior within the hospitality industry.

## Table of Contents
- [Problem Statement](#problem-statement)
- [Project Objectives](#project-objectives)
- [Data Sources](#data-sources)
- [Tools & Technologies Used](#tools-&-technologies-used)
- [Key Insights](#key-insights)
- [How to Use](#how-to-use)
- [Screenshots](#screenshots)
- [Limitations](#limitations)


## Problem Statement
AtliQ Grands owns multiple five-star hotels across India. They have been in the hospitality industry for the past 20 years. Due to strategic moves from other competitors and ineffective decision-making in management, AtliQ Grands are losing its market share and revenue in the luxury/business hotels category. As a strategic move, the managing director of AtliQ Grands wanted to incorporate “Business and Data Intelligence” to regain their market share and revenue.

## Project Objectives
- Analyze booking patterns and seasonality.
- Identify top revenue-generating segments.
- Explore customer demographics and booking behaviors.
- Provide actionable insights for revenue optimization.

## Data Sources
This project uses multiple CSV files as data source. Below is the description of each of the datasets.

1. **dim_date**
2. **dim_hotels**
3. **dim_rooms**
4. **fact_aggregated_bookings**
5. **fact_bookings**

---

### `dim_date` 
This dimensional datset contans information related to dates.

| Column      | Description                                                                 |
|-------------|-----------------------------------------------------------------------------|
| `date`      | Represents the dates present in May, June, and July.                        |
| `mmm yy`    | Represents the date in the format of `mmm yy` (month name and year).        |
| `week no`   | Represents the unique week number for that particular date.                 |
| `day_type`  | Indicates whether the day is a Weekend or a Weekday.                        |

---

### `dim_hotels`
This dimensional datset contans information related to hotels. 

| Column         | Description                                                                            |
|----------------|----------------------------------------------------------------------------------------|
| `property_id`  | Unique ID for each of the hotels.                                                      |
| `property_name`| Name of each hotel.                                                                    |
| `category`     | Determines which class (`Luxury`, `Business`) a particular hotel/property belongs to.  |
| `city`         | Indicates the city where the hotel/property is located.                                |

---

### `dim_rooms`
This dimensional datset contans information related to rooms.

| Column        | Description                                                                     |
|---------------|---------------------------------------------------------------------------------|
| `room_id`     | Type of room (`RT1`, `RT2`, `RT3`, `RT4`) in a hotel.                           |
| `room_class`  | Class (`Standard`, `Elite`, `Premium`, `Presidential`) the room type belongs to.|

---

### `fact_aggregated_bookings`
This fact datset contans aggregated booking information of each property on each date.

| Column               | Description                                                                                               |
|----------------------|-----------------------------------------------------------------------------------------------------------|
| `property_id`        | Unique ID for each of the hotels.                                                                         |
| `check_in_date`      | All the check-in dates of the customers.                                                                  |
| `room_category`      | Type of room (`RT1`, `RT2`, `RT3`, `RT4`) in a hotel.                                                     |
| `successful_bookings`| All the successful room bookings that happen for a particular room type in that hotel on that date.       |
| `capacity`           | Maximum count of rooms available for a particular room type in that hotel on that particular date.        |

---

### `fact_bookings`
This fact table has detailed information of each transaction/booking of every property.

| Column              | Description                                                                                                                                                                      |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `booking_id`        | Unique Booking ID for each customer when they booked their rooms.                                                                                                                |
| `property_id`       | Unique ID for each of the hotels.                                                                                                                                                |
| `booking_date`      | Date on which the customer booked their rooms.                                                                                                                                   |
| `check_in_date`     | Date on which the customer checked in (entered) at the hotel.                                                                                                                    |
| `check_out_date`    | Date on which the customer checked out (left) the hotel.                                                                                                                         |
| `no_guests`         | Number of guests who stayed in a particular room in that hotel.                                                                                                                  |
| `room_category`     | Type of room (`RT1`, `RT2`, `RT3`, `RT4`) in a hotel.                                                                                                                            |
| `booking_platform`  | Channel through which the customer booked the room.                                                                                                                              |
| `ratings_given`     | Ratings given by the customer for hotel services.                                                                                                                                |
| `booking_status`    | Indicates booking outcome: whether the customer cancelled (`Cancelled`), successfully stayed (`Checked Out`), or booked but did not stay (`No show`).                           |
| `revenue_generated` | Amount of money generated by the hotel from a particular customer.                                                                                                               |
| `revenue_realized`  | Final amount that goes to the hotel based on booking status: if `Cancelled`, 40% of revenue is deducted and refunded; if `Checked Out`/`No show`, full revenue goes to hotels.   |


## Tools & Technologies Used
- Power BI – Data Visualization & Dashboard Design.
- DAX (Data Analysis Expressions) – For creating KPI Metrics
- Power Query – Data cleaning and transformation.
- Excel/CSV – Data sources.


## Key Insights
### 1. Business Segment Revenue Leadership
The Business category is outperforming the Luxury segment in terms of revenue, showing that travelers have a stronger demand for business-oriented stays.

### 2. Weekend Occupancy and RevPar Trends
Occupancy rate along with Revenue Per Available Room (RevPar) is consistently higher on weekends compared to weekdays, pointing to opportunities for targeted weekend promotions and offers.

### 3. Room Preferences
Among room types, Elite rooms attract the most bookings, followed by Standard, Premium, and then Presidential categories. This reflects a clear guest preference for mid-to-high tier options.

### 4. Top and Bottom Revenue-Generating Properties
In Luxury category hotels, Atliq Exotica in Mumbai contributes the most to total revenue with **118.45M** across all properties, while Atliq Grands in Delhi generates the least with **36.06M**. In Business category Atliq Palace Mumbai generates the maximum revenue of **101.51M** while Atliq Palace Hyderabad generates the least revenue of **44.84M**

### 5. Customer Rating
AtliQ Exotica in Mumbai leads with the highest customer rating of **4.32**, showcasing strong guest satisfaction and a positive service experience. In contrast, AtliQ Seasons, also in Mumbai, holds the lowest rating of **3.74**.

### 6. Booking Outcomes and Conversion Rates
Out of all bookings, **70%** successfully convert into check-outs, indicating strong guest follow-through. However, **24.84%** end in cancellations and **5%** are recorded as no-shows. These trends highlight opportunities to further improve booking conversions.

### 7. Top Revenue Cities
Mumbai leads as the top revenue-generating city, with Bangalore, Hyderabad, and Delhi following, providing direction for resource allocation and marketing strategies.

### 8. Occupancy Rate by City
While Mumbai tops in revenue, Delhi achieves the highest occupancy rate, followed by Hyderabad, Mumbai, and Bangalore, showing potential for better room utilization in these cities.

### 9. City-wise Customer Ratings
Delhi also secures the highest average customer rating, whereas Bangalore ranks lowest, highlighting where service quality improvements may be necessary.

### 10. Platform Performance: Revenue Realization and ADR
The Logtrip platform records the strongest revenue realization rate of **70.06%**, while direct offline bookings achieve the highest Average Daily Rate (ADR) of **$12,791.17**. This provides insights for platform optimization.
On the other hand, Tripster shows the weakest revenue realization rate of **69.8%**, and the direct online channel has the lowest ADR of **$12633.71**, suggesting areas that need performance improvement.

### 11. Seasonal Occupancy Rate Patterns
**Week 32** saw the highest occupancy rate during the observed period, while **week 26** experienced the lowest, offering valuable guidance for seasonal campaigns and resource planning.

  
## How to Use

### Prerequisites

- **Power BI Desktop** installed on your Windows computer.  
  Download from the [official Microsoft Power BI website](https://powerbi.microsoft.com/desktop/).
- You can also download Power BI from Microsoft Store and it is completely free

---

### Steps

- Open Power BI Desktop from your Start Menu or desktop shortcut.
- Click on **File** > **Open**.
- Browse to the location of your `.pbix` file.
- Select the file and click **Open**.
- Power BI Desktop will load the file and display the reports, dashboards, and data models.
- You can now view and analyze the reports


## Screenshots
![Data Model](https://github.com/S-R-HUB/Hospitality-Booking-and-Revenue-Analysis/blob/main/Screenshots/Data%20Model.png)
![Dashboard 1](https://github.com/S-R-HUB/Hospitality-Booking-and-Revenue-Analysis/blob/main/Screenshots/Dashboard%201.png)
![Dasboard 2](https://github.com/S-R-HUB/Hospitality-Booking-and-Revenue-Analysis/blob/main/Screenshots/Dashboard%202.png)
![Revenue_Calendar view](https://github.com/S-R-HUB/Hospitality-Booking-and-Revenue-Analysis/blob/main/Screenshots/Revenue%20in%20Calendar%20View.png)

## Limitations
- Data is limited only to year 2022 for the month of May, June and July. We can add data for more upcoming years
