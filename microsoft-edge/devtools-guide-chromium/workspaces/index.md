---
title: Modifier des fichiers avec des espaces de travail
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/27/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 612e85b8b00a78a40e53ac5c33d187fdae174024
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601851"
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







# <span data-ttu-id="c9fcb-103">Modifier des fichiers avec des espaces de travail</span><span class="sxs-lookup"><span data-stu-id="c9fcb-103">Edit Files With Workspaces</span></span>   



> [!NOTE]
> <span data-ttu-id="c9fcb-104">L’objectif de ce didacticiel consiste à fournir une pratique pratique pour configurer et utiliser des espaces de travail, afin que vous puissiez utiliser des espaces de travail dans vos propres projets.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-104">The goal of this tutorial is to provide hands-on practice in setting up and using Workspaces, so that you are able to use Workspaces in your own projects.</span></span>  <span data-ttu-id="c9fcb-105">Vous pouvez enregistrer les modifications apportées au code source, sur votre ordinateur local, que vous avez effectuées dans DevTools après avoir activé les espaces de travail.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-105">You are able to save the changes to the source code, on your local computer, that you made within DevTools after you enable Workspaces.</span></span>  

> [!CAUTION]
> <span data-ttu-id="c9fcb-106">Éléments **requis**: avant de commencer ce didacticiel, vous devez savoir comment:</span><span class="sxs-lookup"><span data-stu-id="c9fcb-106">**Prerequisites**: Before beginning this tutorial, you should know how to:</span></span>  
> *   [<span data-ttu-id="c9fcb-107">Utiliser HTML, CSS et JavaScript pour créer une page Web</span><span class="sxs-lookup"><span data-stu-id="c9fcb-107">Use HTML, CSS, and JavaScript to build a web page</span></span>][MDNWebGettingStarted]  
> *   [<span data-ttu-id="c9fcb-108">Utiliser DevTools pour apporter des modifications de base à CSS</span><span class="sxs-lookup"><span data-stu-id="c9fcb-108">Use DevTools to make basic changes to CSS</span></span>][DevToolsCssIndex]  
> *   [<span data-ttu-id="c9fcb-109">Exécuter un serveur Web HTTP local</span><span class="sxs-lookup"><span data-stu-id="c9fcb-109">Run a local HTTP web server</span></span>][MDNSimpleLocalHTTPServer]  

## <span data-ttu-id="c9fcb-110">Présentation</span><span class="sxs-lookup"><span data-stu-id="c9fcb-110">Overview</span></span>   

<span data-ttu-id="c9fcb-111">Les espaces de travail vous permettent d’enregistrer les modifications que vous apportez dans devtools à une copie locale du même fichier sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-111">Workspaces enable you to save a change that you make in Devtools to a local copy of the same file on your computer.</span></span>  <span data-ttu-id="c9fcb-112">Par exemple, supposons que:</span><span class="sxs-lookup"><span data-stu-id="c9fcb-112">For example, suppose:</span></span>  

*   <span data-ttu-id="c9fcb-113">Vous avez le code source de votre site sur votre ordinateur de bureau.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-113">You have the source code for your site on your desktop.</span></span>  
*   <span data-ttu-id="c9fcb-114">Vous exécutez un serveur Web local à partir du répertoire de code source, afin que le site soit accessible à l’adresse `localhost:8080` .</span><span class="sxs-lookup"><span data-stu-id="c9fcb-114">You are running a local web server from the source code directory, so that the site is accessible at `localhost:8080`.</span></span>  
*   <span data-ttu-id="c9fcb-115">Vous avez ouvert `localhost:8080` Microsoft Edge et vous utilisez devtools pour modifier la feuille de style en cascade (CSS) du site.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-115">You opened `localhost:8080`  in Microsoft Edge, and you are using DevTools to change the CSS of the site.</span></span>  

<span data-ttu-id="c9fcb-116">Lorsque les espaces de travail sont activés, les modifications que vous apportez dans DevTools sont enregistrées dans le code source sur votre ordinateur de bureau.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-116">With Workspaces enabled, the CSS changes that you make within DevTools are saved to the source code on your desktop.</span></span>  

## <span data-ttu-id="c9fcb-117">Limitations</span><span class="sxs-lookup"><span data-stu-id="c9fcb-117">Limitations</span></span>   

