# INTRODUCTION TO END-TO-END ANALYTICS USING MICROSOFT FABRIC #

Introduction
Microsoft Fabric is an end-to-end analytics platform that provides a single, integrated environment for data professionals and the business to collaborate on data projects.  
Fabric provides a set of integrated services that enable you to ingest, store, process, and analyze data in a single environment.  

Microsoft Fabric provides tools for both citizen and professional data practitioners, and integrates with tools the business needs to make decisions.  
Fabric includes the following services:
- Data engineering
- Data integration
- Data warehousing
- Real-time intelligence
- Data science
- Business intelligence

---

**EXPLORE END-TO-END ANALYTICS WITH MICROSOFT FABRIC**

Scalable analytics can be complex, fragmented, and expensive. 
With Microsoft Fabric, you don't have to spend all of your time combining various services from different vendors.   
Instead, you can use a single product that is easy to understand, set up, create, and manage.   
Fabric offers persona-optimized experiences and tools in an integrated user interface.  
  
In addition to a simple, shared user experience, Fabric is a unified software-as-a-service (SaaS) offering, with all your data stored in a single open format in OneLake.   
OneLake is accessible by all of the analytics engines in the platform.   
Fabric offers scalability, cost-effectiveness, accessibility from anywhere with an internet connection, and continuous updates and maintenance provided by Microsoft.  

**Explore OneLake**
OneLake is Fabric's lake-centric architecture that provides a single, integrated environment for data professionals and the business to collaborate on data projects.  
Fabric's OneLake architecture facilitates collaboration between data team members and saves time by eliminating the need to move and copy data between different systems and teams.  
OneCopy is a key component of OneLake that allows you to read data from a single copy, without moving or duplicating data. 
  
Think of it like OneDrive for data; OneLake combines storage locations across different regions and clouds into a single logical lake, without moving or duplicating data.  
Similar to how Office applications are prewired to use your organizational OneDrive, all the compute workloads in Fabric are preconfigured to work with OneLake.  
Fabric's data warehousing, data engineering (lakehouses and notebooks), data integration (pipelines and dataflows), real time intelligence, and Power BI all use OneLake as their native store without needing any extra configuration. 

