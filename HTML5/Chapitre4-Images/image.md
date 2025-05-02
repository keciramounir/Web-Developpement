# 📷 Les éléments `<img>` en HTML

Les éléments `<img>` en HTML sont utilisés pour **intégrer des images** dans les pages web. L’élément `<img>` est une **balise auto-fermante** et permet d'afficher des images dans le contenu de la page.

---

## ✨ Syntaxe de base

La syntaxe pour intégrer une image est la suivante :

```html
<img src="URL_de_l_image" alt="description de l'image" />
```

- **`src`** (source) : L'URL de l'image que vous souhaitez afficher. Cela peut être un chemin relatif ou une URL complète.
- **`alt`** (texte alternatif) : Une description textuelle de l'image qui est utilisée par les moteurs de recherche, pour les utilisateurs malvoyants, et dans le cas où l'image ne peut pas être affichée.

---

## 🔑 Attributs importants

### ✅ `src`

- Spécifie le chemin ou l'URL de l'image.

```html
<img src="images/photo.jpg" alt="Une belle photo" />
```

### ✅ `alt`

- Fournit une description de l'image. **Essentiel pour l'accessibilité.**

```html
<img src="logo.png" alt="Logo de mon site web" />
```

### ✅ `width` et `height`

- Définissent la largeur et la hauteur de l'image. Vous pouvez spécifier des valeurs en pixels ou en pourcentage.

```html
<img src="image.jpg" alt="Exemple d'image" width="400" height="300" />
```

### ✅ `title`

- Affiche un **texte au survol** de l'image (optionnel).

```html
<img src="image.jpg" alt="Description" title="Survolez-moi pour plus d'infos" />
```

### ✅ `loading`

- Détermine la façon dont l'image doit être chargée.

| Valeur | Description                                             |
| ------ | ------------------------------------------------------- |
| `auto` | Chargement automatique (par défaut).                    |
| `lazy` | Chargement différé (charge l'image lorsque nécessaire). |

```html
<img src="image.jpg" alt="Description" loading="lazy" />
```

### ✅ `style`

- Permet d'ajouter du **style CSS en ligne** à l'image (par exemple, la bordure, la marge, etc.).

```html
<img src="image.jpg" alt="Image stylisée" style="border-radius: 10px;" />
```

---

## 📍 Types d'utilisation des images en HTML

### 🌐 1. Lien vers une image externe

```html
<img src="https://example.com/photo.jpg" alt="Image d'exemple" />
```

### 🖼 2. Image locale (sur votre propre serveur)

```html
<img src="assets/images/photo.jpg" alt="Photo locale" />
```

### 🔄 3. Image de fond en CSS

Vous pouvez aussi utiliser l'image en tant que fond avec CSS.

```css
body {
  background-image: url("image.jpg");
  background-size: cover;
}
```

### 🖌 4. Image en tant qu'élément interactif

Vous pouvez également l'utiliser dans un lien pour rediriger les utilisateurs lorsqu'ils cliquent dessus.

```html
<a href="https://example.com">
  <img src="button.jpg" alt="Cliquez ici" />
</a>
```

### 📑 5. Images dans des tableaux ou des grilles

Les images peuvent être placées dans des éléments `<table>`, `<div>`, ou des grilles CSS.

```html
<table>
  <tr>
    <td><img src="image1.jpg" alt="Image 1" /></td>
    <td><img src="image2.jpg" alt="Image 2" /></td>
  </tr>
</table>
```

---

## ⚠️ Bonnes pratiques

- **Toujours ajouter un texte alternatif (`alt`)** : Cela améliore l'accessibilité et le référencement SEO.
- **Optimiser les images** : Compressez les images pour réduire leur taille et améliorer la vitesse de chargement.
- **Utiliser `width` et `height`** : Cela permet au navigateur de réserver l'espace nécessaire pour l'image, améliorant ainsi la performance.
- **Préférer les formats modernes** comme **WebP** pour des tailles d'images plus petites tout en gardant une qualité optimale.

---

## 🧠 Exemple complet

Voici un exemple complet de la manière dont vous pouvez utiliser les images avec les différents attributs :

```html
<!DOCTYPE html>
<html lang="fr">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Exemples d'Images en HTML</title>
  </head>
  <body>
    <h1>📷 Les Images en HTML</h1>

    <!-- Image locale avec attributs width et height -->
    <img
      src="image.jpg"
      alt="Exemple d'image locale"
      width="400"
      height="300"
    />

    <!-- Image externe -->
    <img src="https://example.com/photo.jpg" alt="Image externe" />

    <!-- Image avec texte au survol -->
    <img
      src="logo.png"
      alt="Logo de l'entreprise"
      title="Survolez pour plus d'informations"
      width="200"
    />

    <!-- Image avec chargement différé -->
    <img src="image2.jpg" alt="Image différée" loading="lazy" />

    <!-- Image dans un lien -->
    <a href="https://example.com">
      <img src="button.jpg" alt="Bouton cliquable" width="100" height="50" />
    </a>

    <!-- Image dans une table -->
    <table>
      <tr>
        <td><img src="image1.jpg" alt="Image 1" width="100" /></td>
        <td><img src="image2.jpg" alt="Image 2" width="100" /></td>
      </tr>
    </table>
  </body>
</html>
```

---

## 📚 Ressources supplémentaires

- [MDN Web Docs - Image](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/img)
- [W3C - HTML Image](https://www.w3.org/TR/html5/semantics.html#the-img-element)
