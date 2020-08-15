---
title: Modifier des fichiers avec des espaces de travail
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/14/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 6971dd96a0d2f32700a8d791f7debfc816887387
ms.sourcegitcommit: 054ad92f0b8f9a15da1e3aed32e8f4379b10860f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/15/2020
ms.locfileid: "10931230"
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

# <span data-ttu-id="3ca8a-103">Modifier des fichiers avec des espaces de travail</span><span class="sxs-lookup"><span data-stu-id="3ca8a-103">Edit files with Workspaces</span></span>  

> [!NOTE]
> <span data-ttu-id="3ca8a-104">L’objectif de ce didacticiel consiste à fournir une pratique pratique pour configurer et utiliser des espaces de travail, afin que vous puissiez utiliser des espaces de travail dans vos propres projets.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-104">The goal of this tutorial is to provide hands-on practice in setting up and using Workspaces, so that you are able to use Workspaces in your own projects.</span></span>  <span data-ttu-id="3ca8a-105">Vous pouvez enregistrer les modifications apportées au code source, sur votre ordinateur local, que vous avez effectuées dans DevTools après avoir activé les espaces de travail.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-105">You are able to save the changes to the source code, on your local computer, that you made within DevTools after you enable Workspaces.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="3ca8a-106">Éléments **requis**: avant de commencer ce didacticiel, vous devez savoir comment effectuer les opérations suivantes.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-106">**Prerequisites**: Before beginning this tutorial, you should know how to perform the following actions.</span></span>  
> 
> *   [<span data-ttu-id="3ca8a-107">Utiliser HTML, CSS et JavaScript pour créer une page Web</span><span class="sxs-lookup"><span data-stu-id="3ca8a-107">Use html, CSS, and JavaScript to build a web page</span></span>][MDNWebGettingStarted]  
> *   [<span data-ttu-id="3ca8a-108">Utiliser DevTools pour apporter des modifications de base à CSS</span><span class="sxs-lookup"><span data-stu-id="3ca8a-108">Use DevTools to make basic changes to CSS</span></span>][DevToolsCssIndex]  
> *   [<span data-ttu-id="3ca8a-109">Exécuter un serveur Web HTTP local</span><span class="sxs-lookup"><span data-stu-id="3ca8a-109">Run a local HTTP web server</span></span>][MDNSimpleLocalHTTPServer]  

## <span data-ttu-id="3ca8a-110">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="3ca8a-110">Overview</span></span>  

<span data-ttu-id="3ca8a-111">Les espaces de travail vous permettent d’enregistrer les modifications que vous apportez dans devtools à une copie locale du même fichier sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-111">Workspaces enable you to save a change that you make in Devtools to a local copy of the same file on your computer.</span></span>  <span data-ttu-id="3ca8a-112">Pour ce didacticiel, vous devez disposer des paramètres suivants sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-112">For this tutorial, you should have the following settings on your machine.</span></span>  

*   <span data-ttu-id="3ca8a-113">Vous avez le code source de votre site sur votre ordinateur de bureau.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-113">You have the source code for your site on your desktop.</span></span>  
*   <span data-ttu-id="3ca8a-114">Vous exécutez un serveur Web local à partir du répertoire de code source, afin que le site soit accessible à l’adresse `localhost:8080` .</span><span class="sxs-lookup"><span data-stu-id="3ca8a-114">You are running a local web server from the source code directory, so that the site is accessible at `localhost:8080`.</span></span>  
*   <span data-ttu-id="3ca8a-115">Vous avez ouvert `localhost:8080` Microsoft Edge et vous utilisez devtools pour modifier la feuille de style en cascade (CSS) du site.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-115">You opened `localhost:8080` in Microsoft Edge, and you are using DevTools to change the CSS of the site.</span></span>  

<span data-ttu-id="3ca8a-116">Lorsque les espaces de travail sont activés, les modifications que vous apportez dans DevTools sont enregistrées dans le code source sur votre ordinateur de bureau.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-116">With Workspaces enabled, the CSS changes that you make within DevTools are saved to the source code on your desktop.</span></span>  

