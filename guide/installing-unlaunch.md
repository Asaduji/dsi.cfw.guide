---
title: Installing Unlaunch
layout: single
sidebar:
  nav: "side"
---

Unlaunch is currently in a beta state. Please exercise **extreme caution.**
{: .notice--info}

Do not visit Data Management, the DSi Shop, or the 3DS Transfer Tool after installing Unlaunch. This will prevent your system from booting until restoring a NAND backup at best, or **brick it entirely** at worst. This notice will be updated once Unlaunch is safer.
{: .notice--danger}

Do note that visiting the aforementioned applications is perfectly safe in HiyaCFW, once installed.
{: .notice--info}

Make sure you have a NAND backup before proceeding!
{: .notice--danger}

## What you need
- The latest release of [Unlaunch](http://problemkaputt.de/unlaunch.zip)
- The latest release of [HBMenu](https://github.com/devkitPro/nds-hb-menu/releases/)

## Instructions

1. Insert your system's SD card into your computer
2. Copy `BOOT.NDS` from the `hbmenu` folder in the HBMenu `.tar.bz2` file to the root of your SD card
  - Likely, twlnf is currently your `boot.nds`; for now, rename it to `boot.bak` or `twlnf.nds`
3. Copy `UNLAUNCH.DSI` from the Unlaunch `.zip` file to the root of your SD card
4. Rename `UNLAUNCH.DSI` to `unlaunch.nds`
5. Unplug your SD card, and insert it in your DSi
6. Power on your DSi, and run your previously-installed entrypoint
  - HBMenu should appear
7. Navigate to `unlaunch.nds`, and press **A**
  - Unlaunch's installer should appear
8. Navigate to `INSTALL NOW` and press **A**
  - If Unlaunch freezes at `LOADING FAT`, there is currently **no safe way** to install Unlaunch on your system
    - We are currently investigating this issue on the Discord; if you have this problem, stating if you've used twlnf in the past will help greatly
  - Running a system update can supposedly fix the problem, but we have not confirmed this
  - Updating your system will not erase any homebrew entrypoints
9. When done, navigate to `POWER DOWN` and press **A**
  - Your system will power off
10. Turn your system on, to verify Unlaunch installed properly
  - You should briefly see the Unlaunch screen, and boot into a version of the DSi Menu with no sound

With Unlaunch installed, your system now has primitive brick protection, unless the launcher's TMD file is destroyed. Unlaunch has protections that should prevent this from happening, and HiyaCFW uses your SD card as the DSi's NAND, making your system theoretically unbrickable.

[Installing HiyaCFW](/guide/installing-hiyacfw){: .btn .btn--light-outline}
{: style="text-align: center;"}