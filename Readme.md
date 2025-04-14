🛒 Scraping Auchan & Monoprix
Ce projet propose deux scripts de scraping avancés pour extraire des données produits depuis Auchan Drive et Monoprix.

🚀 Méthodologie
Scraping Auchan
Récupération des magasins

Automatisation de la navigation sur le site Auchan Drive avec undetected-chromedriver.

Scroll infini pour charger tous les magasins.

Extraction des IDs des magasins nécessaires pour choisir le magasin lors des prochaines requêtes.

Récupération des catégories

Navigation vers la page du magasin sélectionné.

Extraction de tous les liens de catégories produits.

Récupération des articles par catégorie

Pour chaque catégorie :

Scroll infini pour charger tous les articles.

Récupération des liens de chaque produit.

Scraping des produits

Pour chaque lien d'article :

Visite de la page produit.

Sélection du magasin voulu.

Extraction des métadonnées produit (prix, stock, description, etc.).

Technologies utilisées :
Python, Selenium, Undetected-chromedriver, Time, JSON, OS.

Scraping Monoprix
Connexion utilisateur

Accès automatisé au site Monoprix.

Connexion à un compte en saisissant un email.

Récupération des catégories

Appels API au site Monoprix pour récupérer les IDs de toutes les catégories et sous-catégories de produits.

Récupération des produits

Pour chaque sous-catégorie :

Appels API pour récupérer toutes les informations produits (prix, stock, description, etc.) sans passer par l'interface graphique.

Technologies utilisées :
Python, Selenium, Undetected-chromedriver, Requests, JSON.

📦 Prérequis
Python 3.x

Packages Python nécessaires :

selenium

undetected-chromedriver

requests

Installation rapide
bash
Copier
Modifier
pip install selenium undetected-chromedriver requests
🛠️ Lancement
Cloner le projet :

bash
Copier
Modifier
git clone [url_du_repo]
cd [nom_du_dossier]
Exécuter les notebooks :

auchan_scrapping.ipynb : pour scraper toutes les informations produits du site Auchan Drive.

monoprix_scrapping.ipynb : pour scraper toutes les informations produits du site Monoprix via API.

