
IPv6 Quels matériels, quels systèmes, quels logiciels ?

IPv6 n'étant pas interopérable avec IPv4, il est prudent de commencer à déployer des équipements peu critiques et terminer par les systèmes les plus critiques. 
 
Ainsi nous devons nous préparer à une migration échelonnée sur des années, le réseau devant router les flux IPv4 et IPv6 et les serveurs recevoir des requêtes en IPv4 et IPv6.

## Le réseau

La première règle concerne le réseau et peut s'énoncer ainsi :

> Faire fonctionner le réseau en dual-stack.

Le mode dual stack implémente les 2 protocoles en parallèle. Le réseau utilisera une table de routage IPv4 pour les flux IPv4, une table de routage IPv6 pour les flux IPv6. 
Tous les matériels modernes supportent ce mode, mais il est nécessaire de vérifier le dimensionnement de ses équipements réseau.
 
Cela impose une plus grande consommation de ressources sur les routeurs et il faudra 

> 
> Written with [StackEdit](https://stackedit.io/).

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTU3MTMxMTUwOV19
-->