<span data-ttu-id="c9fcb-118">Si vous utilisez une infrastructure moderne, il est probable que vous transformez votre code source en un format facile à mettre en forme, optimisé pour s’exécuter aussi rapidement que possible.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-118">If you are using a modern framework, it probably transforms your source code from a format that is easy to maintain into a format that is optimized to run as quickly as possible.</span></span>  
<span data-ttu-id="c9fcb-119">Les espaces de travail sont généralement en mesure de mapper le code optimisé dans votre code source d’origine avec l’aide des [cartes sources][TreehouseBlogSourceMaps].</span><span class="sxs-lookup"><span data-stu-id="c9fcb-119">Workspaces is usually able to map the optimized code back to your original source code with the help of [source maps][TreehouseBlogSourceMaps].</span></span>  <span data-ttu-id="c9fcb-120">Néanmoins, il existe un grand nombre de variations entre les infrastructures par le biais de cartes sources.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-120">But there is a lot of variation between frameworks over how they use source maps.</span></span>  <span data-ttu-id="c9fcb-121">Devtools ne prend pas en charge toutes les variations.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-121">Devtools simply does support all the variations.</span></span>  

<span data-ttu-id="c9fcb-122">Les espaces de travail ne fonctionnent pas avec les infrastructures suivantes:</span><span class="sxs-lookup"><span data-stu-id="c9fcb-122">Workspaces is known to not work with these frameworks:</span></span>  

*   <span data-ttu-id="c9fcb-123">Créer une application réactive</span><span class="sxs-lookup"><span data-stu-id="c9fcb-123">Create React App</span></span>  

<!-- If you run into issues while using Workspaces with your framework of choice, or you get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  

## <span data-ttu-id="c9fcb-124">Fonctionnalité connexe: substitutions locales</span><span class="sxs-lookup"><span data-stu-id="c9fcb-124">Related feature: Local Overrides</span></span>   

<span data-ttu-id="c9fcb-125">Les **substitutions locales** sont une autre fonctionnalité devtools similaire aux espaces de travail.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-125">**Local Overrides** is another DevTools feature that is similar to Workspaces.</span></span>  <span data-ttu-id="c9fcb-126">Utilisez les substitutions locales lorsque vous voulez tester des modifications apportées à une page, et que vous avez besoin de voir ces modifications sur les chargements de page, mais vous n’avez pas à vous soucier de mapper vos modifications au code source de la page.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-126">Use Local Overrides when you want to experiment with changes to a page, and you need to see those changes across page loads, but you do not care about mapping your changes to the source code of the page.</span></span>  

<!--Todo: add section when content is ready  -->  

## <span data-ttu-id="c9fcb-127">Étape 1: installation</span><span class="sxs-lookup"><span data-stu-id="c9fcb-127">Step 1: Setup</span></span>   

<span data-ttu-id="c9fcb-128">Suivez ce didacticiel pour obtenir une expérience pratique avec les espaces de travail.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-128">Complete this tutorial to get hands-on experience with Workspaces.</span></span>  

### <span data-ttu-id="c9fcb-129">Configurer la démonstration</span><span class="sxs-lookup"><span data-stu-id="c9fcb-129">Set up the demo</span></span>   

1.  <span data-ttu-id="c9fcb-130">[Ouvrez la démonstration][GlitchWorkspacesDemo].</span><span class="sxs-lookup"><span data-stu-id="c9fcb-130">[Open the demo][GlitchWorkspacesDemo].</span></span>  <!--In the top-left of the editor, a randomly-generated project name is displayed.  -->  
    
    > ##### <span data-ttu-id="c9fcb-131">Figure1</span><span class="sxs-lookup"><span data-stu-id="c9fcb-131">Figure 1</span></span>  
    > <span data-ttu-id="c9fcb-132">Projet de problème projet ![ d’un problème][ImageGlitchProject]</span><span class="sxs-lookup"><span data-stu-id="c9fcb-132">A Glitch project ![A Glitch project][ImageGlitchProject]</span></span>  
    
    <!--1.  Click the project name.  -->
    <!--1.  Select **Advanced Options** > **Download Project**.  
    
    > ##### Figure 2  
    > The Download Project button  
    > ![The Download Project button][ImageDownloadProjectButton]  
    -->
    <!--1.  Close the tab.  -->
    <!--1.  Unzip the source code and move the unzipped `app` directory to your desktop.  For the rest of this tutorial this directory is referred to as `~/Desktop/app`.  -->  
    
