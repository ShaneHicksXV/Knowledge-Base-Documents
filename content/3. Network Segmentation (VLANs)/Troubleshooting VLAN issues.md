A simple guide for checking VLAN problems without making it harder than it needs to be. 
## Start with the VLAN itself

- Make sure the VLAN exists. 
- Check that the VLAN is active. 
- Confirm the VLAN name and ID are correct. 
### Useful commands

	show vlan brief 
	show vlan 
	show vlan id <vlan-id>
## Check the access port 

- Make sure the port is assigned to the right VLAN. 
- Confirm the port is not shut down. 
- Verify the device connected to the port is actually using that VLAN. 
### Useful commands 

	show interfaces <port> switchport 
	show interfaces status 
	show running-config interface <port>
## Check trunk links 

- If VLAN traffic crosses switches, the trunk has to allow that VLAN. 
- Make sure both sides of the trunk match. 
- Check the native VLAN if traffic is acting strange. 
### Useful commands 
	
	show interfaces trunk 
	show interfaces <port> switchport 
	show running-config interface <port>
## Check Layer 3 VLANs 

- If devices in the same VLAN cannot reach the gateway, check the SVI. 
- If inter-VLAN routing is failing, make sure the VLAN interface is up. 
- Confirm the IP address and mask are correct. 
### Useful commands 

	show ip interface brief 
	show interfaces vlan <vlan-id> 
	show running-config interface vlan <vlan-id> 
## Check MAC learning 

- If a device is connected but traffic is not passing, check whether the switch sees its MAC address. 
- This helps confirm the switch is learning devices on the right VLAN. 
### Useful commands 
	show mac address-table 
	show mac address-table vlan <vlan-id> 
	show mac address-table interface <port>
## Check logs 

- Logs can show trunk changes, VLAN changes, or interface problems. 
- If the issue started suddenly, logs are usually worth checking. 
### Useful commands 

	show logging 
	show spanning-tree vlan <vlan-id>
## Quick checklist 

- Does the VLAN exist? 
- Is the access port in the right VLAN? 
- Is the trunk allowing that VLAN? 
- Is the SVI up if routing is involved? 
- Is the switch learning MAC addresses on that VLAN? 
## Simple rule 

If VLAN traffic is broken, check the VLAN, the port, the trunk, and the SVI in that order.