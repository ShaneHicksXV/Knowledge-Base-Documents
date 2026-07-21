# Basic VLAN Configuration 
## 1. Create the VLAN 

	configure terminal 
	vlan 10 
	name Dummy Vlan 
	exit 
## 2. Put a port in that VLAN 

	interface fa0/1 
	switchport mode access 
	switchport access vlan 10 
	exit  
## 3. If the VLAN must cross switches, make the uplink a trunk

	 interface fa0/24 
	 switchport mode trunk 
	 switchport trunk allowed vlan 10 
	 exit
## 4. Add a management IP if needed

	interface vlan 10 
	ip address 192.168.10.1 255.255.255.0 
	no shutdown exit 
## 5. Set the default gateway if the switch needs to reach other networks 

	ip default-gateway 192.168.10.254 
## 6. Save the config

	copy running-config startup-config 
## 7. Verify everything 

	show vlan brief 
	show interfaces trunk 
	show ip interface brief