1.  <span data-ttu-id="c9fcb-133">Créer un `app` répertoire sur votre ordinateur de bureau.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-133">Create an `app` directory on your desktop.</span></span>  <span data-ttu-id="c9fcb-134">Enregistrez des copies des fichiers dans l' `workspaces-demo` Annuaire.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-134">Save copies of the files in the `workspaces-demo` directory.</span></span>  <span data-ttu-id="c9fcb-135">Pour le reste de ce didacticiel, ce répertoire est appelé `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="c9fcb-135">For the rest of this tutorial this directory is referred to as `~/Desktop/app`.</span></span>  
1.  <span data-ttu-id="c9fcb-136">Démarrez un serveur Web local dans `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="c9fcb-136">Start a local web server in `~/Desktop/app`.</span></span>  <span data-ttu-id="c9fcb-137">Vous trouverez ci-dessous un exemple de code permettant de démarrer `SimpleHTTPServer` , mais vous pouvez utiliser le serveur de votre choix.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-137">Below is some sample code for starting up `SimpleHTTPServer`, but you may use whatever server you prefer.</span></span>  
    
    ```bash
    cd ~/Desktop/app
    python -m SimpleHTTPServer # Python 2
    ```  
    
    ```bash
    cd ~/Desktop/app
    python -m http.server # Python 3
    ```  
    
1.  <span data-ttu-id="c9fcb-138">Ouvrez un onglet dans Microsoft Edge et accédez à la version hébergée localement du site.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-138">Open a tab in Microsoft Edge and go to locally-hosted version of the site.</span></span>  <span data-ttu-id="c9fcb-139">Vous devriez être en mesure d’y accéder à l’aide d’une URL telle que `localhost:8080` ou `http://0.0.0.0:8080` .</span><span class="sxs-lookup"><span data-stu-id="c9fcb-139">You should be able to access it using a URL like `localhost:8080` or `http://0.0.0.0:8080`.</span></span>  <span data-ttu-id="c9fcb-140">Le [numéro de port][WikiPortURLs] exact est différent.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-140">The exact [port number][WikiPortURLs] may be different.</span></span>  
    
    > ##### <span data-ttu-id="c9fcb-141">Figure 2</span><span class="sxs-lookup"><span data-stu-id="c9fcb-141">Figure 2</span></span>  
    > <span data-ttu-id="c9fcb-142">La démonstration</span><span class="sxs-lookup"><span data-stu-id="c9fcb-142">The demo</span></span>  
    > <span data-ttu-id="c9fcb-143">! [Démonstration] [ImageDemo]</span><span class="sxs-lookup"><span data-stu-id="c9fcb-143">![The demo][ImageDemo]</span></span>  

### <span data-ttu-id="c9fcb-144">Configurer DevTools</span><span class="sxs-lookup"><span data-stu-id="c9fcb-144">Set up DevTools</span></span>   

1.  <span data-ttu-id="c9fcb-145">Appuyez sur `Control` + `Shift` + `J` \ (Windows \) ou `Command` + `Option` + `J` \ (MacOS \) pour ouvrir le panneau **console** de devtools.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-145">Press `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\) to open the **Console** panel of DevTools.</span></span>  
    
    > ##### <span data-ttu-id="c9fcb-146">Figure3</span><span class="sxs-lookup"><span data-stu-id="c9fcb-146">Figure 3</span></span>  
    > <span data-ttu-id="c9fcb-147">Panneau de la **console**</span><span class="sxs-lookup"><span data-stu-id="c9fcb-147">The **Console** panel</span></span>  
    > <span data-ttu-id="c9fcb-148">! [Panneau Console] [ImageConsolePanel]</span><span class="sxs-lookup"><span data-stu-id="c9fcb-148">![The Console panel][ImageConsolePanel]</span></span>  

1.  <span data-ttu-id="c9fcb-149">Cliquez sur l’onglet **sources** .</span><span class="sxs-lookup"><span data-stu-id="c9fcb-149">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="c9fcb-150">Cliquez sur l’onglet **FileSystem** .</span><span class="sxs-lookup"><span data-stu-id="c9fcb-150">Click the **Filesystem** tab.</span></span>  
    
    > ##### <span data-ttu-id="c9fcb-151">Figure 4</span><span class="sxs-lookup"><span data-stu-id="c9fcb-151">Figure 4</span></span>  
    > <span data-ttu-id="c9fcb-152">Onglet **FileSystem**</span><span class="sxs-lookup"><span data-stu-id="c9fcb-152">The **Filesystem** tab</span></span>  
    > <span data-ttu-id="c9fcb-153">! [L’onglet FileSystem] [ImageFilesystem]</span><span class="sxs-lookup"><span data-stu-id="c9fcb-153">![The Filesystem tab][ImageFilesystem]</span></span>  

