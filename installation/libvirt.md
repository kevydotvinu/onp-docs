# Libvirt

The Libvirt installation uses `virt-install` command. We can also use `virt-manger` GUI. Even after the installation is done through the `virt-install` command, we can use `virt-manager` to access the machine using the SSH connection.

## Download

```
curl -LO https://github.com/kevydotvinu/openshift-network-playground/releases/download/v0.1.0/onp-v0.1.0-x86_64.iso
```

## Installation

{% hint style="info" %}
**INFO**

This can be checked using the `virt-host-validate` command from the VM itself. The output of the command should provide `QEMU: Checking for hardware virtualization : PASS`.
{% endhint %}

{% hint style="danger" %}
**IMPORTANT**

The ISO boot will erase ALL the data on the `/dev/sda` disk and install OpenShift Network Playground automatically.
{% endhint %}

```bash
VM_NAME=onp
VCPU=18
MEMORY=73728
VM_DISK=./onp01.img,bus=scsi
NETWORK=network=macvtap-net,model=virtio
CDROM=./onp.iso

virsh destroy ${VM_NAME}
virsh undefine ${VM_NAME}
sudo qemu-img create ${VM_NAME}.img 360G
virt-install --name $VM_NAME \
        --os-variant fedora-coreos-stable \
        --vcpus $VCPU \
        --memory $MEMORY \
        --disk $VM_DISK \
        --network $NETWORK \
        --pxe \
        --cdrom $CDROM \
        --boot hd,cdrom \
        --filesystem type=mount,mode=mapped,source=/mnt,target=/mnt \
        --graphics spice,listen=0.0.0.0 \
        --video virtio \
        --channel spicevmc \
        --console pty,target.type=virtio \
        --serial pty \
        --noautoconsole

function WAIT_FOR_REBOOT {
sp='/-\|'
sc=0

spin() {
   printf "\r[${sp:sc++:1}] $1"
   ((sc==${#sp})) && sc=0
}

endspin() {
   printf "\r%s\n" "$@"
}

until [[ $(sudo virsh -q list | grep -o ${VM_NAME} | wc -c) -eq 0 ]]
do spin "Waiting for the installation and restart ..."
sleep 0.5
done
endspin
}

function START_NODE {
        sudo virsh start ${VM_NAME} > /dev/null
        echo "[✔] Installation completed!"
}

WAIT_FOR_REBOOT
START_NODE
```
