---
icon: material/variable-box
---

# <span class="h1">Variables</span>

 <p class="intro">
    Apprentissage des Variables et des diffèrents types de données en Python.
</p>
---

## <span class="h2">Présentation</span>

<div class="presentation">
    <p style="color: #333; line-height: 1.6;">
        Les variables sont des <strong>étiquettes</strong> , elles sont souvent décrites comme des <strong>boites qui stockent des valeurs</strong>. 
    </p>
    <p style="color: #333; line-height: 1.6;">
        Une variable fait réference à une valeur..
    </p>
</div>

---

## <span class="h2">Chaines de caractères</span>

### Exercices sur les chaines de caractères

[Lien exercices sur les chaine de caractères](exercices/string.md)


---

## <span class="h2">Nombres</span>

En programmation, on utilise souvent des nombres pour mémoriser le score d'un jeu, représenter des données dans de visualisations, stocker des informations dans des applications web, etc.

Python applique **différents traitements aux nombres selon leur utilisation**.
Regardons comment il gére les nombres entiers car se sont les plus facile à utiliser.

- pour lancer python dans le terminal:

```python
$ python3
>>>
```

---

### Nombres entiers

En programmation nous pouvons faire différents calculs:

| Opération | Opérateur | Syntaxe Python | Résultat |
| :--- | :---: | :--- | :--- |
| **Addition** | `+` | `5 + 3` | `8` |
| **Soustraction** | `-` | `10 - 4` | `6` |
| **Multiplication** | `*` | `3 * 7` | `21` |
| **Division** | `/` | `10 / 2` | `5.0` |

??? - note "Exemples"
    ````python
    >>> 2 + 3
    5
    >>> 3 - 2
    1
    >>> 2 * 3
    6
    >>> 3 / 2
    1.5
    ````

Dans une session de terminal, python renvoie **le résultat de l'opération**.
Il utilise 2 symboles de multiplication pour représenter les exposants:

```python
>>> 3 ** 2
9
>>> 3 ** 3
27
>>> 10 ** 6
1000000
```

Python gére également *l'ordre de opérations* et permet d'effectuer **plusieurs opération dans la meme expression**.
On peut utiliser les parenthèses pour modifier l'ordre des opérations et lui demander d'évaluer l'expression dans l'odre souhaité.

```python
# Respecte l'ordre arithmetique de base, multiplication avant addition.
>>> 2 + 3 * 4
14
# Force les prioritées des opérations.
>>> (2 + 3) * 4
20
```

---

### Nombres flottants

Python qualifie de *flottant* tout nombre comportant **un point comme séparateur décimal**.

```python
>>> 0.1 + .1
0.2
>>> .2 + .2
4
>>> 2 * 0.1
0.2
>>> 2.4 * 1.6
3.84
```

!!! note "Note"
    Python peut parfois obtenir un nombre arbitraire de décimales dans la réponse, cela a peu de conséquences.

---

### Nombres entiers et nombres flottants

Lorsqu'on divise 2 nombres (meme si ce sont des nombres entiers) et que le résultat est un nombre entier, **on obtient toujours un nombre flottant**.

```python
>>> 4 / 2
2.0
```

- Si on associe un nombre entier avec un nombre flottant, on obtient également un nombre flottant:

```python
>>> 1 + 2.0
3.0
>>> 2 * 3.0
6.0
>>> 3.0 ** 2
9.0
```

???+ warning "Important"
    Par défaut, Python utilise un nombre flottant dans toute opération qui comprend un nombre flottant, meme si la sortie est nombre entier.

---

### Caractères de soulignement dans les nombres

Dans les nombres long, il est possible de **regrouper des chiffres à l'aide des caractères de soulignement**:

```python
>>> age_univers = 14_000_000
>>> print(age_univers)
14000000
```

> Python ne prend en compte les caractères de soulignement pour stocker les valeurs.

---

### Affectation multiples

On peut affecter des valeurs à plusieurs variables, en utilisant q'une seule ligne.
C'est surtout utiliser pour **initialiser un ensembles de nombres**.

```python
>>> x, y, z = 0, 0, 0
```

Il faut séparer les noms de variables par des virgules, et faire de meme avec les valeurs.
Python *affecte chaque valeur à sa variable*.

---

### Constantes

Une *constante* est une **variable dont la valeur reste inchangé** pendant toute la durée de vie du programme.
Il n'existe pas de constantes native dans python mais la convention est d'écrire **majuscules** les variables à traiter comme telles.

```python
>>> MAX_PLAYER = 20
```

---

### Exercices sur les nombres

[Lien exercices sur les nombres:](exercices/nombres.md) 2-8 à 2-9

---

## <span class="h2">Commentaires</span>

Les commentaires sont extrémement utile dans la majorité des langages de programmation.
Dans les programmes plus long et complexe il est recommendé d'ajouter des notes expliquant la démarche que l'on a suivit.

!!! note "Note"
    Un commentaire permet d'écrire des notes dans un programme sans que cela affecte ce dernier>

---

### Comment écrire des commentaires

Dans Python, le croisillon (#) ***désigne un commentaire***, l'interpréteur Python *ignore tout ce qui suit ce caractère*.

```python
# commentaires.py

# Dire bonjour a tout le monde:
print("Bonjour tout le monde.")
```

Pour un commentaire sur plusieurs lignes:

```python
# commentaires.py

"""
Commmentaire sur plusieurs lignes:
    - pour afficher plus d'informations.
    - Dire bonjour à tout le monde.
"""
print("Bonjour tout le monde.")
```
