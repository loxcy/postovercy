
- ### Script de dechiffrement de partition 
    Vous pouvez utiliser la commande cryptsetup pour déchiffrer la partition et la monter. Voici un exemple de script qui peut vous aider à démarrer :

    ```
    #!/bin/bash

    # Déchiffrement de la partition
    sudo cryptsetup luksOpen /dev/sda5 encrypted

    # Création du point de montage
    sudo mkdir /mnt/encrypted

    # Montage de la partition déchiffrée
    sudo mount /dev/mapper/encrypted /mnt/encrypted

    # Affichage du contenu du répertoire de montage
    ls /mnt/encrypted
    ```
    Ce script déchiffre la partition située sur /dev/sda5, la monte sur /mnt/encrypted et affiche le contenu du répertoire de montage. Vous pouvez adapter ce script à vos besoins en modifiant les chemins de la partition et du point de montage.

    Il est important de noter que vous devrez peut-être exécuter ce script en tant qu'utilisateur root ou en utilisant sudo. Assurez-vous également d'avoir installé le paquet cryptsetup avant de l'exécuter.

- ### Cheatsheet dnf

    ```
            # Mise à jour de la base de données des paquets disponibles
        dnf update

        # Mise à jour de tous les paquets installés
        dnf upgrade

        # Recherche de paquets
        dnf search <nom du paquet>

        # Installation d'un paquet
        dnf install <nom du paquet>

        # Installation de plusieurs paquets en même temps
        dnf install <nom du paquet 1> <nom du paquet 2> <nom du paquet 3>

        # Mise à jour d'un paquet
        dnf update <nom du paquet>

        # Mise à jour de plusieurs paquets en même temps
        dnf update <nom du paquet 1> <nom du paquet 2> <nom du paquet 3>

        # Suppression d'un paquet
        dnf remove <nom du paquet>

        # Suppression de plusieurs paquets en même temps
        dnf remove <nom du paquet 1> <nom du paquet 2> <nom du paquet 3>

        # Réinstallation d'un paquet
        dnf reinstall <nom du paquet>

        # Réinstallation de plusieurs paquets en même temps
        dnf reinstall <nom du paquet 1> <nom du paquet 2> <nom du paquet 3>

        # Afficher les informations sur un paquet
        dnf info <nom du paquet>

        # Afficher la liste des paquets installés
        dnf list installed

        # Afficher la liste des paquets disponibles
        dnf list available

        # Nettoyage des fichiers inutiles
        dnf clean all

        # Mise à jour de la base de données des paquets pour une version spécifique de votre distribution
                dnf update --releasever=<numéro de version>
                dnf update --releasever=27
    ```

