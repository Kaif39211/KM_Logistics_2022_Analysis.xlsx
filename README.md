# K.M Logistics — E-Commerce Sales Analytics (End-to-End Excel Project)

> **31,047 Records | ₹21,176,377 Gross Sales | Microsoft Excel | Pivot Tables · Slicers · Dashboard**

> ⚠️ Dataset is simulated for portfolio purposes. All figures, company names, and platform references are synthetic.

---

<img width="1517" height="594" alt="image" src="https://github.com/user-attachments/assets/4ffeb462-c3e3-4c92-9ecc-61cf000fb459" />


---

## The Problem

Raw logistics data from an e-commerce operation is fragmented by default — inconsistent gender entries, broken date formats, duplicate order IDs, missing geographic fields. Before any insight can be extracted, the data has to be rebuilt from the ground up.

This project takes 31,047 raw transactional records from 2022, cleans and restructures them, then delivers a fully interactive Excel dashboard that gives stakeholders visibility into fulfillment performance, demographic trends, regional revenue, and channel dependency — all filterable in real time.

---

## Dataset

| Field | Detail |
|---|---|
| Records | 31,047 rows |
| Period | Full year 2022 |
| Gross Sales | ₹21,176,377 |
| Platforms | Amazon, Myntra, Flipkart, Ajio, Nalli, Meesho |
| Geography | Pan-India (city, state, pincode) |

**Schema:** `Order ID`, `Customer ID`, `Gender`, `Age`, `Date`, `Status`, `Channel`, `SKU`, `Category`, `Size`, `Qty`, `Amount`, `Ship City`, `Ship State`, `Ship Pincode`, `B2B`

---

## Phase 1 — Raw Data Landscape

The initial dataset tracked individual parcels across major Indian marketplaces.

- Unique Order IDs and SKU codes per transaction
- Fulfillment states: Delivered, Cancelled, Refunded, Returned
- Sales attribution across 7 platforms
- Geographic mapping via city, state, and pincode
- Order valuation in INR

<img width="1902" height="790" alt="image" src="https://github.com/user-attachments/assets/f58e3f2e-674f-44cb-a9b1-56fd944eb4f8" />


---

## Phase 2 — Data Cleaning & Feature Engineering

**Structural Fixes**
- **Date column:** Resolved `########` overflow errors across the timestamp column. Standardized to `DD-MM-YYYY` and extracted a `Month` dimension for trend analysis
- **Gender column:** Merged inconsistent entries (`M`, `Men`, `Male` → `Men` / `W`, `Women` → `Women`) using conditional logic
- **Status column:** Ensured Delivered, Cancelled, and Refunded are mutually exclusive to prevent double-counting revenue
- **Duplicates:** Purged redundant transaction IDs to prevent overstatement of sales KPIs
- **Missing values:** Addressed gaps in geographic fields for complete regional coverage

**Feature Engineering**
- **Age cohorts:** Bucketed customers into Teen (<25), Adult (25–49), Senior (50+) using nested `IF` logic
- **Channel grouping:** Standardized vendor inputs for accurate platform attribution

<img width="1920" height="739" alt="image" src="https://github.com/user-attachments/assets/b30d1119-8b6d-4748-8f06-4ed0ef432369" />


---

## Phase 3 — Analysis & Key Findings

### Channel Performance

| Platform | Orders | Share |
|---|---|---|
| Amazon | 11,016 | 35.5% |
| Myntra | 7,254 | 23.4% |
| Flipkart | 6,703 | 21.6% |
| Ajio | 1,931 | 6.2% |
| Nalli | 1,484 | 4.8% |
| Meesho | 1,398 | 4.5% |
| Others | 1,261 | 4.1% |

Amazon and Myntra alone account for nearly 60% of total volume. Flipkart at 21.6% is a significant third channel often overlooked in the summary view.

### Demographics

**Gender**
- Women: 69.2% of orders
- Men: 30.4% of orders

