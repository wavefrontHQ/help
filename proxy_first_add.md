### Adding a Proxy

Wavefront makes it easy to stream your telemetry data into Wavefront. As shown in the diagram, Wavefront supports two approaches depending on where the metrics originate: push from agents and pull from cloud services.

![Wavefront architecture](images/wavefront_architecture.png)

From most systems an agent collects metrics and pushes it to the Wavefront proxy. The proxy runs within your infrastructure and forwards collected data to the Wavefront service. The proxy provides authentication, [flow control](https://community.wavefront.com/docs/DOC-1034), [metrics preprocessing](https://community.wavefront.com/docs/DOC-1207), and more. The Add Now <i class="arrow-right"/></i> link gives you a script that installs the proxy on your monitored system and optionally a script for installing  Telegraf collector agent.

For data from cloud metrics services such as those offered by [Amazon Web Services (AWS)](https://aws.amazon.com), Wavefront directly pulls the metrics data. [Cloud integrations](https://community.wavefront.com/docs/DOC-1032) currently support AWS CloudWatch, CloudTrail, and EC2 data.
