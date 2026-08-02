# Call Flow

## Objective

Understand how calls are routed between Cisco Webex Calling, Cisco Catalyst 8000V (CUBE), Twilio Elastic SIP Trunk, and the PSTN.

---

# High-Level Call Flow

```
Webex App (11005)
        │
        │ SIP over TLS
        ▼
Cisco Webex Calling Cloud
        │
        │ Registration-Based SIP Trunk
        ▼
Cisco Catalyst 8000V (CUBE)
        │
        │ SIP over TLS
        ▼
Twilio Elastic SIP Trunk
        │
        ▼
Public Switched Telephone Network (PSTN)
```

---

# Internal Call Flow

```
Webex User (11005)

↓

Cisco Webex Calling

↓

Webex User (11002)
```

Internal calls remain within Cisco Webex Calling and do not traverse the Local Gateway.

---

# PSTN Outbound Call Flow

```
Webex App

↓

Cisco Webex Calling

↓

Cisco CUBE

↓

Twilio

↓

PSTN
```

---

# PSTN Inbound Call Flow

```
PSTN

↓

Twilio

↓

Cisco CUBE

↓

Cisco Webex Calling

↓

Webex User
```

---

# SIP Components

- Cisco Webex Calling
- Cisco Catalyst 8000V (CUBE)
- SIP UA
- Dial Peers
- Voice Class DPG
- Voice Class Tenant
- Twilio Elastic SIP Trunk

---

# Security

- SIP over TLS
- Secure RTP (SRTP)
- PKI Certificates
- Trustpoint Authentication

---

# Validation

The following tests were successfully completed:

- Internal Extension Calling
- PSTN Outbound Calling
- SIP Registration
- Secure SIP Signaling
