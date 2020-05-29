---
title: Commencer à analyser les performances de l’exécution
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: bff2d2fb0ff8424303289183ca8c5935ef477381
ms.sourcegitcommit: 50991a04c18283a8890ae33fcc3491c0476c7684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611740"
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







# <span data-ttu-id="9ac0d-103">Commencer à analyser les performances de l’exécution</span><span class="sxs-lookup"><span data-stu-id="9ac0d-103">Get Started With Analyzing Runtime Performance</span></span>   



> [!NOTE]
> <span data-ttu-id="9ac0d-104">Pour plus d’informations sur le chargement plus rapide de vos pages, voir [optimiser le site Web][DevtoolsSpeedGetStarted] .</span><span class="sxs-lookup"><span data-stu-id="9ac0d-104">See [Optimize Website Speed][DevtoolsSpeedGetStarted] to learn how to make your pages load faster.</span></span>  

<span data-ttu-id="9ac0d-105">La performance du runtime correspond à la façon dont votre page s’exécute lorsque celle-ci est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-105">Runtime performance is how your page performs when it is running, as opposed to loading.</span></span>  <span data-ttu-id="9ac0d-106">Ce didacticiel vous explique comment utiliser le panneau performances de Microsoft Edge DevTools pour analyser les performances de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-106">This tutorial teaches you how to use the Microsoft Edge DevTools Performance panel to analyze runtime performance.</span></span>  <span data-ttu-id="9ac0d-107">En ce qui concerne le modèle **ferroviaire** , les compétences que vous apprenez dans ce didacticiel sont utiles pour analyser les phases de réponse, d’animation et d’inactivité de votre page.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-107">In terms of the **RAIL** model, the skills you learn in this tutorial are useful for analyzing the Response, Animation, and Idle phases of your page.</span></span>  

<!--todo: add rail link when section is ready -->  

## <span data-ttu-id="9ac0d-108">Prise en main</span><span class="sxs-lookup"><span data-stu-id="9ac0d-108">Get started</span></span>   

<span data-ttu-id="9ac0d-109">Dans ce didacticiel, vous ouvrez DevTools sur une page active, puis utilisez le volet performance pour trouver un goulet d’étranglement de performance dans la page.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-109">In this tutorial, you open DevTools on a live page and use the Performance panel to find a performance bottleneck on the page.</span></span>  

1.  <span data-ttu-id="9ac0d-110">Ouvrez Microsoft Edge en **mode InPrivate**.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-110">Open Microsoft Edge in **InPrivate Mode**.</span></span>  <span data-ttu-id="9ac0d-111">Le mode InPrivate vérifie que Microsoft Edge s’exécute dans un état propre.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-111">InPrivate Mode ensures that Microsoft Edge runs in a clean state.</span></span>  <span data-ttu-id="9ac0d-112">Par exemple, si vous avez un grand nombre d’extensions installées, ces extensions peuvent créer un bruit dans vos mesures de performances.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-112">For example, if you have a lot of extensions installed, those extensions might create noise in your performance measurements.</span></span>  
    
    <!--TODO: replace section when updated for new Edge  -->
    
1.  <span data-ttu-id="9ac0d-113">Chargez la page suivante dans votre fenêtre InPrivate.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-113">Load the following page in your InPrivate window.</span></span>  <span data-ttu-id="9ac0d-114">Il s’agit de la démonstration que vous allez Profiler.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-114">This is the demo that you're going to profile.</span></span>  <span data-ttu-id="9ac0d-115">La page affiche un grand nombre d’icônes déplacées vers le haut et vers le bas.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-115">The page shows a bunch of little icons moving up and down.</span></span>  
    
    ```https
    https://microsoft-edge-chromium-devtools.glitch.me/jank/
    ```  
    
1.  <span data-ttu-id="9ac0d-116">Appuyez sur `Control` + `Shift` + `I` \ (Windows \) ou `Command` + `Option` + `I` \ (MacOS \) pour ouvrir devtools.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-116">Press `Control`+`Shift`+`I` \(Windows\) or `Command`+`Option`+`I` \(macOS\) to open DevTools.</span></span>  
    
    > ###### <span data-ttu-id="9ac0d-117">Figure1</span><span class="sxs-lookup"><span data-stu-id="9ac0d-117">Figure 1</span></span>  
    > <span data-ttu-id="9ac0d-118">La démonstration à gauche et DevTools sur la droite</span><span class="sxs-lookup"><span data-stu-id="9ac0d-118">The demo on the left, and DevTools on the right</span></span>  
    > ![La démonstration à gauche et DevTools sur la droite][ImageGetStarted]  
    
    > [!NOTE]
    > <span data-ttu-id="9ac0d-120">Pour le reste des captures d’écran, DevTools est [ancré dans une fenêtre séparée][DevtoolsCustomizePlacement] pour que vous puissiez mieux voir le contenu.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-120">For the rest of the screenshots, DevTools is [undocked to a separate window][DevtoolsCustomizePlacement] so that you can see the contents better.</span></span>  
    
### <span data-ttu-id="9ac0d-121">Simuler une UC mobile</span><span class="sxs-lookup"><span data-stu-id="9ac0d-121">Simulate a mobile CPU</span></span>  

