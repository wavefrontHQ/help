### What is an Event?

An event is a record that something of interest has occurred&mdash;an alert has changed state,
a maintenance window has been created, AWS instances have started or stopped, and so on.

Events originate from several different sources. When you perform actions in Wavefront, such as when you edit or snooze an alert, the event source is **System**. When an alert fires or resolves, the source is **System/Alert**. You can manually add **User** events to identify user actions, such as code pushes, that occur outside Wavefront but that affect metrics within Wavefront.

You can close (end) user events that are ongoing (whether they have no end time or a specific end time).

Events display as icons on the X-axis and as lines and regions of a chart. You control which events display using [events() expressions](https://community.wavefront.com/docs/DOC-1157) and can control whether they display at the [chart](https://community.wavefront.com/docs/DOC-1158#jive_content_id_Display_Source_Events) or [dashboard](https://community.wavefront.com/docs/DOC-1063) level. 
