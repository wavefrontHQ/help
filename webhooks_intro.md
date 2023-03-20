### What Is an Alert Target?

An alert target can be one of the following: 

* Email alert target - sends an email when the alert is triggered.
* PagerDuty alert target - sends a PagerDuty message when the alert is triggered.
* Webhook alert target - specifies an HTTP POST request to send to a user-defined URL when the alert is triggered.


For each kind of alert target, you can include data either as simple POST keys and values or in some other format such as JSON.

You can use an alert target to integrate actions with alerts:

1. Create an alert target.
1. Add the alert target name to the <strong>Recipients</strong> field of one or more alerts.
