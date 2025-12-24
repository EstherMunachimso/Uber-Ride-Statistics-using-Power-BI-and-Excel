# INTRODUCTION
Uber is a leading global mobility and delivery technology company with operations **in over 70 countries**. It specializes in **ride-hailing, logistics, and on-demand services**, connecting millions of riders, drivers, couriers, and merchants daily through its app-based, data-driven platform.
Its offerings include ride services such as UberX, Uber Comfort, and Uber Black, as well as Uber Eats for food delivery and Uber for Business for corporate mobility solutions. Beyond transportation, Uber leverages real-time data, dynamic pricing, and route optimization algorithms to improve efficiency, reduce waiting times, and scale urban mobility. The company continues to expand its ecosystem through delivery services, partnerships, and innovations aimed at transforming how people and goods move within cities.

<img width="741" height="370" alt="image" src="https://github.com/user-attachments/assets/e545c69a-a134-4fd0-ab79-585a7f705eb1" />


## Data Gathering
This comprehensive project analyses Uber ride-sharing data for 2024, generating actionable insights into ride patterns, vehicle performance, revenue streams, and customer satisfaction metrics. The initiative delivers an interactive Excel dashboard enabling management to monitor operations, track critical KPIs, and execute data-driven strategic decisions with confidence.


For the purpose of this analysis, I had to find: 

- Operational insights: comprehensive trends in ride demand across date, time, location, and vehicle categories whilst monitoring booking completion rates and cancellation patterns.

  
- Customer & Driver Insights: Assess comprehensive rating systems, understand customer behaviour patterns, and conduct thorough driver performance analysis across all metrics.

  
-  Financial Analysis: Evaluate total revenue streams, average booking values, revenue distribution by vehicle type and location, plus quantify the financial impact of cancellations.

  
- Decision Support: Deliver actionable insights through an intuitive dashboard interface, empowering management to optimise operations and enhance strategic planning.


## Data Collection and Transformation
The dataset was a data directly from Kragle and contained 1 cleaned data file. The data set had 150K+ rows 21 columns and 10+ metrics. The data set was cleaned in excel where I created a pivot table that aids in ease of analysis and I also changed the data formats for ease.
Afterwards, the dataset was loaded into power bi for further analysis and visualization.


<img width="975" height="425" alt="image" src="https://github.com/user-attachments/assets/a6f83e61-7c0c-4668-957f-90c490bfc998" />



## Exploratory Data Analysis
The following are the actions I performed to answer the above business questions

- For the card details, a DAX measure was used to calculate the average customer rating:

`Average Customer Rating = AVERAGE(Sheet1[Customer Rating])`


- a DAX measure was used to calculate the average customer rating:

`Average Driver Rating = AVERAGE(Sheet1[Driver Rating]`

- a measure was used to calculate the average revenue:

`AVERAGE(Sheet1[Booking Value])`


- and equally the total booking value was gotten through this function:

`Total Booking = COUNTA(Sheet1[Cleaned Booking ID])`


- To ascertain the YOY percentage change, the measure was used:

`LastYearBooking = CALCULATE([Total Booking],DATEADD(Sheet1[Date],-1,YEAR))`


<img width="975" height="486" alt="image" src="https://github.com/user-attachments/assets/713ad62f-1456-461e-b493-a2a9692a880f" />



## INSIGHTS


<img width="975" height="544" alt="image" src="https://github.com/user-attachments/assets/9898eecd-b6b5-470d-bd6d-c91a01008d36" />


- 150K total bookings with 93K completed rides indicates a completion rate of roughly 62%, which is decent but leaves room for optimization. The platform is generating strong revenue volume, but operational inefficiencies are reducing realized value.

  
- Pickup is relatively fast, which is a strength. However, the full journey experience is long. This suggests congestion, routing inefficiencies, or extended drop off times. Longer CTAT can negatively affect customer satisfaction and retention.

  
- Q2 and Q3 peak at 38K with a drop in Q4 to 37K which signifies a stable business cycle and less volatility. This suggests the need for Q4 demand stimulation through pricing, promotions, or partnerships.


- The top pickup locations should have higher driver density, faster dispatch priority and dynamic pricing optimization.

  
- Most cancellations are operational failures, not demand failures and these are preventable revenue losses. It is advised to build better driver communication systems, stricter driver compliance monitoring, address validation before booking and vehicle quality enforcement.


- Through the dashboard, demand is price sensitive and customers prioritize affordability and availability over luxury. It is best to scale auto and economy fleets aggressively.


## CONCLUSION
Based on the dashboard analysis, overall performance is primarily driven by high demand concentration in key pickup locations, stable booking trends across months, and strong preference for affordable vehicle categories such as autos and economy rides. Operational efficiency, particularly ride completion rates, arrival times, and cancellation drivers, plays a decisive role in converting demand into realized revenue. Additionally, payment method dominance, especially UPI usage, and geographic clustering of bookings support revenue stability, while inefficiencies in trip duration and service quality constraints limit growth potential. Strengthening operations in high demand zones, reducing preventable cancellations, and optimizing fleet mix are therefore critical to sustaining volume growth and improving customer experience



