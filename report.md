# 📘 Project Report: Diwali Sales Data Analysis

*Author:* [Your Name]  
*Date:* [Current Date]  
*Tools Used:* Python, Pandas, Seaborn, Matplotlib  
*Dataset:* 11,251 Rows | Retail Sales Transactions

---

## 1. 🎯 Executive Summary
The primary objective of this analysis was to *optimize marketing ad spend* for the upcoming Diwali festival season. By analyzing 11,000+ historical sales records, we identified that the business's "Power Users" are *married women aged 26-35 working in the IT and Healthcare sectors, specifically located in **Uttar Pradesh, Maharashtra, and Karnataka*.

*Key Recommendation:* Shifting ad budget to target this specific demographic for *Food, Clothing, and Electronics* categories could significantly increase conversion rates and average order value (AOV).

---

## 2. 📂 Data Overview & Dictionary
The dataset consists of transactional data from a retail store.

| Column Name | Description | Data Type |
| :--- | :--- | :--- |
| User_ID | Unique identifier for the customer | Int |
| Cust_name | Name of the customer | String |
| Product_ID | Unique identifier for the product | String |
| Gender | Gender of the customer (M/F) | String |
| Age Group | Age bracket (e.g., 26-35) | String |
| Marital_Status | 0 (Married) / 1 (Unmarried) | Int |
| State | Geographic location of the customer | String |
| Zone | Region (North, South, East, West) | String |
| Occupation | Customer's profession | String |
| Product_Category| Category of the item purchased | String |
| Orders | Number of items in the transaction | Int |
| Amount | Total revenue generated from the transaction | Int (Cleaned) |

---

## 3. ⚙ Technical Methodology

### 3.1 Data Cleaning (ETL Process)
Before analysis, the raw data required significant cleaning to ensure accuracy:
1.  *Noise Removal:* Dropped unrelated columns Status and unnamed1 which contained no valid data.
2.  *Missing Value Handling:*
    * Identified 12 rows with null values in the Amount column.
    * *Decision:* Dropped these rows (axis=0) as they constituted <0.1% of the dataset and imputation could introduce bias in revenue calculations.
3.  *Data Type Standardization:*
    * Converted Amount from float to int to standardize currency formatting and reduce memory usage.

### 3.2 Exploratory Data Analysis (EDA) Steps
* *Univariate Analysis:* Examined distributions of Gender and Age to understand the customer base composition.
* *Bivariate Analysis:* Correlated Occupation vs. Amount and State vs. Orders to identify high-value segments.
* *Multivariate Analysis:* Looked at Gender + Age Group trends simultaneously to pinpoint the exact target persona.

---

## 4. 📊 Detailed Insights

### 🛒 Customer Demographics
* *Gender:* Females drive the majority of sales. They not only place more orders than men but also have a higher total spend.
* *Age Group:* The *26-35 age bracket* is the most active, contributing to nearly 40% of total revenue. The second strongest group is 36-45.
* *Marital Status:* Married individuals show a significantly higher purchasing frequency compared to singles.

### 📍 Geographic Analysis
* *Top Performing States:*
    1.  *Uttar Pradesh:* Highest total orders and revenue.
    2.  *Maharashtra:* Strong second contender.
    3.  *Karnataka:* Third largest market.
* *Insight:* These three states combined account for a substantial portion of the total national sales. Logistics and inventory stocking should be prioritized here.

### 💼 Occupational Analysis
* *Sectors:* Customers working in *IT, Healthcare, and Aviation* have the highest purchasing power.
* *Strategy:* This suggests that marketing campaigns could be effective on professional platforms (like LinkedIn) or targeted via industry-specific interests.

### 📦 Product Preferences
* *Top Categories:*
    1.  *Food:* Highest volume of orders.
    2.  *Clothing & Apparel:* High volume and high revenue.
    3.  *Electronics:* High ticket size items.
* *Underperformers:* Categories like "Office" and "Veterinary" showed minimal traction during the festival period.

---

## 5. 💡 Strategic Recommendations

1.  *Targeted Ad Campaigns:* Create specific ad sets for *Females, Age 26-35, Married* living in UP/MH/KA. Use imagery that resonates with working professionals (IT/Healthcare).
2.  *Inventory Planning:* Ensure warehouses in the Central and Western zones (UP/Mah) are overstocked with Food and Clothing items to prevent stockouts during the rush.
3.  *Bundle Deals:* Create "Festival Bundles" combining Clothing and Footwear, as these categories show high correlation in purchase behavior.

---

## 6. 🚧 Challenges & Limitations
* *Missing Date Column:* The dataset lacked a specific Date or Time stamp. This prevented Time-Series Analysis (e.g., analyzing sales spikes on weekends vs. weekdays or specific days leading up to Diwali).
* *No Customer Sentiment:* We have purchase data but no review/feedback data, so we cannot determine why customers bought specific items.

---

## 7. 🔮 Future Scope
If more data becomes available, the following analyses would add further value:
* *Market Basket Analysis:* To understand which products are frequently bought together (e.g., Bread + Milk).
* *Churn Prediction:* If we had data over multiple years, we could predict which customers are unlikely to return.
