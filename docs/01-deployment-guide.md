# Cisco Webex Calling Deployment Guide

## Project Overview

This project demonstrates the deployment of Cisco Webex Calling using Cisco Catalyst 8000V (CUBE) as a Registration-Based Local Gateway (RBLG) integrated with Twilio Elastic SIP Trunk for PSTN connectivity.

The deployment was implemented in a Microsoft Azure lab environment and validated using Cisco Webex App clients.

---

# Lab Environment

| Component | Details |
|------------|---------|
| Cloud Platform | Microsoft Azure |
| Voice Gateway | Cisco Catalyst 8000V (CUBE) |
| Collaboration Platform | Cisco Webex Calling |
| Administration | Cisco Control Hub |
| PSTN Provider | Twilio Elastic SIP Trunk |
| SIP Security | TLS |
| Media Security | SRTP |

---

# Lab Objectives

- Deploy Cisco Catalyst 8000V
- Configure Cisco Webex Calling
- Configure Registration-Based Local Gateway
- Configure SIP UA
- Configure Voice Service VoIP
- Configure Dial Peers
- Configure Twilio SIP Trunk
- Validate Internal Calling
- Validate PSTN Calling
- Perform End-to-End Verification

---

# Deployment Workflow

1. Deploy Cisco Catalyst 8000V in Microsoft Azure.
2. Configure licensing and initial device setup.
3. Configure PKI and Trustpoints.
4. Configure Voice Service VoIP.
5. Configure SIP UA.
6. Configure Webex Registration.
7. Configure Dial Peers.
8. Configure Twilio SIP Trunk.
9. Register Cisco CUBE with Webex Calling.
10. Verify successful registration.
11. Test Internal Extension Calling.
12. Test PSTN Calling.

---

# Verification

Deployment was verified using:

- Cisco CLI
- Cisco Control Hub
- Webex App
- Twilio Console

---

# Result

The deployment successfully established secure SIP connectivity between Cisco Webex Calling and the PSTN using Cisco Catalyst 8000V as a Registration-Based Local Gateway.
