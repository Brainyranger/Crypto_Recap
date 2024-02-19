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

C’est un distingueur.

Principe : 

On parcourt les longueurs de clefs possibles, pour chacune d’elle on découpe le texte en
colonnes et on calcule la moyenne des IC de ces colonnes.
\
Lorsque la longueur de clef n’est pas la bonne, on mélange du texte de plusieurs des vraies
colonnes donc des caractères du clair qui ont été chiffré avec des décalages différents, ce qui
brouille la distribution des caractères et donne un IC voisin de celui d’un texte aléatoire.
\
En revanche si la longueur de la clef est bonne, tous les caractères d’une colonne subissent le
même décalage, l’IC de la colonne chiffrée est le même que celui de la colonne claire qui lui
correspond et leur moyenne est voisine de l’IC de la langue.
\
On repère donc une moyenne d’IC supérieure à un certain seuil pour déduire la longueur de la
clef.

## Cryptanalyse automatique : IC Mutuelle
L’indice de coïncidence mutuelle (ICM) entre deux textes \( t_1 \) et \( t_2 \) est la probabilité de tirer au hasard la même lettre dans \( t_1 \) et \( t_2 \). Mathématiquement, il peut être calculé à l'aide de la formule suivante :

$$\[ ICM = \sum_{i=0}^{25} \frac{\min(m_i, n_i)}{mn} \]$$

Où :
- \( m_i \) (resp. \( n_i \)) est le nombre de caractères \( c_i \) dans le texte \( t_1 \) (resp. \( t_2 \)).
- \( m \) (resp. \( n \)) est la taille de \( t_1 \) (resp. \( t_2 \)).

Principe : 

Propriété identique à l’indice de coïncidence
\
Attaque des chiffrements par décalage par analyse successive de
décalés : lorsque le décalage entre les textes est le bon cet indice
est beaucoup plus élevé 

## La cryptanalyse de Vigenère (avec les IC) : décalage de chaque colonne C
Analyse de fréquences directe
Par analyse de fréquences, trouver la position f(Ci) de la lettre la plus
fréquente de la colonne, compte tenu de la position f(langue) de la
lettre la plus fréquente de la langue du message, déduire le décalage
di = f(Ci) − f(langue) de la colonne Ci.

Utilisation des ICM puis analyse de fréquences
Calculer les ICM des Ci et les stocker dans un tableau de
différences de décalage dj − di entre les colonnes i et j
\
Résoudre le système linéaire correspondant pour exprimer le
décalage dj6=i de toutes les colonnes sauf la colonne i en fonction
de di
\
Procéder par analyse de fréquences
I soit sur la colonne i et de di déduire les dj!=i
I soit sur tout le texte après avoir aligné les colonnes j 6= i sur le
décalage di
\
Puis déduire la clef et le déchiffré du texte.
.
## Coefficient de corrélation de Pearson de deux variables aléatoires X et Y

La corrélation entre les variables \( X \) et \( Y \) est calculée à l'aide de la formule suivante :

$$\[ \rho_{X,Y} = \frac{\sum_{i} (X_i - \bar{X})(Y_i - \bar{Y})}{\sqrt{\sum_{i} (X_i - \bar{X})^2 \sum_{i} (Y_i - \bar{Y})^2}} \]$$

Où :
- $$\( X_i \)$$ et $$\( Y_i \)$$ représentent les valeurs de \( X \) et \( Y \) respectivement.
- $$\( \bar{X} \)$$ et $$\( \bar{Y} \)$$ représentent les moyennes de \( X \) et \( Y \) respectivement.
- $$\( sX \)$$ et $$\( sY \)$$ représentent les écarts-types de \( X \) et \( Y \) respectivement.

Une corrélation parfaite des variables \( X \) et \( Y \) produit \( \rho_{X,Y} = 1 \). Plus \( \rho_{X,Y} \) est proche de 1 et plus on peut considérer que la fréquence des caractères dans le texte chiffré en cours de transformation et celle de la langue sont corrélées.


