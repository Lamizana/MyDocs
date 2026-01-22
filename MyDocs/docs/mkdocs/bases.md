# <span class="h1">MkDocs</span>

<p align="center"><em>MkDocs est un générateur de sites statiques <strong>rapide</strong>, <strong>simple</strong> et <strong>élégant</strong>,conçu pour la création de documentation de projet. Les fichiers sources de documentation sont écrits en Markdown et configurés à l'aide d'un unique fichier <strong>YAML</strong>.</em></p>

---

## <span class="h2">Caractéristiques</span>

* De superbes thèmes disponibles.
* Facile à personaliser.
* Previsualiser votre site pendant que vous travaillez.
* Hébergé n'importe ou.

---

## <span class="h2">Installation</span>

Pour installer **Mkdocs**, exécuter la commande suivante depuis la ligne de commande :

```bash
> pip install mkdocs
```

Si mkdocs n'est pas disponible alors il faut passer par python :

```bash
> python -m pip install mkdocs        # installe la commande
> python -m mkdocs                    # préface de chaque commande mkdocs
```

Pour vérifier la version :

```bash
> python -m mkdocs --version
```

---

## <span class="h2">Création d'un nouveau projet</span>

Pour créer un nouveau projet, exécuter la commande suivante :

```bash
> mkdocs new my-project
```

Mkdocs intègre un serveur de développement qui permet de prévisualiser votre documentation pendant que vous travaillez dessus.
Pour ce faire, assurez-vous d'étre dans le meme repertoire que le fichier ***mkdocs.yml*** (*qui est le fichier de configuration*).

```bash
> python -m mkdocs serve
> mkdocs serve
INFO    -  Building documentation...
INFO    -  Cleaning site directory
INFO    -  Documentation built in 0.22 seconds
INFO    -  [15:50:43] Watching paths for changes: 'docs', 'mkdocs.yml'
INFO    -  [15:50:43] Serving on http://127.0.0.1:8000/
```

Pour le chargement automatique :

```bash
python -m mkdocs serve --livereload
```

---

## <span class="h2">Commandes</span>

* `mkdocs new [nom-dossier]` - Créez un nouveau projet.
* `mkdocs serve` - Démarrez le serveur de documentation avec rechargement en direct.
* `mkdocs build` - Générez le site de documentation.
* `mkdocs -h` - Affichez le message d'aide et quittez.

```bash
> mkdocs serve --dev-addr=127.0.0.1:8001    # Lance le serveur.
> mkdocs build                              # Génére le site de documentation.
```
