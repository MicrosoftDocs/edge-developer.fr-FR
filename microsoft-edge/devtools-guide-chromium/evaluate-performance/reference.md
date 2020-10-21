---
description: Référence sur l’ensemble des méthodes permettant d’enregistrer et d’analyser des performances dans Microsoft Edge DevTools.
title: Référence d’analyse des performances
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: d135f83273842a1e128df0bb346f0f126e2fbe8d
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125138"
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

# <span data-ttu-id="f3d3d-104">Référence d’analyse des performances</span><span class="sxs-lookup"><span data-stu-id="f3d3d-104">Performance analysis reference</span></span>  

<span data-ttu-id="f3d3d-105">Cette page est une référence complète des fonctionnalités de Microsoft Edge DevTools liées à l’analyse des performances.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-105">This page is a comprehensive reference of Microsoft Edge DevTools features related to analyzing performance.</span></span>  

<span data-ttu-id="f3d3d-106">Naviguez jusqu’à l' [analyse des performances][DevtoolsEvaluatePerformanceGettingStarted] de l’exécution d’un didacticiel dirigé sur l’analyse des performances d’une page à l’aide de [Microsoft Edge devtools][MicrosoftEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="f3d3d-106">Navigate to [Get Started With Analyzing Runtime Performance][DevtoolsEvaluatePerformanceGettingStarted] for a guided tutorial on how to analyze the performance of a page using [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <span data-ttu-id="f3d3d-107">Performance enregistrement</span><span class="sxs-lookup"><span data-stu-id="f3d3d-107">Record performance</span></span>  

### <span data-ttu-id="f3d3d-108">Enregistrer les performances d’exécution</span><span class="sxs-lookup"><span data-stu-id="f3d3d-108">Record runtime performance</span></span>  

<span data-ttu-id="f3d3d-109">Enregistrez les performances d’exécution lorsque vous souhaitez analyser les performances d’une page en cours d’exécution, plutôt que de procéder au chargement.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-109">Record runtime performance when you want to analyze the performance of a page as it is running, as opposed to loading.</span></span>  

