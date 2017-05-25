<div class="container-fluid">
<div class="row">
<p class="lead">Welcome to Wavefront. Let's get you started.</p>
<hr/>
</div>

<div class="row">
<div class="col-sm-12 col-md-6">
<p>First, have a look at how Wavefront works. The Wavefront platform consists of the Wavefront service and the Wavefront proxy.</p>

<img src="images/wavefront_architecture.png" alt="Wavefront architecture" style="display:block;width:400px;margin:10px auto;"></img>

<p>For most metrics, an agent collects the metrics and pushes them to the Wavefront proxy. The proxy runs within your infrastructure and forwards collected metrics to the Wavefront service. The proxy provides authentication, flow control metrics preprocessing, and more.</p>

<p>For Amazon Web Services, metrics are pulled directly from service by the Wavefront service. Wavefront can get metrics from CloudWatch and CloudTrail and directly from AWS services such as EC2, SQS, and Redshift.</p>
</div>
<div class="col-sm-12 col-md-6"> 
<div class="well">
<video width="100%" controls autoplay><source src="images/onboarding-welcome.mp4" type="video/mp4">Your browser does not support HTML5 video.</video>
</div>
</div>
</div>  
</div>