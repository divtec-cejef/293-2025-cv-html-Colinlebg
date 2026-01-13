## A) Ajouter une taille de texte en `px` (exigence de l’exercice)

Actuellement, vos tailles de texte sont surtout en `rem` et `em`.
Ajoutez **au moins un texte** en `px`, par exemple sur `h1` ou `h2`.

Exemple :
```
h1 {
font-size: 32px;
}
```

💡 *On vous demande de montrer que vous savez utiliser `px`, `em` et `rem`.*

---

## B) Ajouter une police personnalisée avec `@font-face` (obligatoire)

Il manque la partie `@font-face`.
Vous devez télécharger une police (fichiers `.woff2` idéalement) et la mettre dans `fonts/`, puis la charger.

Exemple :
```
@font-face {
font-family: "MaPolice";
src: url("../fonts/mapolice.woff2") format("woff2");
font-weight: 400;
font-style: normal;
}

body {
font-family: "MaPolice", monospace;
}
```

💡 *Avec `@font-face`, votre CV garde la même police même sans Internet.*

> Petit rappel : depuis `css/main.css`, on remonte souvent avec `../fonts/...`.

---

## C) Mettre un `padding` sur le `header` (consigne)

Vous avez du padding sur `.logo`, mais l’exercice demande une **marge intérieure sur `header`**.

Exemple :
```
header {
padding: 20px;
}
```

💡 *Le `padding` donne de “l’air” autour du contenu, c’est plus agréable visuellement.*

---

## D) Navigation : éviter les gros `padding-left: 15rem`

Actuellement :
```
nav ul {
padding-left: 15rem;
}
```

Ça dépend trop de la taille d’écran et ça décale fort la navigation.
Préférez un centrage simple :

```
nav ul {
padding: 0;
margin: 0;
display: flex;
justify-content: center;
gap: 20px;
list-style: none;
}
```

💡 *`flex + justify-content: center` centre correctement sur toutes les tailles d’écran.*

---

## E) Images : `width: auto` est inutile ici

Vous avez :
```
img {
max-width: 100%;
height: auto;
width: auto;
}
```

Avec `max-width: 100%` et `height: auto`, `width: auto` n’apporte rien (valeur par défaut).
Vous pouvez simplifier :

```
img {
max-width: 100%;
height: auto;
}
```

💡 *Moins de CSS = plus lisible, plus facile à maintenir.*

--