1.  <span data-ttu-id="f3d3d-110">Accédez à la page que vous voulez analyser.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-110">Go to the page that you want to analyze.</span></span>  
1.  <span data-ttu-id="f3d3d-111">Cliquez sur l’onglet **performance** dans devtools.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-111">Click the **Performance** tab in DevTools.</span></span>  
1.  <span data-ttu-id="f3d3d-112">Cliquez sur **Enregistrer** \ ( ![ icône d’enregistrement ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="f3d3d-112">Choose **Record** \(![Record icon][ImageRecordIcon]\).</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-record-highlight.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-record-highlight.msft.png":::
       **<span data-ttu-id="f3d3d-114">Record</span><span class="sxs-lookup"><span data-stu-id="f3d3d-114">Record</span></span>**  
    :::image-end:::  
    
1.  <span data-ttu-id="f3d3d-115">Interagir avec la page.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-115">Interact with the page.</span></span>  <span data-ttu-id="f3d3d-116">DevTools enregistre toutes les activités de page résultant de vos interactions.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-116">DevTools records all page activity that occurs as a result of your interactions.</span></span>  
1.  <span data-ttu-id="f3d3d-117">Cliquez de nouveau sur **enregistrement** ou sélectionnez **arrêter** pour arrêter l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-117">Choose **Record** again or choose **Stop** to stop recording.</span></span>  
    
### <span data-ttu-id="f3d3d-118">Enregistrer les performances de chargement</span><span class="sxs-lookup"><span data-stu-id="f3d3d-118">Record load performance</span></span>  

<span data-ttu-id="f3d3d-119">Enregistrez les performances de chargement lorsque vous souhaitez analyser les performances d’une page lors du chargement, plutôt que d’être en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-119">Record load performance when you want to analyze the performance of a page as it is loading, as opposed to running.</span></span>  

1.  <span data-ttu-id="f3d3d-120">Accédez à la page que vous voulez analyser.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-120">Go to the page that you want to analyze.</span></span>  
1.  <span data-ttu-id="f3d3d-121">Ouvrez le panneau **performances** de devtools.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-121">Open the **Performance** panel of DevTools.</span></span>  
1.  <span data-ttu-id="f3d3d-122">Sélectionnez **Actualiser la page** \ ( ![ Actualiser la page ][ImageRefreshPageIcon] \).</span><span class="sxs-lookup"><span data-stu-id="f3d3d-122">Choose **Refresh page** \(![Refresh Page][ImageRefreshPageIcon]\).</span></span>  <span data-ttu-id="f3d3d-123">DevTools enregistre les métriques de performances pendant que la page est actualisée, puis arrête automatiquement l’enregistrement de quelques secondes après la fin de la charge.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-123">DevTools records performance metrics while the page refreshes and then automatically stops the recording a couple seconds after the load finishes.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-refresh-button.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-refresh-button.msft.png":::
       **<span data-ttu-id="f3d3d-125">Actualiser la page</span><span class="sxs-lookup"><span data-stu-id="f3d3d-125">Refresh page</span></span>**  
    :::image-end:::  
    
<span data-ttu-id="f3d3d-126">DevTools effectue automatiquement un zoom avant sur la partie de l’enregistrement où la majeure partie de l’activité s’est produite.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-126">DevTools automatically zooms in on the portion of the recording where most of the activity occurred.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-refreshed.msft.png":::
   <span data-ttu-id="f3d3d-128">Un enregistrement de chargement de page</span><span class="sxs-lookup"><span data-stu-id="f3d3d-128">A page-load recording</span></span>  
:::image-end:::  

### <span data-ttu-id="f3d3d-129">Capture des captures d’écran lors de l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="f3d3d-129">Capture screenshots while recording</span></span>  

<span data-ttu-id="f3d3d-130">Activez la case à cocher **captures d’écran** pour capturer une capture d’écran de chaque image lors de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-130">Enable the **Screenshots** checkbox to capture a screenshot of every frame while recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png":::
   <span data-ttu-id="f3d3d-132">Case à cocher **captures d’écran**</span><span class="sxs-lookup"><span data-stu-id="f3d3d-132">The **Screenshots** checkbox</span></span>  
:::image-end:::  

<span data-ttu-id="f3d3d-133">Accédez à l' [affichage d’une capture d’écran](#view-a-screenshot) pour savoir comment interagir avec les captures d’écran.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-133">Navigate to [View a screenshot](#view-a-screenshot) to learn how to interact with screenshots.</span></span>  

### <span data-ttu-id="f3d3d-134">Forcer le nettoyage de la mémoire lors de l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="f3d3d-134">Force garbage collection while recording</span></span>  

<span data-ttu-id="f3d3d-135">Lors de l’enregistrement d’une page, sélectionnez **collecter le nettoyage** de la mémoire (en-dessous ![ ][ImageCollectGarbageIcon] ) pour forcer le nettoyage de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-135">While you are recording a page, choose **Collect garbage** \(![Collect garbage icon][ImageCollectGarbageIcon]\) to force garbage collection.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-collect-garbage-button.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-collect-garbage-button.msft.png":::
   <span data-ttu-id="f3d3d-137">Collecter les nettoyages de la mémoire</span><span class="sxs-lookup"><span data-stu-id="f3d3d-137">Collect garbage</span></span>  
:::image-end:::  

### <span data-ttu-id="f3d3d-138">Afficher les paramètres d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="f3d3d-138">Show recording settings</span></span>  

<span data-ttu-id="f3d3d-139">Choisissez **paramètres de capture** \ ( ![ paramètres de capture ][ImageCaptureSettingsIcon] \) pour exposer d’autres paramètres liés à la manière dont devtools capture les enregistrements de performances.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-139">Choose **Capture settings** \(![Capture settings][ImageCaptureSettingsIcon]\) to expose more settings related to how DevTools captures performance recordings.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png":::
   <span data-ttu-id="f3d3d-141">Section **paramètres de capture**</span><span class="sxs-lookup"><span data-stu-id="f3d3d-141">The **Capture Settings** section</span></span>  
:::image-end:::  

### <span data-ttu-id="f3d3d-142">Désactiver les exemples JavaScript</span><span class="sxs-lookup"><span data-stu-id="f3d3d-142">Disable JavaScript samples</span></span>  

<span data-ttu-id="f3d3d-143">Par défaut, la section **principale** d’un enregistrement affiche des piles d’appels détaillées des fonctions JavaScript qui ont été appelées lors de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-143">By default, the **Main** section of a recording displays detailed call stacks of JavaScript functions that were called during the recording.</span></span>  <span data-ttu-id="f3d3d-144">Pour désactiver ces piles d’appels:</span><span class="sxs-lookup"><span data-stu-id="f3d3d-144">To disable these call stacks:</span></span>  

1.  <span data-ttu-id="f3d3d-145">Ouvrir le menu **paramètres de capture** .</span><span class="sxs-lookup"><span data-stu-id="f3d3d-145">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="f3d3d-146">Accédez à [afficher les paramètres d’enregistrement](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="f3d3d-146">Navigate to [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="f3d3d-147">Activez la case à cocher **Désactiver les exemples JavaScript** .</span><span class="sxs-lookup"><span data-stu-id="f3d3d-147">Enable the **Disable JavaScript Samples** checkbox.</span></span>  
1.  <span data-ttu-id="f3d3d-148">Prenez un enregistrement de la page.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-148">Take a recording of the page.</span></span>  
    
<span data-ttu-id="f3d3d-149">Les 2 figures suivantes présentent la différence entre la désactivation et l’activation des exemples JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-149">The following 2 figures display the difference between disabling and enabling JavaScript samples.</span></span>  <span data-ttu-id="f3d3d-150">La section **principale** de l’enregistrement est beaucoup plus courte lorsque l’échantillonnage est désactivé, car il omet toutes les piles d’appels JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-150">The **Main** section of the recording is much shorter when sampling is disabled, because it omits all of the JavaScript call stacks.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png":::
         <span data-ttu-id="f3d3d-152">Un exemple d’enregistrement lorsque les exemples de JS sont désactivés</span><span class="sxs-lookup"><span data-stu-id="f3d3d-152">An example of a recording when JS samples are disabled</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png":::
         <span data-ttu-id="f3d3d-154">Exemple d’enregistrement lorsque les exemples de JS sont activés</span><span class="sxs-lookup"><span data-stu-id="f3d3d-154">An example of a recording when JS samples are enabled</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

### <span data-ttu-id="f3d3d-155">Limiter le réseau lors de l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="f3d3d-155">Throttle the network while recording</span></span>  

<span data-ttu-id="f3d3d-156">Pour limiter le réseau lors de l’enregistrement:</span><span class="sxs-lookup"><span data-stu-id="f3d3d-156">To throttle the network while recording:</span></span>  

1.  <span data-ttu-id="f3d3d-157">Ouvrir le menu **paramètres de capture** .</span><span class="sxs-lookup"><span data-stu-id="f3d3d-157">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="f3d3d-158">Accédez à [afficher les paramètres d’enregistrement](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="f3d3d-158">Navigate to [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="f3d3d-159">Définissez **réseau** sur le niveau de limitation souhaité.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-159">Set **Network** to the desired level of throttling.</span></span>  
    
### <span data-ttu-id="f3d3d-160">Limiter le processeur lors de l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="f3d3d-160">Throttle the CPU while recording</span></span>  

<span data-ttu-id="f3d3d-161">Pour limiter le processeur lors de l’enregistrement:</span><span class="sxs-lookup"><span data-stu-id="f3d3d-161">To throttle the CPU while recording:</span></span>  

1.  <span data-ttu-id="f3d3d-162">Ouvrir le menu **paramètres de capture** .</span><span class="sxs-lookup"><span data-stu-id="f3d3d-162">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="f3d3d-163">Accédez à [afficher les paramètres d’enregistrement](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="f3d3d-163">Navigate to [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="f3d3d-164">Définissez **UC** sur le niveau de limitation souhaité.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-164">Set **CPU** to the desired level of throttling.</span></span>  
    
<span data-ttu-id="f3d3d-165">La limitation est relative aux fonctionnalités de votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-165">Throttling is relative to the capabilities of your computer.</span></span>  <span data-ttu-id="f3d3d-166">Par exemple, l’option **2x Slowdown** permet à votre processeur de fonctionner 2 fois plus lent que d’habitude.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-166">For example, the **2x slowdown** option makes your CPU operate 2 times slower than normal.</span></span>  <span data-ttu-id="f3d3d-167">DevTools ne simulez pas vraiment les UC des appareils mobiles, car l’architecture des appareils mobiles est très différente de celle des ordinateurs de bureau et des ordinateurs portables.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-167">DevTools do not truly simulate the CPUs of mobile devices, because the architecture of mobile devices is very different from that of desktops and laptops.</span></span>  

### <span data-ttu-id="f3d3d-168">Activer l’instrumentation avancée de peinture</span><span class="sxs-lookup"><span data-stu-id="f3d3d-168">Enable advanced paint instrumentation</span></span>  

<span data-ttu-id="f3d3d-169">Pour afficher une instrumentation détaillée de Paint:</span><span class="sxs-lookup"><span data-stu-id="f3d3d-169">To view detailed paint instrumentation:</span></span>  

1.  <span data-ttu-id="f3d3d-170">Ouvrir le menu **paramètres de capture** .</span><span class="sxs-lookup"><span data-stu-id="f3d3d-170">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="f3d3d-171">Accédez à [afficher les paramètres d’enregistrement](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="f3d3d-171">Navigate to [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="f3d3d-172">Cochez la case **activer l’instrumentation avancée de peinture (lente)** .</span><span class="sxs-lookup"><span data-stu-id="f3d3d-172">Check the **Enable advanced paint instrumentation (slow)** checkbox.</span></span>  

<span data-ttu-id="f3d3d-173">Pour plus d’informations sur l’interaction entre les informations de Paint, voir [afficher les couches](#view-layers-information) et afficher le [Générateur de profils Paint](#view-paint-profiler).</span><span class="sxs-lookup"><span data-stu-id="f3d3d-173">To learn how to interact with the paint information, navigate to [View layers](#view-layers-information) and [View paint profiler](#view-paint-profiler).</span></span>  

## <span data-ttu-id="f3d3d-174">Enregistrer un enregistrement</span><span class="sxs-lookup"><span data-stu-id="f3d3d-174">Save a recording</span></span>  

<span data-ttu-id="f3d3d-175">Pour enregistrer un enregistrement, cliquez avec le bouton droit, puis choisissez **enregistrer le profil**.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-175">To save a recording, right-click and choose **Save Profile**.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png":::
   **<span data-ttu-id="f3d3d-177">Enregistrer le profil</span><span class="sxs-lookup"><span data-stu-id="f3d3d-177">Save Profile</span></span>**  
:::image-end:::  

## <span data-ttu-id="f3d3d-178">Charger un enregistrement</span><span class="sxs-lookup"><span data-stu-id="f3d3d-178">Load a recording</span></span>  

<span data-ttu-id="f3d3d-179">Pour charger un enregistrement, cliquez avec le bouton droit, puis choisissez **charger le profil**.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-179">To load a recording, right-click and choose **Load Profile**.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png":::
   **<span data-ttu-id="f3d3d-181">Profil de chargement</span><span class="sxs-lookup"><span data-stu-id="f3d3d-181">Load Profile</span></span>**  
:::image-end:::  

## <span data-ttu-id="f3d3d-182">Effacer l’enregistrement précédent</span><span class="sxs-lookup"><span data-stu-id="f3d3d-182">Clear the previous recording</span></span>  

<span data-ttu-id="f3d3d-183">Après avoir effectué un enregistrement, appuyez sur **effacer l’enregistrement** \ ( ![ icône Effacer l’enregistrement ][ImageClearRecordingIcon] \) pour effacer cet enregistrement du panneau **performances** .</span><span class="sxs-lookup"><span data-stu-id="f3d3d-183">After making a recording, press **Clear recording** \(![Clear recording icon][ImageClearRecordingIcon]\) to clear that recording from the **Performance** panel.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png":::
   **<span data-ttu-id="f3d3d-185">Effacer l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="f3d3d-185">Clear recording</span></span>**  
:::image-end:::  

## <span data-ttu-id="f3d3d-186">Analyser un enregistrement de performance</span><span class="sxs-lookup"><span data-stu-id="f3d3d-186">Analyze a performance recording</span></span>  

<span data-ttu-id="f3d3d-187">Une fois que vous avez [enregistré des performances d’exécution](#record-runtime-performance) ou enregistré des performances de [chargement](#record-load-performance), le panneau **performance** fournit un grand nombre de données pour l’analyse des performances de ce qui s’est produit.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-187">After you [record runtime performance](#record-runtime-performance) or [record load performance](#record-load-performance), the **Performance** panel provides a lot of data for analyzing the performance of what just happened.</span></span>  

### <span data-ttu-id="f3d3d-188">Sélectionner une partie d’un enregistrement</span><span class="sxs-lookup"><span data-stu-id="f3d3d-188">Select a portion of a recording</span></span>  

<span data-ttu-id="f3d3d-189">Faites glisser le pointeur de la souris vers la gauche ou la droite dans la **vue d’ensemble** pour sélectionner une partie d’un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-189">Drag your mouse left or right across the **Overview** to select a portion of a recording.</span></span>  <span data-ttu-id="f3d3d-190">La section **vue d’ensemble** contient les graphiques **fps**, **UC**et **net** .</span><span class="sxs-lookup"><span data-stu-id="f3d3d-190">The **Overview** is the section that contains the **FPS**, **CPU**, and **NET** charts.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-zoom-highlighted.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-zoom-highlighted.msft.png":::
   <span data-ttu-id="f3d3d-192">Faites glisser le pointeur de la souris sur la **vue d’ensemble** pour effectuer un zoom</span><span class="sxs-lookup"><span data-stu-id="f3d3d-192">Drag the mouse across the **Overview** to zoom</span></span>  
:::image-end:::  

<span data-ttu-id="f3d3d-193">Pour sélectionner une partie à l’aide du clavier:</span><span class="sxs-lookup"><span data-stu-id="f3d3d-193">To select a portion using the keyboard:</span></span>  

1.  <span data-ttu-id="f3d3d-194">Cliquez sur l’arrière-plan de la section **principale** ou de n’importe quelle section en regard de celle-ci, comme **interactions**, **réseau**ou **GPU**.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-194">Click on the background of the **Main** section, or any of the sections next to it, such as **Interactions**, **Network**, or **GPU**.</span></span>  <span data-ttu-id="f3d3d-195">Ce flux de travail de clavier fonctionne uniquement lorsque l’une de ces sections est activée.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-195">This keyboard workflow only works when one of these sections is in focus.</span></span>  
1.  <span data-ttu-id="f3d3d-196">Utilisez les `W` touches,,, `A` `S` `D` pour effectuer un zoom avant, vous déplacer vers la gauche, effectuer un zoom arrière et vous déplacer à droite, respectivement.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-196">Use the `W`, `A`, `S`, `D` keys to zoom in, move left, zoom out, and move right, respectively.</span></span>  

<span data-ttu-id="f3d3d-197">Pour sélectionner une partie à l’aide d’une pavé tactile:</span><span class="sxs-lookup"><span data-stu-id="f3d3d-197">To select a portion using a trackpad:</span></span>  

1.  <span data-ttu-id="f3d3d-198">Positionnez le pointeur de la souris sur la section **Présentation** ou la section **Détails** .</span><span class="sxs-lookup"><span data-stu-id="f3d3d-198">Hover your mouse over the **Overview** section or the **Details** section.</span></span>  <span data-ttu-id="f3d3d-199">La section **vue d’ensemble** est la zone contenant les graphiques **fps**, **UC**et **net** .</span><span class="sxs-lookup"><span data-stu-id="f3d3d-199">The **Overview** section is the area containing the **FPS**, **CPU**, and **NET** charts.</span></span>  <span data-ttu-id="f3d3d-200">La section **Détails** représente la zone contenant la section **principale** , la section **interactions** , etc.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-200">The **Details** section is the area containing the **Main** section, the **Interactions** section, and so on.</span></span>  
1.  <span data-ttu-id="f3d3d-201">Avec deux doigts, balayez vers le haut pour effectuer un zoom arrière, balayez vers la gauche pour vous déplacer vers la gauche, balayez vers le bas pour effectuer un zoom avant, puis balayez vers la droite pour avancer.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-201">Using two fingers, swipe up to zoom out, swipe left to move left, swipe down to zoom in, and swipe right to move right.</span></span>  

<span data-ttu-id="f3d3d-202">Pour faire défiler un grand graphique en flamme dans la section **principale** ou sur l’un des voisins, cliquez et maintenez le bouton enfoncé tout en faisant glisser le curseur vers le haut et le bas.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-202">To scroll a long flame chart in the **Main** section or any of the neighbors, click and hold while dragging up and down.</span></span>  <span data-ttu-id="f3d3d-203">Faites glisser vers la gauche et vers la droite pour déplacer la partie de l’enregistrement sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-203">Drag left and right to move what portion of the recording is selected.</span></span>  

### <span data-ttu-id="f3d3d-204">Activités de recherche</span><span class="sxs-lookup"><span data-stu-id="f3d3d-204">Search activities</span></span>  

<span data-ttu-id="f3d3d-205">`Control` + `F` `Command` + `F` Pour ouvrir la zone de recherche située en bas du panneau de **performance** , sélectionnez \ (Windows, Linux \) ou \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="f3d3d-205">Select `Control`+`F` \(Windows, Linux\) or `Command`+`F` \(macOS\) to open the search box at the bottom of the **Performance** panel.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-search-regex.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-search-regex.msft.png":::
   <span data-ttu-id="f3d3d-207">Zone de recherche</span><span class="sxs-lookup"><span data-stu-id="f3d3d-207">The search box</span></span>  
:::image-end:::  

<span data-ttu-id="f3d3d-208">Pour parcourir les activités qui correspondent à votre requête:</span><span class="sxs-lookup"><span data-stu-id="f3d3d-208">To navigate activities that match your query:</span></span>  

*   <span data-ttu-id="f3d3d-209">Utilisez les boutons **précédent** \ ( ![ précédent ][ImagePreviousIcon] \) et **suivant** \ ( ![ suivant ][ImageNextIcon] \).</span><span class="sxs-lookup"><span data-stu-id="f3d3d-209">Use the **Previous** \(![Previous][ImagePreviousIcon]\) and **Next** \(![Next][ImageNextIcon]\) buttons.</span></span>  
*   <span data-ttu-id="f3d3d-210">Sélectionner `Shift` + `Enter` pour sélectionner le précédent ou `Enter` pour en sélectionner un autre.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-210">Select `Shift`+`Enter` to select the previous or `Enter` to select the next.</span></span>  

<span data-ttu-id="f3d3d-211">Pour modifier les paramètres d’une requête:</span><span class="sxs-lookup"><span data-stu-id="f3d3d-211">To modify query settings:</span></span>  

*   <span data-ttu-id="f3d3d-212">Appuyer sur respecter la **casse** (respecter la casse ![ ][ImageSearchCaseIcon] ) pour respecter la casse.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-212">Press **Case sensitive** \(![Case sensitive][ImageSearchCaseIcon]\) to make the query case sensitive.</span></span>  
*   <span data-ttu-id="f3d3d-213">**Regex** ![ ][ImageSearchRegexIcon] Pour utiliser une expression régulière dans votre requête, appuyez sur Regex.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-213">Press **Regex** \(![Regex][ImageSearchRegexIcon]\) to use a regular expression in your query.</span></span>  

<span data-ttu-id="f3d3d-214">Pour masquer la zone de recherche, appuyez sur **Annuler**.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-214">To hide the search box, press **Cancel**.</span></span>  

### <span data-ttu-id="f3d3d-215">Afficher l’activité du thread principal</span><span class="sxs-lookup"><span data-stu-id="f3d3d-215">View main thread activity</span></span>  

<span data-ttu-id="f3d3d-216">Utilisez la section **principale** pour afficher l’activité qui s’est produite sur le thread principal de la page.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-216">Use the **Main** section to view activity that occurred on the main thread of the page.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-main-zoomed.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-main-zoomed.msft.png":::
   <span data-ttu-id="f3d3d-218">Section **principale**</span><span class="sxs-lookup"><span data-stu-id="f3d3d-218">The **Main** section</span></span>  
:::image-end:::  

<span data-ttu-id="f3d3d-219">Cliquez sur un événement pour afficher des informations supplémentaires le concernant sous l’onglet **Résumé** .  DevTools souligne l’événement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-219">Click on an event to view more information about it in the **Summary** tab.  DevTools outlines the selected event.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-summary-me.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-summary-me.msft.png":::
   <span data-ttu-id="f3d3d-221">Plus d’informations sur la `anonymous` fonction sous l’onglet **Résumé**</span><span class="sxs-lookup"><span data-stu-id="f3d3d-221">More information about the `anonymous` function in the **Summary** tab</span></span>  
:::image-end:::  

<span data-ttu-id="f3d3d-222">DevTools représente l’activité du thread principal avec un graphique à flamme.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-222">DevTools represents main thread activity with a flame chart.</span></span>  <span data-ttu-id="f3d3d-223">L’axe x représente l’enregistrement dans le temps.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-223">The x-axis represents the recording over time.</span></span>  <span data-ttu-id="f3d3d-224">L’axe y représente la pile d’appels.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-224">The y-axis represents the call stack.</span></span>  <span data-ttu-id="f3d3d-225">Les événements en haut déclenchent les événements situés au-dessous.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-225">The events on top cause the events below it.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-main-flame-chart.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-main-flame-chart.msft.png":::
   <span data-ttu-id="f3d3d-227">Un graphique en flamme</span><span class="sxs-lookup"><span data-stu-id="f3d3d-227">A flame chart</span></span>  
:::image-end:::  

<span data-ttu-id="f3d3d-228">Dans l’illustration précédente, un `click` événement a entraîné `Function Call` une `activitytabs.js` 53 sur ligne.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-228">In the previous figure, a `click` event caused a `Function Call` in `activitytabs.js` on line 53.</span></span>  <span data-ttu-id="f3d3d-229">`Function Call`Vous pouvez voir ci-dessous qu’une fonction anonyme a été appelée.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-229">Below `Function Call` you see that an anonymous function was called.</span></span>  <span data-ttu-id="f3d3d-230">Fonction anonyme appelée, qui a été appelée `a` `wait` `Minor GC` .</span><span class="sxs-lookup"><span data-stu-id="f3d3d-230">The anonymous function called `a`, which called `wait`, which called `Minor GC`.</span></span>  

<span data-ttu-id="f3d3d-231">DevTools attribue des couleurs aléatoires aux scripts.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-231">DevTools assigns scripts random colors.</span></span>  <span data-ttu-id="f3d3d-232">Dans la figure ci-dessus, les appels de fonction à partir d’un script apparaissent en vert clair.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-232">In the previous figure, function calls from one script are colored light green.</span></span>  <span data-ttu-id="f3d3d-233">Les appels d’un autre script sont de couleur beige.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-233">Calls from another script are colored beige.</span></span>  <span data-ttu-id="f3d3d-234">Le jaune foncé représente l’activité de création de scripts et l’événement violet représente l’activité de rendu.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-234">The darker yellow represents scripting activity, and the purple event represents rendering activity.</span></span>  <span data-ttu-id="f3d3d-235">Ces événements en jaune et violet plus foncés sont cohérents dans tous les enregistrements.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-235">These darker yellow and purple events are consistent across all recordings.</span></span>  

<span data-ttu-id="f3d3d-236">Naviguez jusqu’à [Désactiver les exemples JavaScript](#disable-javascript-samples) si vous voulez masquer le graphique à flamme détaillée des appels JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-236">Navigate to [Disable JavaScript samples](#disable-javascript-samples) if you want to hide the detailed flame chart of JavaScript calls.</span></span>  <span data-ttu-id="f3d3d-237">Lorsque les exemples de JS sont désactivés, vous ne voyez que les événements de niveau supérieur, comme `Event: click` et `Function Call` de la figure précédente.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-237">When JS samples are disabled, you only see high-level events such as `Event: click` and `Function Call` from the previous figure.</span></span>  

### <span data-ttu-id="f3d3d-238">Afficher les activités d’un tableau</span><span class="sxs-lookup"><span data-stu-id="f3d3d-238">View activities in a table</span></span>  

<span data-ttu-id="f3d3d-239">Après avoir enregistré une page, il n’est pas nécessaire de dépendre uniquement de la section **principale** permettant d’analyser les activités.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-239">After recording a page, you do not need to rely solely on the **Main** section to analyze activities.</span></span>  <span data-ttu-id="f3d3d-240">DevTools fournit également trois vues tabulaires pour l’analyse des activités.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-240">DevTools also provides three tabular views for analyzing activities.</span></span>  <span data-ttu-id="f3d3d-241">Chaque affichage vous offre une perspective différente des activités:</span><span class="sxs-lookup"><span data-stu-id="f3d3d-241">Each view gives you a different perspective on the activities:</span></span>  

*   <span data-ttu-id="f3d3d-242">Pour afficher les activités racines qui génèrent le plus de tâches, utilisez [l’onglet arborescence des appels](#the-call-tree-tab).</span><span class="sxs-lookup"><span data-stu-id="f3d3d-242">When you want to view the root activities that cause the most work, use [the Call Tree tab](#the-call-tree-tab).</span></span>  
*   <span data-ttu-id="f3d3d-243">Pour afficher les activités pour lesquelles le plus de temps est passé directement, utilisez [l’onglet Bottom-Up](#the-bottom-up-tab).</span><span class="sxs-lookup"><span data-stu-id="f3d3d-243">When you want to view the activities where the most time was directly spent, use [the Bottom-Up tab](#the-bottom-up-tab).</span></span>  
*   <span data-ttu-id="f3d3d-244">Si vous voulez afficher les activités dans l’ordre dans lequel elles se sont produites lors de l’enregistrement, utilisez [l’onglet journal des événements](#the-event-log-tab).</span><span class="sxs-lookup"><span data-stu-id="f3d3d-244">When you want to view the activities in the order in which they occurred during the recording, use [the Event Log tab](#the-event-log-tab).</span></span>  
    
> [!NOTE]
> <span data-ttu-id="f3d3d-245">Les trois sections suivantes se réfèrent à la même démonstration.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-245">The next three sections all refer to the same demo.</span></span>  <span data-ttu-id="f3d3d-246">Exécutez la démonstration vous-même dans les [onglets activité][ActivityTabsDemo].</span><span class="sxs-lookup"><span data-stu-id="f3d3d-246">Run the demo yourself at [Activity Tabs Demo][ActivityTabsDemo].</span></span>  

#### <span data-ttu-id="f3d3d-247">Activités racines</span><span class="sxs-lookup"><span data-stu-id="f3d3d-247">Root activities</span></span>  

<span data-ttu-id="f3d3d-248">Voici une description du concept d' **activités racines** mentionné dans les sections de l’onglet **arborescence des appels** , de **bas en haut** et **Journal des événements** .</span><span class="sxs-lookup"><span data-stu-id="f3d3d-248">Here is an explanation of the **root activities** concept that is mentioned in the **Call Tree** tab, **Bottom-Up** tab, and **Event Log** sections.</span></span>  

<span data-ttu-id="f3d3d-249">Les activités racines peuvent entraîner le fonctionnement du navigateur.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-249">Root activities are those which cause the browser to do some work.</span></span>  <span data-ttu-id="f3d3d-250">Par exemple, lorsque vous cliquez sur une page, le navigateur déclenche une `Event` activité en tant qu’activité racine.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-250">For example, when you click a page, the browser fires an `Event` activity as the root activity.</span></span>  <span data-ttu-id="f3d3d-251">Cela `Event` peut entraîner l’exécution d’un gestionnaire et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-251">That `Event` might cause a handler to run, and so on.</span></span>  

<span data-ttu-id="f3d3d-252">Dans le graphique en flamme de la section **principale** , les activités racines se trouvent en haut du graphique.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-252">In the flame chart of the **Main** section, root activities are at the top of the chart.</span></span>  <span data-ttu-id="f3d3d-253">Dans les onglets **arborescence des appels** et **Journal des événements** , les activités racines sont les éléments de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-253">In the **Call Tree** and **Event Log** tabs, root activities are the top-level items.</span></span>  

<span data-ttu-id="f3d3d-254">Accédez à [l’onglet arborescence des appels](#the-call-tree-tab) pour obtenir un exemple d’activités racines.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-254">Navigate to [The Call Tree tab](#the-call-tree-tab) for an example of root activities.</span></span>  

#### <span data-ttu-id="f3d3d-255">Onglet arborescence des appels</span><span class="sxs-lookup"><span data-stu-id="f3d3d-255">The Call Tree tab</span></span>  

<span data-ttu-id="f3d3d-256">Utilisez l’onglet **arborescence des appels** pour afficher les [activités racines](#root-activities) qui sont à l’origine du problème.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-256">Use the **Call Tree** tab to view which [root activities](#root-activities) cause the most work.</span></span>  

<span data-ttu-id="f3d3d-257">L’onglet **arborescence des appels** affiche uniquement les activités effectuées au cours de la partie sélectionnée de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-257">The **Call Tree** tab only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="f3d3d-258">Naviguez jusqu’à [Sélectionner une portion d’un enregistrement](#select-a-portion-of-a-recording) pour savoir comment sélectionner des parties.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-258">Navigate to [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-call-tree.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-call-tree.msft.png":::
   <span data-ttu-id="f3d3d-260">Onglet **arborescence des appels**</span><span class="sxs-lookup"><span data-stu-id="f3d3d-260">The **Call Tree** tab</span></span>  
:::image-end:::  

<span data-ttu-id="f3d3d-261">Dans l’illustration précédente, le niveau supérieur des éléments de la colonne **Activity** , par exemple, `Evaluate Script` les `Parse HTML` activités racines.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-261">In the previous figure, the top-level of items in the **Activity** column, such as `Evaluate Script` and `Parse HTML` are root activities.</span></span>  <span data-ttu-id="f3d3d-262">L’imbrication représente la pile d’appels.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-262">The nesting represents the call stack.</span></span>  <span data-ttu-id="f3d3d-263">Par exemple, dans l’illustration précédente, `Parse HTML` ce qui a provoqué `Evaluate Script` `Compile Script` et `(anonymous)` .</span><span class="sxs-lookup"><span data-stu-id="f3d3d-263">For example, in the previous figure, `Parse HTML` which caused `Evaluate Script` which caused `Compile Script` and `(anonymous)`.</span></span>  

<span data-ttu-id="f3d3d-264">Le **temps libre** représente le temps passé directement dans cette activité.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-264">**Self Time** represents the time directly spent in that activity.</span></span>  <span data-ttu-id="f3d3d-265">**Durée totale** représente le temps passé à cette activité ou à un des enfants.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-265">**Total Time** represents the time spent in that activity or any of the children.</span></span>  

<span data-ttu-id="f3d3d-266">Choisissez **temps libre**, **durée totale**ou **activité** pour trier le tableau selon la colonne.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-266">Choose **Self Time**, **Total Time**, or **Activity** to sort the table by that column.</span></span>  

<span data-ttu-id="f3d3d-267">Utilisez la zone de texte **filtre** pour filtrer les événements par nom d’activité.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-267">Use the **Filter** text box to filter events by activity name.</span></span>  

<span data-ttu-id="f3d3d-268">Par défaut, le menu de **regroupement** a la valeur **aucun regroupement**.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-268">By default the **Grouping** menu is set to **No Grouping**.</span></span>  <span data-ttu-id="f3d3d-269">Utilisez le menu de **regroupement** pour trier la table d’activité en fonction de différents critères.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-269">Use the **Grouping** menu to sort the activity table based on various criteria.</span></span>  

<span data-ttu-id="f3d3d-270">Pour **Show Heaviest Stack** afficher ![ ][ImageShowHeaviestStackIcon] une autre table à droite de la table **Activity** , sélectionnez Afficher la pile la plus lourde.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-270">Choose **Show Heaviest Stack** \(![Show Heaviest Stack][ImageShowHeaviestStackIcon]\) to reveal another table to the right of the **Activity** table.</span></span>  <span data-ttu-id="f3d3d-271">Cliquez sur une activité pour remplir la table de pile la plus **lourde** .</span><span class="sxs-lookup"><span data-stu-id="f3d3d-271">Click on an activity to populate the **Heaviest Stack** table.</span></span>  <span data-ttu-id="f3d3d-272">La table des piles les plus **lourdes** vous indique les enfants de l’activité sélectionnée qui prenaient le plus de temps à s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-272">The **Heaviest Stack** table shows you which children of the selected activity took the longest time to run.</span></span>  

#### <span data-ttu-id="f3d3d-273">Onglet Bottom-Up</span><span class="sxs-lookup"><span data-stu-id="f3d3d-273">The Bottom-Up tab</span></span>  

<span data-ttu-id="f3d3d-274">Utilisez l’onglet **inférieur** pour afficher les activités qui consomment directement le plus de temps dans l’agrégat.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-274">Use the **Bottom-Up** tab to view which activities directly took up the most time in aggregate.</span></span>  

<span data-ttu-id="f3d3d-275">L’onglet **inférieur** affiche uniquement les activités effectuées au cours de la partie sélectionnée de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-275">The **Bottom-Up** tab only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="f3d3d-276">Naviguez jusqu’à [Sélectionner une portion d’un enregistrement](#select-a-portion-of-a-recording) pour savoir comment sélectionner des parties.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-276">Navigate to [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-bottoms-up.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-bottoms-up.msft.png":::
   <span data-ttu-id="f3d3d-278">Onglet **inférieur**</span><span class="sxs-lookup"><span data-stu-id="f3d3d-278">The **Bottom-Up** tab</span></span>  
:::image-end:::  

<span data-ttu-id="f3d3d-279">Dans le graphique en forme de flamme **de la figure** précédente, naviguez jusqu’à ce que presque en tout le temps soit passé `Parse HTML` .</span><span class="sxs-lookup"><span data-stu-id="f3d3d-279">In the **Main** section flame chart of the previous figure, navigate to that almost practically all of the time was spent running `Parse HTML`.</span></span>  <span data-ttu-id="f3d3d-280">Dans l’onglet **inférieur** de la figure précédente, l’activité supérieure `Parse HTML` .</span><span class="sxs-lookup"><span data-stu-id="f3d3d-280">The top activity in the **Bottom-Up** tab of the previous figure is `Parse HTML`.</span></span>  <!--In the flame chart of the previous figure, the yellow below the calls to `wait` are actually thousands of `Minor GC` calls.  -->  <span data-ttu-id="f3d3d-281">Accédez à l’onglet **inférieur haut** , l’activité la plus coûteuse suivante `Layout` .</span><span class="sxs-lookup"><span data-stu-id="f3d3d-281">Navigate to in the **Bottom-Up** tab, the next most expensive activity is `Layout`.</span></span>  

<span data-ttu-id="f3d3d-282">La colonne de **temps libre** représente le temps agrégé passé directement dans cette activité, sur l’ensemble des occurrences.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-282">The **Self Time** column represents the aggregated time spent directly in that activity, across all of the occurrences.</span></span>  

<span data-ttu-id="f3d3d-283">La colonne **temps total** représente le temps agrégé dépensé dans cette activité ou sur n’importe quel enfant.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-283">The **Total Time** column represents aggregated time spent in that activity or any of the children.</span></span>  

#### <span data-ttu-id="f3d3d-284">Onglet journal des événements</span><span class="sxs-lookup"><span data-stu-id="f3d3d-284">The Event Log tab</span></span>  

<span data-ttu-id="f3d3d-285">Utilisez l’onglet **Journal des événements** pour afficher les activités dans l’ordre dans lequel elles se sont produites lors de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-285">Use the **Event Log** tab to view activities in the order in which they occurred during the recording.</span></span>  

<span data-ttu-id="f3d3d-286">L’onglet **Journal des événements** affiche uniquement les activités effectuées au cours de la partie sélectionnée de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-286">The **Event Log** tab only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="f3d3d-287">Naviguez jusqu’à [Sélectionner une portion d’un enregistrement](#select-a-portion-of-a-recording) pour savoir comment sélectionner des parties.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-287">Navigate to [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-event-log.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-event-log.msft.png":::
   <span data-ttu-id="f3d3d-289">Onglet **Journal des événements**</span><span class="sxs-lookup"><span data-stu-id="f3d3d-289">The **Event Log** tab</span></span>  
:::image-end:::  

<span data-ttu-id="f3d3d-290">La colonne **heure de début** représente le point auquel cette activité a commencé, par rapport au début de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-290">The **Start Time** column represents the point at which that activity started, relative to the start of the recording.</span></span>  <span data-ttu-id="f3d3d-291">Par exemple, l’heure de début de `175.7 ms` l’élément sélectionné dans la figure précédente signifie que l’activité a démarré 175,7 ms après le début de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-291">For example, the start time of `175.7 ms` for the selected item in the previous figure means that activity started 175.7 ms after the recording started.</span></span>  

<span data-ttu-id="f3d3d-292">La colonne **temps libre** représente le temps passé directement dans cette activité.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-292">The **Self Time** column represents the time spent directly in that activity.</span></span>  

<span data-ttu-id="f3d3d-293">Le **nombre total** de colonnes durée représente le temps passé directement dans cette activité ou dans n’importe quel enfant.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-293">The **Total Time** columns represents time spent directly in that activity or in any of the children.</span></span>  

<span data-ttu-id="f3d3d-294">Sélectionnez **heure de début**, **durée automatique**ou **durée totale** pour trier le tableau selon la colonne.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-294">Choose **Start Time**, **Self Time**, or **Total Time** to sort the table by that column.</span></span>

<span data-ttu-id="f3d3d-295">Utilisez la zone de texte **filtre** pour filtrer les activités par nom.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-295">Use the **Filter** text box to filter activities by name.</span></span>  

<span data-ttu-id="f3d3d-296">Utilisez le menu **durée** pour filtrer les activités ayant eu moins de 1 ms ou 15 ms.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-296">Use the **Duration** menu to filter out any activities that took less than 1 ms or 15 ms.</span></span>  <span data-ttu-id="f3d3d-297">Par défaut, le menu **durée** est défini sur **tout**, ce qui signifie que toutes les activités sont affichées.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-297">By default the **Duration** menu is set to **All**, meaning all activities are shown.</span></span>  

<span data-ttu-id="f3d3d-298">Désactivez les cases à cocher **chargement**, **script**, **rendu**ou **peinture** pour filtrer toutes les activités de ces catégories.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-298">Disable the **Loading**, **Scripting**, **Rendering**, or **Painting** checkboxes to filter out all activities from those categories.</span></span>  

### <span data-ttu-id="f3d3d-299">Afficher l’activité GPU</span><span class="sxs-lookup"><span data-stu-id="f3d3d-299">View GPU activity</span></span>  

<span data-ttu-id="f3d3d-300">Afficher l’activité GPU dans la section **GPU** .</span><span class="sxs-lookup"><span data-stu-id="f3d3d-300">View GPU activity in the **GPU** section.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-gpu-zoomed.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-gpu-zoomed.msft.png":::
   <span data-ttu-id="f3d3d-302">Section **GPU**</span><span class="sxs-lookup"><span data-stu-id="f3d3d-302">The **GPU** section</span></span>  
:::image-end:::  

### <span data-ttu-id="f3d3d-303">Afficher les activités pixellisées</span><span class="sxs-lookup"><span data-stu-id="f3d3d-303">View raster activity</span></span>  

<span data-ttu-id="f3d3d-304">Affichez les activités pixellisées dans la section **Raster** .</span><span class="sxs-lookup"><span data-stu-id="f3d3d-304">View raster activity in the **Raster** section.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-raster.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-raster.msft.png":::
   <span data-ttu-id="f3d3d-306">Section **Raster**</span><span class="sxs-lookup"><span data-stu-id="f3d3d-306">The **Raster** section</span></span>  
:::image-end:::  

### <span data-ttu-id="f3d3d-307">Afficher les interactions</span><span class="sxs-lookup"><span data-stu-id="f3d3d-307">View interactions</span></span>  

<span data-ttu-id="f3d3d-308">Utilisez la section **interactions** pour rechercher et analyser les interactions utilisateur qui se sont produites lors de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-308">Use the **Interactions** section to find and analyze user interactions that happened during the recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-interactions-animation.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-interactions-animation.msft.png":::
   <span data-ttu-id="f3d3d-310">Section **interactions**</span><span class="sxs-lookup"><span data-stu-id="f3d3d-310">The **Interactions** section</span></span>  
:::image-end:::  

<span data-ttu-id="f3d3d-311">Une ligne rouge en bas d’une interaction représente le temps passé à attendre le thread principal.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-311">A red line at the bottom of an interaction represents time spent waiting for the main thread.</span></span>  

<span data-ttu-id="f3d3d-312">Cliquez sur une interaction pour afficher davantage d’informations sur celle-ci sous l’onglet **Résumé** .</span><span class="sxs-lookup"><span data-stu-id="f3d3d-312">Click an interaction to view more information about it in the **Summary** tab.</span></span>  

### <span data-ttu-id="f3d3d-313">Analyser les images par seconde (FPS)</span><span class="sxs-lookup"><span data-stu-id="f3d3d-313">Analyze frames per second (FPS)</span></span>  

<span data-ttu-id="f3d3d-314">DevTools offre de nombreuses façons d’analyser les images par seconde:</span><span class="sxs-lookup"><span data-stu-id="f3d3d-314">DevTools provides numerous ways to analyze frames per second:</span></span>  

*   <span data-ttu-id="f3d3d-315">Utilisez [le graphique fps](#the-fps-chart) pour obtenir une vue d’ensemble des images par seconde au fil de la durée de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-315">Use [the FPS chart](#the-fps-chart) to get an overview of FPS over the duration of the recording.</span></span>  
*   <span data-ttu-id="f3d3d-316">Utilisez [la section cadres](#the-frames-section) pour afficher la durée d’une image particulière.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-316">Use [the Frames section](#the-frames-section) to view how long a particular frame took.</span></span>  
*   <span data-ttu-id="f3d3d-317">Utilisez le **compteur fps** pour une estimation en temps réel de FPS lors de l’exécution de la page.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-317">Use the **FPS meter** for a realtime estimate of FPS as the page runs.</span></span>  <span data-ttu-id="f3d3d-318">Naviguez jusqu’à [l’affichage des images par seconde en temps réel à l’aide du vumètre fps](#view-frames-per-second-in-realtime-with-the-fps-meter).</span><span class="sxs-lookup"><span data-stu-id="f3d3d-318">Navigate to [View frames per second in realtime with the FPS meter](#view-frames-per-second-in-realtime-with-the-fps-meter).</span></span>  
    
#### <span data-ttu-id="f3d3d-319">Graphique FPS</span><span class="sxs-lookup"><span data-stu-id="f3d3d-319">The FPS chart</span></span>  

<span data-ttu-id="f3d3d-320">Le graphique **fps** fournit une vue d’ensemble de la fréquence d’images sur la durée d’un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-320">The **FPS** chart provides an overview of the frame rate across the duration of a recording.</span></span>  <span data-ttu-id="f3d3d-321">En règle générale, plus la barre verte est élevée, plus la fréquence d’images est élevée.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-321">In general, the higher the green bar, the better the frame rate.</span></span>  

<span data-ttu-id="f3d3d-322">Une barre rouge au-dessus du graphique **fps** est une alerte indiquant que le taux d’images a été interrompu comme faible et qu’il a probablement été lésé par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-322">A red bar above the **FPS** chart is a warning that the frame rate dropped so low that it probably harmed the user's experience.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-fps-highlight.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-fps-highlight.msft.png":::
   <span data-ttu-id="f3d3d-324">Graphique **fps**</span><span class="sxs-lookup"><span data-stu-id="f3d3d-324">The **FPS** chart</span></span>  
:::image-end:::  

#### <span data-ttu-id="f3d3d-325">Section cadres</span><span class="sxs-lookup"><span data-stu-id="f3d3d-325">The Frames section</span></span>  

<span data-ttu-id="f3d3d-326">La section **trames** vous indique exactement le temps qu’une image donnée a duré.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-326">The **Frames** section tells you exactly how long a particular frame took.</span></span>  

<span data-ttu-id="f3d3d-327">Pointez sur un cadre pour afficher une info-bulle contenant des informations supplémentaires à son sujet.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-327">Hover over a frame to view a tooltip with more information about it.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-frames-hover.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-frames-hover.msft.png":::
   <span data-ttu-id="f3d3d-329">Survol d’un cadre</span><span class="sxs-lookup"><span data-stu-id="f3d3d-329">Hover over a frame</span></span>  
:::image-end:::  

<span data-ttu-id="f3d3d-330">Cliquez sur un cadre pour afficher encore plus d’informations sur le cadre sous l’onglet **Résumé** .  DevTools plan le cadre sélectionné en bleu.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-330">Click on a frame to view even more information about the frame in the **Summary** tab.  DevTools outlines the selected frame in blue.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-frames-summary.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-frames-summary.msft.png":::
   <span data-ttu-id="f3d3d-332">Afficher un cadre sous l’onglet **Résumé**</span><span class="sxs-lookup"><span data-stu-id="f3d3d-332">View a frame in the **Summary** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="f3d3d-333">Afficher les requêtes réseau</span><span class="sxs-lookup"><span data-stu-id="f3d3d-333">View network requests</span></span>  

<span data-ttu-id="f3d3d-334">Développez la section **réseau** pour afficher une cascade de requêtes réseau qui se sont produites lors de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-334">Expand the **Network** section to view a waterfall of network requests that occurred during the recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-network.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-network.msft.png":::
   <span data-ttu-id="f3d3d-336">Section **réseau**</span><span class="sxs-lookup"><span data-stu-id="f3d3d-336">The **Network** section</span></span>  
:::image-end:::  

<span data-ttu-id="f3d3d-337">Les requêtes sont codées en couleur comme suit:</span><span class="sxs-lookup"><span data-stu-id="f3d3d-337">Requests are color-coded as follows:</span></span>  

*   <span data-ttu-id="f3d3d-338">HTML: bleu</span><span class="sxs-lookup"><span data-stu-id="f3d3d-338">HTML: Blue</span></span>  
*   <span data-ttu-id="f3d3d-339">CSS: pourpre</span><span class="sxs-lookup"><span data-stu-id="f3d3d-339">CSS: Purple</span></span>  
*   <span data-ttu-id="f3d3d-340">JS: jaune</span><span class="sxs-lookup"><span data-stu-id="f3d3d-340">JS: Yellow</span></span>  
*   <span data-ttu-id="f3d3d-341">Images: vert</span><span class="sxs-lookup"><span data-stu-id="f3d3d-341">Images: Green</span></span>  
    
<span data-ttu-id="f3d3d-342">Cliquez sur une demande pour afficher davantage d’informations sur celle-ci sous l’onglet **Résumé** .  Par exemple, dans l’illustration précédente, l’onglet **Résumé** affiche des informations supplémentaires sur la requête bleue sélectionnée dans la section **réseau** .</span><span class="sxs-lookup"><span data-stu-id="f3d3d-342">Click on a request to view more information about it in the **Summary** tab.  For example, in the previous figure, the **Summary** tab is displaying more information about the blue request that is selected in the **Network** section.</span></span>  

<span data-ttu-id="f3d3d-343">Dans le coin supérieur gauche d’une demande, un carré plus foncé est une demande de priorité élevée.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-343">A darker-blue square in the top-left of a request means it is a higher-priority request.</span></span>  <span data-ttu-id="f3d3d-344">Le carré bleu plus clair correspond à un niveau de priorité inférieur.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-344">A lighter-blue square means lower-priority.</span></span>  <span data-ttu-id="f3d3d-345">Par exemple, dans l’illustration précédente, la requête bleue, sélectionnée est d’une priorité plus élevée et celle du vert au-dessous, de priorité inférieure.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-345">For example, in the previous figure, the blue, selected request is higher-priority, and the green one below it is lower-priority.</span></span>  

<span data-ttu-id="f3d3d-346">Dans le 1er des figures suivantes, la requête pour `www.bing.com` est représentée par une ligne située sur la gauche, une barre au milieu avec une partie sombre et une partie claire, et une ligne à droite.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-346">In the 1st of the following figures, the request for `www.bing.com` is represented by a line on the left, a bar in the middle with a dark portion and a light portion, and a line on the right.</span></span>  <span data-ttu-id="f3d3d-347">Dans la deuxième des figures suivantes, la représentation correspondante de la même demande apparaît dans l’onglet **minutage** du panneau **réseau** .</span><span class="sxs-lookup"><span data-stu-id="f3d3d-347">In the 2nd of the following figures shows the corresponding representation of the same request in the **Timing** tab of the **Network** panel.</span></span>  <span data-ttu-id="f3d3d-348">Voici à quoi correspondent les deux représentations suivantes:</span><span class="sxs-lookup"><span data-stu-id="f3d3d-348">Here is how these two representations map to each other:</span></span>

*   <span data-ttu-id="f3d3d-349">La ligne gauche représente tout ce qui concerne le `Connection Start` groupe d’événements compris.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-349">The left line is everything up to the `Connection Start` group of events, inclusive.</span></span>  <span data-ttu-id="f3d3d-350">En d’autres termes, il s’agit de tout ce qui est auparavant `Request Sent` , exclusif.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-350">In other words, it is everything before `Request Sent`, exclusive.</span></span>  
*   <span data-ttu-id="f3d3d-351">La partie claire de la barre est `Request Sent` et `Waiting (TTFB)` .</span><span class="sxs-lookup"><span data-stu-id="f3d3d-351">The light portion of the bar is `Request Sent` and `Waiting (TTFB)`.</span></span>  
*   <span data-ttu-id="f3d3d-352">La partie sombre de la barre est `Content Download` .</span><span class="sxs-lookup"><span data-stu-id="f3d3d-352">The dark portion of the bar is `Content Download`.</span></span>  
*   <span data-ttu-id="f3d3d-353">La ligne droite correspond essentiellement au délai passé pour le thread principal.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-353">The right line is essentially time spent waiting for the main thread.</span></span>  <span data-ttu-id="f3d3d-354">Cette opération n’est pas représentée dans l’onglet **minutage** .</span><span class="sxs-lookup"><span data-stu-id="f3d3d-354">This is not represented in the **Timing** tab.</span></span>  
    
:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-performance-network.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-bing-performance-network.msft.png":::
         <span data-ttu-id="f3d3d-356">Représentation de la barre de lignes de la `www.bing.com` requête</span><span class="sxs-lookup"><span data-stu-id="f3d3d-356">The line-bar representation of the `www.bing.com` request</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-network-timing.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-bing-network-timing.msft.png":::
         <span data-ttu-id="f3d3d-358">Outil **réseau**</span><span class="sxs-lookup"><span data-stu-id="f3d3d-358">The **Network** tool</span></span>  
<span data-ttu-id="f3d3d-359">:::: image-fin:::</span><span class="sxs-lookup"><span data-stu-id="f3d3d-359">:     ::image-end:::</span></span>  
   :::column-end:::
:::row-end:::

### <span data-ttu-id="f3d3d-360">Afficher les métriques de mémoire</span><span class="sxs-lookup"><span data-stu-id="f3d3d-360">View memory metrics</span></span>  

<span data-ttu-id="f3d3d-361">Activez la case à cocher **mémoire** pour afficher les mesures de mémoire du dernier enregistrement.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-361">Enable the **Memory** checkbox to view memory metrics from the last recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-memory-highlight.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-memory-highlight.msft.png":::
   <span data-ttu-id="f3d3d-363">Case à cocher **mémoire**</span><span class="sxs-lookup"><span data-stu-id="f3d3d-363">The **Memory** checkbox</span></span>  
:::image-end:::  

<span data-ttu-id="f3d3d-364">DevTools affiche un nouveau graphique **mémoire** , au-dessus de l’onglet **Résumé** .  Il existe également un nouveau graphique sous le graphique **net** , appelé **tas**.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-364">DevTools displays a new **Memory** chart, above the **Summary** tab.  There is also a new chart below the **NET** chart, called **HEAP**.</span></span>  <span data-ttu-id="f3d3d-365">Le graphique de **tas** fournit les mêmes informations que la ligne de segment de **mémoire** **js** dans le graphique mémoire.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-365">The **HEAP** chart provides the same information as the **JS Heap** line in the **Memory** chart.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-memory-chart.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-memory-chart.msft.png":::
   <span data-ttu-id="f3d3d-367">Métriques de mémoire</span><span class="sxs-lookup"><span data-stu-id="f3d3d-367">Memory metrics</span></span>  
:::image-end:::  

<span data-ttu-id="f3d3d-368">Les lignes de couleur sur le graphique correspondent aux cases à cocher en plus de la couleur du graphique.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-368">The colored lines on the chart map to the colored checkboxes above the chart.</span></span>  
<span data-ttu-id="f3d3d-369">Désactivez une case à cocher pour masquer cette catégorie dans le graphique.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-369">Disable a checkbox to hide that category from the chart.</span></span>  

<span data-ttu-id="f3d3d-370">Le graphique affiche uniquement la zone de l’enregistrement actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-370">The chart only displays the region of the recording that is currently selected.</span></span>  <span data-ttu-id="f3d3d-371">Par exemple, dans l’illustration précédente, le graphique **mémoire** affiche uniquement l’utilisation de la mémoire de la marque 400 ms au 1750 ms.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-371">For example, in the previous figure, the **Memory** chart is only showing memory usage from around the 400 ms mark to the 1750 ms mark.</span></span>  

### <span data-ttu-id="f3d3d-372">Affichage de la durée d’une portion d’un enregistrement</span><span class="sxs-lookup"><span data-stu-id="f3d3d-372">View the duration of a portion of a recording</span></span>  

<span data-ttu-id="f3d3d-373">Lors de l’analyse d’une section comme **Network** ou **principal**, il est possible que vous ayez besoin d’une estimation plus précise de la durée de certains événements.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-373">When analyzing a section like **Network** or **Main**, sometimes you need a more precise estimate of how long certain events took.</span></span>  <span data-ttu-id="f3d3d-374">Maintenez la touche enfoncée, `Shift` puis faites glisser vers la gauche ou la droite pour sélectionner une partie de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-374">Hold `Shift`, click and hold, and drag left or right to select a portion of the recording.</span></span>  <span data-ttu-id="f3d3d-375">Dans la partie inférieure de votre sélection, DevTools indique la durée de la partie.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-375">At the bottom of your selection, DevTools shows how long that portion took.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-main-duration.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-main-duration.msft.png":::
   <span data-ttu-id="f3d3d-377">Affichage de la durée d’une portion d’un enregistrement</span><span class="sxs-lookup"><span data-stu-id="f3d3d-377">View the duration of a portion of a recording</span></span>  
:::image-end:::  

### <span data-ttu-id="f3d3d-378">Affichage d’une capture d’écran</span><span class="sxs-lookup"><span data-stu-id="f3d3d-378">View a screenshot</span></span>  

<span data-ttu-id="f3d3d-379">Pour plus d’informations sur l’activation des captures d’écran, accédez à capture des captures d' [écran lors de l’enregistrement](#capture-screenshots-while-recording) .</span><span class="sxs-lookup"><span data-stu-id="f3d3d-379">Navigate to [Capture screenshots while recording](#capture-screenshots-while-recording) to learn how to enable screenshots.</span></span>  

<span data-ttu-id="f3d3d-380">Placez le pointeur de la souris sur la **vue d’ensemble** pour afficher une capture d’écran illustrant l’apparence de la page pendant ce moment de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-380">Hover over the **Overview** to view a screenshot of how the page looked during that moment of the recording.</span></span>  <span data-ttu-id="f3d3d-381">La section **vue d’ensemble** contient les graphiques **UC**, **fps**et **net** .</span><span class="sxs-lookup"><span data-stu-id="f3d3d-381">The **Overview** is the section that contains the **CPU**, **FPS**, and **NET** charts.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-screenshots-hover.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-screenshots-hover.msft.png":::
   <span data-ttu-id="f3d3d-383">Affichage d’une capture d’écran</span><span class="sxs-lookup"><span data-stu-id="f3d3d-383">View a screenshot</span></span>  
:::image-end:::  

<span data-ttu-id="f3d3d-384">Vous pouvez également afficher les captures d’écran en cliquant sur un cadre dans la section **cadres** .</span><span class="sxs-lookup"><span data-stu-id="f3d3d-384">You may also view screenshots by clicking a frame in the **Frames** section.</span></span>  <span data-ttu-id="f3d3d-385">DevTools affiche une version miniature de la capture d’écran sous l’onglet **Résumé** .</span><span class="sxs-lookup"><span data-stu-id="f3d3d-385">DevTools displays a small version of the screenshot in the **Summary** tab.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-summary-preview.msft.png":::
   <span data-ttu-id="f3d3d-387">Affichage d’une capture d’écran sous l’onglet **Résumé**</span><span class="sxs-lookup"><span data-stu-id="f3d3d-387">View a screenshot in the **Summary** tab</span></span>  
:::image-end:::  

<span data-ttu-id="f3d3d-388">Pour effectuer un zoom avant dans la capture d’écran, cliquez sur la miniature sous l’onglet **Résumé** .</span><span class="sxs-lookup"><span data-stu-id="f3d3d-388">Click the thumbnail in the **Summary** tab to zoom in on the screenshot.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview-select.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-summary-preview-select.msft.png":::
   <span data-ttu-id="f3d3d-390">Effectuer un zoom avant sur une capture d’écran à partir de l’onglet **Résumé**</span><span class="sxs-lookup"><span data-stu-id="f3d3d-390">Zoom into a screenshot from the **Summary** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="f3d3d-391">Afficher les informations sur les couches</span><span class="sxs-lookup"><span data-stu-id="f3d3d-391">View layers information</span></span>  

<span data-ttu-id="f3d3d-392">Pour afficher des informations sur les couches avancées d’une image:</span><span class="sxs-lookup"><span data-stu-id="f3d3d-392">To view advanced layers information about a frame:</span></span>  

1.  <span data-ttu-id="f3d3d-393">[Activez Advanced Paint instrumentation](#enable-advanced-paint-instrumentation).</span><span class="sxs-lookup"><span data-stu-id="f3d3d-393">[Enable advanced paint instrumentation](#enable-advanced-paint-instrumentation).</span></span>  
1.  <span data-ttu-id="f3d3d-394">Sélectionnez une image dans la section **cadre** .</span><span class="sxs-lookup"><span data-stu-id="f3d3d-394">Select a frame in the **Frames** section.</span></span>  <span data-ttu-id="f3d3d-395">DevTools affiche des informations sur les calques sous l’onglet nouveau **calques** , en regard de l’onglet **Journal des événements** .</span><span class="sxs-lookup"><span data-stu-id="f3d3d-395">DevTools displays information about the layers in the new **Layers** tab, next to the **Event Log** tab.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-layers-all.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-layers-all.msft.png":::
       <span data-ttu-id="f3d3d-397">Volet **couches**</span><span class="sxs-lookup"><span data-stu-id="f3d3d-397">The **Layers** pane</span></span>  
    :::image-end:::  
    
<span data-ttu-id="f3d3d-398">Pointez sur un calque pour le mettre en surbrillance dans le diagramme.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-398">Hover over a layer to highlight it in the diagram.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png":::
   <span data-ttu-id="f3d3d-400">Mettre un calque en surbrillance</span><span class="sxs-lookup"><span data-stu-id="f3d3d-400">Highlight a layer</span></span>  
:::image-end:::  

<span data-ttu-id="f3d3d-401">Pour déplacer le diagramme:</span><span class="sxs-lookup"><span data-stu-id="f3d3d-401">To move the diagram:</span></span>  

*   <span data-ttu-id="f3d3d-402">Sélectionnez **mode panoramique** \ ( ![ mode panoramique ][ImagePanModeIcon] \) pour vous déplacer le long des axes X et Y.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-402">Choose **Pan Mode** \(![Pan Mode][ImagePanModeIcon]\) to move along the X and Y axes.</span></span>  
*   <span data-ttu-id="f3d3d-403">**Rotate Mode** ![ ][ImageRotateModeIcon] Pour faire pivoter le long de l’axe Z, sélectionnez mode de rotation.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-403">Choose **Rotate Mode** \(![Rotate Mode][ImageRotateModeIcon]\) to rotate along the Z axis.</span></span>  
*   <span data-ttu-id="f3d3d-404">Sélectionnez **Réinitialiser la transformation** \ ( ![ Réinitialiser la transformation ][ImageResetTransformIcon] \) pour rétablir la position d’origine du diagramme.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-404">Choose **Reset Transform** \(![Reset Transform][ImageResetTransformIcon]\) to reset the diagram to the original position.</span></span>  
    
### <span data-ttu-id="f3d3d-405">Afficher le générateur de dessin Paint</span><span class="sxs-lookup"><span data-stu-id="f3d3d-405">View paint profiler</span></span>  

<span data-ttu-id="f3d3d-406">Pour afficher des informations détaillées sur un événement Paint:</span><span class="sxs-lookup"><span data-stu-id="f3d3d-406">To view advanced information about a paint event:</span></span>  

1.  <span data-ttu-id="f3d3d-407">[Activez Advanced Paint instrumentation](#enable-advanced-paint-instrumentation).</span><span class="sxs-lookup"><span data-stu-id="f3d3d-407">[Enable advanced paint instrumentation](#enable-advanced-paint-instrumentation).</span></span>  
1.  <span data-ttu-id="f3d3d-408">Sélectionnez un événement **Paint** dans la section **principale** .</span><span class="sxs-lookup"><span data-stu-id="f3d3d-408">Select a **Paint** event in the **Main** section.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-paint-profiler.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-paint-profiler.msft.png":::
       <span data-ttu-id="f3d3d-410">Onglet **Paint Profiler1.1**</span><span class="sxs-lookup"><span data-stu-id="f3d3d-410">The **Paint Profiler** tab</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="f3d3d-411">Analyser les performances de rendu à l’aide de l’onglet rendu</span><span class="sxs-lookup"><span data-stu-id="f3d3d-411">Analyze rendering performance with the Rendering tab</span></span>  

<span data-ttu-id="f3d3d-412">Utilisez les fonctionnalités de l’onglet **rendu** pour visualiser les performances de rendu de votre page.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-412">Use the features of the **Rendering** tab to help visualize the rendering performance of your page.</span></span>  

<span data-ttu-id="f3d3d-413">Pour ouvrir l’onglet **rendu** :</span><span class="sxs-lookup"><span data-stu-id="f3d3d-413">To open the **Rendering** tab:</span></span>  

1.  <span data-ttu-id="f3d3d-414">[Ouvrir le menu de commandes][DevToolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="f3d3d-414">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="f3d3d-415">Commencez à taper `Rendering` et sélectionnez `Show Rendering` .</span><span class="sxs-lookup"><span data-stu-id="f3d3d-415">Start typing `Rendering` and select `Show Rendering`.</span></span>  <span data-ttu-id="f3d3d-416">DevTools affiche l’onglet **rendu** en bas de votre fenêtre devtools.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-416">DevTools displays the **Rendering** tab at the bottom of your DevTools window.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-console-drawer-rendering.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-console-drawer-rendering.msft.png":::
       <span data-ttu-id="f3d3d-418">Onglet **rendu**</span><span class="sxs-lookup"><span data-stu-id="f3d3d-418">The **Rendering** tab</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="f3d3d-419">Afficher les images par seconde en temps réel avec le compteur FPS</span><span class="sxs-lookup"><span data-stu-id="f3d3d-419">View frames per second in realtime with the FPS meter</span></span>  

<span data-ttu-id="f3d3d-420">Le **compteur fps** est une superposition qui s’affiche dans le coin supérieur droit de votre fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-420">The **FPS meter** is an overlay that appears in the top-right corner of your viewport.</span></span>  <span data-ttu-id="f3d3d-421">Il fournit une estimation en temps réel de FPS lors de l’exécution de la page.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-421">It provides a realtime estimate of FPS as the page runs.</span></span>  <span data-ttu-id="f3d3d-422">Pour ouvrir le **compteur fps**:</span><span class="sxs-lookup"><span data-stu-id="f3d3d-422">To open the **FPS meter**:</span></span>  

1.  <span data-ttu-id="f3d3d-423">Ouvrez l’onglet **rendu** .  Na [analyse des performances de rendu à l’aide de l’onglet rendu](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="f3d3d-423">Open the **Rendering** tab.  Na [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="f3d3d-424">Activez la case à cocher **vumètre** .</span><span class="sxs-lookup"><span data-stu-id="f3d3d-424">Enable the **FPS Meter** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png":::
       <span data-ttu-id="f3d3d-426">**Vumètre fps**</span><span class="sxs-lookup"><span data-stu-id="f3d3d-426">The **FPS meter**</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="f3d3d-427">Afficher les événements de peinture en temps réel avec le clignotement de la peinture</span><span class="sxs-lookup"><span data-stu-id="f3d3d-427">View painting events in realtime with Paint Flashing</span></span>  

<span data-ttu-id="f3d3d-428">Utilisez la fonction Paint clignotante pour obtenir une vue en temps réel de tous les événements de peinture sur la page.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-428">Use Paint Flashing to get a realtime view of all paint events on the page.</span></span>  <span data-ttu-id="f3d3d-429">Dès qu’une partie de la page est de nouveau peinte, DevTools la place en vert.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-429">Whenever a part of the page gets re-painted, DevTools outlines that section in green.</span></span>  

<span data-ttu-id="f3d3d-430">Pour activer le clignotement des peintures:</span><span class="sxs-lookup"><span data-stu-id="f3d3d-430">To enable Paint Flashing:</span></span>  

1.  <span data-ttu-id="f3d3d-431">Ouvrez l’onglet **rendu** .  Naviguez jusqu’à [l’analyse des performances de rendu avec l’onglet rendu](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="f3d3d-431">Open the **Rendering** tab.  Navigate to [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="f3d3d-432">Activez la case à cocher **Paint clignotant** .</span><span class="sxs-lookup"><span data-stu-id="f3d3d-432">Enable the **Paint Flashing** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png":::
       **<span data-ttu-id="f3d3d-434">Paint clignotant</span><span class="sxs-lookup"><span data-stu-id="f3d3d-434">Paint Flashing</span></span>**  
    :::image-end:::  
    
### <span data-ttu-id="f3d3d-435">Afficher une superposition de calques avec des bordures de calque</span><span class="sxs-lookup"><span data-stu-id="f3d3d-435">View an overlay of layers with Layer Borders</span></span>  

<span data-ttu-id="f3d3d-436">Utilisez les **bordures de calque** pour afficher une superposition des bordures et des vignettes du calque en haut de la page.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-436">Use **Layer Borders** to view an overlay of layer borders and tiles on top of the page.</span></span>  

<span data-ttu-id="f3d3d-437">Pour activer les bordures de calque:</span><span class="sxs-lookup"><span data-stu-id="f3d3d-437">To enable Layer Borders:</span></span>  

1.  <span data-ttu-id="f3d3d-438">Ouvrez l’onglet **rendu** .  Naviguez jusqu’à [l’analyse des performances de rendu avec l’onglet rendu](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="f3d3d-438">Open the **Rendering** tab.  Navigate to [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="f3d3d-439">Activez la case à cocher **bordures de calque** .</span><span class="sxs-lookup"><span data-stu-id="f3d3d-439">Enable the **Layer Borders** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png":::
       **<span data-ttu-id="f3d3d-441">Bordures de calque</span><span class="sxs-lookup"><span data-stu-id="f3d3d-441">Layer Borders</span></span>**  
    :::image-end:::  
    
<span data-ttu-id="f3d3d-442">Accédez aux commentaires figurant dans [debug_colors. cc][ChromiumDebugColors] pour obtenir une description des codes de couleur.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-442">Navigate to the comments in [debug_colors.cc][ChromiumDebugColors] for an explanation of the color-codings.</span></span>  

### <span data-ttu-id="f3d3d-443">Rechercher des problèmes de performances de défilement en temps réel</span><span class="sxs-lookup"><span data-stu-id="f3d3d-443">Find scroll performance issues in realtime</span></span>  

<span data-ttu-id="f3d3d-444">Utilisez des problèmes de performances de défilement pour identifier les éléments de la page qui comportent des écouteurs d’événements liés au défilement qui peuvent nuire aux performances de la page.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-444">Use Scrolling Performance Issues to identify elements of the page that have event listeners related to scrolling that may harm the performance of the page.</span></span>  
<span data-ttu-id="f3d3d-445">DevTools souligne les éléments potentiellement posant problème en bleu-vert.</span><span class="sxs-lookup"><span data-stu-id="f3d3d-445">DevTools outlines the potentially-problematic elements in teal.</span></span>  

<span data-ttu-id="f3d3d-446">Pour afficher les problèmes de performances de défilement:</span><span class="sxs-lookup"><span data-stu-id="f3d3d-446">To view scroll performance issues:</span></span>  

1.  <span data-ttu-id="f3d3d-447">Ouvrez l’onglet **rendu** .  Naviguez jusqu’à [l’analyse des performances de rendu avec l’onglet rendu](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="f3d3d-447">Open the **Rendering** tab.  Navigate to [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="f3d3d-448">Activez la case à cocher **problèmes de performances de défilement** .</span><span class="sxs-lookup"><span data-stu-id="f3d3d-448">Enable the **Scrolling Performance Issues** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png":::
       <span data-ttu-id="f3d3d-450">Les **problèmes de performances de défilement** indiquent que les objets dotés de l’affichage sans calque risquent de nuire aux performances de défilement</span><span class="sxs-lookup"><span data-stu-id="f3d3d-450">**Scrolling Performance Issues** indicates that non-layer viewport-constrained objects may harm scroll performance</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="f3d3d-451">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="f3d3d-451">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCaptureSettingsIcon]: ../media/capture-settings-icon.msft.png  
[ImageClearRecordingIcon]: ../media/clear-recording-icon.msft.png  
[ImageCollectGarbageIcon]: ../media/collect-garbage-icon.msft.png  
[ImageNextIcon]: ../media/next-icon.msft.png  
[ImagePanModeIcon]: ../media/pan-mode-icon.msft.png  
[ImagePreviousIcon]: ../media/previous-icon.msft.png  
[ImageRecordIcon]: ../media/record-icon.msft.png
[ImageRefreshPageIcon]: ../media/refresh-page-icon.msft.png  
[ImageResetTransformIcon]: ../media/reset-transform-icon.msft.png  
[ImageRotateModeIcon]: ../media/rotate-mode-icon.msft.png  
[ImageSearchCaseIcon]: ../media/search-case-icon.msft.png  
[ImageSearchRegexIcon]: ../media/search-regex-icon.msft.png  
[ImageShowHeaviestStackIcon]: ../media/show-heaviest-stack-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"  
[DevToolsCommandMenu]: ../command-menu/index.md#open-the-command-menu "Ouvrez le menu de commandes et exécutez les commandes à l’aide du menu de commandes Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsEvaluatePerformanceGettingStarted]: ./index.md "Prendre en main l’analyse des performances d’exécution | Documents Microsoft"  

[ActivityTabsDemo]: https://microsoft-edge-chromium-devtools.glitch.me/perf/activitytabs.html "Démo des onglets activité | problème"  

[ChromiumDebugColors]: https://cs.chromium.org/chromium/src/cc/debug/debug_colors.cc "debug_colors. cc-recherche de code"  

> [!NOTE]
> <span data-ttu-id="f3d3d-457">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f3d3d-457">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="f3d3d-458">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="f3d3d-458">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="f3d3d-460">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f3d3d-460">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
