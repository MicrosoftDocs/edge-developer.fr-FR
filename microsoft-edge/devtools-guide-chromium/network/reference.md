---
title: Référence d’analyse du réseau
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: c9d205fb2cc478e9c3f20458f461f004035e85e8
ms.sourcegitcommit: a34858dd3260967ba9699842fa839c7a94775fe4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/12/2020
ms.locfileid: "10710398"
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

# <span data-ttu-id="9f3cd-103">Référence d’analyse du réseau</span><span class="sxs-lookup"><span data-stu-id="9f3cd-103">Network Analysis Reference</span></span>  

<span data-ttu-id="9f3cd-104">Découvrez de nouvelles façons d’analyser le chargement de votre page dans cette référence complète des fonctionnalités d’analyse du réseau Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-104">Discover new ways to analyze how your page loads in this comprehensive reference of Microsoft Edge DevTools network analysis features.</span></span>  

<!--
> [!NOTE]
> This reference is based on Microsoft Edge 58.  If you use another version of Microsoft Edge, the UI, and features of DevTools may be different.  Check `edge://help` to see what version of Microsoft Edge you are running.  
-->

## <span data-ttu-id="9f3cd-105">Enregistrer les requêtes réseau</span><span class="sxs-lookup"><span data-stu-id="9f3cd-105">Record network requests</span></span>  

<span data-ttu-id="9f3cd-106">Par défaut, DevTools enregistre toutes les requêtes réseau dans le panneau réseau, tant que DevTools est ouvert.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-106">By default, DevTools records all network requests in the Network panel, so long as DevTools is open.</span></span>  

:::image type="complex" source="../media/network-network-panel.msft.png" alt-text="Panneau réseau" lightbox="../media/network-network-panel.msft.png":::
   <span data-ttu-id="9f3cd-108">Figure 1: panneau **réseau**</span><span class="sxs-lookup"><span data-stu-id="9f3cd-108">Figure 1:  The **Network** panel</span></span>  
:::image-end:::  

### <span data-ttu-id="9f3cd-109">Arrêter l’enregistrement des requêtes réseau</span><span class="sxs-lookup"><span data-stu-id="9f3cd-109">Stop recording network requests</span></span>  

<span data-ttu-id="9f3cd-110">Pour arrêter l’enregistrement de demandes, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-110">To stop recording requests, complete the following steps.</span></span>  

1.  <span data-ttu-id="9f3cd-111">Pour arrêter l' **enregistrement du journal du réseau** , cliquez sur arrêter l' ![ enregistrement réseau ][ImageRecordOnIcon] dans le panneau **réseau** .</span><span class="sxs-lookup"><span data-stu-id="9f3cd-111">Select **Stop recording network log** ![Stop recording network log][ImageRecordOnIcon] on the **Network** panel.</span></span>  <span data-ttu-id="9f3cd-112">Il devient gris pour indiquer que DevTools n’enregistre plus les demandes.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-112">It turns grey to indicate that DevTools is no longer recording requests.</span></span>  
1.  <span data-ttu-id="9f3cd-113">Appuyez sur `Control` + `E` \ (Windows \) ou `Command` + `E` \ (MacOS \) lorsque le panneau **réseau** a le focus.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-113">Press `Control`+`E` \(Windows\) or `Command`+`E` \(macOS\) while the **Network** panel is in focus.</span></span>  

### <span data-ttu-id="9f3cd-114">Supprimer des demandes</span><span class="sxs-lookup"><span data-stu-id="9f3cd-114">Clear requests</span></span>  

<span data-ttu-id="9f3cd-115">Sélectionnez **Effacer** ![ ][ImageClearIcon] le panneau réseau pour effacer toutes les demandes de la table demandes.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-115">Select **Clear** ![Clear][ImageClearIcon] on the Network panel to clear all requests from the Requests table.</span></span>  

:::image type="complex" source="../media/network-network-clear-button.msft.png" alt-text="Bouton Effacer" lightbox="../media/network-network-clear-button.msft.png":::
   <span data-ttu-id="9f3cd-117">Figure 2: bouton **Effacer**</span><span class="sxs-lookup"><span data-stu-id="9f3cd-117">Figure 2:  The **Clear** button</span></span>  
:::image-end:::  

### <span data-ttu-id="9f3cd-118">Enregistrer les demandes lors du chargement de la page</span><span class="sxs-lookup"><span data-stu-id="9f3cd-118">Save requests across page loads</span></span>  

<span data-ttu-id="9f3cd-119">Pour enregistrer les demandes lors du chargement de la page, activez la case à cocher **conservation du journal** dans le panneau réseau.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-119">To save requests across page loads, check the **Preserve log** checkbox on the Network panel.</span></span>  <span data-ttu-id="9f3cd-120">DevTools enregistre toutes les demandes jusqu’à ce que vous désactiviez le **Journal de conservation**.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-120">DevTools saves all requests until you disable **Preserve log**.</span></span>  

:::image type="complex" source="../media/network-network-preserve-log.msft.png" alt-text="Case à cocher conserver le journal" lightbox="../media/network-network-preserve-log.msft.png":::
   <span data-ttu-id="9f3cd-122">Figure 3: case à cocher **conserver le journal**</span><span class="sxs-lookup"><span data-stu-id="9f3cd-122">Figure 3:  The **Preserve Log** checkbox</span></span>  
:::image-end:::  

### <span data-ttu-id="9f3cd-123">Capture de captures d’écran pendant le chargement de la page</span><span class="sxs-lookup"><span data-stu-id="9f3cd-123">Capture screenshots during page load</span></span>  

<span data-ttu-id="9f3cd-124">Capture des captures d’écran pour analyser ce que les utilisateurs voient lorsqu’ils attendent que votre page se charge.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-124">Capture screenshots to analyze what users see as they wait for your page to load.</span></span>  

<span data-ttu-id="9f3cd-125">Pour activer les captures d’écran, sélectionnez **paramètres du réseau** , puis cochez la case **capturer les captures d’écran** dans le panneau **réseau** .</span><span class="sxs-lookup"><span data-stu-id="9f3cd-125">To enable screenshots, select **Network settings** and select **Capture screenshots** checkbox on the **Network** panel.</span></span>  

<span data-ttu-id="9f3cd-126">Actualisez la page lorsque le panneau **réseau** a le focus pour capturer les captures d’écran.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-126">Refresh the page while the **Network** panel is in focus to capture screenshots.</span></span>  

<span data-ttu-id="9f3cd-127">Après avoir capturé une capture d’écran, vous interagissez comme suit.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-127">After capturing a screenshot, you interact with it in the following ways.</span></span>  

*   <span data-ttu-id="9f3cd-128">Placez le pointeur de la souris sur une capture d’écran pour afficher le point d’acquisition de cette capture d’écran.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-128">Hover over a screenshot to view the point at which that screenshot was captured.</span></span>  <span data-ttu-id="9f3cd-129">Une ligne jaune apparaît dans le volet **vue d’ensemble** .</span><span class="sxs-lookup"><span data-stu-id="9f3cd-129">A yellow line appears on the **Overview** pane.</span></span>  
*   <span data-ttu-id="9f3cd-130">Sélectionnez la miniature d’un écran pour filtrer toutes les demandes qui se sont produites après la capture de la capture d’écran.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-130">Select the thumbnail of a screen to filter out any requests that occurred after the screenshot was captured.</span></span>  
*   <span data-ttu-id="9f3cd-131">Double-cliquez sur une miniature pour y effectuer un zoom.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-131">Double-click a thumbnail to zoom into it.</span></span>  

:::image type="complex" source="../media/network-network-screenshot-hover.msft.png" alt-text="Survol d’une capture d’écran" lightbox="../media/network-network-screenshot-hover.msft.png":::
   <span data-ttu-id="9f3cd-133">Figure 4: survol d’une capture d’écran</span><span class="sxs-lookup"><span data-stu-id="9f3cd-133">Figure 4:  Hovering over a screenshot</span></span>  
:::image-end:::  

<!--  ### Replay XHR request  -->

<!--  To replay an XHR request, hover on the request in the Requests table, open the contextual menu \(right-click\), and select **Replay XHR**.  -->

<!--  
:::image type="complex" source="../media/network-replay-xhr.msft.png" alt-text="Selecting Replay XHR" lightbox="../media/network-replay-xhr.msft.png":::
   Old Figure 5:  Selecting Replay XHR  
:::image-end:::  
-->  

## <span data-ttu-id="9f3cd-134">Changer le comportement de chargement</span><span class="sxs-lookup"><span data-stu-id="9f3cd-134">Change loading behavior</span></span>  

### <span data-ttu-id="9f3cd-135">Émuler un visiteur pour la première fois en désactivant le cache du navigateur</span><span class="sxs-lookup"><span data-stu-id="9f3cd-135">Emulate a first-time visitor by disabling the browser cache</span></span>  

<span data-ttu-id="9f3cd-136">Pour émuler la façon dont un utilisateur a expériences de votre site pour la première fois, activez la case à cocher **désactiver le cache** .</span><span class="sxs-lookup"><span data-stu-id="9f3cd-136">To emulate how a first-time user experiences your site, check the **Disable cache** checkbox.</span></span>  <span data-ttu-id="9f3cd-137">DevTools désactive le cache du navigateur.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-137">DevTools disables the browser cache.</span></span>  <span data-ttu-id="9f3cd-138">Cela a pour effet d’émuler de façon plus précise une première utilisation de l’utilisateur, car les requêtes sont servies dans le cache du navigateur sur les visites répétées.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-138">This more accurately emulates a first-time user's experience, because requests are served from the browser cache on repeat visits.</span></span>  

:::image type="complex" source="../media/network-network-disable-cache-checkbox.msft.png" alt-text="Case à cocher Désactiver le cache" lightbox="../media/network-network-disable-cache-checkbox.msft.png":::
   <span data-ttu-id="9f3cd-140">Figure 5: case à cocher **désactiver le cache**</span><span class="sxs-lookup"><span data-stu-id="9f3cd-140">Figure 5:  The **Disable Cache** checkbox</span></span>  
:::image-end:::  

