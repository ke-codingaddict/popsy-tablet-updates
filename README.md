# Popsy tablet updates

Over-the-air update channel for Popsy (rk3326) tablets.

- `manifest.signed`: the latest update. Line 1 is an ECDSA P-256 signature, the rest is JSON.
- Release assets: the update bundles.

Tablets install a bundle only if the manifest signature matches the public key built into their firmware,
and the bundle's SHA-256 matches the signed manifest. This repo contains no secrets.
Updates are published with `ota/publish.sh` from the firmware repo.
