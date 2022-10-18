### Add a Kubernetes Cluster

Tanzu Observability provides a comprehensive solution for monitoring Kubernetes. To set up the Kubernetes integration, you must install the Wavefront Operator. The setup process varies based on the distribution type that you choose to monitor. 

1. In the **Collector Configuration** section, configure the deployment options for the cluster.
    1. In the **Cluster Name** text box provide the name of your Kubernetes cluster.
    1. Choose the distribution type. You have two choices:
        * Kubernetes Cluster - If you choose to install the Wavefront Operator in a Kubernetes cluster (for example, in a VMware vSphere with Tanzu or Amazon EKS cluster), proceed with the next steps. 
        * OpenShift - If you choose to use OpenShift to install the Wavefront Operator, follow the instructions displayed on the Tanzu Observability GUI and click **Finish**.
          The steps you perform are mainly done in the OpenShift Container Platform web console.
          **Note**: Logs (Beta) is not supported when you use OpenShift.

1. For a **Kubernetes Cluster**, enter the configuration options.
   1. Choose whether you want to see the logs for your cluster. By default, the **Logs (Beta)** option is set to on.
   1. Choose whether you want to enable or disable **App Auto-Discovery & Metrics**. By default, the **App Auto-Discovery & Metrics** option is set to on.
   1. Choose whether you want to use an **HTTP Proxy**. If you enable HTTP proxy, to allow outbound traffic, you must also add these URLs to your proxy rules:
      * Logs (Beta): `https://data.mngmt.cloud.vmware.com`
      * Metrics: `https://<your_cluster>.wavefront.com/`
      In addition, you must also configure the HTTP proxy settings, such as: 
      * **Host Name** - HTTP proxy host name.
      * **Port** - HTTP proxy port number.
      * **HTTP Proxy Authentication** - Can be either basic (with user name and password), or CA certificate - based (with a CA certificate).

1. For a **Kubernetes Cluster**, enter the authentication options and click **Next**.
   
   You can authenticate to the Tanzu Observability REST API by using either a user account, or a service account. In both cases the account must have an API token.
1. For a **Kubernetes Cluster**, from the **Script** section, get the deployment script. 
    1. Review the script and click the **Copy to clipboard** button.
    1. Run the script in your Kubernetes cluster.
1. After successful installation, navigate back to the Tanzu Observability GUI, and click **Finish**.

**Read More**<br/>
[Kubernetes Troubleshooting](https://docs.wavefront.com/kubernetes_troubleshooting.html)
