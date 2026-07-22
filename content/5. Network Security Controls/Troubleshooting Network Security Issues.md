A simple guide for finding common security problems without making it complicated. 
## Start with the basics 

- Confirm what is being blocked or allowed. 
- Figure out whether the issue is with a user, device, VLAN, firewall, or ACL. 
- Check whether the problem started after a config change. 
### Useful commands 

	show running-config 
	show access-lists 
	show ip interface brief 
	show logging 
## Check access control lists 

- ACLs can block traffic even when everything else looks fine. 
- Look for deny rules that match the traffic you are testing. 
- Check whether counters are increasing on the rule. 
### Useful commands 

	show access-lists 
	show ip access-lists 
	show running-config | include access-group 
## Check firewall rules 

- Make sure the firewall policy allows the traffic you expect. 
- Verify source, destination, port, and protocol. 
- If traffic works in one direction but not the other, check stateful rules. 
### Useful commands 

	show firewall 
	show policy 
	show session
## Check authentication and authorization 

- If users cannot log in, the problem may be with AAA, RADIUS, or TACACS+. 
- Confirm the user account exists and is not locked out. 
- Check whether the device can reach the authentication server. 
### Useful commands 

	show aaa servers 
	show authentication sessions 
	show running-config | include aaa 
## Check port security and blocking features 

- Port security can shut a port down or restrict devices. 
- Security features like BPDU guard, DHCP snooping, or storm control can also block traffic. 
- Review logs when a port suddenly stops working. 
### Useful commands 

	show port-security 
	show port-security interface <port> 
	show logging
## Check traffic and logs 

- Logs often show what was denied and why. 
- If the issue is active, packet counters can help confirm where traffic is stopping. 
- Look for repeated denies, failed logins, or unusual access attempts. 
### Useful commands 

	show logging 
	show access-lists 
	show interfaces
## Quick checklist 

- Is the traffic being blocked by an ACL or firewall rule? 
- Is the user failing authentication? 
- Did a security policy change recently? 
- Is port security or another protection feature involved? 
- Do the logs show denies or failures? 
## Simple rule If it looks like a security issue, check the rules, the logs, and the counters first.