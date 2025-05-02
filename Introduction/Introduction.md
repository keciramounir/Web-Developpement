# 🧠 Prérequis pour Apprendre le Développement Web (HTML, CSS, JavaScript, MERN)

Bienvenue ! Ce guide explique **tout ce que tu dois savoir avant de commencer à apprendre le développement web**, notamment HTML, CSS, JavaScript et la stack MERN (MongoDB, Express, React, Node.js).

Chaque concept est expliqué clairement, avec définitions, exemples, et contexte. ✨

---

## 🔹 1. Compétences Informatiques de Base

### 💡 Système de fichiers

* Structure de répertoires et de fichiers.
* Exemple : `C:/Utilisateurs/Mounir/Documents/siteweb/index.html`

### 💡 Extensions de fichiers

* `.html`, `.css`, `.js`, `.json`, `.png`, etc.
* Chaque extension a un usage spécifique.

### 💡 Installation de logiciels

* Savoir installer : VS Code, Chrome, Node.js, Git, etc.

---

## 🔹 2. Comment Fonctionne le Web

### 💡 Modèle Client / Serveur

```
Navigateur (Client) <------> Serveur Web
    Requête HTTP         Réponse HTML/CSS/JS
```

### 💡 HTTP vs HTTPS

| Protocole | Description                      | Sécurité      |
| --------- | -------------------------------- | ------------- |
| HTTP      | Protocole de transfert classique | ❌ Non chiffré |
| HTTPS     | Version sécurisée via SSL/TLS    | ✅ Chiffré     |

### 💡 URL (Uniform Resource Locator)

* Adresse complète d'une page web.
* Exemple : `https://www.example.com:443/page?user=mounir#section1`

### 💡 URI (Uniform Resource Identifier)

* Identifie une ressource de manière unique.
* Une URL est un type de URI.

### 💡 Navigateur Web

* Logiciel permettant de consulter des pages web.
* Exemples : Chrome, Firefox, Safari.

### 💡 Navigation Privée

* Mode où l'historique et les cookies ne sont pas enregistrés.

---

## 🔹 3. Anglais Technique de Base

* Lire et comprendre : `variable`, `function`, `loop`, `error`, `undefined`, etc.
* Utiliser Deepl ou Google Translate pour t'aider au début.

---

## 🔹 4. Logique de Programmation (Avant JavaScript)

### 💡 Variables

```js
let age = 25;
```

### 💡 Conditions (if / else)

```js
if (age >= 18) {
  console.log("Majeur");
} else {
  console.log("Mineur");
}
```

### 💡 Boucles (Loops)

```js
for (let i = 0; i < 3; i++) {
  console.log("Hello");
}
```

### 💡 Fonctions

```js
function direBonjour(nom) {
  console.log("Bonjour " + nom);
}
```

### 💡 Tableaux (Arrays)

```js
let fruits = ["pomme", "banane", "orange"];
console.log(fruits[0]); // pomme
```

---

## 🔹 5. Terminal / Ligne de Commande (Base)

### 💡 Naviguer dans les dossiers

```bash
cd mon-dossier
```

### 💡 Lister les fichiers

```bash
ls        # Mac / Linux
dir       # Windows
```

### 💡 Créer des fichiers et dossiers

```bash
mkdir monprojet
touch index.html
```

---

## 🔹 6. Concepts Techniques Importants

### 💡 Console du navigateur

* Inspecter, déboguer, voir les erreurs JS.

### 💡 VS Code (ou éditeur de code)

* Créer, éditer, et organiser ton code avec confort.

### 💡 Git / GitHub (base)

* Suivre l’évolution du code et collaborer.

---

## 🔹 7. Protocoles Réseau & Notions Web

### 💡 Protocoles principaux

#### 📡 FTP (File Transfer Protocol)

* Pour transférer des fichiers entre PC et serveur.
* Remplacé souvent par **SFTP** (sécurisé).

#### 🧠 TCP (Transmission Control Protocol)

* Protocole fiable avec vérification d’ordre et erreurs.

#### ⚡ UDP (User Datagram Protocol)

* Très rapide mais sans garantie. Idéal pour les jeux et le streaming.

#### 📶 IP (Internet Protocol)

* Adresse unique pour chaque appareil en réseau.

### 💡 OSI (modèle en 7 couches)

| Couche | Nom                | Exemple               |
| ------ | ------------------ | --------------------- |
| 7      | Application        | HTTP, FTP, DNS        |
| 6      | Présentation       | SSL, TLS              |
| 5      | Session            | Connexion persistante |
| 4      | Transport          | TCP, UDP              |
| 3      | Réseau             | IP                    |
| 2      | Liaison de données | MAC                   |
| 1      | Physique           | Câbles, Wi-Fi         |

### 💡 htop (Linux uniquement)

* Affiche l’état de la mémoire, CPU, processus.
* Idéal pour vérifier la performance d'un serveur.

---

## 🔹 8. Bases de Données : SQL vs NoSQL

### 🗃️ SQL (Structured Query Language)

* Bases de données **relationnelles** (tables, lignes, colonnes).
* Exemple : MySQL, PostgreSQL, SQLite.
* Fort en relations complexes, transactions.

### 🧩 NoSQL (Not Only SQL)

* Bases **non relationnelles** (JSON, documents, colonnes, graphes).
* Exemple : MongoDB, Firebase, CouchDB.
* Plus flexible, évolutif, rapide pour des structures dynamiques.

| Type de base NoSQL | Description      |
| ------------------ | ---------------- |
| Document Store     | MongoDB, CouchDB |
| Clé/Valeur         | Redis, DynamoDB  |
| Colonne            | Cassandra, HBase |
| Graphe             | Neo4j, OrientDB  |

---

## 🔹 9. C’est quoi une Stack en Développement Web ?

> Une **stack** est une combinaison de technologies (langages, frameworks, bases de données) utilisées ensemble pour développer une application web complète.

### 💻 Stacks les plus connues

| Stack        | Technologies utilisées                   | Côté client (Frontend) | Côté serveur (Backend)     |
| ------------ | ---------------------------------------- | ---------------------- | -------------------------- |
| **MERN**     | MongoDB, Express, React, Node.js         | React                  | Express + Node.js          |
| **MEAN**     | MongoDB, Express, Angular, Node.js       | Angular                | Express + Node.js          |
| **LAMP**     | Linux, Apache, MySQL, PHP                | HTML/CSS/JS + PHP      | Apache + PHP               |
| **LEMP**     | Linux, Nginx, MySQL, PHP                 | HTML/CSS/JS + PHP      | Nginx + PHP                |
| **JAMstack** | JavaScript, APIs, Markup (HTML statique) | HTML/CSS/JS            | APIs tierces ou Serverless |

---

## 🔹 10. Suite de ton apprentissage

| Étape          | Concepts principaux                  |
| -------------- | ------------------------------------ |
| **HTML**       | Structure, balises, images, liens    |
| **CSS**        | Styles, responsive, animations       |
| **JavaScript** | Logique, DOM, événements             |
| **Node.js**    | Serveur backend, scripts             |
| **Express**    | API REST, routes                     |
| **MongoDB**    | Base NoSQL, requêtes                 |
| **React.js**   | Composants, état, interface réactive |

---

## 🚀 Astuce finale

> Ce document est ta fondation. Relis-le souvent. Ensuite, avance pas à pas, pratique tous les jours, et sois curieux.

