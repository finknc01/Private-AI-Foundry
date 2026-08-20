# Mission 00 — Draw the Trust Map

## Briefing
Aster Labs says the data is “private” because the server is on-prem. The security review rejects that sentence.

## Objective
Identify assets, actors, trust boundaries, management planes, data flows, and realistic failure/abuse cases.

## Tasks
Map researchers, administrators, host OS, BMC/management plane concept, GPU runtime, containers, scheduler, storage, model artifacts, datasets, secrets, logs, and network zones. For each boundary ask who can cross it, with what credential, and what they gain.

## Challenge
Choose five threats such as stolen operator credential, overprivileged researcher, exposed secret, malicious container, unpatched host, or management-plane exposure. Map each to assets and controls.

## Evidence
- data/control-flow diagram
- asset table
- trust-boundary map
- threat/control matrix

## Victory condition
You can explain exactly what “private” means in this design and which assumptions could invalidate it.
