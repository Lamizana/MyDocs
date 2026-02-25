<!-- ---
icon: material/gamepad-square
--- -->

# <span class="h1">Strudel</span>

<p class="intro">
    Vous êtes au bon endroit si vous souhaiter apprendre à <strong>créer de la musique avec du code</strong>.
</p>

---

## <span class="h2">Présentation</span>

<div class="presentation">
    <p style="color: #333; line-height: 1.6;">
        <strong>Strudel</strong> permet de composer des morceaux de musiques dynamiques. Il s'agit d'une adaptation officiel du langage de motifs <strong>Tidal Cycles</strong> en Javascript.
    </p>
</div>

[Tidal Cycles](https://tidalcycles.org/)

---

## <span class="h2">Commencer</span>

**Strudel** peux s'utiliser directement à partir du **navigateur** : [Strudel REPL](https://strudel.cc/)

---

## <span class="h2">Logique du Pattern</span>

Contrairement à un logiciel de musique classique où l'on place les notes sur une grille, icic on écrit des **structures**.

La syntaxe ressemble à ceci:

```js
s("bd sd [bd bd] sd")
```

- `s`: Signifie "sound" (le sample à jouer).
- `...`: Tout ce qui est a lintérieur dure un cycle (une **mesure**).
- `[]`: Permet de **subdiviser** le temps, dans l'exemple,  `[bd bd]` joue **deux kicks** dans le même laps de temps qu'un seul  `sd`.

---

## <span class="h2">Atelier</span>

### Premiers sons

Dans ***Strudel REPL*** tapez:

```js
sound("casio")
```

???+ note "Note"
    1. Appuyer sur `ctrl` + `enter` pour lancer le code.
    2. Changer `casio` avec `metal`.
    3. Appuyer sur `ctrl` + `enter` pour mettre à jour.
    4. Appuyer sur `ctrl` + `.` pour arrêter.

Voici d'autres echantillon de sons:

```js
insect wind jazz metal east crow casio space numbers
```

Un sons peut contenir plusieurs échantillons
Pour modifier le numéro d'échantillon:

```js
sound("casio:1")
```

---

## <span class="h2">Tests</span>

Voici différents essais:

```js
s("num:9, bd [<num:8*2 num:8 > oh]")._scope()
```

```js
// Batterie simple Roland :
sound("bd hh sd oh").bank("RolandTR909")
```

```js
note("<[c2 c3]*4 [bb1 bb2]*4 [f2 f3]*4 [eb2 eb3]*4>")
.sound("sawtooth").lpf("<800 2500 4500 8000>")
```

```js
$: note("<[c2 c3]*4 [bb1 bb2]*4 [f2 f3]*4 [eb2 eb3]*4>")
.sound("sawtooth").lpf("<5000>")._scope()

$: sound("sd*4").bank("RolandTR909").lpf(saw.range(1000, 10000).slow(4))._scope()
```

```js
$: note("<[c2 c3]*4 [bb1 bb2]*4 [f2 f3]*4 [eb2 eb3]*4>")
.sound("sawtooth").lpf("1000")._scope()

$: sound("bd rim [bd bd] rim").bank("RolandTR909")._
```

```js
bd= basse d rum​
sd= s nare d rum
rim= coup de cercle
hh= h i h à
oh= o ouvrir h ihat
lt= tom bas
mt= tom du milieu
ht= haut tom
rd= cymbale ride​​
cr= cymbale crash
```

Premier morceau

Voici les notes

```
do (C), ré (D), mi(E), fa (F), sol (G), la (A), si (B).
```


```js
$: note("<[c2 c3]*4 [bb1 bb2]*4 [f2 f3]*4 [eb2 eb3]*4>")
.sound("sawtooth").lpf("1000")._scope()

$: sound("<bd sd [bd bd] sd>*4").bank("bossdr110")._scope()
$: note("- <c2 c3>").sound("gm_synth_brass_2")._scope()
```
