# DHCP

Multiple DHCP servers are running on the ONP environment. The below are the list of interfaces and its networks.

<table><thead><tr><th width="195">Interface</th><th>Network</th><th width="139">Is-enabled</th><th>Service</th></tr></thead><tbody><tr><td><code>baremetal</code></td><td><code>192.168.123.0/24</code></td><td><code>true</code></td><td><code>dhcp.service</code></td></tr><tr><td><code>onp1</code></td><td><code>192.168.124.0/24</code></td><td><code>false</code></td><td><code>onp1-dhcp.service</code></td></tr><tr><td><code>onp2</code></td><td><code>192.168.125.0/24</code></td><td><code>false</code></td><td><code>onp2-dhcp.service</code></td></tr></tbody></table>

## Configuration

It uses `dnsmasq` under the hood. The container builds and starts automatically if it is enabled as it is managed by the systemd.

```
no-daemon
interface=<interface>
dhcp-range=192.168.x.2,192.168.x.254,255.255.255.0
except-interface=lo
bind-interfaces
log-dhcp
dhcp-authoritative
log-asynce
```

```
FROM fedora
MAINTAINER "Vinu K" <vinu@redhat.com>
RUN yum install -y dnsmasq
ADD dnsmasq.conf /dnsmasq.conf
ENTRYPOINT ["dnsmasq"]
CMD ["-C", "/dnsmasq.conf"]
```
