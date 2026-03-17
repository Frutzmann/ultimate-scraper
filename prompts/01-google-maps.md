# Scraping Google Maps

## Objectif

Extraire une liste d'entreprises depuis Google Maps selon un secteur d'activite et une localisation. Recupere : nom, adresse, telephone, site web, email, categories, note Google, nombre d'avis, et liens reseaux sociaux (LinkedIn, Facebook, Instagram).

## Le Prompt

```
Utilise Apify pour scraper Google Maps.

Je cherche des [TYPE D'ENTREPRISE] a [LOCALISATION].

Pour chaque entreprise, recupere :
- Nom
- Adresse
- Telephone
- Site Web
- Email
- Categories
- Note Google
- Nombre d'avis
- LinkedIn
- Facebook
- Instagram

Exporte le tout dans un fichier CSV.
```

## Exemple Concret

> Ce prompt a ete utilise pour generer le fichier [`agences_seo_luxembourg.csv`](../exemples/agences_seo_luxembourg.csv) (176 resultats).

```
Utilise Apify pour scraper Google Maps.

Je cherche des agences SEO a Luxembourg.

Pour chaque entreprise, recupere :
- Nom
- Adresse
- Telephone
- Site Web
- Email
- Categories
- Note Google
- Nombre d'avis
- LinkedIn
- Facebook
- Instagram

Exporte le tout dans un fichier CSV.
```

## Personnalisation

| Parametre | Exemples |
|-----------|----------|
| **Type d'entreprise** | `restaurants`, `cabinets d'avocats`, `agences immobilieres`, `salles de sport` |
| **Localisation** | `Paris`, `Bruxelles`, `Lyon 3eme arrondissement`, `Geneve Suisse` |
| **Champs supplementaires** | `horaires d'ouverture`, `photos`, `avis clients` |

### Astuces

- **Elargir la recherche** : utilisez des termes generiques comme "marketing digital" au lieu de "SEO" pour capter plus de resultats
- **Cibler une zone** : ajoutez le code postal ou l'arrondissement pour affiner
- **Plusieurs recherches** : lancez plusieurs prompts avec des variantes de mots-cles pour maximiser la couverture (ex: "agence SEO", "referencement naturel", "consultant SEO")
