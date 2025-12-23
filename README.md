# 🛡️ DDoS Attack Visualizer

Une visualisation 3D interactive pour expliquer les attaques DDoS de manière pédagogique. Idéal pour les formations en cybersécurité, les sensibilisations en entreprise ou les présentations grand public.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![Three.js](https://img.shields.io/badge/Three.js-000000?style=flat&logo=three.js&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-blue.svg)

## 🎯 Objectif

Permettre à **M. et Mme Tout-le-monde** de comprendre visuellement :
- Ce qu'est une attaque DDoS
- Comment les botnets submergent un serveur
- Pourquoi les utilisateurs légitimes ne peuvent plus accéder au service
- Comment fonctionne une protection anti-DDoS

## ✨ Fonctionnalités

### Visualisation 3D temps réel
- **Serveur central** avec LEDs d'état et indicateurs visuels
- **Clients légitimes** (sphères vertes) qui envoient des requêtes et reçoivent des réponses
- **Attaquants/Botnets** (octaèdres rouges) qui submergent le serveur
- **Trafic bidirectionnel** visible : requêtes (vert) → serveur → réponses (jaune)

### Simulation d'attaque progressive
- 5 niveaux d'intensité d'attaque
- Montée en charge progressive du serveur
- Indicateurs visuels de stress (LEDs orange → rouge, tremblement)
- Message **503 - SERVICE INDISPONIBLE** quand le serveur crash

### Comportement réaliste des clients
- Les clients passent en orange quand leurs requêtes échouent
- Après plusieurs échecs, ils se déconnectent (passent en gris)
- Le serveur ne répond plus aux requêtes légitimes

### Système de défense Anti-DDoS
- Bouclier visuel (dôme géométrique bleu)
- Les paquets malveillants **rebondissent** sur le bouclier
- Les requêtes légitimes **traversent** le bouclier
- Élimination progressive des botnets
- Reconnexion progressive des clients légitimes

### Interface utilisateur
- HUD avec statut serveur et requêtes/seconde
- Panneau de statistiques temps réel
- Indicateur d'intensité d'attaque
- Boutons de contrôle intuitifs

## 🚀 Démo

Ouvrez simplement le fichier `index.html` dans votre navigateur.

### Contrôles

| Bouton | Action |
|--------|--------|
| **Normal** | Réinitialise à un trafic normal |
| **+ Attaque** | Augmente l'intensité de l'attaque (5 niveaux) |
| **🛡️ Anti-DDoS** | Active/désactive la protection |
| **Reset** | Remet tout à zéro |

## 📦 Installation

```bash
# Cloner le repository
git clone https://github.com/votre-username/ddos-visualizer.git

# Ouvrir dans le navigateur
open index.html
# ou
start index.html  # Windows
```

Aucune dépendance à installer, aucun serveur requis. Three.js est chargé via CDN.

## 🛠️ Technologies

- **Three.js** (r128) - Rendu 3D WebGL
- **HTML5 / CSS3** - Interface et animations
- **JavaScript** vanilla - Logique de simulation
- **Google Fonts** - Orbitron & Rajdhani

## 📚 Contenu pédagogique

La page inclut des explications sur :

| Thème | Description |
|-------|-------------|
| 🌐 Le Principe | Définition du DDoS (Distributed Denial of Service) |
| 🤖 Les Botnets | Réseaux d'ordinateurs zombies |
| 🚪 L'Analogie | Comparaison avec une boutique bloquée |
| 🛡️ La Défense | Solutions anti-DDoS (Cloudflare, AWS Shield) |
| 💥 Conséquences | Impact business et technique |
| ⚖️ Aspect Légal | Article 323-2 du Code pénal français |

## 🎨 Personnalisation

### Modifier les paramètres de simulation

```javascript
// Dans le script, ajustez ces constantes :
const MAX_PHASES = 5;                           // Nombre de niveaux d'attaque
const ATTACKERS_PER_PHASE = [0, 20, 50, 100, 180, 300];  // Attaquants par niveau
const SERVER_CAPACITY = 400;                    // Capacité max du serveur
const SHIELD_RADIUS = 22;                       // Taille du bouclier
const MAX_PACKETS = 120;                        // Limite de paquets (performance)
```

### Modifier les couleurs

```javascript
// Couleurs des éléments
const colors = {
    request: 0x44ffaa,   // Requêtes clients (vert)
    response: 0xffdd00,  // Réponses serveur (jaune)
    attack: 0xff2255     // Paquets d'attaque (rouge)
};
```

## 📱 Responsive

L'interface s'adapte aux écrans mobiles et tablettes avec :
- Réduction de la hauteur du canvas
- Boutons adaptés au tactile
- Masquage des statistiques détaillées sur petit écran

## ⚡ Performance

Optimisations intégrées :
- Limite du nombre de paquets simultanés
- Géométries simplifiées
- Mise à jour UI throttlée
- Pixel ratio limité

## 🤝 Contribution

Les contributions sont les bienvenues ! N'hésitez pas à :
- 🐛 Signaler des bugs
- 💡 Proposer des améliorations
- 🔧 Soumettre des pull requests

## 📄 Licence

Ce projet est sous licence MIT. Voir le fichier [LICENSE](LICENSE) pour plus de détails.

## 🏢 À propos

Développé pour les formations en cybersécurité.

---

### 🛡️ Besoin d'accompagnement en cybersécurité ?

**[YPSI](https://ypsi.fr)** vous accompagne dans la protection de vos infrastructures :
- ✅ Audit de sécurité
- ✅ Gestion de crise
- ✅ Formation OSINT
- ✅ Exercices cyber

📧 Contact : [bonjour@ypsi.fr](mailto:bonjour@ypsi.fr)