1.  <span data-ttu-id="c9fcb-154">Cliquez sur **Ajouter un dossier à l’espace de travail**.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-154">Click **Add Folder To Workspace**.</span></span>  
1.  <span data-ttu-id="c9fcb-155">Sélectionnez `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="c9fcb-155">Select `~/Desktop/app`.</span></span>  
1.  <span data-ttu-id="c9fcb-156">Cliquez sur **autoriser** pour accorder à devtools l’autorisation de lecture et d’écriture dans l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-156">Click **Allow** to give DevTools permission to read and write to the directory.</span></span>  
    <span data-ttu-id="c9fcb-157">L’onglet **FileSystem** comporte désormais un point vert en regard de `index.html` , `script.js` et `styles.css` .</span><span class="sxs-lookup"><span data-stu-id="c9fcb-157">In the **Filesystem** tab, there is now a green dot next to `index.html`, `script.js`, and `styles.css`.</span></span>  <span data-ttu-id="c9fcb-158">Ces points verts indiquent que DevTools a établi une correspondance entre les ressources réseau de la page et les fichiers de `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="c9fcb-158">These green dots mean that DevTools has established a mapping between the network resources of the page, and the files in `~/Desktop/app`.</span></span>  
    
    > ##### <span data-ttu-id="c9fcb-159">Figure 5</span><span class="sxs-lookup"><span data-stu-id="c9fcb-159">Figure 5</span></span>  
    > <span data-ttu-id="c9fcb-160">L’onglet **FileSystem** montre désormais un mappage entre les fichiers locaux et les réseaux</span><span class="sxs-lookup"><span data-stu-id="c9fcb-160">The **Filesystem** tab now shows a mapping between the local files and the network ones</span></span>  
    > <span data-ttu-id="c9fcb-161">! [L’onglet FileSystem montre désormais un mappage entre les fichiers locaux et ceux du réseau] [ImageMapping]</span><span class="sxs-lookup"><span data-stu-id="c9fcb-161">![The Filesystem tab now shows a mapping between the local files and the network ones][ImageMapping]</span></span>  

## <span data-ttu-id="c9fcb-162">Étape 2: enregistrer un changement de CSS sur un disque</span><span class="sxs-lookup"><span data-stu-id="c9fcb-162">Step 2: Save a CSS change to disk</span></span>   

1.  <span data-ttu-id="c9fcb-163">Ouvrir `styles.css` .</span><span class="sxs-lookup"><span data-stu-id="c9fcb-163">Open `styles.css`.</span></span>  
    
    > [!NOTE]
    ><span data-ttu-id="c9fcb-164">La `color` propriété d' `h1` éléments est définie sur `fuchsia` .</span><span class="sxs-lookup"><span data-stu-id="c9fcb-164">The `color` property of `h1` elements is set to `fuchsia`.</span></span>
    
    > ##### <span data-ttu-id="c9fcb-165">Figure 6</span><span class="sxs-lookup"><span data-stu-id="c9fcb-165">Figure 6</span></span>  
    > <span data-ttu-id="c9fcb-166">Affichage `styles.css` dans un éditeur de texte</span><span class="sxs-lookup"><span data-stu-id="c9fcb-166">Viewing `styles.css` in a text editor</span></span>  
    > <span data-ttu-id="c9fcb-167">! [Affichage des styles. CSS dans un éditeur de texte] [ImageStylesFuchsia]</span><span class="sxs-lookup"><span data-stu-id="c9fcb-167">![Viewing styles.css in a text editor][ImageStylesFuchsia]</span></span>  


