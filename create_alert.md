
<table>
<tbody>
<tr><th>Property</th><th>Description</th></tr>
<tr>
<td>Events Display</td>
<td>Whether to display event icons for actual or hypothetical alert firings. **Actual Firings** displays event icons on the X-axis for times that the alert fired. **Backtesting** displays hypothetical event icons on the X-axis for times that the alert would have fired based on the Condition and **Alert fires** fields. If this is a new alert, Actual Firings is grayed out.</td>
</tr>
<tr>
<td>Name</td>
<td>The name of the alert. The name should be simple while still making it easy to identify its purpose.</td>
</tr>
<tr>
<td>Condition</td>
<td>A conditional ts() expression that defines the threshold for the alert. You can use any valid ts() language constructs in the expression. You can use free form query mode or the Query Builder to create the expression. The expression coupled with the **Alert fires** setting determines when the alert fires.<br/><br/>
**Alert fires**: The length of time during which the Condition expression must be true before the alert fires. The minimum number of minutes is 2.  If you enter 5 the alerting engine reviews the value of the Condition during the last 5 minute window to see if the alert should fire or not.<br/><br/>
**Alert resolves**: The length of time during which the Condition expression must be false before the alert switches to resolved. The minimum number of minutes is 2.  If you don't enable this field and specify a time, it defaults to the **Alert fires** setting.
</td>
</tr>
<tr>
<td>Display Expression</td>
<td>Optional. The query sent to targets when notified of alert state changes by email. You can use free form query mode or the Query Builder to create the expression. If not set, the query sent is the expression in the Condition field.</td>
</tr>
<tr>
<td>Severity</td>
<td>How important the alert is. The values in decreasing importance are:  SEVERE, WARN, SMOKE, and INFO.</td>
</tr>
<tr>
<td>Notifications</td>
<td>The targets to notify when the alert changes state. A combination of up to ten different email addresses, PagerDuty keys​, VictorOps keys, and Webhooks.</td>
</tr>
<tr>
<td>Additional Information</td>
<td>Any additional information pertinent to the alert. An example would be a link to a run book.</td>
</tr>
<tr>
<td>Tags</td>
<td>Assigned alert tags. You can enter existing alert tags or create new alert tags.</td>
</tr>
</tbody>
</table>
Optionally click the **Advanced** link to configure the properties:
<table>
<tbody>
<tr><th>Property</th><th>Description</th></tr>
<tr>
<td>
Checking Frequency
</td>
<td>The number of minutes between checking whether Condition is true. Minimum and default is 1.
</td>
</tr>
<tr>
<td>Resend Notifications</td>
<td>Whether to resend notification of a firing alert and the number of minutes to wait before resending the notification.</td>
</tr>
</tbody>
</table>

For more information, see:
- [Integrating Wavefront Alerts with HipChat Rooms](https://community.wavefront.com/docs/DOC-1055)
- [Integrating Wavefront Alerts with PagerDuty](https://community.wavefront.com/docs/DOC-1056)
- [Integrating Wavefront Alerts with Slack Channels](https://community.wavefront.com/docs/DOC-1183)
- [Integrating Wavefront Alerts with VictorOps](https://community.wavefront.com/docs/DOC-1251)
- [Integrating Wavefront Alerts with Webhooks](https://community.wavefront.com/docs/DOC-1054)
