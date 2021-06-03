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
# <a name="create-an-extension-tutorial---part-1"></a><span data-ttu-id="461f2-104">Créer un didacticiel d’extension - Partie 1</span><span class="sxs-lookup"><span data-stu-id="461f2-104">Create an extension tutorial - Part 1</span></span>  

## <a name="overview"></a><span data-ttu-id="461f2-105">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="461f2-105">Overview</span></span>  

<span data-ttu-id="461f2-106">L’objectif de ce didacticiel est de créer une extension Microsoft Edge (Chromium) en commençant par un répertoire vide.</span><span class="sxs-lookup"><span data-stu-id="461f2-106">The goal for this tutorial is to build a Microsoft Edge (Chromium) extension starting with an empty directory.</span></span>  <span data-ttu-id="461f2-107">Vous construisez une extension qui fait apparaître l’image DU JOUR.</span><span class="sxs-lookup"><span data-stu-id="461f2-107">You are building an extension that pops up the NASA picture of the day.</span></span> <span data-ttu-id="461f2-108">Dans ce didacticiel, découvrez comment créer une extension en effectuant les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="461f2-108">In this tutorial, learn how to create an extension by completing the following actions.</span></span>  

*   <span data-ttu-id="461f2-109">Création `manifest.json` d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="461f2-109">Creating a `manifest.json` file.</span></span>  
*   <span data-ttu-id="461f2-110">Ajout d’icônes.</span><span class="sxs-lookup"><span data-stu-id="461f2-110">Adding icons.</span></span>  
*   <span data-ttu-id="461f2-111">Ouverture d’une boîte de dialogue par défaut.</span><span class="sxs-lookup"><span data-stu-id="461f2-111">Opening a default pop-up dialog.</span></span>  

## <a name="before-you-begin"></a><span data-ttu-id="461f2-112">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="461f2-112">Before you Begin</span></span>

<span data-ttu-id="461f2-113">Pour tester l’extension terminée que vous construisez dans ce didacticiel, téléchargez le [code source.][ArchiveExtensionGettingStartedPart1]</span><span class="sxs-lookup"><span data-stu-id="461f2-113">To test out the completed extension that you are building in this tutorial, download the [source code][ArchiveExtensionGettingStartedPart1].</span></span>  

## <a name="step-1-create-a-manifestjson-file"></a><span data-ttu-id="461f2-114">Étape 1 : Créer une manifest.jsfichier</span><span class="sxs-lookup"><span data-stu-id="461f2-114">Step 1: Create a manifest.json file</span></span>

<span data-ttu-id="461f2-115">Chaque package d’extension doit avoir `manifest.json` un fichier à la racine.</span><span class="sxs-lookup"><span data-stu-id="461f2-115">Every extension package must have a `manifest.json` file at the root.</span></span>  <span data-ttu-id="461f2-116">Le manifeste fournit des détails sur votre extension, la version du package d’extension, le nom et la description de l’extension, etc.</span><span class="sxs-lookup"><span data-stu-id="461f2-116">The manifest provides details of your extension, the extension package version, the extension name and description, and so on.</span></span>  

<span data-ttu-id="461f2-117">L’extrait de code suivant décrit les informations de base nécessaires dans votre `manifest.json` fichier.</span><span class="sxs-lookup"><span data-stu-id="461f2-117">The following code snippet outlines the basic information needed in your `manifest.json` file.</span></span>  

```json
{
    "name": "NASA picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A Chromium extension to display the NASA picture of the day."
}
```  

## <a name="step-2-add-icons"></a><span data-ttu-id="461f2-118">Étape 2 : Ajouter des icônes</span><span class="sxs-lookup"><span data-stu-id="461f2-118">Step 2: Add icons</span></span>  

<span data-ttu-id="461f2-119">Commencez par créer le `icons` répertoire dans votre projet pour stocker les fichiers d’image d’icône.</span><span class="sxs-lookup"><span data-stu-id="461f2-119">Start by creating the `icons` directory in your project to store the icon image files.</span></span>  <span data-ttu-id="461f2-120">Les icônes sont utilisées pour l’image d’arrière-plan du bouton que les utilisateurs sélectionnent pour lancer l’extension.</span><span class="sxs-lookup"><span data-stu-id="461f2-120">The icons are used for the background image of the button that users select to launch the extension.</span></span>  

:::image type="complex" source="./media/part1-badge1.png" alt-text="Icône de la barre d’outils pour ouvrir votre extension":::
   <span data-ttu-id="461f2-122">Icône de la barre d’outils pour ouvrir votre extension</span><span class="sxs-lookup"><span data-stu-id="461f2-122">Icon on the toolbar to open your extension</span></span>  
:::image-end:::  

