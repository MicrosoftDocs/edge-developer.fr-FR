---
title: Optimiser la vitesse de votre site Web avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 42b742316ccaa64aa35fc1d21c5277e448b2d5b7
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10984623"
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





# <span data-ttu-id="23fb7-103">Optimiser la vitesse de votre site Web avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="23fb7-103">Optimize website speed with Microsoft Edge DevTools</span></span>   



## <span data-ttu-id="23fb7-104">Objectif du didacticiel</span><span class="sxs-lookup"><span data-stu-id="23fb7-104">Goal of tutorial</span></span>  

<span data-ttu-id="23fb7-105">Ce didacticiel vous explique comment utiliser Microsoft Edge DevTools pour trouver des méthodes pour accélérer le chargement de vos sites Web.</span><span class="sxs-lookup"><span data-stu-id="23fb7-105">This tutorial teaches you how to use Microsoft Edge DevTools to find ways to make your websites load faster.</span></span>  

## <span data-ttu-id="23fb7-106">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="23fb7-106">Prerequisites</span></span>  

*   <span data-ttu-id="23fb7-107">Vous devez avoir une connaissance de base du développement Web, semblable à ce qui est enseigné dans cette [Introduction à la classe de développement Web][CourseraIntroductionWebDevelopmentClass].</span><span class="sxs-lookup"><span data-stu-id="23fb7-107">You should have basic web development experience, similar to what is taught in this [Introduction to Web Development class][CourseraIntroductionWebDevelopmentClass].</span></span>  
*   <span data-ttu-id="23fb7-108">Vous n’avez aucune information sur les performances du chargement.</span><span class="sxs-lookup"><span data-stu-id="23fb7-108">You do not need to know anything about load performance.</span></span>  <span data-ttu-id="23fb7-109">Pour plus d’informations, consultez ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="23fb7-109">You learn about it in this tutorial!</span></span>  

## <span data-ttu-id="23fb7-110">Introduction</span><span class="sxs-lookup"><span data-stu-id="23fb7-110">Introduction</span></span>   

<span data-ttu-id="23fb7-111">C’est Thomas.</span><span class="sxs-lookup"><span data-stu-id="23fb7-111">This is Tony.</span></span>  <span data-ttu-id="23fb7-112">Thierry est très célèbre dans la société de chat.</span><span class="sxs-lookup"><span data-stu-id="23fb7-112">Tony is very famous in cat society.</span></span>  <span data-ttu-id="23fb7-113">Il a créé un site Web de telle sorte que ses fans puissent en savoir plus sur ses produits préférés.</span><span class="sxs-lookup"><span data-stu-id="23fb7-113">He has built a website so that his fans are able to learn about his favorite foods.</span></span>  <span data-ttu-id="23fb7-114">Ses fans aiment le site, mais Thomas cesse d’entendre que le site se charge lentement.</span><span class="sxs-lookup"><span data-stu-id="23fb7-114">His fans love the site, but Tony keeps hearing complaints that the site loads slowly.</span></span>  <span data-ttu-id="23fb7-115">Thomas vous a demandé de lui permettre d’accélérer le site.</span><span class="sxs-lookup"><span data-stu-id="23fb7-115">Tony has asked you to help him speed the site up.</span></span>  

:::image type="complex" source="../media/speed-tony.msft.png" alt-text="Bernard le chat" lightbox="../media/speed-tony.msft.png":::
   <span data-ttu-id="23fb7-117">Bernard le chat</span><span class="sxs-lookup"><span data-stu-id="23fb7-117">Tony the cat</span></span>  
:::image-end:::  

## <span data-ttu-id="23fb7-118">Étape 1: Auditez le site</span><span class="sxs-lookup"><span data-stu-id="23fb7-118">Step 1: Audit the site</span></span>   

<span data-ttu-id="23fb7-119">Dès que vous avez fini d’améliorer les performances de chargement d’un site, **Commencez toujours par un audit**.</span><span class="sxs-lookup"><span data-stu-id="23fb7-119">Whenever you set out to improve the load performance of a site, **always start with an audit**.</span></span>  
<span data-ttu-id="23fb7-120">L’audit comporte 2 fonctions importantes:</span><span class="sxs-lookup"><span data-stu-id="23fb7-120">The audit has 2 important functions:</span></span>  

*   <span data-ttu-id="23fb7-121">Il crée un **planning de référence** pour vous pour mesurer les changements ultérieurs.</span><span class="sxs-lookup"><span data-stu-id="23fb7-121">It creates a **baseline** for you to measure subsequent changes against.</span></span>  
*   <span data-ttu-id="23fb7-122">Ce service vous donne des **conseils utiles** sur les modifications qui ont le plus d’impact.</span><span class="sxs-lookup"><span data-stu-id="23fb7-122">It gives you **actionable tips** on what changes have the most impact.</span></span>  
    
### <span data-ttu-id="23fb7-123">Configuration</span><span class="sxs-lookup"><span data-stu-id="23fb7-123">Set up</span></span>   

<span data-ttu-id="23fb7-124">Tout d’abord, vous devez configurer le site pour pouvoir le modifier ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="23fb7-124">First, you must set up the site so that you are able to make changes to it later.</span></span>  

