# Unlocking the Bootloader via WPInternals

## Requirements

- WPInternals - [download here](https://wpinternals.net/index.php/downloads)
- Windows Device Recovery Tools - [download here](https://support.microsoft.com/en-us/help/12379/windows-10-mobile-device-recovery-tool-faq)
- A good internet connection - you will download about 3 GB of data

## Guide

- Install Windows Device Recovery Tool (it installs drivers we need).
- Disable BitLocker on the device.
- Remove μSD card from your device.
- Turn on your phone, unlock it and plug it to PC.
- Start WPInternals, read `Getting started` section and then navigate to `Download` section (the left menu).
- Fill the `Producttype` and `Productcode` fields (if they are not filled automatically), click `search` and then `Download all`.
- Check the version of your Windows 10 Mobile, if it's bigger than `10.0.15254.547`, you can't unlock your phone, you have 2 options: either you wait for a new release of WPInternals, or you can flash back old version of Windows 10 Mobile.
- Select `Unlock bootloader` from the left menu, click OK to switch phone into `Flash-mode`.
- Check if original FFU and emergency programmer are selected (they should be already) and click `Unlock`.
- Wait for WPInternals to do their job, WPInternals may need an assistance, so pay attention what WPInternals tell you.
- Boot phone into normal mode.
- You have successfully unlocked the bootloader on your Lumia!
