# ACL and Security Commands 
## 1. Enter configuration mode

	enable 
	configure terminal 
## 2. Create a standard ACL 

	access-list 10 permit 192.168.1.0 0.0.0.255 
	access-list 10 deny any 
## 3. Apply the ACL to an interface 

	interface gigabitEthernet 0/1 
	ip access-group 10 in 
	exit 
## 4. Add basic device security 

	enable secret StrongPassword123 
	service password-encryption 
	line console 0 
	password ConsolePass123 
	login 
	exit 
	
	line vty 0 4 
	password VTYPass123 
	login 
	exit 
## 5. Save the configuration

	copy running-config startup-config 
## 6. Verify the ACL and security

	show access-lists 
	show ip interface gigabitEthernet 0/1 
	show running-config