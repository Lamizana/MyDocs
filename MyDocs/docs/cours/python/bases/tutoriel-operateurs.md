# <span class="h1">Opérateurs</span>

---

## <span class="h2">Introduction</span>

Les opérateurs permettent de **manipuler les données**. 
Python en propose plusieurs catégories.

???+ note "Note"
    Comme d'habitude, si vous n'avez pas ou la flemme de créer un environnement python :

    [Ouvrir avec Basthon](https://basthon.fr/){ target="_blank" .md-button }

---

## <span class="h2">Opérateurs Arithmétiques</span>

Voici la liste de tous les opérateurs logique :

| Opérateur | Description      | Exemple   | Résultat |
|-----------|------------------|-----------|----------|
| `+`       | Addition         | `5 + 3`   | `8`      |
| `-`       | Soustraction     | `10 - 4`  | `6`      |
| `*`       | Multiplication   | `3 * 7`   | `21`     |
| `/`       | Division         | `15 / 4`  | `3.75`   |
| `//`      | Division entière | `15 // 4` | `3`      |
| `%`       | Modulo (reste)   | `15 % 4`  | `3`      |
| `**`      | Exponentiation   | `2 ** 3`  | `8`      |

### Exemples

```python
# Addition
print(10 + 5)    # 15

# Soustraction
print(10 - 5)    # 5

# Multiplication
print(10 * 5)    # 50

# Division
print(10 / 4)    # 2.5

# Division entière
print(10 // 4)   # 2

# Modulo (reste de la division)
print(10 % 4)    # 2

# Exponentiation
print(2 ** 4)    # 16
```

---

## <span class="h2">Ordre des Opérations</span>

Python respecte les priorités mathématiques :

```python
# Multiplication avant addition
print(2 + 3 * 4)    # 14

# Utiliser parenthèses pour modifier
print((2 + 3) * 4)  # 20
```

### Priorités (du plus haut au plus bas)

1. `()` Parentheses
2. `**` Exponentiation
3. `* / // %` Multiplication/Division
4. `+ -` Addition/Soustraction

---

## <span class="h2">Opérateurs de Comparaison</span>

| Opérateur | Description | Exemple | Résultat |
|-----------|-------------|---------|----------|
| `==` | Égal à | `5 == 5` | `True` |
| `!=` | Différent de | `5 != 3` | `True` |
| `>` | Supérieur à | `5 > 3` | `True` |
| `<` | Inférieur à | `5 < 3` | `False` |
| `>=` | Supérieur ou égal | `5 >= 5` | `True` |
| `<=` | Inférieur ou égal | `5 <= 3` | `False` |

### Exemples

```python
a = 10
b = 20

print(a == b)   # False
print(a != b)   # True
print(a > b)    # False
print(a < b)    # True
print(a >= b)   # False
print(a <= b)   # True
```

---

## <span class="h2">Opérateurs Logiques</span>

| Opérateur | Description | Exemple |
|-----------|-------------|---------|
| `and` | ET logique | `True and False` → `False` |
| `or` | OU logique | `True or False` → `True` |
| `not` | NON logique | `not True` → `False` |

### Tables de vérité

```python
# AND
print(True and True)    # True
print(True and False)   # False
print(False and True)   # False
print(False and False)  # False

# OR
print(True or True)     # True
print(True or False)    # True
print(False or True)   # True
print(False or False)   # False

# NOT
print(not True)         # False
print(not False)        # True
```

### Exemple pratique

```python
age = 25
permis = True

# ET
print(age >= 18 and permis)  # True

# OU
print(age < 18 or age > 65)  # False
```

---

## <span class="h2">Opérateurs d'Assignation</span>

| Opérateur | Exemple | Équivalent |
|-----------|---------|------------|
| `=` | `x = 5` | - |
| `+=` | `x += 3` | `x = x + 3` |
| `-=` | `x -= 3` | `x = x - 3` |
| `*=` | `x *= 3` | `x = x * 3` |
| `/=` | `x /= 3` | `x = x / 3` |
| `//=` | `x //= 3` | `x = x // 3` |
| `%=` | `x %= 3` | `x = x % 3` |
| `**=` | `x **= 3` | `x = x ** 3` |

### Exemples

```python
x = 10
x += 5      # x = 15
x -= 3      # x = 12
x *= 2      # x = 24
print(x)    # 24
```

---

## <span class="h2">Opérateurs d'Identité</span>

| Opérateur | Description |
|-----------|-------------|
| `is` | Même objet en mémoire |
| `is not` | Objets différents |

```python
a = [1, 2, 3]
b = [1, 2, 3]
c = a

print(a == b)   # True (même contenu)
print(a is b)   # False (objets différents)
print(a is c)   # True (même objet)
```

---

## <span class="h2">Opérateurs d'Appartenance</span>

| Opérateur | Description |
|-----------|-------------|
| `in` | Dans la séquence |
| `not in` | Pas dans la séquence |

```python
texte = "Bonjour"
print("o" in texte)     # True
print("z" in texte)     # False

nombres = [1, 2, 3]
print(2 in nombres)     # True
print(5 in nombres)     # False
```

---

## <span class="h2">Résumé</span>

| Catégorie     | Opérateurs                          |
|---------------|-------------------------------------|
| Arithmétiques | `+`, `-`, `*`, `/`, `//`, `%`, `**` |
| Comparaison   | `==`, `!=`, `>`, `<`, `>=`, `<=`    |
| Logiques      | `and`, `or`, `not`                  |
| Assignation   | `=`, `+=`, `-=`, `*=`, `/=`         |
| Identité      | `is`, `is not`                      |
| Appartenance  | `in`, `not in`                      |

---

## <span class="h2">Exemples Combinés</span>

### Exemple 1: Validation d'âge

```python
age = 20

est_majeur = age >= 18
a_presque_18 = 17 <= age < 18

print(est_majeur)        # True
print(a_presque_18)      # False
```

### Exemple 2: Parité

```python
nombre = 7

est_pair = nombre % 2 == 0
est_impair = nombre % 2 != 0

print(est_pair)      # False
print(est_impair)    # True
```
