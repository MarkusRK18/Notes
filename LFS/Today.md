Start From Linux From Scratch 

1. Installation of Qemu 
```
sudo pacman -S qemu-desktop
```

2. Enable KVM Acceleration

Ensure your user account has permission to use hardware acceleration via KVM
```
sudo usermod -aG kvm $USER
```

Verfiy KVM is active 
```
lsmod | grep kvm
kvm_intel             532480  0
kvm                  1490944  1 kvm_intel
irqbypass              16384  1 kvm
```

3. Install VirtIO Drivers (Highly Recommended)

VirtIO drivers allow your guest operating system to communicate directly with your physical hardware, bypassing slow emulation.

```
yay -S virtio-win
```

4. Install Virt-Manager (Highly Recommended GUI)

Virt-Manager provides a graphical interface similar to VirtualBox. It handles storage creation, networking, and ISO mounting automatically.

```
sudo pacman -S virt-manager libvirt dnsmasq iptables-nft
```

To start and enable the service :
```
sudo systemctl enable --now libvirtd
```


And the Launch the ```
```
Virt-manager
```

Screenshot 
![[Pasted image 20260825103605.png]]

# Installation of Arch Base For Linux From Scratch

### Step 1

1. Download the Arch linux ISO for the https://archlinux.org/download/
### Step 2
1. Now going to  Create the New Virtual Machine in that going to attach the arch linux iso file 
2. Open the Qemu Emulator 
3. Click the file the left side in that click the New Virtual machine option click that 
**Screenshot 
![[Pasted image 20260825104141.png]]

![[Pasted image 20260825104214.png]]

![[Pasted image 20260825104334.png]]

![[Pasted image 20260825104838.png]]

![[Pasted image 20260825104848.png]]