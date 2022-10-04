### Creating an Ingestion Policy
When you create an ingestion policy, you must specify the policy scope and name. Optionally, you can configure a PPS limit and an alert.

The **Scope**, for which you want to monitor the PPS usage, can be one of the following options:

* [Accounts](http://docs.wavefront.com/authorization-faq.html#what-are-user--service-accounts), which can be user and service accounts. You must assign one or more existing accounts.
* [Groups](http://docs.wavefront.com/users_roles.html#create-a-group), which can include user and service accounts. You must assign one or more existing groups.
* [Sources](http://docs.wavefront.com/sources_managing.html), which emit metrics. You can assign exact source names or names with wildcards, for example, <code>appServer1</code> and <code>appServer*</code>.
* [Namespaces](http://docs.wavefront.com/metrics_managing.html#metrics-browser), which group metrics in a hierarchy defined by a name prefix. You can assign exact metric names and namespaces, for example, <code>request.</code> and <code>requests</code>. You can also assign names with wildcards, for example, <code>cpuloadavg*</code> and <code>cpu.*</code>.
* [Point tags](http://docs.wavefront.com/metrics_managing.html#time-series-with-tags), which are optional key-value pairs associated with a metric. You must assign one or more existing point tag pairs, for example, <code>env="dev"</code>. If you assign multiple point tags, you must select the match criterion - either **Has tags** (individual point tags) or **Has all these tags** (a combination of point tags).

**Note**: After you create the policy, you cannot change the scope. You can change only the assigned accounts or objects from that scope. For example, for an ingestion policy that is scoped for groups, you can only add and remove groups for that policy, but you cannot change the scope to accounts or else.
    
If you **Set a PPS limit** per billing period for the policy, you must configure the **Conditions**, **Recipients**, and **Alert Name and Tags** for the associated alert.

**Read More**<br/>
[Examine Usage with Ingestion Policies](https://docs.wavefront.com/ingestion_policies.html)
