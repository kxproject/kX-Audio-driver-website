## Issues

# General

Front and Rear speakers are swapped by default (this is intentional) - explanation why here.
The default speaker configuration is 'Stereo' (2.0) -- you can change this setting by tweaking the 'Surrounder' options.
EAX/EAX2.0/EAX3.0 not fully supported.
MIDI synth volume control may not function in realtime.
If you have ACPI-aware system you may need to disable it. Refer to ACPI guide for details.
You may experience certain audio artifacts in 3-D games - in order to solve this issue select 'Wave 4/5' device as default or turn off hardware acceleration in your application.
Certain hardware configurations can cause constant beeping instead of sound - please review our forum for details.
SoundFonts

Maximum single sample size for SoundFonts may be limited by OS memory settings. Review our FAQ for details
Hardware-Dependent

Settings for phases, levels, etc. may not be optimized for uncommon AC97 codec versions.
SB006x / SB010x cards have an issue with ASIO input and output mappings that can't be fixed (a hardware problem).
SB020x cards (Dell OEM SB Live!) contain different EMU10k1 chips and they aren't supported at the moment.
OS-Dependent

Special adjustment of control panel settings may be required for Win2k (refer to installation guide).
There might be phantom CD-Audio and Wave controls in the Windows Mixer.
The system might fail to go into Stand-by / Suspend modes based on inactivity timer.
Media players may hang if the PC is resumed from a StandBy/Suspend modes with audio files being played.
Windows 98 and Windows ME users may experience problem with additional '-6dB' attenuation. Use 'Wave 8/9' device in order to fix this.
It is highly recommended you do NOT use Windows Mixer (sndvol32) application and tweak the volume only via the kX Mixer.
Other Software

Use of optional third-party skins may cause resource leakage.
Some DVD Players may fail to change the volume when playing AC-3 or multichannel content.
Some TV-Tuner software (e.g. from ATI) may conflict with the kX Audio Driver. See ATI support site for details.
You may experience shutdown problems. See Microsoft support site for details.
When playing back AC-3 content using kX Driver decoder or in 'AC-3 Passthru' mode, the volume control is not available.
