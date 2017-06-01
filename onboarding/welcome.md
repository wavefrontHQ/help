<div class="container-fluid">
<div class="row">
<p class="lead">Welcome to Wavefront. Let's get you started.</p>
<hr/>
</div>
<div>
<p>First, have a look at how Wavefront works. Wavefront consists of the Wavefront service and the Wavefront proxy.</p>

<img src="images/wavefront_architecture.png" alt="Wavefront architecture" style="display:block;width:350px;margin:10px auto;"></img>

<p>For most hosts, applications, and services, an agent collects metrics and pushes them to a Wavefront proxy running within your infrastructure. The proxy forwards collected metrics to the Wavefront service at the same time providing authentication, flow control, metrics preprocessing, and more.</p>

<p>Amazon Web Services metrics are pulled directly by the Wavefront service. Wavefront can get metrics from CloudWatch and CloudTrail and from AWS services such as EC2, SQS, and Redshift.</p>
</div>
</div>  
</div>