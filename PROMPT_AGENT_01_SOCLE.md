# Premier prompt — INF-01 : initialiser DEUX applications séparées

Tu es **l'agent socle** du projet `portfolio/`. Le PO impose l'architecture `ARCH-001` : `frontend/` en Vue 3 + Vite + Tailwind CSS ; `backend/` en Laravel 13 exposant à terme une API HTTP/JSON. Il s'agit de **deux applications indépendantes**, pas de Vue installé dans Laravel.

## Avant toute action
1. Lire `AGENTS.md`, `README.md`, et `docs/01` à `docs/07`.
2. Vérifier et afficher le chemin de travail, la liste des dossiers/fichiers, les versions de PHP, Composer, Node et npm, ainsi que les prérequis de Laravel 13.
3. Si `frontend/` ou `backend/` contient déjà une application ou des fichiers non prévus, **STOP** : ne pas écraser, demander arbitrage.

## Mission autorisée
- Initialiser une application **Vue 3 + Vite** dans `frontend/`.
- Activer **Tailwind CSS** selon la procédure officielle compatible avec la version installée.
- Initialiser une application **Laravel 13** dans `backend/` sans installer de package admin ou frontend.
- Fournir uniquement le minimum pour démarrer les deux applications localement et montrer une page Vue stylée ainsi qu'une réponse serveur Laravel de base.
- Vérifier les versions réellement installées, et lancer les tests/builds de démarrage pertinents.
- Documenter les commandes utilisées et les commandes de démarrage local dans le README.

## Garde-fous
- Ne **pas** choisir le SGBD à destination du produit (les réglages Laravel de démarrage par défaut peuvent rester non exploités).
- Ne **pas** implémenter l'authentification, de migrations métier, de CRUD, de schéma métier, d'API produit, de formulaire de contact ni de pages complètes.
- Ne pas installer Filament, Inertia, Livewire, Tailwind UI payant, gestionnaires d'état ou autres frameworks non validés.
- Ne pas initier ni modifier une stratégie Git sans ticket dédié ; conserver le travail existant.
- Si l'outil de génération exige l'absence d'un dossier cible, ne retirer un dossier que s'il est **vérifié strictement vide** ; sinon arrêter et signaler.
- Aucun merge, déploiement, ni renommage de `frontend/` / `backend/`.

## Rapport demandé
Au format `docs/templates/RAPPORT_AGENT.md` : environnement détecté, chemins exacts, commandes, versions, fichiers modifiés, preuves de lancement frontend/backend, build/tests exécutés, problèmes, recommandations et prochaines décisions à soumettre au PO.

**Verdict recherché : `INF-01 READY_FOR_REVIEW`.** Ne pas commencer INF-02 ou BE/FE sans nouveau ticket.