## <span data-ttu-id="3ca8a-117">Limitations</span><span class="sxs-lookup"><span data-stu-id="3ca8a-117">Limitations</span></span>  

<span data-ttu-id="3ca8a-118">Si vous utilisez une infrastructure moderne, il est probable que vous transformez votre code source en un format facile à mettre en forme, optimisé pour s’exécuter aussi rapidement que possible.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-118">If you are using a modern framework, it probably transforms your source code from a format that is easy to maintain into a format that is optimized to run as quickly as possible.</span></span>  

<span data-ttu-id="3ca8a-119">Les espaces de travail sont généralement en mesure de mapper le code optimisé dans votre code source d’origine avec l’aide des [cartes sources][TreehouseBlogSourceMaps].</span><span class="sxs-lookup"><span data-stu-id="3ca8a-119">Workspaces is usually able to map the optimized code back to your original source code with the help of [source maps][TreehouseBlogSourceMaps].</span></span>  <span data-ttu-id="3ca8a-120">Néanmoins, il existe un grand nombre de variations entre les infrastructures sur la manière dont chacune utilise les mappages sources.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-120">But there is a lot of variation between frameworks over how each uses source maps.</span></span>  <span data-ttu-id="3ca8a-121">Devtools ne prend pas en charge toutes les variations.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-121">Devtools simply does support all of the variations.</span></span>  

<span data-ttu-id="3ca8a-122">Les espaces de travail sont connus pour ne pas fonctionner avec l’infrastructure suivante.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-122">Workspaces is known to not work with the following framework.</span></span>  

*   <span data-ttu-id="3ca8a-123">Créer une application réactive</span><span class="sxs-lookup"><span data-stu-id="3ca8a-123">Create React App</span></span>  
    
    <!-- If you run into issues while using Workspaces with your framework of choice, or you get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  
    
## <span data-ttu-id="3ca8a-124">Fonctionnalité connexe: substitutions locales</span><span class="sxs-lookup"><span data-stu-id="3ca8a-124">Related feature: Local overrides</span></span>  

<span data-ttu-id="3ca8a-125">Les **substitutions locales** sont une autre fonctionnalité devtools similaire aux espaces de travail.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-125">**Local Overrides** is another DevTools feature that is similar to Workspaces.</span></span>  <span data-ttu-id="3ca8a-126">Utilisez les substitutions locales lorsque vous voulez tester des modifications apportées à une page, et que vous avez besoin de voir les modifications de chargement de page, mais vous n’avez pas à vous soucier de mapper vos modifications au code source de la page.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-126">Use Local Overrides when you want to experiment with changes to a page, and you need to see the changes across page loads, but you do not care about mapping your changes to the source code of the page.</span></span>  

<!--Todo: add section when content is ready  -->  

## <span data-ttu-id="3ca8a-127">Étape 1: configuration</span><span class="sxs-lookup"><span data-stu-id="3ca8a-127">Step 1: Set up</span></span>  

<span data-ttu-id="3ca8a-128">Pour bénéficier d’une expérience pratique avec les espaces de travail, effectuez les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-128">Complete the following actions, to get hands-on experience with Workspaces.</span></span>  

### <span data-ttu-id="3ca8a-129">Configurer la démonstration</span><span class="sxs-lookup"><span data-stu-id="3ca8a-129">Set up the demo</span></span>  

1.  <span data-ttu-id="3ca8a-130">[Ouvrez la démonstration][GlitchWorkspacesDemo].</span><span class="sxs-lookup"><span data-stu-id="3ca8a-130">[Open the demo][GlitchWorkspacesDemo].</span></span>  <!--In the top-left of the editor, a randomly-generated project name is displayed.  -->  
    
    :::image type="complex" source="../media/workspaces-glitch-workspaces-demo-source.msft.png" alt-text="Projet de problème" lightbox="../media/workspaces-glitch-workspaces-demo-source.msft.png":::
       <span data-ttu-id="3ca8a-132">Projet de problème</span><span class="sxs-lookup"><span data-stu-id="3ca8a-132">A Glitch project</span></span>  
    :::image-end:::  
    
    <!--1.  Choose the project name.  -->  
    <!--1.  Select **Advanced Options** > **Download Project**.  
    
    :::image type="complex" source="../media/workspaces-glitch-advanced-options-download-project.msft.png" alt-text="The Download Project button" lightbox="../media/workspaces-glitch-advanced-options-download-project.msft.png":::
       The Download Project button  
    :::image-end:::  

    -->  
    <!--1.  Close the tab.  -->  
    <!--1.  Unzip the source code and move the unzipped `app` directory to your desktop.  For the rest of this tutorial the unzipped  directory is referred to as `~/Desktop/app`.  -->  
    
