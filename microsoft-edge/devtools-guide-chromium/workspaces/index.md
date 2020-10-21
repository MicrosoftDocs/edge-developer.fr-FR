---
description: Découvrez comment enregistrer les modifications apportées dans DevTools sur disque.
title: Modifier des fichiers avec des espaces de travail
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 496bbbb34cdf900d36aa7ebfbf79ad63cdf3e6e7
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125348"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# <span data-ttu-id="8e815-104">Modifier des fichiers avec des espaces de travail</span><span class="sxs-lookup"><span data-stu-id="8e815-104">Edit files with Workspaces</span></span>  

> [!NOTE]
> <span data-ttu-id="8e815-105">L’objectif de ce didacticiel consiste à fournir une pratique pratique pour configurer et utiliser des espaces de travail, afin que vous puissiez utiliser des espaces de travail dans vos propres projets.</span><span class="sxs-lookup"><span data-stu-id="8e815-105">The goal of this tutorial is to provide hands-on practice in setting up and using Workspaces, so that you are able to use Workspaces in your own projects.</span></span>  <span data-ttu-id="8e815-106">Vous pouvez enregistrer les modifications apportées au code source, sur votre ordinateur local, que vous avez effectuées dans DevTools après avoir activé les espaces de travail.</span><span class="sxs-lookup"><span data-stu-id="8e815-106">You are able to save the changes to the source code, on your local computer, that you made within DevTools after you enable Workspaces.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="8e815-107">Éléments **requis**: avant de commencer ce didacticiel, vous devez savoir comment effectuer les opérations suivantes.</span><span class="sxs-lookup"><span data-stu-id="8e815-107">**Prerequisites**: Before beginning this tutorial, you should know how to perform the following actions.</span></span>  
> 
> *   [<span data-ttu-id="8e815-108">Utiliser HTML, CSS et JavaScript pour créer une page Web</span><span class="sxs-lookup"><span data-stu-id="8e815-108">Use html, CSS, and JavaScript to build a web page</span></span>][MDNWebGettingStarted]  
> *   [<span data-ttu-id="8e815-109">Utiliser DevTools pour apporter des modifications de base à CSS</span><span class="sxs-lookup"><span data-stu-id="8e815-109">Use DevTools to make basic changes to CSS</span></span>][DevToolsCssIndex]  
> *   [<span data-ttu-id="8e815-110">Exécuter un serveur Web HTTP local</span><span class="sxs-lookup"><span data-stu-id="8e815-110">Run a local HTTP web server</span></span>][MDNSimpleLocalHTTPServer]  

## <span data-ttu-id="8e815-111">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="8e815-111">Overview</span></span>  

<span data-ttu-id="8e815-112">Les espaces de travail vous permettent d’enregistrer les modifications que vous apportez dans devtools à une copie locale du même fichier sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="8e815-112">Workspaces enable you to save a change that you make in Devtools to a local copy of the same file on your computer.</span></span>  <span data-ttu-id="8e815-113">Pour ce didacticiel, vous devez disposer des paramètres suivants sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="8e815-113">For this tutorial, you should have the following settings on your machine.</span></span>  

*   <span data-ttu-id="8e815-114">Vous avez le code source de votre site sur votre ordinateur de bureau.</span><span class="sxs-lookup"><span data-stu-id="8e815-114">You have the source code for your site on your desktop.</span></span>  
*   <span data-ttu-id="8e815-115">Vous exécutez un serveur Web local à partir du répertoire de code source, afin que le site soit accessible à l’adresse `localhost:8080` .</span><span class="sxs-lookup"><span data-stu-id="8e815-115">You are running a local web server from the source code directory, so that the site is accessible at `localhost:8080`.</span></span>  
*   <span data-ttu-id="8e815-116">Vous avez ouvert `localhost:8080` Microsoft Edge et vous utilisez devtools pour modifier la feuille de style en cascade (CSS) du site.</span><span class="sxs-lookup"><span data-stu-id="8e815-116">You opened `localhost:8080` in Microsoft Edge, and you are using DevTools to change the CSS of the site.</span></span>  

<span data-ttu-id="8e815-117">Lorsque les espaces de travail sont activés, les modifications que vous apportez dans DevTools sont enregistrées dans le code source sur votre ordinateur de bureau.</span><span class="sxs-lookup"><span data-stu-id="8e815-117">With Workspaces enabled, the CSS changes that you make within DevTools are saved to the source code on your desktop.</span></span>  

