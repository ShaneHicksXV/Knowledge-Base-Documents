# Port and Interface Configuration

![Putty Software](assets/putty-icon.png)

Putty will be the main software used to start with the configuration of your switch.

## Why port setup matters

Ports are the connection points between the switch and the rest of the network, so they deserve careful attention. When a switch is configured properly, each interface has a clear purpose. Some ports connect to desktop computers, some to printers, and others to access points or other switches. If every port is treated the same way, troubleshooting becomes much harder later. A good administrator pays attention to speed, duplex, shutdown state, and interface description because those details affect both performance and clarity.

## Common tasks

Basic port configuration usually includes turning a port on or off, labeling it with a description, and deciding whether it should be used as an access port or uplink. If a port is unused, it is often better to disable it rather than leave it open. That small step improves organization and reduces risk. A description also helps anyone who looks at the switch later understand what is connected without tracing every cable by hand.

### Example workflow
- Check interface status.
- Add a useful description.
- Enable the port if needed.
- Disable unused ports.
- Verify the result after the change.

#### Practical example

A port that connects to a classroom PC might be labeled by room and desk number, while an uplink port might be labeled for the next switch in the chain. That kind of naming makes the whole system easier to manage.

For additional help with commands for numerous switches in the command line interface, please refer to the following document for details [Command line Cheat Sheet](assets/command-line-cheat-sheet.pdf)

## Related notes

This page links naturally to [Network Security Controls](5.%20Network%20Security%20Controls/index.md) and [Verification & Configuration Management](6.%20Verification%20and%20Configuration%20Management/index.md).