1.  <span data-ttu-id="3ca8a-133">Créer un `app` répertoire sur votre ordinateur de bureau.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-133">Create an `app` directory on your desktop.</span></span>  <span data-ttu-id="3ca8a-134">Enregistrez des copies des fichiers du `workspaces-demo` répertoire dans l' `app` Annuaire.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-134">Save copies of the files from the `workspaces-demo` directory to the `app` directory.</span></span>  <span data-ttu-id="3ca8a-135">Pour le reste du didacticiel, le répertoire est appelé `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="3ca8a-135">For the rest of the tutorial ,the directory is referred to as `~/Desktop/app`.</span></span>  
1.  <span data-ttu-id="3ca8a-136">Démarrez un serveur Web local dans `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="3ca8a-136">Start a local web server in `~/Desktop/app`.</span></span>  <span data-ttu-id="3ca8a-137">Vous trouverez ci-dessous un exemple de code permettant de démarrer `SimpleHTTPServer` , mais vous pouvez utiliser le serveur de votre choix.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-137">Below is some sample code for starting up `SimpleHTTPServer`, but you may use whatever server you prefer.</span></span>  
    
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
    
1.  <span data-ttu-id="3ca8a-138">Ouvrez un onglet dans Microsoft Edge et accédez à la version hébergée localement du site.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-138">Open a tab in Microsoft Edge and go to locally-hosted version of the site.</span></span>  <span data-ttu-id="3ca8a-139">Vous devriez être en mesure d’y accéder à l’aide d’une URL telle que `localhost:8080` ou `http://0.0.0.0:8080` .</span><span class="sxs-lookup"><span data-stu-id="3ca8a-139">You should be able to access it using a URL like `localhost:8080` or `http://0.0.0.0:8080`.</span></span>  <span data-ttu-id="3ca8a-140">Le [numéro de port][WikiPortURLs] exact est différent.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-140">The exact [port number][WikiPortURLs] may be different.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo.msft.png" alt-text="La démonstration" lightbox="../media/workspaces-workspaces-demo.msft.png":::
       <span data-ttu-id="3ca8a-142">La démonstration</span><span class="sxs-lookup"><span data-stu-id="3ca8a-142">The demo</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="3ca8a-143">Configurer DevTools</span><span class="sxs-lookup"><span data-stu-id="3ca8a-143">Set up DevTools</span></span>  

1.  <span data-ttu-id="3ca8a-144">Sélectionnez `Control` + `Shift` + `J` \ (Windows \) ou `Command` + `Option` + `J` \ (MacOS \) pour ouvrir le panneau **console** de devtools.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-144">Select `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\) to open the **Console** panel of DevTools.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-console.msft.png" alt-text="Panneau de la console" lightbox="../media/workspaces-workspaces-demo-console.msft.png":::
       <span data-ttu-id="3ca8a-146">Panneau de la **console**</span><span class="sxs-lookup"><span data-stu-id="3ca8a-146">The **Console** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3ca8a-147">Sélectionnez l’onglet **sources** .</span><span class="sxs-lookup"><span data-stu-id="3ca8a-147">Choose the **Sources** tab.</span></span>  
1.  <span data-ttu-id="3ca8a-148">Sélectionnez l’onglet **FileSystem** .</span><span class="sxs-lookup"><span data-stu-id="3ca8a-148">Choose the **Filesystem** tab.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem.msft.png" alt-text="Onglet FileSystem" lightbox="../media/workspaces-workspaces-demo-sources-filesystem.msft.png":::
       <span data-ttu-id="3ca8a-150">Onglet **FileSystem**</span><span class="sxs-lookup"><span data-stu-id="3ca8a-150">The **Filesystem** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3ca8a-151">Choisissez **Ajouter un dossier à l’espace de travail**.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-151">Choose **Add Folder To Workspace**.</span></span>  
