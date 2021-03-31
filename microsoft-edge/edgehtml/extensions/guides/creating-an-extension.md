---
description: Découvrir comment créer une extension Microsoft Edge
title: Création d’une extension
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, CSS, JavaScript, développeur
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 15cb7a4c187210c885b5d75770bda1c590a8c5d1
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233457"
---
# <span data-ttu-id="1b15c-104">Création d’une extension Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1b15c-104">Creating A Microsoft Edge Extension</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="1b15c-105">Ce guide décrit la création d’une extension pour Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1b15c-105">In this guide, learn to create an extension for Microsoft Edge.</span></span>  <span data-ttu-id="1b15c-106">Cet exemple d’extension vous permet de manipuler des feuilles de style CSS spécifiques pour [docs.Microsoft.com][MicrosoftDocs] , notamment pour vous guider dans la création d’un fichier manifeste, l’interface utilisateur et les scripts d’arrière-plan et de contenu.</span><span class="sxs-lookup"><span data-stu-id="1b15c-106">This example extension allows you to manipulate specific CSS for [docs.microsoft.com][MicrosoftDocs] pages including walking you through creation of a manifest file, the user interface, and background and content scripts.</span></span>  

:::image type="complex" source="../media/color-changer_header.png" alt-text="Docs.microsoft.com Body a changé en bleu":::
   <span data-ttu-id="1b15c-108">Docs.microsoft.com Body a changé en bleu</span><span class="sxs-lookup"><span data-stu-id="1b15c-108">Docs.microsoft.com body changed to blue</span></span>
:::image-end:::

<!--![Docs.microsoft.com body changed to blue][ImageColorChangerHeader]  -->  

<span data-ttu-id="1b15c-109">Ce didacticiel suppose que vous disposez d’une compréhension de base de l’extension d’un navigateur et de son fonctionnement.</span><span class="sxs-lookup"><span data-stu-id="1b15c-109">This tutorial assumes you have basic understanding of what a browser extension is and how it work.</span></span>  <span data-ttu-id="1b15c-110">Pour plus d’informations sur les blocs de construction des extensions, voir [anatomie d’une extension][MDNAnatomyExtension].</span><span class="sxs-lookup"><span data-stu-id="1b15c-110">For more imformation about the building blocks for extensions, see [Anatomy of an extension][MDNAnatomyExtension].</span></span>  

<span data-ttu-id="1b15c-111">Téléchargez le code de l' [exemple complet sur GitHub][GithubMicrosoftEdgeExtensionsDemosColorChanger].</span><span class="sxs-lookup"><span data-stu-id="1b15c-111">Download the code for the [full sample on GitHub][GithubMicrosoftEdgeExtensionsDemosColorChanger].</span></span>  

## <span data-ttu-id="1b15c-112">Création du fichier manifeste</span><span class="sxs-lookup"><span data-stu-id="1b15c-112">Building the manifest file</span></span>  

<span data-ttu-id="1b15c-113">Pour commencer, créez un répertoire pour votre extension et nommez-le `color-changer` .</span><span class="sxs-lookup"><span data-stu-id="1b15c-113">To begin, create a directory for your extension and name it `color-changer`.</span></span>  

<span data-ttu-id="1b15c-114">Dans le `color-changer` dossier, créez un fichier nommé `manifest.json` .</span><span class="sxs-lookup"><span data-stu-id="1b15c-114">Inside the `color-changer` folder, create a file named `manifest.json`.</span></span>  <span data-ttu-id="1b15c-115">Le `manifest.json` fichier est requis pour toutes les extensions et fournit des informations importantes pour l’extension, de l’extension aux autorisations.</span><span class="sxs-lookup"><span data-stu-id="1b15c-115">The `manifest.json` file is required for all extensions and provides important information for the extension, ranging from the extension name to the permissions.</span></span>  

> [!NOTE] 
> <span data-ttu-id="1b15c-116">Ce guide vous guide à travers toutes les clés de manifeste que vous devez utiliser dans ce guide, mais pour obtenir la liste de toutes les clés de manifeste prises en charge et recommandées, voir [clés de manifeste prises en charge][ExtensionsApisupportManifestKeys].</span><span class="sxs-lookup"><span data-stu-id="1b15c-116">This guide walks you through all the manifest keys you must use in this guide, but for a list of all supported and recommended manifest keys, see [Supported manifest keys][ExtensionsApisupportManifestKeys].</span></span>  

<span data-ttu-id="1b15c-117">À l’intérieur `manifest.json` , ajoutez le code suivant.</span><span class="sxs-lookup"><span data-stu-id="1b15c-117">Inside `manifest.json`, add the following code.</span></span>  

```json
{
  "name": "Color Changer",
  "author": "Microsoft Edge Extension Developer",
  "version": "1.0",
  "description": "Change the color of the body on docs.microsoft.com",
  "permissions": [
    "*://docs.microsoft.com/*",
    "tabs"
  ], 
  "browser_action": {
    "default_icon": {
      "20": "images/color-changer20.png",
      "40": "images/color-changer40.png"
    },
    "default_title": "Color Changer",
    "default_popup": "popup.html"
  }
}
```  

### <span data-ttu-id="1b15c-118">Définitions des clés de manifeste</span><span class="sxs-lookup"><span data-stu-id="1b15c-118">Manifest key definitions</span></span>  

