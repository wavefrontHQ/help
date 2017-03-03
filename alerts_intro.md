## What is an Alert?

Alerts focus operations on a system component that could potentially cause service degradation or outage. Alerts are
triggered when a monitored metric reaches a value that indicates a problem in the component. Operators responsible for
fixing the problem are notified when the alert triggers.

Active alerts can be in either the checking or firing states. Inactive alerts are either in maintenance, snoozed, or
invalid. An alert transitions to firing when a condition on a time series evaluates to at least
one true value and no false values during a fixed time window. An alert resolves (transitions back to checking)
when there are either no true values present within the time window, or the time window contains no data.

To disable alert checking for a set of sources during a specific time window you can put them in maintenance.
Alternatively you can disable alert checking for a fixed time window by snoozing the alert.