1.  <span data-ttu-id="23fb7-125">[Ouvrez le code source pour le site](https://glitch.com/edit/#!/tony).</span><span class="sxs-lookup"><span data-stu-id="23fb7-125">[Open the source code for the site](https://glitch.com/edit/#!/tony).</span></span>  <span data-ttu-id="23fb7-126">Cet onglet est appelé **onglet Éditeur**.</span><span class="sxs-lookup"><span data-stu-id="23fb7-126">This tab is referred to as the **editor tab**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-server-js.msft.png" alt-text="Onglet Éditeur" lightbox="../media/speed-glitch-tony-server-js.msft.png":::
       <span data-ttu-id="23fb7-128">**Onglet Éditeur**</span><span class="sxs-lookup"><span data-stu-id="23fb7-128">The **editor tab**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="23fb7-129">Sélectionnez **Thomas**.</span><span class="sxs-lookup"><span data-stu-id="23fb7-129">Select **tony**.</span></span>  <span data-ttu-id="23fb7-130">Un menu s’affiche.</span><span class="sxs-lookup"><span data-stu-id="23fb7-130">A menu appears.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-server-js-remix-project.msft.png" alt-text="Menu qui apparaît après avoir cliqué sur Thierry" lightbox="../media/speed-glitch-tony-server-js-remix-project.msft.png":::
       <span data-ttu-id="23fb7-132">Menu qui apparaît après avoir cliqué sur **Thierry**</span><span class="sxs-lookup"><span data-stu-id="23fb7-132">The menu that appears after clicking **tony**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="23fb7-133">Sélectionnez **Remix Project**.</span><span class="sxs-lookup"><span data-stu-id="23fb7-133">Select **Remix Project**.</span></span>  <span data-ttu-id="23fb7-134">Le nom du projet **passe de Thomas à un** nom généré de manière aléatoire.</span><span class="sxs-lookup"><span data-stu-id="23fb7-134">The name of the project changes from **tony** to some randomly-generated name.</span></span>  <span data-ttu-id="23fb7-135">Vous disposez maintenant de votre propre copie modifiable du code.</span><span class="sxs-lookup"><span data-stu-id="23fb7-135">You now have your own editable copy of the code.</span></span>  <span data-ttu-id="23fb7-136">Par la suite, vous pouvez modifier ce code.</span><span class="sxs-lookup"><span data-stu-id="23fb7-136">Later on, you may make changes to this code.</span></span>  
1.  <span data-ttu-id="23fb7-137">Sélectionner **Afficher** et sélectionner **dans une nouvelle fenêtre**.</span><span class="sxs-lookup"><span data-stu-id="23fb7-137">Select **Show** and select **In a New Window**.</span></span>  <span data-ttu-id="23fb7-138">La démonstration s’ouvre dans un nouvel onglet.  Cet onglet est appelé **onglet démonstration**.  Le chargement du site risque de prendre un certain temps.</span><span class="sxs-lookup"><span data-stu-id="23fb7-138">The demo opens in a new tab.  This tab is be referred to as the **demo tab**.  It may take a while for the site to load.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-show-live.msft.png" alt-text="Onglet démonstration" lightbox="../media/speed-glitch-tony-show-live.msft.png":::
       <span data-ttu-id="23fb7-140">Onglet démonstration</span><span class="sxs-lookup"><span data-stu-id="23fb7-140">The demo tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="23fb7-141">Appuyez sur `Control` + `Shift` + `J` \ (Windows \) ou `Command` + `Option` + `J` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="23fb7-141">Press `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\).</span></span>  <span data-ttu-id="23fb7-142">Microsoft Edge DevTools s’ouvre à côté de la démonstration.</span><span class="sxs-lookup"><span data-stu-id="23fb7-142">Microsoft Edge DevTools opens up alongside the demo.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-show-live-console.msft.png" alt-text="DevTools et la démo" lightbox="../media/speed-glitch-tony-show-live-console.msft.png":::
       <span data-ttu-id="23fb7-144">DevTools et la démo</span><span class="sxs-lookup"><span data-stu-id="23fb7-144">DevTools and the demo</span></span>  
    :::image-end:::  
    
<span data-ttu-id="23fb7-145">Pour le reste des captures d’écran de ce didacticiel, DevTools est affiché dans une fenêtre séparée.</span><span class="sxs-lookup"><span data-stu-id="23fb7-145">For the rest of the screenshots in this tutorial, DevTools is shown in a separate window.</span></span>  <span data-ttu-id="23fb7-146">Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le menu de commandes, `Undock` puis sélectionnez **détacher dans une fenêtre séparée**.</span><span class="sxs-lookup"><span data-stu-id="23fb7-146">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, typing `Undock`, and then selecting **Undock into separate window**.</span></span>  

:::image type="complex" source="../media/speed-console.msft.png" alt-text="DevTools non attaché" lightbox="../media/speed-console.msft.png":::
   <span data-ttu-id="23fb7-148">DevTools non attaché</span><span class="sxs-lookup"><span data-stu-id="23fb7-148">Undocked DevTools</span></span>  
:::image-end:::  

### <span data-ttu-id="23fb7-149">Établir un planning de référence</span><span class="sxs-lookup"><span data-stu-id="23fb7-149">Establish a baseline</span></span>   

<span data-ttu-id="23fb7-150">Le planning de référence est un enregistrement de la façon dont le site a été traité avant d’améliorer ses performances.</span><span class="sxs-lookup"><span data-stu-id="23fb7-150">The baseline is a record of how the site performed before you made any performance improvements.</span></span>  

1.  <span data-ttu-id="23fb7-151">Sélectionnez l’onglet **audits** .  Il est possible qu’il soit masqué derrière le bouton **autres panneaux** \ ( ![ autres panneaux ][ImageMorePanelsIcon] \).</span><span class="sxs-lookup"><span data-stu-id="23fb7-151">Select the **Audits** tab.  It may be hidden behind the **More Panels** \(![More Panels][ImageMorePanelsIcon]\) button.</span></span>  <span data-ttu-id="23fb7-152">Ce panneau comporte une phare, car le projet qui alimente le panneau d’audit est appelé **phare**.</span><span class="sxs-lookup"><span data-stu-id="23fb7-152">There is a Lighthouse on this panel because the project that powers the Audits panel is named **Lighthouse**.</span></span>  
    
    [!INCLUDE [audits-panel-note](../includes/audits-panel-note.md)]  
    
    :::image type="complex" source="../media/speed-audits-performance.msft.png" alt-text="Volet d’audit" lightbox="../media/speed-audits-performance.msft.png":::
       <span data-ttu-id="23fb7-154">Volet **d’audit**</span><span class="sxs-lookup"><span data-stu-id="23fb7-154">The **Audits** panel</span></span>  
    :::image-end:::  
    
    <!--todo: add link to Lighthouse when section is available  -->  
    <!-- /web/tools/lighthouse  -->  
    
1.  <span data-ttu-id="23fb7-155">Associez vos paramètres de configuration d’audit à ceux de la figure précédente.</span><span class="sxs-lookup"><span data-stu-id="23fb7-155">Match your audit configuration settings to those in the previous figure.</span></span>  <span data-ttu-id="23fb7-156">Voici une explication des différentes options disponibles:</span><span class="sxs-lookup"><span data-stu-id="23fb7-156">Here is an explanation of the different options:</span></span>  
    
    *   <span data-ttu-id="23fb7-157">**Appareil**.</span><span class="sxs-lookup"><span data-stu-id="23fb7-157">**Device**.</span></span>  <span data-ttu-id="23fb7-158">Définissez sur **mobile** pour modifier la chaîne de l’agent utilisateur et simuler une fenêtre d’affichage mobile.</span><span class="sxs-lookup"><span data-stu-id="23fb7-158">Setting to **Mobile** changes the user agent string and simulates a mobile viewport.</span></span>  <span data-ttu-id="23fb7-159">Le paramétrage sur **Bureau** à peu près empêche uniquement les changements de **mobilité** .</span><span class="sxs-lookup"><span data-stu-id="23fb7-159">Setting to **Desktop** pretty much just disables the **Mobile** changes.</span></span>  
    *   <span data-ttu-id="23fb7-160">Les **audits**.</span><span class="sxs-lookup"><span data-stu-id="23fb7-160">**Audits**.</span></span>  <span data-ttu-id="23fb7-161">La désactivation d’une catégorie empêche le panneau d’audit d’exécuter ces audits et exclut ces audits de votre rapport.</span><span class="sxs-lookup"><span data-stu-id="23fb7-161">Disabling a category prevents the Audits panel from running those audits, and excludes those audits from your report.</span></span>  <span data-ttu-id="23fb7-162">Laissez les autres catégories activées si vous voulez voir les types de recommandations qui s’offrent à vous.</span><span class="sxs-lookup"><span data-stu-id="23fb7-162">Leave the other categories enabled, if you want to see the types of recommendations that are provide.</span></span>  <span data-ttu-id="23fb7-163">La désactivation des catégories accélère légèrement le processus d’audit.</span><span class="sxs-lookup"><span data-stu-id="23fb7-163">Disabling categories slightly speeds up the auditing process.</span></span>  
    *   <span data-ttu-id="23fb7-164">**Limitation**.</span><span class="sxs-lookup"><span data-stu-id="23fb7-164">**Throttling**.</span></span>  <span data-ttu-id="23fb7-165">Pour simuler la fonction de **4G lente, le ralenti de l’UC 4x** simule les conditions typiques de navigation sur un appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="23fb7-165">Setting to **Simulated Slow 4G, 4x CPU Slowdown** simulates the typical conditions of browsing on a mobile device.</span></span>  <span data-ttu-id="23fb7-166">Son nom est «simulé», car le panneau d’audit n’est pas réellement limité lors du processus d’audit.</span><span class="sxs-lookup"><span data-stu-id="23fb7-166">It is named "simulated" because the Audits panel does not actually throttle during the auditing process.</span></span>  <span data-ttu-id="23fb7-167">Au lieu de cela, il s’agit simplement de l’extrapolation du temps nécessaire au chargement de la page dans des conditions mobiles.</span><span class="sxs-lookup"><span data-stu-id="23fb7-167">Instead, it just extrapolates how long the page would take to load under mobile conditions.</span></span>  <span data-ttu-id="23fb7-168">En revanche, le paramètre **appliedd...** , qui a pour effet de limiter votre processeur et votre réseau, par le biais d’un processus d’audit plus long.</span><span class="sxs-lookup"><span data-stu-id="23fb7-168">The **Applied...** setting, on the other hand, actually throttles your CPU and network, with the tradeoff of a longer auditing process.</span></span>  
    *   <span data-ttu-id="23fb7-169">**Vider le stockage**.</span><span class="sxs-lookup"><span data-stu-id="23fb7-169">**Clear Storage**.</span></span>  <span data-ttu-id="23fb7-170">Activez cette case à cocher pour effacer tout le stockage associé à la page avant chaque audit.</span><span class="sxs-lookup"><span data-stu-id="23fb7-170">Enabling this checkbox clears all storage associated with the page before every audit.</span></span>  <span data-ttu-id="23fb7-171">Ne renseignez pas ce paramètre si vous souhaitez vérifier la manière dont les visiteurs de votre site se familiarisent avec la première fois.</span><span class="sxs-lookup"><span data-stu-id="23fb7-171">Leave this setting on if you want to audit how first-time visitors experience your site.</span></span>  <span data-ttu-id="23fb7-172">Désactivez ce paramètre si vous souhaitez utiliser la répétition d’une visite.</span><span class="sxs-lookup"><span data-stu-id="23fb7-172">Disable this setting when you want the repeat-visit experience.</span></span>  
    
1.  <span data-ttu-id="23fb7-173">Sélectionnez **exécuter les audits**.</span><span class="sxs-lookup"><span data-stu-id="23fb7-173">Select **Run Audits**.</span></span>  <span data-ttu-id="23fb7-174">Après 10 à 30 secondes, le volet d’audit affiche un rapport sur les performances de votre site.</span><span class="sxs-lookup"><span data-stu-id="23fb7-174">After 10 to 30 seconds, the Audits panel shows you a report of the performance of the site.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png" alt-text="Rapport du volet d’audit des performances du site" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png":::
       <span data-ttu-id="23fb7-176">Rapport du volet d’audit des performances du site</span><span class="sxs-lookup"><span data-stu-id="23fb7-176">The report for the Audits panel of the performance of the site</span></span>  
    :::image-end:::  
    
#### <span data-ttu-id="23fb7-177">Gestion des erreurs de rapport</span><span class="sxs-lookup"><span data-stu-id="23fb7-177">Handling report errors</span></span>   

<span data-ttu-id="23fb7-178">Si un message d’erreur apparaît dans votre rapport du panneau d’audit, essayez d’exécuter l’onglet démonstration à partir d’une fenêtre **InPrivate** sans afficher d’autres onglets.</span><span class="sxs-lookup"><span data-stu-id="23fb7-178">If you ever get an error in your Audits panel report, try running the demo tab from an **InPrivate** window with no other tabs open.</span></span>  <span data-ttu-id="23fb7-179">Cela garantit que vous exécutez Microsoft Edge à partir de l’État Clean.</span><span class="sxs-lookup"><span data-stu-id="23fb7-179">This ensures that you are running Microsoft Edge from a clean state.</span></span>  <span data-ttu-id="23fb7-180">Les extensions Microsoft Edge en particulier interfèrent souvent avec le processus d’audit.</span><span class="sxs-lookup"><span data-stu-id="23fb7-180">Microsoft Edge Extensions in particular often interfere with the auditing process.</span></span>  

<!--todo: add screen capture for error in audit -->  
<!--
:::image type="complex" source="../media/speed-.msft.png" alt-text="A report that errored" lightbox="../media/speed-.msft.png":::
   A report that errored  
:::image-end:::  
-->  

### <span data-ttu-id="23fb7-181">Comprendre votre état</span><span class="sxs-lookup"><span data-stu-id="23fb7-181">Understand your report</span></span>   

<span data-ttu-id="23fb7-182">Le nombre situé en haut de votre état correspond au score de performance global du site.</span><span class="sxs-lookup"><span data-stu-id="23fb7-182">The number at the top of your report is the overall performance score for the site.</span></span>  <span data-ttu-id="23fb7-183">Par la suite, au fur et à mesure que vous apportez des modifications à votre code, vous devriez voir ce numéro augmenter.</span><span class="sxs-lookup"><span data-stu-id="23fb7-183">Later, as you make changes to the code, you should see this number rise.</span></span>  <span data-ttu-id="23fb7-184">Un résultat plus élevé correspond à de meilleures performances.</span><span class="sxs-lookup"><span data-stu-id="23fb7-184">A higher score means better performance.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png" alt-text="Le score de performance global" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png":::
   <span data-ttu-id="23fb7-186">Le score de performance global</span><span class="sxs-lookup"><span data-stu-id="23fb7-186">The overall performance score</span></span>  
:::image-end:::  

<span data-ttu-id="23fb7-187">La section **mesures** fournit des mesures quantitatives des performances du site.</span><span class="sxs-lookup"><span data-stu-id="23fb7-187">The **Metrics** section provides quantitative measurements of the performance of the site.</span></span>  <span data-ttu-id="23fb7-188">Chaque métrique donne un aperçu d’un aspect différent des performances.</span><span class="sxs-lookup"><span data-stu-id="23fb7-188">Each metric provides insight into a different aspect of the performance.</span></span>  <span data-ttu-id="23fb7-189">Par exemple, lorsque le contenu est dessiné à l’écran pour **la première fois** , il s’agit d’un jalon important dans la perception de l’utilisateur du chargement de la page, alors que le **temps nécessaire à l’interactivité** correspond au point où la page semble suffisamment prête pour gérer les interactions utilisateur.</span><span class="sxs-lookup"><span data-stu-id="23fb7-189">For example, **First Contentful Paint** tells you when content is first painted to the screen, which is an important milestone in the user's perception of the page load, whereas **Time To Interactive** marks the point at which the page appears ready enough to handle user interactions.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png" alt-text="Section mesures" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png":::
   <span data-ttu-id="23fb7-191">Section **mesures**</span><span class="sxs-lookup"><span data-stu-id="23fb7-191">The **Metrics** section</span></span>  
:::image-end:::  

<span data-ttu-id="23fb7-192">Sélectionnez le bouton bascule surligné dans la figure ci-dessous pour afficher une description de chaque métrique, puis cliquez sur **en savoir plus** pour lire la documentation correspondante.</span><span class="sxs-lookup"><span data-stu-id="23fb7-192">Select the highlighted toggle button in the following figure to see a description for each metric, and click **Learn More** to read documentation about it.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-expanded.msft.png" alt-text="Sélectionner le bouton bascule surligné pour développer les éléments métriques" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-expanded.msft.png":::
   <span data-ttu-id="23fb7-194">Sélectionner le bouton bascule surligné pour développer les éléments métriques</span><span class="sxs-lookup"><span data-stu-id="23fb7-194">Select the highlighted toggle button to expand the Metrics items</span></span>  
:::image-end:::  

<span data-ttu-id="23fb7-195">Le sous-métrique est une collection de captures d’écran qui vous montrent le mode de chargement de la page.</span><span class="sxs-lookup"><span data-stu-id="23fb7-195">Below Metrics is a collection of screenshots that show you how the page looked as it loaded.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png" alt-text="Captures d’écran illustrant l’apparence de la page en cours de chargement" lightbox="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png":::
   <span data-ttu-id="23fb7-197">Captures d’écran illustrant l’apparence de la page en cours de chargement</span><span class="sxs-lookup"><span data-stu-id="23fb7-197">Screenshots of how the page looked while loading</span></span>  
:::image-end:::  

<span data-ttu-id="23fb7-198">La section **opportunités** fournit des conseils spécifiques pour améliorer les performances de chargement de cette page spécifique.</span><span class="sxs-lookup"><span data-stu-id="23fb7-198">The **Opportunities** section provides specific tips on how to improve the load performance of this specific page.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png" alt-text="Section opportunités" lightbox="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png":::
   <span data-ttu-id="23fb7-200">Section **opportunités**</span><span class="sxs-lookup"><span data-stu-id="23fb7-200">The **Opportunities** section</span></span>  
:::image-end:::  

<span data-ttu-id="23fb7-201">Sélectionnez une opportunité pour en savoir plus à son sujet.</span><span class="sxs-lookup"><span data-stu-id="23fb7-201">Select an opportunity to learn more about it.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png" alt-text="Éliminer l’opportunité de blocage des ressources de blocage des rendez-vous" lightbox="../media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png":::
   <span data-ttu-id="23fb7-203">**Éliminer l’opportunité de blocage des ressources de blocage des rendez-** vous</span><span class="sxs-lookup"><span data-stu-id="23fb7-203">**Eliminate render-blocking resources** opportunity</span></span>  
:::image-end:::  

<span data-ttu-id="23fb7-204">Pour plus d’informations sur les raisons de la nécessité d’une opportunité, voir **en savoir plus** sur la résolution des problèmes.</span><span class="sxs-lookup"><span data-stu-id="23fb7-204">Select **Learn More** to see documentation about why an opportunity is important, and specific recommendations on how to fix it.</span></span>  

:::image type="complex" source="../media/speed-web-dev-performance-audits.msft.png" alt-text="Documentation pour l’opportunité de suppression des ressources de blocage de rendu" lightbox="../media/speed-web-dev-performance-audits.msft.png":::
   <span data-ttu-id="23fb7-206">Documentation pour l’opportunité de **suppression des ressources de blocage de rendu**</span><span class="sxs-lookup"><span data-stu-id="23fb7-206">Documentation for the **Eliminate render-blocking resources** opportunity</span></span>  
:::image-end:::  

<span data-ttu-id="23fb7-207">La section **Diagnostics** fournit des informations supplémentaires sur les facteurs qui contribuent au temps de chargement de la page.</span><span class="sxs-lookup"><span data-stu-id="23fb7-207">The **Diagnostics** section provides more information about factors that contribute to the load time of the page.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png" alt-text="Section Diagnostics" lightbox="../media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png":::
   <span data-ttu-id="23fb7-209">Section **Diagnostics**</span><span class="sxs-lookup"><span data-stu-id="23fb7-209">The **Diagnostics** section</span></span>  
:::image-end:::  

<span data-ttu-id="23fb7-210">La section **contrôles réussis** vous montre le fonctionnement correct du site.</span><span class="sxs-lookup"><span data-stu-id="23fb7-210">The **Passed Audits** section shows you what the site is doing correctly.</span></span>  <span data-ttu-id="23fb7-211">Pour développer la section.</span><span class="sxs-lookup"><span data-stu-id="23fb7-211">Select to expand the section.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png" alt-text="Section audits transmis" lightbox="../media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png":::
   <span data-ttu-id="23fb7-213">Section **audits transmis**</span><span class="sxs-lookup"><span data-stu-id="23fb7-213">The **Passed Audits** section</span></span>  
:::image-end:::  

## <span data-ttu-id="23fb7-214">Étape 2: expérimenter</span><span class="sxs-lookup"><span data-stu-id="23fb7-214">Step 2: Experiment</span></span>   

<span data-ttu-id="23fb7-215">La section opportunités de votre rapport d’audit vous donne des conseils pour améliorer les performances de la page.</span><span class="sxs-lookup"><span data-stu-id="23fb7-215">The Opportunities section of your audit report gives you tips on how to improve the performance of the page.</span></span>  <span data-ttu-id="23fb7-216">Dans cette section, vous implémentez les modifications recommandées sur le code base, puis vous auditez le site après chaque modification pour mesurer la vitesse de votre site.</span><span class="sxs-lookup"><span data-stu-id="23fb7-216">In this section, you implement the recommended changes to the codebase, auditing the site after each change to measure how it affects site speed.</span></span>  

### <span data-ttu-id="23fb7-217">Activer la compression de texte</span><span class="sxs-lookup"><span data-stu-id="23fb7-217">Enable text compression</span></span>   

<span data-ttu-id="23fb7-218">Votre rapport déclare qu’il n’est pas l’une des principales opportunités d’améliorer les performances de la page.</span><span class="sxs-lookup"><span data-stu-id="23fb7-218">Your report says that avoiding enormous network payloads is one of the top opportunities for improving the performance of the page.</span></span>  <span data-ttu-id="23fb7-219">L’activation de la compression de texte permet d’améliorer les performances de la page.</span><span class="sxs-lookup"><span data-stu-id="23fb7-219">Enabling text compression is an opportunity to improve the performance of the page.</span></span>  

<span data-ttu-id="23fb7-220">La compression de texte est celle qui consiste à réduire ou compresser la taille d’un fichier texte avant de l’envoyer sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="23fb7-220">Text compression is when you reduce, or compress, the size of a text file before sending it over the network.</span></span>  <span data-ttu-id="23fb7-221">Type semblable à la façon dont vous pouvez Zipper un dossier avant de l’envoyer par courrier électronique afin de réduire la taille.</span><span class="sxs-lookup"><span data-stu-id="23fb7-221">Kind of like how you might zip a folder before emailing it to reduce the size.</span></span>  

<span data-ttu-id="23fb7-222">Avant d’activer la compression, voici quelques méthodes permettant de vérifier manuellement si les ressources de texte sont comprimées.</span><span class="sxs-lookup"><span data-stu-id="23fb7-222">Before you enable compression, here are a couple of ways to manually check whether text resources are compressed.</span></span>  

1.  <span data-ttu-id="23fb7-223">Sélectionnez l’onglet **Network (réseau** ).</span><span class="sxs-lookup"><span data-stu-id="23fb7-223">Select the **Network** tab.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network.msft.png" alt-text="Panneau réseau" lightbox="../media/speed-glitch-tony-remix-network.msft.png":::
       <span data-ttu-id="23fb7-225">Panneau **réseau**</span><span class="sxs-lookup"><span data-stu-id="23fb7-225">The **Network** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="23fb7-226">Sélectionnez l’icône du **paramètre réseau** .</span><span class="sxs-lookup"><span data-stu-id="23fb7-226">Select the **Network setting** icon.</span></span>  
1.  <span data-ttu-id="23fb7-227">Cochez la case **utiliser des lignes de requête volumineuses** .</span><span class="sxs-lookup"><span data-stu-id="23fb7-227">Select the **Use Large Request Rows** checkbox.</span></span>  <span data-ttu-id="23fb7-228">La hauteur des lignes du tableau de requêtes réseau augmente.</span><span class="sxs-lookup"><span data-stu-id="23fb7-228">The height of the rows in the table of network requests increases.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-use-large-request-rows.msft.png" alt-text="Lignes de grande taille dans la table requêtes réseau" lightbox="../media/speed-glitch-tony-remix-network-use-large-request-rows.msft.png":::
       <span data-ttu-id="23fb7-230">Lignes de grande taille dans la table requêtes réseau</span><span class="sxs-lookup"><span data-stu-id="23fb7-230">Large rows in the network requests table</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="23fb7-231">Si vous ne voyez pas la colonne **taille** dans le tableau des requêtes réseau, cliquez sur l’en-tête de la table, puis sélectionnez **taille**.</span><span class="sxs-lookup"><span data-stu-id="23fb7-231">If you do not see the **Size** column in the table of network requests, click the table header and then select **Size**.</span></span>  

<span data-ttu-id="23fb7-232">Chaque cellule **taille** affiche deux valeurs.</span><span class="sxs-lookup"><span data-stu-id="23fb7-232">Each **Size** cell shows two values.</span></span>  <span data-ttu-id="23fb7-233">La valeur supérieure correspond à la taille de la ressource téléchargée.</span><span class="sxs-lookup"><span data-stu-id="23fb7-233">The top value is the size of the downloaded resource.</span></span>  
<span data-ttu-id="23fb7-234">La valeur inférieure correspond à la taille de la ressource non compressée.</span><span class="sxs-lookup"><span data-stu-id="23fb7-234">The bottom value is the size of the uncompressed resource.</span></span>  <span data-ttu-id="23fb7-235">Si les deux valeurs sont identiques, la ressource n’est pas compressée lors de son envoi via le réseau.</span><span class="sxs-lookup"><span data-stu-id="23fb7-235">If the two values are the same, then the resource is not being compressed when it is sent over the network.</span></span>  <span data-ttu-id="23fb7-236">Par exemple, dans l’illustration précédente, les premières et dernières valeurs de `bundle.js` sont `1.2 MB` et `1.2 MB` .</span><span class="sxs-lookup"><span data-stu-id="23fb7-236">For example, in the previous figure, the top and bottom values for `bundle.js` are `1.2 MB` and `1.2 MB`.</span></span>  

<span data-ttu-id="23fb7-237">Vérifiez la compression en inspectant les en-têtes HTTP d’une ressource:</span><span class="sxs-lookup"><span data-stu-id="23fb7-237">Check for compression by inspecting the HTTP headers of a resource:</span></span>  

1.  <span data-ttu-id="23fb7-238">Sélectionnez **bundle.js**.</span><span class="sxs-lookup"><span data-stu-id="23fb7-238">Select **bundle.js**.</span></span>  
1.  <span data-ttu-id="23fb7-239">Sélectionnez l’onglet **en-têtes** .</span><span class="sxs-lookup"><span data-stu-id="23fb7-239">Select the **Headers** tab.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png" alt-text="Onglet en-têtes" lightbox="../media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png":::
       <span data-ttu-id="23fb7-241">Onglet **en-têtes**</span><span class="sxs-lookup"><span data-stu-id="23fb7-241">The **Headers** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="23fb7-242">Recherchez un en-tête dans la section **en-têtes de réponse** `content-encoding` .</span><span class="sxs-lookup"><span data-stu-id="23fb7-242">Search the **Response Headers** section for a `content-encoding` header.</span></span>  <span data-ttu-id="23fb7-243">Vous ne devez pas voir l’une d’elles, ce qui signifie qu’elle n' `bundle.js` a pas été compactée.</span><span class="sxs-lookup"><span data-stu-id="23fb7-243">You should not see one, meaning that `bundle.js` was not compressed.</span></span>  <span data-ttu-id="23fb7-244">Lorsqu’une ressource est compressée, cet en-tête est généralement défini sur `gzip` , `deflate` ou `br` .</span><span class="sxs-lookup"><span data-stu-id="23fb7-244">When a resource is compressed, this header is usually set to `gzip`, `deflate`, or `br`.</span></span>  <span data-ttu-id="23fb7-245">Pour obtenir une description de ces valeurs, voir [directives][MDNContentEncodingDirectives] .</span><span class="sxs-lookup"><span data-stu-id="23fb7-245">See [Directives][MDNContentEncodingDirectives] for an explanation of these values.</span></span>  

<span data-ttu-id="23fb7-246">C’est suffisant pour les explications.</span><span class="sxs-lookup"><span data-stu-id="23fb7-246">Enough with the explanations.</span></span>  <span data-ttu-id="23fb7-247">Le moment est venu d’apporter des modifications.</span><span class="sxs-lookup"><span data-stu-id="23fb7-247">Time to make some changes!</span></span>  <span data-ttu-id="23fb7-248">Autorisez la compression de texte en ajoutant quelques lignes de code:</span><span class="sxs-lookup"><span data-stu-id="23fb7-248">Enable text compression by adding a couple of lines of code:</span></span>  

1.  <span data-ttu-id="23fb7-249">Dans l’onglet Éditeur, cliquez sur **server.js**.</span><span class="sxs-lookup"><span data-stu-id="23fb7-249">In the editor tab, click **server.js**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-server-js.msft.png" alt-text="Modifier server.js" lightbox="../media/speed-glitch-tony-remix-server-js.msft.png":::
       <span data-ttu-id="23fb7-251">Edit</span><span class="sxs-lookup"><span data-stu-id="23fb7-251">Edit</span></span> `server.js`  
    :::image-end:::  
    
1.  <span data-ttu-id="23fb7-252">Ajoutez le code suivant à **server.js**.</span><span class="sxs-lookup"><span data-stu-id="23fb7-252">Add the following code to **server.js**.</span></span>  <span data-ttu-id="23fb7-253">Assurez-vous d’entrer `app.use(compression())` auparavant `app.use(express.static('build'))` .</span><span class="sxs-lookup"><span data-stu-id="23fb7-253">Make sure to put `app.use(compression())` before `app.use(express.static('build'))`.</span></span>  

    ```javascript
    const express = require('express');
    const app = express();
    const fs = require('fs');
    const compression = require('compression');

    app.use(compression());
    app.use(express.static('build'));
    
    const listener = app.listen(process.env.PORT || 1234, function () {
        console.log(`Listening on port ${listener.address().port}`);
    });
    ```  
    
    > [!NOTE]
    > <span data-ttu-id="23fb7-254">En règle générale, vous devez installer le `compression` package par le biais d’une expression similaire `npm i -S compression` , mais cela a déjà été fait pour vous.</span><span class="sxs-lookup"><span data-stu-id="23fb7-254">Usually, you have to install the `compression` package via something like `npm i -S compression`, but this has already been done for you.</span></span>  
    
1.  <span data-ttu-id="23fb7-255">Patientez pendant le déploiement de la nouvelle version du site.</span><span class="sxs-lookup"><span data-stu-id="23fb7-255">Wait for Glitch to deploy the new build of the site.</span></span>  <span data-ttu-id="23fb7-256">L’animation fantaisie en regard des **Outils** signifie que le site est en cours de recréation et de redéploiement.</span><span class="sxs-lookup"><span data-stu-id="23fb7-256">The fancy animation next to **Tools** means that the site is getting rebuilt and redeployed.</span></span>  <span data-ttu-id="23fb7-257">La modification est prête lorsque l’animation en regard des **Outils** est en suspens.</span><span class="sxs-lookup"><span data-stu-id="23fb7-257">The change is ready when the animation next to **Tools** goes away.</span></span>  <span data-ttu-id="23fb7-258">Sélectionnez **Afficher** et sélectionnez **de nouveau dans une nouvelle fenêtre** .</span><span class="sxs-lookup"><span data-stu-id="23fb7-258">Select **Show** and select **In a New Window** again.</span></span>  
    
    <!--
    :::image type="complex" source="../media/speed-glitch-tony-remix-server-js-edited.msft.png" alt-text="The animation that indicates that the site is getting built" lightbox="../media/speed-glitch-tony-remix-server-js-edited.msft.png":::
       The animation that indicates that the site is getting built  
    :::image-end:::  
    -->  
    
<span data-ttu-id="23fb7-259">Utilisez les flux de travail que vous avez appris précédemment pour vérifier que la compression fonctionne:</span><span class="sxs-lookup"><span data-stu-id="23fb7-259">Use the workflows that you learned earlier to manually check that the compression is working:</span></span>  

1.  <span data-ttu-id="23fb7-260">Revenez à l’onglet démonstration et rechargez la page.</span><span class="sxs-lookup"><span data-stu-id="23fb7-260">Go back to the demo tab and reload the page.</span></span>  <span data-ttu-id="23fb7-261">La colonne **taille** doit maintenant afficher 2 valeurs différentes pour les ressources de texte comme `bundle.js` .</span><span class="sxs-lookup"><span data-stu-id="23fb7-261">The **Size** column should now show 2 different values for text resources like `bundle.js`.</span></span>  <span data-ttu-id="23fb7-262">Dans l’illustration suivante, la valeur la plus haute de `256 KB` pour `bundle.js` correspond à la taille du fichier envoyé sur le réseau et la valeur inférieure de `1.2 MB` correspond à la taille de fichier non comprimé.</span><span class="sxs-lookup"><span data-stu-id="23fb7-262">In the figure after the following, the top value of `256 KB` for `bundle.js` is the size of the file that was sent over the network, and the bottom value of `1.2 MB` is the uncompressed file size.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-main.msft.png" alt-text="La colonne taille affiche désormais 2 valeurs différentes pour les ressources de texte" lightbox="../media/speed-glitch-tony-remix-network-main.msft.png":::
       <span data-ttu-id="23fb7-264">La colonne **taille** affiche désormais 2 valeurs différentes pour les ressources de texte</span><span class="sxs-lookup"><span data-stu-id="23fb7-264">The **Size** column now shows 2 different values for text resources</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="23fb7-265">La section **en-têtes de réponse** de `bundle.js` devrait désormais inclure un `content-encoding: gzip` en-tête.</span><span class="sxs-lookup"><span data-stu-id="23fb7-265">The **Response Headers** section for `bundle.js` should now include a `content-encoding: gzip` header.</span></span>
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png" alt-text="La section en-têtes de réponse contient désormais un en-tête de codage de contenu" lightbox="../media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png":::
       <span data-ttu-id="23fb7-267">La section **en-têtes de réponse** contient désormais un en-tête de codage de contenu</span><span class="sxs-lookup"><span data-stu-id="23fb7-267">The **Response Headers** section now contains a content-encoding header</span></span>  
    :::image-end:::  
    
<span data-ttu-id="23fb7-268">Auditez de nouveau la page pour mesurer le type de compression de texte d’impact sur les performances de chargement de la page:</span><span class="sxs-lookup"><span data-stu-id="23fb7-268">Audit the page again to measure what kind of impact text compression has on the load performance of the page:</span></span>  

1.  <span data-ttu-id="23fb7-269">Sélectionnez l’onglet **audits** .</span><span class="sxs-lookup"><span data-stu-id="23fb7-269">Select the **Audits** tab.</span></span>  
1.  <span data-ttu-id="23fb7-270">Sélectionnez **effectuer un audit** \ ( ![ effectuer un audit ][ImagePerformIcon] \).</span><span class="sxs-lookup"><span data-stu-id="23fb7-270">Select **Perform an audit** \(![Perform an audit][ImagePerformIcon]\).</span></span>  
1.  <span data-ttu-id="23fb7-271">Ne modifiez pas les paramètres comme auparavant.</span><span class="sxs-lookup"><span data-stu-id="23fb7-271">Leave the settings the same as before.</span></span>  
1.  <span data-ttu-id="23fb7-272">Sélectionnez **exécuter l’audit**.</span><span class="sxs-lookup"><span data-stu-id="23fb7-272">Select **Run audit**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance.msft.png" alt-text="Rapport d’audit après l’activation de la compression de texte" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance.msft.png":::
       <span data-ttu-id="23fb7-274">Rapport d’audit après l’activation de la compression de texte</span><span class="sxs-lookup"><span data-stu-id="23fb7-274">An Audits report after enabling text compression</span></span>  
    :::image-end:::  
    
<!--  Woohoo!  That looks like progress.  -->  <span data-ttu-id="23fb7-275">Le score de performance global doit être plus élevé, ce qui signifie que le site est plus rapide.</span><span class="sxs-lookup"><span data-stu-id="23fb7-275">Your overall performance score should have increased, meaning that the site is getting faster.</span></span>  

#### <span data-ttu-id="23fb7-276">Compression de texte dans le monde réel</span><span class="sxs-lookup"><span data-stu-id="23fb7-276">Text compression in the real world</span></span>   

<span data-ttu-id="23fb7-277">La plupart des serveurs possèdent réellement des correctifs simples, comme pour l’activation du compactage.</span><span class="sxs-lookup"><span data-stu-id="23fb7-277">Most servers really do have simple fixes like this for enabling compression!</span></span>  <span data-ttu-id="23fb7-278">Il suffit de procéder à une recherche pour configurer le serveur que vous utilisez pour compresser le texte.</span><span class="sxs-lookup"><span data-stu-id="23fb7-278">Just do a search on how to configure whatever server you use to compress text.</span></span>  

### <span data-ttu-id="23fb7-279">Redimensionner des images</span><span class="sxs-lookup"><span data-stu-id="23fb7-279">Resize images</span></span>   

<span data-ttu-id="23fb7-280">Votre rapport indique qu’il est recommandé d’éviter les charges utiles réseau énormes pour améliorer les performances de la page.</span><span class="sxs-lookup"><span data-stu-id="23fb7-280">Your report indicates that avoiding enormous network payloads is one of the top opportunities for improving the performance of the page.</span></span>  <span data-ttu-id="23fb7-281">Le redimensionnement des images permet de réduire la taille de la charge utile du réseau.</span><span class="sxs-lookup"><span data-stu-id="23fb7-281">Resizing images helps reduce the size of the network payload.</span></span>  <span data-ttu-id="23fb7-282">Si votre utilisateur consulte vos images sur un écran d’appareil mobile d’une largeur de 500 pixels, il n’y a rien de plus que d’envoyer une image 1500 à l’échelle des pixels.</span><span class="sxs-lookup"><span data-stu-id="23fb7-282">If your user is viewing your images on a mobile device screen that is 500-pixels-wide, there is really no point in sending a 1500-pixel-wide image.</span></span>  <span data-ttu-id="23fb7-283">Idéalement, vous envoyez une image de 500 pixels, le plus souvent.</span><span class="sxs-lookup"><span data-stu-id="23fb7-283">Ideally, you send a 500-pixel-wide image, at most.</span></span>  

1.  <span data-ttu-id="23fb7-284">Dans votre rapport, cliquez sur **éviter les charges utiles réseau énormes** pour voir les images qui doivent être redimensionnées.</span><span class="sxs-lookup"><span data-stu-id="23fb7-284">In your report, click **Avoid enormous network payloads** to see which images should be resized.</span></span>  <span data-ttu-id="23fb7-285">Il semble que 2 des fichiers jpg dépassent 2000 Ko, ce qui est plus grand que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="23fb7-285">It looks like 2 of the jpg files are over 2000 KB, which is bigger than necessary.</span></span>  
    
    <!--
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png" alt-text="Details about the properly size images opportunity" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png":::
       Details about the properly size images opportunity  
    :::image-end:::  
    -->
    
1.  <span data-ttu-id="23fb7-286">Dans l’onglet Éditeur, ouvrez `src/model.js` .</span><span class="sxs-lookup"><span data-stu-id="23fb7-286">Back in the editor tab, open `src/model.js`.</span></span>  
1.  <span data-ttu-id="23fb7-287">Remplacer `const dir = 'big'` par `const dir = 'small'` .</span><span class="sxs-lookup"><span data-stu-id="23fb7-287">Replace `const dir = 'big'` with `const dir = 'small'`.</span></span>  <span data-ttu-id="23fb7-288">Ce répertoire contient des copies des mêmes images qui ont été redimensionnées.</span><span class="sxs-lookup"><span data-stu-id="23fb7-288">This directory contains copies of the same images which have been resized.</span></span>  
1.  <span data-ttu-id="23fb7-289">Auditez de nouveau la page pour voir l’incidence de cette modification sur les performances de chargement.</span><span class="sxs-lookup"><span data-stu-id="23fb7-289">Audit the page again to see how this change affects load performance.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-compression-small-images-audits-performance.msft.png" alt-text="Rapport d’audit après le redimensionnement d’images" lightbox="../media/speed-glitch-compression-small-images-audits-performance.msft.png":::
       <span data-ttu-id="23fb7-291">Rapport d’audit après le redimensionnement d’images</span><span class="sxs-lookup"><span data-stu-id="23fb7-291">An Audits report after resizing images</span></span>  
    :::image-end:::  
    
<span data-ttu-id="23fb7-292">Il semble que la modification n’ait qu’une incidence mineure sur le score de performance global.</span><span class="sxs-lookup"><span data-stu-id="23fb7-292">Looks like the change only has a minor affect on the overall performance score.</span></span>  <span data-ttu-id="23fb7-293">Néanmoins, il n’y a pas de distinction entre le résultat et la quantité de données réseau que vous enregistrez pour vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="23fb7-293">However, one thing that the score does not show clearly is how much network data you are saving your users.</span></span>  <span data-ttu-id="23fb7-294">La taille totale de l’ancienne photo a été d’environ 5,3 Mo, alors qu’il n’y a que 0,18 mégaoctets.</span><span class="sxs-lookup"><span data-stu-id="23fb7-294">The total size of the old photos was around 5.3 megabytes, whereas now it is only about 0.18 megabytes.</span></span>  

#### <span data-ttu-id="23fb7-295">Redimensionnement d’images dans le monde réel</span><span class="sxs-lookup"><span data-stu-id="23fb7-295">Resizing images in the real world</span></span>   

<span data-ttu-id="23fb7-296">Dans le cas d’une petite application, il est possible de redimensionner une seule fois comme suit.</span><span class="sxs-lookup"><span data-stu-id="23fb7-296">For a small app, doing a one-off resize like this may be good enough.</span></span>  <span data-ttu-id="23fb7-297">Néanmoins, dans le cas d’une application de grande taille, cette solution n’est pas évolutive.</span><span class="sxs-lookup"><span data-stu-id="23fb7-297">But for a large app, this obviously is not scalable.</span></span>  <span data-ttu-id="23fb7-298">Voici quelques stratégies de gestion des images dans les applications volumineuses:</span><span class="sxs-lookup"><span data-stu-id="23fb7-298">Here are some strategies for managing images in large apps:</span></span>  

*   <span data-ttu-id="23fb7-299">Redimensionnez les images lors de votre processus de génération.</span><span class="sxs-lookup"><span data-stu-id="23fb7-299">Resize images during your build process.</span></span>  
*   <span data-ttu-id="23fb7-300">Créez plusieurs tailles de chaque image lors du processus de génération, puis utilisez-la `srcset` dans votre code.</span><span class="sxs-lookup"><span data-stu-id="23fb7-300">Create multiple sizes of each image during the build process and then use `srcset` in your code.</span></span>  <span data-ttu-id="23fb7-301">Lors de l’exécution, le navigateur s’occupe de choisir la taille la mieux appropriée pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="23fb7-301">At runtime, the browser takes care of choosing which size is best for the device.</span></span>  
    <!--See [Relative-sized images][relative].  -->
    
<!--[relative]: /web/fundamentals/design-and-ux/responsive/images#relative_sized_images  -->  

*   <span data-ttu-id="23fb7-302">Utilisez un CDN d’image qui vous permet de redimensionner dynamiquement une image lorsque vous la demandez.</span><span class="sxs-lookup"><span data-stu-id="23fb7-302">Use an image CDN that lets you dynamically resize an image when you request it.</span></span>  
*   <span data-ttu-id="23fb7-303">Optimisez chaque image au moins.</span><span class="sxs-lookup"><span data-stu-id="23fb7-303">At the very least, optimize each image.</span></span>  <span data-ttu-id="23fb7-304">Cela risque de créer des économies considérables.</span><span class="sxs-lookup"><span data-stu-id="23fb7-304">This may create huge savings.</span></span>  
  <span data-ttu-id="23fb7-305">L’optimisation consiste à exécuter une image par le biais d’un programme spécial qui réduit la taille du fichier image.</span><span class="sxs-lookup"><span data-stu-id="23fb7-305">Optimization is when you run an image through a special program that reduces the size of the image file.</span></span>  <span data-ttu-id="23fb7-306">Pour plus d’informations, voir [optimisation d’image essentielle][EssentialImageOptimization] .</span><span class="sxs-lookup"><span data-stu-id="23fb7-306">See [Essential Image Optimization][EssentialImageOptimization] for more tips.</span></span>  
    
### <span data-ttu-id="23fb7-307">Éliminer les ressources de blocage des rendez-vous</span><span class="sxs-lookup"><span data-stu-id="23fb7-307">Eliminate render-blocking resources</span></span>   

<span data-ttu-id="23fb7-308">Votre dernier État dit qu’il est impossible d’éliminer les ressources de blocage de rendu.</span><span class="sxs-lookup"><span data-stu-id="23fb7-308">Your latest report says that eliminating render-blocking resources is now the biggest opportunity.</span></span>  

<span data-ttu-id="23fb7-309">Une ressource de blocage de rendu est un fichier JavaScript ou CSS externe que le navigateur doit télécharger, analyser et exécuter avant d’afficher la page.</span><span class="sxs-lookup"><span data-stu-id="23fb7-309">A render-blocking resource is an external JavaScript or CSS file that the browser must download, parse, and run before it displays the page.</span></span>  <span data-ttu-id="23fb7-310">L’objectif est d’exécuter uniquement le code CSS principal et le code JavaScript requis pour afficher la page correctement.</span><span class="sxs-lookup"><span data-stu-id="23fb7-310">The goal is to only run the core CSS and JavaScript code that is required to display the page properly.</span></span>  

<span data-ttu-id="23fb7-311">La première tâche consiste à trouver le code que vous n’avez pas besoin de réexécuter sur le chargement de la page.</span><span class="sxs-lookup"><span data-stu-id="23fb7-311">The first task, then, is to find code that you do not need to run on page load.</span></span>  

1.  <span data-ttu-id="23fb7-312">Sélectionnez **éliminer les ressources de blocage de rendu** pour afficher les ressources qui se bloquent:</span><span class="sxs-lookup"><span data-stu-id="23fb7-312">Select **Eliminate render-blocking resources** to see the resources that are blocking:</span></span>  
    `lodash.js` <span data-ttu-id="23fb7-313">et `jquery.js` .</span><span class="sxs-lookup"><span data-stu-id="23fb7-313">and `jquery.js`.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png" alt-text="Plus d’informations sur l’opportunité de suppression des ressources de blocage de rendu" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png":::
       <span data-ttu-id="23fb7-315">Plus d’informations sur l’opportunité de **suppression des ressources de blocage de rendu**</span><span class="sxs-lookup"><span data-stu-id="23fb7-315">More information about the **Eliminate render-blocking resources** opportunity</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="23fb7-316">Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le menu de commandes, commencez à taper `Coverage` , puis sélectionnez **afficher la couverture**.</span><span class="sxs-lookup"><span data-stu-id="23fb7-316">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, start typing `Coverage`, and then select **Show Coverage**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-command-coverage.msft.png" alt-text="Ouvrir le menu de commandes à partir du volet audits" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-command-coverage.msft.png":::
       <span data-ttu-id="23fb7-318">Ouvrir le menu de commandes à partir du volet **audits**</span><span class="sxs-lookup"><span data-stu-id="23fb7-318">Open the Command Menu from the **Audits** panel</span></span>  
    :::image-end:::  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png" alt-text="Onglet couverture" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png":::
       <span data-ttu-id="23fb7-320">Onglet **couverture**</span><span class="sxs-lookup"><span data-stu-id="23fb7-320">The **Coverage** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="23fb7-321">Sélectionnez **Actualiser** /actualiser ![ ][ImageRefreshIcon] .</span><span class="sxs-lookup"><span data-stu-id="23fb7-321">Select **Refresh** \(![Refresh][ImageRefreshIcon]\).</span></span>  <span data-ttu-id="23fb7-322">L’onglet **couverture** fournit une vue d’ensemble de la quantité de code `bundle.js` `jquery.js` et `lodash.js` s’exécute pendant le chargement de la page.</span><span class="sxs-lookup"><span data-stu-id="23fb7-322">The **Coverage** tab provides an overview of how much of the code in `bundle.js`, `jquery.js`, and `lodash.js` runs while the page loads.</span></span>  <span data-ttu-id="23fb7-323">Dans l’illustration ci-dessous, à propos de 76% et de 30% des fichiers jQuery et Lodash ne sont pas utilisés, respectivement.</span><span class="sxs-lookup"><span data-stu-id="23fb7-323">In the figure after the following, about 76% and 30% of the jQuery and Lodash files are not used, respectively.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage-reloaded.msft.png" alt-text="Rapport de couverture" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage-reloaded.msft.png":::
       <span data-ttu-id="23fb7-325">Rapport de couverture</span><span class="sxs-lookup"><span data-stu-id="23fb7-325">The Coverage report</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="23fb7-326">Sélectionnez la ligne **jquery.js** .</span><span class="sxs-lookup"><span data-stu-id="23fb7-326">Select the **jquery.js** row.</span></span>  <span data-ttu-id="23fb7-327">DevTools ouvre le fichier dans le volet sources.</span><span class="sxs-lookup"><span data-stu-id="23fb7-327">DevTools opens the file in the Sources panel.</span></span>  <span data-ttu-id="23fb7-328">Une ligne de code a été exécutée si une barre bleue est située en regard.</span><span class="sxs-lookup"><span data-stu-id="23fb7-328">A line of code ran if it has a blue bar next to it.</span></span>  <span data-ttu-id="23fb7-329">Une barre rouge signifie qu’elle n’a pas été exécutée et qu’elle n’est pas nécessaire sur le chargement de la page.</span><span class="sxs-lookup"><span data-stu-id="23fb7-329">A red bar means it was not run, and is definitely not needed on page load.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png" alt-text="Affichage du fichier jQuery dans le panneau sources" lightbox="../media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png":::
       <span data-ttu-id="23fb7-331">Affichage du fichier jQuery dans le panneau **sources**</span><span class="sxs-lookup"><span data-stu-id="23fb7-331">Viewing the jQuery file in the **Sources** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="23fb7-332">Parcourez un bit du code jQuery.</span><span class="sxs-lookup"><span data-stu-id="23fb7-332">Scroll through the jQuery code a bit.</span></span>  <span data-ttu-id="23fb7-333">Voici quelques-unes des lignes qui s’exécutent uniquement en commentaires.</span><span class="sxs-lookup"><span data-stu-id="23fb7-333">Some of the lines that get "run" are actually just comments.</span></span>  <span data-ttu-id="23fb7-334">L’exécution de ce code par le biais d’un Minifier qui tire des commentaires est une autre façon de réduire la taille de ce fichier.</span><span class="sxs-lookup"><span data-stu-id="23fb7-334">Running this code through a minifier that strips comments is another way to reduce the size of this file.</span></span>  

<span data-ttu-id="23fb7-335">En résumé, lorsque vous utilisez votre propre code, l’onglet couverture vous permet d’analyser votre code, ligne par ligne, et d’expédier uniquement le code nécessaire au chargement de la page.</span><span class="sxs-lookup"><span data-stu-id="23fb7-335">In short, when you are working with your own code, the Coverage tab helps you analyze your code, line-by-line, and only ship the code that is needed for page load.</span></span>  

<span data-ttu-id="23fb7-336">Les fichiers et sont-ils `jquery.js` `lodash.js` même nécessaires pour le chargement de la page?</span><span class="sxs-lookup"><span data-stu-id="23fb7-336">Are the `jquery.js` and `lodash.js` files even needed to load the page?</span></span>  <span data-ttu-id="23fb7-337">L’onglet de blocage de requête indique ce qui se produit lorsque les ressources ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="23fb7-337">The Request Blocking tab displays what happens when resources are not available.</span></span>  

1.  <span data-ttu-id="23fb7-338">Sélectionnez l’onglet **Network (réseau** ).</span><span class="sxs-lookup"><span data-stu-id="23fb7-338">Select the **Network** tab.</span></span>  
1.  <span data-ttu-id="23fb7-339">Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir de nouveau le menu de commandes.</span><span class="sxs-lookup"><span data-stu-id="23fb7-339">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu again.</span></span>  
1.  <span data-ttu-id="23fb7-340">Commencez à taper `blocking` , puis sélectionnez **afficher le blocage de requête**.</span><span class="sxs-lookup"><span data-stu-id="23fb7-340">Start typing `blocking` and then select **Show Request Blocking**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png" alt-text="Onglet requête de blocage" lightbox="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png":::
       <span data-ttu-id="23fb7-342">Onglet **requête de blocage**</span><span class="sxs-lookup"><span data-stu-id="23fb7-342">The **Request Blocking** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="23fb7-343">Sélectionnez **Ajouter un modèle** \ ( ![ Ajouter un modèle ][ImageAddPatternIcon] \), tapez `/libs/*` , puis appuyez sur `Enter` pour confirmer.</span><span class="sxs-lookup"><span data-stu-id="23fb7-343">Select **Add Pattern** \(![Add Pattern][ImageAddPatternIcon]\), type `/libs/*`, and then press `Enter` to confirm.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png" alt-text="Ajouter un modèle pour bloquer toute demande de l’annuaire de bibliothèques" lightbox="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png":::
       <span data-ttu-id="23fb7-345">Ajouter un modèle pour bloquer toute demande de l' `libs` Annuaire</span><span class="sxs-lookup"><span data-stu-id="23fb7-345">Add a pattern to block any request to the `libs` directory</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="23fb7-346">Actualisez la page.</span><span class="sxs-lookup"><span data-stu-id="23fb7-346">Refresh the page.</span></span>  <span data-ttu-id="23fb7-347">Les requêtes jQuery et Lodash sont rouges, ce qui signifie que les requêtes ont été bloquées.</span><span class="sxs-lookup"><span data-stu-id="23fb7-347">The jQuery and Lodash requests are red, meaning that the requests were blocked.</span></span>   <span data-ttu-id="23fb7-348">Étant donné que la page est toujours chargée et qu’elle est interactive, il semblerait que les ressources suivantes ne soient pas nécessaires.</span><span class="sxs-lookup"><span data-stu-id="23fb7-348">The page still loads and is interactive, so it looks like these resources are not needed whatsoever!</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-reloaded-drawer-request-blocking-added.msft.png" alt-text="Le volet réseau indique que les requêtes ont été bloquées." lightbox="../media/speed-glitch-tony-remix-updated-network-reloaded-drawer-request-blocking-added.msft.png":::
       <span data-ttu-id="23fb7-350">Le volet **réseau** indique que les requêtes ont été bloquées.</span><span class="sxs-lookup"><span data-stu-id="23fb7-350">The **Network** panel shows that the requests have been blocked</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="23fb7-351">Sélectionnez **Supprimer tous les modèles** \ ( ![ Supprimer tous les modèles ][ImageRemoveIcon] \) pour supprimer le `/libs/*` modèle de blocage.</span><span class="sxs-lookup"><span data-stu-id="23fb7-351">Select **Remove all patterns** \(![Remove all patterns][ImageRemoveIcon]\) to delete the `/libs/*` blocking pattern.</span></span>  
    
<span data-ttu-id="23fb7-352">En règle générale, l’onglet blocage de requête est utile pour simuler le comportement de votre page quand une ressource donnée n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="23fb7-352">In general, the Request Blocking tab is useful for simulating how your page behaves when any given resource is not available.</span></span>  

<span data-ttu-id="23fb7-353">À présent, supprimez les références à ces fichiers du code et auditez de nouveau la page:</span><span class="sxs-lookup"><span data-stu-id="23fb7-353">Now, remove the references to these files from the code and audit the page again:</span></span>  

1.  <span data-ttu-id="23fb7-354">Dans l’onglet Éditeur, ouvrez `template.html` .</span><span class="sxs-lookup"><span data-stu-id="23fb7-354">Back in the editor tab, open `template.html`.</span></span>  
1.  <span data-ttu-id="23fb7-355">Supprimez les éléments `<script src="/libs/lodash.js">` et `<script src="/libs/jquery.js"></script>`.</span><span class="sxs-lookup"><span data-stu-id="23fb7-355">Delete `<script src="/libs/lodash.js">` and `<script src="/libs/jquery.js"></script>`.</span></span>  
1.  <span data-ttu-id="23fb7-356">Attendez que le site soit recréé et redéploiement.</span><span class="sxs-lookup"><span data-stu-id="23fb7-356">Wait for the site to re-build and re-deploy.</span></span>  
1.  <span data-ttu-id="23fb7-357">Auditez de nouveau la page à partir du volet **vérifications** .</span><span class="sxs-lookup"><span data-stu-id="23fb7-357">Audit the page again from the **Audits** panel.</span></span>  <span data-ttu-id="23fb7-358">Votre score global devrait de nouveau s’améliorer.</span><span class="sxs-lookup"><span data-stu-id="23fb7-358">Your overall score should have improved again.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-2-audits-performance.msft.png" alt-text="Rapport d’audit après la suppression des ressources de blocage de rendu" lightbox="../media/speed-glitch-tony-remix-updated-2-audits-performance.msft.png":::
       <span data-ttu-id="23fb7-360">Rapport **d’audit** après la suppression des ressources de blocage de rendu</span><span class="sxs-lookup"><span data-stu-id="23fb7-360">An **Audits** report after removing the render-blocking resources</span></span>  
    :::image-end:::  
    
#### <span data-ttu-id="23fb7-361">Optimisation du chemin de rendu critique dans le monde réel</span><span class="sxs-lookup"><span data-stu-id="23fb7-361">Optimizing the Critical Rendering Path in the real-world</span></span>   

<span data-ttu-id="23fb7-362">Le **chemin de rendu critique** fait référence au code dont vous avez besoin pour charger une page.</span><span class="sxs-lookup"><span data-stu-id="23fb7-362">The **Critical Rendering Path** refers to the code that you need to load a page.</span></span>  <span data-ttu-id="23fb7-363">En règle générale, accélérez le chargement de la page en ne disportant que le code Critical pendant le chargement de la page, puis en chargeant en différé tout le reste.</span><span class="sxs-lookup"><span data-stu-id="23fb7-363">In general, speed up page load by only shipping critical code during the page load, and then lazy-loading everything else.</span></span>  

<!--[CRP]: /web/fundamentals/performance/critical-rendering-path/  -->  

*   <span data-ttu-id="23fb7-364">Il est peu probable que vous puissiez retrouver les scripts que vous pouvez supprimer d’un certain temps, mais il se peut que vous trouviez de nombreux scripts que vous n’avez pas besoin de demander pendant le chargement de la page, et qu’ils puissent être demandés de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="23fb7-364">It is unlikely that you are able to find scripts that you are able to remove outright, but you may find many scripts that you do not need to request during the page load, and instead may be requested asynchronously.</span></span>  <!--See [Using async or defer][async].  -->  
*   <span data-ttu-id="23fb7-365">Si vous utilisez un Framework, vérifiez qu’il dispose du mode de production.</span><span class="sxs-lookup"><span data-stu-id="23fb7-365">If you are using a framework, check if it has a production mode.</span></span>  <span data-ttu-id="23fb7-366">Ce mode peut utiliser une fonctionnalité telle que l’agitation de l' [arborescence][WebpackTreeShaking] afin d’éliminer le code inutile qui bloque le rendu critique.</span><span class="sxs-lookup"><span data-stu-id="23fb7-366">This mode may use a feature such as [tree shaking][WebpackTreeShaking] in order to eliminate unnecessary code that is blocking the critical render.</span></span>  
    
<!--[async]: /web/fundamentals/performance/optimizing-content-efficiency/loading-third-party-javascript/#use_async_or_defer  -->  

### <span data-ttu-id="23fb7-367">Réduire le fonctionnement du thread principal</span><span class="sxs-lookup"><span data-stu-id="23fb7-367">Do less main thread work</span></span>   

<span data-ttu-id="23fb7-368">Votre dernier État montre quelques réductions potentielles mineurs dans la section opportunités, mais si vous examinez la section Diagnostics, il semble que le plus grand goulet d’étranglement soit trop important pour le thread principal.</span><span class="sxs-lookup"><span data-stu-id="23fb7-368">Your latest report shows some minor potential savings in the Opportunities section, but if you look down in the Diagnostics section, it looks like the biggest bottleneck is too much main thread activity.</span></span>  

<span data-ttu-id="23fb7-369">Le thread principal est l’endroit où le navigateur exécute la majeure partie du processus d’affichage d’une page, telle que l’analyse et l’exécution de HTML, CSS et JavaScript.</span><span class="sxs-lookup"><span data-stu-id="23fb7-369">The main thread is where the browser does most of the work needed to display a page, such as parsing and running HTML, CSS, and JavaScript.</span></span>  

<span data-ttu-id="23fb7-370">L’objectif consiste à utiliser le panneau performance pour analyser le travail effectué par le thread principal pendant le chargement de la page, et Rechercher des moyens de différer ou de supprimer le travail inutile.</span><span class="sxs-lookup"><span data-stu-id="23fb7-370">The goal is to use the Performance panel to analyze what work the main thread is doing while the page loads, and find ways to defer or remove unnecessary work.</span></span>  

1.  <span data-ttu-id="23fb7-371">Sélectionnez l’onglet **performance** .</span><span class="sxs-lookup"><span data-stu-id="23fb7-371">Select the **Performance** tab.</span></span>  
1.  <span data-ttu-id="23fb7-372">Sélectionnez **paramètres de capture** \ ( ![ paramètres de capture ][ImageCaptureIcon] \).</span><span class="sxs-lookup"><span data-stu-id="23fb7-372">Select **Capture Settings** \(![Capture Settings][ImageCaptureIcon]\).</span></span>  
1.  <span data-ttu-id="23fb7-373">Définissez **réseau** sur **lente réseau 3G** et **UC** à **6**ralentis.</span><span class="sxs-lookup"><span data-stu-id="23fb7-373">Set **Network** to **Slow 3G** and **CPU** to **6x slowdown**.</span></span>  <span data-ttu-id="23fb7-374">Les appareils mobiles présentent généralement plus de contraintes matérielles que les ordinateurs portables ou de bureau, de sorte que ces paramètres vous permettent de vous familiariser avec le chargement de la page comme si vous utilisiez un appareil moins puissant.</span><span class="sxs-lookup"><span data-stu-id="23fb7-374">Mobile devices typically have more hardware constraints than laptops or desktops, so these settings let you experience the page load as if you were using a less powerful device.</span></span>  
1.  <span data-ttu-id="23fb7-375">Sélectionnez **Actualiser** /actualiser ![ ][ImageRefreshIcon] .</span><span class="sxs-lookup"><span data-stu-id="23fb7-375">Select **Refresh** \(![Refresh][ImageRefreshIcon]\).</span></span>  <span data-ttu-id="23fb7-376">DevTools actualise la page, puis produit une visualisation de tout le temps exécuté pour le chargement de la page.</span><span class="sxs-lookup"><span data-stu-id="23fb7-376">DevTools refreshes the page and then produces a visualization of all the work performed in order to load the page.</span></span>  <span data-ttu-id="23fb7-377">Cette visualisation est appelée **suivi**.</span><span class="sxs-lookup"><span data-stu-id="23fb7-377">This visualization is referred to as the **trace**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png" alt-text="Suivi du panneau de performance du chargement de la page" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png":::
       <span data-ttu-id="23fb7-379">Suivi du panneau de **performance** du chargement de la page</span><span class="sxs-lookup"><span data-stu-id="23fb7-379">The **Performance** panel trace of the page load</span></span>  
    :::image-end:::  
    
<span data-ttu-id="23fb7-380">Le suivi des activités est affiché dans un ordre chronologique, de gauche à droite.</span><span class="sxs-lookup"><span data-stu-id="23fb7-380">The trace shows activity chronologically, from left to right.</span></span>  <span data-ttu-id="23fb7-381">Les graphiques FPS, UC et NET en haut offrent une vue d’ensemble des images par seconde, de l’activité de l’UC et de l’activité du réseau.</span><span class="sxs-lookup"><span data-stu-id="23fb7-381">The FPS, CPU, and NET charts at the top give you an overview of frames per second, CPU activity, and network activity.</span></span>  <span data-ttu-id="23fb7-382">Le bloc de jaune sélectionné que vous voyez dans la figure après ce qui suit, l’UC était entièrement chargée avec l’activité de script.</span><span class="sxs-lookup"><span data-stu-id="23fb7-382">The block of yellow selected that you see in the figure after the following, the CPU was completely busy with scripting activity.</span></span>  <span data-ttu-id="23fb7-383">C’est une idée qu’il est possible que vous puissiez accélérer le chargement de la page en effectuant moins de tâches JavaScript.</span><span class="sxs-lookup"><span data-stu-id="23fb7-383">This is a clue that you may be able to speed up page load by doing less JavaScript work.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png" alt-text="Section vue d’ensemble du suivi" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png":::
   <span data-ttu-id="23fb7-385">Section vue d’ensemble du suivi</span><span class="sxs-lookup"><span data-stu-id="23fb7-385">The Overview section of the trace</span></span>  
:::image-end:::  

<span data-ttu-id="23fb7-386">Examinez la trace pour trouver des moyens d’effectuer moins de tâches JavaScript:</span><span class="sxs-lookup"><span data-stu-id="23fb7-386">Investigate the trace to find ways to do less JavaScript work:</span></span>  

1.  <span data-ttu-id="23fb7-387">Sélectionnez la section **minutage** pour la développer.</span><span class="sxs-lookup"><span data-stu-id="23fb7-387">Select the **Timings** section to expand it.</span></span>  <span data-ttu-id="23fb7-388">En fonction du fait qu’il est possible qu’il y ait quelques mesures de [temporisation][MDNUserTimingApi] , il semble que l’application Thomas utilise le mode développement de réaction.</span><span class="sxs-lookup"><span data-stu-id="23fb7-388">Based on the fact that there may be a bunch of [Timings][MDNUserTimingApi] measures from React, it seems like Tony's app is using the development mode of React.</span></span>  <span data-ttu-id="23fb7-389">Basculer vers le mode de production de réagisser risque de générer un service de performance plus simple.</span><span class="sxs-lookup"><span data-stu-id="23fb7-389">Switching to the production mode of React may yield some easy performance wins.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings.msft.png" alt-text="Section minutage" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings.msft.png":::
       <span data-ttu-id="23fb7-391">Section **minutage**</span><span class="sxs-lookup"><span data-stu-id="23fb7-391">The **Timings** section</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="23fb7-392">Sélectionnez de nouveau **minutages** pour réduire cette section.</span><span class="sxs-lookup"><span data-stu-id="23fb7-392">Select **Timings** again to collapse that section.</span></span>  
1.  <span data-ttu-id="23fb7-393">Naviguez dans la section **principale** .</span><span class="sxs-lookup"><span data-stu-id="23fb7-393">Browse the **Main** section.</span></span>  <span data-ttu-id="23fb7-394">Cette section présente un journal chronologique de l’activité principale du thread, de gauche à droite.</span><span class="sxs-lookup"><span data-stu-id="23fb7-394">This section shows a chronological log of main thread activity, from left to right.</span></span>  <span data-ttu-id="23fb7-395">L’axe y (de haut en bas) montre pourquoi des événements s’est produit.</span><span class="sxs-lookup"><span data-stu-id="23fb7-395">The y-axis (top to bottom) shows why events occurred.</span></span>  <span data-ttu-id="23fb7-396">Par exemple, dans le figyre après ce qui suit, l' `Evaluate Script` événement a entraîné l’exécution de la fonction, ce qui a provoqué son exécution, `(anonymous)` `(anonymous)` `__webpack__require__` et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="23fb7-396">For example, in the figyre after the following, the `Evaluate Script` event caused the `(anonymous)` function to run, which caused `(anonymous)` to run, which caused `__webpack__require__` to run, and so on.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png" alt-text="Section principale" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png":::
       <span data-ttu-id="23fb7-398">Section **principale**</span><span class="sxs-lookup"><span data-stu-id="23fb7-398">The **Main** section</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="23fb7-399">Faites défiler vers le bas jusqu’en bas de la section **principale** .</span><span class="sxs-lookup"><span data-stu-id="23fb7-399">Scroll down to the bottom of the **Main** section.</span></span>  <span data-ttu-id="23fb7-400">Lorsque vous utilisez une infrastructure, la majeure partie de l’activité la plus grande est provoquée par l’infrastructure, qui est généralement hors de votre contrôle.</span><span class="sxs-lookup"><span data-stu-id="23fb7-400">When you use a framework, most of the upper activity is caused by the framework, which is usually out of your control.</span></span>  <span data-ttu-id="23fb7-401">L’activité générée par votre application est généralement située en bas.</span><span class="sxs-lookup"><span data-stu-id="23fb7-401">The activity caused by your app is usually at the bottom.</span></span>  <span data-ttu-id="23fb7-402">Dans cette application, il semble qu’une fonction nommée `App` génère un grand nombre de requêtes sur une `mineBitcoin` fonction.</span><span class="sxs-lookup"><span data-stu-id="23fb7-402">In this app, it seems like a function named `App` is causing a lot of requests to a `mineBitcoin` function.</span></span>  <span data-ttu-id="23fb7-403">Il semble que Thomas utilise les appareils de ses fans pour cryptocurrency...</span><span class="sxs-lookup"><span data-stu-id="23fb7-403">It sounds like Tony might be using the devices of his fans to mine cryptocurrency...</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png" alt-text="Pointez sur l’activité mineBitcoin" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png":::
       <span data-ttu-id="23fb7-405">Pointez sur l' `mineBitcoin` activité</span><span class="sxs-lookup"><span data-stu-id="23fb7-405">Hover on the `mineBitcoin` activity</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="23fb7-406">Bien que les requêtes que votre infrastructure effectue généralement hors de votre contrôle, il est possible que vous puissiez structurer votre application de manière à ce que l’infrastructure s’exécute de manière inefficace.</span><span class="sxs-lookup"><span data-stu-id="23fb7-406">Although the requests that your framework makes are usually out of your control, sometimes you may structure your app in a way that causes the framework to run inefficiently.</span></span>  <span data-ttu-id="23fb7-407">La restructuration de votre application pour qu’elle utilise efficacement l’infrastructure est un moyen de réduire le coût de fonctionnement du thread principal.</span><span class="sxs-lookup"><span data-stu-id="23fb7-407">Restructuring your app to use the framework efficiently is a way to do less main thread work.</span></span>  <span data-ttu-id="23fb7-408">Toutefois, cela nécessite une compréhension approfondie du fonctionnement de l’infrastructure et le type de modification que vous effectuez dans votre propre code afin d’utiliser l’infrastructure plus efficacement.</span><span class="sxs-lookup"><span data-stu-id="23fb7-408">However, this requires a deep understanding of how your framework works, and what kind of changes you make in your own code in order to use the framework more efficiently.</span></span>  
    
1.  <span data-ttu-id="23fb7-409">Développez la section **de haut en bas** .</span><span class="sxs-lookup"><span data-stu-id="23fb7-409">Expand the **Bottom-Up** section.</span></span>  <span data-ttu-id="23fb7-410">Dans cet onglet, les activités ont duré le plus longtemps.</span><span class="sxs-lookup"><span data-stu-id="23fb7-410">This tab breaks down what activities took up the most time.</span></span>  <span data-ttu-id="23fb7-411">S’il n’y a aucun élément dans la section de haut en bas, cliquez sur l’étiquette de la section **principale** .</span><span class="sxs-lookup"><span data-stu-id="23fb7-411">If you do not see anything in the Bottom-Up section, click the label for **Main** section.</span></span>  <span data-ttu-id="23fb7-412">La section **ascendante** affiche uniquement les informations relatives à l’activité, ou au groupe d’activité, que vous avez sélectionné.</span><span class="sxs-lookup"><span data-stu-id="23fb7-412">The **Bottom-Up** section only shows information for whatever activity, or group of activity, you have currently selected.</span></span>  <span data-ttu-id="23fb7-413">Par exemple, si vous avez cliqué sur une des `mineBitcoin` activités, la section de **bas en haut** consiste à afficher les informations relatives à cette activité unique.</span><span class="sxs-lookup"><span data-stu-id="23fb7-413">For example, if you clicked on one of the `mineBitcoin` activities, the **Bottom-Up** section is only going to show information for that one activity.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-summary-minebitcoin.msft.png" alt-text="Onglet inférieur" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-summary-minebitcoin.msft.png":::
       <span data-ttu-id="23fb7-415">Onglet **inférieur**</span><span class="sxs-lookup"><span data-stu-id="23fb7-415">The **Bottom-Up** tab</span></span>  
    :::image-end:::  
    
<span data-ttu-id="23fb7-416">La colonne **temps libre** vous indique le temps passé directement dans chaque activité.</span><span class="sxs-lookup"><span data-stu-id="23fb7-416">The **Self Time** column shows you how much time was spent directly in each activity.</span></span>  <span data-ttu-id="23fb7-417">Par exemple, dans l’illustration suivante, environ 63% du temps de thread principal a été dépensé sur la `mineBitcoin` fonction.</span><span class="sxs-lookup"><span data-stu-id="23fb7-417">For example, in the following figure, about 63% of main thread time was spent on the `mineBitcoin` function.</span></span>  

<span data-ttu-id="23fb7-418">Il est temps de voir si l’utilisation du mode de production et la réduction des activités JavaScript accélèrent le chargement de la page.</span><span class="sxs-lookup"><span data-stu-id="23fb7-418">Time to see whether using production mode and reducing JavaScript activity may speed up the page load.</span></span>  <span data-ttu-id="23fb7-419">Commencer avec le mode production:</span><span class="sxs-lookup"><span data-stu-id="23fb7-419">Start with production mode:</span></span>  

1.  <span data-ttu-id="23fb7-420">Dans l’onglet Éditeur, ouvrez `webpack.config.js` .</span><span class="sxs-lookup"><span data-stu-id="23fb7-420">In the editor tab, open `webpack.config.js`.</span></span>  
1.  <span data-ttu-id="23fb7-421">Remplacez `"mode":"development"` par `"mode":"production"` .</span><span class="sxs-lookup"><span data-stu-id="23fb7-421">Change `"mode":"development"` to `"mode":"production"`.</span></span>  
1.  <span data-ttu-id="23fb7-422">Attendez la fin du déploiement de la nouvelle Build.</span><span class="sxs-lookup"><span data-stu-id="23fb7-422">Wait for the new build to deploy.</span></span>  
1.  <span data-ttu-id="23fb7-423">Auditez de nouveau la page.</span><span class="sxs-lookup"><span data-stu-id="23fb7-423">Audit the page again.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-3-audits-performance.msft.png" alt-text="Rapport d’audit après la configuration de WebPack pour utiliser le mode de production" lightbox="../media/speed-glitch-tony-remix-updated-3-audits-performance.msft.png":::
       <span data-ttu-id="23fb7-425">Rapport d’audit après la configuration de WebPack pour utiliser le mode de production</span><span class="sxs-lookup"><span data-stu-id="23fb7-425">An Audits report after configuring webpack to use production mode</span></span>  
    :::image-end:::  
    
<span data-ttu-id="23fb7-426">Réduisez les activités JavaScript en supprimant la demande `mineBitcoin` :</span><span class="sxs-lookup"><span data-stu-id="23fb7-426">Reduce JavaScript activity by removing the request to `mineBitcoin`:</span></span>  

1.  <span data-ttu-id="23fb7-427">Dans l’onglet Éditeur, ouvrez `src/App.jsx` .</span><span class="sxs-lookup"><span data-stu-id="23fb7-427">In the editor tab, open `src/App.jsx`.</span></span>  
1.  <span data-ttu-id="23fb7-428">Transmettez la demande au `this.mineBitcoin(1500)` `constructor` .</span><span class="sxs-lookup"><span data-stu-id="23fb7-428">Comment out the request to `this.mineBitcoin(1500)` in the `constructor`.</span></span>  
1.  <span data-ttu-id="23fb7-429">Attendez la fin du déploiement de la nouvelle Build.</span><span class="sxs-lookup"><span data-stu-id="23fb7-429">Wait for the new build to deploy.</span></span>  
1.  <span data-ttu-id="23fb7-430">Auditez de nouveau la page.</span><span class="sxs-lookup"><span data-stu-id="23fb7-430">Audit the page again.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-4-audits-performance.msft.png" alt-text="Rapport de vérification après suppression du fonctionnement inutile de JavaScript" lightbox="../media/speed-glitch-tony-remix-updated-4-audits-performance.msft.png":::
       <span data-ttu-id="23fb7-432">Rapport de vérification après suppression du fonctionnement inutile de JavaScript</span><span class="sxs-lookup"><span data-stu-id="23fb7-432">An Audits report after removing unnecessary JavaScript work</span></span>  
    :::image-end:::  
    
<span data-ttu-id="23fb7-433">Il semble que le dernier changement ait entraîné un décalage massif de performances.</span><span class="sxs-lookup"><span data-stu-id="23fb7-433">Looks like that last change caused a massive jump in performance!</span></span>  

> [!NOTE]
> <span data-ttu-id="23fb7-434">Cette section proposait plutôt une présentation du panneau performance.</span><span class="sxs-lookup"><span data-stu-id="23fb7-434">This section provided a rather brief introduction to the Performance panel.</span></span>  <span data-ttu-id="23fb7-435">Pour en savoir plus sur l’analyse des performances des pages, voir référence sur l' [analyse des performances][DevtoolsEvaluatePerformanceReference] .</span><span class="sxs-lookup"><span data-stu-id="23fb7-435">See [Performance Analysis Reference][DevtoolsEvaluatePerformanceReference] to learn more about how to analyze page performance.</span></span>  

<!--todo: add section when available -->  

#### <span data-ttu-id="23fb7-436">Exécution moins importante du thread principal dans le monde réel</span><span class="sxs-lookup"><span data-stu-id="23fb7-436">Doing less main thread work in the real world</span></span>   

<span data-ttu-id="23fb7-437">En règle générale, le panneau **performance** est le moyen le plus courant de comprendre l’activité que votre site effectue au chargement et les manières de supprimer les activités inutiles.</span><span class="sxs-lookup"><span data-stu-id="23fb7-437">In general, the **Performance** panel is the most common way to understand what activity your site does as it loads, and find ways to remove unnecessary activity.</span></span>  

<span data-ttu-id="23fb7-438">Si vous préférez une approche qui ressemble davantage à celle- `console.log()` ci, l' [API de minutage des utilisateurs][MDNUserTimingApi] vous permet de marquer de façon arbitraire certaines phases du cycle de vie de votre application afin d’effectuer le suivi de la durée de chacune de ces phases.</span><span class="sxs-lookup"><span data-stu-id="23fb7-438">If you prefer an approach that feels more like `console.log()`, the [User Timing API][MDNUserTimingApi] enables you to arbitrarily mark up certain phases of your app lifecycle, in order to track how long each of those phases takes.</span></span>  

## <span data-ttu-id="23fb7-439">Résumé</span><span class="sxs-lookup"><span data-stu-id="23fb7-439">Summary</span></span>   

*   <span data-ttu-id="23fb7-440">Dès que vous avez fini d’optimiser les performances de chargement d’un site, commencez toujours par un audit.</span><span class="sxs-lookup"><span data-stu-id="23fb7-440">Whenever you set out to optimize the load performance of a site, always start with an audit.</span></span>  <span data-ttu-id="23fb7-441">L’audit établit un planning de référence et vous donne des conseils sur la manière d’améliorer.</span><span class="sxs-lookup"><span data-stu-id="23fb7-441">The audit establishes a baseline, and gives you tips on how to improve.</span></span>  
*   <span data-ttu-id="23fb7-442">Apportez une modification à la fois, puis auditez la page après chaque modification afin de savoir comment ce changement d’isolement a un impact sur les performances.</span><span class="sxs-lookup"><span data-stu-id="23fb7-442">Make one change at a time, and audit the page after each change in order to see how that isolated change affects performance.</span></span>  

<!--
## Next steps   

*   Run audits on your own site!  If you need help interpreting your report, or finding ways to improve your load performance, check out [Feedback](#feedback) for ways to get help from the DevTools community.  Stack Overflow, the mailing list, or Twitter are probably best for these types of questions.  
*   Please leave [feedback](#feedback) on this tutorial.  I really do use the data to make better tutorials for you.  
-->  

<!--  
  


-->  

<!-- image links -->  

[ImageAddPatternIcon]: ../media/add-pattern-icon.msft.png  
[ImageCaptureIcon]: ../media/capture-icon.msft.png  
[ImageLargeResourceRowsButtonIcon]: ../media/large-resource-rows-button-icon.msft.png  
[ImageMorePanelsIcon]: ../media/more-panels-icon.msft.png  
[ImagePerformIcon]: ../media/perform-icon.msft.png  
[ImageRefreshIcon]: ../media/reload-icon.msft.png  
[ImageRemoveIcon]: ../media/remove-icon.msft.png  
<!-- links -->  

[DevtoolsEvaluatePerformanceReference]: ../evaluate-performance/reference.md "Référence d’analyse des performances | Documents Microsoft"  

[CourseraIntroductionWebDevelopmentClass]: https://www.coursera.org/learn/web-development#syllabus "Présentation de la classe développement Web | Coursera"  

[EssentialImageOptimization]: https://images.guide "Optimisation d’image essentielle"  

[MDNContentEncodingDirectives]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Encoding#Directives "Directives-Content-Encoding | MDN"  
[MDNUserTimingApi]: https://developer.mozilla.org/docs/Web/API/User_Timing_API "API de minutage des utilisateurs | MDN"  

[WebpackTreeShaking]: https://webpack.js.org/guides/tree-shaking "Faire secousses de l’arborescence | Pack d’intercomposition"  

> [!NOTE]
> <span data-ttu-id="23fb7-449">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="23fb7-449">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="23fb7-450">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="23fb7-450">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="23fb7-452">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="23fb7-452">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
