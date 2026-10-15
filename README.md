<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="icon-512.png">
    <source media="(prefers-color-scheme: light)" srcset="icon-512-light.png">
    <img src="icon-512-light.png" width="160" height="160" alt="Mend icon">
  </picture>
</p>

<h1 align="center">Mend</h1>

<p align="center"><b>Mend — an AI repair kit for iPhone, Android, Mac, Windows, Linux and every disk</b></p>

<p align="center">
  Version <b>1.0.12</b> · released 15 Oct 2026 ·
  <a href="https://github.com/JKS-sys/mend-08-oct-2026-releases/releases/latest">Download</a> ·
  <a href="https://ipconfig.co.network/mend">Website</a> ·
  <a href="RELEASE-NOTES.md">Release notes</a>
</p>

<p align="center">⭐ <b>If Mend helps you, please give this repository a star</b> — it is the one thing that tells other people the app is worth a look, and it keeps the project going.</p>

<p align="center">
  <img src="icon-512.png" width="96" height="96" alt="Mend icon, dark">&nbsp;&nbsp;
  <img src="icon-512-light.png" width="96" height="96" alt="Mend icon, light">
</p>

Mend rescues phones and computers in one small app (a few MB): one-click Recovery Mode, iOS and Android
system repair, Mac/Windows/Linux system and boot repair, a corrupted-settings fixer, a partition manager,
deep disk health, tiny de-duplicated backups and a contact manager for every account — with AI that explains each step.
It also carries a **Fix Library of 16,826 known problems across 16 kinds of device** — iPhone, iPad, Mac, Apple Watch,
Apple TV, AirPods, HomePod, Vision Pro, Android, Windows, Linux, ChromeOS, FreeBSD, Haiku, disks and contacts — each
written for that model's own buttons, menus and commands, with the repair that fixes it; **device files,
Configurator, app downloads, scheduled backups with snapshots and evidence-grade message exports**; a command line;
a right-click menu everywhere and a Dock menu; and an interface in **15 languages**.

## See it in action

<p align="center"><img src="demos/health2.webp" width="900" alt="Disk Health: used and free space per volume, general information and a rescue plan for a disk with pending sectors"></p>

**Disk Health.** Every disk card opens with its used · free · total bar (one segment per volume), the general
information and the health ring; a drive with pending sectors gets a five-step rescue plan with a button for each step.

<p align="center"><img src="demos/dups.webp" width="900" alt="Duplicates: picking places, scanning, groups of identical files and look-alike pictures with keep choices"></p>

**Duplicates.** Pick the places (home folders, external disks, cloud storages), scan, choose what to keep in every
group — the rest goes to the Trash and one copy always stays.

<p align="center"><img src="demos/menus.webp" width="900" alt="Right-click menus with Devices, Disks, Go to, Back up, Repair, Appearance and Language drop-downs"></p>

**Right-click with drop-downs.** The connected phones and disks, every page, every backup and repair, appearance and
language — from the in-app menu, the menu-bar icon and the Dock menu.

<p align="center"><img src="demos/splash.webp" width="900" alt="Mend's startup animation: a stitched gold ring sews itself shut around a heartbeat M"></p>

**Startup.** The stitched ring sews itself shut, the heartbeat “M” beats twice, sparks fly and a live heartbeat line
runs underneath — with its own synthesised sound. Any key skips it; *Reduce motion* turns it into a fade.

<p align="center"><img src="demos/devices.webp" width="900" alt="Fix Library: switching between iPad, Apple Watch, Apple TV, Android, Windows, Linux, ChromeOS and Haiku, each with its own animated picture, then opening a Linux fix and the repair coverage"></p>

**16 kinds of device, 16,826 problems.** Every family has its own animated picture and sound. Each problem is
written for the exact model or system: an iPad with a Home button gets the Home-button restart, Ubuntu gets `apt`,
Fedora `dnf`, Arch `pacman`; a Dell PC gets SupportAssist and F12, an HP gets F11 and Sure Recover; a Galaxy gets
Smart Switch and Volume Up + Side key. “What Standard & Full Repair fix” shows the honest split — what a reinstall
fixes, what needs an erase, and what needs steps or a part instead.

| | Problems | Standard Repair fixes | Full Repair fixes |
|---|---:|---:|---:|
| iPhone | 1,223 | 1,118 | 1,126 |
| iPad (21 model families) | 1,656 | 893 | 1,061 |
| Mac | 1,159 | 1,107 | 1,115 |
| Apple Watch (13 models) | 429 | 26 | 117 |
| Apple TV · AirPods · HomePod · Vision Pro | 223 | 2 | 41 |
| Android (12 makers) | 672 | 156 | 252 |
| Windows 10 / 11 / 11 on Arm × 9 PC makers | 1,750 | 876 | 1,001 |
| Linux (16 distributions) | 955 | 426 | 461 |
| ChromeOS · FreeBSD · Haiku | 44 | 10 | 20 |
| Disks (13 kinds of drive × 11 file systems) | 3,039 | 2,520 | 3,000 |
| Contacts | 420 | 336 | 420 |

