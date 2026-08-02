# Twilio Elastic SIP Trunk

## Objective

Configure Twilio Elastic SIP Trunk to provide PSTN connectivity for Cisco Webex Calling through Cisco Catalyst 8000V (CUBE).

---

## Overview

Twilio acts as the PSTN provider in this lab. Outbound calls from Webex Calling are routed through Cisco CUBE and then forwarded to Twilio, which terminates the call to the Public Switched Telephone Network (PSTN).

---

## Call Flow

Webex Calling

↓

Cisco CUBE

↓

Twilio Elastic SIP Trunk

↓

PSTN

---

## Configuration Summary

The Twilio SIP Trunk was configured with:

- SIP Domain
- Authentication
- Secure SIP Signaling
- Outbound Call Routing
- Caller ID Verification

---

## Verification

The following items were verified successfully:

- Outbound PSTN Calls
- SIP Signaling
- Media Flow
- Twilio Call Logs

---

## Troubleshooting

During implementation, the following issue was encountered:

**Twilio Error 21264**

Reason:

Caller ID was not verified.

Resolution:

Verified the caller ID within the Twilio Console and successfully completed outbound PSTN calling.

---

## Result

- PSTN calling was successfully established.
- Twilio call logs confirmed successful call completion.
- Media and signaling were verified.

## Example Configuration

```cisco
dial-peer voice 200 voip
 description Outbound to Twilio
 session protocol sipv2
 session target dns:<Twilio SIP Domain>
 voice-class codec 1
 dtmf-relay rtp-nte
 no vad
```

## Screenshots

### Twilio Elastic SIP Trunk

![Twilio SIP Trunk](../screenshots/07-pstn-call-success.png)



## Notes

- SIP signaling is secured using TLS.
- PSTN calls are routed through Twilio Elastic SIP Trunk.
- Verify Twilio logs if outbound calls fail.
- Ensure dial peers and codecs match provider requirements.
