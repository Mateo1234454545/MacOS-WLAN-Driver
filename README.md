# MacOS-WLAN-Driver
--------------------
Change your WLAN country code.

Compatible with MacOS X Mojave.

802.11d WLAN country code:
--------------------------

- all channels available

- beamforming enabled

- 80mhz enabled on all 5ghz channels

- 1000mw max tx power


MacOS (>=10.14.4):
--------------------------
Use Modded 10.14.3 'IO80211Family.kext':

https://github.com/alessandro893/MacOS-WLAN-Driver/tree/master/AirPortBrcm4360/10.14.3

MacOS (10.13-10.14.3):
--------------------------

1.

Disable 'System Integrity Protection' (csrutil disable)


2. 

Run in terminal:

US (United States) country code:
--------------------------
sudo perl -pi -e 's|\x41\x83\xFC\xFF\x74\x35\x48\x8D\x55\xD0|\x66\xC7\x06\x55\x53\xEB\x34\x8D\x55\xD0|' /System/Library/Extensions/IO80211Family.kext/Contents/PlugIns/AirPortBrcmNIC.kext/Contents/MacOS/AirPortBrcmNIC


3.

Rebuild Caches (run Kext Utility.app)