1.  <span data-ttu-id="c9fcb-168">Cliquez sur l’onglet **éléments** .</span><span class="sxs-lookup"><span data-stu-id="c9fcb-168">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="c9fcb-169">Remplacez la valeur de la `color` propriété de l' `<h1>` élément par votre couleur préférée.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-169">Change the value of the `color` property of the `<h1>` element to your favorite color.</span></span>  
    <span data-ttu-id="c9fcb-170">N’oubliez pas que vous devez cliquer sur l' `<h1>` élément dans l' **arborescence DOM** pour afficher les règles CSS qui lui sont appliquées dans le volet **styles** .</span><span class="sxs-lookup"><span data-stu-id="c9fcb-170">Remember that you need to click the `<h1>` element in the **DOM Tree** in order to see the CSS rules applied to it in the **Styles** pane.</span></span>  <span data-ttu-id="c9fcb-171">Le point vert en regard `styles.css:1` signifie que toutes les modifications que vous apportez sont mappées `~/Desktop/app/styles.css` .</span><span class="sxs-lookup"><span data-stu-id="c9fcb-171">The green dot next to `styles.css:1` means that any change that you make are mapped to `~/Desktop/app/styles.css`.</span></span>  
    
    > ##### <span data-ttu-id="c9fcb-172">Figure 7</span><span class="sxs-lookup"><span data-stu-id="c9fcb-172">Figure 7</span></span>  
    > <span data-ttu-id="c9fcb-173">Un indicateur vert dans lequel le fichier est lié</span><span class="sxs-lookup"><span data-stu-id="c9fcb-173">The green indicator that the file is linked</span></span>  
    > <span data-ttu-id="c9fcb-174">! [Indicateur vert dans lequel le fichier est lié] [ImageStylesGreen]</span><span class="sxs-lookup"><span data-stu-id="c9fcb-174">![The green indicator that the file is linked][ImageStylesGreen]</span></span>  

1.  <span data-ttu-id="c9fcb-175">Ouvrez `styles.css` de nouveau dans un éditeur de texte.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-175">Open `styles.css` in a text editor again.</span></span>  <span data-ttu-id="c9fcb-176">La `color` propriété est désormais définie pour votre couleur préférée.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-176">The `color` property is now set to your favorite color.</span></span>  
1.  <span data-ttu-id="c9fcb-177">Rechargez la page.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-177">Reload the page.</span></span>  <span data-ttu-id="c9fcb-178">La couleur de l' `<h1>` élément est toujours définie pour votre couleur préférée.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-178">The color of the `<h1>` element is still set to your favorite color.</span></span>  <span data-ttu-id="c9fcb-179">Cela fonctionne, car lorsque vous avez effectué la modification, DevTools enregistré la modification sur le disque.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-179">This works because when you made the change, DevTools saved the change to disk.</span></span>  <span data-ttu-id="c9fcb-180">Ensuite, lorsque vous rechargez la page, votre serveur local a desservi la copie modifiée du fichier à partir du disque.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-180">And then, when you reloaded the page, your local server served the modified copy of the file from disk.</span></span>  

## <span data-ttu-id="c9fcb-181">Étape 3: enregistrer un changement HTML sur le disque</span><span class="sxs-lookup"><span data-stu-id="c9fcb-181">Step 3: Save an HTML change to disk</span></span>   

### <span data-ttu-id="c9fcb-182">Changer le code HTML du panneau éléments</span><span class="sxs-lookup"><span data-stu-id="c9fcb-182">Change HTML from the Elements Panel</span></span>  

<span data-ttu-id="c9fcb-183">Vous pouvez modifier le code HTML dans le panneau d’éléments, mais vos modifications apportées à l’arborescence DOM ne sont pas enregistrées sur le disque et ne s’appliquent qu’à la session de navigateur actuelle.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-183">You may make changes to the HTML from the Element Panel, but your changes to the DOM tree are not saved to disk and only effect the current browser session.</span></span>  
<span data-ttu-id="c9fcb-184">L’arborescence DOM n’est pas HTML.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-184">The DOM tree is not HTML.</span></span>  

<!--### Try changing HTML from the Elements panel   

> [!WARNING]
> The workflow that you are about to try does not work.  You are trying it now so that you do not waste time later trying to figure out why it is not working.  

1.  Click the **Elements** tab.  
1.  Double click the text content of the `h1` element, which says `Workspaces Demo`, and replace it with `I ❤️  Cake`.  
    
    > ##### Old Figure 9  
    > Attempting to change HTML from the **DOM Tree** of the **Elements** panel  
    > ![Attempting to change HTML from the DOM Tree of the Elements panel][ImageElementsCake]  

1.  Open `~/Desktop/app/index.html` in a text editor.  The change that you just made does not appear.  
1.  Reload the page.  The page reverts to its original title.  

#### Optional: Why it is not working   

