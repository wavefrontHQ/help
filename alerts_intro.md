## What is an Alert?

Alerts focus operations on a system component that could potentially cause service degradation or outage. Alerts are
triggered when a monitored metric reaches a value that indicates a problem in the component.

Active alerts can be in either the checking or firing states. Inactive alerts are either in maintenance,
invalid, or snoozed. An alert transitions to firing when a condition on a time series evaluates to at least
one true value and zero false values during a specified time window. An alert resolves and transitions back to checking
when there are either no true values present within the time window, or the time window contains no data.
