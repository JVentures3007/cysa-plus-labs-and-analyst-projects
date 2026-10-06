# Chapter 10 — Indicator, Log, and Preservation Analysis

## Portfolio summary

This chapter set combines public threat-intelligence evaluation, controlled analysis of a synthetic authentication log, and legal-hold/preservation planning. The exercises emphasize integrity, scope control, cleanup, evidence limits, and defensible reporting.

## Labs completed

| Lab ID | Activity | Demonstrated outcome |
|---|---|---|
| CYSA-C10-L01 | OTX indicator evaluation | Reviewed pulse context and displayed counters while treating community intelligence as an investigative lead rather than proof of compromise. |
| CYSA-C10-L02 | Authentication-log acquisition and analysis | Transferred a synthetic log in an isolated lab, verified integrity, documented a temporary firewall exception, found invalid-user clusters and a separate accepted public-key session, then removed temporary services and rules. |
| CYSA-C10-L03 | Legal hold and preservation plan | Produced a tabletop plan covering preservation scope, deletion suspension, protected master copies, access logging, integrity checks, secure transfer, and custody acknowledgment. |

## Workflow

1. Review intelligence-source context and record what the platform actually displays.
2. Transfer training evidence over an isolated lab path with a narrowly scoped, temporary firewall rule.
3. Verify the transferred artifact before analysis.
4. Search authentication events by event type and correlate activity into bounded clusters.
5. Distinguish failed-login patterns from an accepted session and subsequent privileged commands.
6. Remove temporary transfer services and network exceptions.
7. Document preservation roles, master/working-copy separation, integrity checks, access controls, and handoff records.

## Results and lessons

- Threat-intelligence hits are leads; repeated community references are not independent corroboration.
- A failed transfer is itself useful evidence when the root cause and minimal corrective change are documented.
- Authentication findings must not be converted into attacker attribution without source-host telemetry and authorization context.
- Custody receipt is not the same as legal release from a hold.
- Cleanup evidence belongs in the workflow, not as an afterthought.

## Evidence and limitations

The evidence supported the performed acquisition and analysis workflow. The raw training log was not included in the public portfolio, a separate preserved-working-copy rehash was not retained, and full source-host telemetry was unavailable. Accordingly, this writeup makes no claim of real compromise, attacker identity, or live legal process. Raw screenshots, addresses, credentials, course prompts, and learner-answer material are excluded.
