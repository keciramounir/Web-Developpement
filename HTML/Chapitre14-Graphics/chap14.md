# 🎨 Graphismes HTML : Canvas vs SVG

Bienvenue dans ce guide de démarrage rapide sur les **graphiques HTML** ! Ici, vous découvrirez deux technologies puissantes pour dessiner des formes, des textes, des images et bien plus encore dans vos pages web : **HTML Canvas** 🖌️ et **SVG (Scalable Vector Graphics)** 🧩.

---

## 🖼️ Qu’est-ce que `<canvas>` ?

Le **canvas HTML** est un conteneur rectangulaire utilisé pour dessiner dynamiquement des graphismes via **JavaScript**.

### 🔧 Caractéristiques :

- 📦 Élément : `<canvas>`
- ⚙️ Nécessite JavaScript pour dessiner
- 🖍️ Supporte les lignes, formes, textes, images...
- 🌍 Compatible avec tous les navigateurs modernes

### ✅ Exemple de base :

```html
<canvas
  id="myCanvas"
  width="200"
  height="100"
  style="border:1px solid #000;"
></canvas>
```

### 🎯 Exemple d’utilisation avec JavaScript :

#### ➤ Dessiner une ligne :

```html
<script>
  var c = document.getElementById("myCanvas");
  var ctx = c.getContext("2d");
  ctx.moveTo(0, 0);
  ctx.lineTo(200, 100);
  ctx.stroke();
</script>
```

#### ➤ Dessiner un cercle :

```html
ctx.beginPath(); ctx.arc(95, 50, 40, 0, 2 * Math.PI); ctx.stroke();
```

#### ➤ Écrire du texte :

```html
ctx.font = "30px Arial"; ctx.fillText("Bonjour Canvas", 10, 50);
```

#### ➤ Dégradé linéaire :

```html
var grd = ctx.createLinearGradient(0, 0, 200, 0); grd.addColorStop(0, "red");
grd.addColorStop(1, "white"); ctx.fillStyle = grd; ctx.fillRect(10, 10, 150,
80);
```

---

## 🧩 Qu’est-ce que `<svg>` ?

Le **SVG** est un langage XML qui permet de dessiner des graphismes vectoriels redimensionnables, intégrés directement dans le HTML.

### 📐 Caractéristiques :

- ✍️ Élément : `<svg>`
- 📏 Basé sur XML
- ⚙️ Chaque forme est un objet DOM
- 🌀 Animations, événements JavaScript, CSS possibles
- 🔍 Résolution indépendante (pas de perte de qualité)

### ✅ Exemple de base :

```html
<svg width="100" height="100">
  <circle
    cx="50"
    cy="50"
    r="40"
    stroke="green"
    stroke-width="4"
    fill="yellow"
  />
</svg>
```

### 🎯 Autres exemples utiles :

#### ➤ Rectangle avec coins arrondis et opacité :

```html
<rect
  x="50"
  y="20"
  rx="20"
  ry="20"
  width="150"
  height="150"
  style="fill:red;stroke:black;stroke-width:5;opacity:0.5"
/>
```

#### ➤ Étoile :

```html
<polygon
  points="100,10 40,198 190,78 10,78 160,198"
  style="fill:lime;stroke:purple;stroke-width:5;fill-rule:evenodd;"
/>
```

#### ➤ Dégradé + texte :

```html
<defs>
  <linearGradient id="grad1">
    <stop offset="0%" stop-color="yellow" />
    <stop offset="100%" stop-color="red" />
  </linearGradient>
</defs>
<ellipse cx="100" cy="70" rx="85" ry="55" fill="url(#grad1)" />
<text fill="#fff" font-size="45" x="50" y="86">SVG</text>
```

---

## ⚖️ Comparaison : SVG vs Canvas

| 🎯 Critère             | 🧩 SVG                 | 🖼️ Canvas                  |
| ---------------------- | ---------------------- | -------------------------- |
| 🔍 Résolution          | Indépendante           | Dépendante                 |
| 📦 Structure DOM       | Oui (XML)              | Non                        |
| 🧠 Mémorise les formes | Oui                    | Non                        |
| 🎨 Rendu de texte      | Excellente             | Moyen                      |
| 🕹️ Événements          | Gérés individuellement | Non                        |
| 🎮 Jeux ou animations  | Peu adapté             | Très adapté                |
| 📸 Sauvegarde d’image  | Complexe               | Facile en `.png` ou `.jpg` |

---

## 📚 En résumé

- 🖼️ **Canvas** : idéal pour les **jeux**, animations dynamiques, effets complexes 🎮
- 🧩 **SVG** : parfait pour les **illustrations statiques**, icônes, graphiques interactifs 📊

---

## 🚀 Pour aller plus loin :

- [🧠 HTML Canvas Tutorial](https://www.w3schools.com/html/html5_canvas.asp)
- [📐 SVG Tutorial](https://www.w3schools.com/graphics/svg_intro.asp)

---

✨ Bon dessin interactif ! Que ce soit en pixels ou en vecteurs, donnez vie à vos idées dans le navigateur !

```

```
