# DNS64

DNS64 is a DNS service that returns AAAA records with these synthetic IPv6 addresses for IPv4-only destinations (with A but not AAAA records in the DNS). This lets IPv6-only clients use NAT64 gateways without any other configuration.

The benefit of using DNS64 is that, the IPv6 single-stack cluster cannot communicate to the whole internet as the 40% of the internet moved to IPv6 stack and it needs a middle man called NAT64 to do the translation. DNS64 can help to resolve the hostname to IPv6 IP and handover to NAT64.

The OpenShift Network Playground uses `bind` package for this. It listens on `sno0` interface and use the network `192.168.126.0/24`.

<table data-header-hidden data-full-width="false"><thead><tr><th width="242"></th><th></th><th data-hidden></th><th data-hidden></th></tr></thead><tbody><tr><td>Directory</td><td><code>/opt/openshift-network-playground/dns64/</code></td><td></td><td></td></tr><tr><td>Service</td><td><code>dns64.service</code></td><td></td><td></td></tr></tbody></table>
