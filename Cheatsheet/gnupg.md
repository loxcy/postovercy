GnuPG - Cheatsheet
===============
<!-- meta ------------------------------------------------------------------------------

Description ==  Cheatsheet de l'outils GnuPG
Tags        ==  Cheatsheet Tool Linux GnuPG GPG PGP

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

## Commande de base
```bash

gpg --gen-key               ## crée une nouvelle paire de clés avec les parametre par defauts  
gpg --expert --full-gen-key ## crée une nouvelle paire de clés manuellement 
gpg --list-keys             ## liste les cles publiques  
gpg --list-secret-keys      ## liste les cles privées
```

## Gestion des cles
```bash
gpg --allow-secret-key-import --import "private_key.txt"           ## importe une cles privée  
gpg --import "publickey.txt"                                       ## importe une clé publique
gpg -ao privatekey.asc --export-secret-keys <$Nom_Ou_Adresse_Mail> ## Exporte la cle privée  
gpg -ao publickey.asc --export <$Nom_Ou_Adresse_Mail>              ## Exporte la cle publique 
gpg --delete-secret-key <$Nom_Ou_Adresse_Mail>                     ## Supprime la clé privée  
gpg --delete-key <$Nom_Ou_Adresse_Mail>                            ## Supprime la clé publique  
gpg -ao certificate.asc --gen-revoke <$Nom_Ou_Adresse_Mail>        ## revoque la clé  
```

## Envoyer un message
```bash
## Chiffre un message 
gpg -e -a -u "expediteur" -r "destinataire" --output msg_encrypted.txt msg.txt

    Options:
    -e : Encrypt
    -a : ASCII (!binaire)
    -u : Specifie la clé privée
    -r : Specifie la cle publique du destinataire.
    --output : Fichier de sortie, format par defaut .asc (ASCII) ou .gpg (binaire).
    

gpg -d msg.txt  ## dechiffre le message avec la cle par defaut
```