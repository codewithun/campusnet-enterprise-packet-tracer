# Troubleshooting Report

## Issue: HSRP group number exceeds supported range
- Symptom: Packet Tracer reports `HSRP version 2 is required for specified group number`.
- Cause: HSRP v1 supports group numbers 0–255.
- Resolution used for Building B VLAN 290: use HSRP group 90 while keeping VLAN ID 290 and virtual gateway 192.168.91.1.
- Verification: `show standby brief` showed DIST-B1 Active and DIST-B2 Standby for VLAN 290.

## Current Known State
- Core-to-distribution routed links and OSPF area 0 were configured and previously verified.
- CORE-1 and CORE-2 have LACP EtherChannel group 1.
- Building A HSRP was verified.
- Building B HSRP VLANs 210, 220, and 290 were verified.
- Building C and D configurations still need completion and verification.
- Guest ACL and end-to-end testing remain to be verified.