## <span data-ttu-id="8e815-118">Limitations</span><span class="sxs-lookup"><span data-stu-id="8e815-118">Limitations</span></span>  

<span data-ttu-id="8e815-119">Si vous utilisez une infrastructure moderne, il est probable que vous transformez votre code source en un format facile à mettre en forme, optimisé pour s’exécuter aussi rapidement que possible.</span><span class="sxs-lookup"><span data-stu-id="8e815-119">If you are using a modern framework, it probably transforms your source code from a format that is easy to maintain into a format that is optimized to run as quickly as possible.</span></span>  

<span data-ttu-id="8e815-120">Les espaces de travail sont généralement en mesure de mapper le code optimisé dans votre code source d’origine avec l’aide des [cartes sources][TreehouseBlogSourceMaps].</span><span class="sxs-lookup"><span data-stu-id="8e815-120">Workspaces is usually able to map the optimized code back to your original source code with the help of [source maps][TreehouseBlogSourceMaps].</span></span>  <span data-ttu-id="8e815-121">Néanmoins, il existe un grand nombre de variations entre les infrastructures sur la manière dont chacune utilise les mappages sources.</span><span class="sxs-lookup"><span data-stu-id="8e815-121">But there is a lot of variation between frameworks over how each uses source maps.</span></span>  <span data-ttu-id="8e815-122">Devtools ne prend pas en charge toutes les variations.</span><span class="sxs-lookup"><span data-stu-id="8e815-122">Devtools simply does support all of the variations.</span></span>  

<span data-ttu-id="8e815-123">Les espaces de travail sont connus pour ne pas fonctionner avec l’infrastructure suivante.</span><span class="sxs-lookup"><span data-stu-id="8e815-123">Workspaces is known to not work with the following framework.</span></span>  

*   <span data-ttu-id="8e815-124">Créer une application réactive</span><span class="sxs-lookup"><span data-stu-id="8e815-124">Create React App</span></span>  

    <!-- If you run into issues while using Workspaces with your framework of choice, or you get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  
    
## <span data-ttu-id="8e815-125">Fonctionnalité connexe: substitutions locales</span><span class="sxs-lookup"><span data-stu-id="8e815-125">Related feature: Local overrides</span></span>  

<span data-ttu-id="8e815-126">Les **substitutions locales** sont une autre fonctionnalité devtools similaire aux espaces de travail.</span><span class="sxs-lookup"><span data-stu-id="8e815-126">**Local Overrides** is another DevTools feature that is similar to Workspaces.</span></span>  <span data-ttu-id="8e815-127">Utilisez les substitutions locales lorsque vous voulez tester des modifications apportées à une page, et que vous avez besoin de voir les modifications de chargement de page, mais vous n’avez pas à vous soucier de mapper vos modifications au code source de la page.</span><span class="sxs-lookup"><span data-stu-id="8e815-127">Use Local Overrides when you want to experiment with changes to a page, and you need to see the changes across page loads, but you do not care about mapping your changes to the source code of the page.</span></span>  

<!--Todo: add section when content is ready  -->  

## <span data-ttu-id="8e815-128">Étape 1: configuration</span><span class="sxs-lookup"><span data-stu-id="8e815-128">Step 1: Set up</span></span>  

<span data-ttu-id="8e815-129">Pour bénéficier d’une expérience pratique avec les espaces de travail, effectuez les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="8e815-129">Complete the following actions, to get hands-on experience with Workspaces.</span></span>  

### <span data-ttu-id="8e815-130">Configurer la démonstration</span><span class="sxs-lookup"><span data-stu-id="8e815-130">Set up the demo</span></span>  

