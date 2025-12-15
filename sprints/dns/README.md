# DNS (MSP mindset)

## Mental model
DNS answers one question: “What IP should I use for this name?”
DNS does NOT prove routing works. Always separate:
- Name resolution (DNS)
- Reachability (routing/gateway/firewall)

## Baseline checks (Windows)
Run these first:
- `ipconfig /all` (DNS servers, suffix, gateway, DHCP)
- `nslookup <name>` (does it resolve? which server answered?)
- `ping <resolved-ip>` (can you reach the destination?)

## Common MSP patterns
- Wrong DNS server handed out by DHCP (wrong VLAN or scope)
- VPN changes DNS behavior (split tunnel vs full tunnel)
- Internal names resolve only on internal DNS (not public)

## Anki deck
Use: `/anki/MSP_DNS_Interview_Master_1-50.csv`

Reminder: When importing to Anki → **Allow HTML in fields: OFF**
If HTML is on, the questions become hard to read due to formatting issues
