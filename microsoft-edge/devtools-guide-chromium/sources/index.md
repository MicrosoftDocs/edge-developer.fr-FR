---
description: Utilisez l’outil Sources pour afficher, modifier et déboguer JavaScript renvoyé par le serveur, et pour inspecter les ressources qui font la page web actuelle.  Pour utiliser l’outil Sources comme environnement de développement, ajoutez des fichiers sources à un espace de travail.
title: Vue d’ensemble de l’outil Sources
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/20/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 6ba6a7615c2d9e2b70975af01edeeb3e10db8e59
ms.sourcegitcommit: 31741a0c331816642ceafd20680bd3206c87c7bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "11579742"
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
# <a name="sources-tool-overview"></a><span data-ttu-id="48cbf-105">Vue d’ensemble de l’outil Sources</span><span class="sxs-lookup"><span data-stu-id="48cbf-105">Sources tool overview</span></span>  

<span data-ttu-id="48cbf-106">Utilisez **l’outil Sources** pour afficher, modifier et déboguer le code JavaScript frontal et inspecter les ressources qui font la page web actuelle.</span><span class="sxs-lookup"><span data-stu-id="48cbf-106">Use the **Sources** tool to view, modify, and debug front-end JavaScript code, and to inspect the resources that make up the current webpage.</span></span>  <span data-ttu-id="48cbf-107">**L’outil Sources** possède trois volets :</span><span class="sxs-lookup"><span data-stu-id="48cbf-107">The **Sources** tool has three panes:</span></span>  

| <span data-ttu-id="48cbf-108">Volet</span><span class="sxs-lookup"><span data-stu-id="48cbf-108">Pane</span></span> | <span data-ttu-id="48cbf-109">Actions</span><span class="sxs-lookup"><span data-stu-id="48cbf-109">Actions</span></span> |
|---|---|
| <span data-ttu-id="48cbf-110">**Volet navigateur**</span><span class="sxs-lookup"><span data-stu-id="48cbf-110">**Navigator** pane</span></span> | <span data-ttu-id="48cbf-111">Naviguez parmi les ressources renvoyées à partir du serveur pour construire la page web actuelle.</span><span class="sxs-lookup"><span data-stu-id="48cbf-111">Navigate among the resources that are returned from the server to construct the current webpage.</span></span>  <span data-ttu-id="48cbf-112">Sélectionnez des fichiers, des images et d’autres ressources et affichez leurs chemins d’accès.</span><span class="sxs-lookup"><span data-stu-id="48cbf-112">Select files, images, and other resources, and view their paths.</span></span>  <span data-ttu-id="48cbf-113">Vous pouvez également configurer un espace de travail local pour enregistrer les modifications directement dans les fichiers sources.</span><span class="sxs-lookup"><span data-stu-id="48cbf-113">Optionally, set up a local Workspace to save changes directly to source files.</span></span> |
| <span data-ttu-id="48cbf-114">**Volet** Éditeur</span><span class="sxs-lookup"><span data-stu-id="48cbf-114">**Editor** pane</span></span> | <span data-ttu-id="48cbf-115">Afficher les fichiers JavaScript, HTML, CSS et autres qui sont renvoyés à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="48cbf-115">View JavaScript, HTML, CSS, and other files that are returned from the server.</span></span>  <span data-ttu-id="48cbf-116">A apporter des modifications expérimentales à JavaScript ou CSS.</span><span class="sxs-lookup"><span data-stu-id="48cbf-116">Make experimental edits to JavaScript or CSS.</span></span>  <span data-ttu-id="48cbf-117">Vos modifications sont conservées jusqu’à ce que vous actualisiez la page ou après l’actualisation de la page si vous enregistrez dans un fichier local avec espaces de travail.</span><span class="sxs-lookup"><span data-stu-id="48cbf-117">Your changes are preserved until you refresh the page, or are preserved after page refresh if you save to a local file with Workspaces.</span></span> <span data-ttu-id="48cbf-118">Lorsque vous utilisez des espaces de travail ou des substitutions, vous pouvez également modifier des fichiers HTML.</span><span class="sxs-lookup"><span data-stu-id="48cbf-118">When you use Workspaces or Overrides, you can edit HTML files as well.</span></span> |
| <span data-ttu-id="48cbf-119">**Volet Débogger**</span><span class="sxs-lookup"><span data-stu-id="48cbf-119">**Debugger** pane</span></span> | <span data-ttu-id="48cbf-120">Utilisez le débogger JavaScript pour définir des points d’arrêt, suspendre l’exécution de JavaScript et passer pas à pas le code, y compris les modifications que vous avez faites, tout en regardant les expressions JavaScript que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="48cbf-120">Use the JavaScript Debugger to set breakpoints, pause running JavaScript, and step through the code, including any edits you have made, while watching any JavaScript expressions you specify.</span></span>  <span data-ttu-id="48cbf-121">Observez et modifiez manuellement les valeurs des variables qui sont dans l’étendue de la ligne de code actuelle.</span><span class="sxs-lookup"><span data-stu-id="48cbf-121">Watch and manually change the values of variables that are in-scope for the current line of code.</span></span> |

<span data-ttu-id="48cbf-122">La figure suivante montre le volet **Navigateur** mis en surbrillon avec une \*\*\*\* zone rouge dans le coin supérieur \*\*\*\* gauche de DevTools, le volet Éditeur mis en surbrillon dans le coin supérieur droit et le volet Débogueur mis en évidence en bas.</span><span class="sxs-lookup"><span data-stu-id="48cbf-122">The following figure shows the **Navigator** pane highlighted with a red box in the upper left corner of DevTools, the **Editor** pane highlighted in the upper right, and the **Debugger** pane highlighted on the bottom.</span></span>  <span data-ttu-id="48cbf-123">À l’extrême gauche se trouve la partie principale de la fenêtre du navigateur, affichant la page web rendue grisée, car le débogger est suspendu sur un point d’arrêt :</span><span class="sxs-lookup"><span data-stu-id="48cbf-123">On the far left side is the main part of the browser window, showing the rendered webpage grayed-out because the debugger is paused on a breakpoint:</span></span>

:::image type="complex" source="../media/sources-panes-narrow-layout.msft.png" alt-text="Volets de l’outil Sources, dans une disposition étroite" lightbox="../media/sources-panes-narrow-layout.msft.png":::
   <span data-ttu-id="48cbf-125">Volets de l’outil Sources, dans une disposition étroite</span><span class="sxs-lookup"><span data-stu-id="48cbf-125">The panes of the Sources tool, in narrow layout</span></span>  
:::image-end:::  

<span data-ttu-id="48cbf-126">Lorsque DevTools est \*\*\*\* large, le volet Débogueur est placé à droite et inclut **Scope** et **Watch**:</span><span class="sxs-lookup"><span data-stu-id="48cbf-126">When DevTools is wide, the **Debugger** pane is placed on the right, and includes **Scope** and **Watch**:</span></span>  

:::image type="complex" source="../media/sources-panes-wide-layout.msft.png" alt-text="Parcourir, afficher, modifier et déboguer JavaScript renvoyé par le serveur" lightbox="../media/sources-panes-wide-layout.msft.png":::
   <span data-ttu-id="48cbf-128">Parcourir, afficher, modifier et déboguer JavaScript renvoyé par le serveur</span><span class="sxs-lookup"><span data-stu-id="48cbf-128">Navigate, view, edit, and debug JavaScript returned by the server</span></span>  
:::image-end:::  

<span data-ttu-id="48cbf-129">Pour optimiser la taille de l’outil Sources, désédockez DevTools dans une fenêtre distincte et déplacez éventuellement la fenêtre DevTools vers un moniteur distinct.</span><span class="sxs-lookup"><span data-stu-id="48cbf-129">To maximize the size of the Sources tool, undock DevTools into a separate window, and optionally move the DevTools window to a separate monitor.</span></span>  <span data-ttu-id="48cbf-130">Voir [Change Microsoft Edge placement de DevTools (Undock, Dock to bottom, Dock to left)][DevToolsCustomizePlacement].</span><span class="sxs-lookup"><span data-stu-id="48cbf-130">See [Change Microsoft Edge DevTools placement (Undock, Dock to bottom, Dock to left)][DevToolsCustomizePlacement].</span></span>

