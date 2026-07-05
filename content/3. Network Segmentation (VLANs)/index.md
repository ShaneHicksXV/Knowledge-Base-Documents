# Network Segmentation (VLANs)

![Network Segmentation Diagram](images/network-segmentation.png)

The diagram shows how a network is divided into smaller, isolated zones or segments.
## Why VLANs matter

VLANs, or Virtual Local Area Networks, are a simple but powerful way to divide one physical switch network into multiple logical networks. In basic device administration, VLANs help separate users, devices, and services so traffic stays organized and easier to manage. For example, student devices, staff devices, and printers can live in different VLANs even if they are plugged into the same switch hardware. That separation improves security, reduces unnecessary broadcast traffic, and makes troubleshooting cleaner. Instead of treating the switch like one large flat network, VLANs let you build a structure that matches how the organization actually works.

## How segmentation helps

Segmentation is useful because it limits how far traffic can spread. If one area of the network has a problem, VLANs can help contain it. They also make it easier to apply policy later, especially when you want different groups to have different access rules. In a lab environment, you may only need a few VLANs, but the same concept scales to larger networks. A well-planned VLAN structure makes the switch easier to understand and the network easier to support.

### Typical VLAN planning ideas
- Put similar devices in the same VLAN.
- Keep management traffic separate from user traffic.
- Use clear names that match the purpose of each VLAN.
- Document which ports belong to each VLAN.

## Basic configuration flow

The usual process starts by creating the VLAN, naming it, and then assigning ports to it. Access ports belong to one VLAN, while trunk ports carry multiple VLANs between switches. That distinction matters because it affects how traffic moves through the network. If you are building out a switch from scratch, VLAN planning should happen before port assignment so the configuration stays clean and consistent.

#### Example idea

A small office might have one VLAN for general users, one for guest devices, and one for network management. That setup is simple, but it already gives better control than a flat network.

## Related pages

This page connects to [Basic Device Administration](2.%20Basic%20Device%20Administration/index), [Port & Interface Configuration](4.%20Port%20and%20Interface%20Configuration/index), [index](5.%20Network%20Security%20Controls/index.md), and [Verification & Configuration Management](6.%20Verification%20and%20Configuration%20Management/index.md)