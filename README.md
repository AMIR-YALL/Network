# Enterprise Network Design with High Availability (Cisco Packet Tracer)

## 📌 Project Overview
This project demonstrates the design and configuration of a resilient enterprise network topology using Cisco Packet Tracer. The primary goal is to ensure high availability, redundancy, and efficient traffic flow across the network using industry-standard routing and switching protocols.

## 🏗️ Network Topology
The network follows a hierarchical design model:
- **Core Layer:** Edge Router connecting to the ISP/Internet.
- **Distribution Layer:** Two Multilayer Switches (MLS) providing Inter-VLAN routing and Gateway Redundancy.
- **Access Layer:** Access switches connecting end-user devices (PCs, Laptops).
- **Redundancy:** Redundant links between Distribution and Access layers to prevent single points of failure.

## ⚙️ Technologies & Protocols Implemented

| Technology | Description |
| :--- | :--- |
| **OSPF** | Dynamic routing protocol used in the Core layer to exchange routes between the edge router and distribution switches. |
| **HSRP** | Hot Standby Router Protocol configured on Distribution Switches to provide a virtual gateway IP for end-users, ensuring seamless failover. |
| **VLANs** | Network segmentation using VLAN 10 (e.g., Sales/IT) and VLAN 20 (e.g., HR/Finance) to reduce broadcast domains and improve security. |
| **802.1Q Trunking** | Configured on uplinks between switches to carry traffic for multiple VLANs. |
| **Rapid-PVST** | Rapid Per-VLAN Spanning Tree Protocol used to prevent Layer 2 loops and ensure fast convergence. |
| **STP Load Balancing** | Tuned STP priorities on switches to load balance traffic between VLANs (e.g., one switch is root for VLAN 10, the other for VLAN 20). |
| **SVI (Switch Virtual Interface)** | Used on Multilayer Switches for Inter-VLAN routing. |
