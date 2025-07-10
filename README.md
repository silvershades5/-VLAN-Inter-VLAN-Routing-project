# VLAN & Inter-VLAN Routing (Router-on-a-Stick)

This project demonstrates how to configure VLANs and enable inter-VLAN communication using a router-on-a-stick setup in Cisco Packet Tracer.

## 🧠 Technologies
- Cisco Packet Tracer
- VLAN Configuration
- 802.1Q Trunking
- Subinterfaces on Router
- Access & Trunk ports

## 🧱 Topology Overview
![Topology Diagram](vlan_topology.png)

## ⚙️ Switch Configuration
```bash
enable
conf t

vlan 10
name HR
exit

vlan 20
name SALES
exit

interface range fa0/1 - 2
switchport mode access
switchport access vlan 10
exit

interface range fa0/3 - 4
switchport mode access
switchport access vlan 20
exit

interface fa0/5
switchport mode trunk
exit
