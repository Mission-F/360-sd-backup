<p align="center">
  <img src="assets/icona.png" width="132" alt="">
</p>

<h1 align="center">360 SD Backup</h1>

<p align="center">
  <b>That tiny card holds months of your work.<br>Protect it before it reminds you why you should have.</b>
</p>

<p align="center">
  <a href="https://github.com/Mission-F/360-sd-backup/releases/latest/download/360-SD-Backup.dmg"><b>Download free for Mac</b></a>
  &nbsp;·&nbsp; macOS 12 or later &nbsp;·&nbsp; under 1 MB
</p>

<p align="center">
  <img src="assets/ready.png" width="440" alt="The main screen: card found, one big Create backup button">
</p>

---

You already know how this ends.

Your Raspberry Pi runs for months without a single complaint. It sits in a corner and does its job. Then one day the power flickers, the micro SD gives up, and it never boots again.

And with that card go the system, the settings you fixed at two in the morning, and that one command you found after hours of trying and never wrote down.

**360 SD Backup was built for that day.** We made it because we needed it ourselves: a simple way to know that whatever happens to that card, the work on it is not lost.

Insert the card. Press one button. Done.

## A backup you can't restore is not a backup

Copying a card is easy. Knowing the copy works is another story. That is why this program doesn't trust itself:

1. It **copies** the entire card, sector by sector.
2. It **reopens the file** it just created and checks it from scratch.
3. It **reads the card a second time** and compares the fingerprints.

The file only gets its final name if everything matches. If something is off, it tells you. No half-finished backups, no surprises on the day you need one.

Restoring is just as careful: it checks the **entire** file before touching the card, then reads back everything it wrote.

<p align="center">
  <img src="assets/progress.png" width="400" alt="Two progress rings: overall progress and the current step">
  <img src="assets/done.png" width="400" alt="Backup ready and verified">
</p>

## What you can do

- **Create a full backup** in a single `.zip` file, compressed and ready to archive.
- **Restore it** to another card and bring back an identical Raspberry Pi.
- **Format a card** and make it normal again, with all its space available, including cards your Mac can no longer use after living in a Raspberry Pi.
- **Let it work in the background**, with progress always visible in the menu bar.

The program only shows removable cards and disks, so your Mac's own disk never appears. Before erasing a card, it asks you first.

## Free. Really.

No account. No subscription. No ads. No data leaving your Mac.

The interface follows your Mac: Italian if your system is in Italian, English otherwise.

## Installation

1. [Download the DMG](https://github.com/Mission-F/360-sd-backup/releases/latest/download/360-SD-Backup.dmg) and open it.
2. Drag **360 SD Backup** onto the **Applications** folder.
3. The first time you open it, macOS will block it, because the program doesn't have Apple's paid signature. Go to **System Settings > Privacy & Security** and click **Open Anyway**. You only need to do this once.

To read and write the card, macOS will ask for an administrator password. The program never sees or stores it: macOS handles it.

## Before you start

- Shut down the Raspberry Pi cleanly with `sudo shutdown -h now`, then remove the card.
- If your Mac says the disk is not readable, choose **Ignore**.
- To restore, you need a card at least as large as the original.
- A backup is a complete copy, including passwords and keys. Treat it with the same care as the card.
- Do not run the original Raspberry Pi and its clone on the same network at the same time.

## Where things stand

This is an early version and we would rather tell you exactly how things are. Backup has been tried on a real card. Restore and format have passed our tests on virtual cards, including damaged files and simulated faulty cards, but not yet a full round trip on a real Raspberry Pi. The Apple Silicon build is included, but it has only been run on Intel.

If your data matters, try it on a spare card before you need it. That is the best advice for any backup.

## License

This program is **free but not open source**: you can download it and use it freely, including for work, under the terms in the [LICENSE](LICENSE) file. It is provided as is, without warranty.

© 2026 360 Management System. All rights reserved. For any request: supporto@360msystem.it

Apple, Mac and macOS are trademarks of Apple Inc. Raspberry Pi is a trademark of Raspberry Pi Ltd. This project is not affiliated with or endorsed by these companies.
