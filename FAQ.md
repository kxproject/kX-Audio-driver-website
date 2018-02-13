## FAQ (Frequently asked questions)

# General

What is the kX Project?
Is the kX Driver FREE?
Which soundcards can I use with the kX driver?
Does kX Driver support SB Live! 24 Bit, Extigy, Audigy LS, Audigy2 NX, USB, Firewire or AC97 audio hardware?
Why should I use the kX driver and not the drivers that came with my soundcard? What are the advantages of the kX Audio driver?
Are the kX drivers aimed at musicians or gamers or both?
Under which Operating Systems can I use the kX driver?
Does the kX driver incorporate DirectX support?
Where can I find the latest version?
Why do I experience clicks and audio artifacts in games?
Does the kX driver have ASIO support? ASIOv2?
Will I get low latency with Cakewalk's Sonar?
Does the kX driver support multiple soundcards? How many?
Can I use the standard Windows Mixer with the kX driver?
Is there a dedicated mixer included with the kX driver set?
What are the mixer features? Can I save and restore my mixer settings?
Will there be GSIF support?
Will there be support for the Extigy and Audigy2 NX USB cards?
Why am I experiencing serious CPU load when I use kX ASIO driver under Logic?
Why are the Front and Rear outputs swapped by default?
Where can I get support for the kX Audio Driver?
Why is there no 'Wave 2/3' device?
Why is my CT4830/SB0090/SB0220 recognized as CT4832/SB0092/SB0222? Does it affect sound quality?
Why cannot I hear any sound when using GigaStudio / GigaSampler?
Where can I find additional information?
Installation / Uninstallation

Why does Windows tell me that I am missing required DLLs when I try to install the kX driver?
How do I install the kX driver under Windows 2000, Windows XP, Windows Vista or Windows 7?
How can I uninstall kX drivers?
What are the minimum system requirements for running the kX driver?
Why does Windows tell me that I am missing required DLLs when I try to install the kX driver?
Why do I get the following message: 'The ordinal 11 could not be located in the dynamic link library DSOUND.DLL'?
Why do I get the message that kxsetup.exe is linked to missing export SHELL32.DLL:SHGetSpecialFolderPathA?
ASIO

Does the kX driver have ASIO support? ASIOv2?
Why do I get the following message: "Error creating input buffer: -2147467263 (#0) [size=4096] ret=-2147467263"?
What kind of latency can I expect to see?
Does kX support ASIO 2 Direct Monitoring?
Why my audio application doesn't detect any ASIO inputs?
ASIO does not work on Windows 8
DSP

Are DSP effects supported by the kX driver?
Is there an effects control panel included with the kX driver set?
Are there new effects included with the kX driver set?
Can I write my own DSP effects for use with the kX driver set?
SoundFonts

Can I use SoundFonts with the kX driver?
Is there a SoundFont control panel included with the kX driver set?
Can I use the Vienna SoundFont editor with the kX drivers?
Can I use the Alive SoundFont editor with the kX drivers?
Is there a 32MB limit on sample playback? Does this apply to the Audigy as well?
Why cann't I load large SoundFonts?
How to get quadrophonic MIDI out of an SBLive with SoundFonts using VMM?
How to setup an SBLive for quadraphonic audio playback?
Troubleshooting

Everything is ok, but I have only one problem, using "Master Mixer" I have some crakles/popes sometimes. Why?
ASIO does not work on Windows 8
kX Mixer does not remember its settings after reboot on Windows 8
After installing kX Driver I cannot hear anything. Why?
Why do I hear audio feedback when using NetMeeting?
How do I turn off the recording feedback?
Why cannot kX Mixer find kxskin.kxs file, although it is in the same folder?
Why do I experience clicks and data corruption while copying / burning CDs? I have a VIA 686B Southbridge chipset.
Why does Windows tell me that I am missing required DLLs when I try to install the kX driver?
Why do I get the following message: 'The ordinal 11 could not be located in the dynamic link library DSOUND.DLL'?
Why do I get the following message: "Error creating input buffer: -2147467263 (#0) [size=4096] ret=-2147467263"?
Why does Cubase cause Unrecoverable Application Error (Blue Screens) in the file emuaps.vxd?
Why do I get the message that kxsetup.exe is linked to missing export SHELL32.DLL:SHGetSpecialFolderPathA?
Why do I experience shutdown problems with the kX Mixer?
Why do I get 'Debug assertion failed' error?
How do I tweak my computer for optimum performance?
My MIDI playback is crackling no matter what SoundFont I use - what should I do? I have VIA chipset and AMD processor.
Why cannot I hear any sound when using GigaStudio / GigaSampler?
Q. What is the kX Project?

