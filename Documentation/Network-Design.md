# Network Design

## Business Scenario

A growing organization requires a secure and scalable enterprise campus network capable of supporting employee workstations, IP phones, wireless devices, and Internet connectivity. This project demonstrates the design and implementation of a Cisco-based campus network using industry best practices for segmentation, management, and verification.

The design provides a solid networking foundation that can be expanded in future projects with dynamic routing protocols such as OSPF, EIGRP, and BGP.

## Project Overview

The Enterprise Campus Network Foundation lab establishes the core infrastructure of a small enterprise network using Cisco routing and switching technologies. The objective is to create a stable, scalable campus network that supports data, voice, wireless, and Internet connectivity while following enterprise networking best practices.

---

## Objectives

- Build a functional enterprise campus network
- Configure Layer 2 switching
- Configure Layer 3 routing
- Implement VLAN segmentation
- Support voice and wireless devices
- Provide Internet connectivity through an ISP
- Verify end-to-end network communication

---

## Network Topology

The lab consists of:

- Cisco 2901 Router (FSNA-RTR)
- Cisco Catalyst 2960 Switch (FSNA-SW1)
- Cisco Catalyst 2960 Switch (FSNA-SW2)
- Wireless Access Point
- User Workstations
- IP Phones
- ISP Connection
- PSTN Simulation

---

## VLAN Design

| VLAN | Name | Network | Purpose |
|------|------|---------|---------|
|100|Management|192.168.100.0/24|Network Device Management|
|120|Data|192.168.200.0/24|User Devices|
|150|Voice|192.168.150.0/24|IP Telephony|

---

## Design Highlights

- Hierarchical campus design
- VLAN segmentation for security and performance
- Separate management network
- Voice traffic isolated from user data
- Wireless connectivity integrated into the campus network
- Internet access through an upstream ISP
- PSTN connectivity for IP telephony demonstration

## Design Principles

The network was designed using several enterprise networking principles:

- Hierarchical campus architecture
- Logical VLAN segmentation
- Separate management network
- Scalable Layer 2 switching
- Centralized Layer 3 routing
- Structured documentation
- Simplified troubleshooting and verification
---

## Topology Diagram

Refer to **enterprise-campus-topology.png** located in the repository root.
