---
description: Découvrez comment enregistrer les modifications apportées dans DevTools sur le disque.
title: Modifier des fichiers avec les espaces de travail
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 640bb80e01f776c763af053cf8354ce90cf52e93
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564664"
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
# <a name="edit-files-with-workspaces"></a><span data-ttu-id="b9f2d-104">Modifier des fichiers avec les espaces de travail</span><span class="sxs-lookup"><span data-stu-id="b9f2d-104">Edit files with Workspaces</span></span>  

<span data-ttu-id="b9f2d-105">Ce didacticiel fournit des pratiques pratiques sur la configuration et l’utilisation d’un espace de travail.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-105">This tutorial provides hands-on practice in setting up and using a Workspace.</span></span>  <span data-ttu-id="b9f2d-106">Une fois que vous avez ajouté des fichiers à un espace de travail, les modifications que vous a faites dans votre code source dans DevTools sont enregistrées sur votre ordinateur local et sont conservées après l’actualisation de la page web.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-106">After you add files to a Workspace, the changes that you make in your source code within DevTools are saved on your local computer, and are preserved after you refresh the webpage.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="b9f2d-107">**Conditions préalables**: avant de commencer ce didacticiel, vous devez savoir comment effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-107">**Prerequisites**: Before beginning this tutorial, you should know how to perform the following actions.</span></span>  
> 
> *   [<span data-ttu-id="b9f2d-108">Utiliser html, CSS et JavaScript pour créer une page web</span><span class="sxs-lookup"><span data-stu-id="b9f2d-108">Use html, CSS, and JavaScript to build a web page</span></span>][MDNWebGettingStarted]  
> *   [<span data-ttu-id="b9f2d-109">Utiliser DevTools pour apporter des modifications de base à CSS</span><span class="sxs-lookup"><span data-stu-id="b9f2d-109">Use DevTools to make basic changes to CSS</span></span>][DevToolsCssIndex]  
> *   [<span data-ttu-id="b9f2d-110">Exécuter un serveur web HTTP local</span><span class="sxs-lookup"><span data-stu-id="b9f2d-110">Run a local HTTP web server</span></span>][MDNSimpleLocalHTTPServer]  

## <a name="overview"></a><span data-ttu-id="b9f2d-111">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="b9f2d-111">Overview</span></span>  

<span data-ttu-id="b9f2d-112">Les espaces de travail vous permettent d’enregistrer une modification que vous a faites dans Devtools sur une copie locale du même fichier sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-112">Workspaces enable you to save a change that you make in Devtools to a local copy of the same file on your computer.</span></span>  <span data-ttu-id="b9f2d-113">Pour ce didacticiel, vous devez avoir les paramètres suivants sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-113">For this tutorial, you should have the following settings on your machine.</span></span>  

*   <span data-ttu-id="b9f2d-114">Vous avez le code source de votre site sur votre bureau.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-114">You have the source code for your site on your desktop.</span></span>  
*   <span data-ttu-id="b9f2d-115">Vous exécutez un serveur web local à partir du répertoire de code source, afin que le site soit accessible à l’adresse `localhost:8080` .</span><span class="sxs-lookup"><span data-stu-id="b9f2d-115">You are running a local web server from the source code directory, so that the site is accessible at `localhost:8080`.</span></span>  
*   <span data-ttu-id="b9f2d-116">Vous avez ouvert dans Microsoft Edge, et vous utilisez DevTools pour modifier le `localhost:8080` CSS du site.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-116">You opened `localhost:8080` in Microsoft Edge, and you are using DevTools to change the CSS of the site.</span></span>  

<span data-ttu-id="b9f2d-117">Une fois les espaces de travail activés, les modifications CSS que vous a faites dans DevTools sont enregistrées dans le code source sur votre bureau.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-117">With Workspaces enabled, the CSS changes that you make within DevTools are saved to the source code on your desktop.</span></span>  

## <a name="limitations"></a><span data-ttu-id="b9f2d-118">Limitations</span><span class="sxs-lookup"><span data-stu-id="b9f2d-118">Limitations</span></span>  

