Leaf-2 and Spine are all preconfigured
Please find all necesaary info at th lab1.png 

## Exercise-1

# The Goal: Make necesary configs at Leaf1 so as to make it able to ping Host2 (10.10.10.3) from Host1

# Verification: run "make pingtest"

# Steps:

At Leaf-1 Configure:

The Interfaces for
	Access (tagged with vlan 100)
	ISL 
	system 
PrefixSet and Policies for BGP
Tunnel Interface to handle vxlan with vni 100
Mac-VRF (evi 100)
Default Network Instance


## Exercise-2

# The Goal: Change Host1-Leaf1 link to untagged and make it possible to ping Host2 (10.10.10.3) from Host1)

# Tip: The commands for Host1 can be found by running "make help"

# Verification: run "make pingtest"

# Steps:

Tag the interface at Host1
Tag the interface at Leaf1


## Exercise-3

# The Goal: Change Host1-Leaf1 link to tagged by vlan 200 
Now you need sonme extra configgs to make it possible to ping Host2 (10.10.10.3) from Host1)

# Tip: The commands for Host1 can be found by running "make help"

# Verification: run "make pingtest"

# Steps:

At both Leaf1 and Leaf2
Create an IRB intf
Create a routed vxlan
Create IP-VRF








