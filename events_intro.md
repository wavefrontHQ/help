### What is an Event?

An event is a record that something of interest has occurred – an alert has changed state,
a maintenance window has been created, AWS instances have started or stopped, and so on.

Events originate from several different sources. Some events are generated when you perform actions in Wavefront.
When you edit or snooze an alert, the event source is **System**. When an alert fires or resolves, the source
is **System/Alert**.

You can manually add **User** events to identify user actions, such as code pushes, that occur outside Wavefront but that affect metrics within Wavefront.

You can close (end) user events that are ongoing (whether they have no end time or a specific end time).
