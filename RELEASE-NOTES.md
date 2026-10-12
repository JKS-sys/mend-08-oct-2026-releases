# Mend release notes

Newest first. Downloads: https://github.com/JKS-sys/mend-08-oct-2026-releases/releases/latest · https://ipconfig.co.network/mend

## Mend 1.0.8 — 12 Oct 2026

- **Backups that carry on after a dropped connection:** “Could not receive from mobilebackup2 (-4) … Backup Aborted” is now explained (the iPhone locked or slept, the cable moved or a hub dropped power) and the backup continues by itself, incrementally, up to three tries — in the app and in `mend backup`. Apple Configurator's “Failed to connect to the device (-2)” right after asks you to reconnect first. A new button restarts the iPhone connection service (usbmuxd, or Apple Mobile Device Service on Windows). Progress bars no longer fill the log with hundreds of identical lines.
- **Separate, incremental backups for every device:** each kind of data on its own — iPhone/iPad contacts, messages, WhatsApp, calls, notes, calendar, Safari, bookmarks, voicemail, photos, music, ringtones, books and recordings; Android contacts (each account), camera photos, pictures, WhatsApp media, downloads, documents, music, movies and recordings; and every contacts account on this computer. Data is saved as a new version only when it changed; files are mirrored, copying only what's new or changed. “Back up everything separately”, a folder of your choice (drive or NAS), and an overview of every device on the Tiny Backups page.
- **Fix backed-up contacts and add them to iCloud:** choose contacts saved from phones and backups; Mend fixes them, merges duplicates, skips people already in the account, saves a .vcf copy and adds the rest to iCloud, Google or any internet account.
- **Menu-bar (tray) icon and where Mend shows itself:** Dock and menu bar, Dock only, menu bar only, or background only (taskbar and tray on Windows and Linux). The menu-bar icon has the main commands; in menu-bar and background modes closing the window keeps Mend running, and starting Mend again shows it. Only one Mend runs at a time.
- **Schedules everywhere:** when there's no systemd user session (some ChromeOS containers) and on FreeBSD, automatic backups use cron.
- **Layouts:** separate-backup tiles use round buttons so names fit at every width; the overlap checker now accounts for clipped text.

- **11,570 repairs for 16 kinds of device:** the Fix Library adds iPad (21 model families), Apple Watch (13 models), Apple TV, AirPods, HomePod, Vision Pro, Android (12 makers), Windows 10, 11 and 11 on Arm (on 9 PC makers), Linux (16 distributions), ChromeOS, FreeBSD and Haiku, and grows disks to 3,039 (ReFS, ZFS, F2FS, M.2 SATA, RAID/NAS volumes, Thunderbolt docks and disk images). Each problem uses that model's own buttons, menus, recovery keys and commands, and says whether Standard Repair, Full Repair, steps or a part fixes it. Every family has its own animated picture and sound.
- **Device files (iMazing-style):** a Files tab browses an iPhone or iPad like a drive — photos, music files, ringtones, books, recordings — over USB or Wi-Fi; copy anything to the computer; Quick Transfer files or folders onto the device or into an app's Documents; new folder, rename, delete and a right-click menu.
- **Configurator:** a Manage tab builds configuration profiles (Wi-Fi, 16 restrictions, Kiosk Mode, web clips, passcode rules), shows the colour-coded XML, saves, signs (keychain certificate) and installs them on one or every connected device; supervises a freshly erased device; removes profiles; backs up, installs an .ipa on or restarts every connected device at once.
- **App downloads:** download App Store apps as .ipa files with your own Apple Account (ipatool) and install them on this device or all of them. Apps that share files are marked and open in the Files tab.
- **Automatic backups:** daily or weekly, over USB or Wi-Fi, one device or all, even while Mend is closed (launchd, systemd timer or Task Scheduler). Each backup keeps a snapshot (an APFS clone on a Mac), archived snapshots are kept forever, old ones are cleaned by count and age, and any drive or NAS can hold them. Backups can now be incremental.
- **Evidence reports:** Messages, WhatsApp and every other kind of backup data export as a printable report with case details, the device's serial and IMEI, SHA-256 of the source database and the backup manifest, a fingerprint of the rows, every message's metadata and attachments, page numbers and signature lines. New exports: message attachments, notes attachments, ringtones and books.
- **Command line:** `Mend --cli` (or `mend` after Settings › Command line): devices, info, backup (with snapshots and cleaning), backups, snapshots, export, extract, files and screenshot.
- **15 languages:** English, German, French, Spanish, Italian, Portuguese, Ukrainian, Russian, Arabic, Japanese, Korean, Simplified and Traditional Chinese, Hindi and Tamil for menus, tabs and buttons; Mend AI answers in the chosen language. Follows the computer's language on first start.
- **Right-click menus everywhere and a Dock menu:** text fields, selected text, links, logs and code, sidebar places and fixes each get their own items, plus every app command. Right-click Mend in the Dock for Find a Repair, Checkup, Mend AI, each area, Back Up iPhone Now and Full Disk Report.
- **Closing the window quits Mend completely** (also ⌘W and the new Quit item), stopping running helpers; nothing stays behind in the Dock.
- **Disk Health art no longer crowds the text:** the SSD/HDD picture sits in its own tile with a label, clear of the health ring and the heading.
- **More colour:** commands to type and device and system names get their own colours, the XML of profiles is colour-coded, folder paths alternate colours, and menu icons each take a colour.
- **More sounds:** device files, transfers, snapshots, schedules, profiles, evidence, printing, languages, Kiosk Mode, app downloads, menus, quitting, every connected device, and a motif per device family.

- **Standard Repair and Full Repair for macOS:** the same two levels as iPhone. Standard Repair makes a restore point and reinstalls macOS over itself — files, apps and settings stay. Full Repair erases the Mac and installs a clean macOS (Erase All Content and Settings on Apple silicon). Pick the installer in the new “Standard & Full Repair” tab.
- **4,109 fixes, and 1,000+ for every repair:** the Fix Library now holds 1,223 iPhone & iPad, 1,159 Mac, 1,307 disk and 420 contact problems. Each repair screen shows exactly what it resolves:
  - **iPhone:** Standard Repair 1,118, Deep Repair 1,126.
  - **Mac:** Standard Repair 1,107, Full Repair 1,115.
  - **Disks:** Standard Repair (check and repair the file system) 1,024; Full Repair (erase and reformat) 1,280 — every common file system on every kind of drive, with that file system's own repair commands.
  - **Contacts:** Fix everything 336, Rebuild 420 — every real problem kind in each of 14 kinds of source.
  - It also shows, honestly, which problems need steps or hardware instead. Tap a number to see the list. The Library has new Disks and Contacts tabs.
