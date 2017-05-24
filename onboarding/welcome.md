<div class="container-fluid">
<div class="row">
<p class="lead">Welcome to Wavefront. Let's get you started.</p>
<hr/>
</div>

<div class="row">
<div class="col-sm-12 col-md-6">
First, have a look at how Wavefront works.

Wavefront makes it easy to stream your data into Wavefront. Wavefront supports two approaches depending on where the metrics originate: push from agents and pull from cloud services.

<img src="images/wavefront_architecture.png" alt="Wavefront architecture" style="height:75%;"></img>

An agent collects metrics and pushes it to the Wavefront proxy. The proxy runs within your infrastructure and forwards collected data to the Wavefront service. The proxy provides authentication, [flow control](https://community.wavefront.com/docs/DOC-1034), [metrics preprocessing](https://community.wavefront.com/docs/DOC-1207), and more.

Wavefront directly pulls metrics data from cloud services such as Amazon Web Services (AWS). Wavefront offers CloudWatch, CloudTrail, and AWS Metrics+ [cloud integrations](https://community.wavefront.com/docs/DOC-1032).
</div>
<div class="col-sm-12 col-md-6"> 
<div class="well">
<video width="100%" controls autoplay><source src="images/onboarding-welcome.mp4" type="video/mp4">Your browser does not support HTML5 video.</video>
</div>
</div>
</div>  
</div>