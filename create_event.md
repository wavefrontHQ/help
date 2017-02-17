<dl>
<dt>Name</dt>
<dd>The name displayed on the Events page and when you hover over an event icon on the X-axis of a chart.</dd>
<dt>Type</dt>
<dd>The type of the event, such as alert or code push. While there are no limitations to what you can enter into this field, try to limit it to type. You can enter additional information about the event in  the Details field.  You can enter the type as an event parameter in events() queries</a>.</dd>
<dt>Start Time</dt>
<dd>When the event starts. The options are Now or a specific day and time.</dd>
<dt>End Time</dt>
<dd>When the event ends. The options are:
<ul>
<li>Instantaneous - the event ends almost instantaneously with the start time. The exact interval is indeterminate. The Events page can report that the event starts and ends at exactly the same time or that it lasts a few seconds.</li>
<li>Ongoing - the event does not have a specific end time. </li>
<li>The event ends at the specific day and time.</li>
</ul>
</dd>
<dt>Classification</dt>
<dd>The event classification: Severe, Warn, Info, and Unclassified. You can enter the classification as an event parameter in events() queries.</dd>
<dt>Event Tags</dt>
<dd>Assigned event tags. You can enter existing event tags or create new event tags.</dd>
<dt>Details</dt>
<dd>Additional details about the event.</dd>
<dt>Display Event in Chart</dt>
<dd>Displays only when creating an event from a chart. Whether to add an events(name=&lt;name&gt;) query to the chart so that the event displays. Default: true.</dd>
</dl>

{% include events_links.md %}
