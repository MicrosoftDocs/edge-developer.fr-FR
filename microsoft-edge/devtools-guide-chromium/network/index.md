---
description: Didacticiel sur les fonctionnalités réseau les plus populaires dans Microsoft Edge DevTools.
title: Inspecter l’activité réseau dans Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 63a0c8dc1d481ee3fba93146c2e2925bbdd07203
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11565042"
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
# <a name="inspect-network-activity-in-microsoft-edge-devtools"></a><span data-ttu-id="7a970-104">Inspecter l’activité réseau dans Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="7a970-104">Inspect network activity in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="7a970-105">Il s’agit d’un didacticiel pratique de certaines des fonctionnalités de DevTools les plus couramment utilisées liées à l’inspection de l’activité réseau d’une page.</span><span class="sxs-lookup"><span data-stu-id="7a970-105">This is a hands-on tutorial of some of the most commonly-used DevTools features related to inspecting network activity for a page.</span></span>  

<span data-ttu-id="7a970-106">Si vous souhaitez parcourir les fonctionnalités, accédez à [Référence réseau.][DevtoolsNetworkReference]</span><span class="sxs-lookup"><span data-stu-id="7a970-106">If you want to browse features, navigate to [Network Reference][DevtoolsNetworkReference].</span></span>  

<!--TODO: This entire section needs a Microsoft Edge DevTools re-write  -->

<!-- Read on, or watch the video version of this tutorial:  -->  

<!--
> [!VIDEO embed/e1gAyQuIFQo]  
-->

## <a name="when-to-use-the-network-panel"></a><span data-ttu-id="7a970-107">Quand utiliser le panneau réseau</span><span class="sxs-lookup"><span data-stu-id="7a970-107">When to use the Network panel</span></span>  

<span data-ttu-id="7a970-108">En règle générale, utilisez le panneau Réseau lorsque vous devez vous assurer que les ressources sont téléchargées ou téléchargées comme prévu.</span><span class="sxs-lookup"><span data-stu-id="7a970-108">In general, use the Network panel when you need to make sure that resources are being downloaded or uploaded as expected.</span></span>  <span data-ttu-id="7a970-109">Les cas d’utilisation les plus courants pour le panneau réseau sont :</span><span class="sxs-lookup"><span data-stu-id="7a970-109">The most common use cases for the Network panel are:</span></span>  

*   <span data-ttu-id="7a970-110">S’assurer que les ressources sont réellement téléchargées ou téléchargées.</span><span class="sxs-lookup"><span data-stu-id="7a970-110">Making sure that resources are actually being uploaded or downloaded at all.</span></span>  
*   <span data-ttu-id="7a970-111">Inspection des propriétés d’une ressource individuelle, telles que les en-têtes HTTP, le contenu, la taille, etc.</span><span class="sxs-lookup"><span data-stu-id="7a970-111">Inspecting the properties of an individual resource, such as the HTTP headers, content, size, and so on.</span></span>  
    
<span data-ttu-id="7a970-112">Si vous recherchez des moyens d’améliorer les performances de chargement de page, ne **commencez** pas par **l’outil** Réseau.</span><span class="sxs-lookup"><span data-stu-id="7a970-112">If you are looking for ways to improve page load performance, **do not** start with the **Network** tool.</span></span>  <span data-ttu-id="7a970-113">Il existe de nombreux types de problèmes de performances de charge qui ne sont pas liés à l’activité réseau.</span><span class="sxs-lookup"><span data-stu-id="7a970-113">There are many types of load performance issues that are not related to network activity.</span></span>  <span data-ttu-id="7a970-114">Commencez par le panneau Audits, car il vous propose des suggestions ciblées sur l’amélioration de votre page.</span><span class="sxs-lookup"><span data-stu-id="7a970-114">Start with the Audits panel because it gives you targeted suggestions on how to improve your page.</span></span>  <span data-ttu-id="7a970-115">Accédez à [Optimiser la vitesse du site web.][DevtoolsSpeedGetStarted]</span><span class="sxs-lookup"><span data-stu-id="7a970-115">Navigate to [Optimize Website Speed][DevtoolsSpeedGetStarted].</span></span>  

## <a name="open-the-network-panel"></a><span data-ttu-id="7a970-116">Ouvrir le panneau réseau</span><span class="sxs-lookup"><span data-stu-id="7a970-116">Open the Network panel</span></span>  

<span data-ttu-id="7a970-117">Pour obtenir le meilleur de ce didacticiel, ouvrez la démonstration et testez les fonctionnalités sur la page de démonstration.</span><span class="sxs-lookup"><span data-stu-id="7a970-117">To get the most out of this tutorial, open up the demo and try out the features on the demo page.</span></span>  

1.  <span data-ttu-id="7a970-118">Ouvrez [la démonstration Prise en main.][GlitchNetworkGetStarted]</span><span class="sxs-lookup"><span data-stu-id="7a970-118">Open the [Get Started Demo][GlitchNetworkGetStarted].</span></span>  
    
    :::image type="complex" source="../media/network-glitch-inspect-network-activity-demo.msft.png" alt-text="Démonstration" lightbox="../media/network-glitch-inspect-network-activity-demo.msft.png":::
       <span data-ttu-id="7a970-120">Démonstration</span><span class="sxs-lookup"><span data-stu-id="7a970-120">The demo</span></span>  
    :::image-end:::  
    
    <!--You may prefer to move the demo to a separate window.  -->  
    
    <!--
    :::image type="complex" source="../media/network-tutorial/windows.msft.png" alt-text="The demo in one window and this tutorial in a different window" lightbox="../media/network-tutorial/windows.msft.png":::
       The demo in one window and this tutorial in a different window  
    :::image-end:::  
    -->
    
