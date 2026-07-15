# Troubleshooting

## Overview

This document outlines common issues that may occur during deployment of the Enterprise Campus Network Foundation lab and the methods used to identify and resolve them.

---

## Issue 1 — Interface Down

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

Incorrect VLAN assignment.

### Resolution

Verified VLAN membership.

```bash
show vlan brief
```

Assigned interfaces to the correct VLAN.

---

## Issue 3 — Trunk Link Not Passing Traffic

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

Incorrect management IP address or default gateway.

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

Incorrect IP configuration.

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

The final network successfully supported:

- Data connectivity
- Voice VLAN communication
- Wireless access
- Management network access
- Internet connectivity
