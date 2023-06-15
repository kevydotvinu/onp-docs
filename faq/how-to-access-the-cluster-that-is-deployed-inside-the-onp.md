# How to access the cluster that is deployed inside the ONP?

Since the DNAT rules are in place in the OpenShift Network Playground host, access to the OpenShift cluster will be using the same host IP.

## OpenShift Console

<details>

<summary>Step1: Add DNS</summary>

```
echo "<onp-ip> console-openshift-console.apps.ocp.example.local oauth-openshift.apps.ocp.example.local" | sudo tee -a /etc/hosts
```

</details>

<details>

<summary>Step2: Access Console</summary>

```
URL     : console-openshift-console.apps.ocp.example.local
Username: kubeadmin
Password: <password>
```

</details>

## OpenShift CLI

<details>

<summary>Step1: Add DNS</summary>

```
echo "<onp-ip> console-openshift-console.apps.ocp.example.local oauth-openshift.apps.ocp.example.local" | sudo tee -a /etc/hosts
```

</details>

<details>

<summary>Step2: SSH to OpenShift Network Playground Host</summary>

```
ssh onp@<onp-ip>
```

</details>

<details>

<summary>Step3: Use <code>oc</code> Command</summary>

```
oc get clusterversion
```

</details>
