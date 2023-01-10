Gnome-Screenshot - Cheatsheet
===============
<!-- meta ------------------------------------------------------------------------------

Description ==  Cheatsheet de l'outils de capture de Gnome
Tags        ==  Cheatsheet Tool Gnome Capture Screenshot

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

# Tutoriel complet sur gnome-screenshot

Gnome-screenshot est un outil de capture d'écran intégré à GNOME, l'environnement de bureau populaire pour Linux. Voici comment utiliser ses principales fonctionnalités :

## Prise de capture d'écran complète

Pour prendre une capture d'écran de l'ensemble de votre écran, ouvrez le terminal et utilisez la commande suivante :

```
gnome-screenshot
```

Vous pouvez également utiliser le raccourci clavier `Impression écran` (généralement situé en haut à droite de votre clavier) pour prendre une capture d'écran complète.

## Prise de capture d'écran d'une fenêtre

Pour prendre une capture d'écran d'une fenêtre spécifique, utilisez la commande suivante :

```
gnome-screenshot -w
```

Lorsque vous exécutez cette commande, votre curseur se transformera en une croix. Cliquez sur la fenêtre que vous souhaitez capturer pour prendre une capture d'écran.

## Prise de capture d'écran d'une zone spécifique

Pour prendre une capture d'écran d'une zone spécifique de votre écran, utilisez la commande suivante :

```
gnome-screenshot -a
```

Lorsque vous exécutez cette commande, votre curseur se transformera en une croix. Cliquez et faites glisser pour sélectionner la zone que vous souhaitez capturer. Relâchez pour prendre la capture d'écran.

## Enregistrement de la capture d'écran dans un fichier

Par défaut, les captures d'écran prises avec gnome-screenshot sont enregistrées dans votre répertoire personnel sous le nom `Screenshot.png`. Vous pouvez utiliser l'option `-f` pour spécifier un nom de fichier personnalisé :

```
gnome-screenshot -f mon-fichier.png
```

Vous pouvez également utiliser l'option `-d` pour définir un délai avant de prendre la capture d'écran :

```
gnome-screenshot -d 10 -f mon-fichier.png
```

Cela vous donne 10 secondes pour ouvrir les fenêtres ou les menus que vous souhaitez capturer avant que la capture d'écran soit prise.

## Autres option
    -b : permet de ne pas inclure la barre de défilement dans la capture d'écran.
    -i : active l'indicateur de sélection (une bordure rouge) pour indiquer la zone sélectionnée lors de la capture d'écran d'une fenêtre ou d'une zone spécifique.
    --display=DISPLAY : permet de spécifier l'affichage à utiliser lors de la capture d'écran.
    --include-pointer : inclut le pointeur de souris dans la capture d'écran.
    --border-effect=EFFECT : ajoute un effet de bordure autour de la capture d'écran.
    --frame : ajoute une bordure autour de la capture d'écran.
    --keep-aspect-ratio : conserve le ratio d'aspect lors de la sélection d'une zone pour la capture d'écran.
    --remove-border : enlève la bordure autour de la fenêtre lors de la capture d'écran d'une fenêtre spécifique.
