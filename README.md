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

## Data Cleaning and Manipulations

## Dropped Duplicate Rows
- **Action:** Removed 31,994 duplicate entries.
- **Reason:** To ensure data uniqueness and accuracy for the analysis.

## Handled Missing Values
- **Action:** Columns such as 'company' and 'agent' were removed.
- **Reason:** Missing values were addressed, and columns were removed due to their low impact on the analysis.

## Imputed 'Children' Column
- **Action:** Replaced missing values in the 'children' column with the mode (0).
- **Reason:** To reflect transactions with no children present.

## Standardized 'Country' Column
- **Action:** Substituted missing 'country' values with 'other'.
- **Reason:** To maintain data integrity without significantly altering the dataset's size.

## Eliminated Rows with No Guests
- **Action:** Excluded bookings with zero adults, children, and babies.
- **Reason:** These records do not contribute meaningfully to demand analysis.

## Type Conversion
- **Action:** Converted 'children' and 'reservation_status_date' columns to appropriate data types.
- **Reason:** For more accurate computation and representation.

## Added Calculated Columns
- **Action:** Introduced 'total_people' and 'total_stay' columns.
- **Reason:** To facilitate a more granular analysis of guest composition and stay duration.

## Filtered Out Negative ADR Values
- **Action:** Removed records with negative ADR values.
- **Reason:** Since average daily rate should be non-negative.

## Strategic Recommendations

To achieve the business objectives of optimizing hotel operations, maximizing revenue, and enhancing guest satisfaction, the following strategies are suggested:

## Dynamic Pricing and Promotions
- **Objective:** Utilize insights from seasonal booking trends and ADR analysis.
- **Action:** Implement dynamic pricing for high-demand periods (May to August) and special promotions during off-peak months (especially January and November).

## Targeted Marketing
- **Objective:** Focus marketing efforts on popular hotel types and room categories.
- **Action:** Emphasize City hotel offerings and popular room types (A, D, E) and tailor marketing to attract transient customers, the largest customer segment.

## Cancellation Policy Optimization
- **Objective:** Address high cancellation rates, especially in City hotels.
- **Action:** Review and revise cancellation policies, considering strategies like non-refundable rates or early booking incentives.

## Enhance Family-Friendly Services
- **Objective:** Reduce high cancellation rates among bookings with children or babies.
- **Action:** Improve family-friendly amenities and services, such as child care, entertainment options, or family packages.

## Distribution Channel Analysis
- **Objective:** Focus on efficient distribution channels.
- **Action:** Given high cancellation rates from TA/TO channels, strengthen direct booking channels or corporate partnerships.

## Meal Plan Optimization
- **Objective:** Align with the popularity of 'BB' (Bed & Breakfast).
- **Action:** Enhance breakfast offerings and consider special breakfast packages; evaluate and adjust 'FB' (Full Board) offerings.

## Guest Experience Improvement
- **Objective:** Address guest satisfaction for those not getting their reserved room type.
- **Action:** Offer compensations or upgrades to enhance satisfaction and potentially increase ADR.

## Utilize Data for Forecasting
- **Objective:** Leverage EDA insights for better forecasting and resource allocation.
- **Action:** Ensure staffing and inventory are aligned with expected demand, continuously monitor metrics, and adapt strategies.

The EDA of the hotel booking dataset provides valuable insights into customer preferences, booking trends, and revenue factors. By strategically implementing these solutions, the hotel can optimize its operations, enhance guest satisfaction, and maximize revenue. Leveraging data-driven insights for informed decision-making is key to aligning with business objectives and market dynamics. Continuous monitoring and adaptation of strategies will be crucial for sustained growth and competitiveness in the hospitality industry.

- **Handling a Large Amount of Duplicate Data:** Significant effort was needed to identify and remove duplicate entries to ensure data quality.
- **Dealing with Incorrect Data Types:** Several columns had to be converted to appropriate data types for accurate analysis.
- **Choosing Appropriate Visualization Techniques:** Selecting the right visualization tools and techniques was crucial to effectively convey the findings.
- **Addressing Numerous Null Values in the Dataset:** The dataset contained a substantial number of null values, which required careful handling to maintain data integrity.

