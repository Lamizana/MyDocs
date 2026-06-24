# MyDocs

Site documentaire sur la programmation - Propulsé par MkDocs et Material theme.

---

## Stack Technique

- **Site**: MkDocs + Material for MkDocs
- **Hébergement**: GitHub Pages
- **Cours**: Python, JavaScript, React, Git, Data/IA

---

## Contenu

### Projets

- **Transcendence** - Application web Pong multiplayer
- **Minishell** - Interpréteur de commandes
- **ft_irc** - Serveur IRC en C++
- **Push Swap** - Algorithme de tri optimisé
- **So Long** - Jeu 2D en C

### Cours

- Python (bases, pandas, numpy, scikit-learn)
- JavaScript, React, Redux
- Git & GitHub
- MkDocs

---

## Installation locale

```bash
# Créer un environnement virtuel
python3 -m venv .env

# Activer l'environnement
source .env/bin/activate

# Installer les dépendances
pip install --upgrade pip
pip install -r requirements.txt

# Rajouter des depandances dans le fichier requirements.txt
pip freeze > requirements .txt
```

---

## Commandes

| Commande           | Description                   |
|--------------------|-------------------------------|
| `mkdocs serve`     | Serveur local avec hot-reload |
| `mkdocs build`     | Générer le site statique      |
| `mkdocs gh-deploy` | Déployer sur GitHub Pages     |

```bash
# Serveur local
mkdocs serve --dev-addr=127.0.0.1:8001
mkdocs serve --dev-addr=127.0.0.1:8001 --livereload

# Si les commandes ne fonctionne pas, essayer :
python3 -m mkdocs serve --dev-addr=127.0.0.1:8001
python3 -m mkdocs serve --dev-addr=127.0.0.1:8001 --livereload

# Déploiement
mkdocs gh-deploy
```

---

## À Propos

Développé par **Alex Lamizana** - Étudiant 42 Angoulême, spécialisation Data & IA.

- [Voir le site](https://lamizana.github.io/MyDocs/)
- [Mon profil GitHub](https://github.com/Lamizana)
