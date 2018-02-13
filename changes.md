# Changelog

12/28/2013 - Version 5.00.3552 (BETA) released

kX now opensource on github!
This change log will no longer be maintained.

12/18/2010 - Version 5.00.3551 (ALPHA) released

Fixed issue with Wave HQ unsupported in Windows 7 (should work with all p16v-compatible cards now). p17-based cards will NOT support Wave HQ (as usual)
Fixed mapping for Audigy2 ZS notebook side outputs
Fixed kX Mixer memory leak (system hangs while HDD activity is high, kxmixer allocates a lot of memory), specific to Windows 7
Fixed kX Mixer combo boxes showing no settings, empty lists (SPDIF and similar options), specific to Windows 7
Added support for 32/64 ASIO clients under x64 OS (new feature)
Improved 32/64-bit installer with support for UAC
Fixed ASIO registration issues under x64 OS
Fixed issue with ASIO driver not showing correct device names (you may see a UAC message when starting kX Mixer, this is OK)
Installer updated, removed several shortcuts, added new ones, simplified installing, removed legacy code
Fixed AC3 decoding not working under x64 OS
Fixed AC3 passthrough problem introduced in 3543, should work fine now for Audigy/Audigy2
SDK changes:
License agreement is GPL now
Changed �char *� to �const char *� in most places, some plugins might no longer load, need to update and re-compile them
KX_MAX_NAME is now obsolete, use KX_MAX_STRING [set to 128 by default]
More parts of the driver released open-source under GPL
OS X driver released opensource (without kX HAL though, just CoreAudio layer)

09/18/2009 - Version 5.00.3550 (BETA) released

Fixed issue with add-ons on multidevice configurations (E-DSP Control, 'mnu_idx')
Fixed issue with PCs with more than 2Gb of memory, thanks to thrillhouse82
Fixed issue with kX Console unable to launch from the tray menu after changing current folder
Fixed 'slow tooltips' issue in kX DSP
Fixed 'no labels' issue in kX DSP

08/19/2009 - Version 5.00.3549 (BETA) released

Fixed memory issues with PCs with more than 2Gb of memory
Added an internal option in order to fix A2ZSNB noisy playback issue

07/28/2009 - Version 5.00.3548 (BETA) released

Fixed a bug with Power Management (ASIO channels not restored properly after Sleep/Hibernation)
Fixed a bug 'Master Mixer unusable' on 10k1 cards in Vista and Windows 7
Fixed support for multiple E-DSP devices
Fixed compatibility issue with Windows 7
Certain parts of kX API and kX Mixer plugin management released opensource (GPL-covered)
Included Mac OS X-compatible SDK with full source code for kxapi.a

07/19/2009 - Version 5.00.3547 (BETA) released

Fixed issues with x64 driver (during DSP reset and restoring plugin settings)
Fixed kX DSP tooltip issue

04/19/2009 - Version 5.00.3546 (ALPHA) released

Added support for 64-bit Windows (Vista x64 and Windows XP x64)
Added digital signature for the driver and the installer (signed by CEntrance, Inc.)
DSP plugins and Add-ons from previous versions are no longer compatible!
Added experimental support for 44.1kHz mode for E-DSP devices (kxctrl-tweakable, use on your own risk!)
Fixed E-DSP KX_IN/KX_OUT assignments for ASIO
kX is no longer installed into windows/system32 folder, but stays in Program Files, do NOT copy any kX files to system32!
Added to the driver installer KXM and micro effects by stylus [see the SDK for instructions]
Added to the driver installer UFX plugins by Max M. [32-bit version only]
Added to the driver installer ProFX and synth plugins by LeMury [32-bit version only]
Added 'sa.minus' Spectrum Analyzer by Max M.
Fixed multichannel fxbus assignment issue
Fixed issues with loudness compensator (based on Russ changes)
SFMan32.dll is not installed for x64 platforms, because it is not 100%-compatible with 64-bit OS
Removed card/model information from the INF file (and in Device Manager you will only see 'Generic' cards now)
Known issues:
Launching KXS, KXP, KXL files from Explorer might not work in Vista due to UAC
Speaker Test does not work in Vista
SPDIF AC3 output may not work correctly in Win64
CodeMax library is not supported under Win64
SDK / For developer:
iKX class updated to be cross-platform [supports OS X now]
(note the changes in create(), open(), close(), destroy() - see kxctrl sample)
edspctrl is cross-platform now
kxctrl is cross-platform now
Most of the SDK sources released under GPL (GNU Public License)
SDK license agreement updated
Since the mixer is no longer in system32 folder, kFile::get_full_skin_path function is used (see efx-tube example)
Most DWORD pointers in SDK replaced by uintptr_t:
e.g. publish_plugins, iKXPluginGUI::extended_gui, kMenu::track etc...
Certain 'ints' replaced with 'size_t'
MFC Timer uses UINT_PTR instead of UINT, if your code uses timer, update accordingly (see 'dynamica' example)
kxparam_t is 'int' for x64 builds, thus, most DSP effects need to be updated
iKXPlugin::get_plugin_presets() returns kxparam_t* instead of char * (all plugins need to be updated!)
Most char pointers updated to 'const char *'

08/11/2008 - Version 5.00.3545 (BETA) released

Fixed a bug in INF file introduced in 3544 ("KX_WAVEOUT89_NAME" issue)
ASIO send routing fixed for 10k2 cards (should not show FXBus16 as an option now)
Renamed 'unknown' cards to kX Mixer-recognizable model names (without "?")

07/28/2008 - Version 5.00.3544 (BETA) released

improved 24-bit support
changed default routings and WinMM device names
updated kX Router
added 'reload firmware' button for E-DSP control
fixed power management issues with E-DSP
Surrounder+ default preset set to 'direct path'
optimized FXBusX microcode

07/17/2008 - Version 5.00.3543 (BETA) released

added support for 24/48 ASIO for all 10k2-based devices (audigy, audigy2, E-DSP)
added E-DSP control panel
E-DSP code is GPL-covered and included with the SDK
most DSP effects (epilog, prolog, xrouting, fxbus, ...) were re-written to provide bit-accurate playback and recording on default volume settings

05/28/2008 - Version 5.00.3542 (BETA) released

