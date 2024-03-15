### What Is an Event?

An event is a record that something of interest has occurred&mdash;an alert has changed state,
a maintenance window has been created, AWS instances have started or stopped, and so on.

Events originate from several different sources. When you perform actions in Tanzu Observability, such as when you edit or snooze an alert, the event source is **System**. When an alert fires or resolves, the source is **System/Alert**. You can manually add **User** events to identify user actions, such as code pushes, that occur outside Tanzu Observability but affect metrics within the system.

You can close (end) user events that are ongoing (whether they have no end time or a specific end time).

Events display as icons on the X-axis and as lines and regions of a chart. You specify which events display using [Basic events() Queries](https://docs.wavefront.com/events_queries.html) and control whether they display at the [chart](https://docs.wavefront.com/charts_events_displaying.html) or [dashboard](https://docs.wavefront.com/charts_events_displaying.html#control-event-overlays) level.
