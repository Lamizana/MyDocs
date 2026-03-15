# <span class="h1">Variables et Affectation</span>

---

## <span class="h2">Introduction</span>

Les variables sont des **conteneurs** qui permettent de stocker des données en mémoire. Elles sont essentielles dans tout programme informatique.

!!! info "Analogie"
    Une variable c'est comme une boîte avec une étiquette. On met une valeur dans la boîte, et on peut la récupérer grâce à l'étiquette.

---

## <span class="h2">Créer une Variable</span>

En Python, créer une variable est simple :

```python
nom = "Alex"
age = 25
taille = 1.75
```

### Convention de nommage

| Règle | Correct | Incorrect |
|-------|---------|-----------|
| Minuscules | `mon_nom` | `monNom` |
| Pas d'espace | `age_utilisateur` | `age utilisateur` |
| Pas de chiffre au début | `age1` | `1age` |
| Pas de mot réservé | `print_` | `print` |

!!! tip "Bonnes pratiques"
    Utilisez le **snake_case** : `mon_nom_de_variable`

---

## <span class="h2">Affectation Multiple</span>

Python permet d'affecter plusieurs variables en une ligne :

```python
x, y, z = 1, 2, 3
print(x)  # 1
print(y)  # 2
print(z)  # 3
```

### Initialiser à la même valeur

```python
a = b = c = 0
print(a, b, c)  # 0 0 0
```

---

## <span class="h2">Modifier une Variable</span>

On peut modifier la valeur d'une variable à tout moment :

```python
compteur = 0
print(compteur)  # 0

compteur = 1
print(compteur)  # 1
```

### Opérations combinées

```python
x = 5
x = x + 1  # x = 6
x += 3     # x = 9 (forme abrégée)
```

---

## <span class="h2">Constantes</span>

Une **constante** est une variable dont la valeur ne doit pas changer. Python n'a pas de vraies constantes, mais par convention :

```python
MAX_SCORE = 100
TAUX_TVA = 0.20
PI = 3.14159
```

!!! warning "Important"
    Par convention, les constantes s'écrivent en **MAJUSCULES**.

---

## <span class="h2">Supprimer une Variable</span>

```python
nom = "Alex"
print(nom)  # Alex

del nom
print(nom)  # Erreur: name 'nom' is not defined
```

---

## <span class="h2">Afficher une Variable</span>

```python
nom = "Alex"
print(nom)           # Alex
print("Bonjour", nom)  # Bonjour Alex
```

---

## <span class="h2">Résumé</span>

| Concept | Description |
|---------|-------------|
| `x = 5` | Créer une variable |
| `x, y = 1, 2` | Affectation multiple |
| `x += 1` | Incrémentation |
| `del x` | Supprimer |
| `MAJUSCULES` | Convention constante |

---

## <span class="h2">Exemples</span>

### Exemple 1: Gestion d'un score

```python
score = 0
print("Score initial:", score)

score += 10
print("Après bonus:", score)

score -= 3
print("Après pénalité:", score)
```

### Exemple 2: Échanger deux variables

```python
a = 5
b = 10

# Méthode classique
temp = a
a = b
b = temp

# En Python (plus simple)
a, b = b, a
```
