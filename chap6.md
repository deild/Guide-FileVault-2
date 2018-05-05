### Secondary Precautionary Measure: Prevent Attacker With Physical Access To FileVault 2 Encrypted OS X Computer From Taking Your Encryption Key In StandBy Mode

If you are still concerned that an attacker can grab your encryption key from RAM during standby, you may make use of a power management feature in OS X named “**DestroyFVKeyOnStandby**“.

“**DestroyFVKeyOnStandBy**” essentially demolishes the FileVault encryption key when proceeding into standby mode.  
**Altering Sleep Options Using The “pmset” Command.**

There are two sleep options available for adjusting:

| Option | Value | Description |
| --- | --- | ---: |
| destroyfvkeyonstandby | 1 | Eliminates the full volume encryption key from memory when the computer is put to sleep and is reliant on the value of hibernate mode. |
| hibernatemode | 25 | Compels the computer to instantly write memory to disk and also eliminates power from memory upon sleep mode. |

The command to type into Terminal **as the root user** is: `sudo pmset -a destroyfvkeyonstandby 1`

The above command will permit the demolition of the FileVault key in standby mode for every **-a** power mode. \(Charger **-c**, Battery **-b**, and UPS **-u**.\)

You may also choose to type into Terminal as the root user: `sudo pmset -a destroyfvkeyonstandby 1 hibernatemode 25`