<span data-ttu-id="9ac0d-122">Les appareils mobiles disposent d’une puissance UC plus réduite que les ordinateurs de bureau et les ordinateurs portables.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-122">Mobile devices have much less CPU power than desktops and laptops.</span></span>  <span data-ttu-id="9ac0d-123">Dès lors que vous profilez une page, utilisez la limitation de l’UC pour simuler l’exécution de votre page sur les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-123">Whenever you profile a page, use CPU Throttling to simulate how your page performs on mobile devices.</span></span>  

1.  <span data-ttu-id="9ac0d-124">Dans DevTools, cliquez sur l’onglet **performance** .</span><span class="sxs-lookup"><span data-stu-id="9ac0d-124">In DevTools, click the **Performance** tab.</span></span>  
1.  <span data-ttu-id="9ac0d-125">Vérifiez que la case à cocher **captures d’écran** est activée.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-125">Make sure that the **Screenshots** checkbox is enabled.</span></span>  
1.  <span data-ttu-id="9ac0d-126">Cliquez sur paramètres de capture **paramètres de capture** ![ ][ImageCaptureSettingsIcon] .</span><span class="sxs-lookup"><span data-stu-id="9ac0d-126">Click **Capture Settings** ![Capture Settings][ImageCaptureSettingsIcon].</span></span>  <span data-ttu-id="9ac0d-127">DevTools révèle les paramètres liés à la manière dont il capture les métriques de performances.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-127">DevTools reveals settings related to how it captures performance metrics.</span></span>  
1.  <span data-ttu-id="9ac0d-128">Pour **processeur**, sélectionnez **4x Slowdown**.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-128">For **CPU**, select **4x slowdown**.</span></span>  <span data-ttu-id="9ac0d-129">DevTools limite votre processeur de sorte qu’il soit 4 fois plus lent que d’habitude.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-129">DevTools throttles your CPU so that it is 4 times slower than usual.</span></span>  
    
    > ###### <span data-ttu-id="9ac0d-130">Figure 2</span><span class="sxs-lookup"><span data-stu-id="9ac0d-130">Figure 2</span></span>  
    > <span data-ttu-id="9ac0d-131">Limitation de l’UC</span><span class="sxs-lookup"><span data-stu-id="9ac0d-131">CPU throttling</span></span>  
    > ![Limitation de l’UC][ImageCPUThrottling]  
    
    > [!NOTE]
    > <span data-ttu-id="9ac0d-133">Lorsque vous testez d’autres pages, si vous voulez vous assurer qu’elles fonctionnent bien sur les appareils mobiles de bas niveau, définissez une limitation d’UC de **6 à 6 ralentissements**.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-133">When testing other pages, if you want to ensure that they work well on low-end mobile devices, set CPU Throttling to **6x slowdown**.</span></span>  <span data-ttu-id="9ac0d-134">Cette démonstration ne fonctionne pas correctement avec 6 fois, de sorte qu’elle utilise uniquement 4x Slowdown à des fins d’instructions.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-134">This demo doesn't work well with 6x slowdown, so it just uses 4x slowdown for instructional purposes.</span></span>  
    
### <span data-ttu-id="9ac0d-135">Configurer la démonstration</span><span class="sxs-lookup"><span data-stu-id="9ac0d-135">Set up the demo</span></span>  

<span data-ttu-id="9ac0d-136">Il est difficile de créer une démonstration de performance d’exécution qui fonctionne de façon cohérente pour tous les lecteurs de ce site Web.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-136">It is hard to create a runtime performance demo that works consistently for all readers of this website.</span></span>  <span data-ttu-id="9ac0d-137">Dans cette section, vous pouvez personnaliser la démonstration pour vous assurer que votre interface est relativement cohérente avec les captures d’écran et les descriptions qui s’affichent dans ce didacticiel, quelle que soit la configuration de votre compte.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-137">This section lets you customize the demo to ensure that your experience is relatively consistent with the screenshots and descriptions you see in this tutorial, regardless of your particular setup.</span></span>

1.  <span data-ttu-id="9ac0d-138">Continuez à cliquer sur **Ajouter 10** jusqu’à ce que l’icône bleue se déplace sensiblement plus lentement qu’auparavant.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-138">Keep clicking **Add 10** until the blue icons move noticeably slower than before.</span></span>  <span data-ttu-id="9ac0d-139">Sur une machine haut de gamme, il est possible qu’il y ait plus de 20 clics.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-139">On a high-end machine, it may take about 20 clicks.</span></span>  
1.  <span data-ttu-id="9ac0d-140">Cliquez sur **optimiser**.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-140">Click **Optimize**.</span></span>  <span data-ttu-id="9ac0d-141">Les icônes bleues doivent se déplacer plus rapidement et plus facilement.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-141">The blue icons should move faster and more smoothly.</span></span>  

    > [!NOTE]
    > <span data-ttu-id="9ac0d-142">Si vous ne voyez pas une différence notable entre les versions optimisées et non optimisées, essayez de cliquer sur **soustraire 10** fois et de réessayer.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-142">If you don't see a noticeable difference between the optimized and un-optimized versions, try clicking **Subtract 10** a few times and trying again.</span></span>  
    > <span data-ttu-id="9ac0d-143">Si vous ajoutez un trop grand nombre d’icônes bleues, vous allez simplement augmenter la capacité du processeur et vous ne verrez pas une différence majeure dans les résultats pour les deux versions.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-143">If you add too many blue icons, you're just going to max out the CPU and you're not going to see a major difference in the results for the two versions.</span></span>  

