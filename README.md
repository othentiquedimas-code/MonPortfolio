# Portfolio Fullstack — MVP V1

**État :** dossier de travail préparé. Applications frontend et backend **non initialisées**.  
**Pilotage :** Product Owner + copilote, réalisation par agents IA.  
**Architecture ARCH-001 : VALIDÉE par le PO.**

## Objectif
Portfolio professionnel dynamique pour un développeur Fullstack : présenter profil, compétences, expériences, projets, CV, contact et réseaux sociaux. Un seul propriétaire gère les contenus par un back-office sécurisé. Pas d'inscription publique. MVP simple.

## Architecture et dossiers
```
portfolio/
├── frontend/           # application Vue 3 + Vite + Tailwind (à initialiser)
├── backend/            # application Laravel 13, API HTTP/JSON (à initialiser)
├── docs/               # référentiel métier / décisions / backlog / contrats
├── AGENTS.md           # règles communes
├── PROMPT_AGENT_01_SOCLE.md
└── README.md
```
**Obligatoire :** deux applications indépendantes ; **pas de Vue dans Laravel**. Le site public et le back-office sont dans l'application Vue. Laravel héberge la logique et les API, pas les pages du site. La topologie Git n'est **pas** décidée par cette architecture de dossiers.

## Stack validée
- `frontend/` : Vue 3, Vite, Tailwind CSS.
- `backend/` : Laravel 13 et API JSON.
- **Non décidés :** SGBD, mécanisme d'authentification API, schémas/endpoints API, hébergement, domaine, stratégie de médias. Les agents proposent sans imposer.
- **Exclus par défaut :** Filament, Inertia, Livewire et bibliothèques CRUD non approuvées.

## Lire avant d'agir
1. `AGENTS.md`
2. `docs/01_PRODUIT_MVP.md`
3. `docs/02_REGLES_METIER.md`
4. `docs/03_DECISIONS.md`
5. `docs/04_BACKLOG.md`
6. `docs/05_PROTOCOLE_AGENTS.md`
7. `docs/06_QUALITE_LIVRAISON.md`
8. `docs/07_CONTRAT_API.md`

## Premier pas sur Windows
Décompresser l'archive **dans le dossier parent** choisi (exemple `C:\PROJETS\`). Puis ouvrir `portfolio/` dans VS Code :
```powershell
cd C:\PROJETS\portfolio
code .
```
Les dossiers `frontend/` et `backend/` sont volontairement **vides**, pas encore générés : il faut ensuite confier `PROMPT_AGENT_01_SOCLE.md` à l'agent socle. Aucun agent ne doit lancer de commande depuis un répertoire inconnu.

**À retenir :** `ARCH-001` est déjà décidée. Ne pas relancer une comparaison entre Vue intégré et Vue séparé.
