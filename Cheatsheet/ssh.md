SSH - Cheatsheet
===============
<!-- meta ------------------------------------------------------------------------------

Description ==  Cheatsheet de l'outils SSH
Tags        ==  Cheatsheet Tool SSH Linux

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

## Installer le serveur
```sh
sudo dnf install openssh-server -y
```

## Activer le deamon
```sh
sudo systemctl enable --now sshd
sudo systemctl restart sshd
```

## Configuration 
*conseil : changer le port d'écoute et bloquer la connection par mot de passe.*

Chemin du fichier de configutaion :  
> /etc/ssh/ssd_config  

- ### Editer le comportement de SELinux pour le nouveau port :
    ```sh
    semanage port -a -t ssh_port_t -p tcp $PORT
    ```
- ### Ouvrir le port dans le pare-feu
    ```sh
    firewall-cmd --add-port=$PORT/tcp --permanent
    ```
- ### pour envoyer un cle publique depuis le client vers le serveur
    ```sh
    ssh-copy-id -i KEY_FILE  -p PORT USER@SERVER_ADRESS
    ```