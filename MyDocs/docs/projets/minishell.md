---
title: Minishell
---

# <span class="h1">Minishell</span>

## Description

Projet 42 visant à créer un **interpréteur de commandes** (shell) similaire à bash. Ce projet est une excellente introduction aux systèmes UNIX.

---

## Compétences Acquises

- **Programmation système** UNIX
- **Gestion des processus** (fork, exec, wait)
- **Parsing** et analyse syntaxique
- **Signaux** (SIGINT, SIGQUIT, etc.)
- **Redirections** et pipes

---

## Stack Technique

- **Langage**: C
- **Système**: Linux/UNIX
- **Outils**: Makefile, GCC

---

## Défis Relevés

1. **Boucle interactive** : Implémentation du read-eval-print loop (REPL)
2. **Gestion des signaux** : Comportement comme bash (Ctrl+C, Ctrl+\)
3. **Parsing complexe** : Gestion des quotes, redirections, pipes
4. **Builtins** : Implémentation de cd, echo, env, export, unset, etc.

---

## Fonctionnalités

- Commandes内置 (cd, echo, pwd, export, unset, env, exit)
- Redirections (`>`, `>>`, `<`)
- Pipes (`|`)
- Variables d'environnement
- Gestion des erreurs

---

## Lien

[:fontawesome-brands-github: Voir le code](https://github.com/Lamizana/Minishell){ .md-button .md-button--primary }
