percentile() returns the estimated percentile for `percentage`, across the time series described by tsExpression.

Standard aggregation functions like percentile() interpolate data in each time series. The aggregation function itself is applied to the interpolated series.

If you are aggregating thousands of time series, query performance might be affected.

**Doc & Video**

[Time Series and Interpolation](https://www.youtube.com/watch?v=9LnDszVrJs4)<br>
[Optimize Dashboard Performance](https://docs.wavefront.com/ui_dashboards.html#ensure-optimal-dashboard-performance)
