# Stellaris Lewd Playset Builder

**18+ only.** A desktop app and a curated catalog for the adult ("lewd") mods of *Stellaris*, scattered across
LoversLab and the Steam Workshop – built around **Lustful Void**.

Instead of picking one of many ready-made playsets, you build **one playset of your own**: the species, portraits
and features you want, together with the general mods you play with. The app fills in what they need, tells you
what clashes and why, puts them in a working load order and checks them against the current game version.

> **Alpha.** Everything below works on the maintainer's PC; it has not been used on many others yet. Only the newest
> Stellaris version (4.5.4) is supported. Windows only.

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
   who accept support are listed with their pages.

Behind it, a **catalog** of ~650 mods: every mod's files were read and compared with the game (what it adds,
which game objects it changes, what the game removed since), most were started in the game (launch tests), and the
Workshop comments and LoversLab support threads were read for problem reports.

## Install

1. Download the latest version from [Releases](../../releases): the **Setup** file installs the app (for your
   Windows user, no admin rights), the **portable** file runs without installing.
2. The app is not code-signed, so Windows SmartScreen may warn on first start: *More info → Run anyway*.
3. Start it. It finds Steam, the game and your Paradox launcher by itself.

A new version is announced inside the app; nothing updates or installs by itself.

## What the app does on your PC

- **Reads** your installed mods and your launcher playsets (from a copy of the launcher's database).
- **Writes only when you click it:** a *new* launcher playset (your existing ones stay as they are; the launcher's
  database is backed up first, and the app refuses while the launcher or the game runs), mods it downloads into
  your Stellaris mod folder (an older copy you have is never overwritten), the merge patch and the merged mod (each
  in its own folder, replaced only by the app's own next build).
- **Never runs** anything from a downloaded archive; archives are unpacked with Windows' own `tar.exe`.

## What the app talks to

- **GitHub**, at most once a day: whether a new app version exists.
- **Steam** only when you subscribe mods (through your running Steam client), **LoversLab** only when you log in or
  download (in a window of the app, with your login; the login stays in the app). Pictures are loaded from the
  mods' pages.
- Nothing else. The app sends nothing about you, your mods or your playsets anywhere.

## Support

If the app helps you, you can support it on [Ko-fi](https://ko-fi.com/platinphoenix31043) – there is also a button in
the app. All mods belong to their authors: the app links to their pages; please support them there too.

## Source

This repository holds the releases. The source code is not public (yet).
