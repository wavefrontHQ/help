AGGREGATION FUNCTIONS: [[colorWrapper type=header text=avg()]]

`avg(<tsExpression>[,metrics|sources|sourceTags|pointTags|<pointTagKey>])`

**Tips to improve performance**
- Consider using align() to align the metrics to the same time. Then aggregate the aligned metrics with an aggregation function, e.g. ‘avg(align(1m, <[[colorWrapper text=tsExpression]]>))’
- If you don’t need to interpolate the underlying data, use rawavg() instead of avg()