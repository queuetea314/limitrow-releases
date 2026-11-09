# Limitrow releases

Signed and notarized builds of [Limitrow](https://limitrow.appsurd.lol) — the limits of your AI
coding assistants on a panel by the Dock.

This repository holds release files only: the disk images, their SHA-256 checksums and the
release notes. The source code is not public.

- **Download:** <https://limitrow.appsurd.lol/download> always points to the newest release.
- **Requirements:** macOS 15 or later, Apple Silicon or Intel.
- **Updates:** Limitrow checks <https://limitrow.appsurd.lol/updates/appcast.xml> and asks before
  installing anything.

Every file is signed with Developer ID (team `5QVM5Y9RYP`) and notarized by Apple. To check a
download:

```bash
shasum -a 256 Limitrow-*.dmg   # compare with SHA256SUMS.txt in the same release
spctl -a -vv -t open --context context:primary-signature Limitrow-*.dmg
```
