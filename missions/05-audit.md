# Mission 05 — Who Touched What?

## Briefing
A sensitive model artifact changed overnight. The file is valid; nobody knows who changed it.

## Objective
Design enough logging/auditing to reconstruct administrative and workload-relevant actions.

## Build
Choose a small set of important events to capture: authentication, sudo/admin action, service change, protected-file change, workload start/stop, and secret access where your tooling supports it.

## Incident
Using test accounts, perform a known sequence of benign administrative actions, then reconstruct the sequence from logs without relying on memory.

## Evidence
- event-source map
- timestamped reconstruction
- retention/integrity considerations
- gaps you could not answer

## Victory condition
Your audit trail answers “who, what, when, from where, and with what privilege” for the test incident—or explicitly documents what it cannot answer.
