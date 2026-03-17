<div align="center">

# Ultimate Scraper

### Scrape n'importe quoi avec Claude Code + Apify. En langage naturel.

[![Claude Code](https://img.shields.io/badge/Claude_Code-Opus-blueviolet?style=for-the-badge&logo=anthropic)](https://claude.com/claude-code)
[![Apify MCP](https://img.shields.io/badge/Apify-MCP_Server-00C853?style=for-the-badge)](https://apify.com/)
[![Langue](https://img.shields.io/badge/Langue-Fran%C3%A7ais-blue?style=for-the-badge)]()
[![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)](LICENSE)
[![Prompts](https://img.shields.io/badge/Prompts-5_pr%C3%AAts_%C3%A0_l'emploi-ff69b4?style=for-the-badge)]()

</div>

---

<div align="center">

**176 agences scrapees** | **50+ decideurs identifies** | **3 sources** | **5 prompts prets a l'emploi**

</div>

---

## Video

`[LIEN VIDEO A VENIR]`

---

## Le Workflow en 3 Etapes

```
1. SCRAPER          →    2. ENRICHIR          →    3. FORMATER
Google Maps              Identifier les              Dashboard HTML
YouTube                  decideurs (CEO,             CSV structure
LinkedIn                 fondateurs) via             Tableau triable
                         LinkedIn
```

| Etape | Ce que fait Claude | Output |
|-------|-------------------|--------|
| **Scraper** | Interroge Apify pour extraire les donnees brutes d'une source | CSV avec nom, adresse, telephone, site web, reseaux sociaux |
| **Enrichir** | Croise les donnees avec LinkedIn pour trouver les decideurs | Dataset enrichi avec noms, postes, profils LinkedIn |
| **Formater** | Genere un dashboard HTML interactif a partir des donnees | Fichier HTML autonome, dark theme, tableau triable |

---

## Demarrage Rapide

### 1. Installer Claude Code

```bash
npm install -g @anthropic-ai/claude-code
```

### 2. Creer un compte Apify

Rendez-vous sur [apify.com](https://apify.com/) et creez un compte gratuit (le free tier suffit pour commencer).

### 3. Ajouter la config MCP

Copiez le contenu de [`config/claude-mcp-config.json`](config/claude-mcp-config.json) dans votre fichier `~/.claude.json` (section `mcpServers`).

---

## Sources Supportees

| Source | Ce qu'on extrait | Prompt |
|--------|-----------------|--------|
| **Google Maps** | Entreprises, adresses, telephones, sites web, avis, reseaux sociaux | [01-google-maps.md](prompts/01-google-maps.md) |
| **YouTube** | Chaines, videos, stats, commentaires, transcripts | [02-youtube.md](prompts/02-youtube.md) |
| **LinkedIn** | Pages entreprises, profils, postes, connexions | [03-linkedin.md](prompts/03-linkedin.md) |

---

## Prompts Prets a l'Emploi

1. [**Google Maps**](prompts/01-google-maps.md) — Scraper des entreprises par secteur et localisation
2. [**YouTube**](prompts/02-youtube.md) — Extraire les donnees de chaines et videos
3. [**LinkedIn**](prompts/03-linkedin.md) — Scraper des profils et pages entreprises
4. [**Enrichissement Decideurs**](prompts/04-enrichissement-decideurs.md) — Identifier les decideurs a partir d'un CSV brut
5. [**Generation Dashboard**](prompts/05-generation-dashboard.md) — Creer un dashboard HTML interactif

---

<div align="center">

## Integre l'IA dans ton business

<img src="https://img.shields.io/badge/Francois-L'Atelier_de_l'Automatisation-blueviolet?style=for-the-badge" alt="Francois ALA"/>

**Francois** | L'Atelier de l'Automatisation

Libere-toi de tes taches administratives et automatise ton business avec l'IA.

[![Prendre RDV](https://img.shields.io/badge/Calendly-Prendre_RDV_(15_min)-00a2ff?style=for-the-badge&logo=calendly)](https://calendly.com/latelierautomatisation/15min)

[![YouTube](https://img.shields.io/badge/YouTube-@FrancoisALA-red?style=for-the-badge&logo=youtube)](https://www.youtube.com/@FrancoisALA)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Francois_ALA-0077B5?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/francoisala)

</div>

---

## FAQ

<details>
<summary><strong>Est-ce legal de scraper ces donnees ?</strong></summary>

Le scraping de donnees publiquement accessibles est generalement legal dans l'UE, conformement a la jurisprudence recente. Les donnees extraites ici (Google Maps, YouTube) sont publiques. Pour LinkedIn, respectez les conditions d'utilisation et limitez-vous aux donnees publiques. N'utilisez jamais ces donnees pour du spam ou du harcelement.
</details>

<details>
<summary><strong>Combien ca coute ?</strong></summary>

- **Claude Code** : inclus dans votre abonnement Claude (Pro, Team ou Enterprise)
- **Apify** : le free tier offre $5/mois de credits, suffisant pour des centaines de scrapes. Les Actors utilises coutent generalement entre $0.25 et $2 pour 1000 resultats.
</details>

<details>
<summary><strong>Je peux scraper d'autres sources ?</strong></summary>

Oui ! Apify propose 3000+ Actors pour scraper pratiquement n'importe quelle source : Amazon, TripAdvisor, Twitter/X, Instagram, Booking, Airbnb, etc. Adaptez simplement les prompts a votre source cible. Claude Code trouvera automatiquement le bon Actor sur Apify.
</details>

<details>
<summary><strong>Quel niveau technique faut-il ?</strong></summary>

Aucun. C'est la toute la puissance de cette approche : vous ecrivez en langage naturel, Claude Code fait le reste. Si vous savez ecrire un email, vous savez scraper avec cet outil.
</details>

<details>
<summary><strong>Ca marche sur Windows / Mac / Linux ?</strong></summary>

Oui, Claude Code fonctionne sur les trois plateformes. Il suffit d'avoir Node.js installe.
</details>

---

## Licence

Ce projet est sous licence [MIT](LICENSE). Utilisez-le, modifiez-le, partagez-le librement.

---

<div align="center">

**Fait avec Claude Code** | **[Prendre RDV](https://calendly.com/latelierautomatisation/15min)** | **[@FrancoisALA](https://www.youtube.com/@FrancoisALA)**

</div>
