
Préparer une migration en IPv6

Ce nouveau cycle de présentation est là pour échanger autour des best practices pour la mise en place d'un plan d'adressage IPv6 au sein d'une organisation (entreprise, établissement public, ...). Il suppose que vous êtes déjà familier avec le format IPv6

## Pourquoi passer à IPv6 ?
sous-titre: quel problème IPv6 prétend résoudre ?

IPv4 est victime de son succès et les adresses publiques autorisées par le protocole ont été entièrement attribuées. Il est possible de racheter des adresses déjà attribuées pour un prix de l'ordre de [25$ par adresse](https://auctions.ipv4.global/).

IPv6 en utilisant un format d'adresse en 128 bits au lieu de 32 bits pour IPv4 permet d'allouer en nombre d'adresses à peu près illimité ([avec un adressage sur 150 bits, on peut adresser chaque atome de la terre](https://fr.wikipedia.org/wiki/Ordres_de_grandeur_de_nombres#1039_%C3%A0_10100)). 

2 mécanismes nous permettent quand même de continuer à vivre avec IPv4 :
 - Les adresses privées, non routées sur Internet,  qui peuvent être utilisées parallèlement  par plusieurs organisations 
 - Le NAT qui permet de translater un subnet d'adresses privées vers une seule adresse publique 
  
Ainsi, en pratique, la plupart des organisations utilise le réseau privé 10.0.0.0/8 et ne s'estime pas encore concerné par  IPv6. De plus, tous les opérateurs Internet grand public regroupent les réseaux personnels (home network) sur une seule adresse IP (NAT), et certains regroupent même plusieurs 

Toutefois, l'arrivée d'objets connectés (caméras vidéo, bornes wifi, étiquettes connectées dans la distribution ...) augmente le nombre de subnets à attribuer et bouscule le plan d'adressage des entreprises. 

Grâce à un plan d'adressage plus large, IPv6 permet de répondre à cette demande. 


La seule alternative possible à IPv4 s'appelle IPv6. En d'autres termes, la seule décision que nous avons, c'est **quand** nous allons passer à IPv6 ! En effet, il a fallu près de 15 ans pour stabiliser et sécuriser IPv6, il n'est pas crédible d'attendre un autre protocole de transport. 




De plus, ces subnets souvent peu critiques sont des bons candidats pour une première expérience en IPv6.
 


> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTM3NzIyOTIyNCwtMTM2Mjk4NjQzNywtMz
Y4ODIwMTQyLDcwNTI0NzAxMiw2MjkyNDI5MzcsMTAyNTM1NzQ4
NCwxMzk1NzQzMTE3XX0=
-->