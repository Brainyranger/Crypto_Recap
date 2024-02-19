**Résistance : temps de cryptanalyse / durée de vie de l’information**

# Principe : 
On peut utiliser un cryptosystème pour chiffrer une information tant que le temps pour
effectuer la cryptanalyse du système dépasse la durée de la pertinence de
l’information.

# Chiffrement parfait

## Intuition
Un cryptosystème sera dit un chiffrement parfait lorsque la donnée
d’un message chiffré ne révèle aucune fuite d’information sur la clef ou
le message clair correspondant et aucune information non plus sur les
textes chiffrés futurs.
\
Caractérisation
Supposons qu’un cryptosystème vérifie
**#K = #P = #C**
alors il sera un chiffrement parfait ssi on a
Toutes les clefs sont utilisées avec la même probabilité
\
Pour tout couple (m, c) ∈ P × C il existe une unique clef k telle que
ek(m) = c.

Exemple : Vernam’s One Time Pad. C’est le seul cryptosystème à chiffrement parfait!
