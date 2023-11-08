## Add a Kubernetes Integration

VMware Aria Operations for Applications (formerly known as Tanzu Observability by Wavefront) provides a comprehensive solution for monitoring Kubernetes. To set up the Kubernetes integration, you must install and configure our Kubernetes Metrics Collector and a Wavefront proxy. With the 2022-48.x release we introduced the Kubernetes Observability Operator which simplifies the deployment of the Kubernetes Metrics Collector and the Wavefront proxy. 

The setup process varies based on the distribution type that you choose to monitor, and whether your Operations for Applications service is onboarded to the VMware Cloud services platform.


1. Log in to your product cluster.
2. Click **Integrations** on the toolbar.
3. In the **Featured** section, click the **Kubernetes** tile.
4. Click **Add Integration**.


### Kubernetes Quick Install Using the Kubernetes Operator

1. In the **Collector Configuration** section, configure the deployment options for the cluster.
    1. In the **Cluster Name** text box provide the name of your Kubernetes cluster.
    1. Choose the **Kubernetes Cluster** as a distribution type. 
1. Choose whether you want to see the logs for your cluster. By default, the **Logs** option is enabled.
1. Choose whether you want to enable or disable **Metrics**. By default, the **Metrics** option is enabled.
1. Choose whether you want to use an **HTTP Proxy**. 
   If you enable HTTP proxy, to allow outbound traffic, you must add these URLs to your proxy rules:
    * **Logs**: <code>https://data.mgmt.cloud.vmware.com</code>
    * **Metrics**: <code>https://your_cluster.wavefront.com/</code>
      
   In addition, you must also configure the HTTP proxy settings, such as: 
  
      1. **Host Name** - HTTP proxy host name.
      2. **Port** - HTTP proxy port number.
      3. **HTTP Proxy Authentication** - Can be either basic (with user name and password), or CA certificate - based (with a CA certificate).

1. Enter the authentication options and click **Next**.
   
   The authentication options vary depending on whether your [Operations for Applications service is onboarded to VMware Cloud services](https://docs.wavefront.com/subscriptions-differences.html). For more details, see [Proxy Authentication Types](https://docs.wavefront.com/proxies_installing.html#proxy-authentication-types).
   
   * If your service **is onboarded** to VMware Cloud services, choose to authenticate by using either an **OAuth App** or an **API token**. 

     * **OAuth App** authentication requires you to use an existing App ID, App Secret, and Organization ID of a server to server app that has the **Proxies** service role assigned and belongs to the VMware Cloud services organization running the service.
     * **API Token** authentication requires you to use an API token that belongs to your user account in the VMware Cloud organization running the service. Note that you must regenerate and reconfigure the API Token periodically depending on the token TTL configuration.

   * If your service is **not onboarded** to VMware Cloud services, you can authenticate to the Operations for Applications REST API by using either a user account, or a service account. In both cases, the account must have an Operations for Applications API token associated with it.
   
1. In the **Script** section, review the script and click the **Copy to clipboard** button.
   
   * When your service **is onboarded** to VMware Cloud services:
     * If you have selected **OAuth App** as the authentication type, replace `<CSP_APP_ID>` and `<CSP_APP_SECRET>` with your server to server app credentials and `<CSP_ORG_ID>` with the ID of the VMware Cloud organization running the service.
     * If you have selected **API token** as the authentication type, replace `<CSP_API_TOKEN>` with your VMware Cloud services API token.
   * When your service is **not onboarded** to VMware Cloud services, proceed to the next step.
1. Run the script in your Kubernetes cluster.
1. After successful installation, return back to the Operations for Applications UI, and click **Finish**.

### Kubernetes Install in an OpenShift Cluster

Complete the steps below and click **Finish**.

**Note**: The Logs feature is not supported when you use OpenShift.


#### Install and Configure the Operations for Applications Helm Chart on OpenShift Enterprise 4.x
    
This section contains the installation and configuration steps for full-stack monitoring of OpenShift clusters using the Operations for Applications Helm Chart.
    
**Install the Operations for Applications Helm Chart**
    
1. Log in to the OpenShift Container Platform web console as an administrator.
    
2. Create a project named <code>MyProject</code>.
    
3. In the left pane, navigate to **Helm** and select **Install a Helm Chart from the developer catalog**.
    
4. Search for **MyProject** and click **Install Helm Chart**.
    
5. Install from the **form view** tab. Replace the following parameters with your values:

    * clusterName: &lt;OPENSHIFT_CLUSTER_NAME&gt;
    * token: [&lt;YOUR_WF_API_TOKEN&gt;](https://docs.wavefront.com/users_account_managing.html#generate-an-api-token)
    * url: https://&lt;YOUR_WF_INSTANCE&gt;.wavefront.com
    
6. Click **Install**.
    
   Because default parameters are used, the Kubernetes Metrics Collector runs as a DaemonSet and uses a Wavefront proxy as a sink. The Collector auto discovers the pods and services that expose metrics and dynamically starts collecting metrics for the targets. It collects metrics from the Kubernetes API server, if configured.
    
   Now, go back to your Operations for Applications cluster and search for the <code>OPENSHIFT_CLUSTER_NAME</code> in the Kubernetes integration dashboards.
    
**Configure the Collector to Use an Existing Proxy**    

To configure the Kubernetes Metrics Collector to use a Wavefront proxy that's already running in your environment, follow these steps:
    
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
    
1. In the left pane, navigate to **Helm**, and choose your installation.
    
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
    
    
#### Install and Configure the Collector on OpenShift Enterprise 3.x

**Note**: The Helm or manually-installed Kubernetes Metrics Collector and Wavefront proxy is deprecated. Our new Observability for Kubernetes Operator replaces the Helm or manually installed Kubernetes Metrics Collector and Wavefront proxy for all Kubernetes Distributions except for OpenShift Container Platform. For more information, see [Obsolescence and Remediation](https://docs.wavefront.com/wavefront_obsolescence_policy.html#kubernetes-integration).

Our Collector supports monitoring of OpenShift clusters:
    
* To monitor OpenShift Origin 3.9, follow the steps in [Installation and Configuration on OpenShift](https://github.com/wavefronthq/wavefront-kubernetes-collector/tree/main/docs/openshift.md).
    
* To monitor OpenShift Enterprise 3.11, follow the steps in [Installation and Configuration of the Operator on OpenShift](https://github.com/wavefronthq/wavefront-kubernetes-collector/tree/main/docs/openshift-operator.md).

### Learn More

* [Kubernetes Overview](https://docs.wavefront.com/wavefront_kubernetes.html)
* [Kubernetes Troubleshooting](https://docs.wavefront.com/kubernetes_troubleshooting.html)
