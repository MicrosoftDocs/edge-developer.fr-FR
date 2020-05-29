---
description: Extensions démarrées 1ère partie
title: Créez une extension simple qui s’affiche avec la NASA image du jour.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/08/2020
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: Edge-chrome, développement Web, html, CSS, JavaScript, développeur, extensions
ms.openlocfilehash: dd5c1dab0cb9b54b79be7d2728cb9bfde0945185
ms.sourcegitcommit: 0bc1312a1e6a0ac37cf385201db4361fc05184fc
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2020
ms.locfileid: "10683622"
---
# <span data-ttu-id="01b63-104">Créez une extension simple qui s’affiche avec la NASA image du jour.</span><span class="sxs-lookup"><span data-stu-id="01b63-104">Build A Simple Extension That Pops Up NASA Picture Of The Day</span></span>  

[<span data-ttu-id="01b63-105">Source du package d’extension terminée pour cette partie</span><span class="sxs-lookup"><span data-stu-id="01b63-105">Completed Extension Package Source for This Part</span></span>][ArchiveExtensionGettingStartedPart1]  

## <span data-ttu-id="01b63-106">Présentation</span><span class="sxs-lookup"><span data-stu-id="01b63-106">Overview</span></span>  

<span data-ttu-id="01b63-107">Dans la première partie, l’objectif est de générer une extension de chrome de contour très simple à partir d’un répertoire vide.</span><span class="sxs-lookup"><span data-stu-id="01b63-107">In part 1, the goal is to build a very simple Edge Chromium Extension starting with an empty directory.</span></span>  <span data-ttu-id="01b63-108">L’objectif de cette extension consiste à effectuer les tâches suivantes.</span><span class="sxs-lookup"><span data-stu-id="01b63-108">The goal for this Extension is to complete the following tasks.</span></span>  

*   <span data-ttu-id="01b63-109">Créer des icônes pour l’extension pouvant être utilisées à plusieurs emplacements et de tailles différentes</span><span class="sxs-lookup"><span data-stu-id="01b63-109">Create icons for the Extension that may be used in multiple places and in different sizes</span></span>  
*   <span data-ttu-id="01b63-110">Créer un `manifest.json` fichier simple</span><span class="sxs-lookup"><span data-stu-id="01b63-110">Create a simple `manifest.json` file</span></span>  
*   <span data-ttu-id="01b63-111">Afficher une icône de lancement qui, lorsqu’elle est sélectionnée, affiche une fenêtre contextuelle contenant l’image de NASA du jour.</span><span class="sxs-lookup"><span data-stu-id="01b63-111">Display a launch icon that when selected displays a pop-up window containing the NASA picture of the day</span></span>  

## <span data-ttu-id="01b63-112">Notions de base des fichiers manifeste</span><span class="sxs-lookup"><span data-stu-id="01b63-112">The manifest file basics</span></span>  

<span data-ttu-id="01b63-113">Chaque package d’extension doit avoir un `manifest.json` fichier à la racine.</span><span class="sxs-lookup"><span data-stu-id="01b63-113">Every Extension package must have a `manifest.json` file at the root.</span></span>  <span data-ttu-id="01b63-114">Vous devez considérer ceci comme le plan de l’extension.</span><span class="sxs-lookup"><span data-stu-id="01b63-114">You should think of this as the blueprint for the Extension.</span></span>  <span data-ttu-id="01b63-115">Il indique au moteur du navigateur quelle version de l’API d’extension est attendue, le nom et la description de l’extension ainsi que de nombreuses autres informations, dont la plupart sont décrites dans le Guide de mise en route de l’extension multipoint.</span><span class="sxs-lookup"><span data-stu-id="01b63-115">It tells the browser engine what version of the Extension API the Extension expects, the name and description of the Extension, and lots of other details, many of which are discussed in this multi-part Extension Getting Started guide.</span></span>  

<span data-ttu-id="01b63-116">Voici un simple</span><span class="sxs-lookup"><span data-stu-id="01b63-116">Below is the simple</span></span>  `manifest.json`  

```json
{
    "name": "NASA Picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A Chromium Extension to show the NASA Picture of the Day."
}
```  

## <span data-ttu-id="01b63-117">Configuration des icônes d’extension</span><span class="sxs-lookup"><span data-stu-id="01b63-117">Extension icons setup</span></span>  

