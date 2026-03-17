# Scraping LinkedIn

## Objectif

Extraire des donnees depuis LinkedIn : pages entreprises, profils publics, postes et informations de contact.

> **Attention** : LinkedIn a des conditions d'utilisation strictes concernant le scraping. Limitez-vous aux donnees publiquement accessibles et n'utilisez jamais ces donnees pour du spam ou du harcelement. Respectez les limites de taux et le RGPD.

## Le Prompt

### Scraper des pages entreprises

```
Utilise Apify pour scraper les pages LinkedIn de ces entreprises :
[LISTE D'URLs LinkedIn OU NOMS D'ENTREPRISES]

Pour chaque entreprise, recupere :
- Nom de l'entreprise
- Description
- Secteur d'activite
- Taille (nombre d'employes)
- Siege social
- Site web
- Specialites
- Nombre de followers

Exporte le tout dans un fichier CSV.
```

### Scraper des profils publics

```
Utilise Apify pour scraper ces profils LinkedIn publics :
[LISTE D'URLs LinkedIn]

Pour chaque profil, recupere :
- Nom complet
- Titre / Poste actuel
- Entreprise actuelle
- Localisation
- Resume / A propos
- Experience (3 derniers postes)

Exporte le tout dans un fichier CSV.
```

## Exemple Concret

> Utilise pour enrichir les donnees des agences SEO du Luxembourg a partir de leurs pages LinkedIn.

```
Utilise Apify pour scraper les pages LinkedIn des entreprises suivantes :
- https://www.linkedin.com/company/adoraweb
- https://www.linkedin.com/company/adwire-luxembourg
- https://www.linkedin.com/company/aixh

Pour chaque entreprise, recupere :
- Nom de l'entreprise
- Description
- Secteur d'activite
- Taille (nombre d'employes)
- Siege social
- Site web
- Specialites
- Employes cles (fondateurs, CEO, directeurs)

Exporte le tout dans un fichier CSV.
```

## Personnalisation

| Parametre | Exemples |
|-----------|----------|
| **Source** | Pages entreprises, profils individuels, resultats de recherche |
| **Donnees** | `employes cles`, `postes recents`, `specialites`, `certifications` |
| **Filtres** | `fondateurs uniquement`, `C-level`, `directeurs marketing` |

### Astuces

- **Partez du CSV Google Maps** : utilisez les URLs LinkedIn extraites pour enrichir automatiquement
- **Ciblez les decideurs** : combinez avec le prompt d'enrichissement ([04-enrichissement-decideurs.md](04-enrichissement-decideurs.md))
- **Respectez les limites** : ne scrapez pas plus de quelques dizaines de profils a la fois
