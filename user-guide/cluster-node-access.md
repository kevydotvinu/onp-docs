# Cluster Node Access

The OpenShift cluster node access is something that the user needs when it comes to network-related tasks because the cluster node access might be broken and the node will not be accessible through SSH connection in that case. The Cockpit console of the virtual machines solves that problem by leveraging the serial console feature of Libvirt.

<figure><img src="../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/vm-serial-console-option.png" alt=""><figcaption></figcaption></figure>

<details>

<summary>Credentials</summary>

```
username: core
password: Core@123
```

</details>

{% hint style="info" %}
**TIP**\
Press `Enter` when we select the Serial console (console1) option to get the prompt.
{% endhint %}