<span data-ttu-id="b9f2d-119">Si vous utilisez une infrastructure moderne, il transforme probablement votre code source à partir d’un format facile à gérer dans un format optimisé pour s’exécuter aussi rapidement que possible.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-119">If you are using a modern framework, it probably transforms your source code from a format that is easy to maintain into a format that is optimized to run as quickly as possible.</span></span>  

<span data-ttu-id="b9f2d-120">Les espaces de travail sont généralement en mesure de ma cartographier le code optimisé sur votre code source d’origine à l’aide de [cartes sources.][TreehouseBlogSourceMaps]</span><span class="sxs-lookup"><span data-stu-id="b9f2d-120">Workspaces is usually able to map the optimized code back to your original source code with the help of [source maps][TreehouseBlogSourceMaps].</span></span>  <span data-ttu-id="b9f2d-121">Toutefois, il existe de nombreuses variations entre les frameworks sur la façon dont chaque infrastructure utilise les cartes sources.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-121">But there is a lot of variation between frameworks over how each framework uses source maps.</span></span>  <span data-ttu-id="b9f2d-122">Devtools ne prend pas en charge toutes les variantes.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-122">Devtools doesn't support all of the variations.</span></span>  

<span data-ttu-id="b9f2d-123">Les espaces de travail ne fonctionnent pas avec l’infrastructure suivante.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-123">Workspaces is known to not work with the following framework.</span></span>  

*   <span data-ttu-id="b9f2d-124">Créer React application</span><span class="sxs-lookup"><span data-stu-id="b9f2d-124">Create React App</span></span>  

    <!-- If you run into issues while using Workspaces with your framework of choice, or you get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  
    
## <a name="related-feature-local-overrides"></a><span data-ttu-id="b9f2d-125">Fonctionnalité connexe : substitutions locales</span><span class="sxs-lookup"><span data-stu-id="b9f2d-125">Related feature: Local overrides</span></span>  

<span data-ttu-id="b9f2d-126">**Local Overrides** est une autre fonctionnalité DevTools similaire à Workspaces.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-126">**Local Overrides** is another DevTools feature that is similar to Workspaces.</span></span>  <span data-ttu-id="b9f2d-127">Utilisez les substitutions locales lorsque vous souhaitez expérimenter les modifications apportées à une page web et que vous devez afficher les modifications sur les chargements de pages web, mais que vous ne vous souciez pas de ma mappage de vos modifications au code source de la page web.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-127">Use Local Overrides when you want to experiment with changes to a webpage, and you need to display the changes across webpage loads, but you do not care about mapping your changes to the source code of the webpage.</span></span>  

<!--Todo: add section when content is ready  -->  

## <a name="step-1-set-up"></a><span data-ttu-id="b9f2d-128">Étape 1 : Configurer</span><span class="sxs-lookup"><span data-stu-id="b9f2d-128">Step 1: Set up</span></span>  

<span data-ttu-id="b9f2d-129">Pour obtenir une expérience pratique avec les espaces de travail, vous pouvez effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-129">Complete the following actions, to get hands-on experience with Workspaces.</span></span>  

### <a name="set-up-the-demo"></a><span data-ttu-id="b9f2d-130">Configurer la démonstration</span><span class="sxs-lookup"><span data-stu-id="b9f2d-130">Set up the demo</span></span>  

1.  <span data-ttu-id="b9f2d-131">[Ouvrez la démonstration.][GlitchWorkspacesDemo]</span><span class="sxs-lookup"><span data-stu-id="b9f2d-131">[Open the demo][GlitchWorkspacesDemo].</span></span>  <!--In the top-left of the editor, a randomly-generated project name is displayed.  -->  
    
    :::image type="complex" source="../media/workspaces-glitch-workspaces-demo-source.msft.png" alt-text="Un projet Glitch" lightbox="../media/workspaces-glitch-workspaces-demo-source.msft.png":::
       <span data-ttu-id="b9f2d-133">Un projet Glitch</span><span class="sxs-lookup"><span data-stu-id="b9f2d-133">A Glitch project</span></span>  
    :::image-end:::  
    
    <!--1.  Choose the project name.  -->  
    <!--1.  Choose **Advanced Options** > **Download Project**.  
    
    :::image type="complex" source="../media/workspaces-glitch-advanced-options-download-project.msft.png" alt-text="The Download Project button" lightbox="../media/workspaces-glitch-advanced-options-download-project.msft.png":::
       The Download Project button  
    :::image-end:::  

    -->  
    <!--1.  Close the tab.  -->  
    <!--1.  Unzip the source code and move the unzipped `app` directory to your desktop.  For the rest of this tutorial the unzipped directory is referred to as `~/Desktop/app`.  -->  
    
