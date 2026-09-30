# SEEKER Updates

This repository hosts approved SEEKER desktop update metadata and release assets. The SEEKER application trusts releases signed by the Ed25519 public key in `update-public-key.pem` and independently verifies each downloaded installer SHA-256.

## Publish a release

1. Build and smoke-test the macOS ARM64, macOS x64, and Windows x64 installers on their native operating systems.
2. Upload approved installer files to a GitHub release in this repository or another HTTPS location.
3. Create a `latest.json` object matching the schema below. Asset keys are `mac-arm64`, `mac-x64`, and `windows-x64`. Include each exact filename, HTTPS URL, and SHA-256 digest.
4. Sign the JSON payload (excluding `signature`) with the offline Ed25519 private key. Keep that private key out of this repository and back it up securely.
5. Commit the signed `latest.json` to `main`. The installed app checks this raw file.

Example payload (replace placeholders; this is not a published update):

```json
{
  "schemaVersion": 1,
  "product": "SEEKER",
  "latestVersion": "0.4.0-beta.1",
  "minimumSupportedVersion": "0.4.0-beta.1",
  "releaseNotes": "Release notes here.",
  "releaseNotesUrl": "https://github.com/Autonomous-Capital-Allocation-System/SEEKER-Updates/releases",
  "assets": {
    "mac-arm64": { "filename": "SEEKER-0.4.0-beta.1-arm64.dmg", "url": "https://example.invalid/arm64.dmg", "sha256": "<64 lowercase hex characters>" },
    "mac-x64": { "filename": "SEEKER-0.4.0-beta.1-x64.dmg", "url": "https://example.invalid/x64.dmg", "sha256": "<64 lowercase hex characters>" },
    "windows-x64": { "filename": "SEEKER-0.4.0-beta.1-x64.exe", "url": "https://example.invalid/windows.exe", "sha256": "<64 lowercase hex characters>" }
  },
  "signature": "<base64 Ed25519 signature over canonical JSON payload>"
}
```

No `latest.json` is published until a release is approved and all three platform installers are available. Do not publish resumes, mailbox data, OAuth client files, access tokens, or the update signing key.
