### Creating a Derived Metric

When you create a derived metric, you specify the following information:

- **Name** Name that Wavefront uses to save your metric.
- **Query** A query that you want to save. Wavefront will run the query periodically (once a minute by default) and reingest the metric into the system. Use a function like `aliasMetric` or `aliasSource()` to make sure that you don't ingest a metric as itself. You can then use the new metric (the aliased metric) in other queries. The metric will be availabe right away because the query runs in the background.
- **Include results in the last *N* minutes** Ensures that you don't lose data. Increase this number on systems with connection problems.
- **Execute the query every *N* minutes** Defaults to 1. If you want to save results of the query less frequently, change this number. 1 minute is the lowest interval.
- **Tags** Allows you to find your metric easily.
- **Advanced** Select the **Include Obsolete Metrics** check box to include metrics that are older than 4 weeks each time we run the query. Selecting this option can become expensive, that's why it's not selected by default. 

After you've saved the query, we run it at the specified interval, and you can use the resulting metric in other queries.

{% include derived_metrics_links.md %}
