# Open Net Worth — releases

Your wealth, on your computer.

This repository hosts the built releases of [Open Net Worth](https://github.com/open-net-worth-ai/open-net-worth):
the desktop apps and their update feed, the server package and the Docker Compose file. The
source code lives in [open-net-worth-ai/open-net-worth](https://github.com/open-net-worth-ai/open-net-worth).

## Desktop app

| Platform | Download | Terminal install |
|---|---|---|
| macOS (Apple Silicon; signed and notarized) | [Open-Net-Worth-mac-arm64.dmg](https://github.com/open-net-worth-ai/open-net-worth-releases/releases/latest/download/Open-Net-Worth-mac-arm64.dmg) | `curl -fsSL https://opennetworth.ai/install.sh \| sh` |
| Windows 10/11 x64 | [Open-Net-Worth-windows-x64-setup.exe](https://github.com/open-net-worth-ai/open-net-worth-releases/releases/latest/download/Open-Net-Worth-windows-x64-setup.exe) | `irm https://opennetworth.ai/install.ps1 \| iex` (PowerShell) |
| Linux x86_64 | [AppImage](https://github.com/open-net-worth-ai/open-net-worth-releases/releases/latest/download/Open-Net-Worth-linux-x86_64.AppImage) or [.deb](https://github.com/open-net-worth-ai/open-net-worth-releases/releases/latest/download/Open-Net-Worth-linux-amd64.deb) | `curl -fsSL https://opennetworth.ai/install.sh \| sh` |

On macOS, open the `.dmg` and drag **Open Net Worth** to Applications. The Windows installer is
not code-signed yet, so SmartScreen may warn you: choose **More info**, then **Run anyway**. The
terminal installers check the download against the release's `SHA256SUMS` first.

Installed apps update themselves and offer **Restart to Update** when a new version is ready.

## Server

```bash
curl -fsSL https://github.com/open-net-worth-ai/open-net-worth-releases/releases/latest/download/install-server.sh | sh
onw start --open
```

Installs `open-net-worth` with [uv](https://docs.astral.sh/uv/) on its own Python, then runs it
at `http://127.0.0.1:8080`.

## Docker

```bash
curl -fsSLO https://github.com/open-net-worth-ai/open-net-worth-releases/releases/latest/download/docker-compose.yml
AUTH_PASSWORD='pick a password' docker compose up -d
```

Runs `ghcr.io/open-net-worth-ai/open-net-worth`, pinned to the release the file came with.

## Verifying a release

Every release carries `SHA256SUMS` and a signed `manifest.json`, each with a minisign
signature (`.minisig`).

All versions: [Releases](https://github.com/open-net-worth-ai/open-net-worth-releases/releases).
Full install guide: [docs.opennetworth.ai](https://docs.opennetworth.ai). More at
[opennetworth.ai](https://opennetworth.ai).
