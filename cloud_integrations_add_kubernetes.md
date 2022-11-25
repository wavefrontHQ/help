### Add a Kubernetes Cluster

Tanzu Observability provides a comprehensive solution for monitoring Kubernetes. To set up the Kubernetes integration, you must install and configure the Wavefront Operator. The setup process varies based on the distribution type that you choose to monitor. 

You have two choices:

  * **Kubernetes Cluster** - If you choose to install the Wavefront Operator in a Kubernetes cluster (for example, in a VMware vSphere with Tanzu or Amazon EKS cluster), proceed with the steps below.
   
  * **OpenShift** - If you choose to use OpenShift to install the Wavefront Operator, follow the instructions displayed on the Tanzu Observability GUI and click **Finish**.
          
    **Note**: Logs (Beta) is not supported when you use OpenShift.

**To monitor a Kubernetes Cluster**:

1. Enter the configuration options.
   1. In the **Cluster Name** text box, enter a meaningful cluster name.
   1. (Optional) Choose whether you want to see the logs for your cluster. By default, the **Logs (Beta)** option is enabled.
      This option is available only if you have the Logs (Beta) feature enabled for your cluster. For more information, see [Get Started with Logs (Beta)](https://docs.wavefront.com/logging_overview.html).
   1. Choose whether you want to enable or disable **Metrics**. By default, the **Metrics** option is enabled.
   1. Choose whether you want to use an **HTTP Proxy**. If you enable HTTP proxy, to allow outbound traffic, you must add these URLs to your proxy rules:
      * Logs (Beta): `https://data.mngmt.cloud.vmware.com`
      * Metrics: `https://<your_cluster>.wavefront.com/`
   
   1. If you enable HTTP Proxy, you must also configure the HTTP proxy settings, such as: 
     
      * **Host Name** - HTTP proxy host name.
      * **Port** - HTTP proxy port number.
      * **HTTP Proxy Authentication** - Can be either basic (with user name and password), or CA certificate - based (with a CA certificate).

1. Enter the authentication options and click **Next**.
   
   You can authenticate to the Tanzu Observability REST API by using either a user account, or a service account. In both cases the account must have an API token.
1. From the **Script** section, get the deployment script. 
    1. Review the script and click the **Copy to clipboard** button.
    1. Run the script in your Kubernetes cluster.
1. After successful installation, return back to the Tanzu Observability GUI, and click **Finish**.

**Read More**<br/>
[Kubernetes Overview](https://docs.wavefront.com/wavefront_kubernetes.html)<br/>
[Kubernetes Troubleshooting](https://docs.wavefront.com/kubernetes_troubleshooting.html)
