### Creating a Derived Metric

When you create a derived metric, you specify the following information:

- **Name**: The name for the metric.
- **Query**: The query that you want to save. Operations for Applications will run the query periodically (once a minute by default) and reingest the metric into the system. Use a function like `aliasMetric()` or `aliasSource()` to make sure that you don't ingest a metric as itself. You can then use the new metric (the aliased metric) in other queries. The metric will be available right away because the query runs in the background.
- **Include results in the last *N* minutes** Ensures that you don't lose data. Increase this number on systems with connection problems.
- **Execute the query every *N* minutes** Defaults to 1. If you want to save results of the query less frequently, change this number. 1 minute is the lowest interval.
- **Tags** Allows you to find your metric easily.

After you've saved the query, Operations for Applications runs it at the specified interval, and you can use the resulting metric in other queries.

**Read More**<br/>
[Derived Metrics](https://docs.wavefront.com/derived_metrics.html)
