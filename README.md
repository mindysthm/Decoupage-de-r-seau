Méthode symétrique

|         | Adresse réseau          | Adresse de brodcast | Adresse de début de plage | Adresse de fin de plage
| :--------------- |:---------------:| -----:| -----:| -----:|
|Pole informatique (50) | 172.16.1.0/26       |  172.16.1.63| 172.16.1.1 | 172.16.1.62
|Pole administratif (20) | 172.16.1.64/26           |   172.16.1.127 | 172.16.1.65 | 172.16.1.126
| Pole technicien (15) | 172.16.1.128/26        |    172.16.1.191 | 172.16.1.129 | 172.16.1.190
| Pole dev (12)  | 172.16.1.192/26       |     172.16.1.255 | 172.16.1.193 | 172.16.1.254

Le réseau est en 172.16.1.0/24. Le pole avec le plus d'équipements est l'informatique (50). Pour que tout le monde ait le même nombre d'adresses, on va se caler sur celui-ci. 
Le nombre supérieur correspond à 2 puissance 6 soit 64 équipements. On enlève 2 équipements pour l'adresse broadcast et l'adresse du réseau. On a donc 62 adresses pour chaque pôle
Pour le CIDR, on prend 32 - la puissance 6 = 26


Méthode asymétrique

|         | Adresse réseau          | Adresse de brodcast | Adresse de début de plage | Adresse de fin de plage
| :--------------- |:---------------:| -----:| -----:| -----:|
|Pole informatique  |  172.16.1.0/26       |  172.16.1.63 | 172.16.1.1 | 172.16.1.62
|Pole administratif  |172.16.1.64/26            |  172.16.1.95 | 172.16.1.65 | 172.16.1.94
| Pole technicien  | 172.16.1.96/26          |    172.16.1.111 | 172.16.1.97 | 172.16.1.110
| Pole dev   | 172.16.1.112/26       |    172.16.1.127 | 172.16.1.113 | 172.16.1.126

On cherche en premier le nombre d'hôte pour chaque département de la liste ci-dessus :

Pole info (50 équipements) --> 2^6 - 2 = 64 - 2 = 62  

Pole administratif (20 équipements) --> 2^5 - 2 = 32 - 2 = 30

Pole technicien (15 équipements) --> 2^4-2 = 16 - 2 = 14

Pole dev (12 équipements) --> 2^4 - 2 = 16 - 2 = 14