1.  <span data-ttu-id="8e815-131">[Ouvrez la démonstration][GlitchWorkspacesDemo].</span><span class="sxs-lookup"><span data-stu-id="8e815-131">[Open the demo][GlitchWorkspacesDemo].</span></span>  <!--In the top-left of the editor, a randomly-generated project name is displayed.  -->  
    
    :::image type="complex" source="../media/workspaces-glitch-workspaces-demo-source.msft.png" alt-text="Projet de problème" lightbox="../media/workspaces-glitch-workspaces-demo-source.msft.png":::
       <span data-ttu-id="8e815-133">Projet de problème</span><span class="sxs-lookup"><span data-stu-id="8e815-133">A Glitch project</span></span>  
    :::image-end:::  
    
    <!--1.  Choose the project name.  -->  
    <!--1.  Choose **Advanced Options** > **Download Project**.  
    
    :::image type="complex" source="../media/workspaces-glitch-advanced-options-download-project.msft.png" alt-text="Projet de problème" lightbox="../media/workspaces-glitch-advanced-options-download-project.msft.png":::
       The Download Project button  
    :::image-end:::  

    -->  
    <!--1.  Close the tab.  -->  
    <!--1.  Unzip the source code and move the unzipped `app` directory to your desktop.  For the rest of this tutorial the unzipped directory is referred to as `~/Desktop/app`.  -->  
    
1.  <span data-ttu-id="8e815-134">Créer un `app` répertoire sur votre ordinateur de bureau.</span><span class="sxs-lookup"><span data-stu-id="8e815-134">Create an `app` directory on your desktop.</span></span>  <span data-ttu-id="8e815-135">Enregistrez des copies des fichiers du `workspaces-demo` répertoire dans l' `app` Annuaire.</span><span class="sxs-lookup"><span data-stu-id="8e815-135">Save copies of the files from the `workspaces-demo` directory to the `app` directory.</span></span>  <span data-ttu-id="8e815-136">Pour le reste du didacticiel, le répertoire est appelé `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="8e815-136">For the rest of the tutorial, the directory is referred to as `~/Desktop/app`.</span></span>  
1.  <span data-ttu-id="8e815-137">Démarrez un serveur Web local dans `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="8e815-137">Start a local web server in `~/Desktop/app`.</span></span>  <span data-ttu-id="8e815-138">Vous trouverez ci-dessous un exemple de code permettant de démarrer `SimpleHTTPServer` , mais vous pouvez utiliser le serveur de votre choix.</span><span class="sxs-lookup"><span data-stu-id="8e815-138">Below is some sample code for starting up `SimpleHTTPServer`, but you may use whatever server you prefer.</span></span>  
    
    :::row:::
       :::column span="":::
          ```bash
          cd ~/Desktop/app
          python -m SimpleHTTPServer # Python 2
          ```  
       :::column-end:::  
       :::column span="":::
          ```bash
          cd ~/Desktop/app
          python -m http.server # Python 3
          ```  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="8e815-139">Ouvrez un onglet dans Microsoft Edge et accédez à la version hébergée localement du site.</span><span class="sxs-lookup"><span data-stu-id="8e815-139">Open a tab in Microsoft Edge and go to locally-hosted version of the site.</span></span>  <span data-ttu-id="8e815-140">Vous devriez être en mesure d’y accéder à l’aide d’une URL telle que `localhost:8080` ou `http://0.0.0.0:8080` .</span><span class="sxs-lookup"><span data-stu-id="8e815-140">You should be able to access it using a URL like `localhost:8080` or `http://0.0.0.0:8080`.</span></span>  <span data-ttu-id="8e815-141">Le [numéro de port][WikiPortURLs] exact est différent.</span><span class="sxs-lookup"><span data-stu-id="8e815-141">The exact [port number][WikiPortURLs] may be different.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo.msft.png" alt-text="Projet de problème" lightbox="../media/workspaces-workspaces-demo.msft.png":::
       <span data-ttu-id="8e815-143">La démonstration</span><span class="sxs-lookup"><span data-stu-id="8e815-143">The demo</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="8e815-144">Configurer DevTools</span><span class="sxs-lookup"><span data-stu-id="8e815-144">Set up DevTools</span></span>  

1.  <span data-ttu-id="8e815-145">Sélectionnez `Control` + `Shift` + `J` \ (Windows, Linux \) ou `Command` + `Option` + `J` \ (MacOS \) pour ouvrir le panneau **console** du devtools.</span><span class="sxs-lookup"><span data-stu-id="8e815-145">Select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\) to open the **Console** panel of DevTools.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-console.msft.png" alt-text="Projet de problème" lightbox="../media/workspaces-workspaces-demo-console.msft.png":::
       <span data-ttu-id="8e815-147">Panneau de la **console**</span><span class="sxs-lookup"><span data-stu-id="8e815-147">The **Console** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="8e815-148">Sélectionnez l’onglet **sources** .</span><span class="sxs-lookup"><span data-stu-id="8e815-148">Choose the **Sources** tab.</span></span>  
