# Cisco Webex Calling Registration

## Objective

Register Cisco Catalyst 8000V (CUBE) as a Registration-Based Local Gateway (RBLG) with Cisco Webex Calling.

---

## Overview

Cisco CUBE was configured to register securely with Cisco Webex Calling using a Registration-Based SIP Trunk. Once registration completed successfully, the Local Gateway became available to route calls between Webex Calling and the PSTN.

---

## Registration Workflow

1. Create a Registration-Based Trunk in Cisco Control Hub.
2. Download the registration details.
3. Configure SIP UA on Cisco CUBE.
4. Configure TLS certificates.
5. Configure SIP registration credentials.
6. Verify successful registration.

---

## Verification Commands

```cisco
show sip-ua register status
```

Expected Output

```
Status : Registered
```

---

## Control Hub Verification

Navigate to:

Calling
→ PSTN & Routing
→ Trunks

Expected Status

```
Online
```

---

## Result

- Cisco CUBE successfully registered with Webex Calling.
- SIP trunk status changed to **Online**.
- Internal and PSTN calls were successfully established.

---

## Related Screenshots

- `01-control-hub-trunk-online.png`
- `02-cube-sip-registration.png`
