# OPNsense

OPNsense is the open-source firewall and routing platform used in the homelab. It runs on dedicated hardware in the rack and serves as the primary gateway and DNS resolver.

## Overview

| Property | Value |
|----------|-------|
| Version | OPNsense (latest stable) |
| Role | Firewall, router, DNS, DHCP |
| WAN interface | Xfinity (DHCP) |
| LAN interface | 192.168.1.1/24 |

## Features in Use

- **Firewall rules** – Stateful packet filtering between VLANs and WAN
- **DHCP server** – Managed address assignments for all LAN devices
- **DNS resolver (Unbound)** – Local DNS with upstream forwarding
- **Cloudflare DDNS** – Dynamic DNS updates via the built-in DDNS client (see [Internet](internet.md))
- **VLANs** – Segmentation between server, IoT, and management networks

## Interfaces

| Name | Interface | CIDR | Description |
|------|-----------|------|-------------|
| WAN  | em0 | DHCP | Xfinity upstream |
| LAN  | em1 | 192.168.1.1/24 | Main LAN |
| SERVERS | em1.10 | 10.0.0.1/24 | Server VLAN |

## DDNS Configuration

Dynamic DNS is configured under **Services → Dynamic DNS** using the Cloudflare provider. See [Internet](internet.md) for details.
