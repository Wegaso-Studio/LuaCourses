
# Introduction:

## Brève explications
- Il y a des choses à savoir qui sont identiques à tout les langages de codes pour que tu comprenne on va utiliser un langage qu'on va appeler "pseudo code"!

- Ce code n'existe pas il est representatif d'un code quelconque et sert seulement à la compréhension.

## Les types de données
- Le code en général peut envoyer, recevoir, enregistrer plusiueurs type de données.

- On retrouvera notamment comment coder des phrases, des chiffres

- Voici les types de donnée standards: (il en existe d'autres mais qui ne sont pas interessants à connaître pour le moment, tu peux aussi faire tes propres recherches sur le net)
  - Le **nil** pour indiquer une valeur indéfinie ou nulle (souvent pour initialiser une `variable*` on y vient plus tard)

  - Le **boolean** sert a dire au code si c'est vrai ou non (on pourra récupérer cette valeur lors d'une `condition*` on y vient plus tard)

  - Le **number** permet d'indiquer un chiffre (Il sera different qu'un chiffre/nombre dans une `string*`)

  - La **string** est une forme permettant d'inscrire des mots ou des phrases (nous parlerons aussi des `délimiteurs de chaîne de caractères*`, et des `caractères d'annulation*`)

  - Le **array** la meilleure manière de faire une liste que nous pourrons itérer plus tard avec une `boucle*` ou des methodes natives en Lua

  - La **table** permettant de concerver des données en clé-valeur (`key-value*` on y vient plus tard)

## Les bases en programmation
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

## Le pseudo code:
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

---
# Initiation au lua:

## Les commentaires
- Les commentaires sont importants nous allons les voir en premier !

- pour commenter une seule ligne il faut mettre deux tirets `--`

- pour commenter plusieurs lignes deux tirets, deux crochets ouvrants et deux fermants `--[[ mon message ]]`
    
    exemple:
    ```lua
    -- mon commentaire super important en une seule ligne

    --[[
        Mon pavé comme j'ai l'habitude de faire..
        Plutôt qu'un lorem ipsum débile, je préfère perdre du temps
        à taper des phrases inutiles au lieu de faire
        des pseudo phrase en plus du pseudo code.
        renseigne toi sur le "lorem ipsum" ^^
        C'est sympa à connaitre si tu ne connais pas encore!

        Lorem ipsum dolor sit amet, consectetur adipiscing elit,
        sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
        Ut enim ad minim veniam.
    ]]
    ```

## Les variable
- Une variable est comme une petite mémoire qui retient ce qu'on met dedans.

- Elle se compose d'une clé et d'une valeur `key-value` la **clé** c'est le nom qu'on donne à l'élément dans cette petite mémoire.

- Et la **valeur** c'est ce qu'on souhaite mémoriser dans cette petite mémoire, j'ai l'habitude de prendre l'exemple d'une petite boite ^^
    ```
            +------- Valeur/Value: ("mon souvenir")
            |
            V

    +-----------------------+
    |                       |
    |                       |
    |  Clé/Key: (ma-boite)  | 
    |                       |
    |                       |
    +-----------------------+
    ```
- En langage *Lua* on crée une variable en la précédent du mot `local` suivi de la clé et de la valeur.

    ```lua
    local ma-boite = "mon souvenir"

    -- Ce sera toujours comme ça ! Voici plusieurs exemples de variables
    local myAge = 34
    local isMajor = true
    local myName = "Stéphan M."
    local myFavoriteAnimals = ["cats", "dogs"]

    local myVacancyPlan = {
        destination = "Kentucky",
        amountAvailable = 5863,
        cashType = "currency_usd",
        passports = ["driver_license", "id_card"]
    }
    ```
- Tu remarquera donc qu'une variable peut contenir une `table*` d'une ou plusieurs données de types différents (ça s'appelle une programmation orienté objet `OOP programmation`)

## Les valeurs de base
- Les `string` sont des mots ou phrases qui s'ecrivent dans des guillements (ce sont d'ailleurs les seules valeurs dans des guillemets)
    - Il y a 3 type de guillements
        - guillemets doubles
        ```lua
        local str = "Ma chaine de caractères"
        ```
        - guillemets simple
        ```lua
        local str = 'Ma chaine de caractères'
        ```
        - guillemets backticks
        ```lua
        local str = `Ma chaine de caractères`
        ```
        
    - Le Lua accepte les 3 mais il y a une petite chose a savoir
        - les backticks sont utilisés en Lua pour les props principalement (question de fonctionnement fiveM framework)
        - les guillemets simples ne permettent plus de créer facilement des apostrophes.
        ex:
        ```lua
        local maStringCassee = 'l'ecureuil'
        ```
        - Tu remarque que la syntaxe affiche une sifférence après " l' " c'est parceque le code pense que la string s'arrête à 'l' tout le reste n'est pas compris ecureuil' erreur de syntaxe
        - Comment faire haaaa! Ok on utilise le fameux antislash devant le caractère qu'on veut annuler (c'est le `caractères d'annulation*`)
        ex: 
        ```lua
        local maStringReparee = 'l\'ecureuil'
        ```

    - Petit bonus grace à l'antislash on va pouvoir effectuer certaines actions comme retourner a la ligne avec `\n` dans une string
        ex:
        ```lua
        local str = "Voici ma longue phrase,\n Je l'ai donc coupé en deux avec \\n"

- Les `number` sont des nombres on les ecrits normalement
    - on dit `int` les nombres entiers
    - on dit `float` pour un nombre a virgule
    - on dit `double` pour les nombre a 2 décimales
        ```lua
        local int = 548
        local float = 230.1257
        local double = 23.15
        ```

- Les `boolean` *(bool)* valeur vrai/faux
    - deux valeurs existent seulement false ou true cela s'écrit sans guillemets
        ```lua
        local boolean = false
        local bool = true
        ```
- `nil` qui sert a initialiser une variable vide
    - On l'utilise souvent quand on souhaite changer sa valeur plus tard dans le code
        ```lua
            local isChecked = nil
            -- Tu comprendras lors des conditions a quoi sert cette valeur
        ```

## La concaténation
- La concaténation permet de mettre ensemble plusieurs données de type `string` afin de n'en faire qu'une seule
- en Lua la concaténation se fait soit avec:
    - les caratères ` .. `
    - la methode `string.format(string, values)`

- Tu remarqueras dans les exercices que j'ai pu fabriquer des `result` sur base d'une phrase en integrant les variables, c'est ça la concaténation
    ex:
    ```lua
    local monPrenom = "Stephan"
    local result = "Mon prénom est " .. monPrenom
    print(result)
    ```
- Tu as remarqué que j'ai laissé un espace après le mot `est` ?
    - Cet espace c'est l'espace entre le mot `est` et la variable `monPrenom`
    - sans cet espace la console renvoie `Mon prénom estStephan`
- Une autre manière consiste a definir l'espace tout seul
    ex:
    ```lua
    
    local monPrenom = "Stephan"
    local result = "Mon prénom est" .. " " .. monPrenom
    print(result)
    ```
- Grace a ceci ` .. " " .. ` nous avons donc créer un espace entre les mots

- Exemple maintenant de string.format()
    ex:
    ```lua
    local monPrenom = "Stephan"
    local result = string.format("Mon prénom est %s", monPrenom)
    print(result)

