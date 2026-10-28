# 07 — Contrat API (à spécifier et valider)

**Statut : OUVERT — aucun endpoint métier n'est encore autorisé.**  
Architecture imposée : `frontend/` consomme en HTTP/JSON l'application Laravel 13 dans `backend/`.

## À renseigner avec le PO lors de DEC-01
- Base URL selon environnement local/prod et stratégie CORS/proxy.
- Ressources publiques en lecture (profil, projets, expériences, compétences, réseaux).
- Authentification admin et règles d'accès (O-AUTH).
- Format de réponse JSON, pagination (si utile), erreurs et codes HTTP.
- Contrats écriture admin et validation des champs par entité.
- Contrat upload CV/images si retenu.
- Quelques fixtures JSON de référence pour permettre le frontend en parallèle.

## Statut obligatoire
Chaque endpoint proposé : `DRAFT` → `APPROUVÉ PAR PO` → `IMPLÉMENTÉ` → `TESTÉ`.

**N'inventez ni routes, ni champs, ni statuts, ni tokens avant arbitrage.** L'agent peut proposer des conventions, pas les imposer.
