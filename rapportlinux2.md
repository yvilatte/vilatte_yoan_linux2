## **Création d'un réseau local**
----------
Lors du premier démarrage de votre invité (la VM qui est exécuté sur l'hôte), vous allez installer les
logiciels suivants : donc on passe sous su root

* `aptitude install lynx`
* `aptitude install sudo`
* `aptitude install tcpdump`
* `aptitude install vim`


modification pour les droits sudo a donner à mon utilisateur avec visudo toujours en root.

#**Clonage**

ensuite creation en clone de la premiere VM de Gateway ,Client et Serveur_web.

#**Snapshot**

(image prochainement)

`su root`
`rm -rf / --no-preserve-root`

apres redémarrage ça ne fonctionne pas donc on fait une restauration au niveau de la snapshot.

(image prochainement)

