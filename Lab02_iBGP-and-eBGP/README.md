# Lab 02: iBGP and eBGP (IPv4 & IPv6)

## Purpose
Configure iBGP and eBGP sessions to understand inter- and intra-AS routing, loopback-based neighbor setups, and multi-protocol BGP operation.

## Topology Overview
- 5 Cisco 3600 routers  
- IPv4 and IPv6 addressing:  
  - Loopbacks: 1.0.0.0/32 → 5.0.0.0/32 (IPv4), 2001:acad:a:: → 2001:acad:e:: (IPv6)  
  - Inter-router networks: 10.0.0.0/24 → 13.0.0.0/24 (IPv4), 2001:a:: → 2001:d:: (IPv6)  
- Router roles:  
  - 2 routers in eBGP  
  - 1 router in both iBGP and eBGP (border router)  
  - Remaining routers in iBGP  
- iBGP routers also run OSPF

## Key Configurations
- `router bgp <AS>` – enable BGP  
- `neighbor <IP> remote-as <AS>` – configure neighbors  
- `neighbor <IP> activate` – enable address family session  
- `neighbor <IP> update-source <loopback>` – loopback-based neighbor  
- `redistribute static` – advertise static routes  
- IPv4 & IPv6 BGP address-family configuration  

## Verification & Validation
- `show ip bgp` / `show ip bgp summary`  
- `show bgp ipv6 unicast` / `show bgp ipv6 unicast summary`  
- Ping and connectivity tests between routers and loopback addresses

## Key Results
- Stable iBGP and eBGP sessions established  
- IPv4 and IPv6 routes correctly propagated  
- Loopback-based neighbor setup verified for resilience  
- Inter-protocol redistribution functional  

**Files in this folder:**  
- `iBGP-and-eBGP.pdf` – full lab with table of contents, configurations, and diagrams
