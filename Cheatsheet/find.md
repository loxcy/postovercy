Find - Cheatsheet
====
<!-- meta ------------------------------------------------------------------------------

Description ==  Cheatsheet des commandes de l'outils de recherchefind sous Linux
Tags        ==  Cheatsheet Tool Linux Find Recherche

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
La commande "find" est un outil puissant sur un système d'exploitation Linux qui permet de rechercher des fichiers ou des répertoires sur le système de fichiers.  
Elle est particulièrement utile lorsque vous avez besoin de trouver un fichier précis sur votre ordinateur, mais que vous ne connaissez pas son emplacement exact.

```bash
## Utilisation

## recherchera "monfichier.txt" dans le répertoire "/home/utilisateur" et ses sous-répertoires.
find /home/utilisateur -name monfichier.txt 

# Rechercher tous les fichiers du répertoire "/home/utilisateur" qui ont été modifiés il y a moins de 7 jours 
find /home/utilisateur -mtime -7

# Pour les répertoires de "/home/utilisateur" qui ont été modifiés il y a moins de 7 jours :
find /home/utilisateur -type d -mtime -7

# Tous les fichiers du répertoire "/home/utilisateur" qui ont un nom qui commence par "monfichier" :
find /home/utilisateur -name 'monfichier*'
```