1.  <span data-ttu-id="b9f2d-134">Créez `app` un répertoire sur votre bureau.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-134">Create an `app` directory on your desktop.</span></span>  <span data-ttu-id="b9f2d-135">Enregistrez des copies des fichiers du `workspaces-demo` répertoire dans `app` le répertoire.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-135">Save copies of the files from the `workspaces-demo` directory to the `app` directory.</span></span>  <span data-ttu-id="b9f2d-136">Pour le reste du didacticiel, le répertoire est appelé `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="b9f2d-136">For the rest of the tutorial, the directory is referred to as `~/Desktop/app`.</span></span>  
1.  <span data-ttu-id="b9f2d-137">Démarrez un serveur web local dans `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="b9f2d-137">Start a local web server in `~/Desktop/app`.</span></span>  <span data-ttu-id="b9f2d-138">Voici un exemple de code pour le démarrage, mais vous pouvez `SimpleHTTPServer` utiliser n’importe quel serveur de votre préférence.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-138">Below is some sample code for starting up `SimpleHTTPServer`, but you may use whatever server you prefer.</span></span>  
    
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
    
1.  <span data-ttu-id="b9f2d-139">Ouvrez un onglet Microsoft Edge accédez à la version hébergée localement du site.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-139">Open a tab in Microsoft Edge and navigate to locally-hosted version of the site.</span></span>  <span data-ttu-id="b9f2d-140">Vous devriez être en mesure d’y accéder à l’aide d’une URL comme `localhost:8080` ou `http://0.0.0.0:8080` .</span><span class="sxs-lookup"><span data-stu-id="b9f2d-140">You should be able to access it using a URL like `localhost:8080` or `http://0.0.0.0:8080`.</span></span>  <span data-ttu-id="b9f2d-141">Le numéro [de port exact][WikiPortURLs] peut être différent.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-141">The exact [port number][WikiPortURLs] may be different.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo.msft.png" alt-text="Démonstration" lightbox="../media/workspaces-workspaces-demo.msft.png":::
       <span data-ttu-id="b9f2d-143">Démonstration</span><span class="sxs-lookup"><span data-stu-id="b9f2d-143">The demo</span></span>  
    :::image-end:::  
    
### <a name="set-up-devtools"></a><span data-ttu-id="b9f2d-144">Configurer DevTools</span><span class="sxs-lookup"><span data-stu-id="b9f2d-144">Set up DevTools</span></span>  

1.  <span data-ttu-id="b9f2d-145">Sélectionnez `Control` + `Shift` + `J` \(Windows, Linux\) ou `Command` \(macOS\) pour ouvrir le panneau + `Option` + `J` **console** de DevTools.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-145">Select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\) to open the **Console** panel of DevTools.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-console.msft.png" alt-text="Panneau console" lightbox="../media/workspaces-workspaces-demo-console.msft.png":::
       <span data-ttu-id="b9f2d-147">Panneau **console**</span><span class="sxs-lookup"><span data-stu-id="b9f2d-147">The **Console** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b9f2d-148">Accédez à **l’outil Sources.**</span><span class="sxs-lookup"><span data-stu-id="b9f2d-148">Navigate to the **Sources** tool.</span></span>  
1.  <span data-ttu-id="b9f2d-149">Dans le **volet Navigateur** (à gauche), choisissez l’onglet **Système de** fichiers.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-149">In the **Navigator** pane (on the left), choose the **Filesystem** tab.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem.msft.png" alt-text="Onglet Système de fichiers" lightbox="../media/workspaces-workspaces-demo-sources-filesystem.msft.png":::
       <span data-ttu-id="b9f2d-151">Onglet **Système de** fichiers</span><span class="sxs-lookup"><span data-stu-id="b9f2d-151">The **Filesystem** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b9f2d-152">Choisissez **Ajouter un dossier à l’espace de travail.**</span><span class="sxs-lookup"><span data-stu-id="b9f2d-152">Choose **Add Folder To Workspace**.</span></span>  
