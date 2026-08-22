# Les conditions avancées
Nous y voilà on a vu tout les type de données, les opérateurs, les opérateurs de comparaisons, les conditions de base
Maintenant je vais vous expliquer les conditions un peu plus en détail en mélangeant un peu tout ce qu'on vient de voir

## Plusieurs conditions
- Imaginons que nous devions vérifier plusieurs choses sur la même variable

    ex:
    ```lua
    local variable = "france"

    if variable == true then
        if variable == "france" then
            print("FRANCE")
        end
    end
    ```
- Pas très pratique si je devais aussi verifier d'autres choses *(surtout avec les `tables` et `listes` que nous verrons juste avant les fonctions)* on a de la chance les créateurs du code Lua y ont pensé et grace aux `opérateurs logiques` qu'on a vu plus tôt dans le cours on va pouvoir verifier les deux en même temps

    ex:
    ```lua
    local variable = "france"

    if variable == true and variable == "france" then
        print("FRANCE")
    end
    ```

## Not condition
- il est possible de verifier si quelque chose "n'est pas" avec not
- je vais de suite montrer un exemple qui parlera plus que moi:

    ex:
    ```lua
    local variable = false

    if not variable then
        print("test reussi")
    end
    ```

## True condition
- Vous remarquerez aussi que devoir ecrire `if variable == true` c'est vite long et redondant
- la aussi les créateurs y ont pensé
- il suffit de juste faire l'inverse du not:

    ex:
    ```lua
    local variable = false

    if variable then
        print("test reussi")
    end
    ```
- ce qui rendrait notre premier code beaucoup plus clair
    ex:
    ```lua
    -- la variable
    local variable = "france"
    -- SI variable est "true" ET QUE variable EGAL "france" ALORS
    if variable and variable == "france" then
        -- Imprime "FRANCE"
        print("FRANCE")
    end
    ```

- AVANT/APRES

    ex:
    ```lua
    local variable1 = "france"
    if variable1 == true then
        if variable1 == "france" then
            print("FRANCE")
        end
    end
    ```


    ```lua
    local variable2 = "belgique"
    if variable and variable == "belgique" then
        print("BELGIQUE")
    end
    ```

## Un gros exemple
- je vais utiliser des choses que nous n'avons pas encore vu concentrez vous sur les conditions:
```lua
    -- datas est nil par defaut
    local datas = nil

    -- on imagine recevoir ces données de l'utilisateur
    -- (si on enleve ce bloc on declanche l'erreur principale)
    -- (si on passe a false une valeur du tableu on declanche la deuxieme erreur)
    datas = {
        firstname = "Stephan",
        lastname = "M.",
        dob = "XX/01/1992",
        mail = false
    }

    -- SI data est "false" ALORS
    if not datas then
        print("SCRIPT ERROR: Aucune donnée reçue")
        -- arrête la lecture du script
        return
    end

    -- Pour chaque donnée dans la table (donc firstname, lastname, etc..)
    for key, value in pairs(datas) do
        if not value then
            print(string.format("SCRIPT ERROR: la clé %s, n'a pas de valeur", key))
        end
    end
```

## Suite du cours
- Vous pouvez tester le code dans [tools-online](https://www.tools-online.app/)
- Pour la suite rendez vous aux listes et tableaux en **cliquant ici**