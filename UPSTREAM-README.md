# Playden runtime kit 0.13

The runtime kit for Playden for PS5 0.7.0: Wine for the PS5 (prospero-win), the graphics drivers (DXVK for Direct3D
8–11, vkd3d-proton for Direct3D 12), Wine Mono, video and audio decoding (GStreamer and FFmpeg), a clean Windows
environment and the per-game app shell. Playden accepts only this kit: `manifest.json` SHA-256 `d1dbc8e1b5b98691950369a89ef87c1dff5b7064a31844ccf20a4bed99b0e55b`.

Playden 0.7.0 downloads and installs this kit by itself on its first start. To install it by hand, unzip both
downloads next to each other and run this from the `playden-ps5-0.7.0` folder:

```sh
python3 tools/console_kit_upload.py ../playden-kit-0.13 --host <PS5 IP> --replace
```

- `playden-kit/`: the kit, installed to `/data/playden/kits/playden-kit` on the console.
- `SOURCES.md`: the source revision of every component.
- `LICENSES/`: the license texts of the components. See also Playden's `THIRD_PARTY_NOTICES.md`.

Tested on firmware 13.60. Other firmware versions are allowed but untested.
