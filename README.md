# Portfolio Fullstack — MVP V1

**État :** Applications initialisées (ticket INF-01). `frontend/` = Vue 3 + Vite + Tailwind CSS ; `backend/` = Laravel 13 API HTTP/JSON.
**Pilotage :** Product Owner + copilote, réalisation par agents IA.
**Architecture ARCH-001 : VALIDÉE par le PO.**

## Objectif
Portfolio professionnel dynamique pour un développeur Fullstack : présenter profil, compétences, expériences, projets, CV, contact et réseaux sociaux. Un seul propriétaire gère les contenus par un back-office sécurisé. Pas d'inscription publique. MVP simple.

## Architecture et dossiers
```
portfolio/
├── frontend/           # application Vue 3 + Vite + Tailwind CSS (initialisée)
├── backend/            # application Laravel 13, API HTTP/JSON (initialisée)
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
Les dossiers `frontend/` et `backend/` sont initialisés : il faut exécuter les commandes d'installation ci-dessous avant de lancer les applications. Aucun agent ne doit lancer de commande depuis un répertoire inconnu.

## Installation et démarrage

### Prérequis
- PHP ≥ 8.3 (testé avec PHP 8.3.33)
- Composer ≥ 2.8
- Node.js ≥ 20 (testé avec Node v24.12.0, npm 11.10.0)

### Backend — Laravel 13 (API HTTP/JSON)
```powershell
cd backend
composer install
cp .env.example .env
php artisan key:generate
php artisan migrate
php artisan serve
```
Le backend Laravel démarre sur `http://localhost:8000` et sert la page d'accueil HTML par défaut. Les endpoints API JSON seront définis lorsque le contrat API aura été arbitré (décision O-API en attente).

### Frontend — Vue 3 + Vite + Tailwind CSS
```powershell
cd frontend
npm install
npm run dev       # serveur de développement
npm run build     # build de production (dossier dist/)
```

### Vérifications effectuées (INF-01)
- `composer create-project laravel/laravel:^13.0 backend` — PASS
- `php artisan --version` → Laravel Framework 13.39.0 — PASS
- `php artisan test --no-coverage` → 2 passed, 2 assertions — PASS
- `npm create vite@latest frontend -- --template vue` — PASS
- `npm install` — 35 packages, 0 vulnérabilités — PASS
- `npm install -D tailwindcss @tailwindcss/vite` — PASS
- `npm run build` — build de production réussi, dossier `dist/` généré — PASS

**À retenir :** `ARCH-001` est déjà décidée. Ne pas relancer une comparaison entre Vue intégré et Vue séparé.
