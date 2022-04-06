### Getting Data

It is easy to stream your data into Tanzu Observability by Wavefront. We support two approaches depending on where the metrics originate: push from agents and pull from cloud services.

![Wavefront architecture](images/wavefront_architecture.png)

An agent collects metrics and pushes it to the Wavefront proxy. The proxy runs within your infrastructure and forwards collected data to the Wavefront service. The proxy provides authentication, [flow control](https://docs.wavefront.com/proxies_configuring.html), [metrics preprocessing](https://docs.wavefront.com/proxies_preprocessor_rules.html), and more.

Tanzu Observability directly pulls metrics data from cloud services such as [Amazon Web Services (AWS)](https://aws.amazon.com). Our Amazon Web Services [integration](https://docs.wavefront.com/integrations_aws_metrics.html) collects CloudWatch, CloudTrail, and AWS service data.
