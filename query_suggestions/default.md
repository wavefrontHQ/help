MISSING DATA FUNCTIONS: [[queryFunctionName type=header text=default()]]

`default([<[[queryFunctionName type=body text=timeWindow]]>,] [<[[queryFunctionName type=body text=delayTime]]>,] <defaultValue>, <tsExpression> [.orElse<defaultIfNoData>])`

**Tips to improve performance**
- Use <[[queryFunctionName type=body text=timeWindow]]>to focus on the data you really need.

- Use <[[queryFunctionName type=body text=timeWindow]]> to specify a gap before the inserted data in case of