<p align="center"><img src="demos/library.webp" width="900" alt="Fix Library: opening a fix, ticking steps, switching to Mac, searching for beach ball when opening apps"></p>

**Fix Library.** Search in your own words (“wifi keeps dropping”, “stuck on the Apple logo”),
filter by colour-coded category, open a fix and tick off the numbered steps as you go. Star the fixes you want to keep,
mark a problem “It's fixed!” and copy the steps to send to someone. Menus and paths are blue with violet ›,
keys and buttons are gold, numbers are cyan, *keeps your data* is green and *erases* is red — so you can tell what
a step does before reading it. The buttons under each fix run the matching repair.

<p align="center"><img src="demos/files.webp" width="900" alt="Device files: opening Photos, selecting three pictures, the right-click menu, then browsing inside the VLC app"></p>

**Device files.** Browse the iPhone or iPad like a drive — photos and videos, music files, ringtones,
books, recordings — over USB or Wi-Fi. Copy anything to the computer, and **Quick Transfer** files or whole folders
onto the device or straight into an app's Documents (VLC, Documents, any Files-compatible app). New folders, rename,
delete, a right-click menu, and the free space as a bar.

<p align="center"><img src="demos/manage.webp" width="900" alt="Configurator: turning on Wi-Fi, restrictions and Kiosk Mode, then the colour-coded XML of the profile"></p>

**Configurator.** Build Apple configuration profiles — Wi-Fi, 16 restrictions, Kiosk Mode (Single App), web clips,
passcode rules — see the colour-coded XML, save the .mobileconfig, sign it with a certificate from your keychain and
install it on one device or every connected one (Apple Configurator on a Mac). Supervise a freshly erased device,
remove profiles, and back up, install an .ipa on, or restart every connected device at once. The Apps tab downloads
App Store apps as **.ipa** files with your own Apple Account (ipatool) and installs them on any of your devices.

<p align="center"><img src="demos/autobackup.webp" width="900" alt="Automatic backups: turning on a daily Wi-Fi schedule, taking a snapshot, archiving one and cleaning old ones"></p>

**Automatic backups with snapshots.** Daily or weekly, over USB or Wi-Fi, for one device or every connected one — even
while Mend is closed (launchd on a Mac, a systemd timer on Linux, Task Scheduler on Windows). Each backup keeps a
**snapshot** (an APFS clone on a Mac, so unchanged files take no extra space), snapshots you archive are kept forever,
and old ones are **cleaned** by count and age. Point the backups folder at an external drive or a NAS.
**Messages, WhatsApp and everything else** export as CSV or HTML, and as an **evidence report** for court or
compliance: case details, the device's serial and IMEI, SHA-256 of the source database and the backup manifest, every
message with its metadata and attachments, page numbers and signature lines.

<p align="center"><img src="demos/separate.webp" width="900" alt="Separate backups: backing up contacts, then photos with a progress bar, then every kind at once"></p>

**Separate, incremental backups.** Every kind of data on every device is backed up on its own — on an iPhone or
iPad: contacts, messages, WhatsApp, calls, notes, calendar, Safari, bookmarks, voicemail, photos and videos, music,
ringtones, books and recordings; on Android: each contacts account, camera photos, pictures, WhatsApp media,
downloads, documents, music, movies and recordings; on this computer: every contacts account. Each is
**incremental**: data is saved as a new version only when it changed (every earlier version kept), and files are
mirrored — only new or changed photos and files are copied, nothing already saved is deleted. Point it at an
external drive or NAS.

<p align="center"><img src="demos/tocloud.webp" width="900" alt="Choosing backed-up contacts from an iPhone, an Android account and a separate backup, then fixing them and adding them to iCloud"></p>

**Fix backed-up contacts and add them to iCloud.** Pick contacts saved from phones — iPhone backups, Android
accounts, separate backups, library books — and Mend fixes every problem, merges duplicates, skips people already in
the account, saves a .vcf copy and adds the rest to your iCloud, Google or other internet account.

<p align="center"><img src="demos/presence.webp" width="900" alt="Settings: choosing Menu bar only, Background only, Dock only and Dock and menu bar"></p>

**Dock, menu bar or background.** Show Mend in the Dock and the menu bar, only one of them, or neither — running
quietly in the background (taskbar and system tray on Windows and Linux). The menu-bar icon has Find a Repair,
Checkup, Mend AI, Back Up iPhone Now, Full Disk Report and every area. With the menu-bar icon only or in the
background, closing the window keeps Mend running; start Mend again to bring it back.