<span data-ttu-id="461f2-123">Pour les icônes, nous vous recommandons d’utiliser :</span><span class="sxs-lookup"><span data-stu-id="461f2-123">For icons, we recommend using:</span></span> 
*   `PNG` <span data-ttu-id="461f2-124">pour les icônes, mais vous pouvez également utiliser `BMP` `GIF` , ou `ICO` `JPEG` formats.</span><span class="sxs-lookup"><span data-stu-id="461f2-124">format for icons, but you may also use `BMP`, `GIF`, `ICO` or `JPEG` formats.</span></span>  
*   <span data-ttu-id="461f2-125">Images de 128 x 128 px, qui sont resa taille par le navigateur si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="461f2-125">Images that are 128 x 128 px, which are resized by the browser if necessary.</span></span>  

<span data-ttu-id="461f2-126">Les répertoires de votre projet doivent être similaires à la structure suivante.</span><span class="sxs-lookup"><span data-stu-id="461f2-126">The directories of your project should be similar to the following structure.</span></span>   

```shell
└── part1
    ├── _manifest.json
    └── icons
        ├── nasapod16x16.png
        ├── nasapod32x32.png
        ├── nasapod48x48.png
        └── nasapod128x128.png
```  

<span data-ttu-id="461f2-127">Ensuite, ajoutez les icônes au `manifest.json` fichier.</span><span class="sxs-lookup"><span data-stu-id="461f2-127">Next, add the icons to the `manifest.json` file.</span></span> <span data-ttu-id="461f2-128">Mettez à jour votre fichier avec les informations des icônes afin qu’il corresponde à l’extrait de `manifest.json` code suivant.</span><span class="sxs-lookup"><span data-stu-id="461f2-128">Update your `manifest.json` file with the icons information so that it matches the following code snippet.</span></span> <span data-ttu-id="461f2-129">Les fichiers répertoriés dans le code suivant sont disponibles dans le fichier `png` de téléchargement mentionné plus haut dans cet article.</span><span class="sxs-lookup"><span data-stu-id="461f2-129">The `png` files listed in the following code are available in the download file mentioned earlier in this article.</span></span>  

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

## <a name="step-3-open-a-default-pop-up-dialog"></a><span data-ttu-id="461f2-130">Étape 3 : Ouvrir une boîte de dialogue de fenêtre pop-up par défaut</span><span class="sxs-lookup"><span data-stu-id="461f2-130">Step 3: Open a default pop-up dialog</span></span>  

<span data-ttu-id="461f2-131">À présent, créez `HTML` un fichier à exécuter lorsque l’utilisateur lance votre extension.</span><span class="sxs-lookup"><span data-stu-id="461f2-131">Now, create a `HTML` file to run when the user launches your extension.</span></span>  <span data-ttu-id="461f2-132">Créez le fichier HTML nommé `popup.html` dans un répertoire nommé `popup` .</span><span class="sxs-lookup"><span data-stu-id="461f2-132">Create the HTML file named `popup.html` in a directory named `popup`.</span></span>  <span data-ttu-id="461f2-133">Lorsque les utilisateurs sélectionnent l’icône pour lancer l’extension, une boîte de dialogue `popup/popup.html` modale s’affiche.</span><span class="sxs-lookup"><span data-stu-id="461f2-133">When users select the icon to launch the extension, `popup/popup.html` is displayed as a modal dialog.</span></span>  

<span data-ttu-id="461f2-134">Ajoutez le code de l’extrait de code suivant pour `popup.html` afficher l’image des étoiles.</span><span class="sxs-lookup"><span data-stu-id="461f2-134">Add the code from the following code snippet to `popup.html` to display the stars image.</span></span>  

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

<span data-ttu-id="461f2-135">Veillez à ajouter le fichier image `images/stars.jpeg` au dossier images.</span><span class="sxs-lookup"><span data-stu-id="461f2-135">Ensure that you add the image file `images/stars.jpeg` to the images folder.</span></span>  <span data-ttu-id="461f2-136">Les répertoires de votre projet doivent être similaires à la structure suivante.</span><span class="sxs-lookup"><span data-stu-id="461f2-136">The directories of your project should be similar to the following structure.</span></span>   

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

<span data-ttu-id="461f2-137">Enfin, assurez-vous d’inscrire la fenêtre pop-up sous , comme `manifest.json` `browser_action` illustré dans l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="461f2-137">Finally, ensure you register the pop-up in `manifest.json` under `browser_action`, as shown in the following code snippet.</span></span>  

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

## <a name="next-steps"></a><span data-ttu-id="461f2-138">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="461f2-138">Next steps</span></span>
<span data-ttu-id="461f2-139">C’est tout ce dont vous avez besoin pour développer une extension de travail.</span><span class="sxs-lookup"><span data-stu-id="461f2-139">That is everything you need to develop a working extension.</span></span>  <span data-ttu-id="461f2-140">À présent, poursuivez le chargement de version test et testez votre extension.</span><span class="sxs-lookup"><span data-stu-id="461f2-140">Now, continue on to sideload and test your extension.</span></span> <span data-ttu-id="461f2-141">Pour plus d’informations, [accédez à Sideload an extension][TestExtensionSideload].</span><span class="sxs-lookup"><span data-stu-id="461f2-141">For more information, navigate to [Sideload an extension][TestExtensionSideload].</span></span>  

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
