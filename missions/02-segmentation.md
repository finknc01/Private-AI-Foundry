# Mission 02 — Divide the Kingdom

## Briefing
Researchers need workload access. They do not need the same path to management interfaces, monitoring backends, or every other workload.

## Objective
Design and test management/data/workload segmentation.

## Build
Use namespaces/VM networks to model at least three zones: management, workload, and data/services. Define allowed flows first, then implement them with routing/firewall rules.

## Deliberate misconfiguration
Temporarily allow one flow that should be denied, such as workload → management service. Detect it with your validation matrix, then restore policy.

## Evidence
- zone diagram
- source/destination/port policy table
- allowed/denied test results
- packet/firewall evidence

## Victory condition
You can prove segmentation with tests rather than pointing at a diagram.
