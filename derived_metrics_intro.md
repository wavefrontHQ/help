### What is a Derived Metric?

You can create a derived metric by setting up a query that includes an `aliasMetric` or `aliasSource`, and saving that query from the `Derived Metrics` page.

Wavefront runs that query in the background, by default approximately once a minute and you can use the (alias) metric in other queries.

Derived metrics is useful for certain use cases:
* Simplify the user experience by condensing the result of your query down to a single metric. All users can use that metric in other queries.
* Improve performance by pre-processing expensive queries. Other queries can use the result(s) instead of running the whole query.
