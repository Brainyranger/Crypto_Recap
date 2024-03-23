
Rivest, Shamir, Adleman
☞1977 première instance d’un cryptosystème à clé publique : RSA.
\
RSA
\
Basé sur la difficulté de calculer une racine e-ième mod un entier N de
factorisation inconnue \
Si on sait factoriser facilement alors ce problème se résout tout
aussi facilement. Mais ATTENTION ce ne sont pas des problèmes
polynomialement équivalents. \

Soient p et q deux nombres premiers et n = pq. On choisit deux entiers
e, d tels que ed = 1 mod ϕ(n). L’application
F(n,e) : \
Z/nZ → Z/nZ définie par x 7→ x
e mod n
\
F est bien à sens unique, difficulté basée sur le calcul de la racine
e-ieme modulaire.
\
La trappe est la connaissance de d (ou de manière équivalente p
et q).
\
☞on chiffre en faisant x<sup>e</sup> mod n on déchiffre en calculant y<sup>d</sup> mod n

\
**Signer avec RSA** \
☞La signature permet d’authentifier l’expéditeur d’un message
La signature RSA \
Soit N = pq un entier RSA et (e, d) un couple d’exposants de
chiffrement/déchiffrement choisis par l’expéditeur.
L’expéditeur publie N et d \
Un message m ∈ (Z/NZ)
× envoyé par l’expéditeur aura pour signature
sm = m<sup>e</sup> mod N \
Le destinataire recevra le couple (m,s) et authentifiera l’expéditeur
à partir ses clés publiques (N, d) en vérifiant \
m = sm<sup>d</sup> mod N

\
## Théorème chinois des restes
### Théorème
Soit m1 et m2 deux éléments de A un anneau euclidien. \
Si pgcd(m1, m2) = 1 alors nous avons l’isomorphisme d’anneau \
A/m1A × A/m2A ' A/(m1m2)A

