# CLAUDE.md — Randomizer Download

## What this project does
The **public** download page for Rein's Randomizer. It exists so Rein can share one link
instead of sending an 80 MB file around.

The app's source code is NOT here — it lives in the private `reins-randomizer` repo.
This repo holds only the install page and the released installers.

## File structure
- `docs/index.html` — the download page, served by GitHub Pages
- `README.md` — same install instructions, for anyone who lands on the repo itself

## Where things live
- Public repo: `github.com/reinthibaut/randomizer-download`
- Live page: `reinthibaut.github.io/randomizer-download`
- Installers: attached to the GitHub Release in this repo
  - Windows: `ReinsRandomizer-Setup.exe`
  - macOS: `ReinsRandomizer.dmg` (universal — runs on both Apple Silicon and Intel)
  - Linux: `ReinsRandomizer.AppImage` (any distro) and `ReinsRandomizer.deb` (Ubuntu/Mint/Debian)
- Private source: `github.com/reinthibaut/reins-randomizer`

## Language
The app's interface is in Dutch, so this page and README are in Dutch too. Cypher's
equivalent page is in English because that app has a different audience — don't "fix" this
one to match it.

## Rules
- **This repo is public.** Never put keys, personal data, `.env` files, student names, or
  app source here.
- Release assets must always be named `ReinsRandomizer-Setup.exe`, `ReinsRandomizer.dmg`,
  `ReinsRandomizer.AppImage` and `ReinsRandomizer.deb` — the download links point at
  `/releases/latest/download/<name>`, which only resolves if the filenames stay identical
  across versions. electron-builder produces versioned names like
  `Rein's Randomizer-1.0.0-universal.dmg`, so they must be renamed before uploading. Getting
  this wrong breaks the download button silently — the page still looks fine.
- The `.deb` maintainer email lives in the source repo's `package.json` under
  `build.linux.maintainer` and is readable by anyone who downloads the package, so it uses
  the GitHub noreply address rather than a personal one. Building a `.deb` fails outright
  without it.
- GitHub Pages serves from the `docs/` folder on `main`. Changing that folder breaks the site.
- Never run git commands without asking Rein first.
- Never delete files without confirming.

## Publishing a new version
1. **Windows**: in the private repo run `npm run dist`, then rename
   `dist/Rein's Randomizer Setup <version>.exe` to `ReinsRandomizer-Setup.exe`
2. **macOS and Linux**: trigger the "Build installers" workflow in the private repo
   (`gh workflow run build-installers.yml --repo reinthibaut/reins-randomizer`), download
   both artifacts, then rename:
   - `Rein's Randomizer-<version>-universal.dmg` → `ReinsRandomizer.dmg`
   - `Rein's Randomizer-<version>.AppImage` → `ReinsRandomizer.AppImage`
   - `classroom-randomizer_<version>_amd64.deb` → `ReinsRandomizer.deb`

   Neither build can run on Windows — macOS packaging needs `hdiutil`, Linux needs
   `dpkg`/`fakeroot`.
3. Create a release here with all four files attached
4. Update the version number and file sizes shown in `docs/index.html` and `README.md`

## Stack
Static HTML, no build step, no dependencies. GitHub Pages for hosting.