> [!NOTE]
> This section describes why the workflow from [Try changing HTML from the Elements panel](#try-changing-html-from-the-elements-panel) does not work.  You should skip this section if you do not care why.  

*   The tree of nodes that you see on the **Elements** panel represents the [DOM][MDNWebAPIsDOM] of the page.  
*   To display a page, a browser fetches HTML over the network, parses the HTML, and then converts it into a tree of DOM nodes.  
*   If the page has any JavaScript, that JavaScript may add, delete, or change DOM nodes.  CSS may change the DOM, too, using the [`content`][MDNCSSContent] property.  
*   The browser eventually uses the DOM to determine what content it should present to browser users.  
*   Therefore, the final state of the page that users see may be very different from the HTML that the browser fetched.  
*   This makes it difficult for DevTools to resolve where a change made in the **Elements** panel should be saved, because the DOM is affected by HTML, JavaScript, and CSS.  

In short, the **DOM Tree** `!==` HTML.  
-->
### <span data-ttu-id="c9fcb-185">Changer le code HTML dans le panneau sources</span><span class="sxs-lookup"><span data-stu-id="c9fcb-185">Change HTML from the Sources panel</span></span>   

<span data-ttu-id="c9fcb-186">Si vous voulez enregistrer une modification apportée au code HTML de la page, utilisez le panneau **sources** .</span><span class="sxs-lookup"><span data-stu-id="c9fcb-186">If you want to save a change to the HTML of the page, do it using the **Sources** panel.</span></span>  

1.  <span data-ttu-id="c9fcb-187">Cliquez sur l’onglet **sources** .</span><span class="sxs-lookup"><span data-stu-id="c9fcb-187">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="c9fcb-188">Cliquez sur l’onglet **page** .</span><span class="sxs-lookup"><span data-stu-id="c9fcb-188">Click the **Page** tab.</span></span>  
1.  <span data-ttu-id="c9fcb-189">Cliquez sur **(index)**.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-189">Click **(index)**.</span></span>  <span data-ttu-id="c9fcb-190">Le code HTML de la page s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-190">The HTML for the page opens.</span></span>  
1.  <span data-ttu-id="c9fcb-191">Remplacer `<h1>Workspaces Demo</h1>` par `<h1>I ❤️  Cake</h1>` .</span><span class="sxs-lookup"><span data-stu-id="c9fcb-191">Replace `<h1>Workspaces Demo</h1>` with `<h1>I ❤️  Cake</h1>`.</span></span>  <span data-ttu-id="c9fcb-192">Voir [figure 8](#figure-8).</span><span class="sxs-lookup"><span data-stu-id="c9fcb-192">See [Figure 8](#figure-8).</span></span>  
1.  <span data-ttu-id="c9fcb-193">Appuyez sur `Control` + `S` \ (Windows \) ou `Command` + `S` \ (MacOS \) pour enregistrer la modification.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-193">Press `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save the change.</span></span>  
1.  <span data-ttu-id="c9fcb-194">Rechargez la page.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-194">Reload the page.</span></span>  <span data-ttu-id="c9fcb-195">Le `<h1>` nouveau texte est encore affiché dans l’élément.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-195">The `<h1>` element is still displaying the new text.</span></span>  
    
    > ##### <span data-ttu-id="c9fcb-196">Figure8</span><span class="sxs-lookup"><span data-stu-id="c9fcb-196">Figure 8</span></span>  
    > <span data-ttu-id="c9fcb-197">La ligne 12 a été définie sur</span><span class="sxs-lookup"><span data-stu-id="c9fcb-197">Line 12 has been set to</span></span> `I ❤️  Cake`  
    > <span data-ttu-id="c9fcb-198">! [Changer le code HTML dans le panneau sources] [ImageSourcesCakeHTML]</span><span class="sxs-lookup"><span data-stu-id="c9fcb-198">![Changing HTML from the Sources panel][ImageSourcesCakeHTML]</span></span>  

1.  <span data-ttu-id="c9fcb-199">Ouvrir `~/Desktop/app/index.html` .</span><span class="sxs-lookup"><span data-stu-id="c9fcb-199">Open `~/Desktop/app/index.html`.</span></span>  <span data-ttu-id="c9fcb-200">L' `<h1>` élément contient le nouveau texte.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-200">The `<h1>` element contains the new text.</span></span>  

## <span data-ttu-id="c9fcb-201">Étape 4: enregistrer un changement JavaScript sur le disque</span><span class="sxs-lookup"><span data-stu-id="c9fcb-201">Step 4: Save a JavaScript change to disk</span></span>   

<span data-ttu-id="c9fcb-202">Le panneau **sources** est également l’endroit où il est possible de modifier le langage JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-202">The **Sources** panel is also the place to make changes to JavaScript.</span></span>  <span data-ttu-id="c9fcb-203">Néanmoins, il est possible que vous ayez besoin d’accéder à d’autres panneaux, comme le panneau **éléments** ou le panneau de la **console** , tout en apportant des modifications à votre site.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-203">But sometimes you need to access other panels, such as the **Elements** panel or the **Console** panel, while making changes to your site.</span></span>  <span data-ttu-id="c9fcb-204">Il est possible de faire en sorte que le panneau **sources** s’ouvre avec d’autres panneaux.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-204">There is a way to have the **Sources** panel open alongside other panels.</span></span>  

1.  <span data-ttu-id="c9fcb-205">Cliquez sur l’onglet **éléments** .</span><span class="sxs-lookup"><span data-stu-id="c9fcb-205">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="c9fcb-206">Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="c9fcb-206">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  <span data-ttu-id="c9fcb-207">Le **menu de commandes** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-207">The **Command Menu** opens.</span></span>  
1.  <span data-ttu-id="c9fcb-208">Tapez `QS` , puis sélectionnez **afficher la source rapide**.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-208">Type `QS`, then select **Show Quick Source**.</span></span>  <span data-ttu-id="c9fcb-209">Dans la partie inférieure de la fenêtre DevTools, il existe désormais un onglet **source rapide** .  L’onglet affiche le contenu de `index.html` , qui est le dernier fichier que vous avez modifié dans le panneau **sources** .</span><span class="sxs-lookup"><span data-stu-id="c9fcb-209">At the bottom of your DevTools window there is now a **Quick Source** tab.  The tab is displaying the contents of `index.html`, which is the last file you edited in the **Sources** panel.</span></span>  <span data-ttu-id="c9fcb-210">L’onglet **source rapide** fournit l’éditeur à partir du panneau **sources** , de sorte que vous pouvez modifier des fichiers en ouvrant d’autres panneaux.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-210">The **Quick Source** tab gives you the editor from the **Sources** panel, so that you are able to edit files while having other panels open.</span></span>  
    
    > ##### <span data-ttu-id="c9fcb-211">Figure9</span><span class="sxs-lookup"><span data-stu-id="c9fcb-211">Figure 9</span></span>  
    > <span data-ttu-id="c9fcb-212">Ouverture de l’onglet **source rapide** à l’aide du **menu de commandes**</span><span class="sxs-lookup"><span data-stu-id="c9fcb-212">Opening the **Quick Source** tab using the **Command Menu**</span></span>  
    > <span data-ttu-id="c9fcb-213">! [Ouverture de l’onglet source rapide à l’aide du menu de commandes] [ImageCommandMenuQuickSource]</span><span class="sxs-lookup"><span data-stu-id="c9fcb-213">![Opening the Quick Source tab using Command Menu][ImageCommandMenuQuickSource]</span></span>  

1.  <span data-ttu-id="c9fcb-214">`Control` + `P` `Command` + `P` Pour ouvrir la boîte de dialogue **ouvrir le fichier** , appuyez sur \ (Windows \) ou \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="c9fcb-214">Press `Control`+`P` \(Windows\) or `Command`+`P` \(macOS\) to open the **Open File** dialog.</span></span>  <span data-ttu-id="c9fcb-215">Voir [figure 10](#figure-10).</span><span class="sxs-lookup"><span data-stu-id="c9fcb-215">See [Figure 10](#figure-10).</span></span>  
1.  <span data-ttu-id="c9fcb-216">Tapez `script` , puis sélectionnez **app/script. js**.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-216">Type `script`, then select **app/script.js**.</span></span>  
    
    > ##### <span data-ttu-id="c9fcb-217">Figure10</span><span class="sxs-lookup"><span data-stu-id="c9fcb-217">Figure 10</span></span>  
    > <span data-ttu-id="c9fcb-218">Ouverture `script.js` à l’aide de la boîte de dialogue **ouvrir le fichier**</span><span class="sxs-lookup"><span data-stu-id="c9fcb-218">Opening `script.js` using the **Open File** dialog</span></span>  
    > <span data-ttu-id="c9fcb-219">! [Ouverture de script. js à l’aide de la boîte de dialogue Ouvrir le fichier] [ImageOpenFileDialog]</span><span class="sxs-lookup"><span data-stu-id="c9fcb-219">![Opening script.js using the Open File dialog][ImageOpenFileDialog]</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="c9fcb-220">Le `Save Changes To Disk With Workspaces` lien dans la démonstration est appliqué régulièrement.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-220">The `Save Changes To Disk With Workspaces` link in the demo is styled regularly.</span></span>  
    
1.  <span data-ttu-id="c9fcb-221">Ajoutez le code suivant en bas de **script. js** à l’aide de l’onglet **source rapide** .</span><span class="sxs-lookup"><span data-stu-id="c9fcb-221">Add the following code to the bottom of **script.js** using the **Quick Source** tab.</span></span>  
    
    ```javascript
    console.log('greetings from script.js');
    document.querySelector('a').style = 'font-style:italic';
    ```  
    
1.  <span data-ttu-id="c9fcb-222">Appuyez sur `Control` + `S` \ (Windows \) ou `Command` + `S` \ (MacOS \) pour enregistrer la modification.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-222">Press `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save the change.</span></span>  
1.  <span data-ttu-id="c9fcb-223">Rechargez la page.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-223">Reload the page.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="c9fcb-224">Le lien dans la page est désormais italique.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-224">The link on the page is now italic.</span></span>
    
    > ##### <span data-ttu-id="c9fcb-225">Figure11</span><span class="sxs-lookup"><span data-stu-id="c9fcb-225">Figure 11</span></span>  
    > <span data-ttu-id="c9fcb-226">Le lien dans la page est désormais en italique</span><span class="sxs-lookup"><span data-stu-id="c9fcb-226">The link on the page is now italic</span></span>  
    > <span data-ttu-id="c9fcb-227">! [Le lien dans la page est désormais italique] [ImageScriptItalic]</span><span class="sxs-lookup"><span data-stu-id="c9fcb-227">![The link on the page is now italic][ImageScriptItalic]</span></span>  

## <span data-ttu-id="c9fcb-228">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="c9fcb-228">Next steps</span></span>   

<span data-ttu-id="c9fcb-229">Utilisez ce que vous avez appris dans ce didacticiel pour configurer des espaces de travail dans votre projet.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-229">Use what you have learned in this tutorial to set up Workspaces in your own project.</span></span>  <!-- If you run into any issues or are able to get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->

 <!--  -->



<!-- 
If you have more feedback on these topics or anything else, please use any of the channels below:
*   [Mailing List][AlphabetGroupsAlphabetBrowserDevTools]  
*   [Twitter][TwitterAlphabetBrowserDevTools]  
-->

<!-- image links -->  

[ImageGlitchProject]: /microsoft-edge/devtools-guide-chromium/media/workspaces-glitch-workspaces-demo-source.msft.png "Figure 1: projet de problème avec un nom généré de manière aléatoire"  
<!--[ImageDownloadProjectButton]: /microsoft-edge/devtools-guide-chromium/media/workspaces-glitch-advanced-options-download-project.msft.png "old Figure 2: The Download Project button"  -->  
[ImageDemo]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-demo.msft.png "figure 2: démonstration"  
[ImageConsolePanel]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-Demo-console.msft.png "figure 3: le panneau Console"  
[ImageFilesystem]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-Demo-sources-FileSystem.msft.png "figure 4: onglet FileSystem"  
[ImageMapping]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-Demo-sources-FileSystem-Folder.msft.png "figure 5: l’onglet FileSystem montre désormais un mappage entre les fichiers locaux et les réseaux"  
[ImageStylesFuchsia]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-Demo-sources-FileSystem-CSS.msft.png "figure 6: affichage des styles. CSS dans un éditeur de texte"  
[ImageStylesGreen]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-Demo-Elements-styles-CSS.msft.png "figure 7: indicateur vert dans lequel le fichier est lié"  
[ImageSourcesCakeHTML]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-Demo-sources-page-H1.msft.png "figure 8: modification du code HTML dans le panneau sources"  
<!--[ImageElementsCake]: /microsoft-edge/devtools-guide-chromium/media/workspaces-workspaces-demo-change-h1.msft.png "Old Figure 9: Attempting to change HTML from the DOM Tree of the Elements panel"  -->  
[ImageCommandMenuQuickSource]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-Demo-Search-Show-Quick-source.msft.png "figure 9: ouverture de l’onglet source rapide à l’aide du menu de commande"  
[ImageOpenFileDialog]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-Demo-Search-script.msft.png "figure 10: ouverture de script. js à l’aide de la boîte de dialogue Ouvrir le fichier"  
[ImageScriptItalic]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-Demo-Elements-styles-Quick-Source-script.msft.png "figure 11: le lien dans la page est désormais italique"  

<!-- links -->  

[DevToolsCssIndex]: /microsoft-edge/devtools-guide-chromium/css/index "Découvrir comment afficher et modifier des feuilles CSS"  

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
> <span data-ttu-id="c9fcb-249">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c9fcb-249">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c9fcb-250">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/workspaces/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="c9fcb-250">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/workspaces/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="c9fcb-252">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c9fcb-252">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
