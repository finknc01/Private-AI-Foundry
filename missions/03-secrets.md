# Mission 03 — The Secret That Escaped

## Briefing
A developer commits a fake API credential to a sample configuration. Nothing is compromised because it is synthetic—but the process failure is real.

## Objective
Learn secret lifecycle: creation, storage, distribution, access, rotation, revocation, and audit.

## Build
Use only fake lab secrets. Compare unsafe patterns—plaintext config, environment leakage, overly broad file access—with a safer local secret-handling method appropriate to your environment.

## Incident
Place a synthetic credential in a disposable file/repository branch, then practice the correct response: treat it as exposed, remove it from active use, rotate/revoke the fake value, and document why deleting the visible line alone is insufficient.

## Evidence
- secret data-flow diagram
- access matrix
- synthetic incident response
- repository hygiene checklist

## Victory condition
You can explain why “the secret is not in the README” is not a secret-management strategy.
