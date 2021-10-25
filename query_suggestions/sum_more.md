[[queryFunctionName type=header text=sum()]] returns the sum of the time series described by tsExpression.

Standard aggregation functions like [[queryFunctionName type=header text=sum()]] interpolate data in each time series. The aggregation function itself is applied to the interpolated series.

If you are aggregating thousands of time series, query performance might be affected.

**Doc & Video:**

[Be Smart About Aggregation](https://docs.wavefront.com/query_language_performance.html#be-smart-about-aggregation)<br>
[Aggregating Time Series](https://docs-sandbox-a.wavefront.com/query_language_aggregate_functions.html)<br>
[Video: Time Series and Interpolation](https://youtu.be/9LnDszVrJs4)