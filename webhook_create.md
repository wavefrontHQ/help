### Creating a Webhook

When you create a webhook you specify the list of conditions on that alert that can trigger the webhook and the content
of the POST body to send to the webhook endpoint. Wavefront provides templates for the webhook payload. The templates support
[Mustache syntax](https://mustache.github.io/) and a set of variables that you can use to customize the message.

{% include webhooks_links.md %}
