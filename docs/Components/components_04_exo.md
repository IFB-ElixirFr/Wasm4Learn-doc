```
::Exo
---
consigne: "Recherchez toutes les fonctions dont le nom contient 'file' (*i.e* fichier). Attention 'file' doit être entre guillemets."
tips: En informatique on parle de guillemets simples ou simples guillemets pour faire référence  à l'apostrophe (' '). On parle de guillemets doubles ou doubles guillemets pour faire référence au guillemets (" "). Cette appellation nous vient du monde anglo-saxon (*single quote* et *double quote*). Dans le langage R, les deux formes ont la même signification et permettent de désigner une suite de caractères qu'on appelle *chaîne de caractères* (ici 'file' ou "file"). Cela permet une certaine flexibilité si une chaîne de caractères contient un guillemet simple par exemple (*e.g.* x <- "extrémités 5' et 3' des molécules d'ADN").
solution: apropos("file")
---
::
```