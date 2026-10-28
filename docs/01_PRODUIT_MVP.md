# 01 — Produit MVP V1 (validé au niveau macro)

## Finalité
Portfolio professionnel dynamique pour développeur Fullstack, orienté recruteurs. Le propriétaire actualise le contenu depuis un back-office sans modifier le code. Pas de produit SaaS et pas de fonctionnalités superflues.

## Côté public (Vue)
- Accueil / profil : présentation, titre, informations et photo éventuelle.
- Projets : réalisations avec description, technologies, liens pertinents et image éventuelle.
- Expériences professionnelles.
- Compétences.
- CV disponible si le propriétaire en fournit un.
- Contact et liens vers les réseaux sociaux professionnels.
- Responsive mobile/desktop.

## Back-office (Vue)
- Connexion/déconnexion du propriétaire unique.
- Modifier le profil et les informations de contact.
- Ajouter/modifier/supprimer les projets, expériences, compétences et liens sociaux.
- Mettre à jour le CV et les images pertinentes.
- Voir les modifications sur le site public après enregistrement.

## Hors MVP
Blog, CRM, témoignages, réservations, multi-administrateurs, inscription publique, paiement, analytics avancées, messagerie interne, notifications complexes, IA.

## Décisions de détail à prendre avant implémentation concernée
- Site en une page ou plusieurs pages.
- Contact par coordonnées/liens seulement ou formulaire e-mail ; rien à inventer.
- Champs métier exacts et traitement des suppressions.
- Règles de publication de projets : pas de statuts complexes présumés.
- CV et images : contraintes, formats et emplacement de stockage.

## Succès du MVP
L'admin change projets/expériences/profil/réseaux sans toucher au code ; le visiteur consulte les données à jour ; les API administratives sont protégées ; interface mobile lisible ; livraison reproductible.
