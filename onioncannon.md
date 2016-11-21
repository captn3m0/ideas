# onioncannon

Similar to [pushjet](https://pushjet.io/), but with the following idea:

- Push all app notifications to other clients
- Add/Remove clients at will
- All traffic reaches a central server
- All traffic is encrypted at source, but the uuid of the client can be used to talk to them

## Use Case

- I wanted to build a simple "auto-type OTP" Chrome Extension.
- Without using pushbullet (Should be FOSS)
- Without giving my OTP to anyone else (should be E2E)
- Without having to worry about NATs and firewalls (should be a publicly hosted service)

Somewhat related to the idea is http://github.com/decant, which allows me to build the "read SMS" part of it.

What I envision is essentially a simple client-registration protocol:

- `[Device A]` generates a UUID.
- `[Device B]` generates a UUID.
- B generates a QR code using the UUID.
- A scans the QR code to get the UUID and pushes a sample event.
- B gets the event, and can decide to push events to A if needed.

The QR code includes:

1. The UUID of a client
2. A public key fingerprint of the PGP key of the client
3. Metadata containing:
- Public Key
- URL where the public key can be found
- Misc Client Information

Any client who scans this can now start sending encrypted data to the client.

The nice thing is that you can transmit data however between these two parties, once it is encrypted. Use GCM/pusher if you wish.
