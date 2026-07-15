
# Verification

## Overview

After completing the configuration, the network was verified to ensure all devices communicated successfully and the intended network design was operating correctly.

---

## Router Verification

### Verify Interface Status

```bash
show ip interface brief
```

**Expected Result**

- All configured interfaces are **up/up**
- Correct IP addresses are assigned
- No interfaces are administratively down

---

### Verify Routing Table

```bash
show ip route
```

**Expected Result**

- Connected networks are present
- Static routes (if configured) appear in the routing table
- Default route is installed

---

### Verify Running Configuration

```bash
show running-config
```

**Expected Result**

- Interfaces configured correctly
- Hostname configured
- Security settings present
- Management configuration verified

---

## Switch Verification

### Verify VLANs

```bash
show vlan brief
```

**Expected Result**

- VLAN 100 – Management
- VLAN 200 – Data
- VLAN 150 – Voice
- Correct access ports assigned

---

### Verify Trunk Links

```bash
show interfaces trunk
```

**Expected Result**

- Trunk ports operational
- Required VLANs allowed across the trunk

---

### Verify Interface Status

```bash
show interfaces status
```

**Expected Result**

- Active interfaces connected
- Speed and duplex negotiated correctly

---

## Connectivity Testing

### Ping Gateway

```bash
ping <default-gateway>
```

**Expected Result**

Successful replies received.

---

### End-to-End Connectivity

Verified communication between:

- User PCs
- Wireless devices
- Router
- Switch management interfaces

All devices successfully communicated without packet loss.

---

## Internet Connectivity

Verified connectivity through the simulated ISP router.

---

## Voice Network

Verified IP Phones received network connectivity through the Voice VLAN.

---

## Result

✅ All verification tests completed successfully.

Verification Item	                      Status
Router Interfaces                       	✅
Switch Interfaces                       	✅
VLAN 100	                                ✅
VLAN 150	                                ✅
VLAN 200	                                ✅
Trunk Links	                              ✅
End-to-End Ping	                          ✅
Wireless Connectivity	                    ✅
Internet Connectivity	                    ✅

The Enterprise Campus Network Foundation lab met all design objectives and provided stable connectivity for data, voice, wireless, and management services.
