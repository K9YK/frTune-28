# frTune-28
frTune-28 is a small application that allows an Icom RC-28 controller to be used with FlexRadio SmartSDR

frTune-28 uses the Flex API and works over the local network (it does not have SmartLink/remote connectivity yet, however you could connect it over a VPN).

Note:  It is advised that you should make sure to connect your RC-28 to your computer, and that Windows recognizes it, before you start frTune-28 for the first time.

Download latest release:
 - Windows:   https://github.com/K9YK/frTune-28/releases/download/v2.2.2-Windows/frTune-28.Setup.v2.2.2.-.Windows.exe

Suggestion:  You can just leave frTune-28 running all the time on your PC (minimized).  It will automatically connect and transparently control tuning whenever you have SmartSDR running. 

Settings:
 - Station Name: This is the name of the station instance that you want your RC-28 to work with.  Your station name is displayed at the bottom middle of your SmartSDR window.
 - Radio: If your FlexRadio is on the same subnet as your computer running SmartSDR, your radio should appear in the drop-down (uses Flex Discovery).  You also have the option to manually specify the IP address of your radio.
 - Radio IP:  Automatically displays the IP address of your radio if you select it from the Radio drop-down, or you can enter your radio's IP address if you selected Manual in the Radio drop-down
 - Enable Snap Tuning: When enabled, your radio will automatically tune to the nearest even 1KHz when you cick with your mouse to tune in the panadapter.  Most QSO's take place on an even KHz and this makes tuning by clicking with your mouse much faster. 

Controller Functions:
 - The Link LED will flash green when the app is running, but your specified station is NOT connected to the radio. The Link LED will light solid green when the app is running and your specified station IS connected to your radio.
 - The F1 button changes between fast and slow tuning rates. Press and hold to lock the tuning dial. The F1 LED will blink when the dial is locked. Press and hold again to unlock the tuning dial.
 - The F2 button switches between normal tuning and RIT. Press and hold F2 to reset RIT tuning back to zero.
 - The transmit button puts your radio into transmit for the station specified in the settings.
 - The 'Snap Tuning' feature will automatically tune your radio to the nearest 1Khz tuning step when you click to tune with your mouse in the panadapter. Since most QSOs typically take place on an even Khz, this makes clicking to tune a lot faster. You can of course disable snap tuning in the settings.  Snap Tuning will work with any station connected to your radio.

Version History:
  Version 2.2.2 - 12/19/2025
   - fixed a bug that prevented Flex stations with a space character in the name from being recognized
  Version 2.2.1 - 12/12/2025
   - now uses Flex Discovery in the settings window to allow selection of a radio on the local network
   - updates/fixes for the Mac version
  Version 2.1.1 - 12/6/2025
   - updated core Flex libraries 
   - now handles up to 8 slices (Flex 6700)
   - minor client handling bug fixes
  Version 2.0.6 - 6/12/2025
   - Adjusted settings window size
   - Now saves the main window location in the config file on shutdown
   - Added application icon
     
