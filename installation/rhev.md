# RHEV

In the RHEV installation, the additional configuration we need is Pass-Through Host CPU. Please see the below image for the same.

<figure><img src="../.gitbook/assets/Screenshot from 2023-06-14 21-22-02.png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
**INFO**

In Red Hat Virtualization, enable the `Pass-Through Host CPU` CPU option in the Virtual Machine settings (Under the Host section).
{% endhint %}

## Download

```
curl -LO https://github.com/kevydotvinu/openshift-network-playground/releases/download/v0.1.0/onp-v0.1.0-x86_64.iso
```

## Installation

Boot it up and wait for the installation to complete. Monitor the progress in the machine console.

{% hint style="danger" %}
**IMPORTANT**

The ISO boot will erase ALL the data on the `/dev/sda` disk and install OpenShift Network Playground automatically.
{% endhint %}
