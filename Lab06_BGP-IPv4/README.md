# Lab 06: BGP (IPv4) – Multi-Protocol Connectivity

## Purpose
Configure BGP in IPv4 and integrate with OSPF and EIGRP to practice multi-protocol routing and redistribution on Cisco ISR4321 routers.

## Topology Overview
- 7 ISR4321 routers with NIM-2T modules  
- 6 networks total  
- Router roles:
  - 2 EIGRP routers  
  - 1 BGP router  
  - 2 OSPF routers  
  - 2 ABRs (EIGRP↔BGP, BGP↔OSPF)  
- Serial interfaces: S0/1/0, S0/1/1  
- IPv4 networks: 192.168.1.0 → 192.168.6.0  

## Key Configurations
- `router bgp <AS>` – enable BGP  
- `network <IP> mask <mask>` – advertise networks  
- `neighbor <IP> remote-as <AS>` – configure neighbor  
- `redistribute <protocol>` – inter-protocol redistribution  
- `router-id <ID>` – assign router IDs

## Verification & Validation
- `show ip bgp` / `show ip bgp summary`  
- Ping tests between routers and networks

## Key Results
- BGP IPv4 routing established  
- Multi-protocol redistribution with OSPF/EIGRP verified  
- IPv4 connectivity across all networks confirmed

**Files in this folder:**  
- `BGP-IPv4.pdf` – full lab with table of contents, configurations, and diagrams  