| <span data-ttu-id="1b15c-119">Clé</span><span class="sxs-lookup"><span data-stu-id="1b15c-119">Key</span></span> | <span data-ttu-id="1b15c-120">Détails</span><span class="sxs-lookup"><span data-stu-id="1b15c-120">Details</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="1b15c-121">name</span><span class="sxs-lookup"><span data-stu-id="1b15c-121">name</span></span>][MDNManifestjsonName] | <span data-ttu-id="1b15c-122">Nom de l’extension.</span><span class="sxs-lookup"><span data-stu-id="1b15c-122">The name of the extension.</span></span>  |  
| [<span data-ttu-id="1b15c-123">auteur</span><span class="sxs-lookup"><span data-stu-id="1b15c-123">author</span></span>][MDNManifestjsonAuthor] | <span data-ttu-id="1b15c-124">Auteur de l’extension.</span><span class="sxs-lookup"><span data-stu-id="1b15c-124">The author of the extension.</span></span>  |  
| [<span data-ttu-id="1b15c-125">version</span><span class="sxs-lookup"><span data-stu-id="1b15c-125">version</span></span>][MDNManifestjsonVersion] | <span data-ttu-id="1b15c-126">Numéro de version de l’extension.</span><span class="sxs-lookup"><span data-stu-id="1b15c-126">The extension version number.</span></span>  |  
| [<span data-ttu-id="1b15c-127">description</span><span class="sxs-lookup"><span data-stu-id="1b15c-127">description</span></span>][MDNManifestjsonDescription] | <span data-ttu-id="1b15c-128">Description de l’extension affichée dans la section à propos du menu extension dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1b15c-128">The description of the extension displayed in the About section of the extension menu in Microsoft Edge.</span></span>  |  
| [<span data-ttu-id="1b15c-129">attribué</span><span class="sxs-lookup"><span data-stu-id="1b15c-129">permissions</span></span>][MDNManifestjsonPermissions] | <span data-ttu-id="1b15c-130">Tableau de chaînes demandant des autorisations pour l’extension.</span><span class="sxs-lookup"><span data-stu-id="1b15c-130">An array of strings requesting permissions for the extension.</span></span>  <span data-ttu-id="1b15c-131">Pour votre extension, vous demandez des autorisations pour afficher les sites Web visités \(«onglets» \) et mettre à jour le contenu des URL correspondantes « `*://docs.microsoft.com/*` ».</span><span class="sxs-lookup"><span data-stu-id="1b15c-131">For your extension, you are requesting permissions to see the websites visited \("tabs"\) and to update content on URLs matching "`*://docs.microsoft.com/*`".</span></span>  |  
| [<span data-ttu-id="1b15c-132">browser_action</span><span class="sxs-lookup"><span data-stu-id="1b15c-132">browser_action</span></span>][MDNManifestjsonBrowserAction] | <span data-ttu-id="1b15c-133">Contient les informations relatives à une icône.</span><span class="sxs-lookup"><span data-stu-id="1b15c-133">Contains the information for an icon.</span></span> <span data-ttu-id="1b15c-134">L’icône est placée sur la barre d’outils Microsoft Edge, à droite de la barre d’adresse.</span><span class="sxs-lookup"><span data-stu-id="1b15c-134">The icon is placed on the Microsoft Edge toolbar, to the right of the address bar.</span></span>  |  

#### <span data-ttu-id="1b15c-135">définitions de clés de browser_action</span><span class="sxs-lookup"><span data-stu-id="1b15c-135">browser_action Key definitions</span></span>  

| <span data-ttu-id="1b15c-136">Clé</span><span class="sxs-lookup"><span data-stu-id="1b15c-136">Key</span></span> | <span data-ttu-id="1b15c-137">Détails</span><span class="sxs-lookup"><span data-stu-id="1b15c-137">Details</span></span> |  
|:--- |:--- |  
| `default_icon` | <span data-ttu-id="1b15c-138">Icône utilisée dans la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="1b15c-138">The icon that is used in the toolbar.</span></span>  |  
| `default_title` | <span data-ttu-id="1b15c-139">Texte qui s’affiche lorsqu’un utilisateur pointe sur l’icône dans la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="1b15c-139">The text that is displayed when a user hovers over the icon in the toolbar.</span></span>  |  
| `default_popup` | <span data-ttu-id="1b15c-140">Chemin d’accès au fichier HTML de la fenêtre contextuelle.</span><span class="sxs-lookup"><span data-stu-id="1b15c-140">The path to the HTML file for the pop-up window.</span></span>  |  

<span data-ttu-id="1b15c-141">À présent que vous avez créé le fichier manifeste, vous avez besoin d’une interface utilisateur pour l’extension.</span><span class="sxs-lookup"><span data-stu-id="1b15c-141">Now that you have created the manifest file, you need a user interface for the extension.</span></span>  

## <span data-ttu-id="1b15c-142">Création de la fenêtre contextuelle</span><span class="sxs-lookup"><span data-stu-id="1b15c-142">Creating the pop-up</span></span>  

<span data-ttu-id="1b15c-143">Pour votre extension, créez une fenêtre contextuelle pour l’interface utilisateur, comme ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="1b15c-143">For your extension, create a pop-up for the user interface, like below.</span></span>  

:::image type="complex" source="../media/color-changer_popup.png" alt-text="Interface contextuelle de l’extension":::
   <span data-ttu-id="1b15c-145">Interface contextuelle de l’extension</span><span class="sxs-lookup"><span data-stu-id="1b15c-145">The pop-up interface of the extension</span></span>
:::image-end:::

<!--![The pop-up interface of the extension][ImageColorChangerPopup]  -->  

<span data-ttu-id="1b15c-146">Créez un fichier nommé `popup.html` à la racine de votre `color-changer` dossier.</span><span class="sxs-lookup"><span data-stu-id="1b15c-146">Create a file named `popup.html` in the root of your `color-changer` folder.</span></span>  <span data-ttu-id="1b15c-147">Collez le code suivant `popup.html` .</span><span class="sxs-lookup"><span data-stu-id="1b15c-147">Paste the following code into `popup.html`.</span></span>  

```html
<!DOCTYPE html>
<html>
    <head>
        <link rel="stylesheet" type="text/css" href="css/styles.css" />
    </head>
    <body>
        <h1>Creating a Microsoft Edge Extension</h1>
        <p>Color Changer</p>
        <input id="aliceblue" type="button" value="Aliceblue" />
        <input id="cornsilk" type="button" value="Cornsilk" />
        <input id="reset" type="button" value="Reset" />
        <script src="js/popup.js"></script>
    </body>
</html>
```  

<span data-ttu-id="1b15c-148">Dans `popup.html` , vous créez un titre, un paragraphe et trois boutons \(AliceBlue, Cornsilk et Reset \).</span><span class="sxs-lookup"><span data-stu-id="1b15c-148">In `popup.html`, you create a title, a paragraph, and three buttons \(Aliceblue, Cornsilk, and Reset\).</span></span>  

<span data-ttu-id="1b15c-149">À présent, créez un dossier nommé `css` et dans créer un fichier nommé `styles.css` .</span><span class="sxs-lookup"><span data-stu-id="1b15c-149">Now create a folder named `css` and inside create a file named `styles.css`.</span></span>  <span data-ttu-id="1b15c-150">Ajoutez les styles ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="1b15c-150">Add the styles below.</span></span>  

