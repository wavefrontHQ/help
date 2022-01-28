### Add an Amazon Web Services Cloud Integration

To add an Amazon Web Services Cloud integration, first select the AWS services you want to set up.

* **CloudWatch & Metrics+**
* **CloudWatch & Metrics+ & CloudTrail**

Then, establish a trust relationship between Amazon and Wavefront.

You start by granting Wavefront read-only access to your Amazon account or by giving Wavefront limited access. To achieve this, you can use a CLI method or a UI method.

For detailed instructions, see:

* [Giving Wavefront Global Read-Only Access](https://docs.wavefront.com/integrations_aws_overview.html#give-wavefront-read-only-access-to-your-amazon-account-and-get-the-role-arn)
* [Giving Wavefront Limited Access](https://docs.wavefront.com/integrations_aws_overview.html#giving-wavefront-limited-access)

Then, depending on your choice:

1. In the **Name** text box, provide a meaningful name.
2. In the **Role ARN from Amazon IAM** text box, provide the Role ARN that you got after giving Wavefront read-only access to your Amazon account.
3. If you have selected to set up **CloudWatch & Metrics+ & CloudTrail**, you must enter the following CloudTrail settings:
   
   * **Bucket Name** -- Enter the S3 bucket containing CloudTrail logs.
   * (Optional) **Prefix** -- A log file prefix specified when you created the CloudTrail.
   * **CloudTrail Region** -- The AWS Region where the CloudTrail logs reside.
   
4. Click **Register**.
