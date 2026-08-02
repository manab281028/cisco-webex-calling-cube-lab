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
## Verification

### Command

```cisco
show sip-ua register status
```

### Example Output

```text
CUBE# show sip-ua register status

Registrar: sip-us10.wxc-di.webex.com
State: REGISTERED
Transport: TLS
Expires: 3600
```

### Screenshot

![SIP Registration](../screenshots/02-cube-sip-registration.png)

- SIP signaling uses TLS 1.2.
- Registration is performed against Cisco Webex Calling.
- Authentication credentials and certificates have been omitted for security.
- Connection reuse improves SIP efficiency.
- Registrar and outbound proxy values are environment-specific.
