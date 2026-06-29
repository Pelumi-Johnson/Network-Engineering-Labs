# Remote Access VPN Lab: Raspberry Pi + WireGuard + Cisco 1941

## Overview
This project documents a remote-access VPN lab built with a Raspberry Pi running WireGuard/PiVPN, a Cisco 1941 router, and a Cisco 2960 switch.

The goal was to securely access a private Cisco lab network from an external network without exposing Cisco management services directly to the public internet.

## Technologies Used
- Raspberry Pi
- WireGuard / PiVPN
- Cisco 1941 Router
- Cisco 2960 Switch
- Cisco IOS CLI
- DuckDNS / DDNS
- NAT / Port Forwarding
- tcpdump
- PuTTY / SSH / Telnet
- Windows WireGuard Client

## What I Built
- Deployed WireGuard VPN on a Raspberry Pi inside the lab network
- Configured Cisco static NAT for UDP 51820
- Configured home-router port forwarding to the Cisco WAN interface
- Used DuckDNS so the VPN could connect using a domain name instead of a changing public IP
- Configured split tunneling for lab-only traffic
- Validated the VPN path using WireGuard handshakes, ping tests, Cisco NAT translations, and tcpdump
- Remotely managed Cisco lab devices through the VPN

## Network Path
```text
External Laptop
-> WireGuard VPN
-> DuckDNS Endpoint
-> Home Router Port Forward
-> Cisco 1941 Static NAT
-> Raspberry Pi WireGuard Server
-> 10.10.10.0/24 Lab Network
-> Cisco Router/Switch Management
```

## Key Skills Demonstrated
- Remote-access VPN deployment
- Cisco NAT and port forwarding
- Dynamic DNS configuration
- Split tunneling
- Linux packet capture with tcpdump
- Cisco IOS remote management
- Layered network troubleshooting

## Project Documentation
[Download the full project PDF](Remote_Access_VPN_Project_Section.pdf)
