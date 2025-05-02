# 🔗 Les liens HTML (`<a>`)

## 📌 Définition

En HTML, la balise `<a>` (pour "anchor", ancre) sert à **créer un lien hypertexte** vers une autre page, un fichier, une section de la page, une adresse e-mail, etc.

---

## ✍️ Syntaxe de base

```html
<a href="URL">Texte cliquable</a>
```

Exemple :

```html
<a href="https://www.openai.com">Visitez OpenAI</a>
```

---

## 🧱 Attributs essentiels

### ✅ `href` (Hypertext REFerence)

- Spécifie l’URL de destination.
- Peut être **absolue** ou **relative**.

```html
<!-- Lien absolu -->
<a href="https://example.com">Site externe</a>

<!-- Lien relatif -->
<a href="page2.html">Page interne</a>
```

### ✅ `target`

- Contrôle l’ouverture du lien.

| Valeur    | Description                          |
| --------- | ------------------------------------ |
| `_self`   | (par défaut) Ouvre dans la même page |
| `_blank`  | Ouvre dans un **nouvel onglet**      |
| `_parent` | Ouvre dans la fenêtre parente        |
| `_top`    | Ouvre dans la fenêtre principale     |

```html
<a href="https://example.com" target="_blank">Ouvrir dans un nouvel onglet</a>
```

### ✅ `title`

- Affiche un **texte flottant** au survol.

```html
<a href="doc.pdf" title="Télécharger le PDF">Documentation</a>
```

### ✅ `download`

- Permet de **télécharger** un fichier au lieu de l’ouvrir.

```html
<a href="fichier.pdf" download>Télécharger le PDF</a>
```

---

## 📍 Types de liens

### 🌐 1. Lien vers une page externe

```html
<a href="https://openai.com" target="_blank">OpenAI</a>
```

### 🧭 2. Lien vers une page interne

```html
<a href="/contact.html">Contact</a>
```

### 🎯 3. Lien vers une section d’une même page (ancre)

```html
<!-- Lien -->
<a href="#apropos">Aller à la section À propos</a>

<!-- Cible -->
<h2 id="apropos">À propos</h2>
```

### 📂 4. Lien vers un fichier à télécharger

```html
<a href="cv.pdf" download>Télécharger mon CV</a>
```

### 📧 5. Lien vers une adresse e-mail

```html
<a href="mailto:contact@example.com">Envoyer un email</a>
```

### 📞 6. Lien vers un numéro de téléphone

```html
<a href="tel:+213661234567">Appeler maintenant</a>
```

---

## ⚠️ Bonnes pratiques

- Ajoute `rel="noopener noreferrer"` pour des liens externes avec `target="_blank"` (sécurité).

```html
<a href="https://exemple.com" target="_blank" rel="noopener noreferrer"
  >Lien sécurisé</a
>
```

- Utilise des **textes explicites** (pas juste "cliquez ici").
- Structure ton site avec des liens internes clairs.

---

## 🧠 Exemple complet en HTML

```html
<!DOCTYPE html>
<html lang="fr">
  <head>
    <meta charset="UTF-8" />
    <title>Exemples de liens HTML</title>
  </head>
  <body>
    <!-- Lien externe -->
    <a href="https://www.openai.com" target="_blank" rel="noopener noreferrer"
      >Visitez OpenAI</a
    ><br />

    <!-- Lien interne -->
    <a href="services.html">Nos services</a><br />

    <!-- Lien vers une ancre -->
    <a href="#contact">Aller à la section Contact</a><br />

    <!-- Lien de téléchargement -->
    <a href="guide.pdf" download>Télécharger le guide PDF</a><br />

    <!-- Lien mail -->
    <a href="mailto:support@example.com">Contactez-nous par e-mail</a><br />

    <!-- Lien téléphone -->
    <a href="tel:+213661234567">Appelez-nous</a>

    <hr />

    <!-- Cible de l’ancre -->
    <h2 id="contact">Contact</h2>
    <p>Vous pouvez nous joindre via le formulaire de contact.</p>
  </body>
</html>
```
