---
title: Référence d’analyse des performances
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 59e2f67d773102554b96749690fae51da09428a8
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10984039"
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







# <span data-ttu-id="88c0e-103">Référence d’analyse des performances</span><span class="sxs-lookup"><span data-stu-id="88c0e-103">Performance analysis reference</span></span>   



<span data-ttu-id="88c0e-104">Cette page est une référence complète des fonctionnalités de Microsoft Edge DevTools liées à l’analyse des performances.</span><span class="sxs-lookup"><span data-stu-id="88c0e-104">This page is a comprehensive reference of Microsoft Edge DevTools features related to analyzing performance.</span></span>  

<span data-ttu-id="88c0e-105">Pour plus d’informations sur l’analyse des performances d’une page à l’aide de [Microsoft Edge devtools][MicrosoftEdgeDevTools], voir mise [en route][DevtoolsEvaluatePerformanceGettingStarted] de l’analyse des performances de l’exécution d’une page.</span><span class="sxs-lookup"><span data-stu-id="88c0e-105">See [Get Started With Analyzing Runtime Performance][DevtoolsEvaluatePerformanceGettingStarted] for a guided tutorial on how to analyze the performance of a page using [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <span data-ttu-id="88c0e-106">Performance enregistrement</span><span class="sxs-lookup"><span data-stu-id="88c0e-106">Record performance</span></span>   

### <span data-ttu-id="88c0e-107">Enregistrer les performances d’exécution</span><span class="sxs-lookup"><span data-stu-id="88c0e-107">Record runtime performance</span></span>   

<span data-ttu-id="88c0e-108">Enregistrez les performances d’exécution lorsque vous souhaitez analyser les performances d’une page en cours d’exécution, plutôt que de procéder au chargement.</span><span class="sxs-lookup"><span data-stu-id="88c0e-108">Record runtime performance when you want to analyze the performance of a page as it is running, as opposed to loading.</span></span>  

1.  <span data-ttu-id="88c0e-109">Accédez à la page que vous voulez analyser.</span><span class="sxs-lookup"><span data-stu-id="88c0e-109">Go to the page that you want to analyze.</span></span>  
1.  <span data-ttu-id="88c0e-110">Cliquez sur l’onglet **performance** dans devtools.</span><span class="sxs-lookup"><span data-stu-id="88c0e-110">Click the **Performance** tab in DevTools.</span></span>  
1.  <span data-ttu-id="88c0e-111">Cliquez sur **Enregistrer** \ ( ![ Enregistrer ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="88c0e-111">Click **Record** \(![Record][ImageRecordIcon]\).</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-record-highlight.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-record-highlight.msft.png":::
       **<span data-ttu-id="88c0e-113">Record</span><span class="sxs-lookup"><span data-stu-id="88c0e-113">Record</span></span>**  
    :::image-end:::  
    
1.  <span data-ttu-id="88c0e-114">Interagir avec la page.</span><span class="sxs-lookup"><span data-stu-id="88c0e-114">Interact with the page.</span></span>  <span data-ttu-id="88c0e-115">DevTools enregistre toutes les activités de page résultant de vos interactions.</span><span class="sxs-lookup"><span data-stu-id="88c0e-115">DevTools records all page activity that occurs as a result of your interactions.</span></span>  
1.  <span data-ttu-id="88c0e-116">Cliquez de nouveau sur **Enregistrer** ou cliquez sur **arrêter** pour arrêter l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="88c0e-116">Click **Record** again or click **Stop** to stop recording.</span></span>  
    
### <span data-ttu-id="88c0e-117">Enregistrer les performances de chargement</span><span class="sxs-lookup"><span data-stu-id="88c0e-117">Record load performance</span></span>   

<span data-ttu-id="88c0e-118">Enregistrez les performances de chargement lorsque vous souhaitez analyser les performances d’une page lors du chargement, plutôt que d’être en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="88c0e-118">Record load performance when you want to analyze the performance of a page as it is loading, as opposed to running.</span></span>  

1.  <span data-ttu-id="88c0e-119">Accédez à la page que vous voulez analyser.</span><span class="sxs-lookup"><span data-stu-id="88c0e-119">Go to the page that you want to analyze.</span></span>  
1.  <span data-ttu-id="88c0e-120">Ouvrez le panneau **performances** de devtools.</span><span class="sxs-lookup"><span data-stu-id="88c0e-120">Open the **Performance** panel of DevTools.</span></span>  
1.  <span data-ttu-id="88c0e-121">Cliquez sur **Actualiser la page** \ ( ![ Actualiser la page ][ImageRefreshPageIcon] \).</span><span class="sxs-lookup"><span data-stu-id="88c0e-121">Click **Refresh page** \(![Refresh Page][ImageRefreshPageIcon]\).</span></span>  <span data-ttu-id="88c0e-122">DevTools enregistre les métriques de performances pendant que la page est actualisée, puis arrête automatiquement l’enregistrement de quelques secondes après la fin de la charge.</span><span class="sxs-lookup"><span data-stu-id="88c0e-122">DevTools records performance metrics while the page refreshes and then automatically stops the recording a couple seconds after the load finishes.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-refresh-button.msft.png" alt-text="Actualiser la page" lightbox="../media/evaluate-performance-performance-refresh-button.msft.png":::
       **<span data-ttu-id="88c0e-124">Actualiser la page</span><span class="sxs-lookup"><span data-stu-id="88c0e-124">Refresh page</span></span>**  
    :::image-end:::  
    
<span data-ttu-id="88c0e-125">DevTools effectue automatiquement un zoom avant sur la partie de l’enregistrement où la majeure partie de l’activité s’est produite.</span><span class="sxs-lookup"><span data-stu-id="88c0e-125">DevTools automatically zooms in on the portion of the recording where most of the activity occurred.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed.msft.png" alt-text="Un enregistrement de chargement de page" lightbox="../media/evaluate-performance-performance-refreshed.msft.png":::
   <span data-ttu-id="88c0e-127">Un enregistrement de chargement de page</span><span class="sxs-lookup"><span data-stu-id="88c0e-127">A page-load recording</span></span>  
:::image-end:::  

### <span data-ttu-id="88c0e-128">Capture des captures d’écran lors de l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="88c0e-128">Capture screenshots while recording</span></span>   

<span data-ttu-id="88c0e-129">Activez la case à cocher **captures d’écran** pour capturer une capture d’écran de chaque image lors de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="88c0e-129">Enable the **Screenshots** checkbox to capture a screenshot of every frame while recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png" alt-text="Case à cocher captures d’écran" lightbox="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png":::
   <span data-ttu-id="88c0e-131">Case à cocher **captures d’écran**</span><span class="sxs-lookup"><span data-stu-id="88c0e-131">The **Screenshots** checkbox</span></span>  
:::image-end:::  

<span data-ttu-id="88c0e-132">Pour plus d’informations sur l’interaction avec les captures d’écran, voir [afficher une capture d’écran](#view-a-screenshot) .</span><span class="sxs-lookup"><span data-stu-id="88c0e-132">See [View a screenshot](#view-a-screenshot) to learn how to interact with screenshots.</span></span>  

### <span data-ttu-id="88c0e-133">Forcer le nettoyage de la mémoire lors de l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="88c0e-133">Force garbage collection while recording</span></span>   

<span data-ttu-id="88c0e-134">Pendant que vous enregistrez une page, cliquez sur **collecter le nettoyage** de la mémoire pour le nettoyage de la ![ ][ImageCollectGarbageIcon] mémoire.</span><span class="sxs-lookup"><span data-stu-id="88c0e-134">While you are recording a page, click **Collect garbage** \(![Collect garbage][ImageCollectGarbageIcon]\) to force garbage collection.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-collect-garbage-button.msft.png" alt-text="Collecter les nettoyages de la mémoire" lightbox="../media/evaluate-performance-performance-collect-garbage-button.msft.png":::
   <span data-ttu-id="88c0e-136">Collecter les nettoyages de la mémoire</span><span class="sxs-lookup"><span data-stu-id="88c0e-136">Collect garbage</span></span>  
:::image-end:::  

### <span data-ttu-id="88c0e-137">Afficher les paramètres d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="88c0e-137">Show recording settings</span></span>   

<span data-ttu-id="88c0e-138">Cliquez sur **paramètres de capture** \ (paramètres de ![ capture ][ImageCaptureSettingsIcon] \) pour exposer d’autres paramètres liés à la manière dont devtools capture les enregistrements de performance.</span><span class="sxs-lookup"><span data-stu-id="88c0e-138">Click **Capture settings** \(![Capture settings][ImageCaptureSettingsIcon]\) to expose more settings related to how DevTools captures performance recordings.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png" alt-text="Section paramètres de capture" lightbox="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png":::
   <span data-ttu-id="88c0e-140">Section **paramètres de capture**</span><span class="sxs-lookup"><span data-stu-id="88c0e-140">The **Capture Settings** section</span></span>  
:::image-end:::  

### <span data-ttu-id="88c0e-141">Désactiver les exemples JavaScript</span><span class="sxs-lookup"><span data-stu-id="88c0e-141">Disable JavaScript samples</span></span>   

<span data-ttu-id="88c0e-142">Par défaut, la section **principale** d’un enregistrement affiche des piles d’appels détaillées des fonctions JavaScript qui ont été appelées lors de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="88c0e-142">By default, the **Main** section of a recording displays detailed call stacks of JavaScript functions that were called during the recording.</span></span>  <span data-ttu-id="88c0e-143">Pour désactiver ces piles d’appels:</span><span class="sxs-lookup"><span data-stu-id="88c0e-143">To disable these call stacks:</span></span>  

1.  <span data-ttu-id="88c0e-144">Ouvrir le menu **paramètres de capture** .</span><span class="sxs-lookup"><span data-stu-id="88c0e-144">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="88c0e-145">Voir [afficher les paramètres d’enregistrement](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="88c0e-145">See [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="88c0e-146">Activez la case à cocher **Désactiver les exemples JavaScript** .</span><span class="sxs-lookup"><span data-stu-id="88c0e-146">Enable the **Disable JavaScript Samples** checkbox.</span></span>  
1.  <span data-ttu-id="88c0e-147">Prenez un enregistrement de la page.</span><span class="sxs-lookup"><span data-stu-id="88c0e-147">Take a recording of the page.</span></span>  
    
<span data-ttu-id="88c0e-148">Les 2 figures suivantes présentent la différence entre la désactivation et l’activation des exemples JavaScript.</span><span class="sxs-lookup"><span data-stu-id="88c0e-148">The following 2 figures display the difference between disabling and enabling JavaScript samples.</span></span>  <span data-ttu-id="88c0e-149">La section **principale** de l’enregistrement est beaucoup plus courte lorsque l’échantillonnage est désactivé, car il omet toutes les piles d’appels JavaScript.</span><span class="sxs-lookup"><span data-stu-id="88c0e-149">The **Main** section of the recording is much shorter when sampling is disabled, because it omits all of the JavaScript call stacks.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png" alt-text="Un exemple d’enregistrement lorsque les exemples de JS sont désactivés" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png":::
         <span data-ttu-id="88c0e-151">Un exemple d’enregistrement lorsque les exemples de JS sont désactivés</span><span class="sxs-lookup"><span data-stu-id="88c0e-151">An example of a recording when JS samples are disabled</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png" alt-text="Exemple d’enregistrement lorsque les exemples de JS sont activés" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png":::
         <span data-ttu-id="88c0e-153">Exemple d’enregistrement lorsque les exemples de JS sont activés</span><span class="sxs-lookup"><span data-stu-id="88c0e-153">An example of a recording when JS samples are enabled</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

### <span data-ttu-id="88c0e-154">Limiter le réseau lors de l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="88c0e-154">Throttle the network while recording</span></span>   

<span data-ttu-id="88c0e-155">Pour limiter le réseau lors de l’enregistrement:</span><span class="sxs-lookup"><span data-stu-id="88c0e-155">To throttle the network while recording:</span></span>  

1.  <span data-ttu-id="88c0e-156">Ouvrir le menu **paramètres de capture** .</span><span class="sxs-lookup"><span data-stu-id="88c0e-156">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="88c0e-157">Voir [afficher les paramètres d’enregistrement](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="88c0e-157">See [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="88c0e-158">Définissez **réseau** sur le niveau de limitation souhaité.</span><span class="sxs-lookup"><span data-stu-id="88c0e-158">Set **Network** to the desired level of throttling.</span></span>  
    
### <span data-ttu-id="88c0e-159">Limiter le processeur lors de l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="88c0e-159">Throttle the CPU while recording</span></span>   

<span data-ttu-id="88c0e-160">Pour limiter le processeur lors de l’enregistrement:</span><span class="sxs-lookup"><span data-stu-id="88c0e-160">To throttle the CPU while recording:</span></span>  

1.  <span data-ttu-id="88c0e-161">Ouvrir le menu **paramètres de capture** .</span><span class="sxs-lookup"><span data-stu-id="88c0e-161">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="88c0e-162">Voir [afficher les paramètres d’enregistrement](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="88c0e-162">See [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="88c0e-163">Définissez **UC** sur le niveau de limitation souhaité.</span><span class="sxs-lookup"><span data-stu-id="88c0e-163">Set **CPU** to the desired level of throttling.</span></span>  
    
<span data-ttu-id="88c0e-164">La limitation est relative aux fonctionnalités de votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="88c0e-164">Throttling is relative to the capabilities of your computer.</span></span>  <span data-ttu-id="88c0e-165">Par exemple, l’option **2x Slowdown** permet à votre processeur de fonctionner 2 fois plus lent que d’habitude.</span><span class="sxs-lookup"><span data-stu-id="88c0e-165">For example, the **2x slowdown** option makes your CPU operate 2 times slower than normal.</span></span>  <span data-ttu-id="88c0e-166">DevTools ne simulez pas vraiment les UC des appareils mobiles, car l’architecture des appareils mobiles est très différente de celle des ordinateurs de bureau et des ordinateurs portables.</span><span class="sxs-lookup"><span data-stu-id="88c0e-166">DevTools do not truly simulate the CPUs of mobile devices, because the architecture of mobile devices is very different from that of desktops and laptops.</span></span>  

### <span data-ttu-id="88c0e-167">Activer l’instrumentation avancée de peinture</span><span class="sxs-lookup"><span data-stu-id="88c0e-167">Enable advanced paint instrumentation</span></span>   

<span data-ttu-id="88c0e-168">Pour afficher une instrumentation détaillée de Paint:</span><span class="sxs-lookup"><span data-stu-id="88c0e-168">To view detailed paint instrumentation:</span></span>  

1.  <span data-ttu-id="88c0e-169">Ouvrir le menu **paramètres de capture** .</span><span class="sxs-lookup"><span data-stu-id="88c0e-169">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="88c0e-170">Voir [afficher les paramètres d’enregistrement](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="88c0e-170">See [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="88c0e-171">Cochez la case **activer l’instrumentation avancée de peinture (lente)** .</span><span class="sxs-lookup"><span data-stu-id="88c0e-171">Check the **Enable advanced paint instrumentation (slow)** checkbox.</span></span>  

<span data-ttu-id="88c0e-172">Pour plus d’informations sur l’interaction avec les informations de Paint, voir [afficher les couches](#view-layers-information) et afficher le [Générateur de profils Paint](#view-paint-profiler).</span><span class="sxs-lookup"><span data-stu-id="88c0e-172">To learn how to interact with the paint information, see [View layers](#view-layers-information) and [View paint profiler](#view-paint-profiler).</span></span>  

## <span data-ttu-id="88c0e-173">Enregistrer un enregistrement</span><span class="sxs-lookup"><span data-stu-id="88c0e-173">Save a recording</span></span>   

<span data-ttu-id="88c0e-174">Pour enregistrer un enregistrement, cliquez avec le bouton droit et sélectionnez **enregistrer le profil**.</span><span class="sxs-lookup"><span data-stu-id="88c0e-174">To save a recording, right-click and select **Save Profile**.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png" alt-text="Enregistrer le profil" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png":::
   **<span data-ttu-id="88c0e-176">Enregistrer le profil</span><span class="sxs-lookup"><span data-stu-id="88c0e-176">Save Profile</span></span>**  
:::image-end:::  

## <span data-ttu-id="88c0e-177">Charger un enregistrement</span><span class="sxs-lookup"><span data-stu-id="88c0e-177">Load a recording</span></span>   

<span data-ttu-id="88c0e-178">Pour charger un enregistrement, cliquez avec le bouton droit et sélectionnez **charger le profil**.</span><span class="sxs-lookup"><span data-stu-id="88c0e-178">To load a recording, right-click and select **Load Profile**.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png" alt-text="Profil de chargement" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png":::
   **<span data-ttu-id="88c0e-180">Profil de chargement</span><span class="sxs-lookup"><span data-stu-id="88c0e-180">Load Profile</span></span>**  
:::image-end:::  

## <span data-ttu-id="88c0e-181">Effacer l’enregistrement précédent</span><span class="sxs-lookup"><span data-stu-id="88c0e-181">Clear the previous recording</span></span>   

<span data-ttu-id="88c0e-182">Après avoir effectué un enregistrement, appuyez sur **effacer l’enregistrement** \ ( ![ effacer l’enregistrement ][ImageClearRecordingIcon] \) pour effacer cet enregistrement du panneau **performances** .</span><span class="sxs-lookup"><span data-stu-id="88c0e-182">After making a recording, press **Clear recording** \(![Clear recording][ImageClearRecordingIcon]\) to clear that recording from the **Performance** panel.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png" alt-text="Effacer l’enregistrement" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png":::
   **<span data-ttu-id="88c0e-184">Effacer l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="88c0e-184">Clear recording</span></span>**  
:::image-end:::  

## <span data-ttu-id="88c0e-185">Analyser un enregistrement de performance</span><span class="sxs-lookup"><span data-stu-id="88c0e-185">Analyze a performance recording</span></span>   

<span data-ttu-id="88c0e-186">Une fois que vous avez [enregistré des performances d’exécution](#record-runtime-performance) ou enregistré des performances de [chargement](#record-load-performance), le panneau **performance** fournit un grand nombre de données pour l’analyse des performances de ce qui s’est produit.</span><span class="sxs-lookup"><span data-stu-id="88c0e-186">After you [record runtime performance](#record-runtime-performance) or [record load performance](#record-load-performance), the **Performance** panel provides a lot of data for analyzing the performance of what just happened.</span></span>  

### <span data-ttu-id="88c0e-187">Sélectionner une partie d’un enregistrement</span><span class="sxs-lookup"><span data-stu-id="88c0e-187">Select a portion of a recording</span></span>   

<span data-ttu-id="88c0e-188">Faites glisser le pointeur de la souris vers la gauche ou la droite dans la **vue d’ensemble** pour sélectionner une partie d’un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="88c0e-188">Drag your mouse left or right across the **Overview** to select a portion of a recording.</span></span>  <span data-ttu-id="88c0e-189">La section **vue d’ensemble** contient les graphiques **fps**, **UC**et **net** .</span><span class="sxs-lookup"><span data-stu-id="88c0e-189">The **Overview** is the section that contains the **FPS**, **CPU**, and **NET** charts.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-zoom-highlighted.msft.png" alt-text="Faites glisser le pointeur de la souris sur la vue d’ensemble pour effectuer un zoom" lightbox="../media/evaluate-performance-performance-zoom-highlighted.msft.png":::
   <span data-ttu-id="88c0e-191">Faites glisser le pointeur de la souris sur la **vue d’ensemble** pour effectuer un zoom</span><span class="sxs-lookup"><span data-stu-id="88c0e-191">Drag the mouse across the **Overview** to zoom</span></span>  
:::image-end:::  

<span data-ttu-id="88c0e-192">Pour sélectionner une partie à l’aide du clavier:</span><span class="sxs-lookup"><span data-stu-id="88c0e-192">To select a portion using the keyboard:</span></span>  

1.  <span data-ttu-id="88c0e-193">Cliquez sur l’arrière-plan de la section **principale** ou de n’importe quelle section en regard de celle-ci, comme **interactions**, **réseau**ou **GPU**.</span><span class="sxs-lookup"><span data-stu-id="88c0e-193">Click on the background of the **Main** section, or any of the sections next to it, such as **Interactions**, **Network**, or **GPU**.</span></span>  <span data-ttu-id="88c0e-194">Ce flux de travail de clavier fonctionne uniquement lorsque l’une de ces sections est activée.</span><span class="sxs-lookup"><span data-stu-id="88c0e-194">This keyboard workflow only works when one of these sections is in focus.</span></span>  
1.  <span data-ttu-id="88c0e-195">Utilisez les `W` touches,,, `A` `S` `D` pour effectuer un zoom avant, vous déplacer vers la gauche, effectuer un zoom arrière et vous déplacer à droite, respectivement.</span><span class="sxs-lookup"><span data-stu-id="88c0e-195">Use the `W`, `A`, `S`, `D` keys to zoom in, move left, zoom out, and move right, respectively.</span></span>  

<span data-ttu-id="88c0e-196">Pour sélectionner une partie à l’aide d’une pavé tactile:</span><span class="sxs-lookup"><span data-stu-id="88c0e-196">To select a portion using a trackpad:</span></span>  

1.  <span data-ttu-id="88c0e-197">Positionnez le pointeur de la souris sur la section **Présentation** ou la section **Détails** .</span><span class="sxs-lookup"><span data-stu-id="88c0e-197">Hover your mouse over the **Overview** section or the **Details** section.</span></span>  <span data-ttu-id="88c0e-198">La section **vue d’ensemble** est la zone contenant les graphiques **fps**, **UC**et **net** .</span><span class="sxs-lookup"><span data-stu-id="88c0e-198">The **Overview** section is the area containing the **FPS**, **CPU**, and **NET** charts.</span></span>  <span data-ttu-id="88c0e-199">La section **Détails** représente la zone contenant la section **principale** , la section **interactions** , etc.</span><span class="sxs-lookup"><span data-stu-id="88c0e-199">The **Details** section is the area containing the **Main** section, the **Interactions** section, and so on.</span></span>  
1.  <span data-ttu-id="88c0e-200">Avec deux doigts, balayez vers le haut pour effectuer un zoom arrière, balayez vers la gauche pour vous déplacer vers la gauche, balayez vers le bas pour effectuer un zoom avant, puis balayez vers la droite pour avancer.</span><span class="sxs-lookup"><span data-stu-id="88c0e-200">Using two fingers, swipe up to zoom out, swipe left to move left, swipe down to zoom in, and swipe right to move right.</span></span>  

<span data-ttu-id="88c0e-201">Pour faire défiler un grand graphique en flamme dans la section **principale** ou sur l’un des voisins, cliquez et maintenez le bouton enfoncé tout en faisant glisser le curseur vers le haut et le bas.</span><span class="sxs-lookup"><span data-stu-id="88c0e-201">To scroll a long flame chart in the **Main** section or any of the neighbors, click and hold while dragging up and down.</span></span>  <span data-ttu-id="88c0e-202">Faites glisser vers la gauche et vers la droite pour déplacer la partie de l’enregistrement sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="88c0e-202">Drag left and right to move what portion of the recording is selected.</span></span>  

### <span data-ttu-id="88c0e-203">Activités de recherche</span><span class="sxs-lookup"><span data-stu-id="88c0e-203">Search activities</span></span>   

<span data-ttu-id="88c0e-204">`Control` + `F` `Command` + `F` Pour ouvrir la zone de recherche située en bas du panneau de **performance** , appuyez sur \ (Windows \) ou \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="88c0e-204">Press `Control`+`F` \(Windows\) or `Command`+`F` \(macOS\) to open the search box at the bottom of the **Performance** panel.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-search-regex.msft.png" alt-text="Zone de recherche" lightbox="../media/evaluate-performance-performance-search-regex.msft.png":::
   <span data-ttu-id="88c0e-206">Zone de recherche</span><span class="sxs-lookup"><span data-stu-id="88c0e-206">The search box</span></span>  
:::image-end:::  

<span data-ttu-id="88c0e-207">Pour parcourir les activités qui correspondent à votre requête:</span><span class="sxs-lookup"><span data-stu-id="88c0e-207">To navigate activities that match your query:</span></span>  

*   <span data-ttu-id="88c0e-208">Utilisez les boutons **précédent** \ ( ![ précédent ][ImagePreviousIcon] \) et **suivant** \ ( ![ suivant ][ImageNextIcon] \).</span><span class="sxs-lookup"><span data-stu-id="88c0e-208">Use the **Previous** \(![Previous][ImagePreviousIcon]\) and **Next** \(![Next][ImageNextIcon]\) buttons.</span></span>  
*   <span data-ttu-id="88c0e-209">Appuyez `Shift` + `Enter` pour sélectionner le précédent ou `Enter` pour en sélectionner un autre.</span><span class="sxs-lookup"><span data-stu-id="88c0e-209">Press `Shift`+`Enter` to select the previous or `Enter` to select the next.</span></span>  

<span data-ttu-id="88c0e-210">Pour modifier les paramètres d’une requête:</span><span class="sxs-lookup"><span data-stu-id="88c0e-210">To modify query settings:</span></span>  

*   <span data-ttu-id="88c0e-211">Appuyer sur respecter la **casse** (respecter la casse ![ ][ImageSearchCaseIcon] ) pour respecter la casse.</span><span class="sxs-lookup"><span data-stu-id="88c0e-211">Press **Case sensitive** \(![Case sensitive][ImageSearchCaseIcon]\) to make the query case sensitive.</span></span>  
*   <span data-ttu-id="88c0e-212">**Regex** ![ ][ImageSearchRegexIcon] Pour utiliser une expression régulière dans votre requête, appuyez sur Regex.</span><span class="sxs-lookup"><span data-stu-id="88c0e-212">Press **Regex** \(![Regex][ImageSearchRegexIcon]\) to use a regular expression in your query.</span></span>  

<span data-ttu-id="88c0e-213">Pour masquer la zone de recherche, appuyez sur **Annuler**.</span><span class="sxs-lookup"><span data-stu-id="88c0e-213">To hide the search box, press **Cancel**.</span></span>  

### <span data-ttu-id="88c0e-214">Afficher l’activité du thread principal</span><span class="sxs-lookup"><span data-stu-id="88c0e-214">View main thread activity</span></span>   

<span data-ttu-id="88c0e-215">Utilisez la section **principale** pour afficher l’activité qui s’est produite sur le thread principal de la page.</span><span class="sxs-lookup"><span data-stu-id="88c0e-215">Use the **Main** section to view activity that occurred on the main thread of the page.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-main-zoomed.msft.png" alt-text="Section principale" lightbox="../media/evaluate-performance-performance-main-zoomed.msft.png":::
   <span data-ttu-id="88c0e-217">Section **principale**</span><span class="sxs-lookup"><span data-stu-id="88c0e-217">The **Main** section</span></span>  
:::image-end:::  

<span data-ttu-id="88c0e-218">Cliquez sur un événement pour afficher des informations supplémentaires le concernant sous l’onglet **Résumé** .  DevTools souligne l’événement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="88c0e-218">Click on an event to view more information about it in the **Summary** tab.  DevTools outlines the selected event.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-summary-me.msft.png" alt-text="Plus d’informations sur la fonction anonyme sous l’onglet Résumé" lightbox="../media/evaluate-performance-performance-summary-me.msft.png":::
   <span data-ttu-id="88c0e-220">Plus d’informations sur la `anonymous` fonction sous l’onglet **Résumé**</span><span class="sxs-lookup"><span data-stu-id="88c0e-220">More information about the `anonymous` function in the **Summary** tab</span></span>  
:::image-end:::  

<span data-ttu-id="88c0e-221">DevTools représente l’activité du thread principal avec un graphique à flamme.</span><span class="sxs-lookup"><span data-stu-id="88c0e-221">DevTools represents main thread activity with a flame chart.</span></span>  <span data-ttu-id="88c0e-222">L’axe x représente l’enregistrement dans le temps.</span><span class="sxs-lookup"><span data-stu-id="88c0e-222">The x-axis represents the recording over time.</span></span>  <span data-ttu-id="88c0e-223">L’axe y représente la pile d’appels.</span><span class="sxs-lookup"><span data-stu-id="88c0e-223">The y-axis represents the call stack.</span></span>  <span data-ttu-id="88c0e-224">Les événements en haut déclenchent les événements situés au-dessous.</span><span class="sxs-lookup"><span data-stu-id="88c0e-224">The events on top cause the events below it.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-main-flame-chart.msft.png" alt-text="Un graphique en flamme" lightbox="../media/evaluate-performance-performance-main-flame-chart.msft.png":::
   <span data-ttu-id="88c0e-226">Un graphique en flamme</span><span class="sxs-lookup"><span data-stu-id="88c0e-226">A flame chart</span></span>  
:::image-end:::  

<span data-ttu-id="88c0e-227">Dans l’illustration précédente, un `click` événement a entraîné `Function Call` une `activitytabs.js` 53 sur ligne.</span><span class="sxs-lookup"><span data-stu-id="88c0e-227">In the previous figure, a `click` event caused a `Function Call` in `activitytabs.js` on line 53.</span></span>  <span data-ttu-id="88c0e-228">`Function Call`Vous pouvez voir ci-dessous qu’une fonction anonyme a été appelée.</span><span class="sxs-lookup"><span data-stu-id="88c0e-228">Below `Function Call` you see that an anonymous function was called.</span></span>  <span data-ttu-id="88c0e-229">Fonction anonyme appelée, qui a été appelée `a` `wait` `Minor GC` .</span><span class="sxs-lookup"><span data-stu-id="88c0e-229">The anonymous function called `a`, which called `wait`, which called `Minor GC`.</span></span>  

<span data-ttu-id="88c0e-230">DevTools attribue des couleurs aléatoires aux scripts.</span><span class="sxs-lookup"><span data-stu-id="88c0e-230">DevTools assigns scripts random colors.</span></span>  <span data-ttu-id="88c0e-231">Dans la figure ci-dessus, les appels de fonction à partir d’un script apparaissent en vert clair.</span><span class="sxs-lookup"><span data-stu-id="88c0e-231">In the previous figure, function calls from one script are colored light green.</span></span>  <span data-ttu-id="88c0e-232">Les appels d’un autre script sont de couleur beige.</span><span class="sxs-lookup"><span data-stu-id="88c0e-232">Calls from another script are colored beige.</span></span>  <span data-ttu-id="88c0e-233">Le jaune foncé représente l’activité de création de scripts et l’événement violet représente l’activité de rendu.</span><span class="sxs-lookup"><span data-stu-id="88c0e-233">The darker yellow represents scripting activity, and the purple event represents rendering activity.</span></span>  <span data-ttu-id="88c0e-234">Ces événements en jaune et violet plus foncés sont cohérents dans tous les enregistrements.</span><span class="sxs-lookup"><span data-stu-id="88c0e-234">These darker yellow and purple events are consistent across all recordings.</span></span>  

<span data-ttu-id="88c0e-235">Pour masquer le graphique de flamme d’appels JavaScript, voir [Désactiver les exemples JavaScript](#disable-javascript-samples) .</span><span class="sxs-lookup"><span data-stu-id="88c0e-235">See [Disable JavaScript samples](#disable-javascript-samples) if you want to hide the detailed flame chart of JavaScript calls.</span></span>  <span data-ttu-id="88c0e-236">Lorsque les exemples de JS sont désactivés, vous ne voyez que les événements de niveau supérieur, comme `Event: click` et `Function Call` de la figure précédente.</span><span class="sxs-lookup"><span data-stu-id="88c0e-236">When JS samples are disabled, you only see high-level events such as `Event: click` and `Function Call` from the previous figure.</span></span>  

### <span data-ttu-id="88c0e-237">Afficher les activités d’un tableau</span><span class="sxs-lookup"><span data-stu-id="88c0e-237">View activities in a table</span></span>   

<span data-ttu-id="88c0e-238">Après avoir enregistré une page, il n’est pas nécessaire de dépendre uniquement de la section **principale** permettant d’analyser les activités.</span><span class="sxs-lookup"><span data-stu-id="88c0e-238">After recording a page, you do not need to rely solely on the **Main** section to analyze activities.</span></span>  <span data-ttu-id="88c0e-239">DevTools fournit également trois vues tabulaires pour l’analyse des activités.</span><span class="sxs-lookup"><span data-stu-id="88c0e-239">DevTools also provides three tabular views for analyzing activities.</span></span>  <span data-ttu-id="88c0e-240">Chaque affichage vous offre une perspective différente des activités:</span><span class="sxs-lookup"><span data-stu-id="88c0e-240">Each view gives you a different perspective on the activities:</span></span>  

*   <span data-ttu-id="88c0e-241">Pour afficher les activités racines qui génèrent le plus de tâches, utilisez [l’onglet arborescence des appels](#the-call-tree-tab).</span><span class="sxs-lookup"><span data-stu-id="88c0e-241">When you want to view the root activities that cause the most work, use [the Call Tree tab](#the-call-tree-tab).</span></span>  
*   <span data-ttu-id="88c0e-242">Pour afficher les activités pour lesquelles le plus de temps est passé directement, utilisez [l’onglet inférieur](#the-bottom-up-tab).</span><span class="sxs-lookup"><span data-stu-id="88c0e-242">When you want to view the activities where the most time was directly spent, use [the Bottom-Up tab](#the-bottom-up-tab).</span></span>  
*   <span data-ttu-id="88c0e-243">Si vous voulez afficher les activités dans l’ordre dans lequel elles se sont produites lors de l’enregistrement, utilisez [l’onglet journal des événements](#the-event-log-tab).</span><span class="sxs-lookup"><span data-stu-id="88c0e-243">When you want to view the activities in the order in which they occurred during the recording, use [the Event Log tab](#the-event-log-tab).</span></span>  
    
> [!NOTE]
> <span data-ttu-id="88c0e-244">Les trois sections suivantes se réfèrent à la même démonstration.</span><span class="sxs-lookup"><span data-stu-id="88c0e-244">The next three sections all refer to the same demo.</span></span>  <span data-ttu-id="88c0e-245">Exécutez la démonstration vous-même dans les [onglets activité][ActivityTabsDemo].</span><span class="sxs-lookup"><span data-stu-id="88c0e-245">Run the demo yourself at [Activity Tabs Demo][ActivityTabsDemo].</span></span>  

#### <span data-ttu-id="88c0e-246">Activités racines</span><span class="sxs-lookup"><span data-stu-id="88c0e-246">Root activities</span></span>   

<span data-ttu-id="88c0e-247">Voici une description du concept d' **activités racines** mentionné dans les sections de l’onglet **arborescence des appels** , de **bas en haut** et **Journal des événements** .</span><span class="sxs-lookup"><span data-stu-id="88c0e-247">Here is an explanation of the **root activities** concept that is mentioned in the **Call Tree** tab, **Bottom-Up** tab, and **Event Log** sections.</span></span>  

<span data-ttu-id="88c0e-248">Les activités racines peuvent entraîner le fonctionnement du navigateur.</span><span class="sxs-lookup"><span data-stu-id="88c0e-248">Root activities are those which cause the browser to do some work.</span></span>  <span data-ttu-id="88c0e-249">Par exemple, lorsque vous cliquez sur une page, le navigateur déclenche une `Event` activité en tant qu’activité racine.</span><span class="sxs-lookup"><span data-stu-id="88c0e-249">For example, when you click a page, the browser fires an `Event` activity as the root activity.</span></span>  <span data-ttu-id="88c0e-250">Cela `Event` peut entraîner l’exécution d’un gestionnaire et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="88c0e-250">That `Event` might cause a handler to run, and so on.</span></span>  

<span data-ttu-id="88c0e-251">Dans le graphique en flamme de la section **principale** , les activités racines se trouvent en haut du graphique.</span><span class="sxs-lookup"><span data-stu-id="88c0e-251">In the flame chart of the **Main** section, root activities are at the top of the chart.</span></span>  <span data-ttu-id="88c0e-252">Dans les onglets **arborescence des appels** et **Journal des événements** , les activités racines sont les éléments de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="88c0e-252">In the **Call Tree** and **Event Log** tabs, root activities are the top-level items.</span></span>  

<span data-ttu-id="88c0e-253">Voir [l’onglet arborescence des appels](#the-call-tree-tab) pour obtenir un exemple d’activités racines.</span><span class="sxs-lookup"><span data-stu-id="88c0e-253">See [The Call Tree tab](#the-call-tree-tab) for an example of root activities.</span></span>  

#### <span data-ttu-id="88c0e-254">Onglet arborescence des appels</span><span class="sxs-lookup"><span data-stu-id="88c0e-254">The Call Tree tab</span></span>   

<span data-ttu-id="88c0e-255">Utilisez l’onglet **arborescence des appels** pour afficher les [activités racines](#root-activities) qui sont à l’origine du problème.</span><span class="sxs-lookup"><span data-stu-id="88c0e-255">Use the **Call Tree** tab to view which [root activities](#root-activities) cause the most work.</span></span>  

<span data-ttu-id="88c0e-256">L’onglet **arborescence des appels** affiche uniquement les activités effectuées au cours de la partie sélectionnée de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="88c0e-256">The **Call Tree** tab only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="88c0e-257">Pour plus d’informations sur la sélection de parties, voir [Sélectionner une portion d’un enregistrement](#select-a-portion-of-a-recording) .</span><span class="sxs-lookup"><span data-stu-id="88c0e-257">See [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-call-tree.msft.png" alt-text="Onglet arborescence des appels" lightbox="../media/evaluate-performance-performance-call-tree.msft.png":::
   <span data-ttu-id="88c0e-259">Onglet **arborescence des appels**</span><span class="sxs-lookup"><span data-stu-id="88c0e-259">The **Call Tree** tab</span></span>  
:::image-end:::  

<span data-ttu-id="88c0e-260">Dans l’illustration précédente, le niveau supérieur des éléments de la colonne **Activity** , par exemple, `Evaluate Script` les `Parse HTML` activités racines.</span><span class="sxs-lookup"><span data-stu-id="88c0e-260">In the previous figure, the top-level of items in the **Activity** column, such as `Evaluate Script` and `Parse HTML` are root activities.</span></span>  <span data-ttu-id="88c0e-261">L’imbrication représente la pile d’appels.</span><span class="sxs-lookup"><span data-stu-id="88c0e-261">The nesting represents the call stack.</span></span>  <span data-ttu-id="88c0e-262">Par exemple, dans l’illustration précédente, `Parse HTML` ce qui a provoqué `Evaluate Script` `Compile Script` et `(anonymous)` .</span><span class="sxs-lookup"><span data-stu-id="88c0e-262">For example, in the previous figure, `Parse HTML` which caused `Evaluate Script` which caused `Compile Script` and `(anonymous)`.</span></span>  

<span data-ttu-id="88c0e-263">Le **temps libre** représente le temps passé directement dans cette activité.</span><span class="sxs-lookup"><span data-stu-id="88c0e-263">**Self Time** represents the time directly spent in that activity.</span></span>  <span data-ttu-id="88c0e-264">**Durée totale** représente le temps passé à cette activité ou à un des enfants.</span><span class="sxs-lookup"><span data-stu-id="88c0e-264">**Total Time** represents the time spent in that activity or any of the children.</span></span>  

<span data-ttu-id="88c0e-265">Cliquez sur **durée automatique**, **durée totale**ou **activité** pour trier le tableau selon la colonne.</span><span class="sxs-lookup"><span data-stu-id="88c0e-265">Click **Self Time**, **Total Time**, or **Activity** to sort the table by that column.</span></span>  

<span data-ttu-id="88c0e-266">Utilisez la zone de texte **filtre** pour filtrer les événements par nom d’activité.</span><span class="sxs-lookup"><span data-stu-id="88c0e-266">Use the **Filter** text box to filter events by activity name.</span></span>  

<span data-ttu-id="88c0e-267">Par défaut, le menu de **regroupement** a la valeur **aucun regroupement**.</span><span class="sxs-lookup"><span data-stu-id="88c0e-267">By default the **Grouping** menu is set to **No Grouping**.</span></span>  <span data-ttu-id="88c0e-268">Utilisez le menu de **regroupement** pour trier la table d’activité en fonction de différents critères.</span><span class="sxs-lookup"><span data-stu-id="88c0e-268">Use the **Grouping** menu to sort the activity table based on various criteria.</span></span>  

<span data-ttu-id="88c0e-269">Pour **Show Heaviest Stack** afficher ![ ][ImageShowHeaviestStackIcon] une autre table à droite de la table **Activity** , cliquez sur Afficher la pile la plus lourde.</span><span class="sxs-lookup"><span data-stu-id="88c0e-269">Click **Show Heaviest Stack** \(![Show Heaviest Stack][ImageShowHeaviestStackIcon]\) to reveal another table to the right of the **Activity** table.</span></span>  <span data-ttu-id="88c0e-270">Cliquez sur une activité pour remplir la table de pile la plus **lourde** .</span><span class="sxs-lookup"><span data-stu-id="88c0e-270">Click on an activity to populate the **Heaviest Stack** table.</span></span>  <span data-ttu-id="88c0e-271">La table des piles les plus **lourdes** vous indique les enfants de l’activité sélectionnée qui prenaient le plus de temps à s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="88c0e-271">The **Heaviest Stack** table shows you which children of the selected activity took the longest time to run.</span></span>  

#### <span data-ttu-id="88c0e-272">Onglet inférieur</span><span class="sxs-lookup"><span data-stu-id="88c0e-272">The Bottom-Up tab</span></span>   

<span data-ttu-id="88c0e-273">Utilisez l’onglet **inférieur** pour afficher les activités qui consomment directement le plus de temps dans l’agrégat.</span><span class="sxs-lookup"><span data-stu-id="88c0e-273">Use the **Bottom-Up** tab to view which activities directly took up the most time in aggregate.</span></span>  

<span data-ttu-id="88c0e-274">L’onglet **inférieur** affiche uniquement les activités effectuées au cours de la partie sélectionnée de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="88c0e-274">The **Bottom-Up** tab only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="88c0e-275">Pour plus d’informations sur la sélection de parties, voir [Sélectionner une portion d’un enregistrement](#select-a-portion-of-a-recording) .</span><span class="sxs-lookup"><span data-stu-id="88c0e-275">See [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-bottoms-up.msft.png" alt-text="Onglet inférieur" lightbox="../media/evaluate-performance-performance-bottoms-up.msft.png":::
   <span data-ttu-id="88c0e-277">Onglet **inférieur**</span><span class="sxs-lookup"><span data-stu-id="88c0e-277">The **Bottom-Up** tab</span></span>  
:::image-end:::  

<span data-ttu-id="88c0e-278">Dans le graphique en forme de flamme **de la figure** précédente, vous pouvez voir que presque tout le temps est passé en temps `Parse HTML` .</span><span class="sxs-lookup"><span data-stu-id="88c0e-278">In the **Main** section flame chart of the previous figure, see that almost practically all of the time was spent running `Parse HTML`.</span></span>  <span data-ttu-id="88c0e-279">Dans l’onglet **inférieur** de la figure précédente, l’activité supérieure `Parse HTML` .</span><span class="sxs-lookup"><span data-stu-id="88c0e-279">The top activity in the **Bottom-Up** tab of the previous figure is `Parse HTML`.</span></span>  <!--In the flame chart of the previous figure, the yellow below the calls to `wait` are actually thousands of `Minor GC` calls.  -->  <span data-ttu-id="88c0e-280">Reportez-vous à la rubrique dans l’onglet en **bas** , l’activité la plus coûteuse suivante `Layout` .</span><span class="sxs-lookup"><span data-stu-id="88c0e-280">See in the **Bottom-Up** tab, the next most expensive activity is `Layout`.</span></span>  

<span data-ttu-id="88c0e-281">La colonne de **temps libre** représente le temps agrégé passé directement dans cette activité, sur l’ensemble des occurrences.</span><span class="sxs-lookup"><span data-stu-id="88c0e-281">The **Self Time** column represents the aggregated time spent directly in that activity, across all of the occurrences.</span></span>  

<span data-ttu-id="88c0e-282">La colonne **temps total** représente le temps agrégé dépensé dans cette activité ou sur n’importe quel enfant.</span><span class="sxs-lookup"><span data-stu-id="88c0e-282">The **Total Time** column represents aggregated time spent in that activity or any of the children.</span></span>  

#### <span data-ttu-id="88c0e-283">Onglet journal des événements</span><span class="sxs-lookup"><span data-stu-id="88c0e-283">The Event Log tab</span></span>   

<span data-ttu-id="88c0e-284">Utilisez l’onglet **Journal des événements** pour afficher les activités dans l’ordre dans lequel elles se sont produites lors de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="88c0e-284">Use the **Event Log** tab to view activities in the order in which they occurred during the recording.</span></span>  

<span data-ttu-id="88c0e-285">L’onglet **Journal des événements** affiche uniquement les activités effectuées au cours de la partie sélectionnée de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="88c0e-285">The **Event Log** tab only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="88c0e-286">Pour plus d’informations sur la sélection de parties, voir [Sélectionner une portion d’un enregistrement](#select-a-portion-of-a-recording) .</span><span class="sxs-lookup"><span data-stu-id="88c0e-286">See [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-event-log.msft.png" alt-text="Onglet journal des événements" lightbox="../media/evaluate-performance-performance-event-log.msft.png":::
   <span data-ttu-id="88c0e-288">Onglet **Journal des événements**</span><span class="sxs-lookup"><span data-stu-id="88c0e-288">The **Event Log** tab</span></span>  
:::image-end:::  

<span data-ttu-id="88c0e-289">La colonne **heure de début** représente le point auquel cette activité a commencé, par rapport au début de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="88c0e-289">The **Start Time** column represents the point at which that activity started, relative to the start of the recording.</span></span>  <span data-ttu-id="88c0e-290">Par exemple, l’heure de début de `175.7 ms` l’élément sélectionné dans la figure précédente signifie que l’activité a démarré 175,7 ms après le début de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="88c0e-290">For example, the start time of `175.7 ms` for the selected item in the previous figure means that activity started 175.7 ms after the recording started.</span></span>  

<span data-ttu-id="88c0e-291">La colonne **temps libre** représente le temps passé directement dans cette activité.</span><span class="sxs-lookup"><span data-stu-id="88c0e-291">The **Self Time** column represents the time spent directly in that activity.</span></span>  

<span data-ttu-id="88c0e-292">Le **nombre total** de colonnes durée représente le temps passé directement dans cette activité ou dans n’importe quel enfant.</span><span class="sxs-lookup"><span data-stu-id="88c0e-292">The **Total Time** columns represents time spent directly in that activity or in any of the children.</span></span>  

<span data-ttu-id="88c0e-293">Cliquez sur **heure de début**, **durée automatique**ou **durée totale** pour trier le tableau selon la colonne.</span><span class="sxs-lookup"><span data-stu-id="88c0e-293">Click **Start Time**, **Self Time**, or **Total Time** to sort the table by that column.</span></span>

<span data-ttu-id="88c0e-294">Utilisez la zone de texte **filtre** pour filtrer les activités par nom.</span><span class="sxs-lookup"><span data-stu-id="88c0e-294">Use the **Filter** text box to filter activities by name.</span></span>  

<span data-ttu-id="88c0e-295">Utilisez le menu **durée** pour filtrer les activités ayant eu moins de 1 ms ou 15 ms.</span><span class="sxs-lookup"><span data-stu-id="88c0e-295">Use the **Duration** menu to filter out any activities that took less than 1 ms or 15 ms.</span></span>  <span data-ttu-id="88c0e-296">Par défaut, le menu **durée** est défini sur **tout**, ce qui signifie que toutes les activités sont affichées.</span><span class="sxs-lookup"><span data-stu-id="88c0e-296">By default the **Duration** menu is set to **All**, meaning all activities are shown.</span></span>  

<span data-ttu-id="88c0e-297">Désactivez les cases à cocher **chargement**, **script**, **rendu**ou **peinture** pour filtrer toutes les activités de ces catégories.</span><span class="sxs-lookup"><span data-stu-id="88c0e-297">Disable the **Loading**, **Scripting**, **Rendering**, or **Painting** checkboxes to filter out all activities from those categories.</span></span>  

### <span data-ttu-id="88c0e-298">Afficher l’activité GPU</span><span class="sxs-lookup"><span data-stu-id="88c0e-298">View GPU activity</span></span>   

<span data-ttu-id="88c0e-299">Afficher l’activité GPU dans la section **GPU** .</span><span class="sxs-lookup"><span data-stu-id="88c0e-299">View GPU activity in the **GPU** section.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-gpu-zoomed.msft.png" alt-text="Section GPU" lightbox="../media/evaluate-performance-performance-gpu-zoomed.msft.png":::
   <span data-ttu-id="88c0e-301">Section **GPU**</span><span class="sxs-lookup"><span data-stu-id="88c0e-301">The **GPU** section</span></span>  
:::image-end:::  

### <span data-ttu-id="88c0e-302">Afficher les activités pixellisées</span><span class="sxs-lookup"><span data-stu-id="88c0e-302">View raster activity</span></span>   

<span data-ttu-id="88c0e-303">Affichez les activités pixellisées dans la section **Raster** .</span><span class="sxs-lookup"><span data-stu-id="88c0e-303">View raster activity in the **Raster** section.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-raster.msft.png" alt-text="Section raster" lightbox="../media/evaluate-performance-performance-raster.msft.png":::
   <span data-ttu-id="88c0e-305">Section **Raster**</span><span class="sxs-lookup"><span data-stu-id="88c0e-305">The **Raster** section</span></span>  
:::image-end:::  

### <span data-ttu-id="88c0e-306">Afficher les interactions</span><span class="sxs-lookup"><span data-stu-id="88c0e-306">View interactions</span></span>   

<span data-ttu-id="88c0e-307">Utilisez la section **interactions** pour rechercher et analyser les interactions utilisateur qui se sont produites lors de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="88c0e-307">Use the **Interactions** section to find and analyze user interactions that happened during the recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-interactions-animation.msft.png" alt-text="Section interactions" lightbox="../media/evaluate-performance-performance-interactions-animation.msft.png":::
   <span data-ttu-id="88c0e-309">Section **interactions**</span><span class="sxs-lookup"><span data-stu-id="88c0e-309">The **Interactions** section</span></span>  
:::image-end:::  

<span data-ttu-id="88c0e-310">Une ligne rouge en bas d’une interaction représente le temps passé à attendre le thread principal.</span><span class="sxs-lookup"><span data-stu-id="88c0e-310">A red line at the bottom of an interaction represents time spent waiting for the main thread.</span></span>  

<span data-ttu-id="88c0e-311">Cliquez sur une interaction pour afficher davantage d’informations sur celle-ci sous l’onglet **Résumé** .</span><span class="sxs-lookup"><span data-stu-id="88c0e-311">Click an interaction to view more information about it in the **Summary** tab.</span></span>  

### <span data-ttu-id="88c0e-312">Analyser les images par seconde (FPS)</span><span class="sxs-lookup"><span data-stu-id="88c0e-312">Analyze frames per second (FPS)</span></span>   

<span data-ttu-id="88c0e-313">DevTools offre de nombreuses façons d’analyser les images par seconde:</span><span class="sxs-lookup"><span data-stu-id="88c0e-313">DevTools provides numerous ways to analyze frames per second:</span></span>  

*   <span data-ttu-id="88c0e-314">Utilisez [le graphique fps](#the-fps-chart) pour obtenir une vue d’ensemble des images par seconde au fil de la durée de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="88c0e-314">Use [the FPS chart](#the-fps-chart) to get an overview of FPS over the duration of the recording.</span></span>  
*   <span data-ttu-id="88c0e-315">Utilisez [la section cadres](#the-frames-section) pour afficher la durée d’une image particulière.</span><span class="sxs-lookup"><span data-stu-id="88c0e-315">Use [the Frames section](#the-frames-section) to view how long a particular frame took.</span></span>  
*   <span data-ttu-id="88c0e-316">Utilisez le **compteur fps** pour une estimation en temps réel de FPS lors de l’exécution de la page.</span><span class="sxs-lookup"><span data-stu-id="88c0e-316">Use the **FPS meter** for a realtime estimate of FPS as the page runs.</span></span>  <span data-ttu-id="88c0e-317">Voir [trames d’affichage par seconde en temps réel avec le compteur fps](#view-frames-per-second-in-realtime-with-the-fps-meter).</span><span class="sxs-lookup"><span data-stu-id="88c0e-317">See [View frames per second in realtime with the FPS meter](#view-frames-per-second-in-realtime-with-the-fps-meter).</span></span>  
    
#### <span data-ttu-id="88c0e-318">Graphique FPS</span><span class="sxs-lookup"><span data-stu-id="88c0e-318">The FPS chart</span></span>   

<span data-ttu-id="88c0e-319">Le graphique **fps** fournit une vue d’ensemble de la fréquence d’images sur la durée d’un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="88c0e-319">The **FPS** chart provides an overview of the frame rate across the duration of a recording.</span></span>  <span data-ttu-id="88c0e-320">En règle générale, plus la barre verte est élevée, plus la fréquence d’images est élevée.</span><span class="sxs-lookup"><span data-stu-id="88c0e-320">In general, the higher the green bar, the better the frame rate.</span></span>  

<span data-ttu-id="88c0e-321">Une barre rouge au-dessus du graphique **fps** est une alerte indiquant que le taux d’images a été interrompu comme faible et qu’il a probablement été lésé par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="88c0e-321">A red bar above the **FPS** chart is a warning that the frame rate dropped so low that it probably harmed the user's experience.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-fps-highlight.msft.png" alt-text="Graphique FPS" lightbox="../media/evaluate-performance-performance-fps-highlight.msft.png":::
   <span data-ttu-id="88c0e-323">Graphique **fps**</span><span class="sxs-lookup"><span data-stu-id="88c0e-323">The **FPS** chart</span></span>  
:::image-end:::  

#### <span data-ttu-id="88c0e-324">Section cadres</span><span class="sxs-lookup"><span data-stu-id="88c0e-324">The Frames section</span></span>   

<span data-ttu-id="88c0e-325">La section **trames** vous indique exactement le temps qu’une image donnée a duré.</span><span class="sxs-lookup"><span data-stu-id="88c0e-325">The **Frames** section tells you exactly how long a particular frame took.</span></span>  

<span data-ttu-id="88c0e-326">Pointez sur un cadre pour afficher une info-bulle contenant des informations supplémentaires à son sujet.</span><span class="sxs-lookup"><span data-stu-id="88c0e-326">Hover over a frame to view a tooltip with more information about it.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-frames-hover.msft.png" alt-text="Survol d’un cadre" lightbox="../media/evaluate-performance-performance-frames-hover.msft.png":::
   <span data-ttu-id="88c0e-328">Survol d’un cadre</span><span class="sxs-lookup"><span data-stu-id="88c0e-328">Hover over a frame</span></span>  
:::image-end:::  

<span data-ttu-id="88c0e-329">Cliquez sur un cadre pour afficher encore plus d’informations sur le cadre sous l’onglet **Résumé** .  DevTools plan le cadre sélectionné en bleu.</span><span class="sxs-lookup"><span data-stu-id="88c0e-329">Click on a frame to view even more information about the frame in the **Summary** tab.  DevTools outlines the selected frame in blue.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-frames-summary.msft.png" alt-text="Afficher un cadre sous l’onglet Résumé" lightbox="../media/evaluate-performance-performance-frames-summary.msft.png":::
   <span data-ttu-id="88c0e-331">Afficher un cadre sous l’onglet **Résumé**</span><span class="sxs-lookup"><span data-stu-id="88c0e-331">View a frame in the **Summary** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="88c0e-332">Afficher les requêtes réseau</span><span class="sxs-lookup"><span data-stu-id="88c0e-332">View network requests</span></span>   

<span data-ttu-id="88c0e-333">Développez la section **réseau** pour afficher une cascade de requêtes réseau qui se sont produites lors de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="88c0e-333">Expand the **Network** section to view a waterfall of network requests that occurred during the recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-network.msft.png" alt-text="Section réseau" lightbox="../media/evaluate-performance-performance-network.msft.png":::
   <span data-ttu-id="88c0e-335">Section **réseau**</span><span class="sxs-lookup"><span data-stu-id="88c0e-335">The **Network** section</span></span>  
:::image-end:::  

<span data-ttu-id="88c0e-336">Les requêtes sont codées en couleur comme suit:</span><span class="sxs-lookup"><span data-stu-id="88c0e-336">Requests are color-coded as follows:</span></span>  

*   <span data-ttu-id="88c0e-337">HTML: bleu</span><span class="sxs-lookup"><span data-stu-id="88c0e-337">HTML: Blue</span></span>  
*   <span data-ttu-id="88c0e-338">CSS: pourpre</span><span class="sxs-lookup"><span data-stu-id="88c0e-338">CSS: Purple</span></span>  
*   <span data-ttu-id="88c0e-339">JS: jaune</span><span class="sxs-lookup"><span data-stu-id="88c0e-339">JS: Yellow</span></span>  
*   <span data-ttu-id="88c0e-340">Images: vert</span><span class="sxs-lookup"><span data-stu-id="88c0e-340">Images: Green</span></span>  
    
<span data-ttu-id="88c0e-341">Cliquez sur une demande pour afficher davantage d’informations sur celle-ci sous l’onglet **Résumé** .  Par exemple, dans l’illustration précédente, l’onglet **Résumé** affiche des informations supplémentaires sur la requête bleue sélectionnée dans la section **réseau** .</span><span class="sxs-lookup"><span data-stu-id="88c0e-341">Click on a request to view more information about it in the **Summary** tab.  For example, in the previous figure, the **Summary** tab is displaying more information about the blue request that is selected in the **Network** section.</span></span>  

<span data-ttu-id="88c0e-342">Dans le coin supérieur gauche d’une demande, un carré plus foncé est une demande de priorité élevée.</span><span class="sxs-lookup"><span data-stu-id="88c0e-342">A darker-blue square in the top-left of a request means it is a higher-priority request.</span></span>  <span data-ttu-id="88c0e-343">Le carré bleu plus clair correspond à un niveau de priorité inférieur.</span><span class="sxs-lookup"><span data-stu-id="88c0e-343">A lighter-blue square means lower-priority.</span></span>  <span data-ttu-id="88c0e-344">Par exemple, dans l’illustration précédente, la requête bleue, sélectionnée est d’une priorité plus élevée et celle du vert au-dessous, de priorité inférieure.</span><span class="sxs-lookup"><span data-stu-id="88c0e-344">For example, in the previous figure, the blue, selected request is higher-priority, and the green one below it is lower-priority.</span></span>  

<span data-ttu-id="88c0e-345">Dans le 1er des figures suivantes, la requête pour `www.bing.com` est représentée par une ligne située sur la gauche, une barre au milieu avec une partie sombre et une partie claire, et une ligne à droite.</span><span class="sxs-lookup"><span data-stu-id="88c0e-345">In the 1st of the following figures, the request for `www.bing.com` is represented by a line on the left, a bar in the middle with a dark portion and a light portion, and a line on the right.</span></span>  <span data-ttu-id="88c0e-346">Dans la deuxième des figures suivantes, la représentation correspondante de la même demande apparaît dans l’onglet **minutage** du panneau **réseau** .</span><span class="sxs-lookup"><span data-stu-id="88c0e-346">In the 2nd of the following figures shows the corresponding representation of the same request in the **Timing** tab of the **Network** panel.</span></span>  <span data-ttu-id="88c0e-347">Voici à quoi correspondent les deux représentations suivantes:</span><span class="sxs-lookup"><span data-stu-id="88c0e-347">Here is how these two representations map to each other:</span></span>

*   <span data-ttu-id="88c0e-348">La ligne gauche représente tout ce qui concerne le `Connection Start` groupe d’événements compris.</span><span class="sxs-lookup"><span data-stu-id="88c0e-348">The left line is everything up to the `Connection Start` group of events, inclusive.</span></span>  <span data-ttu-id="88c0e-349">En d’autres termes, il s’agit de tout ce qui est auparavant `Request Sent` , exclusif.</span><span class="sxs-lookup"><span data-stu-id="88c0e-349">In other words, it is everything before `Request Sent`, exclusive.</span></span>  
*   <span data-ttu-id="88c0e-350">La partie claire de la barre est `Request Sent` et `Waiting (TTFB)` .</span><span class="sxs-lookup"><span data-stu-id="88c0e-350">The light portion of the bar is `Request Sent` and `Waiting (TTFB)`.</span></span>  
*   <span data-ttu-id="88c0e-351">La partie sombre de la barre est `Content Download` .</span><span class="sxs-lookup"><span data-stu-id="88c0e-351">The dark portion of the bar is `Content Download`.</span></span>  
*   <span data-ttu-id="88c0e-352">La ligne droite correspond essentiellement au délai passé pour le thread principal.</span><span class="sxs-lookup"><span data-stu-id="88c0e-352">The right line is essentially time spent waiting for the main thread.</span></span>  <span data-ttu-id="88c0e-353">Cette opération n’est pas représentée dans l’onglet **minutage** .</span><span class="sxs-lookup"><span data-stu-id="88c0e-353">This is not represented in the **Timing** tab.</span></span>  
    
:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-performance-network.msft.png" alt-text="Représentation de la barre de lignes de la requête www.bing.com" lightbox="../media/evaluate-performance-bing-performance-network.msft.png":::
         <span data-ttu-id="88c0e-355">Représentation de la barre de lignes de la `www.bing.com` requête</span><span class="sxs-lookup"><span data-stu-id="88c0e-355">The line-bar representation of the `www.bing.com` request</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-network-timing.msft.png" alt-text="Section réseau" lightbox="../media/evaluate-performance-bing-network-timing.msft.png":::
         <span data-ttu-id="88c0e-357">Section **réseau**</span><span class="sxs-lookup"><span data-stu-id="88c0e-357">The **Network** section</span></span>  
<span data-ttu-id="88c0e-358">:::: image-fin:::</span><span class="sxs-lookup"><span data-stu-id="88c0e-358">:      ::image-end:::</span></span>  
   :::column-end:::
:::row-end:::

### <span data-ttu-id="88c0e-359">Afficher les métriques de mémoire</span><span class="sxs-lookup"><span data-stu-id="88c0e-359">View memory metrics</span></span>   

<span data-ttu-id="88c0e-360">Activez la case à cocher **mémoire** pour afficher les mesures de mémoire du dernier enregistrement.</span><span class="sxs-lookup"><span data-stu-id="88c0e-360">Enable the **Memory** checkbox to view memory metrics from the last recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-memory-highlight.msft.png" alt-text="Case à cocher mémoire" lightbox="../media/evaluate-performance-performance-memory-highlight.msft.png":::
   <span data-ttu-id="88c0e-362">Case à cocher **mémoire**</span><span class="sxs-lookup"><span data-stu-id="88c0e-362">The **Memory** checkbox</span></span>  
:::image-end:::  

<span data-ttu-id="88c0e-363">DevTools affiche un nouveau graphique **mémoire** , au-dessus de l’onglet **Résumé** .  Il existe également un nouveau graphique sous le graphique **net** , appelé **tas**.</span><span class="sxs-lookup"><span data-stu-id="88c0e-363">DevTools displays a new **Memory** chart, above the **Summary** tab.  There is also a new chart below the **NET** chart, called **HEAP**.</span></span>  <span data-ttu-id="88c0e-364">Le graphique de **tas** fournit les mêmes informations que la ligne de segment de **mémoire** **js** dans le graphique mémoire.</span><span class="sxs-lookup"><span data-stu-id="88c0e-364">The **HEAP** chart provides the same information as the **JS Heap** line in the **Memory** chart.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-memory-chart.msft.png" alt-text="Métriques de mémoire" lightbox="../media/evaluate-performance-performance-memory-chart.msft.png":::
   <span data-ttu-id="88c0e-366">Métriques de mémoire</span><span class="sxs-lookup"><span data-stu-id="88c0e-366">Memory metrics</span></span>  
:::image-end:::  

<span data-ttu-id="88c0e-367">Les lignes de couleur sur le graphique correspondent aux cases à cocher en plus de la couleur du graphique.</span><span class="sxs-lookup"><span data-stu-id="88c0e-367">The colored lines on the chart map to the colored checkboxes above the chart.</span></span>  
<span data-ttu-id="88c0e-368">Désactivez une case à cocher pour masquer cette catégorie dans le graphique.</span><span class="sxs-lookup"><span data-stu-id="88c0e-368">Disable a checkbox to hide that category from the chart.</span></span>  

<span data-ttu-id="88c0e-369">Le graphique affiche uniquement la zone de l’enregistrement actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="88c0e-369">The chart only displays the region of the recording that is currently selected.</span></span>  <span data-ttu-id="88c0e-370">Par exemple, dans l’illustration précédente, le graphique **mémoire** affiche uniquement l’utilisation de la mémoire de la marque 400 ms au 1750 ms.</span><span class="sxs-lookup"><span data-stu-id="88c0e-370">For example, in the previous figure, the **Memory** chart is only showing memory usage from around the 400 ms mark to the 1750 ms mark.</span></span>  

### <span data-ttu-id="88c0e-371">Affichage de la durée d’une portion d’un enregistrement</span><span class="sxs-lookup"><span data-stu-id="88c0e-371">View the duration of a portion of a recording</span></span>   

<span data-ttu-id="88c0e-372">Lors de l’analyse d’une section comme **Network** ou **principal**, il est possible que vous ayez besoin d’une estimation plus précise de la durée de certains événements.</span><span class="sxs-lookup"><span data-stu-id="88c0e-372">When analyzing a section like **Network** or **Main**, sometimes you need a more precise estimate of how long certain events took.</span></span>  <span data-ttu-id="88c0e-373">Maintenez la touche enfoncée, `Shift` puis faites glisser vers la gauche ou la droite pour sélectionner une partie de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="88c0e-373">Hold `Shift`, click and hold, and drag left or right to select a portion of the recording.</span></span>  <span data-ttu-id="88c0e-374">Dans la partie inférieure de votre sélection, DevTools indique la durée de la partie.</span><span class="sxs-lookup"><span data-stu-id="88c0e-374">At the bottom of your selection, DevTools shows how long that portion took.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-main-duration.msft.png" alt-text="Affichage de la durée d’une portion d’un enregistrement" lightbox="../media/evaluate-performance-performance-main-duration.msft.png":::
   <span data-ttu-id="88c0e-376">Affichage de la durée d’une portion d’un enregistrement</span><span class="sxs-lookup"><span data-stu-id="88c0e-376">View the duration of a portion of a recording</span></span>  
:::image-end:::  

### <span data-ttu-id="88c0e-377">Affichage d’une capture d’écran</span><span class="sxs-lookup"><span data-stu-id="88c0e-377">View a screenshot</span></span>   

<span data-ttu-id="88c0e-378">Pour plus d’informations sur l’activation des captures d’écran, voir capturer des captures [d’écran lors de l’enregistrement](#capture-screenshots-while-recording) .</span><span class="sxs-lookup"><span data-stu-id="88c0e-378">See [Capture screenshots while recording](#capture-screenshots-while-recording) to learn how to enable screenshots.</span></span>  

<span data-ttu-id="88c0e-379">Placez le pointeur de la souris sur la **vue d’ensemble** pour afficher une capture d’écran illustrant l’apparence de la page pendant ce moment de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="88c0e-379">Hover over the **Overview** to view a screenshot of how the page looked during that moment of the recording.</span></span>  <span data-ttu-id="88c0e-380">La section **vue d’ensemble** contient les graphiques **UC**, **fps**et **net** .</span><span class="sxs-lookup"><span data-stu-id="88c0e-380">The **Overview** is the section that contains the **CPU**, **FPS**, and **NET** charts.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-screenshots-hover.msft.png" alt-text="Affichage d’une capture d’écran" lightbox="../media/evaluate-performance-performance-screenshots-hover.msft.png":::
   <span data-ttu-id="88c0e-382">Affichage d’une capture d’écran</span><span class="sxs-lookup"><span data-stu-id="88c0e-382">View a screenshot</span></span>  
:::image-end:::  

<span data-ttu-id="88c0e-383">Vous pouvez également afficher les captures d’écran en cliquant sur un cadre dans la section **cadres** .</span><span class="sxs-lookup"><span data-stu-id="88c0e-383">You may also view screenshots by clicking a frame in the **Frames** section.</span></span>  <span data-ttu-id="88c0e-384">DevTools affiche une version miniature de la capture d’écran sous l’onglet **Résumé** .</span><span class="sxs-lookup"><span data-stu-id="88c0e-384">DevTools displays a small version of the screenshot in the **Summary** tab.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview.msft.png" alt-text="Affichage d’une capture d’écran sous l’onglet Résumé" lightbox="../media/evaluate-performance-performance-summary-preview.msft.png":::
   <span data-ttu-id="88c0e-386">Affichage d’une capture d’écran sous l’onglet **Résumé**</span><span class="sxs-lookup"><span data-stu-id="88c0e-386">View a screenshot in the **Summary** tab</span></span>  
:::image-end:::  

<span data-ttu-id="88c0e-387">Pour effectuer un zoom avant dans la capture d’écran, cliquez sur la miniature sous l’onglet **Résumé** .</span><span class="sxs-lookup"><span data-stu-id="88c0e-387">Click the thumbnail in the **Summary** tab to zoom in on the screenshot.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview-select.msft.png" alt-text="Effectuer un zoom avant sur une capture d’écran à partir de l’onglet Résumé" lightbox="../media/evaluate-performance-performance-summary-preview-select.msft.png":::
   <span data-ttu-id="88c0e-389">Effectuer un zoom avant sur une capture d’écran à partir de l’onglet **Résumé**</span><span class="sxs-lookup"><span data-stu-id="88c0e-389">Zoom into a screenshot from the **Summary** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="88c0e-390">Afficher les informations sur les couches</span><span class="sxs-lookup"><span data-stu-id="88c0e-390">View layers information</span></span>   

<span data-ttu-id="88c0e-391">Pour afficher des informations sur les couches avancées d’une image:</span><span class="sxs-lookup"><span data-stu-id="88c0e-391">To view advanced layers information about a frame:</span></span>  

1.  <span data-ttu-id="88c0e-392">[Activez Advanced Paint instrumentation](#enable-advanced-paint-instrumentation).</span><span class="sxs-lookup"><span data-stu-id="88c0e-392">[Enable advanced paint instrumentation](#enable-advanced-paint-instrumentation).</span></span>  
1.  <span data-ttu-id="88c0e-393">Sélectionnez une image dans la section **cadre** .</span><span class="sxs-lookup"><span data-stu-id="88c0e-393">Select a frame in the **Frames** section.</span></span>  <span data-ttu-id="88c0e-394">DevTools affiche des informations sur les calques sous l’onglet nouveau **calques** , en regard de l’onglet **Journal des événements** .</span><span class="sxs-lookup"><span data-stu-id="88c0e-394">DevTools displays information about the layers in the new **Layers** tab, next to the **Event Log** tab.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-layers-all.msft.png" alt-text="Volet couches" lightbox="../media/evaluate-performance-layers-all.msft.png":::
       <span data-ttu-id="88c0e-396">Volet **couches**</span><span class="sxs-lookup"><span data-stu-id="88c0e-396">The **Layers** pane</span></span>  
    :::image-end:::  
    
<span data-ttu-id="88c0e-397">Pointez sur un calque pour le mettre en surbrillance dans le diagramme.</span><span class="sxs-lookup"><span data-stu-id="88c0e-397">Hover over a layer to highlight it in the diagram.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png" alt-text="Mettre un calque en surbrillance" lightbox="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png":::
   <span data-ttu-id="88c0e-399">Mettre un calque en surbrillance</span><span class="sxs-lookup"><span data-stu-id="88c0e-399">Highlight a layer</span></span>  
:::image-end:::  

<span data-ttu-id="88c0e-400">Pour déplacer le diagramme:</span><span class="sxs-lookup"><span data-stu-id="88c0e-400">To move the diagram:</span></span>  

*   <span data-ttu-id="88c0e-401">Cliquez sur **mode panoramique** \ ( ![ mode panoramique ][ImagePanModeIcon] \) pour vous déplacer le long des axes X et Y.</span><span class="sxs-lookup"><span data-stu-id="88c0e-401">Click **Pan Mode** \(![Pan Mode][ImagePanModeIcon]\) to move along the X and Y axes.</span></span>  
*   <span data-ttu-id="88c0e-402">Cliquez sur **mode pivoter** \ ( ![ mode pivoter ][ImageRotateModeIcon] \) pour faire pivoter le long de l’axe Z.</span><span class="sxs-lookup"><span data-stu-id="88c0e-402">Click **Rotate Mode** \(![Rotate Mode][ImageRotateModeIcon]\) to rotate along the Z axis.</span></span>  
*   <span data-ttu-id="88c0e-403">Cliquez sur **Réinitialiser la transformation** \ (réinitialiser la ![ transformation ][ImageResetTransformIcon] \) pour rétablir la position d’origine du diagramme.</span><span class="sxs-lookup"><span data-stu-id="88c0e-403">Click **Reset Transform** \(![Reset Transform][ImageResetTransformIcon]\) to reset the diagram to the original position.</span></span>  
    
### <span data-ttu-id="88c0e-404">Afficher le générateur de dessin Paint</span><span class="sxs-lookup"><span data-stu-id="88c0e-404">View paint profiler</span></span>   

<span data-ttu-id="88c0e-405">Pour afficher des informations détaillées sur un événement Paint:</span><span class="sxs-lookup"><span data-stu-id="88c0e-405">To view advanced information about a paint event:</span></span>  

1.  <span data-ttu-id="88c0e-406">[Activez Advanced Paint instrumentation](#enable-advanced-paint-instrumentation).</span><span class="sxs-lookup"><span data-stu-id="88c0e-406">[Enable advanced paint instrumentation](#enable-advanced-paint-instrumentation).</span></span>  
1.  <span data-ttu-id="88c0e-407">Sélectionnez un événement **Paint** dans la section **principale** .</span><span class="sxs-lookup"><span data-stu-id="88c0e-407">Select a **Paint** event in the **Main** section.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-paint-profiler.msft.png" alt-text="Onglet Paint Profiler1.1" lightbox="../media/evaluate-performance-paint-profiler.msft.png":::
       <span data-ttu-id="88c0e-409">Onglet **Paint Profiler1.1**</span><span class="sxs-lookup"><span data-stu-id="88c0e-409">The **Paint Profiler** tab</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="88c0e-410">Analyser les performances de rendu à l’aide de l’onglet rendu</span><span class="sxs-lookup"><span data-stu-id="88c0e-410">Analyze rendering performance with the Rendering tab</span></span>   

<span data-ttu-id="88c0e-411">Utilisez les fonctionnalités de l’onglet **rendu** pour visualiser les performances de rendu de votre page.</span><span class="sxs-lookup"><span data-stu-id="88c0e-411">Use the features of the **Rendering** tab to help visualize the rendering performance of your page.</span></span>  

<span data-ttu-id="88c0e-412">Pour ouvrir l’onglet **rendu** :</span><span class="sxs-lookup"><span data-stu-id="88c0e-412">To open the **Rendering** tab:</span></span>  

1.  <span data-ttu-id="88c0e-413">[Ouvrir le menu de commandes][DevToolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="88c0e-413">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="88c0e-414">Commencez à taper `Rendering` et sélectionnez `Show Rendering` .</span><span class="sxs-lookup"><span data-stu-id="88c0e-414">Start typing `Rendering` and select `Show Rendering`.</span></span>  <span data-ttu-id="88c0e-415">DevTools affiche l’onglet **rendu** en bas de votre fenêtre devtools.</span><span class="sxs-lookup"><span data-stu-id="88c0e-415">DevTools displays the **Rendering** tab at the bottom of your DevTools window.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-console-drawer-rendering.msft.png" alt-text="Onglet rendu" lightbox="../media/evaluate-performance-console-drawer-rendering.msft.png":::
       <span data-ttu-id="88c0e-417">Onglet **rendu**</span><span class="sxs-lookup"><span data-stu-id="88c0e-417">The **Rendering** tab</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="88c0e-418">Afficher les images par seconde en temps réel avec le compteur FPS</span><span class="sxs-lookup"><span data-stu-id="88c0e-418">View frames per second in realtime with the FPS meter</span></span>   

<span data-ttu-id="88c0e-419">Le **compteur fps** est une superposition qui s’affiche dans le coin supérieur droit de votre fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="88c0e-419">The **FPS meter** is an overlay that appears in the top-right corner of your viewport.</span></span>  <span data-ttu-id="88c0e-420">Il fournit une estimation en temps réel de FPS lors de l’exécution de la page.</span><span class="sxs-lookup"><span data-stu-id="88c0e-420">It provides a realtime estimate of FPS as the page runs.</span></span>  <span data-ttu-id="88c0e-421">Pour ouvrir le **compteur fps**:</span><span class="sxs-lookup"><span data-stu-id="88c0e-421">To open the **FPS meter**:</span></span>  

1.  <span data-ttu-id="88c0e-422">Ouvrez l’onglet **rendu** .  [Pour plus d’efficacité, voir analyser les performances de rendu avec l’onglet rendu](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="88c0e-422">Open the **Rendering** tab.  See [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="88c0e-423">Activez la case à cocher **vumètre** .</span><span class="sxs-lookup"><span data-stu-id="88c0e-423">Enable the **FPS Meter** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png" alt-text="Vumètre FPS" lightbox="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png":::
       <span data-ttu-id="88c0e-425">**Vumètre fps**</span><span class="sxs-lookup"><span data-stu-id="88c0e-425">The **FPS meter**</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="88c0e-426">Afficher les événements de peinture en temps réel avec le clignotement de la peinture</span><span class="sxs-lookup"><span data-stu-id="88c0e-426">View painting events in realtime with Paint Flashing</span></span>   

<span data-ttu-id="88c0e-427">Utilisez la fonction Paint clignotante pour obtenir une vue en temps réel de tous les événements de peinture sur la page.</span><span class="sxs-lookup"><span data-stu-id="88c0e-427">Use Paint Flashing to get a realtime view of all paint events on the page.</span></span>  <span data-ttu-id="88c0e-428">Dès qu’une partie de la page est de nouveau peinte, DevTools la place en vert.</span><span class="sxs-lookup"><span data-stu-id="88c0e-428">Whenever a part of the page gets re-painted, DevTools outlines that section in green.</span></span>  

<span data-ttu-id="88c0e-429">Pour activer le clignotement des peintures:</span><span class="sxs-lookup"><span data-stu-id="88c0e-429">To enable Paint Flashing:</span></span>  

1.  <span data-ttu-id="88c0e-430">Ouvrez l’onglet **rendu** .  [Pour plus d’efficacité, voir analyser les performances de rendu avec l’onglet rendu](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="88c0e-430">Open the **Rendering** tab.  See [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="88c0e-431">Activez la case à cocher **Paint clignotant** .</span><span class="sxs-lookup"><span data-stu-id="88c0e-431">Enable the **Paint Flashing** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png" alt-text="Paint clignotant" lightbox="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png":::
       **<span data-ttu-id="88c0e-433">Paint clignotant</span><span class="sxs-lookup"><span data-stu-id="88c0e-433">Paint Flashing</span></span>**  
    :::image-end:::  
    
### <span data-ttu-id="88c0e-434">Afficher une superposition de calques avec des bordures de calque</span><span class="sxs-lookup"><span data-stu-id="88c0e-434">View an overlay of layers with Layer Borders</span></span>   

<span data-ttu-id="88c0e-435">Utilisez les **bordures de calque** pour afficher une superposition des bordures et des vignettes du calque en haut de la page.</span><span class="sxs-lookup"><span data-stu-id="88c0e-435">Use **Layer Borders** to view an overlay of layer borders and tiles on top of the page.</span></span>  

<span data-ttu-id="88c0e-436">Pour activer les bordures de calque:</span><span class="sxs-lookup"><span data-stu-id="88c0e-436">To enable Layer Borders:</span></span>  

1.  <span data-ttu-id="88c0e-437">Ouvrez l’onglet **rendu** .  [Pour plus d’efficacité, voir analyser les performances de rendu avec l’onglet rendu](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="88c0e-437">Open the **Rendering** tab.  See [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="88c0e-438">Activez la case à cocher **bordures de calque** .</span><span class="sxs-lookup"><span data-stu-id="88c0e-438">Enable the **Layer Borders** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png" alt-text="Bordures de calque" lightbox="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png":::
       **<span data-ttu-id="88c0e-440">Bordures de calque</span><span class="sxs-lookup"><span data-stu-id="88c0e-440">Layer Borders</span></span>**  
    :::image-end:::  
    
<span data-ttu-id="88c0e-441">[`debug_colors.cc`][ChromiumDebugColors]Pour obtenir une description des codes de couleur, voir les commentaires.</span><span class="sxs-lookup"><span data-stu-id="88c0e-441">See the comments in [`debug_colors.cc`][ChromiumDebugColors] for an explanation of the color-codings.</span></span>  

### <span data-ttu-id="88c0e-442">Rechercher des problèmes de performances de défilement en temps réel</span><span class="sxs-lookup"><span data-stu-id="88c0e-442">Find scroll performance issues in realtime</span></span>   

<span data-ttu-id="88c0e-443">Utilisez des problèmes de performances de défilement pour identifier les éléments de la page qui comportent des écouteurs d’événements liés au défilement qui peuvent nuire aux performances de la page.</span><span class="sxs-lookup"><span data-stu-id="88c0e-443">Use Scrolling Performance Issues to identify elements of the page that have event listeners related to scrolling that may harm the performance of the page.</span></span>  
<span data-ttu-id="88c0e-444">DevTools souligne les éléments potentiellement posant problème en bleu-vert.</span><span class="sxs-lookup"><span data-stu-id="88c0e-444">DevTools outlines the potentially-problematic elements in teal.</span></span>  

<span data-ttu-id="88c0e-445">Pour afficher les problèmes de performances de défilement:</span><span class="sxs-lookup"><span data-stu-id="88c0e-445">To view scroll performance issues:</span></span>  

1.  <span data-ttu-id="88c0e-446">Ouvrez l’onglet **rendu** .  [Pour plus d’efficacité, voir analyser les performances de rendu avec l’onglet rendu](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="88c0e-446">Open the **Rendering** tab.  See [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="88c0e-447">Activez la case à cocher **problèmes de performances de défilement** .</span><span class="sxs-lookup"><span data-stu-id="88c0e-447">Enable the **Scrolling Performance Issues** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png" alt-text="Les problèmes de performances de défilement indiquent que les objets dotés de l’affichage sans calque risquent de nuire aux performances de défilement" lightbox="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png":::
       <span data-ttu-id="88c0e-449">Les **problèmes de performances de défilement** indiquent que les objets dotés de l’affichage sans calque risquent de nuire aux performances de défilement</span><span class="sxs-lookup"><span data-stu-id="88c0e-449">**Scrolling Performance Issues** indicates that non-layer viewport-constrained objects may harm scroll performance</span></span>  
    :::image-end:::  
    
<!--  
<!--    


-->  

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
> <span data-ttu-id="88c0e-455">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="88c0e-455">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="88c0e-456">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="88c0e-456">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="88c0e-458">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="88c0e-458">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
