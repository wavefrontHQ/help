## Creating a Maintenance Window

You create a maintenance window in the Alerts and Maintenance Windows browsers by clicking the **Create Maintenance Window** button at the top of the filter bar.

## Maintenance Window Properties

<dl>
<dt>Name</dt>
<dd>The name of the maintenance window.</dd>
<dt>Description</dt>
<dd>Additional information about the maintenance window. Information entered into this field appears directly below the maintenance window in the Maintenance Windows browser.</dd>
<dt>Start Time</dt>
<dd>The start time of the maintenance window:
<dl><dt>Now</dt><dd>The maintenance window starts immediately.</dd>
<dd><i class="fa fa-calendar"></i></dt><dd>The maintenance window starts on the specified date and time. Click the text field and choose a date and time or type a date and time in the format MM/DD/YYYY HH:MM [AM|PM].</dd></dl>
<dt>End Time</dt><dd><i class="fa fa-calendar"></i> The end time of the maintenance window. The end time must be after the start time. Click the text field and choose a date and time or type a date and time in the format MM/DD/YYYY HH:MM [AM|PM].</dd>
<dt>Affected Alerts and Sources</dt>
<dd>The alerts and sources to suppress during the maintenance window. All alerts that have tags in the <strong>Alert Tags</strong> field are suppressed. An alert is suppressed if at least one of sources identified by the <strong>Source Tags</strong> and <strong>Sources</strong> fields causes the alert condition to be met. You must configure at least one alert tag, source, or source tag.</dd>
</dl>
