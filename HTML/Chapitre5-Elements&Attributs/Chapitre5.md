# 📝 Guide Complet des Éléments et Attributs HTML

HTML (HyperText Markup Language) est un langage de balisage utilisé pour structurer le contenu sur le web. Ce fichier vous aidera à comprendre tous les éléments HTML importants, leurs attributs associés, et la différence entre le HTML sémantique et non-sémantique.

---

## 1. 🎯 **Éléments HTML**

Les éléments HTML sont utilisés pour structurer le contenu d'une page web. Un élément est constitué d’une **balise d'ouverture** et d’une **balise de fermeture** (sauf dans certains cas).

### 1.1 **Éléments de base**

- `<html>` : L'élément racine de tout document HTML.
- `<head>` : Contient des informations méta sur la page (titre, liens vers les feuilles de style, etc.).
- `<body>` : Contient le contenu visible de la page web.
- `<title>` : Définit le titre de la page, visible dans l'onglet du navigateur.
- `<h1>` à `<h6>` : Définit les titres de niveau 1 à 6, du plus grand au plus petit.
- `<p>` : Définit un paragraphe.
- `<a>` : Définit un lien hypertexte.
- `<img>` : Définit une image.
- `<ul>` : Définit une liste non ordonnée.
- `<ol>` : Définit une liste ordonnée.
- `<li>` : Définit un élément de liste.

### 1.2 **Éléments de structure**

- `<header>` : Contient les éléments d'en-tête, comme le logo et la navigation principale.
- `<footer>` : Contient les éléments de pied de page, comme les informations de copyright.
- `<nav>` : Contient la navigation principale du site.
- `<article>` : Définit un contenu autonome, comme un article de blog ou une publication.
- `<section>` : Définit une section d'un document, souvent utilisée pour organiser le contenu.
- `<aside>` : Définit un contenu supplémentaire ou latéral (souvent des informations annexes).
- `<main>` : Définit le contenu principal d'une page, unique et central.
- `<div>` : Utilisé pour diviser la page en sections, mais sans signification sémantique propre.
- `<span>` : Utilisé pour regrouper du contenu en ligne sans signification sémantique propre.

---

## 2. ⚙️ **Attributs HTML**

Les attributs HTML fournissent des informations supplémentaires sur un élément. Chaque attribut se compose d’un nom et d’une valeur.

### 2.1 **Attributs communs**

- `id` : Définit un identifiant unique pour un élément (utile pour les styles CSS ou les scripts JavaScript).

```html
<p id="description">Voici un paragraphe.</p>
```

- `class` : Associe un élément à une ou plusieurs classes CSS.

```html
<p class="highlight">Ceci est un texte important.</p>
```

- `style` : Applique des styles CSS directement à un élément.

```html
<p style="color: red;">Texte en rouge.</p>
```

- `href` : Définit la destination d’un lien `<a>`.

```html
<a href="https://www.example.com">Visitez Example.com</a>
```

- `src` : Définit la source d’une image `<img>`.

```html
<img src="image.jpg" alt="Image d'exemple" />
```

- `alt` : Fournit une description textuelle alternative pour une image.

```html
<img src="image.jpg" alt="Un chat mignon" />
```

- `title` : Affiche un texte au survol de l’élément.

```html
<a href="https://www.example.com" title="Visiter Example.com">Cliquez ici</a>
```

- `target` : Définit où le lien s'ouvrira (ex : dans un nouvel onglet avec `_blank`).

```html
<a href="https://www.example.com" target="_blank"
  >Ouvrir dans un nouvel onglet</a
>
```

- `type` : Définit le type de contenu ou de fichier (souvent utilisé dans les formulaires et les liens).

---

## 3. 🌍 **HTML Sémantique vs Non-Sémantique**

### 3.1 **HTML Sémantique**

Le **HTML sémantique** consiste à utiliser des balises qui décrivent le rôle du contenu qu’elles contiennent. Cela améliore l'accessibilité, le SEO (référencement), et la lisibilité du code.

#### Exemples :

- `<article>` : Utilisé pour contenir un contenu autonome (ex : un article de blog).
- `<section>` : Utilisé pour diviser le contenu en sections logiques (ex : section à propos, section services).
- `<header>` : Contient des informations d'en-tête (ex : logo, menu de navigation).
- `<footer>` : Contient des informations de bas de page (ex : copyright, mentions légales).
- `<nav>` : Contient la navigation de la page.
- `<main>` : Contient le contenu principal, unique, de la page.

#### Exemple de structure sémantique :

```html
<main>
  <header>
    <h1>Bienvenue sur mon site</h1>
    <nav>
      <a href="#services">Nos services</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <section id="services">
    <h2>Nos Services</h2>
    <p>Voici ce que nous proposons...</p>
  </section>

  <footer>
    <p>&copy; 2025 Mon Site Web</p>
  </footer>
</main>
```

### 3.2 **HTML Non-Sémantique**

Le **HTML non-sémantique** utilise des balises qui ne donnent pas de signification particulière au contenu qu’elles contiennent. Ce type de balises est souvent utilisé pour la mise en page ou des besoins généraux sans sémantique particulière.

#### Exemples :

- `<div>` : Un conteneur générique sans signification sémantique.
- `<span>` : Un conteneur générique en ligne sans signification sémantique.

#### Exemple de structure non-sémantique :

```html
<div>
  <div>
    <h1>Bienvenue sur mon site</h1>
    <div>
      <a href="#services">Nos services</a>
      <a href="#contact">Contact</a>
    </div>
  </div>

  <div>
    <h2>Nos Services</h2>
    <p>Voici ce que nous proposons...</p>
  </div>

  <div>
    <p>&copy; 2025 Mon Site Web</p>
  </div>
</div>
```

---

## 4. 🧑‍💻 **Conclusion**

L'utilisation d'éléments et d'attributs HTML est essentielle pour structurer et styliser vos pages web. Il est important de privilégier l’utilisation des balises sémantiques pour une meilleure organisation et une meilleure accessibilité, tout en réduisant l’utilisation des balises non-sémantiques, sauf lorsque cela est nécessaire.

---

## 📚 **Ressources supplémentaires**

- [MDN Web Docs - HTML Elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)
- [W3C - HTML5 Semantic Elements](https://www.w3.org/TR/html5/sections.html)
