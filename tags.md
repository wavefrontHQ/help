A _tag_ is custom metadata that provides application-specific meaning to metrics and VMware Aria Operations for Applications entities, such as alerts,
dashboards, events, and sources. Tags group metrics and entities according to categories that you define.

The primary use of tags is to limit the number of metrics and entities that you are querying or working with at once. Limiting
the number of metrics reduces query time. Limiting the number of entities reduces information overload.

In queries, Operations for Applications supports filtering metrics with **source** and **point** tags and filtering events with **alert** and **event** tags.

In the UI and API, you can specify alert, dashboard, event, and source tags to filter those entities in their respective browsers and during API invocations. In the UI, tags display as gray labeled icons <span class="v-align wf-tag-component item label label-default"><span class="tag-container v-align"><i class="fa fa-tag"></i>MyService.MyApp</span></span> in the filter bar and below each entity in the entity browser.

**Watch Videos**<br/>
[Tagging Your Data](https://www.youtube.com/watch?v=9tt4orZHQts&index=3&list=PLmp0id7yKiEdaWcjNtGikcyqpNcPNbn_K)<br/>
[Organizing with Tags](https://vmwaretv.vmware.com/media/t/1_12xb5gcm/252649793)