1.  <span data-ttu-id="9ac0d-144">Cliquez sur **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-144">Click **Un-Optimize**.</span></span>  <span data-ttu-id="9ac0d-145">Les icônes bleues se déplacent plus lentement et Jank.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-145">The blue icons move slower and with more jank again.</span></span>  

### <span data-ttu-id="9ac0d-146">Enregistrer les performances d’exécution</span><span class="sxs-lookup"><span data-stu-id="9ac0d-146">Record runtime performance</span></span>   

<span data-ttu-id="9ac0d-147">Lorsque vous avez exécuté la version optimisée de la page, les icônes bleu se déplacent plus vite.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-147">When you ran the optimized version of the page, the blue icons move faster.</span></span>  
<span data-ttu-id="9ac0d-148">Pourquoi?</span><span class="sxs-lookup"><span data-stu-id="9ac0d-148">Why is that?</span></span>  <span data-ttu-id="9ac0d-149">Les deux versions sont supposées déplacer les icônes de la même quantité d’espace sur une même durée.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-149">Both versions are supposed to move the icons the same amount of space in the same amount of time.</span></span>  <span data-ttu-id="9ac0d-150">Prenez un enregistrement dans le panneau performance pour découvrir comment détecter le goulet d’étranglement de performance dans la version non optimisée.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-150">Take a recording in the Performance panel to learn how to detect the performance bottleneck in the un-optimized version.</span></span>  

1.  <span data-ttu-id="9ac0d-151">Dans DevTools, cliquez sur **Enregistrer** l' ![ enregistrement ][ImageRecordIcon] .</span><span class="sxs-lookup"><span data-stu-id="9ac0d-151">In DevTools, click **Record** ![Record][ImageRecordIcon].</span></span>  
    <span data-ttu-id="9ac0d-152">DevTools capture les métriques de performances lors de l’exécution de la page.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-152">DevTools captures performance metrics as the page runs.</span></span>  
    
    > ###### <span data-ttu-id="9ac0d-153">Figure3</span><span class="sxs-lookup"><span data-stu-id="9ac0d-153">Figure 3</span></span> 
    > <span data-ttu-id="9ac0d-154">Profil de la page</span><span class="sxs-lookup"><span data-stu-id="9ac0d-154">Profiling the page</span></span>  
    > ![Profil de la page][ImagePageProfiling]  
    
1.  <span data-ttu-id="9ac0d-156">Patientez quelques secondes.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-156">Wait a few seconds.</span></span>  
1.  <span data-ttu-id="9ac0d-157">Cliquez sur **arrêter**.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-157">Click **Stop**.</span></span>  <span data-ttu-id="9ac0d-158">DevTools arrête d’enregistrer, traite les données, puis affiche les résultats dans le panneau performance.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-158">DevTools stops recording, processes the data, then displays the results on the Performance panel.</span></span>  
    
    > ###### <span data-ttu-id="9ac0d-159">Figure 4</span><span class="sxs-lookup"><span data-stu-id="9ac0d-159">Figure 4</span></span>  
    > <span data-ttu-id="9ac0d-160">Résultats du profil</span><span class="sxs-lookup"><span data-stu-id="9ac0d-160">The results of the profile</span></span>  
    > ![Résultats du profil][ImageProfileResults]  

<span data-ttu-id="9ac0d-162">C’est un volume de données énorme.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-162">Wow, that is an overwhelming amount of data.</span></span>  <span data-ttu-id="9ac0d-163">Ne vous inquiétez pas, c’est bien plus clair.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-163">Don't worry, it'll all make more sense shortly.</span></span>  

## <span data-ttu-id="9ac0d-164">Analyser les résultats</span><span class="sxs-lookup"><span data-stu-id="9ac0d-164">Analyze the results</span></span>   

<span data-ttu-id="9ac0d-165">Une fois que vous avez enregistré les performances de la page, vous pouvez mesurer l’efficacité de la page et trouver les causes éventuelles.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-165">Once you've got a recording the performance of the page, you can measure how poor the performance of the page is, and find the any causes.</span></span>  

### <span data-ttu-id="9ac0d-166">Analyser les images par seconde</span><span class="sxs-lookup"><span data-stu-id="9ac0d-166">Analyze frames per second</span></span>  

<span data-ttu-id="9ac0d-167">Le principal indicateur de mesure des performances d’une animation est le nombre d’images par seconde (FPS).</span><span class="sxs-lookup"><span data-stu-id="9ac0d-167">The main metric for measuring the performance of any animation is frames per second \(FPS\).</span></span>  <span data-ttu-id="9ac0d-168">Les utilisateurs sont satisfaits lorsque les animations s’exécutent à 60 ips.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-168">Users are happy when animations run at 60 FPS.</span></span>  