Fixed input name on Audigy2 ZS Notebook (mic / line-in)
Fixed 'Stereo Mix + Gain' microcode
Added bit-accurate 16/48 playback (SPDIF-out bugfix) on Audigy2/Audigy devices [via EpilogX and FXBusX]
Added bit-accurate 24/48 playback on Audgiy2/Audigy devices [via EpilogX and FXBusX, WinMM only]
Added initial support for E-DSP audio cards (E-mu 0404, 1010, 1212, 1616, 1820) - 16/48 mode ONLY
Added CLEAX2Reverb effect with 64 presets [by Russ]

04/05/2008 - Version 5.00.3541 (BETA) released

Fixed issue with 'Wave' mixer slider (introduced in 3540)
Fixed issue with AC-3 support under WinXP (introduced in 3540)
Fixed AC97 3DSE selection on certain card models
Increase number of plugin categories
Fixed minor WinXP mixer issues
Fixed 10k1 Surrounder+ issues
Fixed skin issue of the FXRouter effect

03/28/2008 - Version 5.00.3540 (BETA) released

Fixed multichannel playback in Vista
Minor Vista compatibility issues fixed
Fixed AC-3 decoding/passthrough in Vista (via separate SPDIF device)
Improved compatibility with certain TV-Tuners (WinXP)
Removed joystick INF file, since it did not work anyway
Fixed Master volume in sndvol32.exe and minor Mixer API-related fixes (WinXP, Vista)

08/23/2007 - Version 5.00.3539 (BETA, internal) released

This is long-expected Vista-compatible (x86 only) release
Most changes found in 3538 changelog
Significant changes since 3538m:
- ASIO support under Vista
- Fixed disabled device state in Vista control panel
- kX Mixer master controls are not working (known issue)
- The driver no longer links against debugging libraries, legacy DSP effects and plugins will not work without recompilation

01/21/2007 - Version 5.00.3538 (BETA, internal) released

Re-arranged kX Distributions
Removed Win98 support
kX Manager code completely re-written
Added initial support for 6.1 and 7.1 speaker-sets
Fixed bug with 'kxctrl -shw 19' option
Added an option for AC97.2 input (on the AC97 mixer page)
Added support for Audigy2 Zs Notebook
Added '24/96 Router' for P16V hardware mixer (Audigy2 only)
Added 'kX Console' menu item
Added support for multiple ASIO drivers
Improved SoundFont attack issue
Improved kX DSP connect/disconnect features (hold 'Alt' button for legacy behaviour)
Plugin window position is now saved and restored automatically with the settings
Fixed bug with HpSp plugin (invalid channel assignment)
Improved Speaker Test applet
Changed the default routing for ASIO recording (kX In0/1 is now equal to WinMM Rec path)
Improved support for hidden kX DSP effects
Improved Power Management / Hibernation support
Polish, German, Spanish, Chinese and Danish translations updated
Turkish translation added
Fixed bug with MX6 mixer automation support
Changed default recording level for Wave/Synth sources ('what you hear' is now OFF by default)
kX ASIO driver re-written to support 24/96 and other formats (Audigy2 only) (EXPERIMENTAL, not yet functional)
Added buttons to copy Hardware Configuration / IO Status to clipboard
Improved 24-bit and 32-bit format support (Audigy2)
Added custom SoundFont manager (sfman32.dll)
Added custom VSTi-based SoundFont manager
Added hack to fix Cubase SX patch names issue
Fixed minor bug in Dane disassembler
Added support for WinRar3-archived skins
Added option to minimize / restore kX DSP objects
Added option to disable content redraw while dragging kX Manager windows
Fixed some CLReverb4-related bugs
Crossover, BoobleGum, Vibrato effects added
Removed RemoteIR acceleration
Fixed several SB22x-related issues
Improved SRC DSP effect
Initial support for Audigy2 Value added
Fixed incorrect translation (8-point surround)
kX Tray icon should be visible after Explorer crashes
ASIO Control panel improved
Added CD-SPDIF AC-3 decoding support
Improved DSP-P16v resampling quality (i2s output, analog, audigy1/2)
New DSP Effects added (newer Dynamica, ADC, Mixy etc.)
Initial GSIF2 support (without recording and/or MIDI-In/Out)
Fixed issue with invalid icons in Speaker Test applet
Fixed issue with Audigy2 AC-3 passthru for certain decoder models
Added additinal ASIO performance tweaks for SMP/HT machines (up to 1ms latency!)
Fixed issues with ASIO control panel not saving changes
ASIO sync code moved to kernel level
Improved 'Driver Compatibility' window
Changed default peak meter mode
Fixed issue when renaming plugins (spaces)
Fixed issue with kX Mixer handling multiple Surrounder instances incorrectly
Improved SoundFont support for looped samples
Fixed bug with invalid AllNoteOff/AllSoundsOff message handling
Added sync method selection for kX ASIO control panel
Added 'default' button for ASIO control panel
Fixed brightness MIDI controller
Added option to disable UART routing to kX Control device ('driver compatibility')
Added support for dynamic drum channel assignment (kxctrl -shw 21 value)
Several translations updated (Chinese, Polish etc.)
Improved ASIO sync code (should improve performance compared to 3534f)
Added option to assign double-click action on system tray
Updated mixy42, mixy82 and loudness plugins
Enhaced support for assignable mixer controls (-ma option for kxctrl)
Improved minimized windows support
Added Vista support [ASIO, Synth, DSP]
Improved AC-3 stability
Fixed BSOD issue with volume controls
Added support for analog-ins on A2ZS Notebook
Fixed issue with 24/96 router
Fixed skin memory leak issue (Note: use Zip instead of Rar)
Fixed EFX effects boot time issue
kX API/kX SDK:
Added support for constant registers (Dane)
Added support for kX Plugin Manager and kX Manager Add-ons
Added support for p16v per-channel volumes
Added access for kernel-level ASIO timers
Added support for 'RAW' midi events in kX Automation
kX SDK License Agreement has been updated to Revision 4
kX API revised -- legacy plugins are no longer supported
Added support for HWND extraction for iKXPluginGUI
Added support for IKX_CLOSE_AND_REOPEN notification
note to kX API Developers: include 'kxcompat.h' file for your legacy code
Added passthru on/off functions
Updated kX Add-on architecture
Added option to launch any effect/kX Mixer applet from the skin by GUID

