## A) Balises <p> dans les <li>

Vous avez des `<p>` à l'intérieur des `<li>`

Ce n'est pas faux car HTML l'autorise mais ça ne fait pas de sens d'un point de vue sémantique. Vos <li> contiennent qu'une seule phrase, dans le cadre d'un CV comme ceci, le <li> fait déjà office de texte, donc c'est suffisant, ça surcharge moi.

---

## B) Ajouter une taille de texte en `px` (exigence de l’exercice)

Vous utilisez `rem` et `em`, mais il manque une taille en `px` pour un texte.

Exemple :
```
h1 {
font-size: 32px;
}
```

💡 *On vous demande de montrer que vous savez utiliser `px`, `em` et `rem`.*

---

## C) Ajouter une police personnalisée avec `@font-face` (obligatoire)

Il manque une vraie police via `@font-face`.
Téléchargez une police (idéalement `.woff2`) et mettez-la dans `fonts/`.

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

💡 *Avec `@font-face`, la police fonctionne même sans Internet (contrairement à Google Fonts).*

---

## D) Mettre un `padding` sur le `header` (consigne)

L’exercice demande une marge intérieure sur le header (pas seulement sur `.logo`).

Exemple :
```
header {
padding: 20px;
}
```

💡 *Le `padding` ajoute de l’espace “à l’intérieur” du bloc → plus lisible et plus propre.*

---

## E) Mettre une marge extérieure au `footer` (consigne)

Ajoutez une marge extérieure au footer.

Exemple :
```
footer {
margin-top: 30px;
}
```

💡 *La `margin` sépare les blocs entre eux, alors que le `padding` espace le contenu à l’intérieur.*

---

## F) Navigation : éviter `padding-left: 15rem` (pas responsive)

Vous avez :
```
nav ul {
padding-left: 15rem;
}
```

Ça décale beaucoup selon la taille d’écran.
Préférez un centrage au lieu de “pousser” avec du padding.

Exemple :
```
nav ul {
list-style: none;
padding: 0;
margin: 20px 0 0;
display: flex;
justify-content: center;
gap: 20px;
}
```

💡 *`flex + justify-content: center` centre le menu sur toutes les tailles d’écran.*

---

## G) Images : `width: auto` inutile ici

Vous avez :
```
img {
max-width: 100%;
height: auto;
width: auto;
}
```

`width: auto` est la valeur par défaut, donc vous pouvez simplifier :

```
img {
max-width: 100%;
height: auto;
}
```

💡 *Moins de CSS = plus simple à lire et à maintenir.*

* 📱 Responsive : le menu reste-t-il lisible sur petit écran ?
* ✅ Validateur W3C : pas d’erreurs HTML/CSS après correction de l’accolade en trop