1.  <span data-ttu-id="3ca8a-152">Entrée `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="3ca8a-152">Enter `~/Desktop/app`.</span></span>  
1.  <span data-ttu-id="3ca8a-153">Sélectionnez **autoriser** pour accorder à devtools l’autorisation de lecture et d’écriture dans l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-153">Choose **Allow** to give DevTools permission to read and write to the directory.</span></span>  
    <span data-ttu-id="3ca8a-154">L’onglet **FileSystem** comporte désormais un point vert en regard de `index.html` , `script.js` et `styles.css` .</span><span class="sxs-lookup"><span data-stu-id="3ca8a-154">In the **Filesystem** tab, there is now a green dot next to `index.html`, `script.js`, and `styles.css`.</span></span>  <span data-ttu-id="3ca8a-155">Ces points verts indiquent que DevTools a établi une correspondance entre les ressources réseau de la page et les fichiers de `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="3ca8a-155">These green dots mean that DevTools has established a mapping between the network resources of the page, and the files in `~/Desktop/app`.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem-folder.msft.png" alt-text="L’onglet FileSystem montre désormais un mappage entre les fichiers locaux et les réseaux" lightbox="../media/workspaces-workspaces-demo-sources-filesystem-folder.msft.png":::
       <span data-ttu-id="3ca8a-157">L’onglet **FileSystem** montre désormais un mappage entre les fichiers locaux et les réseaux</span><span class="sxs-lookup"><span data-stu-id="3ca8a-157">The **Filesystem** tab now shows a mapping between the local files and the network ones</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="3ca8a-158">Étape 2: enregistrer un changement de CSS sur un disque</span><span class="sxs-lookup"><span data-stu-id="3ca8a-158">Step 2: Save a CSS change to disk</span></span>  

1.  <span data-ttu-id="3ca8a-159">Ouvrir `styles.css` .</span><span class="sxs-lookup"><span data-stu-id="3ca8a-159">Open `styles.css`.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="3ca8a-160">La `color` propriété d' `h1` éléments est définie sur `fuchsia` .</span><span class="sxs-lookup"><span data-stu-id="3ca8a-160">The `color` property of `h1` elements is set to `fuchsia`.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem-css.msft.png" alt-text="Afficher les styles. CSS dans un éditeur de texte" lightbox="../media/workspaces-workspaces-demo-sources-filesystem-css.msft.png":::
       <span data-ttu-id="3ca8a-162">Afficher `styles.css` dans un éditeur de texte</span><span class="sxs-lookup"><span data-stu-id="3ca8a-162">View `styles.css` in a text editor</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3ca8a-163">Sélectionnez l’onglet **éléments** .</span><span class="sxs-lookup"><span data-stu-id="3ca8a-163">Choose the **Elements** tab.</span></span>  
1.  <span data-ttu-id="3ca8a-164">Remplacez la valeur de la `color` propriété de l' `<h1>` élément par votre couleur préférée.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-164">Change the value of the `color` property of the `<h1>` element to your favorite color.</span></span>  
    <span data-ttu-id="3ca8a-165">N’oubliez pas que vous devez sélectionner l' `<h1>` élément dans l' **arborescence DOM** pour pouvoir voir les règles CSS qui lui sont appliquées dans le volet **styles** .</span><span class="sxs-lookup"><span data-stu-id="3ca8a-165">Remember that you need to choose the `<h1>` element in the **DOM Tree** in order to see the CSS rules applied to it in the **Styles** pane.</span></span>  <span data-ttu-id="3ca8a-166">Le point vert en regard `styles.css:1` signifie que toutes les modifications que vous apportez sont mappées `~/Desktop/app/styles.css` .</span><span class="sxs-lookup"><span data-stu-id="3ca8a-166">The green dot next to `styles.css:1` means that any change that you make are mapped to `~/Desktop/app/styles.css`.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-elements-styles-css.msft.png" alt-text="Un indicateur vert dans lequel le fichier est lié" lightbox="../media/workspaces-workspaces-demo-elements-styles-css.msft.png":::
       <span data-ttu-id="3ca8a-168">Un indicateur vert dans lequel le fichier est lié</span><span class="sxs-lookup"><span data-stu-id="3ca8a-168">The green indicator that the file is linked</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3ca8a-169">Ouvrez `styles.css` de nouveau dans un éditeur de texte.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-169">Open `styles.css` in a text editor again.</span></span>  <span data-ttu-id="3ca8a-170">La `color` propriété est désormais définie pour votre couleur préférée.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-170">The `color` property is now set to your favorite color.</span></span>  
