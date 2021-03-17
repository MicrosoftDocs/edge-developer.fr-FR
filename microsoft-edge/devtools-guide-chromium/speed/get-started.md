---
description: Découvrez comment utiliser Microsoft Edge DevTools pour trouver des moyens d’accélérer la charge de vos sites web.
title: Optimiser la vitesse du site web avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 75c9df5d86ce994cebfda882a0adfa2664b6ec30
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439443"
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

# <a name="optimize-website-speed-with-microsoft-edge-devtools"></a><span data-ttu-id="aa6d6-104">Optimiser la vitesse du site web avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="aa6d6-104">Optimize website speed with Microsoft Edge DevTools</span></span>  

## <a name="goal-of-tutorial"></a><span data-ttu-id="aa6d6-105">Objectif du didacticiel</span><span class="sxs-lookup"><span data-stu-id="aa6d6-105">Goal of tutorial</span></span>  

<span data-ttu-id="aa6d6-106">Ce didacticiel vous apprend à utiliser Microsoft Edge DevTools pour trouver des moyens d’accélérer la charge de vos sites web.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-106">This tutorial teaches you how to use Microsoft Edge DevTools to find ways to make your websites load faster.</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="aa6d6-107">Prérequis</span><span class="sxs-lookup"><span data-stu-id="aa6d6-107">Prerequisites</span></span>  

*   <span data-ttu-id="aa6d6-108">Vous devez avoir une expérience de développement web de base, semblable à ce qui est appris dans cette [classe Introduction au développement Web.][CourseraIntroductionWebDevelopmentClass]</span><span class="sxs-lookup"><span data-stu-id="aa6d6-108">You should have basic web development experience, similar to what is taught in this [Introduction to Web Development class][CourseraIntroductionWebDevelopmentClass].</span></span>  
*   <span data-ttu-id="aa6d6-109">Vous n’avez rien à savoir sur les performances de chargement.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-109">You do not need to know anything about load performance.</span></span>  <span data-ttu-id="aa6d6-110">Vous en apprendrez davantage à ce sujet dans ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-110">You learn about it in this tutorial.</span></span>  

## <a name="introduction"></a><span data-ttu-id="aa6d6-111">Introduction</span><span class="sxs-lookup"><span data-stu-id="aa6d6-111">Introduction</span></span>  

<span data-ttu-id="aa6d6-112">Il s’agit de Tony.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-112">This is Tony.</span></span>  <span data-ttu-id="aa6d6-113">Tony est très moderne dans la société des chats.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-113">Tony is very famous in cat society.</span></span>  <span data-ttu-id="aa6d6-114">Il a créé un site web pour que ses fans puissent en savoir plus sur son favori.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-114">He has built a website so that his fans are able to learn about his favorite foods.</span></span>  <span data-ttu-id="aa6d6-115">Ses fans aiment le site, mais Tony ne cesse d’entendre des plaintes concernant le chargement lent du site.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-115">His fans love the site, but Tony keeps hearing complaints that the site loads slowly.</span></span>  <span data-ttu-id="aa6d6-116">Tony vous a demandé de l’aider à accélérer le site.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-116">Tony has asked you to help him speed the site up.</span></span>  

:::image type="complex" source="../media/speed-tony.msft.png" alt-text="Tony le chat" lightbox="../media/speed-tony.msft.png":::
   <span data-ttu-id="aa6d6-118">Tony le chat</span><span class="sxs-lookup"><span data-stu-id="aa6d6-118">Tony the cat</span></span>  
:::image-end:::  

## <a name="step-1-audit-the-site"></a><span data-ttu-id="aa6d6-119">Étape 1 : Auditer le site</span><span class="sxs-lookup"><span data-stu-id="aa6d6-119">Step 1: Audit the site</span></span>  

<span data-ttu-id="aa6d6-120">Chaque fois que vous définissez pour améliorer les performances de charge d’un site, **commencez toujours par un audit.**</span><span class="sxs-lookup"><span data-stu-id="aa6d6-120">Whenever you set out to improve the load performance of a site, **always start with an audit**.</span></span>  
<span data-ttu-id="aa6d6-121">L’audit a 2 fonctions importantes :</span><span class="sxs-lookup"><span data-stu-id="aa6d6-121">The audit has 2 important functions:</span></span>  

*   <span data-ttu-id="aa6d6-122">Il crée une ligne **de** base pour vous aider à mesurer les modifications ultérieures.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-122">It creates a **baseline** for you to measure subsequent changes against.</span></span>  
*   <span data-ttu-id="aa6d6-123">Il vous donne des **conseils actionnables** sur les modifications qui ont le plus d’impact.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-123">It gives you **actionable tips** on what changes have the most impact.</span></span>  
    
### <a name="set-up"></a><span data-ttu-id="aa6d6-124">Configuration</span><span class="sxs-lookup"><span data-stu-id="aa6d6-124">Set up</span></span>  

<span data-ttu-id="aa6d6-125">Tout d’abord, vous devez configurer le site afin de pouvoir y apporter des modifications ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-125">First, you must set up the site so that you are able to make changes to it later.</span></span>  

