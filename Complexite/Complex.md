# Définition
Étant donné un algorithme résolvant un problème défini à partir d’une
entrée de taille n. La complexité de l’algorithme représente le nombre
d’opérations nécessaires pour résoudre le problème en fonction de n.

# Classes importantes de complexité
**Constante en t : C = O(1) pour tout constante C.**

**Complexité polynomiale en t : P(t) opérations où P est un polynôme de degré k > 1** 
\on a P(t) = O(tk) = 2<sup>O(log(t))</sup>

**Complexité exponentielle en t :** 2<sup>O(tk)</sup> opérations pour une constante k > 1 fixée.

**Entre les deux** : complexité sous-exponentielle L[α, c] = exp(ct<sup>α</sup>log(t)<sup>1-α</sup>) n’est
ni polynomiale ni exponentielle pour α ∈]0, 1[ et c une constante fixée.

**Problème facile ? Problème difficile ?**
Un problème est facile s’il se résout au plus en temps polynomial en la taille de
son entrée.
\ Un problème est difficile si l’on ne sait pas mieux faire qu’en temps exponentiel!

# Définitions
Un problème appartient à P s’il existe un algorithme polynomial
(en la taille n décrivant le problème) pour résoudre ce problème.
\
Un problème appartient à N P s’il existe un algorithme polynomial
(en la taille n décrivant le problème) pour vérifier une solution de
ce problème.

# Taille des entrées
Pour un entier a sa taille est `(a) = log2(a) = O(log(a))

# Complexité naïve sur entier
Pour a > b > 0
\
Addition : O(log(a))
\
Multiplication : O(log(a)log(b))
\
Division : O(log(a/b)log(b)) = O(log(q)log(b))

# Complexités modulo N
Addition : O(log(N))
\
Multiplication : O(log(N)<sup>2</sup>)
\
Inverse (algorithme d’Euclide étendu) : O(log(N)<sup>2</sup>)


\
Complexité échange de clé par Diffie-Hellman-Merkle
Si l’on souhaite échanger une clé de taille L il faudra faire
O(4*L <su>3<sup/>)
opérations binaires.
