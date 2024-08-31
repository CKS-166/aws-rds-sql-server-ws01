---
title : "Review Backup Options and Take a Manual Snapshot"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 4.1 </b> "
---
- Click on **Databases** from the left navigation pane.
- From the list of databases, click on `sqlerver-rdsssql` under **DB Identifier**.
![CreateDB](/images/3-select-db.png)

- Click on the **Maintenance and backups** tab and scroll down to the **Backup** and **Snapshots** sections.
- In the **Backup** section, you will notice that **Automated Backups** are enabled for 7 days and see the **Backup window**.
![CreateDB](/images/3-backup-screen.png)

- Under **Snapshots**, you may see any snapshots that have been taken so far. If none have been taken, this section will be empty.
![CreateDB](/images/3-take-snapshot.png)

- From the **Snapshots** section, click on **Take snapshot**.
- In the **Take DB Snapshot** dialog, provide the **Snapshot name**: `snapshot-sqlerver-rdsssql` and click on **Take Snapshot**.
![CreateDB](/images/3-take-db-snapshot.png)


- Under **Snapshots**, click on the **Manual** tab and notice the snapshot you just took.
  - It may take about 20 minutes for the operation to complete and for the snapshot creation time to appear. You may proceed with the rest of the labs and come back later to check on the status.
![CreateDB](/images/3-snapshot-view.png)

- Optionally, you may view all snapshots by clicking on Snapshots section. To see automatic snapshots, click on System tab
![CreateDB](/images/3-snapshot-view2.png)