1.  <span data-ttu-id="b9f2d-153">Tapez `~/Desktop/app`.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-153">Type `~/Desktop/app`.</span></span>  
1.  <span data-ttu-id="b9f2d-154">Choisissez **Autoriser** pour accorder à DevTools l’autorisation de lire et d’écrire dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-154">Choose **Allow** to give DevTools permission to read and write to the directory.</span></span>  
    <span data-ttu-id="b9f2d-155">Dans **l’onglet Système de** fichiers, un point vert apparaît maintenant à côté `index.html` de , et `script.js` `styles.css` .</span><span class="sxs-lookup"><span data-stu-id="b9f2d-155">In the **Filesystem** tab, a green dot now appears next to `index.html`, `script.js`, and `styles.css`.</span></span>  <span data-ttu-id="b9f2d-156">Un point vert indique que DevTools a établi un mappage entre une ressource réseau de la page et le fichier dans `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="b9f2d-156">A green dot indicates that DevTools has established a mapping between a network resource of the page, and the file in `~/Desktop/app`.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem-folder.msft.png" alt-text="L’onglet Système de fichiers indique maintenant un mappage entre les fichiers locaux et les fichiers réseau" lightbox="../media/workspaces-workspaces-demo-sources-filesystem-folder.msft.png":::
       <span data-ttu-id="b9f2d-158">**L’onglet Système** de fichiers indique maintenant un mappage entre les fichiers locaux et les fichiers réseau</span><span class="sxs-lookup"><span data-stu-id="b9f2d-158">The **Filesystem** tab now indicates a mapping between the local files and the network ones</span></span>  
    :::image-end:::  
    
## <a name="step-2-save-a-css-change-to-disk"></a><span data-ttu-id="b9f2d-159">Étape 2 : Enregistrer une modification CSS sur le disque</span><span class="sxs-lookup"><span data-stu-id="b9f2d-159">Step 2: Save a CSS change to disk</span></span>  

1.  <span data-ttu-id="b9f2d-160">Ouvrez `styles.css` .</span><span class="sxs-lookup"><span data-stu-id="b9f2d-160">Open `styles.css`.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="b9f2d-161">La `color` propriété des éléments est définie sur `h1` `fuchsia` .</span><span class="sxs-lookup"><span data-stu-id="b9f2d-161">The `color` property of `h1` elements is set to `fuchsia`.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem-css.msft.png" alt-text="Afficher styles.css dans un éditeur de texte" lightbox="../media/workspaces-workspaces-demo-sources-filesystem-css.msft.png":::
       <span data-ttu-id="b9f2d-163">Afficher `styles.css` dans un éditeur de texte</span><span class="sxs-lookup"><span data-stu-id="b9f2d-163">View `styles.css` in a text editor</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b9f2d-164">Choisissez **l’outil Éléments.**</span><span class="sxs-lookup"><span data-stu-id="b9f2d-164">Choose the **Elements** tool.</span></span>  
1.  <span data-ttu-id="b9f2d-165">Modifiez la valeur de `color` la propriété de `<h1>` l’élément en votre couleur favorite.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-165">Change the value of the `color` property of the `<h1>` element to your favorite color.</span></span>  
    <span data-ttu-id="b9f2d-166">N’oubliez pas que vous devez choisir l’élément dans l’arborescence DOM pour afficher les règles CSS qui lui sont appliquées dans le `<h1>` **volet Styles.** \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="b9f2d-166">Remember that you need to choose the `<h1>` element in the **DOM Tree** in order to display the CSS rules applied to it in the **Styles** pane.</span></span>  <span data-ttu-id="b9f2d-167">Le point vert en côté signifie que toute modification que vous `styles.css:1` a faites est mappée sur `~/Desktop/app/styles.css` .</span><span class="sxs-lookup"><span data-stu-id="b9f2d-167">The green dot next to `styles.css:1` means that any change that you make are mapped to `~/Desktop/app/styles.css`.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-elements-styles-css.msft.png" alt-text="Indicateur vert qui fait que le fichier est lié" lightbox="../media/workspaces-workspaces-demo-elements-styles-css.msft.png":::
       <span data-ttu-id="b9f2d-169">Indicateur vert qui fait que le fichier est lié</span><span class="sxs-lookup"><span data-stu-id="b9f2d-169">The green indicator that the file is linked</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b9f2d-170">Ouvrez `styles.css` à nouveau dans un éditeur de texte.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-170">Open `styles.css` in a text editor again.</span></span>  <span data-ttu-id="b9f2d-171">La `color` propriété est maintenant définie sur votre couleur favorite.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-171">The `color` property is now set to your favorite color.</span></span>  
1.  <span data-ttu-id="b9f2d-172">Actualisez la page.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-172">Refresh the page.</span></span>  <span data-ttu-id="b9f2d-173">La couleur de `<h1>` l’élément est toujours définie sur votre couleur favorite.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-173">The color of the `<h1>` element is still set to your favorite color.</span></span>  <span data-ttu-id="b9f2d-174">La modification reste pendant une actualisation, car lorsque vous avez apporté la modification, DevTools a enregistré la modification sur le disque.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-174">The change remains across a refresh, because when you made the change DevTools saved the change to disk.</span></span>  <span data-ttu-id="b9f2d-175">Puis, lorsque vous avez actualisé la page, votre serveur local a servi la copie modifiée du fichier à partir du disque.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-175">And then, when you refreshed the page, your local server served the modified copy of the file from disk.</span></span>  
    
## <a name="step-3-save-an-html-change-to-disk"></a><span data-ttu-id="b9f2d-176">Étape 3 : Enregistrer une modification HTML sur le disque</span><span class="sxs-lookup"><span data-stu-id="b9f2d-176">Step 3: Save an HTML change to disk</span></span>  

### <a name="change-html-from-the-elements-panel"></a><span data-ttu-id="b9f2d-177">Modifier le code HTML à partir du panneau Éléments</span><span class="sxs-lookup"><span data-stu-id="b9f2d-177">Change HTML from the Elements Panel</span></span>  

<span data-ttu-id="b9f2d-178">Vous pouvez apporter des modifications au code HTML à partir du panneau d’élément, mais vos modifications apportées à l’arborescence DOM ne sont pas enregistrées sur le disque et n’ont qu’un effet sur la session de navigateur actuelle.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-178">You may make changes to the html from the Element Panel, but your changes to the DOM tree are not saved to disk and only effect the current browser session.</span></span>  

<span data-ttu-id="b9f2d-179">L’arborescence DOM n’est pas html.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-179">The DOM tree is not html.</span></span>  

<!--### Try changing HTML from the Elements panel  

> [!WARNING]
> The workflow that you are about to try does not work.  You are trying it now so that you do not waste time later trying to figure out why it is not working.  

1.  Choose the **Elements** tool.  
1.  Choose and edit the text content of the `h1` element, which says `Workspaces Demo`, and replace it with `I ❤️  Cake`.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-change-h1.msft.png" alt-text="Attempt to change html from the DOM Tree of the Elements panel" lightbox="../media/workspaces-workspaces-demo-change-h1.msft.png":::
       Attempt to change html from the DOM Tree of the **Elements** tool  
    :::image-end:::  
    
1.  Open `~/Desktop/app/index.html` in a text editor.  The change that you just made does not appear.  
1.  Refresh the page.  The page reverts to the original title.  
    
#### Optional: Why it is not working  

> [!NOTE]
> This section describes why the workflow from [Try changing html from the Elements panel](#try-changing-html-from-the-elements-panel) does not work.  You should skip this section if you do not care why.  

*   The tree of nodes that are displayed on the **Elements** tool represents the [DOM][MDNWebAPIsDOM] of the page.  
*   To display a page, a browser fetches html over the network, parses the html, and then converts it into a tree of DOM nodes.  
*   If the page has any JavaScript, that JavaScript may add, delete, or change DOM nodes.  CSS may change the DOM, too, using the [`content`][MDNCSSContent] property.  
*   The browser eventually uses the DOM to determine what content it should present to browser users.  
*   Therefore, the final state of the webpage displayed for users may be very different from the html that the browser fetched.  
*   This makes it difficult for DevTools to resolve where a change made in the **Elements** tool should be saved, because the DOM is affected by HTML, JavaScript, and CSS.  

In short, the **DOM Tree** `!==` HTML.  
-->  

### <a name="change-html-from-the-sources-tool"></a><span data-ttu-id="b9f2d-180">Modifier le code HTML à partir de l’outil Sources</span><span class="sxs-lookup"><span data-stu-id="b9f2d-180">Change HTML from the Sources tool</span></span>  

<span data-ttu-id="b9f2d-181">Si vous souhaitez enregistrer une modification au code HTML de la page web, utilisez **l’outil Sources.**</span><span class="sxs-lookup"><span data-stu-id="b9f2d-181">If you want to save a change to the HTML of the webpage, use the **Sources** tool.</span></span>  

1.  <span data-ttu-id="b9f2d-182">Accédez à **l’outil Sources.**</span><span class="sxs-lookup"><span data-stu-id="b9f2d-182">Navigate to the **Sources** tool.</span></span>  
1.  <span data-ttu-id="b9f2d-183">Dans le **volet Navigateur** (à gauche), choisissez l’onglet **Page.**</span><span class="sxs-lookup"><span data-stu-id="b9f2d-183">In the **Navigator** pane (on the left), choose the **Page** tab.</span></span>  
1.  <span data-ttu-id="b9f2d-184">Choose **(index)**.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-184">Choose **(index)**.</span></span>  <span data-ttu-id="b9f2d-185">Le code HTML de la page s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-185">The HTML for the page opens.</span></span>  
1.  <span data-ttu-id="b9f2d-186">Remplacez `<h1>Workspaces Demo</h1>` par `<h1>I ❤️  Cake</h1>` .</span><span class="sxs-lookup"><span data-stu-id="b9f2d-186">Replace `<h1>Workspaces Demo</h1>` with `<h1>I ❤️  Cake</h1>`.</span></span>  <span data-ttu-id="b9f2d-187">Examinez la figure suivante.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-187">Review the following figure.</span></span>  
1.  <span data-ttu-id="b9f2d-188">Sélectionnez `Control` + `S` \(Windows, Linux\) ou `Command` + `S` \(macOS\) pour enregistrer la modification.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-188">Select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save the change.</span></span>  
1.  <span data-ttu-id="b9f2d-189">Actualisez la page.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-189">Refresh the page.</span></span>  <span data-ttu-id="b9f2d-190">`<h1>`L’élément continue d’afficher le nouveau texte après l’actualisation de la page.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-190">The `<h1>` element continues to display the new text after the page is refreshed.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-page-h1.msft.png" alt-text="Modifier le code HTML à partir de l’outil Sources" lightbox="../media/workspaces-workspaces-demo-sources-page-h1.msft.png":::
       <span data-ttu-id="b9f2d-192">Modifier le code HTML à partir de **l’outil Sources**</span><span class="sxs-lookup"><span data-stu-id="b9f2d-192">Change HTML from the **Sources** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b9f2d-193">Ouvrez `~/Desktop/app/index.html` .</span><span class="sxs-lookup"><span data-stu-id="b9f2d-193">Open `~/Desktop/app/index.html`.</span></span>  <span data-ttu-id="b9f2d-194">`<h1>`L’élément contient le nouveau texte.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-194">The `<h1>` element contains the new text.</span></span>  
    
## <a name="step-4-save-a-javascript-change-to-disk"></a><span data-ttu-id="b9f2d-195">Étape 4 : Enregistrer une modification JavaScript sur le disque</span><span class="sxs-lookup"><span data-stu-id="b9f2d-195">Step 4: Save a JavaScript change to disk</span></span>  

<span data-ttu-id="b9f2d-196">Le principal endroit où utiliser l’éditeur de code de DevTools est **l’outil Sources.**</span><span class="sxs-lookup"><span data-stu-id="b9f2d-196">The main place to use the code editor of DevTools is the **Sources** tool.</span></span>  <span data-ttu-id="b9f2d-197">Mais parfois, vous devez accéder à d’autres outils, tels que l’outil **Éléments** ou le panneau **console,** lors de la modification de fichiers.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-197">But sometimes you need to access other tools, such as the **Elements** tool or the **Console** panel, while editing files.</span></span>  <span data-ttu-id="b9f2d-198">**L’outil Source rapide** vous fournit uniquement l’éditeur de l’outil **Sources,** alors que n’importe quel outil est ouvert.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-198">The **Quick Source** tool gives you just the editor from the **Sources** tool, while any tool is open.</span></span>  

<span data-ttu-id="b9f2d-199">Pour ouvrir l’éditeur de code DevTools avec d’autres outils, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="b9f2d-199">To open the DevTools code editor alongside other tools, do the following:</span></span>  

1.  <span data-ttu-id="b9f2d-200">Accédez à **l’outil Éléments.**</span><span class="sxs-lookup"><span data-stu-id="b9f2d-200">Navigate to the **Elements** tool.</span></span>  
1.  <span data-ttu-id="b9f2d-201">Sélectionnez `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="b9f2d-201">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  <span data-ttu-id="b9f2d-202">Le **menu Commande** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-202">The **Command Menu** opens.</span></span>  
1.  <span data-ttu-id="b9f2d-203">`Quick Source`Tapez, puis choisissez Afficher la source **rapide.**</span><span class="sxs-lookup"><span data-stu-id="b9f2d-203">Type `Quick Source`, and then choose **Show Quick Source**.</span></span>  <span data-ttu-id="b9f2d-204">En bas de la fenêtre DevTools, l’outil **Source** rapide s’affiche, affichant le contenu de , qui est le dernier fichier que vous avez modifié dans l’outil `index.html` **Sources.**</span><span class="sxs-lookup"><span data-stu-id="b9f2d-204">At the bottom of the DevTools window, the **Quick Source** tool appears, displaying the contents of `index.html`, which is the last file you edited in the **Sources** tool.</span></span>    
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-search-show-quick-source.msft.png" alt-text="Ouvrir l’outil Source rapide à l’aide du menu Commande" lightbox="../media/workspaces-workspaces-demo-search-show-quick-source.msft.png":::
       <span data-ttu-id="b9f2d-206">Ouvrir **l’outil Source rapide** à l’aide du **menu Commande**</span><span class="sxs-lookup"><span data-stu-id="b9f2d-206">Open the **Quick Source** tool by using the **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b9f2d-207">Sélectionnez `Control` + `P` \(Windows, Linux\) ou `Command` + `P` \(macOS\) \*\*\*\* pour ouvrir la boîte de dialogue Ouvrir un fichier.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-207">Select `Control`+`P` \(Windows, Linux\) or `Command`+`P` \(macOS\) to open the **Open File** dialog.</span></span>  <span data-ttu-id="b9f2d-208">Examinez la figure suivante.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-208">Review the following figure.</span></span>  
