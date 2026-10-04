# Authorized Network Reconnaissance and Scanning Workflow

**Lab IDs:** CYSA-C05-L01, CYSA-C05-L02, CYSA-C05-L03  
**Status:** Completed and evidence verified  
**Performed:** October 2, 2026  
**Evidence verified:** October 3, 2026

## Objective

Perform authorized reconnaissance against an intentionally vulnerable lab guest, correlate scan results with packet behavior and local ground truth, and use read-only Metasploit auxiliary tooling without claiming exploitation.

## Scope and Safety

The work was limited to owned virtual machines on an isolated private lab network. The vulnerable guest was not attached to household, production, bridged, or external networks. No exploit module, payload, session, credential attack, or third-party target was used.

Public documentation excludes private addressing, host identifiers, raw captures, screenshots, recordings, credentials, and course assessment material.

## Environment and Tools

- Kali Linux analyst VM
- Intentionally vulnerable Linux target VM
- Isolated virtual network
- Nmap
- Wireshark
- Metasploit Framework 6.4 development build
- Wmap 1.5.1

## Lab 1 — Port Scanning and Packet Capture

A baseline Nmap scan of the default TCP port set identified 23 open and 977 closed ports in 4.62 seconds. A complete TCP-port scan identified 30 open and 65,505 closed ports in 7.06 seconds; a repeat completed in 6.89 seconds.

Packet inspection was used to connect scanner output to TCP behavior:

- An open HTTP port showed SYN, SYN/ACK, and RST behavior.
- A tested closed port showed SYN followed by RST/ACK.
- A corrupt initial capture was replaced with a usable retry.

These observations show why port-state conclusions should be supported by both scanner output and packet evidence.

## Lab 2 — Device Fingerprinting

Nmap operating-system detection estimated a Linux 2.6.9–2.6.33 target, categorized it as a general-purpose device, and placed it one hop away.

Local target ground truth showed:

- Linux kernel 2.6.24-16-server
- Ubuntu 8.04

The kernel fit within Nmap's remote estimate. The exact distribution release came from local system metadata, not from the remote fingerprint alone. This distinction prevents an inference from being reported as an observed fact.

A repeat default-port scan returned the same 23-open/977-closed distribution in 5.90 seconds.

## Lab 3 — Metasploit Auxiliary Scanning

Metasploit and its database were initialized, Wmap was loaded, the authorized web target was registered, console output was spooled, and Wmap executed 39 modules in approximately 213.25 seconds.

The stored result identified HTTP TRACE as enabled on TCP port 80. Web-server and scripting-platform banners were also observed.

This was an auxiliary scanning exercise. The evidence does not establish successful exploitation, file upload, authentication bypass, session creation, or target compromise.

## Findings

1. Multiple listening services were exposed by the intentionally vulnerable guest.
2. Packet behavior corroborated representative open and closed TCP-port states.
3. Remote OS detection produced a useful family and kernel-range estimate, but local validation was needed for the exact release.
4. Wmap recorded an HTTP TRACE configuration finding requiring independent validation before operational escalation.
5. Tool output must be separated into observations, inferences, and verified ground truth.

## Evidence and Verification

Private course evidence was attributed to the individual lab IDs and included:

- Target and analyst network-state checks
- Baseline and full-range scan results
- Packet-analysis screenshots
- Remote OS fingerprint and local target facts
- Metasploit database, Wmap, scan, finding, and cleanup checkpoints
- A chapter completion review indexing evidence E01–E52

The chapter evidence record and all three labs were reviewed and marked verified.

## Limitations

- The raw PCAP was not supplied for independent reanalysis.
- Nmap normal/XML output files were not supplied.
- The raw Metasploit spool file was not supplied.
- The HTTP TRACE result was not independently repeated with a separate request/response test.
- Optional service-version, UDP, additional-device, and supplemental scanner exercises were not completed.
- Remediation was proposed but not implemented or retested.
- The cause of the original corrupt capture was not established.

## Recommendations

- Preserve machine-readable Nmap output and raw packet captures in future runs.
- Validate high-impact scanner findings with a second method.
- Disable HTTP TRACE unless a documented application requirement exists.
- Reduce exposed services to the minimum required set.
- Re-scan after remediation and compare results against the original baseline.
- Keep intentionally vulnerable guests isolated and verify routing before every exercise.

## Skills Demonstrated

- Authorized network reconnaissance
- Nmap port scanning and OS fingerprinting
- TCP-state interpretation
- Wireshark packet analysis
- Metasploit auxiliary scanning
- Service and banner analysis
- Evidence correlation
- Scope control and cautious technical reporting

## Lessons Learned

- Scanner classifications are stronger when correlated with packet behavior.
- Remote fingerprints are estimates; local ground truth must be labeled separately.
- A scanner finding is not proof of exploitability or compromise.
- Failed or corrupt evidence should remain in the audit trail even when a valid retry replaces it.
- Evidence quality includes preserving raw, machine-readable artifacts—not only screenshots.

## Sanitization

This writeup omits private IP addresses, credentials, system identifiers, raw captures, screenshots, recordings, copyrighted questions, and keyed answers. Detailed evidence remains in the private course record.
