# 05 — Protocole de collaboration des agents

## Acteurs
- **Product Owner :** tranche les besoins, priorités, changements et validations.
- **Copilote :** organise tickets, dépendances, décisions, intégrations et comptes rendus.
- **Agent Socle :** bootstrap et démarrage des deux applications.
- **Agent Backend :** travaille dans `backend/` pour Laravel API et tests.
- **Agent Frontend :** travaille dans `frontend/` pour Vue, Tailwind et tests.
- **Reviewer :** relit les diff et tests, sans réécrire silencieusement les fonctionnalités.

## Frontières de fichiers
- Backend : `backend/**` ; n'écrit ni dans frontend ni dans contrats sans accord.
- Frontend : `frontend/**` ; n'écrit ni dans backend ni dans contrats sans accord.
- Contrats : `docs/07_CONTRAT_API.md` modifiable seulement sur ticket PO/architecture/coordination.
- Documentation/CI partagée : modifications coordonnées, pas de changements opportunistes par un agent de fonctionnalité.
- Le choix d'un ou plusieurs dépôts Git reste séparé de l'architecture de dossiers. Worktrees à définir après initialisation et dépôt existant ; ne pas les improviser au bootstrap.

## Attribution et rendu
Utiliser `docs/templates/TICKET.md`. Chaque agent déclare son périmètre, ses prérequis et ses chemins avant code, puis termine par `docs/templates/RAPPORT_AGENT.md` avec fichiers changés, tests réellement effectués et risques.

## Garde-fous
- Pas d'invention de règles de gestion.
- Pas de nouveaux composants d'infrastructure, frameworks ni bibliothèques sans validation.
- Pas de modification croisée du contrat API non approuvé.
- Pas de fusion sans revue ; pas d'action en production sans décision du PO.
- Un agent peut rendre son travail et recevoir la revue dès qu'il finit ; pas d'attente artificielle des autres.

## Rythme
**Ticket validé → exécution → rapport → revue → arbitrage si besoin → intégration contrôlée.** Après chaque fusion : smoke limité aux zones affectées.