#### <span data-ttu-id="9f3cd-141">Désactiver le cache du navigateur dans le tiroir du réseau</span><span class="sxs-lookup"><span data-stu-id="9f3cd-141">Disable the browser cache from the Network Conditions drawer</span></span>  

<span data-ttu-id="9f3cd-142">Si vous voulez désactiver le cache lorsque vous travaillez dans d’autres panneaux DevTools, utilisez le tiroir de l’état du réseau.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-142">If you want to disable the cache while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="9f3cd-143">Ouvrez le tiroir de **conditions du réseau** .</span><span class="sxs-lookup"><span data-stu-id="9f3cd-143">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="9f3cd-144">Cochez ou décochez la case **désactiver le cache** .</span><span class="sxs-lookup"><span data-stu-id="9f3cd-144">Check or uncheck the **Disable cache** checkbox.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="9f3cd-145">Vider manuellement le cache du navigateur</span><span class="sxs-lookup"><span data-stu-id="9f3cd-145">Manually clear the browser cache</span></span>  

<span data-ttu-id="9f3cd-146">Pour vider manuellement le cache du navigateur à tout moment, ouvrez le menu contextuel (cliquez avec le bouton droit sur \) n’importe où dans la table demandes et sélectionnez **Vider le cache du navigateur**.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-146">To manually clear the browser cache at any time, open the contextual menu \(right-click\) anywhere in the Requests table and select **Clear Browser Cache**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cache.msft.png" alt-text="Sélection de l’option vider le cache du navigateur" lightbox="../media/network-network-clear-browser-cache.msft.png":::
   <span data-ttu-id="9f3cd-148">Figure 6: sélectionner **Vider le cache du navigateur**</span><span class="sxs-lookup"><span data-stu-id="9f3cd-148">Figure 6:  Selecting **Clear Browser Cache**</span></span>  
:::image-end:::  

### <span data-ttu-id="9f3cd-149">Émuler hors connexion</span><span class="sxs-lookup"><span data-stu-id="9f3cd-149">Emulate offline</span></span>  

<span data-ttu-id="9f3cd-150">Une nouvelle classe d’applications Web, appelées [applications Web progressives][DevtoolsProgressiveWebApps], fonctionne en mode hors connexion avec l’aide des **travailleurs de service**.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-150">A new class of web apps, named [Progressive Web Apps][DevtoolsProgressiveWebApps], functions offline with the help of **service workers**.</span></span>  <span data-ttu-id="9f3cd-151">Vous constaterez peut-être qu’il est utile de simuler rapidement un appareil dépourvu de connexion aux données lors de la création de ce type d’application.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-151">You may find it useful to quickly simulate a device that has no data connection when you are building this type of app.</span></span>  

<!--[ServiceWorkers]: /web/fundamentals/getting-started/primers/service-workers  -->

<span data-ttu-id="9f3cd-152">Sélectionnez le menu déroulant **en ligne** , Rechercher sous **présélections**, puis sélectionnez **hors ligne** pour simuler une interface réseau entièrement hors connexion.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-152">Select the **Online** dropdown menu, search under **Presets**, and select **Offline** to simulate a completely offline network experience.</span></span>  

:::image type="complex" source="../media/network-network-offline-dropdown.msft.png" alt-text="Menu déroulant hors connexion" lightbox="../media/network-network-offline-dropdown.msft.png":::
   <span data-ttu-id="9f3cd-154">Figure 7: menu déroulant **hors connexion**</span><span class="sxs-lookup"><span data-stu-id="9f3cd-154">Figure 7:  The **Offline** dropdown menu</span></span>  
:::image-end:::  

### <span data-ttu-id="9f3cd-155">Émuler une connexion réseau lente</span><span class="sxs-lookup"><span data-stu-id="9f3cd-155">Emulate slow network connections</span></span>  

<span data-ttu-id="9f3cd-156">Émulez des vitesses de connexion 3G, Fast 3G et autres vitesses de connexion dans le menu déroulant **en ligne** .</span><span class="sxs-lookup"><span data-stu-id="9f3cd-156">Emulate Slow 3G, Fast 3G, and other connection speeds from the **Online** dropdown menu.</span></span>  

:::image type="complex" source="../media/network-network-throttling-menu.msft.png" alt-text="Menu déroulant limitation" lightbox="../media/network-network-throttling-menu.msft.png":::
   <span data-ttu-id="9f3cd-158">Figure 8: menu déroulant **limitation**</span><span class="sxs-lookup"><span data-stu-id="9f3cd-158">Figure 8:  The **Throttling** dropdown menu</span></span>  
:::image-end:::  

<span data-ttu-id="9f3cd-159">Vous pouvez faire votre choix parmi une série de présélections, par exemple, lente 3G ou Fast 3G.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-159">You may select from a variety of presets, such as Slow 3G or Fast 3G.</span></span>  <span data-ttu-id="9f3cd-160">Vous pouvez également ajouter vos propres Présélections personnalisées en ouvrant le menu limitation et **Custom**en sélectionnant  >  **Ajouter**personnalisé.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-160">You may also add your own custom presets by opening the Throttling menu and selecting **Custom** > **Add**.</span></span>  

<span data-ttu-id="9f3cd-161">DevTools affiche une icône d’avertissement en regard de l’onglet **réseau** pour vous rappeler que la limitation est activée.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-161">DevTools displays a warning icon next to the **Network** tab to remind you that throttling is enabled.</span></span>  

#### <span data-ttu-id="9f3cd-162">Émuler une connexion réseau lente à partir du tiroir du réseau</span><span class="sxs-lookup"><span data-stu-id="9f3cd-162">Emulate slow network connections from the Network Conditions drawer</span></span>  

<span data-ttu-id="9f3cd-163">Si vous souhaitez limiter la connexion réseau lorsque vous travaillez dans d’autres panneaux DevTools, utilisez le tiroir de l’état du réseau.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-163">If you want to throttle the network connection while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="9f3cd-164">Ouvrez le tiroir de **conditions du réseau** .</span><span class="sxs-lookup"><span data-stu-id="9f3cd-164">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="9f3cd-165">Sélectionnez le débit de connexion souhaité dans le menu **limitation** .</span><span class="sxs-lookup"><span data-stu-id="9f3cd-165">Select your desired connection speed from the **Throttling** menu.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="9f3cd-166">Effacement manuel des cookies du navigateur</span><span class="sxs-lookup"><span data-stu-id="9f3cd-166">Manually clear browser cookies</span></span>  

<span data-ttu-id="9f3cd-167">Pour effacer manuellement les cookies du navigateur à tout moment, ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \) n’importe où dans la table demandes, puis sélectionnez **effacer les cookies du navigateur**.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-167">To manually clear browser cookies at any time, open the contextual menu \(right-click\) anywhere in the Requests table and select **Clear Browser Cookies**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cookies.msft.png" alt-text="Sélection effacer les cookies du navigateur" lightbox="../media/network-network-clear-browser-cookies.msft.png":::
   <span data-ttu-id="9f3cd-169">Figure 9: sélectionnez **effacer les cookies du navigateur**</span><span class="sxs-lookup"><span data-stu-id="9f3cd-169">Figure 9:  Selecting **Clear Browser Cookies**</span></span>  
:::image-end:::  

### <span data-ttu-id="9f3cd-170">Remplacer l’agent utilisateur</span><span class="sxs-lookup"><span data-stu-id="9f3cd-170">Override the user agent</span></span>  

<span data-ttu-id="9f3cd-171">Pour remplacer manuellement l’agent utilisateur, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="9f3cd-171">To manually override the user agent:</span></span>  

1.  <span data-ttu-id="9f3cd-172">Ouvrez le tiroir de **conditions du réseau** .</span><span class="sxs-lookup"><span data-stu-id="9f3cd-172">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="9f3cd-173">Décochez l' **option sélectionner automatiquement**.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-173">Uncheck **Select automatically**.</span></span>  
1.  <span data-ttu-id="9f3cd-174">Choisissez une option de l’agent utilisateur dans le menu ou entrez-en un dans la zone de texte.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-174">Choose a user agent option from the menu, or enter a custom one in the text box.</span></span>  

<!--todo: add network condition section when available -->  

## <span data-ttu-id="9f3cd-175">Demandes de filtre</span><span class="sxs-lookup"><span data-stu-id="9f3cd-175">Filter requests</span></span>  

### <span data-ttu-id="9f3cd-176">Filtrer les demandes par propriétés</span><span class="sxs-lookup"><span data-stu-id="9f3cd-176">Filter requests by properties</span></span>  

<span data-ttu-id="9f3cd-177">Utilisez la zone de texte **filtre** pour filtrer les demandes par propriétés, telles que le domaine ou la taille de la requête.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-177">Use the **Filter** text box to filter requests by properties, such as the domain or size of the request.</span></span>  

