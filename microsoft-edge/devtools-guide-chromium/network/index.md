---
description: Didacticiel sur les fonctionnalités les plus populaires relatives au réseau dans Microsoft Edge DevTools.
title: Examiner l’activité réseau dans Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 3629c2d3711716d6d4a837b29bffef4786eb6d3f
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993449"
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





# <span data-ttu-id="f77a2-104">Examiner l’activité réseau dans Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="f77a2-104">Inspect network activity in Microsoft Edge DevTools</span></span>   



<span data-ttu-id="f77a2-105">Il s’agit d’un didacticiel d’utilisation des fonctionnalités DevTools les plus fréquemment utilisées associées à l’inspection de l’activité réseau d’une page.</span><span class="sxs-lookup"><span data-stu-id="f77a2-105">This is a hands-on tutorial of some of the most commonly-used DevTools features related to inspecting network activity for a page.</span></span>  

<span data-ttu-id="f77a2-106">Pour parcourir les fonctionnalités, voir [référence réseau][DevtoolsNetworkReference] .</span><span class="sxs-lookup"><span data-stu-id="f77a2-106">See [Network Reference][DevtoolsNetworkReference] if you want to browse features instead.</span></span>  

<!--TODO: This entire section needs a Microsoft Edge DevTools re-write  -->

<!-- Read on, or watch the video version of this tutorial:  -->  

<!--
> [!VIDEO embed/e1gAyQuIFQo]  
-->

## <span data-ttu-id="f77a2-107">Quand utiliser le panneau réseau</span><span class="sxs-lookup"><span data-stu-id="f77a2-107">When to use the Network panel</span></span>   

<span data-ttu-id="f77a2-108">En règle générale, utilisez le panneau réseau pour vous assurer que les ressources sont téléchargées ou chargées comme prévu.</span><span class="sxs-lookup"><span data-stu-id="f77a2-108">In general, use the Network panel when you need to make sure that resources are being downloaded or uploaded as expected.</span></span>  <span data-ttu-id="f77a2-109">Les cas d’utilisation les plus courants du panneau réseau sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="f77a2-109">The most common use cases for the Network panel are:</span></span>  

*   <span data-ttu-id="f77a2-110">Vérifiez que les ressources sont en train d’être chargées ou téléchargées du tout.</span><span class="sxs-lookup"><span data-stu-id="f77a2-110">Making sure that resources are actually being uploaded or downloaded at all.</span></span>  
*   <span data-ttu-id="f77a2-111">Inspecter les propriétés d’une ressource individuelle, par exemple, les en-têtes HTTP, le contenu, la taille, etc.</span><span class="sxs-lookup"><span data-stu-id="f77a2-111">Inspecting the properties of an individual resource, such as the HTTP headers, content, size, and so on.</span></span>  
    
<span data-ttu-id="f77a2-112">Si vous cherchez à améliorer les performances de chargement de page, **ne démarrez pas** le panneau réseau.</span><span class="sxs-lookup"><span data-stu-id="f77a2-112">If you are looking for ways to improve page load performance, **do not** start with the Network panel.</span></span>  <span data-ttu-id="f77a2-113">Il existe de nombreux types de problèmes de performances de chargement qui ne sont pas liés à l’activité réseau.</span><span class="sxs-lookup"><span data-stu-id="f77a2-113">There are many types of load performance issues that are not related to network activity.</span></span>  <span data-ttu-id="f77a2-114">Commencez avec le panneau audits, car il vous donne des suggestions ciblées sur l’amélioration de votre page.</span><span class="sxs-lookup"><span data-stu-id="f77a2-114">Start with the Audits panel because it gives you targeted suggestions on how to improve your page.</span></span>  <span data-ttu-id="f77a2-115">Voir [optimiser la vitesse du site Web][DevtoolsSpeedGetStarted].</span><span class="sxs-lookup"><span data-stu-id="f77a2-115">See [Optimize Website Speed][DevtoolsSpeedGetStarted].</span></span>  

## <span data-ttu-id="f77a2-116">Ouvrir le panneau réseau</span><span class="sxs-lookup"><span data-stu-id="f77a2-116">Open the Network panel</span></span>   

<span data-ttu-id="f77a2-117">Pour tirer le meilleur parti de ce didacticiel, ouvrez la démonstration et testez les fonctionnalités de la page de démonstration.</span><span class="sxs-lookup"><span data-stu-id="f77a2-117">To get the most out of this tutorial, open up the demo and try out the features on the demo page.</span></span>  

1.  <span data-ttu-id="f77a2-118">Ouvrir la [démonstration commencer][GlitchNetworkGetStarted].</span><span class="sxs-lookup"><span data-stu-id="f77a2-118">Open the [Get Started Demo][GlitchNetworkGetStarted].</span></span>  
    
    :::image type="complex" source="../media/network-glitch-inspect-network-activity-demo.msft.png" alt-text="La démonstration" lightbox="../media/network-glitch-inspect-network-activity-demo.msft.png":::
       <span data-ttu-id="f77a2-120">La démonstration</span><span class="sxs-lookup"><span data-stu-id="f77a2-120">The demo</span></span>  
    :::image-end:::  
    
    <!--You may prefer to move the demo to a separate window.  -->  
    
    <!--
    :::image type="complex" source="../media/network-tutorial/windows.msft.png" alt-text="The demo in one window and this tutorial in a different window" lightbox="../media/network-tutorial/windows.msft.png":::
       The demo in one window and this tutorial in a different window  
    :::image-end:::  
    -->
    
