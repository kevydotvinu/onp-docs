# DNS

## OpenShift Network Playground DNS

For the host, it uses the NetworkManager + dnsmasq combination. The required entries are added in the `/etc/hosts` and `/etc/NetworkManger/dnsmasq.d/openshift-network-playground.conf` files.

{% hint style="info" %}
**INFO**

For host DNS issues, restart `NetworkManger`
{% endhint %}

## Single Node OpenShift DNS

Since the SNO can be deplyed as single-stack IPv6 cluster in the ONP environment, the DNS64 and NAT64 plays the key role to enable the outside connectivity for the nodes. The DNS64 uses the `bind` package.