<p align="center"><img src="demos/rightclick.webp" width="900" alt="Right-click menus: on the sidebar and anywhere in a screen"></p>

**Right-click anywhere.** The menu fits what's under the pointer — text fields (cut, copy, paste), selected text
(ask Mend AI, find fixes, search the web), logs and code (copy all, save, explain), sidebar places, fixes — plus every
app command. Right-click Mend in the **Dock** for Find a Repair, Checkup, Mend AI, each area, Back Up iPhone Now and
Full Disk Report. Closing the window (or ⌘W) quits Mend completely, stopping anything still running.

<p align="center"><img src="demos/languages.webp" width="900" alt="Settings: switching the interface between German, Japanese, Tamil, Hindi and Spanish"></p>

**15 languages.** English, Deutsch, Français, Español, Italiano, Português, Українська, Русский, العربية, 日本語,
한국어, 简体中文, 繁體中文, हिन्दी and தமிழ் — menus, tabs and buttons switch instantly, and Mend AI answers in your
language. (Long help text and the Fix Library stay in English; Mend AI explains any of it in yours.)

<p align="center"><img src="demos/checkup.webp" width="900" alt="Checkup: a radar sweep while Mend checks disks, storage, memory, security, battery and phones, then a score with Fix buttons"></p>

**Checkup.** One button (⇧⌘C) checks disks, free space, memory, security, battery, sleep, firewall, Time Machine,
updates, recent errors and every connected phone — read-only, about 20 seconds. Each result lands on the radar in its
colour — green good, gold to check, red to fix — and anything that needs attention has a Fix button.

<p align="center"><img src="demos/macrepair.webp" width="900" alt="Standard and Full Repair for macOS: choosing an installer and reviewing the repair"></p>

**Standard and Full Repair for macOS.** The same two levels as iPhone. *Standard Repair* makes a restore point and
reinstalls macOS over itself — your files, apps and settings stay. *Full Repair* erases the Mac and installs a clean
macOS, like new (on Apple silicon through Erase All Content and Settings).

<p align="center"><img src="demos/repair.webp" width="900" alt="Reviewing and running a repair: exact steps, risk badge, live log and a stitched-shut success animation"></p>

**Repairs you can see.** Every repair shows its risk and the exact commands first. While it runs, a seam stitches
itself shut as the percentage climbs and the live log is colour-coded line by line (errors red, success green,
numbers cyan). It finishes with a check, confetti and a chime.

<p align="center"><img src="demos/ai.webp" width="900" alt="Mend AI diagnosing an iPhone stuck on the Apple logo and offering Run buttons"></p>

**Mend AI.** Describe the problem; the AI answers with the safest steps first and turns its suggestions into Run
buttons. It reads the Fix Library too, so its advice matches known fixes. Free for everyone, or use GitHub Copilot,
any local model or an online AI.

<p align="center"><img src="demos/resize.webp" width="900" alt="The Mend window shrinking from 1300 to 760 pixels while every part rearranges to fit"></p>

**Fits any window.** Shrink the window and everything rearranges instead of overlapping: the sidebar folds into an
icon rail, the overview's rings move under the title, cards stack and text wraps.

<p align="center"><img src="demos/disks.webp" width="900" alt="Disks and Partitions: clicking partitions on a colour map"></p>

**Disks & Partitions.** Every disk as a colour map — one colour per file system. Click a partition for its details
and repairs; the system disk is protected.

<p align="center"><img src="demos/health.webp" width="900" alt="Disk Health: SMART score ring, temperature, wear and findings"></p>

**Disk Health.** A health score ring, temperature, wear, power-on time and plain findings from SMART, plus a speed
test and a full read scan.

<p align="center"><img src="demos/diskreport.webp" width="900" alt="Full disk report: health and lifetime gauges, years left, endurance, temperature bar, read/write statistics and every SMART indicator"></p>

**Full disk report.** Every SMART and NVMe indicator with its status, plus health and
lifetime-left gauges, years left at 8 hours a day, projected endurance, data written per powered-on day,
temperature against its limits, read/write statistics since start-up, errors and retries — and each finding comes
with the repair that fixes it: remap bad sectors, a write test that forces remapping, TRIM, self-tests, or the
memory and process checks behind heavy daily writing. A four-state **SMART status** — OK · Warning · Failing · Failed —
stands beside the gauges, and a drive that gives no SMART data (many USB enclosures) says *no data*, never “100 % good”.
Export it as text, Markdown or a web page — one report for all disks, or **Save report** on each disk card and
**Save each disk** for one file per drive. Hard-disk extras: the drive's temperature history as a sparkline, **Stop head
parking** (APM 254) when the heads park many times an hour, stop the spin-down timer, turn the write cache on.

<p align="center"><img src="screenshots/hddlife.png" width="900" alt="Hard-disk life estimate: age, head parking and start-stop counts as bars, with the lowest setting the estimate"></p>

