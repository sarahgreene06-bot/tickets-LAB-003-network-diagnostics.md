# Windows Network Connectivity Diagnostic Lab

## Help Desk Ticket: LAB-003
Date: November 17, 2026
Status: Closed — diagnostics completed
Environment: Personal Windows computer

## Objective
Verify IP configuration, external IPv4 connectivity,
DNS resolution, and browser access in a home lab.
No connectivity failure was reported or reproduced.

## Investigation

### 1. Check network configuration
Command: ipconfig /all

Findings:
- IPv4 address: [REDACTED]
- Subnet mask: [REDACTED]
- Default gateway: [REDACTED]
- DHCP server: [REDACTED]
- DNS server: [REDACTED]
- DHCP enabled and lease information present.

### 2. Test external IPv4 connectivity
Command: ping 8.8.8.8

Result:
- Sent: 4
- Received: 4
- Lost: 0 (0% loss)
- Average round-trip time: 32 ms

Conclusion: The tested external IP address was reachable.
This test did not require a DNS lookup.

### 3. Test DNS resolution
Command: nslookup google.com

Result: The configured DNS server returned IPv4
and IPv6 addresses for google.com.

Conclusion: DNS resolution succeeded for this query.

### 4. Verify browser access
Opened https://www.google.com in Chrome.

Result: Google's homepage loaded successfully.

## Resolution
No fault was identified during testing.
No configuration changes were required.

## Skills Practiced
- Reading IP configuration and DHCP lease information
- Distinguishing IP connectivity from DNS resolution
- Using ping and nslookup
- Verifying browser access
- Documenting findings without assuming a cause

## Privacy
Local network addresses have been redacted.
