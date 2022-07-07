```
[[queryFunctionName type=header text=min(]]<tsExpression>[,metrics|
sources|sourceTags|pointTags|
<pointTagKey>][[queryFunctionName type=header text=)]]
```

**Tips to improve performance**

Consider using [[queryFunctionName type=body text=align()]] to align the metrics to the same time. Then aggregate the aligned metrics with an aggregation function, e.g. ‘[[queryFunctionName type=header text=min]]([[queryFunctionName type=body text=align]](1m, <[[queryFunctionName text=tsExpression]]>))’

```
Use **“align()”** function and set time window to

```
