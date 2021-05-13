---
description: Organisez les ressources par trame, domaine, type ou autre critère.
title: Afficher les ressources de page avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 415ed45bf650aa6800ab674cce74179f783a82c7
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11565070"
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
# <a name="view-page-resources-with-microsoft-edge-devtools"></a><span data-ttu-id="71659-104">Afficher les ressources de page avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="71659-104">View page resources with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="71659-105">Ce guide vous apprend à utiliser Microsoft Edge DevTools pour afficher les ressources d’une page web.</span><span class="sxs-lookup"><span data-stu-id="71659-105">This guide teaches you how to use Microsoft Edge DevTools to view the resources of a web page.</span></span>  <span data-ttu-id="71659-106">Les ressources sont les fichiers dont une page a besoin pour s’afficher correctement.</span><span class="sxs-lookup"><span data-stu-id="71659-106">Resources are the files that a page needs in order to display correctly.</span></span>  <span data-ttu-id="71659-107">Les fichiers CSS, JavaScript et HTML sont des exemples de ressources, ainsi que des images.</span><span class="sxs-lookup"><span data-stu-id="71659-107">Examples of resources include CSS, JavaScript, and HTML files, as well as images.</span></span>  

<span data-ttu-id="71659-108">Ce guide suppose que vous connaissez les principes de base du développement [web][MDNLearnWebDevelopment] et Microsoft Edge [DevTools][MicrosoftEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="71659-108">This guide assumes that you are familiar with the basics of [web development][MDNLearnWebDevelopment] and [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <a name="open-resources"></a><span data-ttu-id="71659-109">Ouvrir des ressources</span><span class="sxs-lookup"><span data-stu-id="71659-109">Open resources</span></span>  

<span data-ttu-id="71659-110">Lorsque vous connaissez le nom de la ressource que vous souhaitez inspecter, le **menu** Commande permet d’ouvrir rapidement la ressource.</span><span class="sxs-lookup"><span data-stu-id="71659-110">When you know the name of the resource that you want to inspect, the **Command Menu** provides a fast way of opening the resource.</span></span>  

1.  <span data-ttu-id="71659-111">Sélectionnez `Control` + `P` \(Windows, Linux\) ou `Command` + `P` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="71659-111">Select `Control`+`P` \(Windows, Linux\) or `Command`+`P` \(macOS\).</span></span>  <span data-ttu-id="71659-112">La **boîte de dialogue Ouvrir** un fichier s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="71659-112">The **Open File** dialog opens.</span></span>  
    
    :::image type="complex" source="../media/resources-command-menu-empty.msft.png" alt-text="Boîte de dialogue Ouvrir un fichier" lightbox="../media/resources-command-menu-empty.msft.png":::
       <span data-ttu-id="71659-114">Boîte **de dialogue Ouvrir un** fichier</span><span class="sxs-lookup"><span data-stu-id="71659-114">The **Open File** dialog</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="71659-115">Choisissez le fichier dans la zone de dépôt ou commencez à taper le nom du fichier, puis sélectionnez une fois que le fichier correct est mis en surbrillence dans la `Enter` zone de saisie automatique.</span><span class="sxs-lookup"><span data-stu-id="71659-115">Choose the file from the dropdown, or start typing the filename and select `Enter` once the correct file is highlighted in the autocomplete box.</span></span>  
    
    :::image type="complex" source="../media/resources-command-menu-file-search.msft.png" alt-text="Tapez un nom de fichier dans la boîte de dialogue Ouvrir un fichier" lightbox="../media/resources-command-menu-file-search.msft.png":::
       <span data-ttu-id="71659-117">Tapez un nom de fichier dans la boîte **de dialogue Ouvrir un** fichier</span><span class="sxs-lookup"><span data-stu-id="71659-117">Type a filename in the **Open File** dialog</span></span>  
    :::image-end:::  
    
### <a name="open-resources-in-the-network-tool"></a><span data-ttu-id="71659-118">Ouvrir des ressources dans l’outil Réseau</span><span class="sxs-lookup"><span data-stu-id="71659-118">Open resources in the Network tool</span></span>  

<span data-ttu-id="71659-119">Accédez [à Inspecter les détails d’une ressource.][DevtoolsNetworkInspectDetailsResource]</span><span class="sxs-lookup"><span data-stu-id="71659-119">Navigate to [Inspect the details of a resource][DevtoolsNetworkInspectDetailsResource].</span></span>  

:::image type="complex" source="../media/resources-network-response.msft.png" alt-text="Inspecter une ressource dans l’outil Réseau" lightbox="../media/resources-network-response.msft.png":::
   <span data-ttu-id="71659-121">Inspecter une ressource dans **l’outil** Réseau</span><span class="sxs-lookup"><span data-stu-id="71659-121">Inspect a resource in the **Network** tool</span></span>  
:::image-end:::  

### <a name="reveal-resources-in-the-network-tool-from-other-panels"></a><span data-ttu-id="71659-122">Faire apparaître des ressources dans l’outil Réseau à partir d’autres panneaux</span><span class="sxs-lookup"><span data-stu-id="71659-122">Reveal resources in the Network tool from other panels</span></span>  

<span data-ttu-id="71659-123">La section [Parcourir les](#browse-resources) ressources ci-dessous vous montre comment afficher les ressources de différentes parties de l’interface utilisateur DevTools.</span><span class="sxs-lookup"><span data-stu-id="71659-123">The [Browse resources](#browse-resources) section below shows you how to view resources from various parts of the DevTools UI.</span></span>  <span data-ttu-id="71659-124">Si vous souhaitez inspecter une \*\*\*\* ressource dans l’outil Réseau, pointez sur la ressource, ouvrez le menu contextuel \(clic droit\), puis choisissez Révéler dans le **panneau Réseau.**</span><span class="sxs-lookup"><span data-stu-id="71659-124">If you ever want to inspect a resource in the **Network** tool,  hover on the resource, open the contextual menu \(right-click\), and choose **Reveal in Network panel**.</span></span>  

:::image type="complex" source="../media/resources-sources-page-reveal-in-network-panel.msft.png" alt-text="Révéler dans le panneau réseau" lightbox="../media/resources-sources-page-reveal-in-network-panel.msft.png":::
   **<span data-ttu-id="71659-126">Révéler dans le panneau réseau</span><span class="sxs-lookup"><span data-stu-id="71659-126">Reveal in Network panel</span></span>**  
:::image-end:::  

## <a name="browse-resources"></a><span data-ttu-id="71659-127">Parcourir les ressources</span><span class="sxs-lookup"><span data-stu-id="71659-127">Browse resources</span></span>  

### <a name="browse-resources-in-the-network-panel"></a><span data-ttu-id="71659-128">Parcourir les ressources dans le panneau Réseau</span><span class="sxs-lookup"><span data-stu-id="71659-128">Browse resources in the Network panel</span></span>  

<span data-ttu-id="71659-129">Accédez à [Journal de l’activité réseau.][DevtoolsNetworkLogActivity]</span><span class="sxs-lookup"><span data-stu-id="71659-129">Navigate to [Log network activity][DevtoolsNetworkLogActivity].</span></span>  

:::image type="complex" source="../media/resources-network-resources.msft.png" alt-text="Ressources de page dans le journal réseau" lightbox="../media/resources-network-resources.msft.png":::
   <span data-ttu-id="71659-131">Ressources de page dans le **journal** réseau</span><span class="sxs-lookup"><span data-stu-id="71659-131">Page resources in the **Network** Log</span></span>  
:::image-end:::  

### <a name="browse-by-directory"></a><span data-ttu-id="71659-132">Parcourir par répertoire</span><span class="sxs-lookup"><span data-stu-id="71659-132">Browse by directory</span></span>  

<span data-ttu-id="71659-133">Pour afficher les ressources d’une page web organisée par répertoire :</span><span class="sxs-lookup"><span data-stu-id="71659-133">To view the resources of a webpage organized by directory:</span></span>  

1.  <span data-ttu-id="71659-134">Ouvrez DevTools.</span><span class="sxs-lookup"><span data-stu-id="71659-134">Open DevTools.</span></span>
1.  <span data-ttu-id="71659-135">Choisissez **l’outil Sources,** puis, dans le volet **Navigateur** dans le coin supérieur gauche, choisissez **l’onglet Page.**</span><span class="sxs-lookup"><span data-stu-id="71659-135">Choose the **Sources** tool, and then in the **Navigator** pane in the upper left, choose the **Page** tab.</span></span>
1.  <span data-ttu-id="71659-136">Choisissez le **bouton Plus d’options** (...) à droite de l’onglet **Page,** puis choisissez **Grouper par dossier.**</span><span class="sxs-lookup"><span data-stu-id="71659-136">Choose the **More options** (...) button to the right of the **Page** tab, and then choose **Group by folder**.</span></span>
    
    :::image type="complex" source="../media/resources-sources-page-empty.msft.png" alt-text="Onglet Page dans le volet Navigateur de l’outil Sources" lightbox="../media/resources-sources-page-empty.msft.png":::
       <span data-ttu-id="71659-138">Onglet **Page** dans le volet **Navigateur** de l’outil **Sources**</span><span class="sxs-lookup"><span data-stu-id="71659-138">The **Page** tab in the **Navigator** pane of the **Sources** tool</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="71659-139">Voici une répartition des éléments non évidents dans la figure précédente.</span><span class="sxs-lookup"><span data-stu-id="71659-139">Here is a breakdown of the non-obvious items in the previous figure.</span></span>  
    
    | <span data-ttu-id="71659-140">Élément de page</span><span class="sxs-lookup"><span data-stu-id="71659-140">Page item</span></span> | <span data-ttu-id="71659-141">Description</span><span class="sxs-lookup"><span data-stu-id="71659-141">Description</span></span> |  
    |:--- |:--- |  
    | `top` | <span data-ttu-id="71659-142">Contexte de navigation de document [principal.][MDNInlineFrame]</span><span class="sxs-lookup"><span data-stu-id="71659-142">The main document [browsing context][MDNInlineFrame].</span></span> |  
    | `airhorner.com` | <span data-ttu-id="71659-143">Le domaine.</span><span class="sxs-lookup"><span data-stu-id="71659-143">The domain.</span></span>  <span data-ttu-id="71659-144">Toutes les ressources imbrmbrées sous celui-ci proviennent de ce domaine.</span><span class="sxs-lookup"><span data-stu-id="71659-144">All resources nested under it come from that domain.</span></span>  <span data-ttu-id="71659-145">Par exemple, l’URL complète du `comlink.global.j` fichier est probablement `https://airhorner.com/scripts/comlink.global.js` .</span><span class="sxs-lookup"><span data-stu-id="71659-145">For example, the full URL of the `comlink.global.j` file is probably `https://airhorner.com/scripts/comlink.global.js`.</span></span> |  
    | `scripts` | <span data-ttu-id="71659-146">Répertoire.</span><span class="sxs-lookup"><span data-stu-id="71659-146">A directory.</span></span> |  
    | `(index)` | <span data-ttu-id="71659-147">Document HTML principal.</span><span class="sxs-lookup"><span data-stu-id="71659-147">The main HTML document.</span></span> |  
    | `sw.js` | <span data-ttu-id="71659-148">Contexte d’runtime de travail de service.</span><span class="sxs-lookup"><span data-stu-id="71659-148">A service worker runtime context.</span></span> |  
    
1.  <span data-ttu-id="71659-149">Choisissez une ressource pour l’afficher dans **l’Éditeur.**</span><span class="sxs-lookup"><span data-stu-id="71659-149">Choose a resource to view it in the **Editor**.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-resource.msft.png" alt-text="Afficher un fichier dans l’Éditeur" lightbox="../media/resources-sources-page-resource.msft.png":::
       <span data-ttu-id="71659-151">Afficher un fichier dans **l’Éditeur**</span><span class="sxs-lookup"><span data-stu-id="71659-151">View a file in the **Editor**</span></span>  
    :::image-end:::  
    
### <a name="browse-by-filename"></a><span data-ttu-id="71659-152">Parcourir par nom de fichier</span><span class="sxs-lookup"><span data-stu-id="71659-152">Browse by filename</span></span>  

<span data-ttu-id="71659-153">Par défaut, l’onglet **Page** groupe les ressources par répertoire.</span><span class="sxs-lookup"><span data-stu-id="71659-153">By default, the **Page** tab groups resources by directory.</span></span>  <span data-ttu-id="71659-154">Pour afficher les ressources de chaque domaine en tant que liste plate, au lieu de les grouper par répertoire :</span><span class="sxs-lookup"><span data-stu-id="71659-154">To display the resources for each domain as a flat list, instead of grouping them by directory:</span></span>

1.  <span data-ttu-id="71659-155">Accédez à **l’outil Sources.**</span><span class="sxs-lookup"><span data-stu-id="71659-155">Navigate to the **Sources** tool.</span></span>  
1.  <span data-ttu-id="71659-156">Dans le **volet Navigateur** (à gauche), choisissez l’onglet **Page.**</span><span class="sxs-lookup"><span data-stu-id="71659-156">In the **Navigator** pane (on the left), choose the **Page** tab.</span></span>  
1.  <span data-ttu-id="71659-157">Choisissez **plus d’options,** `...` puis effacer la coche en regard de **Grouper par dossier.**</span><span class="sxs-lookup"><span data-stu-id="71659-157">Choose **More options** `...` and then clear the checkmark next to **Group by folder**.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-resource-group-by-folder.msft.png" alt-text="Option Grouper par dossier" lightbox="../media/resources-sources-page-resource-group-by-folder.msft.png":::
       <span data-ttu-id="71659-159">Option **Grouper par** dossier</span><span class="sxs-lookup"><span data-stu-id="71659-159">The **Group by folder** option</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="71659-160">Les ressources sont organisées par type de fichier.</span><span class="sxs-lookup"><span data-stu-id="71659-160">Resources are organized by file type.</span></span>  <span data-ttu-id="71659-161">Dans chaque type de fichier, les ressources sont organisées par ordre alphabétique.</span><span class="sxs-lookup"><span data-stu-id="71659-161">Within each file type, the resources are organized alphabetically.</span></span>  

    :::image type="complex" source="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png" alt-text="Onglet Page après la suppression de la coche Grouper par dossier" lightbox="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png":::
       <span data-ttu-id="71659-163">Onglet **Page après** la suppression de la coche **Grouper par** dossier</span><span class="sxs-lookup"><span data-stu-id="71659-163">The **Page** tab after clearing the **Group by folder** check mark</span></span>  
    :::image-end:::  
    
### <a name="browse-by-file-type"></a><span data-ttu-id="71659-164">Parcourir par type de fichier</span><span class="sxs-lookup"><span data-stu-id="71659-164">Browse by file type</span></span>  

<span data-ttu-id="71659-165">Pour grouper des ressources en fonction de leur type de fichier :</span><span class="sxs-lookup"><span data-stu-id="71659-165">To group resources together based on their file type:</span></span>  

1.  <span data-ttu-id="71659-166">Choisissez **l’onglet** Application.  **L’outil Application** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="71659-166">Choose the **Application** tab.  The **Application** tool opens.</span></span>  <span data-ttu-id="71659-167">Par défaut, **le volet** Manifeste s’ouvre généralement en premier.</span><span class="sxs-lookup"><span data-stu-id="71659-167">By default the **Manifest** pane usually opens first.</span></span>  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner.msft.png" alt-text="L’outil Application" lightbox="../media/resources-application-mainfest-airhorner.msft.png":::
       <span data-ttu-id="71659-169">**L’outil Application**</span><span class="sxs-lookup"><span data-stu-id="71659-169">The **Application** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="71659-170">Faites défiler vers le bas **jusqu’au** volet Cadres.</span><span class="sxs-lookup"><span data-stu-id="71659-170">Scroll down to the **Frames** pane.</span></span>  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png" alt-text="Volet Cadres" lightbox="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png":::
       <span data-ttu-id="71659-172">Volet **Cadres**</span><span class="sxs-lookup"><span data-stu-id="71659-172">The **Frames** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="71659-173">Développez les sections qui vous intéressent.</span><span class="sxs-lookup"><span data-stu-id="71659-173">Expand the sections in which you are interested.</span></span>  
1.  <span data-ttu-id="71659-174">Choisissez une ressource pour l’afficher.</span><span class="sxs-lookup"><span data-stu-id="71659-174">Choose a resource to view it.</span></span>  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png" alt-text="Afficher une ressource dans le panneau Application" lightbox="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png":::
       <span data-ttu-id="71659-176">Afficher une ressource dans le panneau **Application**</span><span class="sxs-lookup"><span data-stu-id="71659-176">View a resource in the **Application** panel</span></span>  
    :::image-end:::  
    
#### <a name="browse-files-by-type-in-the-network-panel"></a><span data-ttu-id="71659-177">Parcourir les fichiers par type dans le panneau Réseau</span><span class="sxs-lookup"><span data-stu-id="71659-177">Browse files by type in the Network panel</span></span>  

<span data-ttu-id="71659-178">Accédez à [Filtrer par type de ressource.][DevtoolsNetworkFilterByResourceType]</span><span class="sxs-lookup"><span data-stu-id="71659-178">Navigate to [Filter by resource type][DevtoolsNetworkFilterByResourceType].</span></span>  

:::image type="complex" source="../media/resources-network-resources-filter-css.msft.png" alt-text="Filtre pour CSS dans le journal réseau" lightbox="../media/resources-network-resources-filter-css.msft.png":::
   <span data-ttu-id="71659-180">Filtre pour CSS dans le **journal** réseau</span><span class="sxs-lookup"><span data-stu-id="71659-180">Filter for CSS in the **Network** Log</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="71659-181">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="71659-181">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "outils de développement Microsoft Edge (Chromium) | Documents Microsoft"  
[DevtoolsNetworkFilterByResourceType]: ../network/index.md#filter-by-resource-type "Filtrer par type de ressource : inspecter l’activité réseau dans Microsoft Edge devTools | Documents Microsoft"  
[DevtoolsNetworkInspectDetailsResource]: ../network/index.md#inspect-the-details-of-the-resource "Inspecter les détails de la ressource : inspecter l’activité réseau dans Microsoft Edge de | Documents Microsoft"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity "Journal de l’activité réseau : inspecter l’activité réseau dans Microsoft Edge devTools | Documents Microsoft"  

[MDNInlineFrame]: https://developer.mozilla.org/docs/Web/HTML/Element/iframe "<iframe> : l’élément Inline Frame | MDN"  
[MDNLearnWebDevelopment]: https://developer.mozilla.org/docs/Learn "En savoir plus sur les | MDN"  

> [!NOTE]
> <span data-ttu-id="71659-188">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="71659-188">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="71659-189">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/resources/index) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="71659-189">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/resources/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="71659-191">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="71659-191">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
