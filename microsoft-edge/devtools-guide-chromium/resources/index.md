---
title: Afficher les ressources de page avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 0977d0a9132c19742c3337f9dc0c3e1240508a3d
ms.sourcegitcommit: 4c24edbd1c591914cb4109511534851570a614cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611916"
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





# <span data-ttu-id="f99ed-103">Afficher les ressources de page avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="f99ed-103">View Page Resources With Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="f99ed-104">Ce guide vous explique comment utiliser Microsoft Edge DevTools pour afficher les ressources d’une page Web.</span><span class="sxs-lookup"><span data-stu-id="f99ed-104">This guide teaches you how to use Microsoft Edge DevTools to view the resources of a web page.</span></span>  <span data-ttu-id="f99ed-105">Les ressources sont les fichiers nécessaires à une page pour s’afficher correctement.</span><span class="sxs-lookup"><span data-stu-id="f99ed-105">Resources are the files that a page needs in order to display correctly.</span></span>  <span data-ttu-id="f99ed-106">Les exemples de ressources incluent les fichiers CSS, JavaScript et HTML, ainsi que les images.</span><span class="sxs-lookup"><span data-stu-id="f99ed-106">Examples of resources include CSS, JavaScript, and HTML files, as well as images.</span></span>  

<span data-ttu-id="f99ed-107">Ce guide suppose que vous êtes familiarisé avec les notions de base du [développement Web][MDNLearnWebDevelopment] et de [Microsoft Edge devtools][MicrosoftEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="f99ed-107">This guide assumes that you are familiar with the basics of [web development][MDNLearnWebDevelopment] and [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <span data-ttu-id="f99ed-108">Ouvrir les ressources</span><span class="sxs-lookup"><span data-stu-id="f99ed-108">Open resources</span></span>   

<span data-ttu-id="f99ed-109">Lorsque vous connaissez le nom de la ressource que vous voulez examiner, le **menu de commandes** permet d’ouvrir rapidement la ressource.</span><span class="sxs-lookup"><span data-stu-id="f99ed-109">When you know the name of the resource that you want to inspect, the **Command Menu** provides a fast way of opening the resource.</span></span>  

1.  <span data-ttu-id="f99ed-110">Appuyez sur `Control` + `P` \ (Windows \) ou `Command` + `P` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="f99ed-110">Press `Control`+`P` \(Windows\) or `Command`+`P` \(macOS\).</span></span>  <span data-ttu-id="f99ed-111">La boîte de dialogue **ouvrir le fichier** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="f99ed-111">The **Open File** dialog opens.</span></span>  
    
    > ##### <span data-ttu-id="f99ed-112">Figure1</span><span class="sxs-lookup"><span data-stu-id="f99ed-112">Figure 1</span></span>  
    > <span data-ttu-id="f99ed-113">Boîte de dialogue **ouvrir un fichier**</span><span class="sxs-lookup"><span data-stu-id="f99ed-113">The **Open File** dialog</span></span>  
    > ![Boîte de dialogue Ouvrir un fichier][ImageOpenFile]  
    
1.  <span data-ttu-id="f99ed-115">Sélectionnez le fichier dans la liste déroulante ou commencez à taper le nom du fichier et appuyez `Enter` une fois que le fichier approprié est mis en surbrillance dans la zone de saisie semi-automatique.</span><span class="sxs-lookup"><span data-stu-id="f99ed-115">Select the file from the dropdown, or start typing the filename and press `Enter` once the correct file is highlighted in the autocomplete box.</span></span>  
    
    > ##### <span data-ttu-id="f99ed-116">Figure 2</span><span class="sxs-lookup"><span data-stu-id="f99ed-116">Figure 2</span></span>  
    > <span data-ttu-id="f99ed-117">Saisie d’un nom de fichier dans la boîte de dialogue **ouvrir un fichier**</span><span class="sxs-lookup"><span data-stu-id="f99ed-117">Typing a filename in the **Open File** dialog</span></span>  
    > ![Saisie d’un nom de fichier dans la boîte de dialogue Ouvrir un fichier][ImageFileSearch]  
    
### <span data-ttu-id="f99ed-119">Ouvrir ressources dans le panneau réseau</span><span class="sxs-lookup"><span data-stu-id="f99ed-119">Open resources in the Network panel</span></span>   

<span data-ttu-id="f99ed-120">Voir [inspecter les détails d’une ressource][DevtoolsNetworkInspectDetailsResource].</span><span class="sxs-lookup"><span data-stu-id="f99ed-120">See [Inspect the details of a resource][DevtoolsNetworkInspectDetailsResource].</span></span>  

> ##### <span data-ttu-id="f99ed-121">Figure3</span><span class="sxs-lookup"><span data-stu-id="f99ed-121">Figure 3</span></span>  
> <span data-ttu-id="f99ed-122">Examen d’une ressource dans le panneau réseau</span><span class="sxs-lookup"><span data-stu-id="f99ed-122">Inspecting a resource in the Network panel</span></span>  
> ![Examen d’une ressource dans le panneau réseau][ImageNetworkResponse]  

### <span data-ttu-id="f99ed-124">Afficher les ressources dans le panneau réseau à partir d’autres panneaux</span><span class="sxs-lookup"><span data-stu-id="f99ed-124">Reveal resources in the Network panel from other panels</span></span>   

<span data-ttu-id="f99ed-125">La section [Parcourir les ressources](#browse-resources) ci-dessous vous explique comment afficher les ressources de diverses parties de l’interface utilisateur d’devtools.</span><span class="sxs-lookup"><span data-stu-id="f99ed-125">The [Browse resources](#browse-resources) section below shows you how to view resources from various parts of the DevTools UI.</span></span>  <span data-ttu-id="f99ed-126">Si vous souhaitez inspecter une ressource dans le panneau **réseau** , cliquez avec le bouton droit sur la ressource, puis sélectionnez **afficher dans le panneau réseau**.</span><span class="sxs-lookup"><span data-stu-id="f99ed-126">If you ever want to inspect a resource in the **Network** panel, right-click the resource and select **Reveal in Network panel**.</span></span>  

> ##### <span data-ttu-id="f99ed-127">Figure 4</span><span class="sxs-lookup"><span data-stu-id="f99ed-127">Figure 4</span></span>  
> <span data-ttu-id="f99ed-128">Option **afficher dans le panneau réseau**</span><span class="sxs-lookup"><span data-stu-id="f99ed-128">The **Reveal in Network panel** option</span></span>  
> ![Afficher dans le panneau réseau][ImageRevealNetwork]  

## <span data-ttu-id="f99ed-130">Parcourir les ressources</span><span class="sxs-lookup"><span data-stu-id="f99ed-130">Browse resources</span></span>   

### <span data-ttu-id="f99ed-131">Parcourir les ressources du panneau réseau</span><span class="sxs-lookup"><span data-stu-id="f99ed-131">Browse resources in the Network panel</span></span>   

<span data-ttu-id="f99ed-132">Voir [enregistrement][DevtoolsNetworkLogActivity]de l’activité du réseau.</span><span class="sxs-lookup"><span data-stu-id="f99ed-132">See [Log network activity][DevtoolsNetworkLogActivity].</span></span>  

> ##### <span data-ttu-id="f99ed-133">Figure 5</span><span class="sxs-lookup"><span data-stu-id="f99ed-133">Figure 5</span></span>  
> <span data-ttu-id="f99ed-134">Ressources de page dans le journal réseau</span><span class="sxs-lookup"><span data-stu-id="f99ed-134">Page resources in the Network Log</span></span>  
> ![Ressources de page dans le journal réseau][ImageNetworkLog]  

### <span data-ttu-id="f99ed-136">Parcourir les répertoires</span><span class="sxs-lookup"><span data-stu-id="f99ed-136">Browse by directory</span></span>   

<span data-ttu-id="f99ed-137">Pour afficher les ressources d’une page organisée par annuaire:</span><span class="sxs-lookup"><span data-stu-id="f99ed-137">To view the resources of a page organized by directory:</span></span>  

1.  <span data-ttu-id="f99ed-138">Cliquez sur l’onglet **sources** pour ouvrir le panneau **sources** .</span><span class="sxs-lookup"><span data-stu-id="f99ed-138">Click the **Sources** tab to open the **Sources** panel.</span></span>  
1.  <span data-ttu-id="f99ed-139">Cliquez sur l’onglet **page** pour afficher les ressources de la page.</span><span class="sxs-lookup"><span data-stu-id="f99ed-139">Click the **Page** tab to show the resources of the page.</span></span>  <span data-ttu-id="f99ed-140">Le volet **page** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="f99ed-140">The **Page** pane opens.</span></span>  
    
    > ##### <span data-ttu-id="f99ed-141">Figure 6</span><span class="sxs-lookup"><span data-stu-id="f99ed-141">Figure 6</span></span>  
    > <span data-ttu-id="f99ed-142">Volet **pages**</span><span class="sxs-lookup"><span data-stu-id="f99ed-142">The **Page** pane</span></span>  
    > ![Volet pages][ImagePage]  
    
    <span data-ttu-id="f99ed-144">Voici une répartition des éléments non évidents de la [figure 6](#figure-6):</span><span class="sxs-lookup"><span data-stu-id="f99ed-144">Here is a breakdown of the non-obvious items in [Figure 6](#figure-6):</span></span>  
    
    | <span data-ttu-id="f99ed-145">Élément de page</span><span class="sxs-lookup"><span data-stu-id="f99ed-145">Page item</span></span> | <span data-ttu-id="f99ed-146">Description</span><span class="sxs-lookup"><span data-stu-id="f99ed-146">Description</span></span> |  
    |:--- |:--- |  
    | `top` | <span data-ttu-id="f99ed-147">Le contexte de [navigation][MDNInlineFrame]principal du document.</span><span class="sxs-lookup"><span data-stu-id="f99ed-147">The main document [browsing context][MDNInlineFrame].</span></span> |  
    | `airhorner.com` | <span data-ttu-id="f99ed-148">Le domaine.</span><span class="sxs-lookup"><span data-stu-id="f99ed-148">The domain.</span></span>  <span data-ttu-id="f99ed-149">Toutes les ressources imbriquées sous celle-ci proviennent du domaine.</span><span class="sxs-lookup"><span data-stu-id="f99ed-149">All resources nested under it come from that domain.</span></span>  <span data-ttu-id="f99ed-150">Par exemple, il s’agit probablement de l’URL complète du `comlink.global.j` fichier `https://airhorner.com/scripts/comlink.global.js` .</span><span class="sxs-lookup"><span data-stu-id="f99ed-150">For example, the full URL of the `comlink.global.j` file is probably `https://airhorner.com/scripts/comlink.global.js`.</span></span> |  
    | `scripts` | <span data-ttu-id="f99ed-151">Un répertoire.</span><span class="sxs-lookup"><span data-stu-id="f99ed-151">A directory.</span></span> |  
    | `(index)` | <span data-ttu-id="f99ed-152">Le document HTML principal.</span><span class="sxs-lookup"><span data-stu-id="f99ed-152">The main HTML document.</span></span> |  
    | `sw.js` | <span data-ttu-id="f99ed-153">Contexte du runtime du travailleur de service.</span><span class="sxs-lookup"><span data-stu-id="f99ed-153">A service worker runtime context.</span></span> |  
    
1.  <span data-ttu-id="f99ed-154">Cliquez sur une ressource pour l’afficher dans l' **éditeur**.</span><span class="sxs-lookup"><span data-stu-id="f99ed-154">Click a resource to view it in the **Editor**.</span></span>  
    
    > ##### <span data-ttu-id="f99ed-155">Figure 7</span><span class="sxs-lookup"><span data-stu-id="f99ed-155">Figure 7</span></span>  
    > <span data-ttu-id="f99ed-156">Affichage d’un fichier dans l' **éditeur**</span><span class="sxs-lookup"><span data-stu-id="f99ed-156">Viewing a file in the **Editor**</span></span>  
    > ![Affichage d’un fichier dans l’éditeur][ImageSourcesView]  
    
### <span data-ttu-id="f99ed-158">Parcourir par nom de fichier</span><span class="sxs-lookup"><span data-stu-id="f99ed-158">Browse by filename</span></span>   

<span data-ttu-id="f99ed-159">Par défaut, le volet **page** regroupe les ressources par annuaire.</span><span class="sxs-lookup"><span data-stu-id="f99ed-159">By default the **Page** pane groups resources by directory.</span></span>  <span data-ttu-id="f99ed-160">Pour désactiver ce regroupement et afficher les ressources de chaque domaine sous forme de liste plate:</span><span class="sxs-lookup"><span data-stu-id="f99ed-160">To disable this grouping and view the resources for each domain as a flat list:</span></span>  

1.  <span data-ttu-id="f99ed-161">Ouvrir le volet de **pages** .</span><span class="sxs-lookup"><span data-stu-id="f99ed-161">Open the **Page** pane.</span></span>  <span data-ttu-id="f99ed-162">Voir [Parcourir par annuaire](#browse-by-directory).</span><span class="sxs-lookup"><span data-stu-id="f99ed-162">See [Browse by directory](#browse-by-directory).</span></span>  
1.  <span data-ttu-id="f99ed-163">Cliquez sur **autres options** `...` et désactivez **l’option regrouper par dossier**.</span><span class="sxs-lookup"><span data-stu-id="f99ed-163">Click **More Options** `...` and disable **Group By Folder**.</span></span>  
    
    > ##### <span data-ttu-id="f99ed-164">Figure8</span><span class="sxs-lookup"><span data-stu-id="f99ed-164">Figure 8</span></span>  
    > <span data-ttu-id="f99ed-165">Option de **regroupement par dossier**</span><span class="sxs-lookup"><span data-stu-id="f99ed-165">The **Group By Folder** option</span></span>  
    > ![Option de regroupement par dossier][ImageGroupByFolder]  
    
    <span data-ttu-id="f99ed-167">Les ressources sont organisées par type de fichier.</span><span class="sxs-lookup"><span data-stu-id="f99ed-167">Resources are organized by file type.</span></span>  <span data-ttu-id="f99ed-168">Dans chaque type de fichier, les ressources sont classées par ordre alphabétique.</span><span class="sxs-lookup"><span data-stu-id="f99ed-168">Within each file type the resources are organized alphabetically.</span></span>  
    
    > ##### <span data-ttu-id="f99ed-169">Figure9</span><span class="sxs-lookup"><span data-stu-id="f99ed-169">Figure 9</span></span>  
    > <span data-ttu-id="f99ed-170">Volet de **page** après la désactivation du **groupe par dossier**</span><span class="sxs-lookup"><span data-stu-id="f99ed-170">The **Page** pane after disabling **Group By Folder**</span></span>  
    > ![Volet de page après la désactivation du groupe par dossier][ImageFileNames]  
    
### <span data-ttu-id="f99ed-172">Parcourir par type de fichier</span><span class="sxs-lookup"><span data-stu-id="f99ed-172">Browse by file type</span></span>   

<span data-ttu-id="f99ed-173">Pour regrouper les ressources en fonction de leur type de fichier:</span><span class="sxs-lookup"><span data-stu-id="f99ed-173">To group resources together based on their file type:</span></span>  

1.  <span data-ttu-id="f99ed-174">Cliquez sur l’onglet **application** .  Le volet de l' **application** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="f99ed-174">Click the **Application** tab.  The **Application** panel opens.</span></span>  <span data-ttu-id="f99ed-175">Par défaut, le volet **manifeste** s’ouvre en premier.</span><span class="sxs-lookup"><span data-stu-id="f99ed-175">By default the **Manifest** pane usually opens first.</span></span>  
    
    > ##### <span data-ttu-id="f99ed-176">Figure10</span><span class="sxs-lookup"><span data-stu-id="f99ed-176">Figure 10</span></span>  
    > <span data-ttu-id="f99ed-177">Panneau **application**</span><span class="sxs-lookup"><span data-stu-id="f99ed-177">The **Application** panel</span></span>  
    > ![Panneau application][ImageApplication]  
    
1.  <span data-ttu-id="f99ed-179">Faites défiler vers le bas jusqu’au volet **cadres** .</span><span class="sxs-lookup"><span data-stu-id="f99ed-179">Scroll down to the **Frames** pane.</span></span>  
    
    > ##### <span data-ttu-id="f99ed-180">Figure11</span><span class="sxs-lookup"><span data-stu-id="f99ed-180">Figure 11</span></span>  
    > <span data-ttu-id="f99ed-181">Volet **cadres**</span><span class="sxs-lookup"><span data-stu-id="f99ed-181">The **Frames** pane</span></span>  
    > ![Volet cadres][ImageFrames]  
    
1.  <span data-ttu-id="f99ed-183">Développez les sections qui vous intéressent.</span><span class="sxs-lookup"><span data-stu-id="f99ed-183">Expand the sections in which you are interested.</span></span>  
1.  <span data-ttu-id="f99ed-184">Cliquez sur une ressource pour l’afficher.</span><span class="sxs-lookup"><span data-stu-id="f99ed-184">Click a resource to view it.</span></span>  
    
    > ##### <span data-ttu-id="f99ed-185">Figure12</span><span class="sxs-lookup"><span data-stu-id="f99ed-185">Figure 12</span></span>  
    > <span data-ttu-id="f99ed-186">Affichage d’une ressource dans le volet de l' **application**</span><span class="sxs-lookup"><span data-stu-id="f99ed-186">Viewing a resource in the **Application** panel</span></span>  
    > ![Affichage d’une ressource dans le volet de l’application][ImageApplicationView]  

#### <span data-ttu-id="f99ed-188">Parcourir les fichiers par type dans le panneau réseau</span><span class="sxs-lookup"><span data-stu-id="f99ed-188">Browse files by type in the Network panel</span></span>   

<span data-ttu-id="f99ed-189">Voir [Filtrer par type de ressource][DevtoolsNetworkFilterByResourceType].</span><span class="sxs-lookup"><span data-stu-id="f99ed-189">See [Filter by resource type][DevtoolsNetworkFilterByResourceType].</span></span>  

> ##### <span data-ttu-id="f99ed-190">Figure13</span><span class="sxs-lookup"><span data-stu-id="f99ed-190">Figure 13</span></span>  
> <span data-ttu-id="f99ed-191">Filtrage de CSS dans le journal réseau</span><span class="sxs-lookup"><span data-stu-id="f99ed-191">Filtering for CSS in the Network Log</span></span>  
> ![Filtrage de CSS dans le journal réseau][ImageCSS]  

<!--  -->  



<!-- image links -->  

[ImageOpenFile]: /microsoft-edge/devtools-guide-chromium/media/resources-command-menu-empty.msft.png "Figure 1: boîte de dialogue Ouvrir un fichier"  
[ImageFileSearch]: /microsoft-edge/devtools-guide-chromium/media/resources-command-menu-file-search.msft.png "Figure 2: saisie d’un nom de fichier dans la boîte de dialogue Ouvrir un fichier"  
[ImageNetworkResponse]: /microsoft-edge/devtools-guide-chromium/media/resources-network-response.msft.png "Figure 3: inspection d’une ressource dans le panneau * * Network * *"  
[ImageRevealNetwork]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-reveal-in-network-panel.msft.png "Figure 4: affichage dans le panneau réseau"  
[ImageNetworkLog]: /microsoft-edge/devtools-guide-chromium/media/resources-network-resources.msft.png "Figure 5: ressources de page dans le journal réseau"  
[ImagePage]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-empty.msft.png "Figure 6: volet pages"  
[ImageSourcesView]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-resource.msft.png "Figure 7: affichage d’un fichier dans l’éditeur"  
[ImageGroupByFolder]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-resource-group-by-folder.msft.png "Figure 8: option regroupement par dossier"  
[ImageFileNames]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png "Figure 9: volet pages après la désactivation de l’ensemble des dossiers"  
[ImageApplication]: /microsoft-edge/devtools-guide-chromium/media/resources-application-mainfest-airhorner.msft.png "Figure 10: volet de l’application"  
[ImageFrames]: /microsoft-edge/devtools-guide-chromium/media/resources-application-mainfest-airhorner-frames-expanded.msft.png "Figure 11: volet cadres"  
[ImageApplicationView]: /microsoft-edge/devtools-guide-chromium/media/resources-application-mainfest-airhorner-expanded-resources.msft.png "Figure 12: affichage d’une ressource dans le volet de l’application"  
[ImageCSS]: /microsoft-edge/devtools-guide-chromium/media/resources-network-resources-filter-css.msft.png "Figure 13: filtrage de CSS dans le journal réseau"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Outils de développement Microsoft Edge (chrome)"  
[DevtoolsNetworkFilterByResourceType]: /microsoft-edge/devtools-guide-chromium/network/index#filter-by-resource-type "Filtrer par type de ressource: inspecter l’activité réseau dans Microsoft Edge DevTools"  
[DevtoolsNetworkInspectDetailsResource]: /microsoft-edge/devtools-guide-chromium/network/index#inspect-the-details-of-the-resource "Inspecter les détails de l’activité réseau d’examen des ressources dans Microsoft Edge DevTools"  
[DevtoolsNetworkLogActivity]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Journalisation de l’activité du réseau-Inspectez l’activité réseau dans Microsoft Edge DevTools"  

[MDNInlineFrame]: https://developer.mozilla.org/docs/Web/HTML/Element/iframe "<iframe>: élément de cadre inséré | MDN"  
[MDNLearnWebDevelopment]: https://developer.mozilla.org/docs/Learn "Découvrir le développement Web | MDN"  

> [!NOTE]
> <span data-ttu-id="f99ed-212">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f99ed-212">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="f99ed-213">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/resources/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="f99ed-213">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/resources/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="f99ed-215">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f99ed-215">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
