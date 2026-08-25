# MyDocs

Site documentaire sur la programmation - Propulsé par ProperDocs et Material theme.

---

## Stack Technique

- **Site**: ProperDocs + Material for MkDocs
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

# Rajouter des dépendances dans le fichier requirements.txt
pip freeze > requirements.txt
```

---

## Commandes

| Commande              | Description                   |
|-----------------------|-------------------------------|
| `properdocs serve`    | Serveur local avec hot-reload |
| `properdocs build`    | Générer le site statique      |
| `properdocs gh-deploy`| Déployer sur GitHub Pages     |

```bash
# Serveur local
properdocs serve --dev-addr=127.0.0.1:8001
properdocs serve --dev-addr=127.0.0.1:8001 --livereload

# Déploiement
properdocs gh-deploy
```

---

## À Propos

Développé par **Alex Lamizana** - Étudiant 42 Angoulême, spécialisation Data & IA.

- [Voir le site](https://lamizana.github.io/MyDocs/)
- [Mon profil GitHub](https://github.com/Lamizana)
