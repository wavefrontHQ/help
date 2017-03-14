### What is a Source?

A source is a unique application, host, container, or instance that emits metrics. The source is explicitly set
in the **source** field of a [Wavefront data format](https://community.wavefront.com/docs/DOC-1031) metric. For
cloud integrations, the source is extracted from [AWS service properties or dimensions](https://community.wavefront.com/docs/DOC-1032#jive_content_id_Wavefront_Source_Field).

Sources are automatically removed after 4 weeks of
inactivity, but you can also manually hide sources. While hidden sources are removed from autocomplete, they can still be used in a query when data values are present.

The [Wavefront Query Language](https://community.wavefront.com/docs/DOC-1019) supports filtering for sources
and source tags.
