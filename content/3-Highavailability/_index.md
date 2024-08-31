---
title : "Enable Multi-AZ HA"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 3 </b> "
---
The instructions on this page provide hands-on experience in enabling Multi-AZ for the RDS instance created in the **Create the DB Instance** section.

- Navigate to the **Databases** section of RDS.
- Select the DB Identifier: `sqlserver-rdssql` and click on **Modify**.
![CreateDB](/images/2.2-modify.png)


- From the **Modify DB Instance** page, scroll down to **Multi-AZ deployment** and select **Yes (Mirroring / Always On)**.
![CreateDB](/images/2.2-modify-screen.png)
![CreateDB](/images/2.2-availability-options.png)

- Scroll down to the bottom of the page and click on **Continue**.
![CreateDB](/images/2.2-continue-modify.png)


- On the **Summary** page under **Scheduling of modifications**, select **Apply Immediately** and then click on **Modify DB Instance**.
![CreateDB](/images/2.2-summary-modify.png)
![CreateDB](/images/2.2-schedule-modify.png)
![CreateDB](/images/2.2-modify-click.png)

  - *Note:* The **Apply Immediately** selection will start the process immediately and could cause downtime. It is recommended to apply these changes during a maintenance window in production or a similar environment. This can be done by selecting **Apply during the next scheduled maintenance window**.

- It will take about 30 minutes for Multi-AZ to be set up. Once the process is complete, the status of the database instance will change from **Modifying** to **Available**.

- From the **Databases** page, check that the status of the database instance `sqlerver-rdsssql` is **Available**, then click on the instance name.
- On the **Summary** page, click on the **Configuration** tab. Note that the Multi-AZ information section shows **Yes (Always On)**. Also, check that the **Region & AZ information** and **Secondary Zone information** sections display primary and secondary instances in different availability zones.
![CreateDB](/images/2.2-db-config-screen.png)


- On the **Summary** page, click on the **Connectivity & security** tab. Copy and paste the **Listener endpoint** information to notepad for later use.
![CreateDB](/images/2.2-listener-endpoint.png)

