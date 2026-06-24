---
title: Flux d'exécution
---

# <span class="h1">Contrôle du flux d'exécution</span>

<p class="intro">
     Nous allons ici définir ce qu'est un contrôle de flux et de quoi il en retourne...
</p>

---

## <span class="h2">Introduction</span>

L'activité essentiel d'un programmeur est la résolution de problèmes. Or pour résoudre un probléme informatique, il faut toujours effectuer une série d'actions dans un certain ordre. _La description structuré de ces actions et de l'ordre dans lequel il convient de les effectuer s'appellent un **algorithme**_.


Le "_chemin_" suivie par Python est appelé un **flux d'exécution**, et les constructions qui le modifient sont appelé des **instructions de contrôle de flux**.

Les structures de contrôles sont les groupes d'instructions qui définissent l'ordre dans lequel les actions sont effectuées.En programmation moderne il en existe seulement 3 :

- La séquence.
- La sélection.
- La répétition.

Nous allons aborder dans ce chapitre la **séquence** et la **sélection**.

???+ note "Note"
    Comme d'habitude, si vous n'avez pas ou la flemme de créer un environnement python :

    [Ouvrir avec Basthon](https://basthon.fr/){ target="_blank" .md-button }

---

## <span class="h2">Séquence d'instructions</span>

En régle générales, les instructions d'un programme s'effectue les unes après les autres, _dans l'ordre dans elles ont été écrite dans le script_.

???+ warning "Attention"
    Une mauvaise disposition des instructions peut créer des erreurs sémantiques dans les programmes informatiques. 

Il faut donc être extrémement attentif à l'ordre des instructions dans vos programmes. Prenons la séquence d'instructions suivantes:

```py
>>> a, b = 5, 2
>>> a = b           # 2
>>> b = a           # 2
>>> print(a, b)
2 2 
```

On obtient un résultat inverse si l'on intervertit la deuxième et troisième lignes.

```py
>>> a, b = 5, 2
>>> b = a           # 5
>>> a = b           # 5
>>> print(a, b)
5 5 
```

Python exécute normalement les instrcutions dans l'ordre, sauf s'il rencontre une ***instruction conditionnelle*** (ex: l'instruction `if`). Une telle instruction va permettre au programmede suivre différent chemin suivant les circonstances.

---

## <span class="h2">Sélection ou exécution conditionnelle</span>

Pour pouvoir écrire des applications utiles, il nous faut pouvoir aiguiller notre programme dans différentes directions en fonction de la requete ou circonstance donnée.

Nous devons donc disposer d'instruction capable de tester une certaine condition, vérifier si elle est vrai ou non et de modifier le comportement du programme en conséquence.

L'instruction conditionnelle la plus commune est l'instruction _if_. Allez dans l'éditeur Python et tapez les deux lignes suivantes:

````python
>>> a = 50
>>> if (a > 30):
... 
````

Décryptons ligne par ligne :

1. on affecte la valeur `50` à la variable `a`.
2. instruction conditionnelle `if` (terminé par `:`).
3. le **prompt principal** (`>>>`)est maintenant remplacé par un **prompt secondaire** (`...`).

Nous allons maintenant rajouter une ligne dans notre condition :

```python
>>> a = 50
>>> if (a > 30):
...     print("a depasse les trentes")
```

Appuyer sur `Entré`. Le programme s'execute et vous obtenez :

```python
a depasse les trentes
```

Si vous recommencez en changeant la valeur de la variable `a` à `20`, le code suivant n'affichera plus rien.


TODO: test de TODO