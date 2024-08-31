---
title : "Retrieve DB Instance Endpoint"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 2.2 </b> "
---

- To connect to the DB instance and use it in subsequent labs, you need to retrieve the DB instance endpoint.
- Open the Amazon RDS console and go to the **Databases** section.
- Select the DB Identifier: `sqlserver-rdssql`.
![CreateDB](/images/3-select-db.png)

**Retrieve the Endpoint.**
- Go to the **Connectivity and security** tab on the details page.
- In the **Endpoint & port** section, locate the endpoint of the instance.
![CreateDB](/images/2.2-db-endpoint.png)

- Copy the endpoint and paste it into a notepad to keep it handy for the next steps.
