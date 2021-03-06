---
description: Référence complète des fonctionnalités du panneau réseau Microsoft Edge DevTools.
title: Référence de l’analyse réseau
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: e8e2259e0f95499519c954e2199e191382998649
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398377"
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

# <a name="network-analysis-reference"></a><span data-ttu-id="454db-104">Référence de l’analyse réseau</span><span class="sxs-lookup"><span data-stu-id="454db-104">Network Analysis reference</span></span>  

<span data-ttu-id="454db-105">Découvrez de nouvelles façons d’analyser le chargement de votre page dans cette référence complète des fonctionnalités d’analyse réseau Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="454db-105">Discover new ways to analyze how your page loads in this comprehensive reference of Microsoft Edge DevTools network analysis features.</span></span>  

## <a name="record-network-requests"></a><span data-ttu-id="454db-106">Enregistrer des demandes réseau</span><span class="sxs-lookup"><span data-stu-id="454db-106">Record network requests</span></span>  

<span data-ttu-id="454db-107">Par défaut, DevTools enregistre toutes \*\*\*\* les demandes réseau dans l’outil Réseau, tant que DevTools est ouvert.</span><span class="sxs-lookup"><span data-stu-id="454db-107">By default, DevTools record all network requests in the **Network** tool, so long as DevTools is open.</span></span>  

:::image type="complex" source="../media/network-network-panel.msft.png" alt-text="Panneau réseau" lightbox="../media/network-network-panel.msft.png":::
   <span data-ttu-id="454db-109">Outil **Réseau**</span><span class="sxs-lookup"><span data-stu-id="454db-109">The **Network** tool</span></span>  
:::image-end:::  

### <a name="stop-recording-network-requests"></a><span data-ttu-id="454db-110">Arrêter l’enregistrement des demandes réseau</span><span class="sxs-lookup"><span data-stu-id="454db-110">Stop recording network requests</span></span>  

<span data-ttu-id="454db-111">Pour arrêter l’enregistrement des demandes, complétez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="454db-111">To stop recording requests, complete the following steps.</span></span>  

1.  <span data-ttu-id="454db-112">Dans **l’outil Réseau,** **sélectionnez Arrêter l’enregistrement du journal réseau** \( ![ Arrêter l’enregistrement du journal ][ImageRecordOnIcon] réseau \).</span><span class="sxs-lookup"><span data-stu-id="454db-112">On the **Network** tool, choose **Stop recording network log** \(![Stop recording network log][ImageRecordOnIcon]\).</span></span>  <span data-ttu-id="454db-113">Il devient gris pour indiquer que DevTools n’enregistre plus les demandes.</span><span class="sxs-lookup"><span data-stu-id="454db-113">It turns grey to indicate that DevTools is no longer recording requests.</span></span>  
1.  <span data-ttu-id="454db-114">Sélectionnez `Control` + `E` \(Windows, Linux\) ou `Command` + `E` \(macOS\) \*\*\*\* lorsque l’outil Réseau est en cours de mise au point.</span><span class="sxs-lookup"><span data-stu-id="454db-114">Select `Control`+`E` \(Windows, Linux\) or `Command`+`E` \(macOS\) while the **Network** tool is in focus.</span></span>  

### <a name="clear-requests"></a><span data-ttu-id="454db-115">Effacer les demandes</span><span class="sxs-lookup"><span data-stu-id="454db-115">Clear requests</span></span>  

<span data-ttu-id="454db-116">Sélectionnez **Effacer** \( ![ Effacer \) sur l’outil Réseau pour effacer toutes les demandes de ][ImageClearIcon] la table Demandes. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="454db-116">Choose **Clear** \(![Clear][ImageClearIcon]\) on the **Network** tool to clear all requests from the Requests table.</span></span>  

:::image type="complex" source="../media/network-network-clear-button.msft.png" alt-text="Bouton Effacer" lightbox="../media/network-network-clear-button.msft.png":::
   <span data-ttu-id="454db-118">Bouton \*\*\*\* Effacer</span><span class="sxs-lookup"><span data-stu-id="454db-118">The **Clear** button</span></span>  
:::image-end:::  

### <a name="save-requests-across-page-loads"></a><span data-ttu-id="454db-119">Enregistrer des demandes sur les chargements de page</span><span class="sxs-lookup"><span data-stu-id="454db-119">Save requests across page loads</span></span>  

<span data-ttu-id="454db-120">Pour enregistrer les demandes sur les chargements de page, sur l’outil **Réseau,** activer la case à cocher Conserver **le journal.**</span><span class="sxs-lookup"><span data-stu-id="454db-120">To save requests across page loads, on the **Network** tool, turn on the **Preserve log** checkbox.</span></span>  <span data-ttu-id="454db-121">DevTools enregistre toutes les demandes jusqu’à ce que vous **désactiviez conserver le journal.**</span><span class="sxs-lookup"><span data-stu-id="454db-121">DevTools saves all requests until you disable **Preserve log**.</span></span>  

:::image type="complex" source="../media/network-network-preserve-log.msft.png" alt-text="Case à cocher Conserver le journal" lightbox="../media/network-network-preserve-log.msft.png":::
   <span data-ttu-id="454db-123">Case **à cocher** Conserver le journal</span><span class="sxs-lookup"><span data-stu-id="454db-123">The **Preserve Log** checkbox</span></span>  
:::image-end:::  

### <a name="capture-screenshots-during-page-load"></a><span data-ttu-id="454db-124">Capture d’écran pendant le chargement de la page</span><span class="sxs-lookup"><span data-stu-id="454db-124">Capture screenshots during page load</span></span>  

<span data-ttu-id="454db-125">Capturez des captures d’écran pour analyser ce qui s’affiche pour les utilisateurs en attendant le chargement de votre page.</span><span class="sxs-lookup"><span data-stu-id="454db-125">Capture screenshots to analyze what displays for users while waiting for your page to load.</span></span>  

<span data-ttu-id="454db-126">Pour activer les captures d’écran, \*\*\*\* **sélectionnez Paramètres**réseau et, dans l’outil Réseau, activez la case à cocher Capturer les **captures d’écran.**</span><span class="sxs-lookup"><span data-stu-id="454db-126">To enable screenshots, choose **Network settings**, and on the **Network** tool, turn on the **Capture screenshots** checkbox.</span></span>  

<span data-ttu-id="454db-127">Actualisez la page lorsque **l’outil** Réseau est en cours de mise en place pour capturer des captures d’écran.</span><span class="sxs-lookup"><span data-stu-id="454db-127">Refresh the page while the **Network** tool is in focus to capture screenshots.</span></span>  

<span data-ttu-id="454db-128">Après avoir capturé une capture d’écran, vous interagissez avec elle des manières suivantes.</span><span class="sxs-lookup"><span data-stu-id="454db-128">After capturing a screenshot, you interact with it in the following ways.</span></span>  

*   <span data-ttu-id="454db-129">Pointez sur une capture d’écran pour afficher le point auquel cette capture d’écran a été capturée.</span><span class="sxs-lookup"><span data-stu-id="454db-129">Hover on a screenshot to display the point at which that screenshot was captured.</span></span>  <span data-ttu-id="454db-130">Une ligne jaune s’affiche dans le **volet** Vue d’ensemble.</span><span class="sxs-lookup"><span data-stu-id="454db-130">A yellow line is displayed on the **Overview** pane.</span></span>  
*   <span data-ttu-id="454db-131">Choisissez la miniature d’un écran pour filtrer les demandes qui se sont produites après la capture d’écran.</span><span class="sxs-lookup"><span data-stu-id="454db-131">Choose the thumbnail of a screen to filter out any requests that occurred after the screenshot was captured.</span></span>  
*   <span data-ttu-id="454db-132">Double-cliquez sur une miniature pour la zoomer.</span><span class="sxs-lookup"><span data-stu-id="454db-132">Double-click a thumbnail to zoom into it.</span></span>  

:::image type="complex" source="../media/network-network-screenshot-hover.msft.png" alt-text="Pointer sur une capture d’écran" lightbox="../media/network-network-screenshot-hover.msft.png":::
   <span data-ttu-id="454db-134">Pointer sur une capture d’écran</span><span class="sxs-lookup"><span data-stu-id="454db-134">Hover on a screenshot</span></span>  
:::image-end:::  

<!--  ### Replay XHR request  -->

<!--  To replay an XHR request, hover on the request in the Requests table, open the contextual menu \(right-click\), and choose **Replay XHR**.  -->

<!--  
:::image type="complex" source="../media/network-replay-xhr.msft.png" alt-text="Choose Replay XHR" lightbox="../media/network-replay-xhr.msft.png":::
   Choose Replay XHR  
:::image-end:::  
-->  

## <a name="change-loading-behavior"></a><span data-ttu-id="454db-135">Modifier le comportement de chargement</span><span class="sxs-lookup"><span data-stu-id="454db-135">Change loading behavior</span></span>  

### <a name="emulate-a-first-time-visitor-by-disabling-the-browser-cache"></a><span data-ttu-id="454db-136">Émuler un premier visiteur en désactivant le cache du navigateur</span><span class="sxs-lookup"><span data-stu-id="454db-136">Emulate a first-time visitor by disabling the browser cache</span></span>  

<span data-ttu-id="454db-137">Pour émuler la façon dont un utilisateur se retrouve pour la première fois sur votre site, cochez la case Désactiver le **cache.**</span><span class="sxs-lookup"><span data-stu-id="454db-137">To emulate how a first-time user experiences your site, turn on the **Disable cache** checkbox.</span></span>  <span data-ttu-id="454db-138">DevTools désactive le cache du navigateur.</span><span class="sxs-lookup"><span data-stu-id="454db-138">DevTools disables the browser cache.</span></span>  <span data-ttu-id="454db-139">Cette fonctionnalité émule plus précisément l’expérience d’un premier utilisateur, car les demandes sont reçues à partir du cache du navigateur lors de visites répétées.</span><span class="sxs-lookup"><span data-stu-id="454db-139">This feature more accurately emulates a first-time user's experience, because requests are served from the browser cache on repeat visits.</span></span>  

:::image type="complex" source="../media/network-network-disable-cache-checkbox.msft.png" alt-text="Case à cocher Désactiver le cache" lightbox="../media/network-network-disable-cache-checkbox.msft.png":::
   <span data-ttu-id="454db-141">Case **à cocher** Désactiver le cache</span><span class="sxs-lookup"><span data-stu-id="454db-141">The **Disable Cache** checkbox</span></span>  
:::image-end:::  

#### <a name="disable-the-browser-cache-from-the-network-conditions-drawer"></a><span data-ttu-id="454db-142">Désactiver le cache du navigateur à partir du caisse des conditions réseau</span><span class="sxs-lookup"><span data-stu-id="454db-142">Disable the browser cache from the Network Conditions drawer</span></span>  

<span data-ttu-id="454db-143">Si vous souhaitez désactiver le cache tout en travaillant dans d’autres panneaux DevTools, utilisez le panneau Conditions réseau.</span><span class="sxs-lookup"><span data-stu-id="454db-143">If you want to disable the cache while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="454db-144">Ouvrez le **caisse des conditions réseau.**</span><span class="sxs-lookup"><span data-stu-id="454db-144">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="454db-145">Activer \(ou désactiver\) la case à cocher Désactiver le **cache.**</span><span class="sxs-lookup"><span data-stu-id="454db-145">Turn on \(or off\) the **Disable cache** checkbox.</span></span>  

<!--todo: add network condition section when available -->  

### <a name="manually-clear-the-browser-cache"></a><span data-ttu-id="454db-146">Effacer manuellement le cache du navigateur</span><span class="sxs-lookup"><span data-stu-id="454db-146">Manually clear the browser cache</span></span>  

