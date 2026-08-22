# Initiation au lua:

## 1 - Les commentaires
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

## 2 - Les variable
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

## 3 - Les valeurs de base
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
        - Tu remarque que la syntaxe affiche une différence après " l' " c'est parceque le code pense que la string s'arrête à 'l' tout le reste n'est pas compris ecureuil' erreur de syntaxe
        - Comment faire haaaa! Ok on utilise le fameux antislash devant le caractère qu'on veut annuler (c'est le `caractère d'annulation*`)
      
        ex: 
        ```lua
        local maStringReparee = 'l\'ecureuil'
        ```

    - Petit bonus grace à l'antislash on va pouvoir effectuer certaines actions comme retourner a la ligne avec `\n` dans une string
    
        ex:
        ```lua
        local str = "Voici ma longue phrase,\n Je l'ai donc coupé en deux avec \\n"
        ```

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

## 4 - La concaténation
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

## 5 - Les opérateurs
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

## Petit break sur la théorie..!
- [Clique ici pour aller aux exercices](https://github.com/Wegaso-Studio/LuaCourses/blob/main/LuaBasics/initiation_exercises.md)
