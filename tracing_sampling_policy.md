### What is a Sampling Policy? 

Wavefront [intelligent sampling](http://docs-sandbox-b.wavefront.com/trace_data_sampling.html) significantly reduces the volume of ingested traces and is enabled by default. The goal of intelligent sampling is to retain traces that are likely to be informative. But sometimes intelligent sampling discards traces that you want to keep. 

If intelligent sampling discards traces that you want to keep, you can create a sampling policy to keep the traces you specify. With sampling policies, you retain more data than the default intelligent sampling. That requires more storage and affects your cost. 

### More Info

[Manage Sampling Policies](https://docs.wavefront.com/trace_sampling_policies.html)

[Trace Sampling Overview](https://docs.wavefront.com/trace_data_sampling.html#how-it-works)
