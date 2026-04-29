# enterprise-network-topology
Enterprise Multi-VLAN Network Topology with VRRP & DHCP

A fully simulated enterprise-grade layered network built on **Huawei eNSP**, designed, deployed, and validated independently.

![Network Topology](topology.png)

---

## Overview
This project demonstrates a production-ready enterprise network architecture featuring:
- **Layered design**: Core, aggregation, and access layers with clear role separation
- **7+ VLANs**: Logical isolation across departments (Admin, Business, Management, Wireless, etc.)
- **High availability**: VRRP multi-group virtual gateways with primary/backup priority switching
- **Centralized addressing**: Global DHCP pools serving multiple subnets with lease management
- **Security enforcement**: Firewall trust/untrust zones, granular ACL policies, and PAT/NAT translation
- **Wireless coverage**: AC + Fit AP deployment with multi-SSID VLAN mapping and roaming
- **24-hour stability test**: Achieved 99.9% network connectivity under high traffic load and failover scenarios

---

## Tech Stack
| Category       | Technologies                                                                 |
|----------------|------------------------------------------------------------------------------|
| Simulation     | Huawei eNSP                                                                 |
| Switching      | VLAN Trunking, Link Aggregation (LACP), STP/RSTP                            |
| Routing        | OSPF Dynamic Routing, Static Routes, Default Route Redistribution           |
| Redundancy     | VRRP (vrid 10/20/30/40/101) with preemption and priority tuning             |
| Addressing     | Global DHCP Pools, Subnet Planning, DHCP Relay                              |
| Security       | Firewall Zones (trust/untrust/dmz), ACL, NAT/PAT                            |
| Wireless       | AC + Fit AP, Multi-VLAN SSID, WLAN Service Template                          |
| Tools          | Wireshark (packet capture), Visio (topology design), CLI debugging commands  |

---

## Key Highlights
- **Configuration discipline**: Verified every command line-by-line, cross-checked key parameters 3+ times before applying to avoid outages
- **Fault diagnosis**: Used `display` series commands and Wireshark capture to systematically identify and resolve 12+ types of network faults (e.g., VRRP split-brain, DHCP relay failure, STP loop)
- **Documentation**: Produced a complete configuration manual, topology document, with full command logs and post-mortem fault records
- **Operational workflow**: Every configuration step followed a "read requirements first, verify twice, execute once" approach, simulating production change management processes

---

## Network Architecture
> This table summarizes the VLANs, subnets, and gateway addresses used in the topology:

| VLAN ID | Subnet             | Gateway (VRRP VIP) | Purpose               |
|---------|--------------------|--------------------|-----------------------|
| 10      | 192.168.1.0/24     | 192.168.1.254      | Department A          |
| 20      | 192.168.2.0/24     | 192.168.2.254      | Department B          |
| 30      | 192.168.3.0/24     | 192.168.3.254      | Department C          |
| 40      | 192.168.4.0/24     | 192.168.4.254      | Department D          |
| 50      | 192.168.50.0/24    | -                  | Server Zone           |
| 100     | 192.168.100.0/24   | -                  | Management VLAN       |
| 101     | 192.168.101.0/24   | 192.168.101.254    | Business VLAN         |
| Public  | 201.1.1.0/24       | -                  | NAT External Interface|

---

## Why This Matters for SRE & DevOps Roles
This project demonstrates hands-on skills directly transferable to production environments:
- **Infrastructure as Code mindset**: Every configuration is documented, reproducible, and auditable, laying the foundation for automation
- **Troubleshooting under pressure**: Systematic fault diagnosis workflow applicable to production incidents and on-call rotations
- **Cross-team communication**: Topology documentation and configuration manuals ready for handover to engineering, security, and operations teams
- **Security-first thinking**: ACL policies, zone-based firewall, and NAT all configured with least-privilege principles, aligning with enterprise security standards

---

## About Me
Network operations engineer with backend development experience in Python (Django, FastAPI). Currently seeking **SRE / DevOps / Infrastructure engineering opportunities in Japan**.

- **Languages**: Chinese (Native), English (CET-4), Japanese (learning towards N2)
- **Certifications**: Huawei Datacom HCIP
- **Awards**: National Endeavor Scholarship (2026)
- **Contact**: Tiandcq896@qq.com