- **Disk health beyond DriveDx:** “Full report” reads every SMART/NVMe indicator, then shows health and lifetime-left gauges, years left at 8 h a day, projected endurance, data written per powered-on day, temperature against its limits, read/write statistics since start-up, errors and retries, and a finding for each problem with the repair that fixes it. Export the report as text, Markdown or a web page.
- **Repairs for bad sectors and worn disks:** remap bad sectors (chkdsk /r on Windows, a non-destructive badblocks pass on Linux), a write test that forces remapping (Linux, erases), zero-and-remap for Mac disks (erases), TRIM (trimforce, fstrim, ReTrim), long self-tests and turning SMART on. Heavy daily writing is flagged with what causes it.
- **Contact manager, Kontact style — every account separately, like Contacts on the Mac:** a side pane lists every source and nothing is ever merged:
  - **This Mac:** every account in the Mac's Contacts — any number of iCloud, Google, Outlook/Exchange and Yahoo accounts, plus On My Mac — read and edited through Apple's Contacts framework.
  - **iCloud and CardDAV accounts** signed in here (Fastmail, Yahoo, Nextcloud…).
  - **Every iPhone and iPad**, read from its backup with photos and groups.
  - **Every account on every Android phone**, each Google account and the SIM listed separately.
  - **Mend's own library:** address books kept as .vcf in ~/Mend/Contacts/Library, with the last 30 versions of each kept so any earlier version can be brought back.
  - **Open files:** .vcf, Google or Outlook .csv, and Thunderbird .ldif.
  - **Overview page:** totals, problems, birthdays this month, a search across every source (results stay labelled by source), "Load every source" and "Save every source to the library".
  - **Each source has tabs:** Contacts, Groups (the Mac's own groups or vCard categories), Birthdays & dates (with a calendar .ics), Fix everything, Duplicates, Numbers, and Copy & move (to any account, a library book, an Android phone or a file).
- **Every contact field:** prefix, middle and maiden names, phonetic names, department and role, any number of phones, emails, addresses (with a map link), websites, messaging (WhatsApp, Telegram, Skype…), social profiles, related people, birthday and other dates, groups and notes. Apple's labels are kept, so cards look the same on the iPhone.
- **Phone numbers in detail:** every number is checked with Google's numbering rules for every country. Mend shows:
  - the country and its flag;
  - the type of line: mobile, landline, toll-free, VoIP…;
  - whether the number can really exist;
  - its international, E.164 and local forms, each copyable;
  - Call and WhatsApp buttons, and a one-click fix to the international form.
- **Any number of devices at once:** every connected iPhone, iPad, Android and Mac — in normal, Recovery or DFU mode — gets its own tabs, and repairs run side by side. Changing tab or screen never stops a running job.
- **iPhone data (iMazing-style):** browse and export Messages, WhatsApp, call history, contacts, notes, Safari, calendar and voicemail from a backup (CSV or a printable page), copy out photos, voice memos and WhatsApp media, check a backup for spyware with MVT, and transfer one iPhone to another.
- **Repair another Mac:** revive or restore an Apple silicon Mac in DFU from this Mac with Apple Configurator, with key guides for every Mac; or share its disk and run First Aid, back it up or reinstall macOS onto it. iPhone repair also works through Apple Configurator when idevicerestore can't be installed.
- **No overlaps in small windows:** every screen and tab, including every Contacts view, was checked at 560, 760, 900, 1000 and 1240 px wide.
- **Hard-disk life left:** hard drives have no wear counter, so Mend now estimates their life. It weighs power-on hours against the usual service life of desktop, laptop or NAS drives, head load cycles and start-stops against their ratings, and any bad sectors, then shows which of these sets the figure. It appears as a gauge, a breakdown, years left at 8 hours a day or 24/7, and a line in the exported report.
- **Full report for all disks:** one button reads every disk. A Disk Health setting (on by default) shows the full report for every disk whenever the page opens. The full report now works on Windows too (with smartmontools). TRIM is offered only for SSDs.
- **How each repair fixes problems:** iPhone and Mac repair screens explain step by step what Standard and Full (Deep) Repair replace, what they keep and why that fixes problems. Every fix in the Fix Library is marked with what resolves it: Standard Repair, Full Repair, the steps, or hardware.
- **iPhone Apps tab fixed:** it uses the current ideviceinstaller (`list --xml`) and falls back to older versions. It lists your apps, Apple's apps or all, sorts by name or size, and shows the real error if the iPhone doesn't answer.
- **No more caps:** long lists (contacts, chats, backup files, Android apps, unreadable files) load more as you scroll instead of stopping at a few hundred. iPhone Safari and calendar history is read in full. Any number of iPhones, iPads and Macs can be connected and repaired at the same time.
- **Helpers are found where they really are:**
  - **Apple Configurator from the App Store is detected straight away.** Mend uses its tool from inside the app (or finds the app with Spotlight), so "Install Automation Tools" is no longer needed.
  - **No more "already installed" loop for libimobiledevice and ideviceinstaller.** Mend shows exactly which commands are missing and installs only those Homebrew packages; if Homebrew already has a package, it relinks it instead of reinstalling. ideviceinstaller (for the Apps tab) is now its own helper.
  - **Mend notices installs by itself.** After you press Install it checks every few seconds, and again when you switch back to it — no "Check again" needed.
- **idevicerestore installs reliably:** Mend writes its own build script, which clones libimobiledevice, idevicerestore and ideviceinstaller from GitHub (retrying), builds the newest versions into ~/Mend/limd without sudo, and installs only the Homebrew packages that are missing — no more is.gd link (blocked on some networks) or "already installed" warnings. With Apple Configurator installed, idevicerestore is optional and shown as covered.
- **iPhone backups fixed:**
  - Mend's newest tool build fixes backups that fail with old libimobiledevice on recent iOS.
  - **Back up with Apple Configurator** is a second route that works with every iOS version.
  - A failed backup is explained in plain words, with buttons that fix it: Trust again, build the newest tools, back up with Apple Configurator, choose another folder.
- **Owner Panel → Active devices:** who is using Mend right now, today, this week and this month, on a live radar, with versions, systems, countries and a device list. The data comes from an anonymous heartbeat every 30 minutes: a hashed machine id, version, system and plan, never an IP address.
- **New features:**
  - **Health over time:** disk health, life left and iPhone battery capacity are kept day by day and drawn as lines.
  - **Daily disk watch** (on by default): Mend re-checks every disk once a day while it's open and warns if health drops.
  - **Repair history** for every device.
  - **QR codes** for contacts.
  - **"Sell or give away" checklists** for iPhone and Mac.
- **Mend Pro is now ₹4,000 a month or ₹6,000 a year.**
- **More colour and sound:** every tab has its own colour, and names start in colour. A new animated Contacts overview shows your sources orbiting a contact card. Gauges and date badges are animated. New sounds: sync, library book, dial, a birthday tune, gauge sweep, a wrench when you press Install, and a chime when a helper is ready. Button icons, table columns, fact labels and helper rows have their own colours; new animated pictures — a spinning hard disk or flickering SSD on every disk, an iPhone streaming into a backup drive (broken link when it fails), a toolbox with turning gears while helpers install, an active-devices radar — and new sounds for platters, flash chips and backup streams; section subtitles colour their numbers and paths, and an animated toolbox shows while a helper installs.
- **Checkup (⇧⌘C):** one button checks disks, free space, memory, security, battery, sleep, firewall, Time Machine, updates, recent errors and every connected phone — read-only — and gives a score with a Fix button for anything that needs attention.
- **Fix Library tools:** tick off steps as you go, save fixes with a star, mark a problem “It's fixed!”, filter by Saved, One-click or Fixed, and copy the steps to send to someone.
- **Repair report:** Helpers & Log → Export report saves the checkup, devices, disks, fixed problems and recent repairs as a Markdown file.
- **macOS keeps Mend's permissions after updates:** Mac builds are now signed with one permanent identity, so “Mend would like to access files on a removable volume” and the other permission prompts are asked once — not after every update. The prompts also explain why Mend asks.
- **More colour, no pink:** brackets change colour with each nesting level, section titles and borders take their section's colour, headings and dialog titles are tinted, and keys, numbers and file paths stand out everywhere.
- **More graphics, motion and sound:** gauges that sweep to their value, a temperature bar, a cable pulse between two Macs when one is found in DFU, chat bubbles for messages, colour-coded problem cards in the contact fixer; a radar sweep for the Checkup, an animated Mac being reinstalled, platform icons orbiting the startup logo, a slow colour aurora behind every screen, a colour sweep when you change screens, and new sounds — a note per area, radar, tick-off, star, “fixed” fanfare and report.

## Mend 1.0.7 — 12 Oct 2026

- **11,570 repairs for 16 kinds of device:** the Fix Library adds iPad (21 model families), Apple Watch (13 models), Apple TV, AirPods, HomePod, Vision Pro, Android (12 makers), Windows 10, 11 and 11 on Arm (on 9 PC makers), Linux (16 distributions), ChromeOS, FreeBSD and Haiku, and grows disks to 3,039 (ReFS, ZFS, F2FS, M.2 SATA, RAID/NAS volumes, Thunderbolt docks and disk images). Each problem uses that model's own buttons, menus, recovery keys and commands, and says whether Standard Repair, Full Repair, steps or a part fixes it. Every family has its own animated picture and sound.
- **Device files (iMazing-style):** a Files tab browses an iPhone or iPad like a drive — photos, music files, ringtones, books, recordings — over USB or Wi-Fi; copy anything to the computer; Quick Transfer files or folders onto the device or into an app's Documents; new folder, rename, delete and a right-click menu.
- **Configurator:** a Manage tab builds configuration profiles (Wi-Fi, 16 restrictions, Kiosk Mode, web clips, passcode rules), shows the colour-coded XML, saves, signs (keychain certificate) and installs them on one or every connected device; supervises a freshly erased device; removes profiles; backs up, installs an .ipa on or restarts every connected device at once.
- **App downloads:** download App Store apps as .ipa files with your own Apple Account (ipatool) and install them on this device or all of them. Apps that share files are marked and open in the Files tab.
- **Automatic backups:** daily or weekly, over USB or Wi-Fi, one device or all, even while Mend is closed (launchd, systemd timer or Task Scheduler). Each backup keeps a snapshot (an APFS clone on a Mac), archived snapshots are kept forever, old ones are cleaned by count and age, and any drive or NAS can hold them. Backups can now be incremental.
- **Evidence reports:** Messages, WhatsApp and every other kind of backup data export as a printable report with case details, the device's serial and IMEI, SHA-256 of the source database and the backup manifest, a fingerprint of the rows, every message's metadata and attachments, page numbers and signature lines. New exports: message attachments, notes attachments, ringtones and books.
- **Command line:** `Mend --cli` (or `mend` after Settings › Command line): devices, info, backup (with snapshots and cleaning), backups, snapshots, export, extract, files and screenshot.
- **15 languages:** English, German, French, Spanish, Italian, Portuguese, Ukrainian, Russian, Arabic, Japanese, Korean, Simplified and Traditional Chinese, Hindi and Tamil for menus, tabs and buttons; Mend AI answers in the chosen language. Follows the computer's language on first start.
- **Right-click menus everywhere and a Dock menu:** text fields, selected text, links, logs and code, sidebar places and fixes each get their own items, plus every app command. Right-click Mend in the Dock for Find a Repair, Checkup, Mend AI, each area, Back Up iPhone Now and Full Disk Report.
- **Closing the window quits Mend completely** (also ⌘W and the new Quit item), stopping running helpers; nothing stays behind in the Dock.
- **Disk Health art no longer crowds the text:** the SSD/HDD picture sits in its own tile with a label, clear of the health ring and the heading.
- **More colour:** commands to type and device and system names get their own colours, the XML of profiles is colour-coded, folder paths alternate colours, and menu icons each take a colour.
- **More sounds:** device files, transfers, snapshots, schedules, profiles, evidence, printing, languages, Kiosk Mode, app downloads, menus, quitting, every connected device, and a motif per device family.

- **Standard Repair and Full Repair for macOS:** the same two levels as iPhone. Standard Repair makes a restore point and reinstalls macOS over itself — files, apps and settings stay. Full Repair erases the Mac and installs a clean macOS (Erase All Content and Settings on Apple silicon). Pick the installer in the new “Standard & Full Repair” tab.
- **4,109 fixes, and 1,000+ for every repair:** the Fix Library now holds 1,223 iPhone & iPad, 1,159 Mac, 1,307 disk and 420 contact problems. Each repair screen shows exactly what it resolves:
  - **iPhone:** Standard Repair 1,118, Deep Repair 1,126.
  - **Mac:** Standard Repair 1,107, Full Repair 1,115.
  - **Disks:** Standard Repair (check and repair the file system) 1,024; Full Repair (erase and reformat) 1,280 — every common file system on every kind of drive, with that file system's own repair commands.
  - **Contacts:** Fix everything 336, Rebuild 420 — every real problem kind in each of 14 kinds of source.
  - It also shows, honestly, which problems need steps or hardware instead. Tap a number to see the list. The Library has new Disks and Contacts tabs.
- **Disk health beyond DriveDx:** “Full report” reads every SMART/NVMe indicator, then shows health and lifetime-left gauges, years left at 8 h a day, projected endurance, data written per powered-on day, temperature against its limits, read/write statistics since start-up, errors and retries, and a finding for each problem with the repair that fixes it. Export the report as text, Markdown or a web page.
- **Repairs for bad sectors and worn disks:** remap bad sectors (chkdsk /r on Windows, a non-destructive badblocks pass on Linux), a write test that forces remapping (Linux, erases), zero-and-remap for Mac disks (erases), TRIM (trimforce, fstrim, ReTrim), long self-tests and turning SMART on. Heavy daily writing is flagged with what causes it.
- **Contact manager, Kontact style — every account separately, like Contacts on the Mac:** a side pane lists every source and nothing is ever merged:
  - **This Mac:** every account in the Mac's Contacts — any number of iCloud, Google, Outlook/Exchange and Yahoo accounts, plus On My Mac — read and edited through Apple's Contacts framework.
  - **iCloud and CardDAV accounts** signed in here (Fastmail, Yahoo, Nextcloud…).
  - **Every iPhone and iPad**, read from its backup with photos and groups.
  - **Every account on every Android phone**, each Google account and the SIM listed separately.
  - **Mend's own library:** address books kept as .vcf in ~/Mend/Contacts/Library, with the last 30 versions of each kept so any earlier version can be brought back.
  - **Open files:** .vcf, Google or Outlook .csv, and Thunderbird .ldif.
  - **Overview page:** totals, problems, birthdays this month, a search across every source (results stay labelled by source), "Load every source" and "Save every source to the library".
  - **Each source has tabs:** Contacts, Groups (the Mac's own groups or vCard categories), Birthdays & dates (with a calendar .ics), Fix everything, Duplicates, Numbers, and Copy & move (to any account, a library book, an Android phone or a file).
- **Every contact field:** prefix, middle and maiden names, phonetic names, department and role, any number of phones, emails, addresses (with a map link), websites, messaging (WhatsApp, Telegram, Skype…), social profiles, related people, birthday and other dates, groups and notes. Apple's labels are kept, so cards look the same on the iPhone.
- **Phone numbers in detail:** every number is checked with Google's numbering rules for every country. Mend shows:
  - the country and its flag;
  - the type of line: mobile, landline, toll-free, VoIP…;
  - whether the number can really exist;
  - its international, E.164 and local forms, each copyable;
  - Call and WhatsApp buttons, and a one-click fix to the international form.
- **Any number of devices at once:** every connected iPhone, iPad, Android and Mac — in normal, Recovery or DFU mode — gets its own tabs, and repairs run side by side. Changing tab or screen never stops a running job.
- **iPhone data (iMazing-style):** browse and export Messages, WhatsApp, call history, contacts, notes, Safari, calendar and voicemail from a backup (CSV or a printable page), copy out photos, voice memos and WhatsApp media, check a backup for spyware with MVT, and transfer one iPhone to another.
- **Repair another Mac:** revive or restore an Apple silicon Mac in DFU from this Mac with Apple Configurator, with key guides for every Mac; or share its disk and run First Aid, back it up or reinstall macOS onto it. iPhone repair also works through Apple Configurator when idevicerestore can't be installed.
- **No overlaps in small windows:** every screen and tab, including every Contacts view, was checked at 560, 760, 900, 1000 and 1240 px wide.
- **Hard-disk life left:** hard drives have no wear counter, so Mend now estimates their life. It weighs power-on hours against the usual service life of desktop, laptop or NAS drives, head load cycles and start-stops against their ratings, and any bad sectors, then shows which of these sets the figure. It appears as a gauge, a breakdown, years left at 8 hours a day or 24/7, and a line in the exported report.
- **Full report for all disks:** one button reads every disk. A Disk Health setting (on by default) shows the full report for every disk whenever the page opens. The full report now works on Windows too (with smartmontools). TRIM is offered only for SSDs.
- **How each repair fixes problems:** iPhone and Mac repair screens explain step by step what Standard and Full (Deep) Repair replace, what they keep and why that fixes problems. Every fix in the Fix Library is marked with what resolves it: Standard Repair, Full Repair, the steps, or hardware.
- **iPhone Apps tab fixed:** it uses the current ideviceinstaller (`list --xml`) and falls back to older versions. It lists your apps, Apple's apps or all, sorts by name or size, and shows the real error if the iPhone doesn't answer.
- **No more caps:** long lists (contacts, chats, backup files, Android apps, unreadable files) load more as you scroll instead of stopping at a few hundred. iPhone Safari and calendar history is read in full. Any number of iPhones, iPads and Macs can be connected and repaired at the same time.
- **Helpers are found where they really are:**
  - **Apple Configurator from the App Store is detected straight away.** Mend uses its tool from inside the app (or finds the app with Spotlight), so "Install Automation Tools" is no longer needed.
  - **No more "already installed" loop for libimobiledevice and ideviceinstaller.** Mend shows exactly which commands are missing and installs only those Homebrew packages; if Homebrew already has a package, it relinks it instead of reinstalling. ideviceinstaller (for the Apps tab) is now its own helper.
  - **Mend notices installs by itself.** After you press Install it checks every few seconds, and again when you switch back to it — no "Check again" needed.
- **idevicerestore installs reliably:** Mend writes its own build script, which clones libimobiledevice, idevicerestore and ideviceinstaller from GitHub (retrying), builds the newest versions into ~/Mend/limd without sudo, and installs only the Homebrew packages that are missing — no more is.gd link (blocked on some networks) or "already installed" warnings. With Apple Configurator installed, idevicerestore is optional and shown as covered.
- **iPhone backups fixed:**
  - Mend's newest tool build fixes backups that fail with old libimobiledevice on recent iOS.
  - **Back up with Apple Configurator** is a second route that works with every iOS version.
  - A failed backup is explained in plain words, with buttons that fix it: Trust again, build the newest tools, back up with Apple Configurator, choose another folder.
- **Owner Panel → Active devices:** who is using Mend right now, today, this week and this month, on a live radar, with versions, systems, countries and a device list. The data comes from an anonymous heartbeat every 30 minutes: a hashed machine id, version, system and plan, never an IP address.
- **New features:**
  - **Health over time:** disk health, life left and iPhone battery capacity are kept day by day and drawn as lines.
  - **Daily disk watch** (on by default): Mend re-checks every disk once a day while it's open and warns if health drops.
  - **Repair history** for every device.
  - **QR codes** for contacts.
  - **"Sell or give away" checklists** for iPhone and Mac.
- **Mend Pro is now ₹4,000 a month or ₹6,000 a year.**
- **More colour and sound:** every tab has its own colour, and names start in colour. A new animated Contacts overview shows your sources orbiting a contact card. Gauges and date badges are animated. New sounds: sync, library book, dial, a birthday tune, gauge sweep, a wrench when you press Install, and a chime when a helper is ready. Button icons, table columns, fact labels and helper rows have their own colours; new animated pictures — a spinning hard disk or flickering SSD on every disk, an iPhone streaming into a backup drive (broken link when it fails), a toolbox with turning gears while helpers install, an active-devices radar — and new sounds for platters, flash chips and backup streams; section subtitles colour their numbers and paths, and an animated toolbox shows while a helper installs.
- **Checkup (⇧⌘C):** one button checks disks, free space, memory, security, battery, sleep, firewall, Time Machine, updates, recent errors and every connected phone — read-only — and gives a score with a Fix button for anything that needs attention.
- **Fix Library tools:** tick off steps as you go, save fixes with a star, mark a problem “It's fixed!”, filter by Saved, One-click or Fixed, and copy the steps to send to someone.
- **Repair report:** Helpers & Log → Export report saves the checkup, devices, disks, fixed problems and recent repairs as a Markdown file.
- **macOS keeps Mend's permissions after updates:** Mac builds are now signed with one permanent identity, so “Mend would like to access files on a removable volume” and the other permission prompts are asked once — not after every update. The prompts also explain why Mend asks.
- **More colour, no pink:** brackets change colour with each nesting level, section titles and borders take their section's colour, headings and dialog titles are tinted, and keys, numbers and file paths stand out everywhere.
- **More graphics, motion and sound:** gauges that sweep to their value, a temperature bar, a cable pulse between two Macs when one is found in DFU, chat bubbles for messages, colour-coded problem cards in the contact fixer; a radar sweep for the Checkup, an animated Mac being reinstalled, platform icons orbiting the startup logo, a slow colour aurora behind every screen, a colour sweep when you change screens, and new sounds — a note per area, radar, tick-off, star, “fixed” fanfare and report.

## Mend 1.0.6 — 12 Oct 2026

- **Standard Repair and Full Repair for macOS:** the same two levels as iPhone. Standard Repair makes a restore point and reinstalls macOS over itself — files, apps and settings stay. Full Repair erases the Mac and installs a clean macOS (Erase All Content and Settings on Apple silicon). Pick the installer in the new “Standard & Full Repair” tab.
- **4,109 fixes, and 1,000+ for every repair:** the Fix Library now holds 1,223 iPhone & iPad, 1,159 Mac, 1,307 disk and 420 contact problems. Each repair screen shows exactly what it resolves:
  - **iPhone:** Standard Repair 1,118, Deep Repair 1,126.
  - **Mac:** Standard Repair 1,107, Full Repair 1,115.
  - **Disks:** Standard Repair (check and repair the file system) 1,024; Full Repair (erase and reformat) 1,280 — every common file system on every kind of drive, with that file system's own repair commands.
  - **Contacts:** Fix everything 336, Rebuild 420 — every real problem kind in each of 14 kinds of source.
  - It also shows, honestly, which problems need steps or hardware instead. Tap a number to see the list. The Library has new Disks and Contacts tabs.
- **Disk health beyond DriveDx:** “Full report” reads every SMART/NVMe indicator, then shows health and lifetime-left gauges, years left at 8 h a day, projected endurance, data written per powered-on day, temperature against its limits, read/write statistics since start-up, errors and retries, and a finding for each problem with the repair that fixes it. Export the report as text, Markdown or a web page.
- **Repairs for bad sectors and worn disks:** remap bad sectors (chkdsk /r on Windows, a non-destructive badblocks pass on Linux), a write test that forces remapping (Linux, erases), zero-and-remap for Mac disks (erases), TRIM (trimforce, fstrim, ReTrim), long self-tests and turning SMART on. Heavy daily writing is flagged with what causes it.
- **Contact manager, Kontact style — every account separately, like Contacts on the Mac:** a side pane lists every source and nothing is ever merged:
  - **This Mac:** every account in the Mac's Contacts — any number of iCloud, Google, Outlook/Exchange and Yahoo accounts, plus On My Mac — read and edited through Apple's Contacts framework.
  - **iCloud and CardDAV accounts** signed in here (Fastmail, Yahoo, Nextcloud…).
  - **Every iPhone and iPad**, read from its backup with photos and groups.
  - **Every account on every Android phone**, each Google account and the SIM listed separately.
  - **Mend's own library:** address books kept as .vcf in ~/Mend/Contacts/Library, with the last 30 versions of each kept so any earlier version can be brought back.
  - **Open files:** .vcf, Google or Outlook .csv, and Thunderbird .ldif.
  - **Overview page:** totals, problems, birthdays this month, a search across every source (results stay labelled by source), "Load every source" and "Save every source to the library".
  - **Each source has tabs:** Contacts, Groups (the Mac's own groups or vCard categories), Birthdays & dates (with a calendar .ics), Fix everything, Duplicates, Numbers, and Copy & move (to any account, a library book, an Android phone or a file).
- **Every contact field:** prefix, middle and maiden names, phonetic names, department and role, any number of phones, emails, addresses (with a map link), websites, messaging (WhatsApp, Telegram, Skype…), social profiles, related people, birthday and other dates, groups and notes. Apple's labels are kept, so cards look the same on the iPhone.
- **Phone numbers in detail:** every number is checked with Google's numbering rules for every country. Mend shows:
  - the country and its flag;
  - the type of line: mobile, landline, toll-free, VoIP…;
  - whether the number can really exist;
  - its international, E.164 and local forms, each copyable;
  - Call and WhatsApp buttons, and a one-click fix to the international form.
- **Any number of devices at once:** every connected iPhone, iPad, Android and Mac — in normal, Recovery or DFU mode — gets its own tabs, and repairs run side by side. Changing tab or screen never stops a running job.
- **iPhone data (iMazing-style):** browse and export Messages, WhatsApp, call history, contacts, notes, Safari, calendar and voicemail from a backup (CSV or a printable page), copy out photos, voice memos and WhatsApp media, check a backup for spyware with MVT, and transfer one iPhone to another.
- **Repair another Mac:** revive or restore an Apple silicon Mac in DFU from this Mac with Apple Configurator, with key guides for every Mac; or share its disk and run First Aid, back it up or reinstall macOS onto it. iPhone repair also works through Apple Configurator when idevicerestore can't be installed.
- **No overlaps in small windows:** every screen and tab, including every Contacts view, was checked at 560, 760, 900, 1000 and 1240 px wide.
- **Hard-disk life left:** hard drives have no wear counter, so Mend now estimates their life. It weighs power-on hours against the usual service life of desktop, laptop or NAS drives, head load cycles and start-stops against their ratings, and any bad sectors, then shows which of these sets the figure. It appears as a gauge, a breakdown, years left at 8 hours a day or 24/7, and a line in the exported report.
- **Full report for all disks:** one button reads every disk. A Disk Health setting (on by default) shows the full report for every disk whenever the page opens. The full report now works on Windows too (with smartmontools). TRIM is offered only for SSDs.
- **How each repair fixes problems:** iPhone and Mac repair screens explain step by step what Standard and Full (Deep) Repair replace, what they keep and why that fixes problems. Every fix in the Fix Library is marked with what resolves it: Standard Repair, Full Repair, the steps, or hardware.
- **iPhone Apps tab fixed:** it uses the current ideviceinstaller (`list --xml`) and falls back to older versions. It lists your apps, Apple's apps or all, sorts by name or size, and shows the real error if the iPhone doesn't answer.
- **No more caps:** long lists (contacts, chats, backup files, Android apps, unreadable files) load more as you scroll instead of stopping at a few hundred. iPhone Safari and calendar history is read in full. Any number of iPhones, iPads and Macs can be connected and repaired at the same time.
- **Helpers are found where they really are:**
  - **Apple Configurator from the App Store is detected straight away.** Mend uses its tool from inside the app (or finds the app with Spotlight), so "Install Automation Tools" is no longer needed.
  - **No more "already installed" loop for libimobiledevice and ideviceinstaller.** Mend shows exactly which commands are missing and installs only those Homebrew packages; if Homebrew already has a package, it relinks it instead of reinstalling. ideviceinstaller (for the Apps tab) is now its own helper.
  - **Mend notices installs by itself.** After you press Install it checks every few seconds, and again when you switch back to it — no "Check again" needed.
- **idevicerestore installs reliably:** Mend writes its own build script, which clones libimobiledevice, idevicerestore and ideviceinstaller from GitHub (retrying), builds the newest versions into ~/Mend/limd without sudo, and installs only the Homebrew packages that are missing — no more is.gd link (blocked on some networks) or "already installed" warnings. With Apple Configurator installed, idevicerestore is optional and shown as covered.
- **iPhone backups fixed:**
  - Mend's newest tool build fixes backups that fail with old libimobiledevice on recent iOS.
  - **Back up with Apple Configurator** is a second route that works with every iOS version.
  - A failed backup is explained in plain words, with buttons that fix it: Trust again, build the newest tools, back up with Apple Configurator, choose another folder.
- **Owner Panel → Active devices:** who is using Mend right now, today, this week and this month, on a live radar, with versions, systems, countries and a device list. The data comes from an anonymous heartbeat every 30 minutes: a hashed machine id, version, system and plan, never an IP address.
- **New features:**
  - **Health over time:** disk health, life left and iPhone battery capacity are kept day by day and drawn as lines.
  - **Daily disk watch** (on by default): Mend re-checks every disk once a day while it's open and warns if health drops.
  - **Repair history** for every device.
  - **QR codes** for contacts.
  - **"Sell or give away" checklists** for iPhone and Mac.
- **Mend Pro is now ₹4,000 a month or ₹6,000 a year.**
- **More colour and sound:** every tab has its own colour, and names start in colour. A new animated Contacts overview shows your sources orbiting a contact card. Gauges and date badges are animated. New sounds: sync, library book, dial, a birthday tune, gauge sweep, a wrench when you press Install, and a chime when a helper is ready. Button icons, table columns, fact labels and helper rows have their own colours; new animated pictures — a spinning hard disk or flickering SSD on every disk, an iPhone streaming into a backup drive (broken link when it fails), a toolbox with turning gears while helpers install, an active-devices radar — and new sounds for platters, flash chips and backup streams; section subtitles colour their numbers and paths, and an animated toolbox shows while a helper installs.
- **Checkup (⇧⌘C):** one button checks disks, free space, memory, security, battery, sleep, firewall, Time Machine, updates, recent errors and every connected phone — read-only — and gives a score with a Fix button for anything that needs attention.
- **Fix Library tools:** tick off steps as you go, save fixes with a star, mark a problem “It's fixed!”, filter by Saved, One-click or Fixed, and copy the steps to send to someone.
- **Repair report:** Helpers & Log → Export report saves the checkup, devices, disks, fixed problems and recent repairs as a Markdown file.
- **macOS keeps Mend's permissions after updates:** Mac builds are now signed with one permanent identity, so “Mend would like to access files on a removable volume” and the other permission prompts are asked once — not after every update. The prompts also explain why Mend asks.
- **More colour, no pink:** brackets change colour with each nesting level, section titles and borders take their section's colour, headings and dialog titles are tinted, and keys, numbers and file paths stand out everywhere.
- **More graphics, motion and sound:** gauges that sweep to their value, a temperature bar, a cable pulse between two Macs when one is found in DFU, chat bubbles for messages, colour-coded problem cards in the contact fixer; a radar sweep for the Checkup, an animated Mac being reinstalled, platform icons orbiting the startup logo, a slow colour aurora behind every screen, a colour sweep when you change screens, and new sounds — a note per area, radar, tick-off, star, “fixed” fanfare and report.

## Mend 1.0.5 — 11 Oct 2026

- **Standard Repair and Full Repair for macOS:** the same two levels as iPhone. Standard Repair makes a restore point and reinstalls macOS over itself — files, apps and settings stay. Full Repair erases the Mac and installs a clean macOS (Erase All Content and Settings on Apple silicon). Pick the installer in the new “Standard & Full Repair” tab.
- **1,359 fixes, and 500+ for every repair:** the Fix Library now holds 665 iPhone & iPad and 694 Mac problems. Each repair screen shows exactly what it resolves — iPhone Standard Repair 560 and Deep Repair 568, Mac Standard Repair 642 and Full Repair 650 — and, honestly, which problems need steps (accessories, apps, accounts, carriers) or hardware instead. Tap a number to see the list.
- **Disk health beyond DriveDx:** “Full report” reads every SMART/NVMe indicator, then shows health and lifetime-left gauges, years left at 8 h a day, projected endurance, data written per powered-on day, temperature against its limits, read/write statistics since start-up, errors and retries, and a finding for each problem with the repair that fixes it. Export the report as text, Markdown or a web page.
- **Repairs for bad sectors and worn disks:** remap bad sectors (chkdsk /r on Windows, a non-destructive badblocks pass on Linux), a write test that forces remapping (Linux, erases), zero-and-remap for Mac disks (erases), TRIM (trimforce, fstrim, ReTrim), long self-tests and turning SMART on. Heavy daily writing is flagged with what causes it.
- **Contact manager, Kontact style — every account separately, like Contacts on the Mac:** a side pane lists every source and nothing is ever merged:
  - **This Mac:** every account in the Mac's Contacts — any number of iCloud, Google, Outlook/Exchange and Yahoo accounts, plus On My Mac — read and edited through Apple's Contacts framework.
  - **iCloud and CardDAV accounts** signed in here (Fastmail, Yahoo, Nextcloud…).
  - **Every iPhone and iPad**, read from its backup with photos and groups.
  - **Every account on every Android phone**, each Google account and the SIM listed separately.
  - **Mend's own library:** address books kept as .vcf in ~/Mend/Contacts/Library, with the last 30 versions of each kept so any earlier version can be brought back.
  - **Open files:** .vcf, Google or Outlook .csv, and Thunderbird .ldif.
  - **Overview page:** totals, problems, birthdays this month, a search across every source (results stay labelled by source), "Load every source" and "Save every source to the library".
  - **Each source has tabs:** Contacts, Groups (the Mac's own groups or vCard categories), Birthdays & dates (with a calendar .ics), Fix everything, Duplicates, Numbers, and Copy & move (to any account, a library book, an Android phone or a file).
- **Every contact field:** prefix, middle and maiden names, phonetic names, department and role, any number of phones, emails, addresses (with a map link), websites, messaging (WhatsApp, Telegram, Skype…), social profiles, related people, birthday and other dates, groups and notes. Apple's labels are kept, so cards look the same on the iPhone.
- **Phone numbers in detail:** every number is checked with Google's numbering rules for every country. Mend shows:
  - the country and its flag;
  - the type of line: mobile, landline, toll-free, VoIP…;
  - whether the number can really exist;
  - its international, E.164 and local forms, each copyable;
  - Call and WhatsApp buttons, and a one-click fix to the international form.
- **Any number of devices at once:** every connected iPhone, iPad, Android and Mac — in normal, Recovery or DFU mode — gets its own tabs, and repairs run side by side. Changing tab or screen never stops a running job.
- **iPhone data (iMazing-style):** browse and export Messages, WhatsApp, call history, contacts, notes, Safari, calendar and voicemail from a backup (CSV or a printable page), copy out photos, voice memos and WhatsApp media, check a backup for spyware with MVT, and transfer one iPhone to another.
- **Repair another Mac:** revive or restore an Apple silicon Mac in DFU from this Mac with Apple Configurator, with key guides for every Mac; or share its disk and run First Aid, back it up or reinstall macOS onto it. iPhone repair also works through Apple Configurator when idevicerestore can't be installed.
- **No overlaps in small windows:** every screen and tab, including every Contacts view, was checked at 560, 760, 900, 1000 and 1240 px wide.
- **Hard-disk life left:** hard drives have no wear counter, so Mend now estimates their life. It weighs power-on hours against the usual service life of desktop, laptop or NAS drives, head load cycles and start-stops against their ratings, and any bad sectors, then shows which of these sets the figure. It appears as a gauge, a breakdown, years left at 8 hours a day or 24/7, and a line in the exported report.
- **Full report for all disks:** one button reads every disk. A Disk Health setting (on by default) shows the full report for every disk whenever the page opens. The full report now works on Windows too (with smartmontools). TRIM is offered only for SSDs.
- **How each repair fixes problems:** iPhone and Mac repair screens explain step by step what Standard and Full (Deep) Repair replace, what they keep and why that fixes problems. Every fix in the Fix Library is marked with what resolves it: Standard Repair, Full Repair, the steps, or hardware.
- **iPhone Apps tab fixed:** it uses the current ideviceinstaller (`list --xml`) and falls back to older versions. It lists your apps, Apple's apps or all, sorts by name or size, and shows the real error if the iPhone doesn't answer.
- **No more caps:** long lists (contacts, chats, backup files, Android apps, unreadable files) load more as you scroll instead of stopping at a few hundred. iPhone Safari and calendar history is read in full. Any number of iPhones, iPads and Macs can be connected and repaired at the same time.
- **Helpers are found where they really are:**
  - **Apple Configurator from the App Store is detected straight away.** Mend uses its tool from inside the app (or finds the app with Spotlight), so "Install Automation Tools" is no longer needed.
  - **No more "already installed" loop for libimobiledevice and ideviceinstaller.** Mend shows exactly which commands are missing and installs only those Homebrew packages; if Homebrew already has a package, it relinks it instead of reinstalling. ideviceinstaller (for the Apps tab) is now its own helper.
  - **Mend notices installs by itself.** After you press Install it checks every few seconds, and again when you switch back to it — no "Check again" needed.
- **Mend Pro is now ₹4,000 a month or ₹6,000 a year.**
- **More colour and sound:** every tab has its own colour, and names start in colour. A new animated Contacts overview shows your sources orbiting a contact card. Gauges and date badges are animated. New sounds: sync, library book, dial, a birthday tune, gauge sweep, a wrench when you press Install, and a chime when a helper is ready. Button icons, table columns and helper rows have their own colours, section subtitles colour their numbers and paths, and an animated toolbox shows while a helper installs.
- **Checkup (⇧⌘C):** one button checks disks, free space, memory, security, battery, sleep, firewall, Time Machine, updates, recent errors and every connected phone — read-only — and gives a score with a Fix button for anything that needs attention.
- **Fix Library tools:** tick off steps as you go, save fixes with a star, mark a problem “It's fixed!”, filter by Saved, One-click or Fixed, and copy the steps to send to someone.
- **Repair report:** Helpers & Log → Export report saves the checkup, devices, disks, fixed problems and recent repairs as a Markdown file.
- **macOS keeps Mend's permissions after updates:** Mac builds are now signed with one permanent identity, so “Mend would like to access files on a removable volume” and the other permission prompts are asked once — not after every update. The prompts also explain why Mend asks.
- **More colour, no pink:** brackets change colour with each nesting level, section titles and borders take their section's colour, headings and dialog titles are tinted, and keys, numbers and file paths stand out everywhere.
- **More graphics, motion and sound:** gauges that sweep to their value, a temperature bar, a cable pulse between two Macs when one is found in DFU, chat bubbles for messages, colour-coded problem cards in the contact fixer; a radar sweep for the Checkup, an animated Mac being reinstalled, platform icons orbiting the startup logo, a slow colour aurora behind every screen, a colour sweep when you change screens, and new sounds — a note per area, radar, tick-off, star, “fixed” fanfare and report.

## Mend 1.0.4 — 11 Oct 2026

- **Standard Repair and Full Repair for macOS:** the same two levels as iPhone. Standard Repair makes a restore point and reinstalls macOS over itself — files, apps and settings stay. Full Repair erases the Mac and installs a clean macOS (Erase All Content and Settings on Apple silicon). Pick the installer in the new “Standard & Full Repair” tab.
- **1,359 fixes, and 500+ for every repair:** the Fix Library now holds 665 iPhone & iPad and 694 Mac problems. Each repair screen shows exactly what it resolves — iPhone Standard Repair 560 and Deep Repair 568, Mac Standard Repair 642 and Full Repair 650 — and, honestly, which problems need steps (accessories, apps, accounts, carriers) or hardware instead. Tap a number to see the list.
- **Disk health beyond DriveDx:** “Full report” reads every SMART/NVMe indicator, then shows health and lifetime-left gauges, years left at 8 h a day, projected endurance, data written per powered-on day, temperature against its limits, read/write statistics since start-up, errors and retries, and a finding for each problem with the repair that fixes it. Export the report as text, Markdown or a web page.
- **Repairs for bad sectors and worn disks:** remap bad sectors (chkdsk /r on Windows, a non-destructive badblocks pass on Linux), a write test that forces remapping (Linux, erases), zero-and-remap for Mac disks (erases), TRIM (trimforce, fstrim, ReTrim), long self-tests and turning SMART on. Heavy daily writing is flagged with what causes it.
- **Contact manager, Kontact style — every account separately, like Contacts on the Mac:** a side pane lists every source and nothing is ever merged:
  - **This Mac:** every account in the Mac's Contacts — any number of iCloud, Google, Outlook/Exchange and Yahoo accounts, plus On My Mac — read and edited through Apple's Contacts framework.
  - **iCloud and CardDAV accounts** signed in here (Fastmail, Yahoo, Nextcloud…).
  - **Every iPhone and iPad**, read from its backup with photos and groups.
  - **Every account on every Android phone**, each Google account and the SIM listed separately.
  - **Mend's own library:** address books kept as .vcf in ~/Mend/Contacts/Library, with the last 30 versions of each kept so any earlier version can be brought back.
  - **Open files:** .vcf, Google or Outlook .csv, and Thunderbird .ldif.
  - **Overview page:** totals, problems, birthdays this month, a search across every source (results stay labelled by source), "Load every source" and "Save every source to the library".
  - **Each source has tabs:** Contacts, Groups (the Mac's own groups or vCard categories), Birthdays & dates (with a calendar .ics), Fix everything, Duplicates, Numbers, and Copy & move (to any account, a library book, an Android phone or a file).
- **Every contact field:** prefix, middle and maiden names, phonetic names, department and role, any number of phones, emails, addresses (with a map link), websites, messaging (WhatsApp, Telegram, Skype…), social profiles, related people, birthday and other dates, groups and notes. Apple's labels are kept, so cards look the same on the iPhone.
- **Phone numbers in detail:** every number is checked with Google's numbering rules for every country. Mend shows:
  - the country and its flag;
  - the type of line: mobile, landline, toll-free, VoIP…;
  - whether the number can really exist;
  - its international, E.164 and local forms, each copyable;
  - Call and WhatsApp buttons, and a one-click fix to the international form.
- **Any number of devices at once:** every connected iPhone, iPad, Android and Mac — in normal, Recovery or DFU mode — gets its own tabs, and repairs run side by side. Changing tab or screen never stops a running job.
- **iPhone data (iMazing-style):** browse and export Messages, WhatsApp, call history, contacts, notes, Safari, calendar and voicemail from a backup (CSV or a printable page), copy out photos, voice memos and WhatsApp media, check a backup for spyware with MVT, and transfer one iPhone to another.
- **Repair another Mac:** revive or restore an Apple silicon Mac in DFU from this Mac with Apple Configurator, with key guides for every Mac; or share its disk and run First Aid, back it up or reinstall macOS onto it. iPhone repair also works through Apple Configurator when idevicerestore can't be installed.
- **No overlaps in small windows:** every screen and tab, including every Contacts view, was checked at 560, 760, 900, 1000 and 1240 px wide.
- **Hard-disk life left:** hard drives have no wear counter, so Mend now estimates their life. It weighs power-on hours against the usual service life of desktop, laptop or NAS drives, head load cycles and start-stops against their ratings, and any bad sectors, then shows which of these sets the figure. It appears as a gauge, a breakdown, years left at 8 hours a day or 24/7, and a line in the exported report.
- **Full report for all disks:** one button reads every disk. A Disk Health setting (on by default) shows the full report for every disk whenever the page opens. The full report now works on Windows too (with smartmontools). TRIM is offered only for SSDs.
- **How each repair fixes problems:** iPhone and Mac repair screens explain step by step what Standard and Full (Deep) Repair replace, what they keep and why that fixes problems. Every fix in the Fix Library is marked with what resolves it: Standard Repair, Full Repair, the steps, or hardware.
- **iPhone Apps tab fixed:** it uses the current ideviceinstaller (`list --xml`) and falls back to older versions. It lists your apps, Apple's apps or all, sorts by name or size, and shows the real error if the iPhone doesn't answer.
- **No more caps:** long lists (contacts, chats, backup files, Android apps, unreadable files) load more as you scroll instead of stopping at a few hundred. iPhone Safari and calendar history is read in full. Any number of iPhones, iPads and Macs can be connected and repaired at the same time.
- **Mend Pro is now ₹4,000 a month or ₹6,000 a year.**
- **More colour and sound:** every tab has its own colour, and names start in colour. A new animated Contacts overview shows your sources orbiting a contact card. Gauges and date badges are animated. New sounds: sync, library book, dial, a birthday tune, and gauge sweep.
- **Checkup (⇧⌘C):** one button checks disks, free space, memory, security, battery, sleep, firewall, Time Machine, updates, recent errors and every connected phone — read-only — and gives a score with a Fix button for anything that needs attention.
- **Fix Library tools:** tick off steps as you go, save fixes with a star, mark a problem “It's fixed!”, filter by Saved, One-click or Fixed, and copy the steps to send to someone.
- **Repair report:** Helpers & Log → Export report saves the checkup, devices, disks, fixed problems and recent repairs as a Markdown file.
- **macOS keeps Mend's permissions after updates:** Mac builds are now signed with one permanent identity, so “Mend would like to access files on a removable volume” and the other permission prompts are asked once — not after every update. The prompts also explain why Mend asks.
- **More colour, no pink:** brackets change colour with each nesting level, section titles and borders take their section's colour, headings and dialog titles are tinted, and keys, numbers and file paths stand out everywhere.
- **More graphics, motion and sound:** gauges that sweep to their value, a temperature bar, a cable pulse between two Macs when one is found in DFU, chat bubbles for messages, colour-coded problem cards in the contact fixer; a radar sweep for the Checkup, an animated Mac being reinstalled, platform icons orbiting the startup logo, a slow colour aurora behind every screen, a colour sweep when you change screens, and new sounds — a note per area, radar, tick-off, star, “fixed” fanfare and report.

## Mend 1.0.3 — 11 Oct 2026

- **Standard Repair and Full Repair for macOS:** the same two levels as iPhone. Standard Repair makes a restore point and reinstalls macOS over itself — files, apps and settings stay. Full Repair erases the Mac and installs a clean macOS (Erase All Content and Settings on Apple silicon). Pick the installer in the new “Standard & Full Repair” tab.
- **1,359 fixes, and 500+ for every repair:** the Fix Library now holds 665 iPhone & iPad and 694 Mac problems. Each repair screen shows exactly what it resolves — iPhone Standard Repair 560 and Deep Repair 568, Mac Standard Repair 642 and Full Repair 650 — and, honestly, which problems need steps (accessories, apps, accounts, carriers) or hardware instead. Tap a number to see the list.
- **Disk health beyond DriveDx:** “Full report” reads every SMART/NVMe indicator, then shows health and lifetime-left gauges, years left at 8 h a day, projected endurance, data written per powered-on day, temperature against its limits, read/write statistics since start-up, errors and retries, and a finding for each problem with the repair that fixes it. Export the report as text, Markdown or a web page.
- **Repairs for bad sectors and worn disks:** remap bad sectors (chkdsk /r on Windows, a non-destructive badblocks pass on Linux), a write test that forces remapping (Linux, erases), zero-and-remap for Mac disks (erases), TRIM (trimforce, fstrim, ReTrim), long self-tests and turning SMART on. Heavy daily writing is flagged with what causes it.
- **Contact manager:** several iCloud and CardDAV accounts side by side, plus .vcf and .csv files (Google, Outlook, Android exports). Fix everything finds 16 kinds of problem — impossible numbers, missing country codes, misspelt email domains, NAMES IN CAPITALS, invisible characters, empty contacts, huge photos and more — and fixes them in one go. Broken .vcf files are repaired as they open (missing END, quoted-printable text, old base64 photos, duplicate IDs). Copy or move contacts between accounts.
- **Any number of devices at once:** every connected iPhone, iPad, Android and Mac — in normal, Recovery or DFU mode — gets its own tabs, and repairs run side by side. Changing tab or screen never stops a running job.
- **iPhone data (iMazing-style):** browse and export Messages, WhatsApp, call history, contacts, notes, Safari, calendar and voicemail from a backup (CSV or a printable page), copy out photos, voice memos and WhatsApp media, check a backup for spyware with MVT, and transfer one iPhone to another.
- **Repair another Mac:** revive or restore an Apple silicon Mac in DFU from this Mac with Apple Configurator, with key guides for every Mac; or share its disk and run First Aid, back it up or reinstall macOS onto it. iPhone repair also works through Apple Configurator when idevicerestore can't be installed.
- **No overlaps in small windows:** every screen and tab was checked at 560, 760 and 1000 px wide.
- **Checkup (⇧⌘C):** one button checks disks, free space, memory, security, battery, sleep, firewall, Time Machine, updates, recent errors and every connected phone — read-only — and gives a score with a Fix button for anything that needs attention.
- **Fix Library tools:** tick off steps as you go, save fixes with a star, mark a problem “It's fixed!”, filter by Saved, One-click or Fixed, and copy the steps to send to someone.
- **Repair report:** Helpers & Log → Export report saves the checkup, devices, disks, fixed problems and recent repairs as a Markdown file.
- **macOS keeps Mend's permissions after updates:** Mac builds are now signed with one permanent identity, so “Mend would like to access files on a removable volume” and the other permission prompts are asked once — not after every update. The prompts also explain why Mend asks.
- **More colour, no pink:** brackets change colour with each nesting level, section titles and borders take their section's colour, headings and dialog titles are tinted, and keys, numbers and file paths stand out everywhere.
- **More graphics, motion and sound:** gauges that sweep to their value, a temperature bar, a cable pulse between two Macs when one is found in DFU, chat bubbles for messages, colour-coded problem cards in the contact fixer; a radar sweep for the Checkup, an animated Mac being reinstalled, platform icons orbiting the startup logo, a slow colour aurora behind every screen, a colour sweep when you change screens, and new sounds — a note per area, radar, tick-off, star, “fixed” fanfare and report.

## Mend 1.0.2 — 09 Oct 2026

- **Standard Repair and Full Repair for macOS:** the same two levels as iPhone. Standard Repair makes a restore point and reinstalls macOS over itself — files, apps and settings stay. Full Repair erases the Mac and installs a clean macOS (Erase All Content and Settings on Apple silicon). Pick the installer in the new “Standard & Full Repair” tab.
- **Over 1,000 fixes:** the Fix Library now holds 513 iPhone & iPad and 511 Mac problems, with new areas — built-in apps, notifications & Focus, typing, accessibility, CarPlay, HomePod & AirTag, family & Screen Time, Wallet & payments, privacy, Apple Watch, AirPods, Terminal & developer tools and more.
- **Checkup (⇧⌘C):** one button checks disks, free space, memory, security, battery, sleep, firewall, Time Machine, updates, recent errors and every connected phone — read-only — and gives a score with a Fix button for anything that needs attention.
- **Fix Library tools:** tick off steps as you go, save fixes with a star, mark a problem “It's fixed!”, filter by Saved, One-click or Fixed, and copy the steps to send to someone.
- **Repair report:** Helpers & Log → Export report saves the checkup, devices, disks, fixed problems and recent repairs as a Markdown file.
- **macOS keeps Mend's permissions after updates:** Mac builds are now signed with one permanent identity, so “Mend would like to access files on a removable volume” and the other permission prompts are asked once — not after every update. The prompts also explain why Mend asks.
- **More colour, no pink:** brackets change colour with each nesting level, section titles and borders take their section's colour, headings and dialog titles are tinted, and keys, numbers and file paths stand out everywhere.
- **More graphics, motion and sound:** a radar sweep for the Checkup, an animated Mac being reinstalled, platform icons orbiting the startup logo, a slow colour aurora behind every screen, a colour sweep when you change screens, and new sounds — a note per area, radar, tick-off, star, “fixed” fanfare and report.

## Mend 1.0.1 — 09 Oct 2026

- **Fix Library (⌘L):** 433 known problems — 222 for iPhone & iPad and 211 for Mac — in plain words, with numbered steps and the one-click repair that fixes each one. Search in your own words, filter by colour-coded category; fixes also show up in ⌘K and Mend AI uses them when it diagnoses.
- **23 new Mac quick fixes:** restart a stuck sound, Bluetooth, iCloud Drive sync, menu bar or Notification Center; reset Quick Look, the Dock and the print queue; reload the settings service; fix the clock; and see what's going on — busiest processes, memory pressure, free space, sleep blockers, power and battery health, background items, system extensions, profiles, network, recent faults, Time Machine and the firewall.
- **Fits any window size:** every screen now follows the width it really has. The sidebar folds into an icon rail, the overview's rings move under the title, cards stack and text wraps — nothing overlaps when the window is small or the AI panel is open.
- **More colour, no pink:** menus and paths are blue with violet ›, keys and buttons gold, numbers and sizes cyan, brackets violet, quoted names and “keeps your data” green, “erases” red, file names teal, and every command and log line is coloured part by part. Tabs, sections and details each have their own colour.
- **More graphics and motion:** a live heartbeat line under the overview and in the startup show, drifting coloured stitches, a repair picture that stitches itself shut as the percentage climbs (check on success, shake on failure), animated empty-state scenes, toasts with a countdown line.
- **More sounds:** 16 new synthesised effects (page turn, category select, search found, steps, rescue, magic, lock and unlock, fanfare, stitch, heartbeat and more) and four new sound packs — Bells, Pluck, Arcade and Deep.

## Mend 1.0.0 — 08 Oct 2026

**Mend — an AI repair kit for iPhone, Android, Mac, Windows, Linux and every disk.**

- **iPhone & iPad:** enter and leave Recovery Mode in one click (free); Standard repair (reinstall iOS, keep data) and Deep repair (clean iOS) from firmware Apple still signs, downloaded from Apple with a resumable download and a SHA-256 check; DFU steps for every model; device info, battery health and cycles, storage; full local backups, encryption and restore; apps (list, remove, install .ipa); screenshots, live console and crash logs.
- **Android:** reboot to Recovery, Bootloader, Fastboot or Sideload in one click; exit Fastboot; clear every app cache; repair with the official OTA package or the factory image (keep data or wipe); flash single partitions; apps (uninstall, disable, clear data, install .apk); copy photos and files; screenshots and logcat.
- **Mac repair:** First Aid check and repair for every volume, home-folder permissions, Spotlight, “Open With”, font caches, DNS, Dock & Finder, security status, macOS updates, full installers and bootable USB installers, local snapshots, Recovery and Safe Mode restarts, NVRAM.
- **Windows repair:** SFC, DISM scan/repair/cleanup, CHKDSK, Startup Repair, BCD backup and rebuild, network and Windows Update resets, restore points, registry backup, Store and icon fixes, problem drivers, startup programs, MBR→GPT.
- **Linux repair:** broken packages (apt, dnf, pacman), GRUB, initramfs, failed services, errors since boot, desktop reset, DNS, fsck.
- **Corrupted settings fixer:** finds damaged .plist and JSON settings that make apps crash or forget everything, and moves them to ~/Mend/Quarantined Settings — never deletes.
- **Partition manager:** a colour map of every disk; mount, rename, check, repair, format, create, delete, resize, erase, wipe, convert MBR→GPT and clone. The system disk is always protected.
- **Deep disk health:** SMART health score, temperature, life used, data written, remapped and unstable sectors, self-tests, a speed test and a read scan that lists files on unreadable areas.
- **Tiny backups:** content-defined de-duplication and zstd — repeat backups cost almost nothing; verify, browse and restore single files.
- **iCloud contacts:** every field and photo straight on iCloud (or any CardDAV server), duplicates merged, impossible numbers found and fixed, .vcf/.csv import and export.
- **Mend AI for everyone:** describe the problem and get the safest repair first with Run buttons; explanations for every result and repair word; free built-in AI, GitHub Copilot CLI, GitHub Models, every local model and any online AI.
- **Safe by design:** the page can only name repairs from Mend's own list; risky ones show the exact steps first and erases ask you to type the disk or device name.
- **Pro:** ₹20 a month or ₹220 a year through Razorpay, or an activation code; Owner Panel for codes, subscriptions and crash reports.
- **Look and sound:** a heartbeat startup show with sound, plug-in chimes, healing sounds, six sound packs, light and dark themes, no pink anywhere.

### Install

- **macOS** (Apple silicon and Intel): `curl -fsSL https://ipconfig.co.network/updates/mend/install.sh | bash`
- **Windows** (PowerShell): `irm https://ipconfig.co.network/updates/mend/install.ps1 | iex`
- **Linux** (AppImage): `curl -fsSL https://ipconfig.co.network/updates/mend/install.sh | bash` — add `-s -- --deb` for the .deb

First launch on macOS after a manual DMG install: `xattr -cr /Applications/Mend.app` (Mend is ad-hoc signed, not notarized).
