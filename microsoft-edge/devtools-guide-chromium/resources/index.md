---
title: Afficher les ressources de page avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 4265841501bdd74d2976ecab1c2a07f1fb215535
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10984419"
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





# <span data-ttu-id="991fb-103">Afficher les ressources de page avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="991fb-103">View page resources with Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="991fb-104">Ce guide vous explique comment utiliser Microsoft Edge DevTools pour afficher les ressources d’une page Web.</span><span class="sxs-lookup"><span data-stu-id="991fb-104">This guide teaches you how to use Microsoft Edge DevTools to view the resources of a web page.</span></span>  <span data-ttu-id="991fb-105">Les ressources sont les fichiers nécessaires à une page pour s’afficher correctement.</span><span class="sxs-lookup"><span data-stu-id="991fb-105">Resources are the files that a page needs in order to display correctly.</span></span>  <span data-ttu-id="991fb-106">Les exemples de ressources incluent les fichiers CSS, JavaScript et HTML, ainsi que les images.</span><span class="sxs-lookup"><span data-stu-id="991fb-106">Examples of resources include CSS, JavaScript, and HTML files, as well as images.</span></span>  

<span data-ttu-id="991fb-107">Ce guide suppose que vous êtes familiarisé avec les notions de base du [développement Web][MDNLearnWebDevelopment] et de [Microsoft Edge devtools][MicrosoftEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="991fb-107">This guide assumes that you are familiar with the basics of [web development][MDNLearnWebDevelopment] and [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <span data-ttu-id="991fb-108">Ouvrir les ressources</span><span class="sxs-lookup"><span data-stu-id="991fb-108">Open resources</span></span>   

<span data-ttu-id="991fb-109">Lorsque vous connaissez le nom de la ressource que vous voulez examiner, le **menu de commandes** permet d’ouvrir rapidement la ressource.</span><span class="sxs-lookup"><span data-stu-id="991fb-109">When you know the name of the resource that you want to inspect, the **Command Menu** provides a fast way of opening the resource.</span></span>  

1.  <span data-ttu-id="991fb-110">Appuyez sur `Control` + `P` \ (Windows \) ou `Command` + `P` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="991fb-110">Press `Control`+`P` \(Windows\) or `Command`+`P` \(macOS\).</span></span>  <span data-ttu-id="991fb-111">La boîte de dialogue **ouvrir le fichier** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="991fb-111">The **Open File** dialog opens.</span></span>  
    
    :::image type="complex" source="../media/resources-command-menu-empty.msft.png" alt-text="Boîte de dialogue Ouvrir un fichier" lightbox="../media/resources-command-menu-empty.msft.png":::
       <span data-ttu-id="991fb-113">Boîte de dialogue **ouvrir un fichier**</span><span class="sxs-lookup"><span data-stu-id="991fb-113">The **Open File** dialog</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="991fb-114">Sélectionnez le fichier dans la liste déroulante ou commencez à taper le nom du fichier et appuyez `Enter` une fois que le fichier approprié est mis en surbrillance dans la zone de saisie semi-automatique.</span><span class="sxs-lookup"><span data-stu-id="991fb-114">Select the file from the dropdown, or start typing the filename and press `Enter` once the correct file is highlighted in the autocomplete box.</span></span>  
    
    :::image type="complex" source="../media/resources-command-menu-file-search.msft.png" alt-text="Tapez un nom de fichier dans la boîte de dialogue Ouvrir un fichier" lightbox="../media/resources-command-menu-file-search.msft.png":::
       <span data-ttu-id="991fb-116">Tapez un nom de fichier dans la boîte de dialogue **ouvrir un fichier**</span><span class="sxs-lookup"><span data-stu-id="991fb-116">Type a filename in the **Open File** dialog</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="991fb-117">Ouvrir ressources dans le panneau réseau</span><span class="sxs-lookup"><span data-stu-id="991fb-117">Open resources in the Network panel</span></span>   

<span data-ttu-id="991fb-118">Voir [inspecter les détails d’une ressource][DevtoolsNetworkInspectDetailsResource].</span><span class="sxs-lookup"><span data-stu-id="991fb-118">See [Inspect the details of a resource][DevtoolsNetworkInspectDetailsResource].</span></span>  

:::image type="complex" source="../media/resources-network-response.msft.png" alt-text="Inspecter une ressource dans le panneau réseau" lightbox="../media/resources-network-response.msft.png":::
   <span data-ttu-id="991fb-120">Inspecter une ressource dans le panneau **réseau**</span><span class="sxs-lookup"><span data-stu-id="991fb-120">Inspect a resource in the **Network** panel</span></span>  
:::image-end:::  

### <span data-ttu-id="991fb-121">Afficher les ressources dans le panneau réseau à partir d’autres panneaux</span><span class="sxs-lookup"><span data-stu-id="991fb-121">Reveal resources in the Network panel from other panels</span></span>   

<span data-ttu-id="991fb-122">La section [Parcourir les ressources](#browse-resources) ci-dessous vous explique comment afficher les ressources de diverses parties de l’interface utilisateur d’devtools.</span><span class="sxs-lookup"><span data-stu-id="991fb-122">The [Browse resources](#browse-resources) section below shows you how to view resources from various parts of the DevTools UI.</span></span>  <span data-ttu-id="991fb-123">Si vous souhaitez inspecter une ressource dans le panneau **réseau** , cliquez avec le bouton droit sur la ressource, puis sélectionnez **afficher dans le panneau réseau**.</span><span class="sxs-lookup"><span data-stu-id="991fb-123">If you ever want to inspect a resource in the **Network** panel, right-click the resource and select **Reveal in Network panel**.</span></span>  

:::image type="complex" source="../media/resources-sources-page-reveal-in-network-panel.msft.png" alt-text="Afficher dans le panneau réseau" lightbox="../media/resources-sources-page-reveal-in-network-panel.msft.png":::
   **<span data-ttu-id="991fb-125">Afficher dans le panneau réseau</span><span class="sxs-lookup"><span data-stu-id="991fb-125">Reveal in Network panel</span></span>**  
:::image-end:::  

## <span data-ttu-id="991fb-126">Parcourir les ressources</span><span class="sxs-lookup"><span data-stu-id="991fb-126">Browse resources</span></span>   

### <span data-ttu-id="991fb-127">Parcourir les ressources du panneau réseau</span><span class="sxs-lookup"><span data-stu-id="991fb-127">Browse resources in the Network panel</span></span>   

<span data-ttu-id="991fb-128">Voir [enregistrement][DevtoolsNetworkLogActivity]de l’activité du réseau.</span><span class="sxs-lookup"><span data-stu-id="991fb-128">See [Log network activity][DevtoolsNetworkLogActivity].</span></span>  

:::image type="complex" source="../media/resources-network-resources.msft.png" alt-text="Ressources de page dans le journal réseau" lightbox="../media/resources-network-resources.msft.png":::
   <span data-ttu-id="991fb-130">Ressources de page dans le journal **réseau**</span><span class="sxs-lookup"><span data-stu-id="991fb-130">Page resources in the **Network** Log</span></span>  
:::image-end:::  

### <span data-ttu-id="991fb-131">Parcourir les répertoires</span><span class="sxs-lookup"><span data-stu-id="991fb-131">Browse by directory</span></span>   

<span data-ttu-id="991fb-132">Pour afficher les ressources d’une page organisée par annuaire:</span><span class="sxs-lookup"><span data-stu-id="991fb-132">To view the resources of a page organized by directory:</span></span>  

1.  <span data-ttu-id="991fb-133">Cliquez sur l’onglet **sources** pour ouvrir le panneau **sources** .</span><span class="sxs-lookup"><span data-stu-id="991fb-133">Click the **Sources** tab to open the **Sources** panel.</span></span>  
1.  <span data-ttu-id="991fb-134">Cliquez sur l’onglet **page** pour afficher les ressources de la page.</span><span class="sxs-lookup"><span data-stu-id="991fb-134">Click the **Page** tab to show the resources of the page.</span></span>  <span data-ttu-id="991fb-135">Le volet **page** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="991fb-135">The **Page** pane opens.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-empty.msft.png" alt-text="Volet pages" lightbox="../media/resources-sources-page-empty.msft.png":::
       <span data-ttu-id="991fb-137">Volet **pages**</span><span class="sxs-lookup"><span data-stu-id="991fb-137">The **Page** pane</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="991fb-138">Voici une répartition des éléments non évidents de la figure précédente.</span><span class="sxs-lookup"><span data-stu-id="991fb-138">Here is a breakdown of the non-obvious items in the previous figure.</span></span>  
    
    | <span data-ttu-id="991fb-139">Élément de page</span><span class="sxs-lookup"><span data-stu-id="991fb-139">Page item</span></span> | <span data-ttu-id="991fb-140">Description</span><span class="sxs-lookup"><span data-stu-id="991fb-140">Description</span></span> |  
    |:--- |:--- |  
    | `top` | <span data-ttu-id="991fb-141">Le contexte de [navigation][MDNInlineFrame]principal du document.</span><span class="sxs-lookup"><span data-stu-id="991fb-141">The main document [browsing context][MDNInlineFrame].</span></span> |  
    | `airhorner.com` | <span data-ttu-id="991fb-142">Le domaine.</span><span class="sxs-lookup"><span data-stu-id="991fb-142">The domain.</span></span>  <span data-ttu-id="991fb-143">Toutes les ressources imbriquées sous celle-ci proviennent du domaine.</span><span class="sxs-lookup"><span data-stu-id="991fb-143">All resources nested under it come from that domain.</span></span>  <span data-ttu-id="991fb-144">Par exemple, il s’agit probablement de l’URL complète du `comlink.global.j` fichier `https://airhorner.com/scripts/comlink.global.js` .</span><span class="sxs-lookup"><span data-stu-id="991fb-144">For example, the full URL of the `comlink.global.j` file is probably `https://airhorner.com/scripts/comlink.global.js`.</span></span> |  
    | `scripts` | <span data-ttu-id="991fb-145">Un répertoire.</span><span class="sxs-lookup"><span data-stu-id="991fb-145">A directory.</span></span> |  
    | `(index)` | <span data-ttu-id="991fb-146">Le document HTML principal.</span><span class="sxs-lookup"><span data-stu-id="991fb-146">The main HTML document.</span></span> |  
    | `sw.js` | <span data-ttu-id="991fb-147">Contexte du runtime du travailleur de service.</span><span class="sxs-lookup"><span data-stu-id="991fb-147">A service worker runtime context.</span></span> |  
    
1.  <span data-ttu-id="991fb-148">Cliquez sur une ressource pour l’afficher dans l' **éditeur**.</span><span class="sxs-lookup"><span data-stu-id="991fb-148">Click a resource to view it in the **Editor**.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-resource.msft.png" alt-text="Afficher un fichier dans l’éditeur" lightbox="../media/resources-sources-page-resource.msft.png":::
       <span data-ttu-id="991fb-150">Afficher un fichier dans l' **éditeur**</span><span class="sxs-lookup"><span data-stu-id="991fb-150">View a file in the **Editor**</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="991fb-151">Parcourir par nom de fichier</span><span class="sxs-lookup"><span data-stu-id="991fb-151">Browse by filename</span></span>   

<span data-ttu-id="991fb-152">Par défaut, le volet **page** regroupe les ressources par annuaire.</span><span class="sxs-lookup"><span data-stu-id="991fb-152">By default the **Page** pane groups resources by directory.</span></span>  <span data-ttu-id="991fb-153">Pour désactiver ce regroupement et afficher les ressources de chaque domaine sous forme de liste plate:</span><span class="sxs-lookup"><span data-stu-id="991fb-153">To disable this grouping and view the resources for each domain as a flat list:</span></span>  

1.  <span data-ttu-id="991fb-154">Ouvrir le volet de **pages** .</span><span class="sxs-lookup"><span data-stu-id="991fb-154">Open the **Page** pane.</span></span>  <span data-ttu-id="991fb-155">Voir [Parcourir par annuaire](#browse-by-directory).</span><span class="sxs-lookup"><span data-stu-id="991fb-155">See [Browse by directory](#browse-by-directory).</span></span>  
1.  <span data-ttu-id="991fb-156">Cliquez sur **autres options** `...` et désactivez **l’option regrouper par dossier**.</span><span class="sxs-lookup"><span data-stu-id="991fb-156">Click **More Options** `...` and disable **Group By Folder**.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-resource-group-by-folder.msft.png" alt-text="Option de regroupement par dossier" lightbox="../media/resources-sources-page-resource-group-by-folder.msft.png":::
       <span data-ttu-id="991fb-158">Option de **regroupement par dossier**</span><span class="sxs-lookup"><span data-stu-id="991fb-158">The **Group By Folder** option</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="991fb-159">Les ressources sont organisées par type de fichier.</span><span class="sxs-lookup"><span data-stu-id="991fb-159">Resources are organized by file type.</span></span>  <span data-ttu-id="991fb-160">Dans chaque type de fichier, les ressources sont classées par ordre alphabétique.</span><span class="sxs-lookup"><span data-stu-id="991fb-160">Within each file type the resources are organized alphabetically.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png" alt-text="Volet de page après la désactivation du groupe par dossier" lightbox="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png":::
       <span data-ttu-id="991fb-162">Volet de **page** après la désactivation du **groupe par dossier**</span><span class="sxs-lookup"><span data-stu-id="991fb-162">The **Page** pane after disabling **Group By Folder**</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="991fb-163">Parcourir par type de fichier</span><span class="sxs-lookup"><span data-stu-id="991fb-163">Browse by file type</span></span>   

<span data-ttu-id="991fb-164">Pour regrouper les ressources en fonction de leur type de fichier:</span><span class="sxs-lookup"><span data-stu-id="991fb-164">To group resources together based on their file type:</span></span>  

1.  <span data-ttu-id="991fb-165">Cliquez sur l’onglet **application** .  Le volet de l' **application** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="991fb-165">Click the **Application** tab.  The **Application** panel opens.</span></span>  <span data-ttu-id="991fb-166">Par défaut, le volet **manifeste** s’ouvre en premier.</span><span class="sxs-lookup"><span data-stu-id="991fb-166">By default the **Manifest** pane usually opens first.</span></span>  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner.msft.png" alt-text="Panneau application" lightbox="../media/resources-application-mainfest-airhorner.msft.png":::
       <span data-ttu-id="991fb-168">Panneau **application**</span><span class="sxs-lookup"><span data-stu-id="991fb-168">The **Application** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="991fb-169">Faites défiler vers le bas jusqu’au volet **cadres** .</span><span class="sxs-lookup"><span data-stu-id="991fb-169">Scroll down to the **Frames** pane.</span></span>  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png" alt-text="Volet cadres" lightbox="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png":::
       <span data-ttu-id="991fb-171">Volet **cadres**</span><span class="sxs-lookup"><span data-stu-id="991fb-171">The **Frames** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="991fb-172">Développez les sections qui vous intéressent.</span><span class="sxs-lookup"><span data-stu-id="991fb-172">Expand the sections in which you are interested.</span></span>  
1.  <span data-ttu-id="991fb-173">Cliquez sur une ressource pour l’afficher.</span><span class="sxs-lookup"><span data-stu-id="991fb-173">Click a resource to view it.</span></span>  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png" alt-text="Afficher une ressource dans le volet de l’application" lightbox="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png":::
       <span data-ttu-id="991fb-175">Afficher une ressource dans le volet de l' **application**</span><span class="sxs-lookup"><span data-stu-id="991fb-175">View a resource in the **Application** panel</span></span>  
    :::image-end:::  
    
#### <span data-ttu-id="991fb-176">Parcourir les fichiers par type dans le panneau réseau</span><span class="sxs-lookup"><span data-stu-id="991fb-176">Browse files by type in the Network panel</span></span>   

<span data-ttu-id="991fb-177">Voir [Filtrer par type de ressource][DevtoolsNetworkFilterByResourceType].</span><span class="sxs-lookup"><span data-stu-id="991fb-177">See [Filter by resource type][DevtoolsNetworkFilterByResourceType].</span></span>  

:::image type="complex" source="../media/resources-network-resources-filter-css.msft.png" alt-text="Filtrer les feuilles CSS dans le journal réseau" lightbox="../media/resources-network-resources-filter-css.msft.png":::
   <span data-ttu-id="991fb-179">Filtrer les feuilles CSS dans le journal **réseau**</span><span class="sxs-lookup"><span data-stu-id="991fb-179">Filter for CSS in the **Network** Log</span></span>  
:::image-end:::  

<!--  
  


-->  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"  
[DevtoolsNetworkFilterByResourceType]: ../network/index.md#filter-by-resource-type "Filtrer par type de ressource: inspecter l’activité réseau dans Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsNetworkInspectDetailsResource]: ../network/index.md#inspect-the-details-of-the-resource "Inspecter les détails de l’activité du réseau d’examen des ressources dans Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity "Journalisation de l’activité du réseau-Inspectez l’activité réseau dans Microsoft Edge DevTools | Documents Microsoft"  

[MDNInlineFrame]: https://developer.mozilla.org/docs/Web/HTML/Element/iframe "<iframe>: élément de cadre inséré | MDN"  
[MDNLearnWebDevelopment]: https://developer.mozilla.org/docs/Learn "Découvrir le développement Web | MDN"  

> [!NOTE]
> <span data-ttu-id="991fb-186">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="991fb-186">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="991fb-187">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/resources/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="991fb-187">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/resources/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="991fb-189">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="991fb-189">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
