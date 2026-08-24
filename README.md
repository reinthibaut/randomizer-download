# Rein's Randomizer — Download

Share classroom jobs fairly and randomly across the whole school year.

**→ [Download page](https://reinthibaut.github.io/randomizer-download/)**

Or grab the installer directly:

- **Windows** — [ReinsRandomizer-Setup.exe](https://github.com/reinthibaut/randomizer-download/releases/latest/download/ReinsRandomizer-Setup.exe) (~80 MB, Windows 10 and 11, 64-bit) — version 1.0.0
- **Mac** — [ReinsRandomizer.dmg](https://github.com/reinthibaut/randomizer-download/releases/latest/download/ReinsRandomizer.dmg) (~170 MB, macOS 11+, Apple Silicon and Intel) — version 1.0.0
- **Linux** — [ReinsRandomizer.AppImage](https://github.com/reinthibaut/randomizer-download/releases/latest/download/ReinsRandomizer.AppImage) (any distro, no install) or
  [ReinsRandomizer.deb](https://github.com/reinthibaut/randomizer-download/releases/latest/download/ReinsRandomizer.deb) (Ubuntu, Mint, Debian)

## What does it do?

You fill in once who is in the class and which jobs need sharing out. After that the app picks
who does what — at random, but fairly: it keeps track of whose turn it has already been, so the
same person doesn't always end up with the job nobody wants.

**The app itself is in Dutch**, so the screen names below are the ones you'll actually see on
the buttons:

- **Naam sets** (name sets) — lists of names, one per class for instance
- **Taken** (tasks) — what needs sharing out, like wiping the board or taking the bins out
- **Templates** — tie a name set to a set of tasks, to the days it applies on, and to the
  holiday periods that get skipped
- **Volledig schema** (full schedule) — generates the rota for the entire year in one go,
  exportable as a text file
- **Groepen** (groups) — splits the class into small groups, with absences and reshuffling

On **Tracking** the app remembers whose turn it has been and shares things out evenly. On
**Puur willekeurig** (purely random) every pick stands on its own.

## Windows will show a warning — that's expected

When you open the file, Windows shows a blue box:

> **Windows protected your PC**
> Microsoft Defender SmartScreen prevented an unrecognised app from starting.

This happens to every program that hasn't been registered with Microsoft, which costs money and
isn't worth it for a small app like this one. To continue:

1. Click **More info** — the small grey text in that blue box
2. Click **Run anyway** — the button that appears at the bottom
3. The normal installer opens; click through it as usual

If you'd rather not, just ask Rein to install it for you.

## On a Mac, it takes a few more steps

Apple blocks apps that aren't registered with them, and won't let you click straight through
like Windows does.

1. Open the `.dmg` and drag **Rein's Randomizer** into **Applications**
2. Open **Applications** and double-click **Rein's Randomizer** — macOS will refuse:
   > **"Rein's Randomizer" Not Opened** — Apple could not verify "Rein's Randomizer" is free
   > of malware that may harm your Mac or compromise your privacy.
3. Click **Done**. It has to be refused once before Apple lets you allow it.
4. Open **System Settings** → **Privacy & Security**
5. Scroll to the bottom, to **Security**. Click **Open Anyway** next to "Rein's Randomizer was
   blocked to protect your Mac."
6. Enter your Mac password, then click **Open Anyway** again

You only do this once. After that it opens like any other app.

**On macOS Sonoma and earlier** it's quicker: right-click the app → **Open** → **Open**. Apple
removed that shortcut in newer versions.

## On Linux

Linux has no SmartScreen or Gatekeeper equivalent, so there are no security warnings to click
through. For the AppImage you may need to mark it executable first —
`chmod +x ReinsRandomizer.AppImage`, or right-click → Properties → *Allow executing file as
program*. The `.deb` installs by double-clicking it.

## Is this safe?

It's a personal project, not a commercial product. It runs entirely on your own computer —
nothing is uploaded, there's no account, and it needs no internet connection. Your name lists
and rotas are stored only on your own machine.

## Uninstalling

**Windows** — **Settings** → **Apps** → **Rein's Randomizer** → **Uninstall**.

**Mac** — open **Applications**, drag **Rein's Randomizer** to the Bin, empty the Bin. Macs have
no uninstaller; dragging it away is the normal way to remove an app.

**Linux** — `sudo apt remove classroom-randomizer` for the `.deb`. An AppImage you just delete.

Either way your name lists and rotas are **not** deleted — they're kept separately, so
reinstalling picks up where you left off. To wipe them too:

- **Windows** — <kbd>Win</kbd>+<kbd>R</kbd>, paste `%APPDATA%\classroom-randomizer`, Enter, delete the folder
- **Mac** — in Finder press <kbd>Cmd</kbd>+<kbd>Shift</kbd>+<kbd>G</kbd>, paste
  `~/Library/Application Support/classroom-randomizer`, Enter, drag the folder to the Bin
- **Linux** — delete the folder `~/.config/classroom-randomizer`

That erases your name lists, templates and history permanently. Export your schedule first if
you might still need it.

---

This repository contains only the installer and this page. The app's source code is private.