## Les opérateurs
- Ils permettent simplement de calculer des int et floats
    - Additionner: `+`
    - Soustraire: `-`
    - Multiplier: `*`
    - Diviser: `/`
    - Modulo: `%` (renvoie le reste d'une division)
        ex:
        ```lua
        local addition = 2 + 1
        local soustraction = 10 - 1
        local division = 10 / 2
        local multiplication = 12 * 3
        local modulo = 11 / 2
        
        local result = string.format("addition = %s \nsoustraction = %s\ndivision = %s\nmultiplication = %s\nmodulo = %s", addition, soustraction, division, multiplication, modulo)

        print(result)
        ```
        
        - La console renvoie:

        ```plaintext
        addition = 3 
        soustraction = 9
        division = 5.0
        multiplication = 36
        modulo = 1
        ```
## **Petite pause théorique**, pensons à s'exercer.
- Il faut savoir que le code ça s'apprend un peu mais surtout ça se pratique plus tu tape plus tu retiens
  - pour cet exercice je vais t'apprendre la methode `print()`
  - c'est ce qu'on appelle une fonction integrée/native elle fait parti de la syntaxe du Lua basique
  - cette methode permet d'afficher un message dans la console (utile pour le debug et log)

- Tu vas pouvoir executer ton code sur [tools-online lua](https://www.tools-online.app/tools/lua) *<= clique ici*

    ### Exercice 1
    - a) Pour le premier exercice tu vas créer une variable `monNom` *(C'est important de l'ecrire comme ça je t'expliquerais plus tard)*
    - b) La variable contiendra la valeur sous forme de `string` car ce sera un/des mots.
    - c) Ensuite tu pourras afficher dans la console le resultat de ta variable
    - d) Petit bonus commente ton code si tu comprends ce que tu fais
        #### Ex: 
        ```lua
        -- Variable contenant mon nom
        local monNom = "Stephan M."

        --[[
            print() la variable `monNom`
            cequi affiche la valeur `Stephan M.` dans la console.
        ]]
        print(monNom)
        ```
        - La console affiche: `Stephan M.`

    ### Exercice 2
    - a) Pour celui là on va devoir calculer le résultat ton age + mon age divisé par 2 (xD ça sert strictement à rien!)
    - b) J'ai préparé un petit bout de code que tu vas remplir et executer
    - c) Imprime la valeur du résultat dans la console
        #### Ex:
        ```lua
        local neoAge = 34
        --[[ajoute ta variable]]

        local totalAge = ((neoAge + --[[ta clé]]) / 2)

        local result = ("La moitié de nos deux age réuni est de " .. totalAge .. " années.")

        --[[print la valeur du résultat]]
        ```
    ### Exercice 3
    - a) J'ai préparé une variable `result` tu vas devoir fabriquer les variables et leurs valeurs
      - prenom, nom, age
    - b) Tu vas devoir imprimer le résultat sur la console
    - c) Comment le code pour savoir ce qui a été fait et pourquoi
        #### Ex:
        ```lua
        -- J'ai utilisé la methode string.format (tu l'apprendras plus tard ^^) les variables sont après la `string`
        local result = string.format("L'utilisateur s'appelle %s %s, et a %s âge", prenom, nom, age)
        ```

    ### Exercice 4
    - a) Grace aux variables, aux concaténations, aux opérateurs et a print() fabrique un script entier qui:
    - b) Calcule ton age + 12 et renvoie "Si j'avais 12 ans en plus, j'aurais X ans"
    - c) Imprime ton nom + prenom + animal préféré dans une phrase logique.
    - d) Commente ton code
      - pour cet exercice je ne fournis pas de code, penses a stocker dans les variables pour plus de clareté
