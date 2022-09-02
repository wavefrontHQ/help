### Creating an Ingestion Policy
When you create an ingestion policy, you specify the following information:

* **Scope** with objects for the policy data. Can be a set of [user and service accounts](http://docs.wavefront.com/authorization-faq.html#what-are-user--service-accounts), [groups](http://docs.wavefront.com/users_roles.html#create-a-group), [sources](http://docs.wavefront.com/sources_managing.html), [metric namespaces](http://docs.wavefront.com/metrics_managing.html#metrics-browser), or [point tags](http://docs.wavefront.com/metrics_managing.html#time-series-with-tags).

    For the point tags scope, you can enter multiple point tags and select the match criterion - either **Has tags** (individual point tags) or **Has all these tags** (a combination of point tags).

    **Note**: After you create the policy, you cannot change the scope. You can change only the assigned objects from that scope. For example, for an ingestion policy that is scoped for groups, you can only add and remove groups for that policy, but you cannot change the scope to accounts or else.
* Optionally, a **PPS Limit** to set a limit of the PPS usage by the ingestion policy.
* If you set a PPS limit, you must configure the **Conditions**, **Recipients**, and **Alert Name and Tags** for the associated alert.
* Policy name and description to **Create** the policy.

**Read More**<br/>
[Examine Usage with Ingestion Policies](https://docs.wavefront.com/ingestion_policies.html)
