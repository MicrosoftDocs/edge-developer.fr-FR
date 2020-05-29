---
title: Référence d’analyse du réseau
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 460ad05983e7615e8739953ce3cb7d559492bc90
ms.sourcegitcommit: 33663cd7838dddee86228dde469a5e9551bddb02
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611839"
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







# <span data-ttu-id="6454e-103">Référence d’analyse du réseau</span><span class="sxs-lookup"><span data-stu-id="6454e-103">Network Analysis Reference</span></span>   



<span data-ttu-id="6454e-104">Découvrez de nouvelles façons d’analyser le chargement de votre page dans cette référence complète des fonctionnalités d’analyse du réseau Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="6454e-104">Discover new ways to analyze how your page loads in this comprehensive reference of Microsoft Edge DevTools network analysis features.</span></span>  

<!--
> [!NOTE]
> This reference is based on Microsoft Edge 58.  If you use another version of Microsoft Edge, the UI, and features of DevTools may be different.  Check `edge://help` to see what version of Microsoft Edge you are running.  
-->

## <span data-ttu-id="6454e-105">Enregistrer les requêtes réseau</span><span class="sxs-lookup"><span data-stu-id="6454e-105">Record network requests</span></span>   

<span data-ttu-id="6454e-106">Par défaut, DevTools enregistre toutes les requêtes réseau dans le panneau réseau, tant que DevTools est ouvert.</span><span class="sxs-lookup"><span data-stu-id="6454e-106">By default, DevTools records all network requests in the Network panel, so long as DevTools is open.</span></span>  

> ##### <span data-ttu-id="6454e-107">Figure1</span><span class="sxs-lookup"><span data-stu-id="6454e-107">Figure 1</span></span>  
> <span data-ttu-id="6454e-108">Panneau réseau</span><span class="sxs-lookup"><span data-stu-id="6454e-108">The Network panel</span></span>  
> ![Panneau réseau][ImageNetworkPanel]  

### <span data-ttu-id="6454e-110">Arrêter l’enregistrement des requêtes réseau</span><span class="sxs-lookup"><span data-stu-id="6454e-110">Stop recording network requests</span></span>   

<span data-ttu-id="6454e-111">Pour arrêter l’enregistrement des demandes:</span><span class="sxs-lookup"><span data-stu-id="6454e-111">To stop recording requests:</span></span>  

*   <span data-ttu-id="6454e-112">Pour arrêter l' **enregistrement du journal du réseau** , cliquez sur arrêter l' ![ enregistrement réseau ][ImageRecordOnIcon] dans le panneau **réseau** .</span><span class="sxs-lookup"><span data-stu-id="6454e-112">Select **Stop recording network log** ![Stop recording network log][ImageRecordOnIcon] on the **Network** panel.</span></span>  <span data-ttu-id="6454e-113">Il devient gris pour indiquer que DevTools n’enregistre plus les demandes.</span><span class="sxs-lookup"><span data-stu-id="6454e-113">It turns grey to indicate that DevTools is no longer recording requests.</span></span>  
*   <span data-ttu-id="6454e-114">Appuyez sur `Control` + `E` \ (Windows \) ou `Command` + `E` \ (MacOS \) lorsque le panneau **réseau** a le focus.</span><span class="sxs-lookup"><span data-stu-id="6454e-114">Press `Control`+`E` \(Windows\) or `Command`+`E` \(macOS\) while the **Network** panel is in focus.</span></span>  

### <span data-ttu-id="6454e-115">Supprimer des demandes</span><span class="sxs-lookup"><span data-stu-id="6454e-115">Clear requests</span></span>   

<span data-ttu-id="6454e-116">Sélectionnez **Effacer** ![ ][ImageClearIcon] le panneau réseau pour effacer toutes les demandes de la table demandes.</span><span class="sxs-lookup"><span data-stu-id="6454e-116">Select **Clear** ![Clear][ImageClearIcon] on the Network panel to clear all requests from the Requests table.</span></span>  

> ##### <span data-ttu-id="6454e-117">Figure 2</span><span class="sxs-lookup"><span data-stu-id="6454e-117">Figure 2</span></span>  
> <span data-ttu-id="6454e-118">Bouton Effacer</span><span class="sxs-lookup"><span data-stu-id="6454e-118">The Clear button</span></span>  
> ![Bouton Effacer][ImageClearButton]  

### <span data-ttu-id="6454e-120">Enregistrer les demandes lors du chargement de la page</span><span class="sxs-lookup"><span data-stu-id="6454e-120">Save requests across page loads</span></span>   

<span data-ttu-id="6454e-121">Pour enregistrer les demandes lors du chargement de la page, activez la case à cocher **conservation du journal** dans le panneau réseau.</span><span class="sxs-lookup"><span data-stu-id="6454e-121">To save requests across page loads, check the **Preserve log** checkbox on the Network panel.</span></span>  <span data-ttu-id="6454e-122">DevTools enregistre toutes les demandes jusqu’à ce que vous désactiviez le **Journal de conservation**.</span><span class="sxs-lookup"><span data-stu-id="6454e-122">DevTools saves all requests until you disable **Preserve log**.</span></span>  

> ##### <span data-ttu-id="6454e-123">Figure3</span><span class="sxs-lookup"><span data-stu-id="6454e-123">Figure 3</span></span>  
> <span data-ttu-id="6454e-124">Case à cocher conserver le journal</span><span class="sxs-lookup"><span data-stu-id="6454e-124">The Preserve Log checkbox</span></span>  
> ![Case à cocher conserver le journal][ImagePreserveLogCheckBox]  

### <span data-ttu-id="6454e-126">Capture de captures d’écran pendant le chargement de la page</span><span class="sxs-lookup"><span data-stu-id="6454e-126">Capture screenshots during page load</span></span>   

<span data-ttu-id="6454e-127">Capture des captures d’écran pour analyser ce que les utilisateurs voient lorsqu’ils attendent que votre page se charge.</span><span class="sxs-lookup"><span data-stu-id="6454e-127">Capture screenshots to analyze what users see as they wait for your page to load.</span></span>  

<span data-ttu-id="6454e-128">Pour activer les captures d’écran, sélectionnez **paramètres du réseau** , puis cochez la case **capturer les captures d’écran** dans le panneau **réseau** .</span><span class="sxs-lookup"><span data-stu-id="6454e-128">To enable screenshots, select **Network settings** and select **Capture screenshots** checkbox on the **Network** panel.</span></span>  

<span data-ttu-id="6454e-129">Rechargez la page lorsque le panneau **réseau** a le focus pour capturer les captures d’écran.</span><span class="sxs-lookup"><span data-stu-id="6454e-129">Reload the page while the **Network** panel is in focus to capture screenshots.</span></span>  

<span data-ttu-id="6454e-130">Après avoir capturé une capture d’écran, vous interagissez comme suit.</span><span class="sxs-lookup"><span data-stu-id="6454e-130">After capturing a screenshot, you interact with it in the following ways.</span></span>  

*   <span data-ttu-id="6454e-131">Placez le pointeur de la souris sur une capture d’écran pour afficher le point d’acquisition de cette capture d’écran.</span><span class="sxs-lookup"><span data-stu-id="6454e-131">Hover over a screenshot to view the point at which that screenshot was captured.</span></span>  <span data-ttu-id="6454e-132">Une ligne jaune apparaît dans le volet **vue d’ensemble** .</span><span class="sxs-lookup"><span data-stu-id="6454e-132">A yellow line appears on the **Overview** pane.</span></span>  
*   <span data-ttu-id="6454e-133">Sélectionnez la miniature d’un écran pour filtrer toutes les demandes qui se sont produites après la capture de la capture d’écran.</span><span class="sxs-lookup"><span data-stu-id="6454e-133">Select the thumbnail of a screen to filter out any requests that occurred after the screenshot was captured.</span></span>  
*   <span data-ttu-id="6454e-134">Double-cliquez sur une miniature pour effectuer un zoom sur celle-ci.</span><span class="sxs-lookup"><span data-stu-id="6454e-134">Double-click a thumbnail to zoom in on it.</span></span>  

> ##### <span data-ttu-id="6454e-135">Figure 4</span><span class="sxs-lookup"><span data-stu-id="6454e-135">Figure 4</span></span>  
> <span data-ttu-id="6454e-136">Survol d’une capture d’écran</span><span class="sxs-lookup"><span data-stu-id="6454e-136">Hovering over a screenshot</span></span>  
> ![Survol d’une capture d’écran][ImageScreenshotHover]  

<!--  ### Replay XHR request   -->

<!--  To replay an XHR request, right-click the request in the Requests table and select **Replay XHR**.  -->

<!--  
> ##### Old Figure 5  
> Selecting Replay XHR  
> ![Selecting Replay XHR][ImageReplayXHR]  
-->  

## <span data-ttu-id="6454e-138">Changer le comportement de chargement</span><span class="sxs-lookup"><span data-stu-id="6454e-138">Change loading behavior</span></span>  

### <span data-ttu-id="6454e-139">Émuler un visiteur pour la première fois en désactivant le cache du navigateur</span><span class="sxs-lookup"><span data-stu-id="6454e-139">Emulate a first-time visitor by disabling the browser cache</span></span>   

<span data-ttu-id="6454e-140">Pour émuler la façon dont un utilisateur a expériences de votre site pour la première fois, activez la case à cocher **désactiver le cache** .</span><span class="sxs-lookup"><span data-stu-id="6454e-140">To emulate how a first-time user experiences your site, check the **Disable cache** checkbox.</span></span>  <span data-ttu-id="6454e-141">DevTools désactive le cache du navigateur.</span><span class="sxs-lookup"><span data-stu-id="6454e-141">DevTools disables the browser cache.</span></span>  <span data-ttu-id="6454e-142">Cela a pour effet d’émuler de façon plus précise une première utilisation de l’utilisateur, car les requêtes sont servies dans le cache du navigateur sur les visites répétées.</span><span class="sxs-lookup"><span data-stu-id="6454e-142">This more accurately emulates a first-time user's experience, because requests are served from the browser cache on repeat visits.</span></span>  

> ##### <span data-ttu-id="6454e-143">Figure 5</span><span class="sxs-lookup"><span data-stu-id="6454e-143">Figure 5</span></span>  
> <span data-ttu-id="6454e-144">Case à cocher Désactiver le cache</span><span class="sxs-lookup"><span data-stu-id="6454e-144">The Disable Cache checkbox</span></span>  
> <span data-ttu-id="6454e-145">! [Case à cocher Désactiver le cache] [ImageDisableCacheCheckBox]</span><span class="sxs-lookup"><span data-stu-id="6454e-145">![The Disable Cache checkbox][ImageDisableCacheCheckBox]</span></span>  

#### <span data-ttu-id="6454e-146">Désactiver le cache du navigateur dans le tiroir du réseau</span><span class="sxs-lookup"><span data-stu-id="6454e-146">Disable the browser cache from the Network Conditions drawer</span></span>   

<span data-ttu-id="6454e-147">Si vous voulez désactiver le cache lorsque vous travaillez dans d’autres panneaux DevTools, utilisez le tiroir de l’état du réseau.</span><span class="sxs-lookup"><span data-stu-id="6454e-147">If you want to disable the cache while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="6454e-148">Ouvrez le tiroir de **conditions du réseau** .</span><span class="sxs-lookup"><span data-stu-id="6454e-148">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="6454e-149">Cochez ou décochez la case **désactiver le cache** .</span><span class="sxs-lookup"><span data-stu-id="6454e-149">Check or uncheck the **Disable cache** checkbox.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="6454e-150">Vider manuellement le cache du navigateur</span><span class="sxs-lookup"><span data-stu-id="6454e-150">Manually clear the browser cache</span></span>   

<span data-ttu-id="6454e-151">Pour vider manuellement le cache du navigateur à tout moment, cliquez avec le bouton droit n’importe où dans la table demandes et sélectionnez **Vider le cache du navigateur**.</span><span class="sxs-lookup"><span data-stu-id="6454e-151">To manually clear the browser cache at any time, right-click anywhere in the Requests table and select **Clear Browser Cache**.</span></span>  

> ##### <span data-ttu-id="6454e-152">Figure 6</span><span class="sxs-lookup"><span data-stu-id="6454e-152">Figure 6</span></span>  
> <span data-ttu-id="6454e-153">Sélection de l’option vider le cache du navigateur</span><span class="sxs-lookup"><span data-stu-id="6454e-153">Selecting Clear Browser Cache</span></span>  
> <span data-ttu-id="6454e-154">! [Sélection de l’option vider le cache du navigateur] [ImageClearBrowserCache]</span><span class="sxs-lookup"><span data-stu-id="6454e-154">![Selecting Clear Browser Cache][ImageClearBrowserCache]</span></span>  

