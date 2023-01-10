Django
======
<!-- meta ------------------------------------------------------------------------------

Description ==  Cheatsheet du framework django
Tags        ==  Cheatsheet Tool Django Python

Post_Type   ==  Cheatsheet
Preview     ==  cli
Author      ==  Loxcy

Version     == 0.1
Featured    == True
Visible     == False
Draft       == True

created_at  == 2022-01-10 00:00:00
published_at== 2022-01-10 00:00:00
updated_at   == 2022-01-10 00:00:00


---------------------------------------------------------------------------- endmeta -->


## Comandes : 

### Commandes de base
```bash
pip install django              ### Installation
python manage.py help           ### Afficher la liste des commandes disponibles
python manage.py customcommand  ### Exécution de commandes personnalisées
```

### Les plus Fréquentes
```bash
python manage.py runserver  ### Démarrer le serveur de développement

### Préparer et mettre a jour la DB
python manage.py makemigrations && python manage.py migrate  
```

### Base de donnée
```bash

python manage.py makemigrations       ### Préparer les migrations
python manage.py migrate              ### Intégrer les migrations a la DB
python manage.py show_models          ### Afficher la liste des modèles disponibles dans l'application
python manage.py dumpdata > data.json ### Dump de la DB dans un fichier JSON
python manage.py loaddata data.json   ### Chargement des données depuis un fichier JSON
python manage.py flush                ### Vider la base de données
python manage.py reset_db             ### Vider la base de données et relancer les migrations
```

### Création de projet
```bash
django-admin startproject $MON_PROJET   ### Création de projet
python manage.py startapp $MY_APP       ### Création d'une application
python manage.py createsuperuser        ### Création du super utilisateur
```

### Tests
```bash
python manage.py test     # Exécution des tests unitaires
```

### Gestion des utilisateurs
```bash
python manage.py changepassword $USERNAME  ### Changer le mot de passe de l'utilisateur spécifié
python manage.py createsuperuser           ### Créer un super utilisateur
```

### Gestion des fichiers statiques
```bash
python manage.py collectstatic             ### Copier les fichiers statiques dans le répertoire de déploiement
```

### Gestion des traductions
```bash
python manage.py makemessages              ### Créer les fichiers de traduction
python manage.py compilemessages           ### Compiler les fichiers de traduction
```

### Gestion des logs
```bash
python manage.py runprofileserver          ### Exécuter le serveur de profilage avec le niveau de log "profiling"
python manage.py runserverlog              ### Exécuter le serveur avec la journalisation activée
```

### Gestion de l'environnement de développement
```bash
python manage.py runserver --insecure      ### Exécuter le serveur de développement avec l'option --insecure
python manage.py runserver --nothreading   ### Exécuter le serveur de développement sans utiliser de threads
python manage.py runserver --noreload      ### Exécuter le serveur de développement sans la fonctionnalité de recharge automatique
```

### Gestion des modèles
```bash
python manage.py makemigrations --empty    ### Créer une migration vide
python manage.py sqlmigrate $APP_NAME $MIGRATION_NAME  ### Afficher la requête SQL correspondant à une migration spécifique
```

### Gestion des scripts personnalisés
```bash
python manage.py shell_plus ### Exécuter une console interactive avec l'extension django-extensions "shell_plus"
python manage.py runscript $SCRIPT_NAME ### Exécuter un script personnalisé
```

### Gestion de la documentation
```bash
python manage.py build_sphinx   ### Générer la documentation avec Sphinx
```

### Gestion de la sécurité
```bash
python manage.py checksecurity  ### Vérifier les problèmes de sécurité potentiels dans le projet
```

### Gestion des performances
```bash
python manage.py benchmark   ### Exécuter un benchmark du projet
python manage.py querycounts ### Afficher le nombre de requêtes effectuées par vue
```

### Gestion des formulaires
```bash
python manage.py form_wizard    ### Générer un formulaire étape par étape à partir d'un modèle
```

### Gestion des sessions
```bash
python manage.py clearsessions  ### Supprimer toutes les sessions
```

## Datatype
- CharField
    - max_length: la longueur maximale du champ (requis)
    - unique: booléen indiquant si le champ doit être unique
    - blank: booléen indiquant si le champ peut être vide
    - null: booléen indiquant si le champ peut être null
- TextField
    - blank: booléen indiquant si le champ peut être vide
    - null: booléen indiquant si le champ peut être null
