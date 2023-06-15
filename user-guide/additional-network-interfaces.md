# Additional Network Interfaces

To add an additional network interface to the OpenShift cluster nodes, the Cockpit console access is required. For this purpose, the ONP has two interfaces.

* onp1
* onp2

Both the interface can be added directly from the virtual machine console. Here are the steps to achieve that.

<figure><img src="../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

By default, the DHCP server for the additional interface will be turned off. To start and manage the service, the below command will be useful.

#### Check the service

```
onp services
```

#### Start the service

```
sudo systemctl start onp1-dhcp
```

#### Check the logs

```
journalctl -f -u dhcp
```