1.  <span data-ttu-id="9ac0d-169">Regardez le graphique **fps** .</span><span class="sxs-lookup"><span data-stu-id="9ac0d-169">Look at the **FPS** chart.</span></span>  <span data-ttu-id="9ac0d-170">Dès lors que vous voyez une barre rouge au-dessus de fps, cela signifie que la fréquence d' **images**a été déplacée et qu’elle est probablement à l’abri de l’utilisation de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-170">Whenever you see a red bar above **FPS**, it means that the framerate dropped so low that it is probably harming the user experience.</span></span>  <span data-ttu-id="9ac0d-171">En règle générale, plus la barre verte est élevée, plus la fréquence d’images est élevée.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-171">In general, the higher the green bar, the higher the FPS.</span></span>  
    
    > ###### <span data-ttu-id="9ac0d-172">Figure 5</span><span class="sxs-lookup"><span data-stu-id="9ac0d-172">Figure 5</span></span>  
    > <span data-ttu-id="9ac0d-173">Graphique FPS</span><span class="sxs-lookup"><span data-stu-id="9ac0d-173">The FPS chart</span></span>  
    > ![Graphique FPS][ImageFPSChart]  

1.  <span data-ttu-id="9ac0d-175">Sous le graphique **fps** , vous pouvez voir le graphique **CPU** .</span><span class="sxs-lookup"><span data-stu-id="9ac0d-175">Below the **FPS** chart you see the **CPU** chart.</span></span>  <span data-ttu-id="9ac0d-176">Les couleurs du graphique **UC** correspondent aux couleurs sous l’onglet **Résumé** , au bas du panneau de performance.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-176">The colors in the **CPU** chart correspond to the colors in the **Summary** tab, at the bottom of the Performance panel.</span></span>  <span data-ttu-id="9ac0d-177">Le fait que le graphique **UC** est plein de couleur signifie que le processeur a été épuisé lors de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-177">The fact that the **CPU** chart is full of color means that the CPU was maxed out during the recording.</span></span>  <span data-ttu-id="9ac0d-178">Chaque fois que vous voyez le processeur épuisé pour des périodes longues, il s’agit d’un indicateur pour trouver des moyens d’effectuer moins de tâches.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-178">Whenever you see the CPU maxed out for long periods, it is a cue to find ways to do less work.</span></span>  
    
    > ###### <span data-ttu-id="9ac0d-179">Figure 6</span><span class="sxs-lookup"><span data-stu-id="9ac0d-179">Figure 6</span></span>  
    > <span data-ttu-id="9ac0d-180">Onglet graphique UC et synthèse</span><span class="sxs-lookup"><span data-stu-id="9ac0d-180">The CPU chart and Summary tab</span></span>  
    > ![Onglet graphique UC et synthèse][ImageCPUSummary]  

1.  <span data-ttu-id="9ac0d-182">Positionnez le pointeur de la souris sur le graphique **fps**, **UC**ou **net** .</span><span class="sxs-lookup"><span data-stu-id="9ac0d-182">Hover your mouse over the **FPS**, **CPU**, or **NET** charts.</span></span>  <span data-ttu-id="9ac0d-183">DevTools affiche une capture d’écran de la page à ce moment.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-183">DevTools shows a screenshot of the page at that point in time.</span></span>  <span data-ttu-id="9ac0d-184">Déplacez votre souris vers la gauche ou la droite pour relire l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-184">Move your mouse left and right to replay the recording.</span></span>  <span data-ttu-id="9ac0d-185">Il s’agit de la fonction de nettoyage, qui est utile pour analyser manuellement la progression des animations.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-185">This is called scrubbing, and it is useful for manually analyzing the progression of animations.</span></span>  
    
    > ###### <span data-ttu-id="9ac0d-186">Figure 7</span><span class="sxs-lookup"><span data-stu-id="9ac0d-186">Figure 7</span></span>  
    > <span data-ttu-id="9ac0d-187">Affichage d’une capture d’écran de la page entourant la marque 2500ms de l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="9ac0d-187">Viewing a screenshot of the page around the 2500ms mark of the recording</span></span>  
    > ![Affichage d’une capture d’écran de la page entourant la marque 2500ms de l’enregistrement][ImageViewingScreenshot]  

1.  <span data-ttu-id="9ac0d-189">Dans la section **trames** , placez le pointeur de la souris sur l’un des carrés verts.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-189">In the **Frames** section, hover your mouse over one of the green squares.</span></span>  <span data-ttu-id="9ac0d-190">DevTools vous indique les FPS pour cette image particulière.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-190">DevTools shows you the FPS for that particular frame.</span></span>  <span data-ttu-id="9ac0d-191">Chaque image est probablement bien en dessous de la cible de 60 images par seconde.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-191">Each frame is probably well below the target of 60 FPS.</span></span>  
    
    > ###### <span data-ttu-id="9ac0d-192">Figure8</span><span class="sxs-lookup"><span data-stu-id="9ac0d-192">Figure 8</span></span>  
    > <span data-ttu-id="9ac0d-193">Survol d’un cadre</span><span class="sxs-lookup"><span data-stu-id="9ac0d-193">Hovering over a frame</span></span>  
    > ![Survol d’un cadre][ImageFrameHover]  

<span data-ttu-id="9ac0d-195">Bien entendu, avec cette démonstration, il est très évident que la page ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-195">Of course, with this demo, it is pretty obvious that the page is not performing well.</span></span>  <span data-ttu-id="9ac0d-196">Néanmoins, dans de véritables scénarios, il est possible qu’il n’y ait pas de clarté.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-196">But in real scenarios, it may not be so clear, so having all of these tools to make measurements comes in handy.</span></span>  

#### <span data-ttu-id="9ac0d-197">Bonus: Ouvrez la jauge FPS</span><span class="sxs-lookup"><span data-stu-id="9ac0d-197">Bonus: Open the FPS meter</span></span>  

