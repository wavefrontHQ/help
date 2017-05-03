### What is a Webhook?

A webhook is a user-defined HTTP callback. A webhook is usually triggered when a particular event occurs at the source
site. When the event occurs, the source site makes an HTTP POST request to the URL configured for the webhook that
contains data either passed as simple POST keys and values or in some other format such as JSON.

You can use webhooks to integrate actions with alerts:

1. Create a webhook.
1. Add the webhook ID listed under the webhook name in the Webhooks page to the Targets field of an alert.