```css
/* main styles */
* {
    font-family: 'Segoe UI';
}

h1 {
    font-weight: 600;
    font-size: .9em;
}

p {
    font-weight: 500;
    font-size: .8em;
    margin-bottom: 10px;  
}
```  

<span data-ttu-id="1b15c-151">Ce code CSS donne à notre extension quelques styles de base.</span><span class="sxs-lookup"><span data-stu-id="1b15c-151">This CSS gives our extension some basic styles.</span></span>  <span data-ttu-id="1b15c-152">N’hésitez pas à ajouter des styles pour personnaliser votre extension.</span><span class="sxs-lookup"><span data-stu-id="1b15c-152">Feel free to add more styles to customize your extension.</span></span>  

<span data-ttu-id="1b15c-153">Ensuite, vous devez créer le fichier JavaScript qui interagit avec la fenêtre contextuelle.</span><span class="sxs-lookup"><span data-stu-id="1b15c-153">Next, you must create the JavaScript file that interacts with the pop-up.</span></span>  <span data-ttu-id="1b15c-154">Créez un `js` dossier et un fichier nommé `popup.js` à l’intérieur de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="1b15c-154">Create a `js` folder and a file named `popup.js` inside.</span></span>  <span data-ttu-id="1b15c-155">Mettez à jour `popup.js` avec le code suivant.</span><span class="sxs-lookup"><span data-stu-id="1b15c-155">Update `popup.js` with the following code.</span></span>  

```JavaScript
// get the buttons by id
let aliceblue = document.getElementById('aliceblue');
let cornsilk = document.getElementById('cornsilk');
let reset = document.getElementById('reset');

// use tabs.insertCSS to change header color on button click

// aliceblue
aliceblue.onclick = () => {
  browser.tabs.insertCSS({code: "body { background: aliceblue !important; }"});
};

// cornsilk
cornsilk.onclick = () => {
  browser.tabs.insertCSS({code: "body { background: cornsilk !important; }"});
};

// back to original
reset.onclick = () => {
  browser.tabs.insertCSS({code: "body { background: none !important; }"});
};
```  

<span data-ttu-id="1b15c-156">Dans `popup.js` , l’API [Tab][MDNApiTabs] vous permet d’interagir avec les onglets du navigateur et d’injecter du texte et des styles dans le contenu de la page.</span><span class="sxs-lookup"><span data-stu-id="1b15c-156">In `popup.js`, the [tabs][MDNApiTabs] API allows you to interact with the tabs of the browser and inject script and styles into the page content.</span></span>  <span data-ttu-id="1b15c-157">À l’aide de la méthode [Tabs. insertCSS ()][MDNApiTabsInsertcss] , vous injectez la feuille de style CSS spécifiée dans la page qui remplace l’en-tête de [docs.Microsoft.com][MicrosoftDocs] par une autre couleur lorsque l’utilisateur clique sur le bouton spécifié.</span><span class="sxs-lookup"><span data-stu-id="1b15c-157">Using the [tabs.insertCSS()][MDNApiTabsInsertcss] method, you inject the specified CSS into the page which changes the header on [docs.microsoft.com][MicrosoftDocs] to a different color when the specified button is clicked.</span></span>  

<span data-ttu-id="1b15c-158">À présent que vous disposez de la fonctionnalité contextuelle de base, ajoutez des icônes à l’extension.</span><span class="sxs-lookup"><span data-stu-id="1b15c-158">Now that you have the basic pop-up functionality, add icons to the extension.</span></span>  

## <span data-ttu-id="1b15c-159">Ajout d’icônes</span><span class="sxs-lookup"><span data-stu-id="1b15c-159">Adding icons</span></span>  

<span data-ttu-id="1b15c-160">Les icônes servent à représenter l’extension dans la barre d’outils du navigateur, dans le menu extensions et dans d’autres emplacements.</span><span class="sxs-lookup"><span data-stu-id="1b15c-160">Icons are used to represent the extension in the browser toolbar, the extensions menu, and other places.</span></span>  <span data-ttu-id="1b15c-161">Téléchargez les [icônes de votre extension sur GitHub][GithubMicrosoftEdgeExtensionsDemosColorChangerImages].</span><span class="sxs-lookup"><span data-stu-id="1b15c-161">Download the [icons for your extension on GitHub][GithubMicrosoftEdgeExtensionsDemosColorChangerImages].</span></span> <span data-ttu-id="1b15c-162">Pour plus d’informations sur les icônes d’extension dans Microsoft Edge, voir le [Guide de conception][ExtensionsGuidesDesignIcons].</span><span class="sxs-lookup"><span data-stu-id="1b15c-162">For more information about extension icons in Microsoft Edge, see [Design Guide][ExtensionsGuidesDesignIcons].</span></span>  

<span data-ttu-id="1b15c-163">Après avoir téléchargé les icônes de l’extension, enregistrez les icônes dans un `images` dossier `color-changer` .</span><span class="sxs-lookup"><span data-stu-id="1b15c-163">After you download the extension icons, save the icons in an `images` folder inside `color-changer`.</span></span>  

<span data-ttu-id="1b15c-164">L’icône qui s’affiche dans la barre d’outils est définie à l' `default_icon` intérieur de la clé de [browser_action][MDNManifestjsonBrowserAction] , que vous avez déjà ajoutée à votre fichier de manifeste dans une section antérieure.</span><span class="sxs-lookup"><span data-stu-id="1b15c-164">The icon that appears in the toolbar is set using `default_icon` inside of the [browser_action][MDNManifestjsonBrowserAction] key, which you already added to your manifest file in an earlier section.</span></span>  

<span data-ttu-id="1b15c-165">La `icons` clé définit les icônes qui doivent être utilisées dans les menus paramètres d’extensions.</span><span class="sxs-lookup"><span data-stu-id="1b15c-165">The `icons` key defines which icons should be used in the Extensions settings menus.</span></span>  <span data-ttu-id="1b15c-166">Vous trouverez ci-dessous une sélection de plusieurs icônes de tailles différentes pour indiquer les différentes résolutions d’écran.</span><span class="sxs-lookup"><span data-stu-id="1b15c-166">Below, you are specifying multiple icons with different sizes to account for different screen resolutions.</span></span>  <span data-ttu-id="1b15c-167">Le nom des icônes, et les haut-parleurs `25` `48` en pixels des icônes.</span><span class="sxs-lookup"><span data-stu-id="1b15c-167">The name of the icons, `25` and `48` are the heights in pixels of the icons.</span></span>  

