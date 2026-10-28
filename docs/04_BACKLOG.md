# 04 — Backlog ordonné du MVP

**Architecture non négociable :** Vue dans `frontend/`, Laravel API dans `backend/`. Les tâches peuvent se chevaucher **uniquement** quand leurs prérequis sont levés et leurs fichiers ne se recouvrent pas.

| Ticket | Action / livrable | Dépend de | Statut initial | Responsable type |
|---|---|---|---|---|
| INF-00 | Créer `portfolio/`, `frontend/`, `backend/`, `docs/`, `AGENTS.md`, documents | — | FAIT (kit V0.2) | PO/copilote |
| INF-01 | Initialiser séparément Vue/Vite/Tailwind et Laravel 13 ; vérifier démarrages locaux | INF-00 | À FAIRE | Agent socle |
| INF-02 | Documenter scripts local, environnements exemple, ignores et conventions minimales | INF-01 | À FAIRE | Agent socle |
| DEC-01 | Arbitrer O-DB, O-AUTH, O-DATA, O-API nécessaires ; documenter contrat minimal | INF-01 | À FAIRE | PO + architecte |
| UX-01 | Définir sections vitrine + écrans admin minimalistes (sans fonctionnalités ajoutées) | INF-01 | À FAIRE | Front/UX + PO |
| BE-01 | Modèle de données et migrations métier validés + tests de base | DEC-01 | BLOQUÉ | Backend |
| BE-02 | Authentification admin et contrôle API avec tests | BE-01 + O-AUTH validée | BLOQUÉ | Backend |
| BE-03 | Endpoints publics de lecture de contenus selon contrat | BE-01 + O-API validée | BLOQUÉ | Backend |
| FE-01 | Layout responsive public en Vue ; données fictives **conformes au contrat** | UX-01 + contrat O-API minimal | BLOQUÉ | Frontend |
| FE-02 | Projets, expériences, profil, compétences, contact, CV, réseaux | FE-01 | BLOQUÉ | Frontend |
| BE-04 | CRUD projets/expériences protégés | BE-02 + O-DATA | BLOQUÉ | Backend |
| BE-05 | CRUD profil/compétences/réseaux + CV/médias selon O-MEDIA | BE-02 + O-DATA + O-MEDIA | BLOQUÉ | Backend |
| FE-03 | Connexion et shell admin Vue selon contrat O-AUTH | UX-01 + O-AUTH | BLOQUÉ | Frontend |
| FE-04 | Interfaces CRUD admin selon O-API/O-DATA | FE-03 + contrats validés | BLOQUÉ | Frontend |
| INT-01 | Brancher Vue sur API réelle et valider parcours admin → public | BE-03/04/05 + FE-02/04 | BLOQUÉ | Intégration |
| QA-01 | Tests ciblés du MVP + revue sécurité | INT-01 | BLOQUÉ | Reviewer |
| DEP-01 | Déploiement HTTPS, backups et smoke test | QA-01 + O-DEP | BLOQUÉ | Déploiement |

## Déroulement immédiat
1. **Maintenant :** ouvrir le dossier `portfolio/` dans VS Code.
2. **Ensuite :** envoyer `PROMPT_AGENT_01_SOCLE.md` à un seul agent pour INF-01.
3. Examiner le rapport : si validé, autoriser INF-02 et DEC-01/UX-01. La répartition multiagents vient après le socle.
4. Une fois données/auth/contrat approuvés, frontend et backend peuvent travailler **en parallèle** sur des fichiers distincts.

## Critères d'acceptation minimaux
- INF-01 : applications distinctes, versions détectées, `frontend` buildable, `backend` démarre et tests de démarrage pertinents effectués.
- BE : API validée + contrôles d'accès serveur + validations + tests ciblés.
- FE : responsive, états chargement/erreur, cohérence avec contrat.
- INT : mise à jour par l'admin visible sans modifier de code.
- QA/DEP : pas de secrets en dépôt, accès admin protégé, parcours critiques vérifiés.

**Pas d'audit sans fin.** Refaire uniquement les vérifications utiles quand le code ou l'environnement change.
