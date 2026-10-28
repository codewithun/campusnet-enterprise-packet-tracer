# Security Policy

## VLAN Segmentation
Separate users, servers, labs, research, library, guest, and management traffic into distinct VLANs.

## Guest Network
- Guest VLAN: 420, subnet 192.168.41.0/24.
- Guest clients must not access internal ADMIN, FACULTY, CLASSROOM, SERVER, LAB, RESEARCH, LIBRARY, or management networks unless explicitly permitted.
- Internet access is outside the current lab unless an upstream network is added.
- Apply and verify an extended ACL at the appropriate Layer 3 gateway.

## Management
- Reserve management VLANs for network device administration.
- Restrict management access to authorized administrator networks.

## Validation
- Test permitted and denied flows.
- Record ACL configuration and counters.
- Do not claim a policy is enforced until tests confirm it.
