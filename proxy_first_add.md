
Wavefront is a high performance streaming analytics platform designed for monitoring and optimization. The major components of Wavefront include the **Wavefront SaaS application**, which facilitates economies of scale for
deployment, flexibility, and time to value and the Wavefront proxy. The **Wavefront proxy** is the interface to
**collector agents**, which instrument hardware and software applications.

Wavefront makes it easy to stream your telemetry data into Wavefront. It supports two main approaches depending on where
the metrics originate.

From most systems a collector agent collects metrics data and pushes it to the Wavefront proxy. The proxy runs within your infrastructure and forwards collected data to the Wavefront service. The proxy provides authentication, flow control, metrics preprocessing, and more.

For data from cloud metrics services such as those offered by [Amazon Web Services (AWS)](https://aws.amazon.com), Wavefront directly pulls the metrics data. Cloud integrations currently support AWS CloudWatch, CloudTrail, and EC2 data.
For details, see [AWS Metrics Integration](https://community.wavefront.com/docs/DOC-1032).

This diagram summarizes the options:

![Wavefront architecture](images/wavefront_architecture.png)
