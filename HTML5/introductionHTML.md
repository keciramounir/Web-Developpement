# 🧠 Définitions essentielles à connaître avant de coder en HTML

Ce document contient les définitions clés à maîtriser avant de commencer à coder en **HTML**.

---

## 1. HTML (HyperText Markup Language)

Le **HTML** est le **langage de balisage** utilisé pour structurer le contenu d’une page web, comme les titres, paragraphes, images, liens, etc.  
Il ne permet **ni la mise en forme** (c’est le rôle de CSS), **ni l’interactivité** (c’est le rôle de JavaScript), mais il définit l’**organisation du contenu**.

---

## 2. Balise (Tag)

Une **balise HTML** est un mot-clé encadré par des chevrons `< >`. Elle sert à **indiquer la nature d’un élément**.

- Une balise **ouvrante** : `<p>`
- Une balise **fermante** : `</p>`

Exemple :

```html
<p>Ceci est un paragraphe</p>
```

---

## 3. Élément HTML

Un **élément HTML** est l’unité de base du HTML. Il comprend :

- une balise ouvrante Start Tag
- un contenu
- une balise fermante End Tag

Exemple :

```html
<h1>Mon titre</h1>
```

---

## 4. Attribut

Un **attribut** est une information **supplémentaire** ajoutée à une balise. Il modifie ou précise son comportement.
Il est placé **dans la balise ouvrante**, sous forme de `nom="valeur"`.

Exemple :

```html
<a href="https://www.exemple.com">Visiter le site</a>
```

Ici, `href` est un attribut qui précise le lien de destination.

---

## 5. Arborescence (Structure hiérarchique)

Le HTML suit une **structure hiérarchique** en arbre. Certains éléments peuvent contenir d'autres éléments (ex : un `<div>` qui contient des paragraphes ou images).

Exemple :

```html
<div>
  <h2>Titre</h2>
  <p>Texte descriptif</p>
</div>
```

---

## 6. Document HTML de base

C’est la structure minimale d’un fichier HTML valide.
Exemple :

```html
<!DOCTYPE html>
<html lang="fr">
  <head>
    <meta charset="UTF-8" />
    <title>Titre de la page</title>
  </head>
  <body>
    <h1>Bienvenue</h1>
    <p>Ceci est mon premier site.</p>
  </body>
</html>
```

---

## 7. Head vs Body

- La balise `<head>` contient les **métadonnées**, le titre de la page, les liens vers les feuilles de style, etc.
- La balise `<body>` contient **tout ce qui s’affiche à l’écran** : textes, images, liens, etc.

---

## 8. Commentaire HTML

Permet d’ajouter des notes dans le code qui ne seront pas visibles sur la page.

Exemple :

```html
<!-- Ceci est un commentaire -->
```

---

## 9. Auto-fermante (Self-closing tags)

Certaines balises n'ont **pas de contenu** et sont **auto-fermées**.

Exemples :

```html
<img src="image.jpg" alt="Texte alternatif" />
<br />
<hr />
```

---

## 10. Sémantique HTML

La **sémantique** en HTML signifie utiliser les balises selon leur **vraie signification** (et non juste pour la mise en page).

Exemples :

- `<header>` : en-tête de la page
- `<footer>` : pied de page
- `<nav>` : zone de navigation
- `<article>` : contenu autonome
- `<section>` : section de contenu

---

## ✅ À retenir

- Le HTML est la **structure** d’un site web.
- Il utilise des **balises** pour décrire les éléments.
- Il fonctionne avec des **attributs** pour préciser le comportement des balises.
- Il respecte une **hiérarchie** logique et lisible.

---

🎯 **Prochaine étape** : pratiquer avec des exemples concrets !

```

```
