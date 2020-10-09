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
# <span data-ttu-id="85d23-104">Didacticiel créer une extension-partie 1</span><span class="sxs-lookup"><span data-stu-id="85d23-104">Create an extension tutorial - Part 1</span></span>  

## <span data-ttu-id="85d23-105">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="85d23-105">Overview</span></span>  

<span data-ttu-id="85d23-106">L’objectif de ce didacticiel consiste à créer une extension Microsoft Edge (chrome) à partir d’un répertoire vide.</span><span class="sxs-lookup"><span data-stu-id="85d23-106">The goal for this tutorial is to build a Microsoft Edge (Chromium) extension starting with an empty directory.</span></span> <span data-ttu-id="85d23-107">Nous allons générer une extension qui s’affiche avec la NASA image du jour.</span><span class="sxs-lookup"><span data-stu-id="85d23-107">We'll build an extension that pops up the NASA picture of the day.</span></span> <span data-ttu-id="85d23-108">Dans ce didacticiel, vous allez découvrir comment créer une extension en procédant comme suit:</span><span class="sxs-lookup"><span data-stu-id="85d23-108">In this tutorial, you'll learn how to create an extension by:</span></span>

*   <span data-ttu-id="85d23-109">Création d’un `manifest.json` fichier.</span><span class="sxs-lookup"><span data-stu-id="85d23-109">Creating a `manifest.json` file.</span></span>  
*   <span data-ttu-id="85d23-110">Ajouter des icônes.</span><span class="sxs-lookup"><span data-stu-id="85d23-110">Adding icons.</span></span>  
*   <span data-ttu-id="85d23-111">Ouverture d’une boîte de dialogue contextuelle par défaut.</span><span class="sxs-lookup"><span data-stu-id="85d23-111">Opening a default pop-up dialog.</span></span>  

## <span data-ttu-id="85d23-112">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="85d23-112">Before you Begin</span></span>

<span data-ttu-id="85d23-113">Si vous souhaitez tester l’extension complète que vous allez générer dans ce didacticiel, téléchargez le [code source][ArchiveExtensionGettingStartedPart1].</span><span class="sxs-lookup"><span data-stu-id="85d23-113">If you'd like to test out the completed extension that you'll build in this tutorial, download the [source code][ArchiveExtensionGettingStartedPart1].</span></span>  

## <span data-ttu-id="85d23-114">Étape 1: créer un `manifest.json` fichier</span><span class="sxs-lookup"><span data-stu-id="85d23-114">Step 1: Create a `manifest.json` file</span></span>

<span data-ttu-id="85d23-115">Chaque package d’extension doit avoir un `manifest.json` fichier à la racine.</span><span class="sxs-lookup"><span data-stu-id="85d23-115">Every extension package must have a `manifest.json` file at the root.</span></span>  <span data-ttu-id="85d23-116">Le manifeste fournit des détails sur votre extension, la version du package d’extension, le nom de l’extension et la description, etc.</span><span class="sxs-lookup"><span data-stu-id="85d23-116">The manifest provides details of your extension, the extension package version, the extension name and description, and so on.</span></span>  

<span data-ttu-id="85d23-117">L’extrait de code suivant présente les informations de base nécessaires dans votre `manifest.json` fichier.</span><span class="sxs-lookup"><span data-stu-id="85d23-117">The following code snippet outlines the basic information needed in your `manifest.json` file.</span></span>  

```json
{
    "name": "NASA picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A Chromium extension to display the NASA picture of the day."
}
```  

## <span data-ttu-id="85d23-118">Étape 2: ajouter des icônes</span><span class="sxs-lookup"><span data-stu-id="85d23-118">Step 2: Add icons</span></span>  

<span data-ttu-id="85d23-119">Commencez par créer le `icons` répertoire dans votre projet pour stocker les fichiers image d’icône.</span><span class="sxs-lookup"><span data-stu-id="85d23-119">Start by creating the `icons` directory in your project to store the icon image files.</span></span>  <span data-ttu-id="85d23-120">Les icônes sont utilisées pour l’image d’arrière-plan du bouton que les utilisateurs sélectionnent pour lancer l’extension.</span><span class="sxs-lookup"><span data-stu-id="85d23-120">The icons are used for the background image of the button that users select to launch the extension.</span></span>  

:::image type="complex" source="./media/part1-badge1.png" alt-text="Dans la barre d’outils pour ouvrir votre extension":::
   <span data-ttu-id="85d23-122">Dans la barre d’outils pour ouvrir votre extension</span><span class="sxs-lookup"><span data-stu-id="85d23-122">Icon on the toolbar to open your extension</span></span>
:::image-end:::

