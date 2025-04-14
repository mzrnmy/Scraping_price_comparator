# Scraping Auchan & Monoprix

Ce projet propose deux scripts de scraping avancés pour extraire des données produits depuis **Auchan Drive** et **Monoprix**.

---

## Méthodologie

### Scraping Auchan

**1. Récupération des magasins**
- Automatisation de la navigation sur le site Auchan Drive avec **undetected-chromedriver**.
- **Scroll infini** pour charger tous les magasins.
- Extraction des **IDs des magasins** nécessaires pour choisir le magasin lors des prochaines requêtes.

**2. Récupération des catégories**
- Navigation vers la page du magasin sélectionné.
- Extraction de **tous les liens de catégories** produits.

**3. Récupération des articles par catégorie**
- Pour chaque catégorie :
  - **Scroll infini** pour charger tous les articles.
  - **Récupération des liens** de chaque produit.

**4. Scraping des produits**
- Pour chaque lien d'article :
  - Visite de la page produit.
  - Sélection du magasin voulu.
  - Extraction des **métadonnées produit** (prix, stock, description, etc.).

> **Technos utilisées** :  
> Python, Selenium, Undetected-chromedriver, Time, JSON, OS.

---

### Scraping Monoprix

**1. Connexion utilisateur**
- Accès automatisé au site Monoprix.
- Connexion à un compte avec saisie d'un **email**.

**2. Récupération des catégories**
- Appels **API** au site Monoprix pour récupérer les **IDs** de toutes les catégories et sous-catégories produits.

**3. Récupération des produits**
- Pour chaque sous-catégorie :
  - Appels **API** pour récupérer **toutes les informations produits** (prix, stock, description, etc.) sans passer par l'interface graphique.

> **Technos utilisées** :  
> Python, Selenium, Undetected-chromedriver, Requests, JSON.

---
## Remarques
undetected-chromedriver est utilisé pour contourner certaines protections anti-scraping.

Respecter les conditions d'utilisation d'Auchan et de Monoprix lors de l'utilisation du script.



## Prérequis

- un mdp dans un fichier .env 
- Python 3.x
- Packages Python nécessaires :
  - `selenium`
  - `undetected-chromedriver`
  - `requests`

### Installation rapide

```bash
pip install selenium undetected-chromedriver requests