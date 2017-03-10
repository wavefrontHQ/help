### What is a Maintenance Window?

A maintenance window is a time window when preventative maintenance or testing may occur. Typically,
maintenance windows are used when disruptive operations could occur as a result of system maintenance and/or testing.
These disruptive operations create a high likelihood of causing alerts to fire. A maintenance window
allows you to identify when maintenance will occur and which subset of alerts and sources will be affected.

Maintenance windows whose start time is after the current time have the **PENDING** state.
Maintenance windows whose start time is before the current time and end time is after the current time have the **ONGOING** state.
Maintenance windows whose start and end times are before the current time have the **ENDED** state.

You can close (end) maintenance windows before they are due to end and you can extend the end time by various increments.
