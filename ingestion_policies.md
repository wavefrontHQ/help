### View and Manage Ingestion Policies
An ingestion policy is a set of accounts, groups, sources, metric namespaces, or point tags, for which you can monitor the PPS usage and set limits.

**Note**: Only users with the **Ingestion Policies** permission can manage ingestion policies.

This page shows a paginated table of all existing ingestion policies. For each policy:

* The **State** column shows the policy state in terms of PPS limit for the current billing period. The *red* state indicates that the limit is exceeded. The *green* state indicates that the limit is not reached or not set.
* The **Current Usage vs Limit** column shows the policy PPS usage for the current billing period. The *green* progress bar indicates that the usage is below 80% of the limit. The *orange* progress bar indicates that the usage is above 80% of the limit but the limit is not reached yet. The *red* progress bar indicates that the limit is exceeded.
* The **Usage Trend** column shows a line chart of the policy PPS usage from the beginning of the current billing period.

On this page you can sort, search for and filter ingestion policies. You can also drill down and examine the PPS usage by a particular ingestion policy over time, by clicking the name of the ingestion policy and viewing the ingestion policy dashboard. 
If you have the **Ingestion Policies** permission, you also can:
* See the policy history by clicking the ellipsis icon next to the policy and selecting **Versions**. You can also revert the policy to an earlier version.
* Edit a policy by clicking the ellipsis icon next to the policy and selecting **Edit**.
* Delete a policy by clicking the ellipsis icon next to the policy and selecting **Delete**.

**Read More**<br/>
[Examine Usage with Ingestion Policies](https://docs.wavefront.com/ingestion_policies.html)
