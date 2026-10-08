# Campus Network Design and Implementation

A scalable multi-building campus network designed and implemented in Cisco Packet Tracer. Departments are separated into their own VLANs and subnets, and routing connects them across a three-layer hierarchical design. [LAB]

## Project overview

The network follows the standard hierarchical model used in enterprise campus design:

- **Core layer:** three Cisco 2911 routers connect the network segments and the server.
- **Distribution layer:** two multilayer switches aggregate the access switches and connect them to the core.
- **Access layer:** seven Cisco 2950-24 switches connect end devices, with two PCs per switch.

Seven departments each get a dedicated VLAN and /24 subnet, which keeps traffic segmented and makes the network easy to extend with new departments or buildings.

## Topology

<img width="1115" height="367" alt="WhatsApp Image 2026-10-08 at 9 58 55 AM" src="https://github.com/user-attachments/assets/b904b540-bb34-4913-9e1c-84d684399ead" />


| Layer | Devices |
|-------|---------|
| Core | Router1, Router2, Router3 (Cisco 2911), Server0 |
| Distribution | Multilayer Switch0 (Cisco 3650), second multilayer switch (Cisco 3650-24PS) |
| Access | 7 x Cisco 2950-24 switches |
| End devices | 14 PCs, 1 server |

## VLAN and IP addressing plan

| VLAN | Department | Subnet |
|------|------------|--------|
| 10 | Admin | 192.168.10.0/24 |
| 20 | HR | 192.168.20.0/24 |
| 30 | IT | 192.168.30.0/24 |
| 40 | CS | 192.168.40.0/24 |
| 50 | EC | 192.168.50.0/24 |
| 60 | Lab | 192.168.60.0/24 |
| 70 | Staff Room | 192.168.70.0/24 |

## Design goals

- Separate departments into their own broadcast domains with VLANs.
- Use a hierarchical core, distribution and access design that scales as the campus grows.
- Provide routing between departments, the core routers and the server.
- Keep the addressing plan simple, with one /24 subnet per department.

## How to open the project

1. Install [Cisco Packet Tracer](https://www.netacad.com/courses/packet-tracer).
2. Download `campus_network_architecture.pkt` from this repository.
3. Open it in Packet Tracer to explore the topology and device configurations.

## Repository structure

```
campus-network-design-lab/
├── README.md
├── campus_network_architecture.pkt   # Packet Tracer project file
└── docs/
    └── topology.jpeg                 # Network topology diagram
```

## Skills demonstrated

CCNA, TCP/IP, subnetting, VLAN segmentation, routing, switching, hierarchical network design, Cisco Packet Tracer

## Author

Mohammed Akbar Kittur | [LinkedIn](https://www.linkedin.com/in/mohammed-akbar-kittur) | [GitHub](https://github.com/Mohammed-Akbar-Kittur)
