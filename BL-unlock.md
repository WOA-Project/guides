# Unlocking the Bootloader via WPInternals

## Requirements

- WPInternals - [download here](https://wpinternals.net/index.php/downloads)
- Windows Device Recovery Tools - [download here](https://support.microsoft.com/en-us/help/12379/windows-10-mobile-device-recovery-tool-faq)
- A good internet connection - you will download about 3 GB of data

## Guide

- Install Windows Device Recovery Tool (it installs drivers we need).
- Remove μSD card from your device.
- Turn on your phone, unlock it, disable the BitLocker protection in settings and plug it to PC.
- Start WPInternals, read `Getting started` section and then navigate to `Download` section (the left menu).
- Fill the `Producttype` and `Productcode` fields (if they are not filled automatically), click `search` and then `Download all`.
- Select `Unlock bootloader` from the left menu, click OK to switch phone into `Flash-mode`.
- Check if original FFU and emergency programmer are selected (they should be already) and click `Unlock`.
- Wait for WPInternals to do their job, WPInternals may need an assistance, so pay attention what WPInternals tell you.
- Boot phone into normal mode.
- You have successfully unlocked the bootloader on your Lumia!
