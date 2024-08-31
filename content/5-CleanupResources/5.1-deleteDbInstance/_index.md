+++
title = "Delete Database Instance"
weight = 1
chapter = false
pre = "<b>5.1 </b>"
+++

Follow these steps to remove any read replica or database instance(s) created in the workshop.

**Delete Database Instance**

1. Open the **Amazon RDS service console** and click on **Databases** from the left navigation pane.

2. From the list of databases, select `workshop-maz-rds-sqlserver` under **DB identifier** and then click on **Modify**.
![DeleteS3](/images/5-modify-db.png)

3. On the modify page, scroll to the bottom of the page. Uncheck the **Enable deletion protection** option, then click on **Continue**.
![DeleteS3](/images/5-modify-db-screen.png)

4. Select **Apply immediately**, and click on **Modify DB Instance**.
![DeleteS3](/images/5-apply-modify.png)

5. From the list of databases, select `workshop-maz-rds-sqlserver`, and select **Delete** from the Actions dropdown menu.
![DeleteS3](/images/5-delete-db.png)

6. On the Delete instance page, uncheck the **Create final snapshot?** and **Retain automated backups** options. Select the option for **I acknowledge that upon instance deletion, automated backups, including system snapshots and point-in-time recovery, will no longer be available**. Type `delete me` in the textbox to confirm deletion of the database instance, then press the **Delete** button.
![DeleteS3](/images/5-delete-db-screen.png)

