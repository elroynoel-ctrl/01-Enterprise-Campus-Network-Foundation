# Configuration Guide

## Overview

This document outlines the configuration performed during the Enterprise Campus Network Foundation lab. The objective was to build a functional enterprise network supporting data, voice, wireless, and Internet connectivity using Cisco networking devices.

---

## Devices Configured

| Device | Purpose |
|---------|---------|
| Cisco 2901 Router (FSNA-RTR) | Layer 3 routing and Internet connectivity |
| Cisco Catalyst 2960 Switch (FSNA-SW1) | Core access switch |
| Cisco Catalyst 2960 Switch (FSNA-SW2) | Access layer switch |
| Wireless Access Point | Wireless client connectivity |
| Cisco 7960 IP Phones | Voice network simulation |

---
## Configuration Workflow

The Enterprise Campus Network Foundation lab was implemented using the following workflow:

1. Configure the router with hostname, interface addressing, and routing.
2. Configure both switches with management settings and VLANs.
3. Configure access ports and trunk links.
4. Connect end devices, IP phones, and the wireless access point.
5. Verify Layer 2 and Layer 3 connectivity.
6. Perform end-to-end testing using Cisco IOS verification commands.
7. Save all device configurations.

---

## Router Configuration

The Cisco 2901 router was configured to provide Layer 3 connectivity between the enterprise network and the simulated ISP while following Cisco IOS configuration best practices.

### Initial Configuration

The following baseline configuration was completed:

- Configure hostname
- Configure enable secret
- Configure console access
- Configure VTY access
- Enable password encryption
- Configure Message of the Day (MOTD) banner

### Interface Configuration

The router interfaces were configured to establish connectivity with the campus network and upstream ISP.

Tasks completed:

- Assign IPv4 addresses
- Configure subnet masks
- Enable interfaces using:

```bash
no shutdown
```
---

- Verify interface status

### Routing Configuration

Routing was configured to provide connectivity between local networks and the simulated Internet.

Tasks completed:

- Configure default route
- Verify routing table
- Save configuration to startup-config

---

## Switch Configuration

Both Cisco Catalyst 2960 switches provide Layer 2 connectivity throughout the enterprise campus.

### Initial Configuration

Each switch received the following baseline configuration:

- Configure hostname
- Configure management VLAN
- Configure management IP address
- Configure default gateway

### Layer 2 Configuration

The switching infrastructure was configured to support network segmentation and inter-switch communication.

Tasks completed:

- Create VLANs
- Configure access ports
- Configure trunk links
- Assign interfaces to the appropriate VLANs

### Management Configuration

Remote and local management access was configured by:

- Configuring console access
- Configuring VTY access
- Enabling password encryption
- Saving the running configuration

Configuration was verified using:

```bash
show running-config
show vlan brief
show interfaces trunk
```
---

## VLAN Configuration

| VLAN | Name | Purpose |
|------|------|---------|
|100|Management|Network device management|
|120|Data|User devices|
|150|Voice|Cisco IP Phones|

## Verification Commands

The following Cisco IOS commands were used throughout the implementation to verify that the network was configured correctly and operating as expected.

```bash
show ip interface brief
show vlan brief
show interfaces trunk
show running-config
show mac address-table
ping
```

These commands verified:

- Interface operational status
- VLAN creation and port assignments
- Trunk link operation
- Device configuration
- MAC address learning
- End-to-end network connectivity
