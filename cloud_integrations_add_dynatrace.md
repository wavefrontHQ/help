### Add a Dynatrace Integration

The Dynatrace integration is an AI-powered, full-stack, automated performance management solution. This integration collects the metrics from a Dynatrace SaaS environment and sends them to Wavefront.

To set up the Dynatrace integration, you must provide an API token. Click the **How to get the API Token** in the Wavefront UI and follow the instructions. After you copy the generated API token, follow these steps:

1. In the **Name** text box, enter a meaningful name.
2. In the **Base URL** text box, provide your Dynatrace server API endpoint URL.
3. In the **API Token** text box, paste the API token that you copied.
4. (Optional) In the **Metric Allow List** field, add metrics to an allow list by entering a regular expression. For example:
   * To fetch only load action duration metrics, enter: <code>^dynatrace.builtin.synthetic.browser.actionDuration.load.*$</code>
   * To fetch only successful executions count metrics, enter: <code>^dynatrace.builtin.synthetic.browser.success.*$</code>
   * To fetch only server contribution metrics, enter <code>^dynatrace.builtin.synthetic.browser.serverContribution.*$</code>
5. (Optional) Change the **Service Refresh Rate**. The default is 5 minutes.
6. Click **Register**.
