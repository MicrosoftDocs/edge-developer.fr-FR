---
description: Extensions démarrées 1ère partie
title: Créez une extension simple qui s’affiche avec la NASA image du jour.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-chrome, développement Web, html, CSS, JavaScript, développeur, extensions
ms.openlocfilehash: 826401869b98d339e9b156a3727d94bd1182063d
ms.sourcegitcommit: d360e419b5f96f4f691cf7330b0d8dff9126f82e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015764"
---
# Créez une extension simple qui s’affiche avec la NASA image du jour. 
 
<!--  
[Completed Extension Package Source for This Part][ArchiveExtensionGettingStartedPart1]  
-->  

## Présentation  

Dans la première partie, l’objectif est de générer une extension de chrome de contour très simple à partir d’un répertoire vide.  L’objectif de cette extension consiste à effectuer les tâches suivantes.  

*   Créer des icônes pour l’extension pouvant être utilisées à plusieurs emplacements et de tailles différentes  
*   Créer un `manifest.json` fichier simple  
*   Afficher une icône de lancement qui, lorsqu’elle est sélectionnée, affiche une fenêtre contextuelle contenant l’image de NASA du jour.  

## Notions de base des fichiers manifeste  

Chaque package d’extension doit avoir un `manifest.json` fichier à la racine.  Vous devez considérer ceci comme le plan de l’extension.  Il indique au moteur du navigateur quelle version de l’API d’extension est attendue, le nom et la description de l’extension ainsi que de nombreuses autres informations, dont la plupart sont décrites dans le Guide de mise en route de l’extension multipoint.  

Voici un simple  `manifest.json`  

```json
{
    "name": "NASA Picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A Chromium Extension to show the NASA Picture of the Day."
}
```  

## Configuration des icônes d’extension  

Ensuite, ajoutez des icônes au `manifest.json` fichier \ (et créez un nouveau `/icons` répertoire avec les icônes fichiers \).  Les icônes sont utilisées pour l’image d’arrière-plan du bouton que l’utilisateur sélectionne pour lancer l’extension \ (le cas échéant) et d’autres emplacements appropriés.  

`PNG` est le format recommandé, mais vous pouvez également utiliser `BMP` , `GIF` `ICO` et `JPEG` .  Il est recommandé de toujours disposer d’au moins une icône de taille de 128x128 pixels et le navigateur le redimensionne automatiquement le cas échéant.  

Votre structure d’annuaire doit ressembler à ce qui suit.  

<!--  
:::image type="complex" source="./media/part1-heirarchy.png" alt-text="Directory Structure":::
   Directory Structure
:::image-end:::
-->  

<!--![Directory Structure][ImagePart1Heirarchy]  -->  

```shell
└── part1
    ├── _manifest.json
    └── icons
        ├── nasapod16x16.png
        ├── nasapod32x32.png
        ├── nasapod48x48.png
        └── nasapod128x128.png
```  

Le fichier mis à jour `manifest.json` doit apparaître comme suit.  

```json
{
    "name": "NASA Picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A chromium extension to show the NASA Picture of the Day.",
    "icons": {
        "16": "icons/nasapod16x16.png",
        "32": "icons/nasapod32x32.png",
        "48": "icons/nasapod48x48.png",
        "128": "icons/nasapod128x128.png"
    }
}
```  

> [!NOTE]
> Le fichier d’icônes `png` indiqué dans le code précédent est disponible dans le téléchargement zip mentionné en haut de cette page.  

## Ajout d’une boîte de dialogue contextuelle par défaut  

À présent, créez un `HTML` fichier qui s’exécute automatiquement lorsque l’utilisateur clique sur l’icône extension.  

:::image type="complex" source="./media/part1-badge1.png" alt-text="Icône de badge de barre d’outils":::
   Icône de badge de barre d’outils
:::image-end:::

<!--![Toolbar Badge Icon][ImagePart1Badge1]  -->  

Le fichier HTML est nommé `popup/popup.html` .  La sélection de l’icône de l’extension `popup/popup.html` s’exécute comme une boîte de dialogue modale qui s’affiche jusqu’à ce que vous ayez sélectionné hors de la boîte  

Pour cela, enregistrez le fichier comme fenêtre contextuelle par défaut dans le `manifest.json` `browser_action` code suivant.  

