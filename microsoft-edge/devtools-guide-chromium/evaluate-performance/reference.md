---
description: Référence sur toutes les façons d’enregistrer et d’analyser les performances dans Microsoft Edge DevTools.
title: Référence d’analyse des performances
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 5cd7c4aee6eb5f0c48f783e250efa1ef69010fc4
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564349"
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
# <a name="performance-analysis-reference"></a><span data-ttu-id="77422-104">Référence d’analyse des performances</span><span class="sxs-lookup"><span data-stu-id="77422-104">Performance analysis reference</span></span>  

<span data-ttu-id="77422-105">Cette page est une référence complète des fonctionnalités Microsoft Edge DevTools relatives à l’analyse des performances.</span><span class="sxs-lookup"><span data-stu-id="77422-105">This page is a comprehensive reference of Microsoft Edge DevTools features related to analyzing performance.</span></span>  

<span data-ttu-id="77422-106">Accédez [à Prise en main][DevtoolsEvaluatePerformanceGettingStarted] Avec analyse des performances d’exécution pour un didacticiel guidé sur l’analyse des performances d’une page à l’aide Microsoft Edge [DevTools][MicrosoftEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="77422-106">Navigate to [Get Started With Analyzing Runtime Performance][DevtoolsEvaluatePerformanceGettingStarted] for a guided tutorial on how to analyze the performance of a page using [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <a name="record-performance"></a><span data-ttu-id="77422-107">Performances d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="77422-107">Record performance</span></span>  

### <a name="record-runtime-performance"></a><span data-ttu-id="77422-108">Performances d’exécution d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="77422-108">Record runtime performance</span></span>  

<span data-ttu-id="77422-109">Enregistrez les performances d’exécution lorsque vous souhaitez analyser les performances d’une page en cours d’exécution, par opposition au chargement.</span><span class="sxs-lookup"><span data-stu-id="77422-109">Record runtime performance when you want to analyze the performance of a page as it is running, as opposed to loading.</span></span>  

1.  <span data-ttu-id="77422-110">Accédez à la page que vous souhaitez analyser.</span><span class="sxs-lookup"><span data-stu-id="77422-110">Navigate to the page that you want to analyze.</span></span>  
1.  <span data-ttu-id="77422-111">Ouvrez **l’outil** Performance dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="77422-111">Open the **Performance** tool in DevTools.</span></span>  
1.  <span data-ttu-id="77422-112">Choose **Record** \( ![ Record icon ](../media/record-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="77422-112">Choose **Record** \(![Record icon](../media/record-icon.msft.png)\).</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-record-highlight.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-record-highlight.msft.png":::
       **<span data-ttu-id="77422-114">Record</span><span class="sxs-lookup"><span data-stu-id="77422-114">Record</span></span>**  
    :::image-end:::  
    
1.  <span data-ttu-id="77422-115">Interagir avec la page.</span><span class="sxs-lookup"><span data-stu-id="77422-115">Interact with the page.</span></span>  <span data-ttu-id="77422-116">DevTools enregistre toutes les activités de page qui se produisent suite à vos interactions.</span><span class="sxs-lookup"><span data-stu-id="77422-116">DevTools records all page activity that occurs as a result of your interactions.</span></span>  
1.  <span data-ttu-id="77422-117">Choose **Record** again or choose **Stop** to stop recording.</span><span class="sxs-lookup"><span data-stu-id="77422-117">Choose **Record** again or choose **Stop** to stop recording.</span></span>  
    
### <a name="record-load-performance"></a><span data-ttu-id="77422-118">Performances de chargement d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="77422-118">Record load performance</span></span>  

<span data-ttu-id="77422-119">Enregistrez les performances de chargement lorsque vous souhaitez analyser les performances d’une page en cours de chargement, par opposition à l’exécution.</span><span class="sxs-lookup"><span data-stu-id="77422-119">Record load performance when you want to analyze the performance of a page as it is loading, as opposed to running.</span></span>  

1.  <span data-ttu-id="77422-120">Accédez à la page que vous souhaitez analyser.</span><span class="sxs-lookup"><span data-stu-id="77422-120">Navigate to the page that you want to analyze.</span></span>  
1.  <span data-ttu-id="77422-121">Ouvrez **le panneau Performances** de DevTools.</span><span class="sxs-lookup"><span data-stu-id="77422-121">Open the **Performance** panel of DevTools.</span></span>  
1.  <span data-ttu-id="77422-122">Choose **Refresh page** \( Refresh Page ![ ](../media/refresh-page-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="77422-122">Choose **Refresh page** \(![Refresh Page](../media/refresh-page-icon.msft.png)\).</span></span>  <span data-ttu-id="77422-123">DevTools enregistre les mesures de performances pendant l’actualisation de la page, puis arrête automatiquement l’enregistrement quelques secondes après la fin du chargement.</span><span class="sxs-lookup"><span data-stu-id="77422-123">DevTools records performance metrics while the page refreshes and then automatically stops the recording a couple seconds after the load finishes.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-refresh-button.msft.png" alt-text="Page Actualiser" lightbox="../media/evaluate-performance-performance-refresh-button.msft.png":::
       **<span data-ttu-id="77422-125">Page Actualiser</span><span class="sxs-lookup"><span data-stu-id="77422-125">Refresh page</span></span>**  
    :::image-end:::  
    
<span data-ttu-id="77422-126">DevTools effectue automatiquement un zoom avant sur la partie de l’enregistrement où la majeure partie de l’activité s’est produite.</span><span class="sxs-lookup"><span data-stu-id="77422-126">DevTools automatically zooms in on the portion of the recording where most of the activity occurred.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed.msft.png" alt-text="Un enregistrement de chargement de page" lightbox="../media/evaluate-performance-performance-refreshed.msft.png":::
   <span data-ttu-id="77422-128">Un enregistrement de chargement de page</span><span class="sxs-lookup"><span data-stu-id="77422-128">A page-load recording</span></span>  
:::image-end:::  

### <a name="capture-screenshots-while-recording"></a><span data-ttu-id="77422-129">Capture d’écran pendant l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="77422-129">Capture screenshots while recording</span></span>  

<span data-ttu-id="77422-130">Activer la case à cocher **Captures** d’écran pour capturer une capture d’écran de chaque image pendant l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="77422-130">Turn on the **Screenshots** checkbox to capture a screenshot of every frame while recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png" alt-text="Case à cocher Captures d’écran" lightbox="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png":::
   <span data-ttu-id="77422-132">Case **à cocher Captures d’écran**</span><span class="sxs-lookup"><span data-stu-id="77422-132">The **Screenshots** checkbox</span></span>  
:::image-end:::  

<span data-ttu-id="77422-133">Accédez à [Afficher une capture d’écran](#view-a-screenshot) pour apprendre à interagir avec les captures d’écran.</span><span class="sxs-lookup"><span data-stu-id="77422-133">Navigate to [View a screenshot](#view-a-screenshot) to learn how to interact with screenshots.</span></span>  

### <a name="force-garbage-collection-while-recording"></a><span data-ttu-id="77422-134">Forcer le collecte de la garbage lors de l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="77422-134">Force garbage collection while recording</span></span>  

<span data-ttu-id="77422-135">Pendant l’enregistrement d’une page, sélectionnez Collecter la **garbage** \( Collect garbage icon \) pour forcer le ![ collecte de la ](../media/collect-garbage-icon.msft.png) garbage.</span><span class="sxs-lookup"><span data-stu-id="77422-135">While you are recording a page, choose **Collect garbage** \(![Collect garbage icon](../media/collect-garbage-icon.msft.png)\) to force garbage collection.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-collect-garbage-button.msft.png" alt-text="Collecter la garbage" lightbox="../media/evaluate-performance-performance-collect-garbage-button.msft.png":::
   <span data-ttu-id="77422-137">Collecter la garbage</span><span class="sxs-lookup"><span data-stu-id="77422-137">Collect garbage</span></span>  
:::image-end:::  

### <a name="show-recording-settings"></a><span data-ttu-id="77422-138">Afficher les paramètres d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="77422-138">Show recording settings</span></span>  

<span data-ttu-id="77422-139">Choose **Capture settings** \( ![ Capture settings ](../media/capture-settings-icon.msft.png) \) to expose more settings related to how DevTools captures performance recordings.</span><span class="sxs-lookup"><span data-stu-id="77422-139">Choose **Capture settings** \(![Capture settings](../media/capture-settings-icon.msft.png)\) to expose more settings related to how DevTools captures performance recordings.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png" alt-text="Section Capture Paramètres" lightbox="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png":::
   <span data-ttu-id="77422-141">Section **Capture Paramètres**</span><span class="sxs-lookup"><span data-stu-id="77422-141">The **Capture Settings** section</span></span>  
:::image-end:::  

### <a name="disable-javascript-samples"></a><span data-ttu-id="77422-142">Désactiver les exemples JavaScript</span><span class="sxs-lookup"><span data-stu-id="77422-142">Disable JavaScript samples</span></span>  

<span data-ttu-id="77422-143">Par défaut, la section **Main** d’un enregistrement affiche des piles d’appels détaillées de fonctions JavaScript qui ont été appelées pendant l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="77422-143">By default, the **Main** section of a recording displays detailed call stacks of JavaScript functions that were called during the recording.</span></span>  <span data-ttu-id="77422-144">Pour désactiver ces piles d’appels :</span><span class="sxs-lookup"><span data-stu-id="77422-144">To disable these call stacks:</span></span>  

1.  <span data-ttu-id="77422-145">Ouvrez le menu **Paramètres de** capture.</span><span class="sxs-lookup"><span data-stu-id="77422-145">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="77422-146">Accédez à [Afficher les paramètres d’enregistrement.](#show-recording-settings)</span><span class="sxs-lookup"><span data-stu-id="77422-146">Navigate to [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="77422-147">Activer la case **à cocher Désactiver les exemples JavaScript.**</span><span class="sxs-lookup"><span data-stu-id="77422-147">Turn on the **Disable JavaScript Samples** checkbox.</span></span>  
1.  <span data-ttu-id="77422-148">Prenez un enregistrement de la page.</span><span class="sxs-lookup"><span data-stu-id="77422-148">Take a recording of the page.</span></span>  
    
<span data-ttu-id="77422-149">Les 2 figures suivantes affichent la différence entre la désactivation et l’activation des exemples JavaScript.</span><span class="sxs-lookup"><span data-stu-id="77422-149">The following 2 figures display the difference between disabling and enabling JavaScript samples.</span></span>  <span data-ttu-id="77422-150">La section **Main** de l’enregistrement est beaucoup plus courte lorsque l’échantillonnage est désactivé, car elle omet toutes les piles d’appels JavaScript.</span><span class="sxs-lookup"><span data-stu-id="77422-150">The **Main** section of the recording is much shorter when sampling is disabled, because it omits all of the JavaScript call stacks.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png" alt-text="Exemple d’enregistrement lorsque les exemples JS sont désactivés" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png":::
         <span data-ttu-id="77422-152">Exemple d’enregistrement lorsque les exemples JS sont désactivés</span><span class="sxs-lookup"><span data-stu-id="77422-152">An example of a recording when JS samples are disabled</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png" alt-text="Exemple d’enregistrement lorsque les exemples JS sont allumés" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png":::
         <span data-ttu-id="77422-154">Exemple d’enregistrement lorsque les exemples JS sont allumés</span><span class="sxs-lookup"><span data-stu-id="77422-154">An example of a recording when JS samples are turned on</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

### <a name="throttle-the-network-while-recording"></a><span data-ttu-id="77422-155">Limiter le réseau lors de l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="77422-155">Throttle the network while recording</span></span>  

<span data-ttu-id="77422-156">Pour limiter le réseau lors de l’enregistrement :</span><span class="sxs-lookup"><span data-stu-id="77422-156">To throttle the network while recording:</span></span>  

1.  <span data-ttu-id="77422-157">Ouvrez le menu **Paramètres de** capture.</span><span class="sxs-lookup"><span data-stu-id="77422-157">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="77422-158">Accédez à [Afficher les paramètres d’enregistrement.](#show-recording-settings)</span><span class="sxs-lookup"><span data-stu-id="77422-158">Navigate to [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="77422-159">Définissez **le** réseau sur le niveau de limitation souhaité.</span><span class="sxs-lookup"><span data-stu-id="77422-159">Set **Network** to the desired level of throttling.</span></span>  
    
### <a name="throttle-the-cpu-while-recording"></a><span data-ttu-id="77422-160">Limiter l’UC lors de l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="77422-160">Throttle the CPU while recording</span></span>  

<span data-ttu-id="77422-161">Pour limiter le processeur lors de l’enregistrement :</span><span class="sxs-lookup"><span data-stu-id="77422-161">To throttle the CPU while recording:</span></span>  

1.  <span data-ttu-id="77422-162">Ouvrez le menu **Paramètres de** capture.</span><span class="sxs-lookup"><span data-stu-id="77422-162">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="77422-163">Accédez à [Afficher les paramètres d’enregistrement.](#show-recording-settings)</span><span class="sxs-lookup"><span data-stu-id="77422-163">Navigate to [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="77422-164">Définissez **le processeur** sur le niveau de limitation souhaité.</span><span class="sxs-lookup"><span data-stu-id="77422-164">Set **CPU** to the desired level of throttling.</span></span>  
    
<span data-ttu-id="77422-165">La limitation est relative aux fonctionnalités de votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="77422-165">Throttling is relative to the capabilities of your computer.</span></span>  <span data-ttu-id="77422-166">Par exemple, l’option **de ralentissement 2x** ralentit le fonctionnement de votre processeur 2 fois plus lent que la normale.</span><span class="sxs-lookup"><span data-stu-id="77422-166">For example, the **2x slowdown** option makes your CPU operate 2 times slower than normal.</span></span>  <span data-ttu-id="77422-167">DevTools ne simule pas véritablement les processeurs des appareils mobiles, car l’architecture des appareils mobiles est très différente de celle des ordinateurs de bureau et des ordinateurs portables.</span><span class="sxs-lookup"><span data-stu-id="77422-167">DevTools do not truly simulate the CPUs of mobile devices, because the architecture of mobile devices is very different from that of desktops and laptops.</span></span>  

### <a name="turn-on-advanced-paint-instrumentation"></a><span data-ttu-id="77422-168">Activer l’instrumentation de pinceau avancée</span><span class="sxs-lookup"><span data-stu-id="77422-168">Turn on advanced paint instrumentation</span></span>  

<span data-ttu-id="77422-169">Pour afficher l’instrumentation de la couleur détaillée :</span><span class="sxs-lookup"><span data-stu-id="77422-169">To view detailed paint instrumentation:</span></span>  

1.  <span data-ttu-id="77422-170">Ouvrez le menu **Paramètres de** capture.</span><span class="sxs-lookup"><span data-stu-id="77422-170">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="77422-171">Accédez à [Afficher les paramètres d’enregistrement.](#show-recording-settings)</span><span class="sxs-lookup"><span data-stu-id="77422-171">Navigate to [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="77422-172">Activez **la case à cocher Activer l’instrumentation de pinceau avancée (lente).**</span><span class="sxs-lookup"><span data-stu-id="77422-172">Check the **Enable advanced paint instrumentation (slow)** checkbox.</span></span>  

<span data-ttu-id="77422-173">Pour apprendre à interagir avec les informations de paint, accédez à [Afficher](#view-layers-information) les couches et [afficher le profileur de paint.](#view-paint-profiler)</span><span class="sxs-lookup"><span data-stu-id="77422-173">To learn how to interact with the paint information, navigate to [View layers](#view-layers-information) and [View paint profiler](#view-paint-profiler).</span></span>  

## <a name="save-a-recording"></a><span data-ttu-id="77422-174">Enregistrer un enregistrement</span><span class="sxs-lookup"><span data-stu-id="77422-174">Save a recording</span></span>  

<span data-ttu-id="77422-175">Pour enregistrer un enregistrement, ouvrez le menu contextuel \(clic droit\), puis choisissez **Enregistrer le profil.**</span><span class="sxs-lookup"><span data-stu-id="77422-175">To save a recording, open the contextual menu \(right-click\), and choose **Save Profile**.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png" alt-text="Enregistrer le profil" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png":::
   **<span data-ttu-id="77422-177">Enregistrer le profil</span><span class="sxs-lookup"><span data-stu-id="77422-177">Save Profile</span></span>**  
:::image-end:::  

## <a name="load-a-recording"></a><span data-ttu-id="77422-178">Charger un enregistrement</span><span class="sxs-lookup"><span data-stu-id="77422-178">Load a recording</span></span>  

<span data-ttu-id="77422-179">Pour charger un enregistrement, ouvrez le menu contextuel \(clic droit\), puis choisissez **Charger le profil.**</span><span class="sxs-lookup"><span data-stu-id="77422-179">To load a recording, open the contextual menu \(right-click\), and choose **Load Profile**.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png" alt-text="Charger le profil" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png":::
   **<span data-ttu-id="77422-181">Charger le profil</span><span class="sxs-lookup"><span data-stu-id="77422-181">Load Profile</span></span>**  
:::image-end:::  

## <a name="clear-the-previous-recording"></a><span data-ttu-id="77422-182">Effacer l’enregistrement précédent</span><span class="sxs-lookup"><span data-stu-id="77422-182">Clear the previous recording</span></span>  

<span data-ttu-id="77422-183">Après avoir enregistré l’enregistrement, sélectionnez **Effacer l’enregistrement** \( Effacer l’icône d’enregistrement \) pour effacer cet enregistrement à ![ partir du panneau ](../media/clear-recording-icon.msft.png) **Performances.**</span><span class="sxs-lookup"><span data-stu-id="77422-183">After making a recording, choose **Clear recording** \(![Clear recording icon](../media/clear-recording-icon.msft.png)\) to clear that recording from the **Performance** panel.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png" alt-text="Effacer l’enregistrement" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png":::
   **<span data-ttu-id="77422-185">Effacer l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="77422-185">Clear recording</span></span>**  
:::image-end:::  

## <a name="analyze-a-performance-recording"></a><span data-ttu-id="77422-186">Analyser un enregistrement des performances</span><span class="sxs-lookup"><span data-stu-id="77422-186">Analyze a performance recording</span></span>  

<span data-ttu-id="77422-187">Une fois que vous avez enregistré \*\*\*\* [les](#record-runtime-performance) performances d’exécution ou les performances de chargement d’enregistrement, [](#record-load-performance)le panneau Performances fournit un grand nombre de données pour analyser les performances de ce qui vient de se produire.</span><span class="sxs-lookup"><span data-stu-id="77422-187">After you [record runtime performance](#record-runtime-performance) or [record load performance](#record-load-performance), the **Performance** panel provides a lot of data for analyzing the performance of what just happened.</span></span>  

### <a name="select-a-portion-of-a-recording"></a><span data-ttu-id="77422-188">Sélectionner une partie d’un enregistrement</span><span class="sxs-lookup"><span data-stu-id="77422-188">Select a portion of a recording</span></span>  

<span data-ttu-id="77422-189">Faites glisser votre souris vers la gauche ou la droite dans la **vue d’ensemble** pour sélectionner une partie d’un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="77422-189">Drag your mouse left or right across the **Overview** to select a portion of a recording.</span></span>  <span data-ttu-id="77422-190">La **vue d’ensemble** est la section qui contient **les graphiques FPS,** **CPU**et **NET.**</span><span class="sxs-lookup"><span data-stu-id="77422-190">The **Overview** is the section that contains the **FPS**, **CPU**, and **NET** charts.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-zoom-highlighted.msft.png" alt-text="Faire glisser la souris sur la vue d’ensemble pour effectuer un zoom" lightbox="../media/evaluate-performance-performance-zoom-highlighted.msft.png":::
   <span data-ttu-id="77422-192">Faire glisser la souris sur la **vue d’ensemble** pour effectuer un zoom</span><span class="sxs-lookup"><span data-stu-id="77422-192">Drag the mouse across the **Overview** to zoom</span></span>  
:::image-end:::  

<span data-ttu-id="77422-193">Pour sélectionner une partie à l’aide du clavier :</span><span class="sxs-lookup"><span data-stu-id="77422-193">To select a portion using the keyboard:</span></span>  

1.  <span data-ttu-id="77422-194">Choisissez l’arrière-plan de la section **Main** ou l’une des sections en de côté, telles que **Interactions,** **Réseau**ou **GPU.**</span><span class="sxs-lookup"><span data-stu-id="77422-194">Choose the background of the **Main** section, or any of the sections next to it, such as **Interactions**, **Network**, or **GPU**.</span></span>  <span data-ttu-id="77422-195">Ce flux de travail de clavier ne fonctionne que lorsque l’une de ces sections est en focus.</span><span class="sxs-lookup"><span data-stu-id="77422-195">This keyboard workflow only works when one of these sections is in focus.</span></span>  
1.  <span data-ttu-id="77422-196">Utilisez les `W` touches `A` , , , `S` pour `D` zoomer, déplacer vers la gauche, zoom arrière et déplacer vers la droite, respectivement.</span><span class="sxs-lookup"><span data-stu-id="77422-196">Use the `W`, `A`, `S`, `D` keys to zoom in, move left, zoom out, and move right, respectively.</span></span>  

<span data-ttu-id="77422-197">Pour sélectionner une partie à l’aide d’un trackpad, effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="77422-197">To select a portion using a trackpad, complete the following actions.</span></span>  

1.  <span data-ttu-id="77422-198">Pointez votre souris sur la section **Vue** d’ensemble ou la section **Détails.**</span><span class="sxs-lookup"><span data-stu-id="77422-198">Hover your mouse over the **Overview** section or the **Details** section.</span></span>  <span data-ttu-id="77422-199">La section **Vue d’ensemble** est la zone contenant **les graphiques FPS,** **CPU**et **NET.**</span><span class="sxs-lookup"><span data-stu-id="77422-199">The **Overview** section is the area containing the **FPS**, **CPU**, and **NET** charts.</span></span>  <span data-ttu-id="77422-200">La section **Détails** est la zone contenant la section **Main,** la section **Interactions,** etc.</span><span class="sxs-lookup"><span data-stu-id="77422-200">The **Details** section is the area containing the **Main** section, the **Interactions** section, and so on.</span></span>  
1.  <span data-ttu-id="77422-201">À l’aide de deux doigts, effectuez un balayage vers le haut pour effectuer un zoom arrière, un balayage vers la gauche pour se déplacer vers la gauche, un balayage vers le bas pour effectuer un zoom avant et un balayage vers la droite pour se déplacer vers la droite.</span><span class="sxs-lookup"><span data-stu-id="77422-201">Using two fingers, swipe up to zoom out, swipe left to move left, swipe down to zoom in, and swipe right to move right.</span></span>  

<span data-ttu-id="77422-202">Pour faire défiler un graphique long dans la section **Main** ou l’un des voisins, choisissez et maintenez tout en faisant glisser vers le haut et vers le bas.</span><span class="sxs-lookup"><span data-stu-id="77422-202">To scroll a long flame chart in the **Main** section or any of the neighbors, choose and hold while dragging up and down.</span></span>  <span data-ttu-id="77422-203">Faites glisser vers la gauche et la droite pour déplacer la partie de l’enregistrement choisie.</span><span class="sxs-lookup"><span data-stu-id="77422-203">Drag left and right to move what portion of the recording is chosen.</span></span>  

### <a name="search-activities"></a><span data-ttu-id="77422-204">Activités de recherche</span><span class="sxs-lookup"><span data-stu-id="77422-204">Search activities</span></span>  

<span data-ttu-id="77422-205">Sélectionnez `Control` + `F` \(Windows, Linux\) ou `Command` + `F` \(macOS\) \*\*\*\* pour ouvrir la zone de recherche en bas du panneau Performances.</span><span class="sxs-lookup"><span data-stu-id="77422-205">Select `Control`+`F` \(Windows, Linux\) or `Command`+`F` \(macOS\) to open the search box at the bottom of the **Performance** panel.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-search-regex.msft.png" alt-text="Zone de recherche" lightbox="../media/evaluate-performance-performance-search-regex.msft.png":::
   <span data-ttu-id="77422-207">Zone de recherche</span><span class="sxs-lookup"><span data-stu-id="77422-207">The search box</span></span>  
:::image-end:::  

<span data-ttu-id="77422-208">Pour naviguer dans les activités qui correspondent à votre requête :</span><span class="sxs-lookup"><span data-stu-id="77422-208">To navigate activities that match your query:</span></span>  

*   <span data-ttu-id="77422-209">Utilisez les **boutons** Précédent \( ![ Précédent ](../media/previous-icon.msft.png) \) et **Suivant** \( ![ Suivant ](../media/next-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="77422-209">Use the **Previous** \(![Previous](../media/previous-icon.msft.png)\) and **Next** \(![Next](../media/next-icon.msft.png)\) buttons.</span></span>  
*   <span data-ttu-id="77422-210">Sélectionnez `Shift` + `Enter` le précédent ou `Enter` le suivant.</span><span class="sxs-lookup"><span data-stu-id="77422-210">Select `Shift`+`Enter` to select the previous or `Enter` to select the next.</span></span>  

<span data-ttu-id="77422-211">Pour modifier les paramètres de requête :</span><span class="sxs-lookup"><span data-stu-id="77422-211">To modify query settings:</span></span>  

*   <span data-ttu-id="77422-212">Choose **Case sensitive** \( Case sensitive ![ ](../media/search-case-icon.msft.png) \) to make the query case sensitive.</span><span class="sxs-lookup"><span data-stu-id="77422-212">Choose **Case sensitive** \(![Case sensitive](../media/search-case-icon.msft.png)\) to make the query case sensitive.</span></span>  
*   <span data-ttu-id="77422-213">Choisissez **Regex** \( ![ Regex ](../media/search-regex-icon.msft.png) \) pour utiliser une expression régulière dans votre requête.</span><span class="sxs-lookup"><span data-stu-id="77422-213">Choose **Regex** \(![Regex](../media/search-regex-icon.msft.png)\) to use a regular expression in your query.</span></span>  

<span data-ttu-id="77422-214">Pour masquer la zone de recherche, choisissez **Annuler.**</span><span class="sxs-lookup"><span data-stu-id="77422-214">To hide the search box, choose **Cancel**.</span></span>  

### <a name="view-main-thread-activity"></a><span data-ttu-id="77422-215">Afficher l’activité du thread principal</span><span class="sxs-lookup"><span data-stu-id="77422-215">View main thread activity</span></span>  

<span data-ttu-id="77422-216">Utilisez la section **Main** pour afficher l’activité qui s’est produite sur le thread principal de la page.</span><span class="sxs-lookup"><span data-stu-id="77422-216">Use the **Main** section to view activity that occurred on the main thread of the page.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-main-zoomed.msft.png" alt-text="Section Principale" lightbox="../media/evaluate-performance-performance-main-zoomed.msft.png":::
   <span data-ttu-id="77422-218">Section **Principale**</span><span class="sxs-lookup"><span data-stu-id="77422-218">The **Main** section</span></span>  
:::image-end:::  

<span data-ttu-id="77422-219">Choisissez un événement pour afficher plus d’informations à son sujet dans le **panneau Résumé.**</span><span class="sxs-lookup"><span data-stu-id="77422-219">Choose an event to view more information about it in the **Summary** panel.</span></span>  <span data-ttu-id="77422-220">DevTools décrit l’événement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="77422-220">DevTools outlines the selected event.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-summary-me.msft.png" alt-text="Plus d’informations sur la fonction anonyme dans le panneau Résumé" lightbox="../media/evaluate-performance-performance-summary-me.msft.png":::
   <span data-ttu-id="77422-222">Plus d’informations sur `anonymous` la fonction dans le panneau **Résumé**</span><span class="sxs-lookup"><span data-stu-id="77422-222">More information about the `anonymous` function in the **Summary** panel</span></span>  
:::image-end:::  

<span data-ttu-id="77422-223">DevTools représente l’activité de thread principale avec un graphique graphique.</span><span class="sxs-lookup"><span data-stu-id="77422-223">DevTools represents main thread activity with a flame chart.</span></span>  <span data-ttu-id="77422-224">L’axe X représente l’enregistrement au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="77422-224">The x-axis represents the recording over time.</span></span>  <span data-ttu-id="77422-225">L’axe Y représente la pile d’appels.</span><span class="sxs-lookup"><span data-stu-id="77422-225">The y-axis represents the call stack.</span></span>  <span data-ttu-id="77422-226">Les événements en haut provoquent les événements en dessous.</span><span class="sxs-lookup"><span data-stu-id="77422-226">The events on top cause the events below it.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-main-flame-chart.msft.png" alt-text="Graphique de graphique" lightbox="../media/evaluate-performance-performance-main-flame-chart.msft.png":::
   <span data-ttu-id="77422-228">Graphique de graphique</span><span class="sxs-lookup"><span data-stu-id="77422-228">A flame chart</span></span>  
:::image-end:::  

<span data-ttu-id="77422-229">Dans la figure précédente, un événement a `click` provoqué un événement sur la ligne `Function Call` `activitytabs.js` 53.</span><span class="sxs-lookup"><span data-stu-id="77422-229">In the previous figure, a `click` event caused a `Function Call` in `activitytabs.js` on line 53.</span></span>  <span data-ttu-id="77422-230">Vous trouverez `Function Call` ci-dessous un avis sur le fait qu’une fonction anonyme a été exécuté.</span><span class="sxs-lookup"><span data-stu-id="77422-230">Below `Function Call`, review that an anonymous function was run.</span></span>  <span data-ttu-id="77422-231">La fonction anonyme demandée `a` , qui a demandé , qui a demandé `wait` `Minor GC` .</span><span class="sxs-lookup"><span data-stu-id="77422-231">The anonymous function requested `a`, which requested `wait`, which requested `Minor GC`.</span></span>  

<span data-ttu-id="77422-232">DevTools affecte des couleurs aléatoires aux scripts.</span><span class="sxs-lookup"><span data-stu-id="77422-232">DevTools assigns scripts random colors.</span></span>  <span data-ttu-id="77422-233">Dans la figure précédente, les demandes de fonction d’un script sont colorées en vert clair.</span><span class="sxs-lookup"><span data-stu-id="77422-233">In the previous figure, function requests from one script are colored light green.</span></span>  <span data-ttu-id="77422-234">Les demandes provenant d’un autre script sont colorées.</span><span class="sxs-lookup"><span data-stu-id="77422-234">Requests from another script are colored beige.</span></span>  <span data-ttu-id="77422-235">Le jaune foncé représente l’activité de script et l’événement violet représente l’activité de rendu.</span><span class="sxs-lookup"><span data-stu-id="77422-235">The darker yellow represents scripting activity, and the purple event represents rendering activity.</span></span>  <span data-ttu-id="77422-236">Ces événements jaunes et violets plus foncés sont cohérents dans tous les enregistrements.</span><span class="sxs-lookup"><span data-stu-id="77422-236">These darker yellow and purple events are consistent across all recordings.</span></span>  

<span data-ttu-id="77422-237">Accédez [à Désactiver les exemples JavaScript si](#disable-javascript-samples) vous souhaitez masquer le graphique détaillé des requêtes JavaScript.</span><span class="sxs-lookup"><span data-stu-id="77422-237">Navigate to [Disable JavaScript samples](#disable-javascript-samples) if you want to hide the detailed flame chart of JavaScript requests.</span></span>  <span data-ttu-id="77422-238">Lorsque les exemples JS sont désactivés, seuls les événements de haut niveau tels que la figure précédente `Event: choose` `Function Call` `str` s’affichent.</span><span class="sxs-lookup"><span data-stu-id="77422-238">When JS samples are disabled, only high-level events such as `Event: choose` and `Function Call` from the previous figure `str` displayed.</span></span>  

### <a name="view-activities-in-a-table"></a><span data-ttu-id="77422-239">Afficher les activités dans un tableau</span><span class="sxs-lookup"><span data-stu-id="77422-239">View activities in a table</span></span>  

<span data-ttu-id="77422-240">Après avoir enregistré une page, vous n’avez pas besoin de vous appuyer uniquement sur la section **Main** pour analyser les activités.</span><span class="sxs-lookup"><span data-stu-id="77422-240">After recording a page, you do not need to rely solely on the **Main** section to analyze activities.</span></span>  <span data-ttu-id="77422-241">DevTools fournit également trois vues tabulaires pour l’analyse des activités.</span><span class="sxs-lookup"><span data-stu-id="77422-241">DevTools also provides three tabular views for analyzing activities.</span></span>  <span data-ttu-id="77422-242">Chaque affichage vous donne une perspective différente sur les activités :</span><span class="sxs-lookup"><span data-stu-id="77422-242">Each view gives you a different perspective on the activities:</span></span>  

*   <span data-ttu-id="77422-243">Lorsque vous souhaitez afficher les activités racine qui causent le plus de travail, utilisez le panneau Arborescence [des](#the-call-tree-panel) appels.</span><span class="sxs-lookup"><span data-stu-id="77422-243">When you want to view the root activities that cause the most work, use the [Call Tree](#the-call-tree-panel) panel.</span></span>  
*   <span data-ttu-id="77422-244">Lorsque vous souhaitez afficher les activités où le plus de temps a été passé directement, utilisez le [panneau de bas](#the-bottom-up-panel) en haut.</span><span class="sxs-lookup"><span data-stu-id="77422-244">When you want to view the activities where the most time was directly spent, use the [Bottom-Up](#the-bottom-up-panel) panel.</span></span>  
*   <span data-ttu-id="77422-245">Lorsque vous souhaitez afficher les activités dans l’ordre dans lequel elles se sont produites pendant l’enregistrement, utilisez le panneau [Journal des](#the-event-log-panel) événements.</span><span class="sxs-lookup"><span data-stu-id="77422-245">When you want to view the activities in the order in which they occurred during the recording, use the [Event Log](#the-event-log-panel) panel.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="77422-246">Les trois sections suivantes font toutes référence à la même démonstration.</span><span class="sxs-lookup"><span data-stu-id="77422-246">The next three sections all refer to the same demo.</span></span>  <span data-ttu-id="77422-247">Exécutez la démonstration vous-même [à la démonstration des onglets d’activité.][ActivityTabsDemo]</span><span class="sxs-lookup"><span data-stu-id="77422-247">Run the demo yourself at [Activity Tabs Demo][ActivityTabsDemo].</span></span>  

#### <a name="root-activities"></a><span data-ttu-id="77422-248">Activités racine</span><span class="sxs-lookup"><span data-stu-id="77422-248">Root activities</span></span>  

<span data-ttu-id="77422-249">Voici une explication **du concept** d’activités racine \*\*\*\* mentionné dans le panneau Arborescence des **appels,** le panneau inférieur vers le haut et le panneau **Journal des** événements.</span><span class="sxs-lookup"><span data-stu-id="77422-249">Here is an explanation of the **root activities** concept that is mentioned in the **Call Tree** panel, **Bottom-Up** panel, and **Event Log** panel.</span></span>  

<span data-ttu-id="77422-250">Les activités racines sont celles qui entraînent le travail du navigateur.</span><span class="sxs-lookup"><span data-stu-id="77422-250">Root activities are those which cause the browser to do some work.</span></span>  <span data-ttu-id="77422-251">Par exemple, lorsque vous choisissez une page web, le navigateur exécute une `Event` activité en tant qu’activité racine.</span><span class="sxs-lookup"><span data-stu-id="77422-251">For example, when you choose a webpage, the browser runs an `Event` activity as the root activity.</span></span>  <span data-ttu-id="77422-252">Cela `Event` peut entraîner l’exécuter, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="77422-252">That `Event` may cause a handler to run, and so on.</span></span>  

<span data-ttu-id="77422-253">Dans le graphique graphique de la section **Main,** les activités racine sont en haut du graphique.</span><span class="sxs-lookup"><span data-stu-id="77422-253">In the flame chart of the **Main** section, root activities are at the top of the chart.</span></span>  <span data-ttu-id="77422-254">Dans les **panneaux Arborescence des appels** **et Journal des** événements, les activités racines sont les éléments de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="77422-254">In the **Call Tree** and **Event Log** panels, root activities are the top-level items.</span></span>  

<span data-ttu-id="77422-255">Accédez au panneau [Arborescence des](#the-call-tree-panel) appels pour obtenir un exemple d’activités racine.</span><span class="sxs-lookup"><span data-stu-id="77422-255">Navigate to the [Call Tree](#the-call-tree-panel) panel for an example of root activities.</span></span>  

#### <a name="the-call-tree-panel"></a><span data-ttu-id="77422-256">Panneau Arborescence des appels</span><span class="sxs-lookup"><span data-stu-id="77422-256">The Call Tree panel</span></span>  

<span data-ttu-id="77422-257">Utilisez le **panneau Arborescence des** appels pour afficher les [activités racine qui](#root-activities) sont à l’origine du travail le plus important.</span><span class="sxs-lookup"><span data-stu-id="77422-257">Use the **Call Tree** panel to view which [root activities](#root-activities) cause the most work.</span></span>  

<span data-ttu-id="77422-258">Le **panneau Arborescence** des appels affiche uniquement les activités pendant la partie sélectionnée de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="77422-258">The **Call Tree** panel only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="77422-259">Accédez [à Sélectionner une partie d’un enregistrement](#select-a-portion-of-a-recording) pour découvrir comment sélectionner des parties.</span><span class="sxs-lookup"><span data-stu-id="77422-259">Navigate to [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-call-tree.msft.png" alt-text="Panneau Arborescence des appels" lightbox="../media/evaluate-performance-performance-call-tree.msft.png":::
   <span data-ttu-id="77422-261">Panneau **Arborescence des** appels</span><span class="sxs-lookup"><span data-stu-id="77422-261">The **Call Tree** panel</span></span>  
:::image-end:::  

<span data-ttu-id="77422-262">Dans la figure précédente, le niveau \*\*\*\* supérieur des éléments dans la colonne Activité, tels que les activités racine, `Evaluate Script` et sont des activités `Parse HTML` racine.</span><span class="sxs-lookup"><span data-stu-id="77422-262">In the previous figure, the top-level of items in the **Activity** column, such as `Evaluate Script` and `Parse HTML` are root activities.</span></span>  <span data-ttu-id="77422-263">L’imbrmbrage représente la pile d’appels.</span><span class="sxs-lookup"><span data-stu-id="77422-263">The nesting represents the call stack.</span></span>  <span data-ttu-id="77422-264">Par exemple, dans la figure précédente, ce `Parse HTML` qui a provoqué et `Evaluate Script` `Compile Script` `(anonymous)` .</span><span class="sxs-lookup"><span data-stu-id="77422-264">For example, in the previous figure, `Parse HTML` which caused `Evaluate Script` which caused `Compile Script` and `(anonymous)`.</span></span>  

<span data-ttu-id="77422-265">**Le temps libre** représente le temps passé directement dans cette activité.</span><span class="sxs-lookup"><span data-stu-id="77422-265">**Self Time** represents the time directly spent in that activity.</span></span>  <span data-ttu-id="77422-266">**Le temps** total représente le temps consacré à cette activité ou à l’un des enfants.</span><span class="sxs-lookup"><span data-stu-id="77422-266">**Total Time** represents the time spent in that activity or any of the children.</span></span>  

<span data-ttu-id="77422-267">Choisissez **Temps libre,** **Temps total**ou **Activité** pour trier le tableau par colonne.</span><span class="sxs-lookup"><span data-stu-id="77422-267">Choose **Self Time**, **Total Time**, or **Activity** to sort the table by that column.</span></span>  

<span data-ttu-id="77422-268">Utilisez la zone de texte **Filtrer** pour filtrer les événements par nom d’activité.</span><span class="sxs-lookup"><span data-stu-id="77422-268">Use the **Filter** text box to filter events by activity name.</span></span>  

<span data-ttu-id="77422-269">Par défaut, le menu **De** regroupement est définie sur **Aucun regroupement.**</span><span class="sxs-lookup"><span data-stu-id="77422-269">By default the **Grouping** menu is set to **No Grouping**.</span></span>  <span data-ttu-id="77422-270">Utilisez le menu **Regroupement pour** trier le tableau d’activité en fonction de différents critères.</span><span class="sxs-lookup"><span data-stu-id="77422-270">Use the **Grouping** menu to sort the activity table based on various criteria.</span></span>  

<span data-ttu-id="77422-271">Choose **Show Heaviest Stack** \( Show ![ Heaviest Stack ](../media/show-heaviest-stack-icon.msft.png) \) to reveal another table to the right of the **Activity** table.</span><span class="sxs-lookup"><span data-stu-id="77422-271">Choose **Show Heaviest Stack** \(![Show Heaviest Stack](../media/show-heaviest-stack-icon.msft.png)\) to reveal another table to the right of the **Activity** table.</span></span>  <span data-ttu-id="77422-272">Choisissez une activité pour remplir la table **Stack la plus** lourde.</span><span class="sxs-lookup"><span data-stu-id="77422-272">Choose an activity to populate the **Heaviest Stack** table.</span></span>  <span data-ttu-id="77422-273">Le **tableau Stack le plus lourd** affiche les enfants de l’activité sélectionnée qui ont mis le plus de temps à s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="77422-273">The **Heaviest Stack** table displays which children of the selected activity took the longest time to run.</span></span>  

#### <a name="the-bottom-up-panel"></a><span data-ttu-id="77422-274">Panneau de Bottom-Up</span><span class="sxs-lookup"><span data-stu-id="77422-274">The Bottom-Up panel</span></span>  

<span data-ttu-id="77422-275">Utilisez le **panneau Bas vers le** haut pour afficher les activités qui ont pris le plus de temps dans l’agrégation.</span><span class="sxs-lookup"><span data-stu-id="77422-275">Use the **Bottom-Up** panel to view which activities directly took up the most time in aggregate.</span></span>  

<span data-ttu-id="77422-276">Le **panneau Inférieur vers le** haut affiche uniquement les activités pendant la partie sélectionnée de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="77422-276">The **Bottom-Up** panel only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="77422-277">Accédez [à Sélectionner une partie d’un enregistrement](#select-a-portion-of-a-recording) pour découvrir comment sélectionner des parties.</span><span class="sxs-lookup"><span data-stu-id="77422-277">Navigate to [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-bottoms-up.msft.png" alt-text="Panneau de Bottom-Up" lightbox="../media/evaluate-performance-performance-bottoms-up.msft.png":::
   <span data-ttu-id="77422-279">Panneau **bas vers le** haut</span><span class="sxs-lookup"><span data-stu-id="77422-279">The **Bottom-Up** panel</span></span>  
:::image-end:::  

<span data-ttu-id="77422-280">Dans le **graphique de** la section Main de la figure précédente, accédez à cette quasi-totalité du temps passé en cours d’exécution. `Parse HTML`</span><span class="sxs-lookup"><span data-stu-id="77422-280">In the **Main** section flame chart of the previous figure, navigate to that almost practically all of the time was spent running `Parse HTML`.</span></span>  <span data-ttu-id="77422-281">L’activité la plus importante dans **le panneau De** bas en haut de la figure précédente est `Parse HTML` .</span><span class="sxs-lookup"><span data-stu-id="77422-281">The top activity in the **Bottom-Up** panel of the previous figure is `Parse HTML`.</span></span>  <!--In the flame chart of the previous figure, the yellow below the calls to `wait` are actually thousands of `Minor GC` calls.  -->  <span data-ttu-id="77422-282">Accédez au **panneau De bas en** haut, l’activité la plus coûteuse suivante est `Layout` .</span><span class="sxs-lookup"><span data-stu-id="77422-282">Navigate to the **Bottom-Up** panel, the next most expensive activity is `Layout`.</span></span>  

<span data-ttu-id="77422-283">La **colonne Temps** libre représente le temps agrégé passé directement dans cette activité, dans toutes les occurrences.</span><span class="sxs-lookup"><span data-stu-id="77422-283">The **Self Time** column represents the aggregated time spent directly in that activity, across all of the occurrences.</span></span>  

<span data-ttu-id="77422-284">La **colonne Temps total** représente le temps agrégé passé dans cette activité ou n’importe quel enfant.</span><span class="sxs-lookup"><span data-stu-id="77422-284">The **Total Time** column represents aggregated time spent in that activity or any of the children.</span></span>  

#### <a name="the-event-log-panel"></a><span data-ttu-id="77422-285">Panneau Journal des événements</span><span class="sxs-lookup"><span data-stu-id="77422-285">The Event Log panel</span></span>  

<span data-ttu-id="77422-286">Utilisez le **panneau Journal des** événements pour afficher les activités dans l’ordre dans lequel elles se sont produites pendant l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="77422-286">Use the **Event Log** panel to view activities in the order in which they occurred during the recording.</span></span>  

<span data-ttu-id="77422-287">Le **panneau Journal des** événements affiche uniquement les activités pendant la partie sélectionnée de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="77422-287">The **Event Log** panel only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="77422-288">Accédez [à Sélectionner une partie d’un enregistrement](#select-a-portion-of-a-recording) pour découvrir comment sélectionner des parties.</span><span class="sxs-lookup"><span data-stu-id="77422-288">Navigate to [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-event-log.msft.png" alt-text="Panneau Journal des événements" lightbox="../media/evaluate-performance-performance-event-log.msft.png":::
   <span data-ttu-id="77422-290">Panneau **Journal des événements**</span><span class="sxs-lookup"><span data-stu-id="77422-290">The **Event Log** panel</span></span>  
:::image-end:::  

<span data-ttu-id="77422-291">La **colonne Heure** de début représente le point auquel cette activité a démarré, par rapport au début de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="77422-291">The **Start Time** column represents the point at which that activity started, relative to the start of the recording.</span></span>  <span data-ttu-id="77422-292">Par exemple, l’heure de début de l’élément sélectionné dans la figure précédente signifie que l’activité a démarré 175,7 ms après le démarrage de `175.7 ms` l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="77422-292">For example, the start time of `175.7 ms` for the selected item in the previous figure means that activity started 175.7 ms after the recording started.</span></span>  

<span data-ttu-id="77422-293">La **colonne Temps** libre représente le temps passé directement dans cette activité.</span><span class="sxs-lookup"><span data-stu-id="77422-293">The **Self Time** column represents the time spent directly in that activity.</span></span>  

<span data-ttu-id="77422-294">Les **colonnes Temps** total représentent le temps passé directement dans cette activité ou dans l’un des enfants.</span><span class="sxs-lookup"><span data-stu-id="77422-294">The **Total Time** columns represents time spent directly in that activity or in any of the children.</span></span>  

<span data-ttu-id="77422-295">Choisissez **Heure de début,** **Temps**libre ou **Durée totale** pour trier le tableau par colonne.</span><span class="sxs-lookup"><span data-stu-id="77422-295">Choose **Start Time**, **Self Time**, or **Total Time** to sort the table by that column.</span></span>

<span data-ttu-id="77422-296">Utilisez la **zone de** texte Filtrer pour filtrer les activités par nom.</span><span class="sxs-lookup"><span data-stu-id="77422-296">Use the **Filter** text box to filter activities by name.</span></span>  

<span data-ttu-id="77422-297">Utilisez le menu **Durée** pour filtrer toutes les activités dont la durée est inférieure à 1 ms ou 15 ms.</span><span class="sxs-lookup"><span data-stu-id="77422-297">Use the **Duration** menu to filter out any activities that took less than 1 ms or 15 ms.</span></span>  <span data-ttu-id="77422-298">Par défaut, le menu **Durée** est définie sur **Tous,** ce qui signifie que toutes les activités sont affichées.</span><span class="sxs-lookup"><span data-stu-id="77422-298">By default the **Duration** menu is set to **All**, meaning all activities are shown.</span></span>  

<span data-ttu-id="77422-299">Désactivez les case à cocher **Chargement,** **Script,** \*\*\*\* **Rendu**ou Dessin pour filtrer toutes les activités de ces catégories.</span><span class="sxs-lookup"><span data-stu-id="77422-299">Disable the **Loading**, **Scripting**, **Rendering**, or **Painting** checkboxes to filter out all activities from those categories.</span></span>  

### <a name="view-gpu-activity"></a><span data-ttu-id="77422-300">Afficher l’activité GPU</span><span class="sxs-lookup"><span data-stu-id="77422-300">View GPU activity</span></span>  

<span data-ttu-id="77422-301">Afficher l’activité GPU dans la section **GPU.**</span><span class="sxs-lookup"><span data-stu-id="77422-301">View GPU activity in the **GPU** section.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-gpu-zoomed.msft.png" alt-text="Section GPU" lightbox="../media/evaluate-performance-performance-gpu-zoomed.msft.png":::
   <span data-ttu-id="77422-303">Section **GPU**</span><span class="sxs-lookup"><span data-stu-id="77422-303">The **GPU** section</span></span>  
:::image-end:::  

### <a name="view-raster-activity"></a><span data-ttu-id="77422-304">Afficher l’activité de raster</span><span class="sxs-lookup"><span data-stu-id="77422-304">View raster activity</span></span>  

<span data-ttu-id="77422-305">Afficher l’activité de raster dans la section **Raster.**</span><span class="sxs-lookup"><span data-stu-id="77422-305">View raster activity in the **Raster** section.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-raster.msft.png" alt-text="Section Raster" lightbox="../media/evaluate-performance-performance-raster.msft.png":::
   <span data-ttu-id="77422-307">Section **Raster**</span><span class="sxs-lookup"><span data-stu-id="77422-307">The **Raster** section</span></span>  
:::image-end:::  

### <a name="view-interactions"></a><span data-ttu-id="77422-308">Afficher les interactions</span><span class="sxs-lookup"><span data-stu-id="77422-308">View interactions</span></span>  

<span data-ttu-id="77422-309">Utilisez la section **Interactions pour** rechercher et analyser les interactions utilisateur qui se sont produites pendant l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="77422-309">Use the **Interactions** section to find and analyze user interactions that happened during the recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-interactions-animation.msft.png" alt-text="Section Interactions" lightbox="../media/evaluate-performance-performance-interactions-animation.msft.png":::
   <span data-ttu-id="77422-311">Section **Interactions**</span><span class="sxs-lookup"><span data-stu-id="77422-311">The **Interactions** section</span></span>  
:::image-end:::  

<span data-ttu-id="77422-312">Une ligne rouge au bas d’une interaction représente le temps passé à attendre le thread principal.</span><span class="sxs-lookup"><span data-stu-id="77422-312">A red line at the bottom of an interaction represents time spent waiting for the main thread.</span></span>  

<span data-ttu-id="77422-313">Choisissez une interaction pour afficher plus d’informations à ce sujet dans le **panneau Résumé.**</span><span class="sxs-lookup"><span data-stu-id="77422-313">Choose an interaction to view more information about it in the **Summary** panel.</span></span>  

### <a name="analyze-frames-per-second-fps"></a><span data-ttu-id="77422-314">Analyser les images par seconde (FPS)</span><span class="sxs-lookup"><span data-stu-id="77422-314">Analyze frames per second (FPS)</span></span>  

<span data-ttu-id="77422-315">DevTools offre de nombreuses façons d’analyser les images par seconde :</span><span class="sxs-lookup"><span data-stu-id="77422-315">DevTools provides numerous ways to analyze frames per second:</span></span>  

*   <span data-ttu-id="77422-316">Utilisez [le graphique FPS pour](#the-fps-chart) obtenir une vue d’ensemble du service FPS pendant toute la durée de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="77422-316">Use [the FPS chart](#the-fps-chart) to get an overview of FPS over the duration of the recording.</span></span>  
*   <span data-ttu-id="77422-317">Utilisez [la section Frames pour](#the-frames-section) afficher la durée d’un cadre particulier.</span><span class="sxs-lookup"><span data-stu-id="77422-317">Use [the Frames section](#the-frames-section) to view how long a particular frame took.</span></span>  
*   <span data-ttu-id="77422-318">Utilisez la **jauge FPS** pour une estimation en temps réel du service FPS lors de l’utilisation de la page.</span><span class="sxs-lookup"><span data-stu-id="77422-318">Use the **FPS meter** for a realtime estimate of FPS as the page runs.</span></span>  <span data-ttu-id="77422-319">Accédez à [Afficher les images par seconde en temps réel avec la jauge FPS.](#view-frames-per-second-in-realtime-with-the-fps-meter)</span><span class="sxs-lookup"><span data-stu-id="77422-319">Navigate to [View frames per second in realtime with the FPS meter](#view-frames-per-second-in-realtime-with-the-fps-meter).</span></span>  
    
#### <a name="the-fps-chart"></a><span data-ttu-id="77422-320">Graphique FPS</span><span class="sxs-lookup"><span data-stu-id="77422-320">The FPS chart</span></span>  

<span data-ttu-id="77422-321">Le **graphique FPS** fournit une vue d’ensemble de la fréquence d’images pendant toute la durée d’un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="77422-321">The **FPS** chart provides an overview of the frame rate across the duration of a recording.</span></span>  <span data-ttu-id="77422-322">En règle générale, plus la barre verte est élevée, plus la fréquence d’images est élevée.</span><span class="sxs-lookup"><span data-stu-id="77422-322">In general, the higher the green bar, the better the frame rate.</span></span>  

<span data-ttu-id="77422-323">Une barre rouge au-dessus **du graphique FPS** est un avertissement signalant que la fréquence d’images a été si faible qu’elle a probablement nuire à l’expérience de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="77422-323">A red bar above the **FPS** chart is a warning that the frame rate dropped so low that it probably harmed the user's experience.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-fps-highlight.msft.png" alt-text="Graphique FPS" lightbox="../media/evaluate-performance-performance-fps-highlight.msft.png":::
   <span data-ttu-id="77422-325">Graphique **FPS**</span><span class="sxs-lookup"><span data-stu-id="77422-325">The **FPS** chart</span></span>  
:::image-end:::  

#### <a name="the-frames-section"></a><span data-ttu-id="77422-326">Section Cadres</span><span class="sxs-lookup"><span data-stu-id="77422-326">The Frames section</span></span>  

<span data-ttu-id="77422-327">La section **Frames** vous indique exactement la durée d’un cadre particulier.</span><span class="sxs-lookup"><span data-stu-id="77422-327">The **Frames** section tells you exactly how long a particular frame took.</span></span>  

<span data-ttu-id="77422-328">Pointez sur un cadre pour afficher une info-bulle avec plus d’informations à son sujet.</span><span class="sxs-lookup"><span data-stu-id="77422-328">Hover on a frame to view a tooltip with more information about it.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-frames-hover.msft.png" alt-text="Pointer sur un cadre" lightbox="../media/evaluate-performance-performance-frames-hover.msft.png":::
   <span data-ttu-id="77422-330">Pointer sur un cadre</span><span class="sxs-lookup"><span data-stu-id="77422-330">Hover on a frame</span></span>  
:::image-end:::  

<span data-ttu-id="77422-331">Choisissez un cadre pour afficher plus d’informations sur le cadre dans le **panneau Résumé.**</span><span class="sxs-lookup"><span data-stu-id="77422-331">Choose a frame to view more information about the frame in the **Summary** panel.</span></span>  <span data-ttu-id="77422-332">DevTools présente le cadre sélectionné en bleu.</span><span class="sxs-lookup"><span data-stu-id="77422-332">DevTools outlines the selected frame in blue.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-frames-summary.msft.png" alt-text="Afficher un cadre dans le panneau Résumé" lightbox="../media/evaluate-performance-performance-frames-summary.msft.png":::
   <span data-ttu-id="77422-334">Afficher un cadre dans le **panneau Résumé**</span><span class="sxs-lookup"><span data-stu-id="77422-334">View a frame in the **Summary** panel</span></span>  
:::image-end:::  

### <a name="view-network-requests"></a><span data-ttu-id="77422-335">Afficher les demandes réseau</span><span class="sxs-lookup"><span data-stu-id="77422-335">View network requests</span></span>  

<span data-ttu-id="77422-336">Développez la section **Réseau** pour afficher une cascade de demandes réseau qui se sont produites pendant l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="77422-336">Expand the **Network** section to view a waterfall of network requests that occurred during the recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-network.msft.png" alt-text="Section Réseau" lightbox="../media/evaluate-performance-performance-network.msft.png":::
   <span data-ttu-id="77422-338">Section **Réseau**</span><span class="sxs-lookup"><span data-stu-id="77422-338">The **Network** section</span></span>  
:::image-end:::  

<span data-ttu-id="77422-339">Les demandes sont codées en couleur comme suit :</span><span class="sxs-lookup"><span data-stu-id="77422-339">Requests are color-coded as follows:</span></span>  

*   <span data-ttu-id="77422-340">HTML : Bleu</span><span class="sxs-lookup"><span data-stu-id="77422-340">HTML: Blue</span></span>  
*   <span data-ttu-id="77422-341">CSS : Violet</span><span class="sxs-lookup"><span data-stu-id="77422-341">CSS: Purple</span></span>  
*   <span data-ttu-id="77422-342">JS : Jaune</span><span class="sxs-lookup"><span data-stu-id="77422-342">JS: Yellow</span></span>  
*   <span data-ttu-id="77422-343">Images : vert</span><span class="sxs-lookup"><span data-stu-id="77422-343">Images: Green</span></span>  
    
<span data-ttu-id="77422-344">Choisissez une demande pour afficher plus d’informations à son sujet dans le **panneau De** synthèse.</span><span class="sxs-lookup"><span data-stu-id="77422-344">Choose a request to view more information about it in the **Summary** panel.</span></span>  <span data-ttu-id="77422-345">Par exemple, dans la \*\*\*\* figure précédente, le panneau Résumé affiche plus d’informations sur la demande bleue sélectionnée dans la section **Réseau.**</span><span class="sxs-lookup"><span data-stu-id="77422-345">For example, in the previous figure, the **Summary** panel is displaying more information about the blue request that is selected in the **Network** section.</span></span>  

<span data-ttu-id="77422-346">Un carré bleu foncé dans le haut à gauche d’une demande signifie qu’il s’agit d’une demande de priorité supérieure.</span><span class="sxs-lookup"><span data-stu-id="77422-346">A darker-blue square in the top-left of a request means it is a higher-priority request.</span></span>  <span data-ttu-id="77422-347">Un carré bleu clair signifie une priorité inférieure.</span><span class="sxs-lookup"><span data-stu-id="77422-347">A lighter-blue square means lower-priority.</span></span>  <span data-ttu-id="77422-348">Par exemple, dans la figure précédente, la demande sélectionnée en bleu est de priorité supérieure et la demande verte en dessous est de priorité inférieure.</span><span class="sxs-lookup"><span data-stu-id="77422-348">For example, in the previous figure, the blue, selected request is higher-priority, and the green one below it is lower-priority.</span></span>  

<span data-ttu-id="77422-349">Dans la première des figures suivantes, la demande est représentée par une ligne à gauche, une barre au milieu avec une partie sombre et une partie claire, et une ligne à `www.bing.com` droite.</span><span class="sxs-lookup"><span data-stu-id="77422-349">In the 1st of the following figures, the request for `www.bing.com` is represented by a line on the left, a bar in the middle with a dark portion and a light portion, and a line on the right.</span></span>  <span data-ttu-id="77422-350">La deuxième des figures suivantes montre la représentation correspondante \*\*\*\* de la même demande dans le panneau Minutage de **l’outil** Réseau.</span><span class="sxs-lookup"><span data-stu-id="77422-350">In the 2nd of the following figures shows the corresponding representation of the same request in the **Timing** panel of the **Network** tool.</span></span>  <span data-ttu-id="77422-351">Voici comment ces deux représentations se maient l’une à l’autre :</span><span class="sxs-lookup"><span data-stu-id="77422-351">Here is how these two representations map to each other:</span></span>

*   <span data-ttu-id="77422-352">La ligne de gauche est tout jusqu’au `Connection Start` groupe d’événements, inclus.</span><span class="sxs-lookup"><span data-stu-id="77422-352">The left line is everything up to the `Connection Start` group of events, inclusive.</span></span>  <span data-ttu-id="77422-353">En d’autres termes, il s’agit de tout ce qui est `Request Sent` avant , exclusif.</span><span class="sxs-lookup"><span data-stu-id="77422-353">In other words, it is everything before `Request Sent`, exclusive.</span></span>  
*   <span data-ttu-id="77422-354">La partie claire de la barre est `Request Sent` et `Waiting (TTFB)` .</span><span class="sxs-lookup"><span data-stu-id="77422-354">The light portion of the bar is `Request Sent` and `Waiting (TTFB)`.</span></span>  
*   <span data-ttu-id="77422-355">La partie sombre de la barre est `Content Download` .</span><span class="sxs-lookup"><span data-stu-id="77422-355">The dark portion of the bar is `Content Download`.</span></span>  
*   <span data-ttu-id="77422-356">La droite est essentiellement le temps passé à attendre le thread principal.</span><span class="sxs-lookup"><span data-stu-id="77422-356">The right line is essentially time spent waiting for the main thread.</span></span>  <span data-ttu-id="77422-357">Cela n’est pas représenté dans le **panneau Minutage.**</span><span class="sxs-lookup"><span data-stu-id="77422-357">This is not represented in the **Timing** panel.</span></span>  
    
:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-performance-network.msft.png" alt-text="Représentation de la barre de lignes de la demande www.bing.com ligne" lightbox="../media/evaluate-performance-bing-performance-network.msft.png":::
         <span data-ttu-id="77422-359">Représentation de la demande dans la barre de `www.bing.com` lignes</span><span class="sxs-lookup"><span data-stu-id="77422-359">The line-bar representation of the `www.bing.com` request</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-network-timing.msft.png" alt-text="L’outil Réseau" lightbox="../media/evaluate-performance-bing-network-timing.msft.png":::
         <span data-ttu-id="77422-361">**L’outil** Réseau</span><span class="sxs-lookup"><span data-stu-id="77422-361">The **Network** tool</span></span>  
<span data-ttu-id="77422-362">: ::image-end:::</span><span class="sxs-lookup"><span data-stu-id="77422-362">:     ::image-end:::</span></span>  
   :::column-end:::
:::row-end:::

### <a name="view-memory-metrics"></a><span data-ttu-id="77422-363">Afficher les mesures de mémoire</span><span class="sxs-lookup"><span data-stu-id="77422-363">View memory metrics</span></span>  

<span data-ttu-id="77422-364">Activer la case **à** cocher Mémoire pour afficher les mesures de mémoire du dernier enregistrement.</span><span class="sxs-lookup"><span data-stu-id="77422-364">Turn on the **Memory** checkbox to view memory metrics from the last recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-memory-highlight.msft.png" alt-text="Case à cocher Mémoire" lightbox="../media/evaluate-performance-performance-memory-highlight.msft.png":::
   <span data-ttu-id="77422-366">Case **à** cocher Mémoire</span><span class="sxs-lookup"><span data-stu-id="77422-366">The **Memory** checkbox</span></span>  
:::image-end:::  

<span data-ttu-id="77422-367">DevTools affiche un \*\*\*\* nouveau graphique mémoire, au-dessus du **panneau Résumé.**</span><span class="sxs-lookup"><span data-stu-id="77422-367">DevTools displays a new **Memory** chart, above the **Summary** panel.</span></span>  <span data-ttu-id="77422-368">Il existe également un nouveau graphique sous le **graphique NET,** appelé **TAS**.</span><span class="sxs-lookup"><span data-stu-id="77422-368">There is also a new chart below the **NET** chart, called **HEAP**.</span></span>  <span data-ttu-id="77422-369">Le **graphique HEAP** fournit les mêmes informations que la ligne Tas **JS** dans le **graphique mémoire.**</span><span class="sxs-lookup"><span data-stu-id="77422-369">The **HEAP** chart provides the same information as the **JS Heap** line in the **Memory** chart.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-memory-chart.msft.png" alt-text="Mesures de mémoire" lightbox="../media/evaluate-performance-performance-memory-chart.msft.png":::
   <span data-ttu-id="77422-371">Mesures de mémoire</span><span class="sxs-lookup"><span data-stu-id="77422-371">Memory metrics</span></span>  
:::image-end:::  

<span data-ttu-id="77422-372">Les lignes de couleur sur le graphique sont m interactives avec les case à cocher colorées au-dessus du graphique.</span><span class="sxs-lookup"><span data-stu-id="77422-372">The colored lines on the chart map to the colored checkboxes above the chart.</span></span>  
<span data-ttu-id="77422-373">Désactivez une case à cocher pour masquer cette catégorie dans le graphique.</span><span class="sxs-lookup"><span data-stu-id="77422-373">Disable a checkbox to hide that category from the chart.</span></span>  

<span data-ttu-id="77422-374">Le graphique affiche uniquement la région de l’enregistrement actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="77422-374">The chart only displays the region of the recording that is currently selected.</span></span>  <span data-ttu-id="77422-375">Par exemple, dans la \*\*\*\* figure précédente, le graphique Mémoire affiche uniquement l’utilisation de la mémoire d’environ 400 ms à la marque 1750 ms.</span><span class="sxs-lookup"><span data-stu-id="77422-375">For example, in the previous figure, the **Memory** chart is only showing memory usage from around the 400 ms mark to the 1750 ms mark.</span></span>  

### <a name="view-the-duration-of-a-portion-of-a-recording"></a><span data-ttu-id="77422-376">Afficher la durée d’une partie d’un enregistrement</span><span class="sxs-lookup"><span data-stu-id="77422-376">View the duration of a portion of a recording</span></span>  

<span data-ttu-id="77422-377">Lors de l’analyse d’une section telle que **Réseau** ou **Main,** vous avez parfois besoin d’une estimation plus précise de la durée de certains événements.</span><span class="sxs-lookup"><span data-stu-id="77422-377">When analyzing a section like **Network** or **Main**, sometimes you need a more precise estimate of how long certain events took.</span></span>  <span data-ttu-id="77422-378">`Shift`Maintenez, choisissez et maintenez, puis faites glisser vers la gauche ou la droite pour sélectionner une partie de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="77422-378">Hold `Shift`, choose and hold, and drag left or right to select a portion of the recording.</span></span>  <span data-ttu-id="77422-379">En bas de votre sélection, DevTools indique la durée de cette portion.</span><span class="sxs-lookup"><span data-stu-id="77422-379">At the bottom of your selection, DevTools shows how long that portion took.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-main-duration.msft.png" alt-text="Afficher la durée d’une partie d’un enregistrement" lightbox="../media/evaluate-performance-performance-main-duration.msft.png":::
   <span data-ttu-id="77422-381">Afficher la durée d’une partie d’un enregistrement</span><span class="sxs-lookup"><span data-stu-id="77422-381">View the duration of a portion of a recording</span></span>  
:::image-end:::  

### <a name="view-a-screenshot"></a><span data-ttu-id="77422-382">Afficher une capture d’écran</span><span class="sxs-lookup"><span data-stu-id="77422-382">View a screenshot</span></span>  

<span data-ttu-id="77422-383">Accédez à [Capture d’écran lors de l’enregistrement](#capture-screenshots-while-recording) pour découvrir comment activer les captures d’écran.</span><span class="sxs-lookup"><span data-stu-id="77422-383">Navigate to [Capture screenshots while recording](#capture-screenshots-while-recording) to learn how to turn on screenshots.</span></span>  

<span data-ttu-id="77422-384">Pointez sur la **vue d’ensemble** pour afficher une capture d’écran de l’affichage de la page pendant ce moment de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="77422-384">Hover on the **Overview** to view a screenshot of how the page looked during that moment of the recording.</span></span>  <span data-ttu-id="77422-385">La **vue d’ensemble** est la section qui contient les graphiques **UC,** **FPS**et **NET.**</span><span class="sxs-lookup"><span data-stu-id="77422-385">The **Overview** is the section that contains the **CPU**, **FPS**, and **NET** charts.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-screenshots-hover.msft.png" alt-text="Afficher une capture d’écran" lightbox="../media/evaluate-performance-performance-screenshots-hover.msft.png":::
   <span data-ttu-id="77422-387">Afficher une capture d’écran</span><span class="sxs-lookup"><span data-stu-id="77422-387">View a screenshot</span></span>  
:::image-end:::  

<span data-ttu-id="77422-388">Vous pouvez également afficher des captures d’écran en choisissant un cadre dans la section **Cadres.**</span><span class="sxs-lookup"><span data-stu-id="77422-388">You may also view screenshots by choosing a frame in the **Frames** section.</span></span>  <span data-ttu-id="77422-389">DevTools affiche une petite version de la capture d’écran dans le **panneau Résumé.**</span><span class="sxs-lookup"><span data-stu-id="77422-389">DevTools displays a small version of the screenshot in the **Summary** panel.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview.msft.png" alt-text="Afficher une capture d’écran dans le panneau Résumé" lightbox="../media/evaluate-performance-performance-summary-preview.msft.png":::
   <span data-ttu-id="77422-391">Afficher une capture d’écran dans le **panneau Résumé**</span><span class="sxs-lookup"><span data-stu-id="77422-391">View a screenshot in the **Summary** panel</span></span>  
:::image-end:::  

<span data-ttu-id="77422-392">Choisissez la miniature du panneau Résumé **pour** effectuer un zoom avant sur la capture d’écran.</span><span class="sxs-lookup"><span data-stu-id="77422-392">Choose the thumbnail in the **Summary** panel to zoom in on the screenshot.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview-select.msft.png" alt-text="Zoom sur une capture d’écran à partir du panneau Résumé" lightbox="../media/evaluate-performance-performance-summary-preview-select.msft.png":::
   <span data-ttu-id="77422-394">Zoom sur une capture d’écran à partir du **panneau Résumé**</span><span class="sxs-lookup"><span data-stu-id="77422-394">Zoom into a screenshot from the **Summary** panel</span></span>  
:::image-end:::  

### <a name="view-layers-information"></a><span data-ttu-id="77422-395">Afficher les informations sur les couches</span><span class="sxs-lookup"><span data-stu-id="77422-395">View layers information</span></span>  

<span data-ttu-id="77422-396">Pour afficher les informations sur les couches avancées sur un cadre :</span><span class="sxs-lookup"><span data-stu-id="77422-396">To view advanced layers information about a frame:</span></span>  

1.  <span data-ttu-id="77422-397">[Activer l’instrumentation de pinceau avancée.](#turn-on-advanced-paint-instrumentation)</span><span class="sxs-lookup"><span data-stu-id="77422-397">[Turn on advanced paint instrumentation](#turn-on-advanced-paint-instrumentation).</span></span>  
1.  <span data-ttu-id="77422-398">Choisissez un cadre dans la section **Cadres.**</span><span class="sxs-lookup"><span data-stu-id="77422-398">Choose a frame in the **Frames** section.</span></span>  <span data-ttu-id="77422-399">DevTools affiche des informations sur les couches du nouveau panneau **Calques,** à côté du panneau **Journal des** événements.</span><span class="sxs-lookup"><span data-stu-id="77422-399">DevTools displays information about the layers in the new **Layers** panel, next to the **Event Log** panel.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-layers-all.msft.png" alt-text="Volet Calques" lightbox="../media/evaluate-performance-layers-all.msft.png":::
       <span data-ttu-id="77422-401">Volet **Calques**</span><span class="sxs-lookup"><span data-stu-id="77422-401">The **Layers** pane</span></span>  
    :::image-end:::  
    
<span data-ttu-id="77422-402">Pointez sur un calque pour le surligner dans le diagramme.</span><span class="sxs-lookup"><span data-stu-id="77422-402">Hover on a layer to highlight it in the diagram.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png" alt-text="Surligner un calque" lightbox="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png":::
   <span data-ttu-id="77422-404">Surligner un calque</span><span class="sxs-lookup"><span data-stu-id="77422-404">Highlight a layer</span></span>  
:::image-end:::  

<span data-ttu-id="77422-405">Pour déplacer le diagramme :</span><span class="sxs-lookup"><span data-stu-id="77422-405">To move the diagram:</span></span>  

*   <span data-ttu-id="77422-406">Choisissez **Pan Mode** \( Pan Mode ![ ](../media/pan-mode-icon.msft.png) \) pour vous déplacer le long des axes X et Y.</span><span class="sxs-lookup"><span data-stu-id="77422-406">Choose **Pan Mode** \(![Pan Mode](../media/pan-mode-icon.msft.png)\) to move along the X and Y axes.</span></span>  
*   <span data-ttu-id="77422-407">Choisissez **Le mode Rotation** \( Mode rotation ![ ](../media/rotate-mode-icon.msft.png) \) pour faire pivoter le long de l’axe Z.</span><span class="sxs-lookup"><span data-stu-id="77422-407">Choose **Rotate Mode** \(![Rotate Mode](../media/rotate-mode-icon.msft.png)\) to rotate along the Z axis.</span></span>  
*   <span data-ttu-id="77422-408">Choisissez **Réinitialiser la transformation** \( ![ Réinitialiser la transformation \) pour rétablir la position ](../media/reset-transform-icon.msft.png) d’origine du diagramme.</span><span class="sxs-lookup"><span data-stu-id="77422-408">Choose **Reset Transform** \(![Reset Transform](../media/reset-transform-icon.msft.png)\) to reset the diagram to the original position.</span></span>  
    
### <a name="view-paint-profiler"></a><span data-ttu-id="77422-409">Afficher le profileur de pinceau</span><span class="sxs-lookup"><span data-stu-id="77422-409">View paint profiler</span></span>  

<span data-ttu-id="77422-410">Pour afficher des informations avancées sur un événement de pinceau :</span><span class="sxs-lookup"><span data-stu-id="77422-410">To view advanced information about a paint event:</span></span>  

1.  <span data-ttu-id="77422-411">[Activer](#turn-on-advanced-paint-instrumentation).</span><span class="sxs-lookup"><span data-stu-id="77422-411">[Turn on](#turn-on-advanced-paint-instrumentation).</span></span>  
1.  <span data-ttu-id="77422-412">Choisissez un **Paint** dans la section **Main.**</span><span class="sxs-lookup"><span data-stu-id="77422-412">Choose a **Paint** event in the **Main** section.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-paint-profiler.msft.png" alt-text="Panneau Paint profileur" lightbox="../media/evaluate-performance-paint-profiler.msft.png":::
       <span data-ttu-id="77422-414">Panneau **Paint profileur**</span><span class="sxs-lookup"><span data-stu-id="77422-414">The **Paint Profiler** panel</span></span>  
    :::image-end:::  
    
## <a name="analyze-rendering-performance-with-the-rendering-tool"></a><span data-ttu-id="77422-415">Analyser les performances de rendu à l’aide de l’outil de rendu</span><span class="sxs-lookup"><span data-stu-id="77422-415">Analyze rendering performance with the Rendering tool</span></span>  

<span data-ttu-id="77422-416">Utilisez les fonctionnalités du panneau **de** rendu pour visualiser les performances de rendu de votre page.</span><span class="sxs-lookup"><span data-stu-id="77422-416">Use the features of the **Rendering** panel to help visualize the rendering performance of your page.</span></span>  

<span data-ttu-id="77422-417">Pour ouvrir **l’outil de** rendu :</span><span class="sxs-lookup"><span data-stu-id="77422-417">To open the **Rendering** tool:</span></span>  

1.  <span data-ttu-id="77422-418">[Ouvrez le menu Commande.][DevToolsCommandMenu]</span><span class="sxs-lookup"><span data-stu-id="77422-418">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="77422-419">Commencez à taper `Rendering` et sélectionnez `Show Rendering` .</span><span class="sxs-lookup"><span data-stu-id="77422-419">Start typing `Rendering` and select `Show Rendering`.</span></span>  <span data-ttu-id="77422-420">DevTools affiche l’outil **de** rendu en bas de votre fenêtre DevTools.</span><span class="sxs-lookup"><span data-stu-id="77422-420">DevTools displays the **Rendering** tool at the bottom of your DevTools window.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-console-drawer-rendering.msft.png" alt-text="Outil de rendu" lightbox="../media/evaluate-performance-console-drawer-rendering.msft.png":::
       <span data-ttu-id="77422-422">Outil **de rendu**</span><span class="sxs-lookup"><span data-stu-id="77422-422">The **Rendering** tool</span></span>  
    :::image-end:::  
    
### <a name="view-frames-per-second-in-realtime-with-the-fps-meter"></a><span data-ttu-id="77422-423">Afficher les images par seconde en temps réel avec la jauge FPS</span><span class="sxs-lookup"><span data-stu-id="77422-423">View frames per second in realtime with the FPS meter</span></span>  

<span data-ttu-id="77422-424">La **jauge FPS** est une superposition qui apparaît dans le coin supérieur droit de votre vue.</span><span class="sxs-lookup"><span data-stu-id="77422-424">The **FPS meter** is an overlay that appears in the top-right corner of your viewport.</span></span>  <span data-ttu-id="77422-425">Il fournit une estimation en temps réel du service FPS à mesure que la page s’exécute.</span><span class="sxs-lookup"><span data-stu-id="77422-425">It provides a realtime estimate of FPS as the page runs.</span></span>  <span data-ttu-id="77422-426">Pour ouvrir la **jauge FPS**:</span><span class="sxs-lookup"><span data-stu-id="77422-426">To open the **FPS meter**:</span></span>  

1.  <span data-ttu-id="77422-427">Ouvrez **l’outil de** rendu.</span><span class="sxs-lookup"><span data-stu-id="77422-427">Open the **Rendering** tool.</span></span>  <span data-ttu-id="77422-428">[Analysez les performances de rendu à l’aide de l’outil de rendu.](#analyze-rendering-performance-with-the-rendering-tool)</span><span class="sxs-lookup"><span data-stu-id="77422-428">[Analyze rendering performance with the Rendering tool](#analyze-rendering-performance-with-the-rendering-tool).</span></span>  
1.  <span data-ttu-id="77422-429">Activer la case **à cocher Indicateur FPS.**</span><span class="sxs-lookup"><span data-stu-id="77422-429">Turn on the **FPS Meter** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png" alt-text="Indicateur FPS" lightbox="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png":::
       <span data-ttu-id="77422-431">Indicateur **FPS**</span><span class="sxs-lookup"><span data-stu-id="77422-431">The **FPS meter**</span></span>  
    :::image-end:::  
    
### <a name="view-painting-events-in-realtime-with-paint-flashing"></a><span data-ttu-id="77422-432">Afficher les événements de dessin en temps réel avec Paint clignotement</span><span class="sxs-lookup"><span data-stu-id="77422-432">View painting events in realtime with Paint Flashing</span></span>  

<span data-ttu-id="77422-433">Utilisez Paint clignotement pour obtenir une vue en temps réel de tous les événements de pinceau sur la page.</span><span class="sxs-lookup"><span data-stu-id="77422-433">Use Paint Flashing to get a realtime view of all paint events on the page.</span></span>  <span data-ttu-id="77422-434">Chaque fois qu’une partie de la page est peint à nouveau, DevTools souligne cette section en vert.</span><span class="sxs-lookup"><span data-stu-id="77422-434">Whenever a part of the page gets re-painted, DevTools outlines that section in green.</span></span>  

<span data-ttu-id="77422-435">Pour activer Paint clignotement, effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="77422-435">To turn on Paint Flashing, complete the following actions.</span></span>  

1.  <span data-ttu-id="77422-436">Ouvrez **l’outil de** rendu.</span><span class="sxs-lookup"><span data-stu-id="77422-436">Open the **Rendering** tool.</span></span>  <span data-ttu-id="77422-437">Accédez à [Analyser les performances de rendu à l’aide de l’outil de rendu.](#analyze-rendering-performance-with-the-rendering-tool)</span><span class="sxs-lookup"><span data-stu-id="77422-437">Navigate to [Analyze rendering performance with the Rendering tool](#analyze-rendering-performance-with-the-rendering-tool).</span></span>  
1.  <span data-ttu-id="77422-438">Activer la case **à Paint clignotement.**</span><span class="sxs-lookup"><span data-stu-id="77422-438">Turn on the **Paint Flashing** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png" alt-text="Paint Clignotement" lightbox="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png":::
       **<span data-ttu-id="77422-440">Paint Clignotement</span><span class="sxs-lookup"><span data-stu-id="77422-440">Paint Flashing</span></span>**  
    :::image-end:::  
    
### <a name="view-an-overlay-of-layers-with-layer-borders"></a><span data-ttu-id="77422-441">Afficher une superposition de couches avec des bordures de calque</span><span class="sxs-lookup"><span data-stu-id="77422-441">View an overlay of layers with Layer Borders</span></span>  

<span data-ttu-id="77422-442">Utilisez **les bordures de** calque pour afficher une superposition de bordures de calque et de vignettes au-dessus de la page.</span><span class="sxs-lookup"><span data-stu-id="77422-442">Use **Layer Borders** to view an overlay of layer borders and tiles on top of the page.</span></span>  

<span data-ttu-id="77422-443">Pour activer les bordures de calque, effectuer les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="77422-443">To turn on Layer Borders, complete the following actions,</span></span>  

1.  <span data-ttu-id="77422-444">Ouvrez **l’outil de** rendu.</span><span class="sxs-lookup"><span data-stu-id="77422-444">Open the **Rendering** tool.</span></span>  <span data-ttu-id="77422-445">Accédez à [Analyser les performances de rendu à l’aide de l’outil de rendu.](#analyze-rendering-performance-with-the-rendering-tool)</span><span class="sxs-lookup"><span data-stu-id="77422-445">Navigate to [Analyze rendering performance with the Rendering tool](#analyze-rendering-performance-with-the-rendering-tool).</span></span>  
1.  <span data-ttu-id="77422-446">Activer la case **à cocher Bordures** de calque.</span><span class="sxs-lookup"><span data-stu-id="77422-446">Turn on the **Layer Borders** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png" alt-text="Bordures de calque" lightbox="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png":::
       **<span data-ttu-id="77422-448">Bordures de calque</span><span class="sxs-lookup"><span data-stu-id="77422-448">Layer Borders</span></span>**  
    :::image-end:::  
    
<span data-ttu-id="77422-449">Accédez aux commentaires dans [debug_colors.cc][ChromiumDebugColors] pour obtenir une explication des codages de couleurs.</span><span class="sxs-lookup"><span data-stu-id="77422-449">Navigate to the comments in [debug_colors.cc][ChromiumDebugColors] for an explanation of the color-codings.</span></span>  

### <a name="find-scroll-performance-issues-in-realtime"></a><span data-ttu-id="77422-450">Rechercher les problèmes de performances de défilement en temps réel</span><span class="sxs-lookup"><span data-stu-id="77422-450">Find scroll performance issues in realtime</span></span>  

<span data-ttu-id="77422-451">Utilisez les problèmes de performances de défilement pour identifier les éléments de la page qui ont des écouteurs d’événements liés au défilement qui peuvent nuire aux performances de la page.</span><span class="sxs-lookup"><span data-stu-id="77422-451">Use Scrolling Performance Issues to identify elements of the page that have event listeners related to scrolling that may harm the performance of the page.</span></span>  
<span data-ttu-id="77422-452">DevTools décrit les éléments potentiellement problématiques dans le teal.</span><span class="sxs-lookup"><span data-stu-id="77422-452">DevTools outlines the potentially-problematic elements in teal.</span></span>  

<span data-ttu-id="77422-453">Pour afficher les problèmes de performances de défilement, effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="77422-453">To view scroll performance issues, complete the following actions.</span></span> 

1.  <span data-ttu-id="77422-454">Ouvrez **l’outil de** rendu.</span><span class="sxs-lookup"><span data-stu-id="77422-454">Open the **Rendering** tool.</span></span>  <span data-ttu-id="77422-455">Accédez à [Analyser les performances de rendu à l’aide de l’outil de rendu.](#analyze-rendering-performance-with-the-rendering-tool)</span><span class="sxs-lookup"><span data-stu-id="77422-455">Navigate to [Analyze rendering performance with the Rendering tool](#analyze-rendering-performance-with-the-rendering-tool).</span></span>  
1.  <span data-ttu-id="77422-456">Activer la case **à cocher Problèmes de performances de** défilement.</span><span class="sxs-lookup"><span data-stu-id="77422-456">Turn on the **Scrolling Performance Issues** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png" alt-text="Des problèmes de performances de défilement indiquent que les objets non soumis à la contrainte de la vue de couche peuvent nuire aux performances de défilement" lightbox="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png":::
       <span data-ttu-id="77422-458">**Des problèmes de performances de** défilement indiquent que les objets non soumis à la contrainte de la vue de couche peuvent nuire aux performances de défilement</span><span class="sxs-lookup"><span data-stu-id="77422-458">**Scrolling Performance Issues** indicates that non-layer viewport-constrained objects may harm scroll performance</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="77422-459">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="77422-459">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "outils de développement Microsoft Edge (Chromium) | Documents Microsoft"  
[DevToolsCommandMenu]: ../command-menu/index.md#open-the-command-menu "Ouvrez le menu Commande - Exécutez les commandes avec la Microsoft Edge menu de commande DevTools | Documents Microsoft"  
[DevtoolsEvaluatePerformanceGettingStarted]: ./index.md "Commencer à analyser les performances d’exécution | Documents Microsoft"  

[ActivityTabsDemo]: https://microsoft-edge-chromium-devtools.glitch.me/perf/activitytabs.html "Démonstration des onglets Activité | glitch"  

[ChromiumDebugColors]: https://cs.chromium.org/chromium/src/cc/debug/debug_colors.cc "debug_colors.cc - Recherche de code"  

> [!NOTE]
> <span data-ttu-id="77422-465">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="77422-465">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="77422-466">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="77422-466">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="77422-468">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="77422-468">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
