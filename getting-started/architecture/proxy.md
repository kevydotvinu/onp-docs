# Proxy

The OpenShift Network Playground uses `squid` for the proxy. It is a SSL-bump proxy. The certificates associated with it will be placed inside `/opt/openshift-network-playground/proxy/certs/` directory. However, the compact OpenShift cluster which is deployed by the OpenShift Network Playground automatically adds that in the `install-config.yaml` file.

The proxy service is managed by systemd service named `proxy.service`.

<table data-header-hidden data-full-width="false"><thead><tr><th width="242"></th><th></th><th data-hidden></th><th data-hidden></th></tr></thead><tbody><tr><td>Directory</td><td><code>/opt/openshift-network-playground/proxy/</code></td><td></td><td></td></tr><tr><td>Service</td><td><code>proxy.service</code></td><td></td><td></td></tr></tbody></table>

{% hint style="info" %}
**INFO**

By default only compact cluster uses the proxy and not SNO cluster.
{% endhint %}

All the files (`Containerfile` and configuration) related to the proxy will be placed under the `/opt/openshift-network-playground/proxy/` directory.
