# VLAN / Gateway / APIPA Sprint (think like an MSP)

## Mental model
When networking fails, separate:
1) Do you have a valid IP (or APIPA)?
2) Can you reach your default gateway?
3) Can you reach internal destinations?
4) Can you reach external destinations?

Valid IP does NOT mean correct VLAN.
Gateway ping does NOT mean full routing works.

## Baseline checks (Windows)
- `ipconfig /all` (IP range, gateway, DNS, DHCP server)
- `ping <gateway>` (first-hop reachability)
- `ping <known-internal-ip>` (internal routing)
- `ping 8.8.8.8` (external routing)
- `tracert <destination>` (view traffic)

## Common MSP patterns
- Desk moves / conference room ports mapped to different VLANs
- Guest VLAN allows internet only, blocks internal access
- Voice VLAN vs data VLAN mismatches (phone passthrough)
- ACLs (Access Control Lists) allow ping but block applications

## Anki deck
Use: `/anki/MSP_VLAN_Gateway_APIPA_Interview_Master_1-50.csv`

Reminder: Anki import → **Allow HTML in fields: OFF**
