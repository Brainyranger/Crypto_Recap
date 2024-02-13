**Al Kindi (vers 800) explique dans son ouvrage de cryptanalyse la méthode de l’étude des fréquences.**

## Cryptanalyse du chiffrement par décalage
Analyse de fréquence : Dans de nombreuses langues, certaines lettres apparaissent plus fréquemment que d'autres. En analysant les fréquences d'apparition des lettres dans le texte chiffré, il est possible d'essayer de deviner la clé de décalage en supposant que la lettre la plus fréquente correspond à la lettre la plus fréquente dans la langue donnée.

##  Cryptanalyse du chiffrement mono-alphabétique
Méthode force brute assistée avec des hypothèses à faire tout au long
de l’attaque.
\
Besoin de plus que la fréquence des lettres pour y arriver efficacement,
il faut s’intéresser à la fréquence de groupes de lettres, à la façon dont
les caractères se succèdent, s’articulent.
\
De même on peut utiliser la fréquence des tétragrammes dans une
stratégie itérative de hill climbing 

## Substitution homophonique
Pour casser la fréquence des caractères
associer plusieurs caractères de substitution aux caractères ou
groupes de caractères ou mots les plus fréquents et choisir
aléatoirement quelle variante utiliser à chaque occurrence
ajouter des caractères parasites sans signification
