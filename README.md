# Cisco Webex Calling + CUBE Registration-Based Local Gateway Lab

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
