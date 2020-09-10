
ou créer son premier LAN IPv6

Quel subnet doit-on allouer en IPv6 ?

Si on se calque sur IPv4, où les subnets courants sont en /24 pour allouer jusqu'à 254 hosts, un /120 devrait être correct., et en prenant très large, un /112 serait le bout du monde : après tout qui veut avoir plus de 50.000 hosts sur le même segment.

Pourtant, la RFC4291 impose un masque /64 pour tous les subnets.

Il faut bien re c'est simple ! mais on peut quand même se demander si 
Simple : 

> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE0NzczMzA2OTYsODU5MzM1NTY2XX0=
-->