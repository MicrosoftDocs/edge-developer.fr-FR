---
description: Créez une extension qui s’affiche avec la NASA image du jour.
title: Didacticiel créer une extension-partie 1
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: Edge-chrome, développement Web, html, CSS, JavaScript, développeur, extensions
ms.openlocfilehash: 3809bfac714621cf97184127132487ed93958a2f
ms.sourcegitcommit: 845a0d53a86bee3678f421adee26b3372cefce57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104706"
---
# Didacticiel créer une extension-partie 1  

## Vue d'ensemble  

L’objectif de ce didacticiel consiste à créer une extension Microsoft Edge (chrome) à partir d’un répertoire vide. Nous allons générer une extension qui s’affiche avec la NASA image du jour. Dans ce didacticiel, vous allez découvrir comment créer une extension en procédant comme suit:

*   Création d’un `manifest.json` fichier.  
*   Ajouter des icônes.  
*   Ouverture d’une boîte de dialogue contextuelle par défaut.  

## Avant de commencer

Si vous souhaitez tester l’extension complète que vous allez générer dans ce didacticiel, téléchargez le [code source][ArchiveExtensionGettingStartedPart1].  

## Étape 1: créer un `manifest.json` fichier

Chaque package d’extension doit avoir un `manifest.json` fichier à la racine.  Le manifeste fournit des détails sur votre extension, la version du package d’extension, le nom de l’extension et la description, etc.  

L’extrait de code suivant présente les informations de base nécessaires dans votre `manifest.json` fichier.  

```json
{
    "name": "NASA picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A Chromium extension to display the NASA picture of the day."
}
```  

## Étape 2: ajouter des icônes  

Commencez par créer le `icons` répertoire dans votre projet pour stocker les fichiers image d’icône.  Les icônes sont utilisées pour l’image d’arrière-plan du bouton que les utilisateurs sélectionnent pour lancer l’extension.  

:::image type="complex" source="./media/part1-badge1.png" alt-text="Dans la barre d’outils pour ouvrir votre extension":::
   Dans la barre d’outils pour ouvrir votre extension
:::image-end:::

Pour les icônes, nous vous recommandons d’utiliser: 
*   `PNG` mettre en forme des icônes, mais vous pouvez également utiliser des `BMP` `GIF` `ICO` formats, ou `JPEG` .  
*   Images de 128 x 128 PX, redimensionnées par le navigateur si nécessaire.  

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

Ajoutez ensuite les icônes au `manifest.json` fichier. Mettez à jour votre `manifest.json` fichier à l’aide des informations d’icônes de sorte qu’il corresponde à l’extrait de code suivant. Les `png` fichiers répertoriés dans le code suivant sont disponibles dans le fichier de téléchargement mentionné précédemment dans cet article.  

```json
{
    &quot;name&quot;: &quot;NASA picture of the day viewer&quot;,
    &quot;version&quot;: &quot;0.0.0.1&quot;,
    &quot;manifest_version&quot;: 2,
    &quot;description&quot;: &quot;A chromium extension to show the NASA picture of the day.&quot;,
    &quot;icons&quot;: {
        &quot;16&quot;: &quot;icons/nasapod16x16.png&quot;,
        &quot;32&quot;: &quot;icons/nasapod32x32.png&quot;,
        &quot;48&quot;: &quot;icons/nasapod48x48.png&quot;,
        &quot;128&quot;: &quot;icons/nasapod128x128.png"
    }
}
```  

## Étape 3: ouvrir une boîte de dialogue contextuelle par défaut  

À présent, créez un `HTML` fichier qui s’exécute lorsque l’utilisateur lance votre extension.  Créez le fichier HTML appelé `popup.html` dans un répertoire appelé `popup` .  Lorsque les utilisateurs sélectionnent l’icône pour lancer l’extension, `popup/popup.html` s’affichent sous forme de boîte de dialogue modale.  

Ajoutez le code de l’extrait de code suivant pour `popup.html` afficher l’image de l’étoile.  

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

Assurez-vous d’ajouter le fichier image `images/stars.jpeg` au dossier images.  Les répertoires de votre projet doivent être similaires à la structure suivante.   

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

Enfin, vérifiez que vous inscrivez la fenêtre contextuelle `manifest.json` sous `browser_action` , comme illustré dans l’extrait de code suivant.  

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

## Étapes suivantes
C’est tout ce dont vous avez besoin pour développer une extension de travail. À présent, passez à charger et testez votre extension. Pour plus d’informations, voir [charger une extension][TestExtensionSideload].  


<!-- image links -->  

<!--[ImagePart1Heirarchy]: ./media/part1-heirarchy.png "Directory Structure"  -->  
<!--[ImagePart1Badge1]: ./media/part1-badge1.png "Toolbar Badge Icon"  -->  
<!--[ImagePart1Heirarchy1]: ./media/part1-heirarchy1.png "Directory Structure for Extension"  -->  
<!--[ImagePart1Threedots]: ./media/part1-threedots.png "Choose Extensions"  -->  
<!--[ImagePart1DevelopermodeToggle]: ./media/part1-developermode-toggle.png "Enable Developer Mode"  -->  
<!--[ImagePart1InstalledExtension]: ./media/part1-installed-extension.png "Installed Extensions"  -->  

<!-- links -->  

[ArchiveExtensionGettingStartedPart1]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/extension-getting-started-part1/part1 "Source du package d’extension terminée | Documents Microsoft"

[TestExtensionSideload]: ./extension-sideloading.md "Testez votre extension (chargement indépendant) | Documents Microsoft"
