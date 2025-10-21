# SecShare
**SecShare** — secure file sharing

## About
SecShare lets you securely share files between two computers using end-to-end encryption over a direct TCP (peer-to-peer) connection — no server required.

## Download
Latest release (versioned): https://github.com/hichem2216/SecShare/releases/

## Installation
1. Download `SecShare-<version>_installation.exe` (or `.zip`, `.dmg`, etc.)
2. Verify checksum and signature (see **Security** below).
3. Run installer / unpack archive.

## Features
- **E2EE (ECC → AES)** — Ephemeral Elliptic-Curve Diffie–Hellman for key agreement, then symmetric encryption (AES-GCM) for payload confidentiality and integrity.
- **Signature (ECDSA)** — Messages and releases are signed with ECDSA to guarantee authenticity and non-repudiation.
- **Fingerprint** — SHA-256 fingerprint of the public key is published so peers can verify identity using code QR.
- **Serverless (TCP-only)** — Peer-to-peer direct transfers over TCP (no central server required). 

## Screenshots
(link to `/assets/screenshots/...`)

## Security / Verification
- SHA256 checksums published in each release and in `CHECKSUMS-<version>.txt`.
- GPG signatures provided: `SECURESHARE-<version>.tar.gz.sig`.
- How to verify:
  ```bash
  sha256sum SecShare-<version>_installation.exe
  gpg --verify SecShare-<version>.sig SecShare-<version>-win-x64.exe# SecShare
If GPG shows a “Good signature” message and the checksum matches,
your downloaded file is authentic and safe to use.
