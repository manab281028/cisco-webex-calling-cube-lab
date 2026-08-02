# Troubleshooting Guide

## Overview

During the implementation of this Cisco Webex Calling lab, several issues were encountered and successfully resolved. This section documents the troubleshooting process and the resolution for each issue.

---

# Issue 1 – CUBE Registration Failed

### Symptoms

- SIP trunk not registering
- Trunk status Offline
- Registration unsuccessful

### Verification

```cisco
show sip-ua register status
```

### Resolution

- Verified SIP UA configuration
- Verified registration credentials
- Verified DNS resolution
- Verified TLS certificates
- Confirmed successful registration in Cisco Control Hub

---

# Issue 2 – Webex Phone Services Disconnected

### Symptoms

- Phone Services Disconnected
- Softphone Disconnected
- Unable to place internal calls

### Resolution

- Verified user licensing
- Confirmed Webex Calling Professional license
- Verified extension assignment
- Re-signed into the Webex App
- Confirmed successful phone service registration

---

# Issue 3 – Internal Calls Failed

### Symptoms

- Extension 11005 unable to call 11002

### Resolution

- Verified user configuration
- Verified dial peers
- Confirmed user provisioning
- Verified Webex Calling registration

---

# Issue 4 – PSTN Calls Failed

### Symptoms

- Calls failed to reach the PSTN

### Resolution

- Verified outbound dial peers
- Verified Twilio SIP Trunk
- Confirmed destination patterns
- Verified SIP signaling

---

# Issue 5 – Twilio Error 21264

### Symptoms

Twilio rejected outbound calls.

### Root Cause

Caller ID was not verified.

### Resolution

Verified the outbound caller ID in Twilio Console.

Outbound PSTN calling completed successfully.

---

# Issue 6 – SIP Registration Verification

### Verification Commands

```cisco
show sip-ua register status

show dial-peer voice summary

show voice class tenant

show voice class dpg

show call active voice brief
```

---

# Lessons Learned

- Verify registration before troubleshooting dial peers.
- Confirm licensing before troubleshooting the Webex App.
- Validate SIP registration from both CLI and Control Hub.
- Verify Twilio caller ID before testing PSTN calls.
- Troubleshoot from the client toward the PSTN instead of assuming the gateway is at fault.
