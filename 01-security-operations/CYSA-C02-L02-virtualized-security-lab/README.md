# Virtualized Security Lab Environment

**Lab ID:** CYSA-C02-L02  
**Status:** Completed and evidence verified  
**Completed:** September 29, 2026

## Objective

Build a repeatable, contained environment for defensive security analysis while keeping an intentionally vulnerable target off external networks.

## Scenario

An owned Linux workstation was configured as a virtualization host for three lab guests: a security-analysis workstation, an intentionally vulnerable target, and a supplemental Windows 11 system. The environment needed local analyst-to-target connectivity, denied outside IPv4 routing for the target, and a clean rollback point for future Windows exercises.

## Environment

- Owned Ubuntu Linux virtualization host
- QEMU/KVM, libvirt, virsh, and virt-manager
- Dedicated private /24 virtual network with DHCP
- Kali Linux analysis guest
- Metasploitable 2 target guest
- Windows 11 Pro guest with emulated TPM 2.0 and a clean-install snapshot

No external scanning, third-party testing, or production systems were involved.

## Procedure

1. Verified hardware virtualization support, memory, storage, and host firewall state.
2. Installed and validated the QEMU/KVM and libvirt management stack.
3. Resolved system-libvirt authorization and session-refresh issues.
4. Inspected the default NAT network, stopped it, and disabled autostart.
5. Defined and activated a dedicated network without a libvirt forwarding element.
6. Imported Kali and converted the target disk to a QEMU-compatible format.
7. Attached the guests only to the dedicated lab network.
8. Installed Windows 11 with UEFI-style virtual hardware and an emulated TPM.
9. Saved a clean Windows installation snapshot.
10. Verified local Kali-to-target reachability.
11. Verified that the target had only a connected private route, no default IPv4 route, and no route to an outside IPv4 test address.
12. Preserved troubleshooting history and final-state evidence separately from this public summary.

## Evidence Collected

Private course evidence includes:

- Virtual network definition and state
- Guest configuration and boot-state views
- Target interface and routing output
- Local analyst-to-target reachability results
- Failed outside-route test from the target
- Windows installation, virtual TPM, and snapshot views
- File hashes and duplicate tracking for the evidence set
- A complete technical evidence report

Raw screenshots, videos, account details, and course assessment materials are intentionally not published.

## Findings

- The default NAT network was inactive and not configured to start automatically.
- The dedicated lab network had no configured forwarding element.
- Kali could communicate with the target over the private lab segment.
- The target had no default IPv4 route and returned a local routing failure for an outside IPv4 destination.
- The Windows 11 guest booted successfully and retained a clean-install snapshot.
- The configuration met the tested local-connectivity and denied-egress objectives at the recorded time.

## Analysis

The paired tests were important. Local reachability alone would not prove containment, and a failed outside ping alone could reflect packet loss or ICMP filtering. Reviewing the target route table together with the immediate “network unreachable” result provided stronger evidence that the target lacked an outside IPv4 path in the tested configuration.

The result is deliberately narrow: it does not claim an air gap, universal isolation, or the absence of every possible IPv6, second-interface, proxy, or host-mediated route. Network attachment and routing must be rechecked before each later exercise.

## Recommendations / Remediation

- Confirm each guest's active interfaces before starting a lab.
- Recheck routing and outside reachability before using the vulnerable target.
- Keep the default NAT network disabled unless a specific authorized exercise requires it.
- Preserve a clean snapshot before high-impact guest changes.
- Keep intentionally vulnerable guests off household and production networks.
- Store credentials and raw evidence outside the public repository.

## Skills Demonstrated

- QEMU/KVM virtualization
- libvirt and virt-manager administration
- Network segmentation and lab isolation
- IPv4 subnet and route interpretation
- Virtual disk extraction and conversion
- Guest provisioning and lifecycle troubleshooting
- Authorized local account recovery
- Evidence attribution and technical reporting
- Scope control and cautious security claims

## CySA+ / Analyst Competency Mapping

- Security operations environment preparation
- Secure lab architecture
- Network configuration validation
- Troubleshooting and root-cause analysis
- Evidence collection and preservation
- Technical documentation for analyst workflows

## Lessons Learned

- Installation, daemon availability, authorization, and session state are separate dependencies.
- A virtual network can exist but remain inactive.
- A bridge address does not prove usable outside routing.
- Transfer equality and publisher authenticity are different integrity questions.
- Commands must be executed in the correct host or guest context.
- Final-state validation is more defensible than relying on configuration intent.

## Sanitization

This writeup omits credentials, host and user identifiers, raw recordings, screenshots, home-network details, copyrighted question text, and answer material. Private evidence remains in the course evidence system.
