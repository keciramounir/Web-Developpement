# 💬 Commentaires en HTML

Les **commentaires HTML** sont des lignes de texte dans le code qui **ne s’affichent pas dans le navigateur**. Ils sont utilisés uniquement par les développeurs pour **expliquer**, **organiser**, ou **désactiver temporairement** des parties du code.

---

## ✍️ Comment écrire un commentaire HTML ?

La syntaxe est la suivante :

```html
<!-- Ceci est un commentaire HTML -->
```

````

Un commentaire commence par `<!--` et se termine par `-->`.

---

## 📌 Utilisations des commentaires en HTML

### ✅ 1. Ajouter des explications dans le code

Les commentaires permettent de **documenter le code** pour vous-même ou pour d’autres développeurs.

```html
<!-- Section de présentation -->
<section>
  <h2>À propos de moi</h2>
</section>
```

---

### ✅ 2. Marquer des sections du code

Ils aident à **repérer rapidement** certaines parties dans un long fichier HTML.

```html
<!-- ================== FOOTER ================== -->
<footer>
  <p>&copy; 2025 Mon Site</p>
</footer>
```

---

### ✅ 3. Désactiver temporairement une partie du code

Utile pour tester ou désactiver du code sans le supprimer.

```html
<!-- <p>Ce texte est temporairement désactivé</p> -->
```

---

## ❌ Attention

- Les commentaires **ne doivent pas être imbriqués** :

  ```html
  <!-- Ceci est <!-- incorrect -->
  -->
  ```

  Cela peut provoquer des erreurs de rendu.

- Ne mettez **pas d’informations sensibles** dans les commentaires, car ils sont visibles dans le **code source** de la page.

---

## 👨‍💻 Pourquoi c’est utile pour un développeur ?

- Pour garder son code **lisible et compréhensible**.
- Pour faciliter le **travail en équipe**.
- Pour gagner du temps lors du **débogage ou de la maintenance**.
- Pour expérimenter sans supprimer le code original.

---

## ✅ Bonnes pratiques

- Soyez clair et concis dans vos commentaires.
- Utilisez-les pour **expliquer le “pourquoi”**, pas juste le “quoi”.
- Nettoyez les commentaires inutiles avant la mise en production.

---

🧠 **Exemple complet :**

```html
<!-- Début du bloc principal -->
<main>
  <!-- Titre de la page -->
  <h1>Bienvenue sur mon portfolio</h1>

  <!-- Cette section contiendra une galerie plus tard -->
  <!-- <section class="galerie">...</section> -->
</main>
```

---

🔚 Les commentaires HTML sont un outil simple mais puissant pour rendre votre code plus **professionnel**, **collaboratif** et **maintenable**.

```


````
