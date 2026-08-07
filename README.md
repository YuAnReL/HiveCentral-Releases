# HiveCentral Release Evidence

This public repository stores release evidence and corresponding source for
[HiveCentral](https://github.com/YuAnReL/HiveCentral), a local-first terminal
workspace for multi-agent projects.

HiveCentral is distributed through npm. This repository is not an installer,
update feed, or second package manager, and HiveCentral does not query it to
discover or install updates.

## Availability

The initial npm release is being prepared. Until the
[`hivecentral` npm package](https://www.npmjs.com/package/hivecentral) exists and
has passed anonymous installed-product acceptance, no stable public release is
advertised.

The first supported native target is macOS on Apple Silicon (`darwin-arm64`).
Apple Developer ID signing and notarization may be added as future hardening;
they are not prerequisites for the initial npm channel.

## Install And Manage

After the first stable version is published:

```sh
npm install -g hivecentral
hivecentral
```

HiveCentral also supports a temporary invocation through npm:

```sh
npx hivecentral
```

npm owns the complete package lifecycle:

```sh
npm install -g hivecentral@latest
npm install -g hivecentral@<version>
npm uninstall -g hivecentral
```

Normal npm uninstall removes the package and command link while preserving
HiveCentral Application Home and its Provider, Project, and Session data.

## Release Evidence

Each public version may include:

- the byte-identical npm package tarball and its SHA-256 checksum;
- a version-matched corresponding-source archive and checksum;
- an SPDX SBOM and license inventory;
- the package source notice and release metadata;
- the exact source commit and commit-pinned build/workflow identity.

Assets for an existing version are immutable. A rerun may reuse them only when
their allowlist, source identity, and bytes match exactly.

The development repository is currently private, so npm provenance is not
claimed for these builds. Public corresponding source and the evidence above
provide the release audit trail. If the source repository becomes public,
future GitHub Actions trusted publications may additionally carry npm
provenance.

## Recovery Use

The mirrored tarball is an audit and registry-outage fallback. If a maintainer
directs users to a specific verified release asset, npm can install that exact
tarball and still own removal and version replacement:

```sh
npm install -g /absolute/path/to/hivecentral-<version>.tgz
```

There is no supported `curl | sh`, Manifest v2, self-updater, or custom
uninstaller path.

## License And Source

HiveCentral is distributed under `GPL-3.0-only`. Every public binary release
must have an anonymously readable, version-matched corresponding-source archive
in its release evidence.
