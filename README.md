# XoDen runtime mirror

A separate download area for the Windows-on-PS5 runtime used by XoDen.
This repository contains public upstream runtime metadata only; app source,
account data and games are not included.

## Download

[Runtime kit 0.13 release](https://github.com/griches/xoden-runtime/releases/tag/v0.13.0)

- `playden-kit-0.13.zip`: unchanged Playden runtime kit (429,631,275 bytes).
- `playden-update.json`: unchanged upstream discovery metadata. XoDen reads
  only its kit section; the app section describes upstream Playden and is not
  used to install or update XoDen.
- Checksums, provenance, source revisions and notices are attached as well.

The kit includes Wine for PS5 from prospero-win, DXVK, vkd3d-proton, Wine Mono,
video/audio support, a template Wine bottle and PS5 title shells. Games are
separate downloads. Binaries are release assets to keep them out of Git history.

## Attribution and source

Mirrored byte-for-byte from [Playden v0.7.2](https://github.com/leolobato/playden-ps5/releases/tag/v0.7.2).
The kit is Playden's work, with each component retaining its original attribution
and license. The original `LICENSES/` directory remains inside the zip.
See [third-party notices](THIRD_PARTY_NOTICES.md), [original source list](SOURCES.md),
[exact provenance](provenance.json) and [upstream instructions](UPSTREAM-README.md).
No ownership of those components is claimed by XoDen.

Each future kit gets a separate release and must be tested before XoDen changes
its compiled manifest checksum. Runtime versioning is independent of the app.

## Verify

Download the two upstream assets and `SHA256SUMS`, then run:

```sh
shasum -a 256 -c SHA256SUMS
```

The original manifest is also supplied separately as `kit-manifest.json`.
Its SHA-256 is `d1dbc8e1b5b98691950369a89ef87c1dff5b7064a31844ccf20a4bed99b0e55b`.