1.  <span data-ttu-id="7a970-121">Pour [ouvrir DevTools,][DevToolsOpen]sélectionnez `Control` + `Shift` + `J` \(Windows, Linux\) ou `Command` + `Option` + `J` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="7a970-121">To [Open DevTools][DevToolsOpen], select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  <span data-ttu-id="7a970-122">**L’outil Console** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="7a970-122">The **Console** tool opens.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-console.msft.png" alt-text="The Console" lightbox="../media/network-glitch-console.msft.png":::
       <span data-ttu-id="7a970-124">Console \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="7a970-124">The **Console**</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="7a970-125">Vous pouvez préférer [ancrer DevTools][DevToolsCustomizePlacement]en bas de votre fenêtre.</span><span class="sxs-lookup"><span data-stu-id="7a970-125">You may prefer to [dock DevTools to the bottom of your window][DevToolsCustomizePlacement].</span></span>  
    
    :::image type="complex" source="../media/network-glitch-console-bottom.msft.png" alt-text="DevTools docked to the bottom of the window" lightbox="../media/network-glitch-console-bottom.msft.png":::
       <span data-ttu-id="7a970-127">DevTools docked to the bottom of the window</span><span class="sxs-lookup"><span data-stu-id="7a970-127">DevTools docked to the bottom of the window</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="7a970-128">Ouvrez **l’outil** Réseau.</span><span class="sxs-lookup"><span data-stu-id="7a970-128">Open the **Network** tool.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-bottom.msft.png" alt-text="Outil console dans devTools docked to the bottom of the window" lightbox="../media/network-glitch-network-bottom.msft.png":::
       <span data-ttu-id="7a970-130">**Outil** console dans devTools docked to the bottom of the window</span><span class="sxs-lookup"><span data-stu-id="7a970-130">**Console** tool in the DevTools docked to the bottom of the window</span></span>  
    :::image-end:::  
    
<span data-ttu-id="7a970-131">Pour l’instant, **l’outil** Réseau est vide.</span><span class="sxs-lookup"><span data-stu-id="7a970-131">Right now the **Network** tool is empty.</span></span>  <span data-ttu-id="7a970-132">DevTools enregistre uniquement l’activité réseau après l’avoir ouverte et aucune activité réseau ne s’est produite depuis que vous avez ouvert DevTools.</span><span class="sxs-lookup"><span data-stu-id="7a970-132">DevTools only logs network activity after you open it and no network activity has occurred since you opened DevTools.</span></span>  

## <a name="log-network-activity"></a><span data-ttu-id="7a970-133">Journal de l’activité réseau</span><span class="sxs-lookup"><span data-stu-id="7a970-133">Log network activity</span></span>  

<span data-ttu-id="7a970-134">Pour afficher l’activité réseau qu’une page provoque :</span><span class="sxs-lookup"><span data-stu-id="7a970-134">To view the network activity that a page causes:</span></span>  

1.  <span data-ttu-id="7a970-135">Actualisez la page web.</span><span class="sxs-lookup"><span data-stu-id="7a970-135">Refresh the webpage.</span></span>  <span data-ttu-id="7a970-136">Le panneau Réseau enregistre toute l’activité réseau dans **le journal réseau.**</span><span class="sxs-lookup"><span data-stu-id="7a970-136">The Network panel logs all network activity in the **Network Log**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network.msft.png" alt-text="Journal réseau" lightbox="../media/network-glitch-network.msft.png":::
       <span data-ttu-id="7a970-138">Journal **réseau**</span><span class="sxs-lookup"><span data-stu-id="7a970-138">The **Network Log**</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="7a970-139">Chaque ligne du journal **réseau représente** une ressource.</span><span class="sxs-lookup"><span data-stu-id="7a970-139">Each row of the **Network Log** represents a resource.</span></span>  <span data-ttu-id="7a970-140">Par défaut, les ressources sont répertoriées dans l’ordre chronologique.</span><span class="sxs-lookup"><span data-stu-id="7a970-140">By default the resources are listed chronologically.</span></span>  <span data-ttu-id="7a970-141">La ressource supérieure est généralement le document HTML principal.</span><span class="sxs-lookup"><span data-stu-id="7a970-141">The top resource is usually the main HTML document.</span></span>  <span data-ttu-id="7a970-142">La ressource inférieure est la dernière ressource demandée.</span><span class="sxs-lookup"><span data-stu-id="7a970-142">The bottom resource is whatever was requested last.</span></span>  
    
    <span data-ttu-id="7a970-143">Chaque colonne représente des informations sur une ressource.</span><span class="sxs-lookup"><span data-stu-id="7a970-143">Each column represents information about a resource.</span></span>  <span data-ttu-id="7a970-144">Dans la figure précédente, les colonnes par défaut sont affichées.</span><span class="sxs-lookup"><span data-stu-id="7a970-144">In the previous figure the default columns are displayed.</span></span>  

    *   <span data-ttu-id="7a970-145">**État**.</span><span class="sxs-lookup"><span data-stu-id="7a970-145">**Status**.</span></span>  <span data-ttu-id="7a970-146">Code d’état HTTP pour la réponse.</span><span class="sxs-lookup"><span data-stu-id="7a970-146">The HTTP status code for response.</span></span>  
    *   <span data-ttu-id="7a970-147">**Type**.</span><span class="sxs-lookup"><span data-stu-id="7a970-147">**Type**.</span></span>  <span data-ttu-id="7a970-148">Type de ressource.</span><span class="sxs-lookup"><span data-stu-id="7a970-148">The resource type.</span></span>  
    *   <span data-ttu-id="7a970-149">**Initiateur**.</span><span class="sxs-lookup"><span data-stu-id="7a970-149">**Initiator**.</span></span>  <span data-ttu-id="7a970-150">Cause de la demande de ressource.</span><span class="sxs-lookup"><span data-stu-id="7a970-150">The cause of the resource request.</span></span>  <span data-ttu-id="7a970-151">La mise en place d’un lien dans la colonne Initiator vous permet d’obtenir le code source à l’origine de la demande.</span><span class="sxs-lookup"><span data-stu-id="7a970-151">CHoosing a link in the Initiator column takes you to the source code that caused the request.</span></span>  
    *   <span data-ttu-id="7a970-152">**Heure**.</span><span class="sxs-lookup"><span data-stu-id="7a970-152">**Time**.</span></span>  <span data-ttu-id="7a970-153">Durée de la demande.</span><span class="sxs-lookup"><span data-stu-id="7a970-153">The duration of the request.</span></span>  
    *   <span data-ttu-id="7a970-154">**Cascade**.</span><span class="sxs-lookup"><span data-stu-id="7a970-154">**Waterfall**.</span></span>  <span data-ttu-id="7a970-155">Représentation graphique des différentes étapes de la demande.</span><span class="sxs-lookup"><span data-stu-id="7a970-155">A graphical representation of the different stages of the request.</span></span>  <span data-ttu-id="7a970-156">Pour afficher une répartition, pointez sur une cascade.</span><span class="sxs-lookup"><span data-stu-id="7a970-156">To display a breakdown, hover on a Waterfall.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="7a970-157">Le graphique au-dessus du journal réseau est appelé Vue d’ensemble.</span><span class="sxs-lookup"><span data-stu-id="7a970-157">The graph above the Network Log is called the Overview.</span></span>  <span data-ttu-id="7a970-158">Vous n’utiliserez pas le graphique Vue d’ensemble dans ce didacticiel, vous pouvez donc le masquer.</span><span class="sxs-lookup"><span data-stu-id="7a970-158">You will not use the Overview graph in this tutorial, so you may hide it.</span></span>  <span data-ttu-id="7a970-159">Accédez à [Masquer le volet Vue d’ensemble.][DevtoolsReferenceHideOverview]</span><span class="sxs-lookup"><span data-stu-id="7a970-159">Navigate to [Hide the Overview pane][DevtoolsReferenceHideOverview].</span></span>
    
