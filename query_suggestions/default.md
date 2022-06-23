```
[[queryFunctionName type=header text=default(]][<[[queryFunctionName type=body text=timeWindow]]>,] [<[[queryFunctionName type=body text=delayTime]]>,] <defaultValue>, <tsExpression> 
[.orElse<defaultIfNoData>][[queryFunctionName type=header text=)]]
```

**Tips to improve performance**

Use <[[queryFunctionName type=body text=timeWindow]]>to focus on the data you really need.
[[suggestionTip type=time_window name=default]]

Use <[[queryFunctionName type=body text=delayTime]]> to specify a gap before the inserted data in case of
[[suggestionTip type=delay_time name=default]]