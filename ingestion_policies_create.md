### Create an Ingestion Policy

1. An ingestion policy is a set of accounts, groups, sources, metric namespaces, or point tags, for which you can monitor the PPS usage and set limits. Choose the **Scope**, for which you want to monitor the PPS usage, and click **Next**.

* [Accounts](http://docs.wavefront.com/authorization-faq.html#what-are-user--service-accounts), which can be user and service accounts. You must assign one or more existing accounts.
* [Groups](http://docs.wavefront.com/users_roles.html#create-a-group), which can include user and service accounts. You must assign one or more existing groups.
* [Sources](http://docs.wavefront.com/sources_managing.html), which emit metrics. You can assign exact source names or names with wildcards, for example, <code>appServer1</code> and <code>appServer*</code>.
* [Namespaces](http://docs.wavefront.com/metrics_managing.html#metrics-browser), which group metrics in a hierarchy defined by a name prefix. You can assign exact metric names and namespaces, for example, <code>request.</code> and <code>requests</code>. You can also assign names with wildcards, for example, <code>cpuloadavg*</code> and <code>cpu.*</code>.
* [Point tags](http://docs.wavefront.com/metrics_managing.html#time-series-with-tags), which are optional key-value pairs associated with a metric. You must assign one or more existing point tag pairs, for example, <code>env="dev"</code>. If you assign multiple point tags, you must select the match criterion - either **Has tags** (individual point tags) or **Has all these tags** (a combination of point tags).
2. If you **Set a PPS limit** per billing period for the policy, you must also configure the alert settings.

    1. In the **Conditions** panel, select the comparison operator for the alert condition, specify the threshold for at least one severity, and click **Next**.
    2. In the **Recipients** panel,  specify who will receive the alert notifications and click **Next**.
    3. Enter the name of the alert, optionally add tags, and click **Next**.
3.	Enter the policy name and, optionally, a description and click **Create**.

**Read More**<br/>
[Examine Usage with Ingestion Policies](https://docs.wavefront.com/ingestion_policies.html)
