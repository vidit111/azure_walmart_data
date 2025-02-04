Data Discription:
  File: features.csv
  Columns: ['Store', 'Date', 'Temperature', 'Fuel_Price', 'MarkDown1', 'MarkDown2', 'MarkDown3', 'MarkDown4', 'MarkDown5', 'CPI', 'Unemployment', 'IsHoliday']
  
  File: stores.csv
  Columns: ['Store', 'Type', 'Size']
  
  File: test.csv
  Columns: ['Store', 'Dept', 'Date', 'IsHoliday']
  
  File: train.csv
  Columns: ['Store', 'Dept', 'Date', 'Weekly_Sales', 'IsHoliday']


 **🚀 ETL Pipeline: Walmart Sales Data Analysis Using PySpark**  

🔹 **Dataset Overview**  
I worked with **Walmart Sales Data**, consisting of the following files:  

📂 **`features.csv`** – Storespecific details:  
`['Store', 'Date', 'Temperature', 'Fuel_Price', 'MarkDown1', 'MarkDown2', 'MarkDown3', 'MarkDown4', 'MarkDown5', 'CPI', 'Unemployment', 'IsHoliday']`  

📂 **`stores.csv`** – Store information:  
`['Store', 'Type', 'Size']`  

📂 **`train.csv`** – Weekly sales data:  
`['Store', 'Dept', 'Date', 'Weekly_Sales', 'IsHoliday']`  



 **🛠️ ETL Process Breakdown**  

1️⃣ **Data Type Correction** – Despite using `inferSchema=True`, some data types were incorrectly inferred. Explicit type casting was applied.  

2️⃣ **Handling Missing Values** – Checked **Markdown15** columns for `null` values.  

3️⃣ **Imputation** – Replaced missing values in **Markdown15** with their respective mean values.  

4️⃣ **Date Format Validation** – Ensured the **Date** column follows the `"yyyyMMdd"` format. No changes were needed.  

5️⃣ **Feature Engineering** – Calculated a **4Week Moving Average** for `Weekly_Sales` to identify trends.  

6️⃣ **StoreWise Sales Analysis** – Aggregated key metrics per store:  
   ✅ `Total_Weekly_Sales`  
   ✅ `Avg_Weekly_Sales`  
   ✅ `Max_Weekly_Sales`  
   ✅ `Min_Weekly_Sales`  
   ✅ `Total_Transactions`  
   
7️⃣ **Merging Datasets** – Combined `stores.csv` with aggregated store performance data for better analytics.  

8️⃣ **Final Data Exports** – Saved the transformed datasets for further **BI Reporting & Visualization**:  
   📌 `joined_data.csv` – Merged dataset for sales analysis.  
   📌 `store_wise_stats.csv` – Storelevel aggregated insights.  



 **🔍 Output Files & Schema**  

📄 **`joined_data.csv`**:  
`['Store', 'Date', 'Temperature', 'Fuel_Price', 'MarkDown1', 'MarkDown2', 'MarkDown3', 'MarkDown4', 'MarkDown5', 'CPI', 'Unemployment', 'IsHoliday', 'Dept', 'Weekly_Sales', 'IsHoliday', '4_Week_Moving_Avg']`  

📄 **`store_wise_stats.csv`**:  
`['Store', 'Total_Weekly_Sales', 'Avg_Weekly_Sales', 'Max_Weekly_Sales', 'Min_Weekly_Sales', 'Total_Transactions', 'Type', 'Size']`  



🔥 **Next Steps:** Visualizing these insights using **Tableau or Power BI** to identify key business trends.  

🚀 Looking for Data Engineering Opportunities!
I am a passionate fresher eager to start my journey in Data Engineering. This project helped me gain hands-on experience in ETL processes, PySpark, and Data Analytics. I am actively looking for opportunities where I can apply my skills, learn, and contribute to impactful projects.

If you're hiring or have any guidance, I would love to connect and discuss potential roles! Feel free to reach out or share any advice in the comments. Let’s build something amazing together! 💡💼
