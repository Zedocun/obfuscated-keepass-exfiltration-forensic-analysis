# Reconstructing Obfuscated KeePass Exfiltration from Network Traffic

## Overview

This project documents a full forensic reconstruction of an obfuscated KeePass credential exfiltration captured within a PCAP file in a controlled lab environment.

The investigation involved:

- Identifying suspicious TCP activity
- Reassembling ~390MB fragmented data streams
- Reversing layered obfuscation (Hex → Base64 → XOR)
- Recovering a memory dump
- Extracting a KeePass database
- Performing controlled credential recovery
- Validating recovered access via CLI

The focus of this project is investigative methodology and tooling decisions rather than challenge completion.

---

## Investigation Flow

1. Suspicious traffic identification (Ports 1337 / 1338)
2. Large TCP stream reconstruction (~390MB)
3. Hex extraction via tshark
4. Binary reassembly using xxd
5. Base64 decoding
6. XOR deobfuscation (0x41 / 0x42)
7. Memory dump recovery
8. KeePass database extraction
9. Mask-based brute force (single missing character)
10. Credential validation via KPCLI

---

## Skills Demonstrated

- Network Forensics
- TCP Stream Reconstruction
- Large Dataset Handling
- CLI-based Analysis
- Obfuscation Reversal
- KeePass Database Recovery
- Structured Investigation Workflow

---

## Repository Structure

Detailed technical breakdown available in the `/docs` directory.

---

## Disclaimer

This investigation was performed in a controlled lab environment for educational and skill-development purposes.