<span data-ttu-id="01b63-118">Ensuite, ajoutez des icônes au `manifest.json` fichier \ (et créez un nouveau `/icons` répertoire avec les icônes fichiers \).</span><span class="sxs-lookup"><span data-stu-id="01b63-118">Next add some icons to `manifest.json` file \(and create a new `/icons` directory with the icons files\).</span></span>  <span data-ttu-id="01b63-119">Les icônes sont utilisées pour l’image d’arrière-plan du bouton que l’utilisateur sélectionne pour lancer l’extension \ (le cas échéant) et d’autres emplacements appropriés.</span><span class="sxs-lookup"><span data-stu-id="01b63-119">The icons are used for the background image of the button the user selects to launch the extension \(if there is one\), and other places that are appropriate.</span></span>  

`PNG` <span data-ttu-id="01b63-120">est le format recommandé, mais vous pouvez également utiliser `BMP` , `GIF` `ICO` et `JPEG` .</span><span class="sxs-lookup"><span data-stu-id="01b63-120">is the recommended format, but you may also use `BMP`, `GIF`, `ICO` and `JPEG`.</span></span>  <span data-ttu-id="01b63-121">Il est recommandé de toujours disposer d’au moins une icône de taille de 128x128 pixels et le navigateur le redimensionne automatiquement le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="01b63-121">It is recommended to always have at least a 128x128 pixels size icon and the browser automatically resizes it as necessary.</span></span>  

<span data-ttu-id="01b63-122">Votre structure d’annuaire doit ressembler à ce qui suit.</span><span class="sxs-lookup"><span data-stu-id="01b63-122">Your directory structure should look like the following diagram.</span></span>  

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

<span data-ttu-id="01b63-123">Le fichier mis à jour `manifest.json` doit apparaître comme suit.</span><span class="sxs-lookup"><span data-stu-id="01b63-123">Your updated `manifest.json` file should appear as follows.</span></span>  

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
> <span data-ttu-id="01b63-124">Le fichier d’icônes `png` indiqué dans le code précédent est disponible dans le téléchargement zip mentionné en haut de cette page.</span><span class="sxs-lookup"><span data-stu-id="01b63-124">The icon `png` files listed previous code are available in the zip download mentioned at the top of this page.</span></span>  

## <span data-ttu-id="01b63-125">Ajout d’une boîte de dialogue contextuelle par défaut</span><span class="sxs-lookup"><span data-stu-id="01b63-125">Adding a default pop-up dialog</span></span>  

<span data-ttu-id="01b63-126">À présent, créez un `HTML` fichier qui s’exécute automatiquement lorsque l’utilisateur clique sur l’icône extension.</span><span class="sxs-lookup"><span data-stu-id="01b63-126">Now, create an `HTML` file that is automatically run when the user selects on the extension icon.</span></span>  

:::image type="complex" source="./media/part1-badge1.png" alt-text="Icône de badge de barre d’outils":::
   <span data-ttu-id="01b63-128">Icône de badge de barre d’outils</span><span class="sxs-lookup"><span data-stu-id="01b63-128">Toolbar Badge Icon</span></span>
:::image-end:::

<!--![Toolbar Badge Icon][ImagePart1Badge1]  -->  

<span data-ttu-id="01b63-129">Le fichier HTML est nommé `popup/popup.html` .</span><span class="sxs-lookup"><span data-stu-id="01b63-129">The HTML file is named `popup/popup.html`.</span></span>  <span data-ttu-id="01b63-130">La sélection de l’icône de l’extension `popup/popup.html` s’exécute comme une boîte de dialogue modale qui s’affiche jusqu’à ce que vous ayez sélectionné hors de la boîte</span><span class="sxs-lookup"><span data-stu-id="01b63-130">Selecting the Extension icon launches `popup/popup.html` as modal dialog that stays up until you select outside the dialog.</span></span>  

<span data-ttu-id="01b63-131">Pour cela, enregistrez le fichier comme fenêtre contextuelle par défaut dans le `manifest.json` `browser_action` code suivant.</span><span class="sxs-lookup"><span data-stu-id="01b63-131">For this, register the file as a default pop-up in the `manifest.json` under `browser_action` in the following code.</span></span>  

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

