## BOCARAM 8‑Bit Disk Image Set

This directory contains a curated collection of disk images, IMD captures, and reference materials for the BOCA Research *BOCARAM 8‑Bit* expansion boards. These files support archival work, emulator reconstruction, and hardware restoration. [`./Files`](./Files) contains the contents of the disks (identical across all media) in extracted form.

This card may have an earlier revision called **BOCARAM‑XT**. I do not know whether it is the same card or a newer revision. The card photos posted around the retro‑computing web seem to suggest the former. I would assume the driver files work with both cards.

The box reverse has a sticker placed over text that clearly says **BOCARAM‑XT** beneath the “BOCARAM 8‑Bit” label. The drivers appear to conform to EMS for DOS 4.0, and I do not know whether the XT version of the board lacks support for EMS on later versions of DOS.

Documentation suggests that the board supports up to **2 MB** of memory on an XT‑class machine — twice the RAM the 8088 can address directly, and far more than DOS can access without banking in 16‑bit real mode (640 KB). It also claims the card works in a 286‑class machine, despite being an 8‑bit card. Examining the latch and selection logic, it uses F‑series logic, suggesting the designers accounted for the higher bus timing of AT‑class machines. The addressing and data path are still multiplexed on a 16‑bit machine, but the card itself is strictly 8‑bit.

### Disk Images (IMD Format)

IMD is David Dunfield’s disk‑image format for preservation. Filenames use 8.3 format to facilitate working with 16‑bit DOS when creating exact copies of the media.

- **35BOCA.IMD** — 3.5" 720 KB media
- **35HDBOCA.IMD** — 3.5" 1.44 MB media
- **525BOCA.IMD** — 5.25" 360 KB media

### Raw Disk Images (IMG Format)

Converted to raw binary block images for modern emulation and file extraction.

- **BOCARAM_8‑Bit‑1.44MB‑DISK.img** — 1.44 MB DOS‑formatted disk image containing the full BOCA RAM utility suite
- **BOCARAM_8‑Bit‑360K‑DISK.img** — 360 KB image suitable for XT‑class systems and early drives
- **BOCARAM_8‑Bit‑720K‑DISK.img** — 720 KB double‑density image for systems with 3.5" DD drives

### Reference Artwork

- **BOCARAM_8BIT‑BOCA_Research_Inc‑Front.jpg** — High‑resolution PCB top photo
- **BOCARAM_8BIT‑BOCA_Research_Inc‑Back.jpg** — High‑resolution PCB bottom photo

### Documentation

 Official manual covering the BR8B00, BR803, BR810, and BR820 boards, including installation, memory mapping, configuration jumpers, and diagnostic utilities.

- **BOCARAM_8‑Bit_Manual‑BOCA_Research_Inc_BR8B00_BR8B03_BR8B10_BR8B20.pdf**



### `./Files` Contents

- **BRDISK.COM / .SYS** — RAM‑disk utility
- **BREMM.COM / .SYS** — Bespoke Expanded Memory Manager
- **BRINST.COM** — Installation utility for automating driver setup
- **BRSPOOL.COM** — Printer spooler for parallel‑port block‑device printers
- **BRTEST.COM** — Diagnostic test utility for the card
- **EMMSTAT.EXE** — Undocumented in the manual; likely a utility for displaying memory usage
