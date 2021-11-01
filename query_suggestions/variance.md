AGGREGATION FUNCTIONS: [[queryFunctionName type=header text=variance()]]

```
[[queryFunctionName type=header text=variance(]]<tsExpression>
[,metrics|sources|sourceTags|pointTags|
<pointTagKey>][[queryFunctionName type=header text=)]]
```

**Tips to improve performance**
- Consider using [[queryFunctionName type=body text=align()]] to align the metrics to the same time. Then aggregate the aligned metrics with an aggregation function, e.g. ‘[[queryFunctionName type=header text=variance]]([[queryFunctionName type=body text=align]](1m, <[[queryFunctionName text=tsExpression]]>))’

- If you don’t need to interpolate the underlying data, use [[queryFunctionName type=header text=rawvariance()]] instead of [[queryFunctionName type=header text=variance()]]