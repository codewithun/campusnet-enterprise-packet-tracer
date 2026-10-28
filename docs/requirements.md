# Network Requirements

## Functional
- Four buildings connected through redundant core switches.
- Separate VLANs for administration, servers, faculty, classrooms, labs, research, library, guest, and network management.
- Inter-VLAN routing on Layer 3 distribution switches.
- OSPF area 0 for dynamic routing between core and distribution.
- HSRP for redundant default gateways.
- EtherChannel between CORE-1 and CORE-2.
- Guest access restrictions enforced using ACLs.

## Resilience
- Dual core-to-distribution links.
- Redundant distribution switches per building.
- HSRP active/standby gateway operation.
- OSPF reconvergence when a routed link fails.

## Validation
- Verify VLANs, trunks, routing, HSRP, OSPF, ACLs, connectivity, and failover.
