# MyDocs

---

## Installation

Créer un dossier .env pour y télécharger les librairies :

```bash
python3 -m venv .env
```

Pour activer l'environement virtuel :

```bash
source .env/bin/activate 
```

Une fois l'environnemt activé il ne reste plus qu'à y installer les dépendances :

```bash
pip install --upgrade pip           # met à jour pip
pip install -r requirements.txt
```

---

## Commandes

* `mkdocs new [nom-dossier]` - Créez un nouveau projet.
* `mkdocs serve` - Démarrez le serveur de documentation avec rechargement en direct.
* `mkdocs build` - Générez le site de documentation.
* `mkdocs -h` - Affichez le message d'aide et quittez.

```bash
> mkdocs serve --dev-addr=127.0.0.1:8001    # Lance le serveur.
> mkdocs build                              # Génére le site de documentation.
```

Si mkdocs n'est pas disponible alors il faut passer par python :

```bash
python -m pip install mkdocs        # installe la commande
python -m mkdocs                    # préface de chaque commande mkdocs
```

Pour faire en sorte que le serveur se mette automatiquement à jour lors d'un changement, lancer le serveur avec la commande :

```bash
python -m mkdocs serve --livereload
```
