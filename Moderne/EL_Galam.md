ElGamal 1985
Ce cryptosystème est basé sur le DLP.
L’espace des messages est représenté par le groupe (G, ◦). \
Alice tire aléatoirement k et calcule h = [k]g \
Alice publie H = hgi et h et conserve secrètement k \
Chiffrement : Pour envoyer x ∈ G à Alice, Bob choisit \
t ∈ {1, . . . , |H|} aléatoirement et ne le publie pas. Il calcule \
y1 = [t]g et y2 = x ◦ [t]h \
et envoie le couple (y1, y2) à Alice. \
Déchiffrement : Alice calcule y2 ◦ [−1]([k]y1) et retrouve x. \

ElGamal sur les corps finis \
Exemple d’échange ElGamal : \
Alice choisit G = H = Z/pZ \
∗ avec p = 2579 et g = 2 qu’elle publie. Elle
garde secret k = 765 et publie aussi
h = 2765 mod 2579 = 949 \
Bob veut transmettre x = 1299 à Alice. Il choisit t aléatoirement t = 853 
et calcule \
y1 = [t]g = 2853 mod p = 435 puis \
y2 = x ◦ [t]h = 1299 × (949853) mod p = 2396 \
et les envoie à Alice. Elle reçoit donc (435, 2396) et calcule alors : \
x = y2 ◦ [−k]y1 = 2396 × (435765) \
−1 mod 2579 = 1299 \
pour retrouver le message de Bob !
