---
title: Référence d’analyse des performances
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: acd6e3e68f89096cf80c08f0d0c3430ab31eaec1
ms.sourcegitcommit: 50991a04c18283a8890ae33fcc3491c0476c7684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611747"
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







# <span data-ttu-id="2f8c4-103">Référence d’analyse des performances</span><span class="sxs-lookup"><span data-stu-id="2f8c4-103">Performance Analysis Reference</span></span>   



<span data-ttu-id="2f8c4-104">Cette page est une référence complète des fonctionnalités de Microsoft Edge DevTools liées à l’analyse des performances.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-104">This page is a comprehensive reference of Microsoft Edge DevTools features related to analyzing performance.</span></span>  

<span data-ttu-id="2f8c4-105">Pour plus d’informations sur l’analyse des performances d’une page à l’aide de [Microsoft Edge devtools][MicrosoftEdgeDevTools], voir mise [en route][DevtoolsEvaluatePerformanceGettingStarted] de l’analyse des performances de l’exécution d’une page.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-105">See [Get Started With Analyzing Runtime Performance][DevtoolsEvaluatePerformanceGettingStarted] for a guided tutorial on how to analyze the performance of a page using [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <span data-ttu-id="2f8c4-106">Performance enregistrement</span><span class="sxs-lookup"><span data-stu-id="2f8c4-106">Record performance</span></span>   

### <span data-ttu-id="2f8c4-107">Enregistrer les performances d’exécution</span><span class="sxs-lookup"><span data-stu-id="2f8c4-107">Record runtime performance</span></span>   

<span data-ttu-id="2f8c4-108">Enregistrez les performances d’exécution lorsque vous souhaitez analyser les performances d’une page en cours d’exécution, plutôt que de procéder au chargement.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-108">Record runtime performance when you want to analyze the performance of a page as it is running, as opposed to loading.</span></span>  

1.  <span data-ttu-id="2f8c4-109">Accédez à la page que vous voulez analyser.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-109">Go to the page that you want to analyze.</span></span>  
1.  <span data-ttu-id="2f8c4-110">Cliquez sur l’onglet **performance** dans devtools.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-110">Click the **Performance** tab in DevTools.</span></span>  
1.  <span data-ttu-id="2f8c4-111">Cliquez sur **Enregistrer** l' ![ enregistrement ][ImageRecordIcon] .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-111">Click **Record** ![Record][ImageRecordIcon].</span></span>  
    
    > ##### <span data-ttu-id="2f8c4-112">Figure1</span><span class="sxs-lookup"><span data-stu-id="2f8c4-112">Figure 1</span></span>  
    > **<span data-ttu-id="2f8c4-113">Record</span><span class="sxs-lookup"><span data-stu-id="2f8c4-113">Record</span></span>**  
    > ![Record][ImageRecord]  

1.  <span data-ttu-id="2f8c4-115">Interagir avec la page.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-115">Interact with the page.</span></span>  <span data-ttu-id="2f8c4-116">DevTools enregistre toutes les activités de page résultant de vos interactions.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-116">DevTools records all page activity that occurs as a result of your interactions.</span></span>  
1.  <span data-ttu-id="2f8c4-117">Cliquez de nouveau sur **Enregistrer** ou cliquez sur **arrêter** pour arrêter l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-117">Click **Record** again or click **Stop** to stop recording.</span></span>  

### <span data-ttu-id="2f8c4-118">Enregistrer les performances de chargement</span><span class="sxs-lookup"><span data-stu-id="2f8c4-118">Record load performance</span></span>   

<span data-ttu-id="2f8c4-119">Enregistrez les performances de chargement lorsque vous souhaitez analyser les performances d’une page lors du chargement, plutôt que d’être en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-119">Record load performance when you want to analyze the performance of a page as it is loading, as opposed to running.</span></span>  

1.  <span data-ttu-id="2f8c4-120">Accédez à la page que vous voulez analyser.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-120">Go to the page that you want to analyze.</span></span>  
1.  <span data-ttu-id="2f8c4-121">Ouvrez le panneau **performances** de devtools.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-121">Open the **Performance** panel of DevTools.</span></span>  
1.  <span data-ttu-id="2f8c4-122">Cliquez sur **Actualiser** la page ![ Actualiser la page ][ImageRefreshPageIcon] .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-122">Click **Refresh page** ![Refresh Page][ImageRefreshPageIcon].</span></span>  <span data-ttu-id="2f8c4-123">DevTools enregistre les métriques de performances pendant que la page est actualisée, puis arrête automatiquement l’enregistrement de quelques secondes après la fin de la charge.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-123">DevTools records performance metrics while the page refreshes and then automatically stops the recording a couple seconds after the load finishes.</span></span>  
    
    > ##### <span data-ttu-id="2f8c4-124">Figure 2</span><span class="sxs-lookup"><span data-stu-id="2f8c4-124">Figure 2</span></span>  
    > **<span data-ttu-id="2f8c4-125">Actualiser la page</span><span class="sxs-lookup"><span data-stu-id="2f8c4-125">Refresh page</span></span>**  
    > ![Actualiser la page][ImageRefreshPage]  

<span data-ttu-id="2f8c4-127">DevTools effectue automatiquement un zoom avant sur la partie de l’enregistrement où la majeure partie de l’activité s’est produite.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-127">DevTools automatically zooms in on the portion of the recording where most of the activity occurred.</span></span>  

> ##### <span data-ttu-id="2f8c4-128">Figure3</span><span class="sxs-lookup"><span data-stu-id="2f8c4-128">Figure 3</span></span>  
> <span data-ttu-id="2f8c4-129">Un enregistrement de chargement de page</span><span class="sxs-lookup"><span data-stu-id="2f8c4-129">A page-load recording</span></span>  
> ![Un enregistrement de chargement de page][ImageLoadRecording]  

### <span data-ttu-id="2f8c4-131">Capture des captures d’écran lors de l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="2f8c4-131">Capture screenshots while recording</span></span>   

<span data-ttu-id="2f8c4-132">Activez la case à cocher **captures d’écran** pour capturer une capture d’écran de chaque image lors de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-132">Enable the **Screenshots** checkbox to capture a screenshot of every frame while recording.</span></span>  

> ##### <span data-ttu-id="2f8c4-133">Figure 4</span><span class="sxs-lookup"><span data-stu-id="2f8c4-133">Figure 4</span></span>  
> <span data-ttu-id="2f8c4-134">Case à cocher **captures d’écran**</span><span class="sxs-lookup"><span data-stu-id="2f8c4-134">The **Screenshots** checkbox</span></span>  
> ![Case à cocher captures d’écran][ImageScreenshots]  

