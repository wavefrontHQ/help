## Add a Kubernetes Integration

VMware Aria Operations for Applications (formerly known as Tanzu Observability by Wavefront) provides a comprehensive solution for monitoring Kubernetes. To set up the Kubernetes integration, you must install and configure the Wavefront Collector for Kubernetes and a Wavefront proxy. With the 2022-48.x we introduce a new  Kubernetes Observability Operator which simplifies the deployment. 

The setup process varies based on the distribution type that you choose to monitor. 


1. Log in to your product cluster: https://<your_cluster>.wavefront.com.
2. Click **Integrations** on the toolbar.
3. In the **Featured** section, click the **Kubernetes** tile.
4. Click **Add Integration**.


### Kubernetes Quick Install Using the Kubernetes Operator

1. In the **Collector Configuration** section, configure the deployment options for the cluster.
    1. In the **Cluster Name** text box provide the name of your Kubernetes cluster.
    1. Choose the **Kubernetes Cluster** as a distribution type. 
1. Choose whether you want to see the logs for your cluster. By default, the **Logs (Beta)** option is enabled.
1. Choose whether you want to enable or disable **Metrics**. By default, the **Metrics** option is enabled.
1. Choose whether you want to use an **HTTP Proxy**. 
   If you enable HTTP proxy, to allow outbound traffic, you must add these URLs to your proxy rules:
    * **Logs (Beta)**: https://data.mgmt.cloud.vmware.com
    * **Metrics**: https://<your_cluster>.wavefront.com/
      
   In addition, you must also configure the HTTP proxy settings, such as: 
  
      1. **Host Name** - HTTP proxy host name.
      2. **Port** - HTTP proxy port number.
      3. **HTTP Proxy Authentication** - Can be either basic (with user name and password), or CA certificate - based (with a CA certificate).

1. Enter the authentication options and click **Next**.
   
   You can authenticate to the Operations for Applications REST API by using either a user account, or a service account. In both cases the account must have an API token.
   
1. From the **Script** section, get the deployment script. 
    1. Review the script and click the **Copy to clipboard** button.
    1. Run the script in your Kubernetes cluster.
1. After successful installation, return back to the Operations for Applications GUI, and click **Finish**.

### Kubernetes Install in an OpenShift Cluster

Complete the steps below and click **Finish**.

**Note**: Logs (Beta) is not supported when you use OpenShift.


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
    
   Now, go back to your Wavefront cluster and search for the <code>OPENSHIFT_CLUSTER_NAME</code> in the Kubernetes integration dashboards.
    
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
    
    
#### Install and Configure Wavefront Collector on OpenShift Enterprise 3.x

The Wavefront Collector supports monitoring of OpenShift clusters:
    
