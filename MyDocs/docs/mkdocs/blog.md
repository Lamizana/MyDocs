---
title: Mise en place d'un Blog
description: "Ajouter un blog à un site MkDocs avec le plugin Blog de Material for MkDocs et le flux RSS."
icon: fontawesome/solid/blog
---

# <span class="h1">Mise en place d'un Blog</span>

<p align="center"><em>Ajouter un blog à votre site MkDocs avec le plugin Blog de Material for MkDocs.</em></p>

---

## <span class="h2">Plugin Blog</span>

Le plugin **Blog** de Material for MkDocs permet d'ajouter un blog directement dans le site de documentation.

Il faut :
- placer les articles dans `docs/blog/posts/` ;
- définir le fichier des auteurs dans `{blog}/.authors.yml` ;
- chaque article possède un frontmatter `title`, `date` et `authors`.

!!! info "Exemple de frontmatter"
    ```yaml
    ---
    title: Mon premier article
    date: 2026-01-01
    authors:
      - zehd
    categories:
      - 🧪 Science
    ---
    ```

## <span class="h2">Plugin RSS</span>

Dans MkDocs, le plugin RSS sert à générer automatiquement un flux RSS à partir de ton site de documentation.