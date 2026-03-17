# Generation Dashboard HTML

## Objectif

Generer un dashboard HTML autonome, style dark premium, a partir de donnees enrichies. Le fichier HTML est auto-suffisant (pas de dependances externes sauf la police Inter) et peut etre ouvert directement dans un navigateur.

## Le Prompt

```
A partir des donnees enrichies de [DESCRIPTION_DONNEES], genere un dashboard HTML avec :

**Design :**
- Theme dark premium (fond #0f0f13)
- Police Inter (Google Fonts)
- Gradients subtils pour le header
- Style moderne et epure

**Contenu :**
- Header avec titre et sous-titre
- Barre de stats (nombre total, decideurs trouves, sources, etc.)
- Tableau interactif avec toutes les donnees
- Barre de recherche pour filtrer le tableau
- Liens cliquables (sites web, LinkedIn, etc.)
- Badges colores pour les categories/postes

**Technique :**
- Fichier HTML unique et autonome
- Pas de framework JS — vanilla uniquement
- Responsive design
- Tableau triable par colonnes

Sauvegarde le fichier sous [NOM_FICHIER].html
```

## Exemple Concret

> Ce prompt a genere le fichier [`decideurs_agences_seo_luxembourg.html`](../exemples/decideurs_agences_seo_luxembourg.html).

```
A partir des donnees enrichies des agences SEO au Luxembourg (decideurs identifies),
genere un dashboard HTML avec :

**Design :**
- Theme dark premium (fond #0f0f13)
- Police Inter (Google Fonts)
- Gradients subtils pour le header (bleu-violet-rose)
- Style moderne et epure

**Contenu :**
- Header avec titre "Decideurs - Top Agences SEO & Marketing Digital au Luxembourg"
- Barre de stats : nombre d'agences, decideurs identifies, top note moyenne
- Tableau interactif avec : entreprise, decideur, poste, telephone, site web, LinkedIn, note Google
- Barre de recherche pour filtrer le tableau
- Liens cliquables vers les sites web et profils LinkedIn
- Badges colores pour les postes (CEO, Fondateur, Directeur)

**Technique :**
- Fichier HTML unique et autonome
- Pas de framework JS — vanilla uniquement
- Responsive design
- Tableau triable par colonnes

Sauvegarde sous decideurs_agences_seo_luxembourg.html
```

## Personnalisation

| Parametre | Exemples |
|-----------|----------|
| **Theme** | `dark`, `light`, `bleu corporate`, `vert nature` |
| **Visualisations** | `graphiques`, `cartes`, `timeline`, `KPIs` |
| **Interactivite** | `filtres avances`, `export CSV`, `pagination` |
| **Branding** | `logo entreprise`, `couleurs personnalisees`, `footer avec contacts` |

### Astuces

- **Ouvrez le fichier exemple** : ouvrez [`decideurs_agences_seo_luxembourg.html`](../exemples/decideurs_agences_seo_luxembourg.html) dans votre navigateur pour voir le rendu attendu
- **Iterer sur le design** : demandez a Claude d'ajuster les couleurs, la mise en page ou les colonnes apres la premiere generation
- **Ajoutez des graphiques** : demandez des charts en SVG inline pour des visualisations sans dependances
- **Export** : demandez a Claude d'ajouter un bouton "Exporter en CSV" dans le dashboard
