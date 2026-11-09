# Covoiturage étudiant — Organisation du versioning

Projet réalisé dans le cadre du cours de versioning Git.
Application de covoiturage étudiant développée par une équipe de 8 personnes.

## 1. Définition du projet

### Besoins
- **Versions en parallèle** : oui, plusieurs fonctionnalités développées en même temps et des correctifs pendant le développement
- **Besoin de stabilité** : oui, la version publiée doit toujours fonctionner
- **Version test en ligne** : oui, une version de test séparée de la version publiée

### L'équipe
- **Taille** : 8 personnes (équipe moyenne)
- **Niveau d'expertise** : hétérogène

| Rôle | Membre(s) | Missions |
| --- | --- | --- |
| Responsable du dépôt | ... | Crée le dépôt, gère les accès et les protections |
| Responsable des versions | ... | Prépare les versions, fusionne `develop` dans `main`, crée les tags |
| Relecteurs | ..., ... | Relisent et approuvent les Pull Requests |
| Développeurs | ..., ..., ..., ... | Développent sur leurs branches et ouvrent des Pull Requests |

Tous les membres développent et relisent au moins une fois.

## 2. Organisation Git

### Workflow : Git Flow

| Branche | Rôle |
| --- | --- |
| `main` | Version publiée, toujours stable |
| `develop` | Intégration et version de test |
| `feature/...` | Une branche par fonctionnalité, créée depuis `develop` |
| `release/...` | Préparation d'une version avant publication |
| `hotfix/...` | Correctif urgent créé depuis `main` |

### Outils
- **GitHub** : hébergement du dépôt
- **Issues** : une tâche = une issue assignée
- **Projects** : tableau Kanban (À faire / En cours / En review / Fait)
- **Pull Requests** : relecture avant fusion
- **GitHub Actions** : tests et déploiement automatiques

### Règles
- Aucun push direct sur `main` ni `develop` (branches protégées)
- Toute modification passe par une Pull Request vers `develop`
- Au moins 1 approbation par un autre membre avant fusion
- Branches : `feature/nom`, `fix/nom`, `hotfix/nom`, `release/vX.Y`
- Commits : `feat: ...`, `fix: ...`, `docs: ...`
- Versions numérotées : v1.0.0, v1.1.0, v2.0.0

## 3. Pratique en équipe

1. Créer ou prendre une issue
2. Créer sa branche depuis `develop`
3. Faire ses commits et pousser sa branche
4. Ouvrir une Pull Request vers
