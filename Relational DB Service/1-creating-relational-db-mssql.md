{{{
  "title": "Creating an MSSQL Server Relational Database",
  "date": "01-22-2019",
  "author": "",
  "attachments": [],
  "related_products": [],
  "related_questions": [],
  "preview" : "How to create an MSSQL Server Relational Database",
  "thumbnail": "../images/mssql-server-relational-db-preview.png",
  "contentIsHTML": false
}}}

<iframe width="560" height="315" src="https://player.vimeo.com/video/255618938" frameborder="0" allowfullscreen></iframe>
<br>
<br>
This video series shows how to quickly create a Microsoft SQL Server Relational Database. In Part 1, we will demonstrate how to create a new database.

### Introduction

The Microsoft SQL Server (MS-SQL) database is a comprehensive and integrated data management and analysis software application that enables the reliable management of mission-critical information. With a Relational DB, you can create, modify, and delete tables, as well as select, insert, and delete data from existing tables.

### Creating a Relational DB

![RDBS Create Database](../images/rdbs/create1.png)

There are two ways to create a relational database from the DBaaS dashboard. You can click *Create* in the left-hand menu, then select *Relational DB*, or you can select *Services* and then *Relational DB*. This method will take you to a list of your existing databases, where you can create a new one by clicking on the green button at the top of the page.

![RDBS Create Database](../images/rdbs/create2.png)

On the *Create Database* page, there are multiple sections. The Cost Estimator and the Bill Time estimator also show you the amount of CPU, Memory and Storage you have allocated. Other sections show Resources and Options.

![RDBS Create Database](../images/rdbs/create3.png)

To create a database, go to the top dropdown and choose MSSQL, then select the version and edition.

![RDBS Create Database](../images/rdbs/create4.png)

Next, choose a CenturyLink data center location, then a network from your local network, and a unique identifier.

![RDBS Create Database](../images/rdbs/create5.png)

Finally, create and confirm a password for your database. Make sure it is stored safely.

![RDBS Create Database](../images/rdbs/create6.png)

The default settings in the Resources section are the minimums required for acceptable performance. You can set the figures in the CPU, Memory and Storage dropdowns higher to meet your requirements. Note that this will automatically increase the figures in the cost estimator.

![RDBS Create Database](../images/rdbs/create7.png)

In the Options section, you can set Replication to create a replica of the primary database, and choose its location and network. You can also enable Notifications, customize the backup schedule, and select the number of days backups will be kept. Some of these options will also incur additional costs that will be reflected in the Estimator.

![RDBS Create Database](../images/rdbs/create8.png)

The final step is to select the *Create Database* button at the bottom of the page to complete the process. This sends you to a Details page where you can review your selections.

**Part 2:** [Configuring an MSSQL Server Relational Database](../Relational DB Service/2-configuring-relational-db-mssql.md)
