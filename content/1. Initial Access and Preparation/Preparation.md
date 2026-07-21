## Related Categories

After the completion of the steps below click on this link to continue [[Access|Accessing Command Line for Initial Configuration]]

### Network Switch 

![Front view of a network switch with labeled ports](images/network-switch.png)

This picture shows the front panel of a switch and helps identify the ports used for management and uplinks.

# Initial Access and Preparation

## Getting connected to the switch

Before you can configure a switch, you need a reliable way to access it. In many labs, that starts with a console cable and a terminal program. In a live environment, you may use SSH once the management interface is configured. Console access is helpful when the switch is new, reset, or misconfigured. SSH is better for everyday administration because it allows secure remote work. The important thing is to know which access method fits the situation and to avoid guessing when the device is on the line.

## What to check first

Preparation makes switch administration much safer. Before changing anything, review the current hostname, firmware, IP settings, and interface status. It also helps to note whether the switch is standalone, stacked, or connected to other switches. If you start without that information, you may accidentally change the wrong device or disrupt an active connection. A few minutes of preparation can prevent hours of repair.

### Preparation checklist

1. Confirm physical access.
2. Identify the switch model.
3. Record the current configuration.
4. Check whether a management IP already exists.
5. Decide what needs to be changed first.

## Smooth transition to configuration

Once access is stable and the device has been identified, you are ready to move into the more practical work of [Network Segmentation (VLANs)](What%20are%20Vlans%20and%20How%20They%20Work.md) and [Port & Interface Configuration](Configuration%20Interfaces.md). That progression keeps the process organized and easier to learn.