# docs

Dépôt utilitaire pour publier rapidement des pages publiques (politiques de
confidentialité, mentions légales, CGU...) pour n'importe lequel de mes
projets, via GitHub Pages. Basé sur [Astro](https://astro.build) pour un
rendu propre, rapide et moderne — build et déploiement automatiques via
GitHub Actions à chaque push sur `main`.

**Volontairement pas d'index listant tous les projets** : chaque page est
autonome, sans navigation vers les autres. Un lien direct est nécessaire
pour l'atteindre.

## Convention

Un dossier par projet dans `src/pages/`, une page Markdown par page finale,
avec le layout partagé (`src/layouts/Legal.astro`) déjà stylé :

```markdown
---
layout: ../../layouts/Legal.astro
title: Politique de confidentialité — Nom du projet
project: Nom du projet
updated: 16 septembre 2026
description: Courte description pour le <meta>.
---

## Un titre de section

Contenu en Markdown normal...
```

Placé dans `src/pages/nom-du-projet/privacy.md`, ça donne
`https://novenopatch.github.io/docs/nom-du-projet/privacy/`.

## Développement local

```bash
npm install
npm run dev
```

## Déploiement

Automatique : push sur `main`, le workflow `.github/workflows/deploy.yml`
build avec Astro et déploie sur GitHub Pages (source réglée sur "GitHub
Actions" dans les réglages du dépôt, pas sur une branche).

## Pages en ligne

- [Deliv](https://novenopatch.github.io/docs/deliv/)
- [Deliv — politique de confidentialité](https://novenopatch.github.io/docs/deliv/privacy/)
- [HotelPilot Suite](https://novenopatch.github.io/docs/hotelpilot/)
- [HotelPilot Suite — politique de confidentialité](https://novenopatch.github.io/docs/hotelpilot/privacy/)
