# Prerequisites

## OpenShift cluster manager token

The OCM token is used to download the pullsecret and save it locally. It can be copied from [here](https://console.redhat.com/openshift/token/show). It only requires at the time of the first OpenShift cluster deployment.

## Machine

|      Machine     | CPU |  RAM  |  DISK  |
| :--------------: | :-: | :---: | :----: |
| VM or Bare-metal |  20 | 80 GB | 320 GB |

{% hint style="info" %}
**INFO**

Enable nested virtualization if the host is a VM.
{% endhint %}
