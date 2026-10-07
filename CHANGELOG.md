# Changelog

## v0.4.26 — 2026-10-07

Stable Windows installer for CP30/UR4, source
`4445cbd1fa407a6b2e34774b46e2a55b70665759`.
Read delivery is grouped at a minimum60-second cadence; UR4 configuration is
updated on demand, and CP30 polling/results use bounded groups with durable ACK
recovery. Uncertain physical work is not automatically replayed.

The single ZIP contains the installer, its checksum, a production manifest and
installation instructions. Published/downloaded bytes match the verified build;
approved native SDKs are preserved. No service or hardware installation is implied.
Staging is a separate prerelease channel. Historical releases below are preserved.

## v0.1.0

Initial public Windows Device Agent binary release for CP30/SR160 validation.

Security defaults:

- Service runs as `NT SERVICE\RfidEdgeHubDeviceAgent` by default.
- Installer applies restrictive ACLs to app, config and data folders.
- Service does not auto-start unless explicitly requested.
- Start is blocked while the token placeholder is still present.
- Package excludes source code and debug symbol files.
