**Tips to improve performance**
- Use filters to be as specific as possible in queries

    - Faster: `ts(user.metric, source="db-1" AND env="prod")`

    - Slower: `ts(user.metric AND NOT env="dev")`
- **Docs:**

  [Optimize Dashboard Performance](https://docs.wavefront.com/ui_dashboards.html#ensure-optimal-dashboard-performance)<br>
  [Wavefront Query Language Reference](https://docs.wavefront.com/query_language_reference.html#filtering-and-comparison-functions)