<span data-ttu-id="9ac0d-198">Un autre outil pratique est le Vumètre d’FPS, qui fournit des estimations en temps réel pour les images par seconde lors de l’exécution de la page.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-198">Another handy tool is the FPS meter, which provides real-time estimates for FPS as the page runs.</span></span>  

1.  <span data-ttu-id="9ac0d-199">Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le menu de commandes.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-199">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="9ac0d-200">Commencez `Rendering` à taper dans le menu de commandes et sélectionnez **afficher le rendu**.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-200">Start typing `Rendering` in the Command Menu and select **Show Rendering**.</span></span>  
1.  <span data-ttu-id="9ac0d-201">Dans l’onglet **rendu** , activez l' **indicateur fps**.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-201">In the **Rendering** tab, enable **FPS Meter**.</span></span>  <span data-ttu-id="9ac0d-202">Une nouvelle superposition s’affiche dans le coin supérieur droit de votre fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-202">A new overlay appears in the top-right of your viewport.</span></span>  
    
    > ###### <span data-ttu-id="9ac0d-203">Figure9</span><span class="sxs-lookup"><span data-stu-id="9ac0d-203">Figure 9</span></span>  
    > <span data-ttu-id="9ac0d-204">Vumètre FPS</span><span class="sxs-lookup"><span data-stu-id="9ac0d-204">The FPS meter</span></span>  
    > ![Vumètre FPS][ImageFPSMeter]  

1.  <span data-ttu-id="9ac0d-206">Désactivez la **jauge fps** et appuyez `Escape` pour fermer l’onglet **rendu** .  Dans ce didacticiel, vous ne pourrez pas l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-206">Disable the **FPS Meter** and press `Escape` to close the **Rendering** tab.  You won't be using it in this tutorial.</span></span>  

### <span data-ttu-id="9ac0d-207">Détecter le goulet d’étranglement</span><span class="sxs-lookup"><span data-stu-id="9ac0d-207">Find the bottleneck</span></span>  

<span data-ttu-id="9ac0d-208">À présent que vous avez mesuré et vérifié que l’animation ne fonctionne pas correctement, la question suivante consiste à vous répondre: pourquoi?</span><span class="sxs-lookup"><span data-stu-id="9ac0d-208">Now that you've measured and verified that the animation is not performing well, the next question to answer is:  why?</span></span>  

1.  <span data-ttu-id="9ac0d-209">Notez l’onglet Résumé.  Si aucun événement n’est sélectionné, cet onglet vous montre une répartition des activités.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-209">Note the summary tab.  When no events are selected, this tab shows you a breakdown of activity.</span></span>  <span data-ttu-id="9ac0d-210">La page a dépensé la majeure partie de son temps de rendu.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-210">The page spent most of its time rendering.</span></span>  <span data-ttu-id="9ac0d-211">Étant donné que les performances constituent une idée d’avoir moins de travail, vous pouvez réduire la durée du travail de rendu.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-211">Since performance is the art of doing less work, your goal is to reduce the amount of time spent doing rendering work.</span></span>  
    
    > ###### <span data-ttu-id="9ac0d-212">Figure10</span><span class="sxs-lookup"><span data-stu-id="9ac0d-212">Figure 10</span></span>  
    > <span data-ttu-id="9ac0d-213">Onglet Résumé</span><span class="sxs-lookup"><span data-stu-id="9ac0d-213">The Summary tab</span></span>  
    > ![Onglet Résumé][ImageSummaryTab]  

1.  <span data-ttu-id="9ac0d-215">Développez la section **principale** .</span><span class="sxs-lookup"><span data-stu-id="9ac0d-215">Expand the **Main** section.</span></span>  <span data-ttu-id="9ac0d-216">DevTools affiche un graphique d’activité sur le thread principal, au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-216">DevTools shows you a flame chart of activity on the main thread, over time.</span></span>  <span data-ttu-id="9ac0d-217">L’axe x représente l’enregistrement au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-217">The x-axis represents the recording, over time.</span></span>  <span data-ttu-id="9ac0d-218">Chaque barre représente un événement.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-218">Each bar represents an event.</span></span>  <span data-ttu-id="9ac0d-219">Une barre plus large signifie que l’événement a duré plus longtemps.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-219">A wider bar means that event took longer.</span></span>  <span data-ttu-id="9ac0d-220">L’axe y représente la pile d’appels.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-220">The y-axis represents the call stack.</span></span>  <span data-ttu-id="9ac0d-221">Lorsque des événements sont empilés les uns sur les autres, cela signifie que les événements supérieurs ont entraîné des événements plus faibles.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-221">When you see events stacked on top of each other, it means the upper events caused the lower events.</span></span>  
    
    > ##### <span data-ttu-id="9ac0d-222">Figure11</span><span class="sxs-lookup"><span data-stu-id="9ac0d-222">Figure 11</span></span>  
    > <span data-ttu-id="9ac0d-223">Section principale</span><span class="sxs-lookup"><span data-stu-id="9ac0d-223">The Main section</span></span>  
    > ![Section principale][ImageMainSection]  

