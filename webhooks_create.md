### Creating a Webhook

When you create a webhook you specify the list alert state changes that can trigger the webhook, the webhook endpoint, and the content of the POST body to send to the endpoint. 

Wavefront provides payload templates for several notification types. The templates support
[Mustache syntax](https://mustache.github.io/) and a set of functions and variables that you can use to customize the payload.

{% include webhooks_links.md %}
