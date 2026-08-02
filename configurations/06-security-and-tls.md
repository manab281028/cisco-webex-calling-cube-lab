# Security and TLS Configuration

## Objective

Secure SIP signaling between Cisco Webex Calling, Cisco Catalyst 8000V (CUBE), and Twilio using Transport Layer Security (TLS) and Secure Real-Time Transport Protocol (SRTP).

---

## Overview

Security is a critical component of Cisco Webex Calling deployments. In this implementation, TLS was used to encrypt SIP signaling while SRTP was used to protect voice media.

---

## Security Components

- TLS 1.2
- SIP over TLS
- Secure RTP (SRTP)
- PKI Certificates
- Trustpoint Configuration
- Certificate Validation
- SIP Authentication

---

## Components Configured

- PKI
- Trustpoint
- CA Certificate
- SIP TLS
- SRTP
- SIP UA Security
- Secure Registration

---

## Verification

The following items were verified:

- Secure SIP Registration
- TLS Handshake
- Encrypted SIP Signaling
- Successful Secure Call Setup

---

## Best Practices

- Use trusted CA certificates.
- Protect private keys.
- Use TLS 1.2 or later.
- Enable SRTP for media encryption.
- Regularly renew certificates.

---

## Result

- SIP signaling was encrypted using TLS.
- Media streams were protected using SRTP.
- Cisco Webex Calling successfully communicated with Cisco CUBE over a secure connection.

## Example Configuration

```cisco
crypto pki trustpoint WEBEX-CA
 enrollment terminal
 revocation-check none

voice service voip
 sip
  transport tcp tls v1.2

srtp
```
## Notes

- TLS encrypts SIP signaling.
- SRTP encrypts RTP media streams.
- Certificates must remain valid for successful registration.
- Trustpoints should reference the correct Certificate Authority.

## Screenshots

![TLS Configuration](../screenshots/08-tls-configuration.png)
