
Wavefront is a high performance streaming analytics platform designed for monitoring and optimization. The major components of Wavefront include the **Wavefront SaaS application**, which facilitates economies of scale for
deployment, flexibility, and time to value and the Wavefront proxy. The **Wavefront proxy** is the interface to
**collector agents**, which instrument hardware and software applications.

Wavefront makes it easy to stream your telemetry data into Wavefront. As shown in the diagram, Wavefront supports two approaches depending on where the metrics originate: push from agents and pull from cloud services.

![Wavefront architecture](images/wavefront_architecture.png)

From most systems a collector agent collects metrics data and pushes it to the Wavefront proxy. The proxy runs within your infrastructure and forwards collected data to the Wavefront service. The proxy provides authentication, [flow control](https://community.wavefront.com/docs/DOC-1034), [metrics preprocessing](https://community.wavefront.com/docs/DOC-1207), and more.

For data from cloud metrics services such as those offered by [Amazon Web Services (AWS)](https://aws.amazon.com), Wavefront directly pulls the metrics data. Cloud integrations currently support AWS CloudWatch, CloudTrail, and EC2 data.
For details, see [AWS Metrics Integration](https://community.wavefront.com/docs/DOC-1032).
