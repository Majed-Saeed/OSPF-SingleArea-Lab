# OSPF Single Area Configuration – Cisco Packet Tracer

## Overview
This project demonstrates the configuration of **OSPFv2 in a single area** using Cisco Packet Tracer.  
The topology includes three routers and three end devices, with full IP addressing and OSPF implementation.  
The objective is to enable dynamic routing, improve scalability, and verify connectivity across all networks.

---


## Addressing Table

| Device | Interface | IP Address   | Subnet Mask     | Default Gateway |
|--------|-----------|--------------|-----------------|-----------------|
| R1     | G0/0      | 172.16.1.1   | 255.255.255.0   | N/A             |
| R1     | S0/0/0    | 172.16.3.1   | 255.255.255.252 | N/A             |
| R1     | S0/0/1    | 192.168.10.5 | 255.255.255.252 | N/A             |
| R2     | G0/0      | 172.16.2.1   | 255.255.255.0   | N/A             |
| R2     | S0/0/0    | 172.16.3.2   | 255.255.255.252 | N/A             |
| R2     | S0/0/1    | 192.168.10.9 | 255.255.255.252 | N/A             |
| R3     | G0/0      | 192.168.1.1  | 255.255.255.0   | N/A             |
| R3     | S0/0/0    | 192.168.10.6 | 255.255.255.252 | N/A             |
| R3     | S0/0/1    | 192.168.10.10| 255.255.255.252 | N/A             |
| PC1    | NIC       | 172.16.1.2   | 255.255.255.0   | 172.16.1.1      |
| PC2    | NIC       | 172.16.2.2   | 255.255.255.0   | 172.16.2.1      |
| PC3    | NIC       | 192.168.1.2  | 255.255.255.0   | 192.168.1.1     |

---

## OSPF Configuration Summary
- **Process ID:** 10  
- **Router IDs:**  
  - R1 → 1.1.1.1  
  - R2 → 2.2.2.2  
  - R3 → 3.3.3.3  
- **Passive interfaces:** LAN interfaces only  
- All networks included in Area 0  

---

## Verification
- `show ip route ospf` confirms OSPF routes across all routers.  
- End-to-end connectivity verified via successful ICMP ping between:  
  - PC1 ↔ PC2  
  - PC1 ↔ PC3  
  - PC2 ↔ PC3  

---

## Repository Contents
- `OSPF-SingleArea.pka` → Packet Tracer project file  
- `Topology.png` → Network topology diagram  
- `/configs` → Router configuration files  

---

## Skills Demonstrated
- Dynamic routing configuration with OSPFv2  
- Router ID assignment and passive-interface implementation  
- Subnetting and IP addressing design  
- End-to-end connectivity verification in a lab environment