1.  <span data-ttu-id="8e815-149">Sélectionnez l’onglet **FileSystem** .</span><span class="sxs-lookup"><span data-stu-id="8e815-149">Choose the **Filesystem** tab.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem.msft.png" alt-text="Projet de problème" lightbox="../media/workspaces-workspaces-demo-sources-filesystem.msft.png":::
       <span data-ttu-id="8e815-151">Onglet **FileSystem**</span><span class="sxs-lookup"><span data-stu-id="8e815-151">The **Filesystem** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="8e815-152">Choisissez **Ajouter un dossier à l’espace de travail**.</span><span class="sxs-lookup"><span data-stu-id="8e815-152">Choose **Add Folder To Workspace**.</span></span>  
1.  <span data-ttu-id="8e815-153">Entrez `~/Desktop/app`.</span><span class="sxs-lookup"><span data-stu-id="8e815-153">Type `~/Desktop/app`.</span></span>  
1.  <span data-ttu-id="8e815-154">Sélectionnez **autoriser** pour accorder à devtools l’autorisation de lecture et d’écriture dans l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="8e815-154">Choose **Allow** to give DevTools permission to read and write to the directory.</span></span>  
    <span data-ttu-id="8e815-155">L’onglet **FileSystem** comporte désormais un point vert en regard de `index.html` , `script.js` et `styles.css` .</span><span class="sxs-lookup"><span data-stu-id="8e815-155">In the **Filesystem** tab, there is now a green dot next to `index.html`, `script.js`, and `styles.css`.</span></span>  <span data-ttu-id="8e815-156">Ces points verts indiquent que DevTools a établi une correspondance entre les ressources réseau de la page et les fichiers de `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="8e815-156">These green dots mean that DevTools has established a mapping between the network resources of the page, and the files in `~/Desktop/app`.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem-folder.msft.png" alt-text="Projet de problème" lightbox="../media/workspaces-workspaces-demo-sources-filesystem-folder.msft.png":::
       <span data-ttu-id="8e815-158">L’onglet **FileSystem** montre désormais un mappage entre les fichiers locaux et les réseaux</span><span class="sxs-lookup"><span data-stu-id="8e815-158">The **Filesystem** tab now shows a mapping between the local files and the network ones</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="8e815-159">Étape 2: enregistrer un changement de CSS sur un disque</span><span class="sxs-lookup"><span data-stu-id="8e815-159">Step 2: Save a CSS change to disk</span></span>  

1.  <span data-ttu-id="8e815-160">Ouvrir `styles.css` .</span><span class="sxs-lookup"><span data-stu-id="8e815-160">Open `styles.css`.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="8e815-161">La `color` propriété d' `h1` éléments est définie sur `fuchsia` .</span><span class="sxs-lookup"><span data-stu-id="8e815-161">The `color` property of `h1` elements is set to `fuchsia`.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem-css.msft.png" alt-text="Projet de problème" lightbox="../media/workspaces-workspaces-demo-sources-filesystem-css.msft.png":::
       <span data-ttu-id="8e815-163">Afficher `styles.css` dans un éditeur de texte</span><span class="sxs-lookup"><span data-stu-id="8e815-163">View `styles.css` in a text editor</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="8e815-164">Sélectionnez l’onglet **éléments** .</span><span class="sxs-lookup"><span data-stu-id="8e815-164">Choose the **Elements** tab.</span></span>  
1.  <span data-ttu-id="8e815-165">Remplacez la valeur de la `color` propriété de l' `<h1>` élément par votre couleur préférée.</span><span class="sxs-lookup"><span data-stu-id="8e815-165">Change the value of the `color` property of the `<h1>` element to your favorite color.</span></span>  
    <span data-ttu-id="8e815-166">N’oubliez pas que vous devez sélectionner l' `<h1>` élément dans l' **arborescence DOM** pour pouvoir voir les règles CSS qui lui sont appliquées dans le volet **styles** .</span><span class="sxs-lookup"><span data-stu-id="8e815-166">Remember that you need to choose the `<h1>` element in the **DOM Tree** in order to see the CSS rules applied to it in the **Styles** pane.</span></span>  <span data-ttu-id="8e815-167">Le point vert en regard `styles.css:1` signifie que toutes les modifications que vous apportez sont mappées `~/Desktop/app/styles.css` .</span><span class="sxs-lookup"><span data-stu-id="8e815-167">The green dot next to `styles.css:1` means that any change that you make are mapped to `~/Desktop/app/styles.css`.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-elements-styles-css.msft.png" alt-text="Projet de problème" lightbox="../media/workspaces-workspaces-demo-elements-styles-css.msft.png":::
       <span data-ttu-id="8e815-169">Un indicateur vert dans lequel le fichier est lié</span><span class="sxs-lookup"><span data-stu-id="8e815-169">The green indicator that the file is linked</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="8e815-170">Ouvrez `styles.css` de nouveau dans un éditeur de texte.</span><span class="sxs-lookup"><span data-stu-id="8e815-170">Open `styles.css` in a text editor again.</span></span>  <span data-ttu-id="8e815-171">La `color` propriété est désormais définie pour votre couleur préférée.</span><span class="sxs-lookup"><span data-stu-id="8e815-171">The `color` property is now set to your favorite color.</span></span>  
1.  <span data-ttu-id="8e815-172">Actualisez la page.</span><span class="sxs-lookup"><span data-stu-id="8e815-172">Refresh the page.</span></span>  <span data-ttu-id="8e815-173">La couleur de l' `<h1>` élément est toujours définie pour votre couleur préférée.</span><span class="sxs-lookup"><span data-stu-id="8e815-173">The color of the `<h1>` element is still set to your favorite color.</span></span>  <span data-ttu-id="8e815-174">Le changement reste au sein d’une actualisation, car lorsque vous avez modifié DevTools enregistré la modification sur le disque.</span><span class="sxs-lookup"><span data-stu-id="8e815-174">The change remains across a refresh, because when you made the change DevTools saved the change to disk.</span></span>  <span data-ttu-id="8e815-175">Ensuite, lorsque vous avez actualisé la page, votre serveur local a desservi la copie modifiée du fichier à partir du disque.</span><span class="sxs-lookup"><span data-stu-id="8e815-175">And then, when you refreshed the page, your local server served the modified copy of the file from disk.</span></span>  
    
## <span data-ttu-id="8e815-176">Étape 3: enregistrer un changement HTML sur le disque</span><span class="sxs-lookup"><span data-stu-id="8e815-176">Step 3: Save an HTML change to disk</span></span>  

### <span data-ttu-id="8e815-177">Changer le code HTML du panneau éléments</span><span class="sxs-lookup"><span data-stu-id="8e815-177">Change HTML from the Elements Panel</span></span>  

<span data-ttu-id="8e815-178">Vous pouvez modifier le code HTML dans le panneau d’éléments, mais vos modifications apportées à l’arborescence DOM ne sont pas enregistrées sur le disque et ne s’appliquent qu’à la session de navigateur actuelle.</span><span class="sxs-lookup"><span data-stu-id="8e815-178">You may make changes to the html from the Element Panel, but your changes to the DOM tree are not saved to disk and only effect the current browser session.</span></span>  

<span data-ttu-id="8e815-179">L’arborescence DOM n’est pas html.</span><span class="sxs-lookup"><span data-stu-id="8e815-179">The DOM tree is not html.</span></span>  

<!--### Try changing HTML from the Elements panel  

> [!WARNING]
> The workflow that you are about to try does not work.  You are trying it now so that you do not waste time later trying to figure out why it is not working.  

1.  Choose the **Elements** tab.  
1.  Choose and edit the text content of the `h1` element, which says `Workspaces Demo`, and replace it with `I ❤️  Cake`.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-change-h1.msft.png" alt-text="Projet de problème" lightbox="../media/workspaces-workspaces-demo-change-h1.msft.png":::
       Attempt to change html from the DOM Tree of the **Elements** panel  
    :::image-end:::  
    
1.  Open `~/Desktop/app/index.html` in a text editor.  The change that you just made does not appear.  
1.  Refresh the page.  The page reverts to the original title.  
    
#### Optional: Why it is not working  

> [!NOTE]
> This section describes why the workflow from [Try changing html from the Elements panel](#try-changing-html-from-the-elements-panel) does not work.  You should skip this section if you do not care why.  

*   The tree of nodes that you see on the **Elements** panel represents the [DOM][MDNWebAPIsDOM] of the page.  
*   To display a page, a browser fetches html over the network, parses the html, and then converts it into a tree of DOM nodes.  
*   If the page has any JavaScript, that JavaScript may add, delete, or change DOM nodes.  CSS may change the DOM, too, using the [`content`][MDNCSSContent] property.  
*   The browser eventually uses the DOM to determine what content it should present to browser users.  
*   Therefore, the final state of the page that users see may be very different from the html that the browser fetched.  
*   This makes it difficult for DevTools to resolve where a change made in the **Elements** panel should be saved, because the DOM is affected by HTML, JavaScript, and CSS.  

In short, the **DOM Tree** `!==` HTML.  
-->  

### <span data-ttu-id="8e815-180">Changer le code HTML dans le panneau sources</span><span class="sxs-lookup"><span data-stu-id="8e815-180">Change HTML from the Sources panel</span></span>  

<span data-ttu-id="8e815-181">Si vous voulez enregistrer une modification apportée au code HTML de la page, utilisez le panneau **sources** .</span><span class="sxs-lookup"><span data-stu-id="8e815-181">If you want to save a change to the html of the page, do it using the **Sources** panel.</span></span>  

1.  <span data-ttu-id="8e815-182">Sélectionnez l’onglet **sources** .</span><span class="sxs-lookup"><span data-stu-id="8e815-182">Choose the **Sources** tab.</span></span>  
1.  <span data-ttu-id="8e815-183">Sélectionnez l’onglet **page** .</span><span class="sxs-lookup"><span data-stu-id="8e815-183">Choose the **Page** tab.</span></span>  
1.  <span data-ttu-id="8e815-184">Choose **(index)**.</span><span class="sxs-lookup"><span data-stu-id="8e815-184">Choose **(index)**.</span></span>  <span data-ttu-id="8e815-185">Le code HTML de la page s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="8e815-185">The HTML for the page opens.</span></span>  
1.  <span data-ttu-id="8e815-186">Remplacer `<h1>Workspaces Demo</h1>` par `<h1>I ❤️  Cake</h1>` .</span><span class="sxs-lookup"><span data-stu-id="8e815-186">Replace `<h1>Workspaces Demo</h1>` with `<h1>I ❤️  Cake</h1>`.</span></span>  <span data-ttu-id="8e815-187">Voir la figure suivante.</span><span class="sxs-lookup"><span data-stu-id="8e815-187">See the following figure.</span></span>  
1.  <span data-ttu-id="8e815-188">Sélectionnez `Control` + `S` \ (Windows, Linux \) ou `Command` + `S` \ (MacOS \) pour enregistrer la modification.</span><span class="sxs-lookup"><span data-stu-id="8e815-188">Select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save the change.</span></span>  
1.  <span data-ttu-id="8e815-189">Actualisez la page.</span><span class="sxs-lookup"><span data-stu-id="8e815-189">Refresh the page.</span></span>  <span data-ttu-id="8e815-190">Le `<h1>` nouveau texte est encore affiché dans l’élément.</span><span class="sxs-lookup"><span data-stu-id="8e815-190">The `<h1>` element is still displaying the new text.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-page-h1.msft.png" alt-text="Projet de problème" lightbox="../media/workspaces-workspaces-demo-sources-page-h1.msft.png":::
       <span data-ttu-id="8e815-192">Changer le code HTML dans le panneau **sources**</span><span class="sxs-lookup"><span data-stu-id="8e815-192">Change HTML from the **Sources** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="8e815-193">Ouvrir `~/Desktop/app/index.html` .</span><span class="sxs-lookup"><span data-stu-id="8e815-193">Open `~/Desktop/app/index.html`.</span></span>  <span data-ttu-id="8e815-194">L' `<h1>` élément contient le nouveau texte.</span><span class="sxs-lookup"><span data-stu-id="8e815-194">The `<h1>` element contains the new text.</span></span>  
    
## <span data-ttu-id="8e815-195">Étape 4: enregistrer un changement JavaScript sur le disque</span><span class="sxs-lookup"><span data-stu-id="8e815-195">Step 4: Save a JavaScript change to disk</span></span>  

<span data-ttu-id="8e815-196">Le panneau **sources** est également l’endroit où il est possible de modifier le langage JavaScript.</span><span class="sxs-lookup"><span data-stu-id="8e815-196">The **Sources** panel is also the place to make changes to JavaScript.</span></span>  <span data-ttu-id="8e815-197">Néanmoins, il est possible que vous ayez besoin d’accéder à d’autres panneaux, comme le panneau **éléments** ou le panneau de la **console** , tout en apportant des modifications à votre site.</span><span class="sxs-lookup"><span data-stu-id="8e815-197">But sometimes you need to access other panels, such as the **Elements** panel or the **Console** panel, while making changes to your site.</span></span>  <span data-ttu-id="8e815-198">Il est possible de faire en sorte que le panneau **sources** s’ouvre avec d’autres panneaux.</span><span class="sxs-lookup"><span data-stu-id="8e815-198">There is a way to have the **Sources** panel open alongside other panels.</span></span>  

1.  <span data-ttu-id="8e815-199">Sélectionnez l’onglet **éléments** .</span><span class="sxs-lookup"><span data-stu-id="8e815-199">Choose the **Elements** tab.</span></span>  
1.  <span data-ttu-id="8e815-200">Sélectionnez `Control` + `Shift` + `P` \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="8e815-200">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  <span data-ttu-id="8e815-201">Le **menu de commandes** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="8e815-201">The **Command Menu** opens.</span></span>  
1.  <span data-ttu-id="8e815-202">Tapez `QS` , puis sélectionnez **afficher la source rapide**.</span><span class="sxs-lookup"><span data-stu-id="8e815-202">Type `QS`, then choose **Show Quick Source**.</span></span>  <span data-ttu-id="8e815-203">Dans la partie inférieure de la fenêtre DevTools, il existe désormais un onglet **source rapide** .  L’onglet affiche le contenu de `index.html` , qui est le dernier fichier que vous avez modifié dans le panneau **sources** .</span><span class="sxs-lookup"><span data-stu-id="8e815-203">At the bottom of your DevTools window there is now a **Quick Source** tab.  The tab is displaying the contents of `index.html`, which is the last file you edited in the **Sources** panel.</span></span>  <span data-ttu-id="8e815-204">L’onglet **source rapide** fournit l’éditeur à partir du panneau **sources** , de sorte que vous pouvez modifier des fichiers en ouvrant d’autres panneaux.</span><span class="sxs-lookup"><span data-stu-id="8e815-204">The **Quick Source** tab gives you the editor from the **Sources** panel, so that you are able to edit files while having other panels open.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-search-show-quick-source.msft.png" alt-text="Projet de problème" lightbox="../media/workspaces-workspaces-demo-search-show-quick-source.msft.png":::
       <span data-ttu-id="8e815-206">Ouvrir l’onglet **source rapide** à l’aide du **menu de commandes**</span><span class="sxs-lookup"><span data-stu-id="8e815-206">Open the **Quick Source** tab using **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="8e815-207">`Control` + `P` `Command` + `P` Pour ouvrir la boîte de dialogue **ouvrir le fichier** , sélectionnez \ (Windows, Linux \) ou \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="8e815-207">Select `Control`+`P` \(Windows, Linux\) or `Command`+`P` \(macOS\) to open the **Open File** dialog.</span></span>  <span data-ttu-id="8e815-208">Voir la figure suivante.</span><span class="sxs-lookup"><span data-stu-id="8e815-208">See the following figure.</span></span>  
1.  <span data-ttu-id="8e815-209">Tapez `script` , puis sélectionnez **app/script.js**.</span><span class="sxs-lookup"><span data-stu-id="8e815-209">Type `script`, then choose **app/script.js**.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-search-script.msft.png" alt-text="Projet de problème" lightbox="../media/workspaces-workspaces-demo-search-script.msft.png":::
       <span data-ttu-id="8e815-211">Ouvrir `script.js` à l’aide de la boîte de dialogue **ouvrir le fichier**</span><span class="sxs-lookup"><span data-stu-id="8e815-211">Open `script.js` using the **Open File** dialog</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="8e815-212">Le `Save Changes To Disk With Workspaces` lien dans la démonstration est appliqué régulièrement.</span><span class="sxs-lookup"><span data-stu-id="8e815-212">The `Save Changes To Disk With Workspaces` link in the demo is styled regularly.</span></span>  
    
1.  <span data-ttu-id="8e815-213">Ajoutez le code suivant en bas de **script.js** à l’aide de l’onglet **source rapide** .</span><span class="sxs-lookup"><span data-stu-id="8e815-213">Add the following code to the bottom of **script.js** using the **Quick Source** tab.</span></span>  
    
    ```javascript
    console.log('greetings from script.js');
    document.querySelector('a').style = 'font-style:italic';
    ```  
    
1.  <span data-ttu-id="8e815-214">Sélectionnez `Control` + `S` \ (Windows, Linux \) ou `Command` + `S` \ (MacOS \) pour enregistrer la modification.</span><span class="sxs-lookup"><span data-stu-id="8e815-214">Select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save the change.</span></span>  
1.  <span data-ttu-id="8e815-215">Actualisez la page.</span><span class="sxs-lookup"><span data-stu-id="8e815-215">Refresh the page.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="8e815-216">Le lien dans la page est désormais mis en italique.</span><span class="sxs-lookup"><span data-stu-id="8e815-216">The link on the page is now italicized.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-elements-styles-quick-source-script.msft.png" alt-text="Projet de problème" lightbox="../media/workspaces-workspaces-demo-elements-styles-quick-source-script.msft.png":::
       <span data-ttu-id="8e815-218">Le lien dans la page est désormais en italique</span><span class="sxs-lookup"><span data-stu-id="8e815-218">The link on the page is now italicized</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="8e815-219">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="8e815-219">Next steps</span></span>  

<span data-ttu-id="8e815-220">Utilisez ce que vous avez appris dans ce didacticiel pour configurer des espaces de travail dans votre projet.</span><span class="sxs-lookup"><span data-stu-id="8e815-220">Use what you have learned in this tutorial to set up Workspaces in your own project.</span></span>  <!-- If you run into any issues or are able to get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  

<!--  
If you have more feedback on the topics or anything else, please use any of the channels below:  

*   [Mailing List][AlphabetGroupsAlphabetBrowserDevTools]  
*   [Twitter][TwitterAlphabetBrowserDevTools]  -->  

## <span data-ttu-id="8e815-221">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="8e815-221">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsCssIndex]: ../css/index.md "Découvrir comment afficher et modifier des feuilles CSS | Documents Microsoft"  

<!--[LocalOverrides]: ../whats-new/2018/01/devtools#overrides -->  

<!--[AlphabetGroupsAlphabetBrowserDevTools]: https://groups.alphabet.com/forum/#!forum/alphabet-browser-developer-tools "Alphabet Browser DevTools - Alphabet Groups"  -->  

[GlitchWorkspacesDemo]: https://glitch.com/edit/#!/microsoft-edge-chromium-devtools?path=workspaces-demo/index.html:1:0 "Fichiers de démonstration des espaces de travail | Problème"  

[MDNCSSContent]: https://developer.mozilla.org/docs/Web/CSS/content "Contenu-CSS: feuilles de style en cascade | MDN"  
[MDNWebGettingStarted]: https://developer.mozilla.org/docs/Learn/Getting_started_with_the_web "Commencer à utiliser le Web | MDN"  
[MDNSimpleLocalHTTPServer]: https://developer.mozilla.org/docs/Learn/Common_questions/set_up_a_local_testing_server#Running_a_simple_local_HTTP_server "Exécution d’un serveur HTTP local simple | MDN"  
[MDNWebAPIsDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Introduction aux DOM-Web API | MDN"  

<!--[StackOverflowAlphabetBrowserDevTools]: https://stackoverflow.com/questions/ask?tags=alphabet-browser-devtools "Alphabet Browser DevTools - Stack Overflow"  -->

[TreehouseBlogSourceMaps]: https://blog.teamtreehouse.com/introduction-source-maps "Introduction aux cartes sources | Blog Treehouse"  

<!-- [TwitterAlphabetBrowserDevTools]: https://twitter.com/alphabetbrowserdevtools "Alphabet Browser DevTools \(@AlphabetBrowserDevTools\) | Twitter"  -->

[WikiPortURLs]: https://en.wikipedia.org/wiki/Port_(computer_networking)#Use_in_URLs "Port \ (réseau d’ordinateurs \)-Wikipédia"  

> [!NOTE]
> <span data-ttu-id="8e815-230">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8e815-230">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="8e815-231">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/workspaces/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="8e815-231">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/workspaces/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="8e815-233">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8e815-233">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
