# Troubleshooting Interface and Cable Issues (Cisco Networks)

A step-by-step guide to help you troubleshoot Layer 1 (Physical Layer) issues commonly found in Cisco environments. This is ideal for CCNA prep or real-world problem-solving.

---

## Common Media Issues

Typical causes for Layer 1 (physical layer) network issues:

- Disconnected cables or devices powered off

- EMI (Electromagnetic Interference) from nearby motors or devices

- Cable strain or poor management — e.g., RJ-45 connectors under stress

- New applications that introduce unusual traffic patterns

- Half-duplex mismatches, especially with older switches or NICs

## Step-by-Step Troubleshooting Guide

Use these CLI commands:

## Check Interface Status

```bash
show interface
```

Check if the interface is up/down, and look for noise/errors/collisions.
```bash
show interface status
```

Shows whether the port is connected, notconnect, or err-disabled.

## Flowchart: Troubleshooting Switch Media Issues

## Interface Status Code Reference

Line Status

Protocol Status

Interface Status

Common Cause

administratively down

down

disabled

Interface shutdown via shutdown cmd

down

down

notconnect

Bad cable or no cable

up

down

notconnect

Cable plugged but no signal

up

up

connected

Normal operation

## Check Speed and Duplex Mismatches

```bash
show interface status
```

Inspect the Duplex and Speed columns. Mismatches often lead to errors or late collisions.

Example Output:
```bash
Port      Name     Status    Vlan   Duplex  Speed   Type
Fa0/1              connected  1      full    100     10/100BaseTX
```
Ensure both ends are either manually set the same or both set to auto for negotiation.

## Summary

- Always start with show interface and show interface status

- Physically inspect cables and ports

- Remove EMI sources and avoid cable bending

- Match duplex and speed settings

## Recommended Tools

- Cisco Packet Tracer or GNS3 (for practice)

- CCNA Official Study Guide

- Cisco CLI Cheat Sheets
