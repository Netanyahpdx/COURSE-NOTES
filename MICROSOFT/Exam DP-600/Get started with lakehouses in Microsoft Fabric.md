# GET STARTED WITH LAKEHOUSES IN MICROSOFT FABRIC #

**INTRODUCTION**
The foundation of Microsoft Fabric is a lakehouse, which is built on top of the OneLake scalable storage layer and uses Apache Spark and SQL compute engines for big data processing.   
A lakehouse is a unified platform that combines:  
- The flexible and scalable storage of a data lake
- The ability to query and analyze data of a data warehouse   

Imagine your company has been using a data warehouse to store structured data from its transactional systems, such as order history, inventory levels, and customer information.  
You collect unstructured data from social media, website logs, and external sources that are difficult to manage and analyze using the existing data warehouse infrastructure.
Your company's new directive is to improve its decision-making capabilities by analyzing data in various formats across multiple sources, so the company chooses Microsoft Fabric.

In this module, we explore how a lakehouse in Microsoft Fabric provides a scalable and flexible data store for files and tables that you can query using SQL.

---

**EXPLORE THE MICROSOFT FABRIC LAKEHOUSE**    
A **lakehouse** presents as a database and is built on top of a data lake using Delta format tables.  
Lakehouses combine the SQL-based analytical capabilities of a relational data warehouse and the flexibility and scalability of a data lake.  
Lakehouses store all data formats and can be used with various analytics tools and programming languages.  
As cloud based solutions, lakehouses can scale automatically and provide high availability and disaster recovery.   
  
