### Viewing and Managing Ingestion Policies
An ingestion policy is a set of accounts, groups, sources, metric namespaces, or point tags, for which you can monitor the PPS usage and set limits.

**Note**: All users can view the ingestion policies and the dashboards. Only **Super Admin** users can create, edit, and delete ingestion policies and the associated alerts. Only **Super Admin** users can view the policy versions.

This page shows a paginated table of all existing ingestion policies. For each policy:

* The **State** column shows the policy state in terms of PPS limit for the current billing period. The *red* state indicates that the limit is exceeded. The *green* state indicates that the limit is not reached or not set.
* The **Current Usage vs Limit** column shows the policy PPS usage for the current billing period. The *green* progress bar indicates that the usage is below 80% of the limit. The *orange* progress bar indicates that the usage is above 80% of the limit but the limit is not reached yet. The *red* progress bar indicates that the limit is exceeded.
* The **Usage Trend** column shows a line chart of the policy PPS usage from the beginning of the current billing period.

To locate an ingestion policy, in which you're interested, you can:
* Sort the ingestion policies by name, scope, current usage, limit, or time of the last update. 
* Search and, optionally, save and share your search by using the Search field above the ingestion policies table.
* Filter the ingestion policies by the accounts who performed the last updates or by using your saved searches on the left.

To drill down and examine the PPS usage by a particular ingestion policy over time, click the name of the ingestion policy and examine the ingestion policy dashboard.

**Read More**<br/>
[Examine Usage with Ingestion Policies](https://docs.wavefront.com/ingestion_policies.html)
