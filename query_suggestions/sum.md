AGGREGATION FUNCTIONS: [[suggestionColor type=header text=sum()]]

`sum(<tsExpression>[,metrics|sources|sourceTags|pointTags|<pointTagKey>])`

**Tips to improve performance**
- Consider using align() to align the metrics to the same time. Then aggregate the aligned metrics with an aggregation function, e.g. ‘sum(align(1m, <[[suggestionColor text=tsExpression]]>))’.
- If you don’t need to interpolate the underlying data, use rawsum() instead of sum()