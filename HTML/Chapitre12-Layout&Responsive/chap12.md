guide complet sur la **mise en page HTML** et le **design web responsive**, ainsi que d'un fichier HTML illustrant ces concepts.

# 🧱 Mise en page HTML et design web responsive

Ce projet présente les techniques de mise en page en HTML et les principes du design web responsive, permettant de créer des sites adaptables à tous les types d'écrans.

## 🧰 Techniques de mise en page HTML

### 1. Balises sémantiques

Utilisez des balises HTML5 pour structurer votre contenu :

- `<header>` : en-tête de la page
- `<nav>` : menu de navigation
- `<main>` : contenu principal
- `<section>` : section thématique
- `<article>` : contenu autonome
- `<aside>` : contenu complémentaire
- `<footer>` : pied de page

### 2. Techniques de mise en page CSS

- **Float** : méthode traditionnelle utilisant la propriété `float`.
- **Flexbox** : mise en page flexible en une dimension.
- **Grid** : mise en page en deux dimensions.
- **Frameworks CSS** : bibliothèques comme Bootstrap facilitant la création de mises en page réactives.

## 📱 Design web responsive

Le design web responsive permet à un site de s'adapter à différentes tailles d'écran.

### 1. Meta viewport

Ajoutez la balise suivante dans la section `<head>` de votre HTML :

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

### 2. Media queries

Utilisez des media queries pour appliquer des styles en fonction de la taille de l'écran :

```css
@media (max-width: 768px) {
  /* Styles pour les écrans de 768px ou moins */
}
```

### 3. Unités relatives

Privilégiez les unités relatives (`%`, `em`, `rem`) pour les dimensions et les polices afin d'assurer une meilleure adaptabilité.

### 4. Images flexibles

Assurez-vous que les images ne dépassent pas leur conteneur :

```css
img {
  max-width: 100%;
  height: auto;
}
```

## 📂 Structure du projet

```
projet/
├── index.html
├── styles.css
└── README.md
```

## 🔗 Ressources

- [W3Schools - HTML Layout](https://www.w3schools.com/html/html_layout.asp)
- [W3Schools - Responsive Web Design](https://www.w3schools.com/html/html_responsive.asp)
- [MDN - Responsive Design](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Responsive_Design)

---

Ce fichier HTML illustre l'utilisation des balises sémantiques pour structurer la page, l'application de Flexbox pour la mise en page, et l'utilisation de media queries pour assurer la réactivité du site sur différents appareils.

[![Mise en page du site | CSS](https://images.openai.com/thumbnails/4686ea374513bea2f1ae60f3c73165d8.png)](https://www.mytopschool.net/mysti2d/activites/polynesie2/eXeL/SIN/08/CSS/mise_en_page_du_site.html)

Voici un fichier HTML complet en français, conçu pour illustrer les principes fondamentaux de la **mise en page HTML** et du **design web responsive**. Ce fichier intègre des balises sémantiques, des techniques de mise en page modernes (Flexbox et Grid), ainsi que des media queries pour assurer une adaptabilité optimale sur divers appareils.

---

### 📄 `index.html`

```html
<!DOCTYPE html>
<html lang="fr">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Mise en page HTML & Responsive Design</title>
    <style>
      /* Réinitialisation de base */
      * {
        box-sizing: border-box;
        margin: 0;
        padding: 0;
      }

      body {
        font-family: Arial, sans-serif;
        line-height: 1.6;
      }

      /* Mise en page avec Grid */
      .container {
        display: grid;
        grid-template-areas:
          "header header"
          "nav nav"
          "main aside"
          "footer footer";
        grid-template-columns: 3fr 1fr;
        gap: 20px;
        padding: 20px;
      }

      header {
        grid-area: header;
        background-color: #f8f9fa;
        padding: 20px;
      }

      nav {
        grid-area: nav;
        background-color: #e9ecef;
        padding: 20px;
      }

      main {
        grid-area: main;
        background-color: #dee2e6;
        padding: 20px;
      }

      aside {
        grid-area: aside;
        background-color: #ced4da;
        padding: 20px;
      }

      footer {
        grid-area: footer;
        background-color: #adb5bd;
        text-align: center;
        padding: 20px;
      }

      /* Responsive Design */
      @media (max-width: 768px) {
        .container {
          grid-template-areas:
            "header"
            "nav"
            "main"
            "aside"
            "footer";
          grid-template-columns: 1fr;
        }
      }
    </style>
  </head>
  <body>
    <div class="container">
      <header>
        <h1>Mon Site Web</h1>
      </header>
      <nav>
        <ul>
          <li><a href="#">Accueil</a></li>
          <li><a href="#">À propos</a></li>
          <li><a href="#">Services</a></li>
          <li><a href="#">Contact</a></li>
        </ul>
      </nav>
      <main>
        <h2>Contenu Principal</h2>
        <p>
          Bienvenue sur mon site web. Ceci est un exemple de mise en page
          utilisant HTML et CSS pour créer un design responsive adapté à tous
          les appareils.
        </p>
      </main>
      <aside>
        <h2>Informations Supplémentaires</h2>
        <p>
          Voici quelques informations supplémentaires affichées dans la barre
          latérale.
        </p>
      </aside>
      <footer>
        <p>&copy; 2025 Mon Site Web. Tous droits réservés.</p>
      </footer>
    </div>
  </body>
</html>
```

---

### 📘 Explication du Code

- **Balises Sémantiques** : Utilisation de `<header>`, `<nav>`, `<main>`, `<aside>` et `<footer>` pour structurer le contenu de manière significative.

- **CSS Grid** : La classe `.container` utilise `display: grid` pour organiser les différentes sections de la page.

- **Media Queries** : La règle `@media` ajuste la disposition des éléments pour les écrans de 768 pixels de large ou moins, assurant ainsi une expérience utilisateur optimale sur les appareils mobiles.

- **Flexibilité** : Les unités relatives et la grille permettent une adaptation fluide du contenu en fonction de la taille de l'écran.

---

### 🔗 Ressources Complémentaires

- [W3Schools - HTML Layout](https://www.w3schools.com/html/html_layout.asp)
- [W3Schools - Responsive Web Design](https://www.w3schools.com/html/html_responsive.asp)
- [MDN Web Docs - Responsive Design](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Responsive_Design)

---
