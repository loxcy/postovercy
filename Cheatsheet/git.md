Git - Cheatsheet
===============
<!-- meta ------------------------------------------------------------------------------

Description ==  Cheatsheet de l'outils Git pour Linux
Tags        ==  Cheatsheet Tool Git

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

## Commandes basiques
```bash

git init                ## Crée un nouveau repertoire git dans le dossier  
git add <$FICHIER>      ## Ajoute un fichier a la liste d'attente du prochain commit 
git add .               ## Ajoute le dossier complet a la liste d'attente du prochain commit
git add -A              ## Ajoute le dossier complet a la liste d'attente du prochain commit
git commit -m 'Comm'    ## commit les fichier changés et ajoute un commentaire 
git diff                ## Analyse la difference entre les anciens fichiers et ceux en liste d'attente
```

## Branche
```bash
git branch                  ## voir toute les branches locales  
git checkout -b <$BRANCHE>  ## crée une nouvelle branche et la verifie  
git branch -av              ## voir toute les branches locales et distantes  
git checkout <$BRANCHE>     ## Change de branches pour celle specifié  
git branch -d <$BRANCHE>    ## Supprime la branche spécifié  
git push origin <$BRANCHE>  ## Envoi un branche a un depot distant  
git merge <$BRANCHE>        ## merge la branche spécifié avec la branche active
```


## Cache
```bash
## Stocke les modifs dans .git pour masquer temporairement les éléments modifiés (exécuter `git add` avant)  
git stash

git stash apply ## Renvoie les éléments cachés
```


## Historique
```bash
git log                     ## Voir les commits précédents, les messages, et les ids  
git log <nom_du_fichier>    ## Voir qui a modifié un fichier  
git blame <nom_du_fichier>  ## Voir qui a changé un fichier
```

## Revenir en arriere
```bash
git reset --hard HEAD           ## Supprime tout les changements et reviens au precedent commit  
git checkout <nom_du_fichier>    ## Supprime les changements pour revenir a son état precedent
```

## Clonage
```bash
git clone <lien_de_repertoire_distant> ## Clone un repertoire distant 
```

## Rebase
```bash
git rebase main ## pour s'assurer que votre branche peut être fusionnée avec la branche main
```

## Config
```bash
git config --global user.name "prenom nom"`  
git config --global user.email adress@mail.com`  
git config --global user.signingkey <gpg-key-id>`
```

## Doownload single file from github
```bash
wget -L https://raw.githubusercontent.com/<owner-name>/<repo-name>/<branch>/<file>
```  