1.  <span data-ttu-id="7a970-160">Après avoir ouvert DevTools, il enregistre l’activité réseau dans le journal réseau.</span><span class="sxs-lookup"><span data-stu-id="7a970-160">After you open DevTools, it records network activity in the Network Log.</span></span>  
    <span data-ttu-id="7a970-161">Pour le montrer, regardez d’abord le bas du journal réseau et notez la dernière activité. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="7a970-161">To demonstrate this, first look at the bottom of the **Network Log** and make a mental note of the last activity.</span></span>  
1.  <span data-ttu-id="7a970-162">Sélectionnez maintenant le **bouton Obtenir les** données dans la démonstration.</span><span class="sxs-lookup"><span data-stu-id="7a970-162">Now, select the **Get Data** button in the demo.</span></span>  
1.  <span data-ttu-id="7a970-163">Regardez de nouveau le bas du **journal** réseau.</span><span class="sxs-lookup"><span data-stu-id="7a970-163">Look at the bottom of the **Network Log** again.</span></span>  <span data-ttu-id="7a970-164">Une nouvelle ressource nommée `getstarted.json` s’affiche.</span><span class="sxs-lookup"><span data-stu-id="7a970-164">A new resource named `getstarted.json` is displayed.</span></span>  <span data-ttu-id="7a970-165">Pour que la page web demande le fichier, choisissez le **bouton Obtenir des** données.</span><span class="sxs-lookup"><span data-stu-id="7a970-165">To cause the webpage to request the file, choose the **Get Data** button.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-new-resource.msft.png" alt-text="Une nouvelle ressource dans le journal réseau" lightbox="../media/network-glitch-network-new-resource.msft.png":::
       <span data-ttu-id="7a970-167">Une nouvelle ressource dans le **journal réseau**</span><span class="sxs-lookup"><span data-stu-id="7a970-167">A new resource in the **Network Log**</span></span>  
    :::image-end:::  
    
## <a name="show-more-information"></a><span data-ttu-id="7a970-168">Afficher plus d’informations</span><span class="sxs-lookup"><span data-stu-id="7a970-168">Show more information</span></span>  

<span data-ttu-id="7a970-169">Les colonnes du journal réseau sont configurables.</span><span class="sxs-lookup"><span data-stu-id="7a970-169">The columns of the Network Log are configurable.</span></span>  <span data-ttu-id="7a970-170">Vous pouvez masquer les colonnes que vous n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="7a970-170">You may hide columns that you are not using.</span></span>  
<span data-ttu-id="7a970-171">Il existe également de nombreuses colonnes qui sont masquées par défaut et qui peuvent vous être utiles.</span><span class="sxs-lookup"><span data-stu-id="7a970-171">There are also many columns that are hidden by default which you may find useful.</span></span>  

1.  <span data-ttu-id="7a970-172">Pointez sur l’en-tête de la table Journal réseau, ouvrez le menu contextuel \(clic droit\), puis choisissez **Domaine**.</span><span class="sxs-lookup"><span data-stu-id="7a970-172">Hover on the header of the Network Log table, open the contextual menu \(right-click\), and choose **Domain**.</span></span>  <span data-ttu-id="7a970-173">Le domaine de chaque ressource est maintenant affiché.</span><span class="sxs-lookup"><span data-stu-id="7a970-173">The domain of each resource is now shown.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-edit-column.msft.png" alt-text="Activer la colonne Domaine" lightbox="../media/network-glitch-network-edit-column.msft.png":::
       <span data-ttu-id="7a970-175">Activer la colonne Domaine</span><span class="sxs-lookup"><span data-stu-id="7a970-175">Enable the Domain column</span></span>  
    :::image-end:::  
    
    > [!TIP]
    > <span data-ttu-id="7a970-176">Pour passer en revue l’URL complète d’une ressource, pointez sur la cellule dans la **colonne** Nom.</span><span class="sxs-lookup"><span data-stu-id="7a970-176">To review the full URL of a resource, hover on the cell in the **Name** column.</span></span>  
    
## <a name="simulate-a-slower-network-connection"></a><span data-ttu-id="7a970-177">Simuler une connexion réseau plus lente</span><span class="sxs-lookup"><span data-stu-id="7a970-177">Simulate a slower network connection</span></span>  

<span data-ttu-id="7a970-178">La connexion réseau de l’ordinateur que vous utilisez pour créer des sites est probablement plus rapide que les connexions réseau des appareils mobiles de vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="7a970-178">The network connection of the computer that you use to build sites is probably faster than the network connections of the mobile devices of your users.</span></span>  <span data-ttu-id="7a970-179">En limitation de la page, vous obtenez une meilleure idée du temps de chargement d’une page sur un appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="7a970-179">By throttling the page, you get a better idea of how long a page takes to load on a mobile device.</span></span>  

