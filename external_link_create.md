### Creating External Links

You filter which time series can link externally by specifying metric name, source name, and point tag value filters as
regular expressions that the series must match.

An external link consists of a [templated URL](https://docs.wavefront.com/external_links_managing.html) that contains information
about metric names, source names, point tag values, and time window of the originating series.

The template uses [Mustache syntax](https://mustache.github.io/). It supports several properties derived from the series
and supports functions to transform sections in the template.
