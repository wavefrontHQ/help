### Add an Amazon Cloud Integration

Setting up an Amazon cloud integration requires establishing a trust relationship between Amazon and VMware Aria Operations for Applications. 

You start by granting Operations for Applications [read-only access to your Amazon account](https://docs.wavefront.com/integrations_aws_overview.html#give-read-only-access-to-your-amazon-account-and-get-the-role-arn) or by giving [limited access](https://docs.wavefront.com/integrations_aws_overview.html#giving-limited-access).

Then, you register the integration by providing the necessary information. See [AWS Integration Overview](https://docs.wavefront.com/integrations_aws_overview.html) for information about setting up and managing the AWS Cloud integration.

### Set Up AWS CloudWatch Logs (Beta)

You can use an AWS Lambda function to ingest CloudWatch logs to Operations for Applications. CloudWatch provides data and actionable insights to monitor your applications and respond to system-wide performance changes. It also helps you optimize resource utilization and get a unified view of operational health. CloudWatch collects monitoring and operational data in the form of logs, metrics, and events, providing a unified view of AWS resources, applications, and services that run on AWS and on-premises servers. You can use CloudWatch to detect anomalous behavior in your environments, set alarms, visualize logs and metrics side by side, take automated actions, troubleshoot issues, and discover insights to keep applications running smoothly. To understand more about CloudWatch, see the Amazon CloudWatch documentation.

#### Install the Wavefront Proxy

The Wavefront proxy is required to send logs from your systems to Operations for Applications. If you have not already done so, install a [Wavefront proxy (version 12.2 or later)](https://docs.wavefront.com/proxies_installing.html) in your AWS environment.

#### Create an AWS Lambda Function

1. Log in to the AWS Management Console, search for **Lambda**, and select it.
2. Click **Applications** on the left and click the **Create Application** button.
3. Click the **Serverless application** tab, search for **VMware-Log-Insight-Cloud**, and select it.
4. Scroll down and in the **Application settings** section in the bottom right, provide the Wavefront proxy details.
    * In the **APIToken** text box, enter a valid Operations for Applications API token.
    * In the **APIUrl** text box, enter the Wavefront proxy URL.
    * In the **NameOfFunction** text box, enter a meaningful name for the Lambda function.
5. Click **Deploy**.
6. Add a trigger from the CloudWatch log stream.
    * Navigate to your Lambda function and click it.
    * Click the **Add trigger** button and from the drop-down menu select **CloudWatch Logs**.
    * Select the **CloudWatch Logs** Log group that serves as the event source.
    * Give the filter a meaningful name and click **Add**.
      
      Once you create the trigger, your function starts sending logs from CloudWatch to our service. It takes a few minutes for the CloudWatch logs to show up.

#### View the AWS CloudWatch Logs

View logs in the [**Logs Browser**](https://docs.wavefront.com/logging_log_browser.html). It takes a few minutes for the CloudWatch logs to show up.


