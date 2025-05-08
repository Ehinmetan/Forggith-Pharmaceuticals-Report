# Forggith-Pharmaceuticals-Report
As a consultant for a fictional pharmaceutical company, I developed a dynamic and interactive report tailored to specific business needs. This project was part of the deliverables required to successfully complete the Power BI Developer Internship Program organized by Foresight BI
# Table of Content
[Introduction](https://github.com/Ehinmetan/Forggith-Pharmaceuticals-Report/blob/main/README.md#introduction)

[Reporting Requirements](https://github.com/Ehinmetan/Forggith-Pharmaceuticals-Report/blob/main/README.md#reporting-requirements)

[Data Source](https://github.com/Ehinmetan/Forggith-Pharmaceuticals-Report/blob/main/README.md#data-source)

[Data Cleaning & Transformation](https://github.com/Ehinmetan/Forggith-Pharmaceuticals-Report/blob/main/README.md#data-cleaning--transformation)

[Data Modelling](https://github.com/Ehinmetan/Forggith-Pharmaceuticals-Report/blob/main/README.md#data-modelling)

[Visualization](https://github.com/Ehinmetan/Forggith-Pharmaceuticals-Report/blob/main/README.md#visualization)

[Insights](https://github.com/Ehinmetan/Forggith-Pharmaceuticals-Report/blob/main/README.md#insights)

[Recommendation](https://github.com/Ehinmetan/Forggith-Pharmaceuticals-Report/blob/main/README.md#recommendations)


![FORGGITH](https://github.com/user-attachments/assets/9a95c7a7-8a14-4227-9e71-b822b83aacb2)
# Introduction
Forggith Pharmaceuticals is a Pharmaceutical Manufacturing company based in Germany. As a Manufacturing company, they produce medical drugs which get to the consumers through their Distributors.In their efforts to maximise growth, Forggith works with a team of Sales and Marketing pros who ensure retailers are able to get their products through the distributors.Forggith is looking to create some Power BI Reports to assist in guiding their strategies, tactics and operations as a company. For a start, they have identified a couple of numbers they will like to report from their data as reports.
# Reporting Requirements
**A. Sales Performance Overview (Sliced by: Year, Month, Quarter, Team)**

- Total Revenue
- Total Revenue Year To Date (YTD)
- Total Revenue Previous Year YTD
- Total Revenue Same Period Last Year(SPLY)
- Total Target
- Total TargetYTD
- Actual Revenue Performance YTD vs Target YTD
- Revenue Month on Month Percentage Change
- Revenue Distribution by Location
- Revenue by Channel
- Revenue by Product Class
  
**B. Marketing Performance (Slice by Year, Quarter, Month, Product Category and Team)**

- Revenue Achieved vs Revenue Target
- Volume Achieved vs Volume Target
- Actual Revenue by Sales Representative
- Target Revenue Achievement% by Sales Representative
- Actual Volume by Sales Representative
- Target Volume Achievement by Sales Representative
- Actual Revenue Achievement by Sales Team
- Revenue and Volume Achievement by Product.

# Data Source 

The dataset was provided by Ahmed Oyelowo as a one-month internship program on Foresight BI. The dataset consists of 8 tables which includes information on sales transactions as well as set targets for each year.

- DimLocation table: contains city where the store is located, latitude, longitude and a unique identifier.
- DimChannel table: contains channel for drug distribution and a unique identifier.
- Dim SubChannel table: contains sub channel for drugs distribution, channel id and a unique identifier.
- DimProducts table: contains price, name, class of drug and a unique identifier.
- DimEmployees table: contains sales rep name, manager, team and a unique identifier.
- Sales2022: contains monthly transactions of products and quantities sold at different stores for the year 2022.
- Sales2023–2025: contains monthly transactions of products and quantities sold at different stores for the years 2023–2025.
- Target data: contains set targets for the years 2022- 2025.

# Data Cleaning & Transformation
- All 8 tables were imported into Power BI desktop and transformed in power query.
 Both sales tables had similar columns names so they were appended together.
- Each dimension table had its unique identifier in the sales table, except the DimChannel table. The DimChannel tabe was joined with the DimSubChannel table using its unique identifier so as to enable a star schema model.

![forgit dim chanell](https://github.com/user-attachments/assets/de251c83-05bd-4613-babb-df92d058df3b)

- Unpivoting columns in the target table.

![forgit unpivot](https://github.com/user-attachments/assets/f42f5891-af4a-479d-a997-75623059c491)

- Created a Calendar table in Power BI desktop using the DAX formula:
  
  ![dax](https://github.com/user-attachments/assets/4b5a730b-a4bd-428f-8c2c-02afa0e31de4)

 # Data Modelling

- Unique identifiers (Primary keys) in the dimension tables were related to the respective columns (foreign keys) in the facts tables (sales and target tables).
![model](https://github.com/user-attachments/assets/d8992b81-63c6-47e0-b0a1-382865681ba0)

# Visualization

![forgit 1](https://github.com/user-attachments/assets/07efccfa-3b09-45ce-8283-e459bbec22f2)

![forgit 2](https://github.com/user-attachments/assets/545d0291-f7f4-41ed-8a95-ccdbee29a8fe)

# Insights

# Recommendations

