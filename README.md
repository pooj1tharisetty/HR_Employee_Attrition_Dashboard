# HR_Employee_Attrition_Dashboard

# 📊 End-to-End HR Attrition Analytics Dashboard (Microsoft Fabric & Power BI)

## 📌 Project Overview
An end-to-end HR Attrition Analytics project built using **Microsoft Fabric** and **Power BI**. The goal of this project is to help HR leadership identify key drivers behind employee turnover, evaluate departmental attrition risks, and make data-driven retention decisions.

---

## 💡 Business Problem & Objectives
Employee attrition costs organizations significant time, hiring expenses, and lost productivity. The HR leadership team needed answers to three critical questions:
1. **What is our overall attrition rate?**
2. **Which departments are losing the most employees?**
3. **Is there a relationship between pay, age, overtime, and employee decisions to leave?**

---

## 🛠️ Tech Stack & Tools Used
* **Microsoft Fabric Portal:** Workspace creation, Lakehouse environment setup.
* **Dataflow Gen2:** Data ingestion, data transformation, and calculated columns (`Salary Band`, `Age Group`).
* **Fabric Lakehouse:** Storing cleansed HR data.
* **Power BI Desktop & Fabric Service:** Report design, DAX measures, custom color theme, page navigation.
* **Governance & Security:** Column-Level Security (CLS) applied to protect sensitive compensation data (`MonthlyIncome`).

---

## 📐 Key DAX Measures Created
* **Attrition Rate:** `DIVIDE(COUNTROWS(FILTER(HR_Employees, HR_Employees[Attrition] = "Yes")), COUNTROWS(HR_Employees))`
* **Head Count:** Total count of active and departed employees.
* **Employees Left:** Total attrition count (`Attrition = Yes`).
* **Average Tenure of Leavers:** Average years spent at the company before leaving.
* **Average Monthly Income:** Overall employee salary baseline.

---

## 📊 Dashboard Key Insights
* **Overall Attrition Rate:** **16.1%** (Exceeds the industry standard benchmark of 10–15%).
* **Department Insights:** Sales and R&D show distinct turnover metrics; overtime workers exhibit significantly higher attrition compared to non-overtime staff.
* **Demographic Drivers:** Single employees and employees with higher business travel frequency demonstrate higher susceptibility to leaving.

---



## 🔒 Data Security & Governance
* **Column-Level Security (CLS):** Restricted visibility of the `MonthlyIncome` column within OneLake Security to ensure sensitive financial data is hidden from standard report viewers.
