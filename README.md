# Quorum

> Establishing ground truth about systems and the humans operating them.

## The Problem

Modern security tools fail against sophisticated attackers in two fundamental ways.

**At the hardware layer:** Malware living in firmware loads before the OS, before 
any security tool, before anything you can measure from inside the system. Every 
tool that runs inside the OS can be lied to by what lives beneath it. There is 
no open source framework that establishes hardware-level ground truth from outside 
the machine.

**At the behavioral layer:** Every detection system today looks for anomalies — 
things that look weird. But the most sophisticated attackers don't look weird. 
They use valid credentials, legitimate tools, and normal-looking traffic. Worse, 
a long-term attacker can slowly corrupt a behavioral baseline until the system 
learns the attack as "normal." The question of how to detect intent — not just 
deviation — is unsolved.

These two problems are connected. A firmware-level attacker who then operates 
using legitimate credentials is simultaneously invisible at the hardware layer 
and the behavioral layer. No existing open source tool addresses both.

## What Quorum Attempts

Quorum is a research framework with two connected layers:

**Layer 1 — Hardware attestation**  
Using TPM-based measurement, hypervisor introspection, and network boot 
fingerprinting to establish whether a system can be trusted before any 
software-level analysis begins. Measured from outside the system. Unforgeable.

**Layer 2 — Intent-aware behavioral analysis**  
On top of that trusted foundation, detecting not anomalies but patterns of 
intent — including attackers who behave perfectly normally. Built around signals 
that are physically constrained and difficult to fake: timing patterns, cognitive 
latency, biomechanical signals, and long-term behavioral drift that survives 
baseline poisoning attempts.

The connection between these two layers is the novel contribution. Hardware 
attestation tells you whether to trust the machine. Behavioral analysis tells 
you whether to trust the human operating it. Neither alone is sufficient.

## Current Status

Early research phase. Reading foundational papers. Architecture in active design.

This is not a finished tool. It is an open research project. Progress is 
documented honestly in research/notes.md.

## Follow Progress

- Watch this repo for updates
- Read research/notes.md for ongoing thinking
- Open an issue to discuss ideas, papers, or approaches

## Contributing

See CONTRIBUTING.md for details.

## License

Apache 2.0 — see LICENSE
