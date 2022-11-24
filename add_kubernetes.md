## Add a Kubernetes Integration

Tanzu Observability provides a comprehensive solution for monitoring Kubernetes. To set up the Kubernetes integration, you must install and configure the Wavefront Collector and a Wavefront Proxy. The setup process varies based on the distribution type that you choose to monitor. 


### Set Up in a Kubernetes Cluster

1. In the **Collector Configuration** section, configure the deployment options for the cluster.
    1. In the **Cluster Name** text box provide the name of your Kubernetes cluster.
    1. Choose the **Kubernetes Cluster** as a distribution type. 
1. Choose whether you want to see the logs for your cluster. By default, the **Logs (Beta)** option is enabled.
1. Choose whether you want to enable or disable **Metrics**. By default, the **Metrics** option is enabled.
1. Choose whether you want to use an **HTTP Proxy**. 
   If you enable HTTP proxy, to allow outbound traffic, you must add these URLs to your proxy rules:
    * **Logs (Beta)**: https://data.mngmt.cloud.vmware.com
    * **Metrics**: https://<your_cluster>.wavefront.com/
      
   In addition, you must also configure the HTTP proxy settings, such as: 
  
      1. **Host Name** - HTTP proxy host name.
      2. **Port** - HTTP proxy port number.
      3. **HTTP Proxy Authentication** - Can be either basic (with user name and password), or CA certificate - based (with a CA certificate).

1. Enter the authentication options and click **Next**.
   
   You can authenticate to the Tanzu Observability REST API by using either a user account, or a service account. In both cases the account must have an API token.
   
1. From the **Script** section, get the deployment script. 
    1. Review the script and click the **Copy to clipboard** button.
    1. Run the script in your Kubernetes cluster.
1. After successful installation, return back to the Tanzu Observability GUI, and click **Finish**.

### Set Up in an OpenShift Cluster

**Note**: Logs (Beta) is not supported when you use OpenShift.

1. In the **Collector Configuration** section, configure the deployment options for the cluster.
    1. In the **Cluster Name** text box provide the name of your Kubernetes cluster.
    1. Choose the **OpenShift Cluster** as a distribution type. 

1. Follow the instructions below.

#### Install and Configure the Wavefront Helm Chart on OpenShift Enterprise 4.x
    
This section contains the installation and configuration steps for full-stack monitoring of OpenShift clusters using the Wavefront Helm Chart.
    
**Install the Wavefront Helm Chart**
    
1. Log in to the OpenShift Container Platform web console as an administrator.
    
2. Create a project named <code>wavefront</code>.
    
3. In the left pane, navigate to **Helm** and select **Install a Helm Chart from the developer catalog**.
    
4. Search for **Wavefront** and click **Install Helm Chart**.
    
5. Install from the **form view** tab. Replace the following parameters with your values:

    * clusterName: &lt;OPENSHIFT_CLUSTER_NAME&gt;
    * token: [&lt;YOUR_WF_API_TOKEN&gt;](https://docs.wavefront.com/users_account_managing.html#generate-an-api-token)
    * url: https://&lt;YOUR_WF_INSTANCE&gt;.wavefront.com
    
6. Click **Install**.
    
   Because default parameters are used, the Collector runs as a Daemonset and uses <code>wavefront-proxy</code> as a sink. The Collector auto discovers the pods and services that expose metrics and dynamically starts collecting metrics for the targets. It collects metrics from the Kubernetes API server, if configured.
    
   Now, go back to your Wavefront cluster and search for the <code><OPENSHIFT_CLUSTER_NAME></code in the Kubernetes integration dashboards.
    
**Configure the Collector to Use an Existing Proxy**    

To configure Wavefront Collector to use a Wavefront proxy that's already running in your environment, follow these steps:
    
1. In the OpenShift Container Platform web console, on the **yaml view** tab, in the **proxy** section, set **enabled** to false:

    ```yaml
          proxy:
            enabled: false
    ```

    
2. On the **yaml view** tab, add **proxyAddress** under **collector**.
     
     ```yaml
          collector:
            proxyAddress: <YOUR_WF_PROXY_ADDRESS>:2878
      ```
  
    
3. Click **Install**.
    
    
**Advanced Wavefront Proxy Configuration**
    
  You can configure the proxy to change how it processes your data, port numbers, metric prefix, etc. 
  
**Configure the Wavefront Proxy Preprocessor Rules**
    
[Preprocessor rules](https://docs.wavefront.com/proxies_preprocessor_rules.html) allow you to manipulate incoming metrics before they reach the proxy. For example, you can remove confidential text strings or replace unacceptable characters. Follow these steps to create a `ConfigMap` with custom preprocessor rules:
    
1. In the left pane, navigate to **Helm**, and choose the Wavefront installation.
    
2. Under **Actions**, click **Upgrade**.
  
3. On the **yaml view** tab, under **proxy**, add **preprocessor**.
  ```yaml
        proxy:
          preprocessor:
            rules.yaml: |
              '2878':
                # fix %2F to be a / instead.  May be required on EKS.
                - rule    : fix-forward-slash
                  action  : replaceRegex
                  scope   : pointLine
                  search  : "%2F"
                  replace : "/"
                # replace bad characters ("&", "$", "!", "@") with underscores in the entire point line string
                - rule    : replace-badchars
                  action  : replaceRegex
                  scope   : pointLine
                  search  : "[&\\$!@]"
                  replace : "_"
  ```
4. Click **Upgrade**.
    
    
#### Install and Configure Wavefront Operator on OpenShift Enterprise 3.x
    
The Wavefront Collector supports monitoring of OpenShift clusters:
    
* To monitor OpenShift Origin 3.9, follow the steps in [Installation and Configuration on OpenShift](https://github.com/wavefronthq/wavefront-kubernetes-collector/tree/main/docs/openshift.md).
    
* To monitor OpenShift Enterprise 3.11, follow the steps in [Installation and Configuration of Wavefront Collector Operator on OpenShift](https://github.com/wavefronthq/wavefront-kubernetes-collector/tree/main/docs/openshift-operator.md).


### Learn More

* [Kubernetes Overview](https://docs.wavefront.com/wavefront_kubernetes.html)
* [Kubernetes Troubleshooting](https://docs.wavefront.com/kubernetes_troubleshooting.html)
