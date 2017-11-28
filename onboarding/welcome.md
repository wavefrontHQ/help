<div class="container-fluid">
<div class="row">
<p class="lead">Let's get started with Wavefront!</p>
</div>
<div>
<p>First, have a look at how Wavefront works. Wavefront consists of the Wavefront cloud service and the Wavefront proxy.</p>

<img src="images/wavefront_architecture.svg" alt="Integrations Architecture" style="display:block;width:60%;max-width:1000px"></img>

<p>For most hosts, applications, and services, an agent collects metrics and pushes them to a Wavefront proxy running within your infrastructure. The proxy forwards collected metrics to the Wavefront cloud service while providing authentication, buffering, metrics pre-processing, and more.</p>

<p>Amazon Web Services metrics are pulled directly by the Wavefront cloud service. Wavefront can get metrics from CloudWatch and CloudTrail and from AWS services such as EC2, SQS, and Redshift.</p>
</div>
</div>  
</div>
