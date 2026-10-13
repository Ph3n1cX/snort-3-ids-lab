# Snort 3 Network Intrusion Detection Lab

A hands-on learning project documenting how I build and explore a network intrusion detection lab with Snort 3, Kali Linux, VirtualBox, and Metasploitable 2.

> **Project status:** Lab documentation in progress. I will add screenshots, exact commands, and observed alerts as I validate each step. This repository distinguishes planned checks from results actually observed.

## Objectives

- Understand where a network intrusion detection system (NIDS) sits in a lab network.
- Configure and validate a Snort 3 sensor.
- Learn how rules match traffic and how alerts are produced.
- Generate controlled test traffic in an isolated lab and inspect the resulting output.
- Document findings, limitations, and possible defensive responses.

## Lab Environment

| Component | Role |
| --- | --- |
| VirtualBox | Runs the isolated virtual lab |
| Kali Linux (sensor VM) | Runs Snort 3 and inspects network traffic |
| Kali Linux (test VM) | Generates controlled test traffic |
| Metasploitable 2 | Intentionally vulnerable target for authorized lab practice |
| Virtual network | NAT-based lab network; previously used subnet: `10.0.2.0/24` |

**Important:** VirtualBox network modes and IP addresses can vary by host configuration. Confirm the actual interface, addressing, and routing in your own VM before using commands. Keep vulnerable targets isolated and do not run tests against systems you do not own or have explicit permission to assess.

## Concepts Covered

- Packet inspection and network visibility
- Snort 3 configuration and rule syntax
- Alert output and basic interpretation
- Test traffic versus evidence of a detection
- False positives, limitations, and safe lab practices

## Workflow

1. **Verify the lab network** — record each VM's IP address, interface, and network mode.
2. **Verify Snort installation** — capture the Snort version and validate the configuration before running the sensor.
3. **Confirm visibility** — identify the sensor interface and verify that test traffic is visible to it.
4. **Run a controlled test** — use a clearly documented test within the isolated lab.
5. **Inspect output** — save the relevant command output or alert evidence and explain what it does and does not prove.
6. **Document findings** — record the test, expected behaviour, actual result, troubleshooting, and defensive takeaway.

## Evidence and Findings

This section will be updated after each test is performed.

| Test | Status | Evidence / notes |
| --- | --- | --- |
| Record VM addresses and network mode | To document | Add interface and IP details |
| Validate Snort 3 configuration | To document | Add command and validation output |
| Confirm sensor traffic visibility | To document | Add packet-capture or Snort output |
| Trigger a controlled detection | To document | Add the rule, test method, and actual alert |
| Review alert and explain significance | To document | Add analysis and limitations |

No detection result is claimed here until it has been observed and recorded.

## Repository Structure

```text
snort-3-ids-lab/
├── README.md
├── docs/
│   └── lab-notes.md
├── rules/
│   └── README.md
└── evidence/
    └── README.md
```

## What I Learned

I will add concise notes here as the lab progresses, including configuration issues, network visibility challenges, rule behaviour, and how I validated the results.

## Defensive Takeaways

Snort alerts are investigative leads, not automatic proof of compromise. An analyst should validate the rule match, review surrounding traffic and host context where available, consider benign explanations, and document the confidence and limitations of the conclusion.

## Safety

All testing should remain inside systems and networks I own or am explicitly authorized to assess. Do not publish credentials, tokens, public IPs, personal data, or other sensitive information in screenshots or logs.

## Author

**Faisol Daud** — Cybersecurity student building practical skills in network security and SOC analysis.

- GitHub: [@Ph3n1cX](https://github.com/Ph3n1cX)
- LinkedIn: [Faisol Daud](https://www.linkedin.com/in/faisol-daud-268086337/)

---

*Document the evidence. Explain the alert. Be honest about what the test proves.*