![image](https://github.com/user-attachments/assets/1e72af99-61b5-46dd-b862-b0e0409f1ecc)  
  
**Some benefits of a lakehouse include:**    
- Lakehouses use Spark and SQL engines to process large-scale data and support machine learning or predictive modeling analytics.  
- Lakehouse data is organized in a schema-on-read format, which means you define the schema as needed rather than having a predefined schema.  
- Lakehouses support ACID (Atomicity, Consistency, Isolation, Durability) transactions through Delta Lake formatted tables for data consistency and integrity.  
- Lakehouses are a single location for data engineers, data scientists, and data analysts to access and use data.  
A lakehouse is a great option if you want a scalable analytics solution that maintains data consistency.  
It's important to evaluate your specific requirements to determine which solution is the best fit.  

---

**LOAD DATA INTO A LAKEHOUSE:**  

Fabric lakehouses are a central element for your analytics solution.  
You can follow the ETL (Extract, Transform, Load) process to ingest and transform data before loading to the lakehouse.

You can ingest data in many common formats from various sources, including local files, databases, or APIs.  
You can also create Fabric shortcuts to data in external sources, such as Azure Data Lake Store Gen2 or OneLake.  
Use the Lakehouse explorer to browse files, folders, shortcuts, and tables and view their contents within the Fabric platform.

Ingested data can be transformed and then loaded using either using Apache Spark with notebooks or Dataflows Gen2.  
Use Data Factory pipelines to orchestrate your different ETL activities and land the prepared data into your lakehouse.

 **Note:** Dataflows Gen2 are based on Power Query - a familiar tool to data analysts using Excel or Power BI that provides visual representation of transformations as an alternative to traditional programming.

**You can use your lakehouse for many reasons, including:**  
- Analyze using SQL.  
- Train machine learning models. 
- Perform analytics on real-time data.  
- Develop reports in Power BI.  

---

**SECURE A LAKEHOUSE**  

Lakehouse access is managed either through the workspace or item level sharing.  
Workspaces roles should be used for collaborators because these roles grant access to all items within the workspace.  
Item level sharing is best used for granting access for read only needs, such as analytics or Power BI report development.  
Fabric lakehouses also support data governance features including sensitivity labels, and can be extended by using Microsoft Purview with your Fabric tenant.  

**Note:** For more information, see the Security in Microsoft Fabric documentation.

---

**WORK WITH MICROSOFT FABRIC LAKEHOUSES**  
Now that you understand the core capabilities of a Microsoft Fabric lakehouse, let's explore how to work with one.

**CREATE & EXPLORE A LAKEHOUSE**
When you create a new lakehouse, you have three different data items automatically created in your workspace.

- The lakehouse contains shortcuts, folders, files, and tables.  
- The Semantic model (default) provides an easy data source for Power BI report developers.  
- The SQL analytics endpoint allows read-only access to query data with SQL.  
![image](https://github.com/user-attachments/assets/f7c4945b-ee46-45b9-aaa4-dd54c4528f9b)  
You can work with the data in the lakehouse in 2 modes:  
- **LAKEHOUSE** enables you to add and interact with tables, files, and folders in the lakehouse.
- **SQL analytics endpoint** enables you to use SQL to query the tables in the lakehouse and manage its relational semantic model.

![image](https://github.com/user-attachments/assets/7d397075-133b-48ed-95a4-f8b16ecfd235)

---

**INGEST DATA INTO A LAKEHOUSE**  
Ingesting data into your lakehouse is the 1ST step in your ETL process.  
Use any of the following methods to bring data into your lakehouse.   
  
- **Upload**: Upload local files.  
- **Dataflows Gen2**: Import and transform data using Power Query.  
- **Notebooks**: Use Apache Spark to ingest, transform, and load data.  
- **Data Factory pipelines**: Use the Copy data activity.  
This data can then be loaded directly into files or tables.
Consider your data loading pattern when ingesting data to determine if you should load all raw data as files before processing or use staging tables.  

**Spark job definitions** can also be used to submit batch/streaming jobs to Spark clusters.  
By uploading the binary files from the compilation output of different languages (for example, .jar from Java), you can apply different transformation logic to the data hosted on a lakehouse.  
Besides the binary file, you can further customize the behavior of the job by uploading more libraries and command line arguments.  

 **Note:** For more information, see the Create an Apache Spark job definition documentation.

---

**ACCESS DATA USING SHORTCUTS**   

Another way to access and use data in Fabric is to use *shortcuts*.  
Shortcuts enable you to integrate data into your lakehouse while keeping it stored in external storage.  

Shortcuts are useful when you need to source data that's in a different storage account or even a different cloud provider.  
Within your lakehouse you can create shortcuts that point to different storage accounts and other Fabric items like data warehouses, KQL databases, and other lakehouses.
   
Source data permissions and credentials are all managed by OneLake.  
When accessing data through a shortcut to another OneLake location, the identity of the calling user will be utilized to authorize access to the data in the target path of the shortcut.  
The user must have permissions in the target location to read the data.  
   
Shortcuts can be created in both lakehouses and KQL databases, and appear as a folder in the lake.   
This allows Spark, SQL, Real-Time intelligence and Analysis Services to all utilize shortcuts when querying data.  

**Note:** For more information on how to use shortcuts, see OneLake shortcuts documentation in the Microsoft Fabric documentation.

---

**EXPLORE & TRANSFROM DATA IN A LAKEHOUSE**

**TRANSFORM & LOAD DATA**
Most data requires transformations before loading into tables.  
You might ingest raw data directly into a lakehouse and then further transform and load into tables.  
Regardless of your ETL design, you can transform and load data simply using the same tools to ingest data.  
Transformed data can then be loaded as a file or a Delta table.  
   
- Notebooks are favored by data engineers familiar with different programming languages including PySpark, SQL, and Scala.  
- Dataflows Gen2 are excellent for developers familiar with Power BI or Excel since they use the PowerQuery interface.  
- Pipelines provide a visual interface to perform and orchestrate ETL processes. Pipelines can be as simple or as complex as you need.  
   
---
  
**ANALYZE & VISUALIZE DATA IN A LAKEHOUSE**  
    
After data is ingested, transformed, and loaded, it's ready for others to use.   
Fabric items provide the flexibility needed for every organization so you can use the tools that work for you.  
  
Data scientists can use notebooks or Data wrangler to explore and train machine learning models for AI.
Report developers can use the semantic model to create Power BI reports.
Analysts can use the SQL analytics endpoint to query, filter, aggregate, and otherwise explore data in lakehouse tables.
By combining the data visualization capabilities of Power BI with the centralized storage and tabular schema of a data lakehouse, you can implement an end-to-end analytics solution on a single platform.  


project











