# Covoiturage étudiant

Application web permettant aux étudiants d'un même campus de partager leurs trajets
(domicile ↔ école) pour réduire les coûts et l'empreinte carbone.

## Utilisateurs

- **Conducteur** : propose des trajets
- **Passager** : recherche et réserve une place
- **Administrateur** : modère les comptes et les signalements

## Fonctionnalités prévues

### v1.0 — Version minimale
- [ ] Inscription / connexion avec email étudiant
- [ ] Profil utilisateur
- [ ] Publier un trajet (départ, arrivée, date, heure, places, prix)
- [ ] Rechercher un trajet
- [ ] Réserver une place

### v1.1 — Améliorations
- [ ] Annuler une réservation
- [ ] Historique des trajets
- [ ] Notifications par email

### v2.0 — Communauté
- [ ] Messagerie conducteur / passager
- [ ] Notation et avis après un trajet
- [ ] Espace administrateur

## Technologies

| Partie | Technologie |
| --- | --- |
| Front-end | React |
| Back-end | Node.js / Express |
| Base de données | PostgreSQL |
| Versioning | Git / GitHub |

## Organisation Git (Git Flow)

| Branche | Rôle |
| --- | --- |
| `main` | Version en production, toujours stable |
| `develop` | Intégration et version de test |
| `feature/...` | Une branche par fonctionnalité, créée depuis `develop` |
| `release/...` | Préparation d'une version avant passage en production |
| `hotfix/...` | Correctif urgent créé depuis `main` |

## Règles de contribution

- Aucun push direct sur `main` ni `develop`
- Toute modification passe par une Pull Request vers `develop`
- Chaque Pull Request doit être relue et approuvée par au moins 1 membre
- Nommage des branches : `feature/nom`, `fix/nom`, `hotfix/nom`, `release/vX.Y`
- Messages de commit : `feat: ...`, `fix: ...`, `docs: ...`
- Versions numérotées : v1.0.0, v1.1.0, v2.0.0 (versionnage sémantique)
- Jamais de mot de passe ni de clé secrète dans le dépôt

## Équipe

| Membre | Rôle |
| --- | --- |
| Sonny FERREIRA | Responsable du dépôt |
| ... | Front-end |
| ... | Front-end |
| ... | Front-end |
| ... | Back-end |
| ... | Back-end |
| ... | Back-end |
| ... | Base de données |
