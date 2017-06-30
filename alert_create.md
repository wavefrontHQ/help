### Creating Alerts

An alert is a condition and set of targets to be notified when the condition evaluates to true or false for a specified
period of time. You express conditions using [ts() queries](https://docs.wavefront.com/query_language_getting_started.html) and
operators.

You can send alert notifications to various types of targets: email addresses, pager services such as
PagerDuty and VictorOps, communication channels such as Slack and HipChat, and
you can also configure arbitrary actions such as invoking a [webhook](https://docs.wavefront.com/webhooks_managing.html) or
running an auto-remediation script.
