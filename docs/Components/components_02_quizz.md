## Simple

```
::Quiz
---
question: "Il est conseillé d'utiliser l'opérateur '=' plutôt que '<-' pour l'assignation ?"
type: simple
choices:
    -   value: "oui"
        valid: false
    -   value: "non"
        valid: true
---
::
```

## Multiple

```
::Quiz
---
question: "Dans la question précédente, pourquoi faut-il mettre *file* entre guillemets et écrire apropos('file') et non pas apropos(file)"
type: multiple
choices:
    -   value: "Parce que *file* sans guillemet sous-entendrait qu'il existe en mémoire un objet nommé *file*."
        valid: true
    -   value: "Parce que le premier argument de la fonction *apropos()* doit obligatoirement être un chaîne de caractère."
        valid: true
---
::
```
