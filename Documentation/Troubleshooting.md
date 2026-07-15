# Troubleshooting

## Overview

This document outlines common issues that may occur during the deployment of the Enterprise Campus Network Foundation lab. While not every issue was encountered during implementation, each scenario represents a common enterprise networking problem along with the recommended verification and resolution steps.

---

## Issue 1 — The interface was administratively disabled.

### Symptom

A router or switch interface showed:

```
administratively down
```

### Cause

Interface was disabled.

### Resolution

Enabled the interface.

```bash
interface GigabitEthernet0/0
 no shutdown
```

Verified using:

```bash
show ip interface brief
```

---

## Issue 2 — VLAN Connectivity Failure

### Symptom

Hosts could not communicate within their assigned VLAN.

### Cause

One or more switch ports were assigned to the incorrect VLAN.

### Resolution

Verified VLAN membership.

```bash
show vlan brief
```

Assigned interfaces to the correct VLAN.

---

## Issue 3 — The trunk configuration differed btween the connected switches.

### Symptom

Devices connected to different switches could not communicate.

### Cause

Trunk configuration mismatch.

### Resolution

Verified trunk operation.

```bash
show interfaces trunk
```

Confirmed trunk encapsulation and allowed VLANs.

---

## Issue 4 — Management Access Failure

### Symptom

Unable to access the management interface.

### Cause

The management IP address or default gateway was configured incorreclty.

### Resolution

Verified:

- Management VLAN
- Switch IP address
- Default gateway configuration

---

## Issue 5 — End Device Connectivity

### Symptom

A workstation could not reach its gateway.

### Cause

The end device was configured with incorrect IP addressing information.

### Resolution

Verified:

- IP address
- Subnet mask
- Default gateway

Performed connectivity testing using:

```bash
ping
```
---

## Issue 6 — Duplicate IP Address

### Symptom

- A workstation experienced intermittent connectivity.
- The device could not consistently communicate with its default gateway.
- Another host on the network unexpectedly lost connectivity.

### Cause
- Two devices were configured with the same IPv4 address, causing an IP address conflict on the network.

### Resolution
- Verified the IP addressing of affected devices.
- Assigned a unique IPv4 address to the conflicting device.
- Confirmed the correct subnet mask and default gateway configuration.

### Verification
```bash
show arp
ping <default-gateway>
```
### Expected Result
- Each device has a unique IP address.
- Connectivity to the default gateway is restored.
- Network communication is stable.

## Issue 7 — Native VLAN Mismatch

### Symptom
- Devices connected through trunk links could not communicate correctly.
- Some VLAN traffic failed to pass between switches.
- Cisco Discovery Protocol (CDP) displayed a native VLAN mismatch warning.

### Cause
- The native VLAN configured on one end of the trunk link did not match the native VLAN configured on the opposite switch.

### Resolution
- Verified the trunk configuration on both switches.
- Configured the same native VLAN on each side of the trunk.
- Confirmed that the required VLANs were allowed across the trunk link.

### Verification 

```bash
show interfaces trunk
show running-config interface GigabitEthernet0/1
```

### Expected Result
- Trunk ports are operational.
- Native VLANs match on both switches.
- VLAN traffic passes successfully across the trunk link.

---

## Troubleshooting Methodology

The following approach was used throughout the project:

1. Verify physical connectivity.
2. Check interface status.
3. Verify IP addressing.
4. Verify VLAN membership.
5. Verify trunk links.
6. Check routing.
7. Test connectivity using ping.
8. Review the running configuration.

---

## Outcome

All identified issues were resolved through systematic troubleshooting using Cisco IOS verification commands.

This structured troubleshooting methodology provides a repeatable process for diagnosing and resolving common enterprise campus networking issues.

The final network successfully supported:

- Data connectivity
- Voice VLAN communication
- Wireless access
- Management network access
- Internet connectivity
- End-to-end network communication

The troubleshooting scenarios documented in this guide provide a practical reference for identifying and resolving common issues encountered in Cisco enterprise campus networks.
