
Adresser une organisation en IPv6 : les best practices

Ce nouveau cycle de présentation est là pour échanger autour des best practices relatives à la mise en place d'un plan d'adressage IPv6 au sein d'une organisation (entreprise, établissement public, ...). Il s'adresse à un public familiarisé avec le format IPv6.


## Les limitations d'IPv4 ?
sous-titre: quels problèmes IPv6 prétend résoudre ?

IPv4 est victime de son succès et les adresses publiques autorisées par le protocole ont été entièrement attribuées. Il est possible de racheter des adresses déjà attribuées pour un prix de l'ordre de [25$ par adresse](https://auctions.ipv4.global/).

IPv6 en utilisant un format d'adresse en 128 bits au lieu de 32 bits pour IPv4 permet d'allouer un nombre d'adresses en apparence illimité ([150 bits permettent de compter les atomes de la terre](https://fr.wikipedia.org/wiki/Ordres_de_grandeur_de_nombres#1039_%C3%A0_10100)). 

2 mécanismes nous permettent quand même de continuer à vivre avec IPv4 :
 - Les adresses privées, non routées sur Internet,  qui peuvent être utilisées conjointement  par plusieurs organisations 
 - Le NAT qui permet de translater un subnet d'adresses privées vers une seule adresse publique 
  
Ainsi, en pratique, la plupart des organisations utilise le réseau privé 10.0.0.0/8 et ne s'estime pas encore concerné par  IPv6. De plus, tous les opérateurs Internet grand public regroupent les réseaux personnels (home network) sur une seule adresse IP (NAT), et certains regroupent un grand de réseaux personnels sur un nombre réduit d'adresses publiques (large scale NAT). 

Si ces 2 mécanismes permettent effectivement d'économiser les adres
La seule alternative possible à IPv4 s'appelle IPv6. En d'autres termes, la seule décision que nous avons, c'est quand nous allons passer à IPv6 ! En effet, il a fallu près de 15 ans pour stabiliser et sécurisesr IPv46, ils ne répondent pas efficacement à certains usages :
- fusion d'organisations partageant les mêmes adresses en 10.0.0.0/8
- accessibilité de serveurs dont l'adresse est translatée

Nous allons voir qu'IPv6, construit à partir  du retour d'expérience IPv4, apporte des réponses concrètes à ces deux points.

De plu'est pas crédible d'attendre un autre protocole de transport. 

En pratique, la plupart des entreprises utilise le réseau 10.0.0.0/8 et ne s'estime pas encore concerné par  IPv6.

Toutefois, l'arrivée des objets connectés dans les entreprises (caméras vidéo, bornes wifi, étiquettes connectées dans la distribution, capteurs connectés dans les entrepôts, les locaux techniquese IPv, il ns, les véhicules, ...) augmente la demande nombre des subnets à attribuer et bouscule le plan d'adressage des organisations. 
Il ne s'agit plus d'affecter une adresse IP par employé, mais de gérer des ensembles d'objets en nombre difficilement prévisible qui doivent appartenir à des nouveaux subnets pour leur adjoindre le bon niveau de sécurité (côté sécurité, c'est cool  de distinguer facilement un humain d'un interrupteur).

IPv6 est une réponse satisfaisante à ces nouveaux usages. De plus, ces subnets souvent peu critiques sont d'excellents candidats pour une première expérience en IPv6. D'autant plus qu'en configurant ces équipements en IPv6 dès le début, on s'évite une phase de migration ultérieure. 


## Pourquoi IPv6 ?

Parce qu'on n'a pas le choix : 

> la seule alternative à IPv4 s'appelle IPv6


En effet, il a fallu près de 15 ans pour stabiliser et sécuriser le protocole IPv6 et ses implémentations, il n'est pas crédible d'attendre un autre protocole de transport. 
De plus,  IPv6 est complètement fonctionnel sur la plupart des systèmes, y compris les systèmes embarqués qui intègrent dans leur grande majorité un OS linux sur lequel IPv6 est natif depuis la version 2.6 datant de 2006. 


Et si vous m'avez bien suivi,  les seules décisions que nous avons ) prendre, c'est **quand** et **comment** nous allons passer à IPv6 ! 




 



<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEwNDU0MzczNzEsLTE4Mzc0NzY5ODgsLT
MzNTk2Nzk1MSwtMTE0NjQwNzEzOSwtMTIyNDY4MzMwOSwtMTkw
MDQ1MzczNCw3ODgzMTcyOTgsLTE2MDk0MjkxMjEsLTEzNTAxNj
k5OTIsLTEzNjI5ODY0MzcsLTM2ODgyMDE0Miw3MDUyNDcwMTIs
NjI5MjQyOTM3LDEwMjUzNTc0ODQsMTM5NTc0MzExN119
-->