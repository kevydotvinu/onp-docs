# Network

## Network Interface

The main interface of the ONP expose the outside world. Additionally, the machine does have the below list of interfaces.

* baremetal
* provisioning
* onp1
* onp2
* sno0
* nat64

All of the above interfaces are the bridge interface which holds a dummy interface that is created with the same name. For example, baremetal-dummy. For the OpenShift Bare metal IPI cluster uses both the baremetal and provisioning interfaces. The onp1 and onp2 are created for the additional interfaces of the OpenShift cluster nodes. It also provides the DHCP network. The Single Node OpenShift cluster uses the sno0 and nat64 interfaces. The nat64 interface responsible for the IPv6 to IPv4 conversion.

The `nmconnection` key files are added in the ignition and it will get ready in the startup itself. The `MASQUERADE` `nat` rules enables the traffic flow from one interface to another.