1.  <span data-ttu-id="b9f2d-209">`script`Tapez, puis choisissez **application/script.js**.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-209">Type `script`, then choose **app/script.js**.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-search-script.msft.png" alt-text="Ouvrir script.js à l’aide de la boîte de dialogue Ouvrir un fichier" lightbox="../media/workspaces-workspaces-demo-search-script.msft.png":::
       <span data-ttu-id="b9f2d-211">Ouvrir `script.js` à l’aide **de la boîte de dialogue Ouvrir un** fichier</span><span class="sxs-lookup"><span data-stu-id="b9f2d-211">Open `script.js` using the **Open File** dialog</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="b9f2d-212">Le `Save Changes To Disk With Workspaces` lien de la démonstration est régulièrement mis en forme.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-212">The `Save Changes To Disk With Workspaces` link in the demo is styled regularly.</span></span>  
    
1.  <span data-ttu-id="b9f2d-213">Ajoutez le code suivant au bas de la **script.js** l’aide de **l’outil Source** rapide.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-213">Add the following code to the bottom of **script.js** using the **Quick Source** tool.</span></span>  
    
    ```javascript
    console.log('greetings from script.js');
    document.querySelector('a').style = 'font-style:italic';
    ```  
    
1.  <span data-ttu-id="b9f2d-214">Sélectionnez `Control` + `S` \(Windows, Linux\) ou `Command` + `S` \(macOS\) pour enregistrer la modification.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-214">Select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save the change.</span></span>  
1.  <span data-ttu-id="b9f2d-215">Actualisez la page.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-215">Refresh the page.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="b9f2d-216">Le lien de la page est désormais en italique.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-216">The link on the page is now italicized.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-elements-styles-quick-source-script.msft.png" alt-text="Le lien de la page est désormais en italique" lightbox="../media/workspaces-workspaces-demo-elements-styles-quick-source-script.msft.png":::
       <span data-ttu-id="b9f2d-218">Le lien de la page est désormais en italique</span><span class="sxs-lookup"><span data-stu-id="b9f2d-218">The link on the page is now italicized</span></span>  
    :::image-end:::  
    
