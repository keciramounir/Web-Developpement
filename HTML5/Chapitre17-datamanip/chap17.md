- HTML Web APIs
- Geolocation API
- Drag and Drop API
- Web Storage (localStorage & sessionStorage)
- Web Workers
- Server-Sent Events (SSE)

# 🌐 README - HTML Web APIs (en Français)

Les **Web APIs HTML** permettent à votre navigateur d’interagir avec l’environnement, de stocker des données localement, de gérer des événements en arrière-plan ou encore de communiquer avec un serveur. Voici tout ce que vous devez savoir 📚👇

---

## 🔌 1. HTML Web APIs - C'est quoi ?

🔧 Une **Web API** est une **interface de programmation** (API) fournie par les navigateurs qui permet aux développeurs d'accéder à des fonctionnalités comme :

- 📍 la géolocalisation,
- 📂 le glisser-déposer,
- 💾 le stockage local,
- 🧵 les threads en arrière-plan,
- 🔁 les événements envoyés par le serveur...

Ces APIs sont accessibles via **JavaScript**.

---

## 📍 2. HTML Geolocation API

La **Geolocation API** permet d'obtenir la position géographique de l'utilisateur (latitude, longitude...).

### ✅ Utilisation :

```javascript
navigator.geolocation.getCurrentPosition(function (position) {
  console.log("Latitude : " + position.coords.latitude);
  console.log("Longitude : " + position.coords.longitude);
});
```



### ⚠️ À savoir :

- 🔐 Nécessite l’autorisation de l’utilisateur.
- 🌐 Fonctionne mieux sur mobile ou avec le GPS activé.

---

## 📂 3. HTML Drag and Drop API

Permet de déplacer des éléments HTML à l’aide de la souris 🖱️.

### ✅ HTML :

```html
<div id="dragme" draggable="true">Faites glisser moi !</div>
<div id="zone" ondrop="drop(event)" ondragover="allowDrop(event)"></div>
```

### ✅ JavaScript :

```javascript
function allowDrop(ev) {
  ev.preventDefault();
}
function drop(ev) {
  ev.preventDefault();
  const data = ev.dataTransfer.getData("text");
  ev.target.appendChild(document.getElementById(data));
}
```

### 🔑 Attributs clés :

- `draggable="true"` : rend un élément déplaçable
- `ondragstart`, `ondrop`, `ondragover` : événements JS

---

## 💾 4. HTML Web Storage API

Permet de stocker des données localement dans le navigateur, **sans base de données**.

### 🧱 Deux types :

- `localStorage` 🔒 → persistant (reste après fermeture du navigateur)
- `sessionStorage` 🔓 → temporaire (disparaît à la fermeture de l’onglet)

### ✅ Exemple :

```javascript
localStorage.setItem("nom", "Mounir");
let nom = localStorage.getItem("nom"); // "Mounir"
sessionStorage.setItem("jeton", "abc123");
```

### 🧹 Supprimer :

```javascript
localStorage.removeItem("nom");
localStorage.clear(); // Tout effacer
```

---

## 🧵 5. HTML Web Workers API

Permet d’exécuter du JavaScript en **tâche de fond** (thread séparé), sans bloquer l’interface utilisateur.

### ✅ Fichier worker.js :

```javascript
// worker.js
onmessage = function (e) {
  postMessage("Résultat : " + e.data * 2);
};
```

### ✅ Main script :

```javascript
const worker = new Worker("worker.js");
worker.postMessage(10); // Envoie des données

worker.onmessage = function (e) {
  console.log(e.data); // Affiche : Résultat : 20
};
```

### ⚠️ Limitations :

- Pas d’accès au DOM
- Doit être hébergé en HTTPS ou localement

---

## 🔁 6. HTML Server-Sent Events (SSE)

Permet de **recevoir automatiquement des mises à jour du serveur** via une connexion HTTP persistante. (Utilisé pour les notifications, tableaux de bord en temps réel...).

### ✅ Côté client (HTML) :

```javascript
const source = new EventSource("/flux");

source.onmessage = function (event) {
  console.log("Donnée reçue :", event.data);
};
```

### ✅ Côté serveur (ex. Node.js Express) :

```javascript
app.get("/flux", (req, res) => {
  res.setHeader("Content-Type", "text/event-stream");
  setInterval(() => {
    res.write(`data: ${new Date().toISOString()}\n\n`);
  }, 1000);
});
```

### ⚙️ Avantages :

- Léger comparé à WebSocket
- Unidirectionnel (serveur → client)

---

## 🧠 Résumé des APIs

| API                   | Fonction principale                      | Support navigateur |
| --------------------- | ---------------------------------------- | ------------------ |
| 📍 Geolocation        | Obtenir la localisation de l’utilisateur | ✅ Oui             |
| 📂 Drag and Drop      | Déplacer des éléments avec la souris     | ✅ Oui             |
| 💾 Web Storage        | Stocker des données localement           | ✅ Oui             |
| 🧵 Web Workers        | Threads JS en parallèle (non bloquants)  | ✅ Oui             |
| 🔁 Server-Sent Events | Recevoir des messages serveur en continu | ✅ Oui             |

---

## 🚀 Ressources utiles

- 📘 [MDN Web Docs - APIs HTML](https://developer.mozilla.org/fr/docs/Web/API)
- 📍 [API Geolocation](https://developer.mozilla.org/fr/docs/Web/API/Geolocation_API)
- 📂 [API Drag and Drop](https://developer.mozilla.org/fr/docs/Web/API/HTML_Drag_and_Drop_API)
- 💾 [Web Storage](https://developer.mozilla.org/fr/docs/Web/API/Web_Storage_API)
- 🧵 [Web Workers](https://developer.mozilla.org/fr/docs/Web/API/Web_Workers_API)
- 🔁 [SSE - Server-sent events](https://developer.mozilla.org/fr/docs/Web/API/Server-sent_events)

---

📌 **Astuce** : Combinez ces APIs pour créer des applications modernes, interactives et performantes 💡
Exemple : une carte en temps réel avec géolocalisation + SSE pour les alertes météo ⚡

---
````
