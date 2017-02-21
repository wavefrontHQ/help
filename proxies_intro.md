## What is a Proxy? 

In most cases before metrics can begin streaming to Wavefront from a host, application, or service you must add a
Wavefront proxy to your installation. The Wavefront proxy allows you to send your data to Wavefront in a secure, fast,
and reliable manner.

The proxy is a Java program that sends data to Wavefront over HTTPs and handles authentication with your Wavefront
instance through a simple token. The proxy handles hundreds to thousands of simultaneous clients. It   consolidates
points into configurable batches (usually 1 second), adding minimal latency (0.5 second, on average, due to the 1 second
batches).

The proxy works with Wavefront application response codes to ensure end-to-end flow control (due to rate limits or other
capacity/performance thresholds). To address network connectivity issues, it queues point internally in memory and to
disk. Once connectivity is restored it replays queued points but prioritizes real-time traffic. The proxy generates
metrics on the proxy's point rate and memory usage for easy monitoring of the pipeline within the Wavefront application.
