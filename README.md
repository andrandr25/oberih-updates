# Mudi Core update feed

**English** | [Українська](README.uk.md)

Signed packages for Mudi Core (`luci-app-mudi`) on GL.iNet GL-E750 (Mudi V2) routers.

## Install

Stock GL firmware 4.x, router online:

1. Admin panel `http://192.168.8.1` → **Applications → Plug-ins → Sources** → **Add**:
   name `mudi`, URL `https://git.fraola.net/androffka/mudi-updates/raw/branch/main/stable`
2. **Update** the package lists.
3. Find `luci-app-mudi` → **Install**.
4. Reload the page — **Mudi Core** appears in the left menu. Updates arrive by themselves.

## Security

Routers verify `Packages.sig` with the pinned key `87d48f5e9a5bb4a9` (see `mudi-feed.pub`) and the SHA256 of every package before installing. Unsigned or modified files are refused.

| Directory | What |
|---|---|
| `stable/` | releases for everyone |
| `beta/` | early access |
| `extras/` | Blue Merle and its dependencies for the one-click install (unmodified packages, see `extras/SOURCES.txt`) |

Blue Merle changes the modem IMEI; in some countries this is prohibited or regulated. Mudi Core installs it only after you accept that notice.

Proprietary software — see the LICENSE in each package.
