# Modélisation d'un Cryptosystème 

P et C les alphabets pour écrire les messages clairs et les
messages chiffrés respectivement.
K l’ensemble des clefs possibles.
Pour tout K ∈ K on peut définir deux applications 
eK : P → C (Encryption) 
dK : C → P (Decryption) 
telles que dK(eK(x)) = x , pour tout x ∈ P.

**Pour le cas du cryptosystème symétrique : Les applications eK et dK nécessitent la connaissance complète
de K pour être définies.**

# Cryptosystème par substitution

P, C deux alphabets peuvent être différents mais doivent être de même cardinal
K est l’ensemble des bijections de P dans C, c'est à dire K représente l'ensemble de toutes les fonctions de chiffrement possibles qui prennent un texte clair en entrée et produisent un texte chiffré correspondant.
Pour tout $K \in K$, on a :
- $E_K(x) = K(x)$
- $D_K(y) = K^{-1}(y)$

**Pour le cas du cryptosystème par substitution sur alphabets identiques K est l’ensemble des permutations de P dans C.**

# Cryptosystème affine
- \(P\) et \(C\) sont tous les deux égaux à $$\( \mathbb{Z}/26\mathbb{Z} \)$$.
- \(K\) est un sous-ensemble de $$\( \mathbb{Z}/26\mathbb{Z} \times \mathbb{Z}/26\mathbb{Z} \)$$ tel que pour tout $$\( K = (a, b) \in K \)$$,
-  on a $$\( e_K(x) = (ax + b) \mod 26 \)$$.
- Il existe une fonction $$\( d_K : C \rightarrow P \) inverse de \( e_K \)$$.

