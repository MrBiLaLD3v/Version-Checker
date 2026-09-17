# Version-Checker

Central `latest` + `changelogs` catalogs for XSular FiveM resources.

Each resource fetches its JSON on start (`Config.VersionCheck`). The checker never writes files and never auto-updates.

| File | Resource |
|---|---|
| [`xsular_bridge.json`](xsular_bridge.json) | `xsular_bridge` |
| [`xsular_multicharacter.json`](xsular_multicharacter.json) | `xsular_mMultiCharacter` |

Raw URLs:

```
https://raw.githubusercontent.com/MrBiLaLD3v/Version-Checker/refs/heads/main/xsular_bridge.json
https://raw.githubusercontent.com/MrBiLaLD3v/Version-Checker/refs/heads/main/xsular_multicharacter.json
```

## JSON shape

```json
{
  "latest": "1.1.0",
  "download": "https://portal.cfx.re/assets/granted-assets",
  "changelogs": {
    "1.1.0": {
      "Added": ["note"],
      "Updated": ["note"],
      "Fixed": ["note"]
    }
  }
}
```

When a server is behind, the console banner prints every `changelogs` entry newer than the installed `fxmanifest` version, up to `latest`.

## Release

1. Bump the resource `fxmanifest.lua` `version`.
2. Set the same `latest` in that resource's JSON here and add a `changelogs` entry.
3. Push this repo.
