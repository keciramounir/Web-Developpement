# Les Boutons HTML : Tout ce qu'il faut savoir 🔘

Les boutons en HTML sont des éléments interactifs permettant à l'utilisateur d'effectuer des actions. Ils sont utilisés pour soumettre des formulaires, interagir avec des scripts JavaScript, ou encore pour des actions simples telles que fermer une fenêtre ou démarrer une animation.

---

## Sommaire 🗂️

1. [Qu'est-ce qu'un bouton ?](#quest-ce-quun-bouton)
2. [Types de boutons](#types-de-boutons)
3. [Propriétés des boutons](#proprietes-des-boutons)
4. [Événements associés aux boutons](#evenements-associes-aux-boutons)
5. [Boutons avec CSS et JavaScript](#boutons-avec-css-et-javascript)
6. [Exemples pratiques](#exemples-pratiques)
7. [Accessibilité des boutons](#accessibilite-des-boutons)

---

## 1. Qu'est-ce qu'un bouton ? 🔲

Un bouton est un élément HTML utilisé pour déclencher une action. Il est défini avec l'élément `<button>`, ou parfois avec un lien `<a>` ou un élément `<input>` de type `button`. Il peut être stylisé, personnalisé et même animé.

### Syntaxe de base d'un bouton

```html
<button>Cliquer ici</button>
```

Les boutons peuvent être placés dans des formulaires pour soumettre des données, ou dans des pages pour lancer des scripts.

---

## 2. Types de boutons 🔘

En HTML, il existe plusieurs types de boutons, chacun ayant un comportement spécifique :

- **`<button>`** : Utilisé pour créer un bouton standard.

  ```html
  <button type="button">Cliquer</button>
  ```

- **`<input type="button">`** : Crée un bouton, mais ne permet pas de soumettre un formulaire.

  ```html
  <input type="button" value="Soumettre" />
  ```

- **`<input type="submit">`** : Permet de soumettre un formulaire.

  ```html
  <form>
    <input type="submit" value="Envoyer" />
  </form>
  ```

- **`<input type="reset">`** : Réinitialise un formulaire.

  ```html
  <form>
    <input type="reset" value="Réinitialiser" />
  </form>
  ```

- **`<button type="submit">`** : Soumet un formulaire.

  ```html
  <form>
    <button type="submit">Envoyer</button>
  </form>
  ```

- **`<button type="reset">`** : Réinitialise un formulaire.

  ```html
  <form>
    <button type="reset">Réinitialiser</button>
  </form>
  ```

---

## 3. Propriétés des boutons ⚙️

Les boutons en HTML ont plusieurs propriétés que l'on peut manipuler pour améliorer leur interactivité et personnalisation.

### Attributs de base

- **`type`** : Détermine le comportement du bouton. Les valeurs possibles sont :

  - `"button"` : Un bouton classique.
  - `"submit"` : Un bouton pour soumettre un formulaire.
  - `"reset"` : Un bouton pour réinitialiser un formulaire.

- **`name`** : Nom du bouton, utile dans les formulaires.

- **`value`** : Définit la valeur envoyée lors de la soumission du formulaire.

- **`disabled`** : Désactive le bouton pour éviter son utilisation.

  ```html
  <button disabled>Non disponible</button>
  ```

### Style des boutons

- **`class`** : Permet d’ajouter des classes CSS pour styliser le bouton.

  ```html
  <button class="btn-primary">Stylisé</button>
  ```

- **`id`** : Utilisé pour identifier le bouton, par exemple pour le cibler avec JavaScript.

  ```html
  <button id="myButton">Cliquez-moi</button>
  ```

---

## 4. Événements associés aux boutons 🎯

Les boutons peuvent être associés à différents événements pour effectuer des actions.

### Exemple d'événements JavaScript :

```html
<button onclick="alert('Bouton cliqué!')">Cliquez-moi</button>
```

- **`onclick`** : Déclenche un événement lorsqu'un utilisateur clique sur le bouton.
- **`onmouseover`** : Déclenche un événement lorsque la souris survole le bouton.
- **`onfocus`** : Déclenche un événement lorsque le bouton prend le focus.
- **`onblur`** : Déclenche un événement lorsque le bouton perd le focus.

---

## 5. Boutons avec CSS et JavaScript ✨

Les boutons peuvent être stylisés en utilisant CSS pour leur donner une apparence personnalisée, et peuvent être rendus interactifs avec JavaScript.

### Exemple de style avec CSS :

```html
<button class="btn-style">Cliquez-moi</button>
```

```css
.btn-style {
  background-color: #4caf50; /* Vert */
  color: white;
  padding: 15px 32px;
  text-align: center;
  font-size: 16px;
  border: none;
  cursor: pointer;
}

.btn-style:hover {
  background-color: #45a049;
}
```

### Exemple avec JavaScript :

```html
<button id="clickBtn">Cliquez ici</button>

<script>
  document.getElementById("clickBtn").addEventListener("click", function () {
    alert("Bouton cliqué!");
  });
</script>
```

---

## 6. Exemples pratiques 🖥️

- **Bouton qui soumet un formulaire** :

  ```html
  <form action="/submit_form" method="POST">
    <button type="submit">Soumettre</button>
  </form>
  ```

- **Bouton avec effet de survol** :

  ```html
  <button class="hover-effect">Survolez-moi</button>
  ```

  ```css
  .hover-effect {
    background-color: #3498db;
    color: white;
    padding: 10px 20px;
    border: none;
  }

  .hover-effect:hover {
    background-color: #2980b9;
  }
  ```

---

## 7. Accessibilité des boutons ♿

Les boutons doivent être accessibles à tous les utilisateurs, y compris ceux ayant des handicaps. Voici quelques bonnes pratiques :

- **Texte alternatif clair** : Le texte du bouton doit décrire clairement l'action qu'il déclenche.

- **`aria-label`** : Utilisé pour fournir une étiquette plus descriptive pour les technologies d'assistance.

  ```html
  <button aria-label="Soumettre le formulaire">Envoyer</button>
  ```

- **Navigation au clavier** : Assurez-vous que les boutons sont accessibles via la touche **Tab** et peuvent être activés avec **Entrée**.

- **Couleurs contrastées** : Utilisez des couleurs qui offrent un bon contraste pour les personnes malvoyantes.

---

## Conclusion 📝

Les boutons en HTML sont des éléments essentiels pour rendre un site interactif. Ils sont personnalisables à l'aide de HTML, CSS et JavaScript, et peuvent être rendus accessibles et responsives pour une meilleure expérience utilisateur.

---

📚 **Références** :

- [MDN Web Docs - HTML Button](https://developer.mozilla.org/fr/docs/Web/HTML/Element/button)
- [W3C - Accessibilité des formulaires](https://www.w3.org/WAI/WCAG21/Techniques/general/G207.html)