**Age**
- Adult (25–49): 62.9%
- Senior (50+): 19.6%
- Teen (<25): 17.5%

Adult women are the dominant buying segment by a significant margin.

### Top Categories by Revenue

| Category | Revenue |
|---|---|
| Set | ₹10,507,546 |
| Kurta | ₹4,959,377 |
| Western Dress | ₹3,148,836 |
| Top | ₹1,186,199 |
| Saree | ₹1,010,471 |

Sets alone account for nearly 50% of total gross revenue — the single most important product line.

### Regional Performance — Top 5 States

| State | Revenue |
|---|---|
| Maharashtra | ₹2,990,221 |
| Karnataka | ₹2,646,358 |
| Uttar Pradesh | ₹2,104,659 |
| Telangana | ₹1,712,439 |
| Tamil Nadu | ₹1,678,877 |

Maharashtra and Karnataka together represent ~27% of total national revenue.

### Fulfillment & Seasonality

- **Delivery rate:** 92.3% (28,641 of 31,047 orders delivered)
- **Cancellations:** 2.7% | **Returns:** 3.4% | **Refunds:** 1.7%
- **Peak month:** March (₹1,928,066) — Q1 is the strongest quarter, sales decline steadily through summer and stabilize in Q4

<img width="2347" height="866" alt="image" src="https://github.com/user-attachments/assets/cf4cea3f-a785-42a4-bb51-55c28a5a4b65" />


<img width="1010" height="691" alt="image" src="https://github.com/user-attachments/assets/885e6ca7-1433-474e-bb08-a355111123ce" />
<img width="783" height="468" alt="image" src="https://github.com/user-attachments/assets/888c648f-38dc-4026-8c21-0b67fba7f594" />



---

## Phase 4 — Interactive Dashboard

Built in Excel with a centralized slicer control panel. All charts and KPIs update simultaneously when filtered.

**Slicers:**
- Month
- Category
- Age Group
- Channel
- Gender

**KPIs on dashboard:**
- Total orders and gross revenue
- Order status breakdown (Delivered / Cancelled / Returned / Refunded)
- Channel-wise sales distribution
- State-wise revenue map
- Month-wise order quantity vs. amount (dual axis)
- Gender and age segment breakdown

<img width="1728" height="666" alt="image" src="https://github.com/user-attachments/assets/56c3b9b9-f18f-41c7-9fc5-084f450b54e9" />


---

## Recommendations

**1. Protect the Amazon & Myntra relationship**
60% of volume runs through two platforms. Any fee increase or algorithm change on either is a direct revenue hit. Investigate direct-to-consumer or Flipkart growth as a hedge.

**2. Double down on Sets**
₹10.5M in revenue — nearly half of total gross sales from one category. Inventory, procurement, and marketing resources should weight heavily toward Sets, especially heading into Q1.

**3. Scale logistics infrastructure in Maharashtra and Karnataka**
These two states generate ₹5.6M combined. Warehousing and last-mile delivery concentration here directly protects the 92.3% delivery rate at scale.

**4. Q1 capacity planning**
March is the peak month every year. Logistics staffing and warehouse capacity need to be scaled up in January ahead of the Q1 surge, not in response to it.

---

## How to Use

1. Download `KM_Logistics_2022_Analysis.xlsx`
2. Open in Microsoft Excel 2016 or newer
3. Go to the `Dashboard` tab
4. Use the slicers on the left to filter by month, category, age, channel, or gender
5. Raw data and pivot tables are in their respective labeled sheets

---

 **Role: Data Analyst — Sales & Logistics Operations** 

 
 **Others Project -**
 
 1) https://github.com/Kaif39211/pharmaceutical-inventory-analysis-SQL 
                                              2) https://github.com/Kaif39211/zepto_inventory_analysis.sql


                      
## **Contact: [LinkedIn](http://www.linkedin.com/in/kaif-mahaldar-18300b333) | [Email](mailto:kaifmahaldar5@gmail.com)**
