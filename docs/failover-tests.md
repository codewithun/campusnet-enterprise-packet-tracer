# Failover Tests

Perform tests only after saving a working copy of the Packet Tracer file.

| ID | Failure Simulation | Expected Result | Actual Result |
|---|---|---|---|
| FT-01 | Shut down active HSRP distribution SVI/uplink as appropriate | Standby takes over where supported | Pending |
| FT-02 | Disable one core-to-distribution routed link | OSPF uses alternate path | Pending |
| FT-03 | Disable one core switch path | Connectivity remains via surviving paths | Pending |
| FT-04 | Restore failed interface | Routing and HSRP return to intended state | Pending |

Record commands, observations, downtime if measurable, and screenshots.
Do not record a test as passed until it has been executed.
