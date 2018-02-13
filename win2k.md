# WinXP/2k installation

This document is based on e-mails and messages from Trypt0. It is recommended that you try running kxsetup before any manual installations, because the recent kxsetup versions should work without any problems.

To install this driver manually under Windows XP or Windows 2000, first download both the latest kX Audio Driver and the debug MFC libraries.

Don't forget to uninstall LiveWare and/or APS drivers. You may keep PlayCenter or other Creative software.

Next, unRAR the driver onto any temporary directory and unRAR the MFC libraries to your \windows\system32 (\winnt\system32) directory.

After extracting, go to Safe Mode by rebooting the computer and quickly pressing F8 as soon as it passes the POST test.

You should now be in Windows XP Safe Mode.

Now press Windows button and the Pause key at the same time; click the Hardware tab; click Device Manager; double-click "Sound, Video and Game Controllers"; double-click the device soundcard; click on the Driver tab; click on the "Update Driver" button; click Install from a List or Specific Location, click "don't search, I will choose"; click on the Have Disk button and find your drivers on the desktop (or temporary directory); find the appropriate driver for your model.

After installing reboot. Use the kX Mixer tray utility to set up your sound card. (Settings->Reset Settings).

You may also try deleting or re-naming \winnt\Driver Cache\i386\driver.cab file as well as \winnt\inf\wdma10k1.inf and \winnt\inf\wdm_emu.inf files before running kXSetup.