1.  <span data-ttu-id="3ca8a-171">Actualisez la page.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-171">Refresh the page.</span></span>  <span data-ttu-id="3ca8a-172">La couleur de l' `<h1>` élément est toujours définie pour votre couleur préférée.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-172">The color of the `<h1>` element is still set to your favorite color.</span></span>  <span data-ttu-id="3ca8a-173">Le changement opéré sur une actualisation, car lorsque vous avez effectué le changement DevTools enregistré la modification sur le disque.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-173">The change across a refresh, because when you made the change DevTools saved the change to disk.</span></span>  <span data-ttu-id="3ca8a-174">Ensuite, lorsque vous avez actualisé la page, votre serveur local a desservi la copie modifiée du fichier à partir du disque.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-174">And then, when you refreshed the page, your local server served the modified copy of the file from disk.</span></span>  
    
## <span data-ttu-id="3ca8a-175">Étape 3: enregistrer un changement HTML sur le disque</span><span class="sxs-lookup"><span data-stu-id="3ca8a-175">Step 3: Save an HTML change to disk</span></span>  

### <span data-ttu-id="3ca8a-176">Changer le code HTML du panneau éléments</span><span class="sxs-lookup"><span data-stu-id="3ca8a-176">Change HTML from the Elements Panel</span></span>  

<span data-ttu-id="3ca8a-177">Vous pouvez modifier le code HTML dans le panneau d’éléments, mais vos modifications apportées à l’arborescence DOM ne sont pas enregistrées sur le disque et ne s’appliquent qu’à la session de navigateur actuelle.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-177">You may make changes to the html from the Element Panel, but your changes to the DOM tree are not saved to disk and only effect the current browser session.</span></span>  

<span data-ttu-id="3ca8a-178">L’arborescence DOM n’est pas html.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-178">The DOM tree is not html.</span></span>  

<!--### Try changing HTML from the Elements panel  

> [!WARNING]
> The workflow that you are about to try does not work.  You are trying it now so that you do not waste time later trying to figure out why it is not working.  

1.  Choose the **Elements** tab.  
1.  Choose and edit the text content of the `h1` element, which says `Workspaces Demo`, and replace it with `I ❤️  Cake`.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-change-h1.msft.png" alt-text="Attempt to change html from the DOM Tree of the Elements panel" lightbox="../media/workspaces-workspaces-demo-change-h1.msft.png":::
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

### <span data-ttu-id="3ca8a-179">Changer le code HTML dans le panneau sources</span><span class="sxs-lookup"><span data-stu-id="3ca8a-179">Change HTML from the Sources panel</span></span>  

<span data-ttu-id="3ca8a-180">Si vous voulez enregistrer une modification apportée au code HTML de la page, utilisez le panneau **sources** .</span><span class="sxs-lookup"><span data-stu-id="3ca8a-180">If you want to save a change to the html of the page, do it using the **Sources** panel.</span></span>  

