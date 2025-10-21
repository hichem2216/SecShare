**SecShare** — secure file sharing

## About
SecShare lets you securely share files between two computers using end-to-end encryption over a direct TCP (peer-to-peer) connection — no server required.

## Download
Latest release (versioned): https://github.com/<your-account>/SecShare/releases

## Installation
1. Download `SecShare-<version>-win-x64.exe` (or `.zip`, `.dmg`, etc.)
2. Verify checksum and signature (see **Security** below).
3. Run installer / unpack archive.

## Features
- **E2EE (ECC → AES)** — Ephemeral Elliptic-Curve Diffie–Hellman for key agreement, then symmetric encryption (AES-GCM) for payload confidentiality and integrity.
- **Signature (ECDSA)** — Messages and releases are signed with ECDSA to guarantee authenticity and non-repudiation.
- **Fingerprint** — SHA-256 fingerprint of the public key is published so peers can verify identity using code QR.
- **Serverless (TCP-only)** — Peer-to-peer direct transfers over TCP (no central server required). 

## Screenshots
(Insert images or link to `/assets/screenshots/...`)

## Security / Verification
- SHA256 checksums published in each release and in `CHECKSUMS.txt`.
- GPG signatures provided: `SECURESHARE-<version>.tar.gz.sig`.
- How to verify:
  ```bash
  sha256sum SecShare-<version>-win-x64.exe
  gpg --verify SecShare-<version>.sig SecShare-<version>-win-x64.exe# SecShare
