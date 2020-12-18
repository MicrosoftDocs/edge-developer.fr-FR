---
description: Référence complète des fonctionnalités du panneau réseau de Microsoft Edge DevTools.
title: Référence d’analyse du réseau
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: c600197ffa0e415fe42aecc704a523d1b23f8260
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230753"
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

# <span data-ttu-id="d8516-104">Référence d’analyse du réseau</span><span class="sxs-lookup"><span data-stu-id="d8516-104">Network Analysis reference</span></span>  

<span data-ttu-id="d8516-105">Découvrez de nouvelles façons d’analyser le chargement de votre page dans cette référence complète des fonctionnalités d’analyse du réseau Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="d8516-105">Discover new ways to analyze how your page loads in this comprehensive reference of Microsoft Edge DevTools network analysis features.</span></span>  

## <span data-ttu-id="d8516-106">Enregistrer les requêtes réseau</span><span class="sxs-lookup"><span data-stu-id="d8516-106">Record network requests</span></span>  

<span data-ttu-id="d8516-107">Par défaut, DevTools enregistre toutes les demandes réseau dans le panneau **réseau** , tant que devtools est ouvert.</span><span class="sxs-lookup"><span data-stu-id="d8516-107">By default, DevTools record all network requests in the **Network** panel, so long as DevTools is open.</span></span>  

:::image type="complex" source="../media/network-network-panel.msft.png" alt-text="Panneau réseau" lightbox="../media/network-network-panel.msft.png":::
   <span data-ttu-id="d8516-109">Panneau **réseau**</span><span class="sxs-lookup"><span data-stu-id="d8516-109">The **Network** panel</span></span>  
:::image-end:::  

### <span data-ttu-id="d8516-110">Arrêter l’enregistrement des requêtes réseau</span><span class="sxs-lookup"><span data-stu-id="d8516-110">Stop recording network requests</span></span>  

<span data-ttu-id="d8516-111">Pour arrêter l’enregistrement de demandes, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="d8516-111">To stop recording requests, complete the following steps.</span></span>  

1.  <span data-ttu-id="d8516-112">Dans le volet **réseau** , cliquez sur **arrêter l’enregistrement du journal réseau** \ ( ![ arrêter l’enregistrement du journal réseau ][ImageRecordOnIcon] \).</span><span class="sxs-lookup"><span data-stu-id="d8516-112">On the **Network** panel, choose **Stop recording network log** \(![Stop recording network log][ImageRecordOnIcon]\).</span></span>  <span data-ttu-id="d8516-113">Il devient gris pour indiquer que DevTools n’enregistre plus les demandes.</span><span class="sxs-lookup"><span data-stu-id="d8516-113">It turns grey to indicate that DevTools is no longer recording requests.</span></span>  
1.  <span data-ttu-id="d8516-114">`Control` + `E` Dans le panneau réseau du réseau, sélectionnez \ (Windows, Linux \) ou `Command` + `E` \ (MacOS \). \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="d8516-114">Select `Control`+`E` \(Windows, Linux\) or `Command`+`E` \(macOS\) while the **Network** panel is in focus.</span></span>  

### <span data-ttu-id="d8516-115">Supprimer des demandes</span><span class="sxs-lookup"><span data-stu-id="d8516-115">Clear requests</span></span>  

<span data-ttu-id="d8516-116">\*\*\*\* ![ Dans le volet réseau, sélectionnez Effacer \ (Clear ][ImageClearIcon] \) pour effacer toutes les demandes de la table demandes. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="d8516-116">Choose **Clear** \(![Clear][ImageClearIcon]\) on the **Network** panel to clear all requests from the Requests table.</span></span>  

:::image type="complex" source="../media/network-network-clear-button.msft.png" alt-text="Bouton Effacer" lightbox="../media/network-network-clear-button.msft.png":::
   <span data-ttu-id="d8516-118">Bouton **Effacer**</span><span class="sxs-lookup"><span data-stu-id="d8516-118">The **Clear** button</span></span>  
:::image-end:::  

### <span data-ttu-id="d8516-119">Enregistrer les demandes lors du chargement de la page</span><span class="sxs-lookup"><span data-stu-id="d8516-119">Save requests across page loads</span></span>  

<span data-ttu-id="d8516-120">Pour enregistrer les demandes lors du chargement de la page, dans le panneau **réseau** , activez la case à cocher **conserver le journal** .</span><span class="sxs-lookup"><span data-stu-id="d8516-120">To save requests across page loads, on the **Network** panel, turn on the **Preserve log** checkbox.</span></span>  <span data-ttu-id="d8516-121">DevTools enregistre toutes les demandes jusqu’à ce que vous désactiviez le **Journal de conservation**.</span><span class="sxs-lookup"><span data-stu-id="d8516-121">DevTools saves all requests until you disable **Preserve log**.</span></span>  

:::image type="complex" source="../media/network-network-preserve-log.msft.png" alt-text="Case à cocher conserver le journal" lightbox="../media/network-network-preserve-log.msft.png":::
   <span data-ttu-id="d8516-123">Case à cocher **conserver le journal**</span><span class="sxs-lookup"><span data-stu-id="d8516-123">The **Preserve Log** checkbox</span></span>  
:::image-end:::  

### <span data-ttu-id="d8516-124">Capture de captures d’écran pendant le chargement de la page</span><span class="sxs-lookup"><span data-stu-id="d8516-124">Capture screenshots during page load</span></span>  

<span data-ttu-id="d8516-125">Capture des captures d’écran permettant d’analyser ce qui s’affiche pour les utilisateurs lorsque vous patientez pendant le chargement de la page.</span><span class="sxs-lookup"><span data-stu-id="d8516-125">Capture screenshots to analyze what displays for users while waiting for your page to load.</span></span>  

<span data-ttu-id="d8516-126">Pour activer les captures d’écran, choisissez **paramètres du réseau**, puis, dans le volet **réseau** , activez la case à cocher capture des captures d' **écran** .</span><span class="sxs-lookup"><span data-stu-id="d8516-126">To enable screenshots, choose **Network settings**, and on the **Network** panel, turn on the **Capture screenshots** checkbox.</span></span>  

<span data-ttu-id="d8516-127">Actualisez la page lorsque le panneau **réseau** a le focus pour capturer les captures d’écran.</span><span class="sxs-lookup"><span data-stu-id="d8516-127">Refresh the page while the **Network** panel is in focus to capture screenshots.</span></span>  

<span data-ttu-id="d8516-128">Après avoir capturé une capture d’écran, vous interagissez comme suit.</span><span class="sxs-lookup"><span data-stu-id="d8516-128">After capturing a screenshot, you interact with it in the following ways.</span></span>  

*   <span data-ttu-id="d8516-129">Survol d’une capture d’écran pour afficher le point de capture de cette capture d’écran.</span><span class="sxs-lookup"><span data-stu-id="d8516-129">Hover on a screenshot to display the point at which that screenshot was captured.</span></span>  <span data-ttu-id="d8516-130">Une ligne jaune s’affiche dans le volet **vue d’ensemble** .</span><span class="sxs-lookup"><span data-stu-id="d8516-130">A yellow line is displayed on the **Overview** pane.</span></span>  
*   <span data-ttu-id="d8516-131">Choisissez la miniature d’un écran pour filtrer toutes les demandes qui se sont produites après la capture de la capture d’écran.</span><span class="sxs-lookup"><span data-stu-id="d8516-131">Choose the thumbnail of a screen to filter out any requests that occurred after the screenshot was captured.</span></span>  
*   <span data-ttu-id="d8516-132">Double-cliquez sur une miniature pour y effectuer un zoom.</span><span class="sxs-lookup"><span data-stu-id="d8516-132">Double-click a thumbnail to zoom into it.</span></span>  

:::image type="complex" source="../media/network-network-screenshot-hover.msft.png" alt-text="Survol d’une capture d’écran" lightbox="../media/network-network-screenshot-hover.msft.png":::
   <span data-ttu-id="d8516-134">Survol d’une capture d’écran</span><span class="sxs-lookup"><span data-stu-id="d8516-134">Hover on a screenshot</span></span>  
:::image-end:::  

<!--  ### Replay XHR request  -->

<!--  To replay an XHR request, hover on the request in the Requests table, open the contextual menu \(right-click\), and choose **Replay XHR**.  -->

<!--  
:::image type="complex" source="../media/network-replay-xhr.msft.png" alt-text="Choose Replay XHR" lightbox="../media/network-replay-xhr.msft.png":::
   Choose Replay XHR  
:::image-end:::  
-->  

## <span data-ttu-id="d8516-135">Changer le comportement de chargement</span><span class="sxs-lookup"><span data-stu-id="d8516-135">Change loading behavior</span></span>  

### <span data-ttu-id="d8516-136">Émuler un visiteur pour la première fois en désactivant le cache du navigateur</span><span class="sxs-lookup"><span data-stu-id="d8516-136">Emulate a first-time visitor by disabling the browser cache</span></span>  

<span data-ttu-id="d8516-137">Pour émuler la façon dont un utilisateur a expériences sur votre site pour la première fois, activez la case à cocher **désactiver le cache** .</span><span class="sxs-lookup"><span data-stu-id="d8516-137">To emulate how a first-time user experiences your site, turn on the **Disable cache** checkbox.</span></span>  <span data-ttu-id="d8516-138">DevTools désactive le cache du navigateur.</span><span class="sxs-lookup"><span data-stu-id="d8516-138">DevTools disables the browser cache.</span></span>  <span data-ttu-id="d8516-139">Cette fonctionnalité émule plus précisément l’utilisation de la première utilisation de l’utilisateur, car les requêtes sont servies dans le cache du navigateur lors de plusieurs visites.</span><span class="sxs-lookup"><span data-stu-id="d8516-139">This feature more accurately emulates a first-time user's experience, because requests are served from the browser cache on repeat visits.</span></span>  

:::image type="complex" source="../media/network-network-disable-cache-checkbox.msft.png" alt-text="Case à cocher Désactiver le cache" lightbox="../media/network-network-disable-cache-checkbox.msft.png":::
   <span data-ttu-id="d8516-141">Case à cocher **désactiver le cache**</span><span class="sxs-lookup"><span data-stu-id="d8516-141">The **Disable Cache** checkbox</span></span>  
:::image-end:::  

#### <span data-ttu-id="d8516-142">Désactiver le cache du navigateur dans le tiroir du réseau</span><span class="sxs-lookup"><span data-stu-id="d8516-142">Disable the browser cache from the Network Conditions drawer</span></span>  

<span data-ttu-id="d8516-143">Si vous voulez désactiver le cache lorsque vous travaillez dans d’autres panneaux DevTools, utilisez le tiroir de l’état du réseau.</span><span class="sxs-lookup"><span data-stu-id="d8516-143">If you want to disable the cache while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="d8516-144">Ouvrez le tiroir de **conditions du réseau** .</span><span class="sxs-lookup"><span data-stu-id="d8516-144">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="d8516-145">Activez/désactivez la case à cocher **désactiver le cache** .</span><span class="sxs-lookup"><span data-stu-id="d8516-145">Turn on \(or off\) the **Disable cache** checkbox.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="d8516-146">Vider manuellement le cache du navigateur</span><span class="sxs-lookup"><span data-stu-id="d8516-146">Manually clear the browser cache</span></span>  

<span data-ttu-id="d8516-147">Pour vider manuellement le cache du navigateur à tout moment, ouvrez le menu contextuel (cliquez avec le bouton droit sur \) n’importe où dans la table demandes et sélectionnez **Vider le cache du navigateur**.</span><span class="sxs-lookup"><span data-stu-id="d8516-147">To manually clear the browser cache at any time, open the contextual menu \(right-click\) anywhere in the Requests table and choose **Clear Browser Cache**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cache.msft.png" alt-text="Sélectionner vider le cache du navigateur" lightbox="../media/network-network-clear-browser-cache.msft.png":::
   <span data-ttu-id="d8516-149">Sélectionner **Vider le cache du navigateur**</span><span class="sxs-lookup"><span data-stu-id="d8516-149">Choose **Clear Browser Cache**</span></span>  
