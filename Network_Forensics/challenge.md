## Challenge Brief: Two-Stage Data Theft (Network Forensics)

### Scenario

Your organization suspects a workstation was used to exfiltrate sensitive data after a brief unauthorized access window. Security monitoring was limited, but a full packet capture (PCAPNG) was collected during the incident.

Your task is to analyze the capture and reconstruct the attacker’s data theft workflow. The activity is believed to occur in two distinct stages:

1. An initial retrieval from an internal service.
2. A follow-up exfiltration to an internal web endpoint.

A small amount of benign noise traffic is also present.

### Objective

Extract the hidden flag from the capture.
Flag format: `SRC{...}`

### Hints

1. The incident is a strict two-step timeline: **download first**, then **multiple small uploads**.
2. The flag is **not present in plaintext**; you must **decode and reassemble fragments** found across the stages.