1.  <span data-ttu-id="3ca8a-181">Sélectionnez l’onglet **sources** .</span><span class="sxs-lookup"><span data-stu-id="3ca8a-181">Choose the **Sources** tab.</span></span>  
1.  <span data-ttu-id="3ca8a-182">Sélectionnez l’onglet **page** .</span><span class="sxs-lookup"><span data-stu-id="3ca8a-182">Choose the **Page** tab.</span></span>  
1.  <span data-ttu-id="3ca8a-183">Choose **(index)**.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-183">Choose **(index)**.</span></span>  <span data-ttu-id="3ca8a-184">Le code HTML de la page s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-184">The HTML for the page opens.</span></span>  
1.  <span data-ttu-id="3ca8a-185">Remplacer `<h1>Workspaces Demo</h1>` par `<h1>I ❤️  Cake</h1>` .</span><span class="sxs-lookup"><span data-stu-id="3ca8a-185">Replace `<h1>Workspaces Demo</h1>` with `<h1>I ❤️  Cake</h1>`.</span></span>  <span data-ttu-id="3ca8a-186">Voir la figure suivante.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-186">See the following figure.</span></span>  
1.  <span data-ttu-id="3ca8a-187">Sélectionnez `Control` + `S` \ (Windows \) ou `Command` + `S` \ (MacOS \) pour enregistrer la modification.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-187">Select `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save the change.</span></span>  
1.  <span data-ttu-id="3ca8a-188">Actualisez la page.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-188">Refresh the page.</span></span>  <span data-ttu-id="3ca8a-189">Le `<h1>` nouveau texte est encore affiché dans l’élément.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-189">The `<h1>` element is still displaying the new text.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-page-h1.msft.png" alt-text="Changer le code HTML dans le panneau sources" lightbox="../media/workspaces-workspaces-demo-sources-page-h1.msft.png":::
       <span data-ttu-id="3ca8a-191">La ligne 12 est définie sur</span><span class="sxs-lookup"><span data-stu-id="3ca8a-191">Line 12 is set to</span></span> `I ❤️  Cake`  
    :::image-end:::  
    
1.  <span data-ttu-id="3ca8a-192">Ouvrir `~/Desktop/app/index.html` .</span><span class="sxs-lookup"><span data-stu-id="3ca8a-192">Open `~/Desktop/app/index.html`.</span></span>  <span data-ttu-id="3ca8a-193">L' `<h1>` élément contient le nouveau texte.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-193">The `<h1>` element contains the new text.</span></span>  
    
## <span data-ttu-id="3ca8a-194">Étape 4: enregistrer un changement JavaScript sur le disque</span><span class="sxs-lookup"><span data-stu-id="3ca8a-194">Step 4: Save a JavaScript change to disk</span></span>  

<span data-ttu-id="3ca8a-195">Le panneau **sources** est également l’endroit où il est possible de modifier le langage JavaScript.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-195">The **Sources** panel is also the place to make changes to JavaScript.</span></span>  <span data-ttu-id="3ca8a-196">Néanmoins, il est possible que vous ayez besoin d’accéder à d’autres panneaux, comme le panneau **éléments** ou le panneau de la **console** , tout en apportant des modifications à votre site.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-196">But sometimes you need to access other panels, such as the **Elements** panel or the **Console** panel, while making changes to your site.</span></span>  <span data-ttu-id="3ca8a-197">Il est possible de faire en sorte que le panneau **sources** s’ouvre avec d’autres panneaux.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-197">There is a way to have the **Sources** panel open alongside other panels.</span></span>  

1.  <span data-ttu-id="3ca8a-198">Sélectionnez l’onglet **éléments** .</span><span class="sxs-lookup"><span data-stu-id="3ca8a-198">Choose the **Elements** tab.</span></span>  
1.  <span data-ttu-id="3ca8a-199">Sélectionnez `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="3ca8a-199">Select `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  <span data-ttu-id="3ca8a-200">Le **menu de commandes** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-200">The **Command Menu** opens.</span></span>  
1.  <span data-ttu-id="3ca8a-201">Tapez `QS` , puis sélectionnez **afficher la source rapide**.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-201">Type `QS`, then select **Show Quick Source**.</span></span>  <span data-ttu-id="3ca8a-202">Dans la partie inférieure de la fenêtre DevTools, il existe désormais un onglet **source rapide** .  L’onglet affiche le contenu de `index.html` , qui est le dernier fichier que vous avez modifié dans le panneau **sources** .</span><span class="sxs-lookup"><span data-stu-id="3ca8a-202">At the bottom of your DevTools window there is now a **Quick Source** tab.  The tab is displaying the contents of `index.html`, which is the last file you edited in the **Sources** panel.</span></span>  <span data-ttu-id="3ca8a-203">L’onglet **source rapide** fournit l’éditeur à partir du panneau **sources** , de sorte que vous pouvez modifier des fichiers en ouvrant d’autres panneaux.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-203">The **Quick Source** tab gives you the editor from the **Sources** panel, so that you are able to edit files while having other panels open.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-search-show-quick-source.msft.png" alt-text="Ouvrir l’onglet source rapide à l’aide du menu de commandes" lightbox="../media/workspaces-workspaces-demo-search-show-quick-source.msft.png":::
       <span data-ttu-id="3ca8a-205">Ouvrir l’onglet **source rapide** à l’aide du **menu de commandes**</span><span class="sxs-lookup"><span data-stu-id="3ca8a-205">Open the **Quick Source** tab using **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3ca8a-206">`Control` + `P` `Command` + `P` Pour ouvrir la boîte de dialogue **ouvrir le fichier** , sélectionnez \ (Windows \) ou \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="3ca8a-206">Select `Control`+`P` \(Windows\) or `Command`+`P` \(macOS\) to open the **Open File** dialog.</span></span>  <span data-ttu-id="3ca8a-207">Voir la figure suivante.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-207">See the following figure.</span></span>  
