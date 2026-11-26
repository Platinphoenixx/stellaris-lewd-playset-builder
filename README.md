# Stellaris Lewd Playset Builder

**18+ only.** A desktop app and a curated catalog for the adult ("lewd") mods of *Stellaris*, scattered across
LoversLab and the Steam Workshop – built around **Lustful Void**.

Instead of picking one of many ready-made playsets, you build **one playset of your own**: the species, portraits
and features you want, together with the general mods you play with. The app fills in what they need, tells you
what clashes and why, puts them in a working load order and checks them against the current game version.

> **Beta.** Tested on the maintainer's PC and by the first players of the alpha; please report what breaks. Only the
> newest Stellaris version (4.5.4) is supported. Made for Windows; since 0.4.5 there is a **Linux beta** – the
> "Potentially Shitty Vibecoded Version", not tested on Linux by the maintainer. Where the app does not find the game,
> the Workshop or the Stellaris user folder by itself, choose them under **Game**.

## What it does

Four steps, with your playset always shown on the right:

1. **Start** – from scratch, or from a playset you already have in the Paradox launcher: what still works is taken
   over, outdated mods bring their newer version, broken ones are left out.
2. **Choose mods** – by kind (Lustful Void add-ons, species and looks, lewd mechanics, events, ships, interface,
   gameplay, …), as cards with pictures, what each mod adds and how it stands with the game version. What a pick
   needs is added by itself.
3. **Check** – what needs you, each with a button that fixes it (add the missing patch, remove one of two mods
   that do not go together, …), and the suggestions that are really optional.
4. **Install & play** – subscribes the Workshop mods through Steam, downloads the LoversLab mods with your own
   LoversLab login, writes an optional **merge patch** (combines what mods change differently in the same game
   objects), optionally builds **one mod instead of all** of them (loads much faster), and creates the playset in
   the Paradox launcher. Your own local mods and fixes can be ticked in right there, and the creators of your mods
   who accept support are listed with their pages. Later, when a mod is updated or you change your picks,
   **Update everything** brings the merge patch, the merged mod and the launcher playset up to date in place.

When Steam updates Stellaris past the version the catalog is checked against, the app warns you and shows how to go
back to that version (Steam → Properties → Betas). Until the catalog is checked against the new version, the merge patch
is held back (it is made for the catalog's version), and mods already updated for the new game are named.
Fixes made for the newer game – such as **Lustful Void - 4.6 Fix** (since 0.4.6) – are suggested only once your game
is that version.

Behind it, a **catalog** of ~650 mods: every mod's files were read and compared with the game (what it adds,
which game objects it changes, what the game removed since), most were started in the game (launch tests), and the
Workshop comments and LoversLab support threads were read for problem reports.

## Install

1. Download the latest version from [Releases](../../releases): the **Setup** file installs the app (for your
   Windows user, no admin rights), the **portable** file runs without installing (keep the **portable-uninstall** file
   next to it, for removing it cleanly later).
   **Linux beta** ("Potentially Shitty Vibecoded Version", untested): the **linux.tar.gz** – unpack it and run
   `./start.sh`; README-LINUX.txt inside says what it needs (bsdtar for LoversLab downloads) and where it looks.
2. The app is not code-signed, so Windows SmartScreen may warn on first start: *More info → Run anyway*.
3. Start it. It finds Steam, the game and your Paradox launcher by itself.

A new version is announced inside the app; nothing updates or installs by itself.

## What the app does on your PC

- **Reads** your installed mods and your launcher playsets (from a copy of the launcher's database).
- **Writes only when you click it:** a launcher playset – a new one, or in place of one the app made before when you
  choose that (your own playsets are never changed; the launcher's database is backed up first, and the app refuses
  while the launcher or the game runs), mods it downloads into
  your Stellaris mod folder (an older copy you have is never overwritten), the merge patch and the merged mod (each
  in its own folder, replaced only by the app's own next build).
- **Never runs** anything from a downloaded archive; archives are unpacked with Windows' own `tar.exe` (on Linux with `bsdtar`).
- **Uninstalling** (Windows' settings → Apps, or for the portable app the `…-portable-uninstall.exe` next to it) asks,
  one question each, whether to remove what the app made outside its program folder too: the launcher playsets it made,
  merge patches and merged mods, the mods it downloaded from LoversLab, and its own data (picks, LoversLab login,
  launcher backups). Your own mods and playsets are never touched.

## What the app talks to

- **GitHub**: once a day whether a new app version exists, and (since 0.4.7) every two hours whether the catalog is
  newer – then it is downloaded and used from the next start, without a new app version – and (since 0.4.9) for short
  news lines from the maintainer, shown under the top bar.
- **Steam** only when you subscribe mods (through your running Steam client), **LoversLab** only when you log in or
  download (in a window of the app, with your login; the login stays in the app). Pictures are loaded from the
  mods' pages.
- Nothing else. The app sends nothing about you, your mods or your playsets anywhere.

## Support

If the app helps you, you can support it on [Ko-fi](https://ko-fi.com/platinphoenix31043) – there is also a button in
the app. All mods belong to their authors: the app links to their pages; please support them there too.

## Source

This repository holds the releases. The source code is not public (yet).
