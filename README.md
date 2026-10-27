# Blog Site

Projet de blog développé avec Django. Le projet contient actuellement deux applications :

- `blog` : gestion des articles et de leur statut (brouillon ou publié) ;
- `accounts` : fonctionnalités liées aux comptes utilisateurs.

## Prérequis

- Python 3.13 ou une version compatible avec les dépendances du projet ;
- PostgreSQL ;
- `pip`.

## Installation

Depuis le dossier qui contient `manage.py` :

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
```

Configurez ensuite la connexion PostgreSQL dans `blog_site/settings.py` avant de lancer les migrations.

## Lancer le projet

```powershell
python manage.py migrate
python manage.py runserver
```

Le serveur de développement est disponible à l’adresse <http://127.0.0.1:8000/>.
L’interface d’administration est disponible à l’adresse <http://127.0.0.1:8000/admin/>.

Pour créer un compte administrateur :

```powershell
python manage.py createsuperuser
```

## Tests

```powershell
python manage.py test
```

## Structure principale

```text
blog_site/
├── accounts/          # Application des comptes utilisateurs
├── blog/              # Application du blog
├── blog_site/         # Configuration du projet Django
├── manage.py
├── requirements.txt
└── README.md
```

## Développement

Les fichiers générés localement, les environnements virtuels et les informations sensibles ne doivent pas être versionnés. Si vous utilisez un fichier `.env` avec votre propre configuration, celui-ci est déjà exclu par `.gitignore`.