<span data-ttu-id="48cbf-131">Pour charger la page web de démonstration de débogage ci-dessus, voir l’approche de base de l’utilisation [d’un déboguer,](#the-basic-approach-to-using-a-debugger)ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="48cbf-131">To load the debugging demo webpage that's shown above, see [The basic approach to using a debugger](#the-basic-approach-to-using-a-debugger), below.</span></span>

## <a name="using-the-navigator-pane-to-select-files"></a><span data-ttu-id="48cbf-132">Utilisation du volet Navigateur pour sélectionner des fichiers</span><span class="sxs-lookup"><span data-stu-id="48cbf-132">Using the Navigator pane to select files</span></span>

<span data-ttu-id="48cbf-133">Utilisez le **volet Navigateur** (à gauche) pour naviguer parmi les ressources renvoyées par le serveur pour construire la page web actuelle.</span><span class="sxs-lookup"><span data-stu-id="48cbf-133">Use the **Navigator** pane (on the left) to navigate among the resources that are returned from the server to construct the current webpage.</span></span>  <span data-ttu-id="48cbf-134">Sélectionnez des fichiers, des images et d’autres ressources et affichez leurs chemins d’accès.</span><span class="sxs-lookup"><span data-stu-id="48cbf-134">Select files, images, and other resources, and view their paths.</span></span>  

:::image type="complex" source="../media/navigator-pane.msft.png" alt-text="Volet Navigateur" lightbox="../media/navigator-pane.msft.png":::
   <span data-ttu-id="48cbf-136">Volet **Navigateur**</span><span class="sxs-lookup"><span data-stu-id="48cbf-136">The **Navigator** pane</span></span>
:::image-end:::  

<span data-ttu-id="48cbf-137">Pour accéder aux onglets masqués du volet Navigateur, sélectionnez ![ Autres onglets ](../media/more-tabs-icon.msft.png) ( Autres**onglets).**</span><span class="sxs-lookup"><span data-stu-id="48cbf-137">To access any hidden tabs of the Navigator pane, select ![More tabs](../media/more-tabs-icon.msft.png) (**More tabs**).</span></span>

<span data-ttu-id="48cbf-138">Les sous-sections suivantes couvrent le volet Navigateur :</span><span class="sxs-lookup"><span data-stu-id="48cbf-138">The following subsections cover the Navigator pane:</span></span>
*   [<span data-ttu-id="48cbf-139">Utilisation de l’onglet Page pour explorer les ressources qui construisent la page web actuelle</span><span class="sxs-lookup"><span data-stu-id="48cbf-139">Using the Page tab to explore resources that construct the current webpage</span></span>](#using-the-page-tab-to-explore-resources-that-construct-the-current-webpage)
*   [<span data-ttu-id="48cbf-140">Utilisation de l’onglet Système de fichiers pour définir un espace de travail local</span><span class="sxs-lookup"><span data-stu-id="48cbf-140">Using the Filesystem tab to define a local Workspace</span></span>](#using-the-filesystem-tab-to-define-a-local-workspace)
*   [<span data-ttu-id="48cbf-141">Utilisation de l’onglet Remplacements pour remplacer les fichiers serveur par des fichiers locaux</span><span class="sxs-lookup"><span data-stu-id="48cbf-141">Using the Overrides tab to override server files with local files</span></span>](#using-the-overrides-tab-to-override-server-files-with-local-files)
*   [<span data-ttu-id="48cbf-142">Utilisation de l’onglet Scripts de contenu pour Microsoft Edge extensions</span><span class="sxs-lookup"><span data-stu-id="48cbf-142">Using the Content scripts tab for Microsoft Edge extensions</span></span>](#using-the-content-scripts-tab-for-microsoft-edge-extensions)
*   [<span data-ttu-id="48cbf-143">Utilisation de l’onglet Extraits de code pour exécuter des extraits de code JavaScript sur n’importe quelle page</span><span class="sxs-lookup"><span data-stu-id="48cbf-143">Using the Snippets tab to run JavaScript code snippets on any page</span></span>](#using-the-snippets-tab-to-run-javascript-code-snippets-on-any-webpage)
*   [<span data-ttu-id="48cbf-144">Utilisation du menu Commande pour ouvrir des fichiers</span><span class="sxs-lookup"><span data-stu-id="48cbf-144">Using the Command Menu to open files</span></span>](#using-the-command-menu-to-open-files)

### <a name="using-the-page-tab-to-explore-resources-that-construct-the-current-webpage"></a><span data-ttu-id="48cbf-145">Utilisation de l’onglet Page pour explorer les ressources qui construisent la page web actuelle</span><span class="sxs-lookup"><span data-stu-id="48cbf-145">Using the Page tab to explore resources that construct the current webpage</span></span>

<span data-ttu-id="48cbf-146">Utilisez **l’onglet Page** du volet **Navigateur** pour explorer le système de fichiers renvoyé à partir du serveur pour construire la page web actuelle.</span><span class="sxs-lookup"><span data-stu-id="48cbf-146">Use the **Page** tab of the **Navigator** pane to explore the file system that's returned from the server to construct the current webpage.</span></span>  <span data-ttu-id="48cbf-147">Sélectionnez un fichier JavaScript pour l’afficher, le modifier et le déboguer.</span><span class="sxs-lookup"><span data-stu-id="48cbf-147">Select a JavaScript file to view, edit, and debug it.</span></span>  <span data-ttu-id="48cbf-148">**L’onglet Page** répertorie toutes les ressources que la page a chargées.</span><span class="sxs-lookup"><span data-stu-id="48cbf-148">The **Page** tab lists all of the resources that the page has loaded.</span></span>

:::image type="complex" source="../media/sources-page-tab.msft.png" alt-text="Onglet Page dans le volet Navigateur de l’outil Sources" lightbox="../media/sources-page-tab.msft.png":::
   <span data-ttu-id="48cbf-150">Onglet **Page** dans le volet **Navigateur** de l’outil **Sources**</span><span class="sxs-lookup"><span data-stu-id="48cbf-150">The **Page** tab in the **Navigator** pane of the **Sources** tool</span></span>
:::image-end:::  

<span data-ttu-id="48cbf-151">Pour afficher un fichier dans **le** volet Éditeur, sélectionnez un fichier dans l’onglet **Page.**  Pour une image, un aperçu de l’image s’affiche.</span><span class="sxs-lookup"><span data-stu-id="48cbf-151">To display a file in the **Editor** pane, select a file in the **Page** tab.  For an image, a preview of the image is displayed.</span></span>  

<span data-ttu-id="48cbf-152">Pour afficher l’URL ou le chemin d’accès d’une ressource, pointez sur la ressource.</span><span class="sxs-lookup"><span data-stu-id="48cbf-152">To display the URL or path for a resource, hover over the resource.</span></span>

<span data-ttu-id="48cbf-153">Pour charger un fichier dans un nouvel onglet du navigateur ou pour afficher d’autres actions, cliquez avec le bouton droit sur le nom du fichier.</span><span class="sxs-lookup"><span data-stu-id="48cbf-153">To load a file into a new tab of the browser, or to display other actions, right-click on the file name.</span></span>
   
#### <a name="icons-in-the-page-tab"></a><span data-ttu-id="48cbf-154">Icônes dans l’onglet Page</span><span class="sxs-lookup"><span data-stu-id="48cbf-154">Icons in the Page tab</span></span>

<span data-ttu-id="48cbf-155">**L’onglet Page** utilise les icônes suivantes :</span><span class="sxs-lookup"><span data-stu-id="48cbf-155">The **Page** tab uses the following icons:</span></span>
*   <span data-ttu-id="48cbf-156">**L’icône** de fenêtre, ainsi que l’étiquette, représente le cadre de `top` document principal, qui est un [cadre HTML][W3CHtml4Frames].</span><span class="sxs-lookup"><span data-stu-id="48cbf-156">The **window** icon, along with the label `top`, represents the main document frame, which is an [HTML frame][W3CHtml4Frames].</span></span>  
*   <span data-ttu-id="48cbf-157">**L’icône** cloud représente une [origine][HtmlstandardOrigin].</span><span class="sxs-lookup"><span data-stu-id="48cbf-157">The **cloud** icon represents an [origin][HtmlstandardOrigin].</span></span>  
*   <span data-ttu-id="48cbf-158">**L’icône** de dossier représente un répertoire.</span><span class="sxs-lookup"><span data-stu-id="48cbf-158">The **folder** icon represents a directory.</span></span>
*   <span data-ttu-id="48cbf-159">**L’icône** de page représente une ressource.</span><span class="sxs-lookup"><span data-stu-id="48cbf-159">The **page** icon represents a resource.</span></span>  
    
#### <a name="group-files-by-folder-or-as-a-flat-list"></a><span data-ttu-id="48cbf-160">Grouper des fichiers par dossier ou en tant que liste plate</span><span class="sxs-lookup"><span data-stu-id="48cbf-160">Group files by folder or as a flat list</span></span>

<span data-ttu-id="48cbf-161">**L’onglet Page** affiche les fichiers ou les ressources regroupés par serveur et répertoire, ou sous la direction d’une liste plate.</span><span class="sxs-lookup"><span data-stu-id="48cbf-161">The **Page** tab displays files or resources grouped by server and directory, or as a flat list.</span></span>

<span data-ttu-id="48cbf-162">Pour modifier le regroupement des ressources :</span><span class="sxs-lookup"><span data-stu-id="48cbf-162">To change how resources are grouped:</span></span>

1.  <span data-ttu-id="48cbf-163">À côté des onglets du volet Navigateur (à gauche), sélectionnez **le bouton ...** ( Plus**d’options).**</span><span class="sxs-lookup"><span data-stu-id="48cbf-163">Next to the tabs on the Navigator pane (on the left), select the **...** (**More options**) button.</span></span>  <span data-ttu-id="48cbf-164">Un menu s’affiche.</span><span class="sxs-lookup"><span data-stu-id="48cbf-164">A menu appears.</span></span>
1.  <span data-ttu-id="48cbf-165">Sélectionnez ou effacer **l’option Grouper par** dossier.</span><span class="sxs-lookup"><span data-stu-id="48cbf-165">Select or clear the **Group by folder** option.</span></span>  

### <a name="using-the-filesystem-tab-to-define-a-local-workspace"></a><span data-ttu-id="48cbf-166">Utilisation de l’onglet Système de fichiers pour définir un espace de travail local</span><span class="sxs-lookup"><span data-stu-id="48cbf-166">Using the Filesystem tab to define a local Workspace</span></span>

<span data-ttu-id="48cbf-167">Utilisez **l’onglet Système** de fichiers du volet **Navigateur** pour ajouter des fichiers à un espace de travail, afin que les modifications que vous avériez dans DevTools sont enregistrées dans votre système de fichiers local.</span><span class="sxs-lookup"><span data-stu-id="48cbf-167">Use the **Filesystem** tab of the **Navigator** pane to add files to a Workspace, so that changes you make in DevTools get saved to your local file system.</span></span>

<span data-ttu-id="48cbf-168">Un fichier qui se trouve dans un espace de travail est indiqué par un point vert à côté du nom de fichier, dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="48cbf-168">A file that's in a Workspace is indicated by a green dot next to the file name, throughout DevTools.</span></span> 

:::image type="complex" source="../media/sources-filesystem-tab.msft.png" alt-text="Onglet Système de fichiers, pour un espace de travail" lightbox="../media/sources-filesystem-tab.msft.png":::
   <span data-ttu-id="48cbf-170">Onglet **Système de** fichiers, pour un espace de travail</span><span class="sxs-lookup"><span data-stu-id="48cbf-170">The **Filesystem** tab, for a Workspace</span></span>
:::image-end:::  

<span data-ttu-id="48cbf-171">Par défaut, lorsque vous modifiez un fichier dans l’outil **Sources,** vos modifications sont ignorées lorsque vous actualisez la page web.</span><span class="sxs-lookup"><span data-stu-id="48cbf-171">By default, when you edit a file in the **Sources** tool, your changes are discarded when you refresh the webpage.</span></span>  <span data-ttu-id="48cbf-172">**L’outil Sources** fonctionne avec une copie des ressources frontales renvoyées par le serveur web.</span><span class="sxs-lookup"><span data-stu-id="48cbf-172">The **Sources** tool works with a copy of the front-end resources that are returned by the web server.</span></span>  <span data-ttu-id="48cbf-173">Lorsque vous modifiez ces fichiers frontaux renvoyés par le serveur, les modifications ne sont pas persistantes, car vous n’avez pas modifié les fichiers sources.</span><span class="sxs-lookup"><span data-stu-id="48cbf-173">When you modify these front-end files that are returned by the server, the changes don't persist, because you didn't change the source files.</span></span>  <span data-ttu-id="48cbf-174">Vous devez également appliquer vos modifications dans votre code source réel, puis les déployer à nouveau sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="48cbf-174">You need to also apply your edits in your actual source code, and then re-deploy to the server.</span></span>

<span data-ttu-id="48cbf-175">En revanche, lorsque vous utilisez un espace de travail, les modifications que vous a faites à votre code frontal sont conservées lorsque vous actualisez la page web.</span><span class="sxs-lookup"><span data-stu-id="48cbf-175">In contrast, when you use a Workspace, changes that you make to your front-end code are preserved when you refresh the webpage.</span></span>  <span data-ttu-id="48cbf-176">Avec un espace de travail, lorsque vous modifiez le code frontal renvoyé par le serveur, l’outil Sources applique également vos modifications à votre code source local.</span><span class="sxs-lookup"><span data-stu-id="48cbf-176">With a Workspace, when you edit the front-end code that's returned by the server, the Sources tool also applies your edits to your local source code.</span></span>  <span data-ttu-id="48cbf-177">Ensuite, pour que les autres utilisateurs voient vos modifications, vous devez uniquement redéployer vos fichiers sources modifiés sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="48cbf-177">Then for other users to see your changes, you only need to redeploy your changed source files to the server.</span></span>

<span data-ttu-id="48cbf-178">Les espaces de travail fonctionnent bien lorsque le code JavaScript renvoyé par le serveur est identique à votre code source JavaScript local.</span><span class="sxs-lookup"><span data-stu-id="48cbf-178">Workspaces work well when the JavaScript code that's returned by the server is the same as your local JavaScript source code.</span></span>  <span data-ttu-id="48cbf-179">Les espaces de travail ne fonctionnent pas aussi bien lorsque votre flux de travail implique des transformations sur votre code source, telles que la minification ou la compilation [de TypeScript.][TypescriptlangMain]</span><span class="sxs-lookup"><span data-stu-id="48cbf-179">Workspaces don't work as well when your workflow involves transformations on your source code, such as minification or [TypeScript][TypescriptlangMain] compilation.</span></span>  

<span data-ttu-id="48cbf-180">Pour plus d’informations, voir le [didacticiel Modifier les fichiers avec les espaces de travail.][DevtoolsGuideChromiumWorkspacesIndex]</span><span class="sxs-lookup"><span data-stu-id="48cbf-180">For more information, see the tutorial [Edit files with Workspaces][DevtoolsGuideChromiumWorkspacesIndex].</span></span>

### <a name="using-the-overrides-tab-to-override-server-files-with-local-files"></a><span data-ttu-id="48cbf-181">Utilisation de l’onglet Remplacements pour remplacer les fichiers serveur par des fichiers locaux</span><span class="sxs-lookup"><span data-stu-id="48cbf-181">Using the Overrides tab to override server files with local files</span></span>

<span data-ttu-id="48cbf-182">Utilisez **l’onglet Remplacements** du volet **Navigateur** pour remplacer les ressources de page (telles que les images) avec les fichiers d’un dossier local.</span><span class="sxs-lookup"><span data-stu-id="48cbf-182">Use the **Overrides** tab of the **Navigator** pane to override page assets (such as images) with files from a local folder.</span></span>

<span data-ttu-id="48cbf-183">Les éléments de cet onglet remplacent ce que le serveur envoie au navigateur, même après que le serveur a envoyé les biens.</span><span class="sxs-lookup"><span data-stu-id="48cbf-183">Items in this tab override what the server sends to the browser, even after the server has sent the assets.</span></span>  

:::image type="complex" source="../media/overrides-tab.msft.png" alt-text="Onglet Remplacements du volet Navigateur" lightbox="../media/overrides-tab.msft.png":::
   <span data-ttu-id="48cbf-185">Onglet **Remplacements** du volet **Navigateur**</span><span class="sxs-lookup"><span data-stu-id="48cbf-185">The **Overrides** tab of the **Navigator** pane</span></span>
:::image-end:::  

<span data-ttu-id="48cbf-186">La **fonctionnalité Overrides** est similaire à Workspaces.</span><span class="sxs-lookup"><span data-stu-id="48cbf-186">The **Overrides** feature is similar to Workspaces.</span></span>  <span data-ttu-id="48cbf-187">Utilisez les substitutions lorsque vous souhaitez expérimenter les modifications apportées à une page web et que vous devez conserver les modifications après avoir actualisé la page web, mais que vous ne vous souciez pas de ma mappage de vos modifications au code source de la page web.</span><span class="sxs-lookup"><span data-stu-id="48cbf-187">Use Overrides when you want to experiment with changes to a webpage, and you need to keep the changes after you refresh the webpage, but you don't care about mapping your changes to the source code of the webpage.</span></span>  

<span data-ttu-id="48cbf-188">Un fichier qui remplace un fichier qui est renvoyé par le serveur est indiqué par un point violet à côté du nom de fichier, dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="48cbf-188">A file that overrides a file that is returned by the server is indicated by a purple dot next to the file name, throughout DevTools.</span></span>

#### <a name="see-also"></a><span data-ttu-id="48cbf-189">Articles associés</span><span class="sxs-lookup"><span data-stu-id="48cbf-189">See also</span></span>

*   [<span data-ttu-id="48cbf-190">Remplacer les ressources de page web avec des copies locales à l’Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="48cbf-190">Override webpage resources with local copies using Microsoft Edge DevTools</span></span>][DevtoolsJavascriptOverrides]

*   [<span data-ttu-id="48cbf-191">Ma mappant le code prétraité au code source</span><span class="sxs-lookup"><span data-stu-id="48cbf-191">Map preprocessed code to source code</span></span>][DevToolsJavaScriptSourceMaps]

### <a name="using-the-content-scripts-tab-for-microsoft-edge-extensions"></a><span data-ttu-id="48cbf-192">Utilisation de l’onglet Scripts de contenu pour Microsoft Edge extensions</span><span class="sxs-lookup"><span data-stu-id="48cbf-192">Using the Content scripts tab for Microsoft Edge extensions</span></span>

<span data-ttu-id="48cbf-193">Utilisez **l’onglet Scripts** de contenu du volet **Navigateur** pour afficher les scripts de contenu qui ont été chargés par une extension Microsoft Edge que vous avez installée.</span><span class="sxs-lookup"><span data-stu-id="48cbf-193">Use the **Content scripts** tab of the **Navigator** pane to view any content scripts that were loaded by a Microsoft Edge extension that you installed.</span></span> 

:::image type="complex" source="../media/content-scripts-tab.msft.png" alt-text="Onglet Scripts de contenu du volet Navigateur" lightbox="../media/content-scripts-tab.msft.png":::
   <span data-ttu-id="48cbf-195">Onglet **Scripts de contenu** du volet **Navigateur**</span><span class="sxs-lookup"><span data-stu-id="48cbf-195">The **Content scripts** tab of the **Navigator** pane</span></span>
:::image-end:::  

<span data-ttu-id="48cbf-196">Lorsque le débompeur entre dans du code que vous ne connaissez pas, vous pouvez marquer ce code comme du code de bibliothèque, afin d’éviter d’entrer pas à pas dans ce code.</span><span class="sxs-lookup"><span data-stu-id="48cbf-196">When the debugger steps into code that you don't recognize, you might want to mark that code as Library code, to avoid stepping into that code.</span></span>  <span data-ttu-id="48cbf-197">Voir [Marquer les scripts de contenu en tant que code de bibliothèque.][DevToolsJavaScriptGuidesMarkContentScriptsLibraryCode]</span><span class="sxs-lookup"><span data-stu-id="48cbf-197">See [Mark content scripts as Library code][DevToolsJavaScriptGuidesMarkContentScriptsLibraryCode].</span></span>

#### <a name="see-also"></a><span data-ttu-id="48cbf-198">Articles associés</span><span class="sxs-lookup"><span data-stu-id="48cbf-198">See also</span></span>

*   [<span data-ttu-id="48cbf-199">Scripts de contenu</span><span class="sxs-lookup"><span data-stu-id="48cbf-199">Content scripts</span></span>][MDNContentScripts]
*   [<span data-ttu-id="48cbf-200">Didacticiel de création d’extension: partie2</span><span class="sxs-lookup"><span data-stu-id="48cbf-200">Create an extension tutorial Part 2</span></span>][ExtensionsChromiumGetstartPart2ContentScripts]

### <a name="using-the-snippets-tab-to-run-javascript-code-snippets-on-any-webpage"></a><span data-ttu-id="48cbf-201">Utilisation de l’onglet Extraits de code pour exécuter des extraits de code JavaScript sur n’importe quelle page web</span><span class="sxs-lookup"><span data-stu-id="48cbf-201">Using the Snippets tab to run JavaScript code snippets on any webpage</span></span>

<span data-ttu-id="48cbf-202">Utilisez **l’onglet** Extraits de code du volet **Navigateur** pour créer et enregistrer des extraits de code JavaScript, afin que vous pouvez facilement exécuter ces extraits de code sur n’importe quelle page web.</span><span class="sxs-lookup"><span data-stu-id="48cbf-202">Use the **Snippets** tab of the **Navigator** pane to create and save JavaScript code snippets, so that you can easily run these snippets on any webpage.</span></span>

:::image type="complex" source="../media/snippet.msft.png" alt-text="Extrait de code qui insère la bibliothèque jQuery dans une page web" lightbox="../media/snippet.msft.png":::
   <span data-ttu-id="48cbf-204">Extrait de code qui insère la bibliothèque jQuery dans une page web</span><span class="sxs-lookup"><span data-stu-id="48cbf-204">A Snippet that inserts the jQuery library into a webpage</span></span>  
:::image-end:::  

<span data-ttu-id="48cbf-205">Par exemple, supposons que vous entrez fréquemment le code suivant dans la **console**, pour insérer la bibliothèque jQuery dans une page afin que vous pouvez exécuter des commandes jQuery à partir de la **console**:</span><span class="sxs-lookup"><span data-stu-id="48cbf-205">For example, suppose you frequently enter the following code in the **Console**, to insert the jQuery library into a page so that you can run jQuery commands from the **Console**:</span></span>  

```javascript
let script = document.createElement('script');
script.src = 'https://code.jquery.com/jquery-3.2.1.min.js';
script.crossOrigin = 'anonymous';
script.integrity = 'sha256-hwg4gsxgFZhOsEEamdOYGBf13FyQuiTwlAQgxVSNgt4=';
document.head.appendChild(script);
```  

<span data-ttu-id="48cbf-206">Au lieu de cela, vous \*\*\*\* pouvez enregistrer ce code dans un extrait de code, puis l’exécuter facilement quand vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="48cbf-206">Instead, you can save this code in a **Snippet** and then easily run it whenever you need to.</span></span>  <span data-ttu-id="48cbf-207">Lorsque vous sélectionnez `Ctrl` + `S` \(Windows/Linux\) ou `Command` + `S` \(macOS\), DevTools \*\*\*\* enregistre l’extrait de code dans votre système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="48cbf-207">When you select `Ctrl`+`S` \(Windows/Linux\) or `Command`+`S` \(macOS\), DevTools saves the **Snippet** to your file system.</span></span>  

<span data-ttu-id="48cbf-208">Il existe plusieurs façons d’exécuter un extrait de code :</span><span class="sxs-lookup"><span data-stu-id="48cbf-208">There are multiple ways to run a Snippet:</span></span>
*   <span data-ttu-id="48cbf-209">Dans le **volet Navigateur,** sélectionnez l’onglet Extraits de code, puis sélectionnez le fichier d’extraits de code pour l’ouvrir. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="48cbf-209">In the **Navigator** pane, select the **Snippets** tab, and then select the snippets file to open it.</span></span>  <span data-ttu-id="48cbf-210">Ensuite, en bas du volet Éditeur, **sélectionnez Exécuter** \( ![ Le bouton Exécuter ](../media/run-snippet-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="48cbf-210">Then at the bottom of the Editor pane, select **Run** \(![The Run button](../media/run-snippet-icon.msft.png)\).</span></span>  
*   <span data-ttu-id="48cbf-211">Lorsque DevTools a le focus, sélectionnez `Ctrl` + `P` \(Windows/Linux\) ou `Command` + `P` [][DevToolsCommandMenuIndex]\(macOS\) `!` pour ouvrir le menu commande, puis tapez .</span><span class="sxs-lookup"><span data-stu-id="48cbf-211">When DevTools has focus, select `Ctrl`+`P` \(Windows/Linux\) or `Command`+`P` \(macOS\) to open the [Command Menu][DevToolsCommandMenuIndex], and then type `!`.</span></span> 

<span data-ttu-id="48cbf-212">Les extraits de code sont similaires aux bookmarklets.</span><span class="sxs-lookup"><span data-stu-id="48cbf-212">Snippets are similar to bookmarklets.</span></span>

#### <a name="see-also"></a><span data-ttu-id="48cbf-213">Articles associés</span><span class="sxs-lookup"><span data-stu-id="48cbf-213">See also</span></span>

*   [<span data-ttu-id="48cbf-214">Exécuter des extraits de code JavaScript sur n’importe quelle page web avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="48cbf-214">Run snippets of JavaScript on any webpage with Microsoft Edge DevTools</span></span>][DevtoolsGuideChromiumJavascriptSnippets]

### <a name="using-the-command-menu-to-open-files"></a><span data-ttu-id="48cbf-215">Utilisation du menu Commande pour ouvrir des fichiers</span><span class="sxs-lookup"><span data-stu-id="48cbf-215">Using the Command Menu to open files</span></span>

<span data-ttu-id="48cbf-216">Pour ouvrir un fichier, en plus d’utiliser le volet **Navigateur** dans l’outil **Sources,** vous pouvez utiliser le menu Commande de n’importe où dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="48cbf-216">To open a file, in addition to using the **Navigator** pane within the **Sources** tool, you can use the Command Menu from anywhere within DevTools.</span></span>

*   <span data-ttu-id="48cbf-217">N’importe où dans DevTools, sélectionnez `Ctrl` + `P` sur Windows/Linux `Command` + `P` ou sur macOS.</span><span class="sxs-lookup"><span data-stu-id="48cbf-217">From anywhere in DevTools, select `Ctrl`+`P` on Windows/Linux or `Command`+`P` on macOS.</span></span>  <span data-ttu-id="48cbf-218">Le menu Commande s’affiche et répertorie toutes les ressources qui sont dans les onglets du volet **Navigateur** de l’outil **Sources.**</span><span class="sxs-lookup"><span data-stu-id="48cbf-218">The Command Menu appears, and lists all the resources that are in the tabs of the **Navigator** pane of the **Sources** tool.</span></span>  
*   <span data-ttu-id="48cbf-219">Ou, à côté des onglets du volet **Navigateur** dans l’outil **Sources,** sélectionnez le bouton **...** ( Plus**d’options),** puis sélectionnez **Ouvrir le fichier**.</span><span class="sxs-lookup"><span data-stu-id="48cbf-219">Or, next to the tabs of the **Navigator** pane in the **Sources** tool, select the **...** (**More options**) button, and then select **Open File**.</span></span>  

<span data-ttu-id="48cbf-220">Pour afficher et sélectionner dans une liste de tous les fichiers .js, tapez `.js` .</span><span class="sxs-lookup"><span data-stu-id="48cbf-220">To display and pick from a list of all .js files, type `.js`.</span></span>

:::image type="complex" source="../media/sources-command-menu-to-open-file.msft.png" alt-text="Ouverture d’un fichier à l’aide du menu Commande" lightbox="../media/sources-command-menu-to-open-file.msft.png":::
   <span data-ttu-id="48cbf-222">Ouverture d’un fichier à l’aide du menu Commande</span><span class="sxs-lookup"><span data-stu-id="48cbf-222">Opening a file by using the Command Menu</span></span>
:::image-end:::

<span data-ttu-id="48cbf-223">Si vous `?` tapez, le menu Commande affiche plusieurs commandes, notamment **... Ouvrir le fichier**.</span><span class="sxs-lookup"><span data-stu-id="48cbf-223">If you type `?`, the Command Menu shows several commands, including **... Open file**.</span></span>  <span data-ttu-id="48cbf-224">Si vous choisissez `Backspace` d’effacer le menu Commande, une liste de fichiers s’affiche.</span><span class="sxs-lookup"><span data-stu-id="48cbf-224">If you select `Backspace` to clear the Command Menu, a list of files is shown.</span></span>

<span data-ttu-id="48cbf-225">Pour plus d’informations, voir Exécuter des commandes Microsoft Edge menu de commande [DevTools.][DevToolsCommandMenuIndex]</span><span class="sxs-lookup"><span data-stu-id="48cbf-225">For more information, see [Run commands with the Microsoft Edge DevTools Command Menu][DevToolsCommandMenuIndex].</span></span>

## <a name="using-the-editor-pane-to-view-or-edit-files"></a><span data-ttu-id="48cbf-226">Utilisation du volet Éditeur pour afficher ou modifier des fichiers</span><span class="sxs-lookup"><span data-stu-id="48cbf-226">Using the Editor pane to view or edit files</span></span>

<span data-ttu-id="48cbf-227">Utilisez **le** volet Éditeur pour afficher les fichiers frontaux renvoyés à partir du serveur afin de composer la page web actuelle, y compris les fichiers JavaScript, HTML, CSS et image.</span><span class="sxs-lookup"><span data-stu-id="48cbf-227">Use the **Editor** pane to view the front-end files that are returned from the server to compose the current webpage, including JavaScript, HTML, CSS, and image files.</span></span>  <span data-ttu-id="48cbf-228">Lorsque vous modifiez les fichiers \*\*\*\* frontaux dans le volet Éditeur, DevTools met à jour la page web pour exécuter le code modifié.</span><span class="sxs-lookup"><span data-stu-id="48cbf-228">When you edit the front-end files in the **Editor** pane, DevTools updates the webpage to run the modified code.</span></span>  

:::image type="complex" source="../media/editor-pane.msft.png" alt-text="Volet Éditeur dans l’outil Sources" lightbox="../media/editor-pane.msft.png":::
   <span data-ttu-id="48cbf-230">Volet **Éditeur** dans **l’outil Sources**</span><span class="sxs-lookup"><span data-stu-id="48cbf-230">The **Editor** pane in the **Sources** tool</span></span>  
:::image-end:::

<span data-ttu-id="48cbf-231">Le **volet Éditeur** a le niveau de prise en charge suivant pour différents types de fichiers :</span><span class="sxs-lookup"><span data-stu-id="48cbf-231">The **Editor** pane has the following level of support for various file types:</span></span>

| <span data-ttu-id="48cbf-232">Type de fichier</span><span class="sxs-lookup"><span data-stu-id="48cbf-232">File Type</span></span> | <span data-ttu-id="48cbf-233">Actions prises en charge</span><span class="sxs-lookup"><span data-stu-id="48cbf-233">Supported Actions</span></span> |
|---|---|
| <span data-ttu-id="48cbf-234">JavaScript</span><span class="sxs-lookup"><span data-stu-id="48cbf-234">JavaScript</span></span> | <span data-ttu-id="48cbf-235">Afficher, modifier et déboguer.</span><span class="sxs-lookup"><span data-stu-id="48cbf-235">View, edit, and debug.</span></span> |
| <span data-ttu-id="48cbf-236">CSS</span><span class="sxs-lookup"><span data-stu-id="48cbf-236">CSS</span></span> | <span data-ttu-id="48cbf-237">Afficher et modifier.</span><span class="sxs-lookup"><span data-stu-id="48cbf-237">View and edit.</span></span> |
| <span data-ttu-id="48cbf-238">HTML</span><span class="sxs-lookup"><span data-stu-id="48cbf-238">HTML</span></span> | <span data-ttu-id="48cbf-239">Afficher et modifier.</span><span class="sxs-lookup"><span data-stu-id="48cbf-239">View and edit.</span></span> |
| <span data-ttu-id="48cbf-240">Images</span><span class="sxs-lookup"><span data-stu-id="48cbf-240">Images</span></span> | <span data-ttu-id="48cbf-241">Afficher.</span><span class="sxs-lookup"><span data-stu-id="48cbf-241">View.</span></span> |

<span data-ttu-id="48cbf-242">Par défaut, les modifications sont ignorées lorsque vous actualisez la page web.</span><span class="sxs-lookup"><span data-stu-id="48cbf-242">By default, edits are discarded when you refresh the webpage.</span></span>  <span data-ttu-id="48cbf-243">Pour plus d’informations sur la façon d’enregistrer les modifications apportées à votre système de fichiers, voir Utilisation de l’onglet Système de fichiers pour définir un espace de travail [local,](#using-the-filesystem-tab-to-define-a-local-workspace)ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="48cbf-243">For information about how to save the changes to your file system, see [Using the Filesystem tab to define a local Workspace](#using-the-filesystem-tab-to-define-a-local-workspace), above.</span></span>

<span data-ttu-id="48cbf-244">Les sous-sections suivantes couvrent le volet Éditeur :</span><span class="sxs-lookup"><span data-stu-id="48cbf-244">The following subsections cover the Editor pane:</span></span>
*   [<span data-ttu-id="48cbf-245">Modification d’un fichier JavaScript</span><span class="sxs-lookup"><span data-stu-id="48cbf-245">Editing a JavaScript file</span></span>](#editing-a-javascript-file)
*   [<span data-ttu-id="48cbf-246">Reformatage d’un fichier JavaScript minifié avec une impression assez grande</span><span class="sxs-lookup"><span data-stu-id="48cbf-246">Reformatting a minified JavaScript file with pretty-print</span></span>](#reformatting-a-minified-javascript-file-with-pretty-print)
*   [<span data-ttu-id="48cbf-247">Mappage du code minifié à votre code source pour afficher du code lisible</span><span class="sxs-lookup"><span data-stu-id="48cbf-247">Mapping minified code to your source code to show readable code</span></span>](#mapping-minified-code-to-your-source-code-to-show-readable-code)
*   [<span data-ttu-id="48cbf-248">Transformations du code source au code frontal compilé</span><span class="sxs-lookup"><span data-stu-id="48cbf-248">Transformations from source code to compiled front-end code</span></span>](#transformations-from-source-code-to-compiled-front-end-code)
*   [<span data-ttu-id="48cbf-249">Modification d’un fichier CSS</span><span class="sxs-lookup"><span data-stu-id="48cbf-249">Editing a CSS file</span></span>](#editing-a-css-file)
*   [<span data-ttu-id="48cbf-250">Modification d’un fichier HTML</span><span class="sxs-lookup"><span data-stu-id="48cbf-250">Editing an HTML file</span></span>](#editing-an-html-file)
*   [<span data-ttu-id="48cbf-251">Accès à un numéro de ligne ou à une fonction</span><span class="sxs-lookup"><span data-stu-id="48cbf-251">Going to a line number or function</span></span>](#going-to-a-line-number-or-function)
*   [<span data-ttu-id="48cbf-252">Affichage des fichiers sources lors de l’utilisation d’un autre outil</span><span class="sxs-lookup"><span data-stu-id="48cbf-252">Displaying source files when using a different tool</span></span>](#displaying-source-files-when-using-a-different-tool)

### <a name="editing-a-javascript-file"></a><span data-ttu-id="48cbf-253">Modification d’un fichier JavaScript</span><span class="sxs-lookup"><span data-stu-id="48cbf-253">Editing a JavaScript file</span></span>

<span data-ttu-id="48cbf-254">Pour modifier un fichier JavaScript dans DevTools, utilisez le volet Éditeur, dans l’outil **Sources.** \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="48cbf-254">To edit a JavaScript file in DevTools, use the **Editor** pane, within the **Sources** tool.</span></span>

:::image type="complex" source="../media/editing-js-in-editor-pane.msft.png" alt-text="Modification de JavaScript dans le volet éditeur" lightbox="../media/editing-js-in-editor-pane.msft.png":::
   <span data-ttu-id="48cbf-256">Modification de JavaScript dans le volet **éditeur**</span><span class="sxs-lookup"><span data-stu-id="48cbf-256">Editing JavaScript in the **Editor** pane</span></span>  
:::image-end:::

<span data-ttu-id="48cbf-257">Pour charger un fichier dans le volet Éditeur, utilisez l’onglet **Page** dans le volet **Navigateur** (à gauche).</span><span class="sxs-lookup"><span data-stu-id="48cbf-257">To load a file into the Editor pane, use the **Page** tab in the **Navigator** pane (on the left).</span></span>  <span data-ttu-id="48cbf-258">Vous pouvez également utiliser le **menu**DevTools, comme suit : dans le coin supérieur droit de DevTools, sélectionnez Personnaliser et contrôler **DevTools** \( \), puis `...` **sélectionnez Ouvrir un fichier.**</span><span class="sxs-lookup"><span data-stu-id="48cbf-258">Or use the **Command Menu**, as follows: in the upper right of DevTools, select **Customize and control DevTools** \(`...`\) and then select **Open File**.</span></span>

#### <a name="save-and-undo"></a><span data-ttu-id="48cbf-259">Enregistrer et annuler</span><span class="sxs-lookup"><span data-stu-id="48cbf-259">Save and Undo</span></span>

<span data-ttu-id="48cbf-260">Pour que les modifications JavaScript soient appliquées, sélectionnez `Ctrl`+`S` \ (Windows, Linux \) ou `Command`+`S` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="48cbf-260">For JavaScript changes to take effect, select `Ctrl`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\).</span></span>  

<span data-ttu-id="48cbf-261">Si vous modifiez un fichier, un astérisque s’affiche à côté du nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="48cbf-261">If you change a file, an asterisk appears next to the file name.</span></span>
*   <span data-ttu-id="48cbf-262">Pour enregistrer les modifications, sélectionnez `Ctrl` + `S` sur Windows/Linux `Command` + `S` ou sur macOS.</span><span class="sxs-lookup"><span data-stu-id="48cbf-262">To save changes, select `Ctrl`+`S` on Windows/Linux or `Command`+`S` on macOS.</span></span>
*   <span data-ttu-id="48cbf-263">Pour annuler une modification, sélectionnez `Ctrl` + `Z` sur Windows/Linux `Command` + `Z` ou sur macOS.</span><span class="sxs-lookup"><span data-stu-id="48cbf-263">To undo a change, select `Ctrl`+`Z` on Windows/Linux or `Command`+`Z` on macOS.</span></span>

<span data-ttu-id="48cbf-264">Par défaut, vos modifications sont ignorées lorsque vous actualisez la page web.</span><span class="sxs-lookup"><span data-stu-id="48cbf-264">By default, your edits are discarded when you refresh the webpage.</span></span>  <span data-ttu-id="48cbf-265">Pour plus d’informations sur l’enregistrer dans votre système de fichiers local, voir Modifier des fichiers [avec Workspaces][DevtoolsGuideChromiumWorkspacesIndex].</span><span class="sxs-lookup"><span data-stu-id="48cbf-265">For more information about how to save the changes in your local file system, see [Edit files with Workspaces][DevtoolsGuideChromiumWorkspacesIndex].</span></span>

#### <a name="find-and-replace"></a><span data-ttu-id="48cbf-266">Rechercher et remplacer</span><span class="sxs-lookup"><span data-stu-id="48cbf-266">Find and Replace</span></span>

<span data-ttu-id="48cbf-267">Pour rechercher du texte dans \*\*\*\* le fichier actuel, sélectionnez le volet Éditeur pour lui donner le focus, puis sélectionnez `Ctrl` + `F` sur Windows/Linux ou `Command` + `F` sur macOS.</span><span class="sxs-lookup"><span data-stu-id="48cbf-267">To find text in the current file, select the **Editor** pane to give it focus, and then select `Ctrl`+`F` on Windows/Linux, or `Command`+`F` on macOS.</span></span>  

:::image type="complex" source="../media/find-replace.msft.png" alt-text="Rechercher et remplacer, dans le volet Éditeur de l’outil Sources" lightbox="../media/find-replace.msft.png":::
   <span data-ttu-id="48cbf-269">**Rechercher** et **remplacer**, dans le volet **Éditeur** de l’outil **Sources**</span><span class="sxs-lookup"><span data-stu-id="48cbf-269">**Find** and **Replace**, in the **Editor** pane of the **Sources** tool</span></span>
:::image-end:::

<span data-ttu-id="48cbf-270">Pour rechercher et remplacer du texte, sélectionnez le bouton Remplacer **(** **A-\>B**) à gauche de la **boîte** de texte Rechercher.</span><span class="sxs-lookup"><span data-stu-id="48cbf-270">To find and replace text, select the **Replace** (**A-\>B**) button to the left of the **Find** textbox.</span></span> <span data-ttu-id="48cbf-271">Le **bouton** Remplacer (**A-\>B**) s’affiche lors de l’affichage d’un fichier modifiable.</span><span class="sxs-lookup"><span data-stu-id="48cbf-271">The **Replace** (**A-\>B**) button appears when viewing an editable file.</span></span>

#### <a name="showing-the-changes-you-made"></a><span data-ttu-id="48cbf-272">Affichage des modifications que vous avez apportées</span><span class="sxs-lookup"><span data-stu-id="48cbf-272">Showing the changes you made</span></span>

<span data-ttu-id="48cbf-273">Pour passer en revue les modifications apportées \*\*\*\* à un fichier, cliquez avec le bouton droit dans le volet Éditeur, puis sélectionnez **Modifications locales.**</span><span class="sxs-lookup"><span data-stu-id="48cbf-273">To review the changes you made to a file, right-click in the **Editor** pane and then select **Local Modifications**.</span></span>

<span data-ttu-id="48cbf-274">Le **caisse s’ouvre** en bas de DevTools, affichant vos modifications dans l’onglet **Modifications.**</span><span class="sxs-lookup"><span data-stu-id="48cbf-274">The **Drawer** opens at the bottom of DevTools, showing your changes within the **Changes** tab.</span></span>

:::image type="complex" source="../media/local-modifications.msft.png" alt-text="Affichage des modifications locales, sous l’onglet Modifications du caisse" lightbox="../media/local-modifications.msft.png":::
   <span data-ttu-id="48cbf-276">Affichage **des modifications locales,** sous **l’onglet Modifications** du **caisse**</span><span class="sxs-lookup"><span data-stu-id="48cbf-276">Showing **Local Modifications**, in the **Changes** tab of the **Drawer**</span></span>
:::image-end:::

#### <a name="changes-inside-a-function-take-effect"></a><span data-ttu-id="48cbf-277">Les modifications à l’intérieur d’une fonction prennent effet</span><span class="sxs-lookup"><span data-stu-id="48cbf-277">Changes inside a function take effect</span></span>

<span data-ttu-id="48cbf-278">DevTools ne ré-exécute pas de script, de sorte que les seules modifications JavaScript qui prennent effet sont les modifications que vous a faites au sein des fonctions.</span><span class="sxs-lookup"><span data-stu-id="48cbf-278">DevTools doesn't re-run a script, so the only JavaScript changes that take effect are changes that you make within functions.</span></span>  <span data-ttu-id="48cbf-279">Par exemple, dans la figure suivante, nous avons ajouté le code suivant au code JavaScript renvoyé par le serveur :</span><span class="sxs-lookup"><span data-stu-id="48cbf-279">For example, in the following figure, we added the following code to the JavaScript that is returned by the server:</span></span>  
*   <span data-ttu-id="48cbf-280">Nous avons ajouté l’instruction `console.log('A')` en dehors de n’importe quelle fonction.</span><span class="sxs-lookup"><span data-stu-id="48cbf-280">We added the statement `console.log('A')` outside of any function.</span></span>  
*   <span data-ttu-id="48cbf-281">Nous avons ajouté l’instruction `console.log('B')` à l’intérieur d’une `onClick` fonction.</span><span class="sxs-lookup"><span data-stu-id="48cbf-281">We added the statement `console.log('B')` inside an `onClick` function.</span></span>  
<span data-ttu-id="48cbf-282">Nous avons ensuite enregistré les modifications, entré des numéros dans le formulaire, puis sélectionné le bouton du formulaire pour envoyer le formulaire.</span><span class="sxs-lookup"><span data-stu-id="48cbf-282">We then saved the changes, entered numbers into the form, and then selected the form button to send the form.</span></span>  

<span data-ttu-id="48cbf-283">Après l’envoi du formulaire, qui est au niveau `console.log('A')` de l’étendue globale, ne s’exécute pas, mais, à l’intérieur d’une fonction, s’exécute, en sortie dans `console.log('B')` la console `onClick` `B` :</span><span class="sxs-lookup"><span data-stu-id="48cbf-283">After submitting the form, `console.log('A')`, which is at global scope, doesn't run, but `console.log('B')`, inside an `onClick` function, does run, outputting `B` to the Console:</span></span>

:::image type="complex" source="../media/edit-js.msft.png" alt-text="JavaScript de portée globale n’est pas ré-exécuté" lightbox="../media/edit-js.msft.png":::
   <span data-ttu-id="48cbf-285">JavaScript de portée globale n’est pas ré-exécuté</span><span class="sxs-lookup"><span data-stu-id="48cbf-285">Global-scope JavaScript is not re-run</span></span>  
:::image-end:::

### <a name="reformatting-a-minified-javascript-file-with-pretty-print"></a><span data-ttu-id="48cbf-286">Reformatage d’un fichier JavaScript minifié avec une impression assez grande</span><span class="sxs-lookup"><span data-stu-id="48cbf-286">Reformatting a minified JavaScript file with pretty-print</span></span>

<span data-ttu-id="48cbf-287">Pour utiliser pretty-print pour reformater un fichier \*\*\*\* afin de le rendre lisible, sélectionnez le bouton d’impression Pretty \( Format \), qui est affiché sous forme d’accolades, en bas du volet ![ ](../media/format-icon.msft.png) Éditeur.</span><span class="sxs-lookup"><span data-stu-id="48cbf-287">To use pretty-print to reformat a file to make it readable, select the **Pretty print** button \(![Format](../media/format-icon.msft.png)\), which is shown as braces, at the bottom of the Editor pane.</span></span>  <span data-ttu-id="48cbf-288">Ou, si un **bouton Assez** imprimé apparaît en haut du volet Éditeur, vous pouvez sélectionner ce bouton.</span><span class="sxs-lookup"><span data-stu-id="48cbf-288">Or, if a **Pretty-print** button appears at the top of the Editor pane, you can select that button.</span></span>

:::image type="complex" source="../media/minified.msft.png" alt-text="Bouton d’impression Pretty" lightbox="../media/minified.msft.png":::
   <span data-ttu-id="48cbf-290">Bouton **d’impression** Pretty</span><span class="sxs-lookup"><span data-stu-id="48cbf-290">The **Pretty print** button</span></span>  
:::image-end:::  

<span data-ttu-id="48cbf-291">Le fichier reformaté apparaît dans un nouvel onglet, avec le nom `:formatted` du fichier.</span><span class="sxs-lookup"><span data-stu-id="48cbf-291">The reformatted file appears in a new tab, with `:formatted` appended to the file name.</span></span>  <span data-ttu-id="48cbf-292">Le code reformaté est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="48cbf-292">The reformatted code is read-only.</span></span>  

:::image type="complex" source="../media/pretty-printed.msft.png" alt-text="Un fichier JavaScript assez imprimé (reformaté)" lightbox="../media/pretty-printed.msft.png":::
   <span data-ttu-id="48cbf-294">Un fichier JavaScript assez imprimé (reformaté)</span><span class="sxs-lookup"><span data-stu-id="48cbf-294">A pretty-printed (reformatted) JavaScript file</span></span>  
:::image-end:::  

<span data-ttu-id="48cbf-295">Pour faire défiler le fichier reformaté jusqu’au code que vous sélectionnez dans le fichier minifié :</span><span class="sxs-lookup"><span data-stu-id="48cbf-295">To make the reformatted file scroll to the code that you select in the minified file:</span></span> 
1.   <span data-ttu-id="48cbf-296">Si l’onglet de fichier reformaté est ouvert, fermez-le.</span><span class="sxs-lookup"><span data-stu-id="48cbf-296">If the reformatted file tab is open, close it.</span></span>  
1.   <span data-ttu-id="48cbf-297">Sélectionnez du code dans le fichier minifié dans le volet Éditeur.</span><span class="sxs-lookup"><span data-stu-id="48cbf-297">Select some code in the minified file in the Editor pane.</span></span>
1.   <span data-ttu-id="48cbf-298">Sélectionnez **le bouton Imprimer.**</span><span class="sxs-lookup"><span data-stu-id="48cbf-298">Select the **Pretty print** button.</span></span>
<span data-ttu-id="48cbf-299">Le code formaté apparaît dans un nouvel onglet, en faisant défiler jusqu’au code que vous avez sélectionné.</span><span class="sxs-lookup"><span data-stu-id="48cbf-299">The formatted code appears in a new tab, scrolled to the code that you selected.</span></span>

<span data-ttu-id="48cbf-300">Pour plus d’informations, voir [Reformater un fichier JavaScript minifié avec une impression assez .][DevToolsJavaScriptReferenceReformat]</span><span class="sxs-lookup"><span data-stu-id="48cbf-300">For more information, see [Reformat a minified JavaScript file with pretty-print][DevToolsJavaScriptReferenceReformat].</span></span>  

### <a name="mapping-minified-code-to-your-source-code-to-show-readable-code"></a><span data-ttu-id="48cbf-301">Mappage du code minifié à votre code source pour afficher du code lisible</span><span class="sxs-lookup"><span data-stu-id="48cbf-301">Mapping minified code to your source code to show readable code</span></span>

<span data-ttu-id="48cbf-302">Les cartes sources provenant de préprocesseurs entraînent le chargement par DevTools de vos fichiers sources JavaScript d’origine en plus de vos fichiers JavaScript transformés et minifiés qui sont renvoyés par le serveur.</span><span class="sxs-lookup"><span data-stu-id="48cbf-302">Source maps from preprocessors cause DevTools to load your original JavaScript source files in addition to your minified, transformed JavaScript files that are returned by the server.</span></span>  <span data-ttu-id="48cbf-303">Vous affichez ensuite vos fichiers sources d’origine pendant que vous définissez des points d’arrêt et le code pas à pas.</span><span class="sxs-lookup"><span data-stu-id="48cbf-303">You then view your original source files while you set breakpoints and step through code.</span></span>  <span data-ttu-id="48cbf-304">Pendant ce temps, Microsoft Edge exécute réellement votre code minifié.</span><span class="sxs-lookup"><span data-stu-id="48cbf-304">Meanwhile, Microsoft Edge is actually running your minified code.</span></span>  

<span data-ttu-id="48cbf-305">Dans \*\*\*\* le volet Éditeur, si vous cliquez avec le bouton droit sur un fichier JavaScript, puis sélectionnez Ajouter un plan **source,** une boîte de message apparaît, avec une zone de texte **URL** de carte source et un bouton **Ajouter.**</span><span class="sxs-lookup"><span data-stu-id="48cbf-305">In the **Editor** pane, if you right-click a JavaScript file and then select **Add source map**, a popup box appears, with a **Source map URL** textbox and an **Add** button.</span></span>

<span data-ttu-id="48cbf-306">L’approche de mappage de source permet de garder votre code frontal lisible et décomscriptible même après la combinaison, la minification ou la compilation de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="48cbf-306">The source-mapping approach keeps your front-end code human-readable and debuggable even after you combine, minify, or compile it.</span></span>
<span data-ttu-id="48cbf-307">Pour plus d’informations, voir [Ma cartographier le code prétraité au code source.][DevToolsJavaScriptSourceMaps]</span><span class="sxs-lookup"><span data-stu-id="48cbf-307">For more information, see [Map preprocessed code to source code][DevToolsJavaScriptSourceMaps].</span></span>

### <a name="transformations-from-source-code-to-compiled-front-end-code"></a><span data-ttu-id="48cbf-308">Transformations du code source au code frontal compilé</span><span class="sxs-lookup"><span data-stu-id="48cbf-308">Transformations from source code to compiled front-end code</span></span>

<span data-ttu-id="48cbf-309">Si vous utilisez une infrastructure qui transforme vos fichiers JavaScript, tels que React, votre javaScript source local peut être différent du JavaScript frontal renvoyé par le serveur.</span><span class="sxs-lookup"><span data-stu-id="48cbf-309">If you use a framework that transforms your JavaScript files, such as React, your local source JavaScript might be different than the front-end JavaScript that's returned by the server.</span></span>  <span data-ttu-id="48cbf-310">Les espaces de travail ne sont pas pris en charge dans ce scénario, mais le mappage de code source est pris en charge dans ce scénario.</span><span class="sxs-lookup"><span data-stu-id="48cbf-310">Workspaces aren't supported in this scenario, but source code mapping is supported in this scenario.</span></span>  

<span data-ttu-id="48cbf-311">Dans un environnement de développement, votre serveur peut inclure vos cartes sources et vos fichiers d’origine `.ts` `.jsx` ou de React.</span><span class="sxs-lookup"><span data-stu-id="48cbf-311">In a development environment, your server might include your source maps and your original `.ts` or `.jsx` files for React.</span></span>  <span data-ttu-id="48cbf-312">**L’outil Sources** affiche ces fichiers, mais ne vous permet pas de modifier ces fichiers.</span><span class="sxs-lookup"><span data-stu-id="48cbf-312">The **Sources** tool displays these files, but doesn't allow you to edit these files.</span></span>  <span data-ttu-id="48cbf-313">Lorsque vous définissez des points d’arrêt et utilisez le débogueur, DevTools affiche vos fichiers d’origine, mais pas à pas dans la version minifiée de vos `.ts` `.jsx` fichiers JavaScript.</span><span class="sxs-lookup"><span data-stu-id="48cbf-313">When you set breakpoints and use the debugger, DevTools displays your original `.ts` or `.jsx` files, but actually steps-through the minified version of your JavaScript files.</span></span>

<span data-ttu-id="48cbf-314">Dans ce scénario, l’outil **Sources** est utile pour inspecter et passer pas à pas le JavaScript frontal transformé renvoyé à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="48cbf-314">In this scenario, the **Sources** tool is useful for inspecting and stepping-through the transformed, front-end JavaScript that's returned from the server.</span></span>  <span data-ttu-id="48cbf-315">Utilisez le débogger pour définir des expressions Watch et utilisez la console pour entrer des expressions JavaScript afin de manipuler des données dans l’étendue.</span><span class="sxs-lookup"><span data-stu-id="48cbf-315">Use the debugger to define Watch expressions, and use the Console to enter JavaScript expressions to manipulate data that's in-scope.</span></span>

### <a name="editing-a-css-file"></a><span data-ttu-id="48cbf-316">Modification d’un fichier CSS</span><span class="sxs-lookup"><span data-stu-id="48cbf-316">Editing a CSS file</span></span>

<span data-ttu-id="48cbf-317">Il existe deux façons de modifier CSS dans DevTools :</span><span class="sxs-lookup"><span data-stu-id="48cbf-317">There are two ways to edit CSS in DevTools:</span></span>
*   <span data-ttu-id="48cbf-318">Dans **l’outil Elements,** vous travaillez avec un paramètre CSS à la fois, via des contrôles d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="48cbf-318">In the **Elements** tool, you work with one CSS setting at a time, through user interface controls.</span></span>  <span data-ttu-id="48cbf-319">Cette approche est recommandée dans la plupart des cas.</span><span class="sxs-lookup"><span data-stu-id="48cbf-319">This approach is recommended in most cases.</span></span>  <span data-ttu-id="48cbf-320">Pour plus d’informations, voir [Modifier les styles de police CSS][DevToolsInspectStylesEditFonts]et les paramètres dans le volet Styles.</span><span class="sxs-lookup"><span data-stu-id="48cbf-320">For more information, see [Edit CSS font styles and settings in the Styles pane][DevToolsInspectStylesEditFonts].</span></span>
*   <span data-ttu-id="48cbf-321">Dans **l’outil Sources,** vous utilisez un éditeur de texte.</span><span class="sxs-lookup"><span data-stu-id="48cbf-321">In the **Sources** tool, you use a text editor.</span></span>

<span data-ttu-id="48cbf-322">L’outil Sources prend en charge la modification directe d’un fichier CSS.</span><span class="sxs-lookup"><span data-stu-id="48cbf-322">The Sources tool supports directly editing a CSS file.</span></span>  <span data-ttu-id="48cbf-323">Par exemple, si vous modifiez le fichier CSS à partir du didacticiel Modifier les fichiers avec des [espaces][DevtoolsGuideChromiumWorkspacesIndex] de travail pour qu’il corresponde à la règle de style ci-dessous, l’élément dans le coin supérieur gauche de la page web rendue se transforme en `H1` vert :</span><span class="sxs-lookup"><span data-stu-id="48cbf-323">For example, if you edit the CSS file from the tutorial [Edit files with Workspaces][DevtoolsGuideChromiumWorkspacesIndex] to match the style rule below, the `H1` element in the upper left of the rendered webpage changes to green:</span></span>

```css
h1 {
  color: green;
}  
```

:::image type="complex" source="../media/edit-css.msft.png" alt-text="Modifier CSS dans le volet Éditeur pour changer la couleur du texte du titre H1 en vert" lightbox="../media/edit-css.msft.png":::
   <span data-ttu-id="48cbf-325">Modifier CSS dans **le** volet Éditeur pour changer la couleur du texte du titre en `H1` vert</span><span class="sxs-lookup"><span data-stu-id="48cbf-325">Edit CSS in the **Editor** pane to change the text color of the `H1` heading to green</span></span>  
:::image-end:::  

<span data-ttu-id="48cbf-326">Les modifications CSS prennent effet immédiatement ; vous n’avez pas besoin d’enregistrer manuellement les modifications.</span><span class="sxs-lookup"><span data-stu-id="48cbf-326">CSS changes take effect immediately; you don't need to manually save the changes.</span></span>

#### <a name="see-also"></a><span data-ttu-id="48cbf-327">Articles associés</span><span class="sxs-lookup"><span data-stu-id="48cbf-327">See also</span></span>

*   [<span data-ttu-id="48cbf-328">Modifier les styles et paramètres de police CSS dans le volet Styles</span><span class="sxs-lookup"><span data-stu-id="48cbf-328">Edit CSS font styles and settings in the Styles pane</span></span>][DevToolsInspectStylesEditFonts]

*   <span data-ttu-id="48cbf-329">[DevTools pour les débutants : Mise en place de CSS][DevToolsBeginnersCss] - didacticiel</span><span class="sxs-lookup"><span data-stu-id="48cbf-329">[DevTools for beginners: Get started with CSS][DevToolsBeginnersCss] - tutorial</span></span>

### <a name="editing-an-html-file"></a><span data-ttu-id="48cbf-330">Modification d’un fichier HTML</span><span class="sxs-lookup"><span data-stu-id="48cbf-330">Editing an HTML file</span></span>

<span data-ttu-id="48cbf-331">Il existe deux façons de modifier le code HTML dans DevTools :</span><span class="sxs-lookup"><span data-stu-id="48cbf-331">There are two ways to edit HTML in DevTools:</span></span>  
*   <span data-ttu-id="48cbf-332">Dans **l’outil Elements,** vous travaillez avec un élément HTML à la fois, via des contrôles d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="48cbf-332">In the **Elements** tool, you work with one HTML element at a time, through user interface controls.</span></span>  
*   <span data-ttu-id="48cbf-333">Dans **l’outil Sources,** vous utilisez un éditeur de texte.</span><span class="sxs-lookup"><span data-stu-id="48cbf-333">In the **Sources** tool, you use a text editor.</span></span>  

:::image type="complex" source="../media/sources-html-editor.msft.png" alt-text="Éditeur HTML de l’outil Sources" lightbox="../media/sources-html-editor.msft.png":::
   <span data-ttu-id="48cbf-335">Éditeur HTML de l’outil **Sources**</span><span class="sxs-lookup"><span data-stu-id="48cbf-335">The HTML editor of the **Sources** tool</span></span>
:::image-end:::  

<span data-ttu-id="48cbf-336">Contrairement à un fichier JavaScript ou CSS, un fichier HTML renvoyé par le serveur web ne peut pas être modifié directement dans l’outil Sources.</span><span class="sxs-lookup"><span data-stu-id="48cbf-336">Unlike a JavaScript or CSS file, an HTML file that is returned by the web server cannot be directly edited in the Sources tool.</span></span>  <span data-ttu-id="48cbf-337">Pour modifier un fichier HTML à l’aide de l’Éditeur de l’outil Sources, le fichier HTML doit se trouver dans un espace de travail ou sous l’onglet **Remplacements.**  Consultez les sous-sections de l’article actuel :</span><span class="sxs-lookup"><span data-stu-id="48cbf-337">To edit an HTML file using the Editor of the Sources tool, the HTML file must be in a Workspace or on the **Overrides** tab.  See these subsections of the current article:</span></span>
*   [<span data-ttu-id="48cbf-338">Utilisation de l’onglet Système de fichiers pour définir un espace de travail local</span><span class="sxs-lookup"><span data-stu-id="48cbf-338">Using the Filesystem tab to define a local Workspace</span></span>](#using-the-filesystem-tab-to-define-a-local-workspace)
*   [<span data-ttu-id="48cbf-339">Utilisation de l’onglet Remplacements pour remplacer les fichiers serveur par des fichiers locaux</span><span class="sxs-lookup"><span data-stu-id="48cbf-339">Using the Overrides tab to override server files with local files</span></span>](#using-the-overrides-tab-to-override-server-files-with-local-files)
    
<span data-ttu-id="48cbf-340">Pour enregistrer les modifications, sélectionnez `Ctrl` + `S` sur Windows/Linux `Command` + `S` ou sur macOS.</span><span class="sxs-lookup"><span data-stu-id="48cbf-340">To save changes, select `Ctrl`+`S` on Windows/Linux or `Command`+`S` on macOS.</span></span>  <span data-ttu-id="48cbf-341">Un fichier modifié est marqué par un astérisque.</span><span class="sxs-lookup"><span data-stu-id="48cbf-341">An edited file is marked by an asterisk.</span></span>  

<span data-ttu-id="48cbf-342">Pour trouver du texte, sélectionnez `Ctrl` + `F` sur Windows/Linux `Command` + `F` ou sur macOS.</span><span class="sxs-lookup"><span data-stu-id="48cbf-342">To find text, select `Ctrl`+`F` on Windows/Linux or `Command`+`F` on macOS.</span></span>

<span data-ttu-id="48cbf-343">Pour annuler une modification, sélectionnez `Ctrl` + `Z` sur Windows/Linux `Command` + `Z` ou sur macOS.</span><span class="sxs-lookup"><span data-stu-id="48cbf-343">To undo an edit, select `Ctrl`+`Z` on Windows/Linux or `Command`+`Z` on macOS.</span></span>

<span data-ttu-id="48cbf-344">Pour afficher d’autres commandes lors de la modification d’un fichier HTML, dans le volet Éditeur, cliquez avec le bouton droit sur le fichier HTML.</span><span class="sxs-lookup"><span data-stu-id="48cbf-344">To view other commands while editing an HTML file, in the Editor pane, right-click the HTML file.</span></span>

<span data-ttu-id="48cbf-345">Vous pouvez également modifier le code HTML à l’aide d’un éditeur HTML, plutôt que de DevTools.</span><span class="sxs-lookup"><span data-stu-id="48cbf-345">You can also edit HTML by using an HTML editor, rather than DevTools.</span></span>  <span data-ttu-id="48cbf-346">Par exemple, l’article [DevTools for beginners: Get started with HTML and the DOM][DevToolsBeginnersHtml] uses a website that enables HTML editing within the webpage.</span><span class="sxs-lookup"><span data-stu-id="48cbf-346">For example, the article [DevTools for beginners: Get started with HTML and the DOM][DevToolsBeginnersHtml] uses a website that enables HTML editing within the webpage.</span></span>

### <a name="going-to-a-line-number-or-function"></a><span data-ttu-id="48cbf-347">Accès à un numéro de ligne ou à une fonction</span><span class="sxs-lookup"><span data-stu-id="48cbf-347">Going to a line number or function</span></span>

<span data-ttu-id="48cbf-348">Pour aller à un numéro de ligne ou un symbole (par exemple, un nom de fonction) dans le fichier qui est ouvert dans le volet Éditeur, vous pouvez utiliser le menu Commande, plutôt que de faire défiler le fichier.</span><span class="sxs-lookup"><span data-stu-id="48cbf-348">To go to a line number or symbol (such as a function name) in the file which is open in the Editor pane, you can use the Command Menu, rather than scrolling through the file.</span></span>

1.   <span data-ttu-id="48cbf-349">Dans le **volet Navigateur,** sélectionnez les ellipses (...) (**Plus d’options**), puis sélectionnez **Ouvrir le fichier**.</span><span class="sxs-lookup"><span data-stu-id="48cbf-349">In the **Navigator** pane, select the ellipses (...) (**More options**), and then select **Open File**.</span></span>  <span data-ttu-id="48cbf-350">Le menu Commande s’affiche.</span><span class="sxs-lookup"><span data-stu-id="48cbf-350">The Command Menu appears.</span></span>  
1.   <span data-ttu-id="48cbf-351">Tapez l’un des caractères suivants :</span><span class="sxs-lookup"><span data-stu-id="48cbf-351">Type one of the following characters:</span></span>  

| <span data-ttu-id="48cbf-352">Caractère</span><span class="sxs-lookup"><span data-stu-id="48cbf-352">Character</span></span> | <span data-ttu-id="48cbf-353">Nom de la commande</span><span class="sxs-lookup"><span data-stu-id="48cbf-353">Command name</span></span> | <span data-ttu-id="48cbf-354">Objectif</span><span class="sxs-lookup"><span data-stu-id="48cbf-354">Purpose</span></span> |
|---|---|---|
| <span data-ttu-id="48cbf-355">\:</span><span class="sxs-lookup"><span data-stu-id="48cbf-355">\:</span></span> | **<span data-ttu-id="48cbf-356">Aller à la ligne</span><span class="sxs-lookup"><span data-stu-id="48cbf-356">Go to line</span></span>** | <span data-ttu-id="48cbf-357">Aller à un numéro de ligne.</span><span class="sxs-lookup"><span data-stu-id="48cbf-357">Go to a line number.</span></span> |
| \@ | **<span data-ttu-id="48cbf-358">Go to symbol</span><span class="sxs-lookup"><span data-stu-id="48cbf-358">Go to symbol</span></span>** | <span data-ttu-id="48cbf-359">Go to a function.</span><span class="sxs-lookup"><span data-stu-id="48cbf-359">Go to a function.</span></span>  <span data-ttu-id="48cbf-360">Lorsque vous tapez, le menu Commande répertorie les fonctions qui se trouvent dans le fichier JavaScript qui est `@` ouvert dans le volet Éditeur.</span><span class="sxs-lookup"><span data-stu-id="48cbf-360">When you type `@`, the Command Menu lists the functions that are found in the JavaScript file which is open in the Editor pane.</span></span> |
   
<span data-ttu-id="48cbf-361">Pour plus d’informations, voir Exécuter des commandes Microsoft Edge menu de commande [DevTools.][DevToolsCommandMenuIndex]</span><span class="sxs-lookup"><span data-stu-id="48cbf-361">For more information, see [Run commands with the Microsoft Edge DevTools Command Menu][DevToolsCommandMenuIndex].</span></span>

### <a name="displaying-source-files-when-using-a-different-tool"></a><span data-ttu-id="48cbf-362">Affichage des fichiers sources lors de l’utilisation d’un autre outil</span><span class="sxs-lookup"><span data-stu-id="48cbf-362">Displaying source files when using a different tool</span></span>

<span data-ttu-id="48cbf-363">L’endroit principal pour afficher les fichiers sources dans DevTools se trouve dans **l’outil Sources.**</span><span class="sxs-lookup"><span data-stu-id="48cbf-363">The main place to view source files in the DevTools is within the **Sources** tool.</span></span>  <span data-ttu-id="48cbf-364">Mais parfois, vous devez accéder à d’autres outils, tels que **des** éléments ou une **console,** lors de l’affichage ou de la modification de vos fichiers sources.</span><span class="sxs-lookup"><span data-stu-id="48cbf-364">But sometimes you need to access other tools, such as **Elements** or **Console**, while viewing or editing your source files.</span></span>  <span data-ttu-id="48cbf-365">Utilisez **l’outil Sources rapides** dans le [caisse.][DevtoolsCustomizeIndexDrawer]</span><span class="sxs-lookup"><span data-stu-id="48cbf-365">Use the **Quick Sources** tool in the [Drawer][DevtoolsCustomizeIndexDrawer].</span></span>

1.  <span data-ttu-id="48cbf-366">Sélectionnez un outil autre que l’outil **Sources,** tel que **l’outil Éléments.**</span><span class="sxs-lookup"><span data-stu-id="48cbf-366">Select a tool other than the **Sources** tool, such as the **Elements** tool.</span></span>  
1.  <span data-ttu-id="48cbf-367">Sélectionnez `Ctrl` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="48cbf-367">Select `Ctrl`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  <span data-ttu-id="48cbf-368">Le menu Commande s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="48cbf-368">The Command Menu opens.</span></span>  
1.  <span data-ttu-id="48cbf-369">`Quick Source`Tapez, puis sélectionnez **Afficher la source rapide.**</span><span class="sxs-lookup"><span data-stu-id="48cbf-369">Type `Quick Source`, and then select **Show Quick Source**.</span></span>  <span data-ttu-id="48cbf-370">En bas de la fenêtre DevTools, le Panneau s’affiche, avec le **panneau Source** rapide sélectionné.</span><span class="sxs-lookup"><span data-stu-id="48cbf-370">At the bottom of the DevTools window, the Drawer appears, with the **Quick Source** panel selected.</span></span>  <span data-ttu-id="48cbf-371">Le **panneau Source rapide** contient le dernier fichier que vous avez modifié dans l’outil **Sources,** dans une version compacte de l’éditeur de code DevTools.</span><span class="sxs-lookup"><span data-stu-id="48cbf-371">The **Quick Source** panel contains the last file you edited in the **Sources** tool, within a compact version of the DevTools code editor.</span></span>  
1.  <span data-ttu-id="48cbf-372">Sélectionnez `Ctrl` + `P` \(Windows, Linux\) ou `Command` + `P` \(macOS\) \*\*\*\* pour ouvrir la boîte de dialogue Ouvrir un fichier.</span><span class="sxs-lookup"><span data-stu-id="48cbf-372">Select `Ctrl`+`P` \(Windows, Linux\) or `Command`+`P` \(macOS\) to open the **Open File** dialog.</span></span>  

## <a name="using-the-debugger-pane-to-debug-javascript-code"></a><span data-ttu-id="48cbf-373">Utilisation du volet Déboguer le code JavaScript à l’aide du volet Déboguer</span><span class="sxs-lookup"><span data-stu-id="48cbf-373">Using the Debugger pane to debug JavaScript code</span></span>

<span data-ttu-id="48cbf-374">Utilisez le débogger JavaScript pour passer pas à pas le code JavaScript renvoyé par le serveur.</span><span class="sxs-lookup"><span data-stu-id="48cbf-374">Use the JavaScript debugger to step through the JavaScript code that's returned by the server.</span></span> <span data-ttu-id="48cbf-375">Le débogger **inclut** le volet Déboogger, ainsi que les points d’arrêt que vous définissez sur les lignes de code dans le **volet** Éditeur.</span><span class="sxs-lookup"><span data-stu-id="48cbf-375">The debugger includes the **Debugger** pane, along with breakpoints that you set on lines of code in the **Editor** pane.</span></span>

<span data-ttu-id="48cbf-376">Avec le débogger, vous suivez le code pas à pas, tout en regardant les expressions JavaScript que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="48cbf-376">With the debugger, you step through the code, while watching any JavaScript expressions you specify.</span></span>  <span data-ttu-id="48cbf-377">Observez et modifiez manuellement les valeurs des variables et indiquez automatiquement les variables qui sont dans l’étendue de l’instruction actuelle.</span><span class="sxs-lookup"><span data-stu-id="48cbf-377">Watch and manually change variable values, and automatically show which variables are in-scope for the current statement.</span></span>

:::image type="complex" source="../media/sources-paused-breakpoint-highlight-debug-pane.msft.png" alt-text="Volet Débogger de l’outil Sources  " lightbox="../media/sources-paused-breakpoint-highlight-debug-pane.msft.png":::
   <span data-ttu-id="48cbf-379">Volet **Débogger** de l’outil **Sources**</span><span class="sxs-lookup"><span data-stu-id="48cbf-379">The **Debugger** pane of the **Sources** tool</span></span>  
:::image-end:::  

<span data-ttu-id="48cbf-380">Le déboguer prend en charge les actions de débogage standard, telles que :</span><span class="sxs-lookup"><span data-stu-id="48cbf-380">The debugger supports standard debugging actions, such as:</span></span>  
*   <span data-ttu-id="48cbf-381">Définition de points d’arrêt, pour suspendre le code.</span><span class="sxs-lookup"><span data-stu-id="48cbf-381">Setting breakpoints, to pause code.</span></span>
*   <span data-ttu-id="48cbf-382">Code pas à pas.</span><span class="sxs-lookup"><span data-stu-id="48cbf-382">Stepping through code.</span></span>
*   <span data-ttu-id="48cbf-383">Affichage et modification de propriétés et de variables.</span><span class="sxs-lookup"><span data-stu-id="48cbf-383">Viewing and editing properties and variables.</span></span>
*   <span data-ttu-id="48cbf-384">En regardant les valeurs des expressions JavaScript.</span><span class="sxs-lookup"><span data-stu-id="48cbf-384">Watching the values of JavaScript expressions.</span></span>
*   <span data-ttu-id="48cbf-385">Affichage de la pile d’appels (séquence d’appels de fonction jusqu’à présent).</span><span class="sxs-lookup"><span data-stu-id="48cbf-385">Viewing the call stack (the sequence of function calls so far).</span></span>

<span data-ttu-id="48cbf-386">Le débogueur dans DevTools est conçu pour ressembler au débogueur dans [Visual Studio Code][CodeVisualStudioComDocsEditorDebugging] et au débogueur dans Visual Studio [.][DMCVisualStudioDebuggerNavigatingThroughCodeWithTheDebugger]</span><span class="sxs-lookup"><span data-stu-id="48cbf-386">The debugger in DevTools is designed to look, feel, and work like [the debugger in Visual Studio Code][CodeVisualStudioComDocsEditorDebugging] and [the debugger in Visual Studio][DMCVisualStudioDebuggerNavigatingThroughCodeWithTheDebugger].</span></span>

<span data-ttu-id="48cbf-387">Les sous-sections suivantes couvrent le débogage :</span><span class="sxs-lookup"><span data-stu-id="48cbf-387">The following subsections cover debugging:</span></span>
*   [<span data-ttu-id="48cbf-388">Approche de base de l’utilisation d’un débogger</span><span class="sxs-lookup"><span data-stu-id="48cbf-388">The basic approach to using a debugger</span></span>](#the-basic-approach-to-using-a-debugger)
*   [<span data-ttu-id="48cbf-389">Avantages des contrôles Watch et Scope du débogger sur console.log</span><span class="sxs-lookup"><span data-stu-id="48cbf-389">Advantages of the debugger's Watch and Scope over console.log</span></span>](#advantages-of-the-debuggers-watch-and-scope-over-consolelog)
*   [<span data-ttu-id="48cbf-390">Déboguer à Visual Studio Code directement</span><span class="sxs-lookup"><span data-stu-id="48cbf-390">Debug from Visual Studio Code directly</span></span>](#debug-from-visual-studio-code-directly)
*   [<span data-ttu-id="48cbf-391">Articles sur le débogage</span><span class="sxs-lookup"><span data-stu-id="48cbf-391">Articles about debugging</span></span>](#articles-about-debugging)

### <a name="the-basic-approach-to-using-a-debugger"></a><span data-ttu-id="48cbf-392">Approche de base de l’utilisation d’un débogger</span><span class="sxs-lookup"><span data-stu-id="48cbf-392">The basic approach to using a debugger</span></span>

<span data-ttu-id="48cbf-393">Pour résoudre les problèmes de code JavaScript, vous pouvez insérer des `console.log()` instructions dans le volet Éditeur. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="48cbf-393">To troubleshoot JavaScript code, you can insert `console.log()` statements in the **Editor** pane.</span></span>  <span data-ttu-id="48cbf-394">Une autre approche plus puissante consiste à utiliser le débogueur de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="48cbf-394">Another, more powerful approach is to use the debugger of Microsoft Edge DevTools.</span></span>  <span data-ttu-id="48cbf-395">L’utilisation d’un débogger peut être plus simple que , une fois que vous êtes familiarisé avec `console.log()` l’approche du débogger.</span><span class="sxs-lookup"><span data-stu-id="48cbf-395">Using a debugger can actually be simpler than `console.log()`, once you're familiar with the debugger approach.</span></span>

<span data-ttu-id="48cbf-396">Pour utiliser un débogger sur une page web, vous définissez généralement un point d’arrêt, puis vous envoyez un formulaire à partir de la page web, comme suit :</span><span class="sxs-lookup"><span data-stu-id="48cbf-396">To use a debugger on a webpage, you typically set a breakpoint and then send a form from the webpage, as follows:</span></span>

1.  <span data-ttu-id="48cbf-397">Ouvrez la page web dans un nouvel onglet du navigateur.</span><span class="sxs-lookup"><span data-stu-id="48cbf-397">Open the webpage in a new tab of the browser.</span></span>  <span data-ttu-id="48cbf-398">Par exemple, ouvrez cette page web de formulaire dans un nouvel onglet : [Demo: Prise en main Debugging JavaScript with Microsoft Edge (Chromium) DevTools][DevtoolsGlitchMeDebugJsGetStarted].</span><span class="sxs-lookup"><span data-stu-id="48cbf-398">For example, open this form webpage in a new tab: [Demo: Get Started Debugging JavaScript with Microsoft Edge (Chromium) DevTools][DevtoolsGlitchMeDebugJsGetStarted].</span></span>

1.  <span data-ttu-id="48cbf-399">Sélectionnez `F12` pour ouvrir la fenêtre **DevTools,** puis sélectionnez l’onglet **Sources.**</span><span class="sxs-lookup"><span data-stu-id="48cbf-399">Select `F12` to open the **DevTools** window, and then select the **Sources** tab.</span></span>

1.  <span data-ttu-id="48cbf-400">Dans le **volet Navigateur** (à gauche), sélectionnez l’onglet **Page,** puis sélectionnez le fichier JavaScript, tel que `get-started.js` .</span><span class="sxs-lookup"><span data-stu-id="48cbf-400">In the **Navigator** pane (on the left), select the **Page** tab, and then select the JavaScript file, such as `get-started.js`.</span></span>

1.  <span data-ttu-id="48cbf-401">Dans le **volet Éditeur,** sélectionnez un numéro de ligne près d’une ligne suspecte de code, pour définir un point d’arrêt sur cette ligne.</span><span class="sxs-lookup"><span data-stu-id="48cbf-401">In the **Editor** pane, select a line number near a suspect line of code, to set a breakpoint on that line.</span></span>  <span data-ttu-id="48cbf-402">Dans la figure ci-dessous, un point d’arrêt est définie sur la `var sum = addend1 + addend2;` ligne.</span><span class="sxs-lookup"><span data-stu-id="48cbf-402">In the figure below, a breakpoint is set on the line `var sum = addend1 + addend2;`.</span></span>

1.  <span data-ttu-id="48cbf-403">Dans la page web, entrez des valeurs et envoyez le formulaire.</span><span class="sxs-lookup"><span data-stu-id="48cbf-403">In the webpage, enter values and submit the form.</span></span>  <span data-ttu-id="48cbf-404">Par exemple, entrez des numéros, par exemple, puis sélectionnez le bouton Ajouter `5` `1` le numéro **1 et le numéro 2.**</span><span class="sxs-lookup"><span data-stu-id="48cbf-404">For example, enter numbers, such as `5` and `1`, then select the button **Add Number 1 and Number 2**.</span></span>  

    <span data-ttu-id="48cbf-405">Le débogger exécute le code JavaScript, puis s’interrompt au niveau du point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="48cbf-405">The debugger runs the JavaScript code and then pauses at the breakpoint.</span></span>  <span data-ttu-id="48cbf-406">Le débogger est désormais en mode Suspendu, afin que vous pouvez inspecter les valeurs des propriétés qui sont dans l’étendue et passer pas à pas du code.</span><span class="sxs-lookup"><span data-stu-id="48cbf-406">The debugger is now in Paused mode, so you can inspect the values of the properties that are in-scope, and step through the code.</span></span>

    :::image type="complex" source="../media/sources-paused-breakpoint-highlights.msft.png" alt-text="Entrée du mode suspendu du débooeur" lightbox="../media/sources-paused-breakpoint-highlights.msft.png":::
        <span data-ttu-id="48cbf-408">Entrée du mode suspendu du débooeur</span><span class="sxs-lookup"><span data-stu-id="48cbf-408">Entering Paused mode of the debugger</span></span>  
    :::image-end:::  

    <span data-ttu-id="48cbf-409">Dans la figure ci-dessus, nous avons ajouté les expressions de l’observation et nous avons ajouté deux `sum` `typeof sum` lignes au-delà du point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="48cbf-409">In the above figure, we added the Watch expressions `sum` and `typeof sum`, and stepped two lines past the breakpoint.</span></span>

1.  <span data-ttu-id="48cbf-410">Examinez les \*\*\*\* valeurs du volet Étendue, qui indiquent toutes les variables ou propriétés qui sont dans l’étendue du point d’arrêt actuel, ainsi que leurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="48cbf-410">Examine the values in the **Scope** pane, which shows all variables or properties that are in-scope for the current breakpoint, and their values.</span></span>  <span data-ttu-id="48cbf-411">Vous pouvez également ajouter des expressions dans **le volet** d’observation.</span><span class="sxs-lookup"><span data-stu-id="48cbf-411">Or, add expressions in the **Watch** pane.</span></span>  <span data-ttu-id="48cbf-412">Ces expressions sont les mêmes que celles que vous écririez dans une `console.log` instruction pour déboguer votre code.</span><span class="sxs-lookup"><span data-stu-id="48cbf-412">These expressions are the same expressions that you would write within a `console.log` statement to debug your code.</span></span>  <span data-ttu-id="48cbf-413">Pour exécuter des commandes JavaScript pour manipuler des données dans le contexte actuel, utilisez la **console.**</span><span class="sxs-lookup"><span data-stu-id="48cbf-413">To run JavaScript commands to manipulate data in the current context, use the **Console**.</span></span>  <span data-ttu-id="48cbf-414">Pour ouvrir la console, sélectionnez `Esc` .</span><span class="sxs-lookup"><span data-stu-id="48cbf-414">To open the console, select `Esc`.</span></span>  

1.  <span data-ttu-id="48cbf-415">Pas à pas dans le code à l’aide des contrôles en haut **du** volet débogger, par exemple **Étape** ( `F9` ).</span><span class="sxs-lookup"><span data-stu-id="48cbf-415">Step through the code by using the controls at the top of the **Debugger** pane, such as **Step** (`F9`).</span></span>

#### <a name="see-also"></a><span data-ttu-id="48cbf-416">Articles associés</span><span class="sxs-lookup"><span data-stu-id="48cbf-416">See also</span></span>

*   <span data-ttu-id="48cbf-417">[Get started with debugging JavaScript][DevtoolsGuideChromiumJavascriptIndex] - a tutorial using an existing, simple webpage that contains a few form controls.</span><span class="sxs-lookup"><span data-stu-id="48cbf-417">[Get started with debugging JavaScript][DevtoolsGuideChromiumJavascriptIndex] - a tutorial using an existing, simple webpage that contains a few form controls.</span></span>

### <a name="advantages-of-the-debuggers-watch-and-scope-over-consolelog"></a><span data-ttu-id="48cbf-418">Avantages des contrôles Watch et Scope over console\.log du débogger</span><span class="sxs-lookup"><span data-stu-id="48cbf-418">Advantages of the debugger\'s Watch and Scope over console\.log</span></span>

<span data-ttu-id="48cbf-419">Ces trois approches sont équivalentes :</span><span class="sxs-lookup"><span data-stu-id="48cbf-419">These three approaches are equivalent:</span></span>

*   <span data-ttu-id="48cbf-420">Ajout temporaire des instructions et `console.log(sum)` `console.log(typeof sum)` dans le code, où se trouve `sum` l’étendue.</span><span class="sxs-lookup"><span data-stu-id="48cbf-420">Temporarily adding the statements `console.log(sum)` and `console.log(typeof sum)` in the code, where `sum` is in-scope.</span></span>
*   <span data-ttu-id="48cbf-421">Émission des instructions et dans le volet Console des `sum` `console.log(typeof sum)` DevTools, \*\*\*\* lorsque le débogueur est suspendu là où se trouve `sum` l’étendue.</span><span class="sxs-lookup"><span data-stu-id="48cbf-421">Issuing the statements `sum` and `console.log(typeof sum)` in the **Console** pane of the DevTools, when the debugger is paused where `sum` is in-scope.</span></span>
*   <span data-ttu-id="48cbf-422">Définition des expressions **watch** `sum` et dans le volet `typeof sum` **Débogger.**</span><span class="sxs-lookup"><span data-stu-id="48cbf-422">Setting the **Watch** expressions `sum` and `typeof sum` in the **Debugger** pane.</span></span>

<span data-ttu-id="48cbf-423">Lorsque la variable est dans l’étendue et que sa valeur est automatiquement affichée dans la section Étendue du volet Débogger, elle est également superposée dans le volet Éditeur où elle est `sum` `sum` \*\*\*\* \*\*\*\* `sum` calculée.</span><span class="sxs-lookup"><span data-stu-id="48cbf-423">When the variable `sum` is in-scope, `sum` and its value are automatically shown in the **Scope** section of the **Debugger** pane, and are also overlaid in the Editor pane where `sum` is calculated.</span></span>  <span data-ttu-id="48cbf-424">Par exemple, vous n’aurez probablement pas besoin de définir une expression watch pour `sum` .</span><span class="sxs-lookup"><span data-stu-id="48cbf-424">So you probably wouldn't need to define a Watch expression for `sum`.</span></span>

<span data-ttu-id="48cbf-425">Le débogger offre un affichage et un environnement plus riches et plus flexibles qu’une `console.log` instruction.</span><span class="sxs-lookup"><span data-stu-id="48cbf-425">The debugger gives a richer, more flexible display and environment than a `console.log` statement.</span></span>  <span data-ttu-id="48cbf-426">Par exemple, dans le débogger, lorsque vous avancez dans le code, vous pouvez afficher et modifier les valeurs de toutes les propriétés et variables actuellement définies.</span><span class="sxs-lookup"><span data-stu-id="48cbf-426">For example, in the debugger, as you step through the code, you can display and change the values of all currently defined properties and variables.</span></span>  <span data-ttu-id="48cbf-427">Vous pouvez également émettre des instructions JavaScript dans la **console,** par exemple pour modifier des valeurs dans un tableau qui est dans l’étendue.</span><span class="sxs-lookup"><span data-stu-id="48cbf-427">You can also issue JavaScript statements in the **Console**, such as to change values in an array that's in-scope.</span></span>  <span data-ttu-id="48cbf-428">(Pour afficher la console, sélectionnez **Échap.)**</span><span class="sxs-lookup"><span data-stu-id="48cbf-428">(To display the Console, select **Esc**.)</span></span>

<span data-ttu-id="48cbf-429">Les points d’arrêt et les expressions d’observation sont conservés lorsque vous actualisez la page web.</span><span class="sxs-lookup"><span data-stu-id="48cbf-429">Breakpoints and Watch expressions are preserved when you refresh the webpage.</span></span>

### <a name="debug-from-visual-studio-code-directly"></a><span data-ttu-id="48cbf-430">Déboguer à Visual Studio Code directement</span><span class="sxs-lookup"><span data-stu-id="48cbf-430">Debug from Visual Studio Code directly</span></span>

<span data-ttu-id="48cbf-431">Pour utiliser le débogueur plus complet de Visual Studio Code au lieu du débogueur DevTools, utilisez l’extension **Microsoft Edge Tools for VS Code** for Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="48cbf-431">To use the more full-featured debugger of Visual Studio Code instead of the DevTools debugger, use the **Microsoft Edge Tools for VS Code** extension for Visual Studio Code.</span></span>

:::image type="complex" source="../media/microsoft-edge-tools-for-vs-code-extension.msft.png" alt-text="L’extension Microsoft Edge Outils de VS Code pour Visual Studio Code" lightbox="../media/microsoft-edge-tools-for-vs-code-extension.msft.png":::
   <span data-ttu-id="48cbf-433">Les **outils Microsoft Edge d’VS Code** pour Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="48cbf-433">The **Microsoft Edge Tools for VS Code** extension for Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="48cbf-434">Cette extension permet \*\*\*\* d’accéder aux éléments et aux outils réseau de Microsoft Edge DevTools, à partir de Microsoft Visual Studio Code. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="48cbf-434">This extension provides access to the **Elements** and **Network** tools of Microsoft Edge DevTools, from within Microsoft Visual Studio Code.</span></span>  

<span data-ttu-id="48cbf-435">Pour plus d’informations, [voir Visual Studio Code vue][DevToolsVSCodeIndex] d’ensemble et la page GitHub Lisez-moi, Microsoft Edge [Outils][GithubMicrosoftVscodeEdgeDevtools]de développement pour Visual Studio Code .</span><span class="sxs-lookup"><span data-stu-id="48cbf-435">For more information, see [Visual Studio Code overview][DevToolsVSCodeIndex] and the GitHub Readme page, [Microsoft Edge Developer Tools for Visual Studio Code][GithubMicrosoftVscodeEdgeDevtools].</span></span>

### <a name="articles-about-debugging"></a><span data-ttu-id="48cbf-436">Articles sur le débogage</span><span class="sxs-lookup"><span data-stu-id="48cbf-436">Articles about debugging</span></span>

<span data-ttu-id="48cbf-437">Les articles suivants couvrent le volet **Débogger** et les points d’arrêt :</span><span class="sxs-lookup"><span data-stu-id="48cbf-437">The following articles cover the **Debugger** pane and breakpoints:</span></span>

*   <span data-ttu-id="48cbf-438">[Prise en compte du débogage de JavaScript dans Microsoft Edge DevTools][DevtoolsGuideChromiumJavascriptIndex] - Didacticiel (avec captures d’écran), à l’aide d’un projet simple existant.</span><span class="sxs-lookup"><span data-stu-id="48cbf-438">[Get started with debugging JavaScript in Microsoft Edge DevTools][DevtoolsGuideChromiumJavascriptIndex] - A tutorial (with screen captures), using an existing, simple project.</span></span>

*   <span data-ttu-id="48cbf-439">Utilisez les fonctionnalités [du][DevToolsJavaScriptReference] débogger : comment utiliser le débogger pour définir des points d’arrêt, passer du code à pas, afficher et modifier des valeurs de variables, observer des expressions JavaScript et afficher la pile d’appels.</span><span class="sxs-lookup"><span data-stu-id="48cbf-439">[Use the debugger features][DevToolsJavaScriptReference] - How to use the debugger to set breakpoints, step through code, view and modify variable values, watch JavaScript expressions, and view the call stack.</span></span>

*   <span data-ttu-id="48cbf-440">[Suspendez votre code avec des points d’arrêt :][DevToolsJavaScriptBreakpoints] comment définir des points d’arrêt de base et spécialisés dans le débogger.</span><span class="sxs-lookup"><span data-stu-id="48cbf-440">[Pause your code with breakpoints][DevToolsJavaScriptBreakpoints] - How to set basic and specialized breakpoints in the debugger.</span></span>

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="48cbf-441">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="48cbf-441">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsBeginnersCss]: ../beginners/css.md "DevTools pour les débutants : prendre en | Documents Microsoft"
[DevToolsBeginnersHtml]: ../beginners/html.md "DevTools pour les débutants : mise en place du code HTML et du dom | Documents Microsoft"
[DevToolsCommandMenuIndex]: ../command-menu/index.md "Exécuter des commandes avec le menu de commande DevTools de Microsoft Edge | Microsoft Docs"  
[DevtoolsCustomizeIndexDrawer]: ../customize/index.md#drawer "Caisse : personnaliser Microsoft Edge devTools | Documents Microsoft"  
[DevToolsCustomizePlacement]: ../customize/placement.md "Modifier Microsoft Edge placement de DevTools (Undock, Dock to bottom, Dock to left) | Documents Microsoft"
[DevtoolsGuideChromiumJavascriptIndex]: ../javascript/index.md "Commencer à déboguer JavaScript dans Microsoft Edge devTools | Documents Microsoft"  
[DevtoolsGuideChromiumJavascriptSnippets]: ../javascript/snippets.md "Exécutez des extraits de code JavaScript sur n’importe quelle page web avec Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsGuideChromiumWorkspacesIndex]: ../workspaces/index.md "Modifier des fichiers à l'| Documents Microsoft"  
[DevToolsInspectStylesEditFonts]: ../inspect-styles/edit-fonts.md "Modifier les styles et paramètres de police CSS dans le volet Styles | Documents Microsoft"
[DevToolsJavaScriptBreakpoints]: ../javascript/breakpoints.md "Suspendez votre code avec des points d’arrêt | Documents Microsoft"
[DevToolsJavaScriptGuidesMarkContentScriptsLibraryCode]: ../javascript/guides/mark-content-scripts-library-code.md "Marquer les scripts de contenu en tant qu'| Documents Microsoft"
[DevtoolsJavascriptOverrides]: ../javascript/overrides.md "Remplacer les ressources de page web avec des copies locales à l’aide Microsoft Edge DevTools | Documents Microsoft"  
[DevToolsJavaScriptReference]: ../javascript/reference.md "Utiliser les fonctionnalités de débogger | Documents Microsoft"
[DevToolsJavaScriptReferenceReformat]: ../javascript/reference.md#reformat-a-minified-javascript-file-with-pretty-print "Reformater un fichier JavaScript minifié avec une impression assez grande : utilisez les fonctionnalités de débogger | Documents Microsoft"
[DevToolsJavaScriptSourceMaps]: ../javascript/source-maps.md "Ma cartographier le code prétraité sur le code source | Documents Microsoft"
[DevToolsVSCodeIndex]: ../../visual-studio-code/index.md "Visual Studio Code vue d’ensemble | Documents Microsoft"
[ExtensionsChromiumGetstartPart2ContentScripts]: ../../extensions-chromium/getting-started/part2-content-scripts.md "Créer un didacticiel d’extension partie 2 | Documents Microsoft"
<!-- external: -->
[CodeVisualStudioComDocsEditorDebugging]: https://code.visualstudio.com/docs/editor/debugging "Débogage : Visual Studio Code | Documents Microsoft"
[DMCVisualStudioDebuggerNavigatingThroughCodeWithTheDebugger]: /visualstudio/debugger/navigating-through-code-with-the-debugger "Naviguer dans le code avec le Visual Studio débogger | Documents Microsoft"
[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "Microsoft Edge Outils de développement Visual Studio Code | GitHub"
[DevtoolsGlitchMeDebugJsGetStarted]: https://microsoft-edge-chromium-devtools.glitch.me/debug-js/get-started.html "Démonstration : débogage Prise en main JavaScript avec Microsoft Edge (Chromium) DevTools | Documents Microsoft"
[HtmlstandardOrigin]: https://html.spec.whatwg.org/multipage/origin.html#origin "Origine | HTML Standard"  
[W3CHtml4Frames]: https://w3.org/TR/html401/present/frames.html "Cadres | W3C"  
[MDNContentScripts]: https://developer.mozilla.org/Add-ons/WebExtensions/Content_scripts "Scripts de contenu | MDN"  
[TypescriptlangMain]: https://www.typescriptlang.org "TypeScript"

> [!NOTE]
> <span data-ttu-id="48cbf-467">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="48cbf-467">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="48cbf-468">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/sources) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="48cbf-468">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/sources) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="48cbf-470">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="48cbf-470">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
