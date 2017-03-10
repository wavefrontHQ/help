### What is a Source?

A source is a unique application, host, container, or instance that emits metrics. The source is explicitly set
in the **source** field of a [Wavefront data format](https://community.wavefront.com/docs/DOC-1031) metric. For
cloud integrations, the source is extracted from [AWS service properties or dimensions](https://community.wavefront.com/docs/DOC-1032#jive_content_id_Wavefront_Source_Field).

The [Wavefront Query Language](https://community.wavefront.com/docs/DOC-1019) supports filtering for specific sources in queries.

As dynamic services become more prevalent, sources are constantly being started and shut down.
This can lead to sources being included even when they are no longer reporting data. Sources are automatically removed
after 4 weeks of inactivity, but you can also manually remove sources by moving them from an Active to Hidden state.