**Hard-disk life left.** Hard drives have no wear counter, so Mend estimates their life left from:
- age, against the usual service life of desktop, laptop or NAS drives;
- head parking and start-stop counts, against their ratings;
- any bad sectors.

It shows which of these sets the figure, and the years left. **Full report for all** reads every disk at once, and a
Disk Health setting (on by default) shows it whenever the page opens.

<p align="center"><img src="demos/coverage.webp" width="900" alt="How Standard and Deep Repair fix problems: what each replaces, keeps and why it works"></p>

**500+ problems per repair, counted honestly.** Every repair screen shows what it resolves: iPhone Standard Repair
1,118 and Deep Repair 1,126, Mac Standard Repair 1,107 and Full Repair 1,115, disk Standard Repair (check and repair) 1,024 and Full Repair (erase and reformat) 1,280, and contacts Fix everything 336 and Rebuild 420. Problems a reinstall can't fix — accessories,
apps, accounts, carriers and hardware — are listed separately with their steps. Each repair screen explains how it
works: Standard Repair puts back a perfect copy of the system and keeps your data, which removes damaged, half-updated
or mismatched system files; Full Repair also erases your data, which is where a forgotten passcode, unwanted
management or malware lives. Every fix in the Library says which repair resolves it.

<p align="center"><img src="demos/contacts.webp" width="900" alt="Contacts overview: every source in a side pane — this Mac's iCloud, Google and Outlook accounts, iCloud/CardDAV, iPhones, Android accounts and Mend's library — orbiting one contact card"></p>

**Contacts — every account separately, like Contacts on the Mac.** Laid out like KDE Kontact: a side pane of sources,
nothing ever merged:
- **This Mac:** every account in the Mac's Contacts — any number of iCloud, Google, Outlook/Exchange and Yahoo accounts, plus On My Mac — read and edited through Apple's own Contacts framework.
- **iCloud and CardDAV accounts** signed in here.
- **Every iPhone and iPad**, from its backup, with photos and groups.
- **Every account on every Android phone.**
- **Mend's own library:** address books kept as .vcf, with earlier versions kept.
- **Open files:** .vcf, Google or Outlook .csv, and Thunderbird .ldif.

The overview shows totals, problems and birthdays this month, and finds a person in every source at once.

<p align="center"><img src="screenshots/contactcard.png" width="900" alt="A contact with every field and phone number details: India, mobile, real number, international, E.164 and local forms"></p>

**Every field, and every number explained.** Names with prefix, middle, maiden and phonetic forms; work; phones,
emails, addresses, websites, messaging, social profiles, related people, dates, groups and notes. Each phone number is
checked with Google's numbering rules for every country. Mend shows:
- its flag and country, and the type of line (mobile, landline, toll-free, VoIP);
- whether it can really exist;
- its international, E.164 and local forms;
- Call and WhatsApp buttons, and a one-click fix to the international form.

<p align="center"><img src="screenshots/contactfixer.png" width="900" alt="Contact fixer: problems grouped by kind with examples and one Fix button"></p>

**Fix, merge, group and move.** Every source has tabs:
- **Fix everything:** 16 kinds of problem fixed in one go.
- **Duplicates:** merged within that source only.
- **Numbers:** every number with its details.
- **Groups:** the Mac's own groups, or vCard categories.
- **Birthdays & dates:** with a calendar file.
- **Copy & move:** to any account, a library book, an Android phone, or a .vcf, .csv or .ldif file.

Broken .vcf files are repaired as they open.

<p align="center"><img src="screenshots/iphonedata.png" width="900" alt="iPhone data: Messages, WhatsApp, call history, contacts, notes and Safari tiles from a backup"></p>

**iPhone data.** Browse and export Messages, WhatsApp, call history, contacts, notes, Safari, calendar and voicemail
from a backup — as CSV or a printable page — copy out photos, voice memos and WhatsApp media, check a backup for
spyware with MVT, and move everything from one iPhone to another.

<p align="center"><img src="screenshots/othermac.png" width="900" alt="Repair another Mac: two Macs connected by USB-C, one in DFU, with Revive and Restore"></p>

**Repair another Mac.** Connect a Mac that won't start, put it in DFU with the key guide for its model, and revive
it (keeps its files) or restore it (clean macOS) from this Mac. Or share its disk and run First Aid, copy its files
off, or reinstall macOS onto it.

**Any number of devices.** Every connected iPhone, iPad, Android and Mac — normal, Recovery or DFU — gets its own
tabs, and repairs run side by side. Switching tabs or screens never stops a running job.

<p align="center"><img src="demos/backupfix.webp" width="900" alt="A failed iPhone backup explained: the reason in plain words and buttons that fix it"></p>

