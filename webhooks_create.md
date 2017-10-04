### Creating an Alert Target

When you create a create an alert target, the information you specify depends in part on the alert target type. 

* For any alert target, specify when the alert triggers. You also specify the content of the Alert Target POST Body Template. 

* For email alert targets, specify the email target address and subject. 

* For PagerDuty alert targets, specify the PagerDuty key. 

* For webhook alert targets, specify the webhook endpoint and the content of the POST body to send to the endpoint. The endpoint must be a public URL. 

Wavefront provides payload templates for each alert target type, and for several notification targets. The templates support

{% include webhooks_links.md %}
