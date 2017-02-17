An alert is a logical expression (condition) and set of actions that are performed when the condition evaluates to true
or false for a specified period of time. The condition is formulated using ts() queries and operators.

An alert can be in 5 states:
<dl>
<dt>FIRING</dt><dd>The alert is meeting the condition and timing properties.</dd>
<dt>CHECKING</dt><dd>The alert is being checked to see if the condition and timing properties are being met.</dd>
<dt>SNOOZED</dt><dd>The alert is not being checked to determine if the condition and timing properties are being met.</dd>
<dt>IN MAINTENANCE</dt><dd>The alert has an alert tag or a source or set of sources included in a source tag associated
with an ongoing maintenance window. If an alert has a subset of reporting sources associated with in an ongoing maintenance window,
the state displays as CHECKING/IN MAINTENANCE.</dd>
<dt>INVALID</dt><dd>A ts() query in the alert condition is timing out (> 5 min execution) or includes inactive metrics or sources.</dd>
 </dl>

You configure an alert to send notifications to targets when the alert changes state. For example, notifications are
sent when an alert changes state from FIRING to not FIRING (RESOLVED), and when an alert is snoozed. In addition to being
able to send notifications to targets such as email, PagerDuty, and VictorOps, you can also configure arbitrary
actions such as invoking a webhook and running an auto-remediation script.
