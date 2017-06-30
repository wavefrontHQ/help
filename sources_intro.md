### What is a Source?

A source is a unique application, host, container, or instance that emits metrics. The source is explicitly set
in the **source** field of a [Wavefront data format](https://docs.wavefront.com/wavefront_data_format.html) metric. For
AWS integrations, the source is extracted from [AWS service properties or dimensions](https://docs.wavefront.com/integrations_aws_metrics.html#wavefront-source-field).

Sources are automatically hidden after 4 weeks of inactivity, but you can also manually hide sources. While hidden sources are removed from autocomplete, they can still be used in a query when data values are present.

[Wavefront Query Language](https://docs.wavefront.com/query_language_getting_started.html) supports filtering by sources
and source tags.
