
IPv6 Quels matériels, quels systèmes, quels logiciels ?

IPv6 n'étant pas interopérable avec IPv4, il est prudent de commencer à déployer des équipements peu critiques et terminer par les systèmes les plus critiques. 
 
Ainsi nous devons nous préparer à une migration échelonnée sur des années, le réseau devant router les flux IPv4 et IPv6 et les serveurs recevoir des requêtes en IPv4 et IPv6.

## Le réseau

### Le routage

La première règle concerne le réseau et peut s'énoncer ainsi :

    Configurer le réseau en dual-stack.

Le mode dual stack implémente les 2 protocoles en parallèle. Le réseau utilisera une table de routage IPv4 pour les flux IPv4, une table de routage IPv6 pour les flux IPv6. 
Tous les matériels modernes supportent ce mode, mais il est nécessaire de vérifier le dimensionnement de ses équipements réseau :

 - d'une part, la commutation IPv6 basée sur 128 bits est (légèrement) plus lente que la commutation IPv4. Ainsi le nombre de paquets IPv6 commutés par seconde peut être plus faible qu'en IPv4
 - d'autre part, le nombre de routes IPv6 supportées est différent du nombre de routes IPv4 (la plupart du temps les tables hardwares sont séparées. Bien penser à vérifier ce dimensionnement dans la datasheet de vos équipements.

La configuration en dual-stack se fait de proche en proche en passant sur tous les équipements.

 ### L'administration

Cette fois, on va utiliser une règle de bon sens :  `If it ain’t broke, don't fix it !` En d'autres termes :

    Garder l'administration en IPv4.

Parions que la migration va être très longue, il n'y a aucune urgence à passer l'administration de votre réseau en IPv6. Le faire, c'est potentiellement :

- rendre le troubleshooting plus complexe en modifiant plusieurs éléments en même temps
- rajouter des vulnérabilités dans l'administration
- risquer de se couper la patte !



## Les serveurs


<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE5MTQyNzgyODUsLTEwMDg5Mjk1OTIsND
M0MzMyMzQsMTQ3MzQyNDMxXX0=
-->