A. The kX Project is a totally independent development project whose aim is to provide WDM Audio Drivers for newer operating systems for kX-Compatible audio cards. The kX Project is led by Eugene Gavrilov, Max Mikhailov and Hanz Petrov (full list of contributors here).

Top
Q. Is the kX Driver FREE?

A. Yes, the kX Driver is FREE and will remain FREE. However, you can support the development effort by donating to the kX Fund.

Top
Q. How do I install the kX driver under Windows 2000, Windows XP, Windows Vista or Windows 7?

A. Windows 2000, Windows XP, Windows Server 2003, Windows Vista and Windows 7 provide their own certified drivers for some EMU10kX-based audio cards. Our kX Audio Driver has not been certified by Microsoft (WHQL-ed) and thus a special installation procedure might be required. It is recommended that you first try running kXSetup, and if that fails, follow our Windows XP installation guide. Windows 7 is not officially supported yet [April'2009].

Top
Q. Will there be GSIF support?

A. GSIF is supported since 3533 release.

Top
Q. Why am I experiencing serious CPU load when I use kX ASIO driver under Logic?

A. You should try disabling unused kX ASIO inputs and outputs. Logic opens all 16 inputs and 16 outputs by default.

Top
Q. Why are the Front and Rear outputs swapped by default?

A. Refer to the Front and Rear outputs explanation for details.

Top
Q. Why do I experience clicks and data corruption while copying / burning CDs? I have a VIA 686B Southbridge chipset.

Please read our article Via 686B Southbridge and SBLive / Audigy issues.

Top
Q. Why does Windows tell me that I am missing required DLLs when I try to install the kX driver?

A. The kX Mixer and kX Setup are statically linked to certain Windows DLLs, which may or may not be found on every system. You can download the required files from the kX Download page if they are not present on your system.

Top
Q. How can I uninstall kX drivers?

A. Execute: Start Menu - Programs - kX Project - Uninstall or Re-install kX Audio Driver (Version xxxx) - and click 'Remove'. After the driver is removed, uninstall kX Project installation files by choosing 'Uninstall kX Project Package (Version xxxx)'

Top
Q. What are the minimum system requirements for running the kX driver?

A. Most recent kX driver versions will only install on systems running Microsoft Windows 98 Second Edition, Windows Millenium Edition, Windows 2000 or Windows XP, Windows Server 2003, Windows Vista or Windows 7 (both x86 and x64 versions are supported). At least one Creative Labs Audigy or EMU10k1/EMU10k2-based soundcard, or E-mu Systems APS/E-DSP soundcard, is also required. DirectX 9 or newer should be downloaded and installed prior to installing the kX driver. A minimum of 32 MB of RAM and a video adapter capable of displaying HiColor (16 bit) or TrueColor (24bit) are also highly recommended (actually - required).

Top
Q. Why do I get the following message: 'The ordinal 11 could not be located in the dynamic link library DSOUND.DLL'?

A. You have not installed DirectX 8 or newer.

Top
Q. Why do I get the following message: "Error creating input buffer: -2147467263 (#0) [size=4096] ret=-2147467263"?

A. You have not set 'Hardware Acceleration' to 'Full' in the Control Panel.

Top
Q. Why do I get the message that kxsetup.exe is linked to missing export SHELL32.DLL:SHGetSpecialFolderPathA?

A. Your Operating System is Windows 98 Lite - this OS is partially supported by the latest kX Driver releases no longer supported.

Top
Q. Why does Cubase cause Unrecoverable Application Error (Blue Screens) in the file emuaps.vxd

A. You haven't completely uninstalled E-mu APS drivers and removed all APS-related files from your Windows\System32 directory.

Top
Q. Which soundcards can I use with the kX driver?

A. Currently, kX-compatible soundcards include all EMU10k1 and EMU10k2-based PC soundcards manufactured by Creative Technology Ltd. and/or E-mu Systems Inc., including:

The E-mu Audio Production Studio (APS) card
The motherboard models of 10k1 cards (M002, M003 and others)
PCI256 (CT4890, CT4891 and CT4893) and PCI512 (CT4820 and SB0150) including OEM model (CT4790)
The original Live! (CT4620) and Live! Value cards (CT4670)
The Live! X-Gamer, Live! MP3+, Live! Player 1024, Live! Platinum cards (CT4760) and value cards (CT4780)
The Live! X-Gamer 5.1, Live! MP3+ 5.1, Live! Player 5.1, Live! Platinum 5.1, Live! Digital Entertainment 5.1 cards (SB0060, SB0100, SB0102, SB0220, SB0222, SB0103 and SB0105) and Value 5.1 (SB0101)
The generic and custom OEM Live cards (CT4830, CT4831, CT4832, CT4850, CT4870, CT4871 and CT4872)
The Audigy series, including the Audigy MP3+, X-Gamer, Platinum and OEM cards (CT0070, CT0072, SB0090 and SB0092).
The Audigy 2 series, including Gamer, Platinum, Platinum eX and OEM cards (SB0242, SB0244, SB0320, SB0240, SB0240P, SB0280).
The Audigy 2 ZS series, including Audigy 2 ZS Gamer, Platinum and OEM cards (SB0350).
The Audigy 2 ZS Platinum Pro is not fully supported yet. There are issues with the line in ADC.

24/96 support for the Audigy 2 and Audigy 2 ZS cards is under development.
Audigy 2 Value (SB0400), Audigy 2 ZS Notebook (SB0350) and Audigy 4 Pro (SB0380) cards are partially supported.
The Dell OEM SB Live! (SB020x) is not yet supported since it uses a custom version of the EMU10k1, whose details are unknown. Experimental support may be provided when more information about it becomes available.
Soundblaster Live! 5.1 cards (SB022x) are supported.
Soundblaster Live! 24 Bit and Audigy LS are incompatible with kX, since they do not use the 10kX chips.

Audigy2 ZS Notebook is supported, although some limitations apply.
E-mu E-DSP based PCI devices are supported (0404, 1212, 1820, ...).
Extigy is NOT supported and will not be supported.
X-Fi is NOT supported and will not be supported.

Full list of supported boards can be found here, in our knowledgebase article.
Top
Q. Will there be support for the Creative Labs Extigy and Audigy2 NX?

A. The Extigy and Audigy2 NX cards are NOT 10k1/10k2-based card (most of their functionallity is software-based), and since they are USB audio devices they are not kX-compatible. However, we are currently working on ASIO drivers for these cards. In order to finish we will need test samples -- please donate to our kX Fund in order to help us to support both cards.

Top
Q. Under which Operating Systems can I use the kX driver?

A. The kX driver conforms to the WDM (Windows Driver Model) specification and is therefore compatible with the following Microsoft Windows operating systems: Windows XP, Windows 2000, Windows 98 (Second Edition only), and Windows Me. Windows Server 2003, Vista, Vista x64, Windows XP x64, Windows 7, Windows 7 x64 are supported. Windows 98 (First Edition) will not be supported since it has no built-in support for WDM drivers (v1.1 or later).
Mac OS X version is available on our support forums.

Top
Q. Why should I use the kX driver and not the drivers that came with my soundcard? What are the advantages of the kX Audio Driver?

A. The kX driver may or may not suit your own particular needs, although you have little to lose by giving it a try. The kX driver is part of an independent development project, and already offers most if not all of the same features included in the original manufacturers' drivers. In fact, the kX driver set is continually being updated and improved, with frequent driver and supporting application releases.

general advantages
smaller download / software takes up less space on disk
mixer is skinnable
API is open -- SDK, documentation and sample code available for download
skilled users can write their own effects and plugins
open API allows development of custom mixers and other software applications
better functionality
better DSP support [hardware-accelerated custom sound effects]
virtually unlimited signal routing possibilities
complete and flexible control over hardware (without artificially imposed limitations)
direct uninterpolated SPDIF recording from Optical, Coaxial and CDSPDIF sources
GSIF support
bit-to-bit 16/48 playback and recording (SPDIF, Audigy)
better ASIO support
ASIO is supported for all the 10k1 & 10k2-based boards
ASIO v2 based hosts are fully supported
better MIDI support
kX VSTi and kX Automation provide MIDI-based control of DSP effects
extended MIDI CC support
both SoundFont 2.01 & AWE NRPN support
Top
Q. Are the kX drivers aimed at musicians or gamers or both?

A. At present the kX driver is aimed primarily at musicians, and especially those who wish to get the most out of their soundcards (and who have traditionally been left behind by the big soundcard manufacturers, who prefer to concentrate their efforts on the more lucrative gamers market). Features designed specifically for gamers will however be added as development of the drivers continues.

Top
Q. Does the kX driver have ASIO support? ASIOv2?

A. ASIO v2.0 - based hosts are fully supported, however, some ASIO2 features are not implemented due to hardware limitations. 24-bit ASIO support is planned for 10k2-based boards.

Top
Q. What kind of latency can I expect to see?

A. The minimum expected ASIO latency is expected to be 5.33 ms (and possibly as low as 2.66 ms, depending on your hardware/software setup).

Top
Q. Will I get low latency with Cakewalk's Sonar?

A. The kX driver is a kernel-streaming WDM driver, and a latency as low as 10 ms can be expected under Sonar (depending on your hardware/software setup).

Top
Q. Does the kX driver incorporate DirectX support?

A. Currently, DirectSound2D and DirectSound3D are fully supported. DirectSound3D support is under constant development, however it can cause issues with some games. Any offers to help with implementing support for DirectSound3D would be gladly accepted (skilled programmers only please!).

Top
Q. Does the kX driver support multiple soundcards? How many?

A. Multiple soundcards are indeed supported by the kX driver. In theory, an unlimited number of soundcards could be used at once, but in reality you're likely to be limited by the number of PCI slots in your machine. Any combination of EMU10k1 and/or EMU10k2-based cards can be used with the kX driver (together with soundcards by other manufacturers, running their own drivers), provided the BIOS and the OS recognize the cards and assign the resources correctly.

Top
Q. Can I use SoundFonts with the kX driver?

A. Yes, your soundcard will continue to function as a SoundFont-compatible device under the kX driver. SoundFonts can be loaded and unloaded via SoundFont-aware applications, or via the kX Mixer's SoundFont control page. Currently only SF2 files are supported, however SF1 (SBK) files can be converted to SF2 files using a freely available utility.

Top
Q. Is there a SoundFont control panel included with the kX driver set?

A. Yes, the kX Mixer includes a SoundFont control panel, which allows loading and unloading of SoundFonts to compatible soundcards running under the kX drivers.

Top
Q. Can I use the Vienna SoundFont editor with the kX drivers?

A. The current kX driver version provides support for the Vienna SoundFont editor (with the exception of 'wave playback' feature).

Top
Q. Can I use the Alive SoundFont editor with the kX drivers?

A. The Alive editor is currently not fully compatible with the kX driver (improved support is under investigation -- please contact SoundFaction for details).

Top
Q. Is there a 32MB limit on sample playback? Does this apply to the Audigy as well?

A. SoundFont sample playback is limited to 32MB of wave data at one time, although SoundFonts larger than 32MB can be loaded.

Top
Q. Can I use the standard Windows Mixer with the kX driver?

A. Basic Windows Mixer functionality is provided, although the audio mixer (kX Mixer) included with the driver package allows access to many more features. The Windows mixer allows Master, Wave and Synth Playback and Record levels to be controlled. A Line-in slider has also been added for compatibilty with TV-card software.

Top
Q. Is there a dedicated mixer included with the kX driver set?

A. Yes, the kX driver package includes a feature-rich audio mixer, the kX Mixer.

Top
Q. What are the mixer features? Can I save and restore my mixer settings?

A. The kX mixer includes level controls for all inputs and outputs, full control over the AC97 Codec, separate record level controls, selectable digital output mode, etc., etc. The kX Mixer supports save, load and restore of all mixer settings.

Top
Q. Are DSP effects supported by the kX driver?

A. Yes, the kX driver supports DSP effects, with Reverb and Chorus loaded by default for MIDI Synth compatibility.

Top
Q. Is there an effects control panel included with the kX driver set?

A. The kX mixer includes a DSP control panel, allowing editing, loading, patching and unloading of custom DSP effects. A command-line utility is also included with the kX driver package, allowing direct access to many functions.

Top
Q. Are there new effects included with the kX driver set?

A. Yes, in fact all effects included with the kX driver package are new, custom-programmed DSP effects. Currently, Reverb Lite, Stereo Chorus, Delay, Overdrive, M4Tube (TubeSound), Chorus, AutoWah, CL Reverb, ProLogica, RingMod, Eq10a, APS Flanger, APS AutoWah, Stereo/Mono Vocoders, Overdrive2, Encode4, APS Fuzz, Stereo Mix, Mono Mix, Pan, Pan x2, EQ Bandpass, EQ Highpass, EQ Highshelf, EQ Lowpass, EQ Lowshelf, EQ Notch, EQ Peaking, Frequency Splitter and Timbre effects are included with the kX driver package (full list is available here); other effects will be available in the near future.

Top
Q. Can I write my own DSP effects for use with the kX driver set?

A. Yes, the kX driver package includes a DSP compiler and loader, allowing skilled users to program their own DSP effects.

Top
Q. Where can I get support for the kX Audio Driver?

A. The kX Forums have been set up to allow users to ask questions and exchange helpful tips and information with each other. kX developers and collaborators will sometimes drop in to answer questions, but on a limited basis (mainly due to time constraints :-P). Note that the kX Project email address should be used for Bug Reports and suggestions only - support questions will be referred to the kX Forums.

Top
Q. Why do I experience shutdown problems with the kX Mixer?

A. This is a known issue with Windows 2000 / Windows XP. See Microsoft support site for details. Windows 2000 users are advised to install the latest Service Pack - this has reportedly solved the shut-down problem for many kX users.

Top
Q. Why do I get 'Debug assertion failed' message (Expression 'SUCCEEDED(hr)&&gpPicture')?

A. This error indicates that your Internet Explorer installation is corrupted. In order to solve this, re-install Internet Explorer 5.0 or higher.

Top
Q. Why can't I load large SoundFonts?

A. This is caused by Windows memory management restrictions. Try tweaking the following register keys (for Windows 2000 and Windows XP only):

HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Session Manager\Memory Management\
PagedPoolSize
NonPagedPoolSize
NonPagedPoolQuota
PagedPoolQuota
Please search our forum and Microsoft Knowledge Base for details.
Setting PagedPoolSize to 0xffffffff may solve the issue. Review this link for details.
Top
Q. How do I tweak my computer for optimum performance?

A. Start by reading the following explanatory documents: W2k_XP_Optimize.pdf, pcopt.pdf and W2k_XP_Optimize.pdf.

Top
Q: My MIDI playback is crackling no matter what SoundFont I use - what should I do? I have VIA chipset and AMD processor.

A: If you are using any cooling software like VCool, CPUCool, CPUIdle, etc you need to disable it(in VCool you need to disable NB Cool Bit, in CPUIdle disable 'AMD hardware-specific' options).

Top
Q: Why is there no 'Wave 2/3' device?

A: 'Wave 0/1', 'Wave 4/5', 'Wave 6/7', 'Wave 8/9' are the only wave devices available for WinMM / DirectSound applications. They are routed to the corresponding FxBusses, that is, 'Wave 0/1' is routed to 'stereo' mix which goes to 'front' output by default, 'Wave 4/5' is routed to front only, 'Wave 6/7' is routed to rear only, 'Wave 8/9' is routed to center and subwoofer.
Read our Routing guide for details.

Top
Q: Why is my CT4830/SB0090/SB0220 recognized as CT4832/SB0092/SB0222?? Does this affect sound quality?

A: The CT4830 and CT4832 are almost identical cards with different PCI IDs (as programmed into the onboard EEPROM). A CT4832 card is generally an OEM version of the CT4830, although both cards might be marked as 'CT4830'. Neither kX Audio driver performance nor sound quality are affected by the way in which these cards are recognized by kX (the same applies to SB0090/SB0092 and SB0220/SB0222 cards).

Top
Q: Does kX support ASIO 2 Direct Monitoring?

A: When this option in the Audio System Setup dialog is activated, monitoring is handled by the actual audio hardware, that is, the monitored signal does not pass through Cubase VST. Instead, the ASIO driver for the audio hardware is instructed to send the audio from the monitored input directly back to a specified output, thus providing monitoring with practically no latency, i.e. ASIO2 Direct Monitoring simply provides zero latency monitoring of inputs. However, zero latency monitoring is already provided by kX ("direct monitoring" is enabled when you unmute an input on the kX Mixer's "Ins'n'Outs" page), so there is no reason to tax your CPU with ASIO2 direct Monitoring. Contrary to what many people believe, ASIO direct monitoring does not allow monitoring of the incoming signal with VST effects; it only provides monitoring of the dry input signal. In other words, this means that the only thing missing without ASIO2 "direct monitoring" in kX is the lack of direct control from Cubase (or other ASIO host) over hardware pan/level/peakmeter for unprocessed dry signal, although even these can be controlled via the kX Mixer. And of course you can always apply VST/DirectX plug-ins to as many input channels as you want using the kX ASIO driver.

Top
Q:Why cannot kX Mixer find kxskin.kxs file, although it is in the same folder?

A: You should not try executing kX Mixer from the folder you have manually copied it to. kX Mixer should be installed into your Windows/System32 folder by the setup application. Do not try to install it manually - simply re-run the installation program.
Top
Q:After installing kX Driver I cannot hear anything. Why?

A: Before you can enjoy the sound quality offered by the kX Audio driver you need to make sure it is configured correctly. For example, Front and Rear outputs are swapped by default -- make sure you have your speakers plugged into the 'Rear' jack, or disable the swap on the 'Master' page of the kX Mixer. If you have more than 2 speakers (4.0/4.1 or 5.0/5.1 speaker set) - set the desired configuration in the 'Surrounder' window (you can access it via 'Effects' submenu or by clicking the 'Surrounder' button on the main page of the kX Mixer).
Top
Q:Why do I hear audio feedback when using NetMeeting? How do I turn off the recording feedback?

A: kX Audio driver enables 'What you hear' recording mode by default. In order to turn it off, open the kX Mixer, and set Wave and Synth recording levels to the appropriate values on the 'Recording' page.
Top
Q:Why do I experience clicks and audio artifacts in games?

A: Our 3-D Engine is under constant development and might be not 100% compatible with certain games. In order to avoid audio artifacts either disable hardware acceleration in your game or select 'Wave 4/5' as your preferred device.
Top
Q:Why my audio application doesn't detect any ASIO inputs?

A: Select 48000 sampling rate. Due to hardware limitations, the recording functionality is available for this sampling rate only.
Top
Q:How to get quadrophonic MIDI out of an SBLive with SoundFonts using VMM?

A: Please follow this link.
Top
Q:How to setup an SBLive for quadraphonic audio playback?

A: Please follow this link.
Top
Q:Why cannot I hear any sound when using GigaStudio / GigaSampler?

A: kX Audio Driver fully supports GSIF specification. There are currently two GSIF driver sub-sets: VxD and WDM-based. Since kX Audio Driver is a WDM driver, it supports WDM GSIF only. Under certain circumstances, this causes certain compatibility problems with GSIF-aware applications (such as GigaStudio and GigaSampler), especially under Windows 9x / Millenium. Please upgrade your Giga application (and install any patches available from Tascam). If this doesn't solve your problem, the solution is either install Windows 2000 / Windows XP or use the original Creative VxD drivers.
Top
Q:Where can I find additional information?

A: The main sources of information:

kX Help file (also available online)
Additional documentation and articles
kX Forums
kX knowledgebase
GitHub kX documentation
Additinal links

Top
Q: Does kX Driver support SB Live! 24 Bit, Extigy, Audigy2 NX, Audigy LS, USB, Firewire or AC97 audio hardware?

A: NO. These cards are not compatible and there will be NO support for them.

Top
Q: Where can I find the latest version?

A: The latest stable release can be found on the Downloads page.
If you are looking for the latest beta version, these releases are posted on the kX Forums. It is only recommended for experienced users to try these experimental releases.

Top
Q: Everything is ok, but I have only one problem, using "Master Mixer" I have some crakles/popes sometimes. Why?

A: This is a known issue with Windows 7 and later. Right click on KX manager, choose 'Settings', 'Setup Buffers'. Increase second one to 10.00ms (or more if needed).

Top
Q: ASIO does not work on Windows 8

Q: kX Mixer does not remember its settings after reboot on Windows 8

A: The problem is caused by UAC (User Access Control) feature of WIndows 8, and possible bugs in kX driver installer. Please visit our support forum for details. You may need to register manually ASIO DLL and fix some registry entries.
