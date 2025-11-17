# 📖 Silly Story Generator

Un générateur d'histoires aléatoires absurdes et amusantes ! Ce projet génère des histoires loufoques en combinant des personnages, des lieux et des actions de manière aléatoire.

## 🎯 Aperçu

Ce projet est un générateur d'histoires interactif qui permet de :
- Générer des histoires aléatoires avec différentes combinaisons
- Personnaliser le nom du personnage principal
- Convertir les unités entre le système américain (US) et britannique (UK)

## ✨ Fonctionnalités

- **🎲 Génération aléatoire** : Chaque histoire combine aléatoirement des personnages, des lieux et des événements
- **✏️ Personnalisation du nom** : Remplacez "Bob" par le nom de votre choix
- **🌍 Conversion d'unités** : Basculez entre les unités américaines (Fahrenheit, pounds) et britanniques (Centigrade, stone)
- **🎨 Interface simple** : Design épuré et facile à utiliser

## 📂 Structure du projet

```
silly-story-generator/
│
├── index.html          # Structure HTML de l'application
├── main.js             # Logique JavaScript du générateur
└── README.md           # Documentation du projet
```

## 🚀 Installation et utilisation

### Prérequis

- Un navigateur web moderne (Chrome, Firefox, Safari, Edge)
- Aucune dépendance externe requise

### Installation

1. **Clonez le dépôt** :
   ```bash
   git clone https://github.com/VotreUsername/silly-story-generator.git
   ```

2. **Naviguez dans le dossier** :
   ```bash
   cd silly-story-generator
   ```

3. **Ouvrez le fichier HTML** :
   - Double-cliquez sur `index.html`
   - Ou faites un clic droit → "Ouvrir avec" → Votre navigateur

### Utilisation

1. **Entrez un nom personnalisé** (optionnel) :
   - Tapez un nom dans le champ "Enter custom name"
   - Ce nom remplacera "Bob" dans l'histoire

2. **Choisissez le système d'unités** :
   - **US** : Fahrenheit et pounds (par défaut)
   - **UK** : Centigrade et stone

3. **Générez une histoire** :
   - Cliquez sur le bouton "Generate random story"
   - Une nouvelle histoire apparaîtra avec des éléments aléatoires

4. **Régénérez** :
   - Cliquez à nouveau pour obtenir une nouvelle combinaison

## 🎮 Exemple d'histoire

**Sans personnalisation :**
> It was 94 fahrenheit outside, so Willy the Goblin went for a walk. When they got to Disneyland, they stared in horror for a few moments, then spontaneously combusted. Bob saw the whole thing, but was not surprised — Willy the Goblin weighs 300 pounds, and it was a hot day.

**Avec nom personnalisé (Alice) et unités UK :**
> It was 33 centigrade outside, so Father Christmas went for a walk. When they got to the White House, they stared in horror for a few moments, then melted into a puddle on the sidewalk. Alice saw the whole thing, but was not surprised — Father Christmas weighs 21 stone, and it was a hot day.

## 🛠️ Technologies utilisées

- **HTML5** : Structure de la page
- **CSS3** : Styles inline pour la mise en forme
- **JavaScript (Vanilla)** : Logique du générateur
  - Manipulation du DOM
  - Événements
  - Tableaux et fonctions
  - Expressions régulières

## 📝 Détails techniques

### Éléments aléatoires

Le générateur utilise trois catégories d'éléments :

**Personnages (`insertX`) :**
- Willy the Goblin
- Big Daddy
- Father Christmas

**Lieux (`insertY`) :**
- the soup kitchen
- Disneyland
- the White House

**Actions (`insertZ`) :**
- spontaneously combusted
- melted into a puddle on the sidewalk

### Conversions d'unités

| US | UK | Formule |
|----|----|----|
| 94°F | 33°C | (94-32) × 5/9 |
| 300 pounds | 21 stone | 300 ÷ 14 |

### Fonctions principales

```javascript
// Sélection aléatoire d'un élément
randomValueFromArray(array)

// Génération de l'histoire
result()
```

## 🎨 Personnalisation

### Ajouter de nouveaux éléments

Modifiez les tableaux dans `main.js` :

```javascript
const insertX = [
    "Willy the Goblin", 
    "Big Daddy", 
    "Father Christmas",
    "Superman",           // Nouvel élément
    "The Tooth Fairy"     // Nouvel élément
];
```

### Modifier les styles

Les styles sont intégrés dans `index.html` dans la balise `<style>`. Vous pouvez :
- Changer les couleurs
- Modifier la police
- Ajuster la largeur de la page
- Personnaliser l'apparence du bouton

### Changer le modèle d'histoire

Modifiez `storyText` dans `main.js` :

```javascript
const storyText = "Votre nouveau modèle avec :insertx:, :inserty: et :insertz:";
```

## 🐛 Bugs connus

- ⚠️ Le texte original contient un caractère mal encodé : `â€"` au lieu de `—` (em dash)
- Les tableaux de valeurs aléatoires contiennent des virgules dans les chaînes (à nettoyer)
- Faute de frappe dans `insertY` : "kitcher" devrait être "kitchen"
- Faute de frappe dans `insertZ` : "pusddle" devrait être "puddle"

### Corrections suggérées

```javascript
// Correction du texte principal
const storyText = "It was 94 fahrenheit outside, so :insertx: went for a walk. When they got to :inserty:, they stared in horror for a few moments, then :insertz:. Bob saw the whole thing, but was not surprised — :insertx: weighs 300 pounds, and it was a hot day.";

// Correction des tableaux
const insertX = ["Willy the Goblin", "Big Daddy", "Father Christmas"];
const insertY = ["the soup kitchen", "Disneyland", "the White House"];
const insertZ = ["spontaneously combusted", "melted into a puddle on the sidewalk"];
```

## 🚀 Améliorations possibles

- [ ] Ajouter plus de personnages, lieux et actions
- [ ] Créer plusieurs modèles d'histoires
- [ ] Ajouter des animations lors de la génération
- [ ] Sauvegarder les histoires favorites
- [ ] Partager les histoires sur les réseaux sociaux
- [ ] Ajouter des images pour les personnages
- [ ] Mode sombre / clair
- [ ] Support multilingue

## 📚 Apprentissage

Ce projet est idéal pour apprendre :
- ✅ Manipulation du DOM JavaScript
- ✅ Gestion des événements
- ✅ Utilisation des tableaux et boucles
- ✅ Méthodes de chaînes de caractères (`replace`, `replaceAll`)
- ✅ Conditions et logique
- ✅ Génération de nombres aléatoires
- ✅ Interactions formulaire HTML

## 🤝 Contribution

Les contributions sont les bienvenues ! Pour contribuer :

1. Forkez le projet
2. Créez une branche pour votre fonctionnalité (`git checkout -b feature/NouvelleFonctionnalité`)
3. Committez vos changements (`git commit -m 'Ajout d'une nouvelle fonctionnalité'`)
4. Poussez vers la branche (`git push origin feature/NouvelleFonctionnalité`)
5. Ouvrez une Pull Request

## 📄 Licence

Ce projet est fourni à des fins éducatives. Libre d'utilisation et de modification.

## 👤 Auteur

**Votre Nom**
- GitHub: @Adeshero(https://github.com/Adeshero)

## 🙏 Remerciements

- Projet réaliser grâce aux exercice d'apprentissages du site web MDN
- Projet inspiré des exercices d'apprentissage JavaScript

---

**⭐ Si vous aimez ce projet, n'hésitez pas à lui donner une étoile !**