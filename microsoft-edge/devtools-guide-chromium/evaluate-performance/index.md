---
description: Découvrez comment évaluer les performances d’exécution dans Microsoft Edge DevTools.
title: Commencer à analyser les performances d’exécution
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 439d6d4331550b7fc92bfc5fef4c3fc88df38872
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439611"
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

# <a name="get-started-with-analyzing-runtime-performance"></a><span data-ttu-id="1e9ca-104">Commencer à analyser les performances d’exécution</span><span class="sxs-lookup"><span data-stu-id="1e9ca-104">Get started with analyzing Runtime performance</span></span>  

> [!NOTE]
> <span data-ttu-id="1e9ca-105">Pour découvrir comment accélérer le chargement de vos pages, accédez à Optimiser la vitesse [du site web.][DevtoolsSpeedGetStarted]</span><span class="sxs-lookup"><span data-stu-id="1e9ca-105">To learn how to make your pages load faster, navigate to [Optimize Website Speed][DevtoolsSpeedGetStarted].</span></span>  

<span data-ttu-id="1e9ca-106">Les performances d’exécution sont les performances de votre page lorsqu’elle est en cours d’exécution, par opposition au chargement.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-106">Runtime performance is how your page performs when it is running, as opposed to loading.</span></span>  <span data-ttu-id="1e9ca-107">L’article de didacticiel suivant vous explique comment utiliser le panneau DevTools Performance de Microsoft Edge pour analyser les performances d’exécution.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-107">The following tutorial article teaches you how to use the Microsoft Edge DevTools Performance panel to analyze runtime performance.</span></span>  <span data-ttu-id="1e9ca-108">En ce qui concerne le modèle **RAIL,** les compétences que vous apprenez dans ce didacticiel sont utiles pour analyser les phases de réponse, d’animation et d’inactivité de votre page.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-108">In terms of the **RAIL** model, the skills you learn in this tutorial are useful for analyzing the Response, Animation, and Idle phases of your page.</span></span>  

<!--todo: add rail link when section is ready -->  

## <a name="get-started"></a><span data-ttu-id="1e9ca-109">Prise en main</span><span class="sxs-lookup"><span data-stu-id="1e9ca-109">Get started</span></span>  

<span data-ttu-id="1e9ca-110">Dans le didacticiel suivant, vous ouvrez DevTools sur une page en direct et utilisez le panneau Performances pour trouver un goulot d’étranglement des performances sur la page. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="1e9ca-110">In the following tutorial, you open DevTools on a live page and use the **Performance** panel to find a performance bottleneck on the page.</span></span>  

1.  <span data-ttu-id="1e9ca-111">Ouvrez Microsoft Edge **en mode InPrivate.**</span><span class="sxs-lookup"><span data-stu-id="1e9ca-111">Open Microsoft Edge in **InPrivate Mode**.</span></span>  <span data-ttu-id="1e9ca-112">Le mode InPrivate garantit que Microsoft Edge s’exécute dans un état propre.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-112">InPrivate Mode ensures that Microsoft Edge runs in a clean state.</span></span>  <span data-ttu-id="1e9ca-113">Par exemple, si un grand nombre d’extensions sont installées, elles peuvent créer du bruit dans vos mesures de performances.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-113">For example, if you have a lot of extensions installed, the extensions may create noise in your performance measurements.</span></span>  
    
    <!--TODO: replace section when updated for new Edge  -->
    
1.  <span data-ttu-id="1e9ca-114">Chargez la page suivante dans votre fenêtre InPrivate.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-114">Load the following page in your InPrivate window.</span></span>  <span data-ttu-id="1e9ca-115">La page est la démonstration que vous allez profiler.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-115">The page is the demo that you are going to profile.</span></span>  <span data-ttu-id="1e9ca-116">La page affiche un grand nombre de petites icônes qui se déplacent vers le haut et vers le bas.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-116">The page shows a bunch of little icons moving up and down.</span></span>  
    
    ```https
    https://microsoft-edge-chromium-devtools.glitch.me/sluggish/
    ```  
    
1.  <span data-ttu-id="1e9ca-117">Sélectionnez `Control` + `Shift` + `I` \(Windows, Linux\) ou `Command` + `Option` + `I` \(macOS\) pour ouvrir DevTools.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-117">Select `Control`+`Shift`+`I` \(Windows, Linux\) or `Command`+`Option`+`I` \(macOS\) to open DevTools.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-get-started-side-by-side.msft.png" alt-text="Démonstration à gauche et DevTools à droite" lightbox="../media/evaluate-performance-get-started-side-by-side.msft.png":::
       <span data-ttu-id="1e9ca-119">Démonstration à gauche et DevTools à droite</span><span class="sxs-lookup"><span data-stu-id="1e9ca-119">The demo on the left, and DevTools on the right</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="1e9ca-120">Pour le reste des figures, DevTools n’est pas resserpé à une fenêtre distincte pour mieux se concentrer sur le contenu. [][DevtoolsCustomizePlacement]</span><span class="sxs-lookup"><span data-stu-id="1e9ca-120">For the rest of the figures, DevTools is [undocked to a separate window][DevtoolsCustomizePlacement] to better focus on the contents.</span></span>  
    
