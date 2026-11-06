# SCARA Robot updates

This repository publishes Windows application packages for SCARA Robot. Source code remains private.

The application reads `public/update/manifest.json` to discover a newer release. The manifest provides a version, a GitHub Release download URL, and a SHA-256 digest. A release package is published first; the manifest is updated only after the package is available.

The updater verifies the package digest and staged application version before replacing the installed application files. Local mechanical settings remain in `%LOCALAPPDATA%/SCARA Robot`.
