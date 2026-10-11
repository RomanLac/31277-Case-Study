## To Do

- [x] Day 1: Topology, cabling, IPs, hostnames
- [ ] Day 2: OSPF, static routes, passwords, SSH
- [ ] Day 3: VLANs, inter-VLAN routing, DHCP
- [ ] Day 4: NAT and ACLs
- [ ] Day 5: WLAN and full connectivity test
- [ ] Day 6: Report
- [ ] Day 7: Final review and submit

## Address Table

- Addresses follow the VLSM design in Part 1. The first valid host in each subnet is the default gateway, and the second is the host or switch.
- Hosts A1, C and the Mobile Host get their addresses from DHCP, so no static address is set on them.
- R2 G0/0 has no address itself. The addresses are on the subinterfaces (G0/0.10, .20, .99), which are added on Day 3.
- R4, R5 and R6 serial addresses assume R4 S0/1/1 connects to R5 and R4 S0/0/0 connects to R6. If the cabling changes, update this table.
- If the .pkt and this table disagree, the .pkt is the source of truth. Update this table when you change anything.

| Device | Interface / Default Gateway | IP address/prefix |
|---|---|---|
| Internet | G0/0 | 138.25.88.85/30 |
| Internet | S0/1/1 | 209.165.200.1/30 |
| R1 | G0/0 | 192.168.0.113/29 |
| R1 | S0/1/0 | 192.168.0.121/30 |
| R1 | S0/1/1 | 209.165.200.2/30 |
| R2 | G0/0.10 | 192.168.0.65/27 |
| R2 | G0/0.20 | 192.168.0.1/26 |
| R2 | G0/0.99 | 192.168.0.97/29 |
| R2 | G0/1 | 192.168.0.114/29 |
| R3 | G0/0 | 192.168.0.115/29 |
| R3 | G0/1 | 192.168.0.105/29 |
| R4 | S0/1/0 | 192.168.0.122/30 |
| R4 | S0/1/1 | 172.10.0.145/30 |
| R4 | S0/0/0 | 172.10.0.149/30 |
| R5 | G0/0 | 172.10.0.129/28 |
| R5 | S0/1/0 | 172.10.0.146/30 |
| R5 | S0/1/1 | 172.10.0.153/30 |
| R6 | G0/0 | 172.10.0.1/25 |
| R6 | G0/1 | 172.10.0.157/30 |
| R6 | S0/1/0 | 172.10.0.150/30 |
| R6 | S0/1/1 | 172.10.0.154/30 |
| Sw1 | VLAN 99 | 192.168.0.98/29 |
| Sw1 | Default Gateway | 192.168.0.97 |
| Host A1 | NIC VLAN 10 | DHCP |
| Host A2 | NIC VLAN 20 | 192.168.0.2/26 |
| Host A2 | Default Gateway | 192.168.0.1 |
| Host B | NIC | 192.168.0.106/29 |
| Host B | Default Gateway | 192.168.0.105 |
| Host C | NIC | DHCP |
| Host D | NIC | 172.10.0.2/25 |
| Host D | Default Gateway | 172.10.0.1 |
| Mobile Host | Wireless NIC | DHCP |
| External Host | NIC | 138.25.88.86/30 |
