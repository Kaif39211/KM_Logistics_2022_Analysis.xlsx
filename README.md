# Analysis-Dummy-Company-Data-on-Excel
This project is an end-to-end Excel-based data analysis of sales and logistics operations for K.M Logistics Pvt. Ltd. using raw transactional data from 2022. The objective of the project is to clean raw data, structure it for analysis, and generate actionable business insights through reports and visualizations. 

*RAW DATA*--
 The raw dataset consists of the following key attributes:

Order Identifiers: Unique mapping of Order IDs and SKU codes to track individual parcels.

Logistics Status: Real-time tracking of shipment states (e.g., Delivered, Cancelled).

Sales Channels: Attribution of orders to major marketplaces including Amazon, Flipkart, Myntra, and Ajio.

Product Metadata: Granular details including Category (Saree, Kurta, Set), Size, and Quantity.

Geographic Data: Destination mapping via City, State, and Pincode for regional performance analysis.

Financials: Order valuation in INR and currency standardizations.
<img width="1918" height="1008" alt="image" src="https://github.com/user-attachments/assets/fd4ea198-b2cf-48b6-8863-6f46b5864e78" />





**DATA CORRECTION & CLEANING** -- ## 🛠️ Data Transformation & "Dirty Data" Resolution

A significant portion of this project was dedicated to transforming the `RAW SHEET` (31,000+ records) into a verified, analysis-ready dataset. Real-world logistics data is rarely clean; I implemented the following data engineering steps to ensure 100% reporting accuracy.

### 1. Handling Structural Corruption
* **Date Restoration:** Resolved widespread "########" overflow errors in the raw date column. I standardized these into a unified `DD-MM-YYYY` format and extracted a **Month** column to enable seasonality and trend analysis.
* **Size Standardisation:** Cleaned the 'Size' column to remove inconsistencies, ensuring that variants like 'Free', 'M', and '3XL' were correctly categorized for inventory reporting.

### 2. Categorical & Logical Cleaning
* **Gender Normalisation:** The raw data contained inconsistent labels (e.g., "M" vs "Men"). I used conditional logic to unify these into two clean categories: **Men** and **Women**.
* **Status Verification:** Standardized order statuses to ensure "Delivered," "Cancelled," and "Refunded" orders were mutually exclusive for accurate revenue calculation.

### 3. Feature Engineering for Business Intelligence
To provide deeper insights beyond the raw numbers, I engineered new data attributes:
* **Age Group Segmentation:** Created a custom logic to bucket customers into **Teen, Adult, and Old Adult**. This allowed for targeted demographic analysis (e.g., *Who is buying more Sarees vs. Western Wear?*).
* **Channel Attribution:** Grouped disparate SKU data to analyze performance across specific marketplaces including **Amazon, Flipkart, Myntra, Ajio, and Nalli**.

### 4. Quality Assurance (QA)
* **Duplicate Removal:** Identified and purged redundant transaction IDs to prevent the overstatement of sales KPIs.
* **Null Handling:** Addressed missing values in geographic fields (City/State) to ensure the "Sales by State" heatmaps were comprehensive.


<img width="1920" height="1003" alt="image" src="https://github.com/user-attachments/assets/07da7a1c-0808-4a08-bce6-e6275e4959c6" />





**CHART**--
  FOR BATTER ANALYSIS GIVING THE CHART OF (CHANNEL WISE SELLS	/  MEN VS WOMEN TOTAL BUYING SUM / TOP 5 : SELLS STATE	/ MONTH WISE SELLS	/ AGE CATEGORY WISE SELLS)
		
<img width="1919" height="1010" alt="image" src="https://github.com/user-attachments/assets/2c1be1c0-65e7-4956-91ba-131df36d6afa" />



**ANNUAL SALES TYPE**-- 
 GIVING INSIGHTS ON THE BASIS OF ANNUAL SALE

<img width="1901" height="999" alt="image" src="https://github.com/user-attachments/assets/18902c31-f46e-457c-ba4f-7fb59f6dffea" />


**REPORT**
-- CREATE PIVOT CHART & SLICER FOR QUICK ANALISIS
<img width="1920" height="1005" alt="image" src="https://github.com/user-attachments/assets/6ef7ba49-347d-4f6d-af88-552943726743" />
















