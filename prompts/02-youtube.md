# Scraping YouTube

## Objectif

Extraire des donnees depuis YouTube : informations de chaines, details de videos, statistiques, commentaires et transcripts.

## Le Prompt

### Scraper une video

```
Utilise Apify pour scraper cette video YouTube : [URL_VIDEO]

Recupere :
- Titre
- Auteur / Chaine
- Date de publication
- Nombre de vues
- Nombre de likes
- Nombre de commentaires
- Description complete
- Tous les commentaires avec auteur, date et nombre de likes
- Transcript / sous-titres

Exporte le tout dans un fichier Markdown structure.
```

### Scraper une chaine

```
Utilise Apify pour scraper la chaine YouTube : [URL_CHAINE]

Recupere :
- Nom de la chaine
- Nombre d'abonnes
- Nombre total de videos
- Description
- Pour les [NOMBRE] dernieres videos :
  - Titre
  - URL
  - Date de publication
  - Nombre de vues
  - Nombre de likes
  - Duree

Exporte le tout dans un fichier CSV.
```

## Exemple Concret

> Ce prompt a ete utilise pour extraire les donnees de la video `fPssA1JUs18`.

```
Utilise Apify pour scraper cette video YouTube : https://www.youtube.com/watch?v=fPssA1JUs18

Recupere :
- Titre
- Auteur / Chaine
- Date de publication
- Nombre de vues
- Nombre de likes
- Nombre de commentaires
- Description complete
- Tous les commentaires avec auteur, date et nombre de likes
- Transcript / sous-titres

Exporte le tout dans un fichier Markdown structure.
```

## Personnalisation

| Parametre | Exemples |
|-----------|----------|
| **Source** | URL de video, URL de chaine, URL de playlist |
| **Donnees** | `commentaires uniquement`, `stats uniquement`, `transcript uniquement` |
| **Volume** | `les 10 dernieres videos`, `toutes les videos de 2025`, `les 50 videos les plus vues` |
| **Format** | `CSV`, `Markdown`, `JSON` |

### Astuces

- **Analyse concurrentielle** : scrapez les chaines de vos concurrents pour identifier leurs videos les plus performantes
- **Recherche de contenu** : utilisez les transcripts pour analyser les sujets abordes
- **Veille** : scrapez regulierement pour suivre l'evolution des stats
