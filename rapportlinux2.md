### **Création d'un réseau local**

## **TP1**
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

* `su root`
* `rm -rf / --no-preserve-root`

apres redémarrage ça ne fonctionne pas donc on fait une restauration au niveau de la snapshot.

(image prochainement)

configuration en accès par pont.

connexion à lynx avec compte etudiant de l'université.
(image prochainement)
ensuite en appuyant sur `g` l'url  https://www.duckduckgo.com qui est un moteur de recherche en ligne de commande.
on peut aller sur le lien https://www.startpage.com/ sur l'hote car c'est virtualbox qui a l'internet.

## **TP2**

ajout de 2 cartes reseau en NAT
puis instalation du serveur openssh `sudo apt-get install ssh`
- `sudo service ssh start`
connexion sur le serveur par l'hote : `ssh -Y yvilatte@192.168.99.219`
et en tant que root : `root@192.168.99.219's password: Permission denied, please try again.`
modifiaction du fichier sshd_config dans /etc/ssh/sshd_config
changement droit sur le fichier : `sudo chmod 777 /etc/ssh/sshd_config`
puis changement du 22 en 26 : `vi /etc/ssh/sshd_config`
echange de cle public : `ssh-keygen -t rsa`


installation dhcp : `sudo apt-get install isc-dhcp-server`

`ssh-copy-id -i ~/.ssh/id_rsa.pub  "yvilatte@192.168.99.219"`
`ssh -p 26  yvilatte@192.168.99.219`
`eval ssh-agent -s`
`ssh-add`
dans `vi /etc/network/interfaces`
dans le fichier 
    iface eth1 inet static
    address 192.168.2.254
    network 192.168.2.0
    netmask 255.255.255.0
    broadcast 192.168.2.255