1.  <span data-ttu-id="3ca8a-208">Tapez `script` , puis sélectionnez **app/script.js**.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-208">Type `script`, then select **app/script.js**.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-search-script.msft.png" alt-text="Ouvrir script.js à l’aide de la boîte de dialogue Ouvrir le fichier" lightbox="../media/workspaces-workspaces-demo-search-script.msft.png":::
       <span data-ttu-id="3ca8a-210">Ouvrir `script.js` à l’aide de la boîte de dialogue **ouvrir le fichier**</span><span class="sxs-lookup"><span data-stu-id="3ca8a-210">Open `script.js` using the **Open File** dialog</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="3ca8a-211">Le `Save Changes To Disk With Workspaces` lien dans la démonstration est appliqué régulièrement.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-211">The `Save Changes To Disk With Workspaces` link in the demo is styled regularly.</span></span>  
    
1.  <span data-ttu-id="3ca8a-212">Ajoutez le code suivant en bas de **script.js** à l’aide de l’onglet **source rapide** .</span><span class="sxs-lookup"><span data-stu-id="3ca8a-212">Add the following code to the bottom of **script.js** using the **Quick Source** tab.</span></span>  
    
    ```javascript
    console.log('greetings from script.js');
    document.querySelector('a').style = 'font-style:italic';
    ```  
    
1.  <span data-ttu-id="3ca8a-213">Sélectionnez `Control` + `S` \ (Windows \) ou `Command` + `S` \ (MacOS \) pour enregistrer la modification.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-213">Select `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save the change.</span></span>  
1.  <span data-ttu-id="3ca8a-214">Actualisez la page.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-214">Refresh the page.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="3ca8a-215">Le lien dans la page est désormais mis en italique.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-215">The link on the page is now italicized.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-elements-styles-quick-source-script.msft.png" alt-text="Le lien dans la page est désormais en italique" lightbox="../media/workspaces-workspaces-demo-elements-styles-quick-source-script.msft.png":::
       <span data-ttu-id="3ca8a-217">Le lien dans la page est désormais en italique</span><span class="sxs-lookup"><span data-stu-id="3ca8a-217">The link on the page is now italicized</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="3ca8a-218">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="3ca8a-218">Next steps</span></span>  

<span data-ttu-id="3ca8a-219">Utilisez ce que vous avez appris dans ce didacticiel pour configurer des espaces de travail dans votre projet.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-219">Use what you have learned in this tutorial to set up Workspaces in your own project.</span></span>  <!-- If you run into any issues or are able to get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  

<!--  
If you have more feedback on the topics or anything else, please use any of the channels below:  

*   [Mailing List][AlphabetGroupsAlphabetBrowserDevTools]  
*   [Twitter][TwitterAlphabetBrowserDevTools]  
    -->  

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
> <span data-ttu-id="3ca8a-228">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3ca8a-228">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="3ca8a-229">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/workspaces/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="3ca8a-229">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/workspaces/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="3ca8a-231">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3ca8a-231">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
