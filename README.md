# Hotel Bookings Exploratory Data Analysis

## Objective
The main objective of this project is to perform an Exploratory Data Analysis (EDA) on a comprehensive hotel bookings dataset. The goal is to draw useful conclusions about general trends in hotel bookings and understand how various factors governing hotel bookings interact with each other.

## Dataset
We are provided with a dataset containing booking information for a city hotel and a resort hotel, encompassing a wide range of features:

- `hotel`: Name of hotel (City or Resort)
- `is_canceled`: Whether the booking is canceled (0 for not canceled, 1 for canceled)
- `lead_time`: Time (in days) between booking transaction and actual arrival
- `arrival_date_year`: Year of arrival
- `arrival_date_month`: Month of arrival
- `arrival_date_week_number`: Week number of arrival date
- `arrival_date_day_of_month`: Day of month of arrival date
- `stays_in_weekend_nights`: Number of weekend nights spent in a hotel
- `stays_in_week_nights`: Number of weeknights spent in a hotel
- `adults`: Number of adults in a single booking record
- `children`: Number of children in a single booking record
- `babies`: Number of babies in a single booking record
- `meal`: Type of meal chosen
- `country`: Country of origin of customers
- `market_segment`: Segment via which the booking was made
- `distribution_channel`: Medium through which the booking was made
- `is_repeated_guest`: Indicates repeated guest (0 for No, 1 for Yes)
- `previous_cancellations`: Number of previous canceled bookings
- `previous_bookings_not_canceled`: Number of previous non-canceled bookings
- `reserved_room_type`: Room type reserved by the customer
- `assigned_room_type`: Room type assigned to the customer
- `booking_changes`: Number of booking changes done by customers
- `deposit_type`: Type of deposit at the time of making a booking
- `agent`: ID of the booking agent
- `company`: ID of the company making the booking
- `days_in_waiting_list`: Number of days on the waiting list
- `customer_type`: Type of customer (Transient, Group, etc.)
- `adr`: Average Daily Rate
- `required_car_parking_spaces`: Number of car parking spaces requested
- `total_of_special_requests`: Total number of special requests
- `reservation_status`: Current status of the reservation
- `reservation_status_date`: Date of making the reservation status

Total number of rows in data: 119,390
Total number of columns: 32

## Data Cleaning and Feature Engineering
- **Removing Duplicate Rows:** All duplicate rows were dropped.
- **Handling Null Values:** Null values in 'company' and 'agent' were replaced by 0. Null values in 'country' were replaced by 'others'. Null values in 'children' were replaced by the mean of the column.
- **Converting Columns to Appropriate Data Types:** Changed data type of 'children', 'company', 'agent' to int type. Changed data type of 'reservation_status_date' to date type.
- **Removing Outliers:** One outlier was found in the 'adr' column and was dropped.
- **Creating New Columns:** Created 'total_stay' by adding 'stays_in_weekend_nights' + 'stays_in_week_nights'. Created 'total_people' by adding 'adults' + 'children' + 'babies'.

## Conclusion
Key takeaways from the analysis:
- City hotels are busier and generally have a higher ADR than Resort hotels.
- Guests prefer shorter stays, with Resort hotels favored for longer stays.
- High cancellation rates in both hotel types, with few repeat guests.
- July and August are the busiest and most profitable months for both hotels.

## Challenges
- **Handling a Large Amount of Duplicate Data:** Significant effort was needed to identify and remove duplicate entries to ensure data quality.
- **Dealing with Incorrect Data Types:** Several columns had to be converted to appropriate data types for accurate analysis.
- **Choosing Appropriate Visualization Techniques:** Selecting the right visualization tools and techniques was crucial to effectively convey the findings.
- **Addressing Numerous Null Values in the Dataset:** The dataset contained a substantial number of null values, which required careful handling to maintain data integrity.

