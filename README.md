# Cisco Webex Calling + CUBE Registration-Based Local Gateway Lab
![Cisco](https://img.shields.io/badge/Cisco-CUBE-1BA0D7?style=for-the-badge&logo=cisco&logoColor=white)
![Webex](https://img.shields.io/badge/Webex-Calling-00BCEB?style=for-the-badge)
![Azure](https://img.shields.io/badge/Microsoft-Azure-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)
![Twilio](https://img.shields.io/badge/Twilio-SIP%20Trunk-F22F46?style=for-the-badge&logo=twilio&logoColor=white)
![TLS](https://img.shields.io/badge/SIP-TLS-success?style=for-the-badge)
![SRTP](https://img.shields.io/badge/Media-SRTP-orange?style=for-the-badge)

---

## Table of Contents

- Project Overview
- Lab Objectives
- Lab Architecture
- Technology Stack
- Deployment Workflow
- Repository Structure
- Configuration Files
- Documentation
- Screenshots
- Verification
- Troubleshooting
- Lessons Learned

---

## Project Overview

This project demonstrates a complete end-to-end deployment of Cisco Webex Calling using Cisco Catalyst 8000V (CUBE) configured as a Registration-Based Local Gateway.

The lab was built from scratch in Microsoft Azure and integrated with Cisco Webex Control Hub and Twilio PSTN to validate both internal extension calling and external PSTN connectivity.

---

## Lab Objectives

- Deploy Cisco Catalyst 8000V (CUBE)
- Configure Registration-Based Local Gateway
- Register CUBE with Cisco Webex Calling
- Configure SIP Trunk
- Configure Dial Peers
- Configure Voice Service VoIP
- Integrate Twilio Elastic SIP Trunk
- Enable PSTN Calling
- Verify SIP Registration
- Validate Internal Calls
- Validate PSTN Calls
- Troubleshoot SIP Registration and Calling Issues

- ---

# Lab Architecture

The following diagram illustrates the complete call flow between Cisco Webex Calling, Cisco CUBE (Catalyst 8000V), and Twilio PSTN.

> *(Architecture diagram will be displayed below once uploaded to the diagrams folder.)*

<p align="center">
<img src="diagrams/architecture.png" width="1000">
</p>


---

# Technology Stack

| Component | Technology |
|-----------|------------|
| Cloud Platform | Microsoft Azure |
| Voice Gateway | Cisco Catalyst 8000V (CUBE) |
| UC Platform | Cisco Webex Calling |
| Administration | Cisco Control Hub |
| PSTN Provider | Twilio Elastic SIP Trunk |
| SIP Registration | Registration-Based Local Gateway |
| Signaling | SIP over TLS |
| Media | RTP/SRTP |
| Security | TLS Certificates |
| Verification | CLI + Control Hub + Twilio Logs |

---

# Key Features

- Registration-Based Local Gateway (Cisco CUBE)
- Cisco Webex Calling Integration
- Twilio Elastic SIP Trunk Integration
- Internal Extension Calling
- PSTN Calling
- SIP over TLS
- Secure RTP (SRTP)
- Dial Peer Configuration
- Voice Service VoIP Configuration
- SIP Registration Verification
- End-to-End Call Validation
- CLI Verification Commands
- Control Hub Administration
- Troubleshooting and Issue Resolution

## Repository Structure

```text
cisco-webex-calling-cube-lab/
│
├── README.md
├── LICENSE
│
├── diagrams/
│   └── Architecture Diagram
│
├── screenshots/
│   ├── 00-architecture-diagram.png
│   ├── 01-control-hub-trunk-online.png
│   ├── 02-cube-sip-registration.png
│   ├── 03-users-and-extensions.png
│   ├── 04-webex-calling-license.png
│   ├── 05-webex-softphone-connected.png
│   ├── 06-internal-call-success.png
│   └── 07-pstn-call-success.png
│
├── configurations/
│   ├── 01-voice-service-voip.md
│   ├── 02-sip-ua.md
│   ├── 03-dial-peers.md
│   ├── 04-webex-registration.md
│   ├── 05-twilio-sip-trunk.md
│   └── 06-security-and-tls.md
│
└── docs/
    ├── 01-deployment-guide.md
    ├── 02-call-flow.md
    ├── 03-troubleshooting.md
    └── 04-lessons-learned.md
```
## Skills Demonstrated

- Cisco Webex Calling Administration
- Cisco Catalyst 8000V (CUBE) Configuration
- Registration-Based Local Gateway (RBLG)
- SIP over TLS Configuration
- Twilio Elastic SIP Trunk Integration
- Voice Service VoIP Configuration
- SIP UA Configuration
- Dial Peer Configuration
- Cisco Control Hub Administration
- Internal Extension Calling
- PSTN Call Routing
- TLS and SRTP Security
- SIP Registration Verification
- CLI Troubleshooting
- End-to-End Voice Validation