1.  <span data-ttu-id="7a970-180">Choose the **Throttling** dropdown, which is set to **Online** by default.</span><span class="sxs-lookup"><span data-stu-id="7a970-180">Choose the **Throttling** dropdown, which is set to **Online** by default.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-throttling.msft.png" alt-text="Activer la limitation" lightbox="../media/network-glitch-network-throttling.msft.png":::
       <span data-ttu-id="7a970-182">Activer la limitation</span><span class="sxs-lookup"><span data-stu-id="7a970-182">Enable throttling</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="7a970-183">Choose **Slow 3G**.</span><span class="sxs-lookup"><span data-stu-id="7a970-183">Choose **Slow 3G**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-throttling-slow-3g.msft.png" alt-text="Choose Slow 3G" lightbox="../media/network-glitch-network-throttling-slow-3g.msft.png":::
       <span data-ttu-id="7a970-185">Choose Slow 3G</span><span class="sxs-lookup"><span data-stu-id="7a970-185">Choose Slow 3G</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="7a970-186">Appuyez **longuement sur Recharger** \( Rechargez \), puis choisissez ![ Cache vide et ](../media/refresh-icon.msft.png) **Rechargement dur.**</span><span class="sxs-lookup"><span data-stu-id="7a970-186">Long-press **Reload** \(![Reload](../media/refresh-icon.msft.png)\) and then choose **Empty Cache And Hard Reload**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-empty-cache-and-hard-reset.msft.png" alt-text="Cache vide et rechargement dur" lightbox="../media/network-glitch-empty-cache-and-hard-reset.msft.png":::
       **<span data-ttu-id="7a970-188">Cache vide et rechargement dur</span><span class="sxs-lookup"><span data-stu-id="7a970-188">Empty Cache And Hard Reload</span></span>**  
    :::image-end:::  
    
    <span data-ttu-id="7a970-189">Lors des visites répétées, le navigateur sert généralement certains fichiers à partir du [cache,][MDNHTTPCache]ce qui accélère le chargement de la page.</span><span class="sxs-lookup"><span data-stu-id="7a970-189">On repeat visits, the browser usually serves some files from the [cache][MDNHTTPCache], which speeds up the page load.</span></span>  <span data-ttu-id="7a970-190">**Le cache vide et le rechargement dur** forcent le navigateur à se rendre sur le réseau pour toutes les ressources.</span><span class="sxs-lookup"><span data-stu-id="7a970-190">**Empty Cache And Hard Reload** forces the browser to go the network for all resources.</span></span>  <span data-ttu-id="7a970-191">Utilisez-le pour afficher la façon dont un premier visiteur fait l’expérience d’un chargement de page.</span><span class="sxs-lookup"><span data-stu-id="7a970-191">Use it to display how a first-time visitor experiences a page load.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="7a970-192">Le **flux de travail Cache vide et Rechargement** dur n’est disponible que lorsque DevTools est ouvert.</span><span class="sxs-lookup"><span data-stu-id="7a970-192">The **Empty Cache And Hard Reload** workflow is only available when DevTools is open.</span></span>  
    
## <a name="capture-screenshots"></a><span data-ttu-id="7a970-193">Capture d’écran</span><span class="sxs-lookup"><span data-stu-id="7a970-193">Capture screenshots</span></span>  

<span data-ttu-id="7a970-194">Les captures d’écran affichent l’apparence d’une page web au fil du temps pendant son chargement.</span><span class="sxs-lookup"><span data-stu-id="7a970-194">Screenshots display how a webpage looks over time while it loads.</span></span>  

