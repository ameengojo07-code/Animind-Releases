# ANIMIND Studio Releases

This repository is the **public distribution channel only** for official ANIMIND Studio stable updates.

- Main source code remains in the private `ameengojo07-code/blender-ai` repository.
- Only approved, production-ready update archives and their publisher-signed JSON manifest belong here.
- Never upload source archives, private keys, API credentials, personal access tokens, user settings, project files, or test data.
- The ANIMIND updater accepts only HTTPS release URLs hosted on GitHub and verifies the Ed25519 manifest signature before trusting release metadata.
- The updater also verifies the archive byte size and SHA-256, rejects unsafe ZIP contents, and requires user approval before installation.

## Current status

The production Ed25519 public key has been pinned in the private application source. No stable ANIMIND release has been published here yet. The updater remains inactive until a production-ready package and signed manifest are published, the public feed is configured, and installation/update/rollback are tested on the supported Windows + Blender environment.

## Expected release files

For each approved stable version, publish:

1. `ANIMIND_Update_vX.Y.Z.zip` — update-only archive with `desktop/` and `blender_addon/` at its root.
2. `manifest.json` — signed stable-release manifest referencing that exact archive, its byte size, and SHA-256.

Publish the archive as a GitHub Release asset and the signed manifest at a stable public HTTPS URL. Do not publish a manifest with placeholder values or an unsigned manifest.

## Security

If you find a suspected malicious or compromised release, do not install it. Report it to the repository owner and wait for a verified replacement. The release-signing private key must remain offline or in a protected secret store and must never be committed here.
