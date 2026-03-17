# Enrichissement Decideurs

## Objectif

A partir d'un CSV brut d'entreprises (issu d'un scrape Google Maps par exemple), identifier les decideurs (fondateurs, CEO, directeurs) en croisant les donnees avec LinkedIn, et produire un dataset enrichi pret a l'usage.

C'est le **"money prompt"** — celui qui transforme une simple liste d'entreprises en une base de prospection qualifiee.

## Le Prompt

```
J'ai un fichier CSV d'entreprises : [NOM_DU_FICHIER.csv]

Pour chaque entreprise qui a un lien LinkedIn, utilise Apify pour :
1. Trouver les decideurs (fondateur, CEO, directeur, gerant, managing director)
2. Recuperer pour chaque decideur :
   - Nom complet
   - Poste / Titre
   - Profil LinkedIn
   - Email (si disponible publiquement)
3. Ajouter ces informations au dataset

Produis un nouveau fichier enrichi avec :
- Toutes les colonnes du CSV original
- Colonnes supplementaires : Decideur_Nom, Decideur_Poste, Decideur_LinkedIn, Decideur_Email

Genere aussi un resume : combien d'entreprises traitees, combien de decideurs trouves, taux de reussite.
```

## Exemple Concret

> Ce prompt a ete utilise pour transformer le fichier [`agences_seo_luxembourg.csv`](../exemples/agences_seo_luxembourg.csv) (176 agences) en un dataset de 50+ decideurs identifies.

```
J'ai un fichier CSV d'agences SEO au Luxembourg : agences_seo_luxembourg.csv

Pour chaque agence qui a un lien LinkedIn, utilise Apify pour :
1. Trouver les decideurs (fondateur, CEO, directeur, gerant, managing director)
2. Recuperer pour chaque decideur :
   - Nom complet
   - Poste / Titre
   - Profil LinkedIn
   - Email (si disponible publiquement)
3. Ajouter ces informations au dataset

Produis un nouveau fichier enrichi avec :
- Toutes les colonnes du CSV original
- Colonnes supplementaires : Decideur_Nom, Decideur_Poste, Decideur_LinkedIn, Decideur_Email

Genere aussi un resume : combien d'entreprises traitees, combien de decideurs trouves, taux de reussite.
```

## Personnalisation

| Parametre | Exemples |
|-----------|----------|
| **Roles cibles** | `CEO`, `CTO`, `Directeur Marketing`, `Fondateur`, `Head of Sales` |
| **Source CSV** | N'importe quel CSV avec une colonne LinkedIn |
| **Donnees supplementaires** | `anciennete au poste`, `formation`, `publications recentes` |

### Astuces

- **Qualite du CSV source** : plus votre CSV initial contient de liens LinkedIn, plus l'enrichissement sera efficace
- **Ciblez les bons roles** : adaptez la liste des roles selon votre prospection (tech → CTO, marketing → CMO, etc.)
- **Faites-le par batches** : pour les gros CSV, demandez a Claude de traiter par lots de 20-30 entreprises
- **Verifiez les resultats** : Claude peut parfois confondre des employes avec des decideurs — une verification rapide vaut le coup
