# SCARA Robot updates

This public repository distributes Windows application packages for SCARA Robot. Source code remains private.

The application reads `public/update/manifest.json`. The manifest contains a version, a GitHub Release download URL, and a SHA-256 digest. The updater checks the digest and application version before replacing installed files. Mechanical settings in `%LOCALAPPDATA%/SCARA Robot` remain on the user’s computer.

## Publishing a new version

1. Build a matching version in the private source repository. Its **Build SCARA software update** workflow provides a self-contained Windows x64 ZIP and `manifest.json` as an artifact.
2. Create a release in this public repository with tag `vX.Y.Z` and attach the application ZIP.
3. Confirm the release asset SHA-256 matches the generated manifest.
4. Update `public/update/manifest.json` on `main` only after the release asset is available.

Publishing is manual and requires no GitHub token. The first `v1.0.0` package requires the .NET 6 Windows Desktop Runtime.
