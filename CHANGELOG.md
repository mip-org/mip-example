# Changelog

## 2026-06-30

- Converted to the shared MIP channel build system. Replaced the legacy
  `prepare.yaml` recipe format with `source.yaml`, and flattened the layout
  from `packages/<name>/releases/<release>/` to `packages/<name>/<release>/`.
  The sole package, `hello_mip`, now tracks the `main` branch of
  `mip-org/hello_mip` (which carries its own `mip.yaml`), matching the
  `mip-hello` channel.
- `.github/workflows/` are now thin callers delegating to the reusable
  workflows in `mip-org/mip_channel_tools` (`@main`).
- Removed the `channel.yaml` config, the `external/yamlmatlab` git submodule,
  and the per-channel `scripts/` directory (all now provided by the tooling
  repo); added `.gitattributes` and `CLAUDE.md`.
