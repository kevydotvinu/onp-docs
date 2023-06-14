# PXE

The PXE feature of `dnsmasq` used here. The OpenShift Bare metal IPI provisioning network uses this PXE service. The below is the configuration information.

<table data-header-hidden><thead><tr><th width="209"></th><th></th></tr></thead><tbody><tr><td>Directory</td><td><code>/opt/openshift-network-playground/pxe/</code></td></tr><tr><td>Service</td><td><code>pxe.service</code></td></tr></tbody></table>

```
no-daemon
interface=provisioning
dhcp-range=172.22.0.3,172.22.0.253,255.255.255.0
except-interface=lo
bind-interfaces
log-dhcp
log-queries
dhcp-authoritative
log-async
enable-tftp
dhcp-userclass=set:ipxe,iPXE
dhcp-boot=tag:ipxe,http://172.22.0.2/boot.ipxede
```

```
FROM fedora
MAINTAINER "Vinu K" <vinu@redhat.com>
RUN yum install -y dnsmasq
ADD dnsmasq.conf /dnsmasq.conf
ENTRYPOINT ["dnsmasq"]
CMD ["-C", "/dnsmasq.conf"]
```
