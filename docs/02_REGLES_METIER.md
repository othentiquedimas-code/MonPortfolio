# 02 — Règles métier (validation macro)

## Principes validés
- RM-001 : un seul propriétaire/admin gère le contenu ; aucune inscription publique.
- RM-002 : le public consulte les données du portfolio sans compte.
- RM-003 : le propriétaire peut gérer projets, expériences, compétences, profil, réseaux sociaux depuis le back-office.
- RM-004 : toute modification enregistrée et autorisée est reflétée dans le portfolio via les données du backend.
- RM-005 : la vitrine et l'administration sont développées en Vue ; Laravel fournit une API et protège côté serveur l'administration.
- RM-006 : le site reste volontairement simple, sans workflows complexes non demandés.

## Domaines métier à préciser à la bonne étape
- **Profil :** champs exacts, photo, intitulé, liens de CV.
- **Projets :** champs, gestion de l'ordre, visibilité, images, technologies, liens, suppression.
- **Expériences :** champs, dates, emploi actuel, ordre d'affichage.
- **Compétences :** champs, catégorie et ordre si nécessaires.
- **Réseaux sociaux :** plateformes admises et validité des URLs.
- **Contact :** simple lien d'e-mail / WhatsApp / coordonnées, ou formulaire de contact ; décision PO nécessaire.
- **CV/médias :** formats, tailles, stockage, remplacements et suppression.

**Important :** les exemples de champs ne sont pas des colonnes SQL validées. L'agent en charge doit proposer un dictionnaire de données et attendre l'accord PO avant les migrations métier.

## Règles transversales
- L'admin ne peut pas être protégé uniquement en masquant un menu Vue : Laravel contrôle les accès.
- Les données sensibles ne sont pas exposées publiquement.
- Les erreurs de validation doivent être traitées clairement côté frontend et backend.
- Pas d'invention de statuts brouillon/publié, de rôles ou de notifications.
