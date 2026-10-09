# wowsilicon-wine-ci

Manual GitHub Actions build of a WoWSilicon-style Wine runtime tree on a newer
`WineAndAqua/wine` macOS branch (11.19) than the one WoWSilicon ships (11.13).

- `tools/wine-runtime/{fetch-source,build}.sh` are copied unchanged from
  WoWSilicon/WoWSilicon.
- `Packaging/WineRuntime/patches/0001-*.patch` is WoWSilicon's 13 patches
  re-applied to 11.19 by hand (0009 dropped: the handler it guards no longer
  exists in 11.19). Combined into one patch.
- Run: `gh workflow run wine.yml --repo mybaixinyu/wowsilicon-wine-ci`
