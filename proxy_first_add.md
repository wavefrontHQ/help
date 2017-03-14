### Populate Your Data

Wavefront makes it easy to stream your telemetry data into Wavefront. As shown in the diagram, Wavefront supports two approaches depending on where the metrics originate: push from agents and pull from cloud services.

![Wavefront architecture](images/wavefront_architecture.png)

An agent collects metrics and pushes it to the Wavefront proxy. The proxy runs within your infrastructure and forwards collected data to the Wavefront service. The proxy provides authentication, [flow control](https://community.wavefront.com/docs/DOC-1034), [metrics preprocessing](https://community.wavefront.com/docs/DOC-1207), and more. Wavefront offers many options for 
[installing proxies](https://community.wavefront.com/docs/DOC-1271).

Wavefront directly pulls the metrics data from cloud metrics services such as those offered by [Amazon Web Services (AWS)](https://aws.amazon.com). [Cloud integrations](https://community.wavefront.com/docs/DOC-1032) currently support AWS CloudWatch, CloudTrail, and EC2.


