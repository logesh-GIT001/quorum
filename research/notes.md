# Research Notes

Running notes as we read foundational papers and design the architecture.
Most recent entries at the top.

---

## April 2026 — Project start

### Core questions we are trying to answer

1. Can we establish hardware-level ground truth from outside a machine 
   using TPM attestation without requiring a second trusted device?

2. What signals exist in human-computer interaction that are physically 
   constrained enough that an attacker with valid credentials cannot 
   fake them over months?

3. How do we connect hardware trust measurement with behavioral analysis 
   in a way that is more powerful than either layer alone?

### What we know existing tools do

- Wazuh, OSSEC: agent-based, runs inside OS, can be subverted by firmware malware
- TPM tooling (tpm2-tools): exists but no framework connects it to behavioral analysis
- LibVMI: hypervisor introspection exists but is academic and rough
- UBA tools (Splunk UEBA, etc.): all based on anomaly detection, all vulnerable 
  to baseline poisoning, all proprietary

### The gap

No open source project connects hardware-rooted trust measurement with 
intent-aware behavioral analysis. That is what Quorum is building toward.

### Papers to read next

- [ ] TPM 2.0 specification and remote attestation protocol
- [ ] "SoK: Understanding the Prevailing Security Vulnerabilities in TrustZone-assisted TEE Systems"
- [ ] Research on keystroke dynamics and cognitive biometrics
- [ ] MITRE ATT&CK framework — persistence and defense evasion tactics
