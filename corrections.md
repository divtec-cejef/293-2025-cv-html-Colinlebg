## A) Remettre les sections dans `<main>`
- Vos sections (`<section>...</section>`) sont placées après `</main>`
- Veuillez mettre toutes les sections (expérience, compétences, formation) à l’intérieur de `<main>`
- Structure attendue :
```
<main>
  <h1>...</h1>
  <section id="experience">...</section>
  <section id="competences">...</section>
  <section id="formation">...</section>
</main>
```

## B) Photo dans le header : lien cliquable correct
- Votre lien de photo pointe vers `#` (cela ne fait rien)
- Veuillez faire en sorte que le clic ouvre l’image dans un nouvel onglet
- Exemple :
```
<a href="./img/ColinVogt.png" target="_blank" rel="noopener noreferrer">
  <img src="./img/ColinVogt.png" alt="Photo de Colin Vogt">
</a>
```
- (Adaptez le nom du fichier à votre vrai fichier)

## C) Ajouter l’e-mail dans le footer (mailto)
- Le footer doit contenir `&copy;2025` + votre e-mail cliquable
- Exemple :
```
<footer>
  &copy;2025 Colin Vogt —
  <a href="mailto:prenom.nom@email.com">prenom.nom@email.com</a>
</footer>
```

## D) Lien externe : corriger `target` et ajouter la sécurité `rel`
- Votre lien externe utilise `target=_blank` sans guillemets
- Veuillez écrire `target="_blank"` et ajouter `rel="noopener noreferrer"`
- Exemple :
```
<a href="https://..." target="_blank" rel="noopener noreferrer">Lien</a>
```

## Autres
- Évitez les espaces/typos dans les noms de fichiers (source fréquente d’erreurs) (par exemple, votre logo)
- Rickroll son prof est dangereux, surtout quand on suit une formation qui dure **4 ans**
