# CLI Tool

The CLI interface is the only option by which we can consume the complete features of the OpenShift Network Playground. The `onp help` command can print all the available options. To interact with the CLI tool, either use the Cockpit Terminal or the SSH connection.

<details>

<summary>Credentials</summary>

```
username: onp
password: Onp@123
```

</details>

<pre class="language-bash"><code class="lang-bash"><strong>onp help
</strong><strong>OpenShift Network Playground CLI
</strong>
It includes the administrative commands for managing the ONP.

Usage: onp [SUBCOMMAND] [VARIABLE_NAME]=&#x3C;variable>

Subcommands:
  ssh-pullsecret OCM_TOKEN=&#x3C;OCM_TOKEN>  Generate SSH keys and download pullsecret file
  install-config                        Generate install-config.yaml file
  cluster                               Create an OpenShift cluster
  clean                                 Clean old cluster resources
  go-download                           Download and install Golang
  kind-download                         Download and install Kind
  kind-create-onp                       Create a Kind cluster
  kind-delete-onp                       Delete a Kind cluster
  kind-create-ovn                       Create an OVN Kind cluster
  kind-delete-ovn                       Create an OVN Kind cluster
  sno                                   Create an IPv6 single-stack SNO cluster
  onp-files                             Clone the ONP sample manifests
  rhcos-livecd NETWORK=newtork=default  Create a RHCOS VM with custom network
  disconnect-cluster                    Disconnect cluster from internet
  connect-cluster                       Connect cluster to internet
  services                              List services status
  bootstrap-ip                          Show bootstrap IP
  store-release FROM=4.x.y              Store OpenShift 4.x.y release
  restore-release TO=4.x.y              Restore OpenShift 4.x.y release

Example:
  onp cluster LOGLEVEL=debug

Variables:
  OCM_TOKEN     token from https://cloud.redhat.com/openshift/token/show
  RELEASE       stable-4.10, latest-4.9, 4.9.0, etc
  LOGLEVEL      debug, info, warn, error
  NETWORK       network=default, bridge=onp1-dhcp, bridge=onp2-dhcp
  TO            4.10.10, 4.11.11, 4.12.12, etc
  FROM          4.10.10, 4.11.11, 4.12.12, etc

</code></pre>
