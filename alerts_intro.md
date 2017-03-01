## What is an Alert?

Alerts focus operations on a system component that could potentially cause service degradation or outage. Alerts are triggered when a monitored metric reaches a value that indicates a problem in the component.

## Alert States

An alert can be in 5 states:
<dl><dt>FIRING</dt><dd>The alert is meeting the condition and timing properties.</dd>
<dt>CHECKING</dt><dd>The alert is being checked to see if the condition and timing properties are being met.</dd>
<dt>SNOOZED</dt><dd>The alert is not being checked to determine if the condition and timing properties are being met.</dd>
<dt>IN MAINTENANCE</dt><dd>The alert has an alert tag or a source or set of sources included in a source tag associated
with an ongoing maintenance window. If an alert has a subset of reporting sources associated with in an ongoing maintenance window, the state displays as CHECKING/IN MAINTENANCE. If an alert has a subset of reporting sources associated with an ongoing maintenance window but whose other sources are firing, the state displays as FIRING/IN MAINTENANCE.</dd>
<dt>INVALID</dt><dd>A ts() query in the alert condition is timing out (> 5 min execution) or includes inactive metrics or sources.</dd></dl>
