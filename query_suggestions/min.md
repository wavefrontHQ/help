AGGREGATION FUNCTIONS: [[queryFunctionName type=header text=min()]]

`min(<tsExpression>[,metrics|sources|sourceTags|pointTags|<pointTagKey>])`

**Tips to improve performance**
- Consider using align() to align the metrics to the same time. Then aggregate the aligned metrics with an aggregation function, e.g. ‘min(align(1m, <[[queryFunctionName text=tsExpression]]>))’

- If you don’t need to interpolate the underlying data, use rawmin() instead of min()