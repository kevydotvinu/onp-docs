# OpenShift Bare Metal IPI Cluster

## How it works

It uses VirtualBMC service in front of the cluster nodes. In the `install-config.yaml` file, the BMC information will be shared. The installer interact with the VBMC to turn ON the nodes when it requires. To know more about VBMC, please see [this](https://github.com/openstack/virtualbmc).

## Cockpit installation

The bare metal IPI cluster deployment does not require any configuration in OpenShift Network Playground. Once the ONP is ready, the `onp deploy RELEASE=stable` command can be executed to start the installation. The Cockpit also gives the option to do the deployment.

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

## CLI installation

To deploy the cluster using the CLI, the onp command can be used.

```
onp deploy RELEASE=stable OCM_TOKEN=<ocm-token>
```

{% hint style="info" %}
**INFO**

Get OCM\_TOKEN from [https://cloud.redhat.com/openshift/token/show](https://cloud.redhat.com/openshift/token/show). It only requires at the first deployment. The pullsecret saves locally.
{% endhint %}