```json
{
    "name": "NASA Picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A chromium Extension to show the NASA Picture of the Day.",
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

Dans l' `popup` annuaire, ajoutez le fichier `popup.html` et demandez-lui de générer le rendu de l’image étoiles.  Voici le `popup.html` fichier.  

```html
<html lang="en">
    <head>
        <meta charset="UTF-8" />
        <title>NASA Picture of the Day</title>
    </head>
    <body>
        <div>
            <img src="/images/stars.jpeg" alt="stars" />
        </div>
    </body>
</html>
```  

 Ajoutez également un fichier image `images/stars.jpeg` référencé dans le `popup.html` fichier.  

La structure d’annuaire de l’exemple d’extension est affichée dans le schéma suivant.  

<!--  
:::image type="complex" source="./media/part1-heirarchy1.png" alt-text="Directory Structure for Extension":::
   Directory Structure for Extension
:::image-end:::
-->  

<!--![Directory Structure for Extension][ImagePart1Heirarchy1]  -->  

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

<!--  
> [!NOTE]
> The `images/stars.jpeg` file listed in the previous image is available in the [zip download][ArchiveExtensionGettingStartedPart1].  
-->  

C’est tout ce dont vous avez besoin pour créer une extension de travail.  Il ne reste plus qu’à le tester.  

La section suivante explique comment charger l’extension \ (parfois appelée chargement sur le côté \) dans le navigateur Microsoft Edge \ (chrome \) pour la tester.  

## Exécutez votre extension localement dans votre navigateur lors de la création de celle-ci.  

Le navigateur Microsoft Edge \ (chrome \) vous permet d’exécuter facilement et de déboguer vos extensions lors du développement.  

Le processus est relativement simple.  Vous devez d’abord sélectionner les points de suspension en haut de votre navigateur.  Sélectionnez ensuite `Extensions` dans le menu contextuel, comme illustré dans l’image suivante.  

:::image type="complex" source="./media/part1-threedots.png" alt-text="Choisir les extensions":::
   Choisir les extensions
:::image-end:::

<!--![Choose Extensions][ImagePart1Threedots]  -->  

Lorsque vous vous trouvez sur la page **Extensions** comme illustré dans l’image suivante, activez le **mode développeur** en activant le bouton bascule en bas à gauche de la page, comme illustré dans l’image suivante.  

:::image type="complex" source="./media/part1-developermode-toggle.png" alt-text="Activer le mode développeur":::
   Activer le mode développeur
:::image-end:::

<!--![Enable Developer Mode][ImagePart1DevelopermodeToggle]  -->  

## Installation et mise à jour des extensions installées hors Windows Store  

Lorsque vous voulez installer votre extension pour la première fois, vous devez choisir l' `Load Unpacked` option comme illustré dans l’image suivante.  Vous êtes invité à indiquer un répertoire dans lequel vous pouvez classer les ressources d’extension par fichier.  Cette opération installe l’extension comme si vous l’avez déjà téléchargée depuis le Windows Store.  

:::image type="complex" source="./media/part1-installed-extension.png" alt-text="Extensions installées":::
   Extensions installées
:::image-end:::

<!--![Installed Extensions][ImagePart1InstalledExtension]  -->  

Après avoir installé votre extension, vous pouvez la mettre à jour en sélectionnant le `Reload` bouton sous votre liste de extensions.  

Pour supprimer l’extension de votre navigateur, cliquez sur le `Remove` bouton situé en bas de la liste des extensions.  

## Extensions de débogage  

Le débogage d’extensions est relativement simple et prend en charge toutes les fonctionnalités dans DevTools de chrome.  Ces informations ne sont pas abordées dans ce guide de mise en route; il est toutefois essentiel de générer correctement les extensions.  

<!-- image links -->  

<!--[ImagePart1Heirarchy]: ./media/part1-heirarchy.png "Directory Structure"  -->  
<!--[ImagePart1Badge1]: ./media/part1-badge1.png "Toolbar Badge Icon"  -->  
<!--[ImagePart1Heirarchy1]: ./media/part1-heirarchy1.png "Directory Structure for Extension"  -->  
<!--[ImagePart1Threedots]: ./media/part1-threedots.png "Choose Extensions"  -->  
<!--[ImagePart1DevelopermodeToggle]: ./media/part1-developermode-toggle.png "Enable Developer Mode"  -->  
<!--[ImagePart1InstalledExtension]: ./media/part1-installed-extension.png "Installed Extensions"  -->  

<!-- links -->  

[ArchiveExtensionGettingStartedPart1]: ./extension-source/extension-getting-started-part1.zip "Source du package d’extension terminée pour cette partie | Documents Microsoft"  
