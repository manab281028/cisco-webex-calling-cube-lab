# Tenant Configuration

## Purpose

The tenant configuration defines how Cisco CUBE connects to external SIP services. It specifies transport protocols, TLS parameters, media handling, SRTP requirements, and SIP server behavior for individual SIP providers such as Cisco Webex Calling and Twilio Elastic SIP Trunk.

## Overview

In this lab, tenant configuration was used to establish secure SIP connectivity between Cisco CUBE and Cisco Webex Calling using a Registration-Based Local Gateway (RBLG). Separate tenant definitions were configured for Webex Calling and Twilio Elastic SIP Trunk, allowing Cisco CUBE to securely route internal extension calls and external PSTN calls.

## Components Configured

- SIP Tenant Definition
- Registrar Server
- Outbound Proxy
- Transport Protocol (TLS)
- SRTP Media Encryption
- SIP Server Configuration
- Authentication Credentials
- Connection Reuse
- Keepalive Timers
- Codec Preferences

## Example Configuration

- voice class tenant 100

 registrar dns:xxxxxxxxxxxxxxxx

 outbound-proxy dns:xxxxxxxxxxxxxxxx

 connection-reuse

 transport tcp tls

 srtp

 bind control source-interface GigabitEthernet1

 bind media source-interface GigabitEthernet1


 ## Verification

The tenant configuration was verified using the following Cisco IOS XE CLI commands:

```cisco
show running-config | section voice class tenant

show sip-ua register status

show call active voice brief
```

### Expected Result

- Tenant configuration is present in the running configuration.
- Cisco CUBE successfully registers with Cisco Webex Calling.
- SIP signaling uses TLS.
- Calls are successfully established through the configured tenant.

## Notes

- Separate tenant configurations were used for Cisco Webex Calling and Twilio Elastic SIP Trunk.
- TLS was used to secure SIP signaling.
- SRTP was enabled for secure media transmission.
- Configuration values such as domains, credentials, and certificates have been sanitized before publishing.
