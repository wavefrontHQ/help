### Understanding Slow Queries

The Slow Query Dashboard page helps you understand why certain queries take a long time to display. Section links that display after you scroll down the page allow you to jump down to sections containing details.

**Dashboard** summarizes slow queries in the system. You can quickly see the number of slow queries, which slow queries failed to complete vs. which queries took a long time but eventually completed. It also provides you with the number of slow queries by user. The time window [1h, 12h, 1d] buttons control which slow queries you are viewing. 

**Slow Queries** provides details (timestamp, query type, ts() query, points, etc.) about the slow queries.

**Resource Consumption by User** displays each user that ran a slow query in that window and provides details such as time spent, total points scanned, and total CPU consumed.
