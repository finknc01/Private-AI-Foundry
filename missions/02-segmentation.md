# Mission 02 — Divide the Kingdom

## Briefing
Researchers need workload access. They do not need the same path to management interfaces, monitoring backends, or every other workload.

## Objective
Design and test management/data/workload segmentation using RHEL networking and firewall concepts.

## Build
Use disposable RHEL VMs, namespaces, or VM networks to model at least three zones: management, workload, and data/services.

Define the intended source → destination → protocol/port flows **before** implementing them. Use `ip`/NetworkManager for network state as appropriate and firewalld zones/rules for host policy. Temporary namespace-only constructs may use direct `ip`/bridge configuration where that is the point of the lab.

## Deliberate misconfiguration
Temporarily allow one flow that should be denied, such as workload → management service. Detect it with your validation matrix and packet/firewall evidence, then restore the intended firewalld policy.

## Evidence
- zone/trust-boundary diagram
- source/destination/protocol/port policy table
- NetworkManager/route state where relevant
- firewalld zone/rule evidence
- allowed/denied test results
- packet evidence proving where a denied or allowed flow stopped

## Victory condition
You can prove RHEL segmentation with repeatable tests rather than pointing at a diagram, and you can distinguish route/connectivity failures from firewall-policy denials.
