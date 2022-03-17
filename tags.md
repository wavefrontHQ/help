A _tag_ is custom metadata that provides application-specific meaning to metrics and Tanzu Observability by Wavefront entities such as alerts,
dashboards, events, and sources. Tags group metrics and entities according to categories that you define.

The primary use of tags is to limit the number of metrics and entities that you are querying or working with at once. Limiting
the number of metrics reduces query time. Limiting the number of entities reduces information overload.

In queries, Tanzu Observability supports filtering metrics with **source** and **point** tags and filtering events with **alert** and **event** tags.

In the UI and Wavefront API you can specify alert, dashboard, event, and source tags to filter those entities in their
respective browsers and during API invocations. In the Tanzu Observability by Wavefront UI, tags display as gray labeled icons <span class="v-align wf-tag-component item label label-default"><span class="tag-container v-align"><i class="fa fa-tag"></i>MyService.MyApp</span></span> in the filter bar and below each entity in the entity browser.

**Watch Videos**<br/>
[Tagging Your Data with Wavefront](https://www.youtube.com/watch?v=9tt4orZHQts&index=3&list=PLmp0id7yKiEdaWcjNtGikcyqpNcPNbn_K)
[Organizing with Tags](https://bcove.video/3APZACf)
