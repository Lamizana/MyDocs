---
title: Analyse de Dés
---

# <span class="h1">Analyse de Dés avec NumPy</span>

---

## <span class="h2">Introduction</span>

<em>Dans ce projet, nous allons créer un <strong>analyseur de dés</strong> pour maîtriser les fondamentaux de NumPy. Nous allons simuler des lancers de dés et analyser les résultats.</em></p>

---

## <span class="h2">Objectifs du Projet</span>

- Créer des tableaux NumPy
- Générer des nombres aléatoires
- Calculer des statistiques
- Analyser des probabilités
- Visualiser des données

!!! info "Prérequis"
    Ce projet nécessite NumPy installé : `pip install numpy`

---

## <span class="h2">Partie 1: Création du Premier Dés</span>

### Création d'un tableau

```python
import numpy as np

# Les faces d'un dé à 6 faces
faces = np.array([1, 2, 3, 4, 5, 6])

print("Faces du dé:", faces)
print("Nombre de faces:", len(faces))
print("Type de données:", faces.dtype)
```

**Résultat:**
```
Faces du dé: [1 2 3 4 5 6]
Nombre de faces: 6
Type de données: int64
```

---

### Résumé: Création de tableaux

| Méthode | Description | Exemple |
|---------|-------------|---------|
| `np.array([...])` | Tableau à partir d'une liste | `np.array([1,2,3])` |
| `np.arange(start, stop, step)` | Suite arithmétique | `np.arange(1, 7)` |
| `np.array(list(range(...)))` | Convertir une liste | `np.array(range(1,7))` |

---

## <span class="h2">Partie 2: Lancer un Dé</span>

### Première simulation

```python
import numpy as np

# Dé à 6 faces
faces = np.array([1, 2, 3, 4, 5, 6])

# Lancer un dé aléatoire
resultat = np.random.choice(faces)

print(f"Vous avez lancé: {resultat}")
```

### Lancer plusieurs dés

```python
# Lancer 3 dés
lancers = np.random.choice(faces, size=3)

print("Résultats:", lancers)
print("Somme:", np.sum(lancers))
print("Plus grand:", np.max(lancers))
print("Plus petit:", np.min(lancers))
```

---

### Résumé: Nombres aléatoires

```python
np.random.choice(tableau)           # 1 élément aléatoire
np.random.choice(tableau, size=n)   # n éléments
np.random.choice(tableau, size=n, replace=True)  # Avec remise
np.random.choice(tableau, size=n, replace=False)  # Sans remise
```

!!! info "replace=True vs False"
    - **Avec remise**: Le même élément peut apparaître plusieurs fois
    - **Sans remise**: Chaque élément n'apparaît qu'une seule fois

---

## <span class="h2">Partie 3: Statistiques sur 1000 Lancers</span>

### Simulation de masse

```python
import numpy as np

faces = np.array([1, 2, 3, 4, 5, 6])

# Simuler 1000 lancers de dé
nb_lancers = 1000
resultats = np.random.choice(faces, size=nb_lancers)

print("Résultats des 20 premiers lancers:")
print(resultats[:20])

# Statistiques de base
print(f"\n=== Statistiques sur {nb_lancers} lancers ===")
print(f"Moyenne: {np.mean(resultats):.2f}")
print(f"Médiane: {np.median(resultats):.2f}")
print(f"Écart-type: {np.std(resultats):.2f}")
print(f"Min: {np.min(resultats)}")
print(f"Max: {np.max(resultats)}")
```

---

### Compter les occurrences

```python
# Compter combien de fois chaque face apparaît
comptage = np.bincount(resultats)[1:]  # [1:] car pas de 0

print("Nombre d'apparitions par face:")
for i, count in enumerate(comptage, 1):
    print(f"  Face {i}: {count} fois")

# Fréquence (pourcentage)
frequence = comptage / nb_lancers * 100

print("\nFréquence (en %):")
for i, freq in enumerate(frequence, 1):
    print(f"  Face {i}: {freq:.1f}%")
```

---

### Résumé: Statistiques

| Fonction | Description |
|----------|-------------|
| `np.mean(arr)` | Moyenne |
| `np.median(arr)` | Médiane |
| `np.std(arr)` | Écart-type |
| `np.min(arr)` / `np.max(arr)` | Min / Max |
| `np.sum(arr)` | Somme |
| `np.bincount(arr)` | Compte les occurrences |

