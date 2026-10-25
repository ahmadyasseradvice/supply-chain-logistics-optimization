# Supply Chain Logistics & Fulfillment Performance Analysis
**Google Data Analytics Professional Capstone Project**  
**Author:** Ahmad Yasser  
**Tools:** Python (Pandas, Seaborn), SQLite, Kaggle  

---

## 1. Business Task (Ask)
DataCo Global faces recurring shipping delays that jeopardize customer retention, increase churn risk, and threaten service-level agreements (SLAs). 

This project investigates:
* Operational bottlenecks across fulfillment shipping modes and global markets.
* Total company revenue exposure directly tied to delayed shipments.
* Actionable, data-driven supply chain strategies to stabilize delivery timelines.

---

## 2. Methodology & Data Integrity (Prepare & Process)
* **Dataset:** DataCo Smart Supply Chain Dataset (180,519 initial records).
* **Data Integrity (ROCCC):** Sourced from verified supply chain transactions; validated zero null records across critical tracking fields (Order ID, Shipping Mode, Net Profit).
* **Data Cleaning & Filtering:**
  * Removed non-operational records (`CANCELED` and `SUSPECTED_FRAUD`), leaving **172,765 valid orders**.
  * Structured and cast data into an SQLite relational table (`orders_clean`) to run aggregation queries efficiently.

---

## 3. Key Findings (Analyze & Share)

* **100% Failure Rate in First Class Shipping:**
  * All 26,513 First Class orders experienced delivery delays, running an average of **1.00 day behind schedule**.
  * Second Class followed with a **79.83% late delivery rate** (averaging ~2 days behind schedule).
  * *Root Cause:* Schedulers set overly aggressive, unrealistic promised delivery windows in the Order Management System (OMS) that logistics carriers cannot physically meet.

* **Standard Class Drives Core Operations Reliably:**
  * Standard Class accounts for nearly 60% of total volume (103,153 orders) with only a **39.77% late rate** and an average delay of **-0.01 days** (delivering on or slightly ahead of schedule).

* **$20.13 Million in Revenue at Risk:**
  * **57.2% of total company revenue ($20.13M across 98,977 shipments)** arrived late, exposing DataCo to carrier concession claims, chargebacks, and poor customer retention.

---

## 4. Strategic Recommendations (Act)

1. **Recalibrate Delivery SLA Promises:**
   * Extend promised customer delivery windows by **+1 business day for First Class** and **+2 business days for Second Class** in checkout and OMS systems to immediately eliminate false expectations and eliminate artificial delay rates.
2. **Audit Expedited Carrier Contracts:**
   * Review agreements with third-party logistics (3PL) carriers handling First Class shipments to claim contractual refunds for missed guaranteed windows.
3. **Incentivize High-Performing Modes:**
   * Promote Standard Class fulfillment via checkout incentives to protect operational margins while