**Backups that explain themselves.** If an iPhone backup fails, Mend says why in plain words — not trusted, locked,
old tools, no space — and shows the buttons that fix it: Trust again, build the newest iPhone tools, choose another
folder, or back up with Apple Configurator, which works with every iOS version.

<p align="center"><img src="demos/helpers.webp" width="900" alt="Installing a helper: the missing commands are listed and Mend notices by itself when the install finishes"></p>

**Helpers that set themselves up.** Mend lists exactly which free tools are missing and installs only those. If
Homebrew already has a package, Mend links it instead of reinstalling. idevicerestore is built straight from
GitHub into your home folder, with no sudo. Mend notices by itself when an install finishes. With Apple Configurator
installed, iPhone repair needs nothing else.

<p align="center"><img src="screenshots/health.png" width="900" alt="Disk Health: an animated SSD, the health ring and every statistic"></p>

**Health over time.** Every disk gets an animated drive (a spinning platter for hard drives, flickering cells for
SSDs). Its health, life left and the iPhone battery's capacity are kept day by day and drawn as lines that show the
trend. While Mend is open, it re-checks every disk once a day and warns if health drops.

<p align="center"><img src="demos/sell.webp" width="900" alt="Prepare an iPhone to sell: each step ticked off, with buttons for backup and erase"></p>

**Sell or give away.** A checklist for iPhone and Mac: back up, unpair the Watch, sign out of iCloud (which turns off
Activation Lock), remove the SIM, erase. Tick each step off; Mend does the backup and the erase for you. Contacts
also show a **QR code**: point any phone camera at it to add the contact.

<p align="center"><img src="demos/theme.webp" width="900" alt="Switching between light and dark themes with a circular reveal"></p>

**Light and dark.** The theme switches with a circular reveal from where you click. Nine colours, never pink, each
readable on every surface.

## AI

- **Mend AI, built in and free for everyone** — no account, no key, nothing to set up
- **GitHub Copilot CLI and GitHub Models** — use the AI you already have with GitHub
- **Every local AI** — Ollama, LM Studio, llama.cpp, Jan, GPT4All, LocalAI, vLLM, KoboldCpp, Msty, AnythingLLM
- **Online AI services** — any provider, by URL and API key
- **Diagnose** — describe the problem; Mend AI suggests the safest repair first, with one-click Run buttons
- **Explains everything** — every result, log and repair word (DFU, IPSW, SMART, GPT, BCD…) in plain words
- **Safe** — the AI can only suggest repairs from Mend's own list; anything risky shows the exact steps first

## Features

- **Your account** — one email for every build and store: sign in with an emailed code (or password), this computer's
  licence is a signed token verified on the computer (12-hour refresh, 14 days offline); reinstalls never use a second
  seat; at the limit, deactivate another computer from the dialog; rename computers; redeem gift codes
- **Disk Health** — used · free · total per disk with a segment per volume, general information on every card, a
  free-space threshold with desktop notifications, SMART dashboard, a rescue plan for failing disks (back up, clone
  with ddrescue, remap, replace), read-only surface scan, self-tests (short, long, conveyance, stop, progress), the
  drive's error log and statistics, SMART through USB bridges and the SAT driver guide for external disks on a Mac
- **Duplicates** — identical files by content, look-alike pictures, and duplicates in cloud storages (rclone); keep
  rules; the Trash, never the last copy
- **Notifications that open Mend** — backups, disk warnings, low free space, devices; a click opens the right page
- **Right-click everywhere** — Finder Services (nothing to install), File Explorer verbs, GNOME Files / Dolphin /
  Nemo / Thunar entries; menu-bar icon, Dock menu and in-app menus with Devices ▸ / Disks ▸ / Go to ▸ / Back up ▸ /
  Repair ▸ / Appearance ▸ / Language ▸ drop-downs
- **iPhone & iPad** — Recovery Mode in and out in one click (free), Standard repair (keeps data, 1,118 problems), Deep repair
  (clean iOS, 1,126) from signed firmware verified by SHA-256, DFU guide, battery health, backups and restore, apps, screenshots, live console
- **Android** — reboot to Recovery / Bootloader / Fastboot / Sideload, exit Fastboot, official OTA and factory-image
  repair, partition flashing, apps, photo and file copy, screenshots, logcat
- **Mac repair** — First Aid, home permissions, Spotlight, “Open With”, fonts, DNS, Safe Mode and Recovery restarts,
  NVRAM, macOS installers and bootable USB installers, local snapshots; **Standard Repair** (reinstall macOS, keep
  data, 1,107 problems) and **Full Repair** (erase, clean macOS, 1,115); restart a stuck part (sound, Bluetooth,
  iCloud Drive, menu bar, notifications, Quick Look, Dock, print queue) and see what's going on (CPU, memory,
  sleep blockers, battery, background items, extensions, profiles, recent faults, Time Machine, firewall)
