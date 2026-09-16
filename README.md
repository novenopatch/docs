# docs

Dépôt utilitaire pour publier rapidement des pages publiques (politiques de
confidentialité, mentions légales, CGU...) pour n'importe lequel de mes
projets, via GitHub Pages. Zéro build à maintenir : pousser un `.md`, GitHub
Pages (Jekyll intégré) le transforme en page HTML.

Site en ligne : **https://novenopatch.github.io/docs/**

## Convention

Un dossier par projet, un fichier Markdown par page. Chaque fichier a un
en-tête (front matter) avec au minimum un `title` et un `permalink` fixe
(sinon Jekyll génère une URL basée sur le nom de fichier, moins stable) :

```markdown
---
title: Politique de confidentialité — Nom du projet
permalink: /nom-du-projet/privacy/
---

Contenu de la page en Markdown normal...
```

Résultat en ligne : `https://novenopatch.github.io/docs/nom-du-projet/privacy/`

## Ajouter une page pour un nouveau projet

1. Créer (ou réutiliser) le dossier `nom-du-projet/` à la racine.
2. Ajouter le fichier Markdown avec son front matter (`title` + `permalink`).
3. Commit + push sur `main` — GitHub Pages rebuild automatiquement
   (généralement moins de 2 minutes), rien d'autre à faire.

## Projets déjà présents

- [`deliv/`](deliv/) — politique de confidentialité de l'app Deliv.
