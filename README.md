# Version-Checker

Central `latest` + `changelogs` catalogs for XSular FiveM resources.

`xsular_bridge` fetches these files. It never writes files and never auto-updates.

| File | Resource | `latest` |
|---|---|---|
| [`xsular_bridge.json`](xsular_bridge.json) | `xsular_bridge` | `3.1.0` |
| [`xsular_mBanking.json`](xsular_mBanking.json) | `xsular_mBanking` | `1.1.0` |
| [`xsular_mClothing.json`](xsular_mClothing.json) | `xsular_mClothing` | `1.0.0` |
| [`xsular_mGarages.json`](xsular_mGarages.json) | `xsular_mGarages` | `1.1.0` |
| [`xsular_mLoadingScreen.json`](xsular_mLoadingScreen.json) | `xsular_mLoadingScreen` | `1.1.0` |
| [`xsular_mMultiCharacter.json`](xsular_mMultiCharacter.json) | `xsular_mMultiCharacter` | `2.0.0` |
| [`xsular_mPauseMenu.json`](xsular_mPauseMenu.json) | `xsular_mPauseMenu` | `2.0.0` |
| [`xsular_multicharacter.json`](xsular_multicharacter.json) | previous multicharacter filename | `2.0.0` |

Raw URL shape:

```
https://raw.githubusercontent.com/MrBiLaLD3v/Version-Checker/refs/heads/main/<file>
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
