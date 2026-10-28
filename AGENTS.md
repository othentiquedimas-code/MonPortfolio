# Règles obligatoires pour les agents IA

## Autorité
Le PO décide du produit ; les documents approuvés décrivent les comportements à implémenter. **Ne jamais inventer une règle métier, un champ, une relation, une route ou un workflow.** En cas de manque : signaler l'arbitrage et arrêter seulement la partie concernée.

## ARCH-001 — Architecture imposée
- `frontend/` = application Vue 3 + Vite + Tailwind CSS **indépendante**. Elle contient site public **et** back-office.
- `backend/` = application Laravel 13 **indépendante**, API HTTP/JSON et métier.
- `docs/` = source de vérité commune.
- **Interdits :** installer Vue dans Laravel ; transformer Laravel en rendu Blade du portfolio ; adopter Inertia, Livewire ou Filament ; ajouter une troisième application ; inverser l'architecture.
- Pas de paquet supplémentaire important sans accord écrit. Les dépendances officielles nécessaires à la stack validée peuvent être installées par l'agent socle dans le périmètre de son ticket.

## Avant tout changement
Lire `README.md`, `docs/01` à `docs/07` et le ticket en cours. Vérifier le chemin courant, les fichiers existants et les versions installées. Ne jamais écraser une application existante. Demander une décision si un choix technique **non validé** est indispensable pour continuer.

## Périmètre MVP
Profil, CV, projets, expériences, compétences, liens sociaux, contact, administration monopersonnelle. Pas de blog, CRM, clients, paiement, multi-admin, temps réel, IA ni statistiques avancées.

## Limites d'action
- Ne pas créer d'API, tables, règles de publication, stockage média ou mécanisme d'auth selon sa préférence personnelle.
- Ne jamais exposer de secret ni committer les `.env` locaux.
- Ne pas toucher à la production, DNS, domaines ou hébergement sans autorisation.
- Ne pas merger, pousser de force, réécrire l'historique Git ou supprimer des données sans autorisation.
- Une mission = un périmètre défini = un rapport. Seule l'implémentation autorisée par le ticket peut être modifiée.

## Travail et validation
1. Reformuler ticket, dépendances et périmètre avant intervention.
2. Modifier seulement les dossiers/fichiers attribués.
3. Exécuter les contrôles réellement possibles ; distinguer `PASS`, `FAIL`, `NOT_RUN`.
4. Rendre un rapport conforme à `docs/templates/RAPPORT_AGENT.md`.
5. Soumettre à revue indépendante ; ne pas s'auto-approuver.

## Quand une décision manque
```
BLOCKED
Ticket : ...
Question : ...
Options (2 maximum) : ...
Recommandation argumentée : ...
Partie non commencée : ...
```
**Hiérarchie :** décision explicite du PO > décisions documentées > règles métier > contrat validé > ticket > code existant. Signaler les conflits.
