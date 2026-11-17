# Tor directory manager compatibility patch

`tor-dirmgr` is the published 0.47.0 package from crates.io. Its source is unchanged; the rusqlite upper bound in both manifests is widened from `<0.41.0` to `<0.42.0`, following upstream commit [00a62585bcfab121797b6f42393149b97b7c231e](https://gitlab.torproject.org/tpo/core/arti/-/commit/00a62585bcfab121797b6f42393149b97b7c231e).

This lets Galloy and its optional Tor client share rusqlite 0.41 with bundled SQLite 3.54 or later, fixing RUSTSEC-2026-0459 without removing Tor support or updating the rest of Arti.

Source archive: https://static.crates.io/crates/tor-dirmgr/tor-dirmgr-0.47.0.crate
SHA-256: `34ea5e77b43bf1ef5fa213a89cb67080f218df6b418c82527e6bb9862a39aef5`
Upstream source commit: `ce8bc6e0998bd5a4efdf06dd62dce53c98ea1087`.
License: MIT OR Apache-2.0.

Remove the root Cargo patch and this directory once a published compatible Arti release accepts rusqlite 0.41 or later. Verify the default history tests and the Tor feature when replacing it.