<span data-ttu-id="1b15c-168">Dans le fichier [manifest.js][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] , incluez une clé de niveau supérieur pour `icons` .</span><span class="sxs-lookup"><span data-stu-id="1b15c-168">In the [manifest.json][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] file, include a top-level key for `icons`.</span></span>  

```json
  "icons": {
    "25": "images/color-changer25.png",
    "48": "images/color-changer48.png"
  }
```  

### <span data-ttu-id="1b15c-169">Définitions des clés de manifeste</span><span class="sxs-lookup"><span data-stu-id="1b15c-169">Manifest Key definitions</span></span>  

| <span data-ttu-id="1b15c-170">Clé</span><span class="sxs-lookup"><span data-stu-id="1b15c-170">Key</span></span> | <span data-ttu-id="1b15c-171">Détails</span><span class="sxs-lookup"><span data-stu-id="1b15c-171">Details</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="1b15c-172">icônes</span><span class="sxs-lookup"><span data-stu-id="1b15c-172">icons</span></span>][MDNManifestjsonIcons] | <span data-ttu-id="1b15c-173">Icônes de votre extension avec paires clé-valeur de taille d’image `px` et chemin d’image par rapport au répertoire racine de l’extension.</span><span class="sxs-lookup"><span data-stu-id="1b15c-173">The icons for your extension with key-value pairs of image size in `px` and image path relative to the root directory of the extension.</span></span> |  

> [!NOTE]
> <span data-ttu-id="1b15c-174">Utilisez les icônes `inactive##.png` situées dans le dossier images, plus loin dans ce guide.</span><span class="sxs-lookup"><span data-stu-id="1b15c-174">Use the icons named `inactive##.png` located in the images folder later in this guide.</span></span>  

## <span data-ttu-id="1b15c-175">Test de l’extension</span><span class="sxs-lookup"><span data-stu-id="1b15c-175">Testing the extension</span></span>  

<span data-ttu-id="1b15c-176">À présent que vous avez ajouté l’interface utilisateur et les icônes créées, testez votre extension.</span><span class="sxs-lookup"><span data-stu-id="1b15c-176">Now that you have added the user interface and created icons, test your extension.</span></span>  <span data-ttu-id="1b15c-177">Suivez les étapes permettant d' [Ajouter une extension][ExtensionsGuidesAddingRemovingExtensionsAdding] à Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1b15c-177">Walk through the steps for [Adding an extension][ExtensionsGuidesAddingRemovingExtensionsAdding] to Microsoft Edge.</span></span>  <span data-ttu-id="1b15c-178">Ensuite, revenez à ce guide.</span><span class="sxs-lookup"><span data-stu-id="1b15c-178">Afterwards, return to this guide.</span></span>  

<span data-ttu-id="1b15c-179">Une fois votre extension ajoutée, accédez à la page de [docs.Microsoft.com][MicrosoftDocs] .</span><span class="sxs-lookup"><span data-stu-id="1b15c-179">After you add your extension, navigate to any [docs.microsoft.com][MicrosoftDocs] page.</span></span>  <span data-ttu-id="1b15c-180">La fenêtre contextuelle suivante doit apparaître après avoir cliqué sur l’action du navigateur.</span><span class="sxs-lookup"><span data-stu-id="1b15c-180">You should see the following pop-up after clicking on the browser action.</span></span>  <span data-ttu-id="1b15c-181">La couleur du corps du [docs.Microsoft.com][MicrosoftDocs] doit également changer de couleur.</span><span class="sxs-lookup"><span data-stu-id="1b15c-181">The color of the [docs.microsoft.com][MicrosoftDocs] body should also change color.</span></span>  

:::row:::
   :::column span="1":::
      :::image type="complex" source="../media/color-changer_header_aliceblue.png" alt-text="Docs.microsoft.com en-tête modifié comme AliceBlue":::
         <span data-ttu-id="1b15c-183">Docs.microsoft.com en-tête modifié comme AliceBlue</span><span class="sxs-lookup"><span data-stu-id="1b15c-183">Docs.microsoft.com header changed to Aliceblue</span></span> :::image-end:::
      
      <!--![Docs.microsoft.com header changed to Aliceblue][ImageColorChangerHeaderAliceblue]  -->
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="../media/color-changer_header_cornsilk.png" alt-text="Docs.microsoft.com en-tête modifié comme Cornsilk":::
         <span data-ttu-id="1b15c-185">Docs.microsoft.com en-tête modifié comme Cornsilk</span><span class="sxs-lookup"><span data-stu-id="1b15c-185">Docs.microsoft.com header changed to Cornsilk</span></span> :::image-end:::
      
      <!--![Docs.microsoft.com header changed to Cornsilk][ImageColorChangerHeaderCornsilk]  -->
   :::column-end:::
:::row-end:::

<span data-ttu-id="1b15c-186">Si vous rencontrez des erreurs ou des fonctionnalités qui ne fonctionnent pas, voir le guide des [extensions de débogage][ExtensionsGuidesDebuggingExtensions] ou télécharger l' [exemple complet sur GitHub][GithubMicrosoftEdgeExtensionsDemosColorChanger].</span><span class="sxs-lookup"><span data-stu-id="1b15c-186">If you encounter any errors or functionality that does not work, see the [Debugging extensions][ExtensionsGuidesDebuggingExtensions] guide or download the [full sample on GitHub][GithubMicrosoftEdgeExtensionsDemosColorChanger].</span></span>  

## <span data-ttu-id="1b15c-187">Ajouter du contenu et des scripts d’arrière-plan</span><span class="sxs-lookup"><span data-stu-id="1b15c-187">Adding content and background scripts</span></span>  

<span data-ttu-id="1b15c-188">Accédez à l’étape suivante et ajoutez de la logique pour désactiver l’extension du travail sur les pages en dehors du domaine [docs.Microsoft.com][MicrosoftDocs] .</span><span class="sxs-lookup"><span data-stu-id="1b15c-188">Go one step further and add logic to disable the extension from working on pages outside the [docs.microsoft.com][MicrosoftDocs] domain.</span></span>  