1.  <span data-ttu-id="9ac0d-225">L’enregistrement comporte un grand nombre de données.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-225">There is a lot of data in the recording.</span></span>  <span data-ttu-id="9ac0d-226">Effectuez un zoom avant sur un seul événement en cliquant, en maintenant le bouton enfoncé et en faisant glisser le pointeur de la souris sur la **vue d’ensemble**, qui est la section incluant les graphiques **fps**, **UC**et **net** .</span><span class="sxs-lookup"><span data-stu-id="9ac0d-226">Zoom in on a single event by clicking, holding, and dragging your mouse over the **Overview**, which is the section that includes the **FPS**, **CPU**, and **NET** charts.</span></span>  <span data-ttu-id="9ac0d-227">Les onglets **principales** section et **Résumé** affichent uniquement les informations relatives à la partie sélectionnée de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-227">The **Main** section and **Summary** tab only display information for the selected portion of the recording.</span></span>  
    
    > ###### <span data-ttu-id="9ac0d-228">Figure12</span><span class="sxs-lookup"><span data-stu-id="9ac0d-228">Figure 12</span></span>  
    > <span data-ttu-id="9ac0d-229">Zoom avant sur un seul événement</span><span class="sxs-lookup"><span data-stu-id="9ac0d-229">Zoomed in on a single event</span></span>  
    > ![Zoom avant sur un événement][ImageZoomedAnimation]  
    
    > [!NOTE]
    > <span data-ttu-id="9ac0d-231">Pour effectuer un zoom, vous pouvez également mettre au point la section **principale** en cliquant sur son arrière-plan ou en sélectionnant un événement, et en appuyant sur les `W` `A` touches,, `S` et `D` .</span><span class="sxs-lookup"><span data-stu-id="9ac0d-231">Another way to zoom is to focus the **Main** section by clicking its background or selecting an event, and then press the `W`, `A`, `S`, and `D` keys.</span></span>  
    
    1.  <span data-ttu-id="9ac0d-232">Notez le triangle rouge dans le coin supérieur droit du **cadre d’animation** qui a déclenché l’événement.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-232">Note the red triangle in the top-right of the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="9ac0d-233">Dès lors que vous voyez un triangle rouge, il s’agit d’un avertissement indiquant qu’il y a peut-être un problème lié à cet événement.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-233">Whenever you see a red triangle, it is a warning that there may be an issue related to this event.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="9ac0d-234">Le **Frame d’animation déclenché est déclenché** chaque fois qu’un [ `requestAnimationFrame()` rappel][MDNWebRequestAnimationFrame] est exécuté.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-234">The **Animation Frame Fired** event occurs whenever a [`requestAnimationFrame()` callback][MDNWebRequestAnimationFrame] is run.</span></span>  
    
1.  <span data-ttu-id="9ac0d-235">Cliquez sur l’événement déclenché par le cadre de l' **animation** .</span><span class="sxs-lookup"><span data-stu-id="9ac0d-235">Click the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="9ac0d-236">L’onglet **Résumé** affiche maintenant des informations sur cet événement.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-236">The **Summary** tab now shows you information about that event.</span></span>  <span data-ttu-id="9ac0d-237">Notez le lien d' **affichage** .</span><span class="sxs-lookup"><span data-stu-id="9ac0d-237">Note the **Reveal** link.</span></span>  <span data-ttu-id="9ac0d-238">Le fait de cliquer sur cela amène DevTools à mettre en surbrillance l’événement qui a déclenché l’événement déclenché par le cadre de l' **animation** .</span><span class="sxs-lookup"><span data-stu-id="9ac0d-238">Clicking that causes DevTools to highlight the event that initiated the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="9ac0d-239">Notez également le lien **app. js: 95** .</span><span class="sxs-lookup"><span data-stu-id="9ac0d-239">Also note the **app.js:95** link.</span></span>  <span data-ttu-id="9ac0d-240">Un clic vous permet d’atteindre la ligne appropriée dans le code source.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-240">Clicking that jumps you to the relevant line in the source code.</span></span>
    
    > ##### <span data-ttu-id="9ac0d-241">Figure13</span><span class="sxs-lookup"><span data-stu-id="9ac0d-241">Figure 13</span></span>  
    > <span data-ttu-id="9ac0d-242">Plus d’informations sur l’événement déclenché par le cadre d’animation</span><span class="sxs-lookup"><span data-stu-id="9ac0d-242">More information about the Animation Frame Fired event</span></span>  
    > ![Plus d’informations sur l’événement déclenché par le cadre d’animation][ImageAnimationFrameFired]  
    
    > [!NOTE]
    > <span data-ttu-id="9ac0d-244">Après avoir sélectionné un événement, utilisez les touches de direction pour sélectionner les événements en regard de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-244">After selecting an event, use the arrow keys to select the events next to it.</span></span>  

1.  <span data-ttu-id="9ac0d-245">Sous l’événement **app. Update** , il existe un ensemble d’événements Purple.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-245">Under the **app.update** event, there is a bunch of purple events.</span></span>  <span data-ttu-id="9ac0d-246">S’ils étaient plus larges, il semble que chacun d’eux dispose d’un triangle rouge.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-246">If they were wider, it looks as though each one might have a red triangle on it.</span></span>  <span data-ttu-id="9ac0d-247">Cliquez sur l’un des événements de **disposition** Purple désormais.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-247">Click one of the purple **Layout** events now.</span></span>  <span data-ttu-id="9ac0d-248">DevTools fournit des informations supplémentaires sur l’événement sous l’onglet **Résumé** .  En effet, il y a un avertissement sur les flux forcés \ (un autre mot pour la disposition \).</span><span class="sxs-lookup"><span data-stu-id="9ac0d-248">DevTools provides more information about the event in the **Summary** tab.  Indeed, there is a warning about forced reflows \(another word for layout\).</span></span>  

