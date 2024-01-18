
# NAS maison

### ✅Checklist

```bash
    Installer la VM NAS, et vérifier que les disques dur sont bien détectés ✅  
    Installer TrueNAS sur la VM NAS  ✅
    Mettre en place un RAID ZFS avec les trois disques  ✅
    Rendre disponible ce RAID sur le réseau avec un partage réseau  ✅
    Mettre des fichiers sur les disques  ✅
    Accéder au partage réseau via la machine Linux et le protocole NFS  ✅
```

## premier pas 

j'ai prit un main l'os truenas 
surtout lire la doc 

## Premier setup 

j'ai commence a partager des fichier via la carte Hostonly sur mon reseaux virtuelle via le protocle NFS sans aucun setup particulier

## NAS PHYSIQUE

j'avais un vieux nas a la maison qui par contre marche VIA l'os Synology je l'ai configuré pour crée un grand repertoire  
 j'y est transféré toutes les photo/video/autres document dans la nas  
 j'ai ensuite configuré le nas pour que crée un compte admin et deux compte utilisateur  
    -le compte admin (c'est l'admin)
    -le compte membrefamille (qui ne peut acceder au pannel de gestion il a seulement acces au repertoire il peut ajouter et supprimer des données)
    -le compte Invité (qui n'acces que au repertoire FILM il peut juste telechargé il ne peut rien upload)
le partage de repertoire est configuré pour fonctionné avec linux max et windows

## le DRAME

Ayant decouvert l'outils gns3 j'ai eu envie d'integré un nas a un petit reseaux gns3

Le reseaux etait configuré avec un setup router on the stick classique avec 3 VLAN 10 Serveur 20 client 30 admin  
il y avait :
    -1 dns config pour client admin est serveur 
    -1 router relié a internet
    -2 switch 
    -2 client
    -1 admin sous KALI
    -la vm true nas
la vm etait config : pour donner un acces au repertoire DB quand la requetes venait de la VLAN Serveur  
et donné acces au repertoire DOC quand la requetes venait du VLAN 20 et les admin ont les logs admin donc pas de conf particuliere dessus 
j'etait en train de setup un systeme de rapport de logs qui envoyé ca sur un machine qui n'a put etre integeré avant le drame  

c'est quoi le drame ?? et bien juste avant de partir en vacance EN installant WAMP pire erreur de ma vie mon disque dur a rendu l'ame j'ai perdue l'ensemble de mon travail sur ce TP si on exclue le NAS chez moi car je n'avais pas fait de save ailleurs (ca ma bien servit de lecon au passage )