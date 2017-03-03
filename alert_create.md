## Creating Alerts

An alert is a condition and set of targets to be notified when the condition evaluates to true or false for a specified
period of time. You express conditions using [ts() queries](https://community.wavefront.com/docs/DOC-1019) and
operators.

You can send alert notifications to various types of targets: email addresses, pager services such as
[PagerDuty](https://community.wavefront.com/docs/DOC-1056) and
[VictorOps](https://community.wavefront.com/docs/DOC-1251), communication channels such as
[Slack](https://community.wavefront.com/docs/DOC-1183) and [HipChat](https://community.wavefront.com/docs/DOC-1055), and
you can also configure arbitrary actions such as invoking a [webhook](https://community.wavefront.com/docs/DOC-1054) or
running an auto-remediation script.
