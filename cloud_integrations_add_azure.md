### Add a Microsoft Azure Cloud Integration

Adding a Microsoft Azure cloud integration requires establishing a trust relationship between Azure and VMware Aria Operations for Applications (formerly known as Tanzu Observability by Wavefront). The overall process involves the following:

* Getting a Directory ID
* Creating an Azure Active Directory application that represents Operations for Applications inside Azure and getting the Application ID.
* Creating a secret key and getting the Application secret.

To register a Microsoft Azure Cloud Integration:

1. In the **Name** text box, enter a meaningful name.
2. In the **Directory ID** text box, enter your Microsoft Azure Directory ID.
3. In the **Application ID** text box, enter the Azure Active Directory Application (client) ID.
4. In the **Application Secret** text box, enter the secret key that you created. 
   **Note**: The Azure application secret that you enter is securely stored and never exposed except for read only access to the Azure APIs.
5. (Optional) Enter the category names to fetch.
6. (Optional) In the **Metric Allow List** text box, you can add metrics to an allow list by entering a regular expression. 
   For example, <code>^azure.(compute|dbforpostgresql).*$</code>.

   <strong>Note:</strong> Metric names consist of the actual metric name and a suffix (starting with a dot (".")). The suffix represents an aggregation type. In the regular expression, you must use the actual metric names without the aggregation types, such as: <code>count</code>, <code>average</code>, <code>minimum</code>, <code>maximum</code>, <code>sum</code>, and so on.

   For example, the metric names for the metric <code>azure.compute.vm.percentage.cpu</code> are:

   * <code>azure.compute.vm.percentage.cpu.average</code>
   * <code>azure.compute.vm.percentage.cpu.maximum</code>
   * <code>azure.compute.vm.percentage.cpu.minimum</code>
   * <code>azure.compute.vm.percentage.cpu.count</code>
   * <code>azure.compute.vm.percentage.cpu</code> (corresponds to <code>azure.compute.vm.percentage.cpu.total</code>)

   Here, the actual metric name is <code>azure.compute.vm.percentage.cpu</code>, while <code>average</code>, <code>maximum</code>, <code>minimum</code>, and <code>count</code> are the aggregation types. When you create the regular expression, you must use only <code>azure.compute.vm.percentage.cpu</code>. For example, <code>^azure.compute.vm.percentage.cpu$</code>.

7. (Optional) Enter the resource group names to fetch.
8. Select whether you want to fetch logs. 
   If you decide that you want to fetch activity logs, you can also specify the log categories to fetch, e.g. Administrative, Service health, Alert, and so on.
9. Click **Register**.
