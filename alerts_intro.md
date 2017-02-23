## What is an Alert?

An alert is a logical expression (condition) and set of actions that are performed when the condition evaluates to true
or false for a specified period of time. The condition is formulated using ts() queries and operators.

You configure an alert to send notifications to targets when the alert changes state. For example, notifications are
sent when an alert changes state from FIRING to not FIRING (RESOLVED), and when an alert is snoozed. In addition to being
able to send notifications to targets such as email, PagerDuty, and VictorOps, you can also configure arbitrary
actions such as invoking a webhook and running an auto-remediation script.
