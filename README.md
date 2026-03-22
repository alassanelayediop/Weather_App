# 🌤️ Weather App

Application météo en temps réel développée en **Vanilla JavaScript**, utilisant l'API **OpenWeatherMap** pour afficher les conditions météorologiques actuelles et les prévisions sur 5 jours pour n'importe quelle ville du monde.

## 📸 Aperçu

![portfolio-5.jpg](assets/portfolio-5.jpg)
---

## ✨ Fonctionnalités

- 🔍 **Recherche par ville** — via le champ de recherche ou touche `Entrée`
- 🌡️ **Météo en temps réel** — température, humidité, vitesse du vent, condition météo
- 📅 **Prévisions sur 5 jours** — affichage des prévisions à 12h00 chaque jour
- 🎨 **Icônes dynamiques** — icône adaptée selon le type de météo (orage, pluie, neige, nuages...)
- ⚠️ **Gestion des erreurs** — message "ville non trouvée" si la recherche échoue
- 📱 **Design responsive** — s'adapte à toutes les tailles d'écran

---

## 🛠️ Stack technique

| Technologie        | Usage                       |
|--------------------|-----------------------------|
| HTML5              | Structure de la page        |
| CSS3               | Styles et design responsive |
| JavaScript (ES6+)  | Logique applicative         |
| OpenWeatherMap API | Données météo en temps réel |
| Fetch API          | Requêtes HTTP asynchrones   |

---

## 🚀 Démarrage

### 1. Cloner le projet
```bash
git clone https://github.com/alassanelayediop/Weather_App.git
cd Weather_App
```

### 2. Clé API
Le projet utilise l'API **OpenWeatherMap**. La clé est déjà incluse dans `script.js`. Si elle expire, crée un compte gratuit sur [openweathermap.org](https://openweathermap.org/api) et remplace la clé dans :

```javascript
// script.js
const apkikey = 'LA NOUVELLE CLE API'
```

### 3. Lancer l'application
Ouvre simplement `index.html` dans ton navigateur — aucune installation requise ! Ou utilisez **Live Server** sur VS Code pour le développement.

---

## 📡 API utilisée

**OpenWeatherMap** — 2 endpoints :

```
# Météo actuelle
GET https://api.openweathermap.org/data/2.5/weather?q={ville}&appid={clé}&units=metric

# Prévisions 5 jours (toutes les 3h)
GET https://api.openweathermap.org/data/2.5/forecast?q={ville}&appid={clé}&units=metric
```

Les prévisions affichées correspondent aux données à **12h00** pour chaque jour à venir.

---

## 🗂️ Structure du projet

```
Weather_App/
├── index.html              # Page principale
├── style.css               # Styles
├── script.js               # Logique JS (fetch, affichage)
└── assets/
    ├── bg.jpg              # Image de fond
    ├── weather/            # Icônes météo SVG
    │   ├── clear.svg
    │   ├── clouds.svg
    │   ├── rain.svg
    │   ├── drizzle.svg
    │   ├── snow.svg
    │   ├── thunderstorm.svg
    │   └── atmosphere.svg
    └── message/
        ├── search-city.png # Écran d'accueil
        └── not-found.png   # Ville non trouvée
```

---

## 🎯 Correspondance icônes / codes météo

| Code OpenWeatherMap | Icône affichée |
|---------------------|----------------|
| 200 – 232           | ⛈️ Orage       |
| 300 – 321           | 🌦️ Bruine     |
| 500 – 531           | 🌧️ Pluie      |
| 600 – 622           | ❄️ Neige       |
| 700 – 781           | 🌫️ Atmosphère |
| 800                 | ☀️ Ciel dégagé |
| 801 – 804           | ☁️ Nuageux     |

---

## 👨‍💻 Auteur

**Alassane Laye Diop**  
Étudiant en Master TDSI — Université Cheikh Anta Diop de Dakar  
[GitHub](https://github.com/alassanelayediop) • [LinkedIn](https://www.linkedin.com/in/alassane-laye-diop-0a6a57270)
