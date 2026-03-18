# 📦 K.M Logistics & E-Commerce Sales Analytics (End-to-End Excel Project)

## 📊 Executive Summary
In the high-volume e-commerce sector, logistics and marketplace performance dictate profitability. This project executes an end-to-end data analysis pipeline on 31,000+ raw transactional records from K.M Logistics Pvt. Ltd. (2022 data).

The objective was to transform fragmented, corrupted raw data into a dynamic, interactive executive dashboard. By engineering new demographic features and standardizing logistics states, this analysis provides immediate visibility into **Marketplace Dependency, Demographic Purchasing Trends, and Regional Fulfillment Success.**

---

## 🛠️ Technical Stack & Skills Demonstrated
* **Tool:** Advanced Microsoft Excel (Office 365)
* **Data Engineering (Power Query/Native Excel):** Date restoration, Null-handling, Text normalization, Duplicate removal.
* **Feature Engineering (Formulas):** Nested `IF` statements, `VLOOKUP`/`XLOOKUP`, custom binning (Age/Demographics).
* **Data Visualization & BI:** Pivot Tables, Pivot Charts, Interactive Slicers, Dashboard UI/UX Design.

---

## 🗄️ Phase 1: The Raw Data Landscape
The initial dataset consisted of unstructured transactional logs tracking individual parcels across major Indian marketplaces.

* **Order Identifiers:** Unique Order IDs and SKU codes mapping to specific inventory units.
* **Logistics Status:** Real-time shipment states (e.g., Delivered, Cancelled, Refunded, RTO).
* **Sales Channels:** Attribution across Amazon, Flipkart, Myntra, Ajio, and Nalli.
* **Geographic Data:** Destination mapping via City, State, and Pincode.
* **Financials:** Order valuation standardized in INR.

<img width="1918" height="1008" alt="Raw Data Preview" src="https://github.com/user-attachments/assets/fd4ea198-b2cf-48b6-8863-6f46b5864e78" />

---

## 🧹 Phase 2: Data Transformation & "Dirty Data" Resolution
Real-world logistics data is notoriously messy. A significant portion of this project focused on ETL (Extract, Transform, Load) principles to convert 31,000+ records into a verified, analysis-ready dataset.

### 1. Structural Repair & Normalization
* **Date Restoration:** Resolved widespread "########" overflow errors in the raw timestamp column. Standardized dates into a strict `DD-MM-YYYY` format and extracted a separate **Month** dimension to enable seasonality and trend forecasting.
* **Categorical Unification:** Cleaned the 'Gender' column, using conditional logic to merge inconsistent manual entries (e.g., "M", "Men", "Male") into strict binary categories (**Men** / **Women**).
* **Status Verification:** Standardized fulfillment statuses to ensure "Delivered," "Cancelled," and "Refunded" orders were mutually exclusive, preventing the double-counting of recognized revenue.

### 2. Feature Engineering for Business Intelligence
To generate deeper insights beyond surface-level metrics, I engineered new analytical dimensions:
* **Demographic Segmentation:** Created custom logic to bucket customers into specific age cohorts (**Teen, Adult, Senior**). This enables highly targeted marketing analysis (e.g., *Isolating the Adult cohort's preference for Sarees vs. Western Wear*).
* **Channel Grouping:** Standardized vendor inputs to accurately attribute market share across Amazon, Flipkart, Myntra, and Ajio.

### 3. Quality Assurance (QA)
* **Data Cleansing:** Identified and purged redundant transaction IDs to prevent the overstatement of critical Sales KPIs. Addressed missing values in geographic fields to ensure regional heatmaps were comprehensive.

<img width="1920" height="1003" alt="Cleaned Data Preview" src="https://github.com/user-attachments/assets/07da7a1c-0808-4a08-bce6-e6275e4959c6" />

---

## 📈 Phase 3: Exploratory Data Analysis (EDA) & Visualization
Built a suite of Pivot Charts to isolate key performance indicators across multiple dimensions:

1. **Channel-Wise Sales:** Identifying dependency on specific marketplaces (e.g., Amazon vs. Flipkart).
2. **Gender Revenue Split:** Quantifying the total purchasing volume between Men and Women.
3. **Top 5 State Performers:** Geographic heat mapping to identify the strongest logistics routes and customer bases.
4. **Month-over-Month (MoM) Growth:** Tracking seasonal spikes and dips in order volume.
5. **Age Category Preferences:** Correlating specific product types to demographic segments.

<img width="1919" height="1010" alt="Analytical Charts" src="https://github.com/user-attachments/assets/2c1be1c0-65e7-4956-91ba-131df36d6afa" />

---

## 🎯 Phase 4: Annual Sales & Business Insights
Aggregated the granular data into a high-level Annual Sales overview, providing executives with a clear snapshot of yearly performance, peak seasons, and demographic dominance.

<img width="1901" height="999" alt="Annual Sales Overview" src="https://github.com/user-attachments/assets/18902c31-f46e-457c-ba4f-7fb59f6dffea" />

---

## 🕹️ Phase 5: The Executive Interactive Dashboard
The final deliverable is a fully interactive BI Dashboard. By integrating Pivot Tables with multiple Slicers (Timeline, Category, Channel), the dashboard allows non-technical stakeholders to perform rapid, self-service data slicing.

* **Key Functionality:** Users can isolate "Saree" sales on "Amazon" during "Q3" with three clicks, instantly updating all visual metrics to reflect that specific segment.

<img width="1920" height="1005" alt="Interactive Dashboard" src="https://github.com/user-attachments/assets/6ef7ba49-347d-4f6d-af88-552943726743" />

---
**Project Developed by:** Kaif Mahaldar  
**Role:** Data Analyst | E-Commerce Operations & Logistics Analytics  
**Contact:** [LinkedIn](http://www.linkedin.com/in/kaif-mahaldar-18300b333) | [Email](mailto:kaifmahaldar5@gmail.com)
