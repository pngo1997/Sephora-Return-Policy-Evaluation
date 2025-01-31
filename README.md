# 🛍️ Sephora Return Policy Evaluation  

## 📜 Overview  
This project evaluates **Sephora's return policy** using **data warehousing principles**. The goal is to analyze product return patterns, assess their impact on inventory, and enhance return management using **ETL processes, BI dashboards, and data visualization**.

## 🎯 Problem Explanation  
Sephora's **high-end makeup and personal care products** contribute to a **volatile return rate**. Customers often return products due to impulse purchases, unclear return policies, or unsatisfactory products.  

### **Challenges:**  
1. **Lack of transparency in return policy:**  
   - Some customers receive **return bans without clear explanations**.  
   - Sephora needs a structured **return-tracking system**.  
2. **Operational impact of returns:**  
   - **Store staff** may mislead customers on return eligibility to boost sales.  
   - **Inventory turnover** is affected by frequent returns.  
3. **Distinguishing return sources:**  
   - Returns may come from **customers or suppliers**.  
   - Need to evaluate **supplier performance** based on return rates.  

📌 **Solution**: A **data warehouse** to analyze **return trends, customer eligibility, supplier evaluation, and inventory impact**.

## 📊 Data Warehouse Design  

### **📌 Dimensions & Facts**  
| **Dimension**  | **Description** |
|---------------|--------------------------------|
| Time         | Return date, transaction time |
| Product      | Product ID, name, category, price |
| Supplier     | Supplier ID, name, location, contract details |
| Customer     | Customer ID, membership status, purchase history |
| Return Info  | Return ID, reason, return method (online/in-store) |

| **Fact Table**  | **KPIs & Metrics** |
|-----------------|--------------------|
| Return Facts   | Return quantity, return value ($), return rate (%) |
| Customer Eligibility | Customer return frequency, ban status |
| Supplier Evaluation | Supplier-based return rates |
| Inventory Management | Total stock, restock quantity, return impact |

📌 **Normalization:** 2NF applied to **minimize redundancy** while maintaining **business process efficiency**.  

## 🔄 **ETL Process**  
🚀 **Steps:**  
1. **Extract** relevant data from Sephora’s internal systems (**SAP, SQL, Linux-based inventory**).  
2. **Transform** data to maintain consistency:  
   - Standardize **date formats** (YYYY/MM/DD).  
   - Convert **missing values** (e.g., `99999` for unknown numerical data).  
   - Enforce **referential integrity** (linking dimension & fact tables).  
3. **Load** into a structured **data warehouse** for reporting & BI applications.  

📌 **ETL Automation**: Automated pipelines ensure **real-time updates**.

## 📈 **Business Intelligence (BI) Dashboard**  
👥 **Users**: Sephora's **Sales, Supply Chain, and Operations teams**.  

### **1️⃣ Return Performance Dashboard**  
- 📊 **Total Product Returns by Membership Status** (Table format)  
- 🥧 **Return Quantity by Method (Online vs. In-store)** (Pie chart)  
- 📈 **Top 5 Suppliers with Highest Return Rates** (Bar chart)  

### **2️⃣ Customer Behavior Dashboard**  
- 📊 **Sales vs. Returns by Membership Status**  
- 📆 **Quarterly Sales & Return Trends**  

### **3️⃣ Inventory Management Dashboard**  
- 📊 **Year-End Product Inventory Levels** (Tree map)  
- 📆 **Quarterly Inventory Turnover Analysis**  

📌 **BI Tools Used**: **Tableau, Power BI**  

## 📢 **Key Findings & Recommendations**  

✅ **Key Insights**:  
- **Customers with high return frequency risk being banned.**  
- **In-store staff may be influencing return rates by misinforming customers.**  
- **Returns are highest in certain beauty product categories.**  
- **Supplier return rates vary, affecting Sephora’s inventory management.**  

🔧 **Recommended Actions**:  
- 🎯 **Enhance return policy transparency** to reduce customer confusion.  
- 📊 **Monitor supplier return rates** to negotiate better contracts.  
- 🛒 **Improve inventory forecasting** to manage stock turnover effectively.  
- 🏷️ **Restrict excessive returns** based on **customer eligibility metrics**.  

## 🚀 Technologies Used  
🛠 **Data Processing & BI Tools**:  
- **SQL, SAP, Linux-based inventory systems** – Data extraction  
- **ETL tools** (Talend, Informatica) – Data cleaning & transformation  
- **Tableau, Power BI** – Data visualization & BI reporting  

💾 **Data Source**: Synthetic data.

## 📊 Sample Visualizations  

### **1. BI Dashboard**
![BI Dashboard](https://github.com/pngo1997/Images/blob/main/Sephora%20Dashboard.png)  

### **2. Dimensional Model**
![Dimensional Model](https://github.com/pngo1997/Images/blob/main/Sephora%20DM.png)  

### **3. End to End Architecture**
![Overall Architecture](https://github.com/pngo1997/Images/blob/main/Sephora%20AC.png)  

---

## 🏆 Conclusion & Future Scope  
🔍 **Summary**:  
- Sephora needs **better return-tracking** for **customer eligibility, supplier performance, and inventory management**.  
- BI dashboards provide **insightful return metrics** to improve business operations.  

📌 **Future Enhancements**:  
- **Machine learning** to predict fraudulent returns.  
- **Integration with POS data** for real-time tracking.  
- **Customer feedback analysis** to refine return policies.  