- IntegerField
    - blank: booléen indiquant si le champ peut être vide
    - null: booléen indiquant si le champ peut être null
    - unique: booléen indiquant si le champ doit être unique
- DateField
    - auto_now: booléen indiquant si la date doit être mise à jour automatiquement à chaque enregistrement
    - auto_now_add: booléen indiquant si la date doit être enregistrée automatiquement lors de la création de l'objet
- TimeField
    - auto_now: booléen indiquant si l'heure doit être mise à jour automatiquement à chaque enregistrement
    - auto_now_add: booléen indiquant si l'heure doit être enregistrée automatiquement lors de la création de l'objet
- DateTimeField
    - auto_now: booléen indiquant si la date et l'heure doivent être mises à jour automatiquement à chaque enregistrement
    - auto_now_add: booléen indiquant si la date et l'heure doivent être enregistrées automatiquement lors de la création de l'objet
- DecimalField
    - max_digits: le nombre maximum de chiffres (requis)
    - decimal_places: le nombre de chiffres après la virgule (requis)
- EmailField
    - max_length: la longueur maximale du champ (requis)
    - unique: booléen indiquant si le champ doit être unique
    - blank: booléen indiquant si le champ peut être vide
    - null: booléen indiquant si le champ peut être null
- URLField
    - max_length: la longueur maximale du champ (requis)
    - unique: booléen indiquant si le champ doit être unique
    - blank: booléen indiquant si le champ peut être vide
    - null: booléen indiquant si le champ peut être null
- BooleanField
- NullBooleanField
- FileField
    - upload_to: le dossier où le fichier doit être enregistré
    - max_length: la longueur maximale du champ (requis)
    - unique: booléen indiquant si le champ doit être unique
    - blank: booléen indiquant si le champ peut être vide
    - null: booléen indiquant si le champ peut être null
- ImageField
    - upload_to: le dossier où l'image doit être enregistrée
    - max_length: la longueur maximale du champ (requis)
    - unique: booléen indiquant si le champ doit être unique
    - blank: booléen indiquant si le champ peut être vide
    - null: booléen indiquant si le champ peut être null
- ForeignKey
    - on_delete: la stratégie à utiliser lorsqu'un objet lié est supprimé (requis)
    - related_name: le nom de l'attribut inverse de la relation
    - related_query_name: le nom de l'attribut utilisé pour les requêtes inverse
    - to_field: le nom du champ de la classe cible à utiliser comme clé étrangère
- ManyToManyField
    - related_name: le nom de l'attribut inverse de la relation
    - related_query_name: le nom de l'attribut utilisé pour les requêtes inverse
    - through: le nom de la classe intermédiaire à utiliser pour créer un "through model"
    - through_fields: les noms des champs à utiliser dans la classe intermédiaire
    - symmetrical: booléen indiquant si la relation est symétrique (par défaut, True)
- OneToOneField
    - on_delete: la stratégie à utiliser lorsqu'un objet lié est supprimé (requis)
    - related_name: le nom de l'attribut inverse de la relation
    - related_query_name: le nom de l'attribut utilisé pour les requêtes inverse
    - to_field: le nom du champ de la classe cible à utiliser comme clé étrangère

## Fichier admin.py
```python
from django.contrib import admin
from .models import MonModel

# Enregistrement du modèle MonModel auprès de l'administration
admin.site.register(MonModel)

# Définition d'une classe MonModelAdmin héritant de ModelAdmin
class MonModelAdmin(admin.ModelAdmin):
    # Liste des champs à afficher dans la liste des objets
    list_display = ['champ_1', 'champ_2', 'champ_3']
    # Ajout d'un champ de recherche
    search_fields = ['champ_1', 'champ_2']
    # Ajout de filtres sur la liste des objets
    list_filter = ['champ_2']
    # Ajout d'un champ de tri sur la liste des objets
    ordering = ['champ_3']

# Enregistrement de MonModelAdmin auprès de l'administration
admin.site.register(MonModel, MonModelAdmin)

```

