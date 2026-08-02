# Voice Service VoIP Configuration

## Objective

Configure the Cisco Catalyst 8000V (CUBE) as a Registration-Based Local Gateway (RBLG) for Cisco Webex Calling.

---

## Purpose

The `voice service voip` configuration enables SIP call processing on the CUBE and defines how voice traffic is handled.

It is responsible for:

- Enabling SIP-to-SIP call routing
- RTP media handling
- SIP supplementary services
- Fax support
- Voice protocol settings

---

## Example Configuration

```cisco
voice service voip

 allow-connections sip to sip

 media bulk-stats

 rtp-port range 16384 32766

 no supplementary-service sip refer

 no supplementary-service sip handle-replaces

 fax protocol t38 version 0 ls-redundancy
```

---

## Notes

- SIP signaling uses TLS.
- RTP carries the media stream.
- This configuration is part of the Registration-Based Local Gateway deployment.
- Sensitive information such as certificates, passwords, and authentication credentials has been intentionally omitted.
