# enterprise-network-topology
Enterprise Multi-VLAN Network Topology with VRRP &amp; DHCP
A fully simulated enterprise-grade layered network built on **Huawei eNSP**, designed, deployed, and validated independently.

![Network Topology](topology.png)

## Overview

This project demonstrates a production-ready enterprise network architecture featuring:

- **Layered design**: Core, aggregation, and access layers
- **7+ VLANs**: Logical isolation across departments (Admin, Business, Management, Wireless, etc.)
- **High availability**: VRRP multi-group virtual gateways with primary/backup priority
- **Centralized addressing**: Global DHCP pools serving multiple subnets
- **Security enforcement**: Firewall trust/untrust zones, ACL policies, and NAT translation
- **Wireless coverage**: AC + AP deployment with multi-SSID VLAN mapping
- **24-hour stability test**: 99.9% network connectivity achieved under high load

## Tech Stack

| Category | Technologies |
|----------|-------------|
| Simulation | Huawei eNSP |
| Switching | VLAN Trunking, Link Aggregation, STP |
| Routing | OSPF Dynamic Routing, Static Routes |
| Redundancy | VRRP (vrid 10/20/30/40/101) |
| Addressing | Global DHCP Pools, Subnet Planning |
| Security | Firewall Zones (trust/untrust), ACL, NAT |
| Wireless | AC + Fit AP, Multi-VLAN SSID |
| Tools | Wireshark, Visio (topology design) |

## Key Highlights

- **Configuration discipline**: Verified every command line-by-line, cross-checked key parameters 3+ times before applying
- **Fault diagnosis**: Used `display` series commands to systematically identify and resolve 12 types of network faults
- **Documentation**: Produced a complete configuration manual and topology document, with full command logs and fault records
- **Work ethic**: Every configuration step followed a "read requirements first, verify twice, execute once" workflow

## Network Architecture

| VLAN | Subnet | Gateway (VRRP VIP) | Purpose |
|------|--------|---------------------|---------|
| 10 | 192.168.1.0/24 | 192.168.1.254 | Department A |
| 20 | 192.168.2.0/24 | 192.168.2.254 | Department B |
| 30 | 192.168.3.0/24 | 192.168.3.254 | Department C |
| 40 | 192.168.4.0/24 | 192.168.4.254 | Department D |
| 50 | 192.168.50.0/24 | - | Server Zone |
| 100 | 192.168.100.0/24 | - | Management VLAN |
| 101 | 192.168.101.0/24 | 192.168.101.254 | Business VLAN |
| Public | 201.1.1.0/24 | - | NAT External Interface |

## Why This Matters for SRE & DevOps Roles

This project demonstrates skills directly transferable to production environments:

- **Infrastructure as Code mindset**: Every configuration is documented, reproducible, and auditable
- **Troubleshooting under pressure**: Systematic fault diagnosis workflow applicable to production incidents
- **Cross-team communication**: Topology documentation and configuration manuals ready for handover
- **Security-first thinking**: ACL policies, zone-based firewall, and NAT all configured with least-privilege principles

## About Me