## Fichier views.py
```python
      from django.shortcuts import render
      from .models import MonModel

      # Vue gérant la liste des objets de MonModel
      def liste(request):
            # Récupération de tous les objets de MonModel
            objets = MonModel.objects.all()
            # Envoi de la liste des objets au template
            return render(request, 'ma_template.html', {'objets': objets})

      # Vue gérant la création d'un objet de MonModel
      def creation(request):
            # Si la méthode utilisée par la requête est POST
            if request.method == 'POST':
                  # Création d'un formulaire lié à la requête
                  form = MonModelForm(request.POST)
                  # Si le formulaire est valide
                  if form.is_valid():
                        # Enregistrement de l'objet en base de données
                        form.save()
                        # Redirection vers la liste des objets
                        return redirect('liste')
            # Si la méthode utilisée par la requête n'est pas POST ou que le formulaire est invalid
            else:
                  # Création d'un formulaire vide
                  form = MonModelForm()
            # Envoi du formulaire au template
            return render(request, 'ma_template.html', {'form': form})

      # Vue gérant la modification d'un objet de MonModel
      def modification(request, pk):
            # Récupération de l'objet à modifier
            objet = get_object_or_404(MonModel, pk=pk)
            # Si la méthode utilisée par la requête est POST
            if request.method == 'POST':
                  # Création d'un formulaire lié à la requête et à l'objet
                  form = MonModelForm(request.POST, instance=objet)
                  # Si le formulaire est valide
                  if form.is_valid():
                        # Enregistrement de l'objet en base de données
                        form.save()
                        # Redirection vers la liste des objets
                        return redirect('liste')
            # Si la méthode utilisée par la requête n'est pas POST ou que le formulaire est invalid
            else:
                  # Création d'un formulaire lié à l'objet
                  form = MonModelForm(instance=objet)
            # Envoi du formulaire au template
            return render(request, 'ma_template.html', {'form': form})

      # Vue gérant la suppression d'un objet de MonModel
      def suppression(request, pk):
            # Récupération de l'objet à supprimer
            objet = get_object_or_404(MonModel, pk=pk)
            # Si la méthode utilisée par la requête est POST
            if request.method == 'POST':
                  # Suppression de l'objet en base de données
                  objet.delete()
                  # Redirection vers la liste des objets
                  return redirect('liste')
            # Envoi de l'objet au template
            return render(request, 'ma_template.html', {'objet': objet})


```
## Fichier urls.py
```python
      from django.urls import path
      from . import views

      # Définition de l'URL de la liste des objets de MonModel
      urlpatterns = [
            path('liste/', views.liste, name='liste'),
      ]

      # Définition de l'URL de la création d'un objet de MonModel
      urlpatterns += [
            path('creation/', views.creation, name='creation'),
      ]

      # Définition de l'URL de la modification d'un objet de MonModel
      urlpatterns += [
            path('modification/<int:pk>/', views.modification, name='modification'),
      ]

      # Définition de l'URL de la suppression d'un objet de MonModel
      urlpatterns += [
            path('suppression/<int:pk>/', views.suppression, name='suppression'),
      ]

```
## Fichier models.py
```python
      from django.db import models
      from django.utils import timezone

      # Définition d'un modèle MonModel
      class MonModel(models.Model):
            # Champ de type caractères de longueur maximale 100
            champ_1 = models.CharField(max_length=100)
            # Champ de type texte
            champ_2 = models.TextField()
            # Champ de type entier
            champ_3 = models.IntegerField()
            # Champ de type date
            champ_4 = models.DateField(default=timezone.now)
            # Champ de type heure
            champ_5 = models.TimeField(blank=True, null=True)
            # Champ de type date et heure
            champ_6 = models.DateTimeField(default=timezone.now)
            # Champ de type décimal
            champ_7 = models.DecimalField(max_digits=5, decimal_places=2)
            # Champ de type email
            champ_8 = models.EmailField(max_length=254)
            # Champ de type URL
            champ_9 = models.URLField(max_length=200)
            # Champ de type booléen
            champ_10 = models.BooleanField(default=False)
            # Champ de type booléen acceptant null
            champ_11 = models.NullBooleanField()
            # Champ de type fichier
            champ_12 = models.FileField(upload_to='documents/')
            # Champ de type image
            champ_13 = models.ImageField(upload_to='images/')
            # Champ de type clé étrangère
            champ_14 = models.ForeignKey(MonModel, on_delete=models.CASCADE)
            # Champ de type de n-n
            champ_15 = models.ManyToManyField(MonModel)
            # Champ de type 1-1
            champ_16 = models.OneToOneField(MonModel, on_delete=models.CASCADE)

            # Méthode retournant une chaîne représentant l'objet
            def __str__(self):
                  return self.champ_1

```
## Fichier settings.py
```python
      # Configuration de la base de données
      DATABASES = {
            'default': {
                  'ENGINE': 'django.db.backends.mysql',
                  'NAME': 'mon_bd',
                  'USER': 'mon_user',
                  'PASSWORD': 'mon_mdp',
                  'HOST': 'localhost',
                  'PORT': '',
            }
      }

      # Configuration de la langue et de la zone géographique
      LANGUAGE_CODE = 'fr-FR'
      TIME_ZONE = 'Europe/Paris'

      # Configuration de l'URL de l'application
      ROOT_URLCONF = 'mon_projet.urls'

      # Configuration de la gestion des fichiers statiques
      STATIC_URL = '/static/'
      STATICFILES_DIRS = [BASE_DIR / "static"]
      STATIC_ROOT = BASE_DIR / "static_root"

      # Configuration de la gestion des messages
      MESSAGE_STORAGE = 'django.contrib.messages.storage.session.SessionStorage'

      # Configuration de l'authentification
      AUTH_USER_MODEL = 'mon_app.MonUser'

      # Configuration de la gestion des traductions
      LOCALE_PATHS = [BASE_DIR / "locale"]

      # Configuration de la gestion du cache
      CACHES = {
            'default': {
                  'BACKEND': 'django.core.cache.backends.db.DatabaseCache',
                  'LOCATION': 'cache_table',
            }
      }

      # Configuration des middlewares
      MIDDLEWARE = [
            'django.middleware.security.SecurityMiddleware',
            'django.contrib.sessions.middleware.SessionMiddleware',
            'django.middleware.locale.LocaleMiddleware',
            'django.middleware.common.CommonMiddleware',
            'django.middleware.csrf.CsrfViewMiddleware',
            'django.contrib.auth.middleware.AuthenticationMiddleware',
            'django.contrib.messages.middleware.MessageMiddleware',
            'django.middleware.clickjacking.XFrameOptionsMiddleware',
      ]

      # Configuration des applications installées
      INSTALLED_APPS = [
            'django.contrib.admin',
            'django.contrib.auth',
            'django.contrib.contenttypes',
            'django.contrib.sessions',
            'django.contrib.messages',
            'django.contrib.staticfiles',
            'mon_app',
      ]


```
##  syntaxe spécifique de Django pour les fichiers du frontend 
```python
      {% comment %} Un commentaire {% endcomment %}
      {% if condition %} Affichage si vrai {% endif %}
      {% if condition %} Affichage si vrai {% else %} Affichage si faux {% endif %}
      {% for objet in objets %} Affichage pour chaque objet {% endfor %}
      {% with variable=value %} Affectation de la valeur {% endwith %}
      {% load mon_module %} Chargement d'un module de template
      {% include "mon_template.html" %} Inclusion d'un template
      {% extends "mon_template.html" %} Héritage d'un template
      {% block nom_block %} Contenu du block {% endblock %}
      {% csrf_token %} Token CSRF
      {{ variable }} Affichage de la valeur de la variable
      {{ variable|mon_filtre }} Affichage de la valeur de la variable filtrée par mon_filtre
      {% url 'nom_url' objet.id %} Génération de l'URL associée au nom
      {% static 'chemin/fichier.ext' %} Génération de l'URL du fichier statique


```
## syntaxe spécifique de Django pour les fichiers du backend
```python
      # Récupération de tous les objets de MonModel
      objets = MonModel.objects.all()

      # Récupération d'un objet de MonModel avec la clé primaire pk
      objet = MonModel.objects.get(pk=pk)

      # Récupération du premier objet de MonModel avec champ_1='valeur'
      objet = MonModel.objects.filter(champ_1='valeur').first()

      # Création et enregistrement d'un objet de MonModel avec champ_1='valeur'
      objet = MonModel.objects.create(champ_1='valeur')

      # Modification de l'objet de MonModel avec la nouvelle valeur 'nouvelle_valeur' pour le champ champ_1
      objet.champ_1 = 'nouvelle_valeur'

      # Enregistrement des modifications apportées à l'objet de MonModel
      objet.save()
      # Suppression de l'objet de MonModel
      objet.delete()

      # Création d'un formulaire lié à la requête et à l'objet de MonModel
      MonModelForm(request.POST, instance=objet)

      # Vérification de la validité du formulaire
      form.is_valid()

      # Enregistrement d'un objet en base de données via le formulaire
      form.save()

      # Redirection vers l'URL associée au nom avec l'ID de l'objet en argument
      redirect('nom_url', objet.id)
      
      # Génération de l'URL associée au nom avec l'ID de l'objet en argument
      reverse('nom_url', args=[objet.id])


```
## Fichier .py
```python

```
