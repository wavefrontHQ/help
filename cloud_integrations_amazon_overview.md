### Amazon Web Services Integration

Monitor and manage your Amazon Web Services integration instances. If you still haven't set up the integration, click **Set up integration** and do so. Setting up an Amazon Web Services cloud integration requires establishing a trust relationship between Amazon and Tanzu Observability by Wavefront. This involves creating a role in Amazon Web Services, providing it with read-only access, and getting the Role ARN.

After you register you integration, on this **Overview** page, you can:

* Monitor your existing AWS integration instances.
* Add a new integration instance, by clicking the **Add an integration instance** and following the instructions.
* Search through the list of the available integration instances.
* Manage your existing AWS integration instances by clicking the ellipsis icon and selecting an option to:
  * Add an integration to an existing one. 
  
    For example, if you have previously selected to configure CloudWatch and Metrics+, you can also add CloudTrail.
    
  * Edit an integration instance.
  * Enable a previously disabled integration instance.
  * Disable an integration instance.
  * Delete an integration instance if you no longer need it.

**Read More**<br />
* [Amazon Web Services Integration Overview](https://docs.wavefront.com/integrations_aws_overview.html)
* [Set Up and Manage an AWS Integration by Using the API](https://docs.wavefront.com/integrations_aws_overview.html#giving-limited-access)
