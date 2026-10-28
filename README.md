# XoDen runtime

A separate download area for the Windows-on-PS5 runtime used by XoDen. No games, account data or credentials are included.

## Download

[Runtime kit 0.13.1](https://github.com/griches/xoden-runtime/releases/tag/v0.13.1) fixes the native launcher failing to find its graphics runtime after the PS5 root grant. It adds the title-specific `/data/homebrew/<title ID>` directory to the existing runtime lookup roots. Gary confirmed DREDGE opens from its PS5 Home tile with this launcher; extended gameplay and the in-app runtime update remain untested.

The kit is based on [Playden v0.7.2 / kit 0.13](https://github.com/leolobato/playden-ps5/releases/tag/v0.7.2). Only the native title shell, its build marker and the kit manifest changed. Wine, Mesa, DXVK, vkd3d-proton, Mono, the helper, libc and the template bottle are unchanged. The zip retains its original internal prefix `playden-kit-0.13/playden-kit/`; discovery metadata specifies this prefix.

XoDen reads only the kit section of `playden-update.json`. The inherited app section describes upstream Playden; XoDen does not use it to update the app.

## Attribution and source

Each component retains its original attribution and license. The complete original `LICENSES/` directory remains inside the zip. See [notices](THIRD_PARTY_NOTICES.md), [source inventory](SOURCES.md), [exact provenance](provenance.json) and [upstream instructions](UPSTREAM-README.md). No ownership of upstream components is claimed by XoDen.

The release includes the shell source archive, a Git bundle containing the exact patch commit, and `runtime-path-fix.patch`. The source commit is `ffd297dbe7249763bff5f1daaa1c9f9074131eec`, based on upstream `ce289425bb34acbcc98f77b4e00ac98b3c16e4bc`. Binaries stay in release assets rather than Git history.

The original unmodified kit is still available as [0.13.0](https://github.com/griches/xoden-runtime/releases/tag/v0.13.0).

## Verify

Download the release assets and run `shasum -a 256 -c SHA256SUMS` in that directory. XoDen additionally checks the compiled manifest checksum, individual file hashes and modes before admitting a kit.

The 0.13.1 manifest SHA-256 is `1d49095369dc3f76e1465b3ddec3bec1433810d623c7c30bf4bd1680f4d69e59`.
