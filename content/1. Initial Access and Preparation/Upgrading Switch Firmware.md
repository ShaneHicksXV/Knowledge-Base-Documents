# Cisco Switch Firmware Upgrade 

Upgrading the firmware on a Cisco switch helps keep it secure and working properly. Before you start, make sure you know the exact switch model and have the correct firmware file. 
## Steps 

1. Save the current configuration. 
2. Check the current version with `show version`. 
3. Back up the configuration. 
4. Download the correct firmware from Cisco. 
5. Copy the firmware file to the switch flash memory. 
6. Set the switch to boot from the new image. 
7. Save the changes. 
8. Reload the switch. 
9. Check the version again after it comes back up. 
## Useful Commands 

	show version 
	copy running-config startup-config 
	dir flash: copy tftp: flash: 
	show boot reload
## Notes 

- Make sure there is enough space in flash. 
- Do the upgrade during a maintenance window. 
- Keep a backup in case you need to roll back. 
- Verify the switch is working normally after the reboot.