<span data-ttu-id="1b15c-189">Vous devez d’abord créer un [script de contenu][MDNContentScripts].</span><span class="sxs-lookup"><span data-stu-id="1b15c-189">You must first create a [content script][MDNContentScripts].</span></span>  <span data-ttu-id="1b15c-190">Ensuite, vous devez créer des scripts de contenu qui s’exécutent dans le contexte d’une page Web particulière, qui peuvent accéder au contenu d’une page Web et peuvent communiquer avec des scripts en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="1b15c-190">Next, you must create content scripts that run in the context of a particular web page, are able to access the content of a web page, and are able to communicate with background scripts.</span></span>  <span data-ttu-id="1b15c-191">Dans votre `js` annuaire, créez un fichier nommé `content.js` et ajoutez le code suivant.</span><span class="sxs-lookup"><span data-stu-id="1b15c-191">Inside of your `js` directory, create a file named `content.js` and add the following code.</span></span>  

```javascript
// get the URL of the page
var url = document.location.href;

// if not on a docs.microsoft.com domain
if (url.indexOf("//docs.microsoft.com") === -1) {
    // send inactive icons
    browser.runtime.sendMessage({
        "iconPath20": "images/inactive20.png",
        "iconPath40": "images/inactive40.png"
    });
}
```  

