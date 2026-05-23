# RFID Edge Hub Agent Releases

Public binary releases for the RFID Edge Hub Windows Device Agent.

This repository intentionally does not contain application source code. It is only used to publish versioned installable packages for hardware PCs that run CP30/SR160 workflows.

## Current Release

- Version: `0.1.0`
- Package: `device-agent-windows-cp30-sr160-0.1.0.zip`
- SHA256: published next to the ZIP as `device-agent-windows-cp30-sr160-0.1.0.zip.sha256.txt`

Download from the Releases page:

https://github.com/ddacol24/rfid-edge-hub-agent-releases/releases

## Security Checklist

1. Download the ZIP and `.sha256.txt` from the same GitHub Release.
2. Verify the hash before installing:

   ```powershell
   Get-FileHash .\device-agent-windows-cp30-sr160-0.1.0.zip -Algorithm SHA256
   Get-Content .\device-agent-windows-cp30-sr160-0.1.0.zip.sha256.txt
   ```

3. Unzip on the Windows PC connected to CP30/SR160.
4. Run `scripts\install-service.ps1` from elevated PowerShell.
5. Edit `C:\RFIDEdgeHub\device-agent\device-agent.json` locally.
6. Paste the one-time agent token generated in RFID Edge Hub.
7. Test with `scripts\run-console.ps1` before starting the service.
8. Start the service only after heartbeat is visible in the web UI.

Never publish or share `device-agent.json` after inserting a real token.

## What Is In The ZIP

- Windows x64 self-contained agent executable and runtime files.
- Secure install/uninstall scripts.
- Console run script.
- SR160 bridge script.
- Diagnostics script.
- Installation README.
- Token-free config template.

## What Is Not In This Repository

- Source code.
- Private server configuration.
- Real agent tokens.
- Customer data.
- Hardware credentials.
