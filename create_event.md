## Creating an Event

You create a user event by:
<ul>
<li><strong>Events browser</strong> - Clicking the <strong>Create Event</strong> button located at the top of the filter bar.</span></li>
<li><strong>Chart</strong> - Clicking the flag icon <i class="fa fa-flag"></i> located on the far right side of the time
bar. Hover over the chart and set your cursor at a point in time. To make the event instantaneous, click that point.
If the start and end time for the desired event are included in the current time window, click, hold, and drag across the window.</li>
</ul>

## Event Properties

<dl>
<dt>Name</dt>
<dd>The name displayed on the Events page and when you hover over an event icon on the X-axis of a chart.</dd>
<dt>Type</dt>
<dd>The type of the event, such as code push. While there are no limitations to what you can enter into this field, try to limit it to type. You can enter additional information about the event in the Details field.  You can enter the type as an event parameter in events() queries</a>.</dd>
<dt>Start Time</dt>
<dd>The start time of the event:
<dl><dt>Now</dt><dd>The maintenance window starts immediately.</dd>
<dt><i class="fa fa-calendar"></i></dt><dd>The maintenance window starts on the specified date and time.Click the text field and choose a date and time or type a date and time in the format MM/DD/YYYY HH:MM [AM|PM].</dd></dl></dd>
<dt>End Time</dt>
<dd>The end time of the event:
<dl>
<dt>Instantaneous</dt><dd>End the event instantaneously with the start time. The exact interval is indeterminate.
The Events page can report that the event starts and ends at exactly the same time or that it lasts a few seconds.</dd>
<dt>Ongoing</dt><dd>The event does not have a specified end time. You can manually end (close) the event from the Events page.</dd>
<dt><i class="fa fa-calendar"></i></dt><dd>End the event at the specified day and time. Click the text field and choose a date and time or type a date and time in the format MM/DD/YYYY HH:MM [AM|PM].</dd></dl>
<dt>Classification</dt>
<dd>The event classification: SEVERE, WARN, INFO, and UNCLASSIFIED. You can enter the classification as an event parameter in events() queries.</dd>
<dt>Tags</dt>
<dd>Tags to associate with the event. You can start typing the names of existing event tags and matching tags display or create new event tags.</dd>
<dt>Details</dt>
<dd>Additional details about the event.</dd>
<dt>Display Event in Chart</dt>
<dd>Displays only when creating an event from a *chart*. Whether to add an events(name=&lt;name&gt;) query to the chart so that the event displays.</dd>
</dl>
