# dekobon/scoop-bucket

[Scoop](https://scoop.sh) bucket for tools maintained by [@dekobon](https://github.com/dekobon).

## Usage

```powershell
scoop bucket add dekobon https://github.com/dekobon/scoop-bucket
scoop install <app>
```

Or install an app directly without adding the bucket first:

```powershell
scoop install https://github.com/dekobon/scoop-bucket/raw/main/bucket/<app>.json
```

## Available apps

| App | Description |
| --- | --- |
| [`host-identity`](bucket/host-identity.json) | Stable host UUID across platforms, clouds, and Kubernetes. |

## Platform support

Manifests publish Windows binaries for both **x86_64** (`64bit`) and **aarch64** (`arm64`). Scoop selects the matching architecture automatically.

## Updating

Manifests are rendered automatically by the upstream project's release workflow (`.github/workflows/release.yml`) on each `v*` tag — do not edit `bucket/*.json` by hand. Scoop's `checkver` and `autoupdate` metadata keeps the bucket in sync with upstream GitHub releases.
