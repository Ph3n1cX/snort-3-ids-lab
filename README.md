# Snort 3 Network Intrusion Detection Lab

A hands-on project documenting my Snort 3 network intrusion detection lab with Kali Linux, VirtualBox, and Metasploitable 2.

> **Project status:** The lab is working, and I have captured traffic and/or generated Snort alerts during practice. Exact commands, rule details, alert text, and screenshots still need to be added from the original lab output; they are not guessed in this repository.

## Objectives

- Understand where a network intrusion detection system (NIDS) sits in a lab network.
- Configure and validate a Snort 3 sensor.
- Learn how rules match traffic and how alerts are produced.
- Generate controlled test traffic in an isolated lab and inspect the resulting output.
- Document findings, limitations, and possible defensive responses.

## Lab Environment

| Component | Role |
| --- | --- |
| VirtualBox | Runs the virtual lab |
| Kali Linux (sensor VM) | Runs Snort 3 and inspects network traffic |
| Kali Linux (test VM) | Generates controlled test traffic |
| Metasploitable 2 | Intentionally vulnerable target for authorized lab practice |
| Virtual network | NAT-based setup; the lab has previously used `10.0.2.0/24`. Verify the current addresses and mode before testing. |

**Safety note:** VirtualBox networking varies by configuration. Verify the actual interface, IP addresses, and routing in your own VMs. Keep vulnerable targets isolated and only test systems you own or have explicit permission to assess.

## Verified Progress

- [x] Lab is currently working (confirmed by me).
- [x] Traffic capture and/or alert-generation practice has been performed (confirmed by me).
- [ ] Record the exact Snort version, command, and configuration validation output.
- [ ] Add a sanitized excerpt or screenshot of the actual traffic/alert output.
- [ ] Document the rule or test that produced the observed output.
- [ ] Explain the alert's significance, limitations, and defensive next steps.

The first two items reflect my current lab progress. The remaining items require the original command output and evidence so the write-up can be technically specific.

## Workflow

1. **Verify the lab network** — record each VM's IP address, interface, and network mode.
2. **Verify Snort installation** — capture the Snort version and validate the configuration before running the sensor.
3. **Confirm visibility** — identify the sensor interface and verify that test traffic is visible to it.
4. **Run a controlled test** — use a clearly documented test within the isolated lab.
5. **Inspect output** — save the relevant command output or alert evidence and explain what it does and does not prove.
6. **Document findings** — record the test, expected behaviour, actual result, troubleshooting, and defensive takeaway.

## Evidence and Findings

| Item | Status | Next evidence to add |
| --- | --- | --- |
| Lab environment | Lab working | VM addresses, interfaces, and network mode |
| Traffic capture / alert practice | Performed; exact details not yet documented | Sanitized command output or screenshot |
| Snort configuration validation | Needs documentation | Exact command and output |
| Detection rule and test | Needs documentation | Rule text, test method, and observed alert |
| Analyst interpretation | Needs documentation | Context, benign explanations, limitations, and response recommendation |

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

## Analyst Takeaway

A Snort alert is an investigative lead, not automatic proof of compromise. Validate the rule match, inspect surrounding traffic and host context where available, consider benign explanations, and record the confidence and limitations of the conclusion.

## Safety

Keep testing inside systems and networks you own or are explicitly authorized to assess. Sanitize screenshots and logs before publishing; never commit credentials, tokens, personal data, or sensitive network details.

## Author

**Faisol Daud** — Cybersecurity student building practical skills in network security and SOC analysis.

- GitHub: [@Ph3n1cX](https://github.com/Ph3n1cX)
- LinkedIn: [Faisol Daud](https://www.linkedin.com/in/faisol-daud-268086337/)

---

*Document the evidence. Explain the alert. Be honest about what the test proves.*