---
icon: material/react
---

# <span class="h1">Débuter avec React</span>

 <p class="intro">
    Comprendre la logique de <strong>React</strong> pour construire une application interactive et dynamique..
</p>

---

## <span class="h2">Présentation</span>

<div class="presentation">
    <p style="color: #333; line-height: 1.6;">
        Développer une application de prise de commande pour un restaurant de type fast food en utilisant <strong>Redux</strong> et <strong>redux Toolkit</strong>.
    </p>
    <p style="color: #333; line-height: 1.6;">
        L'objectif principal est d'intégrer <strong>Redux</strong> à une application <strong>React</strong>.
        Redux est une <strong>bibliothèque JavaScript de gestion d'état</strong>. Elle permet de centraliser et structurer les données d'une application.
    </p>
</div>

---

## <span class="h2">Objectifs</span>

<span style= "color: #64b5f6 !important;">:material-lightbulb-on:</span> Comprendre les principes de React

<span style= "color: #64b5f6 !important;">:material-lightbulb-on:</span>  Créer une application React

<span style= "color: #64b5f6 !important;">:material-lightbulb-on:</span>  Rendre une application dynamique

---

## <span class="h2">Appréhender la logique React</span>

[Cour OpenClassroom : Débuter avec React](https://openclassrooms.com/fr/courses/8710331-debutez-avec-react)

C'est un **framework front-end**.

!!! note "Note"
    On appelle framework **front-end** tout ensemble de classes, fonctions et utilitaires qui nous facilite la création d'applications web. Ces outils sont compatibles avec tous les navigateurs modernes

**React** est un projet open-source, distribué sous la licence MIT et développé principalement par **Meta**. Leurs produits web et mobile tels que *Facebook*, *Instagram*, *WhatsApp*, reposent en grande partie sur cette technologie.

L'ambition de ***React*** est de créer des interfaces utilisateurs avec un outil rapide et modulaire. L'idée principale derrière React est que vous construisiez votre application à partir de ***composants***.

!!! info "Information"
    Un composant = **HTML** + **CSS** + **JS**.

Alors qu'elle est la différence entre un **framework** et une **librairie** ?

- Un **framework** est un ensemble d'outils ultra complets permettant de **créer une application de A à Z** et fournissant tous les outils nécessaires au développement d'une application.

- Une bibliothèque **s'ajoute à une partie** de votre application. 

---

## <span class="h2">Créer notre App React</span>

### Prérequis

- Node.js installé
- npm installé

### Installation

Pour créer une application react:

```jsx
npx create-react-app MyApp
```

```jsx
# Creer App React avec Vite :
npm create vite@latest base-react -- --template react
```

### Commandes de Bases de `npm`

```c
# Compile l’application pour la production dans le dossier `build`. 
> npm run build
```

React est regroupé en mode production et optimisé pour de meilleures performances.

Les fichiers générés sont minifiés et les noms de fichiers incluent des hash.  
L’application est alors prête à être déployée.

```c
# Lance le runner de tests en mode interactif.
> npm test
```

```c
# Lance l application :
> npm start
```

---

## <span class="h2">Créez votre premier composant React</span>

- `App.jsx` est le **composant principal**

Écrivons maintenant notre premier composant (tous les composants React sont des fonctions).

!!! warning "Warning"
    Dans un composant React, tu ne peux retourner qu’un seul élément parent.

---

## <span class="h2">Manipulez des données dans vos composants JSX</span>

### Qu'est-ce que JSX ?

**JSX** signifie "***JavaScript Extension***" et est une syntaxe propre à React. Elle permet de **mêler le HTML et le JS** en utilisant une syntaxe à balises qui ressemble au HTML, mais qui est en réalité du JavaScript. Le JSX est considéré comme la manière la plus compréhensible d'écrire des composants React.

En React, les accolades **`{`** et **`}`**  sont particulièrement utiles.

!!! note "Note"
    Dès qu'il s'agit d'expressions JavaScript, elles sont écrites entre accolades.

Ça nous permet d'*appliquer des expressions JavaScript directement dans notre JSX* pour :

- Afficher des variables
- Faire des calculs

### Afficher des variables

```jsx
// pour une string
const title = "La maison jungle"
<div>{title}</div>

// pour un nombre
const price = 15
<div>{price}€</div>
```

### Faire de calculs

```jsx
<div>Total: {8 + 10 + 15}Euros</div>
```

### Transformer des données

```jsx
const name = "La maison Jungle"
<h1>name.toUpperCase()</h1>
```

### Utiliser des conditions

```jsx
const isOpen = true
<div>{isOpen ? 'Boutique ouverte' : 'Boutique fermée'}</div>
```

---

## <span class="h2">En résumé</span>

- Une interface utilisateur (ou UI) est **constituée de multiples composants React** qui :
    - Sont réutilisables ; par exemple, un bouton, un élément dans une liste, un titre.
    - Regroupent la structure, les styles et le comportement d'un élément.
    - Sont composés en combinant d'autres composants plus simples.
  
---

- Le **JSX** est une syntaxe créée par React *permettant d'écrire du JavaScript* qui ressemble à du HTML. Il faut suivre quelques règles :
    - Deux composants doivent toujours être wrappés dans un seul composant parent.
    - Les noms des composants commencent par une **majuscule**.
    - Toutes les balises doivent être fermées.

---

- Les accolades ***`{}`*** permettent d'insérer des expressions JavaScript dans le JSX pour créer des interfaces dynamiques.

---

## <span class="h2">Création projet React avec Vite</span>

### Structure du projet

```text
la-maison-jungle/
├── public/                 # Fichiers statiques
│   └── vite.svg
├── src/                    # Code source de l’application
│   ├── assets/             # Images et ressources
│   ├── App.css             # Styles du composant App
│   ├── App.jsx             # Composant principal
│   ├── index.css           # Styles globaux
│   └── main.jsx            # Point d’entrée de l’application
├── index.html              # Template HTML
├── package.json            # Configuration et dépendances
└── vite.config.js          # Configuration Vite
```

---

## <span class="h2">Affichez du contenu dynamique grâce aux listes et aux conditions</span>

### Créez des listes dynamiques avec vos données

???+ note "Note"
    En développement, vous travaillerez constamment avec des listes de données : produits, utilisateurs, articles... Plutôt que de copier-coller du code, vous pouvez ***directement itérer sur vos données et générer des composants React automatiquement***.

La méthode JavaScript  **`map()`**  transforme chaque élément d'un tableau en appliquant une fonction, puis renvoie un nouveau tableau avec les résultats.

```jsx
const numbers = [1, 2, 3, 4]
const doubles = numbers.map(x => x * 2) // [2, 4, 6, 8]
```

En React, **`map()`** va nous permettre de **transformer une liste de données en liste de composants JSX**. Voyons ça en pratique.

- Pour parcourir une `map` et l'afficher :

```jsx
const plantList = [
  'monstera',
  'ficus lyrata', 
  'pothos argenté',
  'yucca',
  'palmier'
]

const ShoppingList = () => {
  return (
    <ul>
      {plantList.map((plant, index) => (
        <li key={`${plant}-${index}`}>{plant}</li>
      ))}
    </ul>
  )
}

export default ShoppingList
```

Pour chaque plante, React crée :

```jsx
<li>Nom de la plante</li>
```

- La key sert à **identifier chaque élément de la liste** pour React.

```jsx
key={`${plant}-${index}`}
```

???+ infos "Information"
    La méthode **`map()`** permet d'itérer sur des données et de retourner un tableau d'éléments. Par ailleurs, les méthodes **`forEach()`**, **`filter()`**, **`reduce()`**, etc., qui permettent de manipuler des tableaux, seront également vos alliés en React.

- Pour recuperer une categories de plantes :

```js
// Fichier data.js
export const plantList = [
  {
    name: "monstera",
    category: "classique",
    id: "1ed",
  },
  {
    name: "ficus lyrata",
    category: "classique",
    id: "2ab",
  }
]
```

```jsx
// Fichier composant jsx :
import { plantList } from '../data/list_plant'

const ShoppingList = () => {
    // Récupérer les catégories (sans doublons) :
    const categories = [...new Set(plantList.map(plant => plant.category))]

    return (
        <ul>
            {categories.map(category => (
                <li key={category}>{category}</li>
            ))}
        </ul>
    )
}

export default ShoppingList
```

???+ note "Explication rapide"
    - **`map`** → extrait une propriété (category)
    - **`Set`** → supprime les doublons
    - **`[...]`** → retransforme en tableau
    - **`key={category}`** → clé unique

### Affichez du contenu de manière conditionnelle

```jsx
const plantList = [
  {
    name: 'monstera',
    category: 'classique',
    id: '1ed',
    isBestSale: true
  },
  {
    name: 'ficus lyrata',
    category: 'classique', 
    id: '2ab',
    isBestSale: false
  }
]

const ShoppingList = () => {
  return (
    <ul>
      {plantList.map((plant) => (
        <li key={plant.id}>
          {plant.isBestSale ? <span>🔥 </span> : <span>👎 </span>}
          {plant.name}
        </li>
      ))}
    </ul>
  )
}
```

Il existe une syntaxe encore plus élégante pour afficher quelque chose ***seulement si une condition est vraie*** grace a l'operateur **`&&`**:

```jsx
{plant.isBestSale && <span>🔥 </span>}
```
