# Exercices d'initiation

- Il faut savoir que le code ça s'apprend un peu mais surtout ça se pratique plus tu tape plus tu retiens
  - pour cet exercice je vais t'apprendre la methode `print()`
  - c'est ce qu'on appelle une fonction integrée/native elle fait parti de la syntaxe du Lua basique
  - cette methode permet d'afficher un message dans la console (utile pour le debug et log)

- Tu vas pouvoir executer ton code sur [tools-online lua](https://www.tools-online.app/tools/lua) *<= clique ici*

## Exercice 1
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

## Exercice 2
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
## Exercice 3
- a) J'ai préparé une variable `result` tu vas devoir fabriquer les variables et leurs valeurs
  - prenom, nom, age
- b) Tu vas devoir imprimer le résultat sur la console
- c) Comment le code pour savoir ce qui a été fait et pourquoi
    #### Ex:
    ```lua
    -- J'ai utilisé la methode string.format (tu l'apprendras plus tard ^^) les variables sont après la `string`
    local result = string.format("L'utilisateur s'appelle %s %s, et a %s âge", prenom, nom, age)
    ```

## Exercice 4
- a) Grace aux variables, aux concaténations, aux opérateurs et a print() fabrique un script entier qui:
- b) Calcule ton age + 12 et renvoie "Si j'avais 12 ans en plus, j'aurais X ans"
- c) Imprime ton nom + prenom + animal préféré dans une phrase logique.
- d) Commente ton code
  - pour cet exercice je ne fournis pas de code, penses a stocker dans les variables pour plus de clareté


## Tu as terminé et tu veux passer à la suite ?
- [Cliques ici](https://github.com/Wegaso-Studio/LuaCourses/blob/main/LuaBasics/comparaisons.md) pour voir le cours sur les comparaisons