- **Windows repair** — SFC, DISM, CHKDSK, Startup Repair, BCD backup and rebuild, network and Windows Update resets,
  restore points, registry backup, problem drivers
- **Linux repair** — broken packages, GRUB, initramfs, failed services, errors since boot, desktop reset
- **Corrupted settings fixer** — finds damaged preference files and moves them aside (never deletes)
- **Partition manager** — create, delete, resize, format, erase, wipe, convert MBR→GPT, clone; the system disk is protected
- **Deep disk health** — SMART score, temperature, wear, bad sectors, self-tests, speed test, read scan; a full
  report with every indicator, lifetime left, years left, endurance and read/write statistics, exported as text,
  Markdown or HTML; repairs for bad sectors (remap, write test), TRIM and worn drives
- **Tiny backups** — content-defined de-duplication and zstd; verify, browse, restore single files
- **Contacts (Kontact-style)** — every account separately: this Mac's iCloud, Google, Outlook/Exchange, Yahoo and
  On My Mac accounts; iCloud/CardDAV; every iPhone (from its backup) and every Android account; Mend's own versioned
  library; .vcf / .csv / .ldif files. Every field, phone-number details for every country, groups, birthdays (.ics),
  fix 16 kinds of problem, merge duplicates, copy or move anywhere
- **iPhone data** — Messages, WhatsApp, calls, contacts, notes, Safari, calendar and voicemail from a backup, exported
  as CSV, HTML or an **evidence report** (hashes, device identity, metadata, attachments, page numbers); photos,
  message attachments, voice memos, voicemail, WhatsApp media, notes attachments, ringtones and books; MVT spyware
  check; transfer to another iPhone
- **Device files** — browse an iPhone or iPad like a drive over USB or Wi-Fi; copy both ways; Quick Transfer into apps
- **Configurator** — build, sign and install configuration profiles (Wi-Fi, restrictions, Kiosk Mode, web clips,
  passcode); supervise; act on every connected device at once
- **App downloads** — App Store apps as .ipa files with your own Apple Account, installed on any of your devices
- **Automatic backups** — scheduled (even with Mend closed), Wi-Fi, snapshots, archiving, automatic cleaning, any drive or NAS
- **Command line** — `mend devices`, `mend backup --udid all --wifi --keep 10`, `mend export messages --backup … --csv`,
  `mend files <udid> ls /DCIM` and more (Settings › Command line sets it up)
- **15 languages** — the interface and Mend AI's answers
- **Separate, incremental backups** — each kind of data on each device on its own; only what's new or changed is saved
- **Contacts to iCloud** — fix backed-up contacts, merge duplicates and add them to iCloud or any internet account
- **Dock, menu bar or background** — choose where Mend shows itself, with a menu-bar (tray) menu
- **Backups that carry on** — a backup that drops part-way (mobilebackup2 -4) resumes by itself; the connection
  service can be restarted from the error
- **Right-click menus and a Dock menu** — everywhere, fitted to what's under the pointer
- **Repair another Mac** — revive or restore an Apple silicon Mac in DFU, or repair a Mac shared as a disk
- **Any number of devices** — every connected phone and Mac gets its own tabs and repairs run side by side
- **Fix Library** — 16,826 problems for 16 kinds of device (iPhone, iPad, Mac, Apple Watch, Apple TV, AirPods,
  HomePod, Vision Pro, Android, Windows, Linux, ChromeOS, FreeBSD, Haiku, disks, contacts), each written for that
  model's buttons, menus and commands; tick off steps, save fixes, mark them fixed, copy steps; also searchable from ⌘K
- **Checkup** — a scored, read-only health check of this computer, its disks and connected phones, with Fix buttons
- **Repair report** — export the checkup, devices, disks, fixed problems and recent repairs as Markdown
- **Colour-coded everything** — paths, keys, numbers, brackets, file names, commands to type, device and system names,
  XML and log lines each have their own colour (no pink), in every screen, tab and menu
- **Sounds and motion** — a heartbeat startup show, animated illustrations, a repair that stitches itself shut,
  an animated picture for every device family, plug-in chimes, 100+ synthesised sounds and ten sound packs; light and dark themes

**AI tidy for contacts.** Names like `RAVI KUMAR WORK NEW 2024 🔥` become `Ravi Kumar`; a six-line note becomes
two lines that still carry every number, date and amount — proposed by the AI you chose (a local model on your Mac
keeps everything on the computer), shown as before → after rows you tick before anything is saved.

## Screenshots

