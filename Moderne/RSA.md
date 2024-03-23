
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
