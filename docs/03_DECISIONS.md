# 03 — Registre des décisions

## VALIDÉES par le PO
| ID | Décision | Statut |
|---|---|---|
| ARCH-001 | Deux applications indépendantes : `frontend/` Vue 3 + Vite + Tailwind, `backend/` Laravel 13 API HTTP/JSON. Pas de Vue dans Laravel. | VALIDÉE |
| PROD-001 | Portfolio Fullstack orienté emploi/recruteurs, MVP simple. | VALIDÉE |
| PROD-002 | Un admin ; public sans compte ; modules profil/projets/expériences/compétences/contact/réseaux/CV. | VALIDÉE |
| TECH-001 | Pas de Filament, Inertia, Livewire ou générateur admin imposé. | VALIDÉE |
| ORG-001 | Un dossier parent `portfolio/` et documentation partagée sous `docs/`. | VALIDÉE |
| ORG-002 | Développement par agents IA avec validation PO et revue. | VALIDÉE |

## OUVERTES — à trancher lorsqu'elles bloquent un ticket
| ID | Question | Moment requis |
|---|---|---|
| O-DB | Quel SGBD et configuration par environnement ? | Avant migrations métier |
| O-AUTH | Quel flux d'authentification frontend distinct ↔ API Laravel (cookie/session ou autre stratégie) ? | Avant backend auth et formulaire de connexion |
| O-API | Routes, formats, erreurs et contrat des API ? | Avant composants branchés sur API |
| O-DATA | Champs/relations et contraintes des entités ? | Avant migrations métier |
| O-CONTACT | Coordonnées directes seules ou formulaire e-mail ? | Avant implémentation contact |
| O-UX | One-page ou plusieurs pages ; structure admin ? | Avant écrans fonctionnels |
| O-MEDIA | Stockage images/CV, type, taille et URL publique ? | Avant uploads |
| O-DEP | Hébergement et URL distinctes ou proxy unifié ; HTTPS/CORS ? | Avant production |

## Règle
Une décision `OUVERTE` ne doit jamais être présentée comme déjà acceptée. L'agent peut proposer au maximum deux options contextualisées au ticket, sans implémenter la partie bloquée.