| | |
|---|---|
| ![Overview](screenshots/home.png) <br> *Overview — devices, disk health, one-click fixes* | ![Fix Library](screenshots/devices.png) <br> *Fix Library — 16,826 problems, 16 kinds of device* |
| ![Files](screenshots/files.png) <br> *Device files — browse, copy, Quick Transfer* | ![Configurator](screenshots/configurator.png) <br> *Configurator — profiles, Kiosk Mode, supervision* |
| ![Automatic backups](screenshots/autobackup.png) <br> *Automatic backups — schedule, snapshots, cleaning* | ![Tamil](screenshots/tamil.png) <br> *15 languages — here in Tamil* |
| ![Separate backups](screenshots/separate.png) <br> *Separate backups — each kind on its own, incremental* | ![Contacts to iCloud](screenshots/tocloud.png) <br> *Fix backed-up contacts and add them to iCloud* |
| ![Settings](screenshots/presence.png) <br> *Dock, menu bar or background* | ![Account](screenshots/account.png) <br> *Your account — one email for every build, computers and seats* |
| ![Duplicates](screenshots/dups.png) <br> *Duplicates — identical files, look-alike pictures, cloud storages* | ![Disk Health](screenshots/health2.png) <br> *Disk Health — used/free per volume, general information, rescue plan* |
| ![iPhone](screenshots/ios.png) <br> *iPhone & iPad — Recovery Mode, repair, backups* | ![Android](screenshots/android.png) <br> *Android — Recovery, Fastboot, OTA repair* |
| ![Disks](screenshots/disks.png) <br> *Disks & Partitions — colour map of every disk* | ![Health](screenshots/health.png) <br> *Disk Health — SMART, wear, temperature* |
| ![Backups](screenshots/backup.png) <br> *Tiny Backups — a fraction of the size* | ![Contacts](screenshots/contacts.png) <br> *Contacts — every account side by side, nothing merged* |
| ![System](screenshots/system.png) <br> *System repair* | ![Mend AI](screenshots/ai.png) <br> *Mend AI — diagnose and run the fix* |
| ![Disk report](screenshots/diskreport.png) <br> *Full disk report — gauges, estimates, every indicator* | ![Contacts](screenshots/contactcard.png) <br> *Contacts — every account, every field, number details* |
| ![Backup](screenshots/backupfix.png) <br> *A failed backup explained, with its fixes* | ![Sell](screenshots/sell.png) <br> *Sell or give away — a checklist with buttons* |
| ![HDD life](screenshots/hddlife.png) <br> *Hard-disk life left — how it's worked out* | ![Contact fixer](screenshots/contactfixer.png) <br> *Contact fixer — 16 kinds of problem in one go* |
| ![iPhone data](screenshots/iphonedata.png) <br> *iPhone data — messages, WhatsApp, calls, notes* | ![Another Mac](screenshots/othermac.png) <br> *Repair another Mac — DFU revive and restore* |

## Helpers

Mend drives free, open tools for phones and SMART data. It shows what's missing and opens a terminal with the install command:
macOS `brew install libimobiledevice libirecovery ideviceinstaller smartmontools ipatool` (idevicerestore and afcclient for device files come with the newest libimobiledevice, which Mend builds for you; Apple Configurator adds profiles and supervision) and
`brew install --cask android-platform-tools`; Debian/Ubuntu `sudo apt install libimobiledevice-utils ideviceinstaller idevicerestore usbmuxd smartmontools adb fastboot`;
Windows `winget install smartmontools.smartmontools Google.PlatformTools`.

## Install

**One way for every system — Pour.** Pour is the package manager for ipconfig.co.network apps; the first line installs
Pour, the second installs Mend (and later `pour upgrade mend` updates it):

```bash
curl -fsSL https://ipconfig.co.network/pour/install | sh
pour install --cask mend
```

