## Théorème fondamental de l’arithmétique
Tout élément qui n’est ni nul ni inversible peut être écrit sous la forme
d’un produit p1p2 · · · pn d’éléments irréductibles et cette décomposition
est unique à association et ordre près des facteurs irréductibles.

## Les nombres premiers 
Les nombres irréductibles sont les nombres premiers !
\
L’ensemble des nombres premiers est infini :
\
Preuve :
\
On suppose qu'il y a un ensemble fini de nombres premiers n1,..,nk
\
On construit un nouveau nombre premier :  $$1 + \prod_{i=1}^{k} n_i$$, ce qui contredit l'hypothèse.

### Lemme
Un entier n > 1 est premier ssi il n’est divisible par aucun entier
compris entre 2 et √n.
### Entiers premiers entre eux
Deux entiers a et b sont premiers entre eux ssi l’ensemble des diviseurs
communs à a et b est réduit aux inversibles.


## Théorème de Lagrange

Soit (G, ×) un groupe fini et H un sous-groupe de G. Alors le cardinal
de H est un diviseur du cardinal de G. (Le cardinal d’un groupe est
aussi appelé ordre.)

### Ordre d’un élément
Soit g un élément d’un groupe fini (G,*). On appelle ordre de g le plus petit entier strictement
positif k tel que 
g<sup>k</sup> = e alors k est un multiple de l’ordre de g

### Corollaire
Tout groupe (G,*) dont l’ordre est un nombre premier est cyclique.

## Théorème de Bachet-Bézout
Soit a et b deux éléments d’un anneau euclidien A. Il existe deux
éléments u et v tel que : 
\
pgcd(a, b) = ua + vb.
\
Une telle égalité s’appelle une relation de Bézout et les coefficients u
et v sont appelés les coefficients de Bézout.
### Corollaires du théorème de Bachet-Bézout
Deux entiers a et b sont premiers entre eux ssi : 
\
leur plus grand commun diviseur est inversible et puisqu’il est positif
c’est 1 :
pgcd(a, b) = 1
\
il existe u et v tel que
ua + vb = 1
\
l’ensemble des entiers qui sont multiples de a ou de b forme l’anneau Z
tout entier
aZ + bZ = 1Z = Z

## Algorithme d’Euclide étendu

$$\[
\begin{cases}
u_0 = 1, v_0 = 0, r_0 = a \\
u_1 = 0, v_1 = 1, r_1 = b \\
u_{i+1} = u_{i-1} - q_i u_i, \\
v_{i+1} = v_{i-1} - q_i v_i, \\
r_{i+1} = r_{i-1} - q_i r_i, \\
\text{si } r_i \neq 0 \text{ et arrêt sinon.}
\end{cases}
\]$$

avec  $$\( q_i = \left\lfloor \frac{r_{i-1}}{r_i} \right\rfloor \) si \( r_i \neq 0 \)$$.
