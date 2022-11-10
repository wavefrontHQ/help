### What Is a Sampling Policy? 

Tanzu Observability by Wavefront performs [intelligent sampling](http://docs.wavefront.com/trace_data_sampling.html) to retain only traces that are likely to be informative, such as traces with errors or traces that take a long time to complete.

If you want more control over the traces retained in Tanzu Observability, you can create a sampling policy to keep the spans you specify. You can then edit, delete, restore, deactivate, and explore the version history of the policy you created. 

With sampling policies, you retain more data than default intelligent sampling. That requires more storage and affects your cost.

**Read More**<br/>
[Trace Sampling Overview](https://docs.wavefront.com/trace_data_sampling.html#how-it-works)<br/>
[Manage Sampling Policies](https://docs.wavefront.com/trace_sampling_policies.html)
