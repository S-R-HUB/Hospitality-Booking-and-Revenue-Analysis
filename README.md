# Hospitality Booking and Revenue Analysis

## Overview
This project utilizes Power BI to analyze hospitality booking patterns and revenue metrics. It offers interactive dashboards and visualizations to help stakeholders gain insights into booking trends, revenue streams, and customer behavior within the hospitality industry.

## Problem Statement
AtliQ Grands owns multiple five-star hotels across India. They have been in the hospitality industry for the past 20 years. Due to strategic moves from other competitors and ineffective decision-making in management, AtliQ Grands are losing its market share and revenue in the luxury/business hotels category. As a strategic move, the managing director of AtliQ Grands wanted to incorporate “Business and Data Intelligence” to regain their market share and revenue..


## Table of Contents
- [Project Objectives](#project-objectives)
- [Data Sources](#data-sources)
- [How to Use](#how-to-use)
- [Setup Instructions](#setup-instructions)
- [Screenshots](#screenshots)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

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
- Business Category generates more Revenue than Luxury
- Occupancy rate is greater on weekends compared to weekdays
- Elite Rooms has highest number of bookings and Presidential rooms has lowest number of bookings
- Atliq Exotica generates the maximum revenue while Atliq Seasons generates the lowest revenue
- Mumbai generates the highest revenue while Delhi generates the lowest revenue
- Occupancy rate is highest in Delhi while Bangalore has the lowest occupancy rate
- Average rating is highest in Delhi while Bangalore has the lowest average rating
  
## How to Use
1. Clone or download this repository.
2. Open the Power BI file (.pbix) in Power BI Desktop.
3. Connect to the data source (update paths/credentials as needed).
4. Refresh the data to view the latest insights.
5. Explore dashboards using interactive filters.


## Screenshots
![Data Model](https://github.com/S-R-HUB/Hospitality-Booking-and-Revenue-Analysis/blob/main/Data%20Model.png?raw=true)
![Dashboard 1](https://github.com/S-R-HUB/Hospitality-Booking-and-Revenue-Analysis/blob/main/Dashboard%201.png?raw=true)
![Dasboard 2](https://github.com/S-R-HUB/Hospitality-Booking-and-Revenue-Analysis/blob/main/Dashboard%202.png?raw=true)
![Revenue_Calendar view](https://github.com/S-R-HUB/Hospitality-Booking-and-Revenue-Analysis/blob/main/Revenue%20in%20Calendar%20View.png?raw=true)


## Contributing