<span data-ttu-id="9f3cd-178">Si vous ne voyez pas la zone de texte, le volet filtres est probablement masqué.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-178">If you do not see the text box, the Filters pane is probably hidden.</span></span>  
<span data-ttu-id="9f3cd-179">Voir [masquer le volet filtres](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="9f3cd-179">See [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

:::image type="complex" source="../media/network-network-filters-textbox.msft.png" alt-text="Zone de texte filtre" lightbox="../media/network-network-filters-textbox.msft.png":::
   <span data-ttu-id="9f3cd-181">Figure 10: zone de texte de **filtre**</span><span class="sxs-lookup"><span data-stu-id="9f3cd-181">Figure 10:  The **Filter** text box</span></span>  
:::image-end:::  

<span data-ttu-id="9f3cd-182">Vous pouvez utiliser plusieurs propriétés simultanément en séparant chaque propriété d’un espace.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-182">You may use multiple properties simultaneously by separating each property with a space.</span></span>  <span data-ttu-id="9f3cd-183">Par exemple, `mime-type:image/png larger-than:1K` affiche tous les png dont la taille est supérieure à 1 Ko.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-183">For example, `mime-type:image/png larger-than:1K` displays all PNGs that are larger than one kilobyte.</span></span>  <span data-ttu-id="9f3cd-184">Ces filtres multi-propriété sont équivalents aux `AND` opérations.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-184">These multi-property filters are equivalent to `AND` operations.</span></span>  `OR` <span data-ttu-id="9f3cd-185">les opérations ne sont actuellement pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-185">operations are currently not supported.</span></span>  

<span data-ttu-id="9f3cd-186">Liste complète des propriétés prises en charge.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-186">The complete list of supported properties.</span></span>  

| <span data-ttu-id="9f3cd-187">Propriété</span><span class="sxs-lookup"><span data-stu-id="9f3cd-187">Property</span></span> | <span data-ttu-id="9f3cd-188">Détails</span><span class="sxs-lookup"><span data-stu-id="9f3cd-188">Details</span></span> |  
|:--- | :--- |  
| `domain` | <span data-ttu-id="9f3cd-189">Afficher uniquement les ressources du domaine spécifié.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-189">Only display resources from the specified domain.</span></span>  <span data-ttu-id="9f3cd-190">Vous pouvez utiliser un caractère générique \ ( `*` \) pour inclure plusieurs domaines.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-190">You may use a wildcard character \(`*`\) to include multiple domains.</span></span>  <span data-ttu-id="9f3cd-191">Par exemple, `*.com` affiche les ressources de tous les noms de domaine se terminant par `.com` .</span><span class="sxs-lookup"><span data-stu-id="9f3cd-191">For example, `*.com` displays resources from all domain names ending in `.com`.</span></span>  <span data-ttu-id="9f3cd-192">DevTools remplit le menu déroulant de saisie semi-automatique avec tous les domaines qu’il a rencontré.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-192">DevTools populates the autocomplete dropdown menu with all of the domains it has encountered.</span></span> |  
| `has-response-header` | <span data-ttu-id="9f3cd-193">Afficher les ressources qui contiennent l’en-tête de réponse HTTP spécifié.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-193">Show the resources that contain the specified HTTP response header.</span></span>  <span data-ttu-id="9f3cd-194">DevTools remplit la liste déroulante de saisie semi-automatique avec tous les en-têtes de réponse qu’il a rencontré.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-194">DevTools populates the autocomplete dropdown with all of the response headers that it has encountered.</span></span> |  
| `is` | <span data-ttu-id="9f3cd-195">Utiliser `is:running` pour rechercher des `WebSocket` ressources.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-195">Use `is:running` to find `WebSocket` resources.</span></span> |  
| `larger-than` | <span data-ttu-id="9f3cd-196">Afficher les ressources dont la taille est supérieure à la taille spécifiée, en octets.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-196">Show resources that are larger than the specified size, in bytes.</span></span>  <span data-ttu-id="9f3cd-197">La définition d’une valeur est égale à la valeur `1000` `1k` .</span><span class="sxs-lookup"><span data-stu-id="9f3cd-197">Setting a value of `1000` is equivalent to setting a value of `1k`.</span></span> |  
| `method` | <span data-ttu-id="9f3cd-198">Afficher les ressources récupérées sur un type de méthode HTTP spécifié.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-198">Show resources that were retrieved over a specified HTTP method type.</span></span>  <span data-ttu-id="9f3cd-199">DevTools remplit la liste déroulante avec toutes les méthodes HTTP qu’il a rencontrées.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-199">DevTools populates the dropdown with all of the HTTP methods it has encountered.</span></span> |  
| `mime-type` | <span data-ttu-id="9f3cd-200">Afficher les ressources d’un type MIME spécifié.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-200">Show resources of a specified MIME type.</span></span>  <span data-ttu-id="9f3cd-201">DevTools remplit la liste déroulante avec tous les types MIME qu’il a rencontré.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-201">DevTools populates the dropdown with all MIME types it has encountered.</span></span> |  
| `mixed-content` | <span data-ttu-id="9f3cd-202">Affichez toutes les ressources de contenu mixte \ ( `mixed-content:all` \) ou uniquement celles actuellement affichées \ ( `mixed-content:displayed` \).</span><span class="sxs-lookup"><span data-stu-id="9f3cd-202">Show all mixed content resources \(`mixed-content:all`\) or just the ones that are currently displayed \(`mixed-content:displayed`\).</span></span> |  
| `scheme` | <span data-ttu-id="9f3cd-203">Afficher les ressources récupérées sur une connexion HTTP \ ( `scheme:http` \) ou protégé https \ ( `scheme:https` \).</span><span class="sxs-lookup"><span data-stu-id="9f3cd-203">Show resources retrieved over unprotected HTTP \(`scheme:http`\) or protected HTTPS \(`scheme:https`\).</span></span> |  
| `set-cookie-domain` | <span data-ttu-id="9f3cd-204">Afficher les ressources qui ont un `Set-Cookie` en-tête avec un `Domain` attribut qui correspond à la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-204">Show the resources that have a `Set-Cookie` header with a `Domain` attribute that matches the specified value.</span></span>  <span data-ttu-id="9f3cd-205">DevTools remplit la saisie semi-automatique avec tous les domaines de cookie qu’il a rencontré.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-205">DevTools populates the autocomplete with all of the cookie domains that it has encountered.</span></span> |  
| `set-cookie-name` | <span data-ttu-id="9f3cd-206">Afficher les ressources possédant un `Set-Cookie` en-tête dont le nom correspond à la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-206">Show the resources that have a `Set-Cookie` header with a name that matches the specified value.</span></span>  <span data-ttu-id="9f3cd-207">DevTools remplit la saisie semi-automatique avec tous les noms de cookie qu’il a rencontré.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-207">DevTools populates the autocomplete with all of the cookie names that it has encountered.</span></span> |  
| `set-cookie-value` | <span data-ttu-id="9f3cd-208">Afficher les ressources dont l' `Set-Cookie` en-tête comporte une valeur qui correspond à la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-208">Show the resources that have a `Set-Cookie` header with a value that matches the specified value.</span></span>  <span data-ttu-id="9f3cd-209">DevTools remplit la saisie semi-automatique avec toutes les valeurs de cookie qu’il a rencontrées.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-209">DevTools populates the autocomplete with all of the cookie values that it has encountered.</span></span> |  
| `status-code` | <span data-ttu-id="9f3cd-210">Afficher uniquement les ressources pour lesquelles le code d’état HTTP correspond au code spécifié.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-210">Show only the resources for which the HTTP status code matches the specified code.</span></span>  <span data-ttu-id="9f3cd-211">DevTools remplit le menu déroulant de saisie semi-automatique avec tous les codes d’État détectés.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-211">DevTools populates the autocomplete dropdown menu with all of the status codes it has encountered.</span></span> |  

### <span data-ttu-id="9f3cd-212">Filtrer les demandes par type</span><span class="sxs-lookup"><span data-stu-id="9f3cd-212">Filter requests by type</span></span>  

<span data-ttu-id="9f3cd-213">Pour filtrer les demandes par type de requête, sélectionnez les boutons **XHR**, **js**, **CSS**, **img**, **multimédia**, **police**, **doc**, **WS** \ (WebSocket \), **manifeste**ou **autre** (n’importe quel autre type non répertorié ici \) sur le panneau réseau.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-213">To filter requests by request type, select the **XHR**, **JS**, **CSS**, **Img**, **Media**, **Font**, **Doc**, **WS** \(WebSocket\), **Manifest**, or **Other** \(any other type not listed here\) buttons on the Network panel.</span></span>  

<span data-ttu-id="9f3cd-214">Si vous ne voyez pas ces boutons, le volet filtres est probablement masqué.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-214">If you do not see these buttons, the Filters pane is probably hidden.</span></span>  
<span data-ttu-id="9f3cd-215">Voir [masquer le volet filtres](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="9f3cd-215">See [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

<span data-ttu-id="9f3cd-216">Pour activer plusieurs filtres de type simultanément, appuyez sur `Control` \ (Windows \) ou `Command` \ (MacOS \), puis sélectionnez.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-216">To enable multiple type filters simultaneously, hold `Control` \(Windows\) or `Command` \(macOS\) and then select.</span></span>  

:::image type="complex" source="../media/network-network-type-filters.msft.png" alt-text="Utiliser les filtres de type pour afficher les ressources JS, CSS et document" lightbox="../media/network-network-type-filters.msft.png":::
   <span data-ttu-id="9f3cd-218">Figure 11: utilisation des filtres de type pour afficher les ressources JS, CSS et document</span><span class="sxs-lookup"><span data-stu-id="9f3cd-218">Figure 11:  Using the Type filters to display JS, CSS, and Document resources</span></span>  
:::image-end:::  

### <span data-ttu-id="9f3cd-219">Filtrer les demandes par heure</span><span class="sxs-lookup"><span data-stu-id="9f3cd-219">Filter requests by time</span></span>  

<span data-ttu-id="9f3cd-220">Sélectionnez et faites glisser vers la gauche ou la droite dans le volet vue d’ensemble pour afficher uniquement les demandes actives au cours de cette période.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-220">Select and drag left or right on the Overview pane to only display requests that were active during that time frame.</span></span>  <span data-ttu-id="9f3cd-221">Le filtre est inclusive.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-221">The filter is inclusive.</span></span>  <span data-ttu-id="9f3cd-222">Toutes les demandes qui ont été actives pendant la durée en surbrillance apparaissent.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-222">Any request that was active during the highlighted time is shown.</span></span>  

:::image type="complex" source="../media/network-network-overview-filter.msft.png" alt-text="Filtrage des requêtes inactives depuis 300M" lightbox="../media/network-network-overview-filter.msft.png":::
   <span data-ttu-id="9f3cd-224">Figure 12: filtrage des requêtes inactives depuis 300 m</span><span class="sxs-lookup"><span data-stu-id="9f3cd-224">Figure 12:  Filtering out any requests that were inactive around 300ms</span></span>  
:::image-end:::  

### <span data-ttu-id="9f3cd-225">Masquer les URL de données</span><span class="sxs-lookup"><span data-stu-id="9f3cd-225">Hide data URLs</span></span>  

<span data-ttu-id="9f3cd-226">Les [URL de données][MDNHTTPDataURIs] sont des petits fichiers incorporés dans d’autres documents.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-226">[Data URLs][MDNHTTPDataURIs] are small files embedded into other documents.</span></span>  <span data-ttu-id="9f3cd-227">Toute demande figurant dans la table demandes qui commence par `data:` est une URL de données.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-227">Any request that you see in the Requests table that starts with `data:` is a data URL.</span></span>  

<span data-ttu-id="9f3cd-228">Cochez la case **Masquer les URL de données** pour masquer les demandes.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-228">Check the **Hide data URLs** checkbox to hide the requests.</span></span>  

:::image type="complex" source="../media/network-network-hide-data-urls.msft.png" alt-text="Case à cocher Masquer les URL de données" lightbox="../media/network-network-hide-data-urls.msft.png":::
   <span data-ttu-id="9f3cd-230">Figure 13: cases à cocher **Masquer les URL de données**</span><span class="sxs-lookup"><span data-stu-id="9f3cd-230">Figure 13:  The **Hide Data URLs** checkbox</span></span>  
:::image-end:::  

## <span data-ttu-id="9f3cd-231">Demandes de tri</span><span class="sxs-lookup"><span data-stu-id="9f3cd-231">Sort requests</span></span>  

<span data-ttu-id="9f3cd-232">Par défaut, les requêtes dans la table demandes sont triées par heure de début, mais vous pouvez trier le tableau en utilisant d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-232">By default, the requests in the Requests table are sorted by initiation time, but you may sort the table using other criteria.</span></span>  

### <span data-ttu-id="9f3cd-233">Trier par colonne</span><span class="sxs-lookup"><span data-stu-id="9f3cd-233">Sort by column</span></span>  

<span data-ttu-id="9f3cd-234">Sélectionnez l’en-tête de n’importe quelle colonne dans les requêtes pour trier les demandes en se sur cette colonne.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-234">Select the header of any column in the Requests to sort requests by that column.</span></span>  

### <span data-ttu-id="9f3cd-235">Trier par phase d’activité</span><span class="sxs-lookup"><span data-stu-id="9f3cd-235">Sort by activity phase</span></span>  

<span data-ttu-id="9f3cd-236">Pour modifier la façon dont les demandes de tri d’une cascade sont triées, pointez sur l’en-tête de la table demandes, ouvrez le menu **contextuel, puis**sélectionnez l’une des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-236">To change how the Waterfall sorts requests, hover on the header of the Requests table, open the contextual menu \(right-click\), hover over **Waterfall**, and select one of the following options.</span></span>  

*   <span data-ttu-id="9f3cd-237">**Heure de début**.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-237">**Start Time**.</span></span>  <span data-ttu-id="9f3cd-238">La première requête lancée est en haut.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-238">The first request that was initiated is at the top.</span></span>  
*   <span data-ttu-id="9f3cd-239">**Temps de réponse**.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-239">**Response Time**.</span></span>  <span data-ttu-id="9f3cd-240">La première demande qui a démarré le téléchargement est en haut.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-240">The first request that started downloading is at the top.</span></span>  
*   <span data-ttu-id="9f3cd-241">**Heure de fin**.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-241">**End Time**.</span></span>  <span data-ttu-id="9f3cd-242">La première demande qui est terminée est en haut.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-242">The first request that finished is at the top.</span></span>  
*   <span data-ttu-id="9f3cd-243">**Durée totale**.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-243">**Total Duration**.</span></span>  <span data-ttu-id="9f3cd-244">La requête avec la configuration de connexion la plus courte et la demande/réponse se trouvent dans la partie supérieure.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-244">The request with the shortest connection setup and request / response is at the top.</span></span>  
*   <span data-ttu-id="9f3cd-245">**Latence**.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-245">**Latency**.</span></span>  <span data-ttu-id="9f3cd-246">La requête qui a attendu le plus court délai d’une réponse est située en haut.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-246">The request that waited the shortest time for a response is at the top.</span></span>  

<span data-ttu-id="9f3cd-247">Ces descriptions présupposent que chaque option respective est classée du plus court au plus long.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-247">These descriptions assume that each respective option is ranked from shortest to longest.</span></span>  <span data-ttu-id="9f3cd-248">La sélection de l’en-tête de la colonne en **cascade** inverse l’ordre.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-248">Selecting the header of the **Waterfall** column reverses the order.</span></span>  

:::image type="complex" source="../media/network-network-waterfall-total-duration.msft.png" alt-text="Tri des cascades par durée totale" lightbox="../media/network-network-waterfall-total-duration.msft.png":::
   <span data-ttu-id="9f3cd-250">Figure 14: trier les cascades en fonction de la durée totale \ (la partie plus claire de chaque barre représente le temps passé en attente et la partie plus foncée est le temps de télécharger les octets \)</span><span class="sxs-lookup"><span data-stu-id="9f3cd-250">Figure 14:  Sorting the Waterfall by total duration  \(The lighter portion of each bar is time spent waiting and the darker portion is time spent downloading bytes\)</span></span>  
:::image-end:::  

## <span data-ttu-id="9f3cd-251">Analyser les requêtes</span><span class="sxs-lookup"><span data-stu-id="9f3cd-251">Analyze requests</span></span>  

<span data-ttu-id="9f3cd-252">Tant que DevTools est ouvert, il enregistre toutes les demandes dans le panneau réseau.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-252">So long as DevTools is open, it logs all requests in the Network panel.</span></span>  
<span data-ttu-id="9f3cd-253">Utilisez le volet réseau pour analyser les requêtes.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-253">Use the Network panel to analyze requests.</span></span>  

### <span data-ttu-id="9f3cd-254">Afficher un journal des demandes</span><span class="sxs-lookup"><span data-stu-id="9f3cd-254">View a log of requests</span></span>  

<span data-ttu-id="9f3cd-255">Utilisez le tableau demandes pour afficher un journal de toutes les demandes effectuées lorsque DevTools est ouvert.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-255">Use the Requests table to view a log of all requests made while DevTools has been open.</span></span>  <span data-ttu-id="9f3cd-256">La sélection ou le passage de demandes au-dessus révèle des informations supplémentaires sur chaque élément.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-256">Selecting or hovering over requests reveals more information about each item.</span></span>  

:::image type="complex" source="../media/network-network-requests-table.msft.png" alt-text="Table demandes" lightbox="../media/network-network-requests-table.msft.png":::
   <span data-ttu-id="9f3cd-258">Figure 15: table demandes</span><span class="sxs-lookup"><span data-stu-id="9f3cd-258">Figure 15:  The Requests table</span></span>  
:::image-end:::  

<span data-ttu-id="9f3cd-259">La table demandes affiche les colonnes suivantes par défaut.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-259">The Requests table displays the following columns by default.</span></span>  

*   <span data-ttu-id="9f3cd-260">**Nom**.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-260">**Name**.</span></span>  <span data-ttu-id="9f3cd-261">Nom de fichier ou un identificateur pour la ressource.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-261">The filename of, or an identifier for, the resource.</span></span>  
*   <span data-ttu-id="9f3cd-262">**Status**.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-262">**Status**.</span></span>  <span data-ttu-id="9f3cd-263">Code d’état HTTP.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-263">The HTTP status code.</span></span>  
*   <span data-ttu-id="9f3cd-264">**Type**.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-264">**Type**.</span></span>  <span data-ttu-id="9f3cd-265">Type MIME de la ressource demandée.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-265">The MIME type of the requested resource.</span></span>  
*   <span data-ttu-id="9f3cd-266">**Initiator**.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-266">**Initiator**.</span></span>  <span data-ttu-id="9f3cd-267">Les requêtes d’ouverture des objets ou processus suivants sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="9f3cd-267">The following objects or processes initiate requests:</span></span>  
    *   <span data-ttu-id="9f3cd-268">**Analyseur**.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-268">**Parser**.</span></span>  <span data-ttu-id="9f3cd-269">Analyseur HTML pour Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-269">The HTML parser for Microsoft Edge.</span></span>  
    *   <span data-ttu-id="9f3cd-270">**Redirect**.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-270">**Redirect**.</span></span>  <span data-ttu-id="9f3cd-271">Une redirection HTTP.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-271">An HTTP redirect.</span></span>  
    *   <span data-ttu-id="9f3cd-272">**Script**.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-272">**Script**.</span></span>  <span data-ttu-id="9f3cd-273">Fonction JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-273">A JavaScript function.</span></span>  
    *   <span data-ttu-id="9f3cd-274">**Autre**.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-274">**Other**.</span></span>  <span data-ttu-id="9f3cd-275">Un autre processus ou action, comme la navigation vers une page par le biais d’un lien ou la saisie d’une URL dans la barre d’adresses.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-275">Some other process or action, such as navigating to a page via a link or entering a URL in the address bar.</span></span>  
*   <span data-ttu-id="9f3cd-276">**Taille**.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-276">**Size**.</span></span>  <span data-ttu-id="9f3cd-277">Taille combinée des en-têtes de réponse et du corps de la réponse, tel qu’il est délivré par le serveur.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-277">The combined size of the response headers plus the response body, as delivered by the server.</span></span>  
*   <span data-ttu-id="9f3cd-278">**Temps**.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-278">**Time**.</span></span>  <span data-ttu-id="9f3cd-279">Durée totale, entre le début de la demande et la réception de l’octet final dans la réponse.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-279">The total duration, from the start of the request to the receipt of the final byte in the response.</span></span>  
*   <span data-ttu-id="9f3cd-280">En [**cascade**](#view-the-timing-of-requests-in-relation-to-one-another).</span><span class="sxs-lookup"><span data-stu-id="9f3cd-280">[**Waterfall**](#view-the-timing-of-requests-in-relation-to-one-another).</span></span>  <span data-ttu-id="9f3cd-281">Répartition visuelle de l’activité pour chaque demande.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-281">A visual breakdown of the activity for each request.</span></span>  

#### <span data-ttu-id="9f3cd-282">Ajouter ou supprimer des colonnes</span><span class="sxs-lookup"><span data-stu-id="9f3cd-282">Add or remove columns</span></span>  

<span data-ttu-id="9f3cd-283">Placez le curseur sur l’en-tête de la table demandes, ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \), puis sélectionnez une option pour la masquer ou l’afficher.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-283">Hover on the header of the Requests table, open the contextual menu \(right-click\), and select an option to hide or show it.</span></span>  <span data-ttu-id="9f3cd-284">Les options actuellement affichées disposent de coches en regard de chaque élément.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-284">Currently displayed options have checkmarks next to each item.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-column.msft.png" alt-text="Ajout d’une colonne dans la table demandes" lightbox="../media/network-network-requests-add-column.msft.png":::
   <span data-ttu-id="9f3cd-286">Figure 16: ajout d’une colonne dans la table demandes</span><span class="sxs-lookup"><span data-stu-id="9f3cd-286">Figure 16:  Adding a column to the Requests table</span></span>  
:::image-end:::  

#### <span data-ttu-id="9f3cd-287">Ajouter des colonnes personnalisées</span><span class="sxs-lookup"><span data-stu-id="9f3cd-287">Add custom columns</span></span>  

<span data-ttu-id="9f3cd-288">Pour ajouter une colonne personnalisée dans la table demandes, positionnez le curseur sur l’en-tête de la table demandes, ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \), puis sélectionnez les **en-têtes de réponse**  >  **gérer les colonnes d’en-tête**.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-288">To add a custom column to the Requests table, hover on the header of the Requests table, open the contextual menu \(right-click\), and select **Response Headers** > **Manage Header Columns**.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-custom.msft.png" alt-text="Ajout d’une colonne personnalisée dans la table demandes" lightbox="../media/network-network-requests-add-custom.msft.png":::
   <span data-ttu-id="9f3cd-290">Figure 17: ajout d’une colonne personnalisée dans la table demandes</span><span class="sxs-lookup"><span data-stu-id="9f3cd-290">Figure 17:  Adding a custom column to the Requests table</span></span>  
:::image-end:::  

### <span data-ttu-id="9f3cd-291">Afficher le minutage des requêtes les uns par rapport aux autres</span><span class="sxs-lookup"><span data-stu-id="9f3cd-291">View the timing of requests in relation to one another</span></span>  

<span data-ttu-id="9f3cd-292">Utilisez la cascade pour afficher le minutage des requêtes les uns par rapport aux autres.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-292">Use the Waterfall to view the timing of requests in relation to one another.</span></span>  
<span data-ttu-id="9f3cd-293">Par défaut, la cascade est organisée selon l’heure de début des requêtes.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-293">By default, the Waterfall is organized by the start time of the requests.</span></span>  
<span data-ttu-id="9f3cd-294">Par conséquent, les demandes qui sont plus éloignées de gauche que celles qui sont plus éloignées.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-294">So, requests that are farther to the left started earlier than those that are farther to the right.</span></span>  

<span data-ttu-id="9f3cd-295">Pour plus d’options, voir [Trier par phase d’activité](#sort-by-activity-phase) .</span><span class="sxs-lookup"><span data-stu-id="9f3cd-295">See [Sort by activity phase](#sort-by-activity-phase) to see the different ways that you may sort the Waterfall.</span></span>  

:::image type="complex" source="../media/network-network-requests-waterfall.msft.png" alt-text="Colonne cascade du volet demandes" lightbox="../media/network-network-requests-waterfall.msft.png":::
   <span data-ttu-id="9f3cd-297">Figure 18: colonne cascade du volet **demandes**</span><span class="sxs-lookup"><span data-stu-id="9f3cd-297">Figure 18:  The Waterfall column of the **Requests** pane</span></span>  
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

### <span data-ttu-id="9f3cd-298">Afficher un aperçu d’un corps de réponse</span><span class="sxs-lookup"><span data-stu-id="9f3cd-298">View a preview of a response body</span></span>  

<span data-ttu-id="9f3cd-299">Pour afficher un aperçu d’un corps de réponse:</span><span class="sxs-lookup"><span data-stu-id="9f3cd-299">To view a preview of a response body:</span></span>  

1.  <span data-ttu-id="9f3cd-300">Sélectionnez l’URL de la requête dans la colonne **nom** de la table demandes.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-300">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="9f3cd-301">Sélectionnez l’onglet **Aperçu** .</span><span class="sxs-lookup"><span data-stu-id="9f3cd-301">Select the **Preview** tab.</span></span>  

<span data-ttu-id="9f3cd-302">Cet onglet est principalement utile pour afficher des images.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-302">This tab is mostly useful for viewing images.</span></span>  

:::image type="complex" source="../media/network-network-resources-preview.msft.png" alt-text="Onglet Aperçu" lightbox="../media/network-network-resources-preview.msft.png":::
   <span data-ttu-id="9f3cd-304">Figure 19: onglet **Aperçu**</span><span class="sxs-lookup"><span data-stu-id="9f3cd-304">Figure 19:  The **Preview** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="9f3cd-305">Afficher le corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="9f3cd-305">View a response body</span></span>  

<span data-ttu-id="9f3cd-306">Pour afficher le corps de la réponse à une demande:</span><span class="sxs-lookup"><span data-stu-id="9f3cd-306">To view the response body to a request:</span></span>  

1.  <span data-ttu-id="9f3cd-307">Sélectionnez l’URL de la requête dans la colonne **nom** de la table demandes.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-307">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="9f3cd-308">Sélectionnez l’onglet **réponse** .</span><span class="sxs-lookup"><span data-stu-id="9f3cd-308">Select the **Response** tab.</span></span>  

:::image type="complex" source="../media/network-network-resources-response.msft.png" alt-text="Onglet réponse" lightbox="../media/network-network-resources-response.msft.png":::
   <span data-ttu-id="9f3cd-310">Figure 20: onglet **réponse**</span><span class="sxs-lookup"><span data-stu-id="9f3cd-310">Figure 20:  The **Response** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="9f3cd-311">Afficher les en-têtes HTTP</span><span class="sxs-lookup"><span data-stu-id="9f3cd-311">View HTTP headers</span></span>  

<span data-ttu-id="9f3cd-312">Pour afficher les données d’en-tête HTTP relatives à une requête:</span><span class="sxs-lookup"><span data-stu-id="9f3cd-312">To view HTTP header data about a request:</span></span>  

1.  <span data-ttu-id="9f3cd-313">Sélectionnez l’URL de la requête dans la colonne **nom** de la table demandes.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-313">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="9f3cd-314">Sélectionnez l’onglet **en-têtes** .</span><span class="sxs-lookup"><span data-stu-id="9f3cd-314">Select the **Headers** tab.</span></span>  

:::image type="complex" source="../media/network-resources-headers.msft.png" alt-text="Onglet en-têtes" lightbox="../media/network-resources-headers.msft.png":::
   <span data-ttu-id="9f3cd-316">Figure 21: onglet **en-têtes**</span><span class="sxs-lookup"><span data-stu-id="9f3cd-316">Figure 21:  The **Headers** tab</span></span>  
:::image-end:::  

#### <span data-ttu-id="9f3cd-317">Afficher une source d’en-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="9f3cd-317">View HTTP header source</span></span>  

<span data-ttu-id="9f3cd-318">Par défaut, l’onglet en-têtes affiche les noms des en-têtes par ordre alphabétique.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-318">By default, the Headers tab shows header names alphabetically.</span></span>  <span data-ttu-id="9f3cd-319">Pour afficher les noms d’en-tête HTTP dans l’ordre dans lequel ils ont été reçus:</span><span class="sxs-lookup"><span data-stu-id="9f3cd-319">To view the HTTP header names in the order they were received:</span></span>  

1.  <span data-ttu-id="9f3cd-320">Ouvrez l’onglet **en-têtes** pour la requête qui vous intéresse.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-320">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="9f3cd-321">Voir [afficher les en-têtes http](#view-http-headers).</span><span class="sxs-lookup"><span data-stu-id="9f3cd-321">See [View HTTP headers](#view-http-headers).</span></span>  
1.  <span data-ttu-id="9f3cd-322">Sélectionnez **afficher la source**, en regard de la section en **-tête de requête** ou **en-tête de réponse** .</span><span class="sxs-lookup"><span data-stu-id="9f3cd-322">Select **view source**, next to the **Request Header** or **Response Header** section.</span></span>  

### <span data-ttu-id="9f3cd-323">Afficher les paramètres de chaîne de requête</span><span class="sxs-lookup"><span data-stu-id="9f3cd-323">View query string parameters</span></span>  

<span data-ttu-id="9f3cd-324">Pour afficher les paramètres de chaîne de requête d’une URL dans un format lisible par l’utilisateur:</span><span class="sxs-lookup"><span data-stu-id="9f3cd-324">To view the query string parameters of a URL in a human-readable format:</span></span>  

1.  <span data-ttu-id="9f3cd-325">Ouvrez l’onglet **en-têtes** pour la requête qui vous intéresse.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-325">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="9f3cd-326">Voir [afficher les en-têtes http](#view-http-headers).</span><span class="sxs-lookup"><span data-stu-id="9f3cd-326">See [View HTTP headers](#view-http-headers).</span></span>  
1.  <span data-ttu-id="9f3cd-327">Accédez à la section **paramètres de chaîne de requête** .</span><span class="sxs-lookup"><span data-stu-id="9f3cd-327">Go to the **Query String Parameters** section.</span></span>  

:::image type="complex" source="../media/network-network-resources-headers-query-string-parameters.msft.png" alt-text="Section paramètres de chaîne de requête" lightbox="../media/network-network-resources-headers-query-string-parameters.msft.png":::
   <span data-ttu-id="9f3cd-329">Figure 22: section **paramètres de chaînes de requête**</span><span class="sxs-lookup"><span data-stu-id="9f3cd-329">Figure 22:  The **Query String Parameters** section</span></span>  
:::image-end:::  

#### <span data-ttu-id="9f3cd-330">Afficher les paramètres de chaîne de requête source</span><span class="sxs-lookup"><span data-stu-id="9f3cd-330">View query string parameters source</span></span>  

<span data-ttu-id="9f3cd-331">Pour afficher la source du paramètre de chaîne de requête d’une requête:</span><span class="sxs-lookup"><span data-stu-id="9f3cd-331">To view the query string parameter source of a request:</span></span>  

1.  <span data-ttu-id="9f3cd-332">Accédez à la section paramètres de chaîne de requête.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-332">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="9f3cd-333">Voir [afficher les paramètres de chaîne de requête](#view-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="9f3cd-333">See [View query string parameters](#view-query-string-parameters).</span></span>  
1.  <span data-ttu-id="9f3cd-334">Sélectionnez **afficher la source**.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-334">Select **view source**.</span></span>  

#### <span data-ttu-id="9f3cd-335">Afficher les paramètres de chaîne de requête codés en URL</span><span class="sxs-lookup"><span data-stu-id="9f3cd-335">View URL-encoded query string parameters</span></span>  

<span data-ttu-id="9f3cd-336">Pour afficher les paramètres de chaîne de requête dans un format lisible par l’utilisateur, mais avec les codages conservés:</span><span class="sxs-lookup"><span data-stu-id="9f3cd-336">To view query string parameters in a human-readable format, but with encodings preserved:</span></span>  

1.  <span data-ttu-id="9f3cd-337">Accédez à la section paramètres de chaîne de requête.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-337">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="9f3cd-338">Voir [afficher les paramètres de chaîne de requête](#view-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="9f3cd-338">See [View query string parameters](#view-query-string-parameters).</span></span>  
1.  <span data-ttu-id="9f3cd-339">Sélectionnez **afficher l’URL**.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-339">Select **view URL encoded**.</span></span>  

### <span data-ttu-id="9f3cd-340">Afficher les cookies</span><span class="sxs-lookup"><span data-stu-id="9f3cd-340">View cookies</span></span>  

<span data-ttu-id="9f3cd-341">Pour afficher les cookies envoyés dans l’en-tête HTTP d’une requête:</span><span class="sxs-lookup"><span data-stu-id="9f3cd-341">To view the cookies sent in the HTTP header of a request:</span></span>  

1.  <span data-ttu-id="9f3cd-342">Sélectionnez l’URL de la requête dans la colonne **nom** de la table demandes.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-342">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="9f3cd-343">Sélectionnez l’onglet **cookies** .</span><span class="sxs-lookup"><span data-stu-id="9f3cd-343">Select the **Cookies** tab.</span></span>  

<!--See [Fields][ManageDataCookiesFields] for a description of each of the columns.  -->

<!--[ManageDataCookiesFields]: manage-data/cookies#fields  -->
<!--TODO: add link when section is available -->

:::image type="complex" source="../media/network-network-resources-cookies.msft.png" alt-text="Onglet cookies" lightbox="../media/network-network-resources-cookies.msft.png":::
   <span data-ttu-id="9f3cd-345">Figure 23: onglet cookies</span><span class="sxs-lookup"><span data-stu-id="9f3cd-345">Figure 23:  The Cookies tab</span></span>  
:::image-end:::  

### <span data-ttu-id="9f3cd-346">Afficher la répartition du minutage d’une requête</span><span class="sxs-lookup"><span data-stu-id="9f3cd-346">View the timing breakdown of a request</span></span>  

<span data-ttu-id="9f3cd-347">Pour afficher la répartition du minutage d’une requête:</span><span class="sxs-lookup"><span data-stu-id="9f3cd-347">To view the timing breakdown of a request:</span></span>  

1.  <span data-ttu-id="9f3cd-348">Sélectionnez l’URL de la requête dans la colonne **nom** de la table demandes.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-348">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="9f3cd-349">Sélectionnez l’onglet **minutage** .</span><span class="sxs-lookup"><span data-stu-id="9f3cd-349">Select the **Timing** tab.</span></span>  

<span data-ttu-id="9f3cd-350">Pour plus d’informations sur l’accès à ces données, voir [aperçu d’une répartition du temps](#preview-a-timing-breakdown) .</span><span class="sxs-lookup"><span data-stu-id="9f3cd-350">See [Preview a timing breakdown](#preview-a-timing-breakdown) for a faster way to access this data.</span></span>  

<span data-ttu-id="9f3cd-351">Pour plus d’informations sur les différentes phases que vous pouvez voir dans l’onglet Minutage, consultez la rubrique [étapes de répartition du temps](#timing-breakdown-phases-explained) .</span><span class="sxs-lookup"><span data-stu-id="9f3cd-351">See [Timing breakdown phases explained](#timing-breakdown-phases-explained) for more information about each of the phases that you may see in the Timing tab.</span></span>  

:::image type="complex" source="../media/network-network-resources-timing.msft.png" alt-text="Onglet Minutage" lightbox="../media/network-network-resources-timing.msft.png":::
   <span data-ttu-id="9f3cd-353">Figure 24: onglet **minutage**</span><span class="sxs-lookup"><span data-stu-id="9f3cd-353">Figure 24:  The **Timing** tab</span></span>  
:::image-end:::  

<span data-ttu-id="9f3cd-354">Plus d’informations sur chacune de ces étapes.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-354">More information about each of the phases.</span></span>  

<span data-ttu-id="9f3cd-355">Pour accéder à cet affichage, voir répartition de l' [affichage du minutage](#view-the-timing-breakdown-of-a-request) .</span><span class="sxs-lookup"><span data-stu-id="9f3cd-355">See [View timing breakdown](#view-the-timing-breakdown-of-a-request) for another way to access this view.</span></span>  

#### <span data-ttu-id="9f3cd-356">Prévisualiser une répartition de minutage</span><span class="sxs-lookup"><span data-stu-id="9f3cd-356">Preview a timing breakdown</span></span>  

<span data-ttu-id="9f3cd-357">Pour afficher un aperçu de la répartition du minutage d’une requête, placez le pointeur sur l’entrée de la requête dans la colonne **cascade** de la table demandes.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-357">To view a preview of the timing breakdown of a request, hover over the entry for the request in the **Waterfall** column of the Requests table.</span></span>  

<span data-ttu-id="9f3cd-358">Pour accéder à ces données qui ne nécessitent pas de pointage, voir [afficher la répartition du minutage d’une demande](#view-the-timing-breakdown-of-a-request) .</span><span class="sxs-lookup"><span data-stu-id="9f3cd-358">See [View the timing breakdown of a request](#view-the-timing-breakdown-of-a-request) for a way to access this data that does not require hovering.</span></span>  

:::image type="complex" source="../media/network-network-resources-waterfall-hover.msft.png" alt-text="> aperçu de la répartition du minutage d’une requête" lightbox="../media/network-network-resources-waterfall-hover.msft.png":::
   <span data-ttu-id="9f3cd-360">Figure 25: prévisualisation de la répartition du minutage d’une requête</span><span class="sxs-lookup"><span data-stu-id="9f3cd-360">Figure 25:  Previewing the timing breakdown of a request</span></span>  
:::image-end:::  

#### <span data-ttu-id="9f3cd-361">Explication des phases de répartition du temps</span><span class="sxs-lookup"><span data-stu-id="9f3cd-361">Timing breakdown phases explained</span></span>  

<span data-ttu-id="9f3cd-362">Plus d’informations sur chacune des phases que vous pouvez voir dans l’onglet **minutage** .</span><span class="sxs-lookup"><span data-stu-id="9f3cd-362">More information about each of the phases you may see in the **Timing** tab.</span></span>  

*   <span data-ttu-id="9f3cd-363">Mise en **file d’attente**.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-363">**Queueing**.</span></span>  <span data-ttu-id="9f3cd-364">Le navigateur met en file d’attente les requêtes dans les cas suivants:</span><span class="sxs-lookup"><span data-stu-id="9f3cd-364">The browser queues requests when:</span></span>  
    *   <span data-ttu-id="9f3cd-365">Il y a des demandes de priorité plus élevées.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-365">There are higher priority requests.</span></span>  
    *   <span data-ttu-id="9f3cd-366">Il existe déjà six connexions TCP ouvertes pour cette origine, qui correspond à la limite.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-366">There are already six TCP connections open for this origin, which is the limit.</span></span>  <span data-ttu-id="9f3cd-367">S’applique uniquement aux protocoles HTTP/1.0 et HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-367">Applies to HTTP/1.0 and HTTP/1.1 only.</span></span>  
    *   <span data-ttu-id="9f3cd-368">Le navigateur alloue de l’espace dans le cache disque.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-368">The browser is briefly allocating space in the disk cache.</span></span>  
*   <span data-ttu-id="9f3cd-369">**Bloqué**.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-369">**Stalled**.</span></span>  <span data-ttu-id="9f3cd-370">La requête peut être bloquée pour l’une des raisons décrites dans la **file d’attente**.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-370">The request could be stalled for any of the reasons described in **Queueing**.</span></span>  
*   <span data-ttu-id="9f3cd-371">**Recherche DNS**.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-371">**DNS Lookup**.</span></span>  <span data-ttu-id="9f3cd-372">Le navigateur résout l’adresse IP pour la requête.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-372">The browser is resolving the IP address for the request.</span></span>  
*   <span data-ttu-id="9f3cd-373">**Connexion initiale**.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-373">**Initial connection**.</span></span>  <span data-ttu-id="9f3cd-374">Le navigateur établit une connexion, notamment les négociations TCP, les tentatives de connexion TCP et la négociation d’une connexion SSL.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-374">The browser is establishing a connection including TCP handshakes, TCP retries, and negotiating an SSL.</span></span>
*   <span data-ttu-id="9f3cd-375">**Négociation de proxy**.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-375">**Proxy negotiation**.</span></span>  <span data-ttu-id="9f3cd-376">Le navigateur négocie la requête avec un [serveur proxy][WikiProxyServer].</span><span class="sxs-lookup"><span data-stu-id="9f3cd-376">The browser is negotiating the request with a [proxy server][WikiProxyServer].</span></span>  
*   <span data-ttu-id="9f3cd-377">**Demande envoyée**.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-377">**Request sent**.</span></span>  <span data-ttu-id="9f3cd-378">La requête est en cours d’envoi.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-378">The request is being sent.</span></span>  
*   <span data-ttu-id="9f3cd-379">**Préparation ServiceWorker**.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-379">**ServiceWorker Preparation**.</span></span>  <span data-ttu-id="9f3cd-380">Le navigateur démarre le travailleur du service.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-380">The browser is starting up the service worker.</span></span>  
*   <span data-ttu-id="9f3cd-381">**Demander à ServiceWorker**.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-381">**Request to ServiceWorker**.</span></span>  <span data-ttu-id="9f3cd-382">La demande est envoyée au travailleur de service.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-382">The request is being sent to the service worker.</span></span>  
*   <span data-ttu-id="9f3cd-383">En **attente \ (TTFB \)**.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-383">**Waiting \(TTFB\)**.</span></span>  <span data-ttu-id="9f3cd-384">Le navigateur attend le premier octet d’une réponse.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-384">The browser is waiting for the first byte of a response.</span></span>  
  <span data-ttu-id="9f3cd-385">TTFB représente le temps à l’octet initial.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-385">TTFB stands for Time To First Byte.</span></span>  <span data-ttu-id="9f3cd-386">Ce minutage inclut un aller-retour d’une latence et la durée du serveur pour préparer la réponse.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-386">This timing includes 1 round trip of latency and the time the server took to prepare the response.</span></span>  
*   <span data-ttu-id="9f3cd-387">**Téléchargement du contenu**.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-387">**Content Download**.</span></span>  <span data-ttu-id="9f3cd-388">Le navigateur reçoit la réponse.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-388">The browser is receiving the response.</span></span>  
*   <span data-ttu-id="9f3cd-389">**Réception**d’une émission.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-389">**Receiving Push**.</span></span>  <span data-ttu-id="9f3cd-390">Le navigateur reçoit des données pour cette réponse via le protocole HTTP/2 Server Poussée.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-390">The browser is receiving data for this response via HTTP/2 Server Push.</span></span>  
*   <span data-ttu-id="9f3cd-391">**Lecture en lecture**.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-391">**Reading Push**.</span></span>  <span data-ttu-id="9f3cd-392">Le navigateur lit les données locales précédemment reçues.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-392">The browser is reading the local data previously received.</span></span>  

### <span data-ttu-id="9f3cd-393">Afficher les initiateurs et les dépendances</span><span class="sxs-lookup"><span data-stu-id="9f3cd-393">View initiators and dependencies</span></span>  

<span data-ttu-id="9f3cd-394">Pour afficher les initiateurs et les dépendances d’une requête, maintenez la touche enfoncée `Shift` et placez le pointeur sur la requête dans la table demandes.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-394">To view the initiators and dependencies of a request, hold `Shift`and hover over the request in the Requests table.</span></span>  <span data-ttu-id="9f3cd-395">Couleurs de DevTools: les initiateurs apparaissent en vert et les dépendances apparaissent en rouge.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-395">DevTools colors: initiators are shown in green and dependencies are shown in red.</span></span>  

:::image type="complex" source="../media/network-network-resources-initiators-dependencies.msft.png" alt-text="Affichage des déclencheurs et des dépendances d’une requête" lightbox="../media/network-network-resources-initiators-dependencies.msft.png":::
   <span data-ttu-id="9f3cd-397">Figure 26: affichage des déclencheurs et dépendances d’une requête</span><span class="sxs-lookup"><span data-stu-id="9f3cd-397">Figure 26:  Viewing the initiators and dependencies of a request</span></span>  
:::image-end:::  

<span data-ttu-id="9f3cd-398">Lorsque la table requêtes est classée dans un ordre chronologique, la première demande verte au-dessus de celle où vous pointez est l’initiateur de la dépendance.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-398">When the Requests table is ordered chronologically, the first green request above the one you are hovering is the initiator of the dependency.</span></span>  <span data-ttu-id="9f3cd-399">Si une autre demande verte s’affiche au-dessus de celle-ci, il s’agit de l’initiateur de l’initiateur.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-399">If another green request appears above that, that higher request is the initiator of the initiator.</span></span>  <span data-ttu-id="9f3cd-400">Et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-400">And so on.</span></span>  

### <span data-ttu-id="9f3cd-401">Afficher les événements de chargement</span><span class="sxs-lookup"><span data-stu-id="9f3cd-401">View load events</span></span>  

<span data-ttu-id="9f3cd-402">DevTools affiche le minutage des `DOMContentLoaded` événements et `load` dans plusieurs emplacements du panneau réseau.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-402">DevTools displays the timing of the `DOMContentLoaded` and `load` events in multiple places on the Network panel.</span></span>  <span data-ttu-id="9f3cd-403">L' `DOMContentLoaded` événement est coloré en bleu et l' `load` événement est rouge.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-403">The `DOMContentLoaded` event is colored blue, and the `load` event is red.</span></span>  

:::image type="complex" source="../media/network-network-requests-load-events.msft.png" alt-text="Emplacements des événements DOMContentLoaded et Load sur le panneau réseau" lightbox="../media/network-network-requests-load-events.msft.png":::
   <span data-ttu-id="9f3cd-405">Figure 27: emplacements des `DOMContentLoaded` `load` événements et sur le panneau réseau</span><span class="sxs-lookup"><span data-stu-id="9f3cd-405">Figure 27:  The locations of the `DOMContentLoaded` and `load` events on the Network panel</span></span>  
:::image-end:::  

### <span data-ttu-id="9f3cd-406">Afficher le nombre total de demandes</span><span class="sxs-lookup"><span data-stu-id="9f3cd-406">View the total number of requests</span></span>  

<span data-ttu-id="9f3cd-407">Le nombre total de demandes est répertorié dans le volet Résumé, au bas du panneau réseau.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-407">The total number of requests is listed in the Summary pane, at the bottom of the Network panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="9f3cd-408">Ce numéro suit uniquement les requêtes qui ont été enregistrées depuis l’ouverture de DevTools.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-408">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="9f3cd-409">Si d’autres requêtes s’est produites avant l’ouverture de DevTools, ces demandes ne sont pas comptabilisées.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-409">If other requests occurred before DevTools was opened, those requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-requests.msft.png" alt-text="Nombre total de demandes depuis l’ouverture de DevTools" lightbox="../media/network-network-total-requests.msft.png":::
   <span data-ttu-id="9f3cd-411">Figure 28: nombre total de demandes depuis l’ouverture de DevTools</span><span class="sxs-lookup"><span data-stu-id="9f3cd-411">Figure 28:  The total number of requests since DevTools was opened</span></span>  
:::image-end:::  

### <span data-ttu-id="9f3cd-412">Affichez la taille totale du téléchargement</span><span class="sxs-lookup"><span data-stu-id="9f3cd-412">View the total download size</span></span>  

<span data-ttu-id="9f3cd-413">La taille de téléchargement totale des demandes figure dans le volet Résumé, en bas du volet réseau.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-413">The total download size of requests is listed in the Summary pane, at the bottom of the Network panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="9f3cd-414">Ce numéro suit uniquement les requêtes qui ont été enregistrées depuis l’ouverture de DevTools.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-414">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="9f3cd-415">Si d’autres requêtes s’est produites avant l’ouverture de DevTools, les requêtes précédentes ne sont pas comptabilisées.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-415">If other requests occurred before DevTools was opened, the previous requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-download-size.msft.png" alt-text="La taille de téléchargement totale des requêtes" lightbox="../media/network-network-total-download-size.msft.png":::
   <span data-ttu-id="9f3cd-417">Figure 29: taille totale du téléchargement de demandes</span><span class="sxs-lookup"><span data-stu-id="9f3cd-417">Figure 29:  The total download size of requests</span></span>  
:::image-end:::  

<span data-ttu-id="9f3cd-418">Pour afficher [le nombre de ressources de taille décompressées, voir afficher la taille d’une ressource](#view-the-uncompressed-size-of-a-resource) , puis décompresser chaque élément.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-418">See [View the uncompressed size of a resource](#view-the-uncompressed-size-of-a-resource) to see how large resources are after the browser uncompresses each item.</span></span>  

### <span data-ttu-id="9f3cd-419">Afficher la trace de pile ayant entraîné une requête</span><span class="sxs-lookup"><span data-stu-id="9f3cd-419">View the stack trace that caused a request</span></span>  

<span data-ttu-id="9f3cd-420">Après qu’une instruction JavaScript demande une ressource, placez le pointeur sur la colonne **Initiator** pour afficher la trace de pile qui se trouve au début de la requête.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-420">After a JavaScript statement requests a resource, hover over the **Initiator** column to view the stack trace leading up to the request.</span></span>  

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
   <span data-ttu-id="9f3cd-422">Figure 30: trace de pile aboutissant à une demande de ressources</span><span class="sxs-lookup"><span data-stu-id="9f3cd-422">Figure 30:  The stack trace leading up to a resource request</span></span>  
:::image-end:::  

### <span data-ttu-id="9f3cd-423">Affichage de la taille de la ressource non compressée</span><span class="sxs-lookup"><span data-stu-id="9f3cd-423">View the uncompressed size of a resource</span></span>  

<span data-ttu-id="9f3cd-424">Activez la case à cocher **utiliser des lignes de requête volumineuses** , puis examinez la valeur inférieure de la colonne **taille** .</span><span class="sxs-lookup"><span data-stu-id="9f3cd-424">Select the **Use large request rows** checkbox and then look at the bottom value of the **Size** column.</span></span>  

:::image type="complex" source="../media/network-network-requests-uncompressed-compare.msft.png" alt-text="Exemple de ressources non compressées" lightbox="../media/network-network-requests-uncompressed-compare.msft.png":::
   <span data-ttu-id="9f3cd-426">Figure 31: exemple de ressources non compressées \ (la taille du `jquery-3.3.1.min.js` fichier qui a été envoyée par le biais du réseau était `29.9 KB` , alors que la taille du fichier non compressé était de `84.9 KB` \)</span><span class="sxs-lookup"><span data-stu-id="9f3cd-426">Figure 31:  An example of uncompressed resources  \(The compressed size of the `jquery-3.3.1.min.js` file that was sent over the network was `29.9 KB`, whereas the uncompressed size was `84.9 KB`\)</span></span>  
:::image-end:::  

## <span data-ttu-id="9f3cd-427">Exporter les données de requête</span><span class="sxs-lookup"><span data-stu-id="9f3cd-427">Export requests data</span></span>  

### <span data-ttu-id="9f3cd-428">Enregistrer toutes les demandes réseau dans un fichier QAR</span><span class="sxs-lookup"><span data-stu-id="9f3cd-428">Save all network requests to a HAR file</span></span>  

<span data-ttu-id="9f3cd-429">Pour enregistrer toutes les demandes réseau dans un fichier QAR, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-429">To save all network requests to a HAR file, complete the following steps.</span></span>  

1.  <span data-ttu-id="9f3cd-430">Positionnez le pointeur sur une requête dans la table demandes et ouvrez le menu contextuel, puis cliquez sur le bouton droit de la souris.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-430">Hover on any request in the Requests table and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="9f3cd-431">Sélectionnez **Save As QAR with content**.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-431">Select **Save as HAR with Content**.</span></span>  <span data-ttu-id="9f3cd-432">DevTools enregistre toutes les demandes qui se sont produites depuis que vous avez ouvert DevTools sur le fichier.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-432">DevTools saves all requests that have occurred since you opened DevTools to the HAR file.</span></span>  <span data-ttu-id="9f3cd-433">Il n’est pas possible de filtrer les demandes ou de n’enregistrer qu’une seule demande.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-433">There is no way to filter requests, or to save just a single request.</span></span>  

<span data-ttu-id="9f3cd-434">Lorsque vous enregistrez un fichier QAR, vous pouvez l’importer de nouveau dans DevTools pour analyse.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-434">Once you save a HAR file, you may import it back into DevTools for analysis.</span></span>  <span data-ttu-id="9f3cd-435">Il suffit de glisser-déplacer le fichier QAR dans la table demandes.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-435">Just drag-and-drop the HAR file into the Requests table.</span></span>  
<!--See also [HAR Analyzer][HARAnalyzer].  -->  

<!--[HARAnalyzer]: https://toolbox.alphabetapps.com/apps/har_analyzer  -->  
<!--Todo: add section link when content is available  -->  

:::image type="complex" source="../media/network-network-requests-save-har-content.msft.png" alt-text="Sélection de l’option Enregistrer sous le contenu de votre fichier" lightbox="../media/network-network-requests-save-har-content.msft.png":::
   <span data-ttu-id="9f3cd-437">Figure 32: sélection **de l’option Enregistrer sous le contenu de votre fichier** .</span><span class="sxs-lookup"><span data-stu-id="9f3cd-437">Figure 32:  Selecting **Save as HAR with Content**</span></span>  
:::image-end:::  

### <span data-ttu-id="9f3cd-438">Copier une ou plusieurs demandes dans le presse-papiers</span><span class="sxs-lookup"><span data-stu-id="9f3cd-438">Copy one or more requests to the clipboard</span></span>  

<span data-ttu-id="9f3cd-439">Dans la colonne **nom** de la table demandes, positionnez le pointeur sur une requête, ouvrez le menu contextuel **, puis**sélectionnez l’une des options suivantes...</span><span class="sxs-lookup"><span data-stu-id="9f3cd-439">Under the **Name** column of the Requests table, hover on a request, open the contextual menu \(right-click\), hover over **Copy**, and select one of the following options.</span></span>  

*   <span data-ttu-id="9f3cd-440">**Copier l’adresse du lien**.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-440">**Copy Link Address**.</span></span>  <span data-ttu-id="9f3cd-441">Copiez l’URL de la requête dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-441">Copy the URL of the request to the clipboard.</span></span>  
*   <span data-ttu-id="9f3cd-442">**Copier la réponse**.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-442">**Copy Response**.</span></span>  <span data-ttu-id="9f3cd-443">Copiez le corps de la réponse dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-443">Copy the response body to the clipboard.</span></span>  
*   <span data-ttu-id="9f3cd-444">**Copy As FETCH**.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-444">**Copy as Fetch**.</span></span>  
*   <span data-ttu-id="9f3cd-445">**Copier comme courbe**.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-445">**Copy as cURL**.</span></span>  <span data-ttu-id="9f3cd-446">Copiez la demande en tant que commande en forme de boucle.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-446">Copy the request as a cURL command.</span></span>  
*   <span data-ttu-id="9f3cd-447">**Copy All As FETCH**.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-447">**Copy All as Fetch**.</span></span>  
*   <span data-ttu-id="9f3cd-448">**Tout copier comme courbe**.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-448">**Copy All as cURL**.</span></span>  <span data-ttu-id="9f3cd-449">Copiez toutes les demandes comme une chaîne de commandes bouclé.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-449">Copy all requests as a chain of cURL commands.</span></span>  
*   <span data-ttu-id="9f3cd-450">**Copy All As QAR**.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-450">**Copy All as HAR**.</span></span>  <span data-ttu-id="9f3cd-451">Copiez toutes les demandes en tant que données QAR.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-451">Copy all requests as HAR data.</span></span>  

:::image type="complex" source="../media/network-network-requests-copy-response.msft.png" alt-text="Sélection de l’option copier la réponse" lightbox="../media/network-network-requests-copy-response.msft.png":::
   <span data-ttu-id="9f3cd-453">Figure 33: sélection de l’option **copier la réponse**</span><span class="sxs-lookup"><span data-stu-id="9f3cd-453">Figure 33:  Selecting **Copy Response**</span></span>  
:::image-end:::  

## <span data-ttu-id="9f3cd-454">Modifier la disposition du panneau réseau</span><span class="sxs-lookup"><span data-stu-id="9f3cd-454">Change the layout of the Network panel</span></span>  

<span data-ttu-id="9f3cd-455">Vous pouvez développer ou réduire des sections de l’interface utilisateur du panneau réseau pour cibler les informations importantes.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-455">You may expand or collapse sections of the Network panel UI to focus important information.</span></span>  

### <span data-ttu-id="9f3cd-456">Masquer le volet filtres</span><span class="sxs-lookup"><span data-stu-id="9f3cd-456">Hide the Filters pane</span></span>  

<span data-ttu-id="9f3cd-457">Par défaut, DevTools affiche le **volet filtres**.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-457">By default, DevTools shows the **Filters pane**.</span></span>  
<span data-ttu-id="9f3cd-458">Sélectionnez **Filter** ![ filtre ][ImageFilterIcon] de filtre pour le masquer.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-458">Select **Filter** ![Filter][ImageFilterIcon] to hide it.</span></span>  

:::image type="complex" source="../media/network-network-resources-hide-filters-button.msft.png" alt-text="Bouton Masquer les filtres" lightbox="../media/network-network-resources-hide-filters-button.msft.png":::
   <span data-ttu-id="9f3cd-460">Figure 34: bouton Masquer les filtres</span><span class="sxs-lookup"><span data-stu-id="9f3cd-460">Figure 34:  The Hide Filters button</span></span>  
:::image-end:::  

### <span data-ttu-id="9f3cd-461">Utiliser des lignes de requête volumineuses</span><span class="sxs-lookup"><span data-stu-id="9f3cd-461">Use large request rows</span></span>  

<span data-ttu-id="9f3cd-462">Utilisez des lignes de grande taille si vous voulez plus d’espace dans votre tableau de requêtes réseau.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-462">Use large rows when you want more whitespace in your network requests table.</span></span>  <span data-ttu-id="9f3cd-463">Certaines colonnes fournissent également quelques informations supplémentaires sur l’utilisation de lignes de grande taille.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-463">Some columns also provide a little more information when using large rows.</span></span>  <span data-ttu-id="9f3cd-464">Par exemple, la valeur la plus en bas de la colonne **taille** correspond à la taille de requête non compressée.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-464">For example, the bottom value of the **Size** column is the uncompressed size of a request.</span></span>  

:::image type="complex" source="../media/network-network-requests-large-request-rows.msft.png" alt-text="Exemple de longues lignes de requête dans le volet requêtes" lightbox="../media/network-network-requests-large-request-rows.msft.png":::
   <span data-ttu-id="9f3cd-466">Figure 35: exemple de longues lignes de requête dans le volet **requêtes**</span><span class="sxs-lookup"><span data-stu-id="9f3cd-466">Figure 35:  An example of large request rows in the **Requests** pane</span></span>  
:::image-end:::  

<span data-ttu-id="9f3cd-467">Activez la case à cocher **utiliser des lignes de requête volumineuses** pour activer les lignes de grande taille.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-467">Select the **Use large request rows** checkbox to enable large rows.</span></span>  

:::image type="complex" source="../media/network-network-requests-use-large-request-rows-on.msft.png" alt-text="Case à cocher utiliser de grandes lignes de requête" lightbox="../media/network-network-requests-use-large-request-rows-on.msft.png":::
   <span data-ttu-id="9f3cd-469">Figure 36: case à cocher **utiliser des lignes de requête volumineuses**</span><span class="sxs-lookup"><span data-stu-id="9f3cd-469">Figure 36:  The **Use large request rows** checkbox</span></span>  
:::image-end:::  

### <span data-ttu-id="9f3cd-470">Masquer le volet vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="9f3cd-470">Hide the Overview pane</span></span>  

<span data-ttu-id="9f3cd-471">Par défaut, DevTools affiche le **volet vue d’ensemble**.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-471">By default, DevTools shows the **Overview pane**.</span></span>  <span data-ttu-id="9f3cd-472">Désélectionnez la case à cocher **afficher la vue d’ensemble** pour la masquer.</span><span class="sxs-lookup"><span data-stu-id="9f3cd-472">Deselect the **Show Overview** checkbox to hide it.</span></span>  

:::image type="complex" source="../media/network-network-requests-show-overview-off.msft.png" alt-text="Case à cocher Afficher la vue d’ensemble" lightbox="../media/network-network-requests-show-overview-off.msft.png":::
   <span data-ttu-id="9f3cd-474">Figure 37: case à cocher **afficher la vue d’ensemble**</span><span class="sxs-lookup"><span data-stu-id="9f3cd-474">Figure 37:  The **Show Overview** checkbox</span></span>  
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
> <span data-ttu-id="9f3cd-478">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9f3cd-478">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="9f3cd-479">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/network/reference) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="9f3cd-479">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="9f3cd-481">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9f3cd-481">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
