# Private-AI-Foundry

> **Project Obsidian — build a private AI environment for sensitive workloads, then challenge its trust assumptions before anyone else does.**

## Lab environment

- **Core environment:** RHEL lab hosts using synthetic users, data, credentials, and fictional infrastructure only.
- **Host-security focus:** SELinux, least privilege, SSH/sudo policy, firewalld/network segmentation, logging/auditing, and container boundaries.
- **Evidence rule:** Defensive controls must map to explicit threats and residual risk; PPML is not represented as a substitute for host/network security.

## Purpose

Private-AI-Foundry is the secure/private-AI infrastructure lab. Fictional **Aster Labs** needs an accelerated environment for sensitive workloads without giving every researcher unrestricted access to hosts, secrets, management interfaces, datasets, or each other's work.

The core question is:

> **What am I protecting, from whom, through which path, and what control actually reduces that risk?**

This is a defensive lab. It uses synthetic data and local test identities and does not contain employer/customer information or offensive exploitation instructions.

## Skills developed

- threat modeling and trust boundaries
- RHEL host hardening and least privilege
- SELinux and host policy reasoning
- management-plane/network segmentation
- secrets handling and credential hygiene
- container/workload isolation
- logging/auditing concepts
- PPML context and its boundary with system security
- defense-in-depth and residual-risk communication

## Obsidian campaign

The files in [`missions/`](missions/) are authoritative. Missions 00–04 plus the Final are the core campaign; Missions 05–06 are valuable extensions when time permits.

| Mission | Security problem | Primary outcome |
|---|---|---|
| [00 — Trust Map](missions/00-trust-map.md) | Identify assets, actors, trust boundaries, and threats | first threat model |
| [01 — Host Hardening](missions/01-host-hardening.md) | Reduce unnecessary privilege and weak host access | defensible host-access model |
| [02 — Segmentation](missions/02-segmentation.md) | Separate workload, data, and management paths | trust-boundary/network diagram + tests |
| [03 — Secrets](missions/03-secrets.md) | Remove plaintext/shared-secret anti-patterns | repeatable secret-handling process |
| [04 — Container Isolation](missions/04-container-isolation.md) | Constrain workload privileges, mounts, and reachability | isolation evidence |
| [05 — Audit](missions/05-audit.md) | Improve accountability and incident evidence | audit/logging timeline **(stretch)** |
| [06 — PPML Boundary](missions/06-ppml.md) | Distinguish mathematical privacy protections from infrastructure controls | PPML/security boundary analysis **(stretch)** |
| [Final — Obsidian Review](missions/final-obsidian-review.md) | Defend the architecture against adversarial design questions | threat/control/residual-risk review |

## Security-boundary rule

“Private” does not automatically mean “secure.” Each control should state:

1. threat or failure it addresses
2. layer where it acts
3. prevention/detection/containment/recovery value
4. evidence that the control behaves as expected
5. residual risk after the control exists

PPML techniques may reduce specific privacy risks in data/model processing, but they do not replace host hardening, segmentation, identity, secrets management, patching, or auditing.

## Evidence standard

Useful artifacts include a threat model, trust diagram, segmentation tests, least-privilege evidence, sanitized RHEL configuration, SELinux evidence, secret-handling procedure, audit timeline, control matrix, PPML boundary analysis, and prioritized residual risks.

Every artifact must clearly distinguish implemented/tested controls from modeled recommendations.

## Completion condition

Project Obsidian is complete when the architecture can survive a hostile design review because its assumptions are explicit, its core controls are testable, and its remaining risks are visible—not because it is merely described as private.