1.  <span data-ttu-id="7a970-195">Choisissez \( ![ Paramètres réseau \) et ](../media/settings-icon.msft.png) cochez la case Capture **d’écran.**</span><span class="sxs-lookup"><span data-stu-id="7a970-195">Choose \(![Network settings](../media/settings-icon.msft.png)\) and turn on the **Capture screenshots** checkbox.</span></span>
1.  <span data-ttu-id="7a970-196">Actualisez la page à l’aide **du cache vide et du flux de travail de rechargement** dur.</span><span class="sxs-lookup"><span data-stu-id="7a970-196">Refresh the page again using the **Empty Cache And Hard Reload** workflow.</span></span>  <span data-ttu-id="7a970-197">Si vous [avez besoin](#simulate-a-slower-network-connection) d’un rappel sur la façon de le faire, accédez à Simuler une connexion plus lente.</span><span class="sxs-lookup"><span data-stu-id="7a970-197">Navigate to [Simulate a slower connection](#simulate-a-slower-network-connection) if you need a reminder on how to do this.</span></span>  
    <span data-ttu-id="7a970-198">Le panneau Captures d’écran fournit des miniatures de l’aperçu de la page à différents points pendant le processus de chargement.</span><span class="sxs-lookup"><span data-stu-id="7a970-198">The Screenshots panel provides thumbnails of how the page looked at various points during the loading process.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots.msft.png" alt-text="Captures d’écran du chargement de la page" lightbox="../media/network-glitch-network-screenshots.msft.png":::
       <span data-ttu-id="7a970-200">Captures d’écran du chargement de la page</span><span class="sxs-lookup"><span data-stu-id="7a970-200">Screenshots of the page load</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="7a970-201">Choisissez la première miniature.</span><span class="sxs-lookup"><span data-stu-id="7a970-201">Choose the first thumbnail.</span></span>  <span data-ttu-id="7a970-202">DevTools vous indique l’activité réseau qui se produisait à ce moment-là.</span><span class="sxs-lookup"><span data-stu-id="7a970-202">DevTools shows you what network activity was occurring at that moment in time.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots-first.msft.png" alt-text="Activité réseau qui s’est produit lors de la première capture d’écran" lightbox="../media/network-glitch-network-screenshots-first.msft.png":::
       <span data-ttu-id="7a970-204">Activité réseau qui s’est produit lors de la première capture d’écran</span><span class="sxs-lookup"><span data-stu-id="7a970-204">The network activity that was happening during the first screenshot</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="7a970-205">Sélectionnez à nouveau \( Paramètres réseau \) et cochez la case Capture d’écran pour fermer le ![ ](../media/settings-icon.msft.png) volet Captures d’écran. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="7a970-205">Choose \(![Network settings](../media/settings-icon.msft.png)\) again and turn off the **Capture screenshots** checkbox to close the Screenshots pane.</span></span>
1.  <span data-ttu-id="7a970-206">Actualisez la page.</span><span class="sxs-lookup"><span data-stu-id="7a970-206">Refresh the page again.</span></span>  
    
## <a name="inspect-the-details-of-the-resource"></a><span data-ttu-id="7a970-207">Inspecter les détails de la ressource</span><span class="sxs-lookup"><span data-stu-id="7a970-207">Inspect the details of the resource</span></span>  

<span data-ttu-id="7a970-208">Choisissez une ressource pour en savoir plus à son sujet.</span><span class="sxs-lookup"><span data-stu-id="7a970-208">Choose a resource to learn more information about it.</span></span>  <span data-ttu-id="7a970-209">Essayez maintenant :</span><span class="sxs-lookup"><span data-stu-id="7a970-209">Try it now:</span></span>  

1.  <span data-ttu-id="7a970-210">Choose `getstarted.html` .</span><span class="sxs-lookup"><span data-stu-id="7a970-210">Choose `getstarted.html`.</span></span>  <span data-ttu-id="7a970-211">Le **panneau En-têtes** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="7a970-211">The **Headers** panel is shown.</span></span>  <span data-ttu-id="7a970-212">Utilisez ce panneau pour inspecter les en-têtes HTTP.</span><span class="sxs-lookup"><span data-stu-id="7a970-212">Use this panel to inspect HTTP headers.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-headers.msft.png" alt-text="Panneau En-têtes" lightbox="../media/network-glitch-network-resources-headers.msft.png":::
       <span data-ttu-id="7a970-214">Panneau **En-têtes**</span><span class="sxs-lookup"><span data-stu-id="7a970-214">The **Headers** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="7a970-215">Choisissez le **panneau d’aperçu.**</span><span class="sxs-lookup"><span data-stu-id="7a970-215">Choose the **Preview** panel.</span></span>  <span data-ttu-id="7a970-216">Un rendu de base du code HTML est affiché.</span><span class="sxs-lookup"><span data-stu-id="7a970-216">A basic rendering of the HTML is shown.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-preview.msft.png" alt-text="Panneau d’aperçu" lightbox="../media/network-glitch-network-resources-preview.msft.png":::
       <span data-ttu-id="7a970-218">Panneau **d’aperçu**</span><span class="sxs-lookup"><span data-stu-id="7a970-218">The **Preview** panel</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="7a970-219">Le panneau est utile lorsqu’une API renvoie un code d’erreur au format HTML.</span><span class="sxs-lookup"><span data-stu-id="7a970-219">The panel is helpful when an API returns an error code in HTML.</span></span>  <span data-ttu-id="7a970-220">Vous trouverez peut-être plus facile de lire le code HTML rendu que le code source HTML, ou lorsque vous examinez des images.</span><span class="sxs-lookup"><span data-stu-id="7a970-220">You may find it easier to read the rendered HTML than the HTML source code, or when you inspect images.</span></span>  

1.  <span data-ttu-id="7a970-221">Sélectionnez **le panneau de** réponse.</span><span class="sxs-lookup"><span data-stu-id="7a970-221">Choose the **Response** panel.</span></span>  <span data-ttu-id="7a970-222">Le code source HTML est affiché.</span><span class="sxs-lookup"><span data-stu-id="7a970-222">The HTML source code is shown.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-response.msft.png" alt-text="Panneau de réponse" lightbox="../media/network-glitch-network-resources-response.msft.png":::
       <span data-ttu-id="7a970-224">Panneau **de** réponse</span><span class="sxs-lookup"><span data-stu-id="7a970-224">The **Response** panel</span></span>  
    :::image-end:::  
    
    > [!TIP]
    > <span data-ttu-id="7a970-225">Lorsqu’un fichier est minifié, sélectionnez le bouton **Format** \( Format \) en bas du panneau De réponse pour re-mettre en forme le contenu du fichier pour une ![ ](../media/format-icon.msft.png) \*\*\*\* lisibilité.</span><span class="sxs-lookup"><span data-stu-id="7a970-225">When a file is minified, choose the **Format** \(![Format](../media/format-icon.msft.png)\) button at the bottom of the **Response** panel to re-format the contents of the file for readability.</span></span>  
    
1.  <span data-ttu-id="7a970-226">Sélectionnez **le panneau De minutage.**</span><span class="sxs-lookup"><span data-stu-id="7a970-226">Choose the **Timing** panel.</span></span>  <span data-ttu-id="7a970-227">Une répartition de l’activité réseau de la ressource s’affiche.</span><span class="sxs-lookup"><span data-stu-id="7a970-227">A breakdown of the network activity for the resource is displayed.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-timing.msft.png" alt-text="Panneau De minutage" lightbox="../media/network-glitch-network-resources-timing.msft.png":::
       <span data-ttu-id="7a970-229">Panneau **De minutage**</span><span class="sxs-lookup"><span data-stu-id="7a970-229">The **Timing** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="7a970-230">Choose **Close** \( ![ Close ](../media/close-icon.msft.png) \) to view the Network Log again.</span><span class="sxs-lookup"><span data-stu-id="7a970-230">Choose **Close** \(![Close](../media/close-icon.msft.png)\) to view the Network Log again.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-close-tabs.msft.png" alt-text="Bouton Fermer" lightbox="../media/network-glitch-network-resources-close-tabs.msft.png":::
       <span data-ttu-id="7a970-232">Bouton \*\*\*\* Fermer</span><span class="sxs-lookup"><span data-stu-id="7a970-232">The **Close** button</span></span>  
    :::image-end:::  
    
## <a name="search-network-headers-and-responses"></a><span data-ttu-id="7a970-233">En-têtes et réponses du réseau de recherche</span><span class="sxs-lookup"><span data-stu-id="7a970-233">Search network headers and responses</span></span>  

<span data-ttu-id="7a970-234">Utilisez le **volet de** recherche lorsque vous devez rechercher dans les en-têtes HTTP et les réponses de toutes les ressources une chaîne ou une expression régulière.</span><span class="sxs-lookup"><span data-stu-id="7a970-234">Use the **Search** pane when you need to search the HTTP headers and responses of all resources for a certain string or regular expression.</span></span>  

<span data-ttu-id="7a970-235">Par exemple, supposons que vous vouliez vérifier que vos ressources utilisent des stratégies de **cache raisonnables.**</span><span class="sxs-lookup"><span data-stu-id="7a970-235">For example, suppose you want to verify that your resources are using reasonable **cache policies**.</span></span>  

<!--TODO: add cache policies section when available  -->

1.  <span data-ttu-id="7a970-236">Choose **Search** \( ![ Search ](../media/search-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="7a970-236">Choose **Search** \(![Search](../media/search-icon.msft.png)\).</span></span>  <span data-ttu-id="7a970-237">Le volet Recherche s’ouvre à gauche du journal réseau.</span><span class="sxs-lookup"><span data-stu-id="7a970-237">The Search pane opens to the left of the Network log.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-empty.msft.png" alt-text="Volet de recherche" lightbox="../media/network-glitch-network-search-empty.msft.png":::
       <span data-ttu-id="7a970-239">Volet \*\*\*\* de recherche</span><span class="sxs-lookup"><span data-stu-id="7a970-239">The **Search** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="7a970-240">Tapez `Cache-Control` et sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="7a970-240">Type `Cache-Control` and select `Enter`.</span></span>  <span data-ttu-id="7a970-241">Le volet De recherche répertorie toutes les instances de ce qu’il trouve dans les en-têtes de ressource `Cache-Control` ou le contenu.</span><span class="sxs-lookup"><span data-stu-id="7a970-241">The Search pane lists all instances of `Cache-Control` that it finds in resource headers or content.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control.msft.png" alt-text="Résultats de recherche pour Cache-Control" lightbox="../media/network-glitch-network-search-cache-control.msft.png":::
       <span data-ttu-id="7a970-243">Résultats de la recherche pour </span><span class="sxs-lookup"><span data-stu-id="7a970-243">Search results for</span></span> `Cache-Control`  
    :::image-end:::  
    
1.  <span data-ttu-id="7a970-244">Choisissez un résultat pour afficher la ressource dans laquelle le résultat a été trouvé.</span><span class="sxs-lookup"><span data-stu-id="7a970-244">Choose a result to view the resource in which the result was found.</span></span>  <span data-ttu-id="7a970-245">Si vous recherchez les détails de la ressource, sélectionnez un résultat pour y aller directement.</span><span class="sxs-lookup"><span data-stu-id="7a970-245">If you are looking at the details of the resource, select a result to go directly to it.</span></span>  <span data-ttu-id="7a970-246">Par exemple, si la requête a été trouvée dans un en-tête, le panneau **En-têtes** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="7a970-246">For example, if the query was found in a header, the **Headers** panel opens.</span></span>   <span data-ttu-id="7a970-247">Si la requête a été trouvée dans le contenu, le panneau **Réponse** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="7a970-247">If the query was found in content, the **Response** panel opens.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png" alt-text="Résultat de recherche mis en évidence dans le panneau En-têtes" lightbox="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png":::
       <span data-ttu-id="7a970-249">Résultat de recherche mis en évidence dans le panneau **En-têtes**</span><span class="sxs-lookup"><span data-stu-id="7a970-249">A search result highlighted in the **Headers** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="7a970-250">Fermez le volet Recherche et le volet **En-têtes.**</span><span class="sxs-lookup"><span data-stu-id="7a970-250">Close the Search pane and the **Headers** panel.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-close.msft.png" alt-text="Boutons Fermer" lightbox="../media/network-glitch-network-search-close.msft.png":::
       <span data-ttu-id="7a970-252">Boutons **Fermer**</span><span class="sxs-lookup"><span data-stu-id="7a970-252">The **Close** buttons</span></span>  
    :::image-end:::  
    
## <a name="filter-resources"></a><span data-ttu-id="7a970-253">Filtrer les ressources</span><span class="sxs-lookup"><span data-stu-id="7a970-253">Filter resources</span></span>  

<span data-ttu-id="7a970-254">DevTools fournit de nombreux flux de travail pour filtrer les ressources qui ne sont pas pertinentes pour la tâche en cours.</span><span class="sxs-lookup"><span data-stu-id="7a970-254">DevTools provides numerous workflows for filtering out resources that are not relevant to the task at hand.</span></span>  

:::image type="complex" source="../media/network-glitch-network-filter-empty.msft.png" alt-text="Barre d’outils Filtres" lightbox="../media/network-glitch-network-filter-empty.msft.png":::
   <span data-ttu-id="7a970-256">Barre **d’outils Filtres**</span><span class="sxs-lookup"><span data-stu-id="7a970-256">The **Filters** toolbar</span></span>  
:::image-end:::  

<span data-ttu-id="7a970-257">La **barre d’outils** Filtres doit être allumée par défaut.</span><span class="sxs-lookup"><span data-stu-id="7a970-257">The **Filters** toolbar should be turned on by default.</span></span>  <span data-ttu-id="7a970-258">Si ce n’est pas le cas :</span><span class="sxs-lookup"><span data-stu-id="7a970-258">If not:</span></span>  

1.  <span data-ttu-id="7a970-259">Choisissez **Filtre** \( ![ Filtre ](../media/filter-icon.msft.png) \) pour l’afficher.</span><span class="sxs-lookup"><span data-stu-id="7a970-259">Choose **Filter** \(![Filter](../media/filter-icon.msft.png)\) to show it.</span></span>  
    
### <a name="filter-by-string-regular-expression-or-property"></a><span data-ttu-id="7a970-260">Filtrer par chaîne, expression régulière ou propriété</span><span class="sxs-lookup"><span data-stu-id="7a970-260">Filter by string, regular expression, or property</span></span>  

<span data-ttu-id="7a970-261">La **zone de** texte Filtre prend en charge différents types de filtrage.</span><span class="sxs-lookup"><span data-stu-id="7a970-261">The **Filter** text box supports many different types of filtering.</span></span>  

1.  <span data-ttu-id="7a970-262">Tapez `png` dans la zone **de** texte Filtrer.</span><span class="sxs-lookup"><span data-stu-id="7a970-262">Type `png` into the **Filter** text box.</span></span>  <span data-ttu-id="7a970-263">Seuls les fichiers contenant le texte `png` sont affichés.</span><span class="sxs-lookup"><span data-stu-id="7a970-263">Only the files that contain the text `png` are shown.</span></span>  <span data-ttu-id="7a970-264">Dans ce cas, les seuls fichiers qui correspondent au filtre sont les images PNG.</span><span class="sxs-lookup"><span data-stu-id="7a970-264">In this case the only files that match the filter are the PNG images.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-png.msft.png" alt-text="Un filtre de chaîne" lightbox="../media/network-glitch-network-filter-png.msft.png":::
       <span data-ttu-id="7a970-266">Un filtre de chaîne</span><span class="sxs-lookup"><span data-stu-id="7a970-266">A string filter</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="7a970-267">Tapez `/.*\.[cj]s+$/`.</span><span class="sxs-lookup"><span data-stu-id="7a970-267">Type `/.*\.[cj]s+$/`.</span></span>  <span data-ttu-id="7a970-268">DevTools filtre toutes les ressources dont le nom de fichier ne se termine pas par un ou plusieurs `j` `c` `s` caractères.</span><span class="sxs-lookup"><span data-stu-id="7a970-268">DevTools filters out any resource with a filename that does not end with a `j` or a `c` followed by 1 or more `s` characters.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-regex.msft.png" alt-text="Filtre d’expression régulière" lightbox="../media/network-glitch-network-filter-regex.msft.png":::
       <span data-ttu-id="7a970-270">Filtre d’expression régulière</span><span class="sxs-lookup"><span data-stu-id="7a970-270">A regular expression filter</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="7a970-271">Tapez `-main.css`.</span><span class="sxs-lookup"><span data-stu-id="7a970-271">Type `-main.css`.</span></span>  <span data-ttu-id="7a970-272">DevTools filtre les `main.css` sorties.</span><span class="sxs-lookup"><span data-stu-id="7a970-272">DevTools filters out `main.css`.</span></span>  <span data-ttu-id="7a970-273">Si un fichier correspond au modèle, son sein est également filtré.</span><span class="sxs-lookup"><span data-stu-id="7a970-273">If any file matches the pattern, tit is also filtered out.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-negative-statement.msft.png" alt-text="Un filtre négatif" lightbox="../media/network-glitch-network-filter-negative-statement.msft.png":::
       <span data-ttu-id="7a970-275">Un filtre négatif</span><span class="sxs-lookup"><span data-stu-id="7a970-275">A negative filter</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="7a970-276">Tapez `domain:cdn.glitch.com` dans la zone **de** texte Filtrer.</span><span class="sxs-lookup"><span data-stu-id="7a970-276">Type `domain:cdn.glitch.com` into the **Filter** text box.</span></span>  <span data-ttu-id="7a970-277">DevTools filtre toutes les ressources avec une URL qui ne correspond pas à ce domaine.</span><span class="sxs-lookup"><span data-stu-id="7a970-277">DevTools filters out any resource with a URL that does not match this domain.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-property-value.msft.png" alt-text="Un filtre de propriété" lightbox="../media/network-glitch-network-filter-property-value.msft.png":::
       <span data-ttu-id="7a970-279">Un filtre de propriété</span><span class="sxs-lookup"><span data-stu-id="7a970-279">A property filter</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="7a970-280">Pour obtenir la liste complète des propriétés filtrables, accédez à [Filtrer les demandes par propriétés.][DevtoolsReferenceProperty]</span><span class="sxs-lookup"><span data-stu-id="7a970-280">For the full list of filterable properties, navigate to [Filter requests by properties][DevtoolsReferenceProperty].</span></span>  
    
1.  <span data-ttu-id="7a970-281">Effacer la **zone de** texte Filtrer de n’importe quel texte.</span><span class="sxs-lookup"><span data-stu-id="7a970-281">Clear the **Filter** text box of any text.</span></span>  
    
### <a name="filter-by-resource-type"></a><span data-ttu-id="7a970-282">Filtrer par type de ressource</span><span class="sxs-lookup"><span data-stu-id="7a970-282">Filter by resource type</span></span>  

<span data-ttu-id="7a970-283">Pour vous concentrer sur un certain type de fichier, comme les feuilles de style :</span><span class="sxs-lookup"><span data-stu-id="7a970-283">To focus in on a certain type of file, such as stylesheets:</span></span>  

1.  <span data-ttu-id="7a970-284">Choisissez **CSS**.</span><span class="sxs-lookup"><span data-stu-id="7a970-284">Choose **CSS**.</span></span>  <span data-ttu-id="7a970-285">Tous les autres types de fichiers sont filtrés.</span><span class="sxs-lookup"><span data-stu-id="7a970-285">All other file types are filtered out.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css.msft.png" alt-text="Afficher uniquement les fichiers CSS" lightbox="../media/network-glitch-network-filter-file-type-css.msft.png":::
       <span data-ttu-id="7a970-287">Afficher uniquement les fichiers CSS</span><span class="sxs-lookup"><span data-stu-id="7a970-287">Show CSS files only</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="7a970-288">Pour afficher également des scripts, sélectionnez et maintenez `Control` \(Windows, Linux\) ou `Command` \(macOS\), puis choisissez **JS**.</span><span class="sxs-lookup"><span data-stu-id="7a970-288">To also display scripts, select and hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and then choose **JS**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css-js.msft.png" alt-text="Afficher uniquement les fichiers CSS et JS" lightbox="../media/network-glitch-network-filter-file-type-css-js.msft.png":::
       <span data-ttu-id="7a970-290">Afficher uniquement les fichiers CSS et JS</span><span class="sxs-lookup"><span data-stu-id="7a970-290">Show CSS and JS files only</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="7a970-291">Pour supprimer les filtres et afficher à nouveau toutes les ressources, choisissez **Tout**.</span><span class="sxs-lookup"><span data-stu-id="7a970-291">To remove the filters and display all resources again, choose **All**.</span></span>  
    
<span data-ttu-id="7a970-292">Pour les autres flux de travail de filtrage, accédez à [Filtrer les demandes.][DevtoolsNetworkReferenceFilter]</span><span class="sxs-lookup"><span data-stu-id="7a970-292">For other filtering workflows, navigate to [Filter requests][DevtoolsNetworkReferenceFilter].</span></span>  

## <a name="block-requests"></a><span data-ttu-id="7a970-293">Bloquer les demandes</span><span class="sxs-lookup"><span data-stu-id="7a970-293">Block requests</span></span>  

<span data-ttu-id="7a970-294">Comment se comporte une page lorsque certaines ressources de page ne sont pas disponibles ?</span><span class="sxs-lookup"><span data-stu-id="7a970-294">How does a page look and behave when some of the page resources are not available?</span></span>  <span data-ttu-id="7a970-295">Échoue-t-elle complètement ou est-elle encore quelque peu fonctionnelle ?</span><span class="sxs-lookup"><span data-stu-id="7a970-295">Does it fail completely, or is it still somewhat functional?</span></span>  <span data-ttu-id="7a970-296">Bloquer les demandes pour savoir :</span><span class="sxs-lookup"><span data-stu-id="7a970-296">Block requests to find out:</span></span>  

1.  <span data-ttu-id="7a970-297">Sélectionnez `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\) pour ouvrir le **menu Commande.**</span><span class="sxs-lookup"><span data-stu-id="7a970-297">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-cli-empty.msft.png" alt-text="Menu Commande" lightbox="../media/network-glitch-network-cli-empty.msft.png":::
       <span data-ttu-id="7a970-299">Menu **Commande**</span><span class="sxs-lookup"><span data-stu-id="7a970-299">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="7a970-300">Tapez `block` , choisissez Afficher le blocage **des**demandes, puis sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="7a970-300">Type `block`, choose **Show Request Blocking**, and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block.msft.png" alt-text="Afficher le blocage des demandes" lightbox="../media/network-glitch-network-cli-block.msft.png":::
       **<span data-ttu-id="7a970-302">Afficher le blocage des demandes</span><span class="sxs-lookup"><span data-stu-id="7a970-302">Show Request Blocking</span></span>**  
    :::image-end:::  
    
1.  <span data-ttu-id="7a970-303">Choose **Add Pattern** \( Add Pattern ![ ](../media/add-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="7a970-303">Choose **Add Pattern** \(![Add Pattern](../media/add-icon.msft.png)\).</span></span>  
1.  <span data-ttu-id="7a970-304">Tapez `main.css`.</span><span class="sxs-lookup"><span data-stu-id="7a970-304">Type `main.css`.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-add-pattern.msft.png" alt-text="Blocage de main.css" lightbox="../media/network-glitch-network-cli-block-add-pattern.msft.png":::
       <span data-ttu-id="7a970-306">Blocage</span><span class="sxs-lookup"><span data-stu-id="7a970-306">Blocking</span></span> `main.css`  
    :::image-end:::  
    
1.  <span data-ttu-id="7a970-307">Choose **Add**.</span><span class="sxs-lookup"><span data-stu-id="7a970-307">Choose **Add**.</span></span>  
1.  <span data-ttu-id="7a970-308">Actualisez la page.</span><span class="sxs-lookup"><span data-stu-id="7a970-308">Refresh the page.</span></span>  <span data-ttu-id="7a970-309">Comme prévu, le style de la page est légèrement décoché car la feuille de style principale a été bloquée.</span><span class="sxs-lookup"><span data-stu-id="7a970-309">As expected, the styling of the page is slightly messed up because the main stylesheet has been blocked.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="7a970-310">Ligne `main.css` du journal réseau.</span><span class="sxs-lookup"><span data-stu-id="7a970-310">The `main.css` row in the Network Log.</span></span>  <span data-ttu-id="7a970-311">Le texte rouge signifie que la ressource a été bloquée.</span><span class="sxs-lookup"><span data-stu-id="7a970-311">The red text means that the resource was blocked.</span></span>
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-main-css.msft.png" alt-text="main.css a été bloqué" lightbox="../media/network-glitch-network-cli-block-main-css.msft.png":::
       `main.css` <span data-ttu-id="7a970-313">a été bloqué</span><span class="sxs-lookup"><span data-stu-id="7a970-313">has been blocked</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="7a970-314">Désélection de la **case à cocher Activer le blocage des** demandes.</span><span class="sxs-lookup"><span data-stu-id="7a970-314">Deselect the **Enable request blocking** checkbox.</span></span>  

## <a name="conclusion"></a><span data-ttu-id="7a970-315">Conclusion</span><span class="sxs-lookup"><span data-stu-id="7a970-315">Conclusion</span></span>  

<span data-ttu-id="7a970-316">Félicitations, vous avez terminé le didacticiel.</span><span class="sxs-lookup"><span data-stu-id="7a970-316">Congratulations, you have completed the tutorial.</span></span>  <span data-ttu-id="7a970-317">Vous savez maintenant comment utiliser **l’outil** Réseau dans Microsoft Edge DevTools !</span><span class="sxs-lookup"><span data-stu-id="7a970-317">You now know how to use the **Network** tool in the Microsoft Edge DevTools!</span></span>

<span data-ttu-id="7a970-318">Accédez à la [référence réseau][DevtoolsNetworkReference] pour découvrir d’autres fonctionnalités DevTools liées à l’inspection de l’activité réseau.</span><span class="sxs-lookup"><span data-stu-id="7a970-318">Navigate to the [Network Reference][DevtoolsNetworkReference] to discover more DevTools features related to inspecting network activity.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="7a970-319">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="7a970-319">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

<!--[CachePolicies]: ../../../web/tools/lighthouse/audits/cache-policy ""  -->  

[DevToolsCustomizePlacement]: ../customize/placement.md "Modifier Microsoft Edge placement de DevTools | Documents Microsoft"  
[DevtoolsNetworkReference]: ./reference.md "Référence de l’analyse réseau | Documents Microsoft"
[DevtoolsNetworkReferenceFilter]: ./reference.md#filter-requests "Demandes de filtrage : référence de l’analyse réseau | Documents Microsoft"  
[DevtoolsReferenceHideOverview]: ./reference.md#hide-the-overview-pane "Masquer le volet Vue d’ensemble - Référence de l’analyse réseau | Documents Microsoft"
[DevtoolsReferenceProperty]: ./reference.md#filter-requests-by-properties "Filtrer les demandes par propriétés : référence de l’analyse réseau | Documents Microsoft"
[DevToolsOpen]: ../open/index.md "Ouvrez Microsoft Edge devTools | Documents Microsoft"  
[DevtoolsSpeedGetStarted]: ../speed/get-started.md "Optimiser la vitesse du site web avec Microsoft Edge devTools | Documents Microsoft"  

[GlitchNetworkGetStarted]: https://microsoft-edge-chromium-devtools.glitch.me/static/network/getstarted.html "Inspecter la démonstration de l’activité | Glitch"  

[MDNHTTPCache]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Mise en cache HTTP | MDN"  

> [!NOTE]
> <span data-ttu-id="7a970-329">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7a970-329">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="7a970-330">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/network/index) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="7a970-330">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="7a970-332">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7a970-332">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
