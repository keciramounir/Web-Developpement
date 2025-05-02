# 🌐 HTML Sémantique vs Non-Sémantique

Dans ce projet, nous mettons en lumière la différence entre **HTML sémantique** et **HTML non-sémantique**. Comprendre cette distinction est essentielle pour structurer correctement vos pages web et améliorer leur lisibilité, accessibilité et SEO.

## 💡 Concepts abordés

### HTML Sémantique 🧑‍💻

Les éléments **sémantiques** en HTML ont une signification explicite et claire pour le contenu qu'ils encapsulent. Ils aident à structurer un document de manière logique et rendent le code plus compréhensible pour les développeurs, les moteurs de recherche et les technologies d'assistance.

**Exemples d'éléments sémantiques :**

- `<header>` : Définit une en-tête pour un document ou une section.
- `<footer>` : Contient des informations de pied de page.
- `<article>` : Représente un contenu autonome, comme un article de blog ou un article de presse.
- `<section>` : Utilisé pour diviser un contenu en sections thématiques.
- `<nav>` : Contient un ensemble de liens de navigation.
- `<aside>` : Représente un contenu secondaire ou complémentaire.
- `<main>` : Représente le contenu principal du document.

### HTML Non-Sémantique 📦

Les éléments **non-sémantiques** sont utilisés pour structurer un document, mais ils ne fournissent aucune signification explicite sur le contenu. Ils sont souvent utilisés pour des fins de mise en page ou d'encapsulation.

**Exemples d'éléments non-sémantiques :**

- `<div>` : Conteneur générique utilisé pour structurer des parties d'une page sans signification.
- `<span>` : Utilisé pour styliser une portion de texte sans signification contextuelle.

## 🖼️ Exemples d'éléments HTML

### HTML Sémantique

```html
<header>
  <h1>Bienvenue sur mon site web</h1>
  <nav>
    <ul>
      <li><a href="#home">Accueil</a></li>
      <li><a href="#about">À propos</a></li>
    </ul>
  </nav>
</header>

<main>
  <section>
    <h2>Introduction</h2>
    <p>Ceci est un paragraphe d'introduction.</p>
  </section>
</main>

<footer>
  <p>© 2025 Mon Site Web</p>
</footer>
```

### HTML Non-Sémantique

```html
<div class="header">
  <h1>Bienvenue sur mon site web</h1>
  <div class="nav">
    <ul>
      <li><a href="#home">Accueil</a></li>
      <li><a href="#about">À propos</a></li>
    </ul>
  </div>
</div>

<div class="main">
  <div class="section">
    <h2>Introduction</h2>
    <p>Ceci est un paragraphe d'introduction.</p>
  </div>
</div>

<div class="footer">
  <p>© 2025 Mon Site Web</p>
</div>
```

## 📚 Pourquoi utiliser le HTML Sémantique ?

- **Accessibilité** : Les technologies d'assistance (comme les lecteurs d'écran) peuvent mieux comprendre le contenu de la page.
- **SEO** : Les moteurs de recherche indexent mieux le contenu et comprennent mieux la structure du document.
- **Lisibilité** : Le code est plus facile à lire et à maintenir grâce à l'utilisation d'éléments explicites.
