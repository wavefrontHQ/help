### What Is a Derived Metric?

You can create a derived metric by setting up a query that includes the `aliasMetric` or `aliasSource` function, and saving that query.

Derived metrics are useful for certain use cases:
* Simplify the user experience by condensing the result of your query down to a single metric. All users can use that metric in other queries.
* Improve performance by pre-processing expensive queries. Other queries can use the result(s) instead of running the whole query.

By default, Tanzu Observability runs that query in the background approximately once a minute. You can use the (aliased) metric in other queries.
