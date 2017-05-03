### Getting Data

Wavefront makes it easy to stream your data into Wavefront. Wavefront supports two approaches depending on where the metrics originate: push from agents and pull from cloud services.

![Wavefront architecture](images/wavefront_architecture.png)

An agent collects metrics and pushes it to the Wavefront proxy. The proxy runs within your infrastructure and forwards collected data to the Wavefront service. The proxy provides authentication, [flow control](https://community.wavefront.com/docs/DOC-1034), [metrics preprocessing](https://community.wavefront.com/docs/DOC-1207), and more.

Wavefront directly pulls metrics data from cloud services such as [Amazon Web Services (AWS)](https://aws.amazon.com). Wavefront offers CloudWatch, CloudTrail, and AWS Metrics+ [cloud integrations](https://community.wavefront.com/docs/DOC-1032).
