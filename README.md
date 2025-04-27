 Azure Data Pipeline Walmart Sales Forecasting Data Engineering Project

 📌 Project Overview

This project focuses on building anAzure Data Engineering Pipeline forWalmart Sales Forecasting Data. The pipeline automates data ingestion, transformation, and storage usingAzure Data Factory, Azure Data Lake, Databricks, and Synapse Analytics, with visualization inpowerBI.


 📂 Data Details

 📝Raw Data Files

1.features.csv

   `Store`, `Date`, `Temperature`, `Fuel_Price`, `MarkDown1`, `MarkDown2`, `MarkDown3`, `MarkDown4`, `MarkDown5`, `CPI`, `Unemployment`, `IsHoliday`

2.stores.csv

   `Store`, `Type`, `Size`

3.train.csv

   `Store`, `Dept`, `Date`, `Weekly_Sales`, `IsHoliday`

 🔄Transformed Files

1.joined\_data.csv

   `Store`, `Date`, `Temperature`, `Fuel_Price`, `MarkDown1`, `MarkDown2`, `MarkDown3`, `MarkDown4`, `MarkDown5`, `CPI`, `Unemployment`, `IsHoliday`, `Dept`, `Weekly_Sales`, `IsHoliday`, `4_Week_Moving_Avg`

2.store\_wise\_stats.csv

   `Store`, `Total_Weekly_Sales`, `Avg_Weekly_Sales`, `Max_Weekly_Sales`, `Min_Weekly_Sales`, `Total_Transactions`, `Type`, `Size`



 ⚙️ Data Pipeline Workflow

 📥1. Data Ingestion

Source: GitHub (Personal Repository)
Tool Used: Azure Data Factory (ADF)
Process: Imported raw CSV files usingADF's copy activity intoAzure Data Lake Gen2 for secure and scalable storage.

 🔄2. Data Processing & Transformation

Tool Used: Azure Databricks (PySpark)
Process:
  PerformedETL (Extract, Transform, Load) operations.
  Cleaned and preprocessed raw data.
  Merged `features.csv`, `stores.csv`, and `train.csv` to generate `joined_data.csv`.
  Created aggregated storewise statistics (`store_wise_stats.csv`).

 📦3. Data Storage

Tool Used: Azure Data Lake Gen2
Process: Processed data was stored back in Data Lake Gen2, ensuring a structured repository for analysis.

 📊4. Data Analysis & Visualization

Tool Used: Azure Synapse Analytics, powerBI
Process:
  Queried transformed data usingSynapse Analytics for insights.
  CreatedpowerBI visualizations to analyze store performance, sales trends, and holiday impact.



 🛠️ Tools & Technologies Used

GitHub Source control & dataset storage
Azure Data Factory (ADF) Data ingestion
Azure Data Lake Gen2 Scalable cloud storage
Azure Databricks (PySpark) ETL processing & data transformation
Azure Synapse Analytics Querying processed data
powerBI Data visualization


 🚀 How to Use

1. Clone this repository:
   git clone https://github.com/yourreponame.git
2. ConfigureAzure Data Factory to pull data from GitHub.
3. UseDatabricks to process the data.
4. Store processed data inAzure Data Lake Gen2.
5. Load data intoAzure Synapse Analytics.
6. Create powerBI dashboards for insights.


 📩 Contact

shrivastavavidit17@gmail.com


 🔗Future Enhancements

✅ Deploy aMachine Learning Model for sales forecasting using Azure ML. ✅ AutomatepowerBI Dashboard Refresh using Azure Logic Apps.
✅ ImplementRealTime Data Processing using Azure Stream Analytics.

Cheers!
