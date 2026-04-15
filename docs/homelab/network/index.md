# Network

Overview of the homelab network infrastructure.

## Contents

- [OPNsense](opnsense.md) – Firewall and router configuration
- [Network Diagram](diagram.md) – Visual network topology and subnet details
- [Internet](internet.md) – Xfinity internet connection and Cloudflare DDNS

## Hardware

| Device | Role |
|--------|------|
| OPNsense appliance | Firewall / router |
| Managed switch | Layer 2 switching |

## Subnets

| Network | CIDR | Description |
|---------|------|-------------|
| LAN | 192.168.1.0/24 | Main LAN |
| Servers | 10.0.0.0/24 | Server VLAN |
