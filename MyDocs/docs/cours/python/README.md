# Variables et types de données simples

## [Index](/README.md)

## Sommaire

1. [Variables.](#variables)
2. [Chaines de caractères.](#chaines-de-caractères)
3. [Nombres.](#nombres)
    - [Nombres entiers.](#nombres-entiers)
    - [Nombres flottants.](#nombres-flottants)
    - [Nombres entiers et nombres flottants.](#nombres-entiers-et-nombres-flottants)
    - [Caractères de soulignement dans les nombres.](#caractères-de-soulignement-dans-les-nombres)
    - [Affectation multiples.](#affectation-multiples)
    - [Constantes.](#constantes)
    - [Exercices sur les nombres.](#exercices-sur-les-nombres)
4. [Commentaires.](#commentaires)
    - [Exercices commentaires.](#exercices-commentaires)

----------------------------------------------------------------------------

## Variables

[Sommaire.](#sommaire)

Les variables sont des *étiquettes*, elles sont souvent décrites comme des **boites qui stockent des valeurs**.
> Une variable fait réference à une valeur.

----------------------------------------------------------------------------

## Chaines de caractères

[Sommaire.](#sommaire)

A faire...

[Lien exercices sur les chaine de caractères:](/base/variables/casse_nom.py): exos 2-3 à 2-7.

```bash
file: cours/base/variables/casse_nom.py
```

----------------------------------------------------------------------------

## Nombres

[Sommaire](#sommaire)

En programmation, on utilise souvent des nombres pour mémoriser le score d'un jeu, représenter des données dans de visualisations, stocker des informations dans des applications web, etc.
Python applique **différents traitements aux nombres selon leur utilisation**.
Regardons comment il gére les nombres entiers car se sont les plus facile à utiliser.

- pour lancer le terminal python:

```bash
$ python3
>>>
```

----------------------------------------------------------------------------

### Nombres entiers

- On peut additionner(+), soustraire(-), multiplier(*) et diviser(/) des nombres entiers dans python:

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

----------------------------------------------------------------------------

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

> [!NOTE]
> Python peut parfois obtenir un nombre arbitraire de décimales dans la réponse, cela a peu de conséquences.

----------------------------------------------------------------------------

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

> [!IMPORTANT]
> Par défaut, Python utilise un nombre flottant dans toute opération qui comprend un nombre flottant, meme si la sortie est nombre entier.

----------------------------------------------------------------------------

### Caractères de soulignement dans les nombres

Dans les nombres long, il est possible de **regrouper des chiffres à l'aide des caractères de soulignement**:

```python
>>> age_univers = 14_000_000
>>> print(age_univers)
14000000
```

> Python ne prend en compte les caractères de soulignement pour stocker les valeurs.

----------------------------------------------------------------------------

### Affectation multiples

On peut affecter des valeurs à plusieurs variables, en utilisant q'une seule ligne.
C'est surtout utiliser pour **initialiser un ensembles de nombres**.

```python
>>> x, y, z = 0, 0, 0
```

Il faut séparer les noms de variables par des virgules, et faire de meme avec les valeurs.
Python *affecte chaque valeur à sa variable*.

----------------------------------------------------------------------------

### Constantes

Une *constante* est une **variable dont la valeur reste inchangé** pendant toute la durée de vie du programme.
Il n'existe pas de constantes native dans python mais la convention est d'écrire **majuscules** les variables à traiter comme telles.

```python
>>> MAX_PLAYER = 20
```

----------------------------------------------------------------------------

### Exercices sur les nombres

[Lien exercices sur les nombres:](/base/variables/nombres.py) 2-8 à 2-9

----------------------------------------------------------------------------

## Commentaires

[Sommaire](#sommaire)

Les commentaires sont extrémement utile dans la majorité des langages de programmation.
Dans les programmes plus long et complexe il est recommendé d'ajouter des notes expliquant
la démarche que l'on a suivit.

> Un commentaire permet d'écrire des notes dans un programme.

----------------------------------------------------------------------------

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

### Quel type de commentaires écrire?

### Exercices commentaires

[Lien exercices sur les commentaires:](/base/variables/commentaires.py) 2-10