<span data-ttu-id="454db-147">Pour effacer manuellement le cache du navigateur à tout moment, ouvrez le menu contextuel \(clic droit\) n’importe où dans la table Demandes et choisissez Effacer le **cache du navigateur.**</span><span class="sxs-lookup"><span data-stu-id="454db-147">To manually clear the browser cache at any time, open the contextual menu \(right-click\) anywhere in the Requests table and choose **Clear Browser Cache**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cache.msft.png" alt-text="Choisir Effacer le cache du navigateur" lightbox="../media/network-network-clear-browser-cache.msft.png":::
   <span data-ttu-id="454db-149">Choisir **Effacer le cache du navigateur**</span><span class="sxs-lookup"><span data-stu-id="454db-149">Choose **Clear Browser Cache**</span></span>  
:::image-end:::  

### <a name="emulate-offline"></a><span data-ttu-id="454db-150">Émuler hors connexion</span><span class="sxs-lookup"><span data-stu-id="454db-150">Emulate offline</span></span>  

<span data-ttu-id="454db-151">Une nouvelle classe d’applications web, nommée [Progressive Web Apps,][DevtoolsProgressiveWebApps]fonctionne en mode hors connexion à l’aide des travailleurs **du service.**</span><span class="sxs-lookup"><span data-stu-id="454db-151">A new class of web apps, named [Progressive Web Apps][DevtoolsProgressiveWebApps], functions offline with the help of **service workers**.</span></span>  <span data-ttu-id="454db-152">Il peut s’avérer utile de simuler rapidement un appareil sans connexion de données lorsque vous construisez ce type d’application.</span><span class="sxs-lookup"><span data-stu-id="454db-152">You may find it useful to quickly simulate a device that has no data connection when you are building this type of app.</span></span>  

<!--[ServiceWorkers]: /web/fundamentals/getting-started/primers/service-workers  -->

<span data-ttu-id="454db-153">Choisissez le menu déroulant **En** ligne, recherchez sous **Presets**et choisissez **Hors** connexion pour simuler une expérience réseau hors connexion.</span><span class="sxs-lookup"><span data-stu-id="454db-153">Choose the **Online** dropdown menu, search under **Presets**, and choose **Offline** to simulate an offline network experience.</span></span>  

:::image type="complex" source="../media/network-network-offline-dropdown.msft.png" alt-text="Menu déroulant Hors connexion" lightbox="../media/network-network-offline-dropdown.msft.png":::
   <span data-ttu-id="454db-155">Menu **déroulant Hors** connexion</span><span class="sxs-lookup"><span data-stu-id="454db-155">The **Offline** dropdown menu</span></span>  
:::image-end:::  

### <a name="emulate-slow-network-connections"></a><span data-ttu-id="454db-156">Émuler les connexions réseau lentes</span><span class="sxs-lookup"><span data-stu-id="454db-156">Emulate slow network connections</span></span>  

<span data-ttu-id="454db-157">Émulez les 3G, les vitesses 3G rapides et d’autres vitesses de connexion à partir du menu déroulant **En** ligne.</span><span class="sxs-lookup"><span data-stu-id="454db-157">Emulate Slow 3G, Fast 3G, and other connection speeds from the **Online** dropdown menu.</span></span>  

:::image type="complex" source="../media/network-network-throttling-menu.msft.png" alt-text="Menu déroulant Limitation" lightbox="../media/network-network-throttling-menu.msft.png":::
   <span data-ttu-id="454db-159">Menu **déroulant Limitation**</span><span class="sxs-lookup"><span data-stu-id="454db-159">The **Throttling** dropdown menu</span></span>  
:::image-end:::  

<span data-ttu-id="454db-160">Vous pouvez choisir parmi différents prérets, tels que Slow 3G ou Fast 3G.</span><span class="sxs-lookup"><span data-stu-id="454db-160">You may choose from different presets, such as Slow 3G or Fast 3G.</span></span>  <span data-ttu-id="454db-161">Pour ajouter vos propres prérets personnalisés, ouvrez le menu Limitation, puis choisissez **Ajouter**  >  **personnalisé.**</span><span class="sxs-lookup"><span data-stu-id="454db-161">To add your own custom presets, open the Throttling menu, and choose **Custom** > **Add**.</span></span>  

<span data-ttu-id="454db-162">DevTools affiche une icône d’avertissement à côté de l’outil Réseau pour vous rappeler que la limitation est activée. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="454db-162">DevTools displays a warning icon next to the **Network** tool to remind you that throttling is enabled.</span></span>  

#### <a name="emulate-slow-network-connections-from-the-network-conditions-drawer"></a><span data-ttu-id="454db-163">Émuler les connexions réseau lentes à partir du caisse des conditions réseau</span><span class="sxs-lookup"><span data-stu-id="454db-163">Emulate slow network connections from the Network Conditions drawer</span></span>  

<span data-ttu-id="454db-164">Si vous souhaitez limiter la connexion réseau tout en travaillant dans d’autres panneaux DevTools, utilisez le panneau Conditions réseau.</span><span class="sxs-lookup"><span data-stu-id="454db-164">If you want to throttle the network connection while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="454db-165">Ouvrez le **caisse des conditions réseau.**</span><span class="sxs-lookup"><span data-stu-id="454db-165">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="454db-166">Choisissez votre vitesse de connexion dans le menu **Limitation.**</span><span class="sxs-lookup"><span data-stu-id="454db-166">Choose your connection speed from the **Throttling** menu.</span></span>  

<!--todo: add network condition section when available -->  

### <a name="manually-clear-browser-cookies"></a><span data-ttu-id="454db-167">Effacer manuellement les cookies du navigateur</span><span class="sxs-lookup"><span data-stu-id="454db-167">Manually clear browser cookies</span></span>  

<span data-ttu-id="454db-168">Pour effacer manuellement les cookies du navigateur à tout moment, pointez n’importe où dans la table Demandes, ouvrez le menu contextuel \(clic droit\), puis choisissez Effacer les **cookies du navigateur.**</span><span class="sxs-lookup"><span data-stu-id="454db-168">To manually clear browser cookies at any time, hover anywhere in the Requests table, open the contextual menu \(right-click\), and choose **Clear Browser Cookies**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cookies.msft.png" alt-text="Choose Clear Browser Cookies" lightbox="../media/network-network-clear-browser-cookies.msft.png":::
   <span data-ttu-id="454db-170">Choose **Clear Browser Cookies**</span><span class="sxs-lookup"><span data-stu-id="454db-170">Choose **Clear Browser Cookies**</span></span>  
:::image-end:::  

### <a name="override-the-user-agent"></a><span data-ttu-id="454db-171">Remplacer l’agent utilisateur</span><span class="sxs-lookup"><span data-stu-id="454db-171">Override the user agent</span></span>  

<span data-ttu-id="454db-172">Pour remplacer manuellement l’agent utilisateur, utilisez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="454db-172">To manually override the user agent, use the following steps.</span></span>  

1.  <span data-ttu-id="454db-173">Ouvrez le **caisse des conditions réseau.**</span><span class="sxs-lookup"><span data-stu-id="454db-173">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="454db-174">Désactiver la case **à cocher Sélectionner** automatiquement.</span><span class="sxs-lookup"><span data-stu-id="454db-174">Turn off the **Select automatically** checkbox.</span></span>  
1.  <span data-ttu-id="454db-175">Choisissez une option d’agent utilisateur dans le menu ou entrez une option personnalisée dans la zone de texte.</span><span class="sxs-lookup"><span data-stu-id="454db-175">Choose a user agent option from the menu, or enter a custom one in the text box.</span></span>  

<!--todo: add network condition section when available -->  

## <a name="filter-requests"></a><span data-ttu-id="454db-176">Filtrer les demandes</span><span class="sxs-lookup"><span data-stu-id="454db-176">Filter requests</span></span>  

### <a name="filter-requests-by-properties"></a><span data-ttu-id="454db-177">Filtrer les demandes par propriétés</span><span class="sxs-lookup"><span data-stu-id="454db-177">Filter requests by properties</span></span>  

<span data-ttu-id="454db-178">Utilisez la **zone de** texte Filtrer pour filtrer les demandes par propriétés, telles que le domaine ou la taille de la demande.</span><span class="sxs-lookup"><span data-stu-id="454db-178">Use the **Filter** text box to filter requests by properties, such as the domain or size of the request.</span></span>  

