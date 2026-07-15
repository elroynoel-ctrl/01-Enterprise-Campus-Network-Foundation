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

## Router Configuration

The Cisco 2901 router was configured with:

- Hostname
- Interface IP addressing
- Default routing
- Management access
- Secure passwords
- Configuration saved to startup-config

---

## Switch Configuration

Both Catalyst 2960 switches were configured with:

- Hostname
- Management VLAN
- Access ports
- Trunk links
- Default gateway
- Console and VTY access
- Password encryption

---

## VLAN Configuration

| VLAN | Name | Purpose |
|------|------|---------|
| 100 | Management | Network device management |
| 120 | Data | User devices |
| 150 | Voice | Cisco IP Phones |

---

## End Devices

The following devices were successfully connected and tested:

- Desktop PCs
- Tablet
- Wireless Access Point
- Cisco IP Phones

---

## Configuration Files

Complete device configurations are available in the **Configs** folder.

- FSNA-RTR.txt
- FSNA-SW1.txt
- FSNA-SW2.txt
