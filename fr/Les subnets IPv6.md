
ou créer son premier LAN IPv6

Quel subnet doit-on allouer en IPv6 ?

Si on se calque sur IPv4, où les subnets courants sont en /24 pour allouer jusqu'à 254 hosts, un /120 devrait être correct., et en prenant très large, un /112 serait le bout du monde : après tout qui veut avoir plus de 50.000 hosts sur le même segment.

Pourtant, la RFC4291 impose un masque /64 pour tous les subnets.

Il faut bien reconnaître que cette règle a le grand avantage de la simplicité et de l'uniformité !

Mais on a quand même se demander si ce n'est pas du gaspillage.

Il faut alors réaliser qu'il reste encore 64 bits pour les réseaux, ce qui donne un nombre encore 

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE5NDE0MDM2MDksODU5MzM1NTY2XX0=
-->