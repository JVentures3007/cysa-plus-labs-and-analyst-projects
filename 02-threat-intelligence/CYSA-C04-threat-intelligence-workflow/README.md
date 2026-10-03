# Threat Intelligence Collection and Analysis Workflow

**Lab IDs:** CYSA-C04-A01, CYSA-C04-A02, CYSA-C04-A03  
**Status:** Completed and evidence verified  
**Performed:** October 1–2, 2026

## Objective

Practice a defensible threat-intelligence workflow: evaluate public indicators, collect structured intelligence through TAXII, interpret STIX objects, detect changes between collections, and connect collection activity to the broader intelligence lifecycle.

## Scope and Safety

All work used public threat-intelligence sources and an owned analysis environment. No third-party systems were scanned, tested, blocked, or attributed. Credentials, account details, API keys, MFA material, raw screenshots, recordings, home-network identifiers, and course assessment content remain private.

## Tools and Standards

- LevelBlue Open Threat Exchange (OTX)
- Pulsedive threat-intelligence feed
- STIX 2.1
- TAXII 2.1
- Python for polling, parsing, counting, and comparison
- Structured evidence indexing and analyst notes

## Activity A01 — Public Indicator Review

Five public IPv4 indicator records were reviewed manually in OTX. For each record, the review considered reputation context, pulse membership, source quality, related activity, and how an analyst might use the indicator in a broader investigation.

### Observations

- Indicator reputation is context, not proof of compromise.
- Age, source quality, recurrence, and corroboration affect the weight of an indicator.
- A public indicator can support hunting or enrichment without justifying an automatic block.
- Overlap across intelligence reports can raise confidence, but does not by itself establish attribution.
- False-positive risk must be considered before operational use.

No claim was made that the reviewed indicators appeared in local telemetry or represented a local compromise.

## Activity A02 — Structured STIX/TAXII Collection

The original STAXX/Limo/OTX feed attempts did not produce a usable authenticated workflow in the available lab environment. The learning objective was therefore completed with a documented adaptation using a Pulsedive TAXII 2.1 feed.

Two successful HTTP 200 collection runs were performed. Each returned 302 STIX objects, including 300 indicator objects.

### Indicator Distribution

| Indicator type | Count | Share |
|---|---:|---:|
| Domain | 134 | 44.7% |
| URL | 94 | 31.3% |
| IPv4 | 67 | 22.3% |
| IPv6 | 5 | 1.7% |
| **Total indicators** | **300** | **100.0%** |

### Run-to-Run Comparison

- Newly present objects in the sampled collection: 0
- Objects with changed content: 3
- Objects no longer present in the sample: 0

The comparison established that the feed could be polled, parsed, summarized, and compared over time. Exact changed fields were not examined, so no claim is made about the operational significance of the three changes.

## Activity A03 — Intelligence Lifecycle Application

A guided exercise connected analyst activities to lifecycle concepts such as requirements, collection, processing, analysis, dissemination, and feedback. The key takeaway was that tools and feeds are only one part of intelligence work: useful output depends on a defined requirement, evidence quality, interpretation, communication, and reassessment.

The public writeup intentionally summarizes the concepts without reproducing keyed exercise answers or copyrighted question text.

## Evidence and Verification

Private evidence was indexed to the individual lab IDs rather than treated as proof for the entire chapter. It includes:

- Manual indicator-review notes
- Failed feed-attempt notes and adaptation rationale
- Successful TAXII response evidence
- Parsed STIX object counts
- A repeat-poll comparison
- Lifecycle exercise completion evidence
- Separate observed results, limitations, and closeout notes

All nine recorded lab steps—three for each activity—were reviewed and marked complete. The three activities were each recorded as 100% complete with verified evidence.

## Findings

1. Public threat-intelligence records are most useful when treated as enrichment and triage inputs rather than standalone conclusions.
2. Standards-based STIX/TAXII collection supports repeatable parsing and comparison across runs.
3. Aggregate object counts can validate collection and processing, but they do not replace field-level analysis.
4. A failed implementation path should remain documented even when an alternate method completes the underlying learning objective.
5. Evidence must be attributed to the specific activity it supports; a chapter-level file does not prove every linked lab.

## Limitations

- The original STAXX dashboard workflow was not completed.
- Pulsedive was used as an explicit adaptation for the structured-feed objective.
- The three changed objects were identified at the object level; their exact changed fields were not analyzed.
- Feed authentication hardening and credential remediation were not independently verified.
- No local telemetry correlation, automated blocking, malware attribution, or compromise assessment was performed.
- Results describe the captured runs only and should not be generalized beyond them.

## Skills Demonstrated

- Threat-intelligence source evaluation
- IOC research and cautious interpretation
- STIX 2.1 object handling
- TAXII 2.1 collection
- Python parsing and change comparison
- Evidence attribution
- False-positive and scope control
- Technical documentation

## Lessons Learned

- Collection success is only the beginning; intelligence value comes from context and analysis.
- Access failures and adaptations should be documented, not silently erased.
- Version, object identity, and timestamp handling matter when comparing structured intelligence.
- A change count is not a severity judgment.
- Strong analyst reporting separates observed facts, interpretations, limitations, and claims not supported by the evidence.

## Sanitization

This writeup contains no indicator values, endpoints, tokens, credentials, account identifiers, raw evidence, private network details, copyrighted question text, or keyed answers. Detailed evidence remains in the private course record.
