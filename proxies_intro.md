## What is a Proxy?

In most cases before metrics can begin streaming to Wavefront from a host, application, or service you must add a
Wavefront proxy to your installation. The proxy allows you to send your data to Wavefront in a secure, fast,
and reliable manner.

A proxy sends data to Wavefront over HTTPs and handles authentication with your Wavefront instance through a simple
token. The proxy consolidates metrics into configurable batches (usually 1 second) and adding minimal latency.

The proxy works with the Wavefront server to ensure end-to-end flow control. When it detects network
connectivity issues, the proxy queues metrics in memory and to disk. Once connectivity is restored the proxy
replays queued metrics but prioritizes real-time traffic. A proxy generates its own usage metrics for easy
monitoring of the pipeline within Wavefront.

There are many ways to [configure](https://community.wavefront.com/docs/DOC-1034) the proxy to tune its behavior. The [proxy preprocessor](https://community.wavefront.com/docs/DOC-1207) allows you to correct errors in metric definition, reducing
the number of invalid metrics which would otherwise be rejected by the proxy.
