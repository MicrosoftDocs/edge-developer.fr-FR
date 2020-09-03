---
description: Référence complète des fonctionnalités du panneau réseau de Microsoft Edge DevTools.
title: Référence d’analyse du réseau
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 38570e6d196314aa6315a34f0b8b1b0b0d740c91
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993617"
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

# <span data-ttu-id="99b8a-104">Référence d’analyse du réseau</span><span class="sxs-lookup"><span data-stu-id="99b8a-104">Network Analysis Reference</span></span>  

<span data-ttu-id="99b8a-105">Découvrez de nouvelles façons d’analyser le chargement de votre page dans cette référence complète des fonctionnalités d’analyse du réseau Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="99b8a-105">Discover new ways to analyze how your page loads in this comprehensive reference of Microsoft Edge DevTools network analysis features.</span></span>  

<!--
> [!NOTE]
> This reference is based on Microsoft Edge 58.  If you use another version of Microsoft Edge, the UI, and features of DevTools may be different.  Check `edge://help` to see what version of Microsoft Edge you are running.  
-->

## <span data-ttu-id="99b8a-106">Enregistrer les requêtes réseau</span><span class="sxs-lookup"><span data-stu-id="99b8a-106">Record network requests</span></span>  

<span data-ttu-id="99b8a-107">Par défaut, DevTools enregistre toutes les requêtes réseau dans le panneau réseau, tant que DevTools est ouvert.</span><span class="sxs-lookup"><span data-stu-id="99b8a-107">By default, DevTools records all network requests in the Network panel, so long as DevTools is open.</span></span>  

:::image type="complex" source="../media/network-network-panel.msft.png" alt-text="Panneau réseau" lightbox="../media/network-network-panel.msft.png":::
   <span data-ttu-id="99b8a-109">Figure 1: panneau **réseau**</span><span class="sxs-lookup"><span data-stu-id="99b8a-109">Figure 1:  The **Network** panel</span></span>  
:::image-end:::  

### <span data-ttu-id="99b8a-110">Arrêter l’enregistrement des requêtes réseau</span><span class="sxs-lookup"><span data-stu-id="99b8a-110">Stop recording network requests</span></span>  

<span data-ttu-id="99b8a-111">Pour arrêter l’enregistrement de demandes, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="99b8a-111">To stop recording requests, complete the following steps.</span></span>  

1.  <span data-ttu-id="99b8a-112">Pour arrêter l' **enregistrement du journal du réseau** , cliquez sur arrêter l' ![ enregistrement réseau ][ImageRecordOnIcon] dans le panneau **réseau** .</span><span class="sxs-lookup"><span data-stu-id="99b8a-112">Select **Stop recording network log** ![Stop recording network log][ImageRecordOnIcon] on the **Network** panel.</span></span>  <span data-ttu-id="99b8a-113">Il devient gris pour indiquer que DevTools n’enregistre plus les demandes.</span><span class="sxs-lookup"><span data-stu-id="99b8a-113">It turns grey to indicate that DevTools is no longer recording requests.</span></span>  
1.  <span data-ttu-id="99b8a-114">Appuyez sur `Control` + `E` \ (Windows \) ou `Command` + `E` \ (MacOS \) lorsque le panneau **réseau** a le focus.</span><span class="sxs-lookup"><span data-stu-id="99b8a-114">Press `Control`+`E` \(Windows\) or `Command`+`E` \(macOS\) while the **Network** panel is in focus.</span></span>  

### <span data-ttu-id="99b8a-115">Supprimer des demandes</span><span class="sxs-lookup"><span data-stu-id="99b8a-115">Clear requests</span></span>  

<span data-ttu-id="99b8a-116">Sélectionnez **Effacer** ![ ][ImageClearIcon] le panneau réseau pour effacer toutes les demandes de la table demandes.</span><span class="sxs-lookup"><span data-stu-id="99b8a-116">Select **Clear** ![Clear][ImageClearIcon] on the Network panel to clear all requests from the Requests table.</span></span>  

:::image type="complex" source="../media/network-network-clear-button.msft.png" alt-text="Bouton Effacer" lightbox="../media/network-network-clear-button.msft.png":::
   <span data-ttu-id="99b8a-118">Figure 2: bouton **Effacer**</span><span class="sxs-lookup"><span data-stu-id="99b8a-118">Figure 2:  The **Clear** button</span></span>  
:::image-end:::  

### <span data-ttu-id="99b8a-119">Enregistrer les demandes lors du chargement de la page</span><span class="sxs-lookup"><span data-stu-id="99b8a-119">Save requests across page loads</span></span>  

<span data-ttu-id="99b8a-120">Pour enregistrer les demandes lors du chargement de la page, activez la case à cocher **conservation du journal** dans le panneau réseau.</span><span class="sxs-lookup"><span data-stu-id="99b8a-120">To save requests across page loads, check the **Preserve log** checkbox on the Network panel.</span></span>  <span data-ttu-id="99b8a-121">DevTools enregistre toutes les demandes jusqu’à ce que vous désactiviez le **Journal de conservation**.</span><span class="sxs-lookup"><span data-stu-id="99b8a-121">DevTools saves all requests until you disable **Preserve log**.</span></span>  

:::image type="complex" source="../media/network-network-preserve-log.msft.png" alt-text="Case à cocher conserver le journal" lightbox="../media/network-network-preserve-log.msft.png":::
   <span data-ttu-id="99b8a-123">Figure 3: case à cocher **conserver le journal**</span><span class="sxs-lookup"><span data-stu-id="99b8a-123">Figure 3:  The **Preserve Log** checkbox</span></span>  
:::image-end:::  

### <span data-ttu-id="99b8a-124">Capture de captures d’écran pendant le chargement de la page</span><span class="sxs-lookup"><span data-stu-id="99b8a-124">Capture screenshots during page load</span></span>  

<span data-ttu-id="99b8a-125">Capture des captures d’écran pour analyser ce que les utilisateurs voient lorsqu’ils attendent que votre page se charge.</span><span class="sxs-lookup"><span data-stu-id="99b8a-125">Capture screenshots to analyze what users see as they wait for your page to load.</span></span>  

<span data-ttu-id="99b8a-126">Pour activer les captures d’écran, sélectionnez **paramètres du réseau** , puis cochez la case **capturer les captures d’écran** dans le panneau **réseau** .</span><span class="sxs-lookup"><span data-stu-id="99b8a-126">To enable screenshots, select **Network settings** and select **Capture screenshots** checkbox on the **Network** panel.</span></span>  

<span data-ttu-id="99b8a-127">Actualisez la page lorsque le panneau **réseau** a le focus pour capturer les captures d’écran.</span><span class="sxs-lookup"><span data-stu-id="99b8a-127">Refresh the page while the **Network** panel is in focus to capture screenshots.</span></span>  

<span data-ttu-id="99b8a-128">Après avoir capturé une capture d’écran, vous interagissez comme suit.</span><span class="sxs-lookup"><span data-stu-id="99b8a-128">After capturing a screenshot, you interact with it in the following ways.</span></span>  

*   <span data-ttu-id="99b8a-129">Placez le pointeur de la souris sur une capture d’écran pour afficher le point d’acquisition de cette capture d’écran.</span><span class="sxs-lookup"><span data-stu-id="99b8a-129">Hover over a screenshot to view the point at which that screenshot was captured.</span></span>  <span data-ttu-id="99b8a-130">Une ligne jaune apparaît dans le volet **vue d’ensemble** .</span><span class="sxs-lookup"><span data-stu-id="99b8a-130">A yellow line appears on the **Overview** pane.</span></span>  
*   <span data-ttu-id="99b8a-131">Sélectionnez la miniature d’un écran pour filtrer toutes les demandes qui se sont produites après la capture de la capture d’écran.</span><span class="sxs-lookup"><span data-stu-id="99b8a-131">Select the thumbnail of a screen to filter out any requests that occurred after the screenshot was captured.</span></span>  
*   <span data-ttu-id="99b8a-132">Double-cliquez sur une miniature pour y effectuer un zoom.</span><span class="sxs-lookup"><span data-stu-id="99b8a-132">Double-click a thumbnail to zoom into it.</span></span>  

:::image type="complex" source="../media/network-network-screenshot-hover.msft.png" alt-text="Survol d’une capture d’écran" lightbox="../media/network-network-screenshot-hover.msft.png":::
   <span data-ttu-id="99b8a-134">Figure 4: survol d’une capture d’écran</span><span class="sxs-lookup"><span data-stu-id="99b8a-134">Figure 4:  Hovering over a screenshot</span></span>  
:::image-end:::  

<!--  ### Replay XHR request  -->

<!--  To replay an XHR request, hover on the request in the Requests table, open the contextual menu \(right-click\), and select **Replay XHR**.  -->

<!--  
:::image type="complex" source="../media/network-replay-xhr.msft.png" alt-text="Selecting Replay XHR" lightbox="../media/network-replay-xhr.msft.png":::
   Old Figure 5:  Selecting Replay XHR  
:::image-end:::  
-->  

## <span data-ttu-id="99b8a-135">Changer le comportement de chargement</span><span class="sxs-lookup"><span data-stu-id="99b8a-135">Change loading behavior</span></span>  

### <span data-ttu-id="99b8a-136">Émuler un visiteur pour la première fois en désactivant le cache du navigateur</span><span class="sxs-lookup"><span data-stu-id="99b8a-136">Emulate a first-time visitor by disabling the browser cache</span></span>  

<span data-ttu-id="99b8a-137">Pour émuler la façon dont un utilisateur a expériences de votre site pour la première fois, activez la case à cocher **désactiver le cache** .</span><span class="sxs-lookup"><span data-stu-id="99b8a-137">To emulate how a first-time user experiences your site, check the **Disable cache** checkbox.</span></span>  <span data-ttu-id="99b8a-138">DevTools désactive le cache du navigateur.</span><span class="sxs-lookup"><span data-stu-id="99b8a-138">DevTools disables the browser cache.</span></span>  <span data-ttu-id="99b8a-139">Cela a pour effet d’émuler de façon plus précise une première utilisation de l’utilisateur, car les requêtes sont servies dans le cache du navigateur sur les visites répétées.</span><span class="sxs-lookup"><span data-stu-id="99b8a-139">This more accurately emulates a first-time user's experience, because requests are served from the browser cache on repeat visits.</span></span>  

:::image type="complex" source="../media/network-network-disable-cache-checkbox.msft.png" alt-text="Case à cocher Désactiver le cache" lightbox="../media/network-network-disable-cache-checkbox.msft.png":::
   <span data-ttu-id="99b8a-141">Figure 5: case à cocher **désactiver le cache**</span><span class="sxs-lookup"><span data-stu-id="99b8a-141">Figure 5:  The **Disable Cache** checkbox</span></span>  
:::image-end:::  

#### <span data-ttu-id="99b8a-142">Désactiver le cache du navigateur dans le tiroir du réseau</span><span class="sxs-lookup"><span data-stu-id="99b8a-142">Disable the browser cache from the Network Conditions drawer</span></span>  

<span data-ttu-id="99b8a-143">Si vous voulez désactiver le cache lorsque vous travaillez dans d’autres panneaux DevTools, utilisez le tiroir de l’état du réseau.</span><span class="sxs-lookup"><span data-stu-id="99b8a-143">If you want to disable the cache while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="99b8a-144">Ouvrez le tiroir de **conditions du réseau** .</span><span class="sxs-lookup"><span data-stu-id="99b8a-144">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="99b8a-145">Cochez ou décochez la case **désactiver le cache** .</span><span class="sxs-lookup"><span data-stu-id="99b8a-145">Check or uncheck the **Disable cache** checkbox.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="99b8a-146">Vider manuellement le cache du navigateur</span><span class="sxs-lookup"><span data-stu-id="99b8a-146">Manually clear the browser cache</span></span>  

