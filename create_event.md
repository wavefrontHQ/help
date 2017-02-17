<table style="width: 100%;">
<tbody>
<tr><th>Property</th><th>Description</th></tr>
<tr>
<td>Name</td>
<td>The name displayed on the Events page and when you hover over an event icon on the X-axis of a chart.</td>
</tr>
<tr>
<td>Type</td>
<td>The type of the event, such as alert or code push. While there are no limitations to what you can enter into this field, try to limit it to type. You can enter additional information about the event in  the Details field.  You can enter the type as an event parameter in events() queries</a>.</td>
</tr>
<tr>
<td>Start Time</td>
<td>When the event starts. The options are Now or a specific day and time.</td>
</tr>
<tr>
<td>End Time</td>
<td>When the event ends. The options are:
<ul>
<li>Instantaneous - the event ends almost instantaneously with the start time. The exact interval is indeterminate. The Events page can report that the event starts and ends at exactly the same time or that it lasts a few seconds.</li>
<li>Ongoing - the event does not have a specific end time. </li>
<li>The event ends at the specific day and time.</li>
</ul>
</td>
</tr>
<tr>
<td>Classification</td>
<td>The event classification: Severe, Warn, Info, and Unclassified. You can enter the classification as an event parameter in events() queries.</td>
</tr>
<tr>
<td>Event Tags</td>
<td>Assigned event tags. You can enter existing event tags or create new event tags.</td>
</tr>
<tr>
<td>Details</td>
<td>Additional details about the event.</td>
</tr>
<tr>
<td>Display Event in Chart</td>
<td>Displays only when creating an event from a chart. Whether to add an events(name=&lt;name&gt;) query to the chart so that the event displays. Default: true.</td>
</tr>
</tbody>
</table>

{% include events_links.md %}
