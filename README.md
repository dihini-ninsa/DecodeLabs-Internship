
---

##  Detailed Project Breakdown

###  Project 1: Data Cleaning & Preparation (The Architecture of Data Integrity)
* **Goal:** Scrub, restructure, and validate a highly irregular raw dataset, transforming it from a "messy collection" into a **"Gold Standard" Source of Truth**.
* **Core Philosophy:** *You must master the 80% cleaning and wrangling phase to earn the right to execute the 20% predictive modeling and dashboarding phase.*
* **Key Implementations:**
  * **Strategic Imputation:** Evaluated missing fields (e.g., handling the `CouponCode` blank rows dynamically without resorting to listwise deletion, preserving statistical power).
  * **The Integrity Audit:** Programmed uniqueness checks (`GROUP BY Order_ID HAVING COUNT(*) > 1`) to eliminate inflated transaction counts and guarantee that every primary key represents exactly one true business entity.
  * **Formatting & Schema Validation:** Standardized text strings, parsed ISO-formatted timestamps, structural currency symbols (`$`), and normalized regional data.

###  Project 2: Exploratory Data Analysis (The Geometry of Distribution)
* **Goal:** Interrogate the cleaned dataset using statistical frameworks to uncover hidden patterns, behavioral anomalies, and operational centers of gravity.
* **Key Implementations:**
  * **Univariate Analysis:** Evaluated the center of gravity and spatial distribution across numeric metrics (`Quantity`, `UnitPrice`, `TotalPrice`).
  * **Robust Central Tendencies:** Dissected the differences between **Mean** (highly sensitive to outlier anomalies) and **Median** (robust against extreme skews) when analyzing e-commerce transactions across different user cohorts.
  * **The Logic Skeleton (Five-Number Summary):** Developed full descriptive profiling using automated descriptive logic (`df.describe()`) to capture structural boundaries: Minimum, Q1 (25th percentile), Median (50th percentile), Q3 (75th percentile), and Maximum values.
  * **Outlier & Trend Identification:** Identified seasonal purchase velocity shifts across major categories (`Monitor`, `Phone`, `Tablet`, `Chair`, `Printer`, `Laptop`, `Desk`).

###  Project 3: SQL Data Analysis (Querying for Relational Truth)
* **Goal:** Design and optimize declarative relational pipelines to isolate key performance indicators, filter granular noise, and construct clean aggregations for executive reporting.
* **Key Implementations:**
  * **Row-Level Filtration Funnels:** Configured complex `WHERE` logic incorporating structural boundaries, exact match indicators, numerical performance limits, and pattern-matching wildcards (`LIKE '%@gmail.com'`).
  * **Categorical Bucketing:** Leveraged performance-optimized `GROUP BY` and aggregation statements (`COUNT`, `SUM`, `AVG`) to collapse massive dimensional logs into distinct, actionable summary matrices.
  * **Database Engine Cost Estimation:** Studied the internal mechanics of database compilation (Parsing -> Binding into Abstract Syntax Trees -> Cost-Based Optimizer execution path matching), ensuring all written SQL scripts minimize CPU, Memory, and Disk I/O bottlenecks.

---

##  Dataset Profile

The underlying pipeline processes a comprehensive retail transaction registry with the following structural layout:

* **Dimensions:** 1,200 total records, 14 feature columns.
* **Core Fields Available:**
  * `OrderID` (Primary alphanumeric key)
  * `Date` / `CustomerID`
  * `Product` catalog categorization (`Laptop`, `Monitor`, `Desk`, `Chair`, `Printer`, `Phone`, `Tablet`)
  * `Quantity` / `UnitPrice` / `TotalPrice` (Financial metrics)
  * `ShippingAddress` / `PaymentMethod` (`Credit Card`, `Debit Card`, `Cash`, `Online`, `Gift Card`)
  * `OrderStatus` transactional states (`Shipped`, `Delivered`, `Pending`, `Cancelled`, `Returned`)
  * `TrackingNumber` / `ItemsInCart` / `CouponCode` / `ReferralSource`

---

##  The Full-Stack & Engineering Edge

As an aspiring **Data Analyst / Machine Learning Engineer** with an active background in **Full-Stack Development (Java Spring Boot, React, MySQL)**, my approach to these projects goes beyond basic reporting:
1. **End-to-End Scalability:** I treat analytical steps as pipeline functions capable of being modularized into software backends.
2. **API & Model Ready:** All text cleaning, integrity tracking, and relational schemas are constructed to interface cleanly with downstream ML frameworks (such as Random Forest/LightGBM algorithms) and predictive microservices.
3. **Database Performance Aware:** With deep familiarity with MySQL relational databases, my SQL extraction plans are designed with cost-based indexing and structural scalability in mind.

---

###  Future Roadmap
- [ ] Connect the Phase 1 & 2 Python cleaning pipelines into an interactive full-stack monitoring dashboard built via React.
- [ ] Integrate a predictive modeling script using LightGBM or Random Forest to forecast product sales trends directly from the SQL dataset aggregates.

***
