
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

### Fournir autant d'adresses que nécessaire
IPv6 en utilisant un format d'adresse en 128 bits au lieu de 32 bits pour IPv4 permet d'allouer un nombre d'adresses en apparence illimité ([150 bits permettent de compter les atomes de la terre](https://fr.wikipedia.org/wiki/Ordres_de_grandeur_de_nombres#1039_%C3%A0_10100)). 

64 bits auraient pu suffire pour fournir des adresses uniques pendant la durée de vie du protocole. En effet, les adresses MAC des cartes Ethernet, codées sur "seulement" 48 bits  [sont loin d'être toutes attribuées](https://macaddress.io/statistics), et la croissance passée permet de prédire sans trop de risques [quelques décennies sans pénurie](https://macaddress.io/statistics/date).


### Fournir des adresses uniques aux organisations

IPv6 prévoit la fourniture d'adresses locales (donc non routées sur Internet), uniques. Pratique quand deux organisations voudront fusionner !

### Abandonner la translation d'adresse

Pour les créateurs d'IPv6, le NAT c'est le mal !

- NAT limite la visibilité des adresses source (statistiques tronquées).
- Surtout NAT limite l'accessibilité des serveurs (impossibilité d'accéder à un service placé derrière une translation). Et les serveurs, ce ne sont pas seulement les gros serveurs Web de mon Intranet, ce sont aussi tous mes objets qui s'administrent ou se consultent via une UI Web ou des API REST. 
- Enfin NAT  donne une fausse impression de sécurité (je vous laisse disserter sur le sujet "NAT = firewall + anonymat ?" [spoiler] Ceux qui se placent dans le camp du oui n'auront pas la moyenne).


### IPv6 est-il parfait ?

Bien sûr IPv6 est un protocole comme une autre qui résout des problèmes et en pose d'autres. 

Le principal obstacle à IPv6, c'est la non interopérabilité avec IPv4. Un client purement IPv6 ne peut pas dialoguer avec un serveur seulement IPv6. Il va falloir prévoir une migration complexe et surtout lente.


### Quels challengers à IPv6 ?

IPv6 apporte des réponses correctes aux problèmes posés par IPv4. Mais quels autres choix avons nous ou pourquoi IPv6 ?

Parce qu'on n'a pas le choix : 

> la seule alternative à IPv4 s'appelle IPv6


En effet, il a fallu près de 15 ans pour stabiliser et sécuriser le protocole IPv6 et ses implémentations, il n'est pas crédible d'attendre un autre protocole de transport. 
De plus,  IPv6 est complètement fonctionnel sur la plupart des systèmes, y compris les systèmes embarqués qui intègrent dans leur grande majorité un OS linux sur lequel IPv6 est natif depuis la version 2.6 datant de 2006. 


Et si vous m'avez bien suivi,  les seules décisions que nous avons ) prendre, c'est **quand** et **comment** nous allons passer à IPv6 ! 

Je n'ai pas la réponse à la première question,  mais je vous propose dans les articles suivants une méthodologie pour vous aider à préparer votre migration vers IPv6.




 



<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEzOTkzNTgyMDIsLTU4OTc0OTg3OCwxOT
E0OTI1MjYxXX0=
-->