### <span data-ttu-id="6454e-155">Émuler hors connexion</span><span class="sxs-lookup"><span data-stu-id="6454e-155">Emulate offline</span></span>   

<span data-ttu-id="6454e-156">Une nouvelle classe d’applications Web, appelée [application Web progressive][DevtoolsProgressiveWebApps], fonctionne en mode hors connexion avec l’aide des **travailleurs de service**.</span><span class="sxs-lookup"><span data-stu-id="6454e-156">A new class of web apps, called [Progressive Web Apps][DevtoolsProgressiveWebApps], functions offline with the help of **service workers**.</span></span>  <span data-ttu-id="6454e-157">Vous constaterez peut-être qu’il est utile de simuler rapidement un appareil dépourvu de connexion aux données lors de la création de ce type d’application.</span><span class="sxs-lookup"><span data-stu-id="6454e-157">You may find it useful to quickly simulate a device that has no data connection when you are building this type of app.</span></span>  

<!--[ServiceWorkers]: /web/fundamentals/getting-started/primers/service-workers  -->

<span data-ttu-id="6454e-158">Sélectionnez le menu déroulant **en ligne** , Rechercher sous **présélections**, puis sélectionnez **hors ligne** pour simuler une interface réseau entièrement hors connexion.</span><span class="sxs-lookup"><span data-stu-id="6454e-158">Select the **Online** dropdown menu, search under **Presets**, and select **Offline** to simulate a completely offline network experience.</span></span>  

> ##### <span data-ttu-id="6454e-159">Figure 7</span><span class="sxs-lookup"><span data-stu-id="6454e-159">Figure 7</span></span>  
> <span data-ttu-id="6454e-160">Menu déroulant hors connexion</span><span class="sxs-lookup"><span data-stu-id="6454e-160">The Offline dropdown menu</span></span>  
> <span data-ttu-id="6454e-161">! [Menu déroulant hors ligne] [ImageOfflineDropdown]</span><span class="sxs-lookup"><span data-stu-id="6454e-161">![The Offline dropdown menu][ImageOfflineDropdown]</span></span>  

### <span data-ttu-id="6454e-162">Émuler une connexion réseau lente</span><span class="sxs-lookup"><span data-stu-id="6454e-162">Emulate slow network connections</span></span>   

<span data-ttu-id="6454e-163">Émulez des vitesses de connexion 3G, Fast 3G et autres vitesses de connexion dans le menu déroulant **en ligne** .</span><span class="sxs-lookup"><span data-stu-id="6454e-163">Emulate Slow 3G, Fast 3G, and other connection speeds from the **Online** dropdown menu.</span></span>  

> ##### <span data-ttu-id="6454e-164">Figure8</span><span class="sxs-lookup"><span data-stu-id="6454e-164">Figure 8</span></span>  
> <span data-ttu-id="6454e-165">Menu déroulant limitation</span><span class="sxs-lookup"><span data-stu-id="6454e-165">The Throttling dropdown menu</span></span>  
> <span data-ttu-id="6454e-166">! [Menu déroulant limitation] [ImageNetworkThrottlingMenu]</span><span class="sxs-lookup"><span data-stu-id="6454e-166">![The Throttling dropdown menu][ImageNetworkThrottlingMenu]</span></span>  

<span data-ttu-id="6454e-167">Vous pouvez faire votre choix parmi une série de présélections, par exemple, lente 3G ou Fast 3G.</span><span class="sxs-lookup"><span data-stu-id="6454e-167">You may select from a variety of presets, such as Slow 3G or Fast 3G.</span></span>  <span data-ttu-id="6454e-168">Vous pouvez également ajouter vos propres Présélections personnalisées en ouvrant le menu limitation et **Custom**en sélectionnant  >  **Ajouter**personnalisé.</span><span class="sxs-lookup"><span data-stu-id="6454e-168">You may also add your own custom presets by opening the Throttling menu and selecting **Custom** > **Add**.</span></span>  

<span data-ttu-id="6454e-169">DevTools affiche une icône d’avertissement en regard de l’onglet **réseau** pour vous rappeler que la limitation est activée.</span><span class="sxs-lookup"><span data-stu-id="6454e-169">DevTools displays a warning icon next to the **Network** tab to remind you that throttling is enabled.</span></span>  

#### <span data-ttu-id="6454e-170">Émuler une connexion réseau lente à partir du tiroir du réseau</span><span class="sxs-lookup"><span data-stu-id="6454e-170">Emulate slow network connections from the Network Conditions drawer</span></span>   

<span data-ttu-id="6454e-171">Si vous souhaitez limiter la connexion réseau lorsque vous travaillez dans d’autres panneaux DevTools, utilisez le tiroir de l’état du réseau.</span><span class="sxs-lookup"><span data-stu-id="6454e-171">If you want to throttle the network connection while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="6454e-172">Ouvrez le tiroir de **conditions du réseau** .</span><span class="sxs-lookup"><span data-stu-id="6454e-172">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="6454e-173">Sélectionnez le débit de connexion souhaité dans le menu **limitation** .</span><span class="sxs-lookup"><span data-stu-id="6454e-173">Select your desired connection speed from the **Throttling** menu.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="6454e-174">Effacement manuel des cookies du navigateur</span><span class="sxs-lookup"><span data-stu-id="6454e-174">Manually clear browser cookies</span></span>   

<span data-ttu-id="6454e-175">Pour effacer manuellement les cookies du navigateur à tout moment, cliquez avec le bouton droit n’importe où dans la table demandes, puis sélectionnez **effacer les cookies du navigateur**.</span><span class="sxs-lookup"><span data-stu-id="6454e-175">To manually clear browser cookies at any time, right-click anywhere in the Requests table and select **Clear Browser Cookies**.</span></span>  

> ##### <span data-ttu-id="6454e-176">Figure9</span><span class="sxs-lookup"><span data-stu-id="6454e-176">Figure 9</span></span>  
> <span data-ttu-id="6454e-177">Sélection effacer les cookies du navigateur</span><span class="sxs-lookup"><span data-stu-id="6454e-177">Selecting Clear Browser Cookies</span></span>  
> <span data-ttu-id="6454e-178">! [Sélectionner des cookies de navigateur clairs] [ImageClearBrowserCookies]</span><span class="sxs-lookup"><span data-stu-id="6454e-178">![Selecting Clear Browser Cookies][ImageClearBrowserCookies]</span></span>  

### <span data-ttu-id="6454e-179">Remplacer l’agent utilisateur</span><span class="sxs-lookup"><span data-stu-id="6454e-179">Override the user agent</span></span>   

<span data-ttu-id="6454e-180">Pour remplacer manuellement l’agent utilisateur, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="6454e-180">To manually override the user agent:</span></span>  

1.  <span data-ttu-id="6454e-181">Ouvrez le tiroir de **conditions du réseau** .</span><span class="sxs-lookup"><span data-stu-id="6454e-181">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="6454e-182">Décochez l' **option sélectionner automatiquement**.</span><span class="sxs-lookup"><span data-stu-id="6454e-182">Uncheck **Select automatically**.</span></span>  
1.  <span data-ttu-id="6454e-183">Choisissez une option de l’agent utilisateur dans le menu ou entrez-en un dans la zone de texte.</span><span class="sxs-lookup"><span data-stu-id="6454e-183">Choose a user agent option from the menu, or enter a custom one in the text box.</span></span>  

<!--todo: add network condition section when available -->  

## <span data-ttu-id="6454e-184">Demandes de filtre</span><span class="sxs-lookup"><span data-stu-id="6454e-184">Filter requests</span></span>   

### <span data-ttu-id="6454e-185">Filtrer les demandes par propriétés</span><span class="sxs-lookup"><span data-stu-id="6454e-185">Filter requests by properties</span></span>   

<span data-ttu-id="6454e-186">Utilisez la zone de texte **filtre** pour filtrer les demandes par propriétés, telles que le domaine ou la taille de la requête.</span><span class="sxs-lookup"><span data-stu-id="6454e-186">Use the **Filter** text box to filter requests by properties, such as the domain or size of the request.</span></span>  