![image](https://github.com/user-attachments/assets/1571aef3-c23b-46af-b8d8-318b8cf447fe)

OneLake is built on top of Azure Data Lake Storage (ADLS) and data can be stored in any format, including Delta, Parquet, CSV, JSON, and more.   
What this means is that all of the compute engines in Fabric automatically store their data in OneLake.   
Data that is stored in OneLake is then directly accessible by all of the compute engines without needing to be moved or copied. 
For tabular data, the analytical engines in Fabric write data in delta-parquet format and all engines interact with the format seamlessly.  

1 important feature of OneLake is the ability to create shortcuts, which are embedded references within OneLake that point to other files or storage locations.   
Shortcuts allow you to quickly source your existing cloud data without having to copy it, and enables Fabric experiences to derive data from the same source to always be in sync.  

![image](https://github.com/user-attachments/assets/08efc7e3-0857-41f7-8907-759953668cb7)

---

**EXPLORE FABRIC'S EXPERIENCES**
Fabric offers a set of analytics experiences that are designed to accomplish specific tasks and work together seamlessly.  

**FABRIC EXPERIENCES:**
- Synapse Data Engineering: data engineering with a Spark platform for data transformation at scale.
- Synapse Data Warehouse: data warehousing with industry-leading SQL performance and scale to support data use.
- Synapse Data Science: data science with Azure Machine Learning and Spark for model training and execution tracking in a scalable environment.
- Synapse Real-Time Intelligence: real-time intelligence to query and analyze large volumes of data in real-time.
- Data Factory: data integration combining Power Query with the scale of Azure Data Factory to move and transform data.
- Power BI: business intelligence for translating data to decisions through interactive reports.
- Fabric provides a comprehensive data analytics solution by unifying all these experiences on a single platform.

---

**EXPLORE WORKSPACES:**
Fabric uses workspaces to contain the different items created across the different experiences.  
Each organization can customize how to separate and control access to the items.  
Some possibilities include *a dedicated workspace for lakehouse development* and *a separate workspace for the production lakehouse*.  

In Microsoft Fabric, workspaces serve as logical containers that help you organize and manage your data, reports, and other assets.  
They provide a clear separation of resources, making it easier to control access and maintain security.  
Each workspace can have its own set of permissions, ensuring that only authorized users can view or modify the contents.  
This structure supports collaboration within teams while maintaining strict access control, which is crucial for both business and IT users.  

Workspaces in Microsoft Fabric also offer settings to manage compute resources and integrate with Git for version control.  
You can configure compute settings to optimize performance and cost, ensuring that your resources are used efficiently.  
Git integration allows you to track changes, collaborate on code, and maintain a history of your work, which is essential for development and data management.  
Additionally, workspaces support features like data lineage and impact analysis, providing a comprehensive view of data flow and dependencies, which enhances transparency and decision making.  

---

**EXPLORE SECURITY & GOVERNANCE:**
Fabric's OneLake is centrally governed and open for collaboration.  
Data is secured and governed in one place, which allows users to easily find and access the data they need.  
Fabric administration is centralized in the admin center.  
  
In the admin center you can manage groups and permissions, configure data sources and gateways, and monitor usage and performance.  
You can also access the Fabric admin APIs and SDKs in the admin center, which you'd use to automate common tasks and integrate Fabric with other systems.  

Your Fabric tenant is natively integrated with Microsoft Purview Information Protection.  
Fabric uses Microsoft Purview Information Protection’s sensitivity labels to help your organization classify and protect sensitive data, from ingestion to export.  

---

**DATA TEAMS & MICROSOFT FABRIC**
Microsoft Fabric's unified data analytics platform makes it easier for data professionals to work together on data projects.  
Fabric removes data silos and the need for access to multiple systems, enhancing collaboration between data professionals.  

**TRADITIONAL ROLES & CHALLENGES:**
In a traditional analytics development process, data engineers and data analysts face several challenges.  
Data engineers perform complex data processing and then curate and serve data sources so data analysts can display data effectively for the business.  
This process requires extensive communication and coordination between the two roles, often leading to potential delays and misinterpretations.  

Data analysts need to perform extensive downstream data transformations before creating Power BI reports.  
This time consuming process often lacks context, making it difficult for analysts to connect with data directly.  

Data scientists also struggle to integrate native data science techniques with existing data systems, which are often complex and cumbersome.  
As a result, data scientists find it challenging to provide data-informed insights efficiently.  

---

**EVOLUTION OF COLLABORATIVE WORKFLOWS**
Microsoft Fabric transforms the analytics development process by unifying tools into a SaaS platform, allowing flexibility for different roles to perform necessary skills without duplicating efforts.

Data engineers can now ingest, transform, and load large amounts of data into OneLake and present it in whichever data store makes most sense.  
Data loading patterns are simplified using pipelines and architectures, such as medallion, can be easily configured using workspaces.

Data analysts gain greater context and streamline processes, transforming data upstream with Data Factory and connecting with data more directly using DirectLake mode.

Data scientists Integrate native data science techniques more easily and use Power BI's interactive reporting to provide data informed insights.

Analytics engineers bridge the gap between data engineering and data analysis by curating data store assets, ensuring data quality, and enabling self service analytics.

Low-to-no-code users and citizen developers can now discover curated data through the OneLake hub, and further process and analyze it to suit their needs without being dependent on data engineers or duplicating data.

---

**ENABLE & USE MICROSOFT FABRIC**  
Before you can explore the end-to-end capabilities of Microsoft Fabric, it must be enabled for your organization.  
You might need to work with your IT department to enable Fabric for your organization.  
The permissions required to enable Fabric are either:  
- Fabric admin (formerly Power BI admin)  
- Power Platform admin  
- Microsoft 365 admin  

**ENABLE MICROSOFT FABRIC**   
If you have admin privileges, you can access the **Admin center** from the **Settings** menu in the upper right corner of the Power BI service.   
From here, you enable Fabric in the **Tenant settings**.  

Admins can make Fabric available to either the entire organization or specific groups of users, who can be organized based on their Microsoft 365 or Microsoft Entra security groups.  
Admins can also delegate the ability to enable Fabric to other users, at the capacity level.  

![image](https://github.com/user-attachments/assets/319342d9-8d9d-4092-8b47-f0f263db8277)

---

**CREATE WORKSPACES**
Workspaces are collaborative environments where you create and manage items like lakehouses, warehouses, and reports.  
All data is stored in OneLake, and is accessed through workspaces.  
Items are displayed in a list or lineage view, which is a visual representation of the dependency between items.  
  
In the Workspace settings, you can configure the license type to use Fabric features.  
There are several other settings you can configure in this area, some of which include:  
- OneDrive access for the workspace  
- Azure Data Lake Gen2 Storage connection  
- Integration with Git for version control  
- Spark workload settings  

![image](https://github.com/user-attachments/assets/2e13f7ca-4a07-4423-91a2-2d643fb6e111)
![image](https://github.com/user-attachments/assets/d7a31abf-6dbf-4c42-a309-74b9313a1ffb)

To grant access to a workspace, choose one of the four available roles.  
These roles have access to all items in a workspace.  
Workspace access is typically granted to collaborators, and it's recommended to grant access to specific items depending on the business need.   

---

**DISCOVER DATA WITH ONELAKE DATA HUB**  
The OneLake data Hub in Microsoft Fabric helps users easily find and access various data sources within their organization.  
Users explore and connect to data sources, ensuring they have the right data for their needs.   
Users only see items shared with them.   
Here are some considerations when using OneLake Hub:  
- Narrow results by domains (if implemented).  
- Filter by workspaces in Explorer.  
- Explore default groups: All data, My data, Endorsed in your org, and Favorites.  
- Filter further by keyword or item type.  

![image](https://github.com/user-attachments/assets/fe558ac8-2d4b-4794-af8c-3d1cac4afeb4)

---

**CREATE ITEMS IN FABRIC**
After you create your Fabric enabled workspace, you can start creating items in Fabric.  
You can create items in Fabric using the Create menu in the upper left corner of the Power BI service.  

![image](https://github.com/user-attachments/assets/c8943394-e9aa-4686-8b30-9ee3f0d241b6)

---

**EXPLORE FABRIC WORKLOADS**
Fabric workloads refer to the different capabilities included in Fabric.  
You can switch between workloads using the workload switcher in the bottom left corner of the navigation pane.  

![image](https://github.com/user-attachments/assets/620c7d2b-165b-44bb-8681-f0079bc562cb)

You might notice that Fabric workloads look similar to other Microsoft data offerings.  
Fabric is built on Power BI and Azure Data Lake Storage, and includes capabilities from Azure Synapse Analytics, Azure Data Factory, Azure Databricks, and Azure Machine Learning.  
What makes Fabric unique is that it brings these capabilities together in a single, SaaS integrated experience without the need for access to Azure resources.  

---

**KNOWLEDGE CHECK**

1. Which of the following is a key benefit of using Microsoft Fabric in data projects?   
It provides a single, integrated environment for data professionals and the business to collaborate on data projects.  

2. What is the default storage format for Fabric's OneLake? 
DELTA   

3. Which of the following Fabric experiences is used to move and transform data?  
DATA FACTORY  








