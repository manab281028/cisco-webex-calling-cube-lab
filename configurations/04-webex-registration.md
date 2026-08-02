# Cisco Webex Calling Registration

## Objective

Register Cisco Catalyst 8000V (CUBE) as a Registration-Based Local Gateway (RBLG) with Cisco Webex Calling.

---

## Overview

In this lab, the Cisco CUBE was configured to register with Cisco Webex Calling using a Registration-Based SIP Trunk.

Once registration completed successfully:

- The SIP trunk status changed to **Online** in Cisco Control Hub.
- CUBE became available as the Local Gateway.
- Calls from Webex users could be routed through CUBE.
- PSTN calls could be forwarded to Twilio.

---

## Registration Process

1. Create a Registration-Based Trunk in Cisco Control Hub.
2. Download the generated registration details.
3. Configure the SIP UA on Cisco CUBE.
4. Import the required certificates.
5. Configure SIP registration credentials.
6. Verify successful registration.

---

## Verification

The following CLI command was used to verify registration:

```cisco
show sip-ua register status
```

Expected Result

```
Status : Registered
```

---

## Control Hub Verification

Navigate to:

Calling
→ PSTN & Routing
→ Trunks

Expected Status:

```
Online
```

---

## Notes

- TLS was used for SIP signaling.
- Registration was verified using both the Cisco CLI and Control Hub.
- Authentication details and certificates have been omitted for security.
