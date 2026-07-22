# Network Switch Administration Troubleshooting 

A simple guide for checking common switch issues without overcomplicating it. 
## Start here

- Make sure the switch is powered on and reachable. 
- Check whether you can log in through SSH. 
- Confirm the management IP address is correct. 
### Useful commands

	ping <switch-ip> 
	ssh <user>@<switch-ip> 
	show version 
	show ip interface brief
## Check the ports

- Look for ports that are down, flapping, or showing errors. 
- Make sure the cable and device on the other end are okay. 
- Check for speed or duplex mismatches. 
### Useful commands

	show interfaces status 
	show interfaces counters errors 
	show interfaces <port> 
	show interface description
## Check VLANs and trunking

- Confirm the port is in the right VLAN. 
- Make sure trunk links allow the correct VLANs. 
- If traffic is not passing, VLAN settings are a common problem. 
### Useful commands

	show vlan brief 
	show interfaces trunk 
	show interfaces <port> switchport
## Check neighbors

- See what is connected to the switch. 
- This helps when a port is connected to another switch or a device you do not recognize. 
### Useful commands

	show cdp neighbors 
	show cdp neighbors detail 
	show lldp neighbors 
## Check MAC learning

- If a device is connected but not working, see whether the switch is learning its MAC address. 
- This can help you find the exact port a device is using. 
### Useful commands

	show mac address-table 
	show mac address-table dynamic 
	show mac address-table vlan <vlan-id> 
## Check logs

- Look at the logs for errors, reboots, link changes, or other clues. 
- Logs often show what happened right before the problem started. 
### Useful commands

	show logging 
	show running-config 
	show running-config interface <port> 
## Quick checklist

- Can you reach the switch? 
- Is the management interface up? 
- Is the port up and error-free? 
- Is the VLAN correct? 
- Is the trunk passing the right VLANs? 
- Does the switch see the connected device? 
## Simple rule If you are stuck, start with

	show ip interface brief 

then check the port, VLAN, MAC table, and logs.