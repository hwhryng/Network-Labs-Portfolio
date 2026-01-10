# Lab 05: BGP (IPv6)

## Purpose
Configure BGP in IPv6 and integrate with OSPF and EIGRP to practice multi-protocol routing and redistribution in GNS3.

## Topology Overview
- 7 routers: Cisco 3660 (OSPF/BGP) and Cisco 7200 (ABR for BGP↔EIGRP)  
- 6 networks total  
- Router roles:
  - 2 OSPF routers  
  - 1 BGP router  
  - 2 EIGRP routers  
  - 2 ABRs (OSPF↔BGP, BGP↔EIGRP)  
- Serial interfaces: S1/0–S1/3, S5/0–S5/1  
- IPv6 networks: 2001:a:: → 2001:f::, 2001:aa:: network

## Key Configurations
- `router bgp <AS>` – enable BGP  
- `address-family ipv6` – enter IPv6 BGP configuration  
- `ipv6 router ospf <process-id>` – enable OSPFv3  
- `ipv6 eigrp <AS>` – enable EIGRP for IPv6  
- `neighbor <IP> activate` – enable BGP neighbor  
- `neighbor <IP> remote-as <AS>`  
- `no bgp default ipv4-unicast` – disable IPv4 AF  
- `redistribute <protocol>` – inter-protocol redistribution  

## Verification & Validation
- `show bgp ipv6 neighbors`  
- `show bgp ipv6 unicast` / `summary`  
- Ping and connectivity tests across IPv6 networks

## Key Results
- BGP IPv6 sessions established and stable  
- Multi-protocol redistribution with OSPF/EIGRP verified  
- IPv6 network connectivity confirmed

**Files in this folder:**  
- `BGP-IPv6.pdf` – full lab with table of contents, configurations, and diagrams  