1.  <span data-ttu-id="aa6d6-126">[Ouvrez le code source pour le site.](https://glitch.com/edit/#!/tony)</span><span class="sxs-lookup"><span data-stu-id="aa6d6-126">[Open the source code for the site](https://glitch.com/edit/#!/tony).</span></span>  <span data-ttu-id="aa6d6-127">Cet onglet est appelé « onglet **éditeur**».</span><span class="sxs-lookup"><span data-stu-id="aa6d6-127">This tab is referred to as the **editor tab**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-server-js.msft.png" alt-text="Onglet Éditeur" lightbox="../media/speed-glitch-tony-server-js.msft.png":::
       <span data-ttu-id="aa6d6-129">Onglet **Éditeur**</span><span class="sxs-lookup"><span data-stu-id="aa6d6-129">The **editor tab**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="aa6d6-130">Choose **tony**.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-130">Choose **tony**.</span></span>  <span data-ttu-id="aa6d6-131">Un menu s’affiche.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-131">A menu appears.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-server-js-remix-project.msft.png" alt-text="Menu qui s’affiche après le choix de Tony" lightbox="../media/speed-glitch-tony-server-js-remix-project.msft.png":::
       <span data-ttu-id="aa6d6-133">Menu qui s’affiche après le choix de **Tony**</span><span class="sxs-lookup"><span data-stu-id="aa6d6-133">The menu that appears after choosing **tony**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="aa6d6-134">Sélectionnez **Projet DeNte**.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-134">Choose **Remix Project**.</span></span>  <span data-ttu-id="aa6d6-135">Le nom du projet change de **Tony** à un nom généré de manière aléatoire.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-135">The name of the project changes from **tony** to some randomly-generated name.</span></span>  <span data-ttu-id="aa6d6-136">Vous avez maintenant votre propre copie modifiable du code.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-136">You now have your own editable copy of the code.</span></span>  <span data-ttu-id="aa6d6-137">Plus tard, vous pouvez apporter des modifications à ce code.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-137">Later on, you may make changes to this code.</span></span>  
1.  <span data-ttu-id="aa6d6-138">Choose **Show** and choose **In a New Window**.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-138">Choose **Show** and choose **In a New Window**.</span></span>  <span data-ttu-id="aa6d6-139">La démonstration s’ouvre dans un nouvel onglet.  Cet onglet est appelé « **onglet de démonstration**».  Le chargement du site peut prendre un certain temps.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-139">The demo opens in a new tab.  This tab is be referred to as the **demo tab**.  It may take a while for the site to load.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-show-live.msft.png" alt-text="Onglet démonstration" lightbox="../media/speed-glitch-tony-show-live.msft.png":::
       <span data-ttu-id="aa6d6-141">Onglet démonstration</span><span class="sxs-lookup"><span data-stu-id="aa6d6-141">The demo tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="aa6d6-142">Sélectionnez `Control` + `Shift` + `J` \(Windows, Linux\) ou `Command` + `Option` + `J` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="aa6d6-142">Select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  <span data-ttu-id="aa6d6-143">Microsoft Edge DevTools s’ouvre en même temps que la démonstration.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-143">Microsoft Edge DevTools opens up alongside the demo.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-show-live-console.msft.png" alt-text="DevTools et la démonstration" lightbox="../media/speed-glitch-tony-show-live-console.msft.png":::
       <span data-ttu-id="aa6d6-145">DevTools et la démonstration</span><span class="sxs-lookup"><span data-stu-id="aa6d6-145">DevTools and the demo</span></span>  
    :::image-end:::  
    
<span data-ttu-id="aa6d6-146">Pour le reste des captures d’écran de ce didacticiel, DevTools est affiché dans une fenêtre distincte.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-146">For the rest of the screenshots in this tutorial, DevTools is shown in a separate window.</span></span>  <span data-ttu-id="aa6d6-147">Sélectionnez `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\) `Undock` \*\*\*\* pour ouvrir le menu Commande, en tapant, puis en sélectionnant Undock dans une fenêtre distincte.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-147">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, typing `Undock`, and then selecting **Undock into separate window**.</span></span>  

:::image type="complex" source="../media/speed-console.msft.png" alt-text="DevTools non barraté" lightbox="../media/speed-console.msft.png":::
   <span data-ttu-id="aa6d6-149">DevTools non barraté</span><span class="sxs-lookup"><span data-stu-id="aa6d6-149">Undocked DevTools</span></span>  
:::image-end:::  

### <a name="establish-a-baseline"></a><span data-ttu-id="aa6d6-150">Établir une ligne de base</span><span class="sxs-lookup"><span data-stu-id="aa6d6-150">Establish a baseline</span></span>  

<span data-ttu-id="aa6d6-151">La ligne de base est un enregistrement de la façon dont le site a été exécuté avant d’apporter des améliorations de performances.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-151">The baseline is a record of how the site performed before you made any performance improvements.</span></span>  

1.  <span data-ttu-id="aa6d6-152">Choisissez **l’outil Audits.**</span><span class="sxs-lookup"><span data-stu-id="aa6d6-152">Choose the **Audits** tool.</span></span>  <span data-ttu-id="aa6d6-153">Il peut être masqué derrière le **bouton Plus de panneaux** \( ![ Plus de ](../media/more-panels-icon.msft.png) panneaux \).</span><span class="sxs-lookup"><span data-stu-id="aa6d6-153">It may be hidden behind the **More Panels** \(![More Panels](../media/more-panels-icon.msft.png)\) button.</span></span>  <span data-ttu-id="aa6d6-154">Ce panneau présente une partie du panneau, car le projet qui alimente le panneau Audits s’appelle **Le Chef d’équipe**.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-154">There is a Lighthouse on this panel because the project that powers the Audits panel is named **Lighthouse**.</span></span>  
    
    [!INCLUDE [audits-panel-note](../includes/audits-panel-note.md)]  
    
    :::image type="complex" source="../media/speed-audits-performance.msft.png" alt-text="Outil Audits" lightbox="../media/speed-audits-performance.msft.png":::
       <span data-ttu-id="aa6d6-156">Outil **Audits**</span><span class="sxs-lookup"><span data-stu-id="aa6d6-156">The **Audits** tool</span></span>  
    :::image-end:::  
    
    <!--todo: add link to Lighthouse when section is available  -->  
    <!-- /web/tools/lighthouse  -->  
    
1.  <span data-ttu-id="aa6d6-157">Correspondez à vos paramètres de configuration d’audit à ceux de la figure précédente.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-157">Match your audit configuration settings to those in the previous figure.</span></span>  <span data-ttu-id="aa6d6-158">Voici une explication des différentes options :</span><span class="sxs-lookup"><span data-stu-id="aa6d6-158">Here is an explanation of the different options:</span></span>  
    
    *   <span data-ttu-id="aa6d6-159">**Appareil**.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-159">**Device**.</span></span>  <span data-ttu-id="aa6d6-160">Définir sur **Mobile** modifie la chaîne de l’agent utilisateur et simule une vue mobile.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-160">Set to **Mobile** changes the user agent string and simulates a mobile viewport.</span></span>  <span data-ttu-id="aa6d6-161">Définir sur **Bureau** ne fait que éteindre les **modifications mobiles.**</span><span class="sxs-lookup"><span data-stu-id="aa6d6-161">Set to **Desktop** pretty much just turns off the **Mobile** changes.</span></span>  
    *   <span data-ttu-id="aa6d6-162">**Audits**.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-162">**Audits**.</span></span>  <span data-ttu-id="aa6d6-163">Désactiver une catégorie pour empêcher le panneau **Audits** d’exécution de ces audits et exclut ces audits de votre rapport.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-163">Turn off a category to prevent the **Audits** panel from running those audits, and excludes those audits from your report.</span></span>  <span data-ttu-id="aa6d6-164">Laissez les autres catégories désactivées si vous souhaitez afficher les types de recommandations fournis.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-164">Leave the other categories Turned on, if you want to display the types of recommendations that are provided.</span></span>  <span data-ttu-id="aa6d6-165">Désactiver les catégories pour accélérer légèrement le processus d’audit.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-165">Turn off categories to slightly speed up the auditing process.</span></span>  
    *   <span data-ttu-id="aa6d6-166">**Limitation**.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-166">**Throttling**.</span></span>  <span data-ttu-id="aa6d6-167">Définie sur **Simulated Slow 4G, 4x CPU Slow** simule les conditions de navigation classiques sur un appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-167">Set to **Simulated Slow 4G, 4x CPU Slowdown** simulates the typical conditions of browsing on a mobile device.</span></span>  <span data-ttu-id="aa6d6-168">Il est nommé « simulé », car le panneau Audits n’est pas réellement limitée pendant le processus d’audit.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-168">It is named "simulated" because the Audits panel does not actually throttle during the auditing process.</span></span>  <span data-ttu-id="aa6d6-169">Au lieu de cela, il extrapole simplement la durée de chargement de la page dans des conditions mobiles.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-169">Instead, it just extrapolates how long the page takes to load under mobile conditions.</span></span>  <span data-ttu-id="aa6d6-170">En **revanche,** le paramètre Appliqué... permet de limiter votre processeur et votre réseau, avec le compromis d’un processus d’audit plus long.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-170">The **Applied...** setting, on the other hand, actually throttles your CPU and network, with the tradeoff of a longer auditing process.</span></span>  
    *   <span data-ttu-id="aa6d6-171">**Effacer le stockage**.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-171">**Clear Storage**.</span></span>  <span data-ttu-id="aa6d6-172">Activer la case à cocher pour effacer tout le stockage associé à la page avant chaque audit.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-172">Turn on the checkbox to clear all storage associated with the page before every audit.</span></span>  <span data-ttu-id="aa6d6-173">Laissez ce paramètre sur si vous souhaitez auditer la façon dont les visiteurs ront la première expérience de votre site.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-173">Leave this setting on if you want to audit how first-time visitors experience your site.</span></span>  <span data-ttu-id="aa6d6-174">Désactiver ce paramètre lorsque vous souhaitez l’expérience de répétition de visite.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-174">Turn off this setting when you want the repeat-visit experience.</span></span>  
    
1.  <span data-ttu-id="aa6d6-175">Choose **Run Audits**.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-175">Choose **Run Audits**.</span></span>  <span data-ttu-id="aa6d6-176">Après 10 à 30 **secondes,** le panneau Audits affiche un rapport sur les performances du site.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-176">After 10 to 30 seconds, the **Audits** panel displays a report of the performance of the site.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png" alt-text="Rapport pour le panneau Audits des performances du site" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png":::
       <span data-ttu-id="aa6d6-178">Rapport pour le panneau Audits des performances du site</span><span class="sxs-lookup"><span data-stu-id="aa6d6-178">The report for the Audits panel of the performance of the site</span></span>  
    :::image-end:::  
    
#### <a name="handling-report-errors"></a><span data-ttu-id="aa6d6-179">Gestion des erreurs de rapport</span><span class="sxs-lookup"><span data-stu-id="aa6d6-179">Handling report errors</span></span>  

<span data-ttu-id="aa6d6-180">Si vous obtenez une erreur dans votre rapport du panneau Audits, essayez d’exécutez l’onglet de démonstration à partir d’une fenêtre **InPrivate** sans aucun autre onglet ouvert.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-180">If you ever get an error in your Audits panel report, try running the demo tab from an **InPrivate** window with no other tabs open.</span></span>  <span data-ttu-id="aa6d6-181">Cela garantit que vous exécutez Microsoft Edge à partir d’un état propre.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-181">This ensures that you are running Microsoft Edge from a clean state.</span></span>  <span data-ttu-id="aa6d6-182">Les extensions Microsoft Edge en particulier interfèrent souvent avec le processus d’audit.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-182">Microsoft Edge Extensions in particular often interfere with the auditing process.</span></span>  

<!--todo: add screen capture for error in audit -->  
<!--
:::image type="complex" source="../media/speed-.msft.png" alt-text="A report that errored" lightbox="../media/speed-.msft.png":::
   A report that errored  
:::image-end:::  
-->  

### <a name="understand-your-report"></a><span data-ttu-id="aa6d6-183">Comprendre votre rapport</span><span class="sxs-lookup"><span data-stu-id="aa6d6-183">Understand your report</span></span>  

<span data-ttu-id="aa6d6-184">Le nombre en haut de votre rapport est le score de performances global du site.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-184">The number at the top of your report is the overall performance score for the site.</span></span>  <span data-ttu-id="aa6d6-185">Plus tard, au cours des modifications apportées au code, le nombre affiché doit augmenter.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-185">Later, as you make changes to the code, the number displayed should rise.</span></span>  <span data-ttu-id="aa6d6-186">Un score plus élevé signifie de meilleures performances.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-186">A higher score means better performance.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png" alt-text="Le score de performances global" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png":::
   <span data-ttu-id="aa6d6-188">Le score de performances global</span><span class="sxs-lookup"><span data-stu-id="aa6d6-188">The overall performance score</span></span>  
:::image-end:::  

<span data-ttu-id="aa6d6-189">La section **Mesures** fournit des mesures quantifias des performances du site.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-189">The **Metrics** section provides quantitative measurements of the performance of the site.</span></span>  <span data-ttu-id="aa6d6-190">Chaque métrique fournit un aperçu d’un aspect différent des performances.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-190">Each metric provides insight into a different aspect of the performance.</span></span>  <span data-ttu-id="aa6d6-191">Par exemple, **First Contentful Paint** vous indique quand le contenu est peint pour la première fois à l’écran, ce qui est un jalon important dans la perception de l’utilisateur du chargement de la page, tandis que **Time To Interactive** marque le point auquel la page apparaît suffisamment prête pour gérer les interactions utilisateur.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-191">For example, **First Contentful Paint** tells you when content is first painted to the screen, which is an important milestone in the user's perception of the page load, whereas **Time To Interactive** marks the point at which the page appears ready enough to handle user interactions.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png" alt-text="Section Mesures" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png":::
   <span data-ttu-id="aa6d6-193">Section **Mesures**</span><span class="sxs-lookup"><span data-stu-id="aa6d6-193">The **Metrics** section</span></span>  
:::image-end:::  

<span data-ttu-id="aa6d6-194">Sélectionnez le bouton bascule mis en surbrillon dans la \*\*\*\* figure suivante pour afficher une description pour chaque métrique, puis sélectionnez En savoir plus pour lire la documentation à ce sujet.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-194">Choose the highlighted toggle button in the following figure to display a description for each metric, and choose **Learn More** to read documentation about it.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-expanded.msft.png" alt-text="Sélectionnez le bouton bascule mis en surbrillon pour développer les éléments Mesures" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-expanded.msft.png":::
   <span data-ttu-id="aa6d6-196">Sélectionnez le bouton bascule mis en surbrillon pour développer les éléments Mesures</span><span class="sxs-lookup"><span data-stu-id="aa6d6-196">Choose the highlighted toggle button to expand the Metrics items</span></span>  
:::image-end:::  

<span data-ttu-id="aa6d6-197">Les mesures ci-dessous sont une collection de captures d’écran qui vous montrent à quoi ressemble la page telle qu’elle a été chargée.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-197">Below Metrics is a collection of screenshots that show you how the page looked as it loaded.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png" alt-text="Captures d’écran de l’aperçu de la page lors du chargement" lightbox="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png":::
   <span data-ttu-id="aa6d6-199">Captures d’écran de l’aperçu de la page lors du chargement</span><span class="sxs-lookup"><span data-stu-id="aa6d6-199">Screenshots of how the page looked while loading</span></span>  
:::image-end:::  

<span data-ttu-id="aa6d6-200">La section **Opportunités** fournit des conseils spécifiques sur l’amélioration des performances de charge de cette page spécifique.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-200">The **Opportunities** section provides specific tips on how to improve the load performance of this specific page.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png" alt-text="Section Opportunités" lightbox="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png":::
   <span data-ttu-id="aa6d6-202">Section **Opportunités**</span><span class="sxs-lookup"><span data-stu-id="aa6d6-202">The **Opportunities** section</span></span>  
:::image-end:::  

<span data-ttu-id="aa6d6-203">Choisissez l’opportunité d’en savoir plus à ce sujet.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-203">Choose an opportunity to learn more about it.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png" alt-text="Éliminer les opportunités de ressources de blocage de rendu" lightbox="../media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png":::
   <span data-ttu-id="aa6d6-205">**Éliminer les opportunités de ressources de blocage de rendu**</span><span class="sxs-lookup"><span data-stu-id="aa6d6-205">**Eliminate render-blocking resources** opportunity</span></span>  
:::image-end:::  

<span data-ttu-id="aa6d6-206">Choose **Learn More** to display documentation about why an opportunity is important, and specific recommendations on how to fix it.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-206">Choose **Learn More** to display documentation about why an opportunity is important, and specific recommendations on how to fix it.</span></span>  

:::image type="complex" source="../media/speed-web-dev-performance-audits.msft.png" alt-text="Documentation relative à l’élimination des ressources de blocage du rendu" lightbox="../media/speed-web-dev-performance-audits.msft.png":::
   <span data-ttu-id="aa6d6-208">Documentation relative à **l’élimination des ressources de blocage du rendu**</span><span class="sxs-lookup"><span data-stu-id="aa6d6-208">Documentation for the **Eliminate render-blocking resources** opportunity</span></span>  
:::image-end:::  

<span data-ttu-id="aa6d6-209">La section **Diagnostics** fournit plus d’informations sur les facteurs qui contribuent au temps de chargement de la page.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-209">The **Diagnostics** section provides more information about factors that contribute to the load time of the page.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png" alt-text="Section Diagnostics" lightbox="../media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png":::
   <span data-ttu-id="aa6d6-211">Section **Diagnostics**</span><span class="sxs-lookup"><span data-stu-id="aa6d6-211">The **Diagnostics** section</span></span>  
:::image-end:::  

<span data-ttu-id="aa6d6-212">La section **Audits passés** vous montre ce que le site fait correctement.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-212">The **Passed Audits** section shows you what the site is doing correctly.</span></span>  <span data-ttu-id="aa6d6-213">Choisissez de développer la section.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-213">Choose to expand the section.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png" alt-text="Section Audits passés" lightbox="../media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png":::
   <span data-ttu-id="aa6d6-215">Section **Audits passés**</span><span class="sxs-lookup"><span data-stu-id="aa6d6-215">The **Passed Audits** section</span></span>  
:::image-end:::  

## <a name="step-2-experiment"></a><span data-ttu-id="aa6d6-216">Étape 2 : Expérimenter</span><span class="sxs-lookup"><span data-stu-id="aa6d6-216">Step 2: Experiment</span></span>  

<span data-ttu-id="aa6d6-217">La section Opportunités de votre rapport d’audit vous donne des conseils pour améliorer les performances de la page.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-217">The Opportunities section of your audit report gives you tips on how to improve the performance of the page.</span></span>  <span data-ttu-id="aa6d6-218">Dans cette section, vous implémentez les modifications recommandées sur la base de code, en auditant le site après chaque modification afin de mesurer l’impact sur la vitesse du site.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-218">In this section, you implement the recommended changes to the codebase, auditing the site after each change to measure how it affects site speed.</span></span>  

### <a name="enable-text-compression"></a><span data-ttu-id="aa6d6-219">Activer la compression de texte</span><span class="sxs-lookup"><span data-stu-id="aa6d6-219">Enable text compression</span></span>  

<span data-ttu-id="aa6d6-220">Votre rapport indique que le fait d’éviter d’importantes charges utiles réseau est l’une des meilleures opportunités pour améliorer les performances de la page.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-220">Your report says that avoiding enormous network payloads is one of the top opportunities for improving the performance of the page.</span></span>  <span data-ttu-id="aa6d6-221">L’activation de la compression de texte est une opportunité d’améliorer les performances de la page.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-221">Enabling text compression is an opportunity to improve the performance of the page.</span></span>  

<span data-ttu-id="aa6d6-222">La compression de texte consiste à réduire ou compresser la taille d’un fichier texte avant de l’envoyer sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-222">Text compression is when you reduce, or compress, the size of a text file before sending it over the network.</span></span>  <span data-ttu-id="aa6d6-223">Semblable à la façon dont vous pouvez archiver un répertoire avant de l’envoyer pour réduire la taille.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-223">Similar to how you may archive a directory before sending it to reduce the size.</span></span>  

<span data-ttu-id="aa6d6-224">Avant d’activer la compression, voici quelques méthodes pour vérifier manuellement si les ressources de texte sont compressées.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-224">Before you enable compression, here are a couple of ways to manually check whether text resources are compressed.</span></span>  

1.  <span data-ttu-id="aa6d6-225">Choisissez **l’outil** Réseau.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-225">Choose the **Network** tool.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network.msft.png" alt-text="Panneau réseau" lightbox="../media/speed-glitch-tony-remix-network.msft.png":::
       <span data-ttu-id="aa6d6-227">Outil **Réseau**</span><span class="sxs-lookup"><span data-stu-id="aa6d6-227">The **Network** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="aa6d6-228">Sélectionnez **l’icône Paramètre** réseau.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-228">Choose the **Network setting** icon.</span></span>  
1.  <span data-ttu-id="aa6d6-229">Cochez **la case Utiliser les lignes De grandes demandes.**</span><span class="sxs-lookup"><span data-stu-id="aa6d6-229">Choose the **Use Large Request Rows** checkbox.</span></span>  <span data-ttu-id="aa6d6-230">La hauteur des lignes du tableau des demandes réseau augmente.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-230">The height of the rows in the table of network requests increases.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-use-large-request-rows.msft.png" alt-text="Lignes de grande taille dans le tableau des demandes réseau" lightbox="../media/speed-glitch-tony-remix-network-use-large-request-rows.msft.png":::
       <span data-ttu-id="aa6d6-232">Lignes de grande taille dans le tableau des demandes réseau</span><span class="sxs-lookup"><span data-stu-id="aa6d6-232">Large rows in the network requests table</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="aa6d6-233">Si la **colonne Taille** dans le tableau des demandes réseau n’est pas affichée, choisissez l’en-tête de tableau > **Taille**.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-233">If the **Size** column in the table of network requests is not displayed, choose the table header > **Size**.</span></span>  

<span data-ttu-id="aa6d6-234">Chaque **cellule Size** affiche deux valeurs.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-234">Each **Size** cell shows two values.</span></span>  <span data-ttu-id="aa6d6-235">La valeur supérieure est la taille de la ressource téléchargée.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-235">The top value is the size of the downloaded resource.</span></span>  
<span data-ttu-id="aa6d6-236">La valeur inférieure est la taille de la ressource non compressée.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-236">The bottom value is the size of the uncompressed resource.</span></span>  <span data-ttu-id="aa6d6-237">Si les deux valeurs sont identiques, la ressource n’est pas compressée lorsqu’elle est envoyée sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-237">If the two values are the same, then the resource is not being compressed when it is sent over the network.</span></span>  <span data-ttu-id="aa6d6-238">Par exemple, dans la figure précédente, les valeurs supérieure et inférieure de `bundle.js` sont `1.2 MB` et `1.2 MB` .</span><span class="sxs-lookup"><span data-stu-id="aa6d6-238">For example, in the previous figure, the top and bottom values for `bundle.js` are `1.2 MB` and `1.2 MB`.</span></span>  

<span data-ttu-id="aa6d6-239">Vérifiez la compression en inspectant les en-têtes HTTP d’une ressource :</span><span class="sxs-lookup"><span data-stu-id="aa6d6-239">Check for compression by inspecting the HTTP headers of a resource:</span></span>  

1.  <span data-ttu-id="aa6d6-240">Choose `bundle.js` .</span><span class="sxs-lookup"><span data-stu-id="aa6d6-240">Choose `bundle.js`.</span></span>  
1.  <span data-ttu-id="aa6d6-241">Choisissez le **panneau En-têtes.**</span><span class="sxs-lookup"><span data-stu-id="aa6d6-241">Choose the **Headers** panel.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png" alt-text="Panneau En-têtes" lightbox="../media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png":::
       <span data-ttu-id="aa6d6-243">Panneau **En-têtes**</span><span class="sxs-lookup"><span data-stu-id="aa6d6-243">The **Headers** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="aa6d6-244">Recherchez **un en-tête dans** la section `content-encoding` En-têtes de réponse.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-244">Search the **Response Headers** section for a `content-encoding` header.</span></span>  <span data-ttu-id="aa6d6-245">Un `content-encoding` titre n’est pas affiché, ce qui signifie `bundle.js` qu’il n’a pas été compressé.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-245">A `content-encoding` heading is not displayed, meaning that `bundle.js` was not compressed.</span></span>  <span data-ttu-id="aa6d6-246">Lorsqu’une ressource est compressée, cet en-tête est généralement définie sur `gzip` `deflate` , ou `br` .</span><span class="sxs-lookup"><span data-stu-id="aa6d6-246">When a resource is compressed, this header is usually set to `gzip`, `deflate`, or `br`.</span></span>  <span data-ttu-id="aa6d6-247">Pour obtenir une explication des valeurs, accédez à [Directives.][MDNContentEncodingDirectives]</span><span class="sxs-lookup"><span data-stu-id="aa6d6-247">For an explanation of the values, navigate to [Directives][MDNContentEncodingDirectives].</span></span>  

<span data-ttu-id="aa6d6-248">Suffisamment avec les explications.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-248">Enough with the explanations.</span></span>  <span data-ttu-id="aa6d6-249">Il est temps d’apporter des modifications.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-249">Time to make some changes.</span></span>  <span data-ttu-id="aa6d6-250">Activez la compression de texte en ajoutant quelques lignes de code :</span><span class="sxs-lookup"><span data-stu-id="aa6d6-250">Enable text compression by adding a couple of lines of code:</span></span>  

1.  <span data-ttu-id="aa6d6-251">Dans l’onglet Éditeur, \*\* choisissezserver.js\*\*.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-251">In the editor tab, choose **server.js**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-server-js.msft.png" alt-text="Modifier server.js" lightbox="../media/speed-glitch-tony-remix-server-js.msft.png":::
       <span data-ttu-id="aa6d6-253">Edit</span><span class="sxs-lookup"><span data-stu-id="aa6d6-253">Edit</span></span> `server.js`  
    :::image-end:::  
    
1.  <span data-ttu-id="aa6d6-254">Ajoutez le code suivant à **server.js**.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-254">Add the following code to **server.js**.</span></span>  <span data-ttu-id="aa6d6-255">Veillez à le `app.use(compression())` placer avant `app.use(express.static('build'))` .</span><span class="sxs-lookup"><span data-stu-id="aa6d6-255">Make sure to put `app.use(compression())` before `app.use(express.static('build'))`.</span></span>  

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
    > <span data-ttu-id="aa6d6-256">En règle générale, vous devez installer le package via quelque chose comme `compression` , mais cela a déjà été fait pour `npm i -S compression` vous.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-256">Usually, you have to install the `compression` package via something like `npm i -S compression`, but this has already been done for you.</span></span>  
    
1.  <span data-ttu-id="aa6d6-257">Attendez que Glitch déploie la nouvelle build du site.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-257">Wait for Glitch to deploy the new build of the site.</span></span>  <span data-ttu-id="aa6d6-258">L’animation originale en de côté **des outils** signifie que le site est en cours de reconstruction et de redéploiement.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-258">The fancy animation next to **Tools** means that the site is getting rebuilt and redeployed.</span></span>  <span data-ttu-id="aa6d6-259">La modification est prête lorsque l’animation en de côté des **outils** disparaît.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-259">The change is ready when the animation next to **Tools** goes away.</span></span>  <span data-ttu-id="aa6d6-260">Choose **Show** and choose **In a New Window** again.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-260">Choose **Show** and choose **In a New Window** again.</span></span>  
    
    <!--
    :::image type="complex" source="../media/speed-glitch-tony-remix-server-js-edited.msft.png" alt-text="The animation that indicates that the site is getting built" lightbox="../media/speed-glitch-tony-remix-server-js-edited.msft.png":::
       The animation that indicates that the site is getting built  
    :::image-end:::  
    -->  
    
<span data-ttu-id="aa6d6-261">Utilisez les flux de travail que vous avez appris précédemment pour vérifier manuellement que la compression fonctionne :</span><span class="sxs-lookup"><span data-stu-id="aa6d6-261">Use the workflows that you learned earlier to manually check that the compression is working:</span></span>  

1.  <span data-ttu-id="aa6d6-262">Revenir à l’onglet de démonstration et actualiser la page.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-262">Go back to the demo tab and refresh the page.</span></span>  <span data-ttu-id="aa6d6-263">La **colonne Taille** doit maintenant afficher 2 valeurs différentes pour les ressources de texte telles que `bundle.js` .</span><span class="sxs-lookup"><span data-stu-id="aa6d6-263">The **Size** column should now show 2 different values for text resources like `bundle.js`.</span></span>  <span data-ttu-id="aa6d6-264">Dans la figure qui suit, la valeur supérieure de for est la taille du fichier qui a été envoyé sur le réseau, et la valeur inférieure est la taille de fichier non `256 KB` `bundle.js` `1.2 MB` compressée.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-264">In the figure after the following, the top value of `256 KB` for `bundle.js` is the size of the file that was sent over the network, and the bottom value of `1.2 MB` is the uncompressed file size.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-main.msft.png" alt-text="La colonne Taille affiche désormais 2 valeurs différentes pour les ressources de texte" lightbox="../media/speed-glitch-tony-remix-network-main.msft.png":::
       <span data-ttu-id="aa6d6-266">La **colonne Taille** affiche désormais 2 valeurs différentes pour les ressources de texte</span><span class="sxs-lookup"><span data-stu-id="aa6d6-266">The **Size** column now shows 2 different values for text resources</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="aa6d6-267">La section **En-têtes de** réponse `bundle.js` pour doit maintenant inclure un `content-encoding: gzip` en-tête.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-267">The **Response Headers** section for `bundle.js` should now include a `content-encoding: gzip` header.</span></span>
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png" alt-text="La section En-têtes de réponse contient désormais un en-tête d’encodage de contenu" lightbox="../media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png":::
       <span data-ttu-id="aa6d6-269">La section **En-têtes de** réponse contient désormais un en-tête d’encodage de contenu</span><span class="sxs-lookup"><span data-stu-id="aa6d6-269">The **Response Headers** section now contains a content-encoding header</span></span>  
    :::image-end:::  
    
<span data-ttu-id="aa6d6-270">Auditer à nouveau la page pour mesurer le type d’impact de la compression de texte sur les performances de charge de la page :</span><span class="sxs-lookup"><span data-stu-id="aa6d6-270">Audit the page again to measure what kind of impact text compression has on the load performance of the page:</span></span>  

1.  <span data-ttu-id="aa6d6-271">Choisissez **l’outil Audits.**</span><span class="sxs-lookup"><span data-stu-id="aa6d6-271">Choose the **Audits** tool.</span></span>  
1.  <span data-ttu-id="aa6d6-272">Choose **Perform an audit** \( Perform an audit ![ ](../media/perform-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="aa6d6-272">Choose **Perform an audit** \(![Perform an audit](../media/perform-icon.msft.png)\).</span></span>  
1.  <span data-ttu-id="aa6d6-273">Laissez les paramètres identiques qu’auparavant.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-273">Leave the settings the same as before.</span></span>  
1.  <span data-ttu-id="aa6d6-274">Choose **Run audit**.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-274">Choose **Run audit**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance.msft.png" alt-text="Un rapport Audits après activation de la compression de texte" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance.msft.png":::
       <span data-ttu-id="aa6d6-276">Un rapport Audits après activation de la compression de texte</span><span class="sxs-lookup"><span data-stu-id="aa6d6-276">An Audits report after enabling text compression</span></span>  
    :::image-end:::  
    
<!--  Woohoo!  That looks like progress.  -->  <span data-ttu-id="aa6d6-277">Votre score de performances global doit avoir augmenté, ce qui signifie que le site devient plus rapide.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-277">Your overall performance score should have increased, meaning that the site is getting faster.</span></span>  

#### <a name="text-compression-in-the-real-world"></a><span data-ttu-id="aa6d6-278">Compression de texte dans le monde réel</span><span class="sxs-lookup"><span data-stu-id="aa6d6-278">Text compression in the real world</span></span>  

<span data-ttu-id="aa6d6-279">La plupart des serveurs ont vraiment des correctifs simples comme celui-ci pour activer la compression !</span><span class="sxs-lookup"><span data-stu-id="aa6d6-279">Most servers really do have simple fixes like this for enabling compression!</span></span>  <span data-ttu-id="aa6d6-280">Il vous suffit d’effectuer une recherche sur la configuration du serveur que vous utilisez pour compresser du texte.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-280">Just do a search on how to configure whatever server you use to compress text.</span></span>  

### <a name="resize-images"></a><span data-ttu-id="aa6d6-281">Resize images</span><span class="sxs-lookup"><span data-stu-id="aa6d6-281">Resize images</span></span>  

<span data-ttu-id="aa6d6-282">Votre rapport indique que le fait d’éviter d’importantes charges utiles réseau est l’une des meilleures opportunités pour améliorer les performances de la page.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-282">Your report indicates that avoiding enormous network payloads is one of the top opportunities for improving the performance of the page.</span></span>  <span data-ttu-id="aa6d6-283">Le re dimensionnement des images permet de réduire la taille de la charge utile du réseau.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-283">Resizing images helps reduce the size of the network payload.</span></span>  <span data-ttu-id="aa6d6-284">Si votre utilisateur affiche vos images sur un écran d’appareil mobile de 500 pixels de large, l’envoi d’une image de 1 500 pixels ne sert à rien.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-284">If your user is viewing your images on a mobile device screen that is 500-pixels-wide, there is really no point in sending a 1500-pixel-wide image.</span></span>  <span data-ttu-id="aa6d6-285">Dans l’idéal, vous envoyez une image de 500 pixels au maximum.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-285">Ideally, you send a 500-pixel-wide image, at most.</span></span>  

1.  <span data-ttu-id="aa6d6-286">Dans votre rapport, choisissez **d’éviter** les charges utiles réseau importantes pour afficher les images à re tailler.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-286">In your report, choose **Avoid enormous network payloads** to display which images should be resized.</span></span>  <span data-ttu-id="aa6d6-287">Il semble que 2 des fichiers jpg font plus de 2 000 Ko, ce qui est plus important que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-287">It looks like 2 of the jpg files are over 2000 KB, which is bigger than necessary.</span></span>  
    
    <!--
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png" alt-text="Details about the properly size images opportunity" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png":::
       Details about the properly size images opportunity  
    :::image-end:::  
    -->
    
1.  <span data-ttu-id="aa6d6-288">De retour dans l’onglet Éditeur, ouvrez `src/model.js` .</span><span class="sxs-lookup"><span data-stu-id="aa6d6-288">Back in the editor tab, open `src/model.js`.</span></span>  
1.  <span data-ttu-id="aa6d6-289">Remplacez `const dir = 'big'` par `const dir = 'small'` .</span><span class="sxs-lookup"><span data-stu-id="aa6d6-289">Replace `const dir = 'big'` with `const dir = 'small'`.</span></span>  <span data-ttu-id="aa6d6-290">Ce répertoire contient des copies des mêmes images qui ont été reserrées.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-290">This directory contains copies of the same images which have been resized.</span></span>  
1.  <span data-ttu-id="aa6d6-291">Auditez de nouveau la page pour afficher l’impact de la modification sur les performances de charge.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-291">Audit the page again to display how the change affects load performance.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-compression-small-images-audits-performance.msft.png" alt-text="Un rapport Audits après re resserr des images" lightbox="../media/speed-glitch-compression-small-images-audits-performance.msft.png":::
       <span data-ttu-id="aa6d6-293">Un rapport Audits après re resserr des images</span><span class="sxs-lookup"><span data-stu-id="aa6d6-293">An Audits report after resizing images</span></span>  
    :::image-end:::  
    
<span data-ttu-id="aa6d6-294">La modification affichée n’a qu’un impact mineur sur le score de performances global.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-294">The change displays only has a minor affect on the overall performance score.</span></span>  <span data-ttu-id="aa6d6-295">Toutefois, une chose que le score ne montre pas clairement est la quantité de données réseau que vous économisez vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-295">However, one thing that the score does not show clearly is how much network data you are saving your users.</span></span>  <span data-ttu-id="aa6d6-296">La taille totale des anciennes photos était d’environ 5,3 mégaoctets, alors qu’elle n’est plus qu’environ 0,18 mégaoctets.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-296">The total size of the old photos was around 5.3 megabytes, whereas now it is only about 0.18 megabytes.</span></span>  

#### <a name="resizing-images-in-the-real-world"></a><span data-ttu-id="aa6d6-297">Re resizing images in the real world</span><span class="sxs-lookup"><span data-stu-id="aa6d6-297">Resizing images in the real world</span></span>  

<span data-ttu-id="aa6d6-298">Pour une petite application, une telle re taille peut être suffisante.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-298">For a small app, doing a one-off resize like this may be good enough.</span></span>  <span data-ttu-id="aa6d6-299">Mais pour une application de grande taille, ce n’est évidemment pas évolutif.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-299">But for a large app, this obviously is not scalable.</span></span>  <span data-ttu-id="aa6d6-300">Voici quelques stratégies de gestion des images dans les applications de grande taille :</span><span class="sxs-lookup"><span data-stu-id="aa6d6-300">Here are some strategies for managing images in large apps:</span></span>  

*   <span data-ttu-id="aa6d6-301">Resize images during your build process.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-301">Resize images during your build process.</span></span>  
*   <span data-ttu-id="aa6d6-302">Créez plusieurs tailles de chaque image pendant le processus de création, puis `srcset` utilisez-la dans votre code.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-302">Create multiple sizes of each image during the build process and then use `srcset` in your code.</span></span>  <span data-ttu-id="aa6d6-303">Au moment de l’utilisation, le navigateur s’occupe de choisir la taille la plus grande pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-303">At runtime, the browser takes care of choosing which size is best for the device.</span></span>  
    <!--Navigate to [Relative-sized images][relative].  -->
    
<!--[relative]: /web/fundamentals/design-and-ux/responsive/images#relative_sized_images  -->  

*   <span data-ttu-id="aa6d6-304">Utilisez un CDN d’image qui vous permet de re tailler dynamiquement une image lorsque vous la demandez.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-304">Use an image CDN that lets you dynamically resize an image when you request it.</span></span>  
*   <span data-ttu-id="aa6d6-305">Au minimum, optimisez chaque image.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-305">At the very least, optimize each image.</span></span>  <span data-ttu-id="aa6d6-306">Cela peut générer d’importantes économies.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-306">This may create huge savings.</span></span>  
  <span data-ttu-id="aa6d6-307">L’optimisation consiste à exécuter une image via un programme spécial qui réduit la taille du fichier image.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-307">Optimization is when you run an image through a special program that reduces the size of the image file.</span></span>  <span data-ttu-id="aa6d6-308">Pour plus d’informations, accédez à [Optimisation de l’image essentielle.][EssentialImageOptimization]</span><span class="sxs-lookup"><span data-stu-id="aa6d6-308">For more tips, navigate to [Essential Image Optimization][EssentialImageOptimization].</span></span>  
    
### <a name="eliminate-render-blocking-resources"></a><span data-ttu-id="aa6d6-309">Éliminer les ressources de blocage de rendu</span><span class="sxs-lookup"><span data-stu-id="aa6d6-309">Eliminate render-blocking resources</span></span>  

<span data-ttu-id="aa6d6-310">Votre dernier rapport indique que l’élimination des ressources de blocage de rendu est désormais la plus grande opportunité.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-310">Your latest report says that eliminating render-blocking resources is now the biggest opportunity.</span></span>  

<span data-ttu-id="aa6d6-311">Une ressource de blocage de rendu est un fichier JavaScript ou CSS externe que le navigateur doit télécharger, explorer et exécuter avant d’afficher la page.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-311">A render-blocking resource is an external JavaScript or CSS file that the browser must download, parse, and run before it displays the page.</span></span>  <span data-ttu-id="aa6d6-312">L’objectif est d’exécuter uniquement le code CSS et JavaScript principal requis pour afficher la page correctement.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-312">The goal is to only run the core CSS and JavaScript code that is required to display the page properly.</span></span>  

<span data-ttu-id="aa6d6-313">La première tâche consiste ensuite à trouver le code que vous n’avez pas besoin d’exécuter lors du chargement de la page.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-313">The first task, then, is to find code that you do not need to run on page load.</span></span>  

1.  <span data-ttu-id="aa6d6-314">Choisissez **Éliminer les ressources de blocage de rendu** pour afficher les ressources qui bloquent :</span><span class="sxs-lookup"><span data-stu-id="aa6d6-314">Choose **Eliminate render-blocking resources** to display the resources that are blocking:</span></span>  
    `lodash.js` <span data-ttu-id="aa6d6-315">et `jquery.js` .</span><span class="sxs-lookup"><span data-stu-id="aa6d6-315">and `jquery.js`.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png" alt-text="Plus d’informations sur l’opportunité d’éliminer les ressources de blocage de rendu" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png":::
       <span data-ttu-id="aa6d6-317">Plus d’informations sur **l’opportunité d’éliminer les ressources de blocage de rendu**</span><span class="sxs-lookup"><span data-stu-id="aa6d6-317">More information about the **Eliminate render-blocking resources** opportunity</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="aa6d6-318">Sélectionnez `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\) `Coverage` \*\*\*\* pour ouvrir le menu Commande, commencez à taper, puis choisissez Afficher la couverture.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-318">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, start typing `Coverage`, and then choose **Show Coverage**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-command-coverage.msft.png" alt-text="Ouvrir le menu Commande à partir du panneau Audits" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-command-coverage.msft.png":::
       <span data-ttu-id="aa6d6-320">Ouvrir le menu Commande à partir du **panneau Audits**</span><span class="sxs-lookup"><span data-stu-id="aa6d6-320">Open the Command Menu from the **Audits** panel</span></span>  
    :::image-end:::  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png" alt-text="L’outil Couverture" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png":::
       <span data-ttu-id="aa6d6-322">**L’outil Couverture**</span><span class="sxs-lookup"><span data-stu-id="aa6d6-322">The **Coverage** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="aa6d6-323">Choose **Refresh** \( ![ Refresh ](../media/reload-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="aa6d6-323">Choose **Refresh** \(![Refresh](../media/reload-icon.msft.png)\).</span></span>  <span data-ttu-id="aa6d6-324">**L’outil** Couverture fournit une vue d’ensemble de la quantité de code dans , et s’exécute pendant le chargement `bundle.js` de la `jquery.js` `lodash.js` page.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-324">The **Coverage** tool provides an overview of how much of the code in `bundle.js`, `jquery.js`, and `lodash.js` runs while the page loads.</span></span>  <span data-ttu-id="aa6d6-325">Dans la figure ci-après, environ 76 % et 30 % des fichiers jQuery et Lodash ne sont pas utilisés, respectivement.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-325">In the figure after the following, about 76% and 30% of the jQuery and Lodash files are not used, respectively.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage-reloaded.msft.png" alt-text="Rapport de couverture" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage-reloaded.msft.png":::
       <span data-ttu-id="aa6d6-327">Rapport de couverture</span><span class="sxs-lookup"><span data-stu-id="aa6d6-327">The Coverage report</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="aa6d6-328">Choisissez la **jquery.js** ligne.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-328">Choose the **jquery.js** row.</span></span>  <span data-ttu-id="aa6d6-329">DevTools ouvre le fichier dans le panneau Sources.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-329">DevTools opens the file in the Sources panel.</span></span>  <span data-ttu-id="aa6d6-330">Une ligne de code s’est en cours d’utilisation si une barre bleue est à côté de cette ligne.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-330">A line of code ran if it has a blue bar next to it.</span></span>  <span data-ttu-id="aa6d6-331">Une barre rouge signifie qu’elle n’a pas été exécuté et n’est absolument pas nécessaire lors du chargement de la page.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-331">A red bar means it was not run, and is definitely not needed on page load.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png" alt-text="Affichage du fichier jQuery dans le panneau Sources" lightbox="../media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png":::
       <span data-ttu-id="aa6d6-333">Affichage du fichier jQuery dans le **panneau Sources**</span><span class="sxs-lookup"><span data-stu-id="aa6d6-333">Viewing the jQuery file in the **Sources** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="aa6d6-334">Faites défiler un peu le code jQuery.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-334">Scroll through the jQuery code a bit.</span></span>  <span data-ttu-id="aa6d6-335">Certaines des lignes qui obtiennent « exécuter » ne sont en fait que des commentaires.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-335">Some of the lines that get "run" are actually just comments.</span></span>  <span data-ttu-id="aa6d6-336">L’exécution de ce code par le biais d’un minifier qui sous-dimensionnait les commentaires est une autre façon de réduire la taille de ce fichier.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-336">Running this code through a minifier that strips comments is another way to reduce the size of this file.</span></span>  

<span data-ttu-id="aa6d6-337">En bref, lorsque vous travaillez avec \*\*\*\* votre propre code, l’outil Couverture vous permet d’analyser votre code, ligne par ligne, et d’expédier uniquement le code nécessaire au chargement de la page.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-337">In short, when you are working with your own code, the **Coverage** tool helps you analyze your code, line-by-line, and only ship the code that is needed for page load.</span></span>  

<span data-ttu-id="aa6d6-338">Les fichiers `jquery.js` et les `lodash.js` fichiers sont-ils nécessaires pour charger la page ?</span><span class="sxs-lookup"><span data-stu-id="aa6d6-338">Are the `jquery.js` and `lodash.js` files even needed to load the page?</span></span>  <span data-ttu-id="aa6d6-339">**L’outil de blocage** des demandes affiche ce qui se produit lorsque les ressources ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-339">The **Request blocking** tool displays what happens when resources are not available.</span></span>  

1.  <span data-ttu-id="aa6d6-340">Choisissez **l’outil** Réseau.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-340">Choose the **Network** tool.</span></span>  
1.  <span data-ttu-id="aa6d6-341">Sélectionnez `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\) pour ouvrir à nouveau le menu commande.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-341">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu again.</span></span>  
1.  <span data-ttu-id="aa6d6-342">Commencez à `blocking` taper, puis choisissez **Afficher le blocage des demandes.**</span><span class="sxs-lookup"><span data-stu-id="aa6d6-342">Start typing `blocking` and then choose **Show Request Blocking**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png" alt-text="Outil de blocage des demandes" lightbox="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png":::
       <span data-ttu-id="aa6d6-344">Outil **de blocage des** demandes</span><span class="sxs-lookup"><span data-stu-id="aa6d6-344">The **Request blocking** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="aa6d6-345">Choose **Add Pattern** \( Add Pattern ![ ](../media/add-pattern-icon.msft.png) \), type , and then select `/libs/*` to `Enter` confirm.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-345">Choose **Add Pattern** \(![Add Pattern](../media/add-pattern-icon.msft.png)\), type `/libs/*`, and then select `Enter` to confirm.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png" alt-text="Ajouter un modèle pour bloquer toute demande dans le répertoire libs" lightbox="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png":::
       <span data-ttu-id="aa6d6-347">Ajouter un modèle pour bloquer toute demande à `libs` l’annuaire</span><span class="sxs-lookup"><span data-stu-id="aa6d6-347">Add a pattern to block any request to the `libs` directory</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="aa6d6-348">Actualisez la page.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-348">Refresh the page.</span></span>  <span data-ttu-id="aa6d6-349">Les demandes jQuery et Lodash sont rouges, ce qui signifie que les demandes ont été bloquées.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-349">The jQuery and Lodash requests are red, meaning that the requests were blocked.</span></span>   <span data-ttu-id="aa6d6-350">La page se charge toujours et est interactive. Il semble donc que ces ressources ne soient pas nécessaires !</span><span class="sxs-lookup"><span data-stu-id="aa6d6-350">The page still loads and is interactive, so it looks like these resources are not needed whatsoever!</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-reloaded-drawer-request-blocking-added.msft.png" alt-text="Le panneau Réseau indique que les demandes ont été bloquées" lightbox="../media/speed-glitch-tony-remix-updated-network-reloaded-drawer-request-blocking-added.msft.png":::
       <span data-ttu-id="aa6d6-352">**L’outil** Réseau indique que les demandes ont été bloquées</span><span class="sxs-lookup"><span data-stu-id="aa6d6-352">The **Network** tool shows that the requests have been blocked</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="aa6d6-353">Choose **Remove all patterns** \( ![ Remove all patterns ](../media/remove-icon.msft.png) \) to delete the blocking `/libs/*` pattern.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-353">Choose **Remove all patterns** \(![Remove all patterns](../media/remove-icon.msft.png)\) to delete the `/libs/*` blocking pattern.</span></span>  
    
<span data-ttu-id="aa6d6-354">En règle générale, **l’outil** de blocage des demandes est utile pour simuler le comportement de votre page lorsqu’une ressource donnée n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-354">In general, the **Request blocking** tool is useful for simulating how your page behaves when any given resource is not available.</span></span>  

<span data-ttu-id="aa6d6-355">Maintenant, supprimez les références à ces fichiers du code et auditer à nouveau la page :</span><span class="sxs-lookup"><span data-stu-id="aa6d6-355">Now, remove the references to these files from the code and audit the page again:</span></span>  

1.  <span data-ttu-id="aa6d6-356">De retour dans l’onglet Éditeur, ouvrez `template.html` .</span><span class="sxs-lookup"><span data-stu-id="aa6d6-356">Back in the editor tab, open `template.html`.</span></span>  
1.  <span data-ttu-id="aa6d6-357">Supprimez les éléments `<script src="/libs/lodash.js">` et `<script src="/libs/jquery.js"></script>`.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-357">Delete `<script src="/libs/lodash.js">` and `<script src="/libs/jquery.js"></script>`.</span></span>  
1.  <span data-ttu-id="aa6d6-358">Attendez que le site soit re-build et re-déployé.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-358">Wait for the site to re-build and re-deploy.</span></span>  
1.  <span data-ttu-id="aa6d6-359">Auditer à nouveau la page à partir de **l’outil Audits.**</span><span class="sxs-lookup"><span data-stu-id="aa6d6-359">Audit the page again from the **Audits** tool.</span></span>  <span data-ttu-id="aa6d6-360">Votre score global devrait de nouveau avoir été amélioré.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-360">Your overall score should have improved again.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-2-audits-performance.msft.png" alt-text="Un rapport Audits après la suppression des ressources de blocage de rendu" lightbox="../media/speed-glitch-tony-remix-updated-2-audits-performance.msft.png":::
       <span data-ttu-id="aa6d6-362">Un **rapport Audits** après la suppression des ressources de blocage de rendu</span><span class="sxs-lookup"><span data-stu-id="aa6d6-362">An **Audits** report after removing the render-blocking resources</span></span>  
    :::image-end:::  
    
#### <a name="optimizing-the-critical-rendering-path-in-the-real-world"></a><span data-ttu-id="aa6d6-363">Optimisation du chemin d’accès de rendu critique dans le monde réel</span><span class="sxs-lookup"><span data-stu-id="aa6d6-363">Optimizing the Critical Rendering Path in the real-world</span></span>  

<span data-ttu-id="aa6d6-364">Le **chemin d’accès** de rendu critique fait référence au code dont vous avez besoin pour charger une page.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-364">The **Critical Rendering Path** refers to the code that you need to load a page.</span></span>  <span data-ttu-id="aa6d6-365">En règle générale, accélèrez le chargement de la page en expédiant uniquement du code critique pendant le chargement de la page, puis en chargeant différée tout le reste.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-365">In general, speed up page load by only shipping critical code during the page load, and then lazy-loading everything else.</span></span>  

<!--[CRP]: /web/fundamentals/performance/critical-rendering-path/  -->  

*   <span data-ttu-id="aa6d6-366">Il est peu probable que vous soyez en mesure de trouver des scripts que vous êtes en mesure de supprimer totalement, mais vous trouverez peut-être de nombreux scripts que vous n’avez pas besoin de demander pendant le chargement de la page et qui peuvent être demandés de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-366">It is unlikely that you are able to find scripts that you are able to remove outright, but you may find many scripts that you do not need to request during the page load, and instead may be requested asynchronously.</span></span>  <!--Navigate to [Using async or defer][async].  -->  
*   <span data-ttu-id="aa6d6-367">Si vous utilisez une infrastructure, vérifiez si elle dispose d’un mode de production.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-367">If you are using a framework, check if it has a production mode.</span></span>  <span data-ttu-id="aa6d6-368">Ce mode peut utiliser une fonctionnalité telle que l’arborescence [afin][WebpackTreeShaking] d’éliminer le code inutile qui bloque le rendu critique.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-368">This mode may use a feature such as [tree shaking][WebpackTreeShaking] in order to eliminate unnecessary code that is blocking the critical render.</span></span>  
    
<!--[async]: /web/fundamentals/performance/optimizing-content-efficiency/loading-third-party-javascript/#use_async_or_defer  -->  

### <a name="do-less-main-thread-work"></a><span data-ttu-id="aa6d6-369">Faire moins de travail de thread principal</span><span class="sxs-lookup"><span data-stu-id="aa6d6-369">Do less main thread work</span></span>  

<span data-ttu-id="aa6d6-370">Votre dernier rapport présente quelques économies potentielles mineures dans la section Opportunités, mais si vous examinez la section Diagnostics, il semble que le goulot d’étranglement le plus important soit une activité de thread principale trop importante.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-370">Your latest report shows some minor potential savings in the Opportunities section, but if you look down in the Diagnostics section, it looks like the biggest bottleneck is too much main thread activity.</span></span>  

<span data-ttu-id="aa6d6-371">Le thread principal est l’endroit où le navigateur fait la plupart des travaux nécessaires à l’affichage d’une page, telles que l’affichage et l’exécution de CODE HTML, CSS et JavaScript.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-371">The main thread is where the browser does most of the work needed to display a page, such as parsing and running HTML, CSS, and JavaScript.</span></span>  

<span data-ttu-id="aa6d6-372">L’objectif est d’utiliser le panneau Performances pour analyser le travail que le thread principal fait pendant le chargement de la page et trouver des moyens de différer ou de supprimer le travail inutile.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-372">The goal is to use the Performance panel to analyze what work the main thread is doing while the page loads, and find ways to defer or remove unnecessary work.</span></span>  

1.  <span data-ttu-id="aa6d6-373">Choisissez **l’outil Performance.**</span><span class="sxs-lookup"><span data-stu-id="aa6d6-373">Choose the **Performance** tool.</span></span>  
1.  <span data-ttu-id="aa6d6-374">Choose **Capture Settings** \( ![ Capture Settings ](../media/capture-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="aa6d6-374">Choose **Capture Settings** \(![Capture Settings](../media/capture-icon.msft.png)\).</span></span>  
1.  <span data-ttu-id="aa6d6-375">Définissez **le** réseau **sur le 3G** et le **processeur** **à 6x le ralentissement.**</span><span class="sxs-lookup"><span data-stu-id="aa6d6-375">Set **Network** to **Slow 3G** and **CPU** to **6x slowdown**.</span></span>  <span data-ttu-id="aa6d6-376">Les appareils mobiles ont généralement plus de contraintes matérielles que les ordinateurs portables ou les ordinateurs de bureau. Ces paramètres vous offrent donc la même expérience que si vous utilisiez un appareil moins puissant.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-376">Mobile devices typically have more hardware constraints than laptops or desktops, so these settings let you experience the page load as if you were using a less powerful device.</span></span>  
1.  <span data-ttu-id="aa6d6-377">Choose **Refresh** \( ![ Refresh ](../media/reload-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="aa6d6-377">Choose **Refresh** \(![Refresh](../media/reload-icon.msft.png)\).</span></span>  <span data-ttu-id="aa6d6-378">DevTools actuale la page, puis produit une visualisation de tout le travail effectué afin de charger la page.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-378">DevTools refreshes the page and then produces a visualization of all the work performed in order to load the page.</span></span>  <span data-ttu-id="aa6d6-379">Cette visualisation est appelée **suivi.**</span><span class="sxs-lookup"><span data-stu-id="aa6d6-379">This visualization is referred to as the **trace**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png" alt-text="Suivi de l’outil Performance du chargement de la page" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png":::
       <span data-ttu-id="aa6d6-381">Suivi **de l’outil** Performance du chargement de la page</span><span class="sxs-lookup"><span data-stu-id="aa6d6-381">The **Performance** tool trace of the page load</span></span>  
    :::image-end:::  
    
<span data-ttu-id="aa6d6-382">Le suivi montre l’activité dans l’ordre chronologique, de gauche à droite.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-382">The trace shows activity chronologically, from left to right.</span></span>  <span data-ttu-id="aa6d6-383">Les graphiques FPS, processeur et NET en haut vous donnent une vue d’ensemble des images par seconde, de l’activité processeur et de l’activité réseau.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-383">The FPS, CPU, and NET charts at the top give you an overview of frames per second, CPU activity, and network activity.</span></span>  <span data-ttu-id="aa6d6-384">Bloc de jaune mis en surbrillant dans la figure suivant, l’UC était complètement occupée par l’activité de script.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-384">The block of yellow highlighted in the figure after the next, the CPU was completely busy with scripting activity.</span></span>  <span data-ttu-id="aa6d6-385">Il s’agit d’un indice qui vous permet d’accélérer le chargement de la page en faisant moins de travail JavaScript.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-385">This is a clue that you may be able to speed up page load by doing less JavaScript work.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png" alt-text="Section Vue d’ensemble du suivi" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png":::
   <span data-ttu-id="aa6d6-387">Section Vue d’ensemble du suivi</span><span class="sxs-lookup"><span data-stu-id="aa6d6-387">The Overview section of the trace</span></span>  
:::image-end:::  

<span data-ttu-id="aa6d6-388">Examinez la trace pour trouver des méthodes pour faire moins de travail JavaScript :</span><span class="sxs-lookup"><span data-stu-id="aa6d6-388">Investigate the trace to find ways to do less JavaScript work:</span></span>  

1.  <span data-ttu-id="aa6d6-389">Sélectionnez la section **Minutages** pour la développer.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-389">Choose the **Timings** section to expand it.</span></span>  <span data-ttu-id="aa6d6-390">En fonction du fait qu’il [][MDNUserTimingApi] peut y avoir plusieurs mesures de minutage de React, il semble que l’application de Tony utilise le mode de développement de React.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-390">Based on the fact that there may be a bunch of [Timings][MDNUserTimingApi] measures from React, it seems like Tony's app is using the development mode of React.</span></span>  <span data-ttu-id="aa6d6-391">Le passage au mode de production de React peut donner des résultats faciles en terme de performances.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-391">Switching to the production mode of React may yield some easy performance wins.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings.msft.png" alt-text="La section Minutage" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings.msft.png":::
       <span data-ttu-id="aa6d6-393">La section **Minutage**</span><span class="sxs-lookup"><span data-stu-id="aa6d6-393">The **Timings** section</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="aa6d6-394">Sélectionnez **de nouveau Minutages** pour réduire cette section.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-394">Choose **Timings** again to collapse that section.</span></span>  
1.  <span data-ttu-id="aa6d6-395">Parcourez la section **Principale.**</span><span class="sxs-lookup"><span data-stu-id="aa6d6-395">Browse the **Main** section.</span></span>  <span data-ttu-id="aa6d6-396">Cette section présente un journal chronologique de l’activité du thread principal, de gauche à droite.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-396">This section shows a chronological log of main thread activity, from left to right.</span></span>  <span data-ttu-id="aa6d6-397">L’axe y (de haut en bas) indique pourquoi les événements se sont produits.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-397">The y-axis (top to bottom) shows why events occurred.</span></span>  <span data-ttu-id="aa6d6-398">Par exemple, dans la figure suivante, l’événement a provoqué l’exécuter, ce qui a provoqué l’exécuter, ce qui a provoqué l’exécuter, `Evaluate Script` `(anonymous)` `(anonymous)` `__webpack__require__` etc.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-398">For example, in the figyre after the following, the `Evaluate Script` event caused the `(anonymous)` function to run, which caused `(anonymous)` to run, which caused `__webpack__require__` to run, and so on.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png" alt-text="Section Main" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png":::
       <span data-ttu-id="aa6d6-400">Section **Main**</span><span class="sxs-lookup"><span data-stu-id="aa6d6-400">The **Main** section</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="aa6d6-401">Faites défiler vers le bas jusqu’au bas de la section **Main.**</span><span class="sxs-lookup"><span data-stu-id="aa6d6-401">Scroll down to the bottom of the **Main** section.</span></span>  <span data-ttu-id="aa6d6-402">Lorsque vous utilisez une infrastructure, la majeure partie de l’activité supérieure est due à l’infrastructure, qui est généralement hors de votre contrôle.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-402">When you use a framework, most of the upper activity is caused by the framework, which is usually out of your control.</span></span>  <span data-ttu-id="aa6d6-403">L’activité provoquée par votre application se trouve généralement en bas.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-403">The activity caused by your app is usually at the bottom.</span></span>  <span data-ttu-id="aa6d6-404">Dans cette application, il semble qu’une fonction nommée soit à l’origine d’un grand nombre de `App` demandes à une `mineBitcoin` fonction.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-404">In this app, it seems like a function named `App` is causing a lot of requests to a `mineBitcoin` function.</span></span>  <span data-ttu-id="aa6d6-405">Il semble que Tony utilise peut-être les périphériques de ses fans pour utiliser la cryptomonnaie...</span><span class="sxs-lookup"><span data-stu-id="aa6d6-405">It sounds like Tony may be using the devices of his fans to mine cryptocurrency...</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png" alt-text="Pointer sur l’activité mineBitcoin" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png":::
       <span data-ttu-id="aa6d6-407">Pointer sur `mineBitcoin` l’activité</span><span class="sxs-lookup"><span data-stu-id="aa6d6-407">Hover on the `mineBitcoin` activity</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="aa6d6-408">Bien que les demandes que votre infrastructure effectue soient généralement hors de votre contrôle, vous pouvez parfois structurer votre application d’une manière qui entraîne une utilisation inefficace de l’infrastructure.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-408">Although the requests that your framework makes are usually out of your control, sometimes you may structure your app in a way that causes the framework to run inefficiently.</span></span>  <span data-ttu-id="aa6d6-409">La réorganisation de votre application afin d’utiliser efficacement l’infrastructure est un moyen de réduire le travail de thread principal.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-409">Restructuring your app to use the framework efficiently is a way to do less main thread work.</span></span>  <span data-ttu-id="aa6d6-410">Toutefois, cela nécessite une connaissance approfondie du fonctionnement de votre infrastructure et du type de modifications que vous a faites dans votre propre code afin d’utiliser l’infrastructure plus efficacement.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-410">However, this requires a deep understanding of how your framework works, and what kind of changes you make in your own code in order to use the framework more efficiently.</span></span>  
    
1.  <span data-ttu-id="aa6d6-411">Développez la section Bas vers **le** haut.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-411">Expand the **Bottom-Up** section.</span></span>  <span data-ttu-id="aa6d6-412">Cet onglet décompose les activités qui ont pris le plus de temps.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-412">This tab breaks down what activities took up the most time.</span></span>  <span data-ttu-id="aa6d6-413">Si rien n’est affiché dans la section Bottom-Up, choisissez l’étiquette de la section **Main.**</span><span class="sxs-lookup"><span data-stu-id="aa6d6-413">If nothing is displayed in the Bottom-Up section, choose the label for **Main** section.</span></span>  <span data-ttu-id="aa6d6-414">La section **Bas vers le haut** affiche uniquement les informations concernant l’activité ou le groupe d’activités que vous avez actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-414">The **Bottom-Up** section only shows information for whatever activity, or group of activity, you have currently selected.</span></span>  <span data-ttu-id="aa6d6-415">Par exemple, si vous avez choisi l’une des activités, la section Bas vers le haut affiche uniquement les informations `mineBitcoin` de cette activité. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="aa6d6-415">For example, if you chose one of the `mineBitcoin` activities, the **Bottom-Up** section is only going to show information for that one activity.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-summary-minebitcoin.msft.png" alt-text="Onglet Bottom-Up'onglet" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-summary-minebitcoin.msft.png":::
       <span data-ttu-id="aa6d6-417">Onglet **Bas vers le** haut</span><span class="sxs-lookup"><span data-stu-id="aa6d6-417">The **Bottom-Up** tab</span></span>  
    :::image-end:::  
    
<span data-ttu-id="aa6d6-418">La **colonne Temps** libre vous indique le temps passé directement dans chaque activité.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-418">The **Self Time** column shows you how much time was spent directly in each activity.</span></span>  <span data-ttu-id="aa6d6-419">Par exemple, dans la figure suivante, environ 63 % du temps du thread principal a été passé sur la `mineBitcoin` fonction.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-419">For example, in the following figure, about 63% of main thread time was spent on the `mineBitcoin` function.</span></span>  

<span data-ttu-id="aa6d6-420">Il est temps de vérifier si l’utilisation du mode de production et la réduction de l’activité JavaScript peuvent accélérer le chargement de la page.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-420">Time to review whether using production mode and reducing JavaScript activity may speed up the page load.</span></span>  <span data-ttu-id="aa6d6-421">Démarrez avec le mode de production :</span><span class="sxs-lookup"><span data-stu-id="aa6d6-421">Start with production mode:</span></span>  

1.  <span data-ttu-id="aa6d6-422">Dans l’onglet Éditeur, ouvrez `webpack.config.js` .</span><span class="sxs-lookup"><span data-stu-id="aa6d6-422">In the editor tab, open `webpack.config.js`.</span></span>  
1.  <span data-ttu-id="aa6d6-423">Change `"mode":"development"` to `"mode":"production"` .</span><span class="sxs-lookup"><span data-stu-id="aa6d6-423">Change `"mode":"development"` to `"mode":"production"`.</span></span>  
1.  <span data-ttu-id="aa6d6-424">Attendez le déploiement de la nouvelle build.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-424">Wait for the new build to deploy.</span></span>  
1.  <span data-ttu-id="aa6d6-425">Auditer à nouveau la page.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-425">Audit the page again.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-3-audits-performance.msft.png" alt-text="Un rapport Audits après avoir configuré webpack pour utiliser le mode production" lightbox="../media/speed-glitch-tony-remix-updated-3-audits-performance.msft.png":::
       <span data-ttu-id="aa6d6-427">Un rapport Audits après avoir configuré webpack pour utiliser le mode production</span><span class="sxs-lookup"><span data-stu-id="aa6d6-427">An Audits report after configuring webpack to use production mode</span></span>  
    :::image-end:::  
    
<span data-ttu-id="aa6d6-428">Réduisez l’activité JavaScript en supprimant la demande à `mineBitcoin` :</span><span class="sxs-lookup"><span data-stu-id="aa6d6-428">Reduce JavaScript activity by removing the request to `mineBitcoin`:</span></span>  

1.  <span data-ttu-id="aa6d6-429">Dans l’onglet Éditeur, ouvrez `src/App.jsx` .</span><span class="sxs-lookup"><span data-stu-id="aa6d6-429">In the editor tab, open `src/App.jsx`.</span></span>  
1.  <span data-ttu-id="aa6d6-430">Commentez la demande dans `this.mineBitcoin(1500)` `constructor` le .</span><span class="sxs-lookup"><span data-stu-id="aa6d6-430">Comment out the request to `this.mineBitcoin(1500)` in the `constructor`.</span></span>  
1.  <span data-ttu-id="aa6d6-431">Attendez le déploiement de la nouvelle build.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-431">Wait for the new build to deploy.</span></span>  
1.  <span data-ttu-id="aa6d6-432">Auditer à nouveau la page.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-432">Audit the page again.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-4-audits-performance.msft.png" alt-text="Un rapport Audits après la suppression de travail JavaScript inutile" lightbox="../media/speed-glitch-tony-remix-updated-4-audits-performance.msft.png":::
       <span data-ttu-id="aa6d6-434">Un rapport Audits après la suppression de travail JavaScript inutile</span><span class="sxs-lookup"><span data-stu-id="aa6d6-434">An Audits report after removing unnecessary JavaScript work</span></span>  
    :::image-end:::  
    
<span data-ttu-id="aa6d6-435">Il semble que cette dernière modification a provoqué un saut important des performances !</span><span class="sxs-lookup"><span data-stu-id="aa6d6-435">Looks like that last change caused a massive jump in performance!</span></span>  

> [!NOTE]
> <span data-ttu-id="aa6d6-436">Cette section a présenté brièvement le panneau Performances.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-436">This section provided a rather brief introduction to the Performance panel.</span></span>  <span data-ttu-id="aa6d6-437">Pour en savoir plus sur l’analyse des performances de page, accédez à [Référence de l’analyse des performances.][DevtoolsEvaluatePerformanceReference]</span><span class="sxs-lookup"><span data-stu-id="aa6d6-437">To learn more about how to analyze page performance, navigate to [Performance Analysis Reference][DevtoolsEvaluatePerformanceReference].</span></span>  

<!--todo: add section when available -->  

#### <a name="doing-less-main-thread-work-in-the-real-world"></a><span data-ttu-id="aa6d6-438">Faire moins de travail de thread principal dans le monde réel</span><span class="sxs-lookup"><span data-stu-id="aa6d6-438">Doing less main thread work in the real world</span></span>  

<span data-ttu-id="aa6d6-439">En règle générale, l’outil **Performance** est le moyen le plus courant de comprendre l’activité que fait votre site pendant son chargement et de trouver des moyens de supprimer les activités inutiles.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-439">In general, the **Performance** tool is the most common way to understand what activity your site does as it loads, and find ways to remove unnecessary activity.</span></span>  

<span data-ttu-id="aa6d6-440">Si vous préférez une approche qui ressemble davantage, l’API de minutage de l’utilisateur vous permet de marquer arbitrairement certaines phases du cycle de vie de votre application, afin de suivre la durée de chacune de ces `console.log()` phases. [][MDNUserTimingApi]</span><span class="sxs-lookup"><span data-stu-id="aa6d6-440">If you prefer an approach that feels more like `console.log()`, the [User Timing API][MDNUserTimingApi] enables you to arbitrarily mark up certain phases of your app lifecycle, in order to track how long each of those phases takes.</span></span>  

## <a name="summary"></a><span data-ttu-id="aa6d6-441">Résumé</span><span class="sxs-lookup"><span data-stu-id="aa6d6-441">Summary</span></span>  

*   <span data-ttu-id="aa6d6-442">Chaque fois que vous définissez pour optimiser les performances de charge d’un site, commencez toujours par un audit.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-442">Whenever you set out to optimize the load performance of a site, always start with an audit.</span></span>  <span data-ttu-id="aa6d6-443">L’audit établit une ligne de base et vous donne des conseils sur la façon d’améliorer.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-443">The audit establishes a baseline, and gives you tips on how to improve.</span></span>  
*   <span data-ttu-id="aa6d6-444">A effectuer une modification à la fois et auditer la page web après chaque modification afin d’afficher l’impact de cette modification isolée sur les performances.</span><span class="sxs-lookup"><span data-stu-id="aa6d6-444">Make one change at a time, and audit the webpage after each change in order to display how that isolated change affects performance.</span></span>  

<!--
## Next steps  

*   Run audits on your own site!  If you need help interpreting your report, or finding ways to improve your load performance, check out [Feedback](#feedback) for ways to get help from the DevTools community.  Stack Overflow, the mailing list, or Twitter are probably best for these types of questions.  
*   Please leave [feedback](#feedback) on this tutorial.  I really do use the data to make better tutorials for you.  
-->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="aa6d6-445">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="aa6d6-445">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsEvaluatePerformanceReference]: ../evaluate-performance/reference.md "Référence de l’analyse des performances | Documents Microsoft"  

[CourseraIntroductionWebDevelopmentClass]: https://www.coursera.org/learn/web-development#syllabus "Présentation des classes de développement Web | Coursera"  

[EssentialImageOptimization]: https://images.guide "Optimisation des images essentielles"  

[MDNContentEncodingDirectives]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Encoding#Directives "Directives : | MDN"  
[MDNUserTimingApi]: https://developer.mozilla.org/docs/Web/API/User_Timing_API "Api de minutage utilisateur | MDN"  

[WebpackTreeShaking]: https://webpack.js.org/guides/tree-shaking "Arborescence de | webpack"  

> [!NOTE]
> <span data-ttu-id="aa6d6-452">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="aa6d6-452">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="aa6d6-453">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="aa6d6-453">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="aa6d6-455">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="aa6d6-455">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
