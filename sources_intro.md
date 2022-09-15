### What Is a Source?

A source is a unique application, host, container, or instance that emits metrics. The source is explicitly set
in the **source** field of a [Wavefront data format](https://docs.wavefront.com/wavefront_data_format.html) metric. For AWS integrations, the source is extracted from [AWS service properties or dimensions](https://docs.wavefront.com/integrations_aws_metrics.html#cloudwatch-sources-and-source-tags).

* Sources that emitted metrics during the last 2 days are in **Recent Metrics** status.
* Sources that didn't emit metrics during the last 2 days are in **Metrics Stopped** status.
* Sources that didn't emit metrics during the last 4 weeks are in **Obsolete** status. In the Metrics browser and Query Editor, obsolete sources are no longer shown in the autocomplete dropdown.

On this page, you can:
* **Hide** sources, including obsolete sources. In the Metrics browser, hidden sources are no longer shown in the autocomplete dropdown. In Query Editor, hidden sources can still be used when data values are present.
* Include or exclude obsolete and hidden sources.
* Search and, optionally, save and share your search by using the Search field above the sources table. 
* Filter sources by status, integrations, tag paths, tags, and saved searches.
* Create a maintenance window for the alerts with a particular source. Click the vertical ellipsis for the target source and select **Add Maintenance Window**.

[Wavefront Query Language](https://docs.wavefront.com/query_language_getting_started.html) supports filtering by sources and source tags.