:::image-end:::  

### <span data-ttu-id="d8516-150">Émuler hors connexion</span><span class="sxs-lookup"><span data-stu-id="d8516-150">Emulate offline</span></span>  

<span data-ttu-id="d8516-151">Une nouvelle classe d’applications Web, appelées [applications Web progressives][DevtoolsProgressiveWebApps], fonctionne en mode hors connexion avec l’aide des **travailleurs de service**.</span><span class="sxs-lookup"><span data-stu-id="d8516-151">A new class of web apps, named [Progressive Web Apps][DevtoolsProgressiveWebApps], functions offline with the help of **service workers**.</span></span>  <span data-ttu-id="d8516-152">Vous constaterez peut-être qu’il est utile de simuler rapidement un appareil dépourvu de connexion aux données lors de la création de ce type d’application.</span><span class="sxs-lookup"><span data-stu-id="d8516-152">You may find it useful to quickly simulate a device that has no data connection when you are building this type of app.</span></span>  

<!--[ServiceWorkers]: /web/fundamentals/getting-started/primers/service-workers  -->

<span data-ttu-id="d8516-153">Sélectionnez le menu déroulant **en ligne** , recherchez sous **présélections**, puis sélectionnez **hors ligne** pour simuler une utilisation du réseau hors connexion.</span><span class="sxs-lookup"><span data-stu-id="d8516-153">Choose the **Online** dropdown menu, search under **Presets**, and choose **Offline** to simulate an offline network experience.</span></span>  

:::image type="complex" source="../media/network-network-offline-dropdown.msft.png" alt-text="Menu déroulant hors connexion" lightbox="../media/network-network-offline-dropdown.msft.png":::
   <span data-ttu-id="d8516-155">Menu déroulant **hors connexion**</span><span class="sxs-lookup"><span data-stu-id="d8516-155">The **Offline** dropdown menu</span></span>  
:::image-end:::  

### <span data-ttu-id="d8516-156">Émuler une connexion réseau lente</span><span class="sxs-lookup"><span data-stu-id="d8516-156">Emulate slow network connections</span></span>  

<span data-ttu-id="d8516-157">Émulez des vitesses de connexion 3G, Fast 3G et autres vitesses de connexion dans le menu déroulant **en ligne** .</span><span class="sxs-lookup"><span data-stu-id="d8516-157">Emulate Slow 3G, Fast 3G, and other connection speeds from the **Online** dropdown menu.</span></span>  

:::image type="complex" source="../media/network-network-throttling-menu.msft.png" alt-text="Menu déroulant limitation" lightbox="../media/network-network-throttling-menu.msft.png":::
   <span data-ttu-id="d8516-159">Menu déroulant **limitation**</span><span class="sxs-lookup"><span data-stu-id="d8516-159">The **Throttling** dropdown menu</span></span>  
:::image-end:::  

<span data-ttu-id="d8516-160">Vous pouvez choisir parmi différents préréglages, par exemple, lente 3G ou Fast 3G.</span><span class="sxs-lookup"><span data-stu-id="d8516-160">You may choose from different presets, such as Slow 3G or Fast 3G.</span></span>  <span data-ttu-id="d8516-161">Pour ajouter vos propres Présélections personnalisées, ouvrez le menu limitation, puis **Sélectionnez**  >  **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="d8516-161">To add your own custom presets, open the Throttling menu, and choose **Custom** > **Add**.</span></span>  

<span data-ttu-id="d8516-162">DevTools affiche une icône d’avertissement en regard de l’onglet **réseau** pour vous rappeler que la limitation est activée.</span><span class="sxs-lookup"><span data-stu-id="d8516-162">DevTools displays a warning icon next to the **Network** tab to remind you that throttling is enabled.</span></span>  

#### <span data-ttu-id="d8516-163">Émuler une connexion réseau lente à partir du tiroir du réseau</span><span class="sxs-lookup"><span data-stu-id="d8516-163">Emulate slow network connections from the Network Conditions drawer</span></span>  

<span data-ttu-id="d8516-164">Si vous souhaitez limiter la connexion réseau lorsque vous travaillez dans d’autres panneaux DevTools, utilisez le tiroir de l’état du réseau.</span><span class="sxs-lookup"><span data-stu-id="d8516-164">If you want to throttle the network connection while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="d8516-165">Ouvrez le tiroir de **conditions du réseau** .</span><span class="sxs-lookup"><span data-stu-id="d8516-165">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="d8516-166">Choisissez votre vitesse de connexion dans le menu **limitation** .</span><span class="sxs-lookup"><span data-stu-id="d8516-166">Choose your connection speed from the **Throttling** menu.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="d8516-167">Effacement manuel des cookies du navigateur</span><span class="sxs-lookup"><span data-stu-id="d8516-167">Manually clear browser cookies</span></span>  

<span data-ttu-id="d8516-168">Pour effacer manuellement les cookies du navigateur à tout moment, positionnez le curseur n’importe où dans le tableau demandes, ouvrez le menu contextuel, puis sélectionnez **effacer les cookies du navigateur**.</span><span class="sxs-lookup"><span data-stu-id="d8516-168">To manually clear browser cookies at any time, hover anywhere in the Requests table, open the contextual menu \(right-click\), and choose **Clear Browser Cookies**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cookies.msft.png" alt-text="Sélectionnez effacer les cookies du navigateur." lightbox="../media/network-network-clear-browser-cookies.msft.png":::
   <span data-ttu-id="d8516-170">Sélectionnez **effacer les cookies du navigateur** .</span><span class="sxs-lookup"><span data-stu-id="d8516-170">Choose **Clear Browser Cookies**</span></span>  
:::image-end:::  

### <span data-ttu-id="d8516-171">Remplacer l’agent utilisateur</span><span class="sxs-lookup"><span data-stu-id="d8516-171">Override the user agent</span></span>  

<span data-ttu-id="d8516-172">Pour remplacer manuellement l’agent utilisateur, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="d8516-172">To manually override the user agent, use the following steps.</span></span>  

1.  <span data-ttu-id="d8516-173">Ouvrez le tiroir de **conditions du réseau** .</span><span class="sxs-lookup"><span data-stu-id="d8516-173">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="d8516-174">Désactiver la case à cocher **sélectionner automatiquement** .</span><span class="sxs-lookup"><span data-stu-id="d8516-174">Turn off the **Select automatically** checkbox.</span></span>  
1.  <span data-ttu-id="d8516-175">Choisissez une option de l’agent utilisateur dans le menu ou entrez-en un dans la zone de texte.</span><span class="sxs-lookup"><span data-stu-id="d8516-175">Choose a user agent option from the menu, or enter a custom one in the text box.</span></span>  

<!--todo: add network condition section when available -->  

## <span data-ttu-id="d8516-176">Demandes de filtre</span><span class="sxs-lookup"><span data-stu-id="d8516-176">Filter requests</span></span>  

### <span data-ttu-id="d8516-177">Filtrer les demandes par propriétés</span><span class="sxs-lookup"><span data-stu-id="d8516-177">Filter requests by properties</span></span>  

<span data-ttu-id="d8516-178">Utilisez la zone de texte **filtre** pour filtrer les demandes par propriétés, telles que le domaine ou la taille de la requête.</span><span class="sxs-lookup"><span data-stu-id="d8516-178">Use the **Filter** text box to filter requests by properties, such as the domain or size of the request.</span></span>  

