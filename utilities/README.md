# Tools For Lenovo T440 Hackintosh Setup

This folder contains a number of different useful tools I find helpful with setting up the full macOS system on the Lenovo ThinkPad T440 Ultrabook. You may not find them useful but they're here for anyone to checkout and use if they want.

#

### Audio Configuration

- Contains 2 separate methods for successfully getting proper system audio functionality with with this configuration. (Credit JCSNIDER for ALC3232 Method and ACIDANTHERA for AppleALC Lilu Plugin)

#

### BIOS Folder

- Contains pictures which show the proper BIOS settings required for the system to boot properly. Anything that show "Permanently Disabled" as an option can be substituted by the "Disable" action instead if you would rather have the option to utilize the features down the road.

#

### HomeEndFix

- Fixes the Home and End button configurations on ThinkPad Hackintosh setups to match Macintosh hardware in the macOS environment.

#

### Hot Patching

- All of sniiki's current files used for HotPatching Lenovo ThinkPad T440 and a bunch of other ".dsl" files which can be used as well. 

#

### maciASL Patches

-  Collection of different maciASL patches for static patching hackintosh DSDT configurations depending on your current pc hardware setup. This folder has plenty of different patches for plenty of different hardware setups, not just Lenovo ThinkPads, however ThinkPads have a designated section specifically for them. Use these patches in conjunction with maciASL to fix errors with your DSDT if you choose to patch your DSDT yourself over going with a precompiled Hot Patch configuration if one exists for your hardware.

#

### Permissions

- Utility for fixing all permissions including kext and other. Run this if you're having issues with kext permissions or if you just want to repair you permissions easily. (Credit insanelyi.com for this script).

#

### ssdtPRGen

- Script for creating a custom SSDT.aml file for your hardware in order to have a functional power configuration for your processor. (Credit goes to Piker for creating this script).

#

### Tools

- Different folders for different purposes like installing useful binaries to the /usr/local/bin folder which can be very helpful with Hackintosh computers. 

#

### TrackPad

- Contains different TrackPad configuration options including VoodooPS2Controller, ApplePS2SmartTouchPad, a Preference Pane for extra trackpad control which works with both Voodoo and ApplePS2 setups. Also includes a way for people who have installed the Lenovo T440 TrackPad Synaptic UltraNav ClickPad to automatically remove VoodooController and associated files and replaces them with ApplePs2SmartTouchPad and it's files.

#

# Command Scripts

### !clover_scripts.command

- Installs the clover startup scripts and daemons found inside of the "Tools/Library/" folder present which is part of the utilities folder. The purpose of these scripts is to ensure Clover services startup at boot when the OS loads. Also is key for the startup of the Clover Preference Pane services and update settings in system settings. Also installs the RC Scripts found in "Tools/etc/" folder.

#

### !gatekeeper.command

- Disables macOS Gatekeeper configuration. Gatekeeper is a fail safe program which is built in to macOS with the purpose of preventing the possibility of third party apps from loading up when they are executed normally by double clicking their respective icons. Instead you must right click the icon and select open from the context menu which will then allow the app to load. This script disables that and allows the normal execution of all applications no matter where they come from.

#

### !homefix.command

- Installs the HomeEndFix files automatically. Fixes the Home and End button configurations on ThinkPad Hackintosh setups to match Macintosh hardware in the macOS environment.

#

### !install_tools.command

- Installs binaries and other tools for hackintosh builds which can be found in the "Tools/usr/" directory and they include a number of different binary apps which can. be executed from the terminal including "patchmatic", "iasl", "lscpi", "gfxutil", "hda-verb", "plistbuddy", "mnt", "sleepwatcher", and a number of other useful tools which are beneficial in setting up a fully working system with the proper tools needed to keep things running smooth. Just execute this script and enter the password for your account and the binaries will be installed to "/usr/local/bin/" folder automatically.  

#

### !kextcache.command

- Repairs and rebuilds kextcache and system kext permissions in "/System/Library/Extensions/" and "/Library/Extensions/" folders respectively. This is helpful if you've install a kernel extension (kext) file yourself by copying and pasting the file directly in to one of these folders as it requires the proper permissions be in place for all system kexts and so this script ensures that the kexts in those folders are all properly configured with the correct permission levels and then it rebuilds the systems kextcache which will allow any new kext files to load correctly upon rebooting the system.

#

### !sleepwatcher.command

- Installs sleepwatcher commands which looks out for the systems configurations before entering sleep mode in order to make some quick changes just before it takes place which allows certain hardware to still be present and useable upon waking up the system following the sleep mode being activated automatically.

