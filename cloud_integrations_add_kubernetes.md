### Add a Kubernetes Cluster

To set up the Kubernetes integration, you must install and configure the Observability for Kubernetes Operator. The setup process varies based on the distribution type that you choose to monitor.

You have two choices for the distribution types:

  * **Kubernetes Cluster** - If you choose to install the Observability for Kubernetes Operator in a Kubernetes cluster (for example, in a VMware vSphere with Tanzu or Amazon EKS cluster), proceed with the steps below.
   
  * **OpenShift** - If you choose to use OpenShift, follow the instructions displayed in the Operations for Applications UI and click **Finish**.
          
    **Note**: Logs feature is not supported when you use OpenShift.

**To monitor a Kubernetes cluster**:

1. In the **Cluster Name** text box, enter a meaningful cluster name.
1. (Optional) Choose whether you want to see the logs for your cluster. By default, the **Logs** option is enabled.

    This option is available only if you have the Logs feature enabled for your cluster. For more information, see [Get Started with Logs](https://docs.wavefront.com/logging_overview.html).
    
1. Choose whether you want to enable or disable **Metrics**. By default, the **Metrics** option is enabled.
1. Choose whether you want to use an **HTTP Proxy**. If you enable HTTP proxy, to allow outbound traffic, you must add these URLs to your proxy rules:
   * Logs: `https://data.mgmt.cloud.vmware.com`
   * Metrics: `https://<your_cluster>.wavefront.com/`
   
1. If you enable HTTP Proxy, you must also configure the HTTP proxy settings, such as: 
     
   * **Host Name** - HTTP proxy host name.
   * **Port** - HTTP proxy port number.
   * **HTTP Proxy Authentication** - Can be either basic (with user name and password), or CA certificate - based (with a CA certificate).

1. Configure the authentication options and click **Next**.
    
1. In the **Script** section, review the script and click the **Copy to clipboard** button.
    
1. Run the script in your Kubernetes cluster.
    
1. After successful installation, return back to the Operations for Applications UI, and click **Finish**.

**Read More**<br/>
[Kubernetes Overview](https://docs.wavefront.com/wavefront_kubernetes.html)<br/>
[Kubernetes Troubleshooting](https://docs.wavefront.com/kubernetes_troubleshooting.html)
[Proxy Authentication Types](https://docs.wavefront.com/proxies_installing.html#proxy-authentication-types)
