```bash
# Lancement d'une machine virtuelle avec un fichier image disque
qemu-system-x86_64 -hda /path/to/disk.img

# Ajout d'un second disque
qemu-system-x86_64 -hda /path/to/disk1.img -hdb /path/to/disk2.img

# Modification de la taille de la mémoire vive de la machine virtuelle
qemu-system-x86_64 -m 2048

# Modification du nombre de coeurs de la machine virtuelle
qemu-system-x86_64 -smp 4

# Activation de l'accélération KVM (si disponible)
qemu-system-x86_64 -enable-kvm

# Redirection du port 22 de la machine virtuelle vers le port 2222 de l'hôte
qemu-system-x86_64 -redir :2222::22

# Redirection de l'audio de la machine virtuelle vers l'hôte
qemu-system-x86_64 -audiodev pa,id=sound0 -device ich9-intel-hda -device hda-output

# Lancement en mode graphique
qemu-system-x86_64 -vga qxl

# Montage d'un dossier hôte en tant que lecteur réseau dans la machine virtuelle
qemu-system-x86_64 -smb /path/to/host/folder

```