Venv - Cheatsheet
===============
<!-- meta ------------------------------------------------------------------------------

Description ==  Cheatsheet de l'outils Venv
Tags        ==  Cheatsheet Tool Venv Python 

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

La commande venv est utilisée pour créer un environnement virtuel Python. Un environnement virtuel Python est un répertoire qui contient une installation indépendante de Python, ainsi que tous les paquets Python qui sont installés dans cet environnement. L'utilisation d'environnements virtuels permet de séparer les dépendances de différents projets Python, ce qui peut être utile lorsque différents projets utilisent des versions différentes de paquets ou des paquets qui entrent en conflit.

Voici comment utiliser venv pour créer et utiliser un environnement virtuel :


```bash
## Créer un environnement virtuel 
python3 -m venv mon_environnement

## Activer l'environnement virtuel
source mon_environnement/bin/activate

## Désactiver l'environnement virtuel 
deactivate

## Installer des paquets Python dans l'environnement virtuel
pip install mon_paquet

##  désinstaller un module de votre environnement virtuel
pip uninstall nom_du_module

## afficher la liste des paquets installés dans l'environnement virtuel
pip freeze

## enregistrer dans un fichier requirements.txt la liste des paquets installés dans l'environnement virtuel 
pip freeze > requirements.txt

## Supprimer un environnement virtuel 
rm -r mon_environnement

```
