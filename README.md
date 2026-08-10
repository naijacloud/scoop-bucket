# scoop-bucket

Scoop bucket for the [NaijaCloud CLI](https://github.com/naijacloud/nc-cli).

## Install

```powershell
scoop bucket add naijacloud https://github.com/naijacloud/scoop-bucket
scoop install naijacloud
```

The CLI is installed under **two names**, `naijacloud` and the shorter `njc`.
Both are shims onto the same executable.

The package is a standalone binary that embeds its own runtime, so Node is not
required. Windows x64 only; for other platforms see the
[install options](https://github.com/naijacloud/nc-cli#install) in the main
repository.

## Upgrading

```powershell
scoop update naijacloud
```

The manifest carries `checkver` and `autoupdate`, so Scoop's own bots can pick
up a new release even if a workflow run is missed.

## Contents

`bucket/naijacloud.json` is generated from
[`packaging/templates/scoop/naijacloud.json`](https://github.com/naijacloud/nc-cli/blob/main/packaging/templates/scoop/naijacloud.json)
and committed here by the release workflow in
[naijacloud/nc-cli](https://github.com/naijacloud/nc-cli) on every release, with
the version and the SHA-256 of the published artifact filled in.

**Do not edit the manifest here.** The next release overwrites it. Change the
template in `nc-cli` instead.

## Issues

Report problems with the CLI itself at
[naijacloud/nc-cli/issues](https://github.com/naijacloud/nc-cli/issues).
