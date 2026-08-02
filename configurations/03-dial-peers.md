# Dial Peers Configuration

## Objective

Configure inbound and outbound dial peers to route calls between Cisco Webex Calling, CUBE, and the Twilio Elastic SIP Trunk.

---

## Purpose

Dial peers determine how calls are matched and routed through the Cisco CUBE.

They are responsible for:

- Matching inbound calls
- Routing outbound PSTN calls
- Routing internal Webex calls
- Selecting SIP destinations
- Codec negotiation

---

## Example Configuration

```cisco
dial-peer voice 100 voip

 description Incoming from Webex

 session protocol sipv2

 incoming uri request

 voice-class codec 1

 dtmf-relay rtp-nte

 no vad
```

```cisco
dial-peer voice 200 voip

 description Outbound to Twilio

 destination-pattern 9T

 session protocol sipv2

 session target dns:<Twilio SIP Domain>

 voice-class codec 1

 dtmf-relay rtp-nte

 no vad
```

---

## Notes

- Separate dial peers are used for inbound and outbound calls.
- Codec preferences should match the service provider requirements.
- Destination patterns vary based on the deployment.
- Actual SIP domains and phone numbers have been omitted for security.
