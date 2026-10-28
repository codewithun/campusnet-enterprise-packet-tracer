# Network Design

## Architecture
Three-layer hierarchical campus design:
1. Core: CORE-1 and CORE-2.
2. Distribution: two Layer 3 switches per building.
3. Access: two Layer 2 switches per building.

## Routing
- OSPF process 1, area 0.
- Core-to-distribution links use /30 transit subnets.
- Distribution switches perform inter-VLAN routing.
- HSRP provides virtual default gateways for client VLANs.

## Redundancy
- CORE-1 and CORE-2 are connected by Layer 2 LACP EtherChannel.
- Each distribution switch has routed links to both core switches.
- Each building has two distribution switches and two access switches.

## Security
- VLAN segmentation.
- Guest network isolation using an extended ACL.
- Management VLANs reserved for network administration.

See `vlan-ip-addressing-plan.md` for VLAN and IP details.