## <a name="next-steps"></a><span data-ttu-id="b9f2d-219">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="b9f2d-219">Next steps</span></span>  

<span data-ttu-id="b9f2d-220">Utilisez ce que vous avez appris dans ce didacticiel pour configurer les espaces de travail dans votre propre projet.</span><span class="sxs-lookup"><span data-stu-id="b9f2d-220">Use what you have learned in this tutorial to set up Workspaces in your own project.</span></span>  <!-- If you run into any issues or are able to get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  

<!--  
If you have more feedback on the topics or anything else, please use any of the channels below:  

*   [Mailing List][AlphabetGroupsAlphabetBrowserDevTools]  
*   [Twitter][TwitterAlphabetBrowserDevTools]  -->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="b9f2d-221">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="b9f2d-221">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsCssIndex]: ../css/index.md "Commencer à afficher et modifier les | Documents Microsoft"  

<!--[LocalOverrides]: ../whats-new/2018/01/devtools#overrides -->  

<!--[AlphabetGroupsAlphabetBrowserDevTools]: https://groups.alphabet.com/forum/#!forum/alphabet-browser-developer-tools "Alphabet Browser DevTools - Alphabet Groups"  -->  

[GlitchWorkspacesDemo]: https://glitch.com/edit/#!/microsoft-edge-chromium-devtools?path=workspaces-demo/index.html:1:0 "Fichiers de démonstration des espaces de travail | Glitch"  

