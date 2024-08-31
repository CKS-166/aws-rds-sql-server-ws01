---
title : "Point In Time Recovery"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 4.2 </b> "
---

Point in time recovery restores the entire snapshot as a separate instance. In other words, Amazon RDS automation provisions a new instance and then restores all databases from the snapshot image.

- Open the Amazon RDS service console. Click on **Databases** from the left navigation pane.
- From the list of databases, select `sqlerver-rdsssql` under **DB Identifier**.
- From the **Actions** menu, click on **Restore to point in time**.
![CreateDB](/images/3-restore-to-pit.png)

- On the **Restore to point in time** page, select **Latest restorable time** from the **Restore time** option. You may also select a custom point in time by choosing **Custom date and time** and providing the desired date and time.
- Provide the following information:
  - **DB instance identifier:** `restored-sqlerver-rdsssql` (example)
  - **DB instance class:** Burstable classes – `db.t3.2xlarge`
![CreateDB](/images/3-restore-pit-screen.png)
![CreateDB](/images/3-restore-pit-screen2.png)


- Scroll down to the bottom of the page and click on **Restore to point in time**.
![CreateDB](/images/3-restore-pit-click.png)

- On the **Databases** page, you will see that the new instance `restored-sqlerver-rdsssql` is in the **creating** state.
![CreateDB](/images/3-restored-db-creating.png)

- Once completed, the status will change from **Creating** to **Available**. You may connect to the restored instance using its endpoint. The operation will take a few minutes to complete.



**Note:**
- Restore time varies depending on the number of transaction log backups needed to be applied on top of the full backup. To reduce recovery time, you may take manual snapshot backups between daily automatic snapshot backups.