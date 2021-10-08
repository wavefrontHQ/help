AGGREGATION FUNCTIONS: [[colorWrapper type=header text=variance()]]

`variance(<tsExpression>[,metrics|sources|sourceTags|pointTags|<pointTagKey>])`

**Tips to improve performance**
- Consider using align() to align the metrics to the same time. Then aggregate the aligned metrics with an aggregation function, e.g. ‘variance(align(1m, <[[colorWrapper text=tsExpression]]>))’
- If you don’t need to interpolate the underlying data, use rawvariance() instead of variance()