02/17/2004 - Version 5.00.3537 (BETA) released

Fixed SMP/HyperThreading compatibility issues
Fixed bug with invalid 24/96 loopback volume level
Fixed bug with invalid 24/96 Master volume after reboot
Improved SPDIF output quality for Audigy2 boards
Swedish, Polish, Brazilian Portuguese, Spanish, Italian, French, Danish and German translations updated
Fixed bug with AC-3 Passthru on Audigy2-based boards
Fixed bug with incorrect handling of DOO mode for certain boards
Added support for 48000 and 192000 sampling rates for the 'Wave HQ' device
Support for 44100 is not available at the moment (additional research is necessary)
Added support for 32-bit (32-32) format for Kernel Streaming clients (fake :))
Default levels for CD-Digital and SPDIF-In set to '-inf'
Fixed bug with FXMix2 plugin (10k1-compatibility issue)
Improved RemoteIR support for trayed WinAmp and Foobar
Improved RPN/NRPN support (fixed certain formulas)
Fixed bug with kX Mixer handling default device change incorrectly
Fixed bug with invalid 'kX1/MicIn' and 'kX0/LineIn' to 'AC97 In' mappings (0dB = 100%)
Fixed invalid AC97 recording gain visualization
Added 'Unload all SoundFonts' button
Added an option to filter EAX calls ('Driver compatibility')
Updated IO Status window
kX API: 'hidden' kX DSP objects partially implemented
Minor kX Setup improvements
Fixed minor bug with default routings and kX Router applet
Added support for SB22x model
Fixed minor bug with 24/96 'Wave HQ' volume
Added support for (32-0) formats
S/PDIF sampling rate is now automatically set/reset when AC-3 Passthru is active
Fixed bug with SPDIF 24/96 recording ('Wave HQ' device)
Fixed minor SoundFont/SFMan-related issue
Added support for certain OEM cards
Fixed bug with 'p16v recording source' selection causing reboots
Fixed bug with AC97-In +/- 12dB jump on mute/unmute
Added two NoiseGate plugins
Added compatibility option for Audigy2 passthru
Improved RemoteIR compatibility with certain WinAmp versions
Added option to disable S/PDIF notifications
Improved RemoteIR support (details...)
Fixed bug with certain settings not saved on reboot
Improved MIDI UART IRQ handling
Major SoundFont memory management improvement (support for large SoundFonts added)
Some SoundFont-related optimizations (voice management engine)
Improved UART Input/Output
Added CLEAX4Reverb effect with certain presets (ALPHA)
Added option to turn on/off AC97 to Front Speakers routing (for 10k2 cards: 'kxctrl -shw 19 1')
Certain AC-3 decoding engine improvements
Fixed issue with kX Router restoring settings incorrectly after Hibernate

12/04/2003 - Version 5.00.3536 (ALPHA) released

This version might be not 100% compatible with HT/SMP machines
Improved 3-D audio attenuation and Doppler models
Improved kernel-level 3-D audio synchronization (BETA)
Improved SMP / HyperThreading compatibility (EXPERIMENTAL)
Improved Interrupt handling code
Added AC97 'Recording Gain' slider (for analog ac97 gain)
Fixed bug with incorrect multibyte characters handling (Chinese etc..)
Fixed bug with kX Mixer notifications / RemoteIR support
Effect names and languages are now sorted alphabetically in the kX Tray menu
Added support for CL-compatible sampling rate interpolation (compatibility option)
Added option to reset hardware voices (kxctrl -rv)
Option to turn off FXBus amounts smoothing added (compatibility option)
Improved SoundFont support (looped and non-looped samples)
Minor sfman32.dll compatibility issues solved
Improved AC-3 decoding of non-standard AC-3 streams
The position of plugin windows are now saved
Fixed bug with center/lfe/digital channels not muted when headphones are plugged-in
Fixed incorrect vertical peak meter visualisation
Fixed minor bug in kX Automation
Added 'Expander', 'Expander+', 'WaveGen3' DSP effects
Added 'Delay A', 'Delay B' and 'Dynamics Processor' effects
Optimized 'FXMix2' effect
Fixed bug with kX DSP displaying resource allocation incorrectly
Danish, Traditional Chinese, Polish and Spanish translations updated
kX API: added card-specific input/output labeling
kX API: added support for text-align properties
Fixed bug with invalid FX routings ('no reverb' issue)

10/14/2003 - Version 5.00.3535 (ALPHA) released

