#ICT40120 #ICTNWK420 #VirtualMachine #Networking #Scott #info

---

## The virtual Environment

The virtual environment is very simple but incredibly important to understand. We'll cover some basics here.

A "host" is a physical machine and a "guest" is the name given to a virtual machine, that resides inside of the host. A single host can have many virtual machines, depending on the resources available. 

The software that provides the host environment is called a "hypervisor", of which there are two types:

Type 1 - Also called bare metal hypervisors, they don't need any other operating system to run on. Examples of this are [VMware ESXi](https://www.vmware.com/au/products/esxi-and-esx.html) and [ProxMox](https://www.proxmox.com/en/proxmox-ve).

[Type 2](Type%202%20virtual%20machines.md) - Runs as an application inside of another operating system, and the application hosts its virtual machines. Examples include [VMware Workstation](https://www.vmware.com/au/products/workstation-pro.html) and [Virtual Box](https://www.virtualbox.org/) 

There are also cloud based options such as Azure and AWS.

## Virtual Networking

There are three types of virtual adapters; [[#Bridged]], [[#Host-Only]] and [[#NAT]].

Generally, the virtual machines that we will use will only require a Host-Only adapter. 
Make sure to [disable DHCP](VMware%20network%20properties#disable%20dhcp) in the [[VMware network properties]].

### Bridged
This adapter is directly connected to the host's network adapter. It allows the guest to connect to the internet. The benefit of using a bridged adapter over a NAT adapter, is that the guest machine will act as a separate device on the network. 

### Host-Only
This virtual adapter only exists within the host machine, with no outside connections. Guests can connect to each other on the same Host-Only network, as well as the Host machine, however they cannot connect to anything outside the host machine. 

### NAT 
This adapter is very similar to the Bridged adapter. Using NAT separates the the virtual network from the LAN, in the same way that a router separates the LAN from the internet. 
For info regarding NAT networking, see [VirtualBox Docs](https://www.virtualbox.org/manual/ch06.html#nat-limitations)

#todo explain nat better

