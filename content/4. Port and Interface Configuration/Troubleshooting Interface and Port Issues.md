A simple guide for figuring out why a switch port or interface is not working right. 
## Start with the port status 

- Check whether the port is up, down, or disabled. 
- Look for admin shutdown, err-disabled, or link flaps. 
- Make sure the device on the other end is powered on. 
### Useful commands 

	show interfaces status 
	show ip interface brief show interfaces <port> 
## Check for errors 

- Error counters can point to bad cables, bad optics, or speed/duplex mismatches. 
- CRC errors, runts, giants, and collisions are all worth checking. 
- A high error count usually means there is a physical or negotiation problem. 
### Useful commands 

	show interfaces <port> counters errors 
	show interfaces <port> show logging 
## Check speed and duplex 

- Both sides of the link should match when possible. 
- A mismatch can cause slow traffic or lots of errors. 
- This is one of the most common port problems. 
### Useful commands 

	show interfaces <port> status 
	show running-config interface <port>
## Check shutdown and err-disabled states 

- A port may look fine at first but still be shut down in the config. 
- Err-disabled usually means the switch protected itself after detecting a problem. 
- Common causes include port security, BPDU guard, and link flaps. 
### Useful commands 

	show interfaces status err-disabled 
	show logging show running-config interface <port>
## Check cabling and neighbors 

- If the link is down, start with the cable and the device on the other end. 
- If it connects to another switch, check the neighbor details. 
- This helps confirm you are looking at the right port and device. 
### Useful commands 

	show cdp neighbors detail 
	show lldp neighbors detail 
	show interfaces <port> switchport
## Check traffic and MAC learning 

- If the port is up but traffic is not passing, see whether the switch is learning MAC addresses. 
- If no MAC address appears, the device may not be sending traffic. 
- If MACs show up on the wrong port, something is miswired or misconfigured. 
### Useful commands 

	show mac address-table 
	show mac address-table interface <port> 
	show mac address-table vlan <vlan-id>
## Quick checklist - Is the port up? 

- Is the port shut down or err-disabled? 
- Are there interface errors? - Do speed and duplex match? 
- Is the cable or device bad? 
- Is the switch learning MAC addresses? 
## Simple rule If a port is acting up, check status, errors, config, and logs in that order.