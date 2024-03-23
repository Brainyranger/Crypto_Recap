☞ En 1976, Diffie, Hellman et Merkle publient le premier schéma
d’échange de clés à l’aide de la notion de clé publique qu’ils
énoncèrent.

# DLP 
**Définition**
Soit (G, ◦) un groupe fini et g ∈ G. Le problème du logarithme discret
(noté DLP) dans le sous-groupe H = hgi de G est défini comme suit :
-Étant donné h ∈ H \
-Comment retrouver k ∈ N tel que h = g ◦ · · · ◦ g (k fois) ?
\
**Notations**
Pour g ∈ G et t ∈ N on notera l’opération d’exponentiation de g en t
par [t]g = g ◦ · · · ◦ g, t fois. Cette notation permet d’homogénéiser les
notations, par exemple : \
Si (G, ×) on a [t]g = g × · · · × g = gt \
Si (G, +) on a [t]g = g + · · · + g = t · g 

Le logarithme discret en base g de h est défini par : \
k = log_g(h)    avec h = [k]g