1.  <span data-ttu-id="9ac0d-249">Sous l’onglet **Résumé** , cliquez sur le lien **app. js: 71** sous **disposition forcée**.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-249">In the **Summary** tab, click the **app.js:71** link under **Layout Forced**.</span></span>  <span data-ttu-id="9ac0d-250">DevTools vous permet d’accéder à la ligne de code qui force la mise en page.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-250">DevTools takes you to the line of code that forced the layout.</span></span>  
    
    > ##### <span data-ttu-id="9ac0d-251">Figure14</span><span class="sxs-lookup"><span data-stu-id="9ac0d-251">Figure 14</span></span>  
    > <span data-ttu-id="9ac0d-252">Ligne de code à l’origine de la disposition forcée.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-252">The line of code that caused the forced layout</span></span>  
    > ![Ligne de code à l’origine de la disposition forcée.][ImageForcedLayoutSRC]  
    
    > [!NOTE]
    > <span data-ttu-id="9ac0d-254">Le problème lié à ce code est le suivant: dans chaque cadre d’animation, il modifie le style de chaque icône, puis interroge la position de chaque icône de la page.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-254">The problem with this code is that, in each animation frame, it changes the style for each icon, and then queries the position of each icon on the page.</span></span>  <span data-ttu-id="9ac0d-255">Dans la mesure où les styles ont changé, le navigateur ne sait pas si chaque position de l’icône a changé, donc il doit redisposer l’icône afin de calculer sa position.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-255">Because the styles changed, the browser doesn't know if each icon position changed, so it has to re-layout the icon in order to compute its position.</span></span>  <!--  See [Avoid forced synchronous layouts][RenderingAvoidSynchronousLayouts] to learn more.  -->

<!-- todo: add layouts section when available -->

<span data-ttu-id="9ac0d-256">Phew!</span><span class="sxs-lookup"><span data-stu-id="9ac0d-256">Phew!</span></span>  <span data-ttu-id="9ac0d-257">C’est un grand nombre d’entre eux, mais vous avez à présent une base solide dans le flux de travail de base pour analyser les performances de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-257">That was a lot to take in, but you now have a solid foundation in the basic workflow for analyzing runtime performance.</span></span>  <span data-ttu-id="9ac0d-258">Bien fait.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-258">Good job.</span></span>  

### <span data-ttu-id="9ac0d-259">Bonus: analysez la version optimisée</span><span class="sxs-lookup"><span data-stu-id="9ac0d-259">Bonus: Analyze the optimized version</span></span>  

<span data-ttu-id="9ac0d-260">À l’aide des flux de travail et des outils que vous venez d’apprendre, cliquez sur **optimiser** dans la démonstration pour activer le code optimisé, effectuer un autre enregistrement de performance, puis analyser les résultats.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-260">Using the workflows and tools that you just learned, click **Optimize** on the demo to enable the optimized code, take another performance recording, and then analyze the results.</span></span>  <span data-ttu-id="9ac0d-261">À partir de la fréquence d’affichage améliorée des événements dans le graphique de flamme de la section **principale** , vous pouvez constater que la version optimisée de l’application présente une plus grande quantité de travail, ce qui améliore les performances.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-261">From the improved framerate to the reduction in events in the flame chart in the **Main** section, you can see that the optimized version of the app does much less work, resulting in better performance.</span></span>  

> [!NOTE]
> <span data-ttu-id="9ac0d-262">Même la version «optimisée» n’est pas idéale, car elle manipule toujours la `top` propriété de chaque icône.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-262">Even this "optimized" version isn't that great, because it still manipulates the `top` property of each icon.</span></span>  <span data-ttu-id="9ac0d-263">Une meilleure approche consiste à respecter les propriétés qui affectent uniquement la composition.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-263">A better approach is to stick to properties that only affect compositing.</span></span>  
<!--  > See [Use transform and opacity changes for animations][RenderingCompositor] for more information.  -->  

<!--todo: add rendering section when available -->

## <span data-ttu-id="9ac0d-264">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="9ac0d-264">Next steps</span></span>

<!--The foundation for understanding performance is the RAIL model.  This model teaches you the performance metrics that are most important to your users.  
See [Measure Performance With The RAIL Model][RAIL] to learn more.  -->  

<span data-ttu-id="9ac0d-265">Pour plus de confort grâce au panneau performances, vous pouvez faire des exercices pratiques.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-265">To get more comfortable with the Performance panel, practice makes perfect.</span></span>  <span data-ttu-id="9ac0d-266">Essayez de Profiler vos propres pages et d’analyser les résultats.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-266">Try profiling your own pages and analyzing the results.</span></span>  <span data-ttu-id="9ac0d-267">Si vous avez des questions sur les résultats, utilisez l’icône de **Commentaires** , appuyez `Alt`  +  `Shift`  +  `I` sur Windows ( `Option`  +  `Shift`  +  `I` sur MacOS) ou [Tweet][TwitterEdgeDevtools].</span><span class="sxs-lookup"><span data-stu-id="9ac0d-267">If you have any questions about your results, use the **Feedback** icon, press `Alt` + `Shift` + `I` on Windows (`Option` + `Shift` + `I` on macOS), or [tweet at us][TwitterEdgeDevtools].</span></span>  <span data-ttu-id="9ac0d-268">Incluez des captures d’écran ou des liens vers des pages reproductibles, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-268">Include screenshots or links to reproducible pages, if possible.</span></span>

