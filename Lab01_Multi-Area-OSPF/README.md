# Lab 01: Multi-Area OSPF (IPv6)

## Purpose
Build a multi-area OSPFv3 network across multiple routers and networks to practice inter-area connectivity, troubleshooting, and IPv6 configurations in Cisco Packet Tracer.

## Topology Overview 
- 5 Cisco 4321 routers, each with NIM-2T modules  
- 5 end-host computers  
- 9 IPv6 networks:
  - 5 networks connecting each PC to its respective router via G0/0/0 interfaces  
  - 4 networks connecting routers to each other via S0/1/0 and S0/1/1 interfaces  
- Area assignment:
  - Routers 1 & 2 + PCs 1–3 → Area 0  
  - Routers 4 & 5 + PCs 4–5 → Area 1  
  - Router 3 interfaces split between Area 0 (G0/0/0 & S0/1/1) and Area 1 (S0/1/0)  
- IPv6 addresses: 2001:X::Y, with letters a–f for first six networks and db8, dc8, dd8 for the last three.

- (diagrams shown in pdf file)

## Key Configurations
- `ipv6 unicast-routing` – enables IPv6 routing  
- `ipv6 router ospf <process-id>` – starts OSPFv3 process  
- `ipv6 ospf <process-id> area <area-id>` – enables OSPFv3 on interfaces  
- `router-id <ID>` – statically sets router ID  
- IPv6 addresses assigned to all router interfaces and PCs

## Verification & Validation
- `show ipv6 ospf interface` – confirm interfaces running OSPFv3  
- `show ipv6 ospf neighbor` – verify OSPF adjacencies  
- `show ipv6 route` – confirm correct route propagation  
- `ping` between PCs and routers across areas

## Key Results
- Multi-area OSPFv3 successfully configured  
- Inter-area routing verified  
- IPv6 connectivity established across all networks  
- Router IDs and adjacency maintained stable

**Files in this folder:**  
- `Multi-Area-OSPF.pdf` – full lab with table of contents, configurations, and diagrams  

