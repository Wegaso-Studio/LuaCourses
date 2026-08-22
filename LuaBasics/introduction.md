
# Introduction:

## 1 - Brève explications
- Il y a des choses à savoir qui sont identiques à tout les langages de codes pour que tu comprenne on va utiliser un langage qu'on va appeler "pseudo code"!

- Ce code n'existe pas il est representatif d'un code quelconque et sert seulement à la compréhension.

## 2 - Les types de données
- Le code en général peut envoyer, recevoir, enregistrer plusieurs type de données.

- On retrouvera notamment comment coder des phrases, des chiffres

- Voici les types de donnée standards: (il en existe d'autres mais qui ne sont pas interessants à connaître pour le moment, tu peux aussi faire tes propres recherches sur le net)
  - Le **nil** pour indiquer une valeur indéfinie ou nulle (souvent pour initialiser une `variable*` on y vient plus tard)

  - Le **boolean** sert a dire au code si c'est vrai ou non (on pourra récupérer cette valeur lors d'une `condition*` on y vient plus tard)

  - Le **number** permet d'indiquer un chiffre (Il sera different qu'un chiffre/nombre dans une `string*`)

  - La **string** est une forme permettant d'inscrire des mots ou des phrases (nous parlerons aussi des `délimiteurs de chaîne de caractères*`, et des `caractères d'annulation*`)

  - Le **array** la meilleure manière de faire une liste que nous pourrons itérer plus tard avec une `boucle*` ou des methodes natives en Lua

  - La **table** permettant de concerver des données en clé-valeur (`key-value*` on y vient plus tard)

## 3 - Les bases en programmation
- **Les variables**
  - une manière de retenir une donnée dans le code de manière definitive, sa valeur peut etre modifiée tout au long du code (chaque langage possède son système de prefix de variables a apprendre avec la syntaxe de base).

- **Les fonctions**
  - permet de creer une fonction réutilisable qui execute un code quand on l'appelle

- **Les boucles**
  - permet d'itérer (fouiller) les tableaux `table*`

- **Les conditions**
  - permet de verifier si la condition est *égale/plus-grande/plus-petite/vrai-fausse* avant d'effectuer le reste du code

- **Les classes**
  - certains code de programmation `backend` utilisent un systeme de classe permettant de structurer le code

- **Les commentaires**
  - Les commentaires sont la forme de code la plus importante pour se retrouver dedans ^^ chaque syntaxe a sa manière (lua = "--", js = "//", cfg = "#", css = "/* */", etc)

## 4 - Le pseudo code:
- Ici je vais donner une base de pseudo code et le code correspondant en `Javascript` afin que tu vois la difference entre un pseudo code et un code réel.

- Pseudo code:
    ```plaintext
    -- variables
        age-minimum = 18
        mon-age = 20

    -- condition
        si mon-age est plus grand ou égal à age-minimum
            -- affichage
                affiche "La personne est majeure"
        sinon
            -- affichage
                affiche "La personne est mineure"
        fin
    ```
    **l'ecran affichera** *"La personne est majeure"*

- Javascript:
    ```js
    // Variables
        const minAge = 18;
        const myAge = 20;

    // Condition
        if (myAge >= minAge) {
            // Affichage
            console.log("La personne est majeure");
        } else {
            // Affichage
            console.log("La personne est mineure");
        };
    ```
    **l'ecran affichera** *"La personne est majeure"* **aussi**.
