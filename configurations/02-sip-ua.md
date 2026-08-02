# SIP UA Configuration

## Objective

Configure the SIP User Agent (SIP UA) on the Cisco Catalyst 8000V (CUBE) to securely register with Cisco Webex Calling as a Registration-Based Local Gateway.

---

## Purpose

The SIP UA configuration is responsible for:

- SIP registration with Cisco Webex Calling
- Authentication
- TLS signaling
- Registrar configuration
- Outbound proxy configuration
- Secure SIP communication

---

## Example Configuration

```cisco
sip-ua

 transport tcp tls v1.2

 registrar dns:<Webex Registrar>

 outbound-proxy dns:<Webex Outbound Proxy>

 retry register 10

 timers register 300

 connection-reuse
```

---

## Notes

- SIP signaling uses TLS 1.2.
- Registration is performed against Cisco Webex Calling.
- Authentication credentials and certificates have been omitted for security.
- Connection reuse improves SIP efficiency.
- Registrar and outbound proxy values are environment-specific.
