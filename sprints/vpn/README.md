# VPN Sprint (Split Tunnel vs Full Tunnel) — MSP mindset

## Mental model (keep it simple)
When a VPN connects, 4 things can still be wrong:
1) IP configuration (DNS, suffix, gateway, adapter state)
2) Routing (which traffic is sent into the tunnel)
3) Name resolution (internal names only resolve via internal DNS)
4) Access control (firewall/ACL/MFA/conditional access)

VPN “Connected” does NOT mean routes and DNS are correct.

## Baseline checks (Windows)
1) ipconfig /all  (DNS, suffix, gateway, adapter)
2) route print    (internal routes vs default route via VPN)
3) nslookup <internal-name> (which DNS server answered)
4) ping / tracert (reachability and where it stops)

## Split vs Full Tunnel quick recognition
- Split tunnel: internet works normally; only internal subnets go over VPN
- Full tunnel: most/all traffic goes over VPN; internet may break by policy

## Anki deck
Use: /anki/MSP_VPN_Interview_Master_1-25.csv

Reminder: Anki import → Allow HTML in fields: OFF
