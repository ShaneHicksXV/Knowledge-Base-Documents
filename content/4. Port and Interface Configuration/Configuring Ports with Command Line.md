# Port Configuration CLI 
## 1. Go into configuration mode configure terminal 
## 2. Configure an access port for one VLAN interface 

	fastethernet 0/1 
	switchport mode access 
	switchport access vlan 10 
	no shutdown 
	exit 
## 3. Configure a trunk port for multiple VLANs interface 

	fastethernet 0/24 
	switchport mode trunk 
	switchport trunk allowed vlan 10,20 
	switchport trunk native vlan 99 
	no shutdown 
	exit 
## 4. Optional port settings speed auto duplex auto 
## 5. Save the configuration copy running-config startup-config 
## 6. Verify the port show interfaces status show vlan brief show interfaces trunk