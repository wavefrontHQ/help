## What is an Alert?

Alerts focus operations on a system component that could potentially cause service degradation or outage. Alerts are triggered when a monitored metric reaches a value that indicates a problem in the component.

## Alert States

An alert can be in 5 states:
<ul><li><strong>FIRING</strong> - The alert is meeting the condition and timing properties.</li>
<li><strong>CHECKING</strong> - The alert is being checked to see if the condition and timing properties are being met.</li>
<li><strong>SNOOZED</strong> - The alert is not being checked to determine if the condition and timing properties are being met.</li>
<li><strong>IN MAINTENANCE</strong> - The alert has an alert tag or a source or set of sources included in a source tag associated
with an ongoing maintenance window. If an alert has a subset of reporting sources associated with in an ongoing maintenance window,
the state displays as CHECKING/IN MAINTENANCE.</li>
<li><strong>INVALID</strong> - A ts() query in the alert condition is timing out (> 5 min execution) or includes inactive metrics or sources.</li></ul>
