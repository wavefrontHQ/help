Standard aggregation functions like [[queryFunctionName type=header text=percentile()]] interpolate data in each time series. The aggregation function is applied to the interpolated series. Aggregating thousands of time series affects query performance.

**Doc & Video:**

[percentile Function](https://docs.wavefront.com/ts_percentile.html)<br>
[Be Smart About Aggregation](https://docs.wavefront.com/query_language_performance.html#be-smart-about-aggregation)<br>
[Video: Time Series and Interpolation](https://youtu.be/9LnDszVrJs4)