# Scenario Overview

During analysis of captured network traffic, abnormal outbound communication was identified.

Indicators included:

- Large-scale outbound data (~390MB)
- Suspicious HTTP object export
- Obfuscated PowerShell logic
- Hex-encoded IP address
- Static XOR key usage

Traffic was observed over TCP ports 1337 and 1338.

The objective was to reconstruct the exfiltrated payload and determine its contents.
