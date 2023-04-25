### Populate Your Data

Operations for Applications makes it easy to stream your own metrics into the system. We support two approaches depending on where the metrics originate: push from agents and pull from cloud services.

An agent collects metrics and pushes them to the Wavefront proxy. The proxy runs within your infrastructure and forwards collected data to Operations for Applications. The proxy provides authentication, [flow control](https://docs.wavefront.com/proxies_configuring.html), [metrics preprocessing](https://docs.wavefront.com/proxies_preprocessor_rules.html), and more.

Operations for Applications directly pulls metrics data from cloud services such as [Amazon Web Services (AWS)](https://aws.amazon.com). Our Amazon Web Services [integration](https://docs.wavefront.com/integrations_aws_metrics.html) collects CloudWatch, CloudTrail, and AWS service data.
