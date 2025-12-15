# DHCP (think like an MSP)

## Mental model
DHCP gives the client:
- IP address
- Subnet mask
- Default gateway
- DNS servers

APIPA (169.254.x.x) Client has not received a lease.
usually means the client cannot reach DHCP from that segment.
sometimes it is a scope issue.

## Baseline checks (Windows)
- `ipconfig /all` (DHCP enabled, DHCP server, lease info)
- `ipconfig /release` then `ipconfig /renew` (can you obtain a lease?)
- `ping <gateway>` (routing baseline)

## Common MSP patterns
- VLAN/port issue prevents DHCP reachability
- Missing DHCP options (gateway/DNS) breaks “working but weird” scenarios
- Multiple DHCP servers cause inconsistent gateway/DNS

## Anki deck
Use: `/anki/MSP_DHCP_Interview_Master_1-50.csv`

Reminder: Anki import → **Allow HTML in fields: OFF**
