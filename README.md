# CrawlerWeb : Un outil de Web Crawling en Python

# Jules Dumouchel


### À propos

CrawlerWeb est une classe Python flexible et facile à utiliser pour le web crawling. Conçue pour être simple mais efficace, elle permet de parcourir des sites web en récupérant les liens et en respectant les bonnes pratiques de politesse du web.
Caractéristiques

Crawl simple: Parcourt les pages web à partir d'une URL de départ, en collectant les liens.
Respect de la politesse: Attend 3 secondes entre chaque requête pour ne pas surcharger les serveurs.
Traitement des Sitemaps: Permet de récupérer les URLs depuis des fichiers sitemap et sitemap index.
Configuration flexible: Paramètres pour limiter le nombre total de pages à visiter et le nombre de liens par page.
Verbose Mode: Option pour activer des logs détaillés pendant le crawl.

## Utilisation


Initialisation

python

crawler = CrawlerWeb("https://example.com", max_urls=50, max_links_page=5, verbose=True)

Démarrer le Crawl

visited_urls = crawler.crawl()

Récupérer les URLs depuis un Sitemap


sitemap_urls = crawler.get_sitemaps_from_index("https://example.com/sitemap_index.xml")
page_urls = crawler.get_urls_from_sitemap("https://example.com/sitemap.xml")

### Exécuter un Crawl Complet à partir d'un Sitemap Index


all_urls = crawler.simple_web_crawler("https://example.com/sitemap_index.xml", max_urls=150)

## Dépendances

Python 3.x
requests
beautifulsoup4

### Installation des Dépendances

bash

pip install requests beautifulsoup4
