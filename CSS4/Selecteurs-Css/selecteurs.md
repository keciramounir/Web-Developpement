## 🎨 1. Sélecteurs de base

### a. Sélecteur universel `*`

```css
* {
  margin: 0;
  padding: 0;
}
```

```html
<p>Tout commence sans marge ni padding.</p>
```

---

### b. Sélecteur de balise (type)

```css
h1 {
  color: blue;
}
```

```html
<h1>Titre en bleu</h1>
```

---

### c. Sélecteur de classe `.ma-classe`

```css
.important {
  font-weight: bold;
  color: red;
}
```

```html
<p class="important">Texte important en rouge gras</p>
```

---

### d. Sélecteur d’ID `#mon-id`

```css
#accueil {
  background-color: lightgreen;
}
```

```html
<div id="accueil">Zone d'accueil</div>
```

---

### e. Sélecteur balise+classe

```css
p.note {
  color: orange;
}
```

```html
<p class="note">Paragraphe de type note</p>
```

---

## 🔗 2. Sélecteurs combinés

### a. Sélecteur descendant `A B`

```css
article p {
  color: darkgray;
}
```

```html
<article>
  <p>Ce paragraphe est dans un article</p>
</article>
```

---

### b. Sélecteur enfant direct `A > B`

```css
ul > li {
  list-style-type: square;
}
```

```html
<ul>
  <li>Item direct</li>
</ul>
```

---

### c. Sélecteur frère immédiat `A + B`

```css
h2 + p {
  color: green;
}
```

```html
<h2>Sous-titre</h2>
<p>Ce paragraphe suit directement le h2</p>
```

---

### d. Sélecteur frères généraux `A ~ B`

```css
h2 ~ p {
  font-style: italic;
}
```

```html
<h2>Sous-titre</h2>
<p>Ce paragraphe sera en italique</p>
<p>Lui aussi</p>
```

---

## 🔐 3. Sélecteurs d’attributs

### a. Avec type précis

```css
input[type="text"] {
  border: 1px solid black;
}
```

```html
<input type="text" /> <input type="password" />
```

---

### b. Attribut qui commence par une valeur `^=`

```css
a[href^="https"] {
  color: green;
}
```

```html
<a href="https://example.com">Lien sécurisé</a>
```

---

### c. Attribut qui se termine par une valeur `$=`

```css
img[src$=".jpg"] {
  border: 2px solid red;
}
```

```html
<img src="photo.jpg" />
```

---

### d. Attribut contenant une valeur `*=`

```css
div[class*="box"] {
  background: #eee;
}
```

```html
<div class="content-box"></div>
```

---

## 🧠 4. Pseudo-classes

### a. `:hover`

```css
button:hover {
  background-color: yellow;
}
```

```html
<button>Passe ta souris ici</button>
```

---

### b. `:first-child`

```css
ul li:first-child {
  color: red;
}
```

```html
<ul>
  <li>Premier</li>
  <li>Deuxième</li>
</ul>
```

---

### c. `:nth-child(n)`

```css
ul li:nth-child(2) {
  font-weight: bold;
}
```

```html
<ul>
  <li>Un</li>
  <li>Deux</li>
  <li>Trois</li>
</ul>
```

---

### d. `:not()`

```css
p:not(.info) {
  color: gray;
}
```

```html
<p class="info">Information</p>
<p>Autre paragraphe</p>
```

---

## 🎭 5. Pseudo-éléments

### a. `::before`

```css
p::before {
  content: "➤ ";
  color: blue;
}
```

```html
<p>Texte avec une flèche avant</p>
```

---

### b. `::after`

```css
p::after {
  content: " ✔";
  color: green;
}
```

```html
<p>Texte validé</p>
```

---

### c. `::first-line`

```css
p::first-line {
  text-transform: uppercase;
}
```

```html
<p>ceci est une première ligne stylée. Et voici le reste.</p>
```

---

### d. `::first-letter`

```css
p::first-letter {
  font-size: 200%;
  color: red;
}
```

```html
<p>La première lettre est grosse et rouge.</p>
```

---

## 🧾 6. Sélecteurs de groupe

```css
h1,
h2,
p {
  margin-bottom: 20px;
}
```

```html
<h1>Titre</h1>
<h2>Sous-titre</h2>
<p>Paragraphe</p>
```

---

---

## 🧩 Sélecteurs CSS **avancés ou spécifiques**

### 1. `:nth-of-type()` et `:last-of-type`

Ciblent un élément parmi les éléments du **même type**.

```css
li:nth-of-type(2) {
  color: red;
}
```

---

### 2. `:only-child`

Cible un élément qui est l’unique enfant de son parent.

```css
p:only-child {
  background: lightblue;
}
```

---

### 3. `:empty`

Cible les éléments **sans contenu** (pas même un espace).

```css
div:empty {
  display: none;
}
```

---

### 4. `:checked`, `:disabled`, `:enabled`

Spécifiques aux **formulaires**.

```css
input:checked {
  border: 2px solid green;
}
```

---

### 5. `:required`, `:optional`, `:valid`, `:invalid`

Validation des champs :

```css
input:invalid {
  border-color: red;
}
```

---

### 6. `:is()` (nouveau, CSS4+)

Simplifie les groupes complexes :

```css
:is(h1, h2, h3) {
  color: purple;
}
```

---

### 7. `:where()` (comme `:is` mais avec **0 de spécificité**)

```css
:where(header, footer, main) {
  margin: 0;
}
```

---

### 8. `::selection`

Cible le texte sélectionné par l'utilisateur.

```css
::selection {
  background: yellow;
  color: black;
}
```

---

### 9. `:has()` (support limité, très puissant)

Cible un élément **parent** selon ce qu’il contient.

```css
article:has(img) {
  border: 2px solid green;
}
```

⚠️ Pas encore supporté dans tous les navigateurs (mais arrive avec CSS Selectors Level 4).

---

## ✅ Conclusion

🎓 **Oui, la liste précédente + cette extension couvre TOUTES les familles de sélecteurs CSS :**

| Catégorie       | Exemples                             |
| --------------- | ------------------------------------ |
| De base         | `*`, `div`, `.class`, `#id`          |
| Combinés        | `>`, `+`, `~`, descendant            |
| Attributs       | `[type="text"]`, `[href^="https"]`   |
| Pseudo-classes  | `:hover`, `:nth-child()`, `:not()`   |
| Pseudo-éléments | `::before`, `::after`, `::selection` |
| Avancés CSS4    | `:is()`, `:where()`, `:has()`        |

---

-
