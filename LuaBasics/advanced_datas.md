## Type de données avancé
- La valeur vrai faux est plus présente qu'on le pense
    - toutes les valeurs nil/false sont false 
    - toutes les autres valeurs sont toujours true

- Je vais mieux exprimer la chose avec un exemple:
    ```lua
    local variable = "mon nom"

    if variable == true then
        print("variable est true")
    end
    ```
- c'est la même chose pour les chiffres
    ```lua
    local number = 15
    if number == true then
        print("number est true")
    end
    ```

- Mais attention contrairement a ce qu'on pourrait croire:
    ```lua
    local number = 0 -- est true
    local variable = "" -- est true
    ```
    *comme je le disais seuls false et nil sont concidéré comme false*

## Comparaisons avancées
- Comparer false ou true sur une string ou un number peut etre interessant dans certaines logiques de verification

    ex:
    ```lua
    local userEntry = nil

    if userEntry == true then
        print("SCRIPT SUCCESS: Le formulaire a été envoyé")
    else
        print("SCRIPT ERROR: Le formulaire n'a pas été envoyé")
    end
    ```
    *la console dira que le formulaire n'a pas été envoyé car `nil = false`*

    ```lua
    local country = "charleroi" -- optionnel
    local state = "Hainaut" -- optionnel
    local postalCode = nil -- obligatoire

    if postalCode == false then
        print("Erreur!, vous devez au minimum entrer le code postal")
    else
        -- Fonction spacimen (ceci n'existe pas j'expliquerais les functions plus tard)
        CreateData(country, state, postalCode)
    end
    ```
