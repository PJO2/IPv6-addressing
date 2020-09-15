
Adresser une organisation en IPv6 : les best practices

Ce nouveau cycle de présentation est là pour échanger autour des best practices relatives à la mise en place d'un plan d'adressage IPv6 au sein d'une organisation (entreprise, établissement public, ...). Il s'adresse à un public familiarisé avec le format IPv6.


## Les limitations d'IPv4 ?
sous-titre: quels problèmes IPv6 prétend résoudre ?

IPv4 est victime de son succès et les adresses publiques autorisées par le protocole ont été entièrement attribuées. Il est possible de racheter des adresses déjà attribuées pour un prix de l'ordre de [25$ par adresse](https://auctions.ipv4.global/).

Malgré l'épuisement des adresses, 2 mécanismes nous permettent quand même de continuer à vivre avec IPv4 :
 - Les adresses privées, non routées sur Internet,  qui peuvent être utilisées conjointement  par plusieurs organisations 
 - Le NAT qui permet de translater un subnet d'adresses privées vers une seule adresse publique 
  
Ainsi, en pratique, la plupart des organisations utilise le réseau privé 10.0.0.0/8 et ne s'estime pas encore concerné par  IPv6. De plus, tous les opérateurs Internet grand public regroupent les réseaux personnels (home network) sur une seule adresse IP (NAT), et certains regroupent même un grand nombre de réseaux personnels sur un nombre réduit d'adresses publiques (large scale NAT). 

Si ces 2 mécanismes permettent effectivement d'économiser les adresses IPv4, ils ne répondent pas efficacement à certains usages :
- fusion d'organisations partageant les mêmes adresses en 10.0.0.0/8
- accessibilité de serveurs dont l'adresse est translatée

De plus, l'arrivée des objets connectés dans les entreprises (caméras vidéo, étiquettes connectées dans la distribution, capteurs connectés dans les entrepôts, les locaux techniques, les véhicules, ...) augmente la demande nombre des subnets à attribuer et bouscule le plan d'adressage des organisations. 
Il ne s'agit plus d'affecter une adresse IP par employé, mais de gérer des ensembles d'objets en nombre difficilement prévisible qui doivent appartenir à des nouveaux subnets pour leur adjoindre le bon niveau de sécurité (côté sécurité, c'est cool  de distinguer facilement un humain d'un interrupteur).

Nous allons voir qu'IPv6, construit à partir  du retour d'expérience IPv4, apporte des réponses concrètes à tous ces points.


## IPv6, la solution ?

IPv6 en utilisant un format d'adresse en 128 bits au lieu de 32 bits pour IPv4 permet d'allouer un nombre d'adresses en apparence illimité ([150 bits permettent de compter les atomes de la terre](https://fr.wikipedia.org/wiki/Ordres_de_grandeur_de_nombres#1039_%C3%A0_10100)). 

64 bits auraient pu suffire pour fournir des adresses uniques. En effet, les adresses MAC des cartes Ethernet, codées sur "seulement" 48 bits  sont [loin d'être toutes attribuées](https://macaddress.io/statistics), et la croissance passée permet de prédire [quelques décennies sans pénurie](https://macaddress.io/statistics/date).



## Pourquoi IPv6 ?

Parce qu'on n'a pas le choix : 

> la seule alternative à IPv4 s'appelle IPv6


En effet, il a fallu près de 15 ans pour stabiliser et sécuriser le protocole IPv6 et ses implémentations, il n'est pas crédible d'attendre un autre protocole de transport. 
De plus,  IPv6 est complètement fonctionnel sur la plupart des systèmes, y compris les systèmes embarqués qui intègrent dans leur grande majorité un OS linux sur lequel IPv6 est natif depuis la version 2.6 datant de 2006. 


Et si vous m'avez bien suivi,  les seules décisions que nous avons ) prendre, c'est **quand** et **comment** nous allons passer à IPv6 ! 




 



<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE5MTc1NTg5MjYsLTI5NDMxMjA2MiwyMD
I3NjE4NjEwLC0xODM3NDc2OTg4LC0zMzU5Njc5NTEsLTExNDY0
MDcxMzksLTEyMjQ2ODMzMDksLTE5MDA0NTM3MzQsNzg4MzE3Mj
k4LC0xNjA5NDI5MTIxLC0xMzUwMTY5OTkyLC0xMzYyOTg2NDM3
LC0zNjg4MjAxNDIsNzA1MjQ3MDEyLDYyOTI0MjkzNywxMDI1Mz
U3NDg0LDEzOTU3NDMxMTddfQ==
-->