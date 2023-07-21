# Customer Service Analysis with Microsoft Fabric
This GitHub Repo intends to give an example how to use Microsoft Fabric for the end to end scenario of getting insights into the performance of the sample data set [Call Center Data from Kaggle](https://www.kaggle.com/datasets/satvicoder/call-center-data?resource=download)

###### Disclaimer: In order to replicate this analysis, you need to sign up for [Microsoft Fabric](https://learn.microsoft.com/en-us/fabric/get-started/fabric-trial)

[Microsoft Fabric Blog Announcement](https://azure.microsoft.com/en-us/blog/introducing-microsoft-fabric-data-analytics-for-the-era-of-ai/)
![alt text](media/MicrosoftFabric.webp)

Microsoft Fabric was announced in Public Preview at Microsoft's Build conference in May 2023. This SaaS product enables end-to-end analytics within one product. From data integration, data pre-processing and engineering to data science and business intelligence, Fabric enables teams to collaborate in a no-/low-code and pro developer environment. Each individual can interact with the respective engine within Fabric according to their skills, be it via Data Factory to bring in data, to using Spark Notebooks or SQL Scripts, to creating PowerBI reports. "Switching" between these different workloads, will give the user a different landing page to start working with the data that is stored in OneLake in the open source Delta Parquet format, for every engine in Fabric to access without the need for data duplication and file format change.

## Let's look at a concrete example that can be found cross-industry: Customer Service Performance
Say suppose an organization is selling B2C products and offers customer service support for whatever inquiry, support or complaint the end user might have. There are several ways how the customer can interact with the company's customer service team: via social media, email, chat or phone calls. The first important step for analyzing the support performance is to consolidate all the data that can be gathered across the interactions with the customer in one place. This one place is called OneLake in Microsoft Fabric, which is an optimized storage for big data analytics workloads, supporting structured, semi-/and un-structured file formats. 

## Prerequisites
- You need a Microsoft Fabric subscription or sign up for a free [Microsoft Fabric (Preview) trial](https://learn.microsoft.com/en-gb/fabric/enterprise/licenses)
- Sign in to [Microsoft Fabric](https://fabric.microsoft.com/)
- Use an existing Microsoft Fabric lakehouse or create a new once by following the steps in this [tutorial](https://learn.microsoft.com/en-gb/fabric/data-engineering/create-lakehouse)

## Step by Step guide for customer service analysis
1. Load Data: Data Engineers can use the [Data Factory](https://learn.microsoft.com/en-us/fabric/get-started/fabric-trial) feature inside of Fabric to ingest, prepare and transform data from other sources and land it into OneLake. In our example, we will upload local files 
   - In Fabric, navigate to the Data Factory experience by clicking on the icon at the bottom left (this is where you switch between the workloads)
   - 
3. Once data is stored in OneLake, it can be used and processed by various engines and therefore people with different skills. For example, merging and pre-processing different data can be achieved in the Spark environment inside the [Synapse Data Engineering experience](https://learn.microsoft.com/en-us/fabric/data-engineering/data-engineering-overview). A data engineer would create within seconds a new lakehouse and a Spark Notebook to transform raw data and get first insights with PySpark, Spark SQL, Spark (Scala), SparkR or HTML. Here is a Notebook you can use to run on the data provided above: PLACEHOLDER
4.  The pre-processing data can then be used (without duplication!) by the [Synapse Data Warehouse](https://learn.microsoft.com/en-us/fabric/data-warehouse/data-warehousing) to perform some SQL queries. This lake-centric data warehouse provides an environment for any skill level from citizen developer to DBAs or pro devs. With the always connected dataset that is integrated into PowerBI, users can achieve via the so-called Direct Lake mode, lighting-fast data visualization and report creation. With the revamped SQL engine over the open source data format, users can focus on their main tasks for data analysis.
5.  With the processed dataset, a business analyst (or any other user obivously) can create with the [Fabric PowerBI experience](https://learn.microsoft.com/en-us/power-bi/fundamentals/fabric-get-started) a semantic business model and BI report by accessing the file directly in OneLake. Anyone knowing and having worked with PowerBI before, will feel familiar with this feature.