!!! info "Théorie"
    Pour un dé parfait, chaque face devrait apparaître environ 16.67% du temps (1/6).

---

## <span class="h2">Partie 4: Visualisation</span>

### Créer un histogramme

```python
import numpy as np

faces = np.array([1, 2, 3, 4, 5, 6])
resultats = np.random.choice(faces, size=10000)

# Compter les occurrences
comptage = np.bincount(resultats)[1:]

# Afficher avec des barres (sans matplotlib)
print("=== Distribution des résultats ===")
for i, count in enumerate(comptage, 1):
    barre = "=" * (count // 100)
    print(f"Face {i}: {barre} ({count})")
```

---

## <span class="h2">Exercice: Comparaison Théorie vs Simulation</span>

```python
import numpy as np

faces = np.array([1, 2, 3, 4, 5, 6])

# Théorique (pourcentage attendu)
print("=== Comparaison Théorie vs Simulation ===\n")

for n in [100, 1000, 10000, 100000]:
    resultats = np.random.choice(faces, size=n)
    comptage = np.bincount(resultats)[1:]
    frequence = comptage / n * 100
    
    print(f"Après {n:>6} lancers:")
    print(f"  Théorique: 16.67% pour chaque face")
    print(f"  Réel:     {frequence[0]:.2f}% {frequence[1]:.2f}% {frequence[2]:.2f}% {frequence[3]:.2f}% {frequence[4]:.2f}% {frequence[5]:.2f}%")
    print()
```

!!! warning "Observation"
    Plus le nombre de lancers augmente, plus les résultats se rapprochent de la théorie (16.67%)

---

## <span class="h2">Projet Final: Analyseur de Dés Complet</span>

Voici le code complet qui combine tout ce que nous avons appris:

```python
import numpy as np

class AnalyseurDe:
    def __init__(self, nb_faces=6):
        self.nb_faces = nb_faces
        self.faces = np.arange(1, nb_faces + 1)
        self.resultats = np.array([])
    
    def lancer(self, nb_lancers=1):
        """Lancer le dé nb_lancers fois"""
        nouveaux = np.random.choice(self.faces, size=nb_lancers)
        self.resultats = np.concatenate([self.resultats, nouveaux])
        return nouveaux
    
    def statistiques(self):
        """Afficher les statistiques"""
        n = len(self.resultats)
        print(f"=== Analyse sur {n} lancers ===")
        print(f"Moyenne: {np.mean(self.resultats):.4f}")
        print(f"Médiane: {np.median(self.resultats):.4f}")
        print(f"Écart-type: {np.std(self.resultats):.4f}")
        print(f"Min: {np.min(self.resultats)}, Max: {np.max(self.resultats)}")
    
    def distribution(self):
        """Afficher la distribution"""
        n = len(self.resultats)
        comptage = np.bincount(self.resultats.astype(int))[1:self.nb_faces+1]
        
        print("\nDistribution:")
        for i, count in enumerate(comptage, 1):
            freq = count / n * 100
            attendu = 100 / self.nb_faces
            diff = freq - attendu
            barre = "=" * int(freq / 2)
            print(f"  Face {i}: {barre} {freq:5.2f}% (attendu: {attendu:.2f}%, diff: {diff:+.2f}%)")
    
    def proba(self, face):
        """Probabilité d'obtenir une face"""
        count = np.sum(self.resultats == face)
        return count / len(self.resultats) * 100

# Utilisation
de = AnalyseurDe(6)
de.lancer(10000)  # Lancer 10000 fois
de.statistiques()
de.distribution()

print(f"\nProba d'obtenir 6: {de.proba(6):.2f}%")
```

---

## <span class="h2">Défis Bonus</span>

1. **Dés pipés**: Modifier le code pour que certaines faces soient plus probables
2. **Plusieurs dés**: Simuler 2 dés et analyser la somme (7 est le plus fréquent!)
3. **Suite consécutive**: Compter les suites consécutives (ex: 1,2,3 apparaît combien de fois?)
4. **Jeu**: Créer un jeu de dés simple

!!! info "Prochain pas"
    Essayez ces défis pour renforcer vos connaissances!

---

## <span class="h2">Exercice Interactif</span>

Essayer le projet directement:

[Ouvrir avec Basthon](https://basthon.fr/){ target="_blank" .md-button }
