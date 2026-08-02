# Global Configuration

## Purpose

The global configuration establishes the foundational settings required for Cisco Catalyst 8000V (CUBE) to operate as a secure Session Border Controller (SBC) and Registration-Based Local Gateway (RBLG) for Cisco Webex Calling.

These settings include system identity, networking, DNS resolution, security, PKI, interface configuration, and global voice services that support SIP signaling and media processing.

---

## Overview

The global configuration prepares the Cisco CUBE before any SIP-specific configuration is applied.

It includes:

- Hostname
- Interface Configuration
- IP Addressing
- DNS Configuration
- NTP Configuration
- PKI Trustpoints
- Certificate Management
- SIP Transport
- Voice Service Initialization
- Security Settings

  ## Components Configured

- Hostname
- Domain Name
- Interface Configuration
- IP Address Assignment
- DNS Servers
- NTP Servers
- PKI Trustpoints
- Certificate Management
- Secure SIP Transport
- Voice Service Initialization
- Logging
- Licensing
- Default Routing
- Management Access

## Example Configuration

The following is a sanitized version of the global Cisco Catalyst 8000V (CUBE) configuration used in this lab.

```cisco
	voice service voip
	  media bulk-stats
	  rtp-port range 16384 32766
	  allow-connections sip to sip
	  no supplementary-service sip refer
	  no supplementary-service sip handle-replaces
	  fax protocol t38 version 0 ls-redundancy 0 hs-redundancy 0 fallback none
	  trace
	  media statistics
	 stun
	  stun flowdata agent-id 1 boot-count 4
	  stun flowdata shared-secret 0 Password123$
	  exit
	 sip
	  asymmetric payload full
	  early-offer forced
	  g729 annexb-all
  exit 
```
