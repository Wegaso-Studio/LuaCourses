# Exercices

## 1) Verifier la majorité
- Ecrire un code permettant de verifer la majorité d'un utilisateur
- vous devez:
  - créer une variable pour l'age et mettre une valeur
  - créer une condition qui vérifie si la personne à minimum 18 ans ou plus
  - Si oui afficher `"Vous pouvez accéder au casino, bienvenue"`
  - Sinon afficher `"Vous ne pouvez pas accéder au casino, faites demi-tour"`
  - Commente ton code en Pseudo code

## 2) Verifier une Entrée utilisateur
- Ecrire un code permettant de vérifier si l'utilisateur a bien entré une valeur
- vous devez:
  - créer une variable avec la valeur `false` ou `nil`
  - créer une condition qui vérifie si la variable est false
  - Si oui afficher une erreur `"SCRIPT ERROR: L'utilisateur n'a pas entré de valeur"`
  - Si l'utilisateur à entré une valeur à la place de `false` ou `nil` faites ce que vous voulez et testez avec une valeur positive.
  - Commentez votre code (cette fois decrivez ce que fais le code et non en pseudo code)

## 3) Verifier si c'est un chien ou un chat
- Ecrire un code permettant de verifier si c'est un animal sauvage ou de compagnie
- vous devez:
  - créer une variable et mettre `"chat"` ou `"chien"` comme valeur
  - créer une double condition
  - Si la valeur est `"chien"` OU que la valeur est `"chat"` afficher `"C'est un animal de compagnie"`
  - Sinon afficher `"C'est un animal sauvage"`
  - Decrivez encore votre code en commentaire

## 4) Verifier si le calcul est bon
### *(quelques tips que nous n'avons pas vu avant sont expliqués dans cet exercice)*
- Ecrire un code qui va vérifier si le calcul est bon
- vous devez:
  - créer trois variables `num1` `num2` et `userEntry`
  - `num1 = 2` & `num1 = 3`
  - créer une condition qui vérifie SI `num1 + num2` est EGAL à `userEntry`
  - Si oui afficher `"Bonne réponse!"`
  - Sinon afficher `"Dommage, recommencez.."`
  - Decrivez encore votre code en commentaire

- TIPS:
  - les variables peuvent etre definies à la chaine

    ex:
    ```lua
    local firstname, lastname, age = "Martin", "Stephan", 34
    ```
  - Les conditions peuvent recevoir des calculs

    ex:
    ```lua
    if (3 * 2) == 6 or (3 * 2) == (3 + 3) then
        print("3x2=6")
    end
    ```
    <details><summary>Tu es vraiment bloqué ? déroules ici pour des indices</summary>

    ```lua
    -- ## LA PARTIE VARIABLE TIPS 1 ## --
    local num1, num2 = 3, 2


    -- ## LA PARTIE CONDITIONS TIPS 2 ## --
    if (num1 + num2) == userEntry then
        -- Ton code
    end

    -- ## LA PARTIE CONDITIONS TIPS 2 + Variable ## --
    local sum = num1 + num2

    if sum == userEntry then
        -- Ton code
    end

    ```

    <details><summary>Toujours bloqué? Réponse complète ici</summary>

    ```lua
    -- Initialisation des variables pour `num1` & `num2`
    local num1, num2 = 3, 2
    -- Initialisation de la variable pour l'entrée utilisateur
    local userEntry = 5
    -- Somme des deux variables `num`
    local sum = num1 + num2

    -- si l'utilisateur a entré la bonne somme comparé a (num1 + num2)
    if sum == userEntry then
        -- Imprime la réponse correcte
        print("Bonne réponse!")
    -- sinon
    else
        -- Imprime la réponse inccorrecte
        print("Dommage, recommencez..")
    end
    ```
    </details>
    </details>