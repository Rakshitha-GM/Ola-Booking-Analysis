# Ola-Booking-Analysis
# 🚖 Ola Bookings Analysis  

This project analyzes **Ola ride booking data** to uncover insights into vehicle types, revenue patterns, cancellations, customer behavior, and ratings. The analysis was performed using **SQL** and visualized with **Power BI dashboards**.  

## 📂 Project Files  
- **Bookings-100000-Rows.xlsx** → Raw dataset used for analysis.  
- **Ola bookings.pbix** → Power BI dashboard file.  
- **Screenshots/** → Dashboard visuals (Vehicle Type, Revenue, Cancellation).  
- **ola.sql** → All SQL queries used for analysis.  

## 🛠 Tools & Technologies  
- **Power BI** → Data visualization and dashboard creation  
- **SQL** → Data extraction and transformation  
- **Excel** → Dataset provided in `.xlsx` format  

## 📊 Dashboard Insights  

### 1️⃣ Overview Dashboard  
- Shows **total bookings, success rate, cancellation rate, and revenue trends** at a glance.  

### 2️⃣ Vehicle Type Analysis  
- Prime Sedan generated the **highest booking value** (8.30M).  
- E-Bikes had the **highest average distance travelled** (25.15 km).  
- Autos had significantly **lower average distance (10.04 km)** compared to other vehicle types.  

### 3️⃣ Revenue Analysis  
- **Cash** was the most preferred payment method, followed by **UPI**.  
- The **Top 5 Customers** contributed significantly to total revenue.  

### 4️⃣ Cancellation Analysis  
- **Total Bookings**: 103,024  
- **Succeeded Bookings**: 63,967  
- **Cancelled Bookings**: 28,933 (**28.08% cancellation rate**)  
- Major reasons:  
  - Customers: “Driver not moving towards pickup” (30.24%).  
  - Drivers: “Personal & car-related issues” (35.49%).  

### 5️⃣ Ratings Dashboard  
- Insights into **customer ratings** for drivers and rides.  
- Helps track **average ratings per vehicle type** and **overall service quality**.  

## 📝 Sample SQL Queries  

Here are a few example queries from the project:  

sql
-- 1. Retrieve all successful bookings
SELECT * FROM bookings WHERE Booking_Status = 'Success';

-- 2. Find the average ride distance for each vehicle type
SELECT Vehicle_Type, AVG(Ride_Distance) AS avg_distance
FROM bookings
GROUP BY Vehicle_Type;

-- 3. Top 5 customers with highest number of rides
SELECT Customer_ID, COUNT(Booking_ID) AS total_rides
FROM bookings
GROUP BY Customer_ID
ORDER BY total_rides DESC
LIMIT 5; 
  
👉 The **full list of queries** is available in the [`ola.sql`](./ola.sql) file.  

## 📌 Key Learnings  
- How different **vehicle categories** contribute to bookings and revenue.  
- Customer preferences for **payment methods**.  
- Patterns in **ride cancellations**.  
- Service quality through **customer ratings**.  
- Hands-on skills in **SQL data analysis** and **Power BI dashboards**.  

## 🚀 How to Use  
1. Download the dataset (`Bookings-100000-Rows.xlsx`).  
2. Open the `.pbix` file in Power BI Desktop.  
3. Connect with the dataset and refresh to view dashboards.  
4. Run queries from `queries.sql` in your SQL environment for insights.  

## 📷 Dashboard Samples  
- Vehicle Type Analysis  
- Revenue Analysis  
- Cancellation Analysis  
- Overview and Ratings dashboards 