Added support for 24/96 playback and recording for Audigy2-based boards (EXPERIMENTAL)
Improved power management support
Improved hardware compatibility with certain audio cards
Fixed bug with AC97 contoller power management
Fix crackling sound on start-up for Audigy2 boards
Improved real-time panning quality
Added option to choose Wave panning method (true pan or balance) - by command-line tool
Added compatibility option to enable AC-3/Multichannel volume change
Added option to unload kX Mixer automatically after start-up ('--once')
Added support for horizontal peak meter
Added a shortcut for the peak meter to the kX Mixer page
Improved IO Status window
Improved 'mute speakers when headphones are plugged-in' option
Added option to choose the desired speaker spatialization method (by using command-line tool)
kX DSP window enlarged
Added real-time update option for kX Editor and kX API (EXPERIMENTAL)
Updated Filter effects (may be not 100%-compatible with previous)
Added APS Compressor+ with Side Chain input
Added MX6 (custom mixer, v 1.113a) DSP effect (described here)
Added high-quality headphones positioning effect (HpSp)
Updated XRouting effect to support 8-point spatialization
Prolog and Epilog effects re-written to support amplification (EXPERIMENTAL)
Improved kX Mixer indication for inputs & outputs (levels measured in dB)
(NOTE: if you have any pre-3535 setting files, the new prolog/epilog features won't be available until you upload new prolog/epilog effects into the DSP. Resetting settings will upload the new effects automatically)
(NOTE: the AC97 slider volume is shown in percents (%); 100% corresponds to 12dB amplification)
The SDK License Agreement has been updated
Danish translation added
Polish translation updated
Brazilian Portuguese translation updated
Improved System Tray icon


08/18/2003 - Version 5.00.3534f released [Quick Fix]

Fixed kX 3-D attenuation model
Fixed kX 3-D Doppler calculation
Fixed kX 3-D Distance Factor issue
Added kX 3-D compatibility / debugging options
Added support for SB0320 card
Added Thai language support

08/02/2003 - Version 5.00.3534 released

On-the-fly support for sfArk v2 files added
Fixed some issues related to WavePCM mixer slider
Fixed minor bug with the setup program under Win98SE / WinME
Fixed incorrect 'Swap Front and Rear' function while in 'Digital Output Only' mode
Improved support for multiple devices
German translation updated
Italian translation updated
Polish translation updated
Fixed real-time pitch calculation for certain card models
Added option to enable/disable real-time resonance and filter cutoff (Synth compatibility)
Added support for 44100 sampling rate for ASIO (ALPHA, without recording!)
Fixed bug with Cubase SX handling ASIO 44100 sampling rate incorrectly
Added option to tweak GSIF buffer size
Added option to mute speakers when headphones are inserted
Fixed bug with B2B plugins
Improved Modulation CC compatibility (VibLfoFreq Divisor in Synth Compatibility panel)
Initial support for hardware-accelerated DirectSound 3-D (attenuation and spatialization)
(In order to disable DirectSound acceleration, select 'Wave 4/5' device)
Added option to choose bank selection method (Synth Compatibility)
Fixed bug with multiple soundfonts playing simultaneously
Added option to select target Synth device on SoundFont upload
Added automation for most plugins
Fixed bug with AC-3 passthru for certain Audigy2 cards
Added 'Multimedia Properties' shortcut
Peak plugin improved
Fixed some minor issues with skin handling code

05/30/2003 - Version 5.00.3533b released [Quick Fix]

Fixed bug with DirectX Panning function (for 10k1-based boards)

05/28/2003 - Version 5.00.3533 released

Some fundamental SoundFont changes:
Fixed modulation, attack, decay, sustain, release formulas
Improved panning quality
Added support for 'Balance' MIDI controller (#8)
Fixed stereo samples support (based on CL behaviour)
Fixed attenuation formulas (based on CL behaviour)
Added 'Synth Compatibility' option
Default Synth volume increased by +6dB
Fixed Velocity to FilterCutoff formula (can be turned off via 'Synth Compatibility' flags)
MIDI Implementation chart revised

Fixed bug with incorrect patch names for drum channels
Fixed bug with clicks when using Vienna
Fixed some sfman32.dll-related issues
Re-distributed sfman32.dll updated (should fix patch name issues with multiple devices)
(NOTE: you may need to install sfman32.dll from a previous driver version if you experience problems with SoundFonts and / or patch names. Please review the following article (SoundFont discussion for details.).
Fixed bug with muted SoundFont devices when running Vienna

Some of the inputs and outputs re-labelled based on IO Assignment guide
Fixed Optical / Coaxial labelling 
(a new 10k2-specific slider 'AC97 In 2' corresponds to Philips UDA ADC codec connected to the AC97 codec)
(in order to be actived, it is necessary to turn on AC97 master volume ("kxctrl -sac97 0 0")
(don't forget to turn it back off by running "kxctrl -sac97 0 9f1f") [EXPERIMENTAL]
Added 'I2S 2 Out' slider for 10k2-based boards

Minor GUI improvements
Added 'Enable Balloon Tooltip' option

Fixed bug with 22050Hz recording frequency being rejected
Added support for 96000Hz recording in 'Direct SPDIF Recording' mode (if supported by hardware)
Added 24-bit audio playback support for 10k2-based boards [EXPERIMENTAL]

Fixed bug with 'Bypass' option not being restored correctly
Plugin presets handling code re-written (ALPHA)
Added option to import / export plugin presets (ALPHA)
Added context menu for selecting presets via kX DSP
Fixed bug with saving settings in version-independent format

Major kX Mixer optimizations solving long delays
Improved kX Mixer memory management

Added option to preserve settings on upgrade/reinstall [EXPERIMENTAL]
Added ASIO Control Panel for kX Mixer (Settings - ASIO Control Panel)
Fixed bug with AC97 controls been swapped (left and right)
Added 'FXBusX', 'Prolog Lite', 'Epilog Lite k1', 'Epilog Lite k2' and 'AC3 Passthru' effects
Added 'FXMix' effect
Updated 'B2B' and '16to32' effects
Fixed bug with help displayed incorrectly
Fixed playback buffer sizes (Setup Buffers window)
I/O (SPDIF) Status window added
Added support for AC-3 passthru for some 10k1-based cards (with chip revision>=7) (ALPHA)
Fixed bug with incorrect WinMM/DSP volumes when set to maximum
Fixed bug with 'LineIn' WinMM slider being handled incorrectly
GSIF support implemented
Improved GSIF audio latency

04/30/2003 - Version 5.00.3532 released

Audigy2 Platinum Ex and External Drive support added
Fixed bug with SPDIF Freq selection
Fixed possible bug with SPDIF Bypass mode
Stereo samples support (SF2) improved
Improved SoundFont velocity/volume/expression handling
Improved SoundFont formulas
Added support for multiple SoundFont loading via 'Load SoundFont' dialog
Improved support for multiple kX-compatible cards
Selective kX driver installation for multi-card set-ups implemented
Added 'Save'/'Restore' option for each kX Mixer applet
kX Ctrl utility updated:
- Interactive mode added
- Options to reset settings / re-initialize DB card added
Fixed bug with incorrect 10k2 microcode dump function
Fixed B2B DSP Effect
Fixed bug with AC-3 passthru for 10k2-based boards - should work correctly now
Improved AC-3 synchronization
Ukrainian translation added
Japanese translation added
Added support for saving / restoring kX Automation settings (ALPHA)
Fixed bug with MRU list of settings
Fixed 'click' when testing speakers
Improved test sample for subwoofer channel
Improved ASIO synchronization
Improved ASIO sample position accuracy
Improved UART Out SysEx handling
Initial GSIF support
Pseudo Mic-in slider for Windows Mixer added (for compatibility only)
Fixed support for sndvol32 mixer notifications (ALPHA, causes slower slider updates)
Fixed bug with Windows Mixer - kX Mixer notifications (redraw)
Fixed bug with 'Reset global settings'
Fixed bug with B2B [v2] plugin
SPDIF-In AC-3 decoding implemented for 10k2-based boards (alpha: high latency...)
New CLEAX3Reverb effect added ('Concert hall' preset)
New Stereo Mix + Gain effect added
Added a 'Software/kX/Mixer/EnableBalloonTooltips' registry option
Fixed bug with APS SPDIF Recording levels
Fixed bug with kX Synth volume
Fixed bug with ASIO Control Panel window
SPDIF Direct Recording option added for 10k2-based boards
Added support for Separate OSD/RemoteIR settings for each device
Improved OSD visual appearance
Notification / RemoteIR code re-written
Enhanced On-Screen Display function added
Added support for Foobar2000 player (kX RemoteIR)
Added support for Windows Media Player (kX RemoteIR)
Added support for WinDVD Player (kX RemoteIR)
Added support for WinAmp 2.xx (kX RemoteIR)

03/27/2003 - Version 5.00.3531 released

Fixed bug with clicks at the beginning of the ASIO / Multichannel playback
Fixed bug with Surrounder effect (Bass redirection)
Fixed bug with Audigy2 support
Additional presets for Eq and Surrounder effects added
SoundFont memory management improved
Brazilian Portuguese translation updated
Italian translation updated
APS Pitch (ALPHA) and Crossfade effects added
'Mute' / 'Bypass' options added for all DSP effects (ALPHA)
An option to disable kX Remote added
An option to disable tooltips added
Support for Multimedia Keyboards added (ALPHA, disabled by default)
Numeric mixer values added
RemoteIR timings changed
Minor GUI updates

03/03/2003 - Version 5.00.3530 BETA released

Fixed bug with kX DSP tooltips not being updated
Fixed bug with kX Mixer window initial position
Fixed bug with 'Re-align plugin' command
Fixed bug with icon association
Fixed 'Always On Top' option for plugins
Fixed bug with ASIO driver device selection
Fixed bug with AC97 codec programming for certain card models (problems with subwoofer and center)
INF file and card names updated
Kernel-level driver partially re-written
(WDM) Multichannel playback support added (via 0/1 device) - up to 6 channels
DirectSound 3-D Software emulation improved (via 4 / 5.1 speakers)
The default routings for 'Wave X/Y' devices changed - read Routing Guide for details
Routing plugin completely re-written (ALPHA) - read Routing Guide for details
Fixed bug with 'Wave Balance' slider (Windows mixer)
Default ASIO routings updated
New 'Decimator', 'Gain', 'Surrounder', 'XRouting' effects added
'WaveGen' effect updated
New Recording sliders added (Rear & Center/Subwoofer levels)
Improved Audigy2 support
Aqua skin updated
'Phantom' recording and playback devices removed
Italian translation updated
Advanced SoundFont control options added (including initial SoundFont Collection support) (ALPHA)
Extended voice analyzer notifications added
Option to disable OSD for kX Remote added
kX Plugin architecture revised
kX Plugin exception handling added
kX Plugin API: support for 'built-in' presets added
kX Plugin API: new 'Combo' control added
kX Plugin API: event handling simplified
Sample 'DSW' Project added to the SDK (\fx_demo folder)
kX SDK package updated
Skin API: Tiled backgrounds support added (ALPHA)
Skin API: built-in plugin skins implemented (ALPHA)

02/07/2003 - Version 5.00.3529 ALPHA released

kX Mixer core partially re-written
kX GUI core re-written
kX Save/Restore settings feature revised and partially re-written
kX Skin Architecture revised
Vienna / SoundFont Editing feature implemented (except 'wave playback') (ALPHA)
Fixed some skin selection related bugs
Initial Audigy2 support added
New NSIS-based Setup program
New APS Everb effect added
kX Setup: OS detection code updated
Major voice management bug fixed (infinite sustained notes)
Voice management improved
Routing-related changes
Korean translation added
Greek translation added
Chinese (Simplified and Traditional) translations added
Added card name to each window's title
'Unknown' i2s output added for 10k2-based boards
'Swap front and rear' option now affects 'digital' outputs
Fixed SoundFont Percussion Banks handling
Fixed issue with analog center/subwoofer on some 10k2-based boards
Fixed bug with Analyzer appearance
Fixed bug with FilterQ parameter being programmed incorrectly (non-realtime)
Fixed internal cache control register programming (less clicks / distortion)
Fixed bug with kX DSP resources leakage
Fixed minor bugs with different translations (such as Spanish)
Fixed bug with skin / language selection
Added support for mute/unmute for psudo-LineIn source (ALPHA)
Default ASIO routings added
Fixed bug with 8-bit data streams mapped into the memory incorrectly (ALPHA)
Drammatically improved ASIO driver memory management (ALPHA)
Implemented MIDI CC 71 (Sound Resonance / FilterQ); '64' = '0' (ALPHA)
FX Amounts implemented (and moved from the 'Effects' page of the mixer to the kX Router applet)

12/02/2002 - Version 5.00.3528 ALPHA released

Hungarian translation added
'SPDIF Source Select' feature for E-mu APS implemented (BETA)
'Analog Gain' feature added for E-mu APS cards (BETA)
Fixed kXSetup to leave any joystick drivers already installed intact
kX Skin: translate window gadgets position made configurable
Fixed bug with WinMM volumes for 4/5, 6/7 and 8/9 devices (in multicard configurations)
Fixed pan formula
Fixed minor GUI bugs
Implemented MIDI CCs 16,17,18,19 (control SendE, SendF, SendG, SendH for 10k2-based cards) (ALPHA)
Implemented MIDI CC 68 (Legato) via Attack Time (ALPHA)
Implemented MIDI CC 72 (Sound [Vol] Release Time); '64' = '0' (ALPHA)
Implemented MIDI CC 73 (Sound [Vol] Attack Time) '64' = '0' (ALPHA)
Implemented MIDI CC 74 (Sound Brightness) '64' = '0' (via Filter Cutoff) (ALPHA)
Note: new controllers implementation is a subject to change
Added support for most real-time SF2.1 NRPNs (ALPHA)
Added support for AWE NRPNs (ALPHA)
Reverb/Chorus formulas changed according to SoundFont 2.01 specification (#8.4.8):
reverb[0..255]=(SF_Reverb(%)*2.5+(MIDI_CC91*50/127))*kXMixerFXAmount/255
that is, SoundFont reverb affects hardware reverb directly and MIDI CC91 affects only 20% of the hardware reverb
Fixed MIDI Note-On Velocity to Filter Cutoff formula (according to SoundFont 2.01 Specification, #8.4.2)

11/09/2002 - Version 5.00.3527 BETA released

Increased the number of hardware-accelerated DirectSound voices reported by the driver
Fixed bug with kxsetup unable to find kxskin.kxs file where special characters are used in the account names
'Disable startup splash' option added
Fixed bug with plugin background painted incorrectly
Added support for presets for kX DSP effects
Recently used settings files listing added
'Line-In' slider now assignable to any kX DSP slider (via kxctrl)
Fixed bug with Norwegian and Sweden localizations displaying SoundFont parameters incorrectly
Fixed bug with Plugin windows header displayed incorrectly
Fixed bug with looped samples (SoundFonts) (ALPHA)
Improved SoundFont voice management (mainly of looped voices) (BETA)
Improved SoundFont 2.01 compatibility
Fixed bug with Bypass mode not restored after reboot
Fixed bug with SoundFont page causing crashes sometimes
Added 'Manifest' file for kX Mixer
WaveGen plugin added
Tooltips font made tweakable
Minor GUI changes
Initial NRPN support (E-mu APS-compatible, not realtime) (ALPHA)
Bulgarian translation added
Croatian translation added
French and Polish translations updated

10/23/2002 - Version 5.00.3526 RC1 released

Fixed bug with SPDIF Bypass mode
Fixed Epilog microcode (RecL and RecR can now be connected directly to the FXBus)
Fixed bug with microcode being positioned incorrectly sometimes (system hangs)
Fixed GUI bug with incorrect windows switching after displaying dialog boxes
Chorus/Reverb formula changed once again ;)
final = SoundFont Reverb Amount (0..1000) / 4 + MIDI CC91 Amount (0..127) * 2 + kX Mixer Synth Reverb Amount (0..255)


Keyboard shortcuts added ('1'..'7', 'd', 'e', 'm', 'r', 'a' for opening corresponding windows)
Fixed major bug with WDM/WinMM Recording synchronization
Fixed bug with Alt-Tab Task Switcher icons displayed incorrectly
B2B effect added - for bit-to-bit playback and AC3 passthru (ALPHA)
AC3Passthru effect fixed (for 10k2-based cards only, ALPHA)
Dummy 'LineIn' slider added to Windows Mixer (for compatibility with TV-Tuner software only, ALPHA)
Improved inter-channel synchronization
Target SPDIF selection for SPDIF Passthru added
New 'Phat EQ Mono' and 'Phat EQ Stereo' effects added
EQ effects updated in order to support non-linear parameter changes
Dutch translation added
Brasilian translation added
Italian translation updated
Swedish translation updated
kX API: custom-drawn kX DSP windows interface revised (BETA, subject to change)
kX API: migrated from CDialog to CWnd base class for all GUI objects (BETA)

10/10/2002 - Version 5.00.3525 released

Norwegian translation added
Fixed bug with multiple instances of 'Peak Meter'
Fixed bug with switching languages
kX API: custom-drawn kX DSP windows implemented (BETA, subject to change)
Fixed bug with kX DSP showing connections incorrectly
Detailed tooltips added for prolog/epilog in kX DSP
Fixed bug with long path names being handled incorrectly
Fixed bug with Global Zone generators (sf2) (ALPHA)
Fixed bug with Effect controls displayed incorrectly
Fixed kX DSP Status displaying hardware resources incorrectly
New effect 'APS Compressor' added
Voice management algorithm improved (BETA)
Fixed bug with allocating stereo voices
Fixed bug with releasing sustained voices
INI-files processing speed improved (BETA)
Fixed bug with Midi voices not being freed after StandBy/Hybernation (BETA)
Improved help launching scheme
Fixed bug with kX Remote handling 'Mute' command incorrectly
Italian translation added
Swedish translation added
Second French translation added
Cnv51To2 (kXSurround) effect added [Mixes 5.1 content into 2 stereo channels]
Reverb/Chorus formulas changed: new formula is:
final = SoundFont Reverb Amount (0..1000) * MIDI CC91 Amount (0..127) / 500 + kX Mixer Synth Reverb Amount (0..255) 
Note: this amount corresponds to FXBUS volume only, the actual effect amount can be changed additionally by tweaking the effect itself.


09/24/2002 - Version 5.00.3524 released

Fixed bug with kX Notification (BSODs when plugging in headphones)
Fixed bug with StandBy/Hybernation and BSODs
Fixed bug with Recording (BSODs)

Fixed bug with StandBy/Hybernation mode (related to DigitalOutputOnly mode)
'Downmix' effect added
Initial support for non-administrator priviledged accounts for Win2k/WinXP
Recent save/restore folder is now saved
Epilog effect re-written using temp registers (allows direct FXBUS-Epilog connections)
Fixed 'Reset All Controllers' MIDI handling
Complete support for custom fonts
Improved 'kxskin.kxs' searching algorithm for kxsetup
Added 'tweak' option for 'Peak' microcode (ALPHA, buggy)
Spanish translation added
Romanian translation added
French translation added

09/12/2002 - Version 5.00.3523 released

New self-extracting setup program
Added support for hardware 'mute', 'vol+', 'vol-' buttons for 10k2-based cards
Added Polish language support
Added support for SysEx-controlled Synth volume
Added labels for peak meters
Fixed minor APS-related bugs
Fixed issue with APS ECard when returning from Hybernate/Standby modes
Fixed bug with multiple note_on events producing clicks (with 'sustain pedal' turned on)
Fixed XTram quota for 10k2 cards (64 instead of 32 XTram registers are now available)
Fixed UART/MPU-out buffering issues (alpha)
Fixed bug with kX Automation handling some registers incorrectly
Fixed some significant issues and bugs with multilayered soundfont handling
Fixed 10k2 spdif output representation
Fixed incorrect hold2 / softpedal handling
Minor kX Setup changes and fixes
Initial support for spdif ins / output jacks status notification
Initial support for APS E-Card ADC gain control and selectable D1/D2 routings
New StereoVolume effect added
APS inputs amplification reverted to pre-3522 state
Minor kX Mixer speed-ups and optimizations
Skin architecture revised (Alpha): custom & embedded fonts, labels, languages etc...
Note: some beta testers reported Bluescreens when trying CD SPDIF playback. If you experience this problem - post your card information on our forum (but, please, avoid duplicating existing postings with the same card model ;).
Reverb/Chorus formulas changed: new formula is:
final = SoundFont Reverb Amount (0..100%) * MIDI CC91 Amount (0..127) * kX Mixer Synth Reverb Amount (0..255) / 100 / 127 + kX Mixer Synth Reverb Amount (0..255) / 10 

Note: this amount corresponds to FXBUS volume only, the actual effect amount can be changed additionally by tweaking the effect itself.


08/05/2002 - Version 5.00.3522 released

Added 'Peak' DSP plugin
Added 'Peak Meter' view for the kX Mixer Analyzer: up to 3 different Peak Meters can be displayed simultaneously
(see Help -- kX DSP Guide for details)
Fixed LiveDrive detection code
Fixed issues with LiveDrive when returning from Hybernate/Standby modes
Added Automation support for Timbre, EQ10a effects
Fixed some bugs with kX Automation applet
Initial support for AC-3 passthru for 10k2-based cards implemented
Fixed APS inputs amplification bug (alpha)
Added support for the German language

07/14/2002 - Version 5.00.3521 Beta released

Cubase Automation VST created featuring realtime FX control via MIDI (Alpha)
Integrated seven filters
Added 'FreqSplitter' effect for controlling subwoofer
Separated 'Synth' and 'Synth2' MIDI per-channel routings
Routing Architecture revised: new 'Router' applet added
Simple OSD for the kX Remote implemented
Adjusted kX Remote sensivity
Custom Save Settings feature implemented (version- and card-independent settings files are now supported)
Realtime ASIO/Synth Routing change implemented (beta)
Double-click on a plugin in the DSP window opens 'Tweak Plugin' dialog
Mixer window is refreshed after 'load/reset dsp'
Added 'kX SoundFont' shortcut to the system tray menu
Added 'Tweak...' option for prolog, epilog, routing and FXBus
Plugins now have numbers in the kX DSP window
kX Skin Architecture now supports RAR archives (avoid using solids!)
Command Line Reference updated
Fixed Cubase SoundFont bug
Fixed Dane assembler bug
Fixed incorrect effect names in system tray after 'Rename microcode'
Fixed renamed effects not restored after 'Reset settings'
DSP Clear and Align flags programmed incorrectly bug fixed
Fixed incorrect Start Menu items installation bug (under 98se)
Fixed SPDIF Bypass for 10k2
SDK: DirectSynth Architecture implemented
note: this version is considered to be Beta - that is, new features were not fully tested and may be incomplete


05/14/2002 - Version 5.00.3520 released

Patch name look-up implemented for SoundFont-aware applications (BETA)
kX Mixer multidevice support subsystem completely re-written (BETA)
'Disable RemoteIR' option removed
RemoteIR/Uart SysEx message filter implemented
On-board Mute/Vol+/Vol- support implemented
Basic support for RemoteIR implemented (Vol+/Vol-/Mute)
Minor GUI / Aqua Skin changes
Added new effects 'Mono Mix', 'Stereo Mix', 'Pan x2', and 'Pan'
Optical / Coaxial inputs re-mapped
Fixed bug in the SDK package

05/05/2002 - Version 5.00.3519 released

Separate device for LiveDrive IR function implemented
Added APS Fuzz effect
Added Encode4 effect
Fixed some Dane disassembler bugs
Added 're-align plugins' command for the kX DSP window
Effect lists are now categorized
Fixed DC level for all the inputs
Increased default kX Synth volume and recording level
Added status line for the kX DSP window
Fixed 'Recording Level' control bug
Minor GUI / Aqua Skin changes

04/24/2002 - Version 5.00.3518 released

Spontaneous volume reset bug partially fixed, however, using the Windows Mixer to adjust volume (instead of the kX Mixer) may cause the bug to reappear (due to a Microsoft internal bug - might be fixed in the future).
Fixed 'phantom' recording devices bug
Optimized AC-3 decoding
Fixed uninstaller bug (Run section)
Fixed SPDIF Frequency switcher bug for Audigy
Implemented SPDIF Bypass for Audigy
Integrated '3D Sound Gen' effect
Separated 'Volume' and 'Volume+DC' DSP effects
Removed 'Default tweaker' for kX Mixer-controlled DSP effects (epilog, prolog, routing)

04/10/2002 - Version 5.00.3517 BETA released

Fixed LiveDrive detection algorithm
WinMM mixer notification implemented
Standard default tweaker is now provided for every tweakable effect
Fixed kxctrl RIFX extraction TRAM bug
Additional ASIO latency improvements made
kXPlugin API updated: note IKXPLUGIN_ defines
Alpha blending is disabled under 98SE due to system instability issues (microsoft bug)
Target SoundFont bank is now selectable via 'Load SoundFont' dialog
SoundFont Bank assignment is now saved in settings file
RemoteIR support can be disabled by using Settings->Disable RemoteIR menu
New effects Flanger, Stereo/Mono Vocoders, Phase and Overdrive2 built-in.
Fixed bug affecting 'playback-only' ASIO clients (such as Fruity).

03/31/2002 - Version 5.00.3516 released

WDM PCM core re-written
Dramatically improved ASIO playback-recording synchronization
UART Out improved
Initial IR support
Fixed bug with enable/disable microcode
Fixed FPU-related bug: AC-3 content playback should be more stable and without artifacts
Fixed interpolation bug when dynamically changing sampling rate
Swap Front/Rear and Route Phones to Center/Sub no longer require DSP reset
One more attempt to support APS E-Drive... it should work now
Changed E-mu APS default mappings
Fixed AC97 front output phase problem
Fixed External subwoofer -related bug
Fixed AC97 codec PCM output volume: physical analog front should sound better now
Fixed headphones routed via center/sub volume
Fixed 10k2 SPDIF output volume being too low
Fixed ASIO buffers allocation strategy (no more lock-ups)

03/10/2002 - Version 5.00.3515 (BETA) released

Separate devices for front/rear/center+subwoofer outputs added
Shell integration - right click context menu added for kX files
DLL--KXL and ZIP--KXS types changed
Fixed bug in 'Register Dane Source' dialog
Fixed bug in Interpolation ROM settings: WinMM should sound better
Added '10 Band EQ' and 'Timbre' DSP effects
Fixed skin registration bug
Lots of kX Setup fixes
New FXBus representation
For Audigy the number of FXBusses increased up to 32
'Always on top' setting is saved now
SoundFont Manager is now included in the kX Software package
StandBy and Hybernation features should work without any problems under 2k/XP/98SE/Me
Fixed Start Menu items installation routine
Windows XP icons revised
kX Plugin API: core GUI-related changes

02/22/2002 - Version 5.00.3514 (BETA) released

ASIO Recording implemented
Fixed memory leaks in kxctrl
Fixed virtual memory leaks on faults in kX ASIO
Fixed 'Speaker Test' dialog reporting 5.1 speakers incorrectly
Fixed but with 'MicBoost' setting Default mapping changed for surround left and right channels, center and subwoofer (should be more logical now)
Fixed bug in multiclient support for ASIO (multiclient playback)
Implemented hardware mute/unmute via onboard connector
Improved mute/unmute strategy when saving and restoring configuration
Changed E-Drive/LiveDrive initialization code. E-Drive may work now (... and may not)
'Rename microcode' implemented
kX Editor improved
MIDI Reverb/Chorus formula changed:
- reverb = send_c*(SoundFont_reverb*255/1000+CC91*255/127)/255 
- chorus = send_d*(SoundFont_chorus*255/1000+CC93*255/127)/255
Fixed TRAM allocation (BSODs on setting TRAM size)
Fixed Optical Output on Audigy Drive
User-friendly error reporing in kX DSP
Fixed RIFX binary GUID bug (re-run 'kxctrl -mx' on your DLLs)
Fixed SoundFont sample size limitation (long-sampled instruments should be played back better)
Skins no longer contain duplicated data. Skin Architecture revised
kXAPI: new CKXFile class for skin support
kXAPI: DSP plugins are now skinnable

02/09/2002 - Version 5.00.3513 released

GUID generator for effect plugins now built-in (Settings->Generate GUID)
Support for RIFX binaries added
Save/Restore microcode state function now supports Dane Sources and RIFX binaries
RIFX extractor updated

02/08/2002 - Version 5.00.3512 released (beta)

Save/Restore microcode state fully implemented (including connections)
Added 'Disconnect input' feature
Fixed microcode translation algorithm
Save/Restore settings: SoundFont loader doesn't mute Master output anymore
Fixed ASIO channel assignment bug
Minor ASIO timing fixes
kX API: function get_connections() implemented
AC3 buffers are now configurable via Settings->SetBuffers

02/06/2002 - Version 5.00.3511 released

Fixed stereo panning bug (panning vs balance).
Brand new skin (Aqua skin).
Fixed incorrect restore of FX parameters.
Fixed Reverb/Chorus MIDI controller-related bug.

01/29/2002 - Version 5.00.3510 released

Reverb and Chorus effects are now properly connected
Reverb and Chorus controls updated (kX mixer -> FX Amounts page)
New Overdrive effect added (built-in, but without controls)
New XSumm effect added (built-in)
TS PentodeM4 effect is no longer loaded by default
Fixed memory leaks in kX mixer
Save/Restore of Reverb/Chorus parameters implemented
Fixed 'Reset Settings' bug
Improved DSP level control

01/22/2002 - Version 5.00.3509 released - BETA release

kX API: added dsp_stop(), dsp_go(), dsp_clear() functions
Added kX DSP -> Clear Microcode menu item
Fixed TRAM address management for 10k2-based cards
Fixed ASIO routing bug (save/restore settings)
Fixed 'Transparent background' bug
DSP Plugin Management is being rewritten. Wait for 3510!
Added Save/Restore input/output level feature
Added 'Reverb Lite' DSP Effect
Added 'Stereo Chorus A' DSP Effect
Partial Save/Restore DSP state support

01/16/2002 - Version 5.00.3508 released

ASIO subsystem rewritten: increased stability
Removed 'ASIO Panic!' menu item
Effective latency reduced to 5.33ms (depends on CPU performance)
Multiple ASIO client support added

01/14/2002 - Version 5.00.3507 released (minor update)

Added 'Language' menu item
Language selection is automatically saved

01/11/2002 - Version 5.00.3506 released

Fixed 'Save/Restore Settings' bug
Fixed 'Minimize' bug
Added Russian language support
Skin Architecture revised
Changed HEX numbers to Decimal (kX ASIO and kX Router)

01/08/2002 - Version 5.00.3505 released

Added Skin selection
Added 'Internet' menu item
HTMLized and updated readme.html file
Program group 'kX Audio Driver' is now created by kxsetup and 'Reset Settings'
Uninstallation made much more easier

01/05/2002 - Version 5.00.3504 released

Added 'SPDIF Bypass' option (for 10k1-based cards only)
Changed default MIDI Synth playback / recording level
Fixed front/rear/headphones output level
Fixed bug causing continious ringing sound on emu10k1-based cards

01/04/2002 - Version 5.00.3503 released

Implemented 'ASIO' applet
Fixed ASIO panning bug
Fixed ASIO memory allocation bug
Revised ASIO Control Panel
Changed window size of ASIO and Router applets (depends on card capabilities now)

01/03/2002 - Version 5.00.3502 released

Added 'Settings/SetUp Buffers' menu: 
- Permits changing the size of playback and recording buffers and the size of Tank Memory.
Decreasing 'Playback Buffer Size' may reduce latency when using DirectX-based software.
Known issues: 
- your machine may hang or you may experience clicks and sound distortion if you specify buffers which are too small.
After changing Tank Memory size it is recommended that you reset DSP.
All buffer changes should be done with no playback/recording activity.
This feature is considered to be in an 'alpha' state. BSODs are possible. 

Modified Card Selection method (minor GUI change)

Right mouse click on kX Mixer window or other applets now displays a popup menu 
similar to the one displayed in system tray. 

01/02/2002 - Version 5.00.3501 released

Fixed ASIO initial click and play/pause/stop clicks
Fixed ASIO latencies greater than 21.33ms
Fixed UAEs if latency is greater than 21.33ms
Added 'ASIO Panic!' menu (Settings/ASIO Panic!) - mutes all ASIO output
Latencies greater or equal to 86ms should no longer have sync problem

01/01/2002 - Initial public release (version 5.00.3500)