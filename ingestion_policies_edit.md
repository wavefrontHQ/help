### Edit an Ingestion Policy
You can edit an ingestion policy and the alert associated with the PPS limit. Editing an ingestion policy creates a new version of that policy.

1. In the **Data** panel, you can do the following changes and click **Next**.

    * Add and remove accounts or objects from the policy scope. You cannot change the scope.
    * Set, update, or remove the PPS limit per billing period for the policy.
    
    Removing the PPS limit dissociates the alert from the ingestion policy and deletes the alert.
2. If you set or updated the PPS limit, you can also configure the alert settings.

    1. In the **Conditions** panel, select the comparison operator for the alert condition, specify the threshold for at least one severity, and click **Next**.
    2. In the **Recipients** panel,  specify who will receive the alert notifications and click **Next**.
    3. Enter the name of the alert, optionally add tags, and click **Next**.
3.	Enter the policy name and, optionally, a description and click **Save**.

**Read More**<br/>
[Examine Usage with Ingestion Policies](https://docs.wavefront.com/ingestion_policies.html)