<span data-ttu-id="2f8c4-136">Pour plus d’informations sur l’interaction avec les captures d’écran, voir [afficher une capture d’écran](#view-a-screenshot) .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-136">See [View a screenshot](#view-a-screenshot) to learn how to interact with screenshots.</span></span>  

### <span data-ttu-id="2f8c4-137">Forcer le nettoyage de la mémoire lors de l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="2f8c4-137">Force garbage collection while recording</span></span>   

<span data-ttu-id="2f8c4-138">Pendant que vous enregistrez une page, cliquez sur **collecter** le nettoyage de la mémoire ![ ][ImageCollectGarbageIcon] pour forcer le nettoyage de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-138">While you are recording a page, click **Collect garbage** ![Collect garbage][ImageCollectGarbageIcon] to force garbage collection.</span></span>  

> ##### <span data-ttu-id="2f8c4-139">Figure 5</span><span class="sxs-lookup"><span data-stu-id="2f8c4-139">Figure 5</span></span>  
> <span data-ttu-id="2f8c4-140">Collecter les nettoyages de la mémoire</span><span class="sxs-lookup"><span data-stu-id="2f8c4-140">Collect garbage</span></span>  
> ![Collecter les nettoyages de la mémoire][ImageCollectGarbage]  

### <span data-ttu-id="2f8c4-142">Afficher les paramètres d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="2f8c4-142">Show recording settings</span></span>   

<span data-ttu-id="2f8c4-143">Cliquez sur **paramètres** ![ de capture ][ImageCaptureSettingsIcon] pour afficher d’autres paramètres liés à la manière dont devtools capture les enregistrements de performances.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-143">Click **Capture settings** ![Capture settings][ImageCaptureSettingsIcon] to expose more settings related to how DevTools captures performance recordings.</span></span>  

> ##### <span data-ttu-id="2f8c4-144">Figure 6</span><span class="sxs-lookup"><span data-stu-id="2f8c4-144">Figure 6</span></span>  
> <span data-ttu-id="2f8c4-145">Section **paramètres de capture**</span><span class="sxs-lookup"><span data-stu-id="2f8c4-145">The **Capture settings** section</span></span>  
> ![Section paramètres de capture][ImageCaptureSettings]  

### <span data-ttu-id="2f8c4-147">Désactiver les exemples JavaScript</span><span class="sxs-lookup"><span data-stu-id="2f8c4-147">Disable JavaScript samples</span></span>   

<span data-ttu-id="2f8c4-148">Par défaut, la section **principale** d’un enregistrement affiche des piles d’appels détaillées des fonctions JavaScript qui ont été appelées lors de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-148">By default, the **Main** section of a recording displays detailed call stacks of JavaScript functions that were called during the recording.</span></span>  <span data-ttu-id="2f8c4-149">Pour désactiver ces piles d’appels:</span><span class="sxs-lookup"><span data-stu-id="2f8c4-149">To disable these call stacks:</span></span>  

1.  <span data-ttu-id="2f8c4-150">Ouvrir le menu **paramètres de capture** .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-150">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="2f8c4-151">Voir [afficher les paramètres d’enregistrement](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="2f8c4-151">See [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="2f8c4-152">Activez la case à cocher **Désactiver les exemples JavaScript** .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-152">Enable the **Disable JavaScript Samples** checkbox.</span></span>  
1.  <span data-ttu-id="2f8c4-153">Prenez un enregistrement de la page.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-153">Take a recording of the page.</span></span>  

<span data-ttu-id="2f8c4-154">La [figure 7](#figure-7) et la [figure 8](#figure-8) montrent la différence entre la désactivation et l’activation des exemples JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-154">[Figure 7](#figure-7) and [Figure 8](#figure-8) show the difference between disabling and enabling JavaScript samples.</span></span>  <span data-ttu-id="2f8c4-155">La section **principale** de l’enregistrement est beaucoup plus courte lorsque l’échantillonnage est désactivé, car il omet toutes les piles d’appels JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-155">The **Main** section of the recording is much shorter when sampling is disabled, because it omits all of the JavaScript call stacks.</span></span>  

> ##### <span data-ttu-id="2f8c4-156">Figure 7</span><span class="sxs-lookup"><span data-stu-id="2f8c4-156">Figure 7</span></span>  
> <span data-ttu-id="2f8c4-157">Un exemple d’enregistrement lorsque les exemples de JS sont désactivés</span><span class="sxs-lookup"><span data-stu-id="2f8c4-157">An example of a recording when JS samples are disabled</span></span>  
> ![Un exemple d’enregistrement lorsque les exemples de JS sont désactivés][ImageJSSamplesDisabled]  

> ##### <span data-ttu-id="2f8c4-159">Figure8</span><span class="sxs-lookup"><span data-stu-id="2f8c4-159">Figure 8</span></span>  
> <span data-ttu-id="2f8c4-160">Exemple d’enregistrement lorsque les exemples de JS sont activés</span><span class="sxs-lookup"><span data-stu-id="2f8c4-160">An example of a recording when JS samples are enabled</span></span>  
> ![Exemple d’enregistrement lorsque les exemples de JS sont activés][ImageJSSamplesEnabled]  

### <span data-ttu-id="2f8c4-162">Limiter le réseau lors de l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="2f8c4-162">Throttle the network while recording</span></span>   

<span data-ttu-id="2f8c4-163">Pour limiter le réseau lors de l’enregistrement:</span><span class="sxs-lookup"><span data-stu-id="2f8c4-163">To throttle the network while recording:</span></span>  

1.  <span data-ttu-id="2f8c4-164">Ouvrir le menu **paramètres de capture** .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-164">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="2f8c4-165">Voir [afficher les paramètres d’enregistrement](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="2f8c4-165">See [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="2f8c4-166">Définissez **réseau** sur le niveau de limitation souhaité.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-166">Set **Network** to the desired level of throttling.</span></span>  

### <span data-ttu-id="2f8c4-167">Limiter le processeur lors de l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="2f8c4-167">Throttle the CPU while recording</span></span>   

<span data-ttu-id="2f8c4-168">Pour limiter le processeur lors de l’enregistrement:</span><span class="sxs-lookup"><span data-stu-id="2f8c4-168">To throttle the CPU while recording:</span></span>  

1.  <span data-ttu-id="2f8c4-169">Ouvrir le menu **paramètres de capture** .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-169">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="2f8c4-170">Voir [afficher les paramètres d’enregistrement](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="2f8c4-170">See [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="2f8c4-171">Définissez **UC** sur le niveau de limitation souhaité.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-171">Set **CPU** to the desired level of throttling.</span></span>  

<span data-ttu-id="2f8c4-172">La limitation est relative aux fonctionnalités de votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-172">Throttling is relative to the capabilities of your computer.</span></span>  <span data-ttu-id="2f8c4-173">Par exemple, l’option **2x Slowdown** permet à votre processeur de fonctionner 2 fois plus lent que d’habitude.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-173">For example, the **2x slowdown** option makes your CPU operate 2 times slower than normal.</span></span>  <span data-ttu-id="2f8c4-174">DevTools ne simulez pas vraiment les UC des appareils mobiles, car l’architecture des appareils mobiles est très différente de celle des ordinateurs de bureau et des ordinateurs portables.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-174">DevTools do not truly simulate the CPUs of mobile devices, because the architecture of mobile devices is very different from that of desktops and laptops.</span></span>  

### <span data-ttu-id="2f8c4-175">Activer l’instrumentation avancée de peinture</span><span class="sxs-lookup"><span data-stu-id="2f8c4-175">Enable advanced paint instrumentation</span></span>   

<span data-ttu-id="2f8c4-176">Pour afficher une instrumentation détaillée de Paint:</span><span class="sxs-lookup"><span data-stu-id="2f8c4-176">To view detailed paint instrumentation:</span></span>  

1.  <span data-ttu-id="2f8c4-177">Ouvrir le menu **paramètres de capture** .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-177">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="2f8c4-178">Voir [afficher les paramètres d’enregistrement](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="2f8c4-178">See [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="2f8c4-179">Cochez la case **activer l’instrumentation avancée de peinture (lente)** .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-179">Check the **Enable advanced paint instrumentation (slow)** checkbox.</span></span>  

<span data-ttu-id="2f8c4-180">Pour plus d’informations sur l’interaction avec les informations de Paint, voir [afficher les couches](#view-layers-information) et afficher le [Générateur de profils Paint](#view-paint-profiler).</span><span class="sxs-lookup"><span data-stu-id="2f8c4-180">To learn how to interact with the paint information, see [View layers](#view-layers-information) and [View paint profiler](#view-paint-profiler).</span></span>  

## <span data-ttu-id="2f8c4-181">Enregistrer un enregistrement</span><span class="sxs-lookup"><span data-stu-id="2f8c4-181">Save a recording</span></span>   

<span data-ttu-id="2f8c4-182">Pour enregistrer un enregistrement, cliquez avec le bouton droit et sélectionnez **enregistrer le profil**.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-182">To save a recording, right-click and select **Save Profile**.</span></span>  

> ##### <span data-ttu-id="2f8c4-183">Figure9</span><span class="sxs-lookup"><span data-stu-id="2f8c4-183">Figure 9</span></span>  
> **<span data-ttu-id="2f8c4-184">Enregistrer le profil</span><span class="sxs-lookup"><span data-stu-id="2f8c4-184">Save Profile</span></span>**  
> ![Enregistrer le profil][ImageSaveProfile]  

## <span data-ttu-id="2f8c4-186">Charger un enregistrement</span><span class="sxs-lookup"><span data-stu-id="2f8c4-186">Load a recording</span></span>   

<span data-ttu-id="2f8c4-187">Pour charger un enregistrement, cliquez avec le bouton droit et sélectionnez **charger le profil**.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-187">To load a recording, right-click and select **Load Profile**.</span></span>  

> ##### <span data-ttu-id="2f8c4-188">Figure10</span><span class="sxs-lookup"><span data-stu-id="2f8c4-188">Figure 10</span></span>  
> **<span data-ttu-id="2f8c4-189">Profil de chargement</span><span class="sxs-lookup"><span data-stu-id="2f8c4-189">Load Profile</span></span>**  
> ![Profil de chargement][ImageLoadProfile]  

## <span data-ttu-id="2f8c4-191">Effacer l’enregistrement précédent</span><span class="sxs-lookup"><span data-stu-id="2f8c4-191">Clear the previous recording</span></span>   

<span data-ttu-id="2f8c4-192">Une fois l’enregistrement terminé, cliquez sur **effacer l'** enregistrement effacer l’enregistrement ![ ][ImageClearRecordingIcon] pour effacer cet enregistrement du panneau **performances** .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-192">After making a recording, press **Clear recording** ![Clear recording][ImageClearRecordingIcon] to clear that recording from the **Performance** panel.</span></span>  

> ##### <span data-ttu-id="2f8c4-193">Figure11</span><span class="sxs-lookup"><span data-stu-id="2f8c4-193">Figure 11</span></span>  
> <span data-ttu-id="2f8c4-194">Effacer l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="2f8c4-194">Clear recording</span></span>  
> ![Effacer l’enregistrement][ImageClearRecording]  

## <span data-ttu-id="2f8c4-196">Analyser un enregistrement de performance</span><span class="sxs-lookup"><span data-stu-id="2f8c4-196">Analyze a performance recording</span></span>   

<span data-ttu-id="2f8c4-197">Une fois que vous avez [enregistré des performances d’exécution](#record-runtime-performance) ou enregistré des performances de [chargement](#record-load-performance), le panneau **performance** fournit un grand nombre de données pour l’analyse des performances de ce qui s’est produit.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-197">After you [record runtime performance](#record-runtime-performance) or [record load performance](#record-load-performance), the **Performance** panel provides a lot of data for analyzing the performance of what just happened.</span></span>  

### <span data-ttu-id="2f8c4-198">Sélectionner une partie d’un enregistrement</span><span class="sxs-lookup"><span data-stu-id="2f8c4-198">Select a portion of a recording</span></span>   

<span data-ttu-id="2f8c4-199">Faites glisser le pointeur de la souris vers la gauche ou la droite dans la **vue d’ensemble** pour sélectionner une partie d’un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-199">Drag your mouse left or right across the **Overview** to select a portion of a recording.</span></span>  <span data-ttu-id="2f8c4-200">La section **vue d’ensemble** contient les graphiques **fps**, **UC**et **net** .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-200">The **Overview** is the section that contains the **FPS**, **CPU**, and **NET** charts.</span></span>  

> ##### <span data-ttu-id="2f8c4-201">Figure12</span><span class="sxs-lookup"><span data-stu-id="2f8c4-201">Figure 12</span></span>  
> <span data-ttu-id="2f8c4-202">Faire glisser la souris sur la vue d’ensemble pour effectuer un zoom</span><span class="sxs-lookup"><span data-stu-id="2f8c4-202">Dragging the mouse across the Overview to zoom</span></span>  
> ![Faire glisser la souris sur la vue d’ensemble pour effectuer un zoom][ImageZoom]  

<span data-ttu-id="2f8c4-204">Pour sélectionner une partie à l’aide du clavier:</span><span class="sxs-lookup"><span data-stu-id="2f8c4-204">To select a portion using the keyboard:</span></span>  

1.  <span data-ttu-id="2f8c4-205">Cliquez sur l’arrière-plan de la section **principale** ou de n’importe quelle section en regard de celle-ci, comme **interactions**, **réseau**ou **GPU**.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-205">Click on the background of the **Main** section, or any of the sections next to it, such as **Interactions**, **Network**, or **GPU**.</span></span>  <span data-ttu-id="2f8c4-206">Ce flux de travail de clavier fonctionne uniquement lorsque l’une de ces sections est activée.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-206">This keyboard workflow only works when one of these sections is in focus.</span></span>  
1.  <span data-ttu-id="2f8c4-207">Utilisez les `W` touches,,, `A` `S` `D` pour effectuer un zoom avant, vous déplacer vers la gauche, effectuer un zoom arrière et vous déplacer à droite, respectivement.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-207">Use the `W`, `A`, `S`, `D` keys to zoom in, move left, zoom out, and move right, respectively.</span></span>  

<span data-ttu-id="2f8c4-208">Pour sélectionner une partie à l’aide d’une pavé tactile:</span><span class="sxs-lookup"><span data-stu-id="2f8c4-208">To select a portion using a trackpad:</span></span>  

1.  <span data-ttu-id="2f8c4-209">Positionnez le pointeur de la souris sur la section **Présentation** ou la section **Détails** .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-209">Hover your mouse over the **Overview** section or the **Details** section.</span></span>  <span data-ttu-id="2f8c4-210">La section **vue d’ensemble** est la zone contenant les graphiques **fps**, **UC**et **net** .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-210">The **Overview** section is the area containing the **FPS**, **CPU**, and **NET** charts.</span></span>  <span data-ttu-id="2f8c4-211">La section **Détails** représente la zone contenant la section **principale** , la section **interactions** , etc.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-211">The **Details** section is the area containing the **Main** section, the **Interactions** section, and so on.</span></span>  
1.  <span data-ttu-id="2f8c4-212">Avec deux doigts, balayez vers le haut pour effectuer un zoom arrière, balayez vers la gauche pour vous déplacer vers la gauche, balayez vers le bas pour effectuer un zoom avant, puis balayez vers la droite pour avancer.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-212">Using two fingers, swipe up to zoom out, swipe left to move left, swipe down to zoom in, and swipe right to move right.</span></span>  

<span data-ttu-id="2f8c4-213">Pour faire défiler un grand graphique en flamme dans la section **principale** ou sur l’un des voisins, cliquez et maintenez le bouton enfoncé tout en faisant glisser le curseur vers le haut et le bas.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-213">To scroll a long flame chart in the **Main** section or any of the neighbors, click and hold while dragging up and down.</span></span>  <span data-ttu-id="2f8c4-214">Faites glisser vers la gauche et vers la droite pour déplacer la partie de l’enregistrement sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-214">Drag left and right to move what portion of the recording is selected.</span></span>  

### <span data-ttu-id="2f8c4-215">Activités de recherche</span><span class="sxs-lookup"><span data-stu-id="2f8c4-215">Search activities</span></span>   

<span data-ttu-id="2f8c4-216">`Control` + `F` `Command` + `F` Pour ouvrir la zone de recherche située en bas du panneau de **performance** , appuyez sur \ (Windows \) ou \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="2f8c4-216">Press `Control`+`F` \(Windows\) or `Command`+`F` \(macOS\) to open the search box at the bottom of the **Performance** panel.</span></span>  

> ##### <span data-ttu-id="2f8c4-217">Figure13</span><span class="sxs-lookup"><span data-stu-id="2f8c4-217">Figure 13</span></span>  
> <span data-ttu-id="2f8c4-218">Utilisation de Regex dans la zone de recherche située en bas de la fenêtre pour rechercher les activités qui commencent par</span><span class="sxs-lookup"><span data-stu-id="2f8c4-218">Using regex in the search box at the bottom of the window to find any activity that begins with</span></span> `E`  
> ![Zone de recherche][ImageSearch]  

<span data-ttu-id="2f8c4-220">Pour parcourir les activités qui correspondent à votre requête:</span><span class="sxs-lookup"><span data-stu-id="2f8c4-220">To navigate activities that match your query:</span></span>  

*   <span data-ttu-id="2f8c4-221">Utilisez les **Previous** ![ boutons précédent ][ImagePreviousIcon] et **suivant** ![ ][ImageNextIcon] .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-221">Use the **Previous** ![Previous][ImagePreviousIcon] and **Next** ![Next][ImageNextIcon] buttons.</span></span>  
*   <span data-ttu-id="2f8c4-222">Appuyez `Shift` + `Enter` pour sélectionner le précédent ou `Enter` pour en sélectionner un autre.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-222">Press `Shift`+`Enter` to select the previous or `Enter` to select the next.</span></span>  

<span data-ttu-id="2f8c4-223">Pour modifier les paramètres d’une requête:</span><span class="sxs-lookup"><span data-stu-id="2f8c4-223">To modify query settings:</span></span>  

*   <span data-ttu-id="2f8c4-224">Respect **Case sensitive** ![ ][ImageSearchCaseIcon] de la casse en tenant compte de la casse.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-224">Press **Case sensitive** ![Case sensitive][ImageSearchCaseIcon] to make the query case sensitive.</span></span>  
*   <span data-ttu-id="2f8c4-225">Appuyez **sur Regex Regex** ![ ][ImageSearchRegexIcon] pour utiliser une expression régulière dans votre requête.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-225">Press **Regex** ![Regex][ImageSearchRegexIcon] to use a regular expression in your query.</span></span>  

<span data-ttu-id="2f8c4-226">Pour masquer la zone de recherche, appuyez sur **Annuler**.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-226">To hide the search box, press **Cancel**.</span></span>  

### <span data-ttu-id="2f8c4-227">Afficher l’activité du thread principal</span><span class="sxs-lookup"><span data-stu-id="2f8c4-227">View main thread activity</span></span>   

<span data-ttu-id="2f8c4-228">Utilisez la section **principale** pour afficher l’activité qui s’est produite sur le thread principal de la page.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-228">Use the **Main** section to view activity that occurred on the main thread of the page.</span></span>  

> ##### <span data-ttu-id="2f8c4-229">Figure14</span><span class="sxs-lookup"><span data-stu-id="2f8c4-229">Figure 14</span></span>  
> <span data-ttu-id="2f8c4-230">Section **principale**</span><span class="sxs-lookup"><span data-stu-id="2f8c4-230">The **Main** section</span></span>  
> ![Section principale][ImageMain]  

<span data-ttu-id="2f8c4-232">Cliquez sur un événement pour afficher des informations supplémentaires le concernant sous l’onglet **Résumé** .  DevTools souligne l’événement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-232">Click on an event to view more information about it in the **Summary** tab.  DevTools outlines the selected event.</span></span>  

> ##### <span data-ttu-id="2f8c4-233">Figure15</span><span class="sxs-lookup"><span data-stu-id="2f8c4-233">Figure 15</span></span>  
> <span data-ttu-id="2f8c4-234">Plus d’informations sur la `anonymous` fonction sous l’onglet **Résumé**</span><span class="sxs-lookup"><span data-stu-id="2f8c4-234">More information about the `anonymous` function in the **Summary** tab</span></span>  
> ![Plus d’informations sur la fonction anonyme sous l’onglet Résumé][ImageMainEventSummary]  

<span data-ttu-id="2f8c4-236">DevTools représente l’activité du thread principal avec un graphique à flamme.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-236">DevTools represents main thread activity with a flame chart.</span></span>  <span data-ttu-id="2f8c4-237">L’axe x représente l’enregistrement dans le temps.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-237">The x-axis represents the recording over time.</span></span>  <span data-ttu-id="2f8c4-238">L’axe y représente la pile d’appels.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-238">The y-axis represents the call stack.</span></span>  <span data-ttu-id="2f8c4-239">Les événements en haut déclenchent les événements situés au-dessous.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-239">The events on top cause the events below it.</span></span>  

> ##### <span data-ttu-id="2f8c4-240">Figure16</span><span class="sxs-lookup"><span data-stu-id="2f8c4-240">Figure 16</span></span>  
> <span data-ttu-id="2f8c4-241">Graphique à flamme dans la section **principale**</span><span class="sxs-lookup"><span data-stu-id="2f8c4-241">A flame chart in the **Main** section</span></span>  
> ![Un graphique en flamme][ImageFlameChart]  

<span data-ttu-id="2f8c4-243">Dans la [figure 16](#figure-16), un `click` événement a entraîné une `Function Call` `activitytabs.js` 53 sur ligne.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-243">In [Figure 16](#figure-16), a `click` event caused a `Function Call` in `activitytabs.js` on line 53.</span></span>  <span data-ttu-id="2f8c4-244">`Function Call`Vous pouvez voir ci-dessous qu’une fonction anonyme a été appelée.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-244">Below `Function Call` you see that an anonymous function was called.</span></span>  <span data-ttu-id="2f8c4-245">Fonction anonyme appelée, qui a été appelée `a` `wait` `Minor GC` .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-245">The anonymous function called `a`, which called `wait`, which called `Minor GC`.</span></span>  

<span data-ttu-id="2f8c4-246">DevTools attribue des couleurs aléatoires aux scripts.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-246">DevTools assigns scripts random colors.</span></span>  <span data-ttu-id="2f8c4-247">Dans la [figure 16](#figure-16), les appels de fonction à partir d’un script apparaissent en vert clair.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-247">In [Figure 16](#figure-16), function calls from one script are colored light green.</span></span>  <span data-ttu-id="2f8c4-248">Les appels d’un autre script sont de couleur beige.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-248">Calls from another script are colored beige.</span></span>  <span data-ttu-id="2f8c4-249">Le jaune foncé représente l’activité de création de scripts et l’événement violet représente l’activité de rendu.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-249">The darker yellow represents scripting activity, and the purple event represents rendering activity.</span></span>  <span data-ttu-id="2f8c4-250">Ces événements en jaune et violet plus foncés sont cohérents dans tous les enregistrements.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-250">These darker yellow and purple events are consistent across all recordings.</span></span>  

<span data-ttu-id="2f8c4-251">Pour masquer le graphique de flamme d’appels JavaScript, voir [Désactiver les exemples JavaScript](#disable-javascript-samples) .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-251">See [Disable JavaScript samples](#disable-javascript-samples) if you want to hide the detailed flame chart of JavaScript calls.</span></span>  <span data-ttu-id="2f8c4-252">Lorsque les exemples de JS sont désactivés, vous ne voyez que les événements de haut niveau, par exemple `Event: click` et `Function Call` de la [figure 16](#figure-16).</span><span class="sxs-lookup"><span data-stu-id="2f8c4-252">When JS samples are disabled, you only see high-level events such as `Event: click` and `Function Call` from [Figure 16](#figure-16).</span></span>  

### <span data-ttu-id="2f8c4-253">Afficher les activités d’un tableau</span><span class="sxs-lookup"><span data-stu-id="2f8c4-253">View activities in a table</span></span>   

<span data-ttu-id="2f8c4-254">Après avoir enregistré une page, il n’est pas nécessaire de dépendre uniquement de la section **principale** permettant d’analyser les activités.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-254">After recording a page, you do not need to rely solely on the **Main** section to analyze activities.</span></span>  <span data-ttu-id="2f8c4-255">DevTools fournit également trois vues tabulaires pour l’analyse des activités.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-255">DevTools also provides three tabular views for analyzing activities.</span></span>  <span data-ttu-id="2f8c4-256">Chaque affichage vous offre une perspective différente des activités:</span><span class="sxs-lookup"><span data-stu-id="2f8c4-256">Each view gives you a different perspective on the activities:</span></span>  

*   <span data-ttu-id="2f8c4-257">Pour afficher les activités racines qui génèrent le plus de tâches, utilisez [l’onglet **arborescence des appels** ](#the-call-tree-tab).</span><span class="sxs-lookup"><span data-stu-id="2f8c4-257">When you want to view the root activities that cause the most work, use [the **Call Tree** tab](#the-call-tree-tab).</span></span>  
*   <span data-ttu-id="2f8c4-258">Pour afficher les activités pour lesquelles le plus de temps est passé directement, utilisez [l’onglet **inférieur** ](#the-bottom-up-tab).</span><span class="sxs-lookup"><span data-stu-id="2f8c4-258">When you want to view the activities where the most time was directly spent, use [the **Bottom-Up** tab](#the-bottom-up-tab).</span></span>  
*   <span data-ttu-id="2f8c4-259">Si vous voulez afficher les activités dans l’ordre dans lequel elles se sont produites lors de l’enregistrement, utilisez [l’onglet **Journal des événements** ](#the-event-log-tab).</span><span class="sxs-lookup"><span data-stu-id="2f8c4-259">When you want to view the activities in the order in which they occurred during the recording, use [the **Event Log** tab](#the-event-log-tab).</span></span>  

> [!NOTE]
> <span data-ttu-id="2f8c4-260">Les trois sections suivantes se réfèrent à la même démonstration.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-260">The next three sections all refer to the same demo.</span></span>  <span data-ttu-id="2f8c4-261">Exécutez la démonstration vous-même dans les [onglets activité][ActivityTabsDemo].</span><span class="sxs-lookup"><span data-stu-id="2f8c4-261">Run the demo yourself at [Activity Tabs Demo][ActivityTabsDemo].</span></span>  

#### <span data-ttu-id="2f8c4-262">Activités racines</span><span class="sxs-lookup"><span data-stu-id="2f8c4-262">Root activities</span></span>   

<span data-ttu-id="2f8c4-263">Voici une description du concept d' **activités racines** mentionné dans les sections de l’onglet **arborescence des appels** , de **bas en haut** et **Journal des événements** .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-263">Here is an explanation of the **root activities** concept that is mentioned in the **Call Tree** tab, **Bottom-Up** tab, and **Event Log** sections.</span></span>  

<span data-ttu-id="2f8c4-264">Les activités racines peuvent entraîner le fonctionnement du navigateur.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-264">Root activities are those which cause the browser to do some work.</span></span>  <span data-ttu-id="2f8c4-265">Par exemple, lorsque vous cliquez sur une page, le navigateur déclenche une `Event` activité en tant qu’activité racine.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-265">For example, when you click a page, the browser fires an `Event` activity as the root activity.</span></span>  <span data-ttu-id="2f8c4-266">Cela `Event` peut entraîner l’exécution d’un gestionnaire et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-266">That `Event` might cause a handler to run, and so on.</span></span>  

<span data-ttu-id="2f8c4-267">Dans le graphique en flamme de la section **principale** , les activités racines se trouvent en haut du graphique.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-267">In the flame chart of the **Main** section, root activities are at the top of the chart.</span></span>  <span data-ttu-id="2f8c4-268">Dans les onglets **arborescence des appels** et **Journal des événements** , les activités racines sont les éléments de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-268">In the **Call Tree** and **Event Log** tabs, root activities are the top-level items.</span></span>  

<span data-ttu-id="2f8c4-269">Voir [l’onglet arborescence des appels](#the-call-tree-tab) pour obtenir un exemple d’activités racines.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-269">See [The Call Tree tab](#the-call-tree-tab) for an example of root activities.</span></span>  

#### <span data-ttu-id="2f8c4-270">Onglet arborescence des appels</span><span class="sxs-lookup"><span data-stu-id="2f8c4-270">The Call Tree tab</span></span>   

<span data-ttu-id="2f8c4-271">Utilisez l’onglet **arborescence des appels** pour afficher les [activités racines](#root-activities) qui sont à l’origine du problème.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-271">Use the **Call Tree** tab to view which [root activities](#root-activities) cause the most work.</span></span>  

<span data-ttu-id="2f8c4-272">L’onglet **arborescence des appels** affiche uniquement les activités effectuées au cours de la partie sélectionnée de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-272">The **Call Tree** tab only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="2f8c4-273">Pour plus d’informations sur la sélection de parties, voir [Sélectionner une portion d’un enregistrement](#select-a-portion-of-a-recording) .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-273">See [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

> ##### <span data-ttu-id="2f8c4-274">Figure17</span><span class="sxs-lookup"><span data-stu-id="2f8c4-274">Figure 17</span></span>  
> <span data-ttu-id="2f8c4-275">Onglet **arborescence des appels**</span><span class="sxs-lookup"><span data-stu-id="2f8c4-275">The **Call Tree** tab</span></span>  
> ![Onglet arborescence des appels][ImageCallTree]  

<span data-ttu-id="2f8c4-277">Dans la [figure 17](#figure-17), le niveau supérieur des éléments de la colonne **Activity** , par exemple, les `Evaluate Script` `Parse HTML` activités racines.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-277">In [Figure 17](#figure-17), the top-level of items in the **Activity** column, such as `Evaluate Script` and `Parse HTML` are root activities.</span></span>  <span data-ttu-id="2f8c4-278">L’imbrication représente la pile d’appels.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-278">The nesting represents the call stack.</span></span>  <span data-ttu-id="2f8c4-279">Par exemple, dans la [figure 17](#figure-17), `Parse HTML` qui a entraîné `Evaluate Script` `Compile Script` et `(anonymous)` .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-279">For example, in [Figure 17](#figure-17), `Parse HTML` which caused `Evaluate Script` which caused `Compile Script` and `(anonymous)`.</span></span>  

<span data-ttu-id="2f8c4-280">Le **temps libre** représente le temps passé directement dans cette activité.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-280">**Self Time** represents the time directly spent in that activity.</span></span>  <span data-ttu-id="2f8c4-281">**Durée totale** représente le temps passé à cette activité ou à un des enfants.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-281">**Total Time** represents the time spent in that activity or any of the children.</span></span>  

<span data-ttu-id="2f8c4-282">Cliquez sur **durée automatique**, **durée totale**ou **activité** pour trier le tableau selon la colonne.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-282">Click **Self Time**, **Total Time**, or **Activity** to sort the table by that column.</span></span>  

<span data-ttu-id="2f8c4-283">Utilisez la zone de texte **filtre** pour filtrer les événements par nom d’activité.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-283">Use the **Filter** text box to filter events by activity name.</span></span>  

<span data-ttu-id="2f8c4-284">Par défaut, le menu de **regroupement** a la valeur **aucun regroupement**.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-284">By default the **Grouping** menu is set to **No Grouping**.</span></span>  <span data-ttu-id="2f8c4-285">Utilisez le menu de **regroupement** pour trier la table d’activité en fonction de différents critères.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-285">Use the **Grouping** menu to sort the activity table based on various criteria.</span></span>  

<span data-ttu-id="2f8c4-286">Cliquez sur Afficher la pile la plus **lourde** ![ ][ImageShowHeaviestStackIcon] pour afficher une autre table à droite de la table **activité** .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-286">Click **Show Heaviest Stack** ![Show Heaviest Stack][ImageShowHeaviestStackIcon] to reveal another table to the right of the **Activity** table.</span></span>  <span data-ttu-id="2f8c4-287">Cliquez sur une activité pour remplir la table de pile la plus **lourde** .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-287">Click on an activity to populate the **Heaviest Stack** table.</span></span>  <span data-ttu-id="2f8c4-288">La table des piles les plus **lourdes** vous indique les enfants de l’activité sélectionnée qui prenaient le plus de temps à s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-288">The **Heaviest Stack** table shows you which children of the selected activity took the longest time to run.</span></span>  

#### <span data-ttu-id="2f8c4-289">Onglet inférieur</span><span class="sxs-lookup"><span data-stu-id="2f8c4-289">The Bottom-Up tab</span></span>   

<span data-ttu-id="2f8c4-290">Utilisez l’onglet **inférieur** pour afficher les activités qui consomment directement le plus de temps dans l’agrégat.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-290">Use the **Bottom-Up** tab to view which activities directly took up the most time in aggregate.</span></span>  

<span data-ttu-id="2f8c4-291">L’onglet **inférieur** affiche uniquement les activités effectuées au cours de la partie sélectionnée de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-291">The **Bottom-Up** tab only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="2f8c4-292">Pour plus d’informations sur la sélection de parties, voir [Sélectionner une portion d’un enregistrement](#select-a-portion-of-a-recording) .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-292">See [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

> ##### <span data-ttu-id="2f8c4-293">Figure 18</span><span class="sxs-lookup"><span data-stu-id="2f8c4-293">Figure 18</span></span>  
> <span data-ttu-id="2f8c4-294">Onglet **inférieur**</span><span class="sxs-lookup"><span data-stu-id="2f8c4-294">The **Bottom-Up** tab</span></span>  
> ![Onglet inférieur][ImageBottomUp]  

<span data-ttu-id="2f8c4-296">Dans le **graphique** en forme de flamme de la [figure 18](#figure-18), observez que presque tout le temps est passé en temps `Parse HTML` .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-296">In the **Main** section flame chart of [Figure 18](#figure-18), see that almost practically all of the time was spent running `Parse HTML`.</span></span>  <span data-ttu-id="2f8c4-297">Dans l’onglet **inférieur** de la [figure 18](#figure-18) , l’activité supérieure `Parse HTML` .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-297">The top activity in the **Bottom-Up** tab of [Figure 18](#figure-18) is `Parse HTML`.</span></span>  <!--In the flame chart of [Figure 18](#figure-18), the yellow below the calls to `wait` are actually thousands of `Minor GC` calls.  -->  <span data-ttu-id="2f8c4-298">Reportez-vous à la rubrique dans l’onglet en **bas** , l’activité la plus coûteuse suivante `Layout` .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-298">See in the **Bottom-Up** tab, the next most expensive activity is `Layout`.</span></span>  

<span data-ttu-id="2f8c4-299">La colonne de **temps libre** représente le temps agrégé passé directement dans cette activité, sur l’ensemble des occurrences.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-299">The **Self Time** column represents the aggregated time spent directly in that activity, across all of the occurrences.</span></span>  

<span data-ttu-id="2f8c4-300">La colonne **temps total** représente le temps agrégé dépensé dans cette activité ou sur n’importe quel enfant.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-300">The **Total Time** column represents aggregated time spent in that activity or any of the children.</span></span>  

#### <span data-ttu-id="2f8c4-301">Onglet journal des événements</span><span class="sxs-lookup"><span data-stu-id="2f8c4-301">The Event Log tab</span></span>   

<span data-ttu-id="2f8c4-302">Utilisez l’onglet **Journal des événements** pour afficher les activités dans l’ordre dans lequel elles se sont produites lors de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-302">Use the **Event Log** tab to view activities in the order in which they occurred during the recording.</span></span>  

<span data-ttu-id="2f8c4-303">L’onglet **Journal des événements** affiche uniquement les activités effectuées au cours de la partie sélectionnée de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-303">The **Event Log** tab only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="2f8c4-304">Pour plus d’informations sur la sélection de parties, voir [Sélectionner une portion d’un enregistrement](#select-a-portion-of-a-recording) .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-304">See [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

> ##### <span data-ttu-id="2f8c4-305">Figure 19</span><span class="sxs-lookup"><span data-stu-id="2f8c4-305">Figure 19</span></span>  
> <span data-ttu-id="2f8c4-306">Onglet **Journal des événements**</span><span class="sxs-lookup"><span data-stu-id="2f8c4-306">The **Event Log** tab</span></span>  
> ![Onglet journal des événements][ImageEventLog]  

<span data-ttu-id="2f8c4-308">La colonne **heure de début** représente le point auquel cette activité a commencé, par rapport au début de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-308">The **Start Time** column represents the point at which that activity started, relative to the start of the recording.</span></span>  <span data-ttu-id="2f8c4-309">Par exemple, l’heure de début de `175.7 ms` l’élément sélectionné dans la [figure 19](#figure-19) signifie que l’activité a démarré 175,7 ms après le début de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-309">For example, the start time of `175.7 ms` for the selected item in [Figure 19](#figure-19) means that activity started 175.7 ms after the recording started.</span></span>  

<span data-ttu-id="2f8c4-310">La colonne **temps libre** représente le temps passé directement dans cette activité.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-310">The **Self Time** column represents the time spent directly in that activity.</span></span>  

<span data-ttu-id="2f8c4-311">Le **nombre total** de colonnes durée représente le temps passé directement dans cette activité ou dans n’importe quel enfant.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-311">The **Total Time** columns represents time spent directly in that activity or in any of the children.</span></span>  

<span data-ttu-id="2f8c4-312">Cliquez sur **heure de début**, **durée automatique**ou **durée totale** pour trier le tableau selon la colonne.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-312">Click **Start Time**, **Self Time**, or **Total Time** to sort the table by that column.</span></span>

<span data-ttu-id="2f8c4-313">Utilisez la zone de texte **filtre** pour filtrer les activités par nom.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-313">Use the **Filter** text box to filter activities by name.</span></span>  

<span data-ttu-id="2f8c4-314">Utilisez le menu **durée** pour filtrer les activités ayant eu moins de 1 ms ou 15 ms.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-314">Use the **Duration** menu to filter out any activities that took less than 1 ms or 15 ms.</span></span>  <span data-ttu-id="2f8c4-315">Par défaut, le menu **durée** est défini sur **tout**, ce qui signifie que toutes les activités sont affichées.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-315">By default the **Duration** menu is set to **All**, meaning all activities are shown.</span></span>  

<span data-ttu-id="2f8c4-316">Désactivez les cases à cocher **chargement**, **script**, **rendu**ou **peinture** pour filtrer toutes les activités de ces catégories.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-316">Disable the **Loading**, **Scripting**, **Rendering**, or **Painting** checkboxes to filter out all activities from those categories.</span></span>  

### <span data-ttu-id="2f8c4-317">Afficher l’activité GPU</span><span class="sxs-lookup"><span data-stu-id="2f8c4-317">View GPU activity</span></span>   

<span data-ttu-id="2f8c4-318">Afficher l’activité GPU dans la section **GPU** .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-318">View GPU activity in the **GPU** section.</span></span>  

> ##### <span data-ttu-id="2f8c4-319">Figure 20</span><span class="sxs-lookup"><span data-stu-id="2f8c4-319">Figure 20</span></span>  
> <span data-ttu-id="2f8c4-320">Section **GPU**</span><span class="sxs-lookup"><span data-stu-id="2f8c4-320">The **GPU** section</span></span>  
> ![Section GPU][ImageGpu]  

### <span data-ttu-id="2f8c4-322">Afficher les activités pixellisées</span><span class="sxs-lookup"><span data-stu-id="2f8c4-322">View raster activity</span></span>   

<span data-ttu-id="2f8c4-323">Affichez les activités pixellisées dans la section **Raster** .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-323">View raster activity in the **Raster** section.</span></span>  

> ##### <span data-ttu-id="2f8c4-324">Figure 21</span><span class="sxs-lookup"><span data-stu-id="2f8c4-324">Figure 21</span></span>  
> <span data-ttu-id="2f8c4-325">Section **Raster**</span><span class="sxs-lookup"><span data-stu-id="2f8c4-325">The **Raster** section</span></span>  
> ![Section raster][ImageRaster]  

### <span data-ttu-id="2f8c4-327">Afficher les interactions</span><span class="sxs-lookup"><span data-stu-id="2f8c4-327">View interactions</span></span>   

<span data-ttu-id="2f8c4-328">Utilisez la section **interactions** pour rechercher et analyser les interactions utilisateur qui se sont produites lors de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-328">Use the **Interactions** section to find and analyze user interactions that happened during the recording.</span></span>  

> ##### <span data-ttu-id="2f8c4-329">Figure 22</span><span class="sxs-lookup"><span data-stu-id="2f8c4-329">Figure 22</span></span>  
> <span data-ttu-id="2f8c4-330">Section **interactions**</span><span class="sxs-lookup"><span data-stu-id="2f8c4-330">The **Interactions** section</span></span>  
> ![Section interactions][ImageInteractions]  

<span data-ttu-id="2f8c4-332">Une ligne rouge en bas d’une interaction représente le temps passé à attendre le thread principal.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-332">A red line at the bottom of an interaction represents time spent waiting for the main thread.</span></span>  

<span data-ttu-id="2f8c4-333">Cliquez sur une interaction pour afficher davantage d’informations sur celle-ci sous l’onglet **Résumé** .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-333">Click an interaction to view more information about it in the **Summary** tab.</span></span>  

### <span data-ttu-id="2f8c4-334">Analyser les images par seconde (FPS)</span><span class="sxs-lookup"><span data-stu-id="2f8c4-334">Analyze frames per second (FPS)</span></span>   

<span data-ttu-id="2f8c4-335">DevTools offre de nombreuses façons d’analyser les images par seconde:</span><span class="sxs-lookup"><span data-stu-id="2f8c4-335">DevTools provides numerous ways to analyze frames per second:</span></span>  

*   <span data-ttu-id="2f8c4-336">Utilisez [le graphique **fps** ](#the-fps-chart) pour obtenir une vue d’ensemble des images par seconde au fil de la durée de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-336">Use [the **FPS** chart](#the-fps-chart) to get an overview of FPS over the duration of the recording.</span></span>  
*   <span data-ttu-id="2f8c4-337">Utilisez [la section **cadres** ](#the-frames-section) pour afficher la durée d’une image particulière.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-337">Use [the **Frames** section](#the-frames-section) to view how long a particular frame took.</span></span>  
*   <span data-ttu-id="2f8c4-338">Utilisez le **compteur fps** pour une estimation en temps réel de FPS lors de l’exécution de la page.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-338">Use the **FPS meter** for a realtime estimate of FPS as the page runs.</span></span>  <span data-ttu-id="2f8c4-339">Voir [trames d’affichage par seconde en temps réel avec le compteur fps](#view-frames-per-second-in-realtime-with-the-fps-meter).</span><span class="sxs-lookup"><span data-stu-id="2f8c4-339">See [View frames per second in realtime with the FPS meter](#view-frames-per-second-in-realtime-with-the-fps-meter).</span></span>  

#### <span data-ttu-id="2f8c4-340">Graphique FPS</span><span class="sxs-lookup"><span data-stu-id="2f8c4-340">The FPS chart</span></span>   

<span data-ttu-id="2f8c4-341">Le graphique **fps** fournit une vue d’ensemble de la fréquence d’images sur la durée d’un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-341">The **FPS** chart provides an overview of the frame rate across the duration of a recording.</span></span>  <span data-ttu-id="2f8c4-342">En règle générale, plus la barre verte est élevée, plus la fréquence d’images est élevée.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-342">In general, the higher the green bar, the better the frame rate.</span></span>  

<span data-ttu-id="2f8c4-343">Une barre rouge au-dessus du graphique **fps** est une alerte indiquant que le taux d’images a été interrompu comme faible et qu’il a probablement été lésé par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-343">A red bar above the **FPS** chart is a warning that the frame rate dropped so low that it probably harmed the user's experience.</span></span>  

> ##### <span data-ttu-id="2f8c4-344">Figure 23</span><span class="sxs-lookup"><span data-stu-id="2f8c4-344">Figure 23</span></span>  
> <span data-ttu-id="2f8c4-345">Graphique FPS</span><span class="sxs-lookup"><span data-stu-id="2f8c4-345">The FPS chart</span></span>  
> ![Graphique FPS][ImageFpsChart]  

#### <span data-ttu-id="2f8c4-347">Section cadres</span><span class="sxs-lookup"><span data-stu-id="2f8c4-347">The Frames section</span></span>   

<span data-ttu-id="2f8c4-348">La section **trames** vous indique exactement le temps qu’une image donnée a duré.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-348">The **Frames** section tells you exactly how long a particular frame took.</span></span>  

<span data-ttu-id="2f8c4-349">Pointez sur un cadre pour afficher une info-bulle contenant des informations supplémentaires à son sujet.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-349">Hover over a frame to view a tooltip with more information about it.</span></span>  

> ##### <span data-ttu-id="2f8c4-350">Figure 24</span><span class="sxs-lookup"><span data-stu-id="2f8c4-350">Figure 24</span></span>  
> <span data-ttu-id="2f8c4-351">Survol d’un cadre</span><span class="sxs-lookup"><span data-stu-id="2f8c4-351">Hovering over a frame</span></span>  
> ![Survol d’un cadre][ImageFramesSection]  

<span data-ttu-id="2f8c4-353">Cliquez sur un cadre pour afficher encore plus d’informations sur le cadre sous l’onglet **Résumé** .  DevTools plan le cadre sélectionné en bleu.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-353">Click on a frame to view even more information about the frame in the **Summary** tab.  DevTools outlines the selected frame in blue.</span></span>  

> ##### <span data-ttu-id="2f8c4-354">Figure 25</span><span class="sxs-lookup"><span data-stu-id="2f8c4-354">Figure 25</span></span>  
> <span data-ttu-id="2f8c4-355">Affichage d’un cadre sous l’onglet **Résumé**</span><span class="sxs-lookup"><span data-stu-id="2f8c4-355">Viewing a frame in the **Summary** tab</span></span>  
> ![Affichage d’un cadre sous l’onglet Résumé][ImageFrameSummary]  

### <span data-ttu-id="2f8c4-357">Afficher les requêtes réseau</span><span class="sxs-lookup"><span data-stu-id="2f8c4-357">View network requests</span></span>   

<span data-ttu-id="2f8c4-358">Développez la section **réseau** pour afficher une cascade de requêtes réseau qui se sont produites lors de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-358">Expand the **Network** section to view a waterfall of network requests that occurred during the recording.</span></span>  

> ##### <span data-ttu-id="2f8c4-359">Figure 26</span><span class="sxs-lookup"><span data-stu-id="2f8c4-359">Figure 26</span></span>  
> <span data-ttu-id="2f8c4-360">Section **réseau**</span><span class="sxs-lookup"><span data-stu-id="2f8c4-360">The **Network** section</span></span>  
> ![Section réseau][ImageNetworkRequest]  

<span data-ttu-id="2f8c4-362">Les requêtes sont codées en couleur comme suit:</span><span class="sxs-lookup"><span data-stu-id="2f8c4-362">Requests are color-coded as follows:</span></span>  

*   <span data-ttu-id="2f8c4-363">HTML: bleu</span><span class="sxs-lookup"><span data-stu-id="2f8c4-363">HTML: Blue</span></span>  
*   <span data-ttu-id="2f8c4-364">CSS: pourpre</span><span class="sxs-lookup"><span data-stu-id="2f8c4-364">CSS: Purple</span></span>  
*   <span data-ttu-id="2f8c4-365">JS: jaune</span><span class="sxs-lookup"><span data-stu-id="2f8c4-365">JS: Yellow</span></span>  
*   <span data-ttu-id="2f8c4-366">Images: vert</span><span class="sxs-lookup"><span data-stu-id="2f8c4-366">Images: Green</span></span>  

<span data-ttu-id="2f8c4-367">Cliquez sur une demande pour afficher davantage d’informations sur celle-ci sous l’onglet **Résumé** .  Par exemple, dans l' [illustration 26](#figure-26) , l’onglet **synthèse** affiche des informations supplémentaires sur la requête bleue sélectionnée dans la section **réseau** .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-367">Click on a request to view more information about it in the **Summary** tab.  For example, in [Figure 26](#figure-26) the **Summary** tab is displaying more information about the blue request that is selected in the **Network** section.</span></span>  

<span data-ttu-id="2f8c4-368">Dans le coin supérieur gauche d’une demande, un carré plus foncé est une demande de priorité élevée.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-368">A darker-blue square in the top-left of a request means it is a higher-priority request.</span></span>  <span data-ttu-id="2f8c4-369">Le carré bleu plus clair correspond à un niveau de priorité inférieur.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-369">A lighter-blue square means lower-priority.</span></span>  <span data-ttu-id="2f8c4-370">Par exemple, dans l' [illustration 26](#figure-26) , le bleu, la requête sélectionnée est d’une priorité plus élevée et le vert au-dessous, de priorité inférieure.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-370">For example, in [Figure 26](#figure-26) the blue, selected request is higher-priority, and the green one below it is lower-priority.</span></span>  

<span data-ttu-id="2f8c4-371">Dans la [figure 27](#figure-27), la requête pour `www.bing.com` est représentée par une ligne à gauche, une barre au milieu avec une partie sombre et une partie claire, et une ligne à droite.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-371">In [Figure 27](#figure-27), the request for `www.bing.com` is represented by a line on the left, a bar in the middle with a dark portion and a light portion, and a line on the right.</span></span>  <span data-ttu-id="2f8c4-372">La [figure 28](#figure-28) montre la représentation correspondante de la même requête dans l’onglet **minutage** du panneau **réseau** .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-372">[Figure 28](#figure-28) shows the corresponding representation of the same request in the **Timing** tab of the **Network** panel.</span></span>  <span data-ttu-id="2f8c4-373">Voici à quoi correspondent les deux représentations suivantes:</span><span class="sxs-lookup"><span data-stu-id="2f8c4-373">Here is how these two representations map to each other:</span></span>

*   <span data-ttu-id="2f8c4-374">La ligne gauche représente tout ce qui concerne le `Connection Start` groupe d’événements compris.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-374">The left line is everything up to the `Connection Start` group of events, inclusive.</span></span>  <span data-ttu-id="2f8c4-375">En d’autres termes, il s’agit de tout ce qui est auparavant `Request Sent` , exclusif.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-375">In other words, it is everything before `Request Sent`, exclusive.</span></span>  
*   <span data-ttu-id="2f8c4-376">La partie claire de la barre est `Request Sent` et `Waiting (TTFB)` .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-376">The light portion of the bar is `Request Sent` and `Waiting (TTFB)`.</span></span>  
*   <span data-ttu-id="2f8c4-377">La partie sombre de la barre est `Content Download` .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-377">The dark portion of the bar is `Content Download`.</span></span>  
*   <span data-ttu-id="2f8c4-378">La ligne droite correspond essentiellement au délai passé pour le thread principal.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-378">The right line is essentially time spent waiting for the main thread.</span></span>  <span data-ttu-id="2f8c4-379">Cette opération n’est pas représentée dans l’onglet **minutage** .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-379">This is not represented in the **Timing** tab.</span></span>  

> ##### <span data-ttu-id="2f8c4-380">Figure 27</span><span class="sxs-lookup"><span data-stu-id="2f8c4-380">Figure 27</span></span>  
> <span data-ttu-id="2f8c4-381">Représentation de la barre de lignes de la `www.bing.com` requête</span><span class="sxs-lookup"><span data-stu-id="2f8c4-381">The line-bar representation of the `www.bing.com` request</span></span>  
> ![Représentation de la barre de lignes de la requête www.bing.com][ImageLineBar]  

> ##### <span data-ttu-id="2f8c4-383">Figure 28</span><span class="sxs-lookup"><span data-stu-id="2f8c4-383">Figure 28</span></span>  
> <span data-ttu-id="2f8c4-384">Représentation de l’onglet **minutage** de la `www.bing.com` requête</span><span class="sxs-lookup"><span data-stu-id="2f8c4-384">The **Timing** tab representation of the `www.bing.com` request</span></span>  
> ![Section réseau][ImageTiming]  

### <span data-ttu-id="2f8c4-386">Afficher les métriques de mémoire</span><span class="sxs-lookup"><span data-stu-id="2f8c4-386">View memory metrics</span></span>   

<span data-ttu-id="2f8c4-387">Activez la case à cocher **mémoire** pour afficher les mesures de mémoire du dernier enregistrement.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-387">Enable the **Memory** checkbox to view memory metrics from the last recording.</span></span>  

> ##### <span data-ttu-id="2f8c4-388">Figure 29</span><span class="sxs-lookup"><span data-stu-id="2f8c4-388">Figure 29</span></span>  
> <span data-ttu-id="2f8c4-389">Case à cocher **mémoire**</span><span class="sxs-lookup"><span data-stu-id="2f8c4-389">The **Memory** checkbox</span></span>  
> ![Case à cocher mémoire][ImageMemory]  

<span data-ttu-id="2f8c4-391">DevTools affiche un nouveau graphique **mémoire** , au-dessus de l’onglet **Résumé** .  Il existe également un nouveau graphique sous le graphique **net** , appelé **tas**.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-391">DevTools displays a new **Memory** chart, above the **Summary** tab.  There is also a new chart below the **NET** chart, called **HEAP**.</span></span>  <span data-ttu-id="2f8c4-392">Le graphique de **tas** fournit les mêmes informations que la ligne de segment de **mémoire** **js** dans le graphique mémoire.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-392">The **HEAP** chart provides the same information as the **JS Heap** line in the **Memory** chart.</span></span>  

> ##### <span data-ttu-id="2f8c4-393">Figure 30</span><span class="sxs-lookup"><span data-stu-id="2f8c4-393">Figure 30</span></span>  
> <span data-ttu-id="2f8c4-394">Métriques de mémoire, au-dessus de l’onglet **Résumé**</span><span class="sxs-lookup"><span data-stu-id="2f8c4-394">Memory metrics, above the **Summary** tab</span></span>  
> ![Métriques de mémoire][ImageMemoryMetrics]  

<span data-ttu-id="2f8c4-396">Les lignes de couleur sur le graphique correspondent aux cases à cocher en plus de la couleur du graphique.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-396">The colored lines on the chart map to the colored checkboxes above the chart.</span></span>  
<span data-ttu-id="2f8c4-397">Désactivez une case à cocher pour masquer cette catégorie dans le graphique.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-397">Disable a checkbox to hide that category from the chart.</span></span>  

<span data-ttu-id="2f8c4-398">Le graphique affiche uniquement la zone de l’enregistrement actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-398">The chart only displays the region of the recording that is currently selected.</span></span>  <span data-ttu-id="2f8c4-399">Par exemple, dans la [figure 30](#figure-30), le graphique **mémoire** affiche uniquement l’utilisation de la mémoire de la marque 400 MS au 1750 ms.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-399">For example, in [Figure 30](#figure-30), the **Memory** chart is only showing memory usage from around the 400 ms mark to the 1750 ms mark.</span></span>  

### <span data-ttu-id="2f8c4-400">Affichage de la durée d’une portion d’un enregistrement</span><span class="sxs-lookup"><span data-stu-id="2f8c4-400">View the duration of a portion of a recording</span></span>   

<span data-ttu-id="2f8c4-401">Lors de l’analyse d’une section comme **Network** ou **principal**, il est possible que vous ayez besoin d’une estimation plus précise de la durée de certains événements.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-401">When analyzing a section like **Network** or **Main**, sometimes you need a more precise estimate of how long certain events took.</span></span>  <span data-ttu-id="2f8c4-402">Maintenez la touche enfoncée, `Shift` puis faites glisser vers la gauche ou la droite pour sélectionner une partie de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-402">Hold `Shift`, click and hold, and drag left or right to select a portion of the recording.</span></span>  <span data-ttu-id="2f8c4-403">Dans la partie inférieure de votre sélection, DevTools indique la durée de la partie.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-403">At the bottom of your selection, DevTools shows how long that portion took.</span></span>  

> ##### <span data-ttu-id="2f8c4-404">Figure 31</span><span class="sxs-lookup"><span data-stu-id="2f8c4-404">Figure 31</span></span>  
> <span data-ttu-id="2f8c4-405">L' `9.47ms` horodatage en bas de la partie sélectionnée indique la durée de la partie.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-405">The `9.47ms` timestamp at the bottom of the selected portion indicates how long that portion took</span></span>  
> ![Affichage de la durée d’une portion d’un enregistrement][ImageDuration]  

### <span data-ttu-id="2f8c4-407">Affichage d’une capture d’écran</span><span class="sxs-lookup"><span data-stu-id="2f8c4-407">View a screenshot</span></span>   

<span data-ttu-id="2f8c4-408">Pour plus d’informations sur l’activation des captures d’écran, voir capturer des captures [d’écran lors de l’enregistrement](#capture-screenshots-while-recording) .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-408">See [Capture screenshots while recording](#capture-screenshots-while-recording) to learn how to enable screenshots.</span></span>  

<span data-ttu-id="2f8c4-409">Placez le pointeur de la souris sur la **vue d’ensemble** pour afficher une capture d’écran illustrant l’apparence de la page pendant ce moment de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-409">Hover over the **Overview** to view a screenshot of how the page looked during that moment of the recording.</span></span>  <span data-ttu-id="2f8c4-410">La section **vue d’ensemble** contient les graphiques **UC**, **fps**et **net** .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-410">The **Overview** is the section that contains the **CPU**, **FPS**, and **NET** charts.</span></span>  

> ##### <span data-ttu-id="2f8c4-411">Figure 32</span><span class="sxs-lookup"><span data-stu-id="2f8c4-411">Figure 32</span></span>  
> <span data-ttu-id="2f8c4-412">Affichage d’une capture d’écran</span><span class="sxs-lookup"><span data-stu-id="2f8c4-412">Viewing a screenshot</span></span>  
> ![Affichage d’une capture d’écran][ImageViewScreenshot]  

<span data-ttu-id="2f8c4-414">Vous pouvez également afficher les captures d’écran en cliquant sur un cadre dans la section **cadres** .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-414">You may also view screenshots by clicking a frame in the **Frames** section.</span></span>  <span data-ttu-id="2f8c4-415">DevTools affiche une version miniature de la capture d’écran sous l’onglet **Résumé** .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-415">DevTools displays a small version of the screenshot in the **Summary** tab.</span></span>  

> ##### <span data-ttu-id="2f8c4-416">Figure 33</span><span class="sxs-lookup"><span data-stu-id="2f8c4-416">Figure 33</span></span>  
> <span data-ttu-id="2f8c4-417">Après avoir cliqué sur le `233.9ms` cadre **Frames** dans la section cadre, la capture d’écran de ce cadre est affichée sous l’onglet **Résumé** .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-417">After clicking the `233.9ms` frame in the **Frames** section, the screenshot for that frame is displayed in the **Summary** tab</span></span>  
> ![Affichage d’une capture d’écran sous l’onglet Résumé][ImageFrameScreenshotSummary]  

<span data-ttu-id="2f8c4-419">Pour effectuer un zoom avant dans la capture d’écran, cliquez sur la miniature sous l’onglet **Résumé** .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-419">Click the thumbnail in the **Summary** tab to zoom in on the screenshot.</span></span>  

> ##### <span data-ttu-id="2f8c4-420">Figure 34</span><span class="sxs-lookup"><span data-stu-id="2f8c4-420">Figure 34</span></span>  
> <span data-ttu-id="2f8c4-421">Après avoir cliqué sur la miniature sous l’onglet **Résumé** , devtools effectue un zoom avant dans la capture d’écran</span><span class="sxs-lookup"><span data-stu-id="2f8c4-421">After clicking the thumbnail in the **Summary** tab, DevTools zooms in on the screenshot</span></span>  
> ![Zoom avant d’une capture d’écran à partir de l’onglet Résumé][ImageFrameScreenshotZoom]  

### <span data-ttu-id="2f8c4-423">Afficher les informations sur les couches</span><span class="sxs-lookup"><span data-stu-id="2f8c4-423">View layers information</span></span>   

<span data-ttu-id="2f8c4-424">Pour afficher des informations sur les couches avancées d’une image:</span><span class="sxs-lookup"><span data-stu-id="2f8c4-424">To view advanced layers information about a frame:</span></span>  

1.  <span data-ttu-id="2f8c4-425">[Activez Advanced Paint instrumentation](#enable-advanced-paint-instrumentation).</span><span class="sxs-lookup"><span data-stu-id="2f8c4-425">[Enable advanced paint instrumentation](#enable-advanced-paint-instrumentation).</span></span>  
1.  <span data-ttu-id="2f8c4-426">Sélectionnez une image dans la section **cadre** .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-426">Select a frame in the **Frames** section.</span></span>  <span data-ttu-id="2f8c4-427">DevTools affiche des informations sur les calques sous l’onglet nouveau **calques** , en regard de l’onglet **Journal des événements** .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-427">DevTools displays information about the layers in the new **Layers** tab, next to the **Event Log** tab.</span></span>  
    
    > ##### <span data-ttu-id="2f8c4-428">Figure 35</span><span class="sxs-lookup"><span data-stu-id="2f8c4-428">Figure 35</span></span>  
    > <span data-ttu-id="2f8c4-429">Volet **couches**</span><span class="sxs-lookup"><span data-stu-id="2f8c4-429">The **Layers** pane</span></span>  
    > ![Volet couches][ImageLayers]  
    
<span data-ttu-id="2f8c4-431">Pointez sur un calque pour le mettre en surbrillance dans le diagramme.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-431">Hover over a layer to highlight it in the diagram.</span></span>  

> ##### <span data-ttu-id="2f8c4-432">Figure 36</span><span class="sxs-lookup"><span data-stu-id="2f8c4-432">Figure 36</span></span>  
> <span data-ttu-id="2f8c4-433">Mise en surbrillance du calque **#39**</span><span class="sxs-lookup"><span data-stu-id="2f8c4-433">Highlighting layer **#39**</span></span>  
> ![Mise en surbrillance d’un calque][ImageLayerHover]  

<span data-ttu-id="2f8c4-435">Pour déplacer le diagramme:</span><span class="sxs-lookup"><span data-stu-id="2f8c4-435">To move the diagram:</span></span>  

*   <span data-ttu-id="2f8c4-436">Cliquez sur le mode panoramique **mode panoramique** ![ ][ImagePanModeIcon] pour vous déplacer sur les axes X et Y.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-436">Click **Pan Mode** ![Pan Mode][ImagePanModeIcon] to move along the X and Y axes.</span></span>  
*   <span data-ttu-id="2f8c4-437">**Rotate Mode** ![ ][ImageRotateModeIcon] Pour faire pivoter le mode de rotation, cliquez sur l’axe Z.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-437">Click **Rotate Mode** ![Rotate Mode][ImageRotateModeIcon] to rotate along the Z axis.</span></span>  
*   <span data-ttu-id="2f8c4-438">Cliquez sur **Réinitialiser** ![ la transformation réinitialiser ][ImageResetTransformIcon] la transformation pour rétablir la position d’origine du diagramme.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-438">Click **Reset Transform** ![Reset Transform][ImageResetTransformIcon] to reset the diagram to the original position.</span></span>  

### <span data-ttu-id="2f8c4-439">Afficher le générateur de dessin Paint</span><span class="sxs-lookup"><span data-stu-id="2f8c4-439">View paint profiler</span></span>   

<span data-ttu-id="2f8c4-440">Pour afficher des informations détaillées sur un événement Paint:</span><span class="sxs-lookup"><span data-stu-id="2f8c4-440">To view advanced information about a paint event:</span></span>  

1.  <span data-ttu-id="2f8c4-441">[Activez Advanced Paint instrumentation](#enable-advanced-paint-instrumentation).</span><span class="sxs-lookup"><span data-stu-id="2f8c4-441">[Enable advanced paint instrumentation](#enable-advanced-paint-instrumentation).</span></span>  
1.  <span data-ttu-id="2f8c4-442">Sélectionnez un événement **Paint** dans la section **principale** .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-442">Select a **Paint** event in the **Main** section.</span></span>  
    
    > ##### <span data-ttu-id="2f8c4-443">Figure 37</span><span class="sxs-lookup"><span data-stu-id="2f8c4-443">Figure 37</span></span>  
    > <span data-ttu-id="2f8c4-444">Onglet **Paint Profiler1.1**</span><span class="sxs-lookup"><span data-stu-id="2f8c4-444">The **Paint Profiler** tab</span></span>  
    > ![Onglet Paint Profiler1.1][ImagePaintProfiler]  
    
## <span data-ttu-id="2f8c4-446">Analyser les performances de rendu à l’aide de l’onglet rendu</span><span class="sxs-lookup"><span data-stu-id="2f8c4-446">Analyze rendering performance with the Rendering tab</span></span>   

<span data-ttu-id="2f8c4-447">Utilisez les fonctionnalités de l’onglet **rendu** pour visualiser les performances de rendu de votre page.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-447">Use the features of the **Rendering** tab to help visualize the rendering performance of your page.</span></span>  

<span data-ttu-id="2f8c4-448">Pour ouvrir l’onglet **rendu** :</span><span class="sxs-lookup"><span data-stu-id="2f8c4-448">To open the **Rendering** tab:</span></span>  

1.  <span data-ttu-id="2f8c4-449">[Ouvrir le menu de commandes][DevToolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="2f8c4-449">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="2f8c4-450">Commencez à taper `Rendering` et sélectionnez `Show Rendering` .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-450">Start typing `Rendering` and select `Show Rendering`.</span></span>  <span data-ttu-id="2f8c4-451">DevTools affiche l’onglet **rendu** en bas de votre fenêtre devtools.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-451">DevTools displays the **Rendering** tab at the bottom of your DevTools window.</span></span>  
    
    > ##### <span data-ttu-id="2f8c4-452">Figure 38</span><span class="sxs-lookup"><span data-stu-id="2f8c4-452">Figure 38</span></span>  
    > <span data-ttu-id="2f8c4-453">Onglet **rendu**</span><span class="sxs-lookup"><span data-stu-id="2f8c4-453">The **Rendering** tab</span></span>  
    > ![Onglet rendu][ImageRenderingTab]  
    
### <span data-ttu-id="2f8c4-455">Afficher les images par seconde en temps réel avec le compteur FPS</span><span class="sxs-lookup"><span data-stu-id="2f8c4-455">View frames per second in realtime with the FPS meter</span></span>   

<span data-ttu-id="2f8c4-456">Le **compteur fps** est une superposition qui s’affiche dans le coin supérieur droit de votre fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-456">The **FPS meter** is an overlay that appears in the top-right corner of your viewport.</span></span>  <span data-ttu-id="2f8c4-457">Il fournit une estimation en temps réel de FPS lors de l’exécution de la page.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-457">It provides a realtime estimate of FPS as the page runs.</span></span>  <span data-ttu-id="2f8c4-458">Pour ouvrir le **compteur fps**:</span><span class="sxs-lookup"><span data-stu-id="2f8c4-458">To open the **FPS meter**:</span></span>  

1.  <span data-ttu-id="2f8c4-459">Ouvrez l’onglet **rendu** .  [Pour plus d’efficacité, voir analyser les performances de rendu avec l’onglet rendu](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="2f8c4-459">Open the **Rendering** tab.  See [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="2f8c4-460">Activez la case à cocher **vumètre** .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-460">Enable the **FPS Meter** checkbox.</span></span>  
    
    > ##### <span data-ttu-id="2f8c4-461">Figure 39</span><span class="sxs-lookup"><span data-stu-id="2f8c4-461">Figure 39</span></span>  
    > <span data-ttu-id="2f8c4-462">Vumètre FPS</span><span class="sxs-lookup"><span data-stu-id="2f8c4-462">The FPS meter</span></span>  
    > ![Vumètre FPS][ImageFpsMeter]  
    
### <span data-ttu-id="2f8c4-464">Afficher les événements de peinture en temps réel avec le clignotement de la peinture</span><span class="sxs-lookup"><span data-stu-id="2f8c4-464">View painting events in realtime with Paint Flashing</span></span>   

<span data-ttu-id="2f8c4-465">Utilisez la fonction Paint clignotante pour obtenir une vue en temps réel de tous les événements de peinture sur la page.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-465">Use Paint Flashing to get a realtime view of all paint events on the page.</span></span>  <span data-ttu-id="2f8c4-466">Dès qu’une partie de la page est de nouveau peinte, DevTools la place en vert.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-466">Whenever a part of the page gets re-painted, DevTools outlines that section in green.</span></span>  

<span data-ttu-id="2f8c4-467">Pour activer le clignotement des peintures:</span><span class="sxs-lookup"><span data-stu-id="2f8c4-467">To enable Paint Flashing:</span></span>  

1.  <span data-ttu-id="2f8c4-468">Ouvrez l’onglet **rendu** .  [Pour plus d’efficacité, voir analyser les performances de rendu avec l’onglet rendu](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="2f8c4-468">Open the **Rendering** tab.  See [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="2f8c4-469">Activez la case à cocher **Paint clignotant** .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-469">Enable the **Paint Flashing** checkbox.</span></span>  
    
    > ##### <span data-ttu-id="2f8c4-470">Figure 40</span><span class="sxs-lookup"><span data-stu-id="2f8c4-470">Figure 40</span></span>  
    > **<span data-ttu-id="2f8c4-471">Paint clignotant</span><span class="sxs-lookup"><span data-stu-id="2f8c4-471">Paint Flashing</span></span>**  
    > ![Paint clignotant][ImagePaintFlashing]  
    
### <span data-ttu-id="2f8c4-473">Afficher une superposition de calques avec des bordures de calque</span><span class="sxs-lookup"><span data-stu-id="2f8c4-473">View an overlay of layers with Layer Borders</span></span>   

<span data-ttu-id="2f8c4-474">Utilisez les **bordures de calque** pour afficher une superposition des bordures et des vignettes du calque en haut de la page.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-474">Use **Layer Borders** to view an overlay of layer borders and tiles on top of the page.</span></span>  

<span data-ttu-id="2f8c4-475">Pour activer les bordures de calque:</span><span class="sxs-lookup"><span data-stu-id="2f8c4-475">To enable Layer Borders:</span></span>  

1.  <span data-ttu-id="2f8c4-476">Ouvrez l’onglet **rendu** .  [Pour plus d’efficacité, voir analyser les performances de rendu avec l’onglet rendu](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="2f8c4-476">Open the **Rendering** tab.  See [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="2f8c4-477">Activez la case à cocher **bordures de calque** .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-477">Enable the **Layer Borders** checkbox.</span></span>  
    
    > ##### <span data-ttu-id="2f8c4-478">Figure 41</span><span class="sxs-lookup"><span data-stu-id="2f8c4-478">Figure 41</span></span>  
    > **<span data-ttu-id="2f8c4-479">Bordures de calque</span><span class="sxs-lookup"><span data-stu-id="2f8c4-479">Layer Borders</span></span>**  
    > ![Bordures de calque][ImageLayerBorders]  
    
<span data-ttu-id="2f8c4-481">[`debug_colors.cc`][ChromiumDebugColors]Pour obtenir une description des codes de couleur, voir les commentaires.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-481">See the comments in [`debug_colors.cc`][ChromiumDebugColors] for an explanation of the color-codings.</span></span>  

### <span data-ttu-id="2f8c4-482">Rechercher des problèmes de performances de défilement en temps réel</span><span class="sxs-lookup"><span data-stu-id="2f8c4-482">Find scroll performance issues in realtime</span></span>   

<span data-ttu-id="2f8c4-483">Utilisez des problèmes de performances de défilement pour identifier les éléments de la page qui comportent des écouteurs d’événements liés au défilement qui peuvent nuire aux performances de la page.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-483">Use Scrolling Performance Issues to identify elements of the page that have event listeners related to scrolling that may harm the performance of the page.</span></span>  
<span data-ttu-id="2f8c4-484">DevTools souligne les éléments potentiellement posant problème en bleu-vert.</span><span class="sxs-lookup"><span data-stu-id="2f8c4-484">DevTools outlines the potentially-problematic elements in teal.</span></span>  

<span data-ttu-id="2f8c4-485">Pour afficher les problèmes de performances de défilement:</span><span class="sxs-lookup"><span data-stu-id="2f8c4-485">To view scroll performance issues:</span></span>  

1.  <span data-ttu-id="2f8c4-486">Ouvrez l’onglet **rendu** .  [Pour plus d’efficacité, voir analyser les performances de rendu avec l’onglet rendu](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="2f8c4-486">Open the **Rendering** tab.  See [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="2f8c4-487">Activez la case à cocher **problèmes de performances de défilement** .</span><span class="sxs-lookup"><span data-stu-id="2f8c4-487">Enable the **Scrolling Performance Issues** checkbox.</span></span>  
 
    > ##### <span data-ttu-id="2f8c4-488">Figure 42</span><span class="sxs-lookup"><span data-stu-id="2f8c4-488">Figure 42</span></span>  
    > <span data-ttu-id="2f8c4-489">Les **problèmes de performances de défilement** indiquent que les objets dotés de l’affichage sans calque risquent de nuire aux performances de défilement</span><span class="sxs-lookup"><span data-stu-id="2f8c4-489">**Scrolling Performance Issues** indicates that non-layer viewport-constrained objects may harm scroll performance</span></span>  
    > ![Les problèmes de performances de défilement indiquent que les objets dotés de l’affichage sans calque risquent de nuire aux performances de défilement][ImageScrollingPerformanceIssues]  
    

<!--    -->  



<!-- image links -->  

[ImageCaptureSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/capture-settings-icon.msft.png  
[ImageClearRecordingIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-recording-icon.msft.png  
[ImageCollectGarbageIcon]: /microsoft-edge/devtools-guide-chromium/media/collect-garbage-icon.msft.png  
[ImageNextIcon]: /microsoft-edge/devtools-guide-chromium/media/next-icon.msft.png  
[ImagePanModeIcon]: /microsoft-edge/devtools-guide-chromium/media/pan-mode-icon.msft.png  
[ImagePreviousIcon]: /microsoft-edge/devtools-guide-chromium/media/previous-icon.msft.png  
[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/media/record-icon.msft.png
[ImageRefreshPageIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-page-icon.msft.png  
[ImageResetTransformIcon]: /microsoft-edge/devtools-guide-chromium/media/reset-transform-icon.msft.png  
[ImageRotateModeIcon]: /microsoft-edge/devtools-guide-chromium/media/rotate-mode-icon.msft.png  
[ImageSearchCaseIcon]: /microsoft-edge/devtools-guide-chromium/media/search-case-icon.msft.png  
[ImageSearchRegexIcon]: /microsoft-edge/devtools-guide-chromium/media/search-regex-icon.msft.png  
[ImageShowHeaviestStackIcon]: /microsoft-edge/devtools-guide-chromium/media/show-heaviest-stack-icon.msft.png  

[ImageRecord]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-record-highlight.msft.png "Figure 1: enregistrement"  
[ImageRefreshPage]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refresh-button.msft.png "Figure 2: actualiser la page"  
[ImageLoadRecording]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed.msft.png "Figure 3: enregistrement de chargement de page"  
[ImageScreenshots]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png "Figure 4: cases à cocher captures d’écran"  
[ImageCollectGarbage]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-collect-garbage-button.msft.png "Figure 5: collecter les éléments nettoyés"  
[ImageCaptureSettings]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png "Figure 6: section paramètres de capture"  
[ImageJSSamplesDisabled]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png "Figure 7: exemple d’enregistrement lorsque les exemples de JS sont désactivés"  
[ImageJSSamplesEnabled]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png "Figure 8: exemple d’enregistrement lorsque les exemples de JS sont activés"  
[ImageSaveProfile]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png "Figure 9: enregistrement du profil"  
[ImageLoadProfile]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png "Figure 10: profil de chargement"  
[ImageClearRecording]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png "Figure 11: effacer l’enregistrement"  
[ImageZoom]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-zoom-highlighted.msft.png "Figure 12: glissement de la souris sur la présentation pour effectuer un zoom"  
[ImageSearch]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-search-regex.msft.png "Figure 13: zone de recherche"  
[ImageMain]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-main-zoomed.msft.png "Figure 14: section principale"  
[ImageMainEventSummary]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-summary-me.msft.png "Figure 15: informations supplémentaires sur la fonction anonyme sous l’onglet Résumé"  
[ImageFlameChart]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-main-flame-chart.msft.png "Figure 16: graphique en flamme"  
[ImageCallTree]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-call-tree.msft.png "Figure 17: onglet de l’arborescence des appels"  
[ImageBottomUp]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-bottoms-up.msft.png "Figure 18: onglet inférieur"  
[ImageEventLog]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-event-log.msft.png "Figure 19: onglet journal des événements"  
[ImageGpu]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-gpu-zoomed.msft.png "Figure 20: section GPU"  
[ImageRaster]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-raster.msft.png "Figure 21: section de pixellisation"  
[ImageInteractions]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-interactions-animation.msft.png "Figure 22: section interactions"  
[ImageFpsChart]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-fps-highlight.msft.png "Figure 23: graphique FPS"  
[ImageFramesSection]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-frames-hover.msft.png "Figure 24: survol d’un cadre"  
[ImageFrameSummary]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-frames-summary.msft.png "Figure 25: affichage d’un cadre sous l’onglet Résumé"  
[ImageNetworkRequest]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-network.msft.png "Figure 26: section réseau"  
[ImageLineBar]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-bing-performance-network.msft.png "Figure 27: représentation de la barre de lignes de la requête www.bing.com"  
[ImageTiming]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-bing-network-timing.msft.png "Figure 28: section réseau"  
[ImageMemory]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-memory-highlight.msft.png "Figure 29: cases à cocher de la mémoire"  
[ImageMemoryMetrics]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-memory-chart.msft.png "Figure 30: métriques de mémoire"  
[ImageDuration]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-main-duration.msft.png "Figure 31: affichage de la durée d’une portion d’un enregistrement"  
[ImageViewScreenshot]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-screenshots-hover.msft.png "Figure 32: affichage d’une capture d’écran"  
[ImageFrameScreenshotSummary]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-summary-preview.msft.png "Figure 33: affichage d’une capture d’écran sous l’onglet Résumé"  
[ImageFrameScreenshotZoom]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-summary-preview-select.msft.png "Figure 34: zoom avant d’une capture d’écran à partir de l’onglet Résumé"  
[ImageLayers]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-layers-all.msft.png "Figure 35: volet couches"  
[ImageLayerHover]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png "Figure 36: mise en surbrillance d’un calque"  
[ImagePaintProfiler]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-paint-profiler.msft.png "Figure 37: onglet Paint Profiler1.1"  
[ImageRenderingTab]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-console-drawer-rendering.msft.png "Figure 38: onglet rendu"  
[ImageFpsMeter]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-jank-console-rendering-frame-rate.msft.png "Figure 39: vumètre d’FPS"  
[ImagePaintFlashing]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png "Figure 40: couleur clignotante"  
[ImageLayerBorders]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png "Figure 41: bordures de calque"  
[ImageScrollingPerformanceIssues]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png "Figure 42: les problèmes de performances de défilement indiquent qu’il est possible que les objets dotés de l’affichage en mode sans couches nuisent aux performances de défilement"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Outils de développement Microsoft Edge (chrome)"  
[DevToolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index#open-the-command-menu "Ouvrir le menu de commandes-exécuter les commandes avec le menu de commandes Microsoft Edge DevTools"  
[DevtoolsEvaluatePerformanceGettingStarted]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/index "Commencer à analyser les performances de l’exécution"  

[ActivityTabsDemo]: https://microsoft-edge-chromium-devtools.glitch.me/perf/activitytabs.html "Démo des onglets d’activité"  

[ChromiumDebugColors]: https://cs.chromium.org/chromium/src/cc/debug/debug_colors.cc "debug_colors. cc-recherche de code"  

> [!NOTE]
> <span data-ttu-id="2f8c4-538">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2f8c4-538">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="2f8c4-539">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="2f8c4-539">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="2f8c4-541">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2f8c4-541">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
