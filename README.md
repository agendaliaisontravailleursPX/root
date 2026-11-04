# Agenda commun — guide de mise en place

Ce dossier contient tout le nécessaire :

| Fichier | À quoi il sert |
|---|---|
| `index.html` | La page vitrine, aux couleurs du mouvement, qui affiche l'agenda |
| `affiche.html` | L'affiche A4 avec QR code, à imprimer |
| `TEXTES.md` | La motion à faire voter, le formulaire, le récapitulatif WhatsApp et la notice des administrateurs |

Durée totale : environ 1 h 30, réparties sur quelques jours.

---

## Étape 1 — Créer l'agenda sur Framagenda (20 min)

1. Créez un compte sur framagenda.org **avec une adresse dédiée au collectif**, jamais votre adresse personnelle. Mot de passe long et unique.
2. Dans le menu de gauche, « + Nouvel agenda ». Nommez-le **Agenda commun AGAN**.
   - Option : créez plusieurs agendas avec une couleur chacun (AG, tractages, manifestations, actions avec les travailleurs).
3. Cliquez sur les trois points à côté de l'agenda, puis sur « Partager » :
   - **Lien public** : cliquez sur « + » à côté de « Lien de partage ». Copiez-le.
   - **Lien d'abonnement** : dans le même menu, « Copier le lien d'abonnement ».
   - **Code d'intégration** : « Copier le code d'intégration ». Dans ce code, gardez uniquement l'adresse entre les guillemets de `src="…"`.
4. Gardez ces trois liens dans une note : vous en aurez besoin à l'étape 2.

> Les intitulés exacts peuvent légèrement varier selon la version de Framagenda.

## Étape 2 — Créer le formulaire (15 min)

1. Créez un formulaire sur un service libre (Yakforms chez un hébergeur du collectif CHATONS, ou Framaforms s'il est disponible). À défaut, Google Forms fonctionne aussi.
2. Recopiez les questions données dans `TEXTES.md`, partie 2.
3. Copiez le lien public du formulaire.

## Étape 3 — Remplir les réglages de la page (5 min)

Ouvrez `index.html` avec un éditeur de texte (Bloc-notes, TextEdit en mode texte, ou directement dans GitHub). En haut du fichier, remplissez les quatre lignes :

```js
integration: "https://framagenda.org/…/embed/…",   // adresse du code d'intégration
lienPublic:  "https://framagenda.org/…",           // lien public
abonnement:  "webcal://framagenda.org/…",          // lien d'abonnement
formulaire:  "https://…"                           // lien du formulaire
```

Ne touchez à rien d'autre. Tant qu'une ligne est vide, le bouton correspondant est grisé : la page reste utilisable.

## Étape 4 — Mettre la page en ligne sur GitHub Pages (20 min)

1. Créez un compte GitHub **avec un pseudonyme**, lié à l'adresse du collectif.
2. « New repository ». Nom : `agenda-commun`. Laissez-le **Public** (obligatoire pour GitHub Pages gratuit).
3. « Add file », puis « Upload files ». Déposez `index.html`, `affiche.html` et ce `README.md`. Validez avec « Commit changes ».
4. Allez dans « Settings », puis « Pages ». Dans « Branch », choisissez `main` et `/ (root)`, puis « Save ».
5. Après une ou deux minutes, l'adresse de la page s'affiche, du type `https://votre-pseudo.github.io/agenda-commun/`.

Le dépôt est public, mais il ne contient **aucune donnée** : les actions restent dans Framagenda, et les propositions dans le formulaire.

## Étape 5 — Imprimer l'affiche (10 min)

1. Ouvrez `affiche.html` dans un éditeur de texte et remplacez l'adresse en haut (`ADRESSE_PAGE`) par celle obtenue à l'étape 4.
2. Ouvrez le fichier dans un navigateur, puis « Imprimer ». Choisissez A4, marges « Aucune », et cochez « Graphiques d'arrière-plan ».
3. Testez le QR code avec votre téléphone avant d'imprimer en nombre.

## Étape 6 — Faire voter l'agenda en AG

Présentez la motion de `TEXTES.md`, partie 1. Elle crée l'agenda commun, fixe la règle d'inscription et mandate les administrateurs.

## Étape 7 — Faire tourner

- Partagez l'agenda Framagenda **en modification** avec les comptes des administrateurs mandatés (menu « Partager », ajout d'utilisateur).
- Suivez la notice des administrateurs (`TEXTES.md`, partie 4).
- Chaque dimanche : envoyez le récapitulatif WhatsApp (`TEXTES.md`, partie 3) et exportez l'agenda en `.ics` (trois points, « Exporter ») comme copie de secours.

## Modifier la page plus tard

Dans GitHub, ouvrez `index.html`, cliquez sur le crayon, modifiez, puis « Commit changes ». La page se met à jour en une ou deux minutes.