<span data-ttu-id="99b8a-147">Pour vider manuellement le cache du navigateur à tout moment, ouvrez le menu contextuel (cliquez avec le bouton droit sur \) n’importe où dans la table demandes et sélectionnez **Vider le cache du navigateur**.</span><span class="sxs-lookup"><span data-stu-id="99b8a-147">To manually clear the browser cache at any time, open the contextual menu \(right-click\) anywhere in the Requests table and select **Clear Browser Cache**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cache.msft.png" alt-text="Sélection de l’option vider le cache du navigateur" lightbox="../media/network-network-clear-browser-cache.msft.png":::
   <span data-ttu-id="99b8a-149">Figure 6: sélectionner **Vider le cache du navigateur**</span><span class="sxs-lookup"><span data-stu-id="99b8a-149">Figure 6:  Selecting **Clear Browser Cache**</span></span>  
:::image-end:::  

### <span data-ttu-id="99b8a-150">Émuler hors connexion</span><span class="sxs-lookup"><span data-stu-id="99b8a-150">Emulate offline</span></span>  

<span data-ttu-id="99b8a-151">Une nouvelle classe d’applications Web, appelées [applications Web progressives][DevtoolsProgressiveWebApps], fonctionne en mode hors connexion avec l’aide des **travailleurs de service**.</span><span class="sxs-lookup"><span data-stu-id="99b8a-151">A new class of web apps, named [Progressive Web Apps][DevtoolsProgressiveWebApps], functions offline with the help of **service workers**.</span></span>  <span data-ttu-id="99b8a-152">Vous constaterez peut-être qu’il est utile de simuler rapidement un appareil dépourvu de connexion aux données lors de la création de ce type d’application.</span><span class="sxs-lookup"><span data-stu-id="99b8a-152">You may find it useful to quickly simulate a device that has no data connection when you are building this type of app.</span></span>  

<!--[ServiceWorkers]: /web/fundamentals/getting-started/primers/service-workers  -->

<span data-ttu-id="99b8a-153">Sélectionnez le menu déroulant **en ligne** , Rechercher sous **présélections**, puis sélectionnez **hors ligne** pour simuler une interface réseau entièrement hors connexion.</span><span class="sxs-lookup"><span data-stu-id="99b8a-153">Select the **Online** dropdown menu, search under **Presets**, and select **Offline** to simulate a completely offline network experience.</span></span>  

:::image type="complex" source="../media/network-network-offline-dropdown.msft.png" alt-text="Menu déroulant hors connexion" lightbox="../media/network-network-offline-dropdown.msft.png":::
   <span data-ttu-id="99b8a-155">Figure 7: menu déroulant **hors connexion**</span><span class="sxs-lookup"><span data-stu-id="99b8a-155">Figure 7:  The **Offline** dropdown menu</span></span>  
:::image-end:::  

### <span data-ttu-id="99b8a-156">Émuler une connexion réseau lente</span><span class="sxs-lookup"><span data-stu-id="99b8a-156">Emulate slow network connections</span></span>  

<span data-ttu-id="99b8a-157">Émulez des vitesses de connexion 3G, Fast 3G et autres vitesses de connexion dans le menu déroulant **en ligne** .</span><span class="sxs-lookup"><span data-stu-id="99b8a-157">Emulate Slow 3G, Fast 3G, and other connection speeds from the **Online** dropdown menu.</span></span>  

:::image type="complex" source="../media/network-network-throttling-menu.msft.png" alt-text="Menu déroulant limitation" lightbox="../media/network-network-throttling-menu.msft.png":::
   <span data-ttu-id="99b8a-159">Figure 8: menu déroulant **limitation**</span><span class="sxs-lookup"><span data-stu-id="99b8a-159">Figure 8:  The **Throttling** dropdown menu</span></span>  
:::image-end:::  

<span data-ttu-id="99b8a-160">Vous pouvez faire votre choix parmi une série de présélections, par exemple, lente 3G ou Fast 3G.</span><span class="sxs-lookup"><span data-stu-id="99b8a-160">You may select from a variety of presets, such as Slow 3G or Fast 3G.</span></span>  <span data-ttu-id="99b8a-161">Vous pouvez également ajouter vos propres Présélections personnalisées en ouvrant le menu limitation et **Custom**en sélectionnant  >  **Ajouter**personnalisé.</span><span class="sxs-lookup"><span data-stu-id="99b8a-161">You may also add your own custom presets by opening the Throttling menu and selecting **Custom** > **Add**.</span></span>  

<span data-ttu-id="99b8a-162">DevTools affiche une icône d’avertissement en regard de l’onglet **réseau** pour vous rappeler que la limitation est activée.</span><span class="sxs-lookup"><span data-stu-id="99b8a-162">DevTools displays a warning icon next to the **Network** tab to remind you that throttling is enabled.</span></span>  

#### <span data-ttu-id="99b8a-163">Émuler une connexion réseau lente à partir du tiroir du réseau</span><span class="sxs-lookup"><span data-stu-id="99b8a-163">Emulate slow network connections from the Network Conditions drawer</span></span>  

<span data-ttu-id="99b8a-164">Si vous souhaitez limiter la connexion réseau lorsque vous travaillez dans d’autres panneaux DevTools, utilisez le tiroir de l’état du réseau.</span><span class="sxs-lookup"><span data-stu-id="99b8a-164">If you want to throttle the network connection while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="99b8a-165">Ouvrez le tiroir de **conditions du réseau** .</span><span class="sxs-lookup"><span data-stu-id="99b8a-165">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="99b8a-166">Sélectionnez le débit de connexion souhaité dans le menu **limitation** .</span><span class="sxs-lookup"><span data-stu-id="99b8a-166">Select your desired connection speed from the **Throttling** menu.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="99b8a-167">Effacement manuel des cookies du navigateur</span><span class="sxs-lookup"><span data-stu-id="99b8a-167">Manually clear browser cookies</span></span>  

<span data-ttu-id="99b8a-168">Pour effacer manuellement les cookies du navigateur à tout moment, ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \) n’importe où dans la table demandes, puis sélectionnez **effacer les cookies du navigateur**.</span><span class="sxs-lookup"><span data-stu-id="99b8a-168">To manually clear browser cookies at any time, open the contextual menu \(right-click\) anywhere in the Requests table and select **Clear Browser Cookies**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cookies.msft.png" alt-text="Sélection effacer les cookies du navigateur" lightbox="../media/network-network-clear-browser-cookies.msft.png":::
   <span data-ttu-id="99b8a-170">Figure 9: sélectionnez **effacer les cookies du navigateur**</span><span class="sxs-lookup"><span data-stu-id="99b8a-170">Figure 9:  Selecting **Clear Browser Cookies**</span></span>  
:::image-end:::  

### <span data-ttu-id="99b8a-171">Remplacer l’agent utilisateur</span><span class="sxs-lookup"><span data-stu-id="99b8a-171">Override the user agent</span></span>  

<span data-ttu-id="99b8a-172">Pour remplacer manuellement l’agent utilisateur, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="99b8a-172">To manually override the user agent:</span></span>  

1.  <span data-ttu-id="99b8a-173">Ouvrez le tiroir de **conditions du réseau** .</span><span class="sxs-lookup"><span data-stu-id="99b8a-173">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="99b8a-174">Décochez l' **option sélectionner automatiquement**.</span><span class="sxs-lookup"><span data-stu-id="99b8a-174">Uncheck **Select automatically**.</span></span>  
1.  <span data-ttu-id="99b8a-175">Choisissez une option de l’agent utilisateur dans le menu ou entrez-en un dans la zone de texte.</span><span class="sxs-lookup"><span data-stu-id="99b8a-175">Choose a user agent option from the menu, or enter a custom one in the text box.</span></span>  

<!--todo: add network condition section when available -->  

## <span data-ttu-id="99b8a-176">Demandes de filtre</span><span class="sxs-lookup"><span data-stu-id="99b8a-176">Filter requests</span></span>  

### <span data-ttu-id="99b8a-177">Filtrer les demandes par propriétés</span><span class="sxs-lookup"><span data-stu-id="99b8a-177">Filter requests by properties</span></span>  

<span data-ttu-id="99b8a-178">Utilisez la zone de texte **filtre** pour filtrer les demandes par propriétés, telles que le domaine ou la taille de la requête.</span><span class="sxs-lookup"><span data-stu-id="99b8a-178">Use the **Filter** text box to filter requests by properties, such as the domain or size of the request.</span></span>  