[MDNCSSContent]: https://developer.mozilla.org/docs/Web/CSS/content "Content - CSS: Cascading Style Sheets | MDN"  
[MDNWebGettingStarted]: https://developer.mozilla.org/docs/Learn/Getting_started_with_the_web "Getting started with the Web | MDN"  
[MDNSimpleLocalHTTPServer]: https://developer.mozilla.org/docs/Learn/Common_questions/set_up_a_local_testing_server#Running_a_simple_local_HTTP_server "Exécution d’un serveur HTTP local simple | MDN"  
[MDNWebAPIsDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Présentation du DOM - Api web | MDN"  

<!--[StackOverflowAlphabetBrowserDevTools]: https://stackoverflow.com/questions/ask?tags=alphabet-browser-devtools "Alphabet Browser DevTools - Stack Overflow"  -->

[TreehouseBlogSourceMaps]: https://blog.teamtreehouse.com/introduction-source-maps "Présentation de l’Cartes | Treehouse Blog"  

<!-- [TwitterAlphabetBrowserDevTools]: https://twitter.com/alphabetbrowserdevtools "Alphabet Browser DevTools \(@AlphabetBrowserDevTools\) | Twitter"  -->

[WikiPortURLs]: https://en.wikipedia.org/wiki/Port_(computer_networking)#Use_in_URLs "Port \(computer networking\) - Wikipedia"  

> [!NOTE]
> <span data-ttu-id="b9f2d-230">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b9f2d-230">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b9f2d-231">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/workspaces/index) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="b9f2d-231">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/workspaces/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="b9f2d-233">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b9f2d-233">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
