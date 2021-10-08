**Tips to improve performance**
- Use filters to be as specific as possible in queries

    - Faster: `ts(user.metric, source="db-1" and env="prod")`

    - Slower: `ts(user.metric and not env="dev")`
- **Docs:**

  [How to dashboard performance](http://docs-sandbox-a.wavefront.com/ui_dashboards.html#ensure-optimal-dashboard-performance)<br>
  [Wavefront Query Language Reference](https://docs.wavefront.com/query_language_reference.html#partial-regex-wildcards-aliases-and-variables)