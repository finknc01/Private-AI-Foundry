# Mission 01 — Harden the Forge

## Briefing
Project Obsidian begins with a RHEL host. If the host is weak, every layer above inherits the problem.

## Objective
Apply RHEL least privilege, service minimization, patch/configuration discipline, secure remote access, SELinux enforcement, firewalld policy, and basic host auditing in a disposable lab environment.

## Build
Record a healthy baseline before changing controls:

- installed/update state with `dnf`/RPM tooling
- users, groups, shells, and `sudo -l`
- SSH configuration and authentication policy
- listening services with `ss -lntup`
- enabled/running services with `systemctl`
- SELinux mode/labels with `getenforce`, `sestatus`, and `ls -Z`
- firewalld zones/services/ports with `firewall-cmd`
- audit/journal evidence available for later validation

Remove or constrain only items you can justify. Keep the host recoverable and record rollback steps before higher-risk changes.

## Defensive tests

1. Create a lab user with intentionally excessive discretionary access, then reduce it to the minimum needed and prove both the allowed and denied cases.
2. Create one safe SELinux labeling/context problem and diagnose the resulting AVC evidence. Restore the correct context rather than disabling SELinux.
3. Expose one harmless high-port lab service, verify the expected firewalld behavior, then restrict it to the intended zone/service policy.

Do not use offensive privilege-escalation techniques; the objective is defensive control validation.

## Evidence
- attack-surface inventory
- package/update and service baseline
- least-privilege matrix
- SELinux enforcing state + AVC/context diagnosis
- firewalld zone/policy evidence
- hardening changes with rationale
- rollback notes and before/after validation

## Victory condition
Every exposed service and privileged account has a documented reason to exist, SELinux remains enforcing, network exposure is intentional, and the evidence proves the resulting access boundaries rather than merely listing hardening settings.