> ##### <span data-ttu-id="9ac0d-269">Figure15</span><span class="sxs-lookup"><span data-stu-id="9ac0d-269">Figure 15</span></span>
> <span data-ttu-id="9ac0d-270">Icône de **Commentaires** dans le Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="9ac0d-270">The **Feedback** icon in the Microsoft Edge DevTools</span></span>  
> ![L’icône \* \* Feedback \* \* dans Microsoft Edge DevTools][ImageFeedbackIcon]

<!-- To really master runtime performance, you've got to learn how the browser translates HTML, CSS, and JS into pixels on a screen.  The best place to start is the [Rendering Performance Overview][RenderingPerformance].  [The Anatomy Of A Frame][FrameAnatomy] dives into even more detail.  -->  

<span data-ttu-id="9ac0d-272">Enfin, il existe de nombreuses façons d’améliorer les performances de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-272">Last, there are many ways to improve runtime performance.</span></span>  <span data-ttu-id="9ac0d-273">Ce didacticiel est axé sur un goulet d’étranglement d’animation particulier qui vous permet d’effectuer une visite guidée du panneau performance, mais ce n’est qu’un des nombreux goulets d’étranglement que vous pouvez rencontrer.</span><span class="sxs-lookup"><span data-stu-id="9ac0d-273">This tutorial focused on one particular animation bottleneck to give you a focused tour through the Performance panel, but it is only one of many bottlenecks you may encounter.</span></span>  <!--  The rest of the Rendering Performance series has a lot of good tips for improving various aspects of runtime performance, such as:  -->

<!--
*   [Optimizing JS Execution][RenderingOptimizeJS]  
*   [Reduce The Scope And Complexity Of Style Calculations][RenderingReduceScope]  
*   [Avoid Large, Complex Layouts And Layout Thrashing][RenderingAvoidThrashing]  
*   [Simplify Paint Complexity And Reduce Paint Areas][RenderingSimplifyPaint]  
*   [Stick To Compositor-Only Properties And Manage Layer Count][RenderingManageLayers]  
*   [Debounce Your Input Handlers][RenderingDebounceInputs]  
-->

<!-- image links -->  

[ImageCaptureSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/capture-settings-icon.msft.png  
[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/media/record-icon.msft.png  

[ImageGetStarted]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-get-started-side-by-side.msft.png "Figure 1: démonstration à gauche et DevTools sur la droite"  
[ImageCPUThrottling]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-capture-settings.msft.png "Figure 2: limitation d’UC"  
[ImagePageProfiling]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-profiling.msft.png "Figure 3: profil de la page"  
[ImageProfileResults]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-capture-results.msft.png "Figure 4: résultats du profil"  
[ImageFPSChart]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-fps-chart.msft.png "Figure 5: graphique FPS"  
[ImageCPUSummary]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-cpu-chart.msft.png "Figure 6: affichage du graphique UC et de l’onglet synthèse, en bleu"  
[ImageViewingScreenshot]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-screenshot-hover.msft.png "Figure 7: affichage d’une capture d’écran de la page avec la marque 2500ms de l’enregistrement"  
[ImageFrameHover]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-frame-hover.msft.png "Figure 8: survol d’un cadre"  
[ImageFPSMeter]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-fps-meter-overlay.msft.png "Figure 9: vumètre d’FPS"  
[ImageSummaryTab]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-summary-tab.msft.png "Figure 10: onglet Résumé"  
[ImageMainSection]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-main.msft.png "Figure 11: section principale"  
[ImageZoomedAnimation]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-main-zoomed.msft.png "Figure 12: zoom avant sur une seule image d’animation déclenchée"  
[ImageAnimationFrameFired]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-animation-frame-fired.msft.png "Figure 13: informations supplémentaires sur l’événement déclenché par le cadre d’une animation"  
[ImageForcedLayoutSRC]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-sources-app-update.msft.png "Figure 14: ligne de code à l’origine de la disposition forcée"  
[ImageFeedbackIcon]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-feedback-icon.msft.png "Figure 15: icône * * Feedback * * dans Microsoft Edge DevTools"

<!-- links -->

[DevtoolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Changer la position de Microsoft Edge DevTools (détacher, ancrer en bas, ancrer à gauche)"  
[DevtoolsSpeedGetStarted]: /microsoft-edge/devtools-guide-chromium/speed/get-started "Optimiser la vitesse de votre site Web avec Microsoft Edge DevTools"  

[TwitterEdgeDevtools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "EdgeDevTools-publiez un tweet | Twitter"  

[MDNWebRequestAnimationFrame]: https://developer.mozilla.org/docs/Web/API/window/requestAnimationFrame "Window. requestAnimationFrame \ (\) | MDN"  

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
> <span data-ttu-id="9ac0d-293">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9ac0d-293">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="9ac0d-294">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="9ac0d-294">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="9ac0d-296">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9ac0d-296">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
