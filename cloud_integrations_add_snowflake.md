### Add a Snowflake Integration

Use the Snowflake integration to monitor a Snowflake database and the ACCOUNT_USAGE schema. 

To register a new Snowflake instance and start monitoring the Snowflake usage, you must give Tanzu Observability access to your Snowflake account. The overall process involves:

* Generating a private and a public key. 
  Snowflake supports key-pair authentication for enhanced authentication security. 
* Creating a custom role that will monitor the Snowflake usage, for example `MYROLE`.
* Granting the role with the `usage` and `monitor` privileges on the warehouse.
* Assigning the role to a new or an already existing user who has the public key assigned.

You can follow the steps provided in our GUI.

After you generate the private and the public keys and create a user with the correct permissions, to register your Snowflake integration, follow these steps:

1. In the **Name** text box, provide a meaningful name.
2. In the **Account ID** text box, enter the Snowflake account identifier with the account name, `<orgname>-<account_name>`.
   For information about the Snowflake account identifiers, see the [Snowflake documentation](https://docs.snowflake.com/en/user-guide/admin-account-identifier.html).
3. Enter the Snowflake user name in the **User Name** text box.

4. Enter the private key in the **Private Key** text box.

   The private key that you enter must begin with the line `----BEGIN PRIVATE KEY----` and end with the line `----END PRIVATE KEY----`. The private key is securely stored and never exposed except for read-only access to the Snowflake APIs.
   
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
