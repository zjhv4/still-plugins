# Still plugin channel

Public, independently versioned Still source and image-processing packages.

Subscribe in Still → Plugins → Updates & channels using this repository's `catalog.json` file link. GitHub raw file links and ordinary HTTPS static directories use the same channel format.

The channel contains plugin packages, checksums, corresponding plugin/SDK [source](source.zip), and [dependency notices](THIRD_PARTY_NOTICES.txt). It contains no application runtime data, accounts, keys, or wallpaper library.

## Building

Extract `source.zip`, install Rust's `wasm32-unknown-unknown` target, and run `python scripts/package_plugins.py` inside `Still-plugin-source`. To publish a new version, update the corresponding plugin's Cargo.toml and plugin.toml version together and regenerate the source snapshot. The manual Rebuild channel workflow builds that snapshot and commits only the resulting package files and catalog.

Clients only upgrade installed packages, verify all four files, preserve configuration, and keep the previous version if validation or migration fails. HTTPS authenticates the subscribed host; the checksums are integrity checks, not an independent publisher signature.
