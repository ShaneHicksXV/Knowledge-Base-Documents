# Commands 
## Get into privileged mode

	enable 
## Enter global configuration mode

	configure terminal 
## Set the hostname 
	
	hostname SW1 
## Add a banner message 

	banner motd #Unauthorized access is prohibited# 
## Set the enable secret password

	enable secret StrongPassword123 
## Set the console password

	line console 0 
	password ConsolePass123 
	login 
	exit 
## Set the VTY password for remote access

	line vty 0 4 
	password VTYPass123 
	login 
	exit 
## Set the switch management IP 

	interface vlan 1 
	ip address 192.168.1.2 255.255.255.0 
	no shutdown 
	exit 
## Set the default gateway

	ip default-gateway 192.168.1.1 
## Set the time 
	
	clock set 20:00:00 Jul 20 2026 
## Save the setup 
	
	copy running-config startup-config