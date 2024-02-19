# Définition 
Inspiré de Alberti : Chiffrement multi-mono-alphabétique
\
On chiffre des blocs de texte de longueur(ligne). Pour la lettre d’indice i d’un bloc on applique
un chiffrement mono-alphabétique eK.
\
Autrement dit on écrit le texte sur ` colonnes et on
utilise une permutation différente pour chaque
colonne.
\
Problème : Trop difficile à utiliser, nécessité de le simplifier
\
Idée : reprendre le chiffrement de Alberti en se restreignant aux chiffrements par décalage.

# Cryptanalyse Vigenere

## Principe du test de kasiski : longueur de la clef (étape 1)

Une répétition dans le message clair si elle se produit à la même
position dans la clef (la même colonne) produit une répétition
dans le message chiffré
\
on repère les répétitions dans le chiffré en espérant qu’elles
correspondent à une répétition dans le clair
\
si c’est le cas la distance (le nombre de caractères entre le début
de chaque occurrence) entre elles fournit un multiple de la
longueur de la clef.

**Remarque : Le pgcd des distances entre les répétitions de motif est probablement un multiple de la longueur de la clef**

## Finalisation de l'attaque : (étape 2)

Si les colonnes sont suffisamment longues on peut espérer que la
distribution des fréquences des caractères de l’alphabet dans chaque
colonne soit à peu près celle du texte complet et surtout celle de la
langue.

-> On découpe le texte chiffré en bloc de caractères et on applique une cryptanalyse par décalage sur les colonnes !

## Cryptanalyse automatique : indice de coïncidence
L'indice de coïncidence \(IC\) d'un texte est la probabilité de tirer un couple de lettres identiques au hasard. Mathématiquement, il peut être calculé à l'aide de la formule suivante :

$$\[ IC = \frac{\sum_{i=0}^{25} C(n_i, 2)}{C(n, 2)} \]$$

Où :
- \( n_i \) est le nombre de fois où la lettre \( c_i \) apparaît dans le texte.
- \( n \) est la longueur totale du texte.
- \( C(n, 2) \) est le nombre total de paires possibles dans le texte, c'est-à-dire le nombre de façons de choisir 2 lettres parmi les \( n \) lettres du texte.
- \( C(n_i, 2) \) est le nombre de paires de la lettre \( c_i \) dans le texte, c'est-à-dire le nombre de façons de choisir 2 occurrences de la lettre \( c_i \) parmi les \( n_i \) occurrences de cette lettre dans le texte.


