# HiveCentral Releases

This repository is the public distribution origin for HiveCentral release
artifacts. Product development and issue tracking live in the
[HiveCentral source repository](https://github.com/YuAnReL/HiveCentral), and a
complete corresponding source archive is attached to each public release.

## Availability

The release channel is being prepared. No stable public release is available
until a signed and notarized version appears on the
[Releases page](https://github.com/YuAnReL/HiveCentral-Releases/releases).

## Install

After the first stable release is published, supported macOS Apple Silicon
systems can install the latest version with:

```sh
curl -fsSL --proto '=https' --proto-redir '=https' --tlsv1.2 \
  https://github.com/YuAnReL/HiveCentral-Releases/releases/latest/download/install.sh | sh
```

The stable bootstrap resolves an immutable release manifest, verifies the
version-pinned installer and product archive, and delegates installation to the
verified installer.

## Supported Platform

- macOS on Apple Silicon (`darwin-arm64`)
- Signed Developer ID Application payloads
- Apple notarization required for public stable releases

## Release Integrity

Stable releases are produced by the HiveCentral release workflow. A release may
include the stable bootstrap, version-pinned installer, product archive,
checksums, update manifests, license inventory, source archive, and
notarization evidence. Published assets should not be edited or replaced
manually.

Installation behavior, security boundaries, and troubleshooting documentation
are included in the corresponding release source archive.
