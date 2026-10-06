# CySA+ Lab & Project Index

This index tracks work completed or scheduled during the CySA+ study path.

## Status Key

- **Completed** — lab/project has been performed and documented
- **In Progress** — work has started
- **Scheduled** — lab/project guide exists and is planned
- **Planned** — portfolio item identified but not yet built

## Security Operations

| Project / Lab | Type | Status | Tools / Technologies | Primary Skills |
|---|---|---|---|---|
| Security Operations Chapter Labs | Chapter lab set | In Progress | Nmap, Linux, Windows tools, logs | Security operations, analysis, documentation |
| [Virtualized Security Lab Environment](../01-security-operations/CYSA-C02-L02-virtualized-security-lab/README.md) | Hands-on lab | Completed | QEMU/KVM, libvirt, Kali Linux, Windows 11 | Lab isolation, routing validation, evidence handling |
| [Chapter 5 Network Reconnaissance Workflow](../01-security-operations/CYSA-C05-network-reconnaissance-and-scanning/README.md) | Chapter lab set | Completed | Nmap, Wireshark, Metasploit, Wmap | Scanning, packet analysis, fingerprinting, auxiliary assessment |
| [Port Scanning & Fingerprinting](../01-security-operations/CYSA-C05-network-reconnaissance-and-scanning/README.md#lab-1--port-scanning-and-packet-capture) | Hands-on lab | Completed | Nmap, Wireshark | Reconnaissance, TCP-state analysis, OS fingerprinting |
| [Metasploit Auxiliary Scanning](../01-security-operations/CYSA-C05-network-reconnaissance-and-scanning/README.md#lab-3--metasploit-auxiliary-scanning) | Hands-on lab | Completed | Metasploit, Wmap | Auxiliary assessment, service analysis, scope control |

## Threat Intelligence

| Project / Lab | Type | Status | Tools / Technologies | Primary Skills |
|---|---|---|---|---|
| [Chapter 4 Threat Intelligence Workflow](../02-threat-intelligence/CYSA-C04-threat-intelligence-workflow/README.md) | Chapter lab set | Completed | OTX, Pulsedive, STIX 2.1, TAXII 2.1, Python | Threat intelligence, IOC analysis, lifecycle application |
| [OTX Indicator Review (A01)](../02-threat-intelligence/CYSA-C04-threat-intelligence-workflow/README.md#activity-a01--public-indicator-review) | Analyst exercise | Completed | LevelBlue OTX | IOC research, source evaluation, false-positive control |
| [STIX/TAXII Collection Workflow (A02)](../02-threat-intelligence/CYSA-C04-threat-intelligence-workflow/README.md#activity-a02--structured-stixtaxii-collection) | Analyst exercise | Completed | Pulsedive, STIX 2.1, TAXII 2.1, Python | Structured threat intelligence, polling, change detection |

## Vulnerability Management

| Project / Lab | Type | Status | Tools / Technologies | Primary Skills |
|---|---|---|---|---|
| [Chapter 6 Vulnerability Scanner Workflow](../03-vulnerability-management/CYSA-C06-vulnerability-scanning-workflow/README.md) | Chapter lab set | Completed | Nessus Essentials, Kali Linux, Nmap | Scanner administration, authorized assessment, coverage analysis |
| [Authorized Single-Host Scan](../03-vulnerability-management/CYSA-C06-vulnerability-scanning-workflow/README.md#lab-2--authorized-single-host-scan) | Hands-on lab | Completed | Nessus Essentials | Scanning, finding identification, evidence preservation |
| [Vulnerability Finding Analysis](../03-vulnerability-management/CYSA-C06-vulnerability-scanning-workflow/README.md#representative-findings) | Analyst exercise | Completed | Nessus output, Linux validation | Validation, limitations, remediation planning |
| [Chapter 7 Vulnerability Analysis and Remediation](../03-vulnerability-management/CYSA-C07-vulnerability-analysis-and-remediation/README.md) | Chapter lab set | Completed | Nessus Essentials, FIRST CVSS Calculator, Kali Linux, Ubuntu Linux | Finding analysis, CVSS interpretation, remediation verification |
| [CVSS Analysis and Local Prioritization](../03-vulnerability-management/CYSA-C07-vulnerability-analysis-and-remediation/README.md#lab-2--validate-cvss-and-prioritize) | Analyst exercise | Completed | FIRST CVSS Calculator, Nessus output | Vector analysis, contextual prioritization, uncertainty handling |
| [Reversible Remediation and Verification](../03-vulnerability-management/CYSA-C07-vulnerability-analysis-and-remediation/README.md#lab-3--remediate-and-verify) | Hands-on lab | Completed | Nessus Essentials, Kali Linux, Ubuntu Linux | Change control, comparative rescanning, residual-risk reporting |
| [Chapter 12 Security Reporting and Documentation](../05-security-reporting/CYSA-C12-security-reporting-and-documentation/README.md) | Reporting chapter set | Completed | Prior scan evidence, public reports, synthetic logs | Executive reporting, evidence-bounded incident documentation |

## Incident Response

| Project / Lab | Type | Status | Tools / Technologies | Primary Skills |
|---|---|---|---|---|
| [Chapter 9 Incident Response Planning and Threat Mapping](../04-incident-response/CYSA-C09-incident-response-planning-and-threat-mapping/README.md) | Chapter lab set | Completed | NIST SP 800-61, MITRE ATT&CK, public sources | Severity classification, communications, phase mapping, ATT&CK mapping |
| [Chapter 10 Indicator, Log, and Preservation Analysis](../04-incident-response/CYSA-C10-indicator-log-and-preservation-analysis/README.md) | Chapter lab set | Completed | OTX, Linux, grep, integrity tools | IOC evaluation, authentication-log analysis, evidence preservation |
| [Public Incident Report Critique](../05-security-reporting/CYSA-C12-security-reporting-and-documentation/README.md#labs-completed) | Analyst research | Completed | Public disclosures, source corroboration | Incident analysis, communication review |
| [Synthetic Incident Reporting Exercise](../05-security-reporting/CYSA-C12-security-reporting-and-documentation/README.md#labs-completed) | Reporting lab | Completed | Synthetic authentication logs, reporting framework | Incident documentation, evidence limits, escalation recommendations |

## ATT&CK & Adversary Mapping

| Project / Lab | Type | Status | Tools / Technologies | Primary Skills |
|---|---|---|---|---|
| [WannaCry Behavior-to-ATT&CK Mapping](../04-incident-response/CYSA-C09-incident-response-planning-and-threat-mapping/README.md) | Analyst project | Completed | MITRE ATT&CK, vendor reporting | Tactic/technique mapping, behavior analysis, attribution limits |

## Automation & AI Security

| Project / Lab | Type | Status | Tools / Technologies | Primary Skills |
|---|---|---|---|---|
| AI in Security Operations | CS0-004 extension | Planned | AI-assisted workflows | Investigation support, summarization, governance |
| AI-Specific Threats | CS0-004 extension | Planned | Prompt-injection/data-poisoning scenarios | AI security, risk analysis |
| SOAR-Style Automation | CS0-004 extension | Planned | Automation workflow design | Enrichment, triage, response automation |

## Integrated Projects

Integrated projects will combine multiple analyst competencies into larger portfolio artifacts rather than isolated chapter exercises.

Examples will include:

- Threat intelligence + IOC enrichment + ATT&CK mapping
- Vulnerability scan + validation + remediation report
- Incident triage + evidence analysis + response report
- Security operations case + executive summary
- AI-assisted analyst workflow with governance controls

## Capstone

The final CySA+ capstone will demonstrate an end-to-end analyst workflow, including evidence intake, technical analysis, prioritization, ATT&CK mapping, response recommendations, and professional reporting.