<span data-ttu-id="6454e-187">Si vous ne voyez pas la zone de texte, le volet filtres est probablement masqué.</span><span class="sxs-lookup"><span data-stu-id="6454e-187">If you do not see the text box, the Filters pane is probably hidden.</span></span>  
<span data-ttu-id="6454e-188">Voir [masquer le volet filtres](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="6454e-188">See [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

> ##### <span data-ttu-id="6454e-189">Figure10</span><span class="sxs-lookup"><span data-stu-id="6454e-189">Figure 10</span></span>  
> <span data-ttu-id="6454e-190">Zone de texte filtres</span><span class="sxs-lookup"><span data-stu-id="6454e-190">The Filters text box</span></span>  
> <span data-ttu-id="6454e-191">! [Zone de texte filtres] [ImageFilterTextBox]</span><span class="sxs-lookup"><span data-stu-id="6454e-191">![The Filters text box][ImageFilterTextBox]</span></span>  

<span data-ttu-id="6454e-192">Vous pouvez utiliser plusieurs propriétés simultanément en séparant chaque propriété d’un espace.</span><span class="sxs-lookup"><span data-stu-id="6454e-192">You may use multiple properties simultaneously by separating each property with a space.</span></span>  <span data-ttu-id="6454e-193">Par exemple, `mime-type:image/png larger-than:1K` affiche tous les png dont la taille est supérieure à 1 Ko.</span><span class="sxs-lookup"><span data-stu-id="6454e-193">For example, `mime-type:image/png larger-than:1K` displays all PNGs that are larger than one kilobyte.</span></span>  <span data-ttu-id="6454e-194">Ces filtres multi-propriété sont équivalents aux `AND` opérations.</span><span class="sxs-lookup"><span data-stu-id="6454e-194">These multi-property filters are equivalent to `AND` operations.</span></span>  `OR` <span data-ttu-id="6454e-195">les opérations ne sont actuellement pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="6454e-195">operations are currently not supported.</span></span>  

<span data-ttu-id="6454e-196">Liste complète des propriétés prises en charge.</span><span class="sxs-lookup"><span data-stu-id="6454e-196">The complete list of supported properties.</span></span>  

| <span data-ttu-id="6454e-197">Propriété</span><span class="sxs-lookup"><span data-stu-id="6454e-197">Property</span></span> | <span data-ttu-id="6454e-198">Détails</span><span class="sxs-lookup"><span data-stu-id="6454e-198">Details</span></span> |  
|:--- | :--- |  
| `domain` | <span data-ttu-id="6454e-199">Afficher uniquement les ressources du domaine spécifié.</span><span class="sxs-lookup"><span data-stu-id="6454e-199">Only display resources from the specified domain.</span></span>  <span data-ttu-id="6454e-200">Vous pouvez utiliser un caractère générique \ ( `*` \) pour inclure plusieurs domaines.</span><span class="sxs-lookup"><span data-stu-id="6454e-200">You may use a wildcard character \(`*`\) to include multiple domains.</span></span>  <span data-ttu-id="6454e-201">Par exemple, `*.com` affiche les ressources de tous les noms de domaine se terminant par `.com` .</span><span class="sxs-lookup"><span data-stu-id="6454e-201">For example, `*.com` displays resources from all domain names ending in `.com`.</span></span>  <span data-ttu-id="6454e-202">DevTools remplit le menu déroulant de saisie semi-automatique avec tous les domaines qu’il a rencontré.</span><span class="sxs-lookup"><span data-stu-id="6454e-202">DevTools populates the autocomplete dropdown menu with all of the domains it has encountered.</span></span> |  
| `has-response-header` | <span data-ttu-id="6454e-203">Afficher les ressources qui contiennent l’en-tête de réponse HTTP spécifié.</span><span class="sxs-lookup"><span data-stu-id="6454e-203">Show the resources that contain the specified HTTP response header.</span></span>  <span data-ttu-id="6454e-204">DevTools remplit la liste déroulante de saisie semi-automatique avec tous les en-têtes de réponse qu’il a rencontré.</span><span class="sxs-lookup"><span data-stu-id="6454e-204">DevTools populates the autocomplete dropdown with all of the response headers that it has encountered.</span></span> |  
| `is` | <span data-ttu-id="6454e-205">Utiliser `is:running` pour rechercher des `WebSocket` ressources.</span><span class="sxs-lookup"><span data-stu-id="6454e-205">Use `is:running` to find `WebSocket` resources.</span></span> |  
| `larger-than` | <span data-ttu-id="6454e-206">Afficher les ressources dont la taille est supérieure à la taille spécifiée, en octets.</span><span class="sxs-lookup"><span data-stu-id="6454e-206">Show resources that are larger than the specified size, in bytes.</span></span>  <span data-ttu-id="6454e-207">La définition d’une valeur est égale à la valeur `1000` `1k` .</span><span class="sxs-lookup"><span data-stu-id="6454e-207">Setting a value of `1000` is equivalent to setting a value of `1k`.</span></span> |  
| `method` | <span data-ttu-id="6454e-208">Afficher les ressources récupérées sur un type de méthode HTTP spécifié.</span><span class="sxs-lookup"><span data-stu-id="6454e-208">Show resources that were retrieved over a specified HTTP method type.</span></span>  <span data-ttu-id="6454e-209">DevTools remplit la liste déroulante avec toutes les méthodes HTTP qu’il a rencontrées.</span><span class="sxs-lookup"><span data-stu-id="6454e-209">DevTools populates the dropdown with all of the HTTP methods it has encountered.</span></span> |  
| `mime-type` | <span data-ttu-id="6454e-210">Afficher les ressources d’un type MIME spécifié.</span><span class="sxs-lookup"><span data-stu-id="6454e-210">Show resources of a specified MIME type.</span></span>  <span data-ttu-id="6454e-211">DevTools remplit la liste déroulante avec tous les types MIME qu’il a rencontré.</span><span class="sxs-lookup"><span data-stu-id="6454e-211">DevTools populates the dropdown with all MIME types it has encountered.</span></span> |  
| `mixed-content` | <span data-ttu-id="6454e-212">Affichez toutes les ressources de contenu mixte \ ( `mixed-content:all` \) ou uniquement celles actuellement affichées \ ( `mixed-content:displayed` \).</span><span class="sxs-lookup"><span data-stu-id="6454e-212">Show all mixed content resources \(`mixed-content:all`\) or just the ones that are currently displayed \(`mixed-content:displayed`\).</span></span> |  
| `scheme` | <span data-ttu-id="6454e-213">Afficher les ressources récupérées sur une connexion HTTP \ ( `scheme:http` \) ou protégé https \ ( `scheme:https` \).</span><span class="sxs-lookup"><span data-stu-id="6454e-213">Show resources retrieved over unprotected HTTP \(`scheme:http`\) or protected HTTPS \(`scheme:https`\).</span></span> |  
| `set-cookie-domain` | <span data-ttu-id="6454e-214">Afficher les ressources qui ont un `Set-Cookie` en-tête avec un `Domain` attribut qui correspond à la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6454e-214">Show the resources that have a `Set-Cookie` header with a `Domain` attribute that matches the specified value.</span></span>  <span data-ttu-id="6454e-215">DevTools remplit la saisie semi-automatique avec tous les domaines de cookie qu’il a rencontré.</span><span class="sxs-lookup"><span data-stu-id="6454e-215">DevTools populates the autocomplete with all of the cookie domains that it has encountered.</span></span> |  
| `set-cookie-name` | <span data-ttu-id="6454e-216">Afficher les ressources possédant un `Set-Cookie` en-tête dont le nom correspond à la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6454e-216">Show the resources that have a `Set-Cookie` header with a name that matches the specified value.</span></span>  <span data-ttu-id="6454e-217">DevTools remplit la saisie semi-automatique avec tous les noms de cookie qu’il a rencontré.</span><span class="sxs-lookup"><span data-stu-id="6454e-217">DevTools populates the autocomplete with all of the cookie names that it has encountered.</span></span> |  
| `set-cookie-value` | <span data-ttu-id="6454e-218">Afficher les ressources dont l' `Set-Cookie` en-tête comporte une valeur qui correspond à la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6454e-218">Show the resources that have a `Set-Cookie` header with a value that matches the specified value.</span></span>  <span data-ttu-id="6454e-219">DevTools remplit la saisie semi-automatique avec toutes les valeurs de cookie qu’il a rencontrées.</span><span class="sxs-lookup"><span data-stu-id="6454e-219">DevTools populates the autocomplete with all of the cookie values that it has encountered.</span></span> |  
| `status-code` | <span data-ttu-id="6454e-220">Afficher uniquement les ressources pour lesquelles le code d’état HTTP correspond au code spécifié.</span><span class="sxs-lookup"><span data-stu-id="6454e-220">Show only the resources for which the HTTP status code matches the specified code.</span></span>  <span data-ttu-id="6454e-221">DevTools remplit le menu déroulant de saisie semi-automatique avec tous les codes d’État détectés.</span><span class="sxs-lookup"><span data-stu-id="6454e-221">DevTools populates the autocomplete dropdown menu with all of the status codes it has encountered.</span></span> |  

### <span data-ttu-id="6454e-222">Filtrer les demandes par type</span><span class="sxs-lookup"><span data-stu-id="6454e-222">Filter requests by type</span></span>   

<span data-ttu-id="6454e-223">Pour filtrer les demandes par type de requête, sélectionnez les boutons **XHR**, **js**, **CSS**, **img**, **multimédia**, **police**, **doc**, **WS** \ (WebSocket \), **manifeste**ou **autre** (n’importe quel autre type non répertorié ici \) sur le panneau réseau.</span><span class="sxs-lookup"><span data-stu-id="6454e-223">To filter requests by request type, select the **XHR**, **JS**, **CSS**, **Img**, **Media**, **Font**, **Doc**, **WS** \(WebSocket\), **Manifest**, or **Other** \(any other type not listed here\) buttons on the Network panel.</span></span>  

<span data-ttu-id="6454e-224">Si vous ne voyez pas ces boutons, le volet filtres est probablement masqué.</span><span class="sxs-lookup"><span data-stu-id="6454e-224">If you do not see these buttons, the Filters pane is probably hidden.</span></span>  
<span data-ttu-id="6454e-225">Voir [masquer le volet filtres](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="6454e-225">See [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

<span data-ttu-id="6454e-226">Pour activer plusieurs filtres de type simultanément, appuyez sur `Control` \ (Windows \) ou `Command` \ (MacOS \), puis sélectionnez.</span><span class="sxs-lookup"><span data-stu-id="6454e-226">To enable multiple type filters simultaneously, hold `Control` \(Windows\) or `Command` \(macOS\) and then select.</span></span>  

> ##### <span data-ttu-id="6454e-227">Figure11</span><span class="sxs-lookup"><span data-stu-id="6454e-227">Figure 11</span></span>  
> <span data-ttu-id="6454e-228">Utiliser les filtres de type pour afficher les ressources JS, CSS et document</span><span class="sxs-lookup"><span data-stu-id="6454e-228">Using the Type filters to display JS, CSS, and Document resources</span></span>  
> <span data-ttu-id="6454e-229">! [En utilisant les filtres de type pour afficher les ressources JS, CSS et documents] [ImageMultiTypeFilter]</span><span class="sxs-lookup"><span data-stu-id="6454e-229">![Using the Type filters to display JS, CSS, and Document resources][ImageMultiTypeFilter]</span></span>  

### <span data-ttu-id="6454e-230">Filtrer les demandes par heure</span><span class="sxs-lookup"><span data-stu-id="6454e-230">Filter requests by time</span></span>   

<span data-ttu-id="6454e-231">Sélectionnez et faites glisser vers la gauche ou la droite dans le volet vue d’ensemble pour afficher uniquement les demandes actives au cours de cette période.</span><span class="sxs-lookup"><span data-stu-id="6454e-231">Select and drag left or right on the Overview pane to only display requests that were active during that time frame.</span></span>  <span data-ttu-id="6454e-232">Le filtre est inclusive.</span><span class="sxs-lookup"><span data-stu-id="6454e-232">The filter is inclusive.</span></span>  <span data-ttu-id="6454e-233">Toutes les demandes qui ont été actives pendant la durée en surbrillance apparaissent.</span><span class="sxs-lookup"><span data-stu-id="6454e-233">Any request that was active during the highlighted time is shown.</span></span>  

> ##### <span data-ttu-id="6454e-234">Figure12</span><span class="sxs-lookup"><span data-stu-id="6454e-234">Figure 12</span></span>  
> <span data-ttu-id="6454e-235">Filtrage des requêtes inactives depuis 300M</span><span class="sxs-lookup"><span data-stu-id="6454e-235">Filtering out any requests that were inactive around 300ms</span></span>  
> <span data-ttu-id="6454e-236">! [Filtrage des requêtes inactives depuis 300M] [ImageOverviewFilter]</span><span class="sxs-lookup"><span data-stu-id="6454e-236">![Filtering out any requests that were inactive around 300ms][ImageOverviewFilter]</span></span>  

### <span data-ttu-id="6454e-237">Masquer les URL de données</span><span class="sxs-lookup"><span data-stu-id="6454e-237">Hide data URLs</span></span>  

<span data-ttu-id="6454e-238">Les [URL de données][MDNHTTPDataURIs] sont des petits fichiers incorporés dans d’autres documents.</span><span class="sxs-lookup"><span data-stu-id="6454e-238">[Data URLs][MDNHTTPDataURIs] are small files embedded into other documents.</span></span>  <span data-ttu-id="6454e-239">Toute demande figurant dans la table demandes qui commence par `data:` est une URL de données.</span><span class="sxs-lookup"><span data-stu-id="6454e-239">Any request that you see in the Requests table that starts with `data:` is a data URL.</span></span>  

<span data-ttu-id="6454e-240">Cochez la case **Masquer les URL de données** pour masquer ces demandes.</span><span class="sxs-lookup"><span data-stu-id="6454e-240">Check the **Hide data URLs** checkbox to hide these requests.</span></span>  

> ##### <span data-ttu-id="6454e-241">Figure13</span><span class="sxs-lookup"><span data-stu-id="6454e-241">Figure 13</span></span>  
> <span data-ttu-id="6454e-242">Case à cocher Masquer les URL de données</span><span class="sxs-lookup"><span data-stu-id="6454e-242">The Hide Data URLs checkbox</span></span>  
> <span data-ttu-id="6454e-243">! [Cases à cocher Masquer les URL de données] [ImageHideDataURLsCheckBox]</span><span class="sxs-lookup"><span data-stu-id="6454e-243">![The Hide Data URLs checkbox][ImageHideDataURLsCheckBox]</span></span>  

## <span data-ttu-id="6454e-244">Demandes de tri</span><span class="sxs-lookup"><span data-stu-id="6454e-244">Sort requests</span></span>  

<span data-ttu-id="6454e-245">Par défaut, les requêtes dans la table demandes sont triées par heure de début, mais vous pouvez trier le tableau en utilisant d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="6454e-245">By default, the requests in the Requests table are sorted by initiation time, but you may sort the table using other criteria.</span></span>  

### <span data-ttu-id="6454e-246">Trier par colonne</span><span class="sxs-lookup"><span data-stu-id="6454e-246">Sort by column</span></span>   

<span data-ttu-id="6454e-247">Sélectionnez l’en-tête de n’importe quelle colonne dans les requêtes pour trier les demandes en se sur cette colonne.</span><span class="sxs-lookup"><span data-stu-id="6454e-247">Select the header of any column in the Requests to sort requests by that column.</span></span>  

### <span data-ttu-id="6454e-248">Trier par phase d’activité</span><span class="sxs-lookup"><span data-stu-id="6454e-248">Sort by activity phase</span></span>   

<span data-ttu-id="6454e-249">Pour modifier la façon dont les demandes de tri en cascade trient, cliquez avec le bouton droit sur l’en-tête de la table demandes, placez le pointeur sur **cascade**, puis sélectionnez l’une des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="6454e-249">To change how the Waterfall sorts requests, right-click the header of the Requests table, hover over **Waterfall**, and select one of the following options.</span></span>  

*   <span data-ttu-id="6454e-250">**Heure de début**.</span><span class="sxs-lookup"><span data-stu-id="6454e-250">**Start Time**.</span></span>  <span data-ttu-id="6454e-251">La première requête lancée est en haut.</span><span class="sxs-lookup"><span data-stu-id="6454e-251">The first request that was initiated is at the top.</span></span>  
*   <span data-ttu-id="6454e-252">**Temps de réponse**.</span><span class="sxs-lookup"><span data-stu-id="6454e-252">**Response Time**.</span></span>  <span data-ttu-id="6454e-253">La première demande qui a démarré le téléchargement est en haut.</span><span class="sxs-lookup"><span data-stu-id="6454e-253">The first request that started downloading is at the top.</span></span>  
*   <span data-ttu-id="6454e-254">**Heure de fin**.</span><span class="sxs-lookup"><span data-stu-id="6454e-254">**End Time**.</span></span>  <span data-ttu-id="6454e-255">La première demande qui est terminée est en haut.</span><span class="sxs-lookup"><span data-stu-id="6454e-255">The first request that finished is at the top.</span></span>  
*   <span data-ttu-id="6454e-256">**Durée totale**.</span><span class="sxs-lookup"><span data-stu-id="6454e-256">**Total Duration**.</span></span>  <span data-ttu-id="6454e-257">La requête avec la configuration de connexion la plus courte et la demande/réponse se trouvent dans la partie supérieure.</span><span class="sxs-lookup"><span data-stu-id="6454e-257">The request with the shortest connection setup and request / response is at the top.</span></span>  
*   <span data-ttu-id="6454e-258">**Latence**.</span><span class="sxs-lookup"><span data-stu-id="6454e-258">**Latency**.</span></span>  <span data-ttu-id="6454e-259">La requête qui a attendu le plus court délai d’une réponse est située en haut.</span><span class="sxs-lookup"><span data-stu-id="6454e-259">The request that waited the shortest time for a response is at the top.</span></span>  

<span data-ttu-id="6454e-260">Ces descriptions présupposent que chaque option respective est classée du plus court au plus long.</span><span class="sxs-lookup"><span data-stu-id="6454e-260">These descriptions assume that each respective option is ranked from shortest to longest.</span></span>  <span data-ttu-id="6454e-261">La sélection de l’en-tête de la colonne en **cascade** inverse l’ordre.</span><span class="sxs-lookup"><span data-stu-id="6454e-261">Selecting the header of the **Waterfall** column reverses the order.</span></span>  

> ##### <span data-ttu-id="6454e-262">Figure14</span><span class="sxs-lookup"><span data-stu-id="6454e-262">Figure 14</span></span>  
> <span data-ttu-id="6454e-263">Le tri des cascades en fonction de la durée totale \ (la partie la plus claire de chaque barre est le temps passé en attente et la partie plus foncée est le temps de télécharger les octets \)</span><span class="sxs-lookup"><span data-stu-id="6454e-263">Sorting the Waterfall by total duration  \(The lighter portion of each bar is time spent waiting and the darker portion is time spent downloading bytes\)</span></span>  
> <span data-ttu-id="6454e-264">! [Trier les cascade en fonction de la durée totale] [ImageWaterfallTotalDuration]</span><span class="sxs-lookup"><span data-stu-id="6454e-264">![Sorting the Waterfall by total duration][ImageWaterfallTotalDuration]</span></span>  

## <span data-ttu-id="6454e-265">Analyser les requêtes</span><span class="sxs-lookup"><span data-stu-id="6454e-265">Analyze requests</span></span>   

<span data-ttu-id="6454e-266">Tant que DevTools est ouvert, il enregistre toutes les demandes dans le panneau réseau.</span><span class="sxs-lookup"><span data-stu-id="6454e-266">So long as DevTools is open, it logs all requests in the Network panel.</span></span>  
<span data-ttu-id="6454e-267">Utilisez le volet réseau pour analyser les requêtes.</span><span class="sxs-lookup"><span data-stu-id="6454e-267">Use the Network panel to analyze requests.</span></span>  

### <span data-ttu-id="6454e-268">Afficher un journal des demandes</span><span class="sxs-lookup"><span data-stu-id="6454e-268">View a log of requests</span></span>   

<span data-ttu-id="6454e-269">Utilisez le tableau demandes pour afficher un journal de toutes les demandes effectuées lorsque DevTools est ouvert.</span><span class="sxs-lookup"><span data-stu-id="6454e-269">Use the Requests table to view a log of all requests made while DevTools has been open.</span></span>  <span data-ttu-id="6454e-270">La sélection ou le passage de demandes au-dessus révèle des informations supplémentaires sur chaque élément.</span><span class="sxs-lookup"><span data-stu-id="6454e-270">Selecting or hovering over requests reveals more information about each item.</span></span>  

> ##### <span data-ttu-id="6454e-271">Figure15</span><span class="sxs-lookup"><span data-stu-id="6454e-271">Figure 15</span></span>  
> <span data-ttu-id="6454e-272">Table demandes</span><span class="sxs-lookup"><span data-stu-id="6454e-272">The Requests table</span></span>  
> <span data-ttu-id="6454e-273">! [Table demandes] [ImageRequestsTable]</span><span class="sxs-lookup"><span data-stu-id="6454e-273">![The Requests table][ImageRequestsTable]</span></span>  

<span data-ttu-id="6454e-274">La table demandes affiche les colonnes suivantes par défaut:</span><span class="sxs-lookup"><span data-stu-id="6454e-274">The Requests table displays the following columns by default:</span></span>  

*   <span data-ttu-id="6454e-275">**Nom**.</span><span class="sxs-lookup"><span data-stu-id="6454e-275">**Name**.</span></span>  <span data-ttu-id="6454e-276">Nom de fichier ou un identificateur pour la ressource.</span><span class="sxs-lookup"><span data-stu-id="6454e-276">The filename of, or an identifier for, the resource.</span></span>  
*   <span data-ttu-id="6454e-277">**Status**.</span><span class="sxs-lookup"><span data-stu-id="6454e-277">**Status**.</span></span>  <span data-ttu-id="6454e-278">Code d’état HTTP.</span><span class="sxs-lookup"><span data-stu-id="6454e-278">The HTTP status code.</span></span>  
*   <span data-ttu-id="6454e-279">**Type**.</span><span class="sxs-lookup"><span data-stu-id="6454e-279">**Type**.</span></span>  <span data-ttu-id="6454e-280">Type MIME de la ressource demandée.</span><span class="sxs-lookup"><span data-stu-id="6454e-280">The MIME type of the requested resource.</span></span>  
*   <span data-ttu-id="6454e-281">**Initiator**.</span><span class="sxs-lookup"><span data-stu-id="6454e-281">**Initiator**.</span></span>  <span data-ttu-id="6454e-282">Les requêtes d’ouverture des objets ou processus suivants sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="6454e-282">The following objects or processes initiate requests:</span></span>  
    *   <span data-ttu-id="6454e-283">**Analyseur**.</span><span class="sxs-lookup"><span data-stu-id="6454e-283">**Parser**.</span></span>  <span data-ttu-id="6454e-284">Analyseur HTML pour Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6454e-284">The HTML parser for Microsoft Edge.</span></span>  
    *   <span data-ttu-id="6454e-285">**Redirect**.</span><span class="sxs-lookup"><span data-stu-id="6454e-285">**Redirect**.</span></span>  <span data-ttu-id="6454e-286">Une redirection HTTP.</span><span class="sxs-lookup"><span data-stu-id="6454e-286">An HTTP redirect.</span></span>  
    *   <span data-ttu-id="6454e-287">**Script**.</span><span class="sxs-lookup"><span data-stu-id="6454e-287">**Script**.</span></span>  <span data-ttu-id="6454e-288">Fonction JavaScript.</span><span class="sxs-lookup"><span data-stu-id="6454e-288">A JavaScript function.</span></span>  
    *   <span data-ttu-id="6454e-289">**Autre**.</span><span class="sxs-lookup"><span data-stu-id="6454e-289">**Other**.</span></span>  <span data-ttu-id="6454e-290">Un autre processus ou action, comme la navigation vers une page par le biais d’un lien ou la saisie d’une URL dans la barre d’adresses.</span><span class="sxs-lookup"><span data-stu-id="6454e-290">Some other process or action, such as navigating to a page via a link or entering a URL in the address bar.</span></span>  
*   <span data-ttu-id="6454e-291">**Taille**.</span><span class="sxs-lookup"><span data-stu-id="6454e-291">**Size**.</span></span>  <span data-ttu-id="6454e-292">Taille combinée des en-têtes de réponse et du corps de la réponse, tel qu’il est délivré par le serveur.</span><span class="sxs-lookup"><span data-stu-id="6454e-292">The combined size of the response headers plus the response body, as delivered by the server.</span></span>  
*   <span data-ttu-id="6454e-293">**Temps**.</span><span class="sxs-lookup"><span data-stu-id="6454e-293">**Time**.</span></span>  <span data-ttu-id="6454e-294">Durée totale, entre le début de la demande et la réception de l’octet final dans la réponse.</span><span class="sxs-lookup"><span data-stu-id="6454e-294">The total duration, from the start of the request to the receipt of the final byte in the response.</span></span>  
*   <span data-ttu-id="6454e-295">En [**cascade**](#view-the-timing-of-requests-in-relation-to-one-another).</span><span class="sxs-lookup"><span data-stu-id="6454e-295">[**Waterfall**](#view-the-timing-of-requests-in-relation-to-one-another).</span></span>  <span data-ttu-id="6454e-296">Répartition visuelle de l’activité pour chaque demande.</span><span class="sxs-lookup"><span data-stu-id="6454e-296">A visual breakdown of the activity for each request.</span></span>  

#### <span data-ttu-id="6454e-297">Ajouter ou supprimer des colonnes</span><span class="sxs-lookup"><span data-stu-id="6454e-297">Add or remove columns</span></span>   

<span data-ttu-id="6454e-298">Cliquez avec le bouton droit sur l’en-tête de la table demandes et sélectionnez une option pour la masquer ou l’afficher.</span><span class="sxs-lookup"><span data-stu-id="6454e-298">Right-click the header of the Requests table and select an option to hide or show it.</span></span>  <span data-ttu-id="6454e-299">Les options actuellement affichées disposent de coches en regard de chaque élément.</span><span class="sxs-lookup"><span data-stu-id="6454e-299">Currently displayed options have checkmarks next to each item.</span></span>  

> ##### <span data-ttu-id="6454e-300">Figure16</span><span class="sxs-lookup"><span data-stu-id="6454e-300">Figure 16</span></span>  
> <span data-ttu-id="6454e-301">Ajout d’une colonne dans la table demandes</span><span class="sxs-lookup"><span data-stu-id="6454e-301">Adding a column to the Requests table</span></span>  
> <span data-ttu-id="6454e-302">! [Ajout d’une colonne dans la table demandes] [ImageRequestsTableAddColumn]</span><span class="sxs-lookup"><span data-stu-id="6454e-302">![Adding a column to the Requests table][ImageRequestsTableAddColumn]</span></span>  

#### <span data-ttu-id="6454e-303">Ajouter des colonnes personnalisées</span><span class="sxs-lookup"><span data-stu-id="6454e-303">Add custom columns</span></span>   

<span data-ttu-id="6454e-304">Pour ajouter une colonne personnalisée à la table demandes, cliquez avec le bouton droit sur l’en-tête de la table demandes et sélectionnez **les en-têtes de réponse**  >  **gérer les colonnes d’en-tête**.</span><span class="sxs-lookup"><span data-stu-id="6454e-304">To add a custom column to the Requests table, right-click the header of the Requests table and select **Response Headers** > **Manage Header Columns**.</span></span>  

> ##### <span data-ttu-id="6454e-305">Figure17</span><span class="sxs-lookup"><span data-stu-id="6454e-305">Figure 17</span></span>  
> <span data-ttu-id="6454e-306">Ajout d’une colonne personnalisée dans la table demandes</span><span class="sxs-lookup"><span data-stu-id="6454e-306">Adding a custom column to the Requests table</span></span>  
> <span data-ttu-id="6454e-307">! [Ajout d’une colonne personnalisée dans la table demandes] [ImageRequestsTableCustomColumn]</span><span class="sxs-lookup"><span data-stu-id="6454e-307">![Adding a custom column to the Requests table][ImageRequestsTableCustomColumn]</span></span>  

### <span data-ttu-id="6454e-308">Afficher le minutage des requêtes les uns par rapport aux autres</span><span class="sxs-lookup"><span data-stu-id="6454e-308">View the timing of requests in relation to one another</span></span>   

<span data-ttu-id="6454e-309">Utilisez la cascade pour afficher le minutage des requêtes les uns par rapport aux autres.</span><span class="sxs-lookup"><span data-stu-id="6454e-309">Use the Waterfall to view the timing of requests in relation to one another.</span></span>  
<span data-ttu-id="6454e-310">Par défaut, la cascade est organisée selon l’heure de début des requêtes.</span><span class="sxs-lookup"><span data-stu-id="6454e-310">By default, the Waterfall is organized by the start time of the requests.</span></span>  
<span data-ttu-id="6454e-311">Par conséquent, les demandes qui sont plus éloignées de gauche que celles qui sont plus éloignées.</span><span class="sxs-lookup"><span data-stu-id="6454e-311">So, requests that are farther to the left started earlier than those that are farther to the right.</span></span>  

<span data-ttu-id="6454e-312">Pour plus d’options, voir [Trier par phase d’activité](#sort-by-activity-phase) .</span><span class="sxs-lookup"><span data-stu-id="6454e-312">See [Sort by activity phase](#sort-by-activity-phase) to see the different ways that you may sort the Waterfall.</span></span>  

> ##### <span data-ttu-id="6454e-313">Figure 18</span><span class="sxs-lookup"><span data-stu-id="6454e-313">Figure 18</span></span>  
> <span data-ttu-id="6454e-314">Colonne cascade du volet demandes</span><span class="sxs-lookup"><span data-stu-id="6454e-314">The Waterfall column of the Requests pane</span></span>  
> <span data-ttu-id="6454e-315">! [La colonne cascade du volet demandes] [ImageRequestsTableWaterfallColumn]</span><span class="sxs-lookup"><span data-stu-id="6454e-315">![The Waterfall column of the Requests pane][ImageRequestsTableWaterfallColumn]</span></span>  

<!-- ### Analyze the frames of a WebSocket Connection   -->

<!--To view the frames of a WebSocket connection:  

1.  Select the URL of the WebSocket connection, under the **Name** column of the Requests table.  
1.  Select the **Frames** tab.  The table shows the last 100 frames.  

To refresh the table, re-click the name of the WebSocket connection under the **Name** column of the Requests table.  -->

<!--
> ##### Old Figure 20  
> The Frames tab  
> ![The Frames tab][ImageFrames]  
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

### <span data-ttu-id="6454e-316">Afficher un aperçu d’un corps de réponse</span><span class="sxs-lookup"><span data-stu-id="6454e-316">View a preview of a response body</span></span>   

<span data-ttu-id="6454e-317">Pour afficher un aperçu d’un corps de réponse:</span><span class="sxs-lookup"><span data-stu-id="6454e-317">To view a preview of a response body:</span></span>  

1.  <span data-ttu-id="6454e-318">Sélectionnez l’URL de la requête dans la colonne **nom** de la table demandes.</span><span class="sxs-lookup"><span data-stu-id="6454e-318">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="6454e-319">Sélectionnez l’onglet **Aperçu** .</span><span class="sxs-lookup"><span data-stu-id="6454e-319">Select the **Preview** tab.</span></span>  

<span data-ttu-id="6454e-320">Cet onglet est principalement utile pour afficher des images.</span><span class="sxs-lookup"><span data-stu-id="6454e-320">This tab is mostly useful for viewing images.</span></span>  

> ##### <span data-ttu-id="6454e-321">Figure 19</span><span class="sxs-lookup"><span data-stu-id="6454e-321">Figure 19</span></span>  
> <span data-ttu-id="6454e-322">Onglet Aperçu</span><span class="sxs-lookup"><span data-stu-id="6454e-322">The Preview tab</span></span>  
> <span data-ttu-id="6454e-323">! [Onglet Aperçu] [ImagePreview]</span><span class="sxs-lookup"><span data-stu-id="6454e-323">![The Preview tab][ImagePreview]</span></span>  

### <span data-ttu-id="6454e-324">Afficher le corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="6454e-324">View a response body</span></span>   

<span data-ttu-id="6454e-325">Pour afficher le corps de la réponse à une demande:</span><span class="sxs-lookup"><span data-stu-id="6454e-325">To view the response body to a request:</span></span>  

1.  <span data-ttu-id="6454e-326">Sélectionnez l’URL de la requête dans la colonne **nom** de la table demandes.</span><span class="sxs-lookup"><span data-stu-id="6454e-326">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="6454e-327">Sélectionnez l’onglet **réponse** .</span><span class="sxs-lookup"><span data-stu-id="6454e-327">Select the **Response** tab.</span></span>  

> ##### <span data-ttu-id="6454e-328">Figure 20</span><span class="sxs-lookup"><span data-stu-id="6454e-328">Figure 20</span></span>  
> <span data-ttu-id="6454e-329">Onglet réponse</span><span class="sxs-lookup"><span data-stu-id="6454e-329">The Response tab</span></span>  
> <span data-ttu-id="6454e-330">! [Onglet réponse] [ImageResponse]</span><span class="sxs-lookup"><span data-stu-id="6454e-330">![The Response tab][ImageResponse]</span></span>  

### <span data-ttu-id="6454e-331">Afficher les en-têtes HTTP</span><span class="sxs-lookup"><span data-stu-id="6454e-331">View HTTP headers</span></span>   

<span data-ttu-id="6454e-332">Pour afficher les données d’en-tête HTTP relatives à une requête:</span><span class="sxs-lookup"><span data-stu-id="6454e-332">To view HTTP header data about a request:</span></span>  

1.  <span data-ttu-id="6454e-333">Sélectionnez l’URL de la requête dans la colonne **nom** de la table demandes.</span><span class="sxs-lookup"><span data-stu-id="6454e-333">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="6454e-334">Sélectionnez l’onglet **en-têtes** .</span><span class="sxs-lookup"><span data-stu-id="6454e-334">Select the **Headers** tab.</span></span>  

> ##### <span data-ttu-id="6454e-335">Figure 21</span><span class="sxs-lookup"><span data-stu-id="6454e-335">Figure 21</span></span>  
> <span data-ttu-id="6454e-336">Onglet en-têtes</span><span class="sxs-lookup"><span data-stu-id="6454e-336">The Headers tab</span></span>  
> <span data-ttu-id="6454e-337">! [Onglet en-têtes] [ImageHeaders]</span><span class="sxs-lookup"><span data-stu-id="6454e-337">![The Headers tab][ImageHeaders]</span></span>  

#### <span data-ttu-id="6454e-338">Afficher une source d’en-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="6454e-338">View HTTP header source</span></span>   

<span data-ttu-id="6454e-339">Par défaut, l’onglet en-têtes affiche les noms des en-têtes par ordre alphabétique.</span><span class="sxs-lookup"><span data-stu-id="6454e-339">By default, the Headers tab shows header names alphabetically.</span></span>  <span data-ttu-id="6454e-340">Pour afficher les noms d’en-tête HTTP dans l’ordre dans lequel ils ont été reçus:</span><span class="sxs-lookup"><span data-stu-id="6454e-340">To view the HTTP header names in the order they were received:</span></span>  

1.  <span data-ttu-id="6454e-341">Ouvrez l’onglet **en-têtes** pour la requête qui vous intéresse.</span><span class="sxs-lookup"><span data-stu-id="6454e-341">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="6454e-342">Voir [afficher les en-têtes http](#view-http-headers).</span><span class="sxs-lookup"><span data-stu-id="6454e-342">See [View HTTP headers](#view-http-headers).</span></span>  
1.  <span data-ttu-id="6454e-343">Sélectionnez **afficher la source**, en regard de la section en **-tête de requête** ou **en-tête de réponse** .</span><span class="sxs-lookup"><span data-stu-id="6454e-343">Select **view source**, next to the **Request Header** or **Response Header** section.</span></span>  

### <span data-ttu-id="6454e-344">Afficher les paramètres de chaîne de requête</span><span class="sxs-lookup"><span data-stu-id="6454e-344">View query string parameters</span></span>   

<span data-ttu-id="6454e-345">Pour afficher les paramètres de chaîne de requête d’une URL dans un format lisible par l’utilisateur:</span><span class="sxs-lookup"><span data-stu-id="6454e-345">To view the query string parameters of a URL in a human-readable format:</span></span>  

1.  <span data-ttu-id="6454e-346">Ouvrez l’onglet **en-têtes** pour la requête qui vous intéresse.</span><span class="sxs-lookup"><span data-stu-id="6454e-346">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="6454e-347">Voir [afficher les en-têtes http](#view-http-headers).</span><span class="sxs-lookup"><span data-stu-id="6454e-347">See [View HTTP headers](#view-http-headers).</span></span>  
1.  <span data-ttu-id="6454e-348">Accédez à la section **paramètres de chaîne de requête** .</span><span class="sxs-lookup"><span data-stu-id="6454e-348">Go to the **Query String Parameters** section.</span></span>  

> ##### <span data-ttu-id="6454e-349">Figure 22</span><span class="sxs-lookup"><span data-stu-id="6454e-349">Figure 22</span></span>  
> <span data-ttu-id="6454e-350">Section paramètres de chaîne de requête</span><span class="sxs-lookup"><span data-stu-id="6454e-350">The Query String Parameters section</span></span>  
> <span data-ttu-id="6454e-351">! [Section des paramètres de chaîne de requête] [ImageQueryStringParameters]</span><span class="sxs-lookup"><span data-stu-id="6454e-351">![The Query String Parameters section][ImageQueryStringParameters]</span></span>  

#### <span data-ttu-id="6454e-352">Afficher les paramètres de chaîne de requête source</span><span class="sxs-lookup"><span data-stu-id="6454e-352">View query string parameters source</span></span>   

<span data-ttu-id="6454e-353">Pour afficher la source du paramètre de chaîne de requête d’une requête:</span><span class="sxs-lookup"><span data-stu-id="6454e-353">To view the query string parameter source of a request:</span></span>  

1.  <span data-ttu-id="6454e-354">Accédez à la section paramètres de chaîne de requête.</span><span class="sxs-lookup"><span data-stu-id="6454e-354">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="6454e-355">Voir [afficher les paramètres de chaîne de requête](#view-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="6454e-355">See [View query string parameters](#view-query-string-parameters).</span></span>  
1.  <span data-ttu-id="6454e-356">Sélectionnez **afficher la source**.</span><span class="sxs-lookup"><span data-stu-id="6454e-356">Select **view source**.</span></span>  

#### <span data-ttu-id="6454e-357">Afficher les paramètres de chaîne de requête codés en URL</span><span class="sxs-lookup"><span data-stu-id="6454e-357">View URL-encoded query string parameters</span></span>   

<span data-ttu-id="6454e-358">Pour afficher les paramètres de chaîne de requête dans un format lisible par l’utilisateur, mais avec les codages conservés:</span><span class="sxs-lookup"><span data-stu-id="6454e-358">To view query string parameters in a human-readable format, but with encodings preserved:</span></span>  

1.  <span data-ttu-id="6454e-359">Accédez à la section paramètres de chaîne de requête.</span><span class="sxs-lookup"><span data-stu-id="6454e-359">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="6454e-360">Voir [afficher les paramètres de chaîne de requête](#view-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="6454e-360">See [View query string parameters](#view-query-string-parameters).</span></span>  
1.  <span data-ttu-id="6454e-361">Sélectionnez **afficher l’URL**.</span><span class="sxs-lookup"><span data-stu-id="6454e-361">Select **view URL encoded**.</span></span>  

### <span data-ttu-id="6454e-362">Afficher les cookies</span><span class="sxs-lookup"><span data-stu-id="6454e-362">View cookies</span></span>   

<span data-ttu-id="6454e-363">Pour afficher les cookies envoyés dans l’en-tête HTTP d’une requête:</span><span class="sxs-lookup"><span data-stu-id="6454e-363">To view the cookies sent in the HTTP header of a request:</span></span>  

1.  <span data-ttu-id="6454e-364">Sélectionnez l’URL de la requête dans la colonne **nom** de la table demandes.</span><span class="sxs-lookup"><span data-stu-id="6454e-364">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="6454e-365">Sélectionnez l’onglet **cookies** .</span><span class="sxs-lookup"><span data-stu-id="6454e-365">Select the **Cookies** tab.</span></span>  

<!--See [Fields][ManageDataCookiesFields] for a description of each of the columns.  -->

<!--[ManageDataCookiesFields]: manage-data/cookies#fields  -->
<!--TODO: add link when section is available -->

> ##### <span data-ttu-id="6454e-366">Figure 23</span><span class="sxs-lookup"><span data-stu-id="6454e-366">Figure 23</span></span>  
> <span data-ttu-id="6454e-367">Onglet cookies</span><span class="sxs-lookup"><span data-stu-id="6454e-367">The Cookies tab</span></span>  
> <span data-ttu-id="6454e-368">! [Onglet cookies] [ImageCookies]</span><span class="sxs-lookup"><span data-stu-id="6454e-368">![The Cookies tab][ImageCookies]</span></span>  

### <span data-ttu-id="6454e-369">Afficher la répartition du minutage d’une requête</span><span class="sxs-lookup"><span data-stu-id="6454e-369">View the timing breakdown of a request</span></span>   

<span data-ttu-id="6454e-370">Pour afficher la répartition du minutage d’une requête:</span><span class="sxs-lookup"><span data-stu-id="6454e-370">To view the timing breakdown of a request:</span></span>  

1.  <span data-ttu-id="6454e-371">Sélectionnez l’URL de la requête dans la colonne **nom** de la table demandes.</span><span class="sxs-lookup"><span data-stu-id="6454e-371">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="6454e-372">Sélectionnez l’onglet **minutage** .</span><span class="sxs-lookup"><span data-stu-id="6454e-372">Select the **Timing** tab.</span></span>  

<span data-ttu-id="6454e-373">Pour plus d’informations sur l’accès à ces données, voir [aperçu d’une répartition du temps](#preview-a-timing-breakdown) .</span><span class="sxs-lookup"><span data-stu-id="6454e-373">See [Preview a timing breakdown](#preview-a-timing-breakdown) for a faster way to access this data.</span></span>  

<span data-ttu-id="6454e-374">Pour plus d’informations sur les différentes phases que vous pouvez voir dans l’onglet Minutage, consultez la rubrique [étapes de répartition du temps](#timing-breakdown-phases-explained) .</span><span class="sxs-lookup"><span data-stu-id="6454e-374">See [Timing breakdown phases explained](#timing-breakdown-phases-explained) for more information about each of the phases that you may see in the Timing tab.</span></span>  

> ##### <span data-ttu-id="6454e-375">Figure 24</span><span class="sxs-lookup"><span data-stu-id="6454e-375">Figure 24</span></span>  
> <span data-ttu-id="6454e-376">Onglet Minutage</span><span class="sxs-lookup"><span data-stu-id="6454e-376">The Timing tab</span></span>  
> <span data-ttu-id="6454e-377">! [Onglet Minutage] [ImageTiming]</span><span class="sxs-lookup"><span data-stu-id="6454e-377">![The Timing tab][ImageTiming]</span></span>  

<span data-ttu-id="6454e-378">Plus d’informations sur chacune de ces étapes.</span><span class="sxs-lookup"><span data-stu-id="6454e-378">More information about each of the phases.</span></span>  

<span data-ttu-id="6454e-379">Pour accéder à cet affichage, voir répartition de l' [affichage du minutage](#view-the-timing-breakdown-of-a-request) .</span><span class="sxs-lookup"><span data-stu-id="6454e-379">See [View timing breakdown](#view-the-timing-breakdown-of-a-request) for another way to access this view.</span></span>  

#### <span data-ttu-id="6454e-380">Prévisualiser une répartition de minutage</span><span class="sxs-lookup"><span data-stu-id="6454e-380">Preview a timing breakdown</span></span>   

<span data-ttu-id="6454e-381">Pour afficher un aperçu de la répartition du minutage d’une requête, placez le pointeur sur l’entrée de la requête dans la colonne **cascade** de la table demandes.</span><span class="sxs-lookup"><span data-stu-id="6454e-381">To view a preview of the timing breakdown of a request, hover over the entry for the request in the **Waterfall** column of the Requests table.</span></span>  

<span data-ttu-id="6454e-382">Pour accéder à ces données qui ne nécessitent pas de pointage, voir [afficher la répartition du minutage d’une demande](#view-the-timing-breakdown-of-a-request) .</span><span class="sxs-lookup"><span data-stu-id="6454e-382">See [View the timing breakdown of a request](#view-the-timing-breakdown-of-a-request) for a way to access this data that does not require hovering.</span></span>  

> ##### <span data-ttu-id="6454e-383">Figure 25</span><span class="sxs-lookup"><span data-stu-id="6454e-383">Figure 25</span></span>  
> <span data-ttu-id="6454e-384">Prévisualisation de la répartition du minutage d’une requête</span><span class="sxs-lookup"><span data-stu-id="6454e-384">Previewing the timing breakdown of a request</span></span>  
> <span data-ttu-id="6454e-385">! [Aperçu de la répartition du minutage d’une requête] [ImageWaterfallHover]</span><span class="sxs-lookup"><span data-stu-id="6454e-385">![Previewing the timing breakdown of a request][ImageWaterfallHover]</span></span>  

#### <span data-ttu-id="6454e-386">Explication des phases de répartition du temps</span><span class="sxs-lookup"><span data-stu-id="6454e-386">Timing breakdown phases explained</span></span>   

<span data-ttu-id="6454e-387">Pour plus d’informations sur les différentes phases que vous pouvez voir dans l’onglet Minutage, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="6454e-387">More information about each of the phases you may see in the Timing tab:</span></span>  

*   <span data-ttu-id="6454e-388">Mise en **file d’attente**.</span><span class="sxs-lookup"><span data-stu-id="6454e-388">**Queueing**.</span></span>  <span data-ttu-id="6454e-389">Le navigateur met en file d’attente les requêtes dans les cas suivants:</span><span class="sxs-lookup"><span data-stu-id="6454e-389">The browser queues requests when:</span></span>  
    *   <span data-ttu-id="6454e-390">Il y a des demandes de priorité plus élevées.</span><span class="sxs-lookup"><span data-stu-id="6454e-390">There are higher priority requests.</span></span>  
    *   <span data-ttu-id="6454e-391">Il existe déjà six connexions TCP ouvertes pour cette origine, qui correspond à la limite.</span><span class="sxs-lookup"><span data-stu-id="6454e-391">There are already six TCP connections open for this origin, which is the limit.</span></span>  <span data-ttu-id="6454e-392">S’applique uniquement aux protocoles HTTP/1.0 et HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="6454e-392">Applies to HTTP/1.0 and HTTP/1.1 only.</span></span>  
    *   <span data-ttu-id="6454e-393">Le navigateur alloue de l’espace dans le cache disque.</span><span class="sxs-lookup"><span data-stu-id="6454e-393">The browser is briefly allocating space in the disk cache.</span></span>  
*   <span data-ttu-id="6454e-394">**Bloqué**.</span><span class="sxs-lookup"><span data-stu-id="6454e-394">**Stalled**.</span></span>  <span data-ttu-id="6454e-395">La requête peut être bloquée pour l’une des raisons décrites dans la **file d’attente**.</span><span class="sxs-lookup"><span data-stu-id="6454e-395">The request could be stalled for any of the reasons described in **Queueing**.</span></span>  
*   <span data-ttu-id="6454e-396">**Recherche DNS**.</span><span class="sxs-lookup"><span data-stu-id="6454e-396">**DNS Lookup**.</span></span>  <span data-ttu-id="6454e-397">Le navigateur résout l’adresse IP pour la requête.</span><span class="sxs-lookup"><span data-stu-id="6454e-397">The browser is resolving the IP address for the request.</span></span>  
*   <span data-ttu-id="6454e-398">**Négociation de proxy**.</span><span class="sxs-lookup"><span data-stu-id="6454e-398">**Proxy negotiation**.</span></span>  <span data-ttu-id="6454e-399">Le navigateur négocie la requête avec un [serveur proxy][WikiProxyServer].</span><span class="sxs-lookup"><span data-stu-id="6454e-399">The browser is negotiating the request with a [proxy server][WikiProxyServer].</span></span>  
*   <span data-ttu-id="6454e-400">**Demande envoyée**.</span><span class="sxs-lookup"><span data-stu-id="6454e-400">**Request sent**.</span></span>  <span data-ttu-id="6454e-401">La requête est en cours d’envoi.</span><span class="sxs-lookup"><span data-stu-id="6454e-401">The request is being sent.</span></span>  
*   <span data-ttu-id="6454e-402">**Préparation ServiceWorker**.</span><span class="sxs-lookup"><span data-stu-id="6454e-402">**ServiceWorker Preparation**.</span></span>  <span data-ttu-id="6454e-403">Le navigateur démarre le travailleur du service.</span><span class="sxs-lookup"><span data-stu-id="6454e-403">The browser is starting up the service worker.</span></span>  
*   <span data-ttu-id="6454e-404">**Demander à ServiceWorker**.</span><span class="sxs-lookup"><span data-stu-id="6454e-404">**Request to ServiceWorker**.</span></span>  <span data-ttu-id="6454e-405">La demande est envoyée au travailleur de service.</span><span class="sxs-lookup"><span data-stu-id="6454e-405">The request is being sent to the service worker.</span></span>  
*   <span data-ttu-id="6454e-406">En **attente \ (TTFB \)**.</span><span class="sxs-lookup"><span data-stu-id="6454e-406">**Waiting \(TTFB\)**.</span></span>  <span data-ttu-id="6454e-407">Le navigateur attend le premier octet d’une réponse.</span><span class="sxs-lookup"><span data-stu-id="6454e-407">The browser is waiting for the first byte of a response.</span></span>  
  <span data-ttu-id="6454e-408">TTFB représente le temps à l’octet initial.</span><span class="sxs-lookup"><span data-stu-id="6454e-408">TTFB stands for Time To First Byte.</span></span>  <span data-ttu-id="6454e-409">Ce minutage inclut un aller-retour d’une latence et la durée du serveur pour préparer la réponse.</span><span class="sxs-lookup"><span data-stu-id="6454e-409">This timing includes 1 round trip of latency and the time the server took to prepare the response.</span></span>  
*   <span data-ttu-id="6454e-410">**Téléchargement du contenu**.</span><span class="sxs-lookup"><span data-stu-id="6454e-410">**Content Download**.</span></span>  <span data-ttu-id="6454e-411">Le navigateur reçoit la réponse.</span><span class="sxs-lookup"><span data-stu-id="6454e-411">The browser is receiving the response.</span></span>  
*   <span data-ttu-id="6454e-412">**Réception**d’une émission.</span><span class="sxs-lookup"><span data-stu-id="6454e-412">**Receiving Push**.</span></span>  <span data-ttu-id="6454e-413">Le navigateur reçoit des données pour cette réponse via le protocole HTTP/2 Server Poussée.</span><span class="sxs-lookup"><span data-stu-id="6454e-413">The browser is receiving data for this response via HTTP/2 Server Push.</span></span>  
*   <span data-ttu-id="6454e-414">**Lecture en lecture**.</span><span class="sxs-lookup"><span data-stu-id="6454e-414">**Reading Push**.</span></span>  <span data-ttu-id="6454e-415">Le navigateur lit les données locales précédemment reçues.</span><span class="sxs-lookup"><span data-stu-id="6454e-415">The browser is reading the local data previously received.</span></span>  

### <span data-ttu-id="6454e-416">Afficher les initiateurs et les dépendances</span><span class="sxs-lookup"><span data-stu-id="6454e-416">View initiators and dependencies</span></span>   

<span data-ttu-id="6454e-417">Pour afficher les initiateurs et les dépendances d’une requête, maintenez la touche enfoncée `Shift` et placez le pointeur sur la requête dans la table demandes.</span><span class="sxs-lookup"><span data-stu-id="6454e-417">To view the initiators and dependencies of a request, hold `Shift`and hover over the request in the Requests table.</span></span>  <span data-ttu-id="6454e-418">Couleurs de DevTools: les initiateurs apparaissent en vert et les dépendances apparaissent en rouge.</span><span class="sxs-lookup"><span data-stu-id="6454e-418">DevTools colors: initiators are shown in green and dependencies are shown in red.</span></span>  

> ##### <span data-ttu-id="6454e-419">Figure 26</span><span class="sxs-lookup"><span data-stu-id="6454e-419">Figure 26</span></span>  
> <span data-ttu-id="6454e-420">Affichage des déclencheurs et des dépendances d’une requête</span><span class="sxs-lookup"><span data-stu-id="6454e-420">Viewing the initiators and dependencies of a request</span></span>  
> <span data-ttu-id="6454e-421">! [Affichage des déclencheurs et dépendances d’une requête] [ImageRequestInitiatorsDependencies]</span><span class="sxs-lookup"><span data-stu-id="6454e-421">![Viewing the initiators and dependencies of a request][ImageRequestInitiatorsDependencies]</span></span>  

<span data-ttu-id="6454e-422">Lorsque la table requêtes est classée dans un ordre chronologique, la première demande verte au-dessus de celle où vous pointez est l’initiateur de la dépendance.</span><span class="sxs-lookup"><span data-stu-id="6454e-422">When the Requests table is ordered chronologically, the first green request above the one you are hovering is the initiator of the dependency.</span></span>  <span data-ttu-id="6454e-423">Si une autre demande verte s’affiche au-dessus de celle-ci, il s’agit de l’initiateur de l’initiateur.</span><span class="sxs-lookup"><span data-stu-id="6454e-423">If another green request appears above that, that higher request is the initiator of the initiator.</span></span>  <span data-ttu-id="6454e-424">Et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="6454e-424">And so on.</span></span>  

### <span data-ttu-id="6454e-425">Afficher les événements de chargement</span><span class="sxs-lookup"><span data-stu-id="6454e-425">View load events</span></span>   

<span data-ttu-id="6454e-426">DevTools affiche le minutage des `DOMContentLoaded` événements et `load` dans plusieurs emplacements du panneau réseau.</span><span class="sxs-lookup"><span data-stu-id="6454e-426">DevTools displays the timing of the `DOMContentLoaded` and `load` events in multiple places on the Network panel.</span></span>  <span data-ttu-id="6454e-427">L' `DOMContentLoaded` événement est coloré en bleu et l' `load` événement est rouge.</span><span class="sxs-lookup"><span data-stu-id="6454e-427">The `DOMContentLoaded` event is colored blue, and the `load` event is red.</span></span>  

> ##### <span data-ttu-id="6454e-428">Figure 27</span><span class="sxs-lookup"><span data-stu-id="6454e-428">Figure 27</span></span>  
> <span data-ttu-id="6454e-429">Emplacement des `DOMContentLoaded` `load` événements et dans le volet réseau</span><span class="sxs-lookup"><span data-stu-id="6454e-429">The locations of the `DOMContentLoaded` and `load` events on the Network panel</span></span>  
> <span data-ttu-id="6454e-430">! [Emplacements des événements DOMContentLoaded et Load sur le panneau réseau] [ImageNetworkPanelDOMContentLoadedLoadEvents]</span><span class="sxs-lookup"><span data-stu-id="6454e-430">![The locations of the DOMContentLoaded and load events on the Network panel][ImageNetworkPanelDOMContentLoadedLoadEvents]</span></span>  

### <span data-ttu-id="6454e-431">Afficher le nombre total de demandes</span><span class="sxs-lookup"><span data-stu-id="6454e-431">View the total number of requests</span></span>   

<span data-ttu-id="6454e-432">Le nombre total de demandes est répertorié dans le volet Résumé, au bas du panneau réseau.</span><span class="sxs-lookup"><span data-stu-id="6454e-432">The total number of requests is listed in the Summary pane, at the bottom of the Network panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="6454e-433">Ce numéro suit uniquement les requêtes qui ont été enregistrées depuis l’ouverture de DevTools.</span><span class="sxs-lookup"><span data-stu-id="6454e-433">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="6454e-434">Si d’autres requêtes s’est produites avant l’ouverture de DevTools, ces demandes ne sont pas comptabilisées.</span><span class="sxs-lookup"><span data-stu-id="6454e-434">If other requests occurred before DevTools was opened, those requests are not counted.</span></span>  

> ##### <span data-ttu-id="6454e-435">Figure 28</span><span class="sxs-lookup"><span data-stu-id="6454e-435">Figure 28</span></span>  
> <span data-ttu-id="6454e-436">Nombre total de demandes depuis l’ouverture de DevTools</span><span class="sxs-lookup"><span data-stu-id="6454e-436">The total number of requests since DevTools was opened</span></span>  
> <span data-ttu-id="6454e-437">! [Nombre total de demandes depuis l’ouverture de DevTools] [ImageTotalRequests]</span><span class="sxs-lookup"><span data-stu-id="6454e-437">![The total number of requests since DevTools was opened][ImageTotalRequests]</span></span>  

### <span data-ttu-id="6454e-438">Affichez la taille totale du téléchargement</span><span class="sxs-lookup"><span data-stu-id="6454e-438">View the total download size</span></span>   

<span data-ttu-id="6454e-439">La taille de téléchargement totale des demandes figure dans le volet Résumé, en bas du volet réseau.</span><span class="sxs-lookup"><span data-stu-id="6454e-439">The total download size of requests is listed in the Summary pane, at the bottom of the Network panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="6454e-440">Ce numéro suit uniquement les requêtes qui ont été enregistrées depuis l’ouverture de DevTools.</span><span class="sxs-lookup"><span data-stu-id="6454e-440">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="6454e-441">Si d’autres requêtes s’est produites avant l’ouverture de DevTools, ces demandes ne sont pas comptabilisées.</span><span class="sxs-lookup"><span data-stu-id="6454e-441">If other requests occurred before DevTools was opened, those requests are not counted.</span></span>  

> ##### <span data-ttu-id="6454e-442">Figure 29</span><span class="sxs-lookup"><span data-stu-id="6454e-442">Figure 29</span></span>  
> <span data-ttu-id="6454e-443">La taille de téléchargement totale des requêtes</span><span class="sxs-lookup"><span data-stu-id="6454e-443">The total download size of requests</span></span>  
> <span data-ttu-id="6454e-444">! [Longueur totale du téléchargement de demandes] [ImageTotalSize]</span><span class="sxs-lookup"><span data-stu-id="6454e-444">![The total download size of requests][ImageTotalSize]</span></span>  

<span data-ttu-id="6454e-445">Pour afficher [le nombre de ressources de taille décompressées, voir afficher la taille d’une ressource](#view-the-uncompressed-size-of-a-resource) , puis décompresser chaque élément.</span><span class="sxs-lookup"><span data-stu-id="6454e-445">See [View the uncompressed size of a resource](#view-the-uncompressed-size-of-a-resource) to see how large resources are after the browser uncompresses each item.</span></span>  

### <span data-ttu-id="6454e-446">Afficher la trace de pile ayant entraîné une requête</span><span class="sxs-lookup"><span data-stu-id="6454e-446">View the stack trace that caused a request</span></span>   

<span data-ttu-id="6454e-447">Après qu’une instruction JavaScript demande une ressource, placez le pointeur sur la colonne **Initiator** pour afficher la trace de pile qui se trouve au début de la requête.</span><span class="sxs-lookup"><span data-stu-id="6454e-447">After a JavaScript statement requests a resource, hover over the **Initiator** column to view the stack trace leading up to the request.</span></span>  

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

> ##### <span data-ttu-id="6454e-448">Figure 30</span><span class="sxs-lookup"><span data-stu-id="6454e-448">Figure 30</span></span>  
> <span data-ttu-id="6454e-449">Trace de pile aboutissant à une demande de ressources</span><span class="sxs-lookup"><span data-stu-id="6454e-449">The stack trace leading up to a resource request</span></span>  
> <span data-ttu-id="6454e-450">! [Trace de pile aboutissant à une demande de ressource] [ImageInitiatorStack]</span><span class="sxs-lookup"><span data-stu-id="6454e-450">![The stack trace leading up to a resource request][ImageInitiatorStack]</span></span>  

### <span data-ttu-id="6454e-451">Affichage de la taille de la ressource non compressée</span><span class="sxs-lookup"><span data-stu-id="6454e-451">View the uncompressed size of a resource</span></span>   

<span data-ttu-id="6454e-452">Activez la case à cocher **utiliser des lignes de requête volumineuses** , puis examinez la valeur inférieure de la colonne **taille** .</span><span class="sxs-lookup"><span data-stu-id="6454e-452">Select the **Use large request rows** checkbox and then look at the bottom value of the **Size** column.</span></span>  

> ##### <span data-ttu-id="6454e-453">Figure 31</span><span class="sxs-lookup"><span data-stu-id="6454e-453">Figure 31</span></span>  
> <span data-ttu-id="6454e-454">Voici un exemple de ressources non compressées \ (la taille du `jquery-3.3.1.min.js` fichier qui a été envoyée par le biais du réseau était `29.9 KB` alors la taille du fichier non compressé `84.9 KB` ).</span><span class="sxs-lookup"><span data-stu-id="6454e-454">An example of uncompressed resources  \(The compressed size of the `jquery-3.3.1.min.js` file that was sent over the network was `29.9 KB`, whereas the uncompressed size was `84.9 KB`\)</span></span>  
> <span data-ttu-id="6454e-455">! [Exemple de ressources non comprimées] [ImageUncompressedResources]</span><span class="sxs-lookup"><span data-stu-id="6454e-455">![An example of uncompressed resources][ImageUncompressedResources]</span></span>  

## <span data-ttu-id="6454e-456">Exporter les données de requête</span><span class="sxs-lookup"><span data-stu-id="6454e-456">Export requests data</span></span>   

### <span data-ttu-id="6454e-457">Enregistrer toutes les demandes réseau dans un fichier QAR</span><span class="sxs-lookup"><span data-stu-id="6454e-457">Save all network requests to a HAR file</span></span>   

<span data-ttu-id="6454e-458">Pour enregistrer toutes les requêtes réseau sur un fichier QAR:</span><span class="sxs-lookup"><span data-stu-id="6454e-458">To save all network requests to a HAR file:</span></span>  

1.  <span data-ttu-id="6454e-459">Cliquez avec le bouton droit sur une requête dans la table demandes.</span><span class="sxs-lookup"><span data-stu-id="6454e-459">Right-click any request in the Requests table.</span></span>  
1.  <span data-ttu-id="6454e-460">Sélectionnez **Save As QAR with content**.</span><span class="sxs-lookup"><span data-stu-id="6454e-460">Select **Save as HAR with Content**.</span></span>  <span data-ttu-id="6454e-461">DevTools enregistre toutes les demandes qui se sont produites depuis que vous avez ouvert DevTools sur le fichier.</span><span class="sxs-lookup"><span data-stu-id="6454e-461">DevTools saves all requests that have occurred since you opened DevTools to the HAR file.</span></span>  <span data-ttu-id="6454e-462">Il n’est pas possible de filtrer les demandes ou de n’enregistrer qu’une seule demande.</span><span class="sxs-lookup"><span data-stu-id="6454e-462">There is no way to filter requests, or to save just a single request.</span></span>  

<span data-ttu-id="6454e-463">Lorsque vous enregistrez un fichier QAR, vous pouvez l’importer de nouveau dans DevTools pour analyse.</span><span class="sxs-lookup"><span data-stu-id="6454e-463">Once you save a HAR file, you may import it back into DevTools for analysis.</span></span>  <span data-ttu-id="6454e-464">Il suffit de glisser-déplacer le fichier QAR dans la table demandes.</span><span class="sxs-lookup"><span data-stu-id="6454e-464">Just drag-and-drop the HAR file into the Requests table.</span></span>  
<!--See also [HAR Analyzer][HARAnalyzer].  -->  

<!--[HARAnalyzer]: https://toolbox.alphabetapps.com/apps/har_analyzer  -->  
<!--Todo: add section link when content is available  -->  

> ##### <span data-ttu-id="6454e-465">Figure 32</span><span class="sxs-lookup"><span data-stu-id="6454e-465">Figure 32</span></span>  
> <span data-ttu-id="6454e-466">Sélection de l’option Enregistrer sous le contenu de votre fichier</span><span class="sxs-lookup"><span data-stu-id="6454e-466">Selecting Save as HAR with Content</span></span>  
> <span data-ttu-id="6454e-467">! [Sélection de l’option Enregistrer sous le contenu d’un fichier [ImageSaveAsHAR]</span><span class="sxs-lookup"><span data-stu-id="6454e-467">![Selecting Save as HAR with Content][ImageSaveAsHAR]</span></span>  

### <span data-ttu-id="6454e-468">Copier une ou plusieurs demandes dans le presse-papiers</span><span class="sxs-lookup"><span data-stu-id="6454e-468">Copy one or more requests to the clipboard</span></span>   

<span data-ttu-id="6454e-469">Dans la colonne **nom** de la table demandes, cliquez avec le bouton droit sur une requête, survolez la **copie**, puis sélectionnez l’une des options suivantes:</span><span class="sxs-lookup"><span data-stu-id="6454e-469">Under the **Name** column of the Requests table, right-click a request, hover over **Copy**, and select one of the following options:</span></span>  

*   <span data-ttu-id="6454e-470">**Copier l’adresse du lien**.</span><span class="sxs-lookup"><span data-stu-id="6454e-470">**Copy Link Address**.</span></span>  <span data-ttu-id="6454e-471">Copiez l’URL de la requête dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="6454e-471">Copy the URL of the request to the clipboard.</span></span>  
*   <span data-ttu-id="6454e-472">**Copier la réponse**.</span><span class="sxs-lookup"><span data-stu-id="6454e-472">**Copy Response**.</span></span>  <span data-ttu-id="6454e-473">Copiez le corps de la réponse dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="6454e-473">Copy the response body to the clipboard.</span></span>  
*   <span data-ttu-id="6454e-474">**Copy As FETCH**.</span><span class="sxs-lookup"><span data-stu-id="6454e-474">**Copy as Fetch**.</span></span>  
*   <span data-ttu-id="6454e-475">**Copier comme courbe**.</span><span class="sxs-lookup"><span data-stu-id="6454e-475">**Copy as cURL**.</span></span>  <span data-ttu-id="6454e-476">Copiez la demande en tant que commande en forme de boucle.</span><span class="sxs-lookup"><span data-stu-id="6454e-476">Copy the request as a cURL command.</span></span>  
*   <span data-ttu-id="6454e-477">**Copy All As FETCH**.</span><span class="sxs-lookup"><span data-stu-id="6454e-477">**Copy All as Fetch**.</span></span>  
*   <span data-ttu-id="6454e-478">**Tout copier comme courbe**.</span><span class="sxs-lookup"><span data-stu-id="6454e-478">**Copy All as cURL**.</span></span>  <span data-ttu-id="6454e-479">Copiez toutes les demandes comme une chaîne de commandes bouclé.</span><span class="sxs-lookup"><span data-stu-id="6454e-479">Copy all requests as a chain of cURL commands.</span></span>  
*   <span data-ttu-id="6454e-480">**Copy All As QAR**.</span><span class="sxs-lookup"><span data-stu-id="6454e-480">**Copy All as HAR**.</span></span>  <span data-ttu-id="6454e-481">Copiez toutes les demandes en tant que données QAR.</span><span class="sxs-lookup"><span data-stu-id="6454e-481">Copy all requests as HAR data.</span></span>  

> ##### <span data-ttu-id="6454e-482">Figure 33</span><span class="sxs-lookup"><span data-stu-id="6454e-482">Figure 33</span></span>  
> <span data-ttu-id="6454e-483">Sélection de l’option copier la réponse</span><span class="sxs-lookup"><span data-stu-id="6454e-483">Selecting Copy Response</span></span>  
> <span data-ttu-id="6454e-484">! [Sélection de l’option copier la réponse] [ImageCopyResponse]</span><span class="sxs-lookup"><span data-stu-id="6454e-484">![Selecting Copy Response][ImageCopyResponse]</span></span>  

## <span data-ttu-id="6454e-485">Modifier la disposition du panneau réseau</span><span class="sxs-lookup"><span data-stu-id="6454e-485">Change the layout of the Network panel</span></span>  

<span data-ttu-id="6454e-486">Vous pouvez développer ou réduire des sections de l’interface utilisateur du panneau réseau pour cibler les informations importantes.</span><span class="sxs-lookup"><span data-stu-id="6454e-486">You may expand or collapse sections of the Network panel UI to focus important information.</span></span>  

### <span data-ttu-id="6454e-487">Masquer le volet filtres</span><span class="sxs-lookup"><span data-stu-id="6454e-487">Hide the Filters pane</span></span>   

<span data-ttu-id="6454e-488">Par défaut, DevTools affiche le **volet filtres**.</span><span class="sxs-lookup"><span data-stu-id="6454e-488">By default, DevTools shows the **Filters pane**.</span></span>  
<span data-ttu-id="6454e-489">Sélectionnez **Filter** ![ filtre ][ImageFilterIcon] de filtre pour le masquer.</span><span class="sxs-lookup"><span data-stu-id="6454e-489">Select **Filter** ![Filter][ImageFilterIcon]  to hide it.</span></span>  

> ##### <span data-ttu-id="6454e-490">Figure 34</span><span class="sxs-lookup"><span data-stu-id="6454e-490">Figure 34</span></span>  
> <span data-ttu-id="6454e-491">Bouton Masquer les filtres</span><span class="sxs-lookup"><span data-stu-id="6454e-491">The Hide Filters button</span></span>  
> <span data-ttu-id="6454e-492">! [Bouton Masquer les filtres] [ImageHideFiltersButton]</span><span class="sxs-lookup"><span data-stu-id="6454e-492">![The Hide Filters button][ImageHideFiltersButton]</span></span>  

### <span data-ttu-id="6454e-493">Utiliser des lignes de requête volumineuses</span><span class="sxs-lookup"><span data-stu-id="6454e-493">Use large request rows</span></span>   

<span data-ttu-id="6454e-494">Utilisez des lignes de grande taille si vous voulez plus d’espace dans votre tableau de requêtes réseau.</span><span class="sxs-lookup"><span data-stu-id="6454e-494">Use large rows when you want more whitespace in your network requests table.</span></span>  <span data-ttu-id="6454e-495">Certaines colonnes fournissent également quelques informations supplémentaires sur l’utilisation de lignes de grande taille.</span><span class="sxs-lookup"><span data-stu-id="6454e-495">Some columns also provide a little more information when using large rows.</span></span>  <span data-ttu-id="6454e-496">Par exemple, la valeur la plus en bas de la colonne **taille** correspond à la taille de requête non compressée.</span><span class="sxs-lookup"><span data-stu-id="6454e-496">For example, the bottom value of the **Size** column is the uncompressed size of a request.</span></span>  

> ##### <span data-ttu-id="6454e-497">Figure 35</span><span class="sxs-lookup"><span data-stu-id="6454e-497">Figure 35</span></span>  
> <span data-ttu-id="6454e-498">Exemple de longues lignes de requête dans le volet requêtes</span><span class="sxs-lookup"><span data-stu-id="6454e-498">An example of large request rows in the Requests pane</span></span>  
> <span data-ttu-id="6454e-499">! [Exemple de grandes lignes de requête dans le volet requêtes] [ImageLargeRequestRows]</span><span class="sxs-lookup"><span data-stu-id="6454e-499">![An example of large request rows in the Requests pane][ImageLargeRequestRows]</span></span>  

<span data-ttu-id="6454e-500">Activez la case à cocher **utiliser des lignes de requête volumineuses** pour activer les lignes de grande taille.</span><span class="sxs-lookup"><span data-stu-id="6454e-500">Select the **Use large request rows** checkbox to enable large rows.</span></span>  

> ##### <span data-ttu-id="6454e-501">Figure 36</span><span class="sxs-lookup"><span data-stu-id="6454e-501">Figure 36</span></span>  
> <span data-ttu-id="6454e-502">Case à cocher grandes lignes de requête</span><span class="sxs-lookup"><span data-stu-id="6454e-502">The Large Request Rows checkbox</span></span>  
> <span data-ttu-id="6454e-503">! [Case à cocher grandes lignes de requête] [ImageLargeRequestRowsCheckbox]</span><span class="sxs-lookup"><span data-stu-id="6454e-503">![The Large Request Rows checkbox][ImageLargeRequestRowsCheckbox]</span></span>  

### <span data-ttu-id="6454e-504">Masquer le volet vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="6454e-504">Hide the Overview pane</span></span>   

<span data-ttu-id="6454e-505">Par défaut, DevTools affiche le **volet vue d’ensemble**.</span><span class="sxs-lookup"><span data-stu-id="6454e-505">By default, DevTools shows the **Overview pane**.</span></span>  
<span data-ttu-id="6454e-506">Désélectionnez la case à cocher **afficher la vue d’ensemble** pour la masquer.</span><span class="sxs-lookup"><span data-stu-id="6454e-506">Deselect the **Show Overview** checkbox to hide it.</span></span>  

> ##### <span data-ttu-id="6454e-507">Figure 37</span><span class="sxs-lookup"><span data-stu-id="6454e-507">Figure 37</span></span>  
> <span data-ttu-id="6454e-508">Case à cocher Afficher la vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="6454e-508">The Show Overview checkbox</span></span>  
> <span data-ttu-id="6454e-509">! [La case à cocher Afficher la présentation] [ImageHideOverviewCheckbox]</span><span class="sxs-lookup"><span data-stu-id="6454e-509">![The Show Overview checkbox][ImageHideOverviewCheckbox]</span></span>  

<!-->   -->  

  

<!-- image links -->  

[ImageCaptureScreenshotsIcon]: /microsoft-edge/devtools-guide-chromium/media/capture-screenshots-icon.msft.png  
[ImageClearIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-requests-icon.msft.png  
[ImageFilterIcon]: /microsoft-edge/devtools-guide-chromium/media/filter-icon.msft.png  
[ImageHideIcon]: /microsoft-edge/devtools-guide-chromium/media/hide-overview-icon.msft.png  
[ImageLargeResourceRowsIcon]: /microsoft-edge/devtools-guide-chromium/media/large-resource-rows-button-icon.msft.png  
[ImageRecordOnIcon]: /microsoft-edge/devtools-guide-chromium/media/record-on-icon.msft.png  

[ImageNetworkPanel]: /microsoft-edge/devtools-guide-chromium/media/network-network-panel.msft.png "Figure 1: panneau réseau"  
[ImageClearButton]: /microsoft-edge/devtools-guide-chromium/media/network-network-clear-button.msft.png "Figure 2: bouton Effacer"  
[ImagePreserveLogCheckBox]: /microsoft-edge/devtools-guide-chromium/media/network-network-preserve-log.msft.png "Figure 3: case à cocher conserver le journal"  
[ImageScreenshotHover]: /microsoft-edge/devtools-guide-chromium/media/network-network-screenshot-hover.msft.png "Figure 4: survol d’une capture d’écran"  
<!--[ImageReplayXHR]: /microsoft-edge/devtools-guide-chromium/media/network-replay-xhr.msft.png "Old Figure 5: Selecting Replay XHR"  -->  
[ImageDisableCacheCheckBox]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Disable-cache-CheckBox.msft.png "figure 5: case à cocher Désactiver le cache"  
[ImageClearBrowserCache]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Clear-Browser-cache.msft.png "figure 6: sélectionner vider le cache du navigateur"  
[ImageOfflineDropdown]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Offline-DropDown.msft.png "figure 7: menu déroulant hors ligne"  
[ImageNetworkThrottlingMenu]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-throttling-menu.msft.png "figure 8: menu de limitation du réseau"  
[ImageClearBrowserCookies]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Clear-Browser-cookies.msft.png "figure 9: sélectionnez Effacer les cookies du navigateur"  
[ImageFilterTextBox]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Filters-TextBox.msft.png "figure 10: zone de texte filtres"  
[ImageMultiTypeFilter]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-type-Filters.msft.png "figure 11: utilisation des filtres de type pour afficher JS, CSS et les ressources de documents"  
[ImageOverviewFilter]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Overview-Filter.msft.png "figure 12: filtrage des requêtes inactives depuis 300M"  
[ImageHideDataURLsCheckBox]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Hide-Data-URLs.msft.png "figure 13: cases à cocher Masquer les URL de données"  
[ImageWaterfallTotalDuration]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Waterfall-Total-Duration.msft.png "figure 14: trier les cascade en fonction de la durée totale"  
[ImageRequestsTable]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-table.msft.png "figure 15: la table demandes"  
[ImageRequestsTableAddColumn]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-Add-Column.msft.png "figure 16: ajout d’une colonne dans la table demandes"  
[ImageRequestsTableCustomColumn]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-Add-Custom.msft.png "figure 17: ajout d’une colonne personnalisée dans la table demandes"  
[ImageRequestsTableWaterfallColumn]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-Waterfall.msft.png "figure 18: colonne cascade du volet demandes"  
[ImagePreview]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Resources-preview.msft.png "figure 19: onglet Aperçu"  
<!--[ImageFrames]: /microsoft-edge/devtools-guide-chromium/media/network-frames.msft.png "Old Figure 20: The Frames tab"  -->  
[ImageResponse]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Resources-Response.msft.png "figure 20: onglet réponse"  
[ImageHeaders]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Resources-headers.msft.png "figure 21: onglet en-têtes"  
[ImageQueryStringParameters]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Resources-headers-query-string-Parameters.msft.png "figure 22: section paramètres de chaînes de requête"  
[ImageCookies]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Resources-cookies.msft.png "figure 23: onglet cookies"  
[ImageTiming]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Resources-timing.msft.png "figure 24: onglet Minutage"  
[ImageWaterfallHover]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Resources-Waterfall-Hover.msft.png "figure 25: prévisualisation de l’intervalle de temps d’une requête"  
[ImageRequestInitiatorsDependencies]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Resources-Initiators-Dependencies.msft.png "figure 26: affichage des déclencheurs et dépendances d’une requête"  
[ImageNetworkPanelDOMContentLoadedLoadEvents]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-Load-Events.msft.png "figure 27: emplacements des événements DOMContentLoaded et Load sur le panneau réseau"  
[ImageTotalRequests]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-total-requests.msft.png "figure 28: le nombre total de demandes depuis DevTools a été ouverte"  
[ImageTotalSize]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-total-download-size.msft.png "figure 29: taille totale du téléchargement de demandes"  
[ImageInitiatorStack]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-Initiator-Stack.msft.png "figure 30: trace de pile aboutissant à une demande de ressource"  
[ImageUncompressedResources]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-Uncompressed-compare.msft.png "figure 31: exemple de ressources non comprimées"  
[ImageSaveAsHAR]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-Save-har-content.msft.png "figure 32: sélectionnez Enregistrer sous le contenu  
[ImageCopyResponse]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-Copy-Response.msft.png "figure 33: sélection de l’option copier la réponse"  
[ImageHideFiltersButton]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Resources-Hide-Filters-Button.msft.png "figure 34: bouton Masquer les filtres"  
[ImageLargeRequestRows]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-large-Request-Rows.msft.png "figure 35: exemple de grandes lignes de requête dans le volet demandes"  
[ImageLargeRequestRowsCheckbox]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-use-large-Request-Rows-on.msft.png "figure 36: case à cocher grandes lignes de requête"  
[ImageHideOverviewCheckbox]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-Show-Overview-OFF.msft.png "figure 37: case à cocher Masquer la vue d’ensemble"  

<!-- links -->  

[DevtoolsProgressiveWebApps]: /microsoft-edge/devtools-guide-chromium/network/progressive-web-apps "Déboguer des applications Web progressives"  

<!--[NetworkConditions]: /microsoft-edge/devtools-guide-chromium/network/network-conditions "Optimize Performance Under Varying Network Conditions"  -->  

[MDNHTTPDataURIs]: https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/Data_URIs "URL de données | MDN"  

[WikiProxyServer]: https://en.wikipedia.org/wiki/Proxy_server "Serveur proxy-Wikipédia"  

> [!NOTE]
> <span data-ttu-id="6454e-550">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6454e-550">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="6454e-551">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/network/reference) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="6454e-551">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="6454e-553">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6454e-553">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
