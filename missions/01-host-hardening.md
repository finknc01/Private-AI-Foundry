# Mission 01 — Harden the Forge

## Briefing
Project Obsidian begins with a Linux host. If the host is weak, every layer above inherits the problem.

## Objective
Apply least privilege, service minimization, patch/configuration discipline, secure remote access, and basic host auditing in a lab environment.

## Build
Inventory listening services, users/groups, sudo access, SSH configuration, file permissions, update state, and firewall posture. Create a documented baseline and make only changes you can justify.

## Defensive test
Create a lab user with intentionally excessive access, then reduce that access to the minimum needed. Demonstrate the before/after permission boundary without attempting privilege escalation exploits.

## Evidence
- attack-surface inventory
- hardening changes with rationale
- least-privilege matrix
- rollback notes

## Victory condition
Every exposed service and privileged account has a documented reason to exist.