1.  <span data-ttu-id="f77a2-121">[Ouvrez devtools][DevToolsOpen] en appuyant sur `Control` + `Shift` + `J` \ (Windows \) ou `Command` + `Option` + `J` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="f77a2-121">[Open DevTools][DevToolsOpen] by pressing `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\).</span></span>  <span data-ttu-id="f77a2-122">Le panneau **console** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="f77a2-122">The **Console** panel opens.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-console.msft.png" alt-text="La console" lightbox="../media/network-glitch-console.msft.png":::
       <span data-ttu-id="f77a2-124">La **console**</span><span class="sxs-lookup"><span data-stu-id="f77a2-124">The **Console**</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="f77a2-125">Vous pouvez [ancrer devtools en bas de la fenêtre][DevToolsCustomizePlacement].</span><span class="sxs-lookup"><span data-stu-id="f77a2-125">You may prefer to [dock DevTools to the bottom of your window][DevToolsCustomizePlacement].</span></span>  
    
    :::image type="complex" source="../media/network-glitch-console-bottom.msft.png" alt-text="DevTools ancré en bas de la fenêtre" lightbox="../media/network-glitch-console-bottom.msft.png":::
       <span data-ttu-id="f77a2-127">DevTools ancré en bas de la fenêtre</span><span class="sxs-lookup"><span data-stu-id="f77a2-127">DevTools docked to the bottom of the window</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f77a2-128">Sélectionnez l’onglet **Network (réseau** ).  Le volet réseau s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="f77a2-128">Select the **Network** tab.  The Network panel opens.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-bottom.msft.png" alt-text="DevTools ancré en bas de la fenêtre" lightbox="../media/network-glitch-network-bottom.msft.png":::
       <span data-ttu-id="f77a2-130">DevTools ancré en bas de la fenêtre</span><span class="sxs-lookup"><span data-stu-id="f77a2-130">DevTools docked to the bottom of the window</span></span>  
    :::image-end:::  
    
<span data-ttu-id="f77a2-131">Pour le moment, le volet réseau est vide.</span><span class="sxs-lookup"><span data-stu-id="f77a2-131">Right now the Network panel is empty.</span></span>  <span data-ttu-id="f77a2-132">DevTools uniquement les journaux d’activité réseau après l’ouverture et aucune activité réseau ne s’est produite depuis que vous avez ouvert DevTools.</span><span class="sxs-lookup"><span data-stu-id="f77a2-132">DevTools only logs network activity after you open it and no network activity has occurred since you opened DevTools.</span></span>  

## <span data-ttu-id="f77a2-133">Journalisation de l’activité du réseau</span><span class="sxs-lookup"><span data-stu-id="f77a2-133">Log network activity</span></span>   

<span data-ttu-id="f77a2-134">Pour afficher l’activité réseau provoquée par une page:</span><span class="sxs-lookup"><span data-stu-id="f77a2-134">To view the network activity that a page causes:</span></span>  

1.  <span data-ttu-id="f77a2-135">Rechargez la page.</span><span class="sxs-lookup"><span data-stu-id="f77a2-135">Reload the page.</span></span>  <span data-ttu-id="f77a2-136">Le panneau réseau enregistre toutes les activités du réseau dans le **Journal du réseau**.</span><span class="sxs-lookup"><span data-stu-id="f77a2-136">The Network panel logs all network activity in the **Network Log**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network.msft.png" alt-text="Journal du réseau" lightbox="../media/network-glitch-network.msft.png":::
       <span data-ttu-id="f77a2-138">**Journal du réseau**</span><span class="sxs-lookup"><span data-stu-id="f77a2-138">The **Network Log**</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="f77a2-139">Chaque ligne du **Journal réseau** représente une ressource.</span><span class="sxs-lookup"><span data-stu-id="f77a2-139">Each row of the **Network Log** represents a resource.</span></span>  <span data-ttu-id="f77a2-140">Par défaut, les ressources sont répertoriées dans l’ordre chronologique.</span><span class="sxs-lookup"><span data-stu-id="f77a2-140">By default the resources are listed chronologically.</span></span>  <span data-ttu-id="f77a2-141">La principale ressource correspond généralement au document HTML principal.</span><span class="sxs-lookup"><span data-stu-id="f77a2-141">The top resource is usually the main HTML document.</span></span>  <span data-ttu-id="f77a2-142">Le dernier élément de la ressource est le dernier demandé.</span><span class="sxs-lookup"><span data-stu-id="f77a2-142">The bottom resource is whatever was requested last.</span></span>  
    
    <span data-ttu-id="f77a2-143">Chaque colonne représente des informations sur une ressource.</span><span class="sxs-lookup"><span data-stu-id="f77a2-143">Each column represents information about a resource.</span></span>  <span data-ttu-id="f77a2-144">Dans la figure précédente, les colonnes par défaut sont affichées.</span><span class="sxs-lookup"><span data-stu-id="f77a2-144">In the previous figure the default columns are displayed.</span></span>  

    *   <span data-ttu-id="f77a2-145">**Status**.</span><span class="sxs-lookup"><span data-stu-id="f77a2-145">**Status**.</span></span>  <span data-ttu-id="f77a2-146">Code d’état HTTP de la réponse.</span><span class="sxs-lookup"><span data-stu-id="f77a2-146">The HTTP status code for response.</span></span>  
    *   <span data-ttu-id="f77a2-147">**Type**.</span><span class="sxs-lookup"><span data-stu-id="f77a2-147">**Type**.</span></span>  <span data-ttu-id="f77a2-148">Type de ressource.</span><span class="sxs-lookup"><span data-stu-id="f77a2-148">The resource type.</span></span>  
    *   <span data-ttu-id="f77a2-149">**Initiator**.</span><span class="sxs-lookup"><span data-stu-id="f77a2-149">**Initiator**.</span></span>  <span data-ttu-id="f77a2-150">La cause de la demande de ressource.</span><span class="sxs-lookup"><span data-stu-id="f77a2-150">The cause of the resource request.</span></span>  <span data-ttu-id="f77a2-151">La sélection d’un lien dans la colonne initiateur vous permet d’accéder au code source à l’origine de la demande.</span><span class="sxs-lookup"><span data-stu-id="f77a2-151">Selecting a link in the Initiator column takes you to the source code that caused the request.</span></span>  
    *   <span data-ttu-id="f77a2-152">**Temps**.</span><span class="sxs-lookup"><span data-stu-id="f77a2-152">**Time**.</span></span>  <span data-ttu-id="f77a2-153">Durée de la requête.</span><span class="sxs-lookup"><span data-stu-id="f77a2-153">The duration of the request.</span></span>  
    *   <span data-ttu-id="f77a2-154">En **cascade**.</span><span class="sxs-lookup"><span data-stu-id="f77a2-154">**Waterfall**.</span></span>  <span data-ttu-id="f77a2-155">Représentation graphique des différentes étapes de la requête.</span><span class="sxs-lookup"><span data-stu-id="f77a2-155">A graphical representation of the different stages of the request.</span></span>  <span data-ttu-id="f77a2-156">Placez le pointeur de la souris sur une cascade pour afficher une répartition.</span><span class="sxs-lookup"><span data-stu-id="f77a2-156">Hover over a Waterfall to see a breakdown.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="f77a2-157">Le graphique au-dessus du journal réseau est appelé vue d’ensemble.</span><span class="sxs-lookup"><span data-stu-id="f77a2-157">The graph above the Network Log is called the Overview.</span></span>  <span data-ttu-id="f77a2-158">Dans ce didacticiel, vous n’utiliserez pas le graphique de vue d’ensemble et vous pouvez le masquer.</span><span class="sxs-lookup"><span data-stu-id="f77a2-158">You will not use the Overview graph in this tutorial, so you may hide it.</span></span>  <span data-ttu-id="f77a2-159">Voir [masquer le volet vue d’ensemble][DevtoolsReferenceHideOverview].</span><span class="sxs-lookup"><span data-stu-id="f77a2-159">See [Hide the Overview pane][DevtoolsReferenceHideOverview].</span></span>
    
1.  <span data-ttu-id="f77a2-160">Après l’ouverture de DevTools, elle enregistre l’activité réseau dans le journal du réseau.</span><span class="sxs-lookup"><span data-stu-id="f77a2-160">After you open DevTools, it records network activity in the Network Log.</span></span>  
    <span data-ttu-id="f77a2-161">Pour en expliquer le résultat, observez d’abord la partie inférieure du **Journal du réseau** et prenez note de la dernière activité.</span><span class="sxs-lookup"><span data-stu-id="f77a2-161">To demonstrate this, first look at the bottom of the **Network Log** and make a mental note of the last activity.</span></span>  
1.  <span data-ttu-id="f77a2-162">À présent, sélectionnez le bouton **obtenir des données** dans la démonstration.</span><span class="sxs-lookup"><span data-stu-id="f77a2-162">Now, select the **Get Data** button in the demo.</span></span>  
1.  <span data-ttu-id="f77a2-163">Regardez de nouveau le journal du **réseau** .</span><span class="sxs-lookup"><span data-stu-id="f77a2-163">Look at the bottom of the **Network Log** again.</span></span>  <span data-ttu-id="f77a2-164">Une nouvelle ressource doit apparaître `getstarted.json` .</span><span class="sxs-lookup"><span data-stu-id="f77a2-164">You should see a new resource called `getstarted.json`.</span></span>  <span data-ttu-id="f77a2-165">Le fait de sélectionner le bouton **Get Data** a entraîné la demande de ce fichier.</span><span class="sxs-lookup"><span data-stu-id="f77a2-165">Selecting the **Get Data** button caused the page to request this file.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-new-resource.msft.png" alt-text="Nouvelle ressource dans le journal réseau" lightbox="../media/network-glitch-network-new-resource.msft.png":::
       <span data-ttu-id="f77a2-167">Nouvelle ressource dans le **Journal réseau**</span><span class="sxs-lookup"><span data-stu-id="f77a2-167">A new resource in the **Network Log**</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="f77a2-168">Afficher plus d’informations</span><span class="sxs-lookup"><span data-stu-id="f77a2-168">Show more information</span></span>   

<span data-ttu-id="f77a2-169">Les colonnes du journal du réseau peuvent être configurées.</span><span class="sxs-lookup"><span data-stu-id="f77a2-169">The columns of the Network Log are configurable.</span></span>  <span data-ttu-id="f77a2-170">Vous pouvez masquer les colonnes que vous n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="f77a2-170">You may hide columns that you are not using.</span></span>  
<span data-ttu-id="f77a2-171">Il existe également plusieurs colonnes qui sont masquées par défaut, qui peuvent être utiles.</span><span class="sxs-lookup"><span data-stu-id="f77a2-171">There are also many columns that are hidden by default which you may find useful.</span></span>  

1.  <span data-ttu-id="f77a2-172">Cliquez avec le bouton droit sur l’en-tête de la table Journal du réseau et sélectionnez **Domain (domaine**).</span><span class="sxs-lookup"><span data-stu-id="f77a2-172">Right-click the header of the Network Log table and select **Domain**.</span></span>  <span data-ttu-id="f77a2-173">Le domaine de chaque ressource est désormais affiché.</span><span class="sxs-lookup"><span data-stu-id="f77a2-173">The domain of each resource is now shown.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-edit-column.msft.png" alt-text="Activez la colonne Domain (domaine)" lightbox="../media/network-glitch-network-edit-column.msft.png":::
       <span data-ttu-id="f77a2-175">Activez la colonne Domain (domaine)</span><span class="sxs-lookup"><span data-stu-id="f77a2-175">Enable the Domain column</span></span>  
    :::image-end:::  
    
    > [!TIP]
    > <span data-ttu-id="f77a2-176">Pour afficher l’URL complète d’une ressource, placez le pointeur de la souris sur la cellule de la colonne **nom** .</span><span class="sxs-lookup"><span data-stu-id="f77a2-176">See the full URL of a resource by hovering over the cell in the **Name** column.</span></span>  
    
## <span data-ttu-id="f77a2-177">Simuler une connexion réseau plus lente</span><span class="sxs-lookup"><span data-stu-id="f77a2-177">Simulate a slower network connection</span></span>   

<span data-ttu-id="f77a2-178">La connexion réseau de l’ordinateur que vous utilisez pour créer des sites est probablement plus rapide que les connexions réseau des appareils mobiles de vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="f77a2-178">The network connection of the computer that you use to build sites is probably faster than the network connections of the mobile devices of your users.</span></span>  <span data-ttu-id="f77a2-179">La limitation de la page vous permet d’obtenir une meilleure idée du temps nécessaire au chargement d’une page sur un appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="f77a2-179">By throttling the page, you get a better idea of how long a page takes to load on a mobile device.</span></span>  

1.  <span data-ttu-id="f77a2-180">Sélectionner la liste déroulante de **limitation** , définie sur **en ligne** par défaut.</span><span class="sxs-lookup"><span data-stu-id="f77a2-180">Select the **Throttling** dropdown, which is set to **Online** by default.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-throttling.msft.png" alt-text="Activer la limitation" lightbox="../media/network-glitch-network-throttling.msft.png":::
       <span data-ttu-id="f77a2-182">Activer la limitation</span><span class="sxs-lookup"><span data-stu-id="f77a2-182">Enable throttling</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f77a2-183">Sélectionnez **3G lente**.</span><span class="sxs-lookup"><span data-stu-id="f77a2-183">Select **Slow 3G**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-throttling-slow-3g.msft.png" alt-text="Sélectionnez 3G lente" lightbox="../media/network-glitch-network-throttling-slow-3g.msft.png":::
       <span data-ttu-id="f77a2-185">Sélectionnez 3G lente</span><span class="sxs-lookup"><span data-stu-id="f77a2-185">Select Slow 3G</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f77a2-186">Appuyez longuement sur **recharger** \ ( ![ recharger ][ImageRefreshIcon] \), puis sélectionnez Vider le **cache et rechargement**.</span><span class="sxs-lookup"><span data-stu-id="f77a2-186">Long-press **Reload** \(![Reload][ImageRefreshIcon]\) and then select **Empty Cache And Hard Reload**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-empty-cache-and-hard-reset.msft.png" alt-text="Vider le cache et procéder au recharge" lightbox="../media/network-glitch-empty-cache-and-hard-reset.msft.png":::
       **<span data-ttu-id="f77a2-188">Vider le cache et procéder au recharge</span><span class="sxs-lookup"><span data-stu-id="f77a2-188">Empty Cache And Hard Reload</span></span>**  
    :::image-end:::  
    
    <span data-ttu-id="f77a2-189">Lorsque vous révisez les visites, le navigateur fournit généralement certains fichiers du [cache][MDNHTTPCache], ce qui accélère le chargement de la page.</span><span class="sxs-lookup"><span data-stu-id="f77a2-189">On repeat visits, the browser usually serves some files from the [cache][MDNHTTPCache], which speeds up the page load.</span></span>  <span data-ttu-id="f77a2-190">Le **vidage du cache et du rechargement forcé** force le navigateur à accéder au réseau pour toutes les ressources.</span><span class="sxs-lookup"><span data-stu-id="f77a2-190">**Empty Cache And Hard Reload** forces the browser to go the network for all resources.</span></span>  <span data-ttu-id="f77a2-191">Cette méthode est utile lorsque vous souhaitez voir la façon dont un visiteur commence à se charger de la page.</span><span class="sxs-lookup"><span data-stu-id="f77a2-191">This is helpful when you want to see how a first-time visitor experiences a page load.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="f77a2-192">Le flux **de travail vider le cache et le chargement papier** est uniquement disponible lorsque devtools est ouvert.</span><span class="sxs-lookup"><span data-stu-id="f77a2-192">The **Empty Cache And Hard Reload** workflow is only available when DevTools is open.</span></span>  
    
## <span data-ttu-id="f77a2-193">Capture de captures d’écran</span><span class="sxs-lookup"><span data-stu-id="f77a2-193">Capture screenshots</span></span>   

<span data-ttu-id="f77a2-194">Les captures d’écran vous permettent de voir l’aspect d’une page au fil du temps pendant son chargement.</span><span class="sxs-lookup"><span data-stu-id="f77a2-194">Screenshots let you see how a page looked over time while it was loading.</span></span>  

1.  <span data-ttu-id="f77a2-195">Sélectionnez \ ( ![ paramètres réseau ][ImageSettingsIcon] \) et cochez la case capturer les captures d' **écran** .</span><span class="sxs-lookup"><span data-stu-id="f77a2-195">Select \(![Network settings][ImageSettingsIcon]\) and select the **Capture screenshots** checkbox.</span></span>
1.  <span data-ttu-id="f77a2-196">Rechargez de nouveau la page par le biais du flux **de travail vider le cache et le chargement papier** .</span><span class="sxs-lookup"><span data-stu-id="f77a2-196">Reload the page again via the **Empty Cache And Hard Reload** workflow.</span></span>  <span data-ttu-id="f77a2-197">Pour savoir comment procéder, voir [simuler une connexion plus lente](#simulate-a-slower-network-connection) si vous avez besoin d’un rappel.</span><span class="sxs-lookup"><span data-stu-id="f77a2-197">See [Simulate a slower connection](#simulate-a-slower-network-connection) if you need a reminder on how to do this.</span></span>  
    <span data-ttu-id="f77a2-198">Le volet capture d’écran fournit des miniatures illustrant la manière dont la page a été recherchée à différents points au cours du processus de chargement.</span><span class="sxs-lookup"><span data-stu-id="f77a2-198">The Screenshots pane provides thumbnails of how the page looked at various points during the loading process.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots.msft.png" alt-text="Captures d’écran du chargement de la page" lightbox="../media/network-glitch-network-screenshots.msft.png":::
       <span data-ttu-id="f77a2-200">Captures d’écran du chargement de la page</span><span class="sxs-lookup"><span data-stu-id="f77a2-200">Screenshots of the page load</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f77a2-201">Sélectionnez la première miniature.</span><span class="sxs-lookup"><span data-stu-id="f77a2-201">Select the first thumbnail.</span></span>  <span data-ttu-id="f77a2-202">DevTools indique l’activité réseau qui se produit à ce moment précis.</span><span class="sxs-lookup"><span data-stu-id="f77a2-202">DevTools shows you what network activity was occurring at that moment in time.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots-first.msft.png" alt-text="Activité réseau qui se produit pendant la première capture d’écran" lightbox="../media/network-glitch-network-screenshots-first.msft.png":::
       <span data-ttu-id="f77a2-204">Activité réseau qui se produit pendant la première capture d’écran</span><span class="sxs-lookup"><span data-stu-id="f77a2-204">The network activity that was happening during the first screenshot</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f77a2-205">Sélectionnez de nouveau \ ( ![ paramètres réseau ][ImageSettingsIcon] \) et désélectionnez la case à cocher **capture** des captures d’écran pour fermer le volet captures d’écran.</span><span class="sxs-lookup"><span data-stu-id="f77a2-205">Select \(![Network settings][ImageSettingsIcon]\) again and deselect the **Capture screenshots** checkbox to close the Screenshots pane.</span></span>
1.  <span data-ttu-id="f77a2-206">Rechargez la page.</span><span class="sxs-lookup"><span data-stu-id="f77a2-206">Reload the page again.</span></span>  
    
## <span data-ttu-id="f77a2-207">Inspecter les détails de la ressource</span><span class="sxs-lookup"><span data-stu-id="f77a2-207">Inspect the details of the resource</span></span>   

<span data-ttu-id="f77a2-208">Pour plus d’informations à ce sujet, sélectionnez une ressource.</span><span class="sxs-lookup"><span data-stu-id="f77a2-208">Select a resource to learn more information about it.</span></span>  <span data-ttu-id="f77a2-209">Essayez-le maintenant:</span><span class="sxs-lookup"><span data-stu-id="f77a2-209">Try it now:</span></span>  

1.  <span data-ttu-id="f77a2-210">Sélectionnez `getstarted.html` .</span><span class="sxs-lookup"><span data-stu-id="f77a2-210">Select `getstarted.html`.</span></span>  <span data-ttu-id="f77a2-211">L’onglet **en-têtes** est affiché.</span><span class="sxs-lookup"><span data-stu-id="f77a2-211">The **Headers** tab is shown.</span></span>  <span data-ttu-id="f77a2-212">Utilisez cet onglet pour inspecter les en-têtes HTTP.</span><span class="sxs-lookup"><span data-stu-id="f77a2-212">Use this tab to inspect HTTP headers.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-headers.msft.png" alt-text="Onglet en-têtes" lightbox="../media/network-glitch-network-resources-headers.msft.png":::
       <span data-ttu-id="f77a2-214">Onglet **en-têtes**</span><span class="sxs-lookup"><span data-stu-id="f77a2-214">The **Headers** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f77a2-215">Sélectionnez l’onglet **Aperçu** .  Un rendu de base du code HTML est affiché.</span><span class="sxs-lookup"><span data-stu-id="f77a2-215">Select the **Preview** tab.  A basic rendering of the HTML is shown.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-preview.msft.png" alt-text="Onglet Aperçu" lightbox="../media/network-glitch-network-resources-preview.msft.png":::
       <span data-ttu-id="f77a2-217">Onglet **Aperçu**</span><span class="sxs-lookup"><span data-stu-id="f77a2-217">The **Preview** tab</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="f77a2-218">Cet onglet est utile lorsqu’une API renvoie un code d’erreur en HTML.</span><span class="sxs-lookup"><span data-stu-id="f77a2-218">This tab is helpful when an API returns an error code in HTML.</span></span>  <span data-ttu-id="f77a2-219">Il est possible que vous puissiez lire le code HTML affiché plus facilement que le code source HTML ou lorsque vous examinez des images.</span><span class="sxs-lookup"><span data-stu-id="f77a2-219">You may find it easier to read the rendered HTML than the HTML source code, or when you inspect images.</span></span>  

1.  <span data-ttu-id="f77a2-220">Sélectionnez l’onglet **réponse** .  Le code source HTML est affiché.</span><span class="sxs-lookup"><span data-stu-id="f77a2-220">Select the **Response** tab.  The HTML source code is shown.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-response.msft.png" alt-text="Onglet réponse" lightbox="../media/network-glitch-network-resources-response.msft.png":::
       <span data-ttu-id="f77a2-222">Onglet **réponse**</span><span class="sxs-lookup"><span data-stu-id="f77a2-222">The **Response** tab</span></span>  
    :::image-end:::  
    
    > [!TIP]
    > <span data-ttu-id="f77a2-223">Lorsqu’un fichier est minified, le fait de sélectionner le bouton **mettre** en forme \ ( ![ format ][ImageFormatIcon] \) en bas de l’onglet **réponse** a reformaté le contenu du fichier pour faciliter la lecture.</span><span class="sxs-lookup"><span data-stu-id="f77a2-223">When a file is minified, selecting the **Format** \(![Format][ImageFormatIcon]\) button at the bottom of the **Response** tab re-formats the contents of the file for readability.</span></span>  
    
1.  <span data-ttu-id="f77a2-224">Sélectionnez l’onglet **minutage** .  Le détail de l’activité réseau de cette ressource est affiché.</span><span class="sxs-lookup"><span data-stu-id="f77a2-224">Select the **Timing** tab.  A breakdown of the network activity for this resource is shown.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-timing.msft.png" alt-text="Onglet Minutage" lightbox="../media/network-glitch-network-resources-timing.msft.png":::
       <span data-ttu-id="f77a2-226">Onglet **minutage**</span><span class="sxs-lookup"><span data-stu-id="f77a2-226">The **Timing** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f77a2-227">Sélectionnez **Close** ( ![ fermer ][ImageCloseIcon] ) pour afficher de nouveau le journal du réseau.</span><span class="sxs-lookup"><span data-stu-id="f77a2-227">Select **Close** \(![Close][ImageCloseIcon]\) to view the Network Log again.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-close-tabs.msft.png" alt-text="Bouton Fermer" lightbox="../media/network-glitch-network-resources-close-tabs.msft.png":::
       <span data-ttu-id="f77a2-229">Bouton **Fermer**</span><span class="sxs-lookup"><span data-stu-id="f77a2-229">The **Close** button</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="f77a2-230">Effectuer une recherche dans les en-têtes et réponses du réseau</span><span class="sxs-lookup"><span data-stu-id="f77a2-230">Search network headers and responses</span></span>   

<span data-ttu-id="f77a2-231">Le volet de **recherche** vous permet d’effectuer une recherche dans les en-têtes et réponses HTTP de toutes les ressources pour une chaîne ou une expression régulière spécifique.</span><span class="sxs-lookup"><span data-stu-id="f77a2-231">Use the **Search** pane when you need to search the HTTP headers and responses of all resources for a certain string or regular expression.</span></span>  

<span data-ttu-id="f77a2-232">Par exemple, supposons que vous vouliez vérifier que vos ressources utilisent des **stratégies de cache**raisonnables.</span><span class="sxs-lookup"><span data-stu-id="f77a2-232">For example, suppose you want to verify that your resources are using reasonable **cache policies**.</span></span>  

<!--TODO: add cache policies section when available  -->

1.  <span data-ttu-id="f77a2-233">Sélectionnez **Rechercher** \ ( ![ Rechercher ][ImageSearchIcon] \).</span><span class="sxs-lookup"><span data-stu-id="f77a2-233">Select **Search** \(![Search][ImageSearchIcon]\).</span></span>  <span data-ttu-id="f77a2-234">Le volet de recherche s’ouvre à gauche du journal du réseau.</span><span class="sxs-lookup"><span data-stu-id="f77a2-234">The Search pane opens to the left of the Network log.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-empty.msft.png" alt-text="Le volet de recherche" lightbox="../media/network-glitch-network-search-empty.msft.png":::
       <span data-ttu-id="f77a2-236">Le volet de **recherche**</span><span class="sxs-lookup"><span data-stu-id="f77a2-236">The **Search** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f77a2-237">Tapez `Cache-Control` et appuyez sur `Enter` .</span><span class="sxs-lookup"><span data-stu-id="f77a2-237">Type `Cache-Control` and press `Enter`.</span></span>  <span data-ttu-id="f77a2-238">Le volet de recherche répertorie toutes les instances `Cache-Control` qu’il recherche dans les en-têtes de ressources ou le contenu.</span><span class="sxs-lookup"><span data-stu-id="f77a2-238">The Search pane lists all instances of `Cache-Control` that it finds in resource headers or content.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control.msft.png" alt-text="Résultats de la recherche pour le contrôle du cache" lightbox="../media/network-glitch-network-search-cache-control.msft.png":::
       <span data-ttu-id="f77a2-240">Résultats de la recherche pour </span><span class="sxs-lookup"><span data-stu-id="f77a2-240">Search results for</span></span> `Cache-Control`  
    :::image-end:::  
    
1.  <span data-ttu-id="f77a2-241">Sélectionnez un résultat pour afficher la ressource dans laquelle le résultat a été trouvé.</span><span class="sxs-lookup"><span data-stu-id="f77a2-241">Select a result to view the resource in which the result was found.</span></span>  <span data-ttu-id="f77a2-242">Si vous examinez les détails de la ressource, sélectionnez un résultat pour y accéder directement.</span><span class="sxs-lookup"><span data-stu-id="f77a2-242">If you are looking at the details of the resource, select a result to go directly to it.</span></span>  <span data-ttu-id="f77a2-243">Par exemple, si la requête se trouve dans un en-tête, l’onglet en-têtes s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="f77a2-243">For example, if the query was found in a header, the Headers tab opens.</span></span>   <span data-ttu-id="f77a2-244">Si la requête se trouve dans le contenu, l’onglet **réponse** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="f77a2-244">If the query was found in content, the **Response** tab opens.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png" alt-text="Résultat de la recherche en surbrillance dans l’onglet en-têtes" lightbox="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png":::
       <span data-ttu-id="f77a2-246">Résultat de la recherche en surbrillance dans l’onglet **en-têtes**</span><span class="sxs-lookup"><span data-stu-id="f77a2-246">A search result highlighted in the **Headers** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f77a2-247">Fermez le volet de recherche et l’onglet en-têtes.</span><span class="sxs-lookup"><span data-stu-id="f77a2-247">Close the Search pane and the Headers tab.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-close.msft.png" alt-text="Boutons Fermer" lightbox="../media/network-glitch-network-search-close.msft.png":::
       <span data-ttu-id="f77a2-249">Boutons **Fermer**</span><span class="sxs-lookup"><span data-stu-id="f77a2-249">The **Close** buttons</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="f77a2-250">Filtrer les ressources</span><span class="sxs-lookup"><span data-stu-id="f77a2-250">Filter resources</span></span>   

<span data-ttu-id="f77a2-251">DevTools fournit de nombreux flux de travail pour filtrer les ressources qui ne sont pas pertinentes pour la tâche en cours.</span><span class="sxs-lookup"><span data-stu-id="f77a2-251">DevTools provides numerous workflows for filtering out resources that are not relevant to the task at hand.</span></span>  

:::image type="complex" source="../media/network-glitch-network-filter-empty.msft.png" alt-text="Barre d’outils filtres" lightbox="../media/network-glitch-network-filter-empty.msft.png":::
   <span data-ttu-id="f77a2-253">Barre d’outils **filtres**</span><span class="sxs-lookup"><span data-stu-id="f77a2-253">The **Filters** toolbar</span></span>  
:::image-end:::  

<span data-ttu-id="f77a2-254">Par défaut, la barre d’outils **filtres** doit être activée.</span><span class="sxs-lookup"><span data-stu-id="f77a2-254">The **Filters** toolbar should be enabled by default.</span></span>  <span data-ttu-id="f77a2-255">Si ce n’est pas le cas:</span><span class="sxs-lookup"><span data-stu-id="f77a2-255">If not:</span></span>  

1.  <span data-ttu-id="f77a2-256">Sélectionnez **Filtrer** \ ( ![ filtre ][ImageFilterIcon] \) pour l’afficher.</span><span class="sxs-lookup"><span data-stu-id="f77a2-256">Select **Filter** \(![Filter][ImageFilterIcon]\) to show it.</span></span>  
    
### <span data-ttu-id="f77a2-257">Filtrer par chaîne, expression régulière ou propriété</span><span class="sxs-lookup"><span data-stu-id="f77a2-257">Filter by string, regular expression, or property</span></span>   

<span data-ttu-id="f77a2-258">La zone de texte **filtre** prend en charge différents types de filtrage.</span><span class="sxs-lookup"><span data-stu-id="f77a2-258">The **Filter** text box supports many different types of filtering.</span></span>  

1.  <span data-ttu-id="f77a2-259">Entrez `png` dans la zone de texte du **filtre** .</span><span class="sxs-lookup"><span data-stu-id="f77a2-259">Type `png` into the **Filter** text box.</span></span>  <span data-ttu-id="f77a2-260">Seuls les fichiers qui contiennent le texte `png` sont affichés.</span><span class="sxs-lookup"><span data-stu-id="f77a2-260">Only the files that contain the text `png` are shown.</span></span>  <span data-ttu-id="f77a2-261">Dans ce cas, les seuls fichiers correspondant au filtre sont les images PNG.</span><span class="sxs-lookup"><span data-stu-id="f77a2-261">In this case the only files that match the filter are the PNG images.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-png.msft.png" alt-text="Filtre de chaîne" lightbox="../media/network-glitch-network-filter-png.msft.png":::
       <span data-ttu-id="f77a2-263">Filtre de chaîne</span><span class="sxs-lookup"><span data-stu-id="f77a2-263">A string filter</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f77a2-264">Entrez `/.*\.[cj]s+$/`.</span><span class="sxs-lookup"><span data-stu-id="f77a2-264">Type `/.*\.[cj]s+$/`.</span></span>  <span data-ttu-id="f77a2-265">DevTools filtre les ressources dont le nom ne se termine pas par un `j` ou après `c` suivi de 1 ou plusieurs `s` caractères.</span><span class="sxs-lookup"><span data-stu-id="f77a2-265">DevTools filters out any resource with a filename that does not end with a `j` or a `c` followed by 1 or more `s` characters.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-regex.msft.png" alt-text="Un filtre d’expression régulier" lightbox="../media/network-glitch-network-filter-regex.msft.png":::
       <span data-ttu-id="f77a2-267">Un filtre d’expression régulier</span><span class="sxs-lookup"><span data-stu-id="f77a2-267">A regular expression filter</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f77a2-268">Entrez `-main.css`.</span><span class="sxs-lookup"><span data-stu-id="f77a2-268">Type `-main.css`.</span></span>  <span data-ttu-id="f77a2-269">DevTools filtre `main.css` .</span><span class="sxs-lookup"><span data-stu-id="f77a2-269">DevTools filters out `main.css`.</span></span>  <span data-ttu-id="f77a2-270">Si un autre fichier correspond au modèle, il sera également filtré.</span><span class="sxs-lookup"><span data-stu-id="f77a2-270">If any other file matched the pattern they would also be filtered out.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-negative-statement.msft.png" alt-text="Un filtre négatif" lightbox="../media/network-glitch-network-filter-negative-statement.msft.png":::
       <span data-ttu-id="f77a2-272">Un filtre négatif</span><span class="sxs-lookup"><span data-stu-id="f77a2-272">A negative filter</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f77a2-273">Entrez `domain:cdn.glitch.com` dans la zone de texte du **filtre** .</span><span class="sxs-lookup"><span data-stu-id="f77a2-273">Type `domain:cdn.glitch.com` into the **Filter** text box.</span></span>  <span data-ttu-id="f77a2-274">DevTools filtre les ressources disposant d’une URL qui ne correspond pas à ce domaine.</span><span class="sxs-lookup"><span data-stu-id="f77a2-274">DevTools filters out any resource with a URL that does not match this domain.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-property-value.msft.png" alt-text="Filtre de propriétés" lightbox="../media/network-glitch-network-filter-property-value.msft.png":::
       <span data-ttu-id="f77a2-276">Filtre de propriétés</span><span class="sxs-lookup"><span data-stu-id="f77a2-276">A property filter</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="f77a2-277">Pour obtenir la liste complète des propriétés filtrées [, voir filtrer les demandes par propriétés][DevtoolsReferenceProperty] .</span><span class="sxs-lookup"><span data-stu-id="f77a2-277">See [Filter requests by properties][DevtoolsReferenceProperty] for the full list of filterable properties.</span></span>  
    
1.  <span data-ttu-id="f77a2-278">Effacez la zone de texte du **filtre** d’un texte.</span><span class="sxs-lookup"><span data-stu-id="f77a2-278">Clear the **Filter** text box of any text.</span></span>  
    
### <span data-ttu-id="f77a2-279">Filtrer par type de ressource</span><span class="sxs-lookup"><span data-stu-id="f77a2-279">Filter by resource type</span></span>   

<span data-ttu-id="f77a2-280">Pour vous concentrer sur un certain type de fichier, tel que les feuilles de style:</span><span class="sxs-lookup"><span data-stu-id="f77a2-280">To focus in on a certain type of file, such as stylesheets:</span></span>  

1.  <span data-ttu-id="f77a2-281">Sélectionnez **CSS**.</span><span class="sxs-lookup"><span data-stu-id="f77a2-281">Select **CSS**.</span></span>  <span data-ttu-id="f77a2-282">Tous les autres types de fichiers sont filtrés.</span><span class="sxs-lookup"><span data-stu-id="f77a2-282">All other file types are filtered out.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css.msft.png" alt-text="Afficher les fichiers CSS uniquement" lightbox="../media/network-glitch-network-filter-file-type-css.msft.png":::
       <span data-ttu-id="f77a2-284">Afficher les fichiers CSS uniquement</span><span class="sxs-lookup"><span data-stu-id="f77a2-284">Show CSS files only</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f77a2-285">Pour afficher les scripts, vous pouvez également appuyer sur `Control` \ (Windows \) ou `Command` \ (MacOS \), puis sélectionner **js**.</span><span class="sxs-lookup"><span data-stu-id="f77a2-285">To also see scripts, hold `Control` \(Windows\) or `Command` \(macOS\) and then select **JS**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css-js.msft.png" alt-text="Afficher les fichiers CSS et JS uniquement" lightbox="../media/network-glitch-network-filter-file-type-css-js.msft.png":::
       <span data-ttu-id="f77a2-287">Afficher les fichiers CSS et JS uniquement</span><span class="sxs-lookup"><span data-stu-id="f77a2-287">Show CSS and JS files only</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f77a2-288">**Tout** sélectionner pour supprimer les filtres et afficher de nouveau toutes les ressources.</span><span class="sxs-lookup"><span data-stu-id="f77a2-288">Select **All** to remove the filters and see all resources again.</span></span>  
    
<span data-ttu-id="f77a2-289">Pour plus d’autres flux de travail de filtrage, voir [Filtrer les demandes][DevtoolsNetworkReferenceFilter] .</span><span class="sxs-lookup"><span data-stu-id="f77a2-289">See [Filter requests][DevtoolsNetworkReferenceFilter] for other filtering workflows.</span></span>  

## <span data-ttu-id="f77a2-290">Bloquer les demandes</span><span class="sxs-lookup"><span data-stu-id="f77a2-290">Block requests</span></span>   

<span data-ttu-id="f77a2-291">Quel est l’aspect et le comportement d’une page lorsque certaines ressources de la page ne sont pas disponibles?</span><span class="sxs-lookup"><span data-stu-id="f77a2-291">How does a page look and behave when some of the page resources are not available?</span></span>  <span data-ttu-id="f77a2-292">Est-ce que l’opération échoue entièrement ou fonctionne-t-elle toujours?</span><span class="sxs-lookup"><span data-stu-id="f77a2-292">Does it fail completely, or is it still somewhat functional?</span></span>  <span data-ttu-id="f77a2-293">Bloquer les requêtes à Rechercher:</span><span class="sxs-lookup"><span data-stu-id="f77a2-293">Block requests to find out:</span></span>  

1.  <span data-ttu-id="f77a2-294">Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le **menu de commandes**.</span><span class="sxs-lookup"><span data-stu-id="f77a2-294">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-cli-empty.msft.png" alt-text="Menu de commandes" lightbox="../media/network-glitch-network-cli-empty.msft.png":::
       <span data-ttu-id="f77a2-296">**Menu de commandes**</span><span class="sxs-lookup"><span data-stu-id="f77a2-296">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f77a2-297">Tapez `block` , sélectionnez **afficher le blocage de requête**, puis appuyez sur `Enter` .</span><span class="sxs-lookup"><span data-stu-id="f77a2-297">Type `block`, select **Show Request Blocking**, and press `Enter`.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block.msft.png" alt-text="Afficher le blocage de requête" lightbox="../media/network-glitch-network-cli-block.msft.png":::
       **<span data-ttu-id="f77a2-299">Afficher le blocage de requête</span><span class="sxs-lookup"><span data-stu-id="f77a2-299">Show Request Blocking</span></span>**  
    :::image-end:::  
    
1.  <span data-ttu-id="f77a2-300">Sélectionnez **Ajouter un modèle** \ ( ![ Ajouter le modèle ][ImageAddIcon] \).</span><span class="sxs-lookup"><span data-stu-id="f77a2-300">Select **Add Pattern** \(![Add Pattern][ImageAddIcon]\).</span></span>  
1.  <span data-ttu-id="f77a2-301">Entrez `main.css`.</span><span class="sxs-lookup"><span data-stu-id="f77a2-301">Type `main.css`.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-add-pattern.msft.png" alt-text="Blocage de main. CSS" lightbox="../media/network-glitch-network-cli-block-add-pattern.msft.png":::
       <span data-ttu-id="f77a2-303">Bloquer</span><span class="sxs-lookup"><span data-stu-id="f77a2-303">Blocking</span></span> `main.css`  
    :::image-end:::  
    
1.  <span data-ttu-id="f77a2-304">Cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="f77a2-304">Select **Add**.</span></span>  
1.  <span data-ttu-id="f77a2-305">Rechargez la page.</span><span class="sxs-lookup"><span data-stu-id="f77a2-305">Reload the page.</span></span>  <span data-ttu-id="f77a2-306">Comme prévu, le style de la page est légèrement gâché, car la feuille de style principale a été bloquée.</span><span class="sxs-lookup"><span data-stu-id="f77a2-306">As expected, the styling of the page is slightly messed up because the main stylesheet has been blocked.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="f77a2-307">`main.css`Ligne du journal du réseau.</span><span class="sxs-lookup"><span data-stu-id="f77a2-307">The `main.css` row in the Network Log.</span></span>  <span data-ttu-id="f77a2-308">Le texte rouge signifie que la ressource a été bloquée.</span><span class="sxs-lookup"><span data-stu-id="f77a2-308">The red text means that the resource was blocked.</span></span>
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-main-css.msft.png" alt-text="main. CSS a été bloqué" lightbox="../media/network-glitch-network-cli-block-main-css.msft.png":::
       `main.css` <span data-ttu-id="f77a2-310">a été bloqué</span><span class="sxs-lookup"><span data-stu-id="f77a2-310">has been blocked</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f77a2-311">Désélectionnez la case à cocher **activer le blocage de requête** .</span><span class="sxs-lookup"><span data-stu-id="f77a2-311">Deselect the **Enable request blocking** checkbox.</span></span>  

## <span data-ttu-id="f77a2-312">Conclusion</span><span class="sxs-lookup"><span data-stu-id="f77a2-312">Conclusion</span></span>  

<span data-ttu-id="f77a2-313">Félicitations, vous avez terminé le didacticiel.</span><span class="sxs-lookup"><span data-stu-id="f77a2-313">Congratulations, you have completed the tutorial.</span></span>  <span data-ttu-id="f77a2-314">Vous savez maintenant comment utiliser le panneau **réseau** dans Microsoft Edge devtools!</span><span class="sxs-lookup"><span data-stu-id="f77a2-314">You now know how to use the **Network** panel in the Microsoft Edge DevTools!</span></span>

<!--




-->  

<span data-ttu-id="f77a2-315">Consultez la [référence réseau][DevtoolsNetworkReference] pour découvrir d’autres fonctionnalités devtools liées à l’examen de l’activité du réseau.</span><span class="sxs-lookup"><span data-stu-id="f77a2-315">Check out the [Network Reference][DevtoolsNetworkReference] to discover more DevTools features related to inspecting network activity.</span></span>  

<!--  
 


-->  

<!-- image links -->  

[ImageAddIcon]: ../media/add-icon.msft.png  
[ImageCloseIcon]: ../media/close-icon.msft.png  
[ImageFilterIcon]: ../media/filter-icon.msft.png  
[ImageFormatIcon]: ../media/format-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  
[ImageScreenshotsIcon]: ../media/screenshots-icon.msft.png  
[ImageSearchIcon]: ../media/search-icon.msft.png  
[ImageSettingsIcon]: ../media/settings-icon.msft.png

<!-- links -->  

<!--[CachePolicies]: ../../../web/tools/lighthouse/audits/cache-policy ""  -->  

[DevToolsCustomizePlacement]: ../customize/placement.md "Changer la position de Microsoft Edge DevTools Documents Microsoft"  
[DevtoolsNetworkReference]: ./reference.md "Référence d’analyse du réseau | Documents Microsoft"
[DevtoolsNetworkReferenceFilter]: ./reference.md#filter-requests "Demandes de filtre-référence d’analyse du réseau | Documents Microsoft"  
[DevtoolsReferenceHideOverview]: ./reference.md#hide-the-overview-pane "Masquer le volet vue d’ensemble-référence d’analyse du réseau | Documents Microsoft"
[DevtoolsReferenceProperty]: ./reference.md#filter-requests-by-properties "Demandes de filtre par propriétés-référence d’analyse du réseau | Documents Microsoft"
[DevToolsOpen]: ../open.md "Ouvrez Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsSpeedGetStarted]: ../speed/get-started.md "Optimiser la vitesse de votre site Web avec Microsoft Edge DevTools | Documents Microsoft"  

[GlitchNetworkGetStarted]: https://microsoft-edge-chromium-devtools.glitch.me/static/network/getstarted.html "Examen de la démonstration d’activité réseau | Problème"  

[MDNHTTPCache]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Mise en cache HTTP MDN"  

> [!NOTE]
> <span data-ttu-id="f77a2-325">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f77a2-325">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="f77a2-326">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/network/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="f77a2-326">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="f77a2-328">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f77a2-328">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