<span data-ttu-id="01b63-132">Dans l' `popup` annuaire, ajoutez le fichier `popup.html` et demandez-lui de générer le rendu de l’image étoiles.</span><span class="sxs-lookup"><span data-stu-id="01b63-132">In the `popup` directory , add the file `popup.html` and have it render the stars image.</span></span>  <span data-ttu-id="01b63-133">Voici le `popup.html` fichier.</span><span class="sxs-lookup"><span data-stu-id="01b63-133">Here is the `popup.html` file.</span></span>  

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

 <span data-ttu-id="01b63-134">Ajoutez également un fichier image `images/stars.jpeg` référencé dans le `popup.html` fichier.</span><span class="sxs-lookup"><span data-stu-id="01b63-134">Also, add an image file `images/stars.jpeg` that is referenced in the `popup.html` file.</span></span>  

<span data-ttu-id="01b63-135">La structure d’annuaire de l’exemple d’extension est affichée dans le schéma suivant.</span><span class="sxs-lookup"><span data-stu-id="01b63-135">The directory structure for the example Extension is displayed in the following diagram.</span></span>  

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

> [!NOTE]
> <span data-ttu-id="01b63-136">Le `images/stars.jpeg` fichier listé dans l’image précédente est disponible dans le [Téléchargement zip][ArchiveExtensionGettingStartedPart1].</span><span class="sxs-lookup"><span data-stu-id="01b63-136">The `images/stars.jpeg` file listed in the previous image is available in the [zip download][ArchiveExtensionGettingStartedPart1].</span></span>  

<span data-ttu-id="01b63-137">C’est tout ce dont vous avez besoin pour créer une extension de travail.</span><span class="sxs-lookup"><span data-stu-id="01b63-137">That is everything you need to build a working Extension.</span></span>  <span data-ttu-id="01b63-138">C’est tout ce qu’il reste à tester.</span><span class="sxs-lookup"><span data-stu-id="01b63-138">All that is left to is test it.</span></span>  

<span data-ttu-id="01b63-139">La section suivante explique comment charger l’extension \ (parfois appelée chargement sur le côté \) dans le navigateur Microsoft Edge \ (chrome \) pour la tester.</span><span class="sxs-lookup"><span data-stu-id="01b63-139">The next section explains how to load the Extension \(sometimes called side loading\) into the Microsoft Edge \(Chromium\) browser to test it.</span></span>  

## <span data-ttu-id="01b63-140">Exécutez votre extension localement dans votre navigateur lors de la création de celle-ci.</span><span class="sxs-lookup"><span data-stu-id="01b63-140">Run your Extension locally in your browser while developing it \(side-loading\)</span></span>  

<span data-ttu-id="01b63-141">Le navigateur Microsoft Edge \ (chrome \) vous permet d’exécuter facilement et de déboguer vos extensions lors du développement.</span><span class="sxs-lookup"><span data-stu-id="01b63-141">The Microsoft Edge \(Chromium\) browser provides a safe and simple way for you to run as well as debug your Extensions while you are developing.</span></span>  

<span data-ttu-id="01b63-142">Le processus est relativement simple.</span><span class="sxs-lookup"><span data-stu-id="01b63-142">The process is quite simple.</span></span>  <span data-ttu-id="01b63-143">Vous devez d’abord sélectionner les points de suspension en haut de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="01b63-143">You must first select the three dots at the top of your browser.</span></span>  <span data-ttu-id="01b63-144">Sélectionnez ensuite `Extensions` dans le menu contextuel, comme illustré dans l’image suivante.</span><span class="sxs-lookup"><span data-stu-id="01b63-144">Next, choose `Extensions` from the context menu as shown in the following image.</span></span>  

:::image type="complex" source="./media/part1-threedots.png" alt-text="Choisir les extensions":::
   <span data-ttu-id="01b63-146">Choisir les extensions</span><span class="sxs-lookup"><span data-stu-id="01b63-146">Choose Extensions</span></span>
:::image-end:::

<!--![Choose Extensions][ImagePart1Threedots]  -->  

<span data-ttu-id="01b63-147">Lorsque vous vous trouvez sur la page **Extensions** comme illustré dans l’image suivante, activez le **mode développeur** en activant le bouton bascule en bas à gauche de la page, comme illustré dans l’image suivante.</span><span class="sxs-lookup"><span data-stu-id="01b63-147">When you are on the **Extensions** page as shown in the following image, enable the **Developer mode** by enabling the toggle at the bottom left of the page as shown in the following image.</span></span>  

