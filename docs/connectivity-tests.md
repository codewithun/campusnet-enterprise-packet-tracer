# Connectivity Tests

Record actual results after testing in Packet Tracer.

| ID | Test | Expected Result | Actual Result |
|---|---|---|---|
| CT-01 | PC to its virtual gateway | Success | Pending |
| CT-02 | ADMIN PC to SERVER subnet | According to policy | Pending |
| CT-03 | Faculty PC to classroom PC | According to policy | Pending |
| CT-04 | Lab PC to research PC | According to policy | Pending |
| CT-05 | Library PC to gateway | Success | Pending |
| CT-06 | Guest PC to internal networks | Blocked by ACL | Pending |
| CT-07 | OSPF-learned remote subnet | Route present | Pending |
| CT-08 | DNS resolution | Success after DNS setup | Pending |
| CT-09 | HTTP access to web server | Success after server setup | Pending |

Suggested commands:
- `show ip route`
- `show ip ospf neighbor`
- `show standby brief`
- `show vlan brief`
- `show interfaces trunk`
- `show access-lists`
