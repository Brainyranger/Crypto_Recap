# Principe 
Polygrammique : chiffrer non plus des caractères individuels mais des
blocs de caractères (des polygrammes).
## Un exemple de substitution polygrammique : le chiffrement de Playfair
Inventé par Wheatstone en 1854 et popularisé par Lord Playfair, utilisé
pendant la Première Guerre Mondiale par les anglais et la Seconde
Guerre Mondiale par les australiens.
\
La clef secrète se présente sous la forme d’un carré 5x5 qui contient
toutes les lettres de l’alphabet, en en confondant 2, telles que I et J ou
V et W.

### Principe du chiffrement de Playfair
S’il s’agit d’une lettre double m m : on glisse une lettre neutre entre les deux m et on
applique à nouveau les règles à partir du premier m (oui tout l’appariement des
caractères se trouve décalé et peut produire de nouveaux doubles plus loin).
\
S’il ne reste qu’un seul caractère m à chiffrer on ajoute derrière une lettre neutre et on
chiffre avec les règles précédentes.
\
Lettre neutre : une lettre peu fréquente, donc facilement identifiable comme neutre
dans le clair après déchiffrement, telle que X si m 6= X évidemment.
