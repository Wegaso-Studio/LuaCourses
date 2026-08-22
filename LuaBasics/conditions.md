# Les conditions
- C'est là que tout ce qu'on vient de voir va commencer a prendre forme
- Nous voilà dans la partie interessante du cours 
- Ici on va pouvoir effectuer nos `print()` sous conditions.

## Structure
- pseudo code:
    ```
    SI variable est (true) ALORS
        imprime "test reussi - true"
    ET SI variable est (false) ALORS
        imprime "test reussi - false"
    FIN
    ```

- de manière logique nous n'allons pas creer cette redondance si variable est (true) elle ne peut pas etre (false) et inversément
- alors on va faire ceci
    ```
    SI variable est (true) ALORS
        imprime "test reussi - true"
    SINON
        imprime "test reussi - false"
    FIN
    ```

- Il sera possible de créer tant qu'on veut:
  - *SI, ET SI, ET SI, ET SI, ET SI, SINON FIN*

- en lua on utilisera les nommages suivants pour exprimer les conditions
  - `if` : Si (condition)
  - `elseif`: Et si (condition)
  - `else`: sinon (condition)
  - `then`: alors (jamais de `then` après un `else`)

- Reprenons notre exemple final en pseudo code et transformons le en lua grace à tout ce qu'on a appris jusque là:
  ```lua
    local variable = true

    if variable == true then
        print("test reussi - true")
    else
        print("test reussi - false")
    end
  ```
  *tu peux essayer de le code dans ton editeur en ligne et changer true false pour voir la difference et mieux comprendre le code*

- les conditions peuvent aussi s'effectuer de plusieurs manière comme vous avez vu dans les `opérateurs de comparaisons`
  - plus,
  - moins,
  - égal,
  - plus et égal,
  - moins et égal

- Alors voici comment les utiliser on va comparer des valeurs de différents type pour y voir plus clair
  - string:
    ```lua
        -- Ici c'est l'entrée utilisateur vous pourrez essayer d'entrer "mot"
        local userEntry = ""
        -- si vous changez le mot à trouver, userEntry devra correspondre
        local word = "mot"

        -- SI l'entrée utilisatuer est EGAL au mot qu'il faut trouver ALORS
        if userEntry == word then
            -- Imprime la réussite
            print("Succès, vous avez trouvé le bon mot")
        -- SINON
        else
            -- Imprime la défaite
            print("Erreur, reesayez...")
        end
    ```
  - numbers:
    ```lua
        -- Changez nil par votre âge
        local userAge = nil
        -- Âge requis
        local ageRequired = 18

        -- SI l'âge de l'utilisateur est PLUS-GRAND OU EGAL à l'âge requis  
        if userAge >= ageRequired then
            -- Imprime la majorité
            print("L'utilisateur est majeur")
        -- SINON
        else
            -- Imprime la minorité
            print("L'utilisateur est mineur")
        end
    ```
  - boolean:
    ```lua
        local variable = true

        if variable == true then
            print("test reussi - true")
        else
            print("test reussi - false")
        end
    ```

## Avant de passer à la suite des conditions !
- J'aimerais repasser sur les `types de données` mais plus particulièrement sur les `boolean` et le `nil`
- [Cliquez ici](https://github.com/Wegaso-Studio/LuaCourses/blob/main/LuaBasics/advanced_datas.md) pour la suite.
