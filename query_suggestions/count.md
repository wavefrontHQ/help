AGGREGATION FUNCTIONS: [[queryFunctionName type=header text=count()]]

`count(<tsExpression>[,metrics|sources|sourceTags|pointTags|<pointTagKey>])`

**Tips to improve performance**
- Consider using align() to align the metrics to the same time. Then aggregate the aligned metrics with an aggregation function, e.g. ‘count(align(1m, <[[queryFunctionName text=tsExpression]]>))’

- If you don’t need to interpolate the underlying data, use rawcount() instead of count()