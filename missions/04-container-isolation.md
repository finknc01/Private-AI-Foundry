# Mission 04 — Contain the Workload

## Briefing
Aster Labs wants researchers to run arbitrary model code. The host must not become indistinguishable from the workload.

## Objective
Understand container privilege boundaries, mounts, users, capabilities, device exposure, and resource limits.

## Build
Run a benign test workload with a deliberately minimal container configuration. Compare root vs non-root execution, broad vs narrow mounts, and unrestricted vs bounded CPU/memory where practical.

## Defensive test
Give one disposable container an unnecessarily broad host mount, observe what data becomes visible, then redesign the mount to least privilege. Do not attempt container escape techniques.

## Evidence
- container trust-boundary diagram
- before/after mount and privilege table
- GPU/device exposure notes

## Victory condition
You can identify which host resources a workload can reach and justify every intentionally exposed resource.
