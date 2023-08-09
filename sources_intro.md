### What Is a Source?

A source is a unique application, host, container, or instance that emits metrics. The source is explicitly set
in the **source** field of an [Operations for Applications data format](https://docs.wavefront.com/wavefront_data_format.html) metric. For AWS integrations, the source is extracted from the [AWS service properties or dimensions](https://docs.wavefront.com/integrations_aws_metrics.html#cloudwatch-sources-and-source-tags).

* Sources that emitted metrics during the last 2 days are in **Recent Metrics** status.
* Sources that didn't emit metrics during the last 2 days are in **Metrics Stopped** status.
* Sources that didn't emit metrics for a certain period (obsolescence period) are in **Obsolete** status. In the Metrics browser and Query Editor, obsolete sources are no longer shown in the autocomplete dropdown.

  **Note**: The obsolescence period for metrics and sources (by default 2 weeks) might vary. You can see your current configuration by looking into the Advanced settings of any [chart](https://docs.wavefront.com/ui_charts.html#include-metrics-that-stopped-reporting) or [dashboard](https://docs.wavefront.com/ui_dashboards.html#set-dashboard-display-preferences-and-settings). To change this configuration, contact [Technical Support](https://docs.wavefront.com/wavefront_support_feedback.html).

On this page, you can:
* Hide sources, including obsolete sources. In the Metrics Browser, the hidden sources are no longer shown in the autocomplete drop-down. In Query Editor, the hidden sources can still be used when data values are present.
* Include or exclude obsolete and hidden sources.
* Search and, optionally, save and share your search. 
* Filter sources by status, integrations, tag paths, tags, and saved searches.
* Create a maintenance window for the alerts with a particular source. Click the ellipsis for the target source and select **Add Maintenance Window**.

[Wavefront Query Language](https://docs.wavefront.com/query_language_getting_started.html) supports filtering by sources and source tags.