<span data-ttu-id="d8516-179">Si la zone de texte n’est pas affichée, le volet **filtres** est probablement masqué.</span><span class="sxs-lookup"><span data-stu-id="d8516-179">If the text box is not displayed, the **Filters** pane is probably hidden.</span></span>  
<span data-ttu-id="d8516-180">Pour plus d’informations, accédez à [la section masquer le volet filtres](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="d8516-180">For more information, navigate to [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

:::image type="complex" source="../media/network-network-filters-textbox.msft.png" alt-text="Zone de texte filtre" lightbox="../media/network-network-filters-textbox.msft.png":::
   <span data-ttu-id="d8516-182">Zone de texte **filtre**</span><span class="sxs-lookup"><span data-stu-id="d8516-182">The **Filter** text box</span></span>  
:::image-end:::  

<span data-ttu-id="d8516-183">Vous pouvez utiliser plusieurs propriétés simultanément en séparant chaque propriété d’un espace.</span><span class="sxs-lookup"><span data-stu-id="d8516-183">You may use multiple properties simultaneously by separating each property with a space.</span></span>  <span data-ttu-id="d8516-184">Par exemple, `mime-type:image/png larger-than:1K` affiche tous les png dont la taille est supérieure à 1 kilo-octets.</span><span class="sxs-lookup"><span data-stu-id="d8516-184">For example, `mime-type:image/png larger-than:1K` displays all PNGs that are larger than 1 kilobyte.</span></span>  <span data-ttu-id="d8516-185">Les filtres multi-propriétés sont équivalents aux `AND` opérations.</span><span class="sxs-lookup"><span data-stu-id="d8516-185">The multi-property filters are equivalent to `AND` operations.</span></span>  `OR` <span data-ttu-id="d8516-186">les opérations ne sont actuellement pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="d8516-186">operations are currently not supported.</span></span>  

<span data-ttu-id="d8516-187">Liste complète des propriétés prises en charge.</span><span class="sxs-lookup"><span data-stu-id="d8516-187">The complete list of supported properties.</span></span>  

| <span data-ttu-id="d8516-188">Propriété</span><span class="sxs-lookup"><span data-stu-id="d8516-188">Property</span></span> | <span data-ttu-id="d8516-189">Détails</span><span class="sxs-lookup"><span data-stu-id="d8516-189">Details</span></span> |  
|:--- | :--- |  
| `domain` | <span data-ttu-id="d8516-190">Afficher uniquement les ressources du domaine spécifié.</span><span class="sxs-lookup"><span data-stu-id="d8516-190">Only display resources from the specified domain.</span></span>  <span data-ttu-id="d8516-191">Vous pouvez utiliser un caractère générique \ ( `*` \) pour inclure plusieurs domaines.</span><span class="sxs-lookup"><span data-stu-id="d8516-191">You may use a wildcard character \(`*`\) to include multiple domains.</span></span>  <span data-ttu-id="d8516-192">Par exemple, `*.com` affiche les ressources de tous les noms de domaine se terminant par `.com` .</span><span class="sxs-lookup"><span data-stu-id="d8516-192">For example, `*.com` displays resources from all domain names ending in `.com`.</span></span>  <span data-ttu-id="d8516-193">DevTools peuplez le menu déroulant de saisie semi-automatique avec tous les domaines trouvés.</span><span class="sxs-lookup"><span data-stu-id="d8516-193">DevTools populate the autocomplete dropdown menu with all of the domains that are found.</span></span> |  
| `has-response-header` | <span data-ttu-id="d8516-194">Affiche les ressources contenant l’en-tête de réponse HTTP spécifié.</span><span class="sxs-lookup"><span data-stu-id="d8516-194">Displays the resources that contain the specified HTTP response header.</span></span>  <span data-ttu-id="d8516-195">DevTools remplissez la liste déroulante de saisie semi-automatique avec tous les en-têtes de réponse détectés.</span><span class="sxs-lookup"><span data-stu-id="d8516-195">DevTools populate the autocomplete dropdown with all of the response headers that are found.</span></span> |  
| `is` | <span data-ttu-id="d8516-196">Utiliser `is:running` pour rechercher des `WebSocket` ressources.</span><span class="sxs-lookup"><span data-stu-id="d8516-196">Use `is:running` to find `WebSocket` resources.</span></span> |  
| `larger-than` | <span data-ttu-id="d8516-197">Affiche les ressources dont la taille est supérieure à la taille spécifiée, en octets.</span><span class="sxs-lookup"><span data-stu-id="d8516-197">Displays resources that are larger than the specified size, in bytes.</span></span>  <span data-ttu-id="d8516-198">La définition d’une valeur est égale à la valeur `1000` `1k` .</span><span class="sxs-lookup"><span data-stu-id="d8516-198">Setting a value of `1000` is equivalent to setting a value of `1k`.</span></span> |  
| `method` | <span data-ttu-id="d8516-199">Affiche les ressources récupérées par le biais d’un type de méthode HTTP spécifié.</span><span class="sxs-lookup"><span data-stu-id="d8516-199">Displays resources that were retrieved over a specified HTTP method type.</span></span>  <span data-ttu-id="d8516-200">DevTools remplissez la liste déroulante avec toutes les méthodes HTTP trouvées.</span><span class="sxs-lookup"><span data-stu-id="d8516-200">DevTools populate the dropdown with all of the HTTP methods  that are found.</span></span> |  
| `mime-type` | <span data-ttu-id="d8516-201">Affiche les ressources d’un type MIME spécifié.</span><span class="sxs-lookup"><span data-stu-id="d8516-201">Displays resources of a specified MIME type.</span></span>  <span data-ttu-id="d8516-202">DevTools remplissez la liste déroulante à l’aide de tous les types MIME trouvés.</span><span class="sxs-lookup"><span data-stu-id="d8516-202">DevTools populate the dropdown with all MIME types  that are found.</span></span> |  
| `mixed-content` | <span data-ttu-id="d8516-203">Affichez toutes les ressources de contenu mixte \ ( `mixed-content:all` \) ou uniquement celles actuellement affichées \ ( `mixed-content:displayed` \).</span><span class="sxs-lookup"><span data-stu-id="d8516-203">Show all mixed content resources \(`mixed-content:all`\) or just the ones that are currently displayed \(`mixed-content:displayed`\).</span></span> |  
| `scheme` | <span data-ttu-id="d8516-204">Affiche les ressources récupérées par le biais d’une connexion HTTP \ ( `scheme:http` \) ou protégé https \ ( `scheme:https` \).</span><span class="sxs-lookup"><span data-stu-id="d8516-204">Displays resources retrieved over unprotected HTTP \(`scheme:http`\) or protected HTTPS \(`scheme:https`\).</span></span> |  
| `set-cookie-domain` | <span data-ttu-id="d8516-205">Affiche les ressources qui ont un `Set-Cookie` en-tête avec un `Domain` attribut qui correspond à la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d8516-205">Displays resources that have a `Set-Cookie` header with a `Domain` attribute that matches the specified value.</span></span>  <span data-ttu-id="d8516-206">DevTools remplir la saisie semi-automatique avec tous les domaines de cookie détectés.</span><span class="sxs-lookup"><span data-stu-id="d8516-206">DevTools populate the autocomplete with all of the cookie domains that are found.</span></span> |  
| `set-cookie-name` | <span data-ttu-id="d8516-207">Affiche les ressources possédant un `Set-Cookie` en-tête dont le nom correspond à la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d8516-207">Displays resources that have a `Set-Cookie` header with a name that matches the specified value.</span></span>  <span data-ttu-id="d8516-208">DevTools remplir la saisie semi-automatique à l’aide du nom de cookie détecté.</span><span class="sxs-lookup"><span data-stu-id="d8516-208">DevTools populate the autocomplete with all of the cookie names that are found.</span></span> |  
| `set-cookie-value` | <span data-ttu-id="d8516-209">Affiche les ressources dont `Set-Cookie` l’en-tête comporte une valeur qui correspond à la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d8516-209">Displays resources that have a `Set-Cookie` header with a value that matches the specified value.</span></span>  <span data-ttu-id="d8516-210">DevTools remplir la saisie semi-automatique avec toutes les valeurs de cookie trouvées.</span><span class="sxs-lookup"><span data-stu-id="d8516-210">DevTools populate the autocomplete with all of the cookie values that are found.</span></span> |  
| `status-code` | <span data-ttu-id="d8516-211">Affiche les ressources qui correspondent au code d’état HTTP spécifique.</span><span class="sxs-lookup"><span data-stu-id="d8516-211">Displays resources that match the specific HTTP status code.</span></span>  <span data-ttu-id="d8516-212">DevTools remplit le menu déroulant de saisie semi-automatique avec tous les codes d’État trouvés.</span><span class="sxs-lookup"><span data-stu-id="d8516-212">DevTools populates the autocomplete dropdown menu with all of the status codes that are found.</span></span> |  

### <span data-ttu-id="d8516-213">Filtrer les demandes par type</span><span class="sxs-lookup"><span data-stu-id="d8516-213">Filter requests by type</span></span>  

<span data-ttu-id="d8516-214">Pour filtrer les demandes par type de requête, sélectionnez l’un des boutons suivants dans le volet **réseau** .</span><span class="sxs-lookup"><span data-stu-id="d8516-214">To filter requests by request type, choose the one of the following buttons on the **Network** panel.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="d8516-215">XHR</span><span class="sxs-lookup"><span data-stu-id="d8516-215">XHR</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="d8516-216">JS</span><span class="sxs-lookup"><span data-stu-id="d8516-216">JS</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="d8516-217">CSS</span><span class="sxs-lookup"><span data-stu-id="d8516-217">CSS</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="d8516-218">IMG</span><span class="sxs-lookup"><span data-stu-id="d8516-218">Img</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="d8516-219">Media</span><span class="sxs-lookup"><span data-stu-id="d8516-219">Media</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="d8516-220">Police</span><span class="sxs-lookup"><span data-stu-id="d8516-220">Font</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="d8516-221">Documentation</span><span class="sxs-lookup"><span data-stu-id="d8516-221">Doc</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="d8516-222">NOMBRES</span><span class="sxs-lookup"><span data-stu-id="d8516-222">WS</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="d8516-223">WebSocket.</span><span class="sxs-lookup"><span data-stu-id="d8516-223">WebSocket.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="d8516-224">Manifeste</span><span class="sxs-lookup"><span data-stu-id="d8516-224">Manifest</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="d8516-225">Other</span><span class="sxs-lookup"><span data-stu-id="d8516-225">Other</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="d8516-226">Tout autre type qui ne figure pas dans la liste.</span><span class="sxs-lookup"><span data-stu-id="d8516-226">Any other type not listed.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="d8516-227">Si ce n’est pas le cas, le volet **filtres** est masqué.</span><span class="sxs-lookup"><span data-stu-id="d8516-227">If the buttons do not display, the **Filters** pane may be hidden.</span></span>  
<span data-ttu-id="d8516-228">Pour plus d’informations, accédez à [la section masquer le volet filtres](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="d8516-228">For more information, navigate to [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

<span data-ttu-id="d8516-229">Pour activer plusieurs filtres de type simultanément, appuyez sur `Control` \ (Windows, Linux \) ou `Command` \ (MacOS \), puis sélectionnez.</span><span class="sxs-lookup"><span data-stu-id="d8516-229">To enable multiple type filters simultaneously, hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and then choose.</span></span>  

:::image type="complex" source="../media/network-network-type-filters.msft.png" alt-text="Utiliser les filtres de type pour afficher les ressources JS, CSS et document" lightbox="../media/network-network-type-filters.msft.png":::
   <span data-ttu-id="d8516-231">Utiliser les filtres de type pour afficher les ressources JS, CSS et document</span><span class="sxs-lookup"><span data-stu-id="d8516-231">Use the Type filters to display JS, CSS, and Document resources</span></span>  
:::image-end:::  

### <span data-ttu-id="d8516-232">Filtrer les demandes par heure</span><span class="sxs-lookup"><span data-stu-id="d8516-232">Filter requests by time</span></span>  

<span data-ttu-id="d8516-233">Sélectionnez et faites glisser vers la gauche ou la droite dans le volet **vue d’ensemble** pour afficher uniquement les demandes qui ont été actives pendant ce laps de temps.</span><span class="sxs-lookup"><span data-stu-id="d8516-233">Choose and drag left or right on the **Overview** pane to only display requests that were active during that time frame.</span></span>  <span data-ttu-id="d8516-234">Le filtre est inclusive.</span><span class="sxs-lookup"><span data-stu-id="d8516-234">The filter is inclusive.</span></span>  <span data-ttu-id="d8516-235">Toutes les demandes qui ont été actives pendant la durée en surbrillance apparaissent.</span><span class="sxs-lookup"><span data-stu-id="d8516-235">Any request that was active during the highlighted time is shown.</span></span>  

:::image type="complex" source="../media/network-network-overview-filter.msft.png" alt-text="Filtrer toutes les demandes inactives à propos de 300 ms" lightbox="../media/network-network-overview-filter.msft.png":::
   <span data-ttu-id="d8516-237">Filtrer toutes les demandes inactives à propos de 300 ms</span><span class="sxs-lookup"><span data-stu-id="d8516-237">Filter out any requests that were inactive around 300 ms</span></span>  
:::image-end:::  

### <span data-ttu-id="d8516-238">Masquer les URL de données</span><span class="sxs-lookup"><span data-stu-id="d8516-238">Hide data URLs</span></span>  

<span data-ttu-id="d8516-239">Les [URL de données][MDNHTTPDataURIs] sont des petits fichiers incorporés dans d’autres documents.</span><span class="sxs-lookup"><span data-stu-id="d8516-239">[Data URLs][MDNHTTPDataURIs] are small files embedded into other documents.</span></span>  <span data-ttu-id="d8516-240">Toute demande qui s’affiche dans la table demandes qui commence par `data:` est une URL de données.</span><span class="sxs-lookup"><span data-stu-id="d8516-240">Any request that displays in the Requests table that starts with `data:` is a data URL.</span></span>  

<span data-ttu-id="d8516-241">Pour masquer les demandes, désactivez la case à cocher **Masquer les URL de données** .</span><span class="sxs-lookup"><span data-stu-id="d8516-241">To hide the requests, turn off the **Hide data URLs** checkbox.</span></span>  

:::image type="complex" source="../media/network-network-hide-data-urls.msft.png" alt-text="Case à cocher Masquer les URL de données" lightbox="../media/network-network-hide-data-urls.msft.png":::
   <span data-ttu-id="d8516-243">Case à cocher **Masquer les URL de données**</span><span class="sxs-lookup"><span data-stu-id="d8516-243">The **Hide Data URLs** checkbox</span></span>  
:::image-end:::  

## <span data-ttu-id="d8516-244">Demandes de tri</span><span class="sxs-lookup"><span data-stu-id="d8516-244">Sort requests</span></span>  

<span data-ttu-id="d8516-245">Par défaut, les requêtes dans la table demandes sont triées par heure de début, mais vous pouvez trier le tableau en utilisant d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="d8516-245">By default, the requests in the Requests table are sorted by initiation time, but you may sort the table using other criteria.</span></span>  

### <span data-ttu-id="d8516-246">Trier par colonne</span><span class="sxs-lookup"><span data-stu-id="d8516-246">Sort by column</span></span>  

<span data-ttu-id="d8516-247">Sélectionnez l’en-tête de n’importe quelle colonne dans les requêtes pour trier les demandes en se sur cette colonne.</span><span class="sxs-lookup"><span data-stu-id="d8516-247">Choose the header of any column in the Requests to sort requests by that column.</span></span>  

### <span data-ttu-id="d8516-248">Trier par phase d’activité</span><span class="sxs-lookup"><span data-stu-id="d8516-248">Sort by activity phase</span></span>  

<span data-ttu-id="d8516-249">Pour modifier la façon dont les demandes de tri d’une cascade sont triées, pointez sur l’en-tête de la table demandes, ouvrez le menu **contextuel, puis**sélectionnez l’une des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="d8516-249">To change how the Waterfall sorts requests, hover on the header of the Requests table, open the contextual menu \(right-click\), hover on **Waterfall**, and choose one of the following options.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="d8516-250">Heure de début</span><span class="sxs-lookup"><span data-stu-id="d8516-250">Start Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="d8516-251">La première requête lancée est en haut.</span><span class="sxs-lookup"><span data-stu-id="d8516-251">The first request that was initiated is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="d8516-252">Temps de réponse</span><span class="sxs-lookup"><span data-stu-id="d8516-252">Response Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="d8516-253">La première demande qui a démarré le téléchargement est en haut.</span><span class="sxs-lookup"><span data-stu-id="d8516-253">The first request that started downloading is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="d8516-254">Heure de fin</span><span class="sxs-lookup"><span data-stu-id="d8516-254">End Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="d8516-255">La première demande qui est terminée est en haut.</span><span class="sxs-lookup"><span data-stu-id="d8516-255">The first request that finished is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="d8516-256">Durée totale</span><span class="sxs-lookup"><span data-stu-id="d8516-256">Total Duration</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="d8516-257">La requête avec les paramètres de connexion les plus courts et la requête ou la réponse est située dans la partie supérieure.</span><span class="sxs-lookup"><span data-stu-id="d8516-257">The request with the shortest connection settings and request or response is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="d8516-258">Latence</span><span class="sxs-lookup"><span data-stu-id="d8516-258">Latency</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="d8516-259">La requête qui a attendu le plus court délai d’une réponse est située en haut.</span><span class="sxs-lookup"><span data-stu-id="d8516-259">The request that waited the shortest time for a response is at the top.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="d8516-260">Ces descriptions présupposent que chaque option respective est classée du plus court au plus long.</span><span class="sxs-lookup"><span data-stu-id="d8516-260">These descriptions assume that each respective option is ranked from shortest to longest.</span></span>  <span data-ttu-id="d8516-261">Sélectionnez l’en-tête de la colonne **cascade** pour inverser l’ordre.</span><span class="sxs-lookup"><span data-stu-id="d8516-261">Choose the header of the **Waterfall** column to reverse the order.</span></span>  

:::image type="complex" source="../media/network-network-waterfall-total-duration.msft.png" alt-text="Trier en cascade la durée totale" lightbox="../media/network-network-waterfall-total-duration.msft.png":::
   <span data-ttu-id="d8516-263">Trier les cascades en fonction de la durée totale \ (la partie plus claire de chaque barre est le temps passé en attente et la partie plus foncée est le temps de télécharger les octets \)</span><span class="sxs-lookup"><span data-stu-id="d8516-263">Sort the Waterfall by total duration  \(The lighter portion of each bar is time spent waiting and the darker portion is time spent downloading bytes\)</span></span>  
:::image-end:::  

## <span data-ttu-id="d8516-264">Analyser les requêtes</span><span class="sxs-lookup"><span data-stu-id="d8516-264">Analyze requests</span></span>  

<span data-ttu-id="d8516-265">Tant que DevTools est ouvert, il enregistre toutes les demandes dans le panneau **réseau** .</span><span class="sxs-lookup"><span data-stu-id="d8516-265">So long as DevTools are open, it logs all requests in the **Network** panel.</span></span>  
<span data-ttu-id="d8516-266">Utilisez le volet réseau pour analyser les requêtes.</span><span class="sxs-lookup"><span data-stu-id="d8516-266">Use the Network panel to analyze requests.</span></span>  

### <span data-ttu-id="d8516-267">Afficher un journal de demandes</span><span class="sxs-lookup"><span data-stu-id="d8516-267">Display a log of requests</span></span>  

<span data-ttu-id="d8516-268">Utilisez le tableau demandes pour afficher un journal de toutes les demandes effectuées lors de l’ouverture de DevTools.</span><span class="sxs-lookup"><span data-stu-id="d8516-268">Use the Requests table to display a log of all requests made while DevTools have been open.</span></span>  <span data-ttu-id="d8516-269">Pour obtenir des informations supplémentaires sur chaque élément, choisissez ou pointez sur demandes.</span><span class="sxs-lookup"><span data-stu-id="d8516-269">To reveals more information about each item, choose or hover on requests.</span></span>  

:::image type="complex" source="../media/network-network-requests-table.msft.png" alt-text="Table demandes" lightbox="../media/network-network-requests-table.msft.png":::
   <span data-ttu-id="d8516-271">Table demandes</span><span class="sxs-lookup"><span data-stu-id="d8516-271">The Requests table</span></span>  
:::image-end:::  

<span data-ttu-id="d8516-272">La table demandes affiche les colonnes suivantes par défaut.</span><span class="sxs-lookup"><span data-stu-id="d8516-272">The Requests table displays the following columns by default.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="d8516-273">Nom</span><span class="sxs-lookup"><span data-stu-id="d8516-273">Name</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="d8516-274">Nom de fichier ou un identificateur pour la ressource.</span><span class="sxs-lookup"><span data-stu-id="d8516-274">The filename of, or an identifier for, the resource.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="d8516-275">Statut</span><span class="sxs-lookup"><span data-stu-id="d8516-275">Status</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="d8516-276">Code d’état HTTP.</span><span class="sxs-lookup"><span data-stu-id="d8516-276">The HTTP status code.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="d8516-277">Type</span><span class="sxs-lookup"><span data-stu-id="d8516-277">Type</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="d8516-278">Type MIME de la ressource demandée.</span><span class="sxs-lookup"><span data-stu-id="d8516-278">The MIME type of the requested resource.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="d8516-279">Initiateur</span><span class="sxs-lookup"><span data-stu-id="d8516-279">Initiator</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="d8516-280">Les objets ou processus suivants déclenchent des demandes.</span><span class="sxs-lookup"><span data-stu-id="d8516-280">The following objects or processes initiate requests.</span></span>  
      
      *   <span data-ttu-id="d8516-281">**Analyseur**  Analyseur HTML pour Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d8516-281">**Parser**  The HTML parser for Microsoft Edge.</span></span>  
      *   <span data-ttu-id="d8516-282">**Rediriger**  Une redirection HTTP.</span><span class="sxs-lookup"><span data-stu-id="d8516-282">**Redirect**  An HTTP redirect.</span></span>  
      *   <span data-ttu-id="d8516-283">**Script**  Fonction JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d8516-283">**Script**  A JavaScript function.</span></span>  
      *   <span data-ttu-id="d8516-284">**Autres**  Un autre processus ou action, tel que la navigation sur une page à l’aide d’un lien ou la saisie d’une URL dans la barre d’adresses.</span><span class="sxs-lookup"><span data-stu-id="d8516-284">**Other**  Some other process or action, such as navigating to a page using a link or entering a URL in the address bar.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="d8516-285">Taille</span><span class="sxs-lookup"><span data-stu-id="d8516-285">Size</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="d8516-286">Taille combinée des en-têtes de réponse et du corps de la réponse, tel qu’il est délivré par le serveur.</span><span class="sxs-lookup"><span data-stu-id="d8516-286">The combined size of the response headers plus the response body, as delivered by the server.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="d8516-287">Heure</span><span class="sxs-lookup"><span data-stu-id="d8516-287">Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="d8516-288">Durée totale, entre le début de la demande et la réception de l’octet final dans la réponse.</span><span class="sxs-lookup"><span data-stu-id="d8516-288">The total duration, from the start of the request to the receipt of the final byte in the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="d8516-289">Cascade</span><span class="sxs-lookup"><span data-stu-id="d8516-289">Waterfall</span></span>](#display-the-timing-relationship-of-requests)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="d8516-290">Répartition visuelle de l’activité pour chaque demande.</span><span class="sxs-lookup"><span data-stu-id="d8516-290">A visual breakdown of the activity for each request.</span></span>  
   :::column-end:::
:::row-end:::  

#### <span data-ttu-id="d8516-291">Ajouter ou supprimer des colonnes</span><span class="sxs-lookup"><span data-stu-id="d8516-291">Add or remove columns</span></span>  

<span data-ttu-id="d8516-292">Placez le pointeur de la souris sur l’en-tête de la table demandes, ouvrez le menu contextuel (cliquez avec le bouton droit sur \), puis choisissez une option pour masquer ou afficher le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="d8516-292">Hover on the header of the Requests table, open the contextual menu \(right-click\), and choose an option to hide or show it.</span></span>  <span data-ttu-id="d8516-293">Les options actuellement affichées disposent de coches en regard de chaque élément.</span><span class="sxs-lookup"><span data-stu-id="d8516-293">Currently displayed options have checkmarks next to each item.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-column.msft.png" alt-text="Ajouter une colonne à la table demandes" lightbox="../media/network-network-requests-add-column.msft.png":::
   <span data-ttu-id="d8516-295">Ajouter une colonne à la table demandes</span><span class="sxs-lookup"><span data-stu-id="d8516-295">Add a column to the Requests table</span></span>  
:::image-end:::  

#### <span data-ttu-id="d8516-296">Ajouter des colonnes personnalisées</span><span class="sxs-lookup"><span data-stu-id="d8516-296">Add custom columns</span></span>  

<span data-ttu-id="d8516-297">Pour ajouter une colonne personnalisée dans la table demandes, positionnez le curseur sur l’en-tête de la table demandes, ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \), puis sélectionnez les **en-têtes de réponse**  >  **gérer les colonnes d’en-tête**.</span><span class="sxs-lookup"><span data-stu-id="d8516-297">To add a custom column to the Requests table, hover on the header of the Requests table, open the contextual menu \(right-click\), and choose **Response Headers** > **Manage Header Columns**.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-custom.msft.png" alt-text="Ajouter une colonne personnalisée à la table demandes" lightbox="../media/network-network-requests-add-custom.msft.png":::
   <span data-ttu-id="d8516-299">Ajouter une colonne personnalisée à la table demandes</span><span class="sxs-lookup"><span data-stu-id="d8516-299">Add a custom column to the Requests table</span></span>  
:::image-end:::  

### <span data-ttu-id="d8516-300">Afficher la relation de minutage des requêtes</span><span class="sxs-lookup"><span data-stu-id="d8516-300">Display the timing relationship of requests</span></span>  

<span data-ttu-id="d8516-301">Utilisez la cascade pour afficher les relations de minutage des requêtes.</span><span class="sxs-lookup"><span data-stu-id="d8516-301">Use the Waterfall to display the timing relationships of requests.</span></span>  
<span data-ttu-id="d8516-302">L’organisation par défaut de la cascade utilise l’heure de début des requêtes.</span><span class="sxs-lookup"><span data-stu-id="d8516-302">The default organization of the Waterfall uses the start time of the requests.</span></span>  
<span data-ttu-id="d8516-303">Par conséquent, les demandes qui sont plus éloignées du volet gauche sont restées plus anciennes que celles qui sont plus éloignées.</span><span class="sxs-lookup"><span data-stu-id="d8516-303">So, requests that are farther to the left started earlier than the requests that are farther to the right.</span></span>  

<span data-ttu-id="d8516-304">Pour passer en revue les différentes façons dont vous pouvez trier les cascade, sélectionnez [Trier par phase d’activité](#sort-by-activity-phase).</span><span class="sxs-lookup"><span data-stu-id="d8516-304">To review the different ways that you may sort the Waterfall, navigate to [Sort by activity phase](#sort-by-activity-phase).</span></span>  

:::image type="complex" source="../media/network-network-requests-waterfall.msft.png" alt-text="Colonne cascade du volet demandes" lightbox="../media/network-network-requests-waterfall.msft.png":::
   <span data-ttu-id="d8516-306">Colonne cascade du volet **demandes**</span><span class="sxs-lookup"><span data-stu-id="d8516-306">The Waterfall column of the **Requests** pane</span></span>  
:::image-end:::  

<!-- ### Analyze the frames of a WebSocket Connection  -->

<!--To review the frames of a WebSocket connection, use the following steps.  

1.  Choose the URL of the WebSocket connection, under the **Name** column of the Requests table.  
1.  Choose the **Frames** tab.  The table shows the last 100 frames.  

To refresh the table, re-choose the name of the WebSocket connection under the **Name** column of the Requests table.  -->

<!--
:::image type="complex" source="../media/network-frames.msft.png" alt-text="The Frames tab" lightbox="../media/network-frames.msft.png":::
   The **Frames** tab  
:::image-end:::  
-->

<!--The table contains the following three columns.  

*   **Data**.  The message payload.  If the message is plain text, it is displayed here.  For binary opcodes, this column displays the name and code of the opcode.  The following opcodes are supported: Continuation Frame, Binary Frame, Connection Close Frame, Ping Frame, and Pong Frame.  
*   **Length**.  The length of the message payload, in bytes.  
*   **Time**.  The time when the message was received or sent.  -->

<!--Messages are color-coded according to each type.  

*   Outgoing text messages are light-green.  
*   Incoming text messages are white.  
*   WebSocket opcodes are light-yellow.  
*   Errors are light-red.  -->

### <span data-ttu-id="d8516-307">Afficher un aperçu d’un corps de réponse</span><span class="sxs-lookup"><span data-stu-id="d8516-307">Display a preview of a response body</span></span>  

<span data-ttu-id="d8516-308">Pour afficher un aperçu du corps de la réponse, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="d8516-308">To display a preview of a response body, use the following steps.</span></span>  

1.  <span data-ttu-id="d8516-309">Sélectionnez l’URL de la requête dans la colonne **nom** de la table demandes.</span><span class="sxs-lookup"><span data-stu-id="d8516-309">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="d8516-310">Sélectionnez l’onglet **Aperçu** .</span><span class="sxs-lookup"><span data-stu-id="d8516-310">Choose the **Preview** tab.</span></span>  

<span data-ttu-id="d8516-311">L’onglet Aperçu est principalement utile pour afficher des images.</span><span class="sxs-lookup"><span data-stu-id="d8516-311">The Preview tab is mostly useful to display images.</span></span>  

:::image type="complex" source="../media/network-network-resources-preview.msft.png" alt-text="Onglet Aperçu" lightbox="../media/network-network-resources-preview.msft.png":::
   <span data-ttu-id="d8516-313">Onglet **Aperçu**</span><span class="sxs-lookup"><span data-stu-id="d8516-313">The **Preview** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="d8516-314">Afficher un corps de réponse</span><span class="sxs-lookup"><span data-stu-id="d8516-314">Display a response body</span></span>  

<span data-ttu-id="d8516-315">Pour afficher le corps de la réponse à une demande, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="d8516-315">To display the response body to a request, use the following steps.</span></span>  

1.  <span data-ttu-id="d8516-316">Sélectionnez l’URL de la requête dans la colonne **nom** de la table demandes.</span><span class="sxs-lookup"><span data-stu-id="d8516-316">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="d8516-317">Sélectionnez l’onglet **réponse** .</span><span class="sxs-lookup"><span data-stu-id="d8516-317">Choose the **Response** tab.</span></span>  

:::image type="complex" source="../media/network-network-resources-response.msft.png" alt-text="Onglet réponse" lightbox="../media/network-network-resources-response.msft.png":::
   <span data-ttu-id="d8516-319">Onglet **réponse**</span><span class="sxs-lookup"><span data-stu-id="d8516-319">The **Response** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="d8516-320">Afficher les en-têtes HTTP</span><span class="sxs-lookup"><span data-stu-id="d8516-320">Display HTTP headers</span></span>  

<span data-ttu-id="d8516-321">Pour afficher des données d’en-tête HTTP sur une requête, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="d8516-321">To display HTTP header data about a request, use the following steps.</span></span>  

1.  <span data-ttu-id="d8516-322">Sélectionnez l’URL de la requête dans la colonne **nom** de la table demandes.</span><span class="sxs-lookup"><span data-stu-id="d8516-322">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="d8516-323">Cliquez sur l’onglet **en-têtes** .</span><span class="sxs-lookup"><span data-stu-id="d8516-323">Choose the **Headers** tab.</span></span>  

:::image type="complex" source="../media/network-resources-headers.msft.png" alt-text="Onglet en-têtes" lightbox="../media/network-resources-headers.msft.png":::
   <span data-ttu-id="d8516-325">Onglet **en-têtes**</span><span class="sxs-lookup"><span data-stu-id="d8516-325">The **Headers** tab</span></span>  
:::image-end:::  

#### <span data-ttu-id="d8516-326">Afficher une source d’en-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="d8516-326">Display HTTP header source</span></span>  

<span data-ttu-id="d8516-327">Par défaut, l’onglet en-têtes affiche les noms des en-têtes par ordre alphabétique.</span><span class="sxs-lookup"><span data-stu-id="d8516-327">By default, the Headers tab shows header names alphabetically.</span></span>  <span data-ttu-id="d8516-328">Pour désactivé présente les noms d’en-tête HTTP dans l’ordre de réception, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="d8516-328">To dsiplay the HTTP header names in the order received, use the following steps.</span></span>  

1.  <span data-ttu-id="d8516-329">Ouvrez l’onglet **en-têtes** pour la requête qui vous intéresse.</span><span class="sxs-lookup"><span data-stu-id="d8516-329">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="d8516-330">Pour plus d’informations, accédez à [afficher les en-têtes http](#display-http-headers).</span><span class="sxs-lookup"><span data-stu-id="d8516-330">For more information, navigate to [Display HTTP headers](#display-http-headers).</span></span>  
1.  <span data-ttu-id="d8516-331">Sélectionnez **afficher la source**, en regard de la section en **-tête de requête** ou **en-tête de réponse** .</span><span class="sxs-lookup"><span data-stu-id="d8516-331">Choose **view source**, next to the **Request Header** or **Response Header** section.</span></span>  

### <span data-ttu-id="d8516-332">Afficher les paramètres de chaîne de requête</span><span class="sxs-lookup"><span data-stu-id="d8516-332">Display query string parameters</span></span>  

<span data-ttu-id="d8516-333">Pour afficher les paramètres de chaîne de requête d’une URL dans un format lisible par l’utilisateur, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="d8516-333">To display the query string parameters of a URL in a human-readable format, use the following steps.</span></span>  

1.  <span data-ttu-id="d8516-334">Ouvrez l’onglet **en-têtes** pour la requête qui vous intéresse.</span><span class="sxs-lookup"><span data-stu-id="d8516-334">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="d8516-335">Pour plus d’informations, accédez à [afficher les en-têtes http](#display-http-headers).</span><span class="sxs-lookup"><span data-stu-id="d8516-335">For more information, navigate to [Display HTTP headers](#display-http-headers).</span></span>  
1.  <span data-ttu-id="d8516-336">Accédez à la section **paramètres de chaîne de requête** .</span><span class="sxs-lookup"><span data-stu-id="d8516-336">Go to the **Query String Parameters** section.</span></span>  

:::image type="complex" source="../media/network-network-resources-headers-query-string-parameters.msft.png" alt-text="Section paramètres de chaîne de requête" lightbox="../media/network-network-resources-headers-query-string-parameters.msft.png":::
   <span data-ttu-id="d8516-338">Section **paramètres de chaîne de requête**</span><span class="sxs-lookup"><span data-stu-id="d8516-338">The **Query String Parameters** section</span></span>  
:::image-end:::  

#### <span data-ttu-id="d8516-339">Afficher les paramètres de chaîne de requête source</span><span class="sxs-lookup"><span data-stu-id="d8516-339">Display query string parameters source</span></span>  

<span data-ttu-id="d8516-340">Pour afficher la source du paramètre de chaîne de requête d’une demande, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="d8516-340">To display the query string parameter source of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="d8516-341">Accédez à la section paramètres de chaîne de requête.</span><span class="sxs-lookup"><span data-stu-id="d8516-341">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="d8516-342">Pour plus d’informations, accédez à [afficher les paramètres de chaîne de requête](#display-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="d8516-342">For more information, navigate to [Display query string parameters](#display-query-string-parameters).</span></span>  
1.  <span data-ttu-id="d8516-343">Sélectionnez **afficher la source**.</span><span class="sxs-lookup"><span data-stu-id="d8516-343">Choose **view source**.</span></span>  

#### <span data-ttu-id="d8516-344">Afficher les paramètres de chaîne de requête codés en URL</span><span class="sxs-lookup"><span data-stu-id="d8516-344">Display URL-encoded query string parameters</span></span>  

<span data-ttu-id="d8516-345">Pour afficher les paramètres de chaîne de requête dans un format lisible par l’utilisateur, mais avec les codages prédéfinis, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="d8516-345">To display query string parameters in a human-readable format, but with encodings preserved, use the following steps.</span></span>  

1.  <span data-ttu-id="d8516-346">Accédez à la section paramètres de chaîne de requête.</span><span class="sxs-lookup"><span data-stu-id="d8516-346">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="d8516-347">Pour plus d’informations, accédez à [afficher les paramètres de chaîne de requête](#display-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="d8516-347">For more information, navigate to [Display query string parameters](#display-query-string-parameters).</span></span>  
1.  <span data-ttu-id="d8516-348">Choisissez **affichage URL encodée**.</span><span class="sxs-lookup"><span data-stu-id="d8516-348">Choose **view URL encoded**.</span></span>  

### <span data-ttu-id="d8516-349">Afficher les cookies</span><span class="sxs-lookup"><span data-stu-id="d8516-349">Display cookies</span></span>  

<span data-ttu-id="d8516-350">Pour afficher les cookies envoyés dans l’en-tête HTTP d’une requête, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="d8516-350">To display the cookies sent in the HTTP header of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="d8516-351">Sélectionnez l’URL de la requête dans la colonne **nom** de la table demandes.</span><span class="sxs-lookup"><span data-stu-id="d8516-351">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="d8516-352">Sélectionnez l’onglet **cookies** .</span><span class="sxs-lookup"><span data-stu-id="d8516-352">Choose the **Cookies** tab.</span></span>  

<!--For more information about each of the columns, navigate to [Fields][ManageDataCookiesFields].  -->  

<!--[ManageDataCookiesFields]: manage-data/cookies#fields  -->  
<!--TODO: add link when section is available -->  

:::image type="complex" source="../media/network-network-resources-cookies.msft.png" alt-text="Onglet cookies" lightbox="../media/network-network-resources-cookies.msft.png":::
   <span data-ttu-id="d8516-354">Onglet cookies</span><span class="sxs-lookup"><span data-stu-id="d8516-354">The Cookies tab</span></span>  
:::image-end:::  

### <span data-ttu-id="d8516-355">Afficher la répartition du minutage d’une requête</span><span class="sxs-lookup"><span data-stu-id="d8516-355">Display the timing breakdown of a request</span></span>  

<span data-ttu-id="d8516-356">Pour afficher la répartition du minutage d’une demande, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="d8516-356">To display the timing breakdown of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="d8516-357">Sélectionnez l’URL de la requête dans la colonne **nom** de la table demandes.</span><span class="sxs-lookup"><span data-stu-id="d8516-357">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="d8516-358">Sélectionnez l’onglet **minutage** .</span><span class="sxs-lookup"><span data-stu-id="d8516-358">Choose the **Timing** tab.</span></span>  

<span data-ttu-id="d8516-359">Pour accéder aux données plus rapidement, accédez à aperçu d' [une répartition du minutage](#preview-a-timing-breakdown).</span><span class="sxs-lookup"><span data-stu-id="d8516-359">For a faster way to access the data, navigate to [Preview a timing breakdown](#preview-a-timing-breakdown).</span></span>  

<span data-ttu-id="d8516-360">Pour plus d’informations sur les différentes phases qui s’affichent dans l’onglet **minutage** , accédez à la [rubrique étapes de répartition du temps](#timing-breakdown-phases-explained).</span><span class="sxs-lookup"><span data-stu-id="d8516-360">For more information about each of the phases that may be displayed in the **Timing** tab, navigate to [Timing breakdown phases explained](#timing-breakdown-phases-explained).</span></span>  

:::image type="complex" source="../media/network-network-resources-timing.msft.png" alt-text="Onglet Minutage" lightbox="../media/network-network-resources-timing.msft.png":::
   <span data-ttu-id="d8516-362">Onglet **minutage**</span><span class="sxs-lookup"><span data-stu-id="d8516-362">The **Timing** tab</span></span>  
:::image-end:::  

<span data-ttu-id="d8516-363">Plus d’informations sur chacune de ces étapes.</span><span class="sxs-lookup"><span data-stu-id="d8516-363">More information about each of the phases.</span></span>  

<span data-ttu-id="d8516-364">Pour plus d’informations sur l’accès à l’affichage, accédez à l' [affichage répartition du minutage](#display-the-timing-breakdown-of-a-request).</span><span class="sxs-lookup"><span data-stu-id="d8516-364">For more information about accessing the display, navigate to [Display timing breakdown](#display-the-timing-breakdown-of-a-request).</span></span>  

#### <span data-ttu-id="d8516-365">Prévisualiser une répartition de minutage</span><span class="sxs-lookup"><span data-stu-id="d8516-365">Preview a timing breakdown</span></span>  

<span data-ttu-id="d8516-366">Pour afficher un aperçu de la répartition du minutage d’une requête, dans la colonne en **cascade** de la table demandes, pointez sur l’entrée de la requête.</span><span class="sxs-lookup"><span data-stu-id="d8516-366">To display a preview of the timing breakdown of a request, in the **Waterfall** column of the Requests table, hover on the entry for the request.</span></span>  

<span data-ttu-id="d8516-367">Pour plus d’informations sur l’accès aux données sans survol, accédez à [afficher la répartition du minutage d’une demande](#display-the-timing-breakdown-of-a-request).</span><span class="sxs-lookup"><span data-stu-id="d8516-367">For more information about how to access the data without hovering, navigate to [Display the timing breakdown of a request](#display-the-timing-breakdown-of-a-request).</span></span>  

:::image type="complex" source="../media/network-network-resources-waterfall-hover.msft.png" alt-text="> afficher la répartition du minutage d’une requête" lightbox="../media/network-network-resources-waterfall-hover.msft.png":::
   <span data-ttu-id="d8516-369">Prévisualiser la répartition du minutage d’une requête</span><span class="sxs-lookup"><span data-stu-id="d8516-369">Preview the timing breakdown of a request</span></span>  
:::image-end:::  

#### <span data-ttu-id="d8516-370">Explication des phases de répartition du temps</span><span class="sxs-lookup"><span data-stu-id="d8516-370">Timing breakdown phases explained</span></span>  

<span data-ttu-id="d8516-371">Plus d’informations sur chacune des phases qui s’affichent dans l’onglet **minutage** .</span><span class="sxs-lookup"><span data-stu-id="d8516-371">More information about each of the phases that may display in the **Timing** tab.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="d8516-372">Mise en file d’attente</span><span class="sxs-lookup"><span data-stu-id="d8516-372">Queueing</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="d8516-373">Le navigateur met en file d’attente les demandes lorsque l’une des conditions suivantes est vraie.</span><span class="sxs-lookup"><span data-stu-id="d8516-373">The browser queues requests when any of the following are true.</span></span>  
      
      *   <span data-ttu-id="d8516-374">Il existe des demandes de priorité élevée.</span><span class="sxs-lookup"><span data-stu-id="d8516-374">Higher priority requests exist.</span></span>  
      *   <span data-ttu-id="d8516-375">Six connexions TCP sont ouvertes pour la même origine, qui correspond à la limite.</span><span class="sxs-lookup"><span data-stu-id="d8516-375">Six TCP connections are open for the same origin, which is the limit.</span></span>  <span data-ttu-id="d8516-376">S’applique uniquement aux protocoles HTTP/1.0 et HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="d8516-376">Applies to HTTP/1.0 and HTTP/1.1 only.</span></span>  
      *   <span data-ttu-id="d8516-377">Le navigateur alloue de l’espace dans le cache disque.</span><span class="sxs-lookup"><span data-stu-id="d8516-377">The browser is briefly allocating space in the disk cache.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="d8516-378">Bloquée</span><span class="sxs-lookup"><span data-stu-id="d8516-378">Stalled</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="d8516-379">La requête est bloquée pour l’une des raisons décrites dans la **file d’attente**.</span><span class="sxs-lookup"><span data-stu-id="d8516-379">The request is stalled for any of the reasons described in **Queueing**.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="d8516-380">Recherche DNS</span><span class="sxs-lookup"><span data-stu-id="d8516-380">DNS Lookup</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="d8516-381">Le navigateur résout l’adresse IP pour la requête.</span><span class="sxs-lookup"><span data-stu-id="d8516-381">The browser is resolving the IP address for the request.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="d8516-382">Connexion initiale</span><span class="sxs-lookup"><span data-stu-id="d8516-382">Initial connection</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="d8516-383">Le navigateur établit une connexion, y compris les négociations TCP, les tentatives de TCP et négocie une couche de socket sécurisée.</span><span class="sxs-lookup"><span data-stu-id="d8516-383">The browser establishes a connection including TCP handshakes, TCP retries, and negotiates a Secure Socket Layer.</span></span>
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="d8516-384">Négociation de proxy</span><span class="sxs-lookup"><span data-stu-id="d8516-384">Proxy negotiation</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="d8516-385">Le navigateur négocie la requête avec un [serveur proxy][WikiProxyServer].</span><span class="sxs-lookup"><span data-stu-id="d8516-385">The browser is negotiating the request with a [proxy server][WikiProxyServer].</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="d8516-386">Demande envoyée</span><span class="sxs-lookup"><span data-stu-id="d8516-386">Request sent</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="d8516-387">La requête est en cours d’envoi.</span><span class="sxs-lookup"><span data-stu-id="d8516-387">The request is being sent.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="d8516-388">Préparation de ServiceWorker</span><span class="sxs-lookup"><span data-stu-id="d8516-388">ServiceWorker Preparation</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="d8516-389">Le navigateur démarre le travailleur de service.</span><span class="sxs-lookup"><span data-stu-id="d8516-389">The browser is starting the service worker.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="d8516-390">Demander à ServiceWorker</span><span class="sxs-lookup"><span data-stu-id="d8516-390">Request to ServiceWorker</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="d8516-391">La demande est envoyée au travailleur de service.</span><span class="sxs-lookup"><span data-stu-id="d8516-391">The request is being sent to the service worker.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="d8516-392">En attente \ (TTFB \)</span><span class="sxs-lookup"><span data-stu-id="d8516-392">Waiting \(TTFB\)</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="d8516-393">Le navigateur attend le premier octet d’une réponse.</span><span class="sxs-lookup"><span data-stu-id="d8516-393">The browser is waiting for the first byte of a response.</span></span>  <span data-ttu-id="d8516-394">TTFB représente le temps à l’octet initial.</span><span class="sxs-lookup"><span data-stu-id="d8516-394">TTFB stands for Time To First Byte.</span></span>  <span data-ttu-id="d8516-395">Ce minutage inclut un aller-retour d’une latence et la durée du serveur pour préparer la réponse.</span><span class="sxs-lookup"><span data-stu-id="d8516-395">This timing includes one round trip of latency and the time the server took to prepare the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="d8516-396">Téléchargement du contenu</span><span class="sxs-lookup"><span data-stu-id="d8516-396">Content Download</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="d8516-397">Le navigateur reçoit la réponse.</span><span class="sxs-lookup"><span data-stu-id="d8516-397">The browser is receiving the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="d8516-398">Réception d’une émission</span><span class="sxs-lookup"><span data-stu-id="d8516-398">Receiving Push</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="d8516-399">Le navigateur reçoit des données pour cette réponse via le protocole HTTP/2 Server Poussée.</span><span class="sxs-lookup"><span data-stu-id="d8516-399">The browser is receiving data for this response via HTTP/2 Server Push.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="d8516-400">Lecture Poussée</span><span class="sxs-lookup"><span data-stu-id="d8516-400">Reading Push</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="d8516-401">Le navigateur lit les données locales précédemment reçues.</span><span class="sxs-lookup"><span data-stu-id="d8516-401">The browser is reading the local data previously received.</span></span>  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="d8516-402">Afficher les initiateurs et les dépendances</span><span class="sxs-lookup"><span data-stu-id="d8516-402">Display initiators and dependencies</span></span>  

<span data-ttu-id="d8516-403">Pour afficher les initiateurs et les dépendances d’une requête, maintenez la touche enfoncée `Shift` et placez le curseur sur la requête dans la table demandes.</span><span class="sxs-lookup"><span data-stu-id="d8516-403">To display the initiators and dependencies of a request, hold `Shift`and hover on the request in the Requests table.</span></span>  <span data-ttu-id="d8516-404">Couleurs de DevTools: les initiateurs apparaissent en vert et les dépendances apparaissent en rouge.</span><span class="sxs-lookup"><span data-stu-id="d8516-404">DevTools colors: initiators are shown in green and dependencies are shown in red.</span></span>  

:::image type="complex" source="../media/network-network-resources-initiators-dependencies.msft.png" alt-text="Afficher les initiateurs et les dépendances d’une requête" lightbox="../media/network-network-resources-initiators-dependencies.msft.png":::
   <span data-ttu-id="d8516-406">Afficher les initiateurs et les dépendances d’une requête</span><span class="sxs-lookup"><span data-stu-id="d8516-406">Display the initiators and dependencies of a request</span></span>  
:::image-end:::  

<span data-ttu-id="d8516-407">Lorsque la table requêtes est classée dans l’ordre chronologique, si vous pointez sur une ligne, la ligne qui la précède affiche une requête verte.</span><span class="sxs-lookup"><span data-stu-id="d8516-407">When the Requests table is ordered chronologically, if you hover on a line, the line preceding it displays a green request.</span></span>  <span data-ttu-id="d8516-408">La requête Green est l’initiateur de la dépendance.</span><span class="sxs-lookup"><span data-stu-id="d8516-408">The green request is the initiator of the dependency.</span></span>  <span data-ttu-id="d8516-409">Si une autre demande verte apparaît sur la ligne avant celle-ci, il s’agit de l’initiateur de l’initiateur.</span><span class="sxs-lookup"><span data-stu-id="d8516-409">If another green request is displayed on the line before that, that higher request is the initiator of the initiator.</span></span>  <span data-ttu-id="d8516-410">Et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="d8516-410">And so on.</span></span>  

### <span data-ttu-id="d8516-411">Afficher les événements de chargement</span><span class="sxs-lookup"><span data-stu-id="d8516-411">Display load events</span></span>  

<span data-ttu-id="d8516-412">DevTools affiche le minutage des `DOMContentLoaded` événements et `load` dans plusieurs emplacements du panneau **réseau** .</span><span class="sxs-lookup"><span data-stu-id="d8516-412">DevTools displays the timing of the `DOMContentLoaded` and `load` events in multiple places on the **Network** panel.</span></span>  <span data-ttu-id="d8516-413">L' `DOMContentLoaded` événement est coloré en bleu et l' `load` événement est rouge.</span><span class="sxs-lookup"><span data-stu-id="d8516-413">The `DOMContentLoaded` event is colored blue, and the `load` event is red.</span></span>  

:::image type="complex" source="../media/network-network-requests-load-events.msft.png" alt-text="Emplacements des événements DOMContentLoaded et Load sur le panneau réseau" lightbox="../media/network-network-requests-load-events.msft.png":::
   <span data-ttu-id="d8516-415">Emplacement des `DOMContentLoaded` `load` événements et dans le volet **réseau**</span><span class="sxs-lookup"><span data-stu-id="d8516-415">The locations of the `DOMContentLoaded` and `load` events on the **Network** panel</span></span>  
:::image-end:::  

### <span data-ttu-id="d8516-416">Afficher le nombre total de demandes</span><span class="sxs-lookup"><span data-stu-id="d8516-416">Display the total number of requests</span></span>  

<span data-ttu-id="d8516-417">Le nombre total de demandes est répertorié dans le volet **Résumé** , au bas du panneau **réseau** .</span><span class="sxs-lookup"><span data-stu-id="d8516-417">The total number of requests is listed in the **Summary** pane, at the bottom of the **Network** panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="d8516-418">Ce numéro suit uniquement les requêtes qui ont été enregistrées depuis l’ouverture de DevTools.</span><span class="sxs-lookup"><span data-stu-id="d8516-418">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="d8516-419">Si d’autres requêtes s’est produites avant l’ouverture de DevTools, ces demandes ne sont pas comptabilisées.</span><span class="sxs-lookup"><span data-stu-id="d8516-419">If other requests occurred before DevTools was opened, those requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-requests.msft.png" alt-text="Nombre total de demandes depuis l’ouverture de DevTools" lightbox="../media/network-network-total-requests.msft.png":::
   <span data-ttu-id="d8516-421">Nombre total de demandes depuis l’ouverture de DevTools</span><span class="sxs-lookup"><span data-stu-id="d8516-421">The total number of requests since DevTools were opened</span></span>  
:::image-end:::  

### <span data-ttu-id="d8516-422">Affichez la taille totale du téléchargement</span><span class="sxs-lookup"><span data-stu-id="d8516-422">Display the total download size</span></span>  

<span data-ttu-id="d8516-423">La taille de téléchargement totale des demandes figure dans le volet **Résumé** , en bas du volet **réseau** .</span><span class="sxs-lookup"><span data-stu-id="d8516-423">The total download size of requests is listed in the **Summary** pane, at the bottom of the **Network** panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="d8516-424">Ce numéro suit uniquement les requêtes qui ont été enregistrées depuis l’ouverture de DevTools.</span><span class="sxs-lookup"><span data-stu-id="d8516-424">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="d8516-425">Si d’autres requêtes s’est produites avant l’ouverture de DevTools, les requêtes précédentes ne sont pas comptabilisées.</span><span class="sxs-lookup"><span data-stu-id="d8516-425">If other requests occurred before DevTools was opened, the previous requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-download-size.msft.png" alt-text="La taille de téléchargement totale des requêtes" lightbox="../media/network-network-total-download-size.msft.png":::
   <span data-ttu-id="d8516-427">La taille de téléchargement totale des requêtes</span><span class="sxs-lookup"><span data-stu-id="d8516-427">The total download size of requests</span></span>  
:::image-end:::  

<span data-ttu-id="d8516-428">Pour vérifier le nombre de ressources disponibles lorsque le navigateur décompresse chaque élément, naviguez jusqu’à [afficher la taille de la ressource](#display-the-uncompressed-size-of-a-resource).</span><span class="sxs-lookup"><span data-stu-id="d8516-428">To verify how large resources are after the browser uncompresses each item, navigate to [display the uncompressed size of a resource](#display-the-uncompressed-size-of-a-resource).</span></span>  

### <span data-ttu-id="d8516-429">Afficher la trace de pile ayant entraîné une requête</span><span class="sxs-lookup"><span data-stu-id="d8516-429">Display the stack trace that caused a request</span></span>  

<span data-ttu-id="d8516-430">Après qu’une instruction JavaScript demande une ressource, pointez sur la colonne **Initiator** pour afficher la trace de pile qui se trouve au début de la requête.</span><span class="sxs-lookup"><span data-stu-id="d8516-430">After a JavaScript statement requests a resource, hover on the **Initiator** column to display the stack trace leading up to the request.</span></span>  

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
   <span data-ttu-id="d8516-432">Trace de pile aboutissant à une demande de ressources</span><span class="sxs-lookup"><span data-stu-id="d8516-432">The stack trace leading up to a resource request</span></span>  
:::image-end:::  

### <span data-ttu-id="d8516-433">Affichage de la taille de la ressource non compressée</span><span class="sxs-lookup"><span data-stu-id="d8516-433">Display the uncompressed size of a resource</span></span>  

<span data-ttu-id="d8516-434">Activez la case à cocher **utiliser des lignes de requête volumineuses** , puis examinez la dernière valeur de la colonne **taille** .</span><span class="sxs-lookup"><span data-stu-id="d8516-434">Turn on the **Use large request rows** checkbox and then review the bottom value of the **Size** column.</span></span>  

:::image type="complex" source="../media/network-network-requests-uncompressed-compare.msft.png" alt-text="Exemple de ressources non compressées" lightbox="../media/network-network-requests-uncompressed-compare.msft.png":::
   <span data-ttu-id="d8516-436">Voici un exemple de ressources non compressées \ (la taille du `jquery-3.3.1.min.js` fichier qui a été envoyée par le biais du réseau était `29.9 KB` alors la taille du fichier non compressé `84.9 KB` ).</span><span class="sxs-lookup"><span data-stu-id="d8516-436">An example of uncompressed resources  \(The compressed size of the `jquery-3.3.1.min.js` file that was sent over the network was `29.9 KB`, whereas the uncompressed size was `84.9 KB`\)</span></span>  
:::image-end:::  

## <span data-ttu-id="d8516-437">Exporter les données de requête</span><span class="sxs-lookup"><span data-stu-id="d8516-437">Export requests data</span></span>  

### <span data-ttu-id="d8516-438">Enregistrer toutes les demandes réseau dans un fichier QAR</span><span class="sxs-lookup"><span data-stu-id="d8516-438">Save all network requests to a HAR file</span></span>  

<span data-ttu-id="d8516-439">Pour enregistrer toutes les demandes réseau dans un fichier QAR, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="d8516-439">To save all network requests to a HAR file, complete the following steps.</span></span>  

1.  <span data-ttu-id="d8516-440">Positionnez le pointeur sur une requête dans la table demandes et ouvrez le menu contextuel, puis cliquez sur le bouton droit de la souris.</span><span class="sxs-lookup"><span data-stu-id="d8516-440">Hover on any request in the Requests table and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="d8516-441">Choisissez **enregistrer en tant que le contenu**.</span><span class="sxs-lookup"><span data-stu-id="d8516-441">Choose **Save as HAR with Content**.</span></span>  <span data-ttu-id="d8516-442">DevTools enregistre toutes les demandes qui se sont produites depuis que vous avez ouvert DevTools sur le fichier.</span><span class="sxs-lookup"><span data-stu-id="d8516-442">DevTools saves all requests that have occurred since you opened DevTools to the HAR file.</span></span>  <span data-ttu-id="d8516-443">Vous ne pouvez pas filtrer les demandes.</span><span class="sxs-lookup"><span data-stu-id="d8516-443">You are not able to filter requests.</span></span>  <span data-ttu-id="d8516-444">Vous ne pouvez pas non plus enregistrer une demande unique.</span><span class="sxs-lookup"><span data-stu-id="d8516-444">You are also not able to save a single request.</span></span>  

<span data-ttu-id="d8516-445">Lorsque vous enregistrez un fichier QAR, vous pouvez l’importer de nouveau dans DevTools pour analyse.</span><span class="sxs-lookup"><span data-stu-id="d8516-445">Once you save a HAR file, you may import it back into DevTools for analysis.</span></span>  <span data-ttu-id="d8516-446">Il suffit de glisser-déplacer le fichier QAR dans la table demandes.</span><span class="sxs-lookup"><span data-stu-id="d8516-446">Just drag-and-drop the HAR file into the Requests table.</span></span>  
<!--For more information, navigate to also [HAR Analyzer][HARAnalyzer].  -->  

<!--[HARAnalyzer]: https://toolbox.alphabetapps.com/apps/har_analyzer  -->  
<!--Todo: add section link when content is available  -->  

:::image type="complex" source="../media/network-network-requests-save-har-content.msft.png" alt-text="Choisissez Enregistrer comme le contenu de votre fichier." lightbox="../media/network-network-requests-save-har-content.msft.png":::
   <span data-ttu-id="d8516-448">Choisissez **Enregistrer comme le contenu de votre fichier** .</span><span class="sxs-lookup"><span data-stu-id="d8516-448">Choose **Save as HAR with Content**</span></span>  
:::image-end:::  

### <span data-ttu-id="d8516-449">Copier une ou plusieurs demandes dans le presse-papiers</span><span class="sxs-lookup"><span data-stu-id="d8516-449">Copy one or more requests to the clipboard</span></span>  

<span data-ttu-id="d8516-450">Dans la colonne **nom** de la table demandes, positionnez le **pointeur sur une**requête, ouvrez le menu contextuel, puis sélectionnez l’une des options suivantes...</span><span class="sxs-lookup"><span data-stu-id="d8516-450">Under the **Name** column of the Requests table, hover on a request, open the contextual menu \(right-click\), hover on **Copy**, and choose one of the following options.</span></span>  

| <span data-ttu-id="d8516-451">Nom</span><span class="sxs-lookup"><span data-stu-id="d8516-451">Name</span></span> | <span data-ttu-id="d8516-452">Détails</span><span class="sxs-lookup"><span data-stu-id="d8516-452">Details</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="d8516-453">Copier l’adresse du lien</span><span class="sxs-lookup"><span data-stu-id="d8516-453">Copy Link Address</span></span>** | <span data-ttu-id="d8516-454">Copiez l’URL de la requête dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="d8516-454">Copy the URL of the request to the clipboard.</span></span> |  
| **<span data-ttu-id="d8516-455">Copier la réponse</span><span class="sxs-lookup"><span data-stu-id="d8516-455">Copy Response</span></span>** | <span data-ttu-id="d8516-456">Copiez le corps de la réponse dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="d8516-456">Copy the response body to the clipboard.</span></span> |  
| **<span data-ttu-id="d8516-457">Copier en tant qu’extraction</span><span class="sxs-lookup"><span data-stu-id="d8516-457">Copy as Fetch</span></span>** | &nbsp; |  
| **<span data-ttu-id="d8516-458">Copier sous forme de courbe</span><span class="sxs-lookup"><span data-stu-id="d8516-458">Copy as cURL</span></span>** | <span data-ttu-id="d8516-459">Copiez la demande en tant que commande en forme de boucle.</span><span class="sxs-lookup"><span data-stu-id="d8516-459">Copy the request as a cURL command.</span></span> |  
| **<span data-ttu-id="d8516-460">Copy All As Fetch</span><span class="sxs-lookup"><span data-stu-id="d8516-460">Copy All as Fetch</span></span>** | &nbsp; |  
| **<span data-ttu-id="d8516-461">Tout copier comme courbe</span><span class="sxs-lookup"><span data-stu-id="d8516-461">Copy All as cURL</span></span>** | <span data-ttu-id="d8516-462">Copiez toutes les demandes comme une chaîne de commandes bouclé.</span><span class="sxs-lookup"><span data-stu-id="d8516-462">Copy all requests as a chain of cURL commands.</span></span> |  
| **<span data-ttu-id="d8516-463">Tout copier comme.</span><span class="sxs-lookup"><span data-stu-id="d8516-463">Copy All as HAR</span></span>** | <span data-ttu-id="d8516-464">Copiez toutes les demandes en tant que données QAR.</span><span class="sxs-lookup"><span data-stu-id="d8516-464">Copy all requests as HAR data.</span></span> |  

<!--
:::row:::
   :::column span="1":::
      **Copy Link Address**  
   :::column-end:::
   :::column span="2":::
      Copy the URL of the request to the clipboard.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy Response**  
   :::column-end:::
   :::column span="2":::
      Copy the response body to the clipboard.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy as Fetch**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy as cURL**  
   :::column-end:::
   :::column span="2":::
      Copy the request as a cURL command.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy All as Fetch**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy All as cURL**  
   :::column-end:::
   :::column span="2":::
      Copy all requests as a chain of cURL commands.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy All as HAR**  
   :::column-end:::
   :::column span="2":::
      Copy all requests as HAR data.  
   :::column-end:::
:::row-end:::  
-->  

:::image type="complex" source="../media/network-network-requests-copy-response.msft.png" alt-text="Cliquez sur copier la réponse." lightbox="../media/network-network-requests-copy-response.msft.png":::
   <span data-ttu-id="d8516-466">Cliquez sur **copier la réponse** .</span><span class="sxs-lookup"><span data-stu-id="d8516-466">Choose **Copy Response**</span></span>  
:::image-end:::  

### <span data-ttu-id="d8516-467">Copier la réponse mise en forme JSON dans le presse-papiers</span><span class="sxs-lookup"><span data-stu-id="d8516-467">Copy formatted response JSON to the clipboard</span></span>  

<span data-ttu-id="d8516-468">Choisissez une requête réseau et naviguez jusqu’au volet **en-têtes** .</span><span class="sxs-lookup"><span data-stu-id="d8516-468">Choose a network request and navigate to the **Headers** pane.</span></span>  <span data-ttu-id="d8516-469">Pour copier la valeur JSON d’une réponse, accédez à **requête Payload**, pointez sur le contenu de la réponse JSON, ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \), puis sélectionnez **copier la valeur**.</span><span class="sxs-lookup"><span data-stu-id="d8516-469">To copy the JSON value of a response, navigate to **Request payload**, hover on the JSON response content, open the contextual menu \(right-click\), and choose **Copy Value**.</span></span>  

:::row:::
   :::column span="":::
        :::image type="complex" source="../media/network-header-copy-property-value.msft.png" alt-text="Copier la valeur dans le menu contextuel" lightbox="../media/network-header-copy-property-value.msft.png":::
          <span data-ttu-id="d8516-471">**Copier la valeur** dans le menu contextuel</span><span class="sxs-lookup"><span data-stu-id="d8516-471">**Copy Value** in contextual menu</span></span>  
        :::image-end:::  
   :::column-end:::
   :::column span="":::
        :::image type="complex" source="../media/network-header-paste-property-value.msft.png" alt-text="Code Visual Studio avec JSON de réponse mis en forme" lightbox="../media/network-header-paste-property-value.msft.png":::
          <span data-ttu-id="d8516-473">Collage de la réponse formatée JSON dans le code Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d8516-473">Pasting formatted response JSON in Visual Studio Code</span></span>  
        :::image-end:::  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="d8516-474">Copier les valeurs de propriétés des requêtes réseau dans le presse-papiers</span><span class="sxs-lookup"><span data-stu-id="d8516-474">Copy property values from network requests to your clipboard</span></span>  

<span data-ttu-id="d8516-475">Pour copier les valeurs de propriétés des requêtes réseau dans le presse-papiers, effectuez les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="d8516-475">To copy property values from network requests to your clipboard, complete the following actions.</span></span>  

1.  <span data-ttu-id="d8516-476">Ouvrez le volet **en-têtes** .</span><span class="sxs-lookup"><span data-stu-id="d8516-476">Open the **Headers** pane.</span></span>  
1.  <span data-ttu-id="d8516-477">Ouvrez l’une des sections d’en-tête suivantes.</span><span class="sxs-lookup"><span data-stu-id="d8516-477">Open one of the following header sections.</span></span>  
    *   <span data-ttu-id="d8516-478">Charge utile de requête \ (JSON \)</span><span class="sxs-lookup"><span data-stu-id="d8516-478">Request payload \(JSON\)</span></span>  
    *   <span data-ttu-id="d8516-479">Données de formulaire</span><span class="sxs-lookup"><span data-stu-id="d8516-479">Form Data</span></span>  
    *   <span data-ttu-id="d8516-480">Paramètres de chaîne de requête</span><span class="sxs-lookup"><span data-stu-id="d8516-480">Query String Parameters</span></span>  
    *   <span data-ttu-id="d8516-481">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="d8516-481">Request Headers</span></span>  
    *   <span data-ttu-id="d8516-482">En-têtes de réponse</span><span class="sxs-lookup"><span data-stu-id="d8516-482">Response Headers</span></span>  
1.  <span data-ttu-id="d8516-483">Ouvrir le menu contextuel \ (cliquez avec le bouton droit sur \) > **copier la valeur**.</span><span class="sxs-lookup"><span data-stu-id="d8516-483">Open the contextual menu \(right-click\) > **Copy value**.</span></span>  <span data-ttu-id="d8516-484">Vous pouvez à présent coller la valeur dans n’importe quel éditeur pour la vérifier.</span><span class="sxs-lookup"><span data-stu-id="d8516-484">You can now paste the value into any editor to review it.</span></span>  
    
## <span data-ttu-id="d8516-485">Modifier la disposition du panneau réseau</span><span class="sxs-lookup"><span data-stu-id="d8516-485">Change the layout of the Network panel</span></span>  

<span data-ttu-id="d8516-486">Vous pouvez développer ou réduire des sections de l’interface utilisateur du panneau **réseau** pour cibler les informations importantes.</span><span class="sxs-lookup"><span data-stu-id="d8516-486">You may expand or collapse sections of the **Network** panel UI to focus important information.</span></span>  

### <span data-ttu-id="d8516-487">Masquer le volet filtres</span><span class="sxs-lookup"><span data-stu-id="d8516-487">Hide the Filters pane</span></span>  

<span data-ttu-id="d8516-488">Par défaut, DevTools affiche le volet **filtres** .</span><span class="sxs-lookup"><span data-stu-id="d8516-488">By default, DevTools show the **Filters** pane.</span></span>  
<span data-ttu-id="d8516-489">Choisissez **filtre** \ ( ![ filtre ][ImageFilterIcon] \) pour le masquer.</span><span class="sxs-lookup"><span data-stu-id="d8516-489">Choose **Filter** \(![Filter][ImageFilterIcon]\) to hide it.</span></span>  

:::image type="complex" source="../media/network-network-resources-hide-filters-button.msft.png" alt-text="Bouton Masquer les filtres" lightbox="../media/network-network-resources-hide-filters-button.msft.png":::
   <span data-ttu-id="d8516-491">Bouton Masquer les filtres</span><span class="sxs-lookup"><span data-stu-id="d8516-491">The Hide Filters button</span></span>  
:::image-end:::  

### <span data-ttu-id="d8516-492">Utiliser des lignes de requête volumineuses</span><span class="sxs-lookup"><span data-stu-id="d8516-492">Use large request rows</span></span>  

<span data-ttu-id="d8516-493">Utilisez des lignes de grande taille si vous voulez plus d’espace dans votre tableau de requêtes réseau.</span><span class="sxs-lookup"><span data-stu-id="d8516-493">Use large rows when you want more whitespace in your network requests table.</span></span>  <span data-ttu-id="d8516-494">Certaines colonnes fournissent également quelques informations supplémentaires sur l’utilisation de lignes de grande taille.</span><span class="sxs-lookup"><span data-stu-id="d8516-494">Some columns also provide a little more information when using large rows.</span></span>  <span data-ttu-id="d8516-495">Par exemple, la valeur la plus en bas de la colonne **taille** correspond à la taille de requête non compressée.</span><span class="sxs-lookup"><span data-stu-id="d8516-495">For example, the bottom value of the **Size** column is the uncompressed size of a request.</span></span>  

:::image type="complex" source="../media/network-network-requests-large-request-rows.msft.png" alt-text="Exemple de longues lignes de requête dans le volet requêtes" lightbox="../media/network-network-requests-large-request-rows.msft.png":::
   <span data-ttu-id="d8516-497">Exemple de longues lignes de requête dans le volet **requêtes**</span><span class="sxs-lookup"><span data-stu-id="d8516-497">An example of large request rows in the **Requests** pane</span></span>  
:::image-end:::  

<span data-ttu-id="d8516-498">Pour activer les lignes de grande taille, activez la case à cocher **utiliser des lignes de requête volumineuses** .</span><span class="sxs-lookup"><span data-stu-id="d8516-498">To enable large rows, turn on the **Use large request rows** checkbox.</span></span>  

:::image type="complex" source="../media/network-network-requests-use-large-request-rows-on.msft.png" alt-text="Case à cocher utiliser de grandes lignes de requête" lightbox="../media/network-network-requests-use-large-request-rows-on.msft.png":::
   <span data-ttu-id="d8516-500">Case à cocher **utiliser de grandes lignes de requête**</span><span class="sxs-lookup"><span data-stu-id="d8516-500">The **Use large request rows** checkbox</span></span>  
:::image-end:::  

### <span data-ttu-id="d8516-501">Masquer le volet vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="d8516-501">Hide the Overview pane</span></span>  

<span data-ttu-id="d8516-502">Par défaut, DevTools affiche le volet **vue d’ensemble** .</span><span class="sxs-lookup"><span data-stu-id="d8516-502">By default, DevTools displays the **Overview** pane.</span></span>  <span data-ttu-id="d8516-503">Pour le masquer, désactivez la case à cocher **afficher la vue d’ensemble** .</span><span class="sxs-lookup"><span data-stu-id="d8516-503">To hide it, turn off the **Show Overview** checkbox.</span></span>  

:::image type="complex" source="../media/network-network-requests-show-overview-off.msft.png" alt-text="Case à cocher Afficher la vue d’ensemble" lightbox="../media/network-network-requests-show-overview-off.msft.png":::
   <span data-ttu-id="d8516-505">Case à cocher **afficher la vue d’ensemble**</span><span class="sxs-lookup"><span data-stu-id="d8516-505">The **Show Overview** checkbox</span></span>  
:::image-end:::  

## <span data-ttu-id="d8516-506">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="d8516-506">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCaptureScreenshotsIcon]: ../media/capture-screenshots-icon.msft.png  
[ImageClearIcon]: ../media/clear-requests-icon.msft.png  
[ImageFilterIcon]: ../media/filter-icon.msft.png  
[ImageHideIcon]: ../media/hide-overview-icon.msft.png  
[ImageLargeResourceRowsIcon]: ../media/large-resource-rows-button-icon.msft.png  
[ImageRecordOnIcon]: ../media/record-on-icon.msft.png  

<!-- links -->  

[DevtoolsProgressiveWebApps]: ../progressive-web-apps/index.md "Déboguer des applications Web progressives | Documents Microsoft"  

<!--[NetworkConditions]: /microsoft-edge/devtools-guide-chromium/network/network-conditions "Optimize Performance Under Varying Network Conditions | Microsoft Docs"  -->  

[MDNHTTPDataURIs]: https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/Data_URIs "URL de données | MDN"  

[WikiProxyServer]: https://en.wikipedia.org/wiki/Proxy_server "Serveur proxy-Wikipédia"  

> [!NOTE]
> <span data-ttu-id="d8516-510">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d8516-510">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="d8516-511">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/network/reference) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="d8516-511">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="d8516-513">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d8516-513">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
