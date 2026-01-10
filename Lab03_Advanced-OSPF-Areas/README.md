# Lab 03: Advanced OSPF Areas (Stubby, Totally Stubby, NSSA)

## Purpose
Explore OSPF area types (stub, totally stubby, NSSA) and integrate OSPF with EIGRP to practice advanced routing and redistribution.

## Topology Overview
- 9 Cisco ISR4321 routers (one router in backbone area with 2 NIM-2Ts)  
- 8 networks across 4 OSPF areas + 1 EIGRP area  
- ABRs connecting areas:
  - Backbone ↔ Stub  
  - Backbone ↔ Totally Stubby  
  - Backbone ↔ NSSA  
  - NSSA ↔ EIGRP  
- Serial DCE connections: S0/1/0, S0/1/1, S0/2/0, S0/2/1

## Key Configurations
- `router ospf <process-id>` – enable OSPF  
- `network <IP> <wildcard> area <area-id>` – assign interfaces to areas  
- `redistribute eigrp <AS>` – import EIGRP routes into OSPF  
- `redistribute ospf <process-id> metric <values>` – import OSPF into EIGRP 
- `router-id <ID>` – assign router IDs

## Verification & Validation
- `show ip ospf` / `show ip ospf database` – validate LSAs and area types  
- `show ip route` – confirm inter-area connectivity  
- `show run` – review all router configurations

## Key Results
- OSPF areas configured correctly, including stub, totally stubby, and NSSA  
- Redistribution with EIGRP verified  
- Routing tables converge across all areas  
- End-to-end connectivity confirmed

**Files in this folder:**  
- `Advanced-OSPF-Areas.pdf` – full lab with table of contents, configurations, and diagrams  
  