That works on **macOS** (Apple silicon and Intel), **Linux** (x86_64 and ARM64, AppImage or .deb), **ChromeOS** (inside the
Linux development environment) and **FreeBSD**. On **Windows** download
[pour-windows-x86_64.exe](https://ipconfig.co.network/pour/install?os=windows) (or run `irm https://ipconfig.co.network/pour/install.ps1 | iex` in PowerShell), then:

```powershell
pour install --cask mend
```

`pour apps` lists everything Pour can install; `pour remove mend` uninstalls. There is no Homebrew formula, cask or tap for Mend.

**If you'd rather not use Pour** — Mend's own one-line installer or a plain download:

- **macOS** — Terminal: `curl -fsSL https://ipconfig.co.network/updates/mend/install.sh | bash` copies **Mend.app** to `/Applications`
  and clears the quarantine flag. From the DMG by hand instead: run `xattr -cr /Applications/Mend.app` once before the first launch.
- **Windows** — PowerShell: `irm https://ipconfig.co.network/updates/mend/install.ps1 | iex`. SmartScreen may warn on first launch:
  *More info → Run anyway*. The same command installs the **ARM64** build on Windows on Arm (Snapdragon / Surface Pro X and similar) —
  or download `Mend_1.0.12_arm64-setup.exe` from the [latest release](https://github.com/JKS-sys/mend-08-oct-2026-releases/releases/latest).
- **Linux x86_64** — AppImage: `curl -fsSL https://ipconfig.co.network/updates/mend/install.sh | bash` (installs to `~/.local/bin/mend`),
  or download `Mend_1.0.12_amd64.AppImage`, then `chmod +x Mend_*.AppImage && ./Mend_*.AppImage` (needs `libfuse2`).
  Debian / Ubuntu: `… | bash -s -- --deb`, or `sudo apt install ./Mend_1.0.12_amd64.deb`.
- **Linux ARM64** (Raspberry Pi 4/5 with a 64-bit OS, ARM laptops and servers) — the same installer line picks `Mend_1.0.12_arm64.deb`
  (`sudo apt install ./Mend_1.0.12_arm64.deb` by hand). ARM64 Linux has a .deb only — there is no ARM AppImage.
- **ChromeOS** — **Settings → Advanced → Developers → Linux development environment → Turn on**, open the **Terminal** app and run
  the Pour lines above (or the installer line — it reads `dpkg --print-architecture` and picks `amd64` or `arm64`). Open Mend from
  the launcher (**Linux apps**). ChromeOS limits USB passthrough, so phone repair and SMART may not reach devices; backups,
  contacts and the AI work fully. Share folders with Linux from the Files app.
- **FreeBSD** (amd64, FreeBSD 14 or later, with a desktop) — as root: `pkg install webkit2-gtk_41 libimobiledevice smartmontools bash curl`,
  then the Pour lines or the installer line. By hand: `tar -xzf Mend_1.0.12_freebsd_amd64.tar.gz && sudo sh install.sh`
  installs to `/usr/local/bin/mend` with a menu entry and icon (`sh install.sh --uninstall` removes them).
- **Haiku** — Haiku isn't supported: Mend's window engine (Tauri/WebKit) has no Haiku port.

Mend updates itself on macOS, Windows (x64 and ARM64) and Linux (AppImage and .deb, x86_64 and ARM64): when a new
version is out it offers to install it and restart. A .deb update asks for your password, like any package install.
On FreeBSD, run `pour upgrade mend` (or the installer again) to update.

## Platforms

| System | CPU | Download | Updates itself |
|---|---|---|---|
| macOS 10.15+ | Apple silicon | `Mend_1.0.12_aarch64.dmg` | yes |
| macOS 10.15+ | Intel | `Mend_1.0.12_x64.dmg` | yes |
| Windows 10 / 11 | x64 | `Mend_1.0.12_x64-setup.exe` | yes |
| Windows 11 | ARM64 | `Mend_1.0.12_arm64-setup.exe` | yes |
| Linux | x86_64 | `Mend_1.0.12_amd64.AppImage` · `Mend_1.0.12_amd64.deb` | yes |
| Linux | ARM64 | `Mend_1.0.12_arm64.deb` | yes |
| ChromeOS (Linux development environment) | x86_64 / ARM64 | the Linux `.deb` for the Chromebook's CPU | yes |
| FreeBSD 14+ | amd64 | `Mend_1.0.12_freebsd_amd64.tar.gz` | no — rerun the installer |
| Haiku | — | not available | — |

Haiku isn't supported: Mend's window engine (Tauri/WebKit) has no Haiku port, so there is no installer to build —
the Fix Library still covers Haiku problems, and a Haiku machine can be reached over SSH from Mend on another computer.

Every installer above is built on the creator's Mac (`update.sh`: Windows with cargo-xwin + NSIS, Linux in Docker);
Mac App Store and Microsoft Store packages are made with `--stores` when the store keys are present.

## Pricing

| Free | Pro monthly | Pro yearly |
|---|---|---|
| ₹0 | **₹4,000 / month** | **₹6,000 / year** |
| Download and use Mend for free | Renews every month, cancel any time | Renews every year — two months cheaper |

After paying you get an activation code at once; in Mend open **Activate Pro** and paste it.

[Get Mend Pro →](https://ipconfig.co.network/mend/buy?plan=monthly) · [yearly](https://ipconfig.co.network/mend/buy?plan=yearly)

## Links

⭐ Found Mend useful? **Star this repository** — it helps others find it.

- Releases and downloads: https://github.com/JKS-sys/mend-08-oct-2026-releases/releases
- Website: https://ipconfig.co.network/mend
- Release notes: [RELEASE-NOTES.md](RELEASE-NOTES.md)
- Update feed: [latest.json](latest.json)

## Creator

Made by Jagadeesh Kumar S, creator — [youtube.com/@JKS-sys](https://www.youtube.com/@JKS-sys)

## Licence

Proprietary. © 2026 Jagadeesh Kumar S. All rights reserved.
The installers are free to download and use; the source code is not published, and copying,
modifying or redistributing Mend is not permitted without written permission.