* To monitor OpenShift Origin 3.9, follow the steps in [Installation and Configuration on OpenShift](https://github.com/wavefronthq/wavefront-kubernetes-collector/tree/main/docs/openshift.md).
    
* To monitor OpenShift Enterprise 3.11, follow the steps in [Installation and Configuration of Wavefront Collector Operator on OpenShift](https://github.com/wavefronthq/wavefront-kubernetes-collector/tree/main/docs/openshift-operator.md).

### Kubernetes Quick Install Using Helm

**Note**: We will deprecate the Helm or manually-installed Wavefront Collector for Kubernetes and Wavefront proxy next year. Our new Kubernetes Operator replaces the Helm or manually installed Wavefront Collector for Kubernetes and Wavefront proxy for all Kubernetes Distributions except for OpenShift Container Platform. For more information, see [Obsolescence and Remediation](https://docs.wavefront.com/wavefront_obsolescence_policy.html#kubernetes-integration).

1. Ensure that you have installed [helm](https://helm.sh/docs/intro/).
2. Add the Wavefront helm repo:
```
helm repo add wavefront https://wavefronthq.github.io/helm/
helm repo update
```
3. To deploy the Wavefront Collector and Wavefront Proxy:

    Using helm 2:
    ```
    helm install wavefront/wavefront --name wavefront --set wavefront.url=[[wavefrontInstanceURL]] --set wavefront.token=[[APIToken]] --set clusterName=<YOUR_CLUSTER_NAME> --namespace wavefront
    ```
    Using helm 3:
    ```
    kubectl create namespace wavefront
    helm install wavefront wavefront/wavefront --set wavefront.url=[[wavefrontInstanceURL]] --set wavefront.token=[[APIToken]] --set clusterName=<YOUR_CLUSTER_NAME> --namespace wavefront
    ```

**Note:** The `clusterName` property refers to the Kubernetes cluster, for example, `dev-cluster`. You must set this property. For vSphere Tanzu, add `--set vspheretanzu.enabled=true` along with helm install command.

Refer to the Wavefront [helm chart](https://github.com/wavefrontHQ/helm/tree/master/wavefront) for further options.

### Kubernetes Manual Install

**Note**: We will deprecate the Helm or manually-installed Wavefront Collector for Kubernetes and Wavefront proxy in 2023. Our new Kubernetes Operator replaces the Helm or manually installed Wavefront Collector for Kubernetes and Wavefront proxy for all Kubernetes Distributions except for OpenShift Container Platform. For more information, see [Obsolescence and Remediation](https://docs.wavefront.com/wavefront_obsolescence_policy.html#kubernetes-integration).

Follow the instructions below to manually set up Kubernetes monitoring. For more details about the available options, see the [Wavefront Collector for Kubernetes Configuration](https://github.com/wavefrontHQ/observability-for-kubernetes/blob/main/docs/collector/configuration.md).


#### Step 1. Deploy a Wavefront Proxy in Kubernetes

1. Download [wavefront.yaml](https://raw.githubusercontent.com/wavefrontHQ/wavefront-kubernetes/master/wavefront-proxy/wavefront.yaml) to your system.
2. Edit the file and set `WAVEFRONT_URL` to `[[wavefrontInstanceURL path="/api/"]]` and `WAVEFRONT_TOKEN` to `[[APIToken]]`.
3. Run `kubectl create -f </path/to>/wavefront.yaml` to deploy the proxy.

The Wavefront proxy and a `wavefront-proxy` service should now be running in Kubernetes.

#### Step 2. Deploy Wavefront Collector for Kubernetes

1. Create a directory named `wavefront-collector-dir` and download the following files to that directory:
  * [0-collector-namespace.yaml](https://raw.githubusercontent.com/wavefrontHQ/observability-for-kubernetes/main/collector/deploy/kubernetes/0-collector-namespace.yaml)
  * [1-collector-cluster-role.yaml](https://raw.githubusercontent.com/wavefrontHQ/observability-for-kubernetes/main/collector/deploy/kubernetes/1-collector-cluster-role.yaml)
  * [2-collector-rbac.yaml](https://raw.githubusercontent.com/wavefrontHQ/observability-for-kubernetes/main/collector/deploy/kubernetes/2-collector-rbac.yaml)
  * [3-collector-service-account.yaml](https://raw.githubusercontent.com/wavefrontHQ/observability-for-kubernetes/main/collector/deploy/kubernetes/3-collector-service-account.yaml)
  * [4-collector-config.yaml](https://raw.githubusercontent.com/wavefrontHQ/observability-for-kubernetes/main/collector/deploy/kubernetes/4-collector-config.yaml)
  * [5-collector-daemonset.yaml](https://raw.githubusercontent.com/wavefrontHQ/observability-for-kubernetes/main/collector/deploy/kubernetes/5-collector-daemonset.yaml)

  **Note**: Download the following file only for vSphere Tanzu environment.
  * [0-vsphere-tanzu-rolebinding.yaml](https://raw.githubusercontent.com/wavefrontHQ/observability-for-kubernetes/main/collector/deploy/vsphere-tanzu/0-vsphere-tanzu-rolebinding.yaml)

2. Edit `4-collector-config.yaml` and replace `clusterName: k8s-cluster` with the name of your Kubernetes cluster.

3. If RBAC is disabled in your Kubernetes cluster, edit `5-collector-daemonset.yaml` and comment out `serviceAccountName: wavefront-collector`.

4. Run `kubectl create -f </path/to/wavefront-collector-dir>/` to deploy the collector on your cluster.

To verify the collector is deployed, run `kubectl get pods -n wavefront-collector`.

#### Step 3. (Optional) Deploy the kube-state-metrics Service

The Wavefront Collector natively collects various [metrics](https://github.com/wavefrontHQ/observability-for-kubernetes/blob/main/docs/collector/metrics.md#kubernetes-state-source) about the state of Kubernetes resources. You can optionally deploy the third party [kube-state-metrics](https://github.com/kubernetes/kube-state-metrics) service to collect additional metrics.

To deploy kube-state-metrics:

1. Download [kube-state.yaml](https://raw.githubusercontent.com/wavefrontHQ/wavefront-kubernetes/master/ksm-all-in-one/kube-state.yaml) to your system.
2. Run `kubectl create -f </path/to>/kube-state.yaml`.

The `kube-state-metrics` service starts running on your cluster. The Wavefront Collector automatically discovers the service and starts collecting metrics from the kube-state-metrics service.

### Learn More

* [Kubernetes Overview](https://docs.wavefront.com/wavefront_kubernetes.html)
* [Kubernetes Troubleshooting](https://docs.wavefront.com/kubernetes_troubleshooting.html)
