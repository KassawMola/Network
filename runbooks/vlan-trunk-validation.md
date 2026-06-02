# VLAN and Trunk Validation Runbook

## Purpose

Validate access VLANs, trunk links, allowed VLAN lists, and operational status before or after a network change.

## Demo Scope

```text
Demo device: catalyst-demo-01
Demo IP: 192.168.1.1
Demo user: admin
```

## Pre-checks

- Confirm the requested VLAN IDs and switch ports.
- Confirm the uplink and downstream device roles.
- Capture current interface and trunk state.
- Verify that the change window and rollback plan are approved.

## Commands

```text
show vlan brief
show interfaces status
show interfaces trunk
show running-config interface <interface>
```

## Validation

- Access ports are assigned to the expected VLAN.
- Trunk ports allow only the required VLANs.
- Native VLAN is documented and intentional.
- Interfaces are up/up where service is expected.

## Rollback

Restore the previous interface configuration and re-run the validation commands.

