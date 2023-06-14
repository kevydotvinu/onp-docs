# Proxy

The OpenShift Network Playground uses `squid` for the proxy. It is a SSL-bump proxy. The certificates associated with it will be placed inside `/opt/openshift-network-playground/proxy/certs/` directory. However, the compact OpenShift cluster which is deployed by the OpenShift Network Playground automatically adds that in the `install-config.yaml` file.

The proxy service is managed by systemd service named `proxy.service`.

{% hint style="info" %}
To restart the proxy service, try 'sudo systemctl restart proxy.service' command.

We can also check the status using 'onp services' command.
{% endhint %}

All the files (`Containerfile` and configuration) related to the proxy will be placed under the `/opt/openshift-network-playground/proxy/` directory.