:::image type="complex" source="./media/part1-developermode-toggle.png" alt-text="Activer le mode développeur":::
   <span data-ttu-id="01b63-149">Activer le mode développeur</span><span class="sxs-lookup"><span data-stu-id="01b63-149">Enable Developer Mode</span></span>
:::image-end:::

<!--![Enable Developer Mode][ImagePart1DevelopermodeToggle]  -->  

## <span data-ttu-id="01b63-150">Installation et mise à jour des extensions installées hors Windows Store</span><span class="sxs-lookup"><span data-stu-id="01b63-150">Installing and updating side-loaded Extensions</span></span>  

<span data-ttu-id="01b63-151">Lorsque vous voulez installer votre extension pour la première fois, vous devez choisir l' `Load Unpacked` option comme illustré dans l’image suivante.</span><span class="sxs-lookup"><span data-stu-id="01b63-151">The first time you want to install your Extension, you choose the `Load Unpacked` option as shown in the following image.</span></span>  <span data-ttu-id="01b63-152">Vous êtes invité à indiquer un répertoire dans lequel vous pouvez classer les ressources d’extension par fichier.</span><span class="sxs-lookup"><span data-stu-id="01b63-152">This prompts you for a directory where you have your Extension assets file by file.</span></span>  <span data-ttu-id="01b63-153">Cette opération installe l’extension comme si vous l’avez déjà téléchargée depuis le Windows Store.</span><span class="sxs-lookup"><span data-stu-id="01b63-153">This installs the Extension as if you had downloaded it from a store.</span></span>  

:::image type="complex" source="./media/part1-installed-extension.png" alt-text="Extensions installées":::
   <span data-ttu-id="01b63-155">Extensions installées</span><span class="sxs-lookup"><span data-stu-id="01b63-155">Installed Extensions</span></span>
:::image-end:::

<!--![Installed Extensions][ImagePart1InstalledExtension]  -->  

<span data-ttu-id="01b63-156">Après avoir installé votre extension, vous pouvez la mettre à jour en sélectionnant le `Reload` bouton sous votre liste de extensions.</span><span class="sxs-lookup"><span data-stu-id="01b63-156">After you install your Extension, you may update it by selecting the `Reload` button under your Extension listing.</span></span>  

<span data-ttu-id="01b63-157">Pour supprimer l’extension de votre navigateur, cliquez sur le `Remove` bouton situé en bas de la liste des extensions.</span><span class="sxs-lookup"><span data-stu-id="01b63-157">To remove the Extension from your browser, click the `Remove` button on the bottom of the Extension listing.</span></span>  

## <span data-ttu-id="01b63-158">Extensions de débogage</span><span class="sxs-lookup"><span data-stu-id="01b63-158">Debugging Extensions</span></span>  

<span data-ttu-id="01b63-159">Le débogage d’extensions est relativement simple et prend en charge toutes les fonctionnalités dans DevTools de chrome.</span><span class="sxs-lookup"><span data-stu-id="01b63-159">Debugging Extensions is quite easy and supports all of the features in Edge Chromium DevTools.</span></span>  <span data-ttu-id="01b63-160">Ces informations ne sont pas abordées dans ce guide de mise en route; il est toutefois essentiel de générer correctement les extensions.</span><span class="sxs-lookup"><span data-stu-id="01b63-160">Those details however are not covered in this getting started guide but are very important to successfully build Extensions.</span></span>  

<!-- image links -->  

<!--[ImagePart1Heirarchy]: ./media/part1-heirarchy.png "Directory Structure"  -->  
<!--[ImagePart1Badge1]: ./media/part1-badge1.png "Toolbar Badge Icon"  -->  
<!--[ImagePart1Heirarchy1]: ./media/part1-heirarchy1.png "Directory Structure for Extension"  -->  
<!--[ImagePart1Threedots]: ./media/part1-threedots.png "Choose Extensions"  -->  
<!--[ImagePart1DevelopermodeToggle]: ./media/part1-developermode-toggle.png "Enable Developer Mode"  -->  
<!--[ImagePart1InstalledExtension]: ./media/part1-installed-extension.png "Installed Extensions"  -->  

<!-- links -->  

[ArchiveExtensionGettingStartedPart1]: ./extension-source/extension-getting-started-part1.zip "Source du package d’extension terminée pour cette partie | Documents Microsoft"  
