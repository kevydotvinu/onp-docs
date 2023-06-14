# Single Node OpenShift Cluster

The OpenShift Network Playground allows to deploy the below three different SNO clusters.

* Single-stack IPv4
* Single-stack IPv6
* Dual-stack

The SNO deployment can only be done using the CLI with `onp` command.

{% tabs %}
{% tab title="IPv4" %}
```bash
onp sno4 RELEASE=stable OCM_TOKEN=<ocm-token>
```
{% endtab %}

{% tab title="IPv6" %}
```
onp sno6 RELEASE=stable OCM_TOKEN=<ocm-token>
```
{% endtab %}

{% tab title="Dual-stack" %}
```
onp sno64 RELEASE=stable OCM_TOKEN=<ocm-token>
```
{% endtab %}
{% endtabs %}

{% hint style="info" %}
**INFO**

Get OCM\_TOKEN from [https://cloud.redhat.com/openshift/token/show](https://cloud.redhat.com/openshift/token/show)
{% endhint %}

{% hint style="info" %}
**TIP**

OCM\_TOKEN only requires at the first deployment. The pullsecret saves locally.
{% endhint %}
