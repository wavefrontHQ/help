Query with NOT

**Tips to improve performance**
- Use filters to be as specific as possible in queries

  - Faster: `ts(user.metric, source="db-1" AND env="prod")`

  - Slower: `ts(user.metric AND NOT env="dev")`

**Doc & Video:**

[Use Filters to Look at the Right Data](https://docs.wavefront.com/query_language_performance.html#use-filters-to-look-at-the-right-data)<br>
[Video: Query Language Basics](https://bcove.video/3FqMmPo)