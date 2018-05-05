## Using A Firmware Password On OS X For Security

### Purpose In Enabling A Firmware Password On OS X

Systems that run OS X can deploy a password for locking OS firmware settings and thwarting inadvertent alterations on firmware situated in a particular system.

The firmware password is recommended for thwarting motivated adversaries from booting from a different system volume, internal or external storage device other than the initial startup disk you’ve chosen.

Notably, utilizing a firmware password thwarts deployment of catch keys to change the cascade of the boot process. Hence, a firmware password obstructs users who don’t possess the password from booting up from any disk other than your chosen startup disk which also prevents the capability to deploy the bulk of startup key combinations.

Furthermore, the firmware password is deployed to impede Direct Memory Access \(DMA\) through interfaces like FireWire. Remember that Target Disk Mode insists on DMA which a firmware password additionally forestalls its utilization on a system. If an adversary tries to mount a volume from an alternative computer that deploys Target Disk Mode, the firmware password has to be entered prior to mounting the volume from the target’s computer.

### How To Set A Firmware Password On An OS X System

* Boot into the macOS built-in recovery system by holding down Command \(⌘\)-R immediately after turning on your Mac via the power button.
* The macOS Recovery utilities window will appear. From the menu bar, click on Utilities &gt; Firmware Password Utility.
* Click “Turn On Firmware Password.”
* Enter a firmware password that is strong and complex. Use a combination of words, symbols, and letters. Click “Set Password.” Memorize this password.
* You may now exit the Firmware Password Utility. Restart Your Mac by clicking on the \(\) menu &gt; Restart.

### How To Know If Firmware Password Is Working As Intended On OS X

The OS X system will request for the firmware password when the user tries to start up from a storage device other than the one chosen in Startup Disk preferences or when booting up from macOS Recovery.

You’ll see something like this:

![](/assets/guide-to-encrypting-mac-os-x-with-filevault-eight.png)

