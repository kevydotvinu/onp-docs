# Backup OpenShift Releases

The OpenShift cluster can be stored and restored to reduce the installation time. The restoration of the cluster hardly takes seven minutes to initialize the cluster.

## How it works

To store the cluster, onp takes the below actions.

* Gracefully shuts down the cluster.
* Copy the virtual machine disk to another location.
* Copy the `kubeconfig` and `kubeadmin-password` files to another location.

The restoration takes the reverse and waits for the cluster to initialize properly.

{% hint style="info" %}
**INFO**

Check if there is any pending CSR and approve it when the cluster initializes.
{% endhint %}

## Store release

```
onp store-release FROM=4.13.0
```

## Restore release

```
onp restore-release TO=4.13.0
```
