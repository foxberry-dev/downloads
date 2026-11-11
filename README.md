# Foxberry downloads

Linux x86_64 installers for Cher, Esi, and Lain. Application source repositories are private; these installers and their packaged contents are public.

| App | Installer | Requirements |
| --- | --- | --- |
| Cher | [cher-installer.sh](https://github.com/foxberry-dev/downloads/releases/download/cher-latest/cher-installer.sh) | Ubuntu 24.04+ or glibc 2.39+ |
| Esi | [esi-installer.sh](https://github.com/foxberry-dev/downloads/releases/download/esi-latest/esi-installer.sh) | Node.js 24.15+, npm, Chrome/Chromium for image exports |
| Lain | [lain-installer.sh](https://github.com/foxberry-dev/downloads/releases/download/lain-latest/lain-installer.sh) | Ubuntu 24.04+ or glibc 2.39+; Chrome/Chromium for exports |

Download and inspect the chosen script, then run `sh <app>-installer.sh`. The installer verifies its pinned archive checksum, installs under `~/.local`, and starts a loopback-only user service. Use `--no-start` to install without configuring or starting a service. Set `FOXBERRY_INSTALL_PREFIX` to choose a different installation prefix.

Add `~/.local/bin` to PATH. Local viewers use ports 38476 (Cher), 38080 (Esi), and 38475 (Lain). Cher's standalone upstreams can be set with `CHER_ESI_URL` and `CHER_LAIN_URL`.

The `<app>-latest` releases contain current installers. Commit-addressed build releases provide immutable archives, checksums, and container images. Installers download from their exact build release. GitHub hosts these files; no GitHub account is required to download them.