<span data-ttu-id="99b8a-179">Si vous ne voyez pas la zone de texte, le volet filtres est probablement masqué.</span><span class="sxs-lookup"><span data-stu-id="99b8a-179">If you do not see the text box, the Filters pane is probably hidden.</span></span>  
<span data-ttu-id="99b8a-180">Voir [masquer le volet filtres](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="99b8a-180">See [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

:::image type="complex" source="../media/network-network-filters-textbox.msft.png" alt-text="Zone de texte filtre" lightbox="../media/network-network-filters-textbox.msft.png":::
   <span data-ttu-id="99b8a-182">Figure 10: zone de texte de **filtre**</span><span class="sxs-lookup"><span data-stu-id="99b8a-182">Figure 10:  The **Filter** text box</span></span>  
:::image-end:::  

<span data-ttu-id="99b8a-183">Vous pouvez utiliser plusieurs propriétés simultanément en séparant chaque propriété d’un espace.</span><span class="sxs-lookup"><span data-stu-id="99b8a-183">You may use multiple properties simultaneously by separating each property with a space.</span></span>  <span data-ttu-id="99b8a-184">Par exemple, `mime-type:image/png larger-than:1K` affiche tous les png dont la taille est supérieure à 1 Ko.</span><span class="sxs-lookup"><span data-stu-id="99b8a-184">For example, `mime-type:image/png larger-than:1K` displays all PNGs that are larger than one kilobyte.</span></span>  <span data-ttu-id="99b8a-185">Ces filtres multi-propriété sont équivalents aux `AND` opérations.</span><span class="sxs-lookup"><span data-stu-id="99b8a-185">These multi-property filters are equivalent to `AND` operations.</span></span>  `OR` <span data-ttu-id="99b8a-186">les opérations ne sont actuellement pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="99b8a-186">operations are currently not supported.</span></span>  

<span data-ttu-id="99b8a-187">Liste complète des propriétés prises en charge.</span><span class="sxs-lookup"><span data-stu-id="99b8a-187">The complete list of supported properties.</span></span>  

| <span data-ttu-id="99b8a-188">Propriété</span><span class="sxs-lookup"><span data-stu-id="99b8a-188">Property</span></span> | <span data-ttu-id="99b8a-189">Détails</span><span class="sxs-lookup"><span data-stu-id="99b8a-189">Details</span></span> |  
|:--- | :--- |  
| `domain` | <span data-ttu-id="99b8a-190">Afficher uniquement les ressources du domaine spécifié.</span><span class="sxs-lookup"><span data-stu-id="99b8a-190">Only display resources from the specified domain.</span></span>  <span data-ttu-id="99b8a-191">Vous pouvez utiliser un caractère générique \ ( `*` \) pour inclure plusieurs domaines.</span><span class="sxs-lookup"><span data-stu-id="99b8a-191">You may use a wildcard character \(`*`\) to include multiple domains.</span></span>  <span data-ttu-id="99b8a-192">Par exemple, `*.com` affiche les ressources de tous les noms de domaine se terminant par `.com` .</span><span class="sxs-lookup"><span data-stu-id="99b8a-192">For example, `*.com` displays resources from all domain names ending in `.com`.</span></span>  <span data-ttu-id="99b8a-193">DevTools remplit le menu déroulant de saisie semi-automatique avec tous les domaines qu’il a rencontré.</span><span class="sxs-lookup"><span data-stu-id="99b8a-193">DevTools populates the autocomplete dropdown menu with all of the domains it has encountered.</span></span> |  
| `has-response-header` | <span data-ttu-id="99b8a-194">Afficher les ressources qui contiennent l’en-tête de réponse HTTP spécifié.</span><span class="sxs-lookup"><span data-stu-id="99b8a-194">Show the resources that contain the specified HTTP response header.</span></span>  <span data-ttu-id="99b8a-195">DevTools remplit la liste déroulante de saisie semi-automatique avec tous les en-têtes de réponse qu’il a rencontré.</span><span class="sxs-lookup"><span data-stu-id="99b8a-195">DevTools populates the autocomplete dropdown with all of the response headers that it has encountered.</span></span> |  
| `is` | <span data-ttu-id="99b8a-196">Utiliser `is:running` pour rechercher des `WebSocket` ressources.</span><span class="sxs-lookup"><span data-stu-id="99b8a-196">Use `is:running` to find `WebSocket` resources.</span></span> |  
| `larger-than` | <span data-ttu-id="99b8a-197">Afficher les ressources dont la taille est supérieure à la taille spécifiée, en octets.</span><span class="sxs-lookup"><span data-stu-id="99b8a-197">Show resources that are larger than the specified size, in bytes.</span></span>  <span data-ttu-id="99b8a-198">La définition d’une valeur est égale à la valeur `1000` `1k` .</span><span class="sxs-lookup"><span data-stu-id="99b8a-198">Setting a value of `1000` is equivalent to setting a value of `1k`.</span></span> |  
| `method` | <span data-ttu-id="99b8a-199">Afficher les ressources récupérées sur un type de méthode HTTP spécifié.</span><span class="sxs-lookup"><span data-stu-id="99b8a-199">Show resources that were retrieved over a specified HTTP method type.</span></span>  <span data-ttu-id="99b8a-200">DevTools remplit la liste déroulante avec toutes les méthodes HTTP qu’il a rencontrées.</span><span class="sxs-lookup"><span data-stu-id="99b8a-200">DevTools populates the dropdown with all of the HTTP methods it has encountered.</span></span> |  
| `mime-type` | <span data-ttu-id="99b8a-201">Afficher les ressources d’un type MIME spécifié.</span><span class="sxs-lookup"><span data-stu-id="99b8a-201">Show resources of a specified MIME type.</span></span>  <span data-ttu-id="99b8a-202">DevTools remplit la liste déroulante avec tous les types MIME qu’il a rencontré.</span><span class="sxs-lookup"><span data-stu-id="99b8a-202">DevTools populates the dropdown with all MIME types it has encountered.</span></span> |  
| `mixed-content` | <span data-ttu-id="99b8a-203">Affichez toutes les ressources de contenu mixte \ ( `mixed-content:all` \) ou uniquement celles actuellement affichées \ ( `mixed-content:displayed` \).</span><span class="sxs-lookup"><span data-stu-id="99b8a-203">Show all mixed content resources \(`mixed-content:all`\) or just the ones that are currently displayed \(`mixed-content:displayed`\).</span></span> |  
| `scheme` | <span data-ttu-id="99b8a-204">Afficher les ressources récupérées sur une connexion HTTP \ ( `scheme:http` \) ou protégé https \ ( `scheme:https` \).</span><span class="sxs-lookup"><span data-stu-id="99b8a-204">Show resources retrieved over unprotected HTTP \(`scheme:http`\) or protected HTTPS \(`scheme:https`\).</span></span> |  
| `set-cookie-domain` | <span data-ttu-id="99b8a-205">Afficher les ressources qui ont un `Set-Cookie` en-tête avec un `Domain` attribut qui correspond à la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="99b8a-205">Show the resources that have a `Set-Cookie` header with a `Domain` attribute that matches the specified value.</span></span>  <span data-ttu-id="99b8a-206">DevTools remplit la saisie semi-automatique avec tous les domaines de cookie qu’il a rencontré.</span><span class="sxs-lookup"><span data-stu-id="99b8a-206">DevTools populates the autocomplete with all of the cookie domains that it has encountered.</span></span> |  
| `set-cookie-name` | <span data-ttu-id="99b8a-207">Afficher les ressources possédant un `Set-Cookie` en-tête dont le nom correspond à la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="99b8a-207">Show the resources that have a `Set-Cookie` header with a name that matches the specified value.</span></span>  <span data-ttu-id="99b8a-208">DevTools remplit la saisie semi-automatique avec tous les noms de cookie qu’il a rencontré.</span><span class="sxs-lookup"><span data-stu-id="99b8a-208">DevTools populates the autocomplete with all of the cookie names that it has encountered.</span></span> |  
| `set-cookie-value` | <span data-ttu-id="99b8a-209">Afficher les ressources dont l' `Set-Cookie` en-tête comporte une valeur qui correspond à la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="99b8a-209">Show the resources that have a `Set-Cookie` header with a value that matches the specified value.</span></span>  <span data-ttu-id="99b8a-210">DevTools remplit la saisie semi-automatique avec toutes les valeurs de cookie qu’il a rencontrées.</span><span class="sxs-lookup"><span data-stu-id="99b8a-210">DevTools populates the autocomplete with all of the cookie values that it has encountered.</span></span> |  
| `status-code` | <span data-ttu-id="99b8a-211">Afficher uniquement les ressources pour lesquelles le code d’état HTTP correspond au code spécifié.</span><span class="sxs-lookup"><span data-stu-id="99b8a-211">Show only the resources for which the HTTP status code matches the specified code.</span></span>  <span data-ttu-id="99b8a-212">DevTools remplit le menu déroulant de saisie semi-automatique avec tous les codes d’État détectés.</span><span class="sxs-lookup"><span data-stu-id="99b8a-212">DevTools populates the autocomplete dropdown menu with all of the status codes it has encountered.</span></span> |  

### <span data-ttu-id="99b8a-213">Filtrer les demandes par type</span><span class="sxs-lookup"><span data-stu-id="99b8a-213">Filter requests by type</span></span>  

<span data-ttu-id="99b8a-214">Pour filtrer les demandes par type de requête, sélectionnez les boutons **XHR**, **js**, **CSS**, **img**, **multimédia**, **police**, **doc**, **WS** \ (WebSocket \), **manifeste**ou **autre** (n’importe quel autre type non répertorié ici \) sur le panneau réseau.</span><span class="sxs-lookup"><span data-stu-id="99b8a-214">To filter requests by request type, select the **XHR**, **JS**, **CSS**, **Img**, **Media**, **Font**, **Doc**, **WS** \(WebSocket\), **Manifest**, or **Other** \(any other type not listed here\) buttons on the Network panel.</span></span>  

<span data-ttu-id="99b8a-215">Si vous ne voyez pas ces boutons, le volet filtres est probablement masqué.</span><span class="sxs-lookup"><span data-stu-id="99b8a-215">If you do not see these buttons, the Filters pane is probably hidden.</span></span>  
<span data-ttu-id="99b8a-216">Voir [masquer le volet filtres](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="99b8a-216">See [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

<span data-ttu-id="99b8a-217">Pour activer plusieurs filtres de type simultanément, appuyez sur `Control` \ (Windows \) ou `Command` \ (MacOS \), puis sélectionnez.</span><span class="sxs-lookup"><span data-stu-id="99b8a-217">To enable multiple type filters simultaneously, hold `Control` \(Windows\) or `Command` \(macOS\) and then select.</span></span>  

:::image type="complex" source="../media/network-network-type-filters.msft.png" alt-text="Utiliser les filtres de type pour afficher les ressources JS, CSS et document" lightbox="../media/network-network-type-filters.msft.png":::
   <span data-ttu-id="99b8a-219">Figure 11: utilisation des filtres de type pour afficher les ressources JS, CSS et document</span><span class="sxs-lookup"><span data-stu-id="99b8a-219">Figure 11:  Using the Type filters to display JS, CSS, and Document resources</span></span>  
:::image-end:::  

### <span data-ttu-id="99b8a-220">Filtrer les demandes par heure</span><span class="sxs-lookup"><span data-stu-id="99b8a-220">Filter requests by time</span></span>  

<span data-ttu-id="99b8a-221">Sélectionnez et faites glisser vers la gauche ou la droite dans le volet vue d’ensemble pour afficher uniquement les demandes actives au cours de cette période.</span><span class="sxs-lookup"><span data-stu-id="99b8a-221">Select and drag left or right on the Overview pane to only display requests that were active during that time frame.</span></span>  <span data-ttu-id="99b8a-222">Le filtre est inclusive.</span><span class="sxs-lookup"><span data-stu-id="99b8a-222">The filter is inclusive.</span></span>  <span data-ttu-id="99b8a-223">Toutes les demandes qui ont été actives pendant la durée en surbrillance apparaissent.</span><span class="sxs-lookup"><span data-stu-id="99b8a-223">Any request that was active during the highlighted time is shown.</span></span>  

:::image type="complex" source="../media/network-network-overview-filter.msft.png" alt-text="Filtrage des requêtes inactives depuis 300M" lightbox="../media/network-network-overview-filter.msft.png":::
   <span data-ttu-id="99b8a-225">Figure 12: filtrage des requêtes inactives depuis 300 m</span><span class="sxs-lookup"><span data-stu-id="99b8a-225">Figure 12:  Filtering out any requests that were inactive around 300ms</span></span>  
:::image-end:::  

### <span data-ttu-id="99b8a-226">Masquer les URL de données</span><span class="sxs-lookup"><span data-stu-id="99b8a-226">Hide data URLs</span></span>  

<span data-ttu-id="99b8a-227">Les [URL de données][MDNHTTPDataURIs] sont des petits fichiers incorporés dans d’autres documents.</span><span class="sxs-lookup"><span data-stu-id="99b8a-227">[Data URLs][MDNHTTPDataURIs] are small files embedded into other documents.</span></span>  <span data-ttu-id="99b8a-228">Toute demande figurant dans la table demandes qui commence par `data:` est une URL de données.</span><span class="sxs-lookup"><span data-stu-id="99b8a-228">Any request that you see in the Requests table that starts with `data:` is a data URL.</span></span>  

<span data-ttu-id="99b8a-229">Cochez la case **Masquer les URL de données** pour masquer les demandes.</span><span class="sxs-lookup"><span data-stu-id="99b8a-229">Check the **Hide data URLs** checkbox to hide the requests.</span></span>  

:::image type="complex" source="../media/network-network-hide-data-urls.msft.png" alt-text="Case à cocher Masquer les URL de données" lightbox="../media/network-network-hide-data-urls.msft.png":::
   <span data-ttu-id="99b8a-231">Figure 13: cases à cocher **Masquer les URL de données**</span><span class="sxs-lookup"><span data-stu-id="99b8a-231">Figure 13:  The **Hide Data URLs** checkbox</span></span>  
:::image-end:::  

## <span data-ttu-id="99b8a-232">Demandes de tri</span><span class="sxs-lookup"><span data-stu-id="99b8a-232">Sort requests</span></span>  

<span data-ttu-id="99b8a-233">Par défaut, les requêtes dans la table demandes sont triées par heure de début, mais vous pouvez trier le tableau en utilisant d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="99b8a-233">By default, the requests in the Requests table are sorted by initiation time, but you may sort the table using other criteria.</span></span>  

### <span data-ttu-id="99b8a-234">Trier par colonne</span><span class="sxs-lookup"><span data-stu-id="99b8a-234">Sort by column</span></span>  

<span data-ttu-id="99b8a-235">Sélectionnez l’en-tête de n’importe quelle colonne dans les requêtes pour trier les demandes en se sur cette colonne.</span><span class="sxs-lookup"><span data-stu-id="99b8a-235">Select the header of any column in the Requests to sort requests by that column.</span></span>  

### <span data-ttu-id="99b8a-236">Trier par phase d’activité</span><span class="sxs-lookup"><span data-stu-id="99b8a-236">Sort by activity phase</span></span>  

<span data-ttu-id="99b8a-237">Pour modifier la façon dont les demandes de tri d’une cascade sont triées, pointez sur l’en-tête de la table demandes, ouvrez le menu **contextuel, puis**sélectionnez l’une des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="99b8a-237">To change how the Waterfall sorts requests, hover on the header of the Requests table, open the contextual menu \(right-click\), hover over **Waterfall**, and select one of the following options.</span></span>  

*   <span data-ttu-id="99b8a-238">**Heure de début**.</span><span class="sxs-lookup"><span data-stu-id="99b8a-238">**Start Time**.</span></span>  <span data-ttu-id="99b8a-239">La première requête lancée est en haut.</span><span class="sxs-lookup"><span data-stu-id="99b8a-239">The first request that was initiated is at the top.</span></span>  
*   <span data-ttu-id="99b8a-240">**Temps de réponse**.</span><span class="sxs-lookup"><span data-stu-id="99b8a-240">**Response Time**.</span></span>  <span data-ttu-id="99b8a-241">La première demande qui a démarré le téléchargement est en haut.</span><span class="sxs-lookup"><span data-stu-id="99b8a-241">The first request that started downloading is at the top.</span></span>  
*   <span data-ttu-id="99b8a-242">**Heure de fin**.</span><span class="sxs-lookup"><span data-stu-id="99b8a-242">**End Time**.</span></span>  <span data-ttu-id="99b8a-243">La première demande qui est terminée est en haut.</span><span class="sxs-lookup"><span data-stu-id="99b8a-243">The first request that finished is at the top.</span></span>  
*   <span data-ttu-id="99b8a-244">**Durée totale**.</span><span class="sxs-lookup"><span data-stu-id="99b8a-244">**Total Duration**.</span></span>  <span data-ttu-id="99b8a-245">La requête avec la configuration de connexion la plus courte et la demande/réponse se trouvent dans la partie supérieure.</span><span class="sxs-lookup"><span data-stu-id="99b8a-245">The request with the shortest connection setup and request / response is at the top.</span></span>  
*   <span data-ttu-id="99b8a-246">**Latence**.</span><span class="sxs-lookup"><span data-stu-id="99b8a-246">**Latency**.</span></span>  <span data-ttu-id="99b8a-247">La requête qui a attendu le plus court délai d’une réponse est située en haut.</span><span class="sxs-lookup"><span data-stu-id="99b8a-247">The request that waited the shortest time for a response is at the top.</span></span>  

<span data-ttu-id="99b8a-248">Ces descriptions présupposent que chaque option respective est classée du plus court au plus long.</span><span class="sxs-lookup"><span data-stu-id="99b8a-248">These descriptions assume that each respective option is ranked from shortest to longest.</span></span>  <span data-ttu-id="99b8a-249">La sélection de l’en-tête de la colonne en **cascade** inverse l’ordre.</span><span class="sxs-lookup"><span data-stu-id="99b8a-249">Selecting the header of the **Waterfall** column reverses the order.</span></span>  

:::image type="complex" source="../media/network-network-waterfall-total-duration.msft.png" alt-text="Tri des cascades par durée totale" lightbox="../media/network-network-waterfall-total-duration.msft.png":::
   <span data-ttu-id="99b8a-251">Figure 14: trier les cascades en fonction de la durée totale \ (la partie plus claire de chaque barre représente le temps passé en attente et la partie plus foncée est le temps de télécharger les octets \)</span><span class="sxs-lookup"><span data-stu-id="99b8a-251">Figure 14:  Sorting the Waterfall by total duration  \(The lighter portion of each bar is time spent waiting and the darker portion is time spent downloading bytes\)</span></span>  
:::image-end:::  

## <span data-ttu-id="99b8a-252">Analyser les requêtes</span><span class="sxs-lookup"><span data-stu-id="99b8a-252">Analyze requests</span></span>  

<span data-ttu-id="99b8a-253">Tant que DevTools est ouvert, il enregistre toutes les demandes dans le panneau réseau.</span><span class="sxs-lookup"><span data-stu-id="99b8a-253">So long as DevTools is open, it logs all requests in the Network panel.</span></span>  
<span data-ttu-id="99b8a-254">Utilisez le volet réseau pour analyser les requêtes.</span><span class="sxs-lookup"><span data-stu-id="99b8a-254">Use the Network panel to analyze requests.</span></span>  

### <span data-ttu-id="99b8a-255">Afficher un journal des demandes</span><span class="sxs-lookup"><span data-stu-id="99b8a-255">View a log of requests</span></span>  

<span data-ttu-id="99b8a-256">Utilisez le tableau demandes pour afficher un journal de toutes les demandes effectuées lorsque DevTools est ouvert.</span><span class="sxs-lookup"><span data-stu-id="99b8a-256">Use the Requests table to view a log of all requests made while DevTools has been open.</span></span>  <span data-ttu-id="99b8a-257">La sélection ou le passage de demandes au-dessus révèle des informations supplémentaires sur chaque élément.</span><span class="sxs-lookup"><span data-stu-id="99b8a-257">Selecting or hovering over requests reveals more information about each item.</span></span>  

:::image type="complex" source="../media/network-network-requests-table.msft.png" alt-text="Table demandes" lightbox="../media/network-network-requests-table.msft.png":::
   <span data-ttu-id="99b8a-259">Figure 15: table demandes</span><span class="sxs-lookup"><span data-stu-id="99b8a-259">Figure 15:  The Requests table</span></span>  
:::image-end:::  

<span data-ttu-id="99b8a-260">La table demandes affiche les colonnes suivantes par défaut.</span><span class="sxs-lookup"><span data-stu-id="99b8a-260">The Requests table displays the following columns by default.</span></span>  

*   <span data-ttu-id="99b8a-261">**Nom**.</span><span class="sxs-lookup"><span data-stu-id="99b8a-261">**Name**.</span></span>  <span data-ttu-id="99b8a-262">Nom de fichier ou un identificateur pour la ressource.</span><span class="sxs-lookup"><span data-stu-id="99b8a-262">The filename of, or an identifier for, the resource.</span></span>  
*   <span data-ttu-id="99b8a-263">**Status**.</span><span class="sxs-lookup"><span data-stu-id="99b8a-263">**Status**.</span></span>  <span data-ttu-id="99b8a-264">Code d’état HTTP.</span><span class="sxs-lookup"><span data-stu-id="99b8a-264">The HTTP status code.</span></span>  
*   <span data-ttu-id="99b8a-265">**Type**.</span><span class="sxs-lookup"><span data-stu-id="99b8a-265">**Type**.</span></span>  <span data-ttu-id="99b8a-266">Type MIME de la ressource demandée.</span><span class="sxs-lookup"><span data-stu-id="99b8a-266">The MIME type of the requested resource.</span></span>  
*   <span data-ttu-id="99b8a-267">**Initiator**.</span><span class="sxs-lookup"><span data-stu-id="99b8a-267">**Initiator**.</span></span>  <span data-ttu-id="99b8a-268">Les requêtes d’ouverture des objets ou processus suivants sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="99b8a-268">The following objects or processes initiate requests:</span></span>  
    *   <span data-ttu-id="99b8a-269">**Analyseur**.</span><span class="sxs-lookup"><span data-stu-id="99b8a-269">**Parser**.</span></span>  <span data-ttu-id="99b8a-270">Analyseur HTML pour Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="99b8a-270">The HTML parser for Microsoft Edge.</span></span>  
    *   <span data-ttu-id="99b8a-271">**Redirect**.</span><span class="sxs-lookup"><span data-stu-id="99b8a-271">**Redirect**.</span></span>  <span data-ttu-id="99b8a-272">Une redirection HTTP.</span><span class="sxs-lookup"><span data-stu-id="99b8a-272">An HTTP redirect.</span></span>  
    *   <span data-ttu-id="99b8a-273">**Script**.</span><span class="sxs-lookup"><span data-stu-id="99b8a-273">**Script**.</span></span>  <span data-ttu-id="99b8a-274">Fonction JavaScript.</span><span class="sxs-lookup"><span data-stu-id="99b8a-274">A JavaScript function.</span></span>  
    *   <span data-ttu-id="99b8a-275">**Autre**.</span><span class="sxs-lookup"><span data-stu-id="99b8a-275">**Other**.</span></span>  <span data-ttu-id="99b8a-276">Un autre processus ou action, comme la navigation vers une page par le biais d’un lien ou la saisie d’une URL dans la barre d’adresses.</span><span class="sxs-lookup"><span data-stu-id="99b8a-276">Some other process or action, such as navigating to a page via a link or entering a URL in the address bar.</span></span>  
*   <span data-ttu-id="99b8a-277">**Taille**.</span><span class="sxs-lookup"><span data-stu-id="99b8a-277">**Size**.</span></span>  <span data-ttu-id="99b8a-278">Taille combinée des en-têtes de réponse et du corps de la réponse, tel qu’il est délivré par le serveur.</span><span class="sxs-lookup"><span data-stu-id="99b8a-278">The combined size of the response headers plus the response body, as delivered by the server.</span></span>  
*   <span data-ttu-id="99b8a-279">**Temps**.</span><span class="sxs-lookup"><span data-stu-id="99b8a-279">**Time**.</span></span>  <span data-ttu-id="99b8a-280">Durée totale, entre le début de la demande et la réception de l’octet final dans la réponse.</span><span class="sxs-lookup"><span data-stu-id="99b8a-280">The total duration, from the start of the request to the receipt of the final byte in the response.</span></span>  
*   <span data-ttu-id="99b8a-281">En [**cascade**](#view-the-timing-of-requests-in-relation-to-one-another).</span><span class="sxs-lookup"><span data-stu-id="99b8a-281">[**Waterfall**](#view-the-timing-of-requests-in-relation-to-one-another).</span></span>  <span data-ttu-id="99b8a-282">Répartition visuelle de l’activité pour chaque demande.</span><span class="sxs-lookup"><span data-stu-id="99b8a-282">A visual breakdown of the activity for each request.</span></span>  

#### <span data-ttu-id="99b8a-283">Ajouter ou supprimer des colonnes</span><span class="sxs-lookup"><span data-stu-id="99b8a-283">Add or remove columns</span></span>  

<span data-ttu-id="99b8a-284">Placez le curseur sur l’en-tête de la table demandes, ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \), puis sélectionnez une option pour la masquer ou l’afficher.</span><span class="sxs-lookup"><span data-stu-id="99b8a-284">Hover on the header of the Requests table, open the contextual menu \(right-click\), and select an option to hide or show it.</span></span>  <span data-ttu-id="99b8a-285">Les options actuellement affichées disposent de coches en regard de chaque élément.</span><span class="sxs-lookup"><span data-stu-id="99b8a-285">Currently displayed options have checkmarks next to each item.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-column.msft.png" alt-text="Ajout d’une colonne dans la table demandes" lightbox="../media/network-network-requests-add-column.msft.png":::
   <span data-ttu-id="99b8a-287">Figure 16: ajout d’une colonne dans la table demandes</span><span class="sxs-lookup"><span data-stu-id="99b8a-287">Figure 16:  Adding a column to the Requests table</span></span>  
:::image-end:::  

#### <span data-ttu-id="99b8a-288">Ajouter des colonnes personnalisées</span><span class="sxs-lookup"><span data-stu-id="99b8a-288">Add custom columns</span></span>  

<span data-ttu-id="99b8a-289">Pour ajouter une colonne personnalisée dans la table demandes, positionnez le curseur sur l’en-tête de la table demandes, ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \), puis sélectionnez les **en-têtes de réponse**  >  **gérer les colonnes d’en-tête**.</span><span class="sxs-lookup"><span data-stu-id="99b8a-289">To add a custom column to the Requests table, hover on the header of the Requests table, open the contextual menu \(right-click\), and select **Response Headers** > **Manage Header Columns**.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-custom.msft.png" alt-text="Ajout d’une colonne personnalisée dans la table demandes" lightbox="../media/network-network-requests-add-custom.msft.png":::
   <span data-ttu-id="99b8a-291">Figure 17: ajout d’une colonne personnalisée dans la table demandes</span><span class="sxs-lookup"><span data-stu-id="99b8a-291">Figure 17:  Adding a custom column to the Requests table</span></span>  
:::image-end:::  

### <span data-ttu-id="99b8a-292">Afficher le minutage des requêtes les uns par rapport aux autres</span><span class="sxs-lookup"><span data-stu-id="99b8a-292">View the timing of requests in relation to one another</span></span>  

<span data-ttu-id="99b8a-293">Utilisez la cascade pour afficher le minutage des requêtes les uns par rapport aux autres.</span><span class="sxs-lookup"><span data-stu-id="99b8a-293">Use the Waterfall to view the timing of requests in relation to one another.</span></span>  
<span data-ttu-id="99b8a-294">Par défaut, la cascade est organisée selon l’heure de début des requêtes.</span><span class="sxs-lookup"><span data-stu-id="99b8a-294">By default, the Waterfall is organized by the start time of the requests.</span></span>  
<span data-ttu-id="99b8a-295">Par conséquent, les demandes qui sont plus éloignées de gauche que celles qui sont plus éloignées.</span><span class="sxs-lookup"><span data-stu-id="99b8a-295">So, requests that are farther to the left started earlier than those that are farther to the right.</span></span>  

<span data-ttu-id="99b8a-296">Pour plus d’options, voir [Trier par phase d’activité](#sort-by-activity-phase) .</span><span class="sxs-lookup"><span data-stu-id="99b8a-296">See [Sort by activity phase](#sort-by-activity-phase) to see the different ways that you may sort the Waterfall.</span></span>  

:::image type="complex" source="../media/network-network-requests-waterfall.msft.png" alt-text="Colonne cascade du volet demandes" lightbox="../media/network-network-requests-waterfall.msft.png":::
   <span data-ttu-id="99b8a-298">Figure 18: colonne cascade du volet **demandes**</span><span class="sxs-lookup"><span data-stu-id="99b8a-298">Figure 18:  The Waterfall column of the **Requests** pane</span></span>  
:::image-end:::  

<!-- ### Analyze the frames of a WebSocket Connection  -->

<!--To view the frames of a WebSocket connection:  

1.  Select the URL of the WebSocket connection, under the **Name** column of the Requests table.  
1.  Select the **Frames** tab.  The table shows the last 100 frames.  

To refresh the table, re-select the name of the WebSocket connection under the **Name** column of the Requests table.  -->

<!--
:::image type="complex" source="../media/network-frames.msft.png" alt-text="The Frames tab" lightbox="../media/network-frames.msft.png":::
   Old Figure 20:  The **Frames** tab  
:::image-end:::  
-->

<!--The table contains three columns:  

*   **Data**.  The message payload.  If the message is plain text, it is displayed here.  For binary opcodes, this column displays the name and code of the opcode.  The following opcodes are supported: Continuation Frame, Binary Frame, Connection Close Frame, Ping Frame, and Pong Frame.  
*   **Length**.  The length of the message payload, in bytes.  
*   **Time**.  The time when the message was received or sent.  -->

<!--Messages are color-coded according to their type:  

*   Outgoing text messages are light-green.  
*   Incoming text messages are white.  
*   WebSocket opcodes are light-yellow.  
*   Errors are light-red.  -->

### <span data-ttu-id="99b8a-299">Afficher un aperçu d’un corps de réponse</span><span class="sxs-lookup"><span data-stu-id="99b8a-299">View a preview of a response body</span></span>  

<span data-ttu-id="99b8a-300">Pour afficher un aperçu d’un corps de réponse:</span><span class="sxs-lookup"><span data-stu-id="99b8a-300">To view a preview of a response body:</span></span>  

1.  <span data-ttu-id="99b8a-301">Sélectionnez l’URL de la requête dans la colonne **nom** de la table demandes.</span><span class="sxs-lookup"><span data-stu-id="99b8a-301">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="99b8a-302">Sélectionnez l’onglet **Aperçu** .</span><span class="sxs-lookup"><span data-stu-id="99b8a-302">Select the **Preview** tab.</span></span>  

<span data-ttu-id="99b8a-303">Cet onglet est principalement utile pour afficher des images.</span><span class="sxs-lookup"><span data-stu-id="99b8a-303">This tab is mostly useful for viewing images.</span></span>  

:::image type="complex" source="../media/network-network-resources-preview.msft.png" alt-text="Onglet Aperçu" lightbox="../media/network-network-resources-preview.msft.png":::
   <span data-ttu-id="99b8a-305">Figure 19: onglet **Aperçu**</span><span class="sxs-lookup"><span data-stu-id="99b8a-305">Figure 19:  The **Preview** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="99b8a-306">Afficher le corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="99b8a-306">View a response body</span></span>  

<span data-ttu-id="99b8a-307">Pour afficher le corps de la réponse à une demande:</span><span class="sxs-lookup"><span data-stu-id="99b8a-307">To view the response body to a request:</span></span>  

1.  <span data-ttu-id="99b8a-308">Sélectionnez l’URL de la requête dans la colonne **nom** de la table demandes.</span><span class="sxs-lookup"><span data-stu-id="99b8a-308">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="99b8a-309">Sélectionnez l’onglet **réponse** .</span><span class="sxs-lookup"><span data-stu-id="99b8a-309">Select the **Response** tab.</span></span>  

:::image type="complex" source="../media/network-network-resources-response.msft.png" alt-text="Onglet réponse" lightbox="../media/network-network-resources-response.msft.png":::
   <span data-ttu-id="99b8a-311">Figure 20: onglet **réponse**</span><span class="sxs-lookup"><span data-stu-id="99b8a-311">Figure 20:  The **Response** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="99b8a-312">Afficher les en-têtes HTTP</span><span class="sxs-lookup"><span data-stu-id="99b8a-312">View HTTP headers</span></span>  

<span data-ttu-id="99b8a-313">Pour afficher les données d’en-tête HTTP relatives à une requête:</span><span class="sxs-lookup"><span data-stu-id="99b8a-313">To view HTTP header data about a request:</span></span>  

1.  <span data-ttu-id="99b8a-314">Sélectionnez l’URL de la requête dans la colonne **nom** de la table demandes.</span><span class="sxs-lookup"><span data-stu-id="99b8a-314">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="99b8a-315">Sélectionnez l’onglet **en-têtes** .</span><span class="sxs-lookup"><span data-stu-id="99b8a-315">Select the **Headers** tab.</span></span>  

:::image type="complex" source="../media/network-resources-headers.msft.png" alt-text="Onglet en-têtes" lightbox="../media/network-resources-headers.msft.png":::
   <span data-ttu-id="99b8a-317">Figure 21: onglet **en-têtes**</span><span class="sxs-lookup"><span data-stu-id="99b8a-317">Figure 21:  The **Headers** tab</span></span>  
:::image-end:::  

#### <span data-ttu-id="99b8a-318">Afficher une source d’en-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="99b8a-318">View HTTP header source</span></span>  

<span data-ttu-id="99b8a-319">Par défaut, l’onglet en-têtes affiche les noms des en-têtes par ordre alphabétique.</span><span class="sxs-lookup"><span data-stu-id="99b8a-319">By default, the Headers tab shows header names alphabetically.</span></span>  <span data-ttu-id="99b8a-320">Pour afficher les noms d’en-tête HTTP dans l’ordre dans lequel ils ont été reçus:</span><span class="sxs-lookup"><span data-stu-id="99b8a-320">To view the HTTP header names in the order they were received:</span></span>  

1.  <span data-ttu-id="99b8a-321">Ouvrez l’onglet **en-têtes** pour la requête qui vous intéresse.</span><span class="sxs-lookup"><span data-stu-id="99b8a-321">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="99b8a-322">Voir [afficher les en-têtes http](#view-http-headers).</span><span class="sxs-lookup"><span data-stu-id="99b8a-322">See [View HTTP headers](#view-http-headers).</span></span>  
1.  <span data-ttu-id="99b8a-323">Sélectionnez **afficher la source**, en regard de la section en **-tête de requête** ou **en-tête de réponse** .</span><span class="sxs-lookup"><span data-stu-id="99b8a-323">Select **view source**, next to the **Request Header** or **Response Header** section.</span></span>  

### <span data-ttu-id="99b8a-324">Afficher les paramètres de chaîne de requête</span><span class="sxs-lookup"><span data-stu-id="99b8a-324">View query string parameters</span></span>  

<span data-ttu-id="99b8a-325">Pour afficher les paramètres de chaîne de requête d’une URL dans un format lisible par l’utilisateur:</span><span class="sxs-lookup"><span data-stu-id="99b8a-325">To view the query string parameters of a URL in a human-readable format:</span></span>  

1.  <span data-ttu-id="99b8a-326">Ouvrez l’onglet **en-têtes** pour la requête qui vous intéresse.</span><span class="sxs-lookup"><span data-stu-id="99b8a-326">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="99b8a-327">Voir [afficher les en-têtes http](#view-http-headers).</span><span class="sxs-lookup"><span data-stu-id="99b8a-327">See [View HTTP headers](#view-http-headers).</span></span>  
1.  <span data-ttu-id="99b8a-328">Accédez à la section **paramètres de chaîne de requête** .</span><span class="sxs-lookup"><span data-stu-id="99b8a-328">Go to the **Query String Parameters** section.</span></span>  

:::image type="complex" source="../media/network-network-resources-headers-query-string-parameters.msft.png" alt-text="Section paramètres de chaîne de requête" lightbox="../media/network-network-resources-headers-query-string-parameters.msft.png":::
   <span data-ttu-id="99b8a-330">Figure 22: section **paramètres de chaînes de requête**</span><span class="sxs-lookup"><span data-stu-id="99b8a-330">Figure 22:  The **Query String Parameters** section</span></span>  
:::image-end:::  

#### <span data-ttu-id="99b8a-331">Afficher les paramètres de chaîne de requête source</span><span class="sxs-lookup"><span data-stu-id="99b8a-331">View query string parameters source</span></span>  

<span data-ttu-id="99b8a-332">Pour afficher la source du paramètre de chaîne de requête d’une requête:</span><span class="sxs-lookup"><span data-stu-id="99b8a-332">To view the query string parameter source of a request:</span></span>  

1.  <span data-ttu-id="99b8a-333">Accédez à la section paramètres de chaîne de requête.</span><span class="sxs-lookup"><span data-stu-id="99b8a-333">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="99b8a-334">Voir [afficher les paramètres de chaîne de requête](#view-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="99b8a-334">See [View query string parameters](#view-query-string-parameters).</span></span>  
1.  <span data-ttu-id="99b8a-335">Sélectionnez **afficher la source**.</span><span class="sxs-lookup"><span data-stu-id="99b8a-335">Select **view source**.</span></span>  

#### <span data-ttu-id="99b8a-336">Afficher les paramètres de chaîne de requête codés en URL</span><span class="sxs-lookup"><span data-stu-id="99b8a-336">View URL-encoded query string parameters</span></span>  

<span data-ttu-id="99b8a-337">Pour afficher les paramètres de chaîne de requête dans un format lisible par l’utilisateur, mais avec les codages conservés:</span><span class="sxs-lookup"><span data-stu-id="99b8a-337">To view query string parameters in a human-readable format, but with encodings preserved:</span></span>  

1.  <span data-ttu-id="99b8a-338">Accédez à la section paramètres de chaîne de requête.</span><span class="sxs-lookup"><span data-stu-id="99b8a-338">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="99b8a-339">Voir [afficher les paramètres de chaîne de requête](#view-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="99b8a-339">See [View query string parameters](#view-query-string-parameters).</span></span>  
1.  <span data-ttu-id="99b8a-340">Sélectionnez **afficher l’URL**.</span><span class="sxs-lookup"><span data-stu-id="99b8a-340">Select **view URL encoded**.</span></span>  

### <span data-ttu-id="99b8a-341">Afficher les cookies</span><span class="sxs-lookup"><span data-stu-id="99b8a-341">View cookies</span></span>  

<span data-ttu-id="99b8a-342">Pour afficher les cookies envoyés dans l’en-tête HTTP d’une requête:</span><span class="sxs-lookup"><span data-stu-id="99b8a-342">To view the cookies sent in the HTTP header of a request:</span></span>  

1.  <span data-ttu-id="99b8a-343">Sélectionnez l’URL de la requête dans la colonne **nom** de la table demandes.</span><span class="sxs-lookup"><span data-stu-id="99b8a-343">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="99b8a-344">Sélectionnez l’onglet **cookies** .</span><span class="sxs-lookup"><span data-stu-id="99b8a-344">Select the **Cookies** tab.</span></span>  

<!--See [Fields][ManageDataCookiesFields] for a description of each of the columns.  -->

<!--[ManageDataCookiesFields]: manage-data/cookies#fields  -->
<!--TODO: add link when section is available -->

:::image type="complex" source="../media/network-network-resources-cookies.msft.png" alt-text="Onglet cookies" lightbox="../media/network-network-resources-cookies.msft.png":::
   <span data-ttu-id="99b8a-346">Figure 23: onglet cookies</span><span class="sxs-lookup"><span data-stu-id="99b8a-346">Figure 23:  The Cookies tab</span></span>  
:::image-end:::  

### <span data-ttu-id="99b8a-347">Afficher la répartition du minutage d’une requête</span><span class="sxs-lookup"><span data-stu-id="99b8a-347">View the timing breakdown of a request</span></span>  

<span data-ttu-id="99b8a-348">Pour afficher la répartition du minutage d’une requête:</span><span class="sxs-lookup"><span data-stu-id="99b8a-348">To view the timing breakdown of a request:</span></span>  

1.  <span data-ttu-id="99b8a-349">Sélectionnez l’URL de la requête dans la colonne **nom** de la table demandes.</span><span class="sxs-lookup"><span data-stu-id="99b8a-349">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="99b8a-350">Sélectionnez l’onglet **minutage** .</span><span class="sxs-lookup"><span data-stu-id="99b8a-350">Select the **Timing** tab.</span></span>  

<span data-ttu-id="99b8a-351">Pour plus d’informations sur l’accès à ces données, voir [aperçu d’une répartition du temps](#preview-a-timing-breakdown) .</span><span class="sxs-lookup"><span data-stu-id="99b8a-351">See [Preview a timing breakdown](#preview-a-timing-breakdown) for a faster way to access this data.</span></span>  

<span data-ttu-id="99b8a-352">Pour plus d’informations sur les différentes phases que vous pouvez voir dans l’onglet Minutage, consultez la rubrique [étapes de répartition du temps](#timing-breakdown-phases-explained) .</span><span class="sxs-lookup"><span data-stu-id="99b8a-352">See [Timing breakdown phases explained](#timing-breakdown-phases-explained) for more information about each of the phases that you may see in the Timing tab.</span></span>  

:::image type="complex" source="../media/network-network-resources-timing.msft.png" alt-text="Onglet Minutage" lightbox="../media/network-network-resources-timing.msft.png":::
   <span data-ttu-id="99b8a-354">Figure 24: onglet **minutage**</span><span class="sxs-lookup"><span data-stu-id="99b8a-354">Figure 24:  The **Timing** tab</span></span>  
:::image-end:::  

<span data-ttu-id="99b8a-355">Plus d’informations sur chacune de ces étapes.</span><span class="sxs-lookup"><span data-stu-id="99b8a-355">More information about each of the phases.</span></span>  

<span data-ttu-id="99b8a-356">Pour accéder à cet affichage, voir répartition de l' [affichage du minutage](#view-the-timing-breakdown-of-a-request) .</span><span class="sxs-lookup"><span data-stu-id="99b8a-356">See [View timing breakdown](#view-the-timing-breakdown-of-a-request) for another way to access this view.</span></span>  

#### <span data-ttu-id="99b8a-357">Prévisualiser une répartition de minutage</span><span class="sxs-lookup"><span data-stu-id="99b8a-357">Preview a timing breakdown</span></span>  

<span data-ttu-id="99b8a-358">Pour afficher un aperçu de la répartition du minutage d’une requête, placez le pointeur sur l’entrée de la requête dans la colonne **cascade** de la table demandes.</span><span class="sxs-lookup"><span data-stu-id="99b8a-358">To view a preview of the timing breakdown of a request, hover over the entry for the request in the **Waterfall** column of the Requests table.</span></span>  

<span data-ttu-id="99b8a-359">Pour accéder à ces données qui ne nécessitent pas de pointage, voir [afficher la répartition du minutage d’une demande](#view-the-timing-breakdown-of-a-request) .</span><span class="sxs-lookup"><span data-stu-id="99b8a-359">See [View the timing breakdown of a request](#view-the-timing-breakdown-of-a-request) for a way to access this data that does not require hovering.</span></span>  

:::image type="complex" source="../media/network-network-resources-waterfall-hover.msft.png" alt-text="> aperçu de la répartition du minutage d’une requête" lightbox="../media/network-network-resources-waterfall-hover.msft.png":::
   <span data-ttu-id="99b8a-361">Figure 25: prévisualisation de la répartition du minutage d’une requête</span><span class="sxs-lookup"><span data-stu-id="99b8a-361">Figure 25:  Previewing the timing breakdown of a request</span></span>  
:::image-end:::  

#### <span data-ttu-id="99b8a-362">Explication des phases de répartition du temps</span><span class="sxs-lookup"><span data-stu-id="99b8a-362">Timing breakdown phases explained</span></span>  

<span data-ttu-id="99b8a-363">Plus d’informations sur chacune des phases que vous pouvez voir dans l’onglet **minutage** .</span><span class="sxs-lookup"><span data-stu-id="99b8a-363">More information about each of the phases you may see in the **Timing** tab.</span></span>  

*   <span data-ttu-id="99b8a-364">Mise en **file d’attente**.</span><span class="sxs-lookup"><span data-stu-id="99b8a-364">**Queueing**.</span></span>  <span data-ttu-id="99b8a-365">Le navigateur met en file d’attente les requêtes dans les cas suivants:</span><span class="sxs-lookup"><span data-stu-id="99b8a-365">The browser queues requests when:</span></span>  
    *   <span data-ttu-id="99b8a-366">Il y a des demandes de priorité plus élevées.</span><span class="sxs-lookup"><span data-stu-id="99b8a-366">There are higher priority requests.</span></span>  
    *   <span data-ttu-id="99b8a-367">Il existe déjà six connexions TCP ouvertes pour cette origine, qui correspond à la limite.</span><span class="sxs-lookup"><span data-stu-id="99b8a-367">There are already six TCP connections open for this origin, which is the limit.</span></span>  <span data-ttu-id="99b8a-368">S’applique uniquement aux protocoles HTTP/1.0 et HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="99b8a-368">Applies to HTTP/1.0 and HTTP/1.1 only.</span></span>  
    *   <span data-ttu-id="99b8a-369">Le navigateur alloue de l’espace dans le cache disque.</span><span class="sxs-lookup"><span data-stu-id="99b8a-369">The browser is briefly allocating space in the disk cache.</span></span>  
*   <span data-ttu-id="99b8a-370">**Bloqué**.</span><span class="sxs-lookup"><span data-stu-id="99b8a-370">**Stalled**.</span></span>  <span data-ttu-id="99b8a-371">La requête peut être bloquée pour l’une des raisons décrites dans la **file d’attente**.</span><span class="sxs-lookup"><span data-stu-id="99b8a-371">The request could be stalled for any of the reasons described in **Queueing**.</span></span>  
*   <span data-ttu-id="99b8a-372">**Recherche DNS**.</span><span class="sxs-lookup"><span data-stu-id="99b8a-372">**DNS Lookup**.</span></span>  <span data-ttu-id="99b8a-373">Le navigateur résout l’adresse IP pour la requête.</span><span class="sxs-lookup"><span data-stu-id="99b8a-373">The browser is resolving the IP address for the request.</span></span>  
*   <span data-ttu-id="99b8a-374">**Connexion initiale**.</span><span class="sxs-lookup"><span data-stu-id="99b8a-374">**Initial connection**.</span></span>  <span data-ttu-id="99b8a-375">Le navigateur établit une connexion, notamment les négociations TCP, les tentatives de connexion TCP et la négociation d’une connexion SSL.</span><span class="sxs-lookup"><span data-stu-id="99b8a-375">The browser is establishing a connection including TCP handshakes, TCP retries, and negotiating an SSL.</span></span>
*   <span data-ttu-id="99b8a-376">**Négociation de proxy**.</span><span class="sxs-lookup"><span data-stu-id="99b8a-376">**Proxy negotiation**.</span></span>  <span data-ttu-id="99b8a-377">Le navigateur négocie la requête avec un [serveur proxy][WikiProxyServer].</span><span class="sxs-lookup"><span data-stu-id="99b8a-377">The browser is negotiating the request with a [proxy server][WikiProxyServer].</span></span>  
*   <span data-ttu-id="99b8a-378">**Demande envoyée**.</span><span class="sxs-lookup"><span data-stu-id="99b8a-378">**Request sent**.</span></span>  <span data-ttu-id="99b8a-379">La requête est en cours d’envoi.</span><span class="sxs-lookup"><span data-stu-id="99b8a-379">The request is being sent.</span></span>  
*   <span data-ttu-id="99b8a-380">**Préparation ServiceWorker**.</span><span class="sxs-lookup"><span data-stu-id="99b8a-380">**ServiceWorker Preparation**.</span></span>  <span data-ttu-id="99b8a-381">Le navigateur démarre le travailleur du service.</span><span class="sxs-lookup"><span data-stu-id="99b8a-381">The browser is starting up the service worker.</span></span>  
*   <span data-ttu-id="99b8a-382">**Demander à ServiceWorker**.</span><span class="sxs-lookup"><span data-stu-id="99b8a-382">**Request to ServiceWorker**.</span></span>  <span data-ttu-id="99b8a-383">La demande est envoyée au travailleur de service.</span><span class="sxs-lookup"><span data-stu-id="99b8a-383">The request is being sent to the service worker.</span></span>  
*   <span data-ttu-id="99b8a-384">En **attente \ (TTFB \)**.</span><span class="sxs-lookup"><span data-stu-id="99b8a-384">**Waiting \(TTFB\)**.</span></span>  <span data-ttu-id="99b8a-385">Le navigateur attend le premier octet d’une réponse.</span><span class="sxs-lookup"><span data-stu-id="99b8a-385">The browser is waiting for the first byte of a response.</span></span>  <span data-ttu-id="99b8a-386">TTFB représente le temps à l’octet initial.</span><span class="sxs-lookup"><span data-stu-id="99b8a-386">TTFB stands for Time To First Byte.</span></span>  <span data-ttu-id="99b8a-387">Ce minutage inclut un aller-retour d’une latence et la durée du serveur pour préparer la réponse.</span><span class="sxs-lookup"><span data-stu-id="99b8a-387">This timing includes 1 round trip of latency and the time the server took to prepare the response.</span></span>  
*   <span data-ttu-id="99b8a-388">**Téléchargement du contenu**.</span><span class="sxs-lookup"><span data-stu-id="99b8a-388">**Content Download**.</span></span>  <span data-ttu-id="99b8a-389">Le navigateur reçoit la réponse.</span><span class="sxs-lookup"><span data-stu-id="99b8a-389">The browser is receiving the response.</span></span>  
*   <span data-ttu-id="99b8a-390">**Réception**d’une émission.</span><span class="sxs-lookup"><span data-stu-id="99b8a-390">**Receiving Push**.</span></span>  <span data-ttu-id="99b8a-391">Le navigateur reçoit des données pour cette réponse via le protocole HTTP/2 Server Poussée.</span><span class="sxs-lookup"><span data-stu-id="99b8a-391">The browser is receiving data for this response via HTTP/2 Server Push.</span></span>  
*   <span data-ttu-id="99b8a-392">**Lecture en lecture**.</span><span class="sxs-lookup"><span data-stu-id="99b8a-392">**Reading Push**.</span></span>  <span data-ttu-id="99b8a-393">Le navigateur lit les données locales précédemment reçues.</span><span class="sxs-lookup"><span data-stu-id="99b8a-393">The browser is reading the local data previously received.</span></span>  

### <span data-ttu-id="99b8a-394">Afficher les initiateurs et les dépendances</span><span class="sxs-lookup"><span data-stu-id="99b8a-394">View initiators and dependencies</span></span>  

<span data-ttu-id="99b8a-395">Pour afficher les initiateurs et les dépendances d’une requête, maintenez la touche enfoncée `Shift` et placez le pointeur sur la requête dans la table demandes.</span><span class="sxs-lookup"><span data-stu-id="99b8a-395">To view the initiators and dependencies of a request, hold `Shift`and hover over the request in the Requests table.</span></span>  <span data-ttu-id="99b8a-396">Couleurs de DevTools: les initiateurs apparaissent en vert et les dépendances apparaissent en rouge.</span><span class="sxs-lookup"><span data-stu-id="99b8a-396">DevTools colors: initiators are shown in green and dependencies are shown in red.</span></span>  

:::image type="complex" source="../media/network-network-resources-initiators-dependencies.msft.png" alt-text="Affichage des déclencheurs et des dépendances d’une requête" lightbox="../media/network-network-resources-initiators-dependencies.msft.png":::
   <span data-ttu-id="99b8a-398">Figure 26: affichage des déclencheurs et dépendances d’une requête</span><span class="sxs-lookup"><span data-stu-id="99b8a-398">Figure 26:  Viewing the initiators and dependencies of a request</span></span>  
:::image-end:::  

<span data-ttu-id="99b8a-399">Lorsque la table requêtes est classée dans un ordre chronologique, la première demande verte au-dessus de celle où vous pointez est l’initiateur de la dépendance.</span><span class="sxs-lookup"><span data-stu-id="99b8a-399">When the Requests table is ordered chronologically, the first green request above the one you are hovering is the initiator of the dependency.</span></span>  <span data-ttu-id="99b8a-400">Si une autre demande verte s’affiche au-dessus de celle-ci, il s’agit de l’initiateur de l’initiateur.</span><span class="sxs-lookup"><span data-stu-id="99b8a-400">If another green request appears above that, that higher request is the initiator of the initiator.</span></span>  <span data-ttu-id="99b8a-401">Et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="99b8a-401">And so on.</span></span>  

### <span data-ttu-id="99b8a-402">Afficher les événements de chargement</span><span class="sxs-lookup"><span data-stu-id="99b8a-402">View load events</span></span>  

<span data-ttu-id="99b8a-403">DevTools affiche le minutage des `DOMContentLoaded` événements et `load` dans plusieurs emplacements du panneau réseau.</span><span class="sxs-lookup"><span data-stu-id="99b8a-403">DevTools displays the timing of the `DOMContentLoaded` and `load` events in multiple places on the Network panel.</span></span>  <span data-ttu-id="99b8a-404">L' `DOMContentLoaded` événement est coloré en bleu et l' `load` événement est rouge.</span><span class="sxs-lookup"><span data-stu-id="99b8a-404">The `DOMContentLoaded` event is colored blue, and the `load` event is red.</span></span>  

:::image type="complex" source="../media/network-network-requests-load-events.msft.png" alt-text="Emplacements des événements DOMContentLoaded et Load sur le panneau réseau" lightbox="../media/network-network-requests-load-events.msft.png":::
   <span data-ttu-id="99b8a-406">Figure 27: emplacements des `DOMContentLoaded` `load` événements et sur le panneau réseau</span><span class="sxs-lookup"><span data-stu-id="99b8a-406">Figure 27:  The locations of the `DOMContentLoaded` and `load` events on the Network panel</span></span>  
:::image-end:::  

### <span data-ttu-id="99b8a-407">Afficher le nombre total de demandes</span><span class="sxs-lookup"><span data-stu-id="99b8a-407">View the total number of requests</span></span>  

<span data-ttu-id="99b8a-408">Le nombre total de demandes est répertorié dans le volet Résumé, au bas du panneau réseau.</span><span class="sxs-lookup"><span data-stu-id="99b8a-408">The total number of requests is listed in the Summary pane, at the bottom of the Network panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="99b8a-409">Ce numéro suit uniquement les requêtes qui ont été enregistrées depuis l’ouverture de DevTools.</span><span class="sxs-lookup"><span data-stu-id="99b8a-409">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="99b8a-410">Si d’autres requêtes s’est produites avant l’ouverture de DevTools, ces demandes ne sont pas comptabilisées.</span><span class="sxs-lookup"><span data-stu-id="99b8a-410">If other requests occurred before DevTools was opened, those requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-requests.msft.png" alt-text="Nombre total de demandes depuis l’ouverture de DevTools" lightbox="../media/network-network-total-requests.msft.png":::
   <span data-ttu-id="99b8a-412">Figure 28: nombre total de demandes depuis l’ouverture de DevTools</span><span class="sxs-lookup"><span data-stu-id="99b8a-412">Figure 28:  The total number of requests since DevTools was opened</span></span>  
:::image-end:::  

### <span data-ttu-id="99b8a-413">Affichez la taille totale du téléchargement</span><span class="sxs-lookup"><span data-stu-id="99b8a-413">View the total download size</span></span>  

<span data-ttu-id="99b8a-414">La taille de téléchargement totale des demandes figure dans le volet Résumé, en bas du volet réseau.</span><span class="sxs-lookup"><span data-stu-id="99b8a-414">The total download size of requests is listed in the Summary pane, at the bottom of the Network panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="99b8a-415">Ce numéro suit uniquement les requêtes qui ont été enregistrées depuis l’ouverture de DevTools.</span><span class="sxs-lookup"><span data-stu-id="99b8a-415">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="99b8a-416">Si d’autres requêtes s’est produites avant l’ouverture de DevTools, les requêtes précédentes ne sont pas comptabilisées.</span><span class="sxs-lookup"><span data-stu-id="99b8a-416">If other requests occurred before DevTools was opened, the previous requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-download-size.msft.png" alt-text="La taille de téléchargement totale des requêtes" lightbox="../media/network-network-total-download-size.msft.png":::
   <span data-ttu-id="99b8a-418">Figure 29: taille totale du téléchargement de demandes</span><span class="sxs-lookup"><span data-stu-id="99b8a-418">Figure 29:  The total download size of requests</span></span>  
:::image-end:::  

<span data-ttu-id="99b8a-419">Pour afficher [le nombre de ressources de taille décompressées, voir afficher la taille d’une ressource](#view-the-uncompressed-size-of-a-resource) , puis décompresser chaque élément.</span><span class="sxs-lookup"><span data-stu-id="99b8a-419">See [View the uncompressed size of a resource](#view-the-uncompressed-size-of-a-resource) to see how large resources are after the browser uncompresses each item.</span></span>  

### <span data-ttu-id="99b8a-420">Afficher la trace de pile ayant entraîné une requête</span><span class="sxs-lookup"><span data-stu-id="99b8a-420">View the stack trace that caused a request</span></span>  

<span data-ttu-id="99b8a-421">Après qu’une instruction JavaScript demande une ressource, placez le pointeur sur la colonne **Initiator** pour afficher la trace de pile qui se trouve au début de la requête.</span><span class="sxs-lookup"><span data-stu-id="99b8a-421">After a JavaScript statement requests a resource, hover over the **Initiator** column to view the stack trace leading up to the request.</span></span>  

<!-- [codepen.io/contoso/pen/yLBrOWa?editors=0010#0](https://codepen.io/contoso/pen/yLBrOWa?editors=0010#0) -->  

<!--
```javascript
function init() {
  getData();
}

function getData() {
  fetch('https:/httpbin.org/get?message=hi');
}

init();
```  
-->  

:::image type="complex" source="../media/network-network-requests-initiator-stack.msft.png" alt-text="Trace de pile aboutissant à une demande de ressources" lightbox="../media/network-network-requests-initiator-stack.msft.png":::
   <span data-ttu-id="99b8a-423">Figure 30: trace de pile aboutissant à une demande de ressources</span><span class="sxs-lookup"><span data-stu-id="99b8a-423">Figure 30:  The stack trace leading up to a resource request</span></span>  
:::image-end:::  

### <span data-ttu-id="99b8a-424">Affichage de la taille de la ressource non compressée</span><span class="sxs-lookup"><span data-stu-id="99b8a-424">View the uncompressed size of a resource</span></span>  

<span data-ttu-id="99b8a-425">Activez la case à cocher **utiliser des lignes de requête volumineuses** , puis examinez la valeur inférieure de la colonne **taille** .</span><span class="sxs-lookup"><span data-stu-id="99b8a-425">Select the **Use large request rows** checkbox and then look at the bottom value of the **Size** column.</span></span>  

:::image type="complex" source="../media/network-network-requests-uncompressed-compare.msft.png" alt-text="Exemple de ressources non compressées" lightbox="../media/network-network-requests-uncompressed-compare.msft.png":::
   <span data-ttu-id="99b8a-427">Figure 31: exemple de ressources non compressées \ (la taille du `jquery-3.3.1.min.js` fichier qui a été envoyée par le biais du réseau était `29.9 KB` , alors que la taille du fichier non compressé était de `84.9 KB` \)</span><span class="sxs-lookup"><span data-stu-id="99b8a-427">Figure 31:  An example of uncompressed resources  \(The compressed size of the `jquery-3.3.1.min.js` file that was sent over the network was `29.9 KB`, whereas the uncompressed size was `84.9 KB`\)</span></span>  
:::image-end:::  

## <span data-ttu-id="99b8a-428">Exporter les données de requête</span><span class="sxs-lookup"><span data-stu-id="99b8a-428">Export requests data</span></span>  

### <span data-ttu-id="99b8a-429">Enregistrer toutes les demandes réseau dans un fichier QAR</span><span class="sxs-lookup"><span data-stu-id="99b8a-429">Save all network requests to a HAR file</span></span>  

<span data-ttu-id="99b8a-430">Pour enregistrer toutes les demandes réseau dans un fichier QAR, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="99b8a-430">To save all network requests to a HAR file, complete the following steps.</span></span>  

1.  <span data-ttu-id="99b8a-431">Positionnez le pointeur sur une requête dans la table demandes et ouvrez le menu contextuel, puis cliquez sur le bouton droit de la souris.</span><span class="sxs-lookup"><span data-stu-id="99b8a-431">Hover on any request in the Requests table and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="99b8a-432">Sélectionnez **Save As QAR with content**.</span><span class="sxs-lookup"><span data-stu-id="99b8a-432">Select **Save as HAR with Content**.</span></span>  <span data-ttu-id="99b8a-433">DevTools enregistre toutes les demandes qui se sont produites depuis que vous avez ouvert DevTools sur le fichier.</span><span class="sxs-lookup"><span data-stu-id="99b8a-433">DevTools saves all requests that have occurred since you opened DevTools to the HAR file.</span></span>  <span data-ttu-id="99b8a-434">Il n’est pas possible de filtrer les demandes ou de n’enregistrer qu’une seule demande.</span><span class="sxs-lookup"><span data-stu-id="99b8a-434">There is no way to filter requests, or to save just a single request.</span></span>  

<span data-ttu-id="99b8a-435">Lorsque vous enregistrez un fichier QAR, vous pouvez l’importer de nouveau dans DevTools pour analyse.</span><span class="sxs-lookup"><span data-stu-id="99b8a-435">Once you save a HAR file, you may import it back into DevTools for analysis.</span></span>  <span data-ttu-id="99b8a-436">Il suffit de glisser-déplacer le fichier QAR dans la table demandes.</span><span class="sxs-lookup"><span data-stu-id="99b8a-436">Just drag-and-drop the HAR file into the Requests table.</span></span>  
<!--See also [HAR Analyzer][HARAnalyzer].  -->  

<!--[HARAnalyzer]: https://toolbox.alphabetapps.com/apps/har_analyzer  -->  
<!--Todo: add section link when content is available  -->  

:::image type="complex" source="../media/network-network-requests-save-har-content.msft.png" alt-text="Sélection de l’option Enregistrer sous le contenu de votre fichier" lightbox="../media/network-network-requests-save-har-content.msft.png":::
   <span data-ttu-id="99b8a-438">Figure 32: sélection **de l’option Enregistrer sous le contenu de votre fichier** .</span><span class="sxs-lookup"><span data-stu-id="99b8a-438">Figure 32:  Selecting **Save as HAR with Content**</span></span>  
:::image-end:::  

### <span data-ttu-id="99b8a-439">Copier une ou plusieurs demandes dans le presse-papiers</span><span class="sxs-lookup"><span data-stu-id="99b8a-439">Copy one or more requests to the clipboard</span></span>  

<span data-ttu-id="99b8a-440">Dans la colonne **nom** de la table demandes, positionnez le pointeur sur une requête, ouvrez le menu contextuel **, puis**sélectionnez l’une des options suivantes...</span><span class="sxs-lookup"><span data-stu-id="99b8a-440">Under the **Name** column of the Requests table, hover on a request, open the contextual menu \(right-click\), hover over **Copy**, and select one of the following options.</span></span>  

*   <span data-ttu-id="99b8a-441">**Copier l’adresse du lien**.</span><span class="sxs-lookup"><span data-stu-id="99b8a-441">**Copy Link Address**.</span></span>  <span data-ttu-id="99b8a-442">Copiez l’URL de la requête dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="99b8a-442">Copy the URL of the request to the clipboard.</span></span>  
*   <span data-ttu-id="99b8a-443">**Copier la réponse**.</span><span class="sxs-lookup"><span data-stu-id="99b8a-443">**Copy Response**.</span></span>  <span data-ttu-id="99b8a-444">Copiez le corps de la réponse dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="99b8a-444">Copy the response body to the clipboard.</span></span>  
*   <span data-ttu-id="99b8a-445">**Copy As FETCH**.</span><span class="sxs-lookup"><span data-stu-id="99b8a-445">**Copy as Fetch**.</span></span>  
*   <span data-ttu-id="99b8a-446">**Copier comme courbe**.</span><span class="sxs-lookup"><span data-stu-id="99b8a-446">**Copy as cURL**.</span></span>  <span data-ttu-id="99b8a-447">Copiez la demande en tant que commande en forme de boucle.</span><span class="sxs-lookup"><span data-stu-id="99b8a-447">Copy the request as a cURL command.</span></span>  
*   <span data-ttu-id="99b8a-448">**Copy All As FETCH**.</span><span class="sxs-lookup"><span data-stu-id="99b8a-448">**Copy All as Fetch**.</span></span>  
*   <span data-ttu-id="99b8a-449">**Tout copier comme courbe**.</span><span class="sxs-lookup"><span data-stu-id="99b8a-449">**Copy All as cURL**.</span></span>  <span data-ttu-id="99b8a-450">Copiez toutes les demandes comme une chaîne de commandes bouclé.</span><span class="sxs-lookup"><span data-stu-id="99b8a-450">Copy all requests as a chain of cURL commands.</span></span>  
*   <span data-ttu-id="99b8a-451">**Copy All As QAR**.</span><span class="sxs-lookup"><span data-stu-id="99b8a-451">**Copy All as HAR**.</span></span>  <span data-ttu-id="99b8a-452">Copiez toutes les demandes en tant que données QAR.</span><span class="sxs-lookup"><span data-stu-id="99b8a-452">Copy all requests as HAR data.</span></span>  

:::image type="complex" source="../media/network-network-requests-copy-response.msft.png" alt-text="Sélection de l’option copier la réponse" lightbox="../media/network-network-requests-copy-response.msft.png":::
   <span data-ttu-id="99b8a-454">Figure 33: sélection de l’option **copier la réponse**</span><span class="sxs-lookup"><span data-stu-id="99b8a-454">Figure 33:  Selecting **Copy Response**</span></span>  
:::image-end:::  

## <span data-ttu-id="99b8a-455">Modifier la disposition du panneau réseau</span><span class="sxs-lookup"><span data-stu-id="99b8a-455">Change the layout of the Network panel</span></span>  

<span data-ttu-id="99b8a-456">Vous pouvez développer ou réduire des sections de l’interface utilisateur du panneau réseau pour cibler les informations importantes.</span><span class="sxs-lookup"><span data-stu-id="99b8a-456">You may expand or collapse sections of the Network panel UI to focus important information.</span></span>  

### <span data-ttu-id="99b8a-457">Masquer le volet filtres</span><span class="sxs-lookup"><span data-stu-id="99b8a-457">Hide the Filters pane</span></span>  

<span data-ttu-id="99b8a-458">Par défaut, DevTools affiche le **volet filtres**.</span><span class="sxs-lookup"><span data-stu-id="99b8a-458">By default, DevTools shows the **Filters pane**.</span></span>  
<span data-ttu-id="99b8a-459">Sélectionnez **Filter** ![ filtre ][ImageFilterIcon] de filtre pour le masquer.</span><span class="sxs-lookup"><span data-stu-id="99b8a-459">Select **Filter** ![Filter][ImageFilterIcon] to hide it.</span></span>  

:::image type="complex" source="../media/network-network-resources-hide-filters-button.msft.png" alt-text="Bouton Masquer les filtres" lightbox="../media/network-network-resources-hide-filters-button.msft.png":::
   <span data-ttu-id="99b8a-461">Figure 34: bouton Masquer les filtres</span><span class="sxs-lookup"><span data-stu-id="99b8a-461">Figure 34:  The Hide Filters button</span></span>  
:::image-end:::  

### <span data-ttu-id="99b8a-462">Utiliser des lignes de requête volumineuses</span><span class="sxs-lookup"><span data-stu-id="99b8a-462">Use large request rows</span></span>  

<span data-ttu-id="99b8a-463">Utilisez des lignes de grande taille si vous voulez plus d’espace dans votre tableau de requêtes réseau.</span><span class="sxs-lookup"><span data-stu-id="99b8a-463">Use large rows when you want more whitespace in your network requests table.</span></span>  <span data-ttu-id="99b8a-464">Certaines colonnes fournissent également quelques informations supplémentaires sur l’utilisation de lignes de grande taille.</span><span class="sxs-lookup"><span data-stu-id="99b8a-464">Some columns also provide a little more information when using large rows.</span></span>  <span data-ttu-id="99b8a-465">Par exemple, la valeur la plus en bas de la colonne **taille** correspond à la taille de requête non compressée.</span><span class="sxs-lookup"><span data-stu-id="99b8a-465">For example, the bottom value of the **Size** column is the uncompressed size of a request.</span></span>  

:::image type="complex" source="../media/network-network-requests-large-request-rows.msft.png" alt-text="Exemple de longues lignes de requête dans le volet requêtes" lightbox="../media/network-network-requests-large-request-rows.msft.png":::
   <span data-ttu-id="99b8a-467">Figure 35: exemple de longues lignes de requête dans le volet **requêtes**</span><span class="sxs-lookup"><span data-stu-id="99b8a-467">Figure 35:  An example of large request rows in the **Requests** pane</span></span>  
:::image-end:::  

<span data-ttu-id="99b8a-468">Activez la case à cocher **utiliser des lignes de requête volumineuses** pour activer les lignes de grande taille.</span><span class="sxs-lookup"><span data-stu-id="99b8a-468">Select the **Use large request rows** checkbox to enable large rows.</span></span>  

:::image type="complex" source="../media/network-network-requests-use-large-request-rows-on.msft.png" alt-text="Case à cocher utiliser de grandes lignes de requête" lightbox="../media/network-network-requests-use-large-request-rows-on.msft.png":::
   <span data-ttu-id="99b8a-470">Figure 36: case à cocher **utiliser des lignes de requête volumineuses**</span><span class="sxs-lookup"><span data-stu-id="99b8a-470">Figure 36:  The **Use large request rows** checkbox</span></span>  
:::image-end:::  

### <span data-ttu-id="99b8a-471">Masquer le volet vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="99b8a-471">Hide the Overview pane</span></span>  

<span data-ttu-id="99b8a-472">Par défaut, DevTools affiche le **volet vue d’ensemble**.</span><span class="sxs-lookup"><span data-stu-id="99b8a-472">By default, DevTools shows the **Overview pane**.</span></span>  <span data-ttu-id="99b8a-473">Désélectionnez la case à cocher **afficher la vue d’ensemble** pour la masquer.</span><span class="sxs-lookup"><span data-stu-id="99b8a-473">Deselect the **Show Overview** checkbox to hide it.</span></span>  

:::image type="complex" source="../media/network-network-requests-show-overview-off.msft.png" alt-text="Case à cocher Afficher la vue d’ensemble" lightbox="../media/network-network-requests-show-overview-off.msft.png":::
   <span data-ttu-id="99b8a-475">Figure 37: case à cocher **afficher la vue d’ensemble**</span><span class="sxs-lookup"><span data-stu-id="99b8a-475">Figure 37:  The **Show Overview** checkbox</span></span>  
:::image-end:::  

<!-- image links -->  

[ImageCaptureScreenshotsIcon]: ../media/capture-screenshots-icon.msft.png  
[ImageClearIcon]: ../media/clear-requests-icon.msft.png  
[ImageFilterIcon]: ../media/filter-icon.msft.png  
[ImageHideIcon]: ../media/hide-overview-icon.msft.png  
[ImageLargeResourceRowsIcon]: ../media/large-resource-rows-button-icon.msft.png  
[ImageRecordOnIcon]: ../media/record-on-icon.msft.png  

<!-- links -->  

[DevtoolsProgressiveWebApps]: /microsoft-edge/devtools-guide-chromium/network/progressive-web-apps "Déboguer des applications Web progressives"  

<!--[NetworkConditions]: /microsoft-edge/devtools-guide-chromium/network/network-conditions "Optimize Performance Under Varying Network Conditions"  -->  

[MDNHTTPDataURIs]: https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/Data_URIs "URL de données | MDN"  

[WikiProxyServer]: https://en.wikipedia.org/wiki/Proxy_server "Serveur proxy-Wikipédia"  

> [!NOTE]
> <span data-ttu-id="99b8a-479">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="99b8a-479">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="99b8a-480">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/network/reference) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="99b8a-480">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="99b8a-482">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="99b8a-482">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
