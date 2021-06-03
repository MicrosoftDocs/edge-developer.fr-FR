---
description: Créer une extension qui fait apparaître l’image DU JOUR
title: Créer un didacticiel d’extension - Partie 1
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge-chromium, développement web, html, css, javascript, développeur, extensions
ms.openlocfilehash: dfbe7893ce576c223d2b1d39ec21b6c5f46d8356
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397509"
---
# <a name="create-an-extension-tutorial---part-1"></a>Créer un didacticiel d’extension - Partie 1  

## <a name="overview"></a>Vue d'ensemble  

L’objectif de ce didacticiel est de créer une extension Microsoft Edge (Chromium) en commençant par un répertoire vide.  Vous construisez une extension qui fait apparaître l’image DU JOUR. Dans ce didacticiel, découvrez comment créer une extension en effectuant les actions suivantes.  

*   Création `manifest.json` d’un fichier.  
*   Ajout d’icônes.  
*   Ouverture d’une boîte de dialogue par défaut.  

## <a name="before-you-begin"></a>Avant de commencer

Pour tester l’extension terminée que vous construisez dans ce didacticiel, téléchargez le [code source.][ArchiveExtensionGettingStartedPart1]  

## <a name="step-1-create-a-manifestjson-file"></a>Étape 1 : Créer une manifest.jsfichier

Chaque package d’extension doit avoir `manifest.json` un fichier à la racine.  Le manifeste fournit des détails sur votre extension, la version du package d’extension, le nom et la description de l’extension, etc.  

L’extrait de code suivant décrit les informations de base nécessaires dans votre `manifest.json` fichier.  

```json
{
    "name": "NASA picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A Chromium extension to display the NASA picture of the day."
}
```  

## <a name="step-2-add-icons"></a>Étape 2 : Ajouter des icônes  

Commencez par créer le `icons` répertoire dans votre projet pour stocker les fichiers d’image d’icône.  Les icônes sont utilisées pour l’image d’arrière-plan du bouton que les utilisateurs sélectionnent pour lancer l’extension.  

:::image type="complex" source="./media/part1-badge1.png" alt-text="Icône de la barre d’outils pour ouvrir votre extension":::
   Icône de la barre d’outils pour ouvrir votre extension  
:::image-end:::  

Pour les icônes, nous vous recommandons d’utiliser : 
*   `PNG` pour les icônes, mais vous pouvez également utiliser `BMP` `GIF` , ou `ICO` `JPEG` formats.  
*   Images de 128 x 128 px, qui sont resa taille par le navigateur si nécessaire.  

Les répertoires de votre projet doivent être similaires à la structure suivante.   

```shell
└── part1
    ├── _manifest.json
    └── icons
        ├── nasapod16x16.png
        ├── nasapod32x32.png
        ├── nasapod48x48.png
        └── nasapod128x128.png
```  

Ensuite, ajoutez les icônes au `manifest.json` fichier. Mettez à jour votre fichier avec les informations des icônes afin qu’il corresponde à l’extrait de `manifest.json` code suivant. Les fichiers répertoriés dans le code suivant sont disponibles dans le fichier `png` de téléchargement mentionné plus haut dans cet article.  

```json
{
    "name": "NASA picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A chromium extension to show the NASA picture of the day.",
    "icons": {
        "16": "icons/nasapod16x16.png",
        "32": "icons/nasapod32x32.png",
        "48": "icons/nasapod48x48.png",
        "128": "icons/nasapod128x128.png"
    }
}
```  

## <a name="step-3-open-a-default-pop-up-dialog"></a>Étape 3 : Ouvrir une boîte de dialogue de fenêtre pop-up par défaut  

À présent, créez `HTML` un fichier à exécuter lorsque l’utilisateur lance votre extension.  Créez le fichier HTML nommé `popup.html` dans un répertoire nommé `popup` .  Lorsque les utilisateurs sélectionnent l’icône pour lancer l’extension, une boîte de dialogue `popup/popup.html` modale s’affiche.  

Ajoutez le code de l’extrait de code suivant pour `popup.html` afficher l’image des étoiles.  

```html
<html lang="en">
    <head>
        <meta charset="UTF-8" />
        <title>NASA picture of the day</title>
    </head>
    <body>
        <div>
            <img src="/images/stars.jpeg" alt="Display the stars image" />
        </div>
    </body>
</html>
```  

Veillez à ajouter le fichier image `images/stars.jpeg` au dossier images.  Les répertoires de votre projet doivent être similaires à la structure suivante.   

```shell
└── part1
    ├── _manifest.json
    ├── icons
    │   ├── nasapod16x16.png
    │   ├── nasapod32x32.png
    │   ├── nasapod48x48.png
    │   └── nasapod128x128.png
    ├── images
    │   └── stars.jpeg
    └── popup
        └── popup.html
```  

Enfin, assurez-vous d’inscrire la fenêtre pop-up sous , comme `manifest.json` `browser_action` illustré dans l’extrait de code suivant.  

```json
{
    "name": "NASA picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A chromium extension to display the NASA picture of the day.",
    "icons": {
        "16": "icons/nasapod16x16.png",
        "32": "icons/nasapod32x32.png",
        "48": "icons/nasapod48x48.png",
        "128": "icons/nasapod128x128.png"
    },
    "browser_action": {
        "default_popup": "popup/popup.html"
    }
}
```  

## <a name="next-steps"></a>Étapes suivantes
C’est tout ce dont vous avez besoin pour développer une extension de travail.  À présent, poursuivez le chargement de version test et testez votre extension. Pour plus d’informations, [accédez à Sideload an extension][TestExtensionSideload].  

<!-- image links -->  

<!--[ImagePart1Heirarchy]: ./media/part1-heirarchy.png "Directory Structure"  -->  
<!--[ImagePart1Badge1]: ./media/part1-badge1.png "Toolbar Badge Icon"  -->  
<!--[ImagePart1Heirarchy1]: ./media/part1-heirarchy1.png "Directory Structure for Extension"  -->  
<!--[ImagePart1Threedots]: ./media/part1-threedots.png "Choose Extensions"  -->  
<!--[ImagePart1DevelopermodeToggle]: ./media/part1-developermode-toggle.png "Enable Developer Mode"  -->  
<!--[ImagePart1InstalledExtension]: ./media/part1-installed-extension.png "Installed Extensions"  -->  

<!-- links -->  

[ArchiveExtensionGettingStartedPart1]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/extension-getting-started-part1/part1 "Source du package d’extension | Documents Microsoft"

[TestExtensionSideload]: ./extension-sideloading.md "Tester votre extension (chargement de version test) | Documents Microsoft"
