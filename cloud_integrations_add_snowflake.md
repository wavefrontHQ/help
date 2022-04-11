### Add a Snowflake Integration

Use the Snowflake integration to monitor a Snowflake database and the ACCOUNT_USAGE schema. 

To register a new Snowflake instance and start monitoring the Snowflake usage, you must give Tanzu Observability by Wavefront access to your Snowflake account. The overall process involves the following steps:

    * Create a custom role that will monitor the Snowflake usage, for example `WAVEFRONT`.
    * Grant the monitoring privileges to the new role.
    * Grant the role with the usage privilege on the warehouse.
    * Assign the role to a new or an already existing user.

Follow the instructions in your Wavefront cluster UI if you don't know how to achieve this.

After you created a user with the correct permissions, to register your Snowflake integration, follow these steps:

1. In the **Name** text box, provide a meaningful name.
2. In the **Account ID** text box, enter your account ID.
   For information about the Snowflake account ID, see the [Snowflake documentation](https://docs.snowflake.com/en/user-guide/admin-account-identifier.html).
3. Enter the Snowflake user name and password in the respective text boxes.
4. In the **Role** and **Warehouse** text boxes, enter the role and the warehouse assigned to the user. 
   If you don't specify a role and warehouse, the default ones that are assigned to the user will be used.
4. (Optional) In the **Metric Allow List** text box, add metrics to a metrics allow list by using a regular expression. For example:
    * To monitor only the daily credit usage and a cloud services rebate for an account within the last 365 days (1 year), enter:
      <code>^snowflake.metering-daily-history.*$</code>
    * To monitor the hourly credit usage for a single warehouse (or all the warehouses in your account) within a specified date range, enter:
      <code>^snowflake.warehouse-metering-history.*$</code>
    * To monitor the average daily storage usage, in bytes, for a single database (or all the databases in your account) within a specified date range, enter:
      <code>^snowflake.database-usage-storage-usage-history.*$</code>
5. (Optional) Change the **Service Refresh Rate**. The default is `60` minutes.
6. Click **Register**.