<span data-ttu-id="454db-179">Si la zone de texte n’est pas affichée, le volet **Filtres** est probablement masqué.</span><span class="sxs-lookup"><span data-stu-id="454db-179">If the text box is not displayed, the **Filters** pane is probably hidden.</span></span>  
<span data-ttu-id="454db-180">Pour plus d’informations, [accédez à Masquer le volet Filtres.](#hide-the-filters-pane)</span><span class="sxs-lookup"><span data-stu-id="454db-180">For more information, navigate to [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

:::image type="complex" source="../media/network-network-filters-textbox.msft.png" alt-text="Zone de texte Filtre" lightbox="../media/network-network-filters-textbox.msft.png":::
   <span data-ttu-id="454db-182">Zone **de texte** Filtre</span><span class="sxs-lookup"><span data-stu-id="454db-182">The **Filter** text box</span></span>  
:::image-end:::  

<span data-ttu-id="454db-183">Vous pouvez utiliser plusieurs propriétés simultanément en séparant chaque propriété par un espace.</span><span class="sxs-lookup"><span data-stu-id="454db-183">You may use multiple properties simultaneously by separating each property with a space.</span></span>  <span data-ttu-id="454db-184">Par exemple, affiche tous les PNG dont la taille `mime-type:image/png larger-than:1K` est supérieure à 1 kilo-octet.</span><span class="sxs-lookup"><span data-stu-id="454db-184">For example, `mime-type:image/png larger-than:1K` displays all PNGs that are larger than 1 kilobyte.</span></span>  <span data-ttu-id="454db-185">Les filtres multi-propriétés sont équivalents aux `AND` opérations.</span><span class="sxs-lookup"><span data-stu-id="454db-185">The multi-property filters are equivalent to `AND` operations.</span></span>  `OR` <span data-ttu-id="454db-186">ne sont actuellement pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="454db-186">operations are currently not supported.</span></span>  

<span data-ttu-id="454db-187">Liste complète des propriétés prise en charge.</span><span class="sxs-lookup"><span data-stu-id="454db-187">The complete list of supported properties.</span></span>  

| <span data-ttu-id="454db-188">Propriété</span><span class="sxs-lookup"><span data-stu-id="454db-188">Property</span></span> | <span data-ttu-id="454db-189">Détails</span><span class="sxs-lookup"><span data-stu-id="454db-189">Details</span></span> |  
|:--- | :--- |  
| `domain` | <span data-ttu-id="454db-190">Afficher uniquement les ressources du domaine spécifié.</span><span class="sxs-lookup"><span data-stu-id="454db-190">Only display resources from the specified domain.</span></span>  <span data-ttu-id="454db-191">Vous pouvez utiliser un caractère générique \( `*` \) pour inclure plusieurs domaines.</span><span class="sxs-lookup"><span data-stu-id="454db-191">You may use a wildcard character \(`*`\) to include multiple domains.</span></span>  <span data-ttu-id="454db-192">Par exemple, `*.com` affiche les ressources de tous les noms de domaine se terminant par `.com` .</span><span class="sxs-lookup"><span data-stu-id="454db-192">For example, `*.com` displays resources from all domain names ending in `.com`.</span></span>  <span data-ttu-id="454db-193">DevTools remplit le menu déroulant de la mise à jour de la mise à jour automatique avec tous les domaines trouvés.</span><span class="sxs-lookup"><span data-stu-id="454db-193">DevTools populate the autocomplete dropdown menu with all of the domains that are found.</span></span> |  
| `has-response-header` | <span data-ttu-id="454db-194">Affiche les ressources qui contiennent l’en-tête de réponse HTTP spécifié.</span><span class="sxs-lookup"><span data-stu-id="454db-194">Displays the resources that contain the specified HTTP response header.</span></span>  <span data-ttu-id="454db-195">DevTools remplit la zone de mise à jour de la mise à jour automatique avec tous les en-têtes de réponse trouvés.</span><span class="sxs-lookup"><span data-stu-id="454db-195">DevTools populate the autocomplete dropdown with all of the response headers that are found.</span></span> |  
| `is` | <span data-ttu-id="454db-196">À `is:running` utiliser pour rechercher des `WebSocket` ressources.</span><span class="sxs-lookup"><span data-stu-id="454db-196">Use `is:running` to find `WebSocket` resources.</span></span> |  
| `larger-than` | <span data-ttu-id="454db-197">Affiche les ressources dont la taille est supérieure à la taille spécifiée, en octets.</span><span class="sxs-lookup"><span data-stu-id="454db-197">Displays resources that are larger than the specified size, in bytes.</span></span>  <span data-ttu-id="454db-198">Définir une valeur de `1000` . `1k`</span><span class="sxs-lookup"><span data-stu-id="454db-198">Setting a value of `1000` is equivalent to setting a value of `1k`.</span></span> |  
| `method` | <span data-ttu-id="454db-199">Affiche les ressources qui ont été récupérées sur un type de méthode HTTP spécifié.</span><span class="sxs-lookup"><span data-stu-id="454db-199">Displays resources that were retrieved over a specified HTTP method type.</span></span>  <span data-ttu-id="454db-200">DevTools remplit la zone de détail avec toutes les méthodes HTTP qui sont trouvées.</span><span class="sxs-lookup"><span data-stu-id="454db-200">DevTools populate the dropdown with all of the HTTP methods  that are found.</span></span> |  
| `mime-type` | <span data-ttu-id="454db-201">Affiche les ressources d’un type MIME spécifié.</span><span class="sxs-lookup"><span data-stu-id="454db-201">Displays resources of a specified MIME type.</span></span>  <span data-ttu-id="454db-202">DevTools remplit la zone de détail avec tous les types MIME trouvés.</span><span class="sxs-lookup"><span data-stu-id="454db-202">DevTools populate the dropdown with all MIME types  that are found.</span></span> |  
| `mixed-content` | <span data-ttu-id="454db-203">Afficher toutes les ressources de contenu mixte \( \) ou uniquement ceux qui sont `mixed-content:all` actuellement affichés \( `mixed-content:displayed` \).</span><span class="sxs-lookup"><span data-stu-id="454db-203">Show all mixed content resources \(`mixed-content:all`\) or just the ones that are currently displayed \(`mixed-content:displayed`\).</span></span> |  
| `scheme` | <span data-ttu-id="454db-204">Affiche les ressources récupérées sur http \( \) ou `scheme:http` HTTPS \( `scheme:https` \) protégées.</span><span class="sxs-lookup"><span data-stu-id="454db-204">Displays resources retrieved over unprotected HTTP \(`scheme:http`\) or protected HTTPS \(`scheme:https`\).</span></span> |  
| `set-cookie-domain` | <span data-ttu-id="454db-205">Affiche les ressources qui ont un `Set-Cookie` en-tête avec un `Domain` attribut qui correspond à la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="454db-205">Displays resources that have a `Set-Cookie` header with a `Domain` attribute that matches the specified value.</span></span>  <span data-ttu-id="454db-206">DevTools remplit la mise à jour automatique avec tous les domaines de cookie trouvés.</span><span class="sxs-lookup"><span data-stu-id="454db-206">DevTools populate the autocomplete with all of the cookie domains that are found.</span></span> |  
| `set-cookie-name` | <span data-ttu-id="454db-207">Affiche les ressources qui ont un `Set-Cookie` en-tête avec un nom qui correspond à la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="454db-207">Displays resources that have a `Set-Cookie` header with a name that matches the specified value.</span></span>  <span data-ttu-id="454db-208">DevTools remplit la mise à jour automatique avec tous les noms de cookies trouvés.</span><span class="sxs-lookup"><span data-stu-id="454db-208">DevTools populate the autocomplete with all of the cookie names that are found.</span></span> |  
| `set-cookie-value` | <span data-ttu-id="454db-209">Affiche les ressources qui ont un `Set-Cookie` en-tête avec une valeur qui correspond à la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="454db-209">Displays resources that have a `Set-Cookie` header with a value that matches the specified value.</span></span>  <span data-ttu-id="454db-210">DevTools remplit la mise à jour automatique avec toutes les valeurs de cookie trouvées.</span><span class="sxs-lookup"><span data-stu-id="454db-210">DevTools populate the autocomplete with all of the cookie values that are found.</span></span> |  
| `status-code` | <span data-ttu-id="454db-211">Affiche les ressources qui correspondent au code d’état HTTP spécifique.</span><span class="sxs-lookup"><span data-stu-id="454db-211">Displays resources that match the specific HTTP status code.</span></span>  <span data-ttu-id="454db-212">DevTools remplit le menu déroulant de lacomplet automatique avec tous les codes d’état trouvés.</span><span class="sxs-lookup"><span data-stu-id="454db-212">DevTools populates the autocomplete dropdown menu with all of the status codes that are found.</span></span> |  

### <a name="filter-requests-by-type"></a><span data-ttu-id="454db-213">Filtrer les demandes par type</span><span class="sxs-lookup"><span data-stu-id="454db-213">Filter requests by type</span></span>  

<span data-ttu-id="454db-214">Pour filtrer les demandes par type de requête, choisissez l’un des boutons suivants sur **l’outil** Réseau.</span><span class="sxs-lookup"><span data-stu-id="454db-214">To filter requests by request type, choose the one of the following buttons on the **Network** tool.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="454db-215">XHR</span><span class="sxs-lookup"><span data-stu-id="454db-215">XHR</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="454db-216">JS</span><span class="sxs-lookup"><span data-stu-id="454db-216">JS</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="454db-217">CSS</span><span class="sxs-lookup"><span data-stu-id="454db-217">CSS</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="454db-218">Img</span><span class="sxs-lookup"><span data-stu-id="454db-218">Img</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="454db-219">Media</span><span class="sxs-lookup"><span data-stu-id="454db-219">Media</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="454db-220">Police</span><span class="sxs-lookup"><span data-stu-id="454db-220">Font</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="454db-221">Doc</span><span class="sxs-lookup"><span data-stu-id="454db-221">Doc</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="454db-222">WS</span><span class="sxs-lookup"><span data-stu-id="454db-222">WS</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="454db-223">WebSocket.</span><span class="sxs-lookup"><span data-stu-id="454db-223">WebSocket.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="454db-224">Manifeste</span><span class="sxs-lookup"><span data-stu-id="454db-224">Manifest</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="454db-225">Other</span><span class="sxs-lookup"><span data-stu-id="454db-225">Other</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="454db-226">Tout autre type non répertorié.</span><span class="sxs-lookup"><span data-stu-id="454db-226">Any other type not listed.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="454db-227">Si les boutons ne s’affichent pas, le volet **Filtres** peut être masqué.</span><span class="sxs-lookup"><span data-stu-id="454db-227">If the buttons do not display, the **Filters** pane may be hidden.</span></span>  
<span data-ttu-id="454db-228">Pour plus d’informations, [accédez à Masquer le volet Filtres.](#hide-the-filters-pane)</span><span class="sxs-lookup"><span data-stu-id="454db-228">For more information, navigate to [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

<span data-ttu-id="454db-229">Pour activer plusieurs filtres de type simultanément, maintenez la main sur `Control` \(Windows, Linux\) ou `Command` \(macOS\), puis choisissez.</span><span class="sxs-lookup"><span data-stu-id="454db-229">To enable multiple type filters simultaneously, hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and then choose.</span></span>  

:::image type="complex" source="../media/network-network-type-filters.msft.png" alt-text="Utiliser les filtres type pour afficher les ressources JS, CSS et Document" lightbox="../media/network-network-type-filters.msft.png":::
   <span data-ttu-id="454db-231">Utiliser les filtres type pour afficher les ressources JS, CSS et Document</span><span class="sxs-lookup"><span data-stu-id="454db-231">Use the Type filters to display JS, CSS, and Document resources</span></span>  
:::image-end:::  

### <a name="filter-requests-by-time"></a><span data-ttu-id="454db-232">Filtrer les demandes par heure</span><span class="sxs-lookup"><span data-stu-id="454db-232">Filter requests by time</span></span>  

<span data-ttu-id="454db-233">Choisissez et faites glisser \*\*\*\* vers la gauche ou la droite dans le volet Vue d’ensemble pour afficher uniquement les demandes qui étaient actives pendant cette période.</span><span class="sxs-lookup"><span data-stu-id="454db-233">Choose and drag left or right on the **Overview** pane to only display requests that were active during that time frame.</span></span>  <span data-ttu-id="454db-234">Le filtre est inclus.</span><span class="sxs-lookup"><span data-stu-id="454db-234">The filter is inclusive.</span></span>  <span data-ttu-id="454db-235">Toute demande qui était active pendant l’heure mise en surbrillant s’affiche.</span><span class="sxs-lookup"><span data-stu-id="454db-235">Any request that was active during the highlighted time is shown.</span></span>  

:::image type="complex" source="../media/network-network-overview-filter.msft.png" alt-text="Filtrer toutes les demandes inactives d’environ 300 ms" lightbox="../media/network-network-overview-filter.msft.png":::
   <span data-ttu-id="454db-237">Filtrer toutes les demandes inactives d’environ 300 ms</span><span class="sxs-lookup"><span data-stu-id="454db-237">Filter out any requests that were inactive around 300 ms</span></span>  
:::image-end:::  

### <a name="hide-data-urls"></a><span data-ttu-id="454db-238">Masquer les URL de données</span><span class="sxs-lookup"><span data-stu-id="454db-238">Hide data URLs</span></span>  

<span data-ttu-id="454db-239">[Les URL de données sont][MDNHTTPDataURIs] de petits fichiers incorporés dans d’autres documents.</span><span class="sxs-lookup"><span data-stu-id="454db-239">[Data URLs][MDNHTTPDataURIs] are small files embedded into other documents.</span></span>  <span data-ttu-id="454db-240">Toute demande qui s’affiche dans la table Demandes qui commence par `data:` est une URL de données.</span><span class="sxs-lookup"><span data-stu-id="454db-240">Any request that displays in the Requests table that starts with `data:` is a data URL.</span></span>  

<span data-ttu-id="454db-241">Pour masquer les demandes, cochez la case Masquer **les URL de** données.</span><span class="sxs-lookup"><span data-stu-id="454db-241">To hide the requests, turn off the **Hide data URLs** checkbox.</span></span>  

:::image type="complex" source="../media/network-network-hide-data-urls.msft.png" alt-text="Case à cocher Masquer les URL de données" lightbox="../media/network-network-hide-data-urls.msft.png":::
   <span data-ttu-id="454db-243">Case **à cocher Masquer les URL de** données</span><span class="sxs-lookup"><span data-stu-id="454db-243">The **Hide Data URLs** checkbox</span></span>  
:::image-end:::  

## <a name="sort-requests"></a><span data-ttu-id="454db-244">Trier les demandes</span><span class="sxs-lookup"><span data-stu-id="454db-244">Sort requests</span></span>  

<span data-ttu-id="454db-245">Par défaut, les demandes de la table Requests sont triées par heure d’initiation, mais vous pouvez trier le tableau à l’aide d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="454db-245">By default, the requests in the Requests table are sorted by initiation time, but you may sort the table using other criteria.</span></span>  

### <a name="sort-by-column"></a><span data-ttu-id="454db-246">Trier par colonne</span><span class="sxs-lookup"><span data-stu-id="454db-246">Sort by column</span></span>  

<span data-ttu-id="454db-247">Choisissez l’en-tête d’une colonne dans les demandes de tri des demandes par cette colonne.</span><span class="sxs-lookup"><span data-stu-id="454db-247">Choose the header of any column in the Requests to sort requests by that column.</span></span>  

### <a name="sort-by-activity-phase"></a><span data-ttu-id="454db-248">Trier par phase d’activité</span><span class="sxs-lookup"><span data-stu-id="454db-248">Sort by activity phase</span></span>  

<span data-ttu-id="454db-249">Pour modifier la façon dont la cascade trie les demandes, pointez sur l’en-tête de la table Requests, ouvrez le menu contextuel \(clic droit\), pointez sur Cascade **et**choisissez l’une des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="454db-249">To change how the Waterfall sorts requests, hover on the header of the Requests table, open the contextual menu \(right-click\), hover on **Waterfall**, and choose one of the following options.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="454db-250">Heure de début</span><span class="sxs-lookup"><span data-stu-id="454db-250">Start Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="454db-251">La première requête qui a été lancée se trouve en haut.</span><span class="sxs-lookup"><span data-stu-id="454db-251">The first request that was initiated is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="454db-252">Temps de réponse</span><span class="sxs-lookup"><span data-stu-id="454db-252">Response Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="454db-253">La première requête qui a démarré le téléchargement se trouve en haut.</span><span class="sxs-lookup"><span data-stu-id="454db-253">The first request that started downloading is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="454db-254">Heure de fin</span><span class="sxs-lookup"><span data-stu-id="454db-254">End Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="454db-255">La première requête terminée se trouve en haut.</span><span class="sxs-lookup"><span data-stu-id="454db-255">The first request that finished is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="454db-256">Durée totale</span><span class="sxs-lookup"><span data-stu-id="454db-256">Total Duration</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="454db-257">La demande avec les paramètres de connexion et la demande ou la réponse les plus courts se trouve en haut.</span><span class="sxs-lookup"><span data-stu-id="454db-257">The request with the shortest connection settings and request or response is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="454db-258">Latence</span><span class="sxs-lookup"><span data-stu-id="454db-258">Latency</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="454db-259">La demande qui a attendu le plus court moment pour une réponse se trouve en haut.</span><span class="sxs-lookup"><span data-stu-id="454db-259">The request that waited the shortest time for a response is at the top.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="454db-260">Ces descriptions supposent que chaque option respective est classée de la plus courte à la plus longue.</span><span class="sxs-lookup"><span data-stu-id="454db-260">These descriptions assume that each respective option is ranked from shortest to longest.</span></span>  <span data-ttu-id="454db-261">Choisissez l’en-tête de la colonne **Cascade** pour inverser l’ordre.</span><span class="sxs-lookup"><span data-stu-id="454db-261">Choose the header of the **Waterfall** column to reverse the order.</span></span>  

:::image type="complex" source="../media/network-network-waterfall-total-duration.msft.png" alt-text="Trier la cascade par durée totale" lightbox="../media/network-network-waterfall-total-duration.msft.png":::
   <span data-ttu-id="454db-263">Trier la cascade par durée totale \(La partie la plus claire de chaque barre est le temps passé en attente et la partie la plus sombre est le temps consacré au téléchargement d’octets\)</span><span class="sxs-lookup"><span data-stu-id="454db-263">Sort the Waterfall by total duration  \(The lighter portion of each bar is time spent waiting and the darker portion is time spent downloading bytes\)</span></span>  
:::image-end:::  

## <a name="analyze-requests"></a><span data-ttu-id="454db-264">Analyser les demandes</span><span class="sxs-lookup"><span data-stu-id="454db-264">Analyze requests</span></span>  

<span data-ttu-id="454db-265">Tant que DevTools est ouvert, il enregistre toutes les demandes dans **l’outil** Réseau.</span><span class="sxs-lookup"><span data-stu-id="454db-265">So long as DevTools are open, it logs all requests in the **Network** tool.</span></span>  
<span data-ttu-id="454db-266">Utilisez le panneau réseau pour analyser les demandes.</span><span class="sxs-lookup"><span data-stu-id="454db-266">Use the Network panel to analyze requests.</span></span>  

### <a name="display-a-log-of-requests"></a><span data-ttu-id="454db-267">Afficher un journal des demandes</span><span class="sxs-lookup"><span data-stu-id="454db-267">Display a log of requests</span></span>  

<span data-ttu-id="454db-268">Utilisez la table Requests pour afficher un journal de toutes les demandes réalisées alors que DevTools a été ouvert.</span><span class="sxs-lookup"><span data-stu-id="454db-268">Use the Requests table to display a log of all requests made while DevTools have been open.</span></span>  <span data-ttu-id="454db-269">Pour révéler plus d’informations sur chaque élément, choisissez ou pointez sur les demandes.</span><span class="sxs-lookup"><span data-stu-id="454db-269">To reveals more information about each item, choose or hover on requests.</span></span>  

:::image type="complex" source="../media/network-network-requests-table.msft.png" alt-text="Table Requests" lightbox="../media/network-network-requests-table.msft.png":::
   <span data-ttu-id="454db-271">Table Requests</span><span class="sxs-lookup"><span data-stu-id="454db-271">The Requests table</span></span>  
:::image-end:::  

<span data-ttu-id="454db-272">La table Requests affiche les colonnes suivantes par défaut.</span><span class="sxs-lookup"><span data-stu-id="454db-272">The Requests table displays the following columns by default.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="454db-273">Nom</span><span class="sxs-lookup"><span data-stu-id="454db-273">Name</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="454db-274">Nom de fichier ou identificateur de la ressource.</span><span class="sxs-lookup"><span data-stu-id="454db-274">The filename of, or an identifier for, the resource.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="454db-275">Statut</span><span class="sxs-lookup"><span data-stu-id="454db-275">Status</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="454db-276">Code d’état HTTP.</span><span class="sxs-lookup"><span data-stu-id="454db-276">The HTTP status code.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="454db-277">Type</span><span class="sxs-lookup"><span data-stu-id="454db-277">Type</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="454db-278">Type MIME de la ressource demandée.</span><span class="sxs-lookup"><span data-stu-id="454db-278">The MIME type of the requested resource.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="454db-279">Initiateur</span><span class="sxs-lookup"><span data-stu-id="454db-279">Initiator</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="454db-280">Les objets ou processus suivants lancent des demandes.</span><span class="sxs-lookup"><span data-stu-id="454db-280">The following objects or processes initiate requests.</span></span>  
      
      *   <span data-ttu-id="454db-281">**Parser**  L’en-tête HTML pour Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="454db-281">**Parser**  The HTML parser for Microsoft Edge.</span></span>  
      *   <span data-ttu-id="454db-282">**Redirection**  Une redirection HTTP.</span><span class="sxs-lookup"><span data-stu-id="454db-282">**Redirect**  An HTTP redirect.</span></span>  
      *   <span data-ttu-id="454db-283">**Script**  Fonction JavaScript.</span><span class="sxs-lookup"><span data-stu-id="454db-283">**Script**  A JavaScript function.</span></span>  
      *   <span data-ttu-id="454db-284">**Autre**  Un autre processus ou une autre action, comme la navigation vers une page à l’aide d’un lien ou la saisie d’une URL dans la barre d’adresses.</span><span class="sxs-lookup"><span data-stu-id="454db-284">**Other**  Some other process or action, such as navigating to a page using a link or entering a URL in the address bar.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="454db-285">Taille</span><span class="sxs-lookup"><span data-stu-id="454db-285">Size</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="454db-286">Taille combinée des en-têtes de réponse et corps de la réponse, tel qu’il est remis par le serveur.</span><span class="sxs-lookup"><span data-stu-id="454db-286">The combined size of the response headers plus the response body, as delivered by the server.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="454db-287">Heure</span><span class="sxs-lookup"><span data-stu-id="454db-287">Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="454db-288">Durée totale, depuis le début de la demande jusqu’à la réception de l’byte final dans la réponse.</span><span class="sxs-lookup"><span data-stu-id="454db-288">The total duration, from the start of the request to the receipt of the final byte in the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="454db-289">Cascade</span><span class="sxs-lookup"><span data-stu-id="454db-289">Waterfall</span></span>](#display-the-timing-relationship-of-requests)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="454db-290">Répartition visuelle de l’activité pour chaque demande.</span><span class="sxs-lookup"><span data-stu-id="454db-290">A visual breakdown of the activity for each request.</span></span>  
   :::column-end:::
:::row-end:::  

#### <a name="add-or-remove-columns"></a><span data-ttu-id="454db-291">Ajouter ou supprimer des colonnes</span><span class="sxs-lookup"><span data-stu-id="454db-291">Add or remove columns</span></span>  

<span data-ttu-id="454db-292">Pointez sur l’en-tête de la table Requests, ouvrez le menu contextuel \(clic droit\), puis choisissez une option pour le masquer ou l’afficher.</span><span class="sxs-lookup"><span data-stu-id="454db-292">Hover on the header of the Requests table, open the contextual menu \(right-click\), and choose an option to hide or show it.</span></span>  <span data-ttu-id="454db-293">Les options actuellement affichées ont des coches en regard de chaque élément.</span><span class="sxs-lookup"><span data-stu-id="454db-293">Currently displayed options have checkmarks next to each item.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-column.msft.png" alt-text="Ajouter une colonne à la table Requests" lightbox="../media/network-network-requests-add-column.msft.png":::
   <span data-ttu-id="454db-295">Ajouter une colonne à la table Requests</span><span class="sxs-lookup"><span data-stu-id="454db-295">Add a column to the Requests table</span></span>  
:::image-end:::  

#### <a name="add-custom-columns"></a><span data-ttu-id="454db-296">Ajouter des colonnes personnalisées</span><span class="sxs-lookup"><span data-stu-id="454db-296">Add custom columns</span></span>  

<span data-ttu-id="454db-297">Pour ajouter une colonne personnalisée à la table Requests, pointez sur l’en-tête de la \*\*\*\* table Requests, ouvrez le menu contextuel \(clic droit\), puis choisissez En-têtes de réponse Gérer les colonnes d’en-tête.  >  \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="454db-297">To add a custom column to the Requests table, hover on the header of the Requests table, open the contextual menu \(right-click\), and choose **Response Headers** > **Manage Header Columns**.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-custom.msft.png" alt-text="Ajouter une colonne personnalisée à la table Requests" lightbox="../media/network-network-requests-add-custom.msft.png":::
   <span data-ttu-id="454db-299">Ajouter une colonne personnalisée à la table Requests</span><span class="sxs-lookup"><span data-stu-id="454db-299">Add a custom column to the Requests table</span></span>  
:::image-end:::  

### <a name="display-the-timing-relationship-of-requests"></a><span data-ttu-id="454db-300">Afficher la relation de minutage des demandes</span><span class="sxs-lookup"><span data-stu-id="454db-300">Display the timing relationship of requests</span></span>  

<span data-ttu-id="454db-301">Utilisez la cascade pour afficher les relations de minutage des demandes.</span><span class="sxs-lookup"><span data-stu-id="454db-301">Use the Waterfall to display the timing relationships of requests.</span></span>  
<span data-ttu-id="454db-302">L’organisation par défaut de la cascade utilise l’heure de début des demandes.</span><span class="sxs-lookup"><span data-stu-id="454db-302">The default organization of the Waterfall uses the start time of the requests.</span></span>  
<span data-ttu-id="454db-303">Ainsi, les demandes qui sont plus à gauche ont commencé plus tôt que les demandes qui sont plus à droite.</span><span class="sxs-lookup"><span data-stu-id="454db-303">So, requests that are farther to the left started earlier than the requests that are farther to the right.</span></span>  

<span data-ttu-id="454db-304">Pour passer en revue les différentes façons de trier la cascade, accédez à [Trier par phase d’activité.](#sort-by-activity-phase)</span><span class="sxs-lookup"><span data-stu-id="454db-304">To review the different ways that you may sort the Waterfall, navigate to [Sort by activity phase](#sort-by-activity-phase).</span></span>  

:::image type="complex" source="../media/network-network-requests-waterfall.msft.png" alt-text="Colonne Cascade du volet Demandes" lightbox="../media/network-network-requests-waterfall.msft.png":::
   <span data-ttu-id="454db-306">Colonne Cascade du volet **Demandes**</span><span class="sxs-lookup"><span data-stu-id="454db-306">The Waterfall column of the **Requests** pane</span></span>  
:::image-end:::  

<!-- ### Analyze the frames of a WebSocket Connection  -->

<!--To review the frames of a WebSocket connection, use the following steps.  

1.  Choose the URL of the WebSocket connection, under the **Name** column of the Requests table.  
1.  Choose the **Frames** panel.  The table shows the last 100 frames.  

To refresh the table, re-choose the name of the WebSocket connection under the **Name** column of the Requests table.  -->

<!--
:::image type="complex" source="../media/network-frames.msft.png" alt-text="The Frames panel" lightbox="../media/network-frames.msft.png":::
   The **Frames** panel  
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

### <a name="display-a-preview-of-a-response-body"></a><span data-ttu-id="454db-307">Afficher un aperçu d’un corps de réponse</span><span class="sxs-lookup"><span data-stu-id="454db-307">Display a preview of a response body</span></span>  

<span data-ttu-id="454db-308">Pour afficher un aperçu d’un corps de réponse, utilisez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="454db-308">To display a preview of a response body, use the following steps.</span></span>  

1.  <span data-ttu-id="454db-309">Choisissez l’URL de la demande, sous la colonne **Nom** de la table Requests.</span><span class="sxs-lookup"><span data-stu-id="454db-309">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="454db-310">Choisissez le **panneau d’aperçu.**</span><span class="sxs-lookup"><span data-stu-id="454db-310">Choose the **Preview** panel.</span></span>  

<span data-ttu-id="454db-311">L’onglet Aperçu est principalement utile pour afficher des images.</span><span class="sxs-lookup"><span data-stu-id="454db-311">The Preview tab is mostly useful to display images.</span></span>  

:::image type="complex" source="../media/network-network-resources-preview.msft.png" alt-text="Panneau d’aperçu" lightbox="../media/network-network-resources-preview.msft.png":::
   <span data-ttu-id="454db-313">Panneau **d’aperçu**</span><span class="sxs-lookup"><span data-stu-id="454db-313">The **Preview** panel</span></span>  
:::image-end:::  

### <a name="display-a-response-body"></a><span data-ttu-id="454db-314">Afficher un corps de réponse</span><span class="sxs-lookup"><span data-stu-id="454db-314">Display a response body</span></span>  

<span data-ttu-id="454db-315">Pour afficher le corps de la réponse à une demande, utilisez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="454db-315">To display the response body to a request, use the following steps.</span></span>  

1.  <span data-ttu-id="454db-316">Choisissez l’URL de la demande, sous la colonne **Nom** de la table Requests.</span><span class="sxs-lookup"><span data-stu-id="454db-316">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="454db-317">Choisissez le **panneau de** réponse.</span><span class="sxs-lookup"><span data-stu-id="454db-317">Choose the **Response** panel.</span></span>  

:::image type="complex" source="../media/network-network-resources-response.msft.png" alt-text="Panneau de réponse" lightbox="../media/network-network-resources-response.msft.png":::
   <span data-ttu-id="454db-319">Panneau **de** réponse</span><span class="sxs-lookup"><span data-stu-id="454db-319">The **Response** panel</span></span>  
:::image-end:::  

### <a name="display-http-headers"></a><span data-ttu-id="454db-320">Afficher les en-têtes HTTP</span><span class="sxs-lookup"><span data-stu-id="454db-320">Display HTTP headers</span></span>  

<span data-ttu-id="454db-321">Pour afficher les données d’en-tête HTTP relatives à une demande, utilisez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="454db-321">To display HTTP header data about a request, use the following steps.</span></span>  

1.  <span data-ttu-id="454db-322">Choisissez l’URL de la demande, sous la colonne **Nom** de la table Requests.</span><span class="sxs-lookup"><span data-stu-id="454db-322">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="454db-323">Choisissez le **psanel d’en-têtes.**</span><span class="sxs-lookup"><span data-stu-id="454db-323">Choose the **Headers** psanel.</span></span>  

:::image type="complex" source="../media/network-resources-headers.msft.png" alt-text="Panneau En-têtes" lightbox="../media/network-resources-headers.msft.png":::
   <span data-ttu-id="454db-325">Panneau **En-têtes**</span><span class="sxs-lookup"><span data-stu-id="454db-325">The **Headers** panel</span></span>  
:::image-end:::  

#### <a name="display-http-header-source"></a><span data-ttu-id="454db-326">Afficher la source d’en-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="454db-326">Display HTTP header source</span></span>  

<span data-ttu-id="454db-327">Par défaut, le panneau **En-têtes** affiche les noms d’en-tête par ordre alphabétique.</span><span class="sxs-lookup"><span data-stu-id="454db-327">By default, the **Headers** panel shows header names alphabetically.</span></span>  <span data-ttu-id="454db-328">Pour dsiplay les noms d’en-tête HTTP dans l’ordre reçu, utilisez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="454db-328">To dsiplay the HTTP header names in the order received, use the following steps.</span></span>  

1.  <span data-ttu-id="454db-329">Ouvrez **le panneau En-têtes** pour la demande qui vous intéresse.</span><span class="sxs-lookup"><span data-stu-id="454db-329">Open the **Headers** panel for the request that interests you.</span></span>  <span data-ttu-id="454db-330">Pour plus d’informations, accédez à [Afficher les en-têtes HTTP.](#display-http-headers)</span><span class="sxs-lookup"><span data-stu-id="454db-330">For more information, navigate to [Display HTTP headers](#display-http-headers).</span></span>  
1.  <span data-ttu-id="454db-331">Choose **view source**, next to the Request **Header** or **Response Header** section.</span><span class="sxs-lookup"><span data-stu-id="454db-331">Choose **view source**, next to the **Request Header** or **Response Header** section.</span></span>  

### <a name="display-query-string-parameters"></a><span data-ttu-id="454db-332">Afficher les paramètres de chaîne de requête</span><span class="sxs-lookup"><span data-stu-id="454db-332">Display query string parameters</span></span>  

<span data-ttu-id="454db-333">Pour afficher les paramètres de chaîne de requête d’une URL dans un format lisible par l’homme, utilisez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="454db-333">To display the query string parameters of a URL in a human-readable format, use the following steps.</span></span>  

1.  <span data-ttu-id="454db-334">Ouvrez **le panneau En-têtes** pour la demande qui vous intéresse.</span><span class="sxs-lookup"><span data-stu-id="454db-334">Open the **Headers** panel for the request that interests you.</span></span>  <span data-ttu-id="454db-335">Pour plus d’informations, accédez à [Afficher les en-têtes HTTP.](#display-http-headers)</span><span class="sxs-lookup"><span data-stu-id="454db-335">For more information, navigate to [Display HTTP headers](#display-http-headers).</span></span>  
1.  <span data-ttu-id="454db-336">Accédez à la section **Paramètres de chaîne de requête.**</span><span class="sxs-lookup"><span data-stu-id="454db-336">Navigate to the **Query String Parameters** section.</span></span>  

:::image type="complex" source="../media/network-network-resources-headers-query-string-parameters.msft.png" alt-text="Section Paramètres de chaîne de requête" lightbox="../media/network-network-resources-headers-query-string-parameters.msft.png":::
   <span data-ttu-id="454db-338">Section **Paramètres de chaîne de** requête</span><span class="sxs-lookup"><span data-stu-id="454db-338">The **Query String Parameters** section</span></span>  
:::image-end:::  

#### <a name="display-query-string-parameters-source"></a><span data-ttu-id="454db-339">Afficher la source des paramètres de chaîne de requête</span><span class="sxs-lookup"><span data-stu-id="454db-339">Display query string parameters source</span></span>  

<span data-ttu-id="454db-340">Pour afficher la source du paramètre de chaîne de requête d’une requête, utilisez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="454db-340">To display the query string parameter source of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="454db-341">Accédez à la section Paramètres de chaîne de requête.</span><span class="sxs-lookup"><span data-stu-id="454db-341">Navigate to the Query String Parameters section.</span></span>  <span data-ttu-id="454db-342">Pour plus d’informations, [accédez à Afficher les paramètres de chaîne de requête.](#display-query-string-parameters)</span><span class="sxs-lookup"><span data-stu-id="454db-342">For more information, navigate to [Display query string parameters](#display-query-string-parameters).</span></span>  
1.  <span data-ttu-id="454db-343">Choisissez **la source d’affichage.**</span><span class="sxs-lookup"><span data-stu-id="454db-343">Choose **view source**.</span></span>  

#### <a name="display-url-encoded-query-string-parameters"></a><span data-ttu-id="454db-344">Afficher les paramètres de chaîne de requête codés en URL</span><span class="sxs-lookup"><span data-stu-id="454db-344">Display URL-encoded query string parameters</span></span>  

<span data-ttu-id="454db-345">Pour afficher les paramètres de chaîne de requête dans un format lisible par l’homme, mais avec des codages conservés, utilisez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="454db-345">To display query string parameters in a human-readable format, but with encodings preserved, use the following steps.</span></span>  

1.  <span data-ttu-id="454db-346">Accédez à la section Paramètres de chaîne de requête.</span><span class="sxs-lookup"><span data-stu-id="454db-346">Navigate to the Query String Parameters section.</span></span>  <span data-ttu-id="454db-347">Pour plus d’informations, [accédez à Afficher les paramètres de chaîne de requête.](#display-query-string-parameters)</span><span class="sxs-lookup"><span data-stu-id="454db-347">For more information, navigate to [Display query string parameters](#display-query-string-parameters).</span></span>  
1.  <span data-ttu-id="454db-348">Choisissez **l’URL d’affichage codée.**</span><span class="sxs-lookup"><span data-stu-id="454db-348">Choose **view URL encoded**.</span></span>  

### <a name="display-cookies"></a><span data-ttu-id="454db-349">Afficher les cookies</span><span class="sxs-lookup"><span data-stu-id="454db-349">Display cookies</span></span>  

<span data-ttu-id="454db-350">Pour afficher les cookies envoyés dans l’en-tête HTTP d’une requête, utilisez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="454db-350">To display the cookies sent in the HTTP header of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="454db-351">Choisissez l’URL de la demande, sous la colonne **Nom** de la table Requests.</span><span class="sxs-lookup"><span data-stu-id="454db-351">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="454db-352">Choisissez le **panneau Cookies.**</span><span class="sxs-lookup"><span data-stu-id="454db-352">Choose the **Cookies** panel.</span></span>  

<!--For more information about each of the columns, navigate to [Fields][ManageDataCookiesFields].  -->  

<!--[ManageDataCookiesFields]: manage-data/cookies#fields  -->  
<!--TODO: add link when section is available -->  

:::image type="complex" source="../media/network-network-resources-cookies.msft.png" alt-text="Panneau Cookies" lightbox="../media/network-network-resources-cookies.msft.png":::
   <span data-ttu-id="454db-354">Panneau Cookies</span><span class="sxs-lookup"><span data-stu-id="454db-354">The Cookies panel</span></span>  
:::image-end:::  

### <a name="display-the-timing-breakdown-of-a-request"></a><span data-ttu-id="454db-355">Affichage de la répartition du minutage d’une demande</span><span class="sxs-lookup"><span data-stu-id="454db-355">Display the timing breakdown of a request</span></span>  

<span data-ttu-id="454db-356">Pour afficher la répartition du minutage d’une demande, utilisez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="454db-356">To display the timing breakdown of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="454db-357">Choisissez l’URL de la demande, sous la colonne **Nom** de la table Requests.</span><span class="sxs-lookup"><span data-stu-id="454db-357">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="454db-358">Sélectionnez **le panneau De minutage.**</span><span class="sxs-lookup"><span data-stu-id="454db-358">Choose the **Timing** panel.</span></span>  

<span data-ttu-id="454db-359">Pour accéder plus rapidement aux données, accédez à l’aperçu [d’une répartition du minutage.](#preview-a-timing-breakdown)</span><span class="sxs-lookup"><span data-stu-id="454db-359">For a faster way to access the data, navigate to [Preview a timing breakdown](#preview-a-timing-breakdown).</span></span>  

<span data-ttu-id="454db-360">Pour plus d’informations sur chacune des phases \*\*\*\* qui peuvent être affichées dans le panneau de minutage, accédez aux phases de répartition [du minutage expliquées.](#timing-breakdown-phases-explained)</span><span class="sxs-lookup"><span data-stu-id="454db-360">For more information about each of the phases that may be displayed in the **Timing** panel, navigate to [Timing breakdown phases explained](#timing-breakdown-phases-explained).</span></span>  

:::image type="complex" source="../media/network-network-resources-timing.msft.png" alt-text="Panneau De minutage" lightbox="../media/network-network-resources-timing.msft.png":::
   <span data-ttu-id="454db-362">Panneau **De minutage**</span><span class="sxs-lookup"><span data-stu-id="454db-362">The **Timing** panel</span></span>  
:::image-end:::  

<span data-ttu-id="454db-363">Plus d’informations sur chacune des phases.</span><span class="sxs-lookup"><span data-stu-id="454db-363">More information about each of the phases.</span></span>  

<span data-ttu-id="454db-364">Pour plus d’informations sur l’accès à l’affichage, accédez à [Afficher la répartition du minutage.](#display-the-timing-breakdown-of-a-request)</span><span class="sxs-lookup"><span data-stu-id="454db-364">For more information about accessing the display, navigate to [Display timing breakdown](#display-the-timing-breakdown-of-a-request).</span></span>  

#### <a name="preview-a-timing-breakdown"></a><span data-ttu-id="454db-365">Afficher un aperçu de la répartition du minutage</span><span class="sxs-lookup"><span data-stu-id="454db-365">Preview a timing breakdown</span></span>  

<span data-ttu-id="454db-366">Pour afficher un aperçu de la répartition du minutage d’une demande, dans la colonne **Cascade** de la table Demandes, pointez sur l’entrée de la demande.</span><span class="sxs-lookup"><span data-stu-id="454db-366">To display a preview of the timing breakdown of a request, in the **Waterfall** column of the Requests table, hover on the entry for the request.</span></span>  

<span data-ttu-id="454db-367">Pour plus d’informations sur l’accès aux données sans pointage, accédez à Afficher la répartition du [minutage d’une demande.](#display-the-timing-breakdown-of-a-request)</span><span class="sxs-lookup"><span data-stu-id="454db-367">For more information about how to access the data without hovering, navigate to [Display the timing breakdown of a request](#display-the-timing-breakdown-of-a-request).</span></span>  

:::image type="complex" source="../media/network-network-resources-waterfall-hover.msft.png" alt-text="> aperçu de la répartition du minutage d’une demande" lightbox="../media/network-network-resources-waterfall-hover.msft.png":::
   <span data-ttu-id="454db-369">Afficher un aperçu de la répartition du minutage d’une demande</span><span class="sxs-lookup"><span data-stu-id="454db-369">Preview the timing breakdown of a request</span></span>  
:::image-end:::  

#### <a name="timing-breakdown-phases-explained"></a><span data-ttu-id="454db-370">Phases de répartition du minutage expliquées</span><span class="sxs-lookup"><span data-stu-id="454db-370">Timing breakdown phases explained</span></span>  

<span data-ttu-id="454db-371">Plus d’informations sur chacune des phases qui peuvent s’afficher dans le **panneau De** minutage.</span><span class="sxs-lookup"><span data-stu-id="454db-371">More information about each of the phases that may display in the **Timing** panel.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="454db-372">File d’attente</span><span class="sxs-lookup"><span data-stu-id="454db-372">Queueing</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="454db-373">Le navigateur place les demandes en file d’attente lorsque l’une des valeurs suivantes est vraie.</span><span class="sxs-lookup"><span data-stu-id="454db-373">The browser queues requests when any of the following are true.</span></span>  
      
      *   <span data-ttu-id="454db-374">Des demandes de priorité élevée existent.</span><span class="sxs-lookup"><span data-stu-id="454db-374">Higher priority requests exist.</span></span>  
      *   <span data-ttu-id="454db-375">Six connexions TCP sont ouvertes pour la même origine, ce qui est la limite.</span><span class="sxs-lookup"><span data-stu-id="454db-375">Six TCP connections are open for the same origin, which is the limit.</span></span>  <span data-ttu-id="454db-376">S’applique uniquement à HTTP/1.0 et HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="454db-376">Applies to HTTP/1.0 and HTTP/1.1 only.</span></span>  
      *   <span data-ttu-id="454db-377">Le navigateur alloue brièvement de l’espace dans le cache disque.</span><span class="sxs-lookup"><span data-stu-id="454db-377">The browser is briefly allocating space in the disk cache.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="454db-378">Bloqué</span><span class="sxs-lookup"><span data-stu-id="454db-378">Stalled</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="454db-379">La demande est bloquée pour l’une des raisons décrites dans **la file d’attente.**</span><span class="sxs-lookup"><span data-stu-id="454db-379">The request is stalled for any of the reasons described in **Queueing**.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="454db-380">Recherche DNS</span><span class="sxs-lookup"><span data-stu-id="454db-380">DNS Lookup</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="454db-381">Le navigateur est en cours de résolution de l’adresse IP de la demande.</span><span class="sxs-lookup"><span data-stu-id="454db-381">The browser is resolving the IP address for the request.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="454db-382">Connexion initiale</span><span class="sxs-lookup"><span data-stu-id="454db-382">Initial connection</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="454db-383">Le navigateur établit une connexion incluant des liaisons TCP, des tentatives TCP et négocie une couche de socket sécurisée.</span><span class="sxs-lookup"><span data-stu-id="454db-383">The browser establishes a connection including TCP handshakes, TCP retries, and negotiates a Secure Socket Layer.</span></span>
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="454db-384">Négociation de proxy</span><span class="sxs-lookup"><span data-stu-id="454db-384">Proxy negotiation</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="454db-385">Le navigateur négocie la demande avec un [serveur proxy.][WikiProxyServer]</span><span class="sxs-lookup"><span data-stu-id="454db-385">The browser is negotiating the request with a [proxy server][WikiProxyServer].</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="454db-386">Demande envoyée</span><span class="sxs-lookup"><span data-stu-id="454db-386">Request sent</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="454db-387">La demande est envoyée.</span><span class="sxs-lookup"><span data-stu-id="454db-387">The request is being sent.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="454db-388">Préparation de ServiceWorker</span><span class="sxs-lookup"><span data-stu-id="454db-388">ServiceWorker Preparation</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="454db-389">Le navigateur démarre le service de travail.</span><span class="sxs-lookup"><span data-stu-id="454db-389">The browser is starting the service worker.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="454db-390">Demande à ServiceWorker</span><span class="sxs-lookup"><span data-stu-id="454db-390">Request to ServiceWorker</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="454db-391">La demande est envoyée au service de travail.</span><span class="sxs-lookup"><span data-stu-id="454db-391">The request is being sent to the service worker.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="454db-392">Waiting \(TTFB\)</span><span class="sxs-lookup"><span data-stu-id="454db-392">Waiting \(TTFB\)</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="454db-393">Le navigateur attend le premier byte d’une réponse.</span><span class="sxs-lookup"><span data-stu-id="454db-393">The browser is waiting for the first byte of a response.</span></span>  <span data-ttu-id="454db-394">TTFB signifie « Time To First Byte ».</span><span class="sxs-lookup"><span data-stu-id="454db-394">TTFB stands for Time To First Byte.</span></span>  <span data-ttu-id="454db-395">Ce délai inclut un aller-retour de latence et le temps que le serveur a pris pour préparer la réponse.</span><span class="sxs-lookup"><span data-stu-id="454db-395">This timing includes one round trip of latency and the time the server took to prepare the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="454db-396">Téléchargement de contenu</span><span class="sxs-lookup"><span data-stu-id="454db-396">Content Download</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="454db-397">Le navigateur reçoit la réponse.</span><span class="sxs-lookup"><span data-stu-id="454db-397">The browser is receiving the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="454db-398">Réception de push</span><span class="sxs-lookup"><span data-stu-id="454db-398">Receiving Push</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="454db-399">Le navigateur reçoit des données pour cette réponse via HTTP/2 Server Push.</span><span class="sxs-lookup"><span data-stu-id="454db-399">The browser is receiving data for this response via HTTP/2 Server Push.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="454db-400">Lecture push</span><span class="sxs-lookup"><span data-stu-id="454db-400">Reading Push</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="454db-401">Le navigateur lit les données locales reçues précédemment.</span><span class="sxs-lookup"><span data-stu-id="454db-401">The browser is reading the local data previously received.</span></span>  
   :::column-end:::
:::row-end:::  

### <a name="display-initiators-and-dependencies"></a><span data-ttu-id="454db-402">Afficher les initiateurs et les dépendances</span><span class="sxs-lookup"><span data-stu-id="454db-402">Display initiators and dependencies</span></span>  

<span data-ttu-id="454db-403">Pour afficher les initiateurs et les dépendances d’une demande, maintenez la demande en attente et pointez dessus `Shift` dans la table Demandes.</span><span class="sxs-lookup"><span data-stu-id="454db-403">To display the initiators and dependencies of a request, hold `Shift`and hover on the request in the Requests table.</span></span>  <span data-ttu-id="454db-404">Couleurs DevTools : les initiateurs sont affichés en vert et les dépendances en rouge.</span><span class="sxs-lookup"><span data-stu-id="454db-404">DevTools colors: initiators are shown in green and dependencies are shown in red.</span></span>  

:::image type="complex" source="../media/network-network-resources-initiators-dependencies.msft.png" alt-text="Afficher les initiateurs et les dépendances d’une demande" lightbox="../media/network-network-resources-initiators-dependencies.msft.png":::
   <span data-ttu-id="454db-406">Afficher les initiateurs et les dépendances d’une demande</span><span class="sxs-lookup"><span data-stu-id="454db-406">Display the initiators and dependencies of a request</span></span>  
:::image-end:::  

<span data-ttu-id="454db-407">Lorsque la table Requests est classé dans l’ordre chronologique, si vous pointez sur une ligne, la ligne qui précède affiche une demande verte.</span><span class="sxs-lookup"><span data-stu-id="454db-407">When the Requests table is ordered chronologically, if you hover on a line, the line preceding it displays a green request.</span></span>  <span data-ttu-id="454db-408">La demande verte est l’initiateur de la dépendance.</span><span class="sxs-lookup"><span data-stu-id="454db-408">The green request is the initiator of the dependency.</span></span>  <span data-ttu-id="454db-409">Si une autre demande verte est affichée sur la ligne avant cette ligne, cette demande supérieure est l’initiateur de l’initiateur.</span><span class="sxs-lookup"><span data-stu-id="454db-409">If another green request is displayed on the line before that, that higher request is the initiator of the initiator.</span></span>  <span data-ttu-id="454db-410">Et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="454db-410">And so on.</span></span>  

### <a name="display-load-events"></a><span data-ttu-id="454db-411">Afficher les événements de chargement</span><span class="sxs-lookup"><span data-stu-id="454db-411">Display load events</span></span>  

<span data-ttu-id="454db-412">DevTools affiche le minutage des événements à plusieurs `DOMContentLoaded` `load` endroits sur **l’outil** Réseau.</span><span class="sxs-lookup"><span data-stu-id="454db-412">DevTools displays the timing of the `DOMContentLoaded` and `load` events in multiple places on the **Network** tool.</span></span>  <span data-ttu-id="454db-413">`DOMContentLoaded`L’événement est bleu et l’événement est `load` rouge.</span><span class="sxs-lookup"><span data-stu-id="454db-413">The `DOMContentLoaded` event is colored blue, and the `load` event is red.</span></span>  

:::image type="complex" source="../media/network-network-requests-load-events.msft.png" alt-text="Emplacements du DOMContentLoaded et chargement des événements sur le panneau réseau" lightbox="../media/network-network-requests-load-events.msft.png":::
   <span data-ttu-id="454db-415">Emplacements des `DOMContentLoaded` événements et des événements `load` sur **l’outil** Réseau</span><span class="sxs-lookup"><span data-stu-id="454db-415">The locations of the `DOMContentLoaded` and `load` events on the **Network** tool</span></span>  
:::image-end:::  

### <a name="display-the-total-number-of-requests"></a><span data-ttu-id="454db-416">Affichage du nombre total de demandes</span><span class="sxs-lookup"><span data-stu-id="454db-416">Display the total number of requests</span></span>  

<span data-ttu-id="454db-417">Le nombre total de demandes \*\*\*\* est répertorié dans le volet Résumé, en bas de **l’outil** Réseau.</span><span class="sxs-lookup"><span data-stu-id="454db-417">The total number of requests is listed in the **Summary** pane, at the bottom of the **Network** tool.</span></span>  

> [!CAUTION]
> <span data-ttu-id="454db-418">Ce numéro suit uniquement les demandes qui ont été enregistrées depuis l’ouverture de DevTools.</span><span class="sxs-lookup"><span data-stu-id="454db-418">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="454db-419">Si d’autres demandes se sont produites avant l’ouverture de DevTools, ces demandes ne sont pas comptabilisées.</span><span class="sxs-lookup"><span data-stu-id="454db-419">If other requests occurred before DevTools was opened, those requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-requests.msft.png" alt-text="Nombre total de demandes depuis l’ouverture de DevTools" lightbox="../media/network-network-total-requests.msft.png":::
   <span data-ttu-id="454db-421">Nombre total de demandes depuis l’ouverture de DevTools</span><span class="sxs-lookup"><span data-stu-id="454db-421">The total number of requests since DevTools were opened</span></span>  
:::image-end:::  

### <a name="display-the-total-download-size"></a><span data-ttu-id="454db-422">Afficher la taille totale du téléchargement</span><span class="sxs-lookup"><span data-stu-id="454db-422">Display the total download size</span></span>  

<span data-ttu-id="454db-423">La taille totale des demandes de \*\*\*\* téléchargement est répertoriée dans le volet Résumé, en bas de **l’outil** Réseau.</span><span class="sxs-lookup"><span data-stu-id="454db-423">The total download size of requests is listed in the **Summary** pane, at the bottom of the **Network** tool.</span></span>  

> [!CAUTION]
> <span data-ttu-id="454db-424">Ce numéro suit uniquement les demandes qui ont été enregistrées depuis l’ouverture de DevTools.</span><span class="sxs-lookup"><span data-stu-id="454db-424">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="454db-425">Si d’autres demandes se sont produites avant l’ouverture de DevTools, les demandes précédentes ne sont pas comptabilisées.</span><span class="sxs-lookup"><span data-stu-id="454db-425">If other requests occurred before DevTools was opened, the previous requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-download-size.msft.png" alt-text="Taille totale des demandes de téléchargement" lightbox="../media/network-network-total-download-size.msft.png":::
   <span data-ttu-id="454db-427">Taille totale des demandes de téléchargement</span><span class="sxs-lookup"><span data-stu-id="454db-427">The total download size of requests</span></span>  
:::image-end:::  

<span data-ttu-id="454db-428">Pour vérifier la taille des ressources une fois que le navigateur a décompressé chaque élément, accédez pour afficher la taille non [compressée d’une ressource.](#display-the-uncompressed-size-of-a-resource)</span><span class="sxs-lookup"><span data-stu-id="454db-428">To verify how large resources are after the browser uncompresses each item, navigate to [display the uncompressed size of a resource](#display-the-uncompressed-size-of-a-resource).</span></span>  

### <a name="display-the-stack-trace-that-caused-a-request"></a><span data-ttu-id="454db-429">Afficher la trace de pile à l’origine d’une demande</span><span class="sxs-lookup"><span data-stu-id="454db-429">Display the stack trace that caused a request</span></span>  

<span data-ttu-id="454db-430">Après qu’une instruction JavaScript demande une ressource, pointez sur la colonne **Initiator** pour afficher la trace de pile précédant la demande.</span><span class="sxs-lookup"><span data-stu-id="454db-430">After a JavaScript statement requests a resource, hover on the **Initiator** column to display the stack trace leading up to the request.</span></span>  

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

:::image type="complex" source="../media/network-network-requests-initiator-stack.msft.png" alt-text="Trace de pile menant à une demande de ressource" lightbox="../media/network-network-requests-initiator-stack.msft.png":::
   <span data-ttu-id="454db-432">Trace de pile menant à une demande de ressource</span><span class="sxs-lookup"><span data-stu-id="454db-432">The stack trace leading up to a resource request</span></span>  
:::image-end:::  

### <a name="display-the-uncompressed-size-of-a-resource"></a><span data-ttu-id="454db-433">Afficher la taille non compressée d’une ressource</span><span class="sxs-lookup"><span data-stu-id="454db-433">Display the uncompressed size of a resource</span></span>  

<span data-ttu-id="454db-434">Activer la case **à cocher** Utiliser les lignes de requête de grande taille, puis passer en revue la valeur inférieure de la **colonne** Taille.</span><span class="sxs-lookup"><span data-stu-id="454db-434">Turn on the **Use large request rows** checkbox and then review the bottom value of the **Size** column.</span></span>  

:::image type="complex" source="../media/network-network-requests-uncompressed-compare.msft.png" alt-text="Exemple de ressources non compressées" lightbox="../media/network-network-requests-uncompressed-compare.msft.png":::
   <span data-ttu-id="454db-436">Exemple de ressources non compressées \(La taille compressée du fichier envoyé sur le réseau était , alors que la taille non compressée était `jquery-3.3.1.min.js` `29.9 KB` `84.9 KB` \)</span><span class="sxs-lookup"><span data-stu-id="454db-436">An example of uncompressed resources  \(The compressed size of the `jquery-3.3.1.min.js` file that was sent over the network was `29.9 KB`, whereas the uncompressed size was `84.9 KB`\)</span></span>  
:::image-end:::  

## <a name="export-requests-data"></a><span data-ttu-id="454db-437">Exporter les données des demandes</span><span class="sxs-lookup"><span data-stu-id="454db-437">Export requests data</span></span>  

### <a name="save-all-network-requests-to-a-har-file"></a><span data-ttu-id="454db-438">Enregistrer toutes les demandes réseau dans un fichier HAR</span><span class="sxs-lookup"><span data-stu-id="454db-438">Save all network requests to a HAR file</span></span>  

<span data-ttu-id="454db-439">Pour enregistrer toutes les demandes réseau dans un fichier HAR, complétez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="454db-439">To save all network requests to a HAR file, complete the following steps.</span></span>  

1.  <span data-ttu-id="454db-440">Pointez sur n’importe quelle demande dans la table Demandes et ouvrez le menu contextuel \(clic droit\).</span><span class="sxs-lookup"><span data-stu-id="454db-440">Hover on any request in the Requests table and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="454db-441">Choose **Save as HAR with Content**.</span><span class="sxs-lookup"><span data-stu-id="454db-441">Choose **Save as HAR with Content**.</span></span>  <span data-ttu-id="454db-442">DevTools enregistre toutes les demandes qui se sont produites depuis que vous avez ouvert DevTools dans le fichier HAR.</span><span class="sxs-lookup"><span data-stu-id="454db-442">DevTools saves all requests that have occurred since you opened DevTools to the HAR file.</span></span>  <span data-ttu-id="454db-443">Vous ne pouvez pas filtrer les demandes.</span><span class="sxs-lookup"><span data-stu-id="454db-443">You are not able to filter requests.</span></span>  <span data-ttu-id="454db-444">Vous ne pouvez pas non plus enregistrer une seule requête.</span><span class="sxs-lookup"><span data-stu-id="454db-444">You are also not able to save a single request.</span></span>  

<span data-ttu-id="454db-445">Une fois que vous enregistrez un fichier HAR, vous pouvez l’importer à nouveau dans DevTools pour analyse.</span><span class="sxs-lookup"><span data-stu-id="454db-445">Once you save a HAR file, you may import it back into DevTools for analysis.</span></span>  <span data-ttu-id="454db-446">Il suffit de glisser-déposer le fichier HAR dans la table Requests.</span><span class="sxs-lookup"><span data-stu-id="454db-446">Just drag-and-drop the HAR file into the Requests table.</span></span>  
<!--For more information, navigate to also [HAR Analyzer][HARAnalyzer].  -->  

<!--[HARAnalyzer]: https://toolbox.alphabetapps.com/apps/har_analyzer  -->  
<!--Todo: add section link when content is available  -->  

:::image type="complex" source="../media/network-network-requests-save-har-content.msft.png" alt-text="Choose Save as HAR with Content" lightbox="../media/network-network-requests-save-har-content.msft.png":::
   <span data-ttu-id="454db-448">Choose **Save as HAR with Content**</span><span class="sxs-lookup"><span data-stu-id="454db-448">Choose **Save as HAR with Content**</span></span>  
:::image-end:::  

### <a name="copy-one-or-more-requests-to-the-clipboard"></a><span data-ttu-id="454db-449">Copier une ou plusieurs demandes dans le Presse-papiers</span><span class="sxs-lookup"><span data-stu-id="454db-449">Copy one or more requests to the clipboard</span></span>  

<span data-ttu-id="454db-450">Sous la **colonne Nom** de la table Demandes, pointez sur une demande, ouvrez le menu contextuel \(clic droit\), pointez sur **Copier**et choisissez l’une des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="454db-450">Under the **Name** column of the Requests table, hover on a request, open the contextual menu \(right-click\), hover on **Copy**, and choose one of the following options.</span></span>  

| <span data-ttu-id="454db-451">Nom</span><span class="sxs-lookup"><span data-stu-id="454db-451">Name</span></span> | <span data-ttu-id="454db-452">Détails</span><span class="sxs-lookup"><span data-stu-id="454db-452">Details</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="454db-453">Copier l’adresse du lien</span><span class="sxs-lookup"><span data-stu-id="454db-453">Copy Link Address</span></span>** | <span data-ttu-id="454db-454">Copiez l’URL de la demande dans le Presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="454db-454">Copy the URL of the request to the clipboard.</span></span> |  
| **<span data-ttu-id="454db-455">Copier la réponse</span><span class="sxs-lookup"><span data-stu-id="454db-455">Copy Response</span></span>** | <span data-ttu-id="454db-456">Copiez le corps de la réponse dans le Presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="454db-456">Copy the response body to the clipboard.</span></span> |  
| **<span data-ttu-id="454db-457">Copier en tant que récupération</span><span class="sxs-lookup"><span data-stu-id="454db-457">Copy as Fetch</span></span>** | &nbsp; |  
| **<span data-ttu-id="454db-458">Copier en tant que cURL</span><span class="sxs-lookup"><span data-stu-id="454db-458">Copy as cURL</span></span>** | <span data-ttu-id="454db-459">Copiez la demande en tant que commande cURL.</span><span class="sxs-lookup"><span data-stu-id="454db-459">Copy the request as a cURL command.</span></span> |  
| **<span data-ttu-id="454db-460">Copier tout en tant que récupération</span><span class="sxs-lookup"><span data-stu-id="454db-460">Copy All as Fetch</span></span>** | &nbsp; |  
| **<span data-ttu-id="454db-461">Copier tout en tant que cURL</span><span class="sxs-lookup"><span data-stu-id="454db-461">Copy All as cURL</span></span>** | <span data-ttu-id="454db-462">Copiez toutes les demandes en tant que chaîne de commandes cURL.</span><span class="sxs-lookup"><span data-stu-id="454db-462">Copy all requests as a chain of cURL commands.</span></span> |  
| **<span data-ttu-id="454db-463">Copier tout en tant que HAR</span><span class="sxs-lookup"><span data-stu-id="454db-463">Copy All as HAR</span></span>** | <span data-ttu-id="454db-464">Copiez toutes les demandes en tant que données HAR.</span><span class="sxs-lookup"><span data-stu-id="454db-464">Copy all requests as HAR data.</span></span> |  

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

:::image type="complex" source="../media/network-network-requests-copy-response.msft.png" alt-text="Choose Copy Response" lightbox="../media/network-network-requests-copy-response.msft.png":::
   <span data-ttu-id="454db-466">Choose **Copy Response**</span><span class="sxs-lookup"><span data-stu-id="454db-466">Choose **Copy Response**</span></span>  
:::image-end:::  

### <a name="copy-formatted-response-json-to-the-clipboard"></a><span data-ttu-id="454db-467">Copier la réponse mise en forme JSON dans le Presse-papiers</span><span class="sxs-lookup"><span data-stu-id="454db-467">Copy formatted response JSON to the clipboard</span></span>  

<span data-ttu-id="454db-468">Choisissez une demande réseau et accédez au volet **En-têtes.**</span><span class="sxs-lookup"><span data-stu-id="454db-468">Choose a network request and navigate to the **Headers** pane.</span></span>  <span data-ttu-id="454db-469">Pour copier la valeur JSON d’une réponse, accédez à La charge utile de la **demande,** pointez sur le contenu de la réponse JSON, ouvrez le menu contextuel \(clic droit\), puis choisissez Copier la **valeur**.</span><span class="sxs-lookup"><span data-stu-id="454db-469">To copy the JSON value of a response, navigate to **Request payload**, hover on the JSON response content, open the contextual menu \(right-click\), and choose **Copy Value**.</span></span>  

:::row:::
   :::column span="":::
        :::image type="complex" source="../media/network-header-copy-property-value.msft.png" alt-text="Copier la valeur dans le menu contextuel" lightbox="../media/network-header-copy-property-value.msft.png":::
          <span data-ttu-id="454db-471">**Copier la valeur** dans le menu contextuel</span><span class="sxs-lookup"><span data-stu-id="454db-471">**Copy Value** in contextual menu</span></span>  
        :::image-end:::  
   :::column-end:::
   :::column span="":::
        :::image type="complex" source="../media/network-header-paste-property-value.msft.png" alt-text="Code microsoft Visual Studio avec réponse mise en forme JSON" lightbox="../media/network-header-paste-property-value.msft.png":::
          <span data-ttu-id="454db-473">Pasting formatted response JSON in Microsoft Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="454db-473">Pasting formatted response JSON in Microsoft Visual Studio Code</span></span>  
        :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="copy-property-values-from-network-requests-to-your-clipboard"></a><span data-ttu-id="454db-474">Copier les valeurs des propriétés des demandes réseau dans votre Presse-papiers</span><span class="sxs-lookup"><span data-stu-id="454db-474">Copy property values from network requests to your clipboard</span></span>  

<span data-ttu-id="454db-475">Pour copier les valeurs des propriétés des demandes réseau dans votre Presse-papiers, effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="454db-475">To copy property values from network requests to your clipboard, complete the following actions.</span></span>  

1.  <span data-ttu-id="454db-476">Ouvrez **le volet En-têtes.**</span><span class="sxs-lookup"><span data-stu-id="454db-476">Open the **Headers** pane.</span></span>  
1.  <span data-ttu-id="454db-477">Ouvrez l’une des sections d’en-tête suivantes.</span><span class="sxs-lookup"><span data-stu-id="454db-477">Open one of the following header sections.</span></span>  
    *   <span data-ttu-id="454db-478">Demander la charge utile \(JSON\)</span><span class="sxs-lookup"><span data-stu-id="454db-478">Request payload \(JSON\)</span></span>  
    *   <span data-ttu-id="454db-479">Données de formulaire</span><span class="sxs-lookup"><span data-stu-id="454db-479">Form Data</span></span>  
    *   <span data-ttu-id="454db-480">Paramètres de chaîne de requête</span><span class="sxs-lookup"><span data-stu-id="454db-480">Query String Parameters</span></span>  
    *   <span data-ttu-id="454db-481">En-têtes de requête</span><span class="sxs-lookup"><span data-stu-id="454db-481">Request Headers</span></span>  
    *   <span data-ttu-id="454db-482">En-têtes de réponse</span><span class="sxs-lookup"><span data-stu-id="454db-482">Response Headers</span></span>  
1.  <span data-ttu-id="454db-483">Ouvrez le menu contextuel \(clic droit\) > **valeur copier.**</span><span class="sxs-lookup"><span data-stu-id="454db-483">Open the contextual menu \(right-click\) > **Copy value**.</span></span>  <span data-ttu-id="454db-484">Vous pouvez maintenant coller la valeur dans n’importe quel éditeur pour la réviser.</span><span class="sxs-lookup"><span data-stu-id="454db-484">You may now paste the value into any editor to review it.</span></span>  
    
## <a name="change-the-layout-of-the-network-panel"></a><span data-ttu-id="454db-485">Modifier la disposition du panneau Réseau</span><span class="sxs-lookup"><span data-stu-id="454db-485">Change the layout of the Network panel</span></span>  

<span data-ttu-id="454db-486">Vous pouvez développer ou réduire \*\*\*\* des sections de l’interface utilisateur de l’outil réseau pour concentrer des informations importantes.</span><span class="sxs-lookup"><span data-stu-id="454db-486">You may expand or collapse sections of the **Network** tool UI to focus important information.</span></span>  

### <a name="hide-the-filters-pane"></a><span data-ttu-id="454db-487">Masquer le volet Filtres</span><span class="sxs-lookup"><span data-stu-id="454db-487">Hide the Filters pane</span></span>  

<span data-ttu-id="454db-488">Par défaut, DevTools affiche le volet **Filtres.**</span><span class="sxs-lookup"><span data-stu-id="454db-488">By default, DevTools show the **Filters** pane.</span></span>  
<span data-ttu-id="454db-489">Choisissez **Filtre** \( ![ Filtre ][ImageFilterIcon] \) pour le masquer.</span><span class="sxs-lookup"><span data-stu-id="454db-489">Choose **Filter** \(![Filter][ImageFilterIcon]\) to hide it.</span></span>  

:::image type="complex" source="../media/network-network-resources-hide-filters-button.msft.png" alt-text="Bouton Masquer les filtres" lightbox="../media/network-network-resources-hide-filters-button.msft.png":::
   <span data-ttu-id="454db-491">Bouton Masquer les filtres</span><span class="sxs-lookup"><span data-stu-id="454db-491">The Hide Filters button</span></span>  
:::image-end:::  

### <a name="use-large-request-rows"></a><span data-ttu-id="454db-492">Utiliser des lignes de requête de grande taille</span><span class="sxs-lookup"><span data-stu-id="454db-492">Use large request rows</span></span>  

<span data-ttu-id="454db-493">Utilisez des lignes de grande taille lorsque vous souhaitez davantage d’espaces dans votre table de demandes réseau.</span><span class="sxs-lookup"><span data-stu-id="454db-493">Use large rows when you want more whitespace in your network requests table.</span></span>  <span data-ttu-id="454db-494">Certaines colonnes fournissent également un peu plus d’informations lors de l’utilisation de lignes de grande taille.</span><span class="sxs-lookup"><span data-stu-id="454db-494">Some columns also provide a little more information when using large rows.</span></span>  <span data-ttu-id="454db-495">Par exemple, la valeur inférieure de la colonne **Size** est la taille non compressée d’une demande.</span><span class="sxs-lookup"><span data-stu-id="454db-495">For example, the bottom value of the **Size** column is the uncompressed size of a request.</span></span>  

:::image type="complex" source="../media/network-network-requests-large-request-rows.msft.png" alt-text="Exemple de lignes de requête importantes dans le volet Demandes" lightbox="../media/network-network-requests-large-request-rows.msft.png":::
   <span data-ttu-id="454db-497">Exemple de lignes de requête importantes dans le **volet Demandes**</span><span class="sxs-lookup"><span data-stu-id="454db-497">An example of large request rows in the **Requests** pane</span></span>  
:::image-end:::  

<span data-ttu-id="454db-498">Pour activer les lignes de grande taille, activez la case à cocher Utiliser les **lignes de requête de** grande taille.</span><span class="sxs-lookup"><span data-stu-id="454db-498">To enable large rows, turn on the **Use large request rows** checkbox.</span></span>  

:::image type="complex" source="../media/network-network-requests-use-large-request-rows-on.msft.png" alt-text="Case à cocher Utiliser les lignes de requête de grande taille" lightbox="../media/network-network-requests-use-large-request-rows-on.msft.png":::
   <span data-ttu-id="454db-500">Case **à cocher Utiliser les lignes de requête de grande** taille</span><span class="sxs-lookup"><span data-stu-id="454db-500">The **Use large request rows** checkbox</span></span>  
:::image-end:::  

### <a name="hide-the-overview-pane"></a><span data-ttu-id="454db-501">Masquer le volet Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="454db-501">Hide the Overview pane</span></span>  

<span data-ttu-id="454db-502">Par défaut, DevTools \*\*\*\* affiche le volet Vue d’ensemble.</span><span class="sxs-lookup"><span data-stu-id="454db-502">By default, DevTools displays the **Overview** pane.</span></span>  <span data-ttu-id="454db-503">Pour le masquer, cochez la case **Afficher la** vue d’ensemble.</span><span class="sxs-lookup"><span data-stu-id="454db-503">To hide it, turn off the **Show Overview** checkbox.</span></span>  

:::image type="complex" source="../media/network-network-requests-show-overview-off.msft.png" alt-text="Case à cocher Afficher la vue d’ensemble" lightbox="../media/network-network-requests-show-overview-off.msft.png":::
   <span data-ttu-id="454db-505">Case **à cocher Afficher la vue d’ensemble**</span><span class="sxs-lookup"><span data-stu-id="454db-505">The **Show Overview** checkbox</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="454db-506">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="454db-506">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCaptureScreenshotsIcon]: ../media/capture-screenshots-icon.msft.png  
[ImageClearIcon]: ../media/clear-requests-icon.msft.png  
[ImageFilterIcon]: ../media/filter-icon.msft.png  
[ImageHideIcon]: ../media/hide-overview-icon.msft.png  
[ImageLargeResourceRowsIcon]: ../media/large-resource-rows-button-icon.msft.png  
[ImageRecordOnIcon]: ../media/record-on-icon.msft.png  

<!-- links -->  

[DevtoolsProgressiveWebApps]: ../progressive-web-apps/index.md "Déboguer les applications web progressives | Documents Microsoft"  

<!--[NetworkConditions]: /microsoft-edge/devtools-guide-chromium/network/network-conditions "Optimize Performance Under Varying Network Conditions | Microsoft Docs"  -->  

[MDNHTTPDataURIs]: https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/Data_URIs "Url de données | MDN"  

[WikiProxyServer]: https://en.wikipedia.org/wiki/Proxy_server "Serveur proxy - Wikipedia"  

> [!NOTE]
> <span data-ttu-id="454db-510">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="454db-510">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="454db-511">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/network/reference) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="454db-511">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="454db-513">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="454db-513">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
