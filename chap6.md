## De quoi macOS et FileVault 2 ne peut pas protéger l'utilisateur

### Attaques de démarrage à froid

macOS et FileVault 2 ne peuvent pas se défendre contre les attaques démarrage à froid (Cold Boot). En effet, les clés de cryptage sont stockées en mémoire lorsque la machine est sous tension. Par exemple, au moment où vous avez entré votre mot de passe au démarrage. Ce problème de sécurité ne se limite pas au chiffrement complet du disque FileVault 2, mais à tous les autres outils logiciels de chiffrement complet du disque. Ainsi, il n'y a pas de logiciel défensif publiquement reconnu contre les attaques de démarrage à froid.

**Pour des raisons de sécurité et de confidentialité, éteignez complètement l'ordinateur lorsque vous n'avez pas l'intention de l'utiliser.**

![guide-to-encrypting-mac-os-x-with-filevault-sixteen](/assets/guide-to-encrypting-mac-os-x-with-filevault-sixteen.jpg)