### <a name="simulate-a-mobile-cpu"></a><span data-ttu-id="1e9ca-121">Simuler une UC mobile</span><span class="sxs-lookup"><span data-stu-id="1e9ca-121">Simulate a mobile CPU</span></span>  

<span data-ttu-id="1e9ca-122">Les appareils mobiles ont beaucoup moins de puissance processeur que les ordinateurs de bureau et les ordinateurs portables.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-122">Mobile devices have much less CPU power than desktops and laptops.</span></span>  <span data-ttu-id="1e9ca-123">Chaque fois que vous profilez une page, utilisez la limitation du processeur pour simuler le fonctionnement de votre page sur les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-123">Whenever you profile a page, use CPU Throttling to simulate how your page performs on mobile devices.</span></span>  

1.  <span data-ttu-id="1e9ca-124">Dans DevTools, choisissez **l’outil Performance.**</span><span class="sxs-lookup"><span data-stu-id="1e9ca-124">In DevTools, choose the **Performance** tool.</span></span>  
1.  <span data-ttu-id="1e9ca-125">Assurez-vous que vous choisissez la case à cocher en regard des **captures d’écran.**</span><span class="sxs-lookup"><span data-stu-id="1e9ca-125">Ensure the you choose the checkbox next to **Screenshots**.</span></span>  
1.  <span data-ttu-id="1e9ca-126">Choose **Capture Settings** \( ![ Capture Settings ](../media/capture-settings-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="1e9ca-126">Choose **Capture Settings** \(![Capture Settings](../media/capture-settings-icon.msft.png)\).</span></span>  <span data-ttu-id="1e9ca-127">DevTools révèle les paramètres liés à la façon dont il capture les mesures de performances.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-127">DevTools reveals settings related to how it captures performance metrics.</span></span>  
1.  <span data-ttu-id="1e9ca-128">Pour **l’UC,** choisissez **un ralentissement 4x.**</span><span class="sxs-lookup"><span data-stu-id="1e9ca-128">For **CPU**, choose **4x slowdown**.</span></span>  <span data-ttu-id="1e9ca-129">DevTools permet de limiter votre processeur de sorte qu’il soit 4 fois plus lent que d’habitude.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-129">DevTools throttles your CPU so that it is 4 times slower than usual.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-capture-settings.msft.png" alt-text="Limitation du processeur" lightbox="../media/evaluate-performance-performance-capture-settings.msft.png":::
       <span data-ttu-id="1e9ca-131">Limitation du processeur</span><span class="sxs-lookup"><span data-stu-id="1e9ca-131">CPU throttle</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="1e9ca-132">Lors du test d’autres pages ; si vous souhaitez vous assurer que chaque page fonctionne bien sur les appareils mobiles bas de gamme, définissez la limitation de l’UC sur un ralentissement **de 6x**.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-132">When testing other pages; if you want to ensure that each page works well on low-end mobile devices, set CPU Throttling to **6x slowdown**.</span></span>  <span data-ttu-id="1e9ca-133">La démonstration ne fonctionne pas bien avec un ralentissement 6x, donc elle utilise simplement un ralentissement 4x à des fins d’instruction.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-133">The demo does not work well with 6x slowdown, so it just uses 4x slowdown for instructional purposes.</span></span>  
    
### <a name="set-up-the-demo"></a><span data-ttu-id="1e9ca-134">Configurer la démonstration</span><span class="sxs-lookup"><span data-stu-id="1e9ca-134">Set up the demo</span></span>  

<span data-ttu-id="1e9ca-135">Il est difficile de créer une démonstration des performances d’exécution qui fonctionne de manière cohérente pour tous les lecteurs du site web.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-135">It is hard to create a runtime performance demo that works consistently for all readers of the website.</span></span>  <span data-ttu-id="1e9ca-136">La section suivante vous permet de personnaliser la démonstration pour vous assurer que votre expérience est relativement cohérente avec les captures d’écran et les descriptions, quelle que soit votre disposition particulière.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-136">The following section lets you customize the demo to ensure that your experience is relatively consistent with the screenshots and descriptions, regardless of your particular set up.</span></span>

1.  <span data-ttu-id="1e9ca-137">Choisissez le **bouton Ajouter 10** jusqu’à ce que les icônes bleues se déplacent sensiblement plus lentement qu’auparavant.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-137">Choose the **Add 10** button until the blue icons move noticeably slower than before.</span></span>  <span data-ttu-id="1e9ca-138">Sur un ordinateur haut de gamme, vous pouvez le choisir environ 20 fois.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-138">On a high-end machine, you may to choose it about 20 times.</span></span>  
1.  <span data-ttu-id="1e9ca-139">Choisissez **Optimiser.**</span><span class="sxs-lookup"><span data-stu-id="1e9ca-139">Choose **Optimize**.</span></span>  <span data-ttu-id="1e9ca-140">Les icônes bleues doivent se déplacer plus rapidement et plus fluidement.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-140">The blue icons should move faster and more smoothly.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="1e9ca-141">Pour mieux afficher une différence entre les versions optimisées et non optimisées, sélectionnez le bouton **Soustraction 10** plusieurs fois et essayez à nouveau.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-141">To better display a difference between the optimized and un-optimized versions, choose the **Subtract 10** button a few times and try again.</span></span>  
    > <span data-ttu-id="1e9ca-142">Si vous ajoutez un trop grand nombre d’icônes bleues, il se peut que vous n’observiez pas de différence majeure dans les résultats des deux versions.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-142">If you add too many blue icons, you may max out the CPU and then you may not observe a major difference in the results for the two versions.</span></span>  
    
1.  <span data-ttu-id="1e9ca-143">Choose **Un-Optimize**.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-143">Choose **Un-Optimize**.</span></span>  <span data-ttu-id="1e9ca-144">Les icônes bleues se déplacent plus lentement et sont de nouveau plus lentes.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-144">The blue icons move slower and with more sluggishness again.</span></span>  
    
### <a name="record-runtime-performance"></a><span data-ttu-id="1e9ca-145">Enregistrer les performances d’exécution</span><span class="sxs-lookup"><span data-stu-id="1e9ca-145">Record runtime performance</span></span>  

<span data-ttu-id="1e9ca-146">Lorsque vous avez publié la version optimisée de la page, les icônes bleues se déplacent plus rapidement.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-146">When you ran the optimized version of the page, the blue icons move faster.</span></span>  <span data-ttu-id="1e9ca-147">Pourquoi?</span><span class="sxs-lookup"><span data-stu-id="1e9ca-147">Why is that?</span></span>  <span data-ttu-id="1e9ca-148">Les deux versions sont supposées déplacer les icônes de la même quantité d’espace dans la même durée.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-148">Both versions are supposed to move the icons the same amount of space in the same amount of time.</span></span>  <span data-ttu-id="1e9ca-149">Prenez un enregistrement dans le panneau Performances pour découvrir comment détecter le goulot d’étranglement des performances dans la version non optimisée.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-149">Take a recording in the Performance panel to learn how to detect the performance bottleneck in the un-optimized version.</span></span>  

1.  <span data-ttu-id="1e9ca-150">Dans DevTools, choisissez **Record** \( ![ Record ](../media/record-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="1e9ca-150">In DevTools, choose **Record** \(![Record](../media/record-icon.msft.png)\).</span></span>  <span data-ttu-id="1e9ca-151">DevTools capture les mesures de performances au cours de l’exécution de la page.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-151">DevTools captures performance metrics as the page runs.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-profiling.msft.png" alt-text="Profiler la page" lightbox="../media/evaluate-performance-performance-profiling.msft.png":::
       <span data-ttu-id="1e9ca-153">Profiler la page</span><span class="sxs-lookup"><span data-stu-id="1e9ca-153">Profile the page</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1e9ca-154">Patientez quelques secondes.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-154">Wait a few seconds.</span></span>  
1.  <span data-ttu-id="1e9ca-155">Choose **Stop**.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-155">Choose **Stop**.</span></span>  <span data-ttu-id="1e9ca-156">DevTools arrête l’enregistrement, traite les données, puis affiche les résultats dans le panneau Performances.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-156">DevTools stops recording, processes the data, then displays the results on the Performance panel.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-capture-results.msft.png" alt-text="Résultats du profil" lightbox="../media/evaluate-performance-performance-capture-results.msft.png":::
       <span data-ttu-id="1e9ca-158">Résultats du profil</span><span class="sxs-lookup"><span data-stu-id="1e9ca-158">The results of the profile</span></span>  
    :::image-end:::  
    
<span data-ttu-id="1e9ca-159">Wow, il s’agit d’une quantité considérable de données.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-159">Wow, that is an overwhelming amount of data.</span></span>  <span data-ttu-id="1e9ca-160">ne vous inquiétez pas, le processus sera bientôt plus logique.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-160">do not worry, soon the process makes more sense.</span></span>  

## <a name="analyze-the-results"></a><span data-ttu-id="1e9ca-161">Analyser les résultats</span><span class="sxs-lookup"><span data-stu-id="1e9ca-161">Analyze the results</span></span>  

<span data-ttu-id="1e9ca-162">Après avoir enregistré les performances de la page, mesurez la qualité des performances de la page et trouvez les causes.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-162">After you record the performance of the page, measure the quality of the performance of the page and find the any causes.</span></span>  

### <a name="analyze-frames-per-second"></a><span data-ttu-id="1e9ca-163">Analyser des images par seconde</span><span class="sxs-lookup"><span data-stu-id="1e9ca-163">Analyze frames per second</span></span>  

<span data-ttu-id="1e9ca-164">La mesure principale pour mesurer les performances d’une animation est l’image par seconde \(FPS\).</span><span class="sxs-lookup"><span data-stu-id="1e9ca-164">The main metric for measuring the performance of any animation is frames per second \(FPS\).</span></span>  <span data-ttu-id="1e9ca-165">Les utilisateurs sont satisfaits lorsque les animations s’exécutent à 60 FPS.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-165">Users are happy when animations run at 60 FPS.</span></span>  

1.  <span data-ttu-id="1e9ca-166">Examinez **le graphique FPS.**</span><span class="sxs-lookup"><span data-stu-id="1e9ca-166">Review the **FPS** chart.</span></span>  <span data-ttu-id="1e9ca-167">Chaque fois qu’une barre rouge est affichée au-dessus de **FPS,** cela signifie que la vitesse d’images est si basse qu’elle nuit probablement à l’expérience utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-167">Whenever a red bar is displayed above **FPS**, it means that the framerate dropped so low that it is probably harming the user experience.</span></span>  <span data-ttu-id="1e9ca-168">En règle générale, plus la barre verte est élevée, plus le FPS est élevé.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-168">In general, the higher the green bar, the higher the FPS.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-fps-chart.msft.png" alt-text="Graphique FPS" lightbox="../media/evaluate-performance-performance-fps-chart.msft.png":::
       <span data-ttu-id="1e9ca-170">Graphique **FPS**</span><span class="sxs-lookup"><span data-stu-id="1e9ca-170">The **FPS** chart</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1e9ca-171">Sous le **graphique FPS,** le **graphique UC** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-171">Below the **FPS** chart, the **CPU** chart is displayed.</span></span>  <span data-ttu-id="1e9ca-172">Les couleurs du **graphique UC** correspondent \*\*\*\* aux couleurs du panneau Résumé, en bas du panneau Performances.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-172">The colors in the **CPU** chart correspond to the colors in the **Summary** panel, at the bottom of the Performance panel.</span></span>  <span data-ttu-id="1e9ca-173">Le fait que le **graphique de l’UC** soit plein de couleurs signifie que l’UC a été maximale pendant l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-173">The fact that the **CPU** chart is full of color means that the CPU was maxed out during the recording.</span></span>  <span data-ttu-id="1e9ca-174">Chaque fois que l’UC a été maximale pendant de longues périodes, il s’agit d’un indicateur qui vous permet de trouver des moyens de faire moins de travail.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-174">Whenever the CPU maxed out for long periods, it is an indicator that you should find ways to do less work.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-cpu-chart.msft.png" alt-text="Graphique de l’UC et panneau De synthèse" lightbox="../media/evaluate-performance-performance-cpu-chart.msft.png":::
       <span data-ttu-id="1e9ca-176">Graphique **de l’UC** et **panneau De** synthèse</span><span class="sxs-lookup"><span data-stu-id="1e9ca-176">The **CPU** chart and **Summary** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1e9ca-177">Pointez sur **les graphiques FPS,** **CPU** **ou NET.**</span><span class="sxs-lookup"><span data-stu-id="1e9ca-177">Hover on the **FPS**, **CPU**, or **NET** charts.</span></span>  <span data-ttu-id="1e9ca-178">DevTools affiche une capture d’écran de la page à ce stade.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-178">DevTools shows a screenshot of the page at that point in time.</span></span>  <span data-ttu-id="1e9ca-179">Déplacez votre souris vers la gauche et la droite pour relire l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-179">Move your mouse left and right to replay the recording.</span></span>  <span data-ttu-id="1e9ca-180">L’action est référencé en tant que nettoyage et est utile pour analyser manuellement la progression des animations.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-180">The action is referenced as scrubbing, and it is useful for manually analyzing the progression of animations.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-screenshot-hover.msft.png" alt-text="Afficher une capture d’écran de la page autour de la marque de 2 500 ms de l’enregistrement" lightbox="../media/evaluate-performance-performance-screenshot-hover.msft.png":::
       <span data-ttu-id="1e9ca-182">Afficher une capture d’écran de la page autour de la marque de 2 500 ms de l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="1e9ca-182">View a screenshot of the page around the 2500ms mark of the recording</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1e9ca-183">Dans la section **Cadres,** pointez sur l’un des carrés verts.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-183">In the **Frames** section, hover on one of the green squares.</span></span>  <span data-ttu-id="1e9ca-184">DevTools vous montre le FPS pour cette image particulière.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-184">DevTools shows you the FPS for that particular frame.</span></span>  <span data-ttu-id="1e9ca-185">Chaque image est probablement bien en dessous de la cible de 60 FPS.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-185">Each frame is probably well below the target of 60 FPS.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-frame-hover.msft.png" alt-text="Pointer sur un cadre" lightbox="../media/evaluate-performance-performance-frame-hover.msft.png":::
       <span data-ttu-id="1e9ca-187">Pointer sur un cadre</span><span class="sxs-lookup"><span data-stu-id="1e9ca-187">Hover on a frame</span></span>  
    :::image-end:::  
    
<span data-ttu-id="1e9ca-188">Bien entendu, l’affichage indique que la page web ne s’exécute pas bien.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-188">Of course, the display indicates that the webpage is not performing well.</span></span>  <span data-ttu-id="1e9ca-189">Toutefois, dans les scénarios réels, il peut ne pas être aussi clair, donc avoir tous les outils pour effectuer des mesures est utile.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-189">But in real scenarios, it may not be so clear, so having all of the tools to make measurements comes in handy.</span></span>  

#### <a name="bonus-open-the-fps-meter"></a><span data-ttu-id="1e9ca-190">Bonus : ouvrir la jauge FPS</span><span class="sxs-lookup"><span data-stu-id="1e9ca-190">Bonus: Open the FPS meter</span></span>  

<span data-ttu-id="1e9ca-191">Un autre outil pratique est la jauge FPS, qui fournit des estimations en temps réel pour FPS lors de l’application de la page.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-191">Another handy tool is the FPS meter, which provides real-time estimates for FPS as the page runs.</span></span>  

1.  <span data-ttu-id="1e9ca-192">Sélectionnez `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\) pour ouvrir le **menu Commande.**</span><span class="sxs-lookup"><span data-stu-id="1e9ca-192">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
1.  <span data-ttu-id="1e9ca-193">Commencez à taper `Rendering` dans le menu Commande **et** choisissez Afficher **le rendu.**</span><span class="sxs-lookup"><span data-stu-id="1e9ca-193">Start typing `Rendering` in the **Command Menu** and choose **Show Rendering**.</span></span>  
1.  <span data-ttu-id="1e9ca-194">Dans **l’outil de** rendu, allumez **la jauge FPS.**</span><span class="sxs-lookup"><span data-stu-id="1e9ca-194">In the **Rendering** tool, turn on **FPS Meter**.</span></span>  <span data-ttu-id="1e9ca-195">Une nouvelle superposition apparaît dans le haut à droite de votre vue.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-195">A new overlay appears in the top-right of your viewport.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-fps-meter-overlay.msft.png" alt-text="Indicateur FPS" lightbox="../media/evaluate-performance-fps-meter-overlay.msft.png":::
       <span data-ttu-id="1e9ca-197">Indicateur **FPS**</span><span class="sxs-lookup"><span data-stu-id="1e9ca-197">The **FPS meter**</span></span>  
        :::image-end:::  
    
1.  <span data-ttu-id="1e9ca-198">Désactiver la jauge **FPS** et choisir de `Escape` fermer l’outil **de** rendu.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-198">Turn off the **FPS Meter** and select `Escape` to close the **Rendering** tool.</span></span>  <span data-ttu-id="1e9ca-199">Vous n’utilisez pas la **jauge FPS** dans ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-199">You are not using **FPS Meter** in this tutorial.</span></span>  
    
### <a name="find-the-bottleneck"></a><span data-ttu-id="1e9ca-200">Rechercher le goulot d’étranglement</span><span class="sxs-lookup"><span data-stu-id="1e9ca-200">Find the bottleneck</span></span>  

<span data-ttu-id="1e9ca-201">Une fois que vous avez mesuré et vérifié que l’animation ne s’exécute pas bien, l’étape suivante consiste à répondre à la question « pourquoi ? ».</span><span class="sxs-lookup"><span data-stu-id="1e9ca-201">After you measured and verified that the animation is not performing well, the next step is to answer the question "why?".</span></span>  

1.  <span data-ttu-id="1e9ca-202">Lorsqu’aucun événement n’est choisi, le **panneau Résumé** vous présente une répartition de l’activité.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-202">When no events are chosen, the **Summary** panel shows you a breakdown of activity.</span></span>  <span data-ttu-id="1e9ca-203">La page a passé la plupart du temps à être rendu.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-203">The page spent most of the time rendering.</span></span>  <span data-ttu-id="1e9ca-204">Étant donné que les performances sont l’art d’avoir moins de travail, votre objectif est de réduire le temps consacré au travail de rendu.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-204">Since performance is the art of doing less work, your goal is to reduce the amount of time spent doing rendering work.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-summary-tab.msft.png" alt-text="Le panneau Résumé" lightbox="../media/evaluate-performance-performance-summary-tab.msft.png":::
       <span data-ttu-id="1e9ca-206">Le **panneau Résumé**</span><span class="sxs-lookup"><span data-stu-id="1e9ca-206">The **Summary** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1e9ca-207">Développez **la** section Main.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-207">Expand the **Main** section.</span></span>  <span data-ttu-id="1e9ca-208">DevTools vous présente un graphique d’activité sur le thread principal, au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-208">DevTools shows you a flame chart of activity on the main thread, over time.</span></span>  <span data-ttu-id="1e9ca-209">L’axe X représente l’enregistrement, au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-209">The x-axis represents the recording, over time.</span></span>  <span data-ttu-id="1e9ca-210">Chaque barre représente un événement.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-210">Each bar represents an event.</span></span>  <span data-ttu-id="1e9ca-211">Une barre plus large signifie que l’événement a pris plus de temps.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-211">A wider bar means that event took longer.</span></span>  <span data-ttu-id="1e9ca-212">L’axe Y représente la pile d’appels.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-212">The y-axis represents the call stack.</span></span>  <span data-ttu-id="1e9ca-213">Lorsque les événements sont empilés les uns sur les autres, cela signifie que les événements supérieurs ont provoqué les événements inférieurs.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-213">When events are stacked on top of each other, it means the upper events caused the lower events.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-main.msft.png" alt-text="Section Main" lightbox="../media/evaluate-performance-performance-main.msft.png":::
       <span data-ttu-id="1e9ca-215">Section **Main**</span><span class="sxs-lookup"><span data-stu-id="1e9ca-215">The **Main** section</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1e9ca-216">Il y a beaucoup de données dans l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-216">There is a lot of data in the recording.</span></span>  <span data-ttu-id="1e9ca-217">Pour effectuer un zoom sur un seul événement ; choisissez, maintenez votre curseur sur \*\*\*\* la vue d’ensemble, qui est la section qui inclut les graphiques **FPS,** **CPU**et **NET.**</span><span class="sxs-lookup"><span data-stu-id="1e9ca-217">To Zoom into a single event; choose, hold, and dragg your cursor over the **Overview**, which is the section that includes the **FPS**, **CPU**, and **NET** charts.</span></span>  <span data-ttu-id="1e9ca-218">La section **Principale** et **le panneau Résumé** affichent uniquement les informations de la partie sélectionnée de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-218">The **Main** section and **Summary** panel only display information for the chosen portion of the recording.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-main-zoomed.msft.png" alt-text="Zoom sur un événement" lightbox="../media/evaluate-performance-performance-main-zoomed.msft.png":::
       <span data-ttu-id="1e9ca-220">Zoom sur un événement</span><span class="sxs-lookup"><span data-stu-id="1e9ca-220">Zoom into an event</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="1e9ca-221">Une autre façon de zoomer, de focuser la section **Main,** de choisir l’arrière-plan ou un événement, et de sélectionner `W` , ou `A` `S` `D` .</span><span class="sxs-lookup"><span data-stu-id="1e9ca-221">Another way to zoom, focus the **Main** section, choose the background or an event, and select `W`, `A`, `S`, or `D`.</span></span>  
    
    1.  <span data-ttu-id="1e9ca-222">Focus sur le triangle rouge dans le haut à droite de l’événement de **tir du cadre d’animation.**</span><span class="sxs-lookup"><span data-stu-id="1e9ca-222">Focus on the red triangle in the top-right of the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="1e9ca-223">Chaque fois qu’un triangle rouge est affiché, il s’agit d’un avertissement signalant qu’il peut y avoir un problème lié à l’événement.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-223">Whenever a red triangle is displayed, it is a warning that there may be an issue related to the event.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="1e9ca-224">**L’événement Animation Frame Fired** se produit chaque fois qu’un rappel [requestAnimationFrame()][MDNWebRequestAnimationFrame] est exécuté.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-224">The **Animation Frame Fired** event occurs whenever a [requestAnimationFrame() callback][MDNWebRequestAnimationFrame] is run.</span></span>  
    
1.  <span data-ttu-id="1e9ca-225">Choisissez **l’événement De cadre d’animation** déclenché.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-225">Choose the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="1e9ca-226">Le **panneau Résumé** vous présente désormais des informations sur cet événement.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-226">The **Summary** panel now shows you information about that event.</span></span>  <span data-ttu-id="1e9ca-227">Notez le **lien Révéler.**</span><span class="sxs-lookup"><span data-stu-id="1e9ca-227">Note the **Reveal** link.</span></span>  <span data-ttu-id="1e9ca-228">Une fois que vous l’avez choisi, DevTools met en évidence l’événement qui a initié l’événement Animation **Frame Fired.**</span><span class="sxs-lookup"><span data-stu-id="1e9ca-228">After you choose it, DevTools to highlights the event that initiated the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="1e9ca-229">En outre, concentrez-vous **surapp.js:95.**</span><span class="sxs-lookup"><span data-stu-id="1e9ca-229">Also, focus on the **app.js:95** link.</span></span>  <span data-ttu-id="1e9ca-230">Une fois que vous l’avez choisi, la ligne pertinente dans le code source s’affiche.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-230">After you choose it, the relevant line in the source code is displayed.</span></span>
    
    :::image type="complex" source="../media/evaluate-performance-performance-animation-frame-fired.msft.png" alt-text="Plus d’informations sur l’événement Animation Frame Fired" lightbox="../media/evaluate-performance-performance-animation-frame-fired.msft.png":::
       <span data-ttu-id="1e9ca-232">Plus d’informations sur **l’événement Animation Frame Fired**</span><span class="sxs-lookup"><span data-stu-id="1e9ca-232">More information about the **Animation Frame Fired** event</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="1e9ca-233">Après avoir choisi un événement, utilisez les touches de direction pour sélectionner les événements en de côté.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-233">After choosing an event, use the arrow keys to select the events next to it.</span></span>  
    
1.  <span data-ttu-id="1e9ca-234">Sous **l’événement app.update,** il y a un grand nombre d’événements violets.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-234">Under the **app.update** event, there is a bunch of purple events.</span></span>  <span data-ttu-id="1e9ca-235">Si chaque événement violet était plus large, il semble que chacun d’eux puisse avoir un triangle rouge.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-235">If each purple event was wider, it looks as though each one may have a red triangle on it.</span></span>  
1.  <span data-ttu-id="1e9ca-236">Choisissez l’un des événements **de disposition violet.**</span><span class="sxs-lookup"><span data-stu-id="1e9ca-236">Choose one of the purple **Layout** events.</span></span>  <span data-ttu-id="1e9ca-237">DevTools fournit plus d’informations sur l’événement dans le **panneau Résumé.**</span><span class="sxs-lookup"><span data-stu-id="1e9ca-237">DevTools provides more information about the event in the **Summary** panel.</span></span>  <span data-ttu-id="1e9ca-238">En effet, il existe un avertissement concernant les réaflows forcés \(un autre mot pour la disposition\).</span><span class="sxs-lookup"><span data-stu-id="1e9ca-238">Indeed, there is a warning about forced reflows \(another word for layout\).</span></span>  
    
1.  <span data-ttu-id="1e9ca-239">Dans le **panneau Résumé,** choisissez le \*\* lienapp.js:71 sous\*\* Disposition **forcée**.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-239">In the **Summary** panel, choose the **app.js:71** link under **Layout Forced**.</span></span>  <span data-ttu-id="1e9ca-240">DevTools vous permet d’aller à la ligne de code qui a forcé la disposition.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-240">DevTools takes you to the line of code that forced the layout.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-sources-app-update.msft.png" alt-text="Ligne de code à l’origine de la disposition forcée" lightbox="../media/evaluate-performance-sources-app-update.msft.png":::
       <span data-ttu-id="1e9ca-242">Ligne de code à l’origine de la disposition forcée</span><span class="sxs-lookup"><span data-stu-id="1e9ca-242">The line of code that caused the forced layout</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="1e9ca-243">Le problème avec le code est que, dans chaque cadre d’animation, il modifie le style de chaque icône, puis interroge la position de chaque icône sur la page.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-243">The problem with the code is that, in each animation frame, it changes the style for each icon, and then queries the position of each icon on the page.</span></span>  <span data-ttu-id="1e9ca-244">Étant donné que les styles ont été modifiés, le navigateur ne sait pas si chaque position d’icône a changé, il doit donc ré-agencer l’icône afin de calculer la nouvelle position.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-244">Because the styles changed, the browser does not know if each icon position changed, so it has to re-layout the icon in order to compute the new position.</span></span>  <!--  > To learn more, navigate to [Avoid forced synchronous layouts][RenderingAvoidSynchronousLayouts].  -->
    
<!-- todo: add layouts section when available -->

<span data-ttu-id="1e9ca-245">Cela a été beaucoup à apprendre.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-245">That was a lot to learn.</span></span>  <span data-ttu-id="1e9ca-246">Vous avez maintenant une base solide dans le flux de travail de base pour l’analyse des performances d’exécution.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-246">You now have a solid foundation in the basic workflow for analyzing runtime performance.</span></span>  <span data-ttu-id="1e9ca-247">Bien fait.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-247">Good job.</span></span>  

### <a name="bonus-analyze-the-optimized-version"></a><span data-ttu-id="1e9ca-248">Bonus : analyser la version optimisée</span><span class="sxs-lookup"><span data-stu-id="1e9ca-248">Bonus: Analyze the optimized version</span></span>  

<span data-ttu-id="1e9ca-249">À l’aide des flux de \*\*\*\* travail et des outils que vous venons d’apprendre, sélectionnez Optimiser sur la démonstration pour activer le code optimisé, prendre un autre enregistrement des performances, puis analyser les résultats.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-249">Using the workflows and tools that you just learned, choose **Optimize** on the demo to turn on the optimized code, take another performance recording, and then analyze the results.</span></span>  <span data-ttu-id="1e9ca-250">De la trame améliorée à la réduction du nombre d’événements dans le graphique de l’animation dans la section **Main,** la version optimisée de l’application fait beaucoup moins de travail, ce qui améliore les performances.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-250">From the improved framerate to the reduction in events in the flame chart in the **Main** section, the optimized version of the app does much less work, resulting in better performance.</span></span>  

> [!NOTE]
> <span data-ttu-id="1e9ca-251">Même la version optimisée n’est pas très bonne, car elle manipule la `top` propriété de chaque icône.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-251">Even the optimized version is not great, because it manipulates the `top` property of every icon.</span></span>  <span data-ttu-id="1e9ca-252">Une meilleure approche consiste à s’en tenir aux propriétés qui affectent uniquement la composition.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-252">A better approach is to stick to properties that only affect compositing.</span></span>  <!--  > For more information, navigate to [Use transform and opacity changes for animations][RenderingCompositor].  -->  

<!--todo: add rendering section when available -->

## <a name="next-steps"></a><span data-ttu-id="1e9ca-253">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="1e9ca-253">Next steps</span></span>

<!--The foundation for understanding performance is the RAIL model.  The RAIL model teaches you the performance metrics that are most important to your users.  
To learn more, navigate to [Measure Performance With The RAIL Model][RAIL].  -->  

<span data-ttu-id="1e9ca-254">Pour vous mettre à l’aise avec **l’outil Performance,** la pratique est parfaite.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-254">To get more comfortable with the **Performance** tool, practice makes perfect.</span></span>  <span data-ttu-id="1e9ca-255">Essayez de profiler vos pages et d’analyser les résultats.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-255">Try profiling your pages and analyzing the results.</span></span>  <span data-ttu-id="1e9ca-256">Si vous avez des questions sur \*\*\*\* vos résultats, utilisez l’icône Envoyer des commentaires, sélectionnez `Alt` + `Shift` + `I` \(Windows, Linux\), `Option` + `Shift` + `I` sélectionnez \(macOS\) ou tweetez l’équipe [DevTools.][TwitterEdgeDevtools]</span><span class="sxs-lookup"><span data-stu-id="1e9ca-256">If you have any questions about your results, use the **Send Feedback** icon, select `Alt`+`Shift`+`I` \(Windows, Linux\), select `Option`+`Shift`+`I` \(macOS\), or [tweet the DevTools team][TwitterEdgeDevtools].</span></span>  <span data-ttu-id="1e9ca-257">Incluez des captures d’écran ou des liens vers des pages reproductibles, si possible.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-257">Include screenshots or links to reproducible pages, if possible.</span></span>  

:::image type="complex" source="../media/evaluate-performance-feedback-icon.msft.png" alt-text="Icône **Commentaires** dans Microsoft Edge DevTools" lightbox="../media/evaluate-performance-feedback-icon.msft.png":::
   <span data-ttu-id="1e9ca-259">Icône **Envoyer des commentaires** dans Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="1e9ca-259">The **Send Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- To really become an expert in runtime performance, you must learn how the browser translates HTML, CSS, and JS into pixels on a screen.  The best place to start is the [Rendering Performance Overview][RenderingPerformance].  [The Anatomy Of A Frame][FrameAnatomy] dives into even more detail.  -->  

<span data-ttu-id="1e9ca-260">Enfin, il existe de nombreuses façons d’améliorer les performances d’exécution.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-260">Last, there are many ways to improve runtime performance.</span></span>  <span data-ttu-id="1e9ca-261">Cet article s’est concentré sur un goulot d’étranglement d’animation particulier pour vous offrir une visite guidée du panneau Performances, mais il ne s’agit que de l’un des nombreux goulots d’étranglement que vous pouvez rencontrer.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-261">This article focused on one particular animation bottleneck to give you a focused tour through the Performance panel, but it is only one of many bottlenecks you may encounter.</span></span>  <!--  The rest of the Rendering Performance series has a lot of good tips for improving various aspects of runtime performance, such as:  -->

<!--
*   [Optimizing JS Execution][RenderingOptimizeJS]  
*   [Reduce The Scope And Complexity Of Style Calculations][RenderingReduceScope]  
*   [Avoid Large, Complex Layouts And Layout Thrashing][RenderingAvoidThrashing]  
*   [Simplify Paint Complexity And Reduce Paint Areas][RenderingSimplifyPaint]  
*   [Stick To Compositor-Only Properties And Manage Layer Count][RenderingManageLayers]  
*   [Debounce Your Input Handlers][RenderingDebounceInputs]  
-->

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="1e9ca-262">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="1e9ca-262">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->

[DevtoolsCustomizePlacement]: ../customize/placement.md "Modifier l’emplacement de Microsoft Edge DevTools (Undock, Dock to Bottom, Dock To Left)"  
[DevtoolsSpeedGetStarted]: ../speed/get-started.md "Optimiser la vitesse du site web avec Microsoft Edge DevTools"  

[TwitterEdgeDevtools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "EdgeDevTools - Publier un tweet | Twitter"  

[MDNWebRequestAnimationFrame]: https://developer.mozilla.org/docs/Web/API/window/requestAnimationFrame "Window.requestAnimationFrame\(\) | MDN"  

<!--[InPrivate]: https://support.microsoft.com/help/4026200/microsoft-edge-browse-inprivate "Browse InPrivate in Microsoft Edge"  -->

<!--[FrameAnatomy]: https://aerotwist.com/blog/the-anatomy-of-a-frame  -->  

<!--[RAIL]: /web/fundamentals/performance/rail  -->  
<!--[RenderingAvoidSynchronousLayouts]: /web/fundamentals/performance/rendering/avoid-large-complex-layouts-and-layout-thrashing#avoid_forced_synchronous_layouts  -->  
<!--[RenderingAvoidThrashing]: /web/fundamentals/performance/rendering/avoid-large-complex-layouts-and-layout-thrashing  -->  
<!--[RenderingCompositor]: /web/fundamentals/performance/rendering/stick-to-compositor-only-properties-and-manage-layer-count#use_transform_and_opacity_changes_for_animations  -->  
<!--[RenderingDebounceInputs]: /web/fundamentals/performance/rendering/debounce-your-input-handlers  -->
<!--[RenderingManageLayers]: /web/fundamentals/performance/rendering/stick-to-compositor-only-properties-and-manage-layer-count  -->  
<!--[RenderingOptimizeJS]: /web/fundamentals/performance/rendering/optimize-javascript-execution  -->  
<!--[RenderingPerformance]: /web/fundamentals/performance/rendering  -->  
<!--[RenderingReduceScope]: /web/fundamentals/performance/rendering/reduce-the-scope-and-complexity-of-style-calculations  -->  
<!--[RenderingSimplifyPaint]: /web/fundamentals/performance/rendering/simplify-paint-complexity-and-reduce-paint-areas  -->  

<!--[StackOverflowAlphabetBrowserDevtools]: https://stackoverflow.com/questions/ask?tags=alphabet-browser-devtools "Alphabet Browser - Stack Overflow"  -->  

> [!NOTE]
> <span data-ttu-id="1e9ca-267">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1e9ca-267">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="1e9ca-268">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/index) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="1e9ca-268">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="1e9ca-270">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1e9ca-270">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