<span data-ttu-id="85d23-123">Pour les icônes, nous vous recommandons d’utiliser:</span><span class="sxs-lookup"><span data-stu-id="85d23-123">For icons, we recommend using:</span></span> 
*   `PNG` <span data-ttu-id="85d23-124">mettre en forme des icônes, mais vous pouvez également utiliser des `BMP` `GIF` `ICO` formats, ou `JPEG` .</span><span class="sxs-lookup"><span data-stu-id="85d23-124">format for icons, but you may also use `BMP`, `GIF`, `ICO` or `JPEG` formats.</span></span>  
*   <span data-ttu-id="85d23-125">Images de 128 x 128 PX, redimensionnées par le navigateur si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="85d23-125">Images that are 128 x 128 px, which are resized by the browser if necessary.</span></span>  

<span data-ttu-id="85d23-126">Les répertoires de votre projet doivent être similaires à la structure suivante.</span><span class="sxs-lookup"><span data-stu-id="85d23-126">The directories of your project should be similar to the following structure.</span></span>   

```shell
└── part1
    ├── _manifest.json
    └── icons
        ├── nasapod16x16.png
        ├── nasapod32x32.png
        ├── nasapod48x48.png
        └── nasapod128x128.png
```  

<span data-ttu-id="85d23-127">Ajoutez ensuite les icônes au `manifest.json` fichier.</span><span class="sxs-lookup"><span data-stu-id="85d23-127">Next, add the icons to the `manifest.json` file.</span></span> <span data-ttu-id="85d23-128">Mettez à jour votre `manifest.json` fichier à l’aide des informations d’icônes de sorte qu’il corresponde à l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="85d23-128">Update your `manifest.json` file with the icons information so that it matches the following code snippet.</span></span> <span data-ttu-id="85d23-129">Les `png` fichiers répertoriés dans le code suivant sont disponibles dans le fichier de téléchargement mentionné précédemment dans cet article.</span><span class="sxs-lookup"><span data-stu-id="85d23-129">The `png` files listed in the following code are available in the download file mentioned earlier in this article.</span></span>  

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

## <span data-ttu-id="85d23-130">Étape 3: ouvrir une boîte de dialogue contextuelle par défaut</span><span class="sxs-lookup"><span data-stu-id="85d23-130">Step 3: Open a default pop-up dialog</span></span>  

<span data-ttu-id="85d23-131">À présent, créez un `HTML` fichier qui s’exécute lorsque l’utilisateur lance votre extension.</span><span class="sxs-lookup"><span data-stu-id="85d23-131">Now, create a `HTML` file that's run when the user launches your extension.</span></span>  <span data-ttu-id="85d23-132">Créez le fichier HTML appelé `popup.html` dans un répertoire appelé `popup` .</span><span class="sxs-lookup"><span data-stu-id="85d23-132">Create the HTML file called `popup.html` in a directory called `popup`.</span></span>  <span data-ttu-id="85d23-133">Lorsque les utilisateurs sélectionnent l’icône pour lancer l’extension, `popup/popup.html` s’affichent sous forme de boîte de dialogue modale.</span><span class="sxs-lookup"><span data-stu-id="85d23-133">When users select the icon to launch the extension, `popup/popup.html` is displayed as a modal dialog.</span></span>  

<span data-ttu-id="85d23-134">Ajoutez le code de l’extrait de code suivant pour `popup.html` afficher l’image de l’étoile.</span><span class="sxs-lookup"><span data-stu-id="85d23-134">Add the code from the following code snippet to `popup.html` to display the stars image.</span></span>  

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

<span data-ttu-id="85d23-135">Assurez-vous d’ajouter le fichier image `images/stars.jpeg` au dossier images.</span><span class="sxs-lookup"><span data-stu-id="85d23-135">Ensure that you add the image file `images/stars.jpeg` to the images folder.</span></span>  <span data-ttu-id="85d23-136">Les répertoires de votre projet doivent être similaires à la structure suivante.</span><span class="sxs-lookup"><span data-stu-id="85d23-136">The directories of your project should be similar to the following structure.</span></span>   

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

<span data-ttu-id="85d23-137">Enfin, vérifiez que vous inscrivez la fenêtre contextuelle `manifest.json` sous `browser_action` , comme illustré dans l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="85d23-137">Finally, ensure you register the pop-up in `manifest.json` under `browser_action`, as shown in the following code snippet.</span></span>  

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

## <span data-ttu-id="85d23-138">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="85d23-138">Next steps</span></span>
<span data-ttu-id="85d23-139">C’est tout ce dont vous avez besoin pour développer une extension de travail.</span><span class="sxs-lookup"><span data-stu-id="85d23-139">That's everything you need to develop a working extension.</span></span> <span data-ttu-id="85d23-140">À présent, passez à charger et testez votre extension.</span><span class="sxs-lookup"><span data-stu-id="85d23-140">Now, continue on to sideload and test your extension.</span></span> <span data-ttu-id="85d23-141">Pour plus d’informations, voir [charger une extension][TestExtensionSideload].</span><span class="sxs-lookup"><span data-stu-id="85d23-141">For more information, see [Sideload an extension][TestExtensionSideload].</span></span>  


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
