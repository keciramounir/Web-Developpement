- Couleurs nommées
- Hex sur 6 & 8 caractères
- RGB / RGBA
- HSL / HSLA
- CMYK (non supporté nativement)
- Autres systèmes (LAB, HWB, LCH...)

---

# 🎨 CSS Colors – Guide Ultra Complet en Français 🇫🇷

Ce document couvre **tous les systèmes de couleur** que vous pouvez (ou devriez) connaître en CSS, avec définitions, exemples, usages réels, avantages et limitations.

---

## 🔹 1. Couleurs par nom (`Color by name`)

CSS reconnaît **147 couleurs nommées** comme `red`, `blue`, `cornflowerblue`, `darkslategray`, etc.

```css
color: gold;
background-color: midnightblue;
```

````

✅ Simple et lisible
❌ Choix limité

---

## 🔹 2. Couleurs hexadécimales (`#RRGGBB` ou `#RRGGBBAA`)

### ➤ `#RRGGBB` (6 caractères)

Chaque paire représente : **Rouge**, **Vert**, **Bleu** (0–255)

```css
color: #ff5733; /* Orange vif */
```

### ➤ `#RRGGBBAA` (8 caractères)

Ajout de la **transparence** (Alpha, `00` à `FF`)

```css
background-color: #00000080; /* Noir semi-transparent */
```

✅ Très utilisé, compatible partout
✅ Contrôle précis des teintes
❌ Moins lisible qu’un nom ou une fonction

---

## 🔹 3. RGB & RGBA

### ➤ `rgb(r, g, b)`

Chaque composant va de 0 à 255 :

```css
color: rgb(255, 0, 0); /* Rouge */
```

### ➤ `rgba(r, g, b, a)`

Ajoute **l'opacité**, de `0` (transparent) à `1` (opaque)

```css
background-color: rgba(0, 128, 0, 0.5); /* Vert transparent */
```

✅ Transparent & intuitif
❌ Moins flexible pour créer des gammes de couleurs

---

## 🔹 4. HSL & HSLA

### ➤ `hsl(hue, saturation%, lightness%)`

- **Hue** (Teinte) : 0–360 (rouge à rouge)
- **Saturation** : 0–100%
- **Lightness** : 0–100%

```css
color: hsl(200, 80%, 50%); /* Bleu saturé */
```

### ➤ `hsla(h, s%, l%, a)`

Ajoute une couche de transparence

```css
background-color: hsla(340, 70%, 60%, 0.4);
```

✅ Facile pour générer des thèmes dynamiques
✅ Très lisible pour le design
❌ Moins universel que RGB

---

## 🔹 5. HEX 3 caractères (`#RGB`)

Abréviation du format HEX quand les valeurs sont doublées :

```css
color: #f00; /* Équivaut à #ff0000 */
```

✅ Très court
❌ Moins précis
⚠️ Ne supporte pas la transparence

---

## 🔹 6. Système CMYK (Non supporté nativement)

> ❌ Le modèle **CMYK (Cyan, Magenta, Yellow, Black)** est **utilisé en impression**, mais **pas supporté par CSS**.

Cependant, vous pouvez convertir CMYK ➤ RGB/HEX via un outil externe :

- [https://www.rapidtables.com/convert/color/cmyk-to-rgb.html](https://www.rapidtables.com/convert/color/cmyk-to-rgb.html)

---

## 🔹 7. Nouvelles fonctions CSS (niveau 4)

### ✅ `color()`

Permet de spécifier une **espace colorimétrique étendue** (`display-p3`, `rec2020`, etc.)

```css
color: color(display-p3 1 0.5 0);
```

✅ Support des écrans HDR
⚠️ Encore peu supporté

---

### ✅ `lab()` et `lch()`

Plus proche de la **perception humaine** (visuellement cohérent)

```css
color: lab(54% 80 67);
color: lch(70% 45 320);
```

✅ Précision perceptuelle
⚠️ Limité aux navigateurs modernes (Chrome, Safari)

---

### ✅ `hwb()` : Hue-Whiteness-Blackness

Alternative au HSL plus naturelle :

```css
color: hwb(240 30% 10%);
```

---

## 🎯 Exemples pratiques

### 🎨 Thème dynamique (mode sombre/clair)

```css
:root {
  --text-color: hsl(220, 15%, 20%);
  --bg-color: hsl(0, 0%, 100%);
}
.dark-mode {
  --text-color: hsl(0, 0%, 90%);
  --bg-color: hsl(0, 0%, 10%);
}
```

---

### 🔍 Hover avec opacité

```css
button {
  background-color: rgba(255, 99, 71, 1);
}
button:hover {
  background-color: rgba(255, 99, 71, 0.7);
}
```

---

## 🛠️ Outils de conversion

- 🎛️ [Coolors.co](https://coolors.co)
- 🧮 [RGB <-> HEX <-> HSL](https://www.colorhexa.com/)
- 🖨️ [CMYK to RGB](https://www.rapidtables.com/convert/color/cmyk-to-rgb.html)
- 🎯 [ColorZilla Chrome](https://www.colorzilla.com/)

---

## 🔐 Accessibilité

Toujours vérifier les **ratios de contraste** pour l'accessibilité (WCAG) :

- [WebAIM Contrast Checker](https://webaim.org/resources/contrastchecker/)
- [Accessible Colors](https://accessible-colors.com/)

---

## 📚 Ressources officielles

- [MDN – CSS Colors](https://developer.mozilla.org/fr/docs/Web/CSS/color_value)
- [W3Schools – CSS Color Names](https://www.w3schools.com/colors/colors_names.asp)
- [CSS Tricks – Guide des couleurs](https://css-tricks.com/almanac/properties/c/color/)

---

## ✅ Résumé comparatif

| Format            | Transparence      | Lisibilité | Support navigateurs | Usage                   |
| ----------------- | ----------------- | ---------- | ------------------- | ----------------------- |
| `color name`      | ❌                | ✅         | ✅                  | Rapide, limité          |
| `#RRGGBB`         | ❌                | ✅         | ✅                  | Web standard            |
| `#RRGGBBAA`       | ✅                | ✅         | ✅ (modernes)       | Précis, moderne         |
| `rgb()`           | ❌                | ✅         | ✅                  | Contrôle direct         |
| `rgba()`          | ✅                | ✅         | ✅                  | Transparence facile     |
| `hsl()`           | ❌                | ✅✅       | ✅                  | Parfait pour les thèmes |
| `hsla()`          | ✅                | ✅✅       | ✅                  | Transparent + lisible   |
| `lab()` / `lch()` | ✅                | ✅✅✅     | 🚧 (expérimental)   | Vision réaliste         |
| `cmyk()`          | ❌ (non supporté) | ❌         | ❌                  | Hors CSS natif          |

---

## 🧠 Astuce bonus : Utilisez des variables CSS pour vos couleurs

```css
:root {
  --primary: #ff6347;
  --primary-rgba: rgba(255, 99, 71, 0.8);
}
button {
  background-color: var(--primary);
}
```

---

## 🧩 À venir

- Support complet de `color(display-p3)` pour écrans Retina
- Prise en charge généralisée de `lab()`, `lch()`, `hwb()`
- Couleurs dynamiques via JavaScript (`style.setProperty()`)

---

👨‍💻 \_Créé avec ❤️ par Mounir Kecira
````
