# 06 — Qualité proportionnée au MVP

## Fini signifie
- Périmètre livré strictement conforme au ticket.
- Application concernée démarre et les tests pertinents passent.
- Aucune donnée secrète committée ; aucun accès admin non autorisé.
- Rapport vérifiable : commande, résultat, fichiers touchés, limites.
- Revue indépendante avant intégration.

## Vérifications critiques
1. Vue démarre et le build frontend se termine sans erreur.
2. Laravel démarre, version conforme et tests de base pertinents.
3. Connexion/déconnexion admin, refus des accès privés anonymes.
4. CRUD projets/expériences/compétences/réseaux/profil réellement persistés.
5. Vitrine Vue affiche les données API actualisées.
6. CV/liens de contact utilisables si fonctionnalités retenues.
7. Interface mobile correcte, erreurs API gérées.
8. Validation serveur, contraintes fichiers, CORS/auth/CSRF selon O-AUTH, HTTPS en production.

## Pas de sur-audit
Tests ciblés par ticket, puis passage critique avant livraison. Réutiliser les preuves PASS encore valides ; ne pas redérouler des campagnes entières sans changement utile.