<span data-ttu-id="1b15c-192">Ce script obtient l’URL de la page active `document.location.href` et vérifie si la page actuelle est sur le domaine [docs.Microsoft.com][MicrosoftDocs] .</span><span class="sxs-lookup"><span data-stu-id="1b15c-192">This script gets the URL of the current page through `document.location.href` and verifies whether the current page is on the [docs.microsoft.com][MicrosoftDocs] domain.</span></span>  <span data-ttu-id="1b15c-193">Si la page n’est pas sur le domaine [docs.Microsoft.com][MicrosoftDocs] \(par exemple  [https://www.bing.com/][|::ref1::|] , \), les chemins d’accès aux icônes inactifs \(icônes grisées \) sont envoyés au script en arrière-plan à l’aide de [Runtime. SendMessage ()][MDNApiRuntimeSendmessage].</span><span class="sxs-lookup"><span data-stu-id="1b15c-193">If the page is not on the [docs.microsoft.com][MicrosoftDocs] domain \(for example  [https://www.bing.com/][|::ref1::|]\), the paths to the inactive icons \(grayed out icons\) are sent to the background script using [runtime.sendMessage()][MDNApiRuntimeSendmessage].</span></span>  

<span data-ttu-id="1b15c-194">Vous devez mettre à jour les [manifest.js][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] du fichier pour inclure la `content_scripts` clé suivante.</span><span class="sxs-lookup"><span data-stu-id="1b15c-194">You must update the [manifest.json][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] file to include the following `content_scripts` key.</span></span>  

```json
  "content_scripts": [{
    "matches": [
        "<all_urls>"
    ],
    "js": ["js/content.js"],
    "run_at": "document_end"
}]
```  

### <span data-ttu-id="1b15c-195">Définitions des clés de manifeste</span><span class="sxs-lookup"><span data-stu-id="1b15c-195">Manifest Key definitions</span></span>  

| <span data-ttu-id="1b15c-196">Clé</span><span class="sxs-lookup"><span data-stu-id="1b15c-196">Key</span></span> | <span data-ttu-id="1b15c-197">Détails</span><span class="sxs-lookup"><span data-stu-id="1b15c-197">Details</span></span> |  
|:--- |:---- |  
| [<span data-ttu-id="1b15c-198">content_scripts</span><span class="sxs-lookup"><span data-stu-id="1b15c-198">content_scripts</span></span>][MDNManifestjsonContentScripts] | <span data-ttu-id="1b15c-199">Contient les informations relatives aux scripts de contenu chargés par le navigateur.</span><span class="sxs-lookup"><span data-stu-id="1b15c-199">Contains the information about which content scripts the browser should load.</span></span> |  

#### <span data-ttu-id="1b15c-200">définitions de clés de content_scripts</span><span class="sxs-lookup"><span data-stu-id="1b15c-200">content_scripts Key definitions</span></span>  

| <span data-ttu-id="1b15c-201">Clé</span><span class="sxs-lookup"><span data-stu-id="1b15c-201">Key</span></span> | <span data-ttu-id="1b15c-202">Détails</span><span class="sxs-lookup"><span data-stu-id="1b15c-202">Details</span></span> |  
|:--- |:---- |  
| `matches` <span data-ttu-id="1b15c-203">\(obligatoire \)</span><span class="sxs-lookup"><span data-stu-id="1b15c-203">\(required\)</span></span> | <span data-ttu-id="1b15c-204">Modèle d’URL à faire correspondre avant de charger le script de contenu.</span><span class="sxs-lookup"><span data-stu-id="1b15c-204">The URL pattern to match prior to loading the content script.</span></span> |  
| `js` | <span data-ttu-id="1b15c-205">Le script qui doit être chargé sur les URL correspondants.</span><span class="sxs-lookup"><span data-stu-id="1b15c-205">The script that should be loaded on matching URLs.</span></span> |  
| `run_at` | <span data-ttu-id="1b15c-206">Spécifie l’emplacement d’insertion des fichiers JavaScript de la `js` clé.</span><span class="sxs-lookup"><span data-stu-id="1b15c-206">Specifies where the JavaScript files from the `js` key are injected.</span></span> |  

<span data-ttu-id="1b15c-207">Ensuite, vous devez créer un [script en arrière-plan][MDNAnatomyExtensionBackgroundScripts].</span><span class="sxs-lookup"><span data-stu-id="1b15c-207">Next, you must create a [background script][MDNAnatomyExtensionBackgroundScripts].</span></span>  <span data-ttu-id="1b15c-208">Les scripts en arrière-plan s’exécutent en arrière-plan du navigateur, s’exécutent indépendamment de la durée de vie d’une fenêtre de navigateur ou de page Web, et sont en mesure de communiquer avec des scripts de contenu.</span><span class="sxs-lookup"><span data-stu-id="1b15c-208">Background scripts run in the background of the browser, run independently of the lifetime of a web page or browser window, and are able to communicate with content scripts.</span></span>  

<span data-ttu-id="1b15c-209">`js`Créez un fichier nommé `background.js` et ajoutez le code suivant à l’intérieur de votre dossier.</span><span class="sxs-lookup"><span data-stu-id="1b15c-209">Inside of your `js` folder, create a file named `background.js` and add the following code.</span></span>  

```javascript
// listen for sendMessage() from content script
browser.runtime.onMessage.addListener(
    function (request, sender, sendResponse) {
        // set the icon for the browser action from sendMessage() in content script
        browser.browserAction.setIcon({
            path: {
                "20": request.iconPath20,
                "40": request.iconPath40
            },
            tabId: sender.tab.id
        });
        // disable browser action for the current tab
        browser.browserAction.disable(sender.tab.id);
    });
```  

<span data-ttu-id="1b15c-210">La méthode [Runtime. onMessage][MDNApiRuntimeOnmessage] écoute pour [Runtime. SendMessage ()][MDNApiRuntimeSendmessage] à partir du script de contenu.</span><span class="sxs-lookup"><span data-stu-id="1b15c-210">The [runtime.onMessage][MDNApiRuntimeOnmessage] method listens for [runtime.sendMessage()][MDNApiRuntimeSendmessage] from the content script.</span></span>  <span data-ttu-id="1b15c-211">Si le domaine de la page n’est pas [docs.Microsoft.com][MicrosoftDocs], la méthode [browserAction. seticon ()][MDNApiBrowseractionSeticon] définit les chemins d’icône vers les images inactives.</span><span class="sxs-lookup"><span data-stu-id="1b15c-211">If the domain of the page is not [docs.microsoft.com][MicrosoftDocs], then [browserAction.setIcon()][MDNApiBrowseractionSeticon] method sets the icon paths to the inactive images.</span></span>  

<span data-ttu-id="1b15c-212">Le script désactive également l’action du navigateur ([browserAction. Disable][MDApiBrowseractionDisable]\), de sorte que les utilisateurs ne puissent pas cliquer sur l’action du navigateur en dehors d’une page de [docs.Microsoft.com][MicrosoftDocs] .</span><span class="sxs-lookup"><span data-stu-id="1b15c-212">The script also disables the browser action \([browserAction.disable][MDApiBrowseractionDisable]\), so that users are not able to click on the browser action outside of a [docs.microsoft.com][MicrosoftDocs] page.</span></span>  

<span data-ttu-id="1b15c-213">Vous devez ajouter le script en arrière-plan à la [manifest.jssur][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] le fichier.</span><span class="sxs-lookup"><span data-stu-id="1b15c-213">You must add the background script to the [manifest.json][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] file.</span></span>  <span data-ttu-id="1b15c-214">Ajoutez la `background` clé suivante à votre manifeste.</span><span class="sxs-lookup"><span data-stu-id="1b15c-214">Add the following `background` key to your manifest.</span></span>  

```json
"background": {
    "scripts": ["js/background.js"],
    "persistent": true
  }
```  

### <span data-ttu-id="1b15c-215">Définitions des clés de manifeste</span><span class="sxs-lookup"><span data-stu-id="1b15c-215">Manifest Key definitions</span></span>  

| <span data-ttu-id="1b15c-216">Clé</span><span class="sxs-lookup"><span data-stu-id="1b15c-216">Key</span></span> | <span data-ttu-id="1b15c-217">Détails</span><span class="sxs-lookup"><span data-stu-id="1b15c-217">Details</span></span>|  
|:--- |:--- |  
| [<span data-ttu-id="1b15c-218">arrière-plan</span><span class="sxs-lookup"><span data-stu-id="1b15c-218">background</span></span>][MDNManifestjsonBackground] | <span data-ttu-id="1b15c-219">Contient les scripts en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="1b15c-219">Contains the background scripts.</span></span> |  

#### <span data-ttu-id="1b15c-220">définitions des touches d’arrière-plan</span><span class="sxs-lookup"><span data-stu-id="1b15c-220">background Key definitions</span></span>  

| <span data-ttu-id="1b15c-221">Clé</span><span class="sxs-lookup"><span data-stu-id="1b15c-221">Key</span></span> | <span data-ttu-id="1b15c-222">Détails</span><span class="sxs-lookup"><span data-stu-id="1b15c-222">Details</span></span> |  
|:--- |:--- |  
| `scripts` | <span data-ttu-id="1b15c-223">Le chemin d’accès à un fichier JavaScript.</span><span class="sxs-lookup"><span data-stu-id="1b15c-223">The path to a JavaScript file.</span></span> |  
| `persistent` <span data-ttu-id="1b15c-224">(obligatoire)</span><span class="sxs-lookup"><span data-stu-id="1b15c-224">(required)</span></span> | <span data-ttu-id="1b15c-225">Ce doit être défini sur `true` ou `false` .</span><span class="sxs-lookup"><span data-stu-id="1b15c-225">This must be set to `true` or `false`.</span></span>  <span data-ttu-id="1b15c-226">S' `true` il est défini sur, le script en arrière-plan est chargé et reste persistant pour la section de navigation entière.</span><span class="sxs-lookup"><span data-stu-id="1b15c-226">If set to `true`, the background script is loaded and persists for the entire browsing section.</span></span>  <span data-ttu-id="1b15c-227">S' `false` il est défini sur, le script en arrière-plan est chargé avec un délai et reste persistant pour la session de navigation.</span><span class="sxs-lookup"><span data-stu-id="1b15c-227">If set to `false`, the background script is loaded with a delay and persists for the browsing session.</span></span> |  

<span data-ttu-id="1b15c-228">Rechargez votre extension et testez à nouveau.</span><span class="sxs-lookup"><span data-stu-id="1b15c-228">Reload your extension and test again.</span></span>  <span data-ttu-id="1b15c-229">Pour recharger votre extension: cliquez sur le **...** pour obtenir les paramètres et plus d’informations dans Microsoft Edge, cliquez sur **Extensions**, cliquez sur votre extension \(**changer de couleur**\), puis cliquez sur **recharger l’extension**.</span><span class="sxs-lookup"><span data-stu-id="1b15c-229">To reload your extension: click the **...** for settings and more in Microsoft Edge, click **Extensions**, click on your extension \(**Color Changer**\), and click **Reload extension**.</span></span>  

<span data-ttu-id="1b15c-230">À présent, ouvrez un nouvel onglet ou actualisez un onglet existant qui n’est pas une page de [docs.Microsoft.com][MicrosoftDocs] .</span><span class="sxs-lookup"><span data-stu-id="1b15c-230">Now, open a new tab or refresh an existing tab that is not a [docs.microsoft.com][MicrosoftDocs] page.</span></span>  <span data-ttu-id="1b15c-231">L’icône inactif doit apparaître et ne pas pouvoir cliquer sur l’action du navigateur.</span><span class="sxs-lookup"><span data-stu-id="1b15c-231">You should see the inactive icon and not be able to click on the browser action.</span></span>  

<span data-ttu-id="1b15c-232">Félicitations!</span><span class="sxs-lookup"><span data-stu-id="1b15c-232">Congratulations!</span></span>  <span data-ttu-id="1b15c-233">Vous avez créé une extension pour Microsoft Edge!</span><span class="sxs-lookup"><span data-stu-id="1b15c-233">You created an extension for Microsoft Edge!</span></span>  <span data-ttu-id="1b15c-234">Affichez l' [exemple complet sur GitHub][GithubMicrosoftEdgeExtensionsDemosColorChanger].</span><span class="sxs-lookup"><span data-stu-id="1b15c-234">View the [full sample on GitHub][GithubMicrosoftEdgeExtensionsDemosColorChanger].</span></span>  <span data-ttu-id="1b15c-235">Poursuivez votre lecture pour en savoir plus sur les extensions.</span><span class="sxs-lookup"><span data-stu-id="1b15c-235">Continue reading to learn more about extensions.</span></span>  

## <span data-ttu-id="1b15c-236">Écrire une extension plus complexe</span><span class="sxs-lookup"><span data-stu-id="1b15c-236">Writing a more complex extension</span></span>  

<span data-ttu-id="1b15c-237">Vous souhaitez écrire une extension plus complexe?</span><span class="sxs-lookup"><span data-stu-id="1b15c-237">Want to write a more complex extension?</span></span>  <span data-ttu-id="1b15c-238">Jetez un coup d’œil à l’extension Beastify sur MDN dans l’article, [votre deuxième extension][MDNYourSecondWebextension].</span><span class="sxs-lookup"><span data-stu-id="1b15c-238">Take a look at the Beastify extension on MDN in the article, [Your second extension][MDNYourSecondWebextension].</span></span>  <span data-ttu-id="1b15c-239">Le modèle d’extension pour Microsoft Edge est légèrement différent du modèle d’extension pour Firefox, l’extension Beastify créée dans [votre deuxième extension][MDNYourSecondWebextension] a été adaptée à la fonction dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1b15c-239">The extension model for Microsoft Edge differs slightly from the extension model for Firefox, the Beastify extension created in [Your second extension][MDNYourSecondWebextension] was adapted to function in Microsoft Edge.</span></span>  <span data-ttu-id="1b15c-240">Consultez-le sur [GitHub][GithubMicrosoftEdgeExtensionsDemosBeastify].</span><span class="sxs-lookup"><span data-stu-id="1b15c-240">Check it out on [GitHub][GithubMicrosoftEdgeExtensionsDemosBeastify].</span></span>  

<span data-ttu-id="1b15c-241">Lorsque vous parcourez l’article sur MDN, [votre deuxième extension][MDNYourSecondWebextension], gardez à l’esprit les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="1b15c-241">While walking through the article on MDN, [Your second extension][MDNYourSecondWebextension], keep in mind the following sections.</span></span>  

### <span data-ttu-id="1b15c-242">API</span><span class="sxs-lookup"><span data-stu-id="1b15c-242">APIs</span></span>  

<span data-ttu-id="1b15c-243">Pour obtenir la liste des API d’extensions prises en charge dans Microsoft Edge, consultez la page [API prises en charge][ExtensionsAPIsupportApis] .</span><span class="sxs-lookup"><span data-stu-id="1b15c-243">See the [Supported APIs][ExtensionsAPIsupportApis] page for a list of supported extensions APIs in Microsoft Edge.</span></span>  

### <span data-ttu-id="1b15c-244">Tailles des icônes</span><span class="sxs-lookup"><span data-stu-id="1b15c-244">Icon sizes</span></span>  

<span data-ttu-id="1b15c-245">Les tailles d’icône de poste par défaut pour Microsoft Edge sont `20px` ,, `25px` `30px` , et `40px` .</span><span class="sxs-lookup"><span data-stu-id="1b15c-245">Preferred extension icon sizes for Microsoft Edge are `20px`, `25px`, `30px`, and `40px`.</span></span>  <span data-ttu-id="1b15c-246">Les autres tailles prises en charge sont `19px` , `35px` et `38px` .</span><span class="sxs-lookup"><span data-stu-id="1b15c-246">Other supported sizes are `19px`, `35px`, and `38px`.</span></span>  <span data-ttu-id="1b15c-247">Pour plus d’informations sur les tailles d’icône et les meilleures pratiques, voir le Guide de [conception][ExtensionsGuidesDesign] .</span><span class="sxs-lookup"><span data-stu-id="1b15c-247">For more info on icon sizes and best practices, see the [Design][ExtensionsGuidesDesign] guide.</span></span>  

### <span data-ttu-id="1b15c-248">JavaScript</span><span class="sxs-lookup"><span data-stu-id="1b15c-248">JavaScript</span></span>  

<span data-ttu-id="1b15c-249">Le modèle d’extension pour Microsoft Edge ne prend pas en charge les promesses JavaScript.</span><span class="sxs-lookup"><span data-stu-id="1b15c-249">The extension model for Microsoft Edge does not support JavaScript Promises.</span></span>  <span data-ttu-id="1b15c-250">Au lieu de cela, utilisez des rappels.</span><span class="sxs-lookup"><span data-stu-id="1b15c-250">Instead, use callbacks.</span></span>  <span data-ttu-id="1b15c-251">Pour consulter d’autres exemples d’utilisation des rappels dans une extension, voir les démonstrations  [impression rapide][GithubMicrosoftEdgeExtensionsDemosQuickPrint] et [échange de texte][GithubMicrosoftEdgeExtensionsDemosTextSwap] .</span><span class="sxs-lookup"><span data-stu-id="1b15c-251">For more examples of using callbacks in an extension, take a look at the  [Quick Print][GithubMicrosoftEdgeExtensionsDemosQuickPrint] and [Text Swap][GithubMicrosoftEdgeExtensionsDemosTextSwap] demos.</span></span>  

<span data-ttu-id="1b15c-252">Passez en revue l’exemple d' [impression rapide][GithubMicrosoftEdgeExtensionsDemosQuickPrint] dans la vidéo suivante.</span><span class="sxs-lookup"><span data-stu-id="1b15c-252">Walk through the [Quick Print][GithubMicrosoftEdgeExtensionsDemosQuickPrint] example in the following video.</span></span>  

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Adding-a-Background-Script-to-you-Edge-Extension/player]  

### <span data-ttu-id="1b15c-253">Manifest.js</span><span class="sxs-lookup"><span data-stu-id="1b15c-253">Manifest.json</span></span>  

*   <span data-ttu-id="1b15c-254">La `author` clé est requise dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1b15c-254">The `author` key is required in Microsoft Edge</span></span>  
*   <span data-ttu-id="1b15c-255">La `activeTab` clé n’est pas prise en charge dans Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1b15c-255">The `activeTab` key is not supported in Microsoft Edge</span></span>  

<span data-ttu-id="1b15c-256">Pour plus d’informations sur les [extensions de navigateur][MDNBrowserExtensions], voir [documents Web MDN][MDNWebDocs].</span><span class="sxs-lookup"><span data-stu-id="1b15c-256">For more information on [Browser Extensions][MDNBrowserExtensions], see [MDN web docs][MDNWebDocs].</span></span>  

<!-- image links -->  

<!--[ImageColorChangerHeader]: ../media/color-changer_header.png "Docs.microsoft.com body changed to blue"  -->  
<!--[ImageColorChangerPopup]: ../media/color-changer_popup.png "The pop-up interface of the extension"  -->  
<!--[ImageColorChangerHeaderAliceblue]: ../media/color-changer_header_aliceblue.png "[Docs.microsoft.com header changed to Aliceblue"  -->  
<!--[ImageColorChangerHeaderCornsilk]: ../media/color-changer_header_cornsilk.png "Docs.microsoft.com header changed to Cornsilk"  -->  

<!-- links -->  

[ExtensionsGuidesAddingRemovingExtensionsAdding]: ./adding-and-removing-extensions.md#adding-an-extension "Ajout d’une extension: ajout, déplacement et suppression d’extensions pour Microsoft Edge | Documents Microsoft"  
[ExtensionsGuidesDebuggingExtensions]: ./debugging-extensions.md "Extensions de débogage | Documents Microsoft"  
[ExtensionsGuidesDesign]: ./design.md "Recommandations en matière de conception pour les extensions Microsoft Edge | Documents Microsoft"  
[ExtensionsGuidesDesignIcons]: ./design.md#icons "Icônes-recommandations en matière de conception pour les extensions Microsoft Edge | Documents Microsoft"  
[ExtensionsAPIsupportApis]: ../api-support/supported-apis.md " API prises en charge Documents Microsoft"  
[ExtensionsApisupportManifestKeys]: ../api-support/supported-manifest-keys.md "Clés de manifeste prises en charge | Documents Microsoft"  

[MicrosoftDocs]: https://docs.microsoft.com "Documents Microsoft"  

[MDNWebDocs]: https://developer.mozilla.org "Documents Web MDN"  
[MDNBrowserExtensions]: https://developer.mozilla.org/Add-ons/WebExtensions "Extensions de navigateur | MDN"  
[MDNAnatomyExtension]: https://developer.mozilla.org/Add-ons/WebExtensions/Anatomy_of_a_WebExtension "Anatomie d’une extension | MDN"  
[MDNAnatomyExtensionBackgroundScripts]: https://developer.mozilla.org/Add-ons/WebExtensions/Anatomy_of_a_WebExtension#Background_scripts "Scripts en arrière-plan-anatomie d’une extension | MDN"  
[MDApiBrowseractionDisable]: https://developer.mozilla.org/Add-ons/WebExtensions/API/browserAction/disable "browserAction. Disable ()-API | MDN" 
[MDNApiBrowseractionSeticon]: https://developer.mozilla.org/Add-ons/WebExtensions/API/browserAction/setIcon "browserAction. setIcon ()-API | MDN"  
[MDNApiRuntimeOnmessage]: https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/onmessage "Runtime. onMessage-API | MDN"  
[MDNApiRuntimeSendmessage]: https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendMessage "Runtime. sendMessage ()-API | MDN"  
[MDNApiTabs]: https://developer.mozilla.org/Add-ons/WebExtensions/API/tabs "onglets-API | MDN"  
[MDNApiTabsInsertcss]: https://developer.mozilla.org/Add-ons/WebExtensions/API/tabs/insertCSS "Tabs. insertCSS ()-API | MDN"  
[MDNContentScripts]: https://developer.mozilla.org/Add-ons/WebExtensions/Content_scripts "Scripts de contenu | MDN"  
[MDNManifestjsonAuthor]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/author "manifest.jsde création sur | MDN"  
[MDNManifestjsonBackground]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/background "arrière-plan-manifest.jssur | MDN"  
[MDNManifestjsonBrowserAction]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/browser_action "browser_action-manifest.jssur | MDN"  
[MDNManifestjsonContentScripts]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/content_scripts "content_scripts-manifest.jssur | MDN"  
[MDNManifestjsonDescription]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/description "Description-manifest.jssur | MDN"  
[MDNManifestjsonIcons]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/icons "icônes-manifest.jssur | MDN"  
[MDNManifestjsonName]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/name "nom-manifest.jssur | MDN"  
[MDNManifestjsonPermissions]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/permissions "autorisations-manifest.jssur | MDN"  
[MDNManifestjsonVersion]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/version "version-manifest.jssur | MDN"  
[MDNYourSecondWebextension]: https://developer.mozilla.org/Add-ons/WebExtensions/Your_second_WebExtension "Votre deuxième extension | MDN"  

[Bing]: https://www.bing.com "Bing"  

[GithubMicrosoftEdgeExtensionsDemosBeastify]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/beastify_edge "Beastify-MicrosoftEdge/MicrosoftEdge-extensions-démonstrations | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosColorChanger]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/color_changer "Changer de couleur-MicrosoftEdge/MicrosoftEdge-extensions-démonstrations | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosColorChangerImages]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/color_changer/images "Images-changement de couleur-MicrosoftEdge/MicrosoftEdge-extensions-démonstrations | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/blob/master/color_changer/manifest.json " MicrosoftEdge/MicrosoftEdge--XX-XX-XX-XXManifest.jsGitHub"  
[GithubMicrosoftEdgeExtensionsDemosQuickPrint]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/quick_print "Impression rapide-MicrosoftEdge/MicrosoftEdge-extensions-démonstrations | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosTextSwap]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/text_swap "Échange de texte-MicrosoftEdge/MicrosoftEdge-extensions-démonstrations | GitHub"  
