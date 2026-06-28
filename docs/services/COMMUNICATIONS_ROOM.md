# Communications Room

The Communications Room represents network links, SSH, VPN/Tailscale, DNS, and host reachability.

It should make connections visible without overwhelming the rest of the interface.

## Purpose

Show how stations and services communicate.

## Visual Theme

- network map table
- link lines
- relay console
- SSH terminal bank
- VPN/tunnel indicators
- DNS board
- cyan/blue active links
- yellow degraded links
- red broken links

## Useful Telemetry

- reachable hosts
- SSH session state
- VPN/Tailscale status
- DNS status
- link latency
- packet loss if available
- active tunnels
- failed connections
- recent connection attempts

## Room Objects

Suggested clickable objects:

```text
network_map
ssh_relay_console
vpn_gateway_panel
dns_status_board
link_monitor
logs_terminal
```

## Common Commands

```text
Open Network Map
Open SSH Session
Check Reachability
View DNS Status
View VPN Status
Ping Station
Trace Route
Assign Engineer
```

## Visual States

```text
idle       links healthy, no active sessions
busy       SSH/VPN/network activity active
warning    degraded link, DNS warning, high latency
error      broken link, VPN down, DNS failed
offline    communications service unavailable
connecting connection attempt in progress
```

## Asset Ideas

```text
room_communications_idle_01.png
room_communications_busy_01.png
room_communications_warning_01.png
prop_network_map_active_01.png
prop_ssh_relay_console_idle_01.png
effect_ssh_beam_active_01.png
```

## Agent Usage

- Engineer manages network/service issues.
- Security officer checks VPN/firewall/security state.
- Signal officer may use network status for sensor routing.

## Safety Notes

Network and firewall changes should require confirmation.

The UI must clearly show the target host before opening a remote command session.
