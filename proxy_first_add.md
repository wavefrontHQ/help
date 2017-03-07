
Wavefront is a high performance streaming analytics platform designed for monitoring and optimization.  The service is
unique in its ability to scale to very high data ingestion rates and query loads. The result is a technology stack
that scales horizontally while providing access to all of the granular data collected for all time.

The major components of Wavefront include the **Wavefront SaaS application**, which facilitates economies of scale for
deployment, flexibility, and time to value and the Wavefront proxy. The **Wavefront proxy** is the interface to
**collector agents**, which instrument hardware and software applications.

Wavefront makes it easy to stream your telemetry data into Wavefront. It supports two main approaches depending on where
the metrics originate.

From most systems you use a collector agent that pushes data to Wavefront. Wavefront requires an intermediary, called a
proxy, between agents and the Wavefront service. The proxy runs within your infrastructure and forwards collected data
to the Wavefront service. The proxy provides authentication, flow control, metrics preprocessing, and more.

For data from cloud metrics services such as those offered by [Amazon Web Services (AWS)](https://aws.amazon.com), Wavefront directly pulls the metrics data. Cloud integrations currently support AWS CloudWatch, CloudTrail, and EC2 data.
For details, see [AWS Metrics Integration](https://community.wavefront.com/docs/DOC-1032).

This diagram summarizes the options:

![Wavefront architecture](images/wavefront_architecture.png)
