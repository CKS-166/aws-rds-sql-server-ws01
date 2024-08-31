---
title : "Create a RDS DB Instance"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 2.1 </b> "
---

- Open the Amazon RDS service console and navigate to the **Databases** section.

- Click **Create database** to start the configuration process.

![CreateDB](/images/2-startcreatedb.png)

**Choose a Database Creation Method**
- In the **Choose a database creation method** section, select **Standard Create**.
- Under **Engine options**, select **Microsoft SQL Server**.
- In the **Edition** section, select **SQL Server Enterprise Edition**.
- Choose the latest version (e.g., SQL Server 2019 15.xx.xx).
![CreateDB](/images/2-createdboptions.png)
![CreateDB](/images/2-createdb-version2.png)

{{% notice note %}}
For this workshop SQL Server Enterprise Edition has been selected and will incur some cost. To use free tier, select SQL Server Express Edition under Editions. Note that some of the advanced features are not supported with SQL Server Express Edition.
{{% /notice %}}

**Templates**
- Select the **Production** template.
![CreateDB](/images/2-createdb-template.png)

**Settings**
- **DB instance identifier**: `sqlserver-rdssql`
- **Master username**: `admin`
- **Master password**: Enter a password.

![CreateDB](/images/2-createdb-setting.png)

**DB Instance Size**
- **DB instance class**: Select **Standard classes** and choose `db.m5.xlarge` from the dropdown.
![CreateDB](/images/2-createdb-instancesize.png)


**Storage**
- **Storage type**: Provisioned IOPS (SSD)
- **Allocated storage**: 20 GiB
- **Provisioned IOPS**: 1000
- **Storage autoscaling**: Check **Enable storage autoscaling**
- **Maximum storage threshold**: 1000 GiB
![CreateDB](/images/2-createdb-storage.png)


**Availability & Durability**
- For this workshop, do not enable Multi-AZ. This feature will be covered in a future section of the workshop.
![CreateDB](/images/2-createdb-availability.png)


**Connectivity**
- **Compute resource**: Don't connect to an EC2 compute resource.
- Expand **Additional connectivity configuration**:
- **Publicly accessible**: No
- **VPC security group**: Choose existing
- **Availability Zone**: Leave default
- **Database port**: Leave default
![CreateDB](/images/2-createdb-connectivity.png)


**Create the Database**
- Leave all other options default and click on **Create database** to create the database.
![CreateDB](/images/2-createdb-last.png)
- It will take a few minutes to provision the Database Instance. You can monitor the provisioning progress from the **Databases List**. The status will change to **Available** once the instance is provisioned.
- Press the Refresh icon to check the latest status progress.
![CreateDB](/images/2-createdb-creating.png)
