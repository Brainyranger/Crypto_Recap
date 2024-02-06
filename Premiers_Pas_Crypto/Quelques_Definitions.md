# Cryptologie : Principes et Études

La **cryptologie** comprend deux principaux domaines :

- **Cryptographie** : étude des cryptosystèmes, qui sont des algorithmes permettant de chiffrer et déchiffrer des données pour les protéger.
  
- **Cryptanalyse** : étude du niveau de sécurité des cryptosystèmes.

Les trois grands points à gérer dans la cryptologie sont :

1. **Confidentialité**
2. **Authentification**
3. **Intégrité**

Le **principe de Kerckhoffs** énonce que la sécurité d'un système ne dépend que de la clé. Autrement dit, le système doit rester sécurisé tant que la clé reste secrète. 

## Première étude de notre premier cryptosystème : Cryptographie Symétrique

La **cryptographie symétrique** (ou cryptographie à clé privée) utilise la même clé secrète pour chiffrer et déchiffrer les données. C'est à dire que la même clé est utilisée des deux côtés de la communication pour sécuriser les échanges de données.

<font color="green"><b>Remarque :</b></font> La sécurité d'un cryptosystème est attestée par la cryptanalyse. 


### Exemple de la Vie Courante : Visite d'un Site Web Sécurisé

Lorsque vous visitez un site Web sécurisé (repéré par "https://" dans l'URL), votre navigateur établit une connexion sécurisée avec le serveur de ce site. Cette connexion sécurisée est établie grâce à un protocole de sécurisation appelé SSL (Secure Sockets Layer) ou TLS (Transport Layer Security).
Le serveur du site envoie alors son certificat SSL à votre navigateur. Ce certificat contient la clé publique du serveur, qui est utilisée pour établir une communication sécurisée entre votre navigateur et le serveur.
Une fois que votre navigateur a reçu le certificat du serveur, il génère une clé de session aléatoire, également connue sous le nom de clé de chiffrement. Cette clé de session est une clé temporaire utilisée uniquement pour cette session particulière de communication entre votre navigateur et le serveur.

## Deuxième cryptosystème : Chiffrement par substitution ou mono-alphabétique

Le chiffrement par substitution consiste sur le fait qu'à chaque élément de P(texte clair) correspond un unique élément de C(texte chiffré).

### Exemple : Chiffrement de César

C'est un exemple simple de chiffrement par substitution où chaque lettre du texte clair est remplacée par une autre lettre, mais en utilisant un décalage fixe dans l'alphabet.