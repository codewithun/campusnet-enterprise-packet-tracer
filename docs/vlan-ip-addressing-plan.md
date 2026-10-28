# VLAN and IP Addressing Plan

All client VLANs use /24 (255.255.255.0).
The virtual gateway is normally .1, distribution switch 1 uses .2,
and distribution switch 2 uses .3.

| Building | VLAN | Name | Subnet | Virtual Gateway |
|---|---:|---|---|---|
| A | 110 | ADMIN | 192.168.10.0/24 | 192.168.10.1 |
| A | 150 | SERVER | 192.168.50.0/24 | 192.168.50.1 |
| A | 190 | NET-MGMT-A | 192.168.90.0/24 | 192.168.90.1 |
| B | 210 | FACULTY | 192.168.20.0/24 | 192.168.20.1 |
| B | 220 | CLASSROOM | 192.168.21.0/24 | 192.168.21.1 |
| B | 290 | NET-MGMT-B | 192.168.91.0/24 | 192.168.91.1 |
| C | 310 | LAB | 192.168.30.0/24 | 192.168.30.1 |
| C | 320 | RESEARCH | 192.168.31.0/24 | 192.168.31.1 |
| C | 390 | NET-MGMT-C | 192.168.92.0/24 | 192.168.92.1 |
| D | 410 | LIBRARY | 192.168.40.0/24 | 192.168.40.1 |
| D | 420 | GUEST | 192.168.41.0/24 | 192.168.41.1 |
| D | 490 | NET-MGMT-D | 192.168.93.0/24 | 192.168.93.1 |

## Core-to-Distribution Transit Links

Transit masks are /30 (255.255.255.252).

| Link | Core IP | Distribution IP | Subnet |
|---|---|---|---|
| CORE-1—DIST-A1 | 10.255.0.1 | 10.255.0.2 | 10.255.0.0/30 |
| CORE-2—DIST-A1 | 10.255.0.5 | 10.255.0.6 | 10.255.0.4/30 |
| CORE-1—DIST-A2 | 10.255.0.9 | 10.255.0.10 | 10.255.0.8/30 |
| CORE-2—DIST-A2 | 10.255.0.13 | 10.255.0.14 | 10.255.0.12/30 |
| CORE-1—DIST-B1 | 10.255.0.17 | 10.255.0.18 | 10.255.0.16/30 |
| CORE-2—DIST-B1 | 10.255.0.21 | 10.255.0.22 | 10.255.0.20/30 |
| CORE-1—DIST-B2 | 10.255.0.25 | 10.255.0.26 | 10.255.0.24/30 |
| CORE-2—DIST-B2 | 10.255.0.29 | 10.255.0.30 | 10.255.0.28/30 |
| CORE-1—DIST-C1 | 10.255.0.33 | 10.255.0.34 | 10.255.0.32/30 |
| CORE-2—DIST-C1 | 10.255.0.37 | 10.255.0.38 | 10.255.0.36/30 |
| CORE-1—DIST-C2 | 10.255.0.41 | 10.255.0.42 | 10.255.0.40/30 |
| CORE-2—DIST-C2 | 10.255.0.45 | 10.255.0.46 | 10.255.0.44/30 |
| CORE-1—DIST-D1 | 10.255.0.49 | 10.255.0.50 | 10.255.0.48/30 |
| CORE-2—DIST-D1 | 10.255.0.53 | 10.255.0.54 | 10.255.0.52/30 |
| CORE-1—DIST-D2 | 10.255.0.57 | 10.255.0.58 | 10.255.0.56/30 |
| CORE-2—DIST-D2 | 10.255.0.61 | 10.255.0.62 | 10.255.0.60/30 |

## HSRP Notes
- Building A groups: 110, 150, 190.
- Building B groups: 210, 220, 90 (VLAN 290 uses group 90).
- Building C planned groups: 110, 120, 190.
- Building D planned groups: 110, 120, 190.
- Group IDs are local to each VLAN/interface and need not equal VLAN IDs.
- On the current Packet Tracer setup, HSRP group numbers above 255 require HSRP v2.
