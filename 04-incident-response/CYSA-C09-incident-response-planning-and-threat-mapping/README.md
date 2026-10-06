# Chapter 9 — Incident Response Planning and Threat Mapping

## Portfolio summary

This chapter set demonstrates evidence-bounded incident response analysis: severity and recoverability classification, response-phase mapping, stakeholder communications planning, and MITRE ATT&CK mapping. The work was completed as guided written and research exercises. It does not claim that a live incident was handled.

## Labs completed

| Lab ID | Activity | Demonstrated outcome |
|---|---|---|
| CYSA-C09-L01 | Severity and recoverability classification | Classified operational and economic impact, identified the need for external support, and kept recovery timing provisional where the scenario lacked evidence. |
| CYSA-C09-L02 | Incident response phase mapping | Mapped seven activities to response phases and corrected routine firewall maintenance to Preparation. |
| CYSA-C09-L03 | Communications planning | Built an authority-and-audience matrix, alternate-channel plan, approval path, and update cadence while preserving uncertainty about data exposure. |
| CYSA-C09-L04 | Threat profile and ATT&CK mapping | Correlated public WannaCry reporting with ATT&CK techniques for data encryption, remote service exploitation, tool transfer, and service creation. |

## Analytical approach

1. Separate observed facts from assumptions and scenario conditions.
2. Classify impact without inferring data compromise that was not established.
3. Map response activities by their immediate purpose, because the same technical action can support investigation or containment.
4. Define communication authority, trusted channels, review requirements, and update timing.
5. Use primary vendor reporting and MITRE ATT&CK to map behavior while treating group association as source-reported context rather than independent attribution.

## Results and lessons

- Severity statements are stronger when operational impact, financial impact, scope confidence, and recovery constraints are stated separately.
- Routine controls belong to preparation unless they are used during an active event.
- Communication plans should make uncertainty visible and require legal/public-relations review before external claims.
- ATT&CK mapping should connect a documented behavior to a technique; it should not fill gaps in initial access, credential theft, exfiltration, or victim impact.

## Evidence and limitations

The reviewed course evidence included lab-specific worksheets/reports and chapter-level completion summaries. Raw course materials, answer keys, learner responses, and sensitive evidence are intentionally excluded from this public version. This portfolio page summarizes demonstrated methods and conclusions without reproducing copyrighted prompts.
