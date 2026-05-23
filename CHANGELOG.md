# Changelog

## v0.1.0

Initial public Windows Device Agent binary release for CP30/SR160 validation.

Security defaults:

- Service runs as `NT SERVICE\RfidEdgeHubDeviceAgent` by default.
- Installer applies restrictive ACLs to app, config and data folders.
- Service does not auto-start unless explicitly requested.
- Start is blocked while the token placeholder is still present.
- Package excludes source code and debug symbol files.
