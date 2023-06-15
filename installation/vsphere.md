# vSphere

In the vSphere installation, the additional configuration we need is hardware virtualization. Please see the below image for the same.

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
**INFO**

In VMware ESXi, enable `Hardware virtualization` (Expose hardware assisted virtualization to the guest OS).
{% endhint %}

## Download

{% code overflow="wrap" %}
```bash
curl -LO https://github.com/kevydotvinu/openshift-network-playground/releases/download/v0.1.0/onp-v0.1.0-x86_64.iso
```
{% endcode %}

## Installation

Boot it up and wait for the installation to complete. Monitor the progress in the machine console.

{% hint style="danger" %}
**IMPORTANT**

The ISO boot will erase ALL the data on the `/dev/sda` disk and install OpenShift Network Playground automatically.
{% endhint %}
