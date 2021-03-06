### What is a Proxy?

Proxies allow you to send your data to Wavefront in a secure, fast, and reliable manner. A proxy generates its own [internal metrics](https://docs.wavefront.com/wavefront_monitoring.html) for easy monitoring of the pipeline within Wavefront.

The proxy works with the Wavefront server to ensure end-to-end flow control. When it detects network
connectivity issues, the proxy queues metrics in memory and to disk. Once connectivity is restored the proxy
replays queued metrics but prioritizes real-time traffic. There are many ways to [configure](https://docs.wavefront.com/proxies_configuring.html) the proxy to tune this behavior.

The [proxy preprocessor](https://docs.wavefront.com/proxies_preprocessor_rules.html) allows you to correct errors in metric definition, reducing the number of invalid metrics which would otherwise be rejected by the proxy.
