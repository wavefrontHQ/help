MISSING DATA FUNCTIONS: [[colorWrapper type=header text=default()]]

`default([<[[colorWrapper type=body text=timeWindow]]>,] [<[[colorWrapper type=body text=delayTime]]>,] <defaultValue>, <tsExpression> [.orElse<defaultIfNoData>])`

**Tips to improve performance**
- Use <[[colorWrapper type=body text=timeWindow]]> to fill in data specific to a desired smaller time window. Omitting this will fill in gaps of missing data for upto 4 weeks.

- Specify <[[colorWrapper type=body text=delayTime]]> to allow a gap before the inserted data. Omitting this will lead to data points being inserted at the beginning of each gap.
