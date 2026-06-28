---
title: Variables
---

# <span class="h1">Variables et Affectation</span>

<p class="intro">
    Apprentissage des Variables et des diffèrents types de données en Python.
</p>

---

## <span class="h2">Introduction</span>

Les variables sont des **conteneurs** qui permettent de stocker des données en mémoire. Elles sont essentielles dans tout programme informatique.

!!! info "Analogie"
    Une variable c'est comme une boîte avec une étiquette. On met une valeur dans la boîte, et on peut la récupérer grâce à l'étiquette.

???+ note "Note"
    Comme d'habitude, si vous n'avez pas ou la flemme de créer un environnement python :

    [Ouvrir avec Basthon](https://basthon.fr/){ target="_blank" .md-button }

---

## <span class="h2">Données et variables</span>

L'essentiel du travail effectue par un programme d'ordimnateur consisite à manipuler des **donnees**. Ces données 
peuvent etre diverses, mais dans la mémoire de l'ordinateur, elles se ramènent toujours en definitive à **une suite 
finie de nombres binaires**.

Pour pouvoir y accéder, le programme fait usage de **variables** de differents types.

!!! warning "Important"
    - Une variable apparait dans la majorité des langages de programmations sous un **nom de variable** quelconque, mais pour l'ordinateur, **il s'agit d'une _référence_ designant une adresse mémoire**, c'est-à-dire un emplacement précis dans la mémoire vive.
    - A cet emplacement est stocké une **valeur** bien déterminée, c'est la donnée qui est stocké sous la forme 
    d'_une suite de nombres binaires_.

---

## <span class="h2">Convention de nommage</span>

| Règle                   | Correct           | Incorrect         |
|-------------------------|-------------------|-------------------|
| Minuscules              | `mon_nom`         | `monNom`          |
| Pas d'espace            | `age_utilisateur` | `age utilisateur` |
| Pas de chiffre au début | `age1`            | `1age`            |
| Pas de mot réservé      | `print_`          | `print`           |

!!! tip "Bonnes pratiques"
    Utilisez le **snake_case** : `mon_nom_de_variable`

---

## <span class="h2">Affectation (ou assignation) d'une variable</span>

Nous allons voir à présent comment **définir** une variable et lui **affecter** une valeur.

> Les termes "affecter une valeur" ou "assigner une valeur" à une variable sont équivalents. Ils désignent 
l'opération par laquelle on établit un lien entre le nom de la variable et sa valeur.

- En python comme dans beaucoup d'autres lngages de programmation, l'opération d'affectation est representé par le 
  signe égal (`=`)

``` py
>>> nom = "Alex"    # affecter la valeur "Alex" à nom
>>> age = 25        # définir la variable "age" et lui donner la valeur 25
>>> taille = 1.75   # assigner sa valeur à la variable "taille"
```
Les exemples ci desssus montrent des _instructions d'affectation_ Python. Apres qu'on les ait exécutées, ils existent 
dans la mémoire de l'ordinateur, à des endroits différents :

- 3 noms de variables : `nom`, `age` et `taille`.
- 3 séquences d'octets où sont encodées les valeurs des variables.

???+ note "A savoir"
    - Ces 3 instuctions ont pour effet de réaliser plusieurs actions dans la mémoire de l'ordinateur :

          - Créer et mémoriser un **nom de variable**.
          - Attribuer un **type** bien déterminé.
          - Créer et mémoriser une **valeur** particulière.
          - Etablir un lien (par un système de **pointeur**) entre le nom de la variable et l'emplacement mémoire de la 
          valeur correspondante.

    !!! info
        Les trois noms de variables sont des _références_.

---

## <span class="h2">Typage des variables</span>

En Python, il n'est pas nécessaire de préciser le type de variables avant de pouvoir les utiliser. Il suffit 
d'assigner une valeur à un nom de variable avant de pouvoir l'utiliser:

- On dit alors que celle-ci est _automatiquement créé avec le type qui correspond au mieux à la valeur fournit_.

De plus on dira que le _typage des variables sous Python est dynamique_, par opposition au _typage statique_ qui est de 
mise en `C` ou `C++`.

???+ note "A savoir"
    === "Typage dynamique"
        - Le typage statique est preférable dans les langages compilés tels que le `C`. Il permet _l'opération de 
        compilation_.

    === "Typage statique"
        - Le typage dynamique pernet d'écrire plus aisément des constructions logique de niveaux elevé, en particulier 
        dans le contexte de la programmation orienté objet.

---

## <span class="h2">Affectation Multiple</span>

Python nous permet d'assigner une valeur à plusieurs variables simultanément :
``` py
>>> x = y = 7
>>> x
7
>>> y
7
```

On peut aussi faire des affectations paralléles ;
``` py
>>> a, b = 4, 1.33
>>> a
4
>>> b
1.33
```

> Dans cette exmple, les variables `a` et `b` prennent respectivement les valeurs `4` et `1.33`

---

## <span class="h2">Operateurs et expressions</span>

On manipule les valeurs et les variables qui les référence en les combinant avec des **opérateurs** pour former des 
**expressions** :

``` python
>>> a, b = 7.3, 12
>>> y = 3 * a + b / 5
>>> y
24.299999999999997
```

1. Ici, nous commençons à affecter aux variables `a` et `b` deux valeurs distinctes, `7.3` et `12`.
2. La seconde ligne consiste à affecter à une nouvelle variable `y` le résultat d'une **expression** qui combine les 
   **opérateurs** `*`,`+` et `/` avec les opérandes `a`, `b`, `3` et `5`.

<div class="soft-skills-grid">
    <div class="soft-skill-card">
        <span class="soft-skill-title">Opérateurs</span><br><br>
        <span class="soft-skill-desc">Symboles spéciaux utilisés pour representer les opérations mathématiques.</span>
    </div>
    
    <div class="soft-skill-card">
        <span class="soft-skill-title">Opérandes</span><br><br>
        <span class="soft-skill-desc">Ce sont les valeurs combinées à l'aide des opérateurs</span>
    </div>
</div>

### 1. Liste des opérateurs logique

| Opérateur | Description      | Exemple   | Résultat |
|-----------|------------------|-----------|----------|
| `+`       | Addition         | `5 + 3`   | `8`      |
| `-`       | Soustraction     | `10 - 4`  | `6`      |
| `*`       | Multiplication   | `3 * 7`   | `21`     |
| `/`       | Division         | `15 / 4`  | `3.75`   |
| `//`      | Division entière | `15 // 4` | `3`      |
| `%`       | Modulo (reste)   | `15 % 4`  | `3`      |
| `**`      | Exponentiation   | `2 ** 3`  | `8`      |

### 2. Priorité des opérations

Lorsqu'il y a plus d'un opérateur dans une expression, l'ordre dans les opérations doivent s'effectuer suit un shéma 
précis, on appelle ça les **régles de priorités**. En Python, elles sont les mêmes qui sont appliquées en 
mathématique.

!!! abstract "À connaitre"
    Pour les mémoriser à l'aide d'un moyen mnémotechnique, l'acronyme **`PEMDAS`**:

    - ***`P` pour parenthése***. Ce sont elles qui ont la plus haute priorité. Elles permettent de "forcer" 
    l'évaluation d'une expression dans l'ordre souhaité.
        - Ainsi: `2 * (3 - 1) = 4`, et `(1 + 1) ** (5 - 2) = 8`
    - **_`E` pour exposants_**. Ils sont evalué ensuite, avant les autres opérations.
        - Ainsi: `2 ** 1 + 1 = 3` (et non 4), et `3 * 1 ** 10 = 3` (et non 59049).
    - **`M` et `D` pour _multiplication_ et _division_**. Elles ont la même priorité. Elles sont evaluées avant 
    _addition `A`_ et la _soustraction `S`_, ces dernière étant effectuées en dernier lieu.
        - Ainsi: `2 * 3 - 1 = 5` (et non 4), et `2 / 3 - 1 =  -0.33333...` (et non 1.0).
    - Si deux opérateurs ont la même priorité, l'évaluation est effectuée de gauche à droite.
        - Ainsi dans: `59 * 100 // 60`, la multiplication se fait en première, suivi de la division.

---

## <span class="h2">Composition</span>

Une des grandes forces d'un langage de programmation de haut niveau est qu'il permet de construire des instructions 
complexes par assemblage de plusieurs instructions. Par exemple, on sait comment additionner deux nombres et comment 
afficher une valeur, on peut donc combiner ses instructions en une seule :

``` python
>>> print(3 + 5)
8
```

Cette fonctionnalité va permettre de programmer des algorithmes complexes de facon claire et concise :

``` python
>>> h, m, s = 15, 27, 34
>>> print("nombre de secondes ecoule depuis minuit = ", h * 3600 + m * 60 + s)
nombre de secondes ecoule depuis minuit 55654
```

!!! warning "Attention"
    Il y a une limite à ce que l'on peut combiner :
    Dans une expression, ce qui est placé à gauche du signe égal et toujours une variable, et non une expression.
    
    - En programmation le signe égal (`=`) est un **symbole d'affectation et non un symbole d'égalité**.
        - Exemple: l'instruction `m + 1 = b` est fausse.
    - Par contre, écrire `a = a + 1` est très fréquent en programmation. Cela signifie "_augmenter la valeur `a` de 
    1_" ou encore **"incrémenter `a`"**.

---

## <span class="h2">Constantes</span>

Une **constante** est une variable dont la valeur ne doit pas changer. Python n'a pas de vraies constantes, mais par convention :

``` python
>>> MAX_SCORE = 100
>>> TAUX_TVA = 0.20
>>> PI = 3.14159
```

!!! warning "Important"
    Par convention, les constantes s'écrivent en **MAJUSCULES**.

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
