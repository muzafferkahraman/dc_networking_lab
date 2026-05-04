## LAB1

This Lab intends to facilitate an environment to help gain insights and practice of configuring 
services with bgp-evpn for a datacenter, with SRLinux.

The Lab Topology is below
<br>
![](lab1.png)
<br>
**After cloning the repo with**
> git clone https://github.com/muzafferkahraman/dc_networking_lab

**Deploy the Lab**
> make deploy 
## Exercise-1
The Goal: Make necesary configs at Leaf1 and Leaf2 so as to make it possible to ping the IP addresses from the same MACVRF
ie
ping 10.0.0.3 from Host1
ping 10.0.1.3 from Host2
<br>
**Verification:** run "make verify_macvrf"<br>
**Hint for Steps:**<br>
At Leaf1 and Leaf2 Configure: <br>
The Interfaces for  Access (tagged with vlans),  ISL, system <br>
PrefixSet and Policies for BGP<br>
Tunnel Interface to handle vxlan with vnis<br>
Default Network Instance<br>
Mac-VRFs<br>
<br>

## Exercise-2
The Goal: Make necesary configs at Leaf1 and Leaf2 so as to make it possible to ping the IP addresses from the different MACVRF
ie
ping 10.0.1.3 from Host1
ping 10.0.0.3 from Host2
<br>
**Verification:** run "make verify_ipvrf"<br>
**Hint for Steps:**<br>
At Leaf1 and Leaf2 Configure:<br>
Irb interfaces<br>
Tunnel Interface to handle vxlan with vnis<br>
IP-VRFs<br>


## Exercise-3
The Goal: Make necesary configs at Border Leaf so as to make it possible to ping the routed host address 10.10.0.2  from the hosts of the Leaf1 and Leaf2
ie
ping 10.10.0.2 from Host1
ping 10.10.0.2 from Host2
<br>
**Verification:** run "make verify_routed"<br>
**Hint for Steps:** (*Configs not stated here, are already provisioned)<br>
At Border Leaf Configure:<br>
The Interfaces for  Access (routed inteface to Host5) <br>
Tunnel Interface to handle vxlan with vnis<br>
IP-VRFs<br>


