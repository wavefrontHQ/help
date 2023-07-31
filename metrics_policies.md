### Managing Metrics Security Policy Rules
The metrics security policy allows you to control access to time series, histograms, and delta counters. The metrics security policy consists of rules that you create and organize in decreasing order of priority. A metrics security rule can allow or block specific metrics for specific accounts ([user accounts](https://docs.wavefront.com/csp_user_management.html) and [service accounts](https://docs.wavefront.com/csp_server_to_server_apps.html)) or [groups](https://docs.wavefront.com/csp_users_roles.html#manage-user-groups).

For an account with blocked access to a particular metric, the metric is hidden in charts, in alerts with enabled metrics security, and in autocomplete lists.

On this page, users with the **Metrics** permission, can:
* Create, edit, clone, and delete policy rules.
* Move policy rules up and down and set their priority.
* View and revert to a previous version of the policy.

To add a rule to the policy:
1. Click **Create a Rule**.
1. In the **Name** text box, enter a meaningful name for the rule.
2. Optionally, in the **Description** text box, enter a description for the rule.
3. Specify the target **Metrics Dimensions**.

    You must enter at least one **Prefix**, **Source**, or **Point Tag**. For multiple **Sources and Point Tags**, select the match criterion - can be either **or** (individual sources and point tags) or **and** (a combination of sources and point tags).
4. Specify the **Access** type - **allow** or **block**, and at least one target **Account** or **Group**. 
5. Click **OK**.
7. Click **Save**.

**Read More**<br/>
[Metrics Security Policy Rules](https://docs.wavefront.com/csp_metrics_security.html)
