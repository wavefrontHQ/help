One of the features that sets Wavefront apart from other monitoring solutions is the ability for you to interact
directly with charts. Rather than receiving a static image of you data, you can work with their charts in real time,
asking questions and receiving answers.

The simplest and most commonly used type of chart is of an individual metric. For example, you might want to show CPU
load across all sources.  The expression is ts(metric.name, [sourceFilter]).  The sourceFilter parameter is optional,
and is used when you only want to see a select set of sources.  For example you can enter the expression ts("cpu.idle")
into a query field to produce a chart of cpu idle time.

With this metric would typically display many lines, which can be difficult to read when changes occur.  In these cases
it may make sense to use one of the ts() aggregation functions.  You could choose to show the average value of all the
cpu.idle metrics across all sources using the avg() function.  Or, you could use sum() to get a total of all of the
sources together for this metric. Aggregate functions are the second most commonly used query after the simple
ts(metric.name, [sourceFilter]) query type.

The cpu.idle metric typically increases over time because it represents a counter metric, or a metric that continuously
increases over time. While counter metrics provide a snapshot of the current count, it does not provide information such
as the rate of change. For this there is a rate() function that transforms a counter to show you the rate of change per
second:  sum(rate(ts("cpu.idle")).
