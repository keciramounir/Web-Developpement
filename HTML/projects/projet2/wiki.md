# Documentation du projet « Mounir – Encyclopedia » 📖

Cette page HTML représente une fiche encyclopédique consacrée au prénom **Mounir**. Elle est structurée en plusieurs parties : en-tête (header), contenu principal (main), barre latérale (sidebar), et pied de page (footer). Le tout est mis en forme avec du CSS interne et le framework Tailwind CSS pour la grille et le flexbox.

---

## Sommaire 🗂️

1. [Structure HTML](#structure-html)
2. [Styles CSS](#styles-css)
3. [Explication du layout](#explication-du-layout)

---

## Structure HTML 🏗️

### 1. En-tête (`header`)

```html
<div class="header flex justify-between items-center">
  <div>
    <a href="#" class="logo">Encyclopedia</a>
  </div>
  <div>
    <input type="text" class="search-box" placeholder="Search Encyclopedia" />
    <button class="search-btn">Search</button>
  </div>
</div>
```

````

- **Logo** : lien `<a>` stylisé en Times New Roman pour évoquer un style « traditionnel ».
- **Barre de recherche** : champ `<input>` + bouton `<button>` pour rechercher dans l’encyclopédie.
- **Flexbox** (Tailwind : `flex justify-between items-center`) pour espacer la zone logo et la recherche.

---

### 2. Contenu principal (`main-content`)

```html
<div class="main-content">
  <h1>Mounir</h1>
  <div class="infobox">
    <div class="infobox-title">Mounir</div>
    <div class="infobox-image">
      <img src="https://via.placeholder.com/200x250" alt="Mounir" />
    </div>
    <div class="infobox-data">
      <span class="infobox-label">Prononciation :</span> moo-NEER
    </div>
    <!-- autres données… -->
  </div>
  <p>
    <strong>Mounir</strong> (Arabic : منير) est un prénom masculin d’origine
    arabe…
  </p>
  <!-- Table des matières et sections -->
</div>
```

- **Titre** (`<h1>`) : police serif pour un rendu formel.
- **Infobox** : encadré à droite (float \:right) qui présente image et informations clés (origine, sens, variations).
- **Paragraphe** : introduction au prénom.

---

### 3. Barre latérale (`sidebar`)

```html
<div class="sidebar">
  <div class="navbox">
    <div class="navbox-title">Related topics</div>
    <ul class="navbox-list">
      <li class="navbox-item"><a href="#">Arabic names</a></li>
      <!-- autres items… -->
    </ul>
  </div>
  <!-- autres navboxes… -->
</div>
```

- **Navbox** : boîtes contenant des liens vers des sujets connexes (noms arabes, racines sémitiques…).
- **Liste inline** (`.navbox-item:display inline`) avec séparateur `·` pour un affichage compact.

---

### 4. Table des matières (TOC)

```html
<div class="toc">
  <div class="toc-title">Contents</div>
  <ul class="toc-list">
    <li class="toc-level-1"><a href="#etymology">1 Etymology</a></li>
    <!-- sous-niveaux… -->
  </ul>
</div>
```

- **Encadré** pour la table des matières, positionné directement sous l’introduction.
- **Classes** `.toc-level-1` et `.toc-level-2` pour gérer l’indentation.

---

### 5. Pied de page (`footer`)

```html
<div class="footer">
  <p>Dernière modification : 15 octobre 2023, 14 :32 (UTC).</p>
  <p>Texte sous licence Creative Commons…</p>
</div>
```

- **Citations légales** : date de dernière édition et licence.
- **Style léger** avec bordure supérieure et fond clair.

---

## Styles CSS 🎨

```css
body {
  font-family: "Georgia", serif;
  background-color: #f6f6f6;
  margin: 0;
  padding: 0;
  display: flex;
  flex-direction: column;
  line-height: 1.6;
  color: #202122;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  background: #fff;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

.header {
  background: #f8f9fa;
  border-bottom: 1px solid #a7d7f9;
  padding: 0.5em 1em;
}

.logo {
  font-family: "Times New Roman", serif;
  font-size: 24px;
  font-weight: bold;
}

.search-box {
  border: 1px solid #a2a9b1;
  padding: 5px;
  width: 200px;
}

.search-btn {
  background: #f8f9fa;
  border: 1px solid #a2a9b1;
  padding: 5px 10px;
  cursor: pointer;
}

.content {
  display: flex;
  padding: 1em;
}

.main-content {
  flex: 1;
  padding-right: 1em;
}
.sidebar {
  width: 300px;
  padding-left: 1em;
  border-left: 1px solid #a7d7f9;
}

.infobox {
  border: 1px solid #a2a9b1;
  background: #f8f9fa;
  padding: 0.5em;
  font-size: 0.9em;
  float: right;
  margin: 0 0 1em 1em;
  width: 250px;
}

.toc {
  background: #f8f9fa;
  border: 1px solid #a2a9b1;
  padding: 0.5em 1em;
  display: inline-block;
  margin: 1em 0;
}

.footer {
  background: #f8f9fa;
  border-top: 1px solid #a7d7f9;
  padding: 1em;
  font-size: 0.9em;
  text-align: center;
}
```

- **Police serif** (`Georgia`, `Linux Libertine`) pour un aspect « encyclopédique ».
- **Flexbox** (`display: flex`) pour la mise en page en colonnes et rangées.
- **Encadrés** (`border`, `background`) pour distinguer les différentes boîtes (infobox, TOC, navboxes).
- **Float** pour positionner l’infobox à droite du texte.

---

## Explication du layout 📐

1. **Flexbox principal** :

   - Le conteneur `.container` utilise `display: flex; flex-direction: column;` pour empiler header → content → footer.

2. **Deux colonnes** :

   - Dans `.content`, `display: flex` crée deux zones côte à côte :

     - `.main-content` (flex: 1) occupe l’espace restant.
     - `.sidebar` a une largeur fixe de 300 px.

3. **Infobox flottante** :

   - Utilisation de `float: right` pour que l’infobox reste à droite du texte principal et que le paragraphe l’entoure.

4. **Responsive basique** :

   - Les largeurs max-width et flexibles garantissent que le contenu s’adapte aux écrans larges ou moyens.

---

✨ **Voilà !** Cette structure permet d’avoir une page claire, organisée, et facile à maintenir.
````
