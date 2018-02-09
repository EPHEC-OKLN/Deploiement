# Tâches réalisées

Au départ , nous avons configuré les Raids sur les deux serveurs  (le grand et le petit) et installé un Vmware ESXI sur les deux: Grand (voir les caractéristiques) et un petit ( Voir les caractéristiques).

 ## Sur le petit serveur 

Nous avons installé du pfSense,debian

- Configurer des vSwitch : 

  wan  ,
  
  dmz , 
  
  web-db  

- Configurer leurs ports groups : 
 
 uz-group,
  
  management Network,
  
  wan-group,
  
  dmz-group,
  
  web-db


## Sur le grand serveur 

nous avons effectué  l': 

  Installation d'un Windows Servers 2016 de base dans le HDD
  
  Installations des 3 autres  à  partir de celui de base dans la SDD:
 
      Windows servers_AD
 
      Windows Servers_Exchange
 
      Windows Servers_deploy 
 
      Windows Servers File
 
Réunitialisation  des copies 
 
Configuration de chaque machine virtuelle  ainsi que l'attribution des adresses IP  

Activation du  DHCP 
  
Installation Debian de base  qui sera dupliqué pour une autre machine  debian-Proxy 

Activation du DNS 

ensuite , nous avons fait les Modifications des hostnames sur les serveurs  web, DB , RP et  suite à un problème rencontré 

nous avons réinstallé  à nouveau des serveurs de déploiement, Exchange,AD.


# Problèmes rencontrés (énoncé du problème + solution)

Durant le déploiement, voici les problèmes rencontrés:

- Le mapping du clavier dû à l'ESXI avec debian 

- deployement d'une vm debian configurer depuis worstation

-le  swapping des fichiers

- Disfonctionnement de tout les serveus windows dupliqués(SSID failed) après le changement de nom de domaine (syspre qui ne fonctionne pas) =>  nous avons opté de supprimer tout les serveurs windows dupliqués et  réinstaller à nouveau les serveurs .
 

# Motivations des technologies/infrastructures utilisées

On a choisit un hyperviseur afin d'installer plusieurs os sur la même machine et les isoler entre eux.

Nous avons fait le choix de ESXI pour sa simplicitée et notre bonne connaissance de celui-ci

pfsense : pour le firewall

debian = pour différents services

# Remarques éventuelles

# Sources (Important !)
https://techmikeny.com/h700-array-guide
https://kb.vmware.com/s/article/1027876
https://technique.arscenic.org/reseau/article/noms-d-hote-hostname-et-noms-de

