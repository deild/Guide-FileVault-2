# Utiliser DestroyFVKeyOnStandBy pour démolir la clé de cryptage lorsque vous passez en mode veille

## Mesure de précaution secondaire : Empêchez l'attaquant avec accès physique à l'ordinateur macOS crypté avec FileVault 2 de prendre votre clé de cryptage en mode veille

Si vous craignez toujours qu'un pirate puisse s'emparer de votre clé de cryptage depuis la RAM en mode veille, vous pouvez utiliser une fonction de gestion de l'alimentation dans macOS appelée "**DestroyFVKeyOnStandby**".

"**Détruire une clé FVFVKeyOnStandBy**" démolit essentiellement la clé de cryptage FileVault lorsque vous passez en mode veille.
**Modification des options de sommeil à l'aide de la commande "pmset"**

Deux options de sommeil sont disponibles pour le réglage :

| Option                | Valeur | Description                                                                                                                                |
| --------------------- | ------ | -----------------------------------------------------------------------------------------------------------------------------------------: |
| destroyfvkeyonstandby | 1      | Élimine de la mémoire la clé de cryptage de tout volume lorsque l'ordinateur est mis en veille et dépend de la valeur du mode hibernation. |
| hibernatemode         | 25     | Oblige l'ordinateur à écrire instantanément de la mémoire sur le disque et élimine également l'alimentation de la mémoire en mode veille.  |

La commande à taper dans le Terminal **en tant qu'utilisateur root** est : `sudo pmset -a destroyfvkeyonstandby 1`

La commande ci-dessus permettra la démolition de la clé FileVault en mode veille pour chaque mode d'alimentation **-a**. \(Chargeur **-c**, Batterie **-b**, et UPS **-u**.\)

Vous pouvez également choisir de taper dans le Terminal **en tant qu'utilisateur root** : `sudo pmset -a destroyfvkeyonstandby 1 hibernatemode 25`

