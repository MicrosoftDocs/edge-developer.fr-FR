---
title: Simuler des appareils mobiles avec le mode appareil dans Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 10c1ee12777965778ebec2d257399dc231e2a01a
ms.sourcegitcommit: 531ec8aa1f89b28bc4d271e8e995f846f2392bc3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/29/2020
ms.locfileid: "10607425"
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





# <span data-ttu-id="1b290-103">Simuler des appareils mobiles avec le mode appareil dans Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="1b290-103">Simulate Mobile Devices with Device Mode in Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="1b290-104">Utilisez le mode appareil pour obtenir un aperçu de l’apparence de votre page et de son exécution sur un appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="1b290-104">Use Device Mode to approximate how your page looks and performs on a mobile device.</span></span>  

<span data-ttu-id="1b290-105">Le mode appareil est le nom de la collection libre de fonctionnalités dans Microsoft Edge DevTools qui vous permettent de simuler des appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="1b290-105">Device Mode is the name for the loose collection of features in Microsoft Edge DevTools that help you simulate mobile devices.</span></span>  <span data-ttu-id="1b290-106">Ces fonctionnalités incluent:</span><span class="sxs-lookup"><span data-stu-id="1b290-106">These features include:</span></span>  

*   [<span data-ttu-id="1b290-107">Simulation d’une fenêtre d’affichage mobile</span><span class="sxs-lookup"><span data-stu-id="1b290-107">Simulating a mobile viewport</span></span>](#simulate-a-mobile-viewport)  
*   [<span data-ttu-id="1b290-108">Limitation du réseau</span><span class="sxs-lookup"><span data-stu-id="1b290-108">Throttling the network</span></span>](#throttle-the-network-only)  
*   [<span data-ttu-id="1b290-109">Limitation de l’UC</span><span class="sxs-lookup"><span data-stu-id="1b290-109">Throttling the CPU</span></span>](#throttle-the-cpu-only)  
*   [<span data-ttu-id="1b290-110">Simulation de géolocalisation</span><span class="sxs-lookup"><span data-stu-id="1b290-110">Simulating geolocation</span></span>](#override-geolocation)  
*   [<span data-ttu-id="1b290-111">Définir l’orientation</span><span class="sxs-lookup"><span data-stu-id="1b290-111">Setting orientation</span></span>](#set-orientation)  

## <span data-ttu-id="1b290-112">Limitations</span><span class="sxs-lookup"><span data-stu-id="1b290-112">Limitations</span></span>   

<span data-ttu-id="1b290-113">Imaginez le mode appareil comme une [approximation prioritaire][WikiApproximation] de l’apparence de votre page sur un appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="1b290-113">Think of Device Mode as a [first-order approximation][WikiApproximation] of how your page looks and feels on a mobile device.</span></span>  <span data-ttu-id="1b290-114">Le mode appareil n’exécute pas réellement votre code sur un appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="1b290-114">With Device Mode you do not actually run your code on a mobile device.</span></span>  <span data-ttu-id="1b290-115">Vous simulez l’expérience utilisateur mobile sur votre ordinateur portable ou votre ordinateur de bureau.</span><span class="sxs-lookup"><span data-stu-id="1b290-115">You simulate the mobile user experience from your laptop or desktop.</span></span>  

<span data-ttu-id="1b290-116">Certains aspects des appareils mobiles qu’DevTools ne seront jamais en mesure de simuler.</span><span class="sxs-lookup"><span data-stu-id="1b290-116">There are some aspects of mobile devices that DevTools will never be able to simulate.</span></span>  <span data-ttu-id="1b290-117">Par exemple, l’architecture des UC mobiles est très différente de l’architecture de l’ordinateur portable ou de l’UC de bureau.</span><span class="sxs-lookup"><span data-stu-id="1b290-117">For example, the architecture of mobile CPUs is very different than the architecture of laptop or desktop CPUs.</span></span>  <span data-ttu-id="1b290-118">En cas de doute, il est préférable d’exécuter votre page sur un appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="1b290-118">When in doubt, your best bet is to actually run your page on a mobile device.</span></span>  <span data-ttu-id="1b290-119">Pour afficher, modifier, déboguer et profiler le code d’une page à partir de votre ordinateur portable ou de votre ordinateur de bureau, vous pouvez utiliser [Remote Debugger] [DevToolsRemoteDebugging].</span><span class="sxs-lookup"><span data-stu-id="1b290-119">Use [Remote Debugging][DevToolsRemoteDebugging] to view, change, debug, and profile the code of a page from your laptop or desktop while it actually runs on a mobile device.</span></span>  

## <span data-ttu-id="1b290-120">Simuler une fenêtre d’affichage mobile</span><span class="sxs-lookup"><span data-stu-id="1b290-120">Simulate a mobile viewport</span></span>   

<span data-ttu-id="1b290-121">Cliquez sur **activer/désactiver** ![ le bouton bascule de la barre d’outils ][ImageDeviceToolbarIcon] de l’appareil pour ouvrir l’interface utilisateur qui vous permet de simuler une fenêtre d’affichage mobile.</span><span class="sxs-lookup"><span data-stu-id="1b290-121">Click **Toggle Device Toolbar** ![Toggle Device Toolbar][ImageDeviceToolbarIcon] to open the UI that enables you to simulate a mobile viewport.</span></span>  

> ##### <span data-ttu-id="1b290-122">Figure1</span><span class="sxs-lookup"><span data-stu-id="1b290-122">Figure 1</span></span>  
> <span data-ttu-id="1b290-123">Barre d’outils de l’appareil</span><span class="sxs-lookup"><span data-stu-id="1b290-123">The Device Toolbar</span></span>  
> ![Barre d’outils de l’appareil][ImageDeviceToolbar]  

<span data-ttu-id="1b290-125">Par défaut, la barre d’outils de l’appareil s’ouvre en mode de fenêtre d’affichage réactif.</span><span class="sxs-lookup"><span data-stu-id="1b290-125">By default the Device Toolbar opens in Responsive Viewport Mode.</span></span>  

### <span data-ttu-id="1b290-126">Mode de fenêtre d’affichage réactif</span><span class="sxs-lookup"><span data-stu-id="1b290-126">Responsive Viewport Mode</span></span>   

<span data-ttu-id="1b290-127">Faites glisser les poignées pour redimensionner la fenêtre d’affichage en fonction des dimensions dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="1b290-127">Drag the handles to resize the viewport to whatever dimensions you need.</span></span>  <span data-ttu-id="1b290-128">Vous avez d’autres valeurs dans les zones largeur et hauteur.</span><span class="sxs-lookup"><span data-stu-id="1b290-128">Or, enter specific values in the width and height boxes.</span></span>  <span data-ttu-id="1b290-129">Dans la [figure 2](#figure-2), la largeur est définie sur `626` et la hauteur est définie sur `516` .</span><span class="sxs-lookup"><span data-stu-id="1b290-129">In [Figure 2](#figure-2), the width is set to `626` and the height is set to `516`.</span></span>  

> ##### <span data-ttu-id="1b290-130">Figure 2</span><span class="sxs-lookup"><span data-stu-id="1b290-130">Figure 2</span></span>  
> <span data-ttu-id="1b290-131">Poignées permettant de modifier les dimensions de la fenêtre d’affichage en mode de fenêtre d’affichage réactif</span><span class="sxs-lookup"><span data-stu-id="1b290-131">The handles for changing the dimensions of the viewport when in Responsive Viewport Mode</span></span>  
> ![Poignées permettant de modifier les dimensions de la fenêtre d’affichage en mode de fenêtre d’affichage réactif][ImageResponsiveHandles]  

#### <span data-ttu-id="1b290-133">Afficher les requêtes multimédias</span><span class="sxs-lookup"><span data-stu-id="1b290-133">Show media queries</span></span>   

<span data-ttu-id="1b290-134">Pour afficher les points d’arrêt de requête multimédias au-dessus de votre fenêtre d’affichage, cliquez sur **plus d’options** , puis sélectionnez **afficher les requêtes multimédias**.</span><span class="sxs-lookup"><span data-stu-id="1b290-134">To show media query breakpoints above your viewport, click **More options** and then select **Show media queries**.</span></span>  

> ##### <span data-ttu-id="1b290-135">Figure3</span><span class="sxs-lookup"><span data-stu-id="1b290-135">Figure 3</span></span>  
> <span data-ttu-id="1b290-136">Afficher les requêtes multimédias</span><span class="sxs-lookup"><span data-stu-id="1b290-136">Show media queries</span></span>  
> ![Afficher les requêtes multimédias][ImageShowMediaQueries]  

<span data-ttu-id="1b290-138">Cliquez sur un point d’arrêt pour modifier la largeur de la fenêtre d’affichage de telle sorte que le point d’arrêt soit déclenché.</span><span class="sxs-lookup"><span data-stu-id="1b290-138">Click a breakpoint to change the width of the viewport so that the breakpoint gets triggered.</span></span>  

> ##### <span data-ttu-id="1b290-139">Figure 4</span><span class="sxs-lookup"><span data-stu-id="1b290-139">Figure 4</span></span>  
> <span data-ttu-id="1b290-140">Cliquez sur un point d’arrêt pour modifier la largeur de la fenêtre d’affichage</span><span class="sxs-lookup"><span data-stu-id="1b290-140">Click a breakpoint to change the width of the viewport</span></span>  
> ![Cliquez sur un point d’arrêt pour modifier la largeur de la fenêtre d’affichage][ImageBreakpoint]  

#### <span data-ttu-id="1b290-142">Définir le type d’appareil</span><span class="sxs-lookup"><span data-stu-id="1b290-142">Set the device type</span></span>   

<span data-ttu-id="1b290-143">Utilisez la liste **type d’appareil** pour simuler un appareil mobile ou un appareil de bureau.</span><span class="sxs-lookup"><span data-stu-id="1b290-143">Use the **Device Type** list to simulate a mobile device or desktop device.</span></span>  

> ##### <span data-ttu-id="1b290-144">Figure 5</span><span class="sxs-lookup"><span data-stu-id="1b290-144">Figure 5</span></span>  
> <span data-ttu-id="1b290-145">Liste **type d’appareil**</span><span class="sxs-lookup"><span data-stu-id="1b290-145">The **Device Type** list</span></span>  
> ![Liste type d’appareil][ImageDeviceType]  

<span data-ttu-id="1b290-147">Le tableau ci-dessous décrit les différences entre les options.</span><span class="sxs-lookup"><span data-stu-id="1b290-147">The table below describes the differences between the options.</span></span>  <span data-ttu-id="1b290-148">La **méthode de rendu** fait référence à la façon dont Microsoft Edge effectue le rendu de la page en tant que fenêtre d’affichage mobile ou de bureau.</span><span class="sxs-lookup"><span data-stu-id="1b290-148">**Rendering method** refers to whether Microsoft Edge renders the page as a mobile or desktop viewport.</span></span>  <span data-ttu-id="1b290-149">**Icône du curseur** désigne le type de curseur qui s’affiche lorsque vous survolez la page.</span><span class="sxs-lookup"><span data-stu-id="1b290-149">**Cursor icon** refers to what type of cursor you see when you hover over the page.</span></span>  <span data-ttu-id="1b290-150">Les **événements déclenchés** font référence au déclenchement de la page `touch` ou aux `click` événements lorsque vous interagissez avec la page.</span><span class="sxs-lookup"><span data-stu-id="1b290-150">**Events fired** refers to whether the page fires `touch` or `click` events when you interact with the page.</span></span>  

| <span data-ttu-id="1b290-151">Option</span><span class="sxs-lookup"><span data-stu-id="1b290-151">Option</span></span> | <span data-ttu-id="1b290-152">Méthode de rendu</span><span class="sxs-lookup"><span data-stu-id="1b290-152">Rendering method</span></span> | <span data-ttu-id="1b290-153">Icône du curseur</span><span class="sxs-lookup"><span data-stu-id="1b290-153">Cursor icon</span></span> | <span data-ttu-id="1b290-154">Événements déclenchés</span><span class="sxs-lookup"><span data-stu-id="1b290-154">Events fired</span></span> |  
|:--- |:--- |:--- |:--- |  
| <span data-ttu-id="1b290-155">Appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="1b290-155">Mobile</span></span> | <span data-ttu-id="1b290-156">Appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="1b290-156">Mobile</span></span> | <span data-ttu-id="1b290-157">Cercle</span><span class="sxs-lookup"><span data-stu-id="1b290-157">Circle</span></span> | <span data-ttu-id="1b290-158">interface tactile</span><span class="sxs-lookup"><span data-stu-id="1b290-158">touch</span></span> |  
| <span data-ttu-id="1b290-159">Mobile \ (sans interaction</span><span class="sxs-lookup"><span data-stu-id="1b290-159">Mobile \(no touch\)</span></span> | <span data-ttu-id="1b290-160">Appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="1b290-160">Mobile</span></span> | <span data-ttu-id="1b290-161">Normal</span><span class="sxs-lookup"><span data-stu-id="1b290-161">Normal</span></span> | <span data-ttu-id="1b290-162"> cliquez sur </span><span class="sxs-lookup"><span data-stu-id="1b290-162">click</span></span> |  
| <span data-ttu-id="1b290-163">Bureau</span><span class="sxs-lookup"><span data-stu-id="1b290-163">Desktop</span></span> | <span data-ttu-id="1b290-164">Bureau</span><span class="sxs-lookup"><span data-stu-id="1b290-164">Desktop</span></span> | <span data-ttu-id="1b290-165">Normal</span><span class="sxs-lookup"><span data-stu-id="1b290-165">Normal</span></span> | <span data-ttu-id="1b290-166"> cliquez sur </span><span class="sxs-lookup"><span data-stu-id="1b290-166">click</span></span> |  
| <span data-ttu-id="1b290-167">Bureau \ (effleurement)</span><span class="sxs-lookup"><span data-stu-id="1b290-167">Desktop \(touch\)</span></span> | <span data-ttu-id="1b290-168">Bureau</span><span class="sxs-lookup"><span data-stu-id="1b290-168">Desktop</span></span> | <span data-ttu-id="1b290-169">Cercle</span><span class="sxs-lookup"><span data-stu-id="1b290-169">Circle</span></span> | <span data-ttu-id="1b290-170">interface tactile</span><span class="sxs-lookup"><span data-stu-id="1b290-170">touch</span></span> |  

> [!NOTE]
> <span data-ttu-id="1b290-171">Si vous ne voyez pas la liste **type d’appareil** , cliquez sur plus d' **options** , puis sélectionnez Ajouter un **type d’appareil**.</span><span class="sxs-lookup"><span data-stu-id="1b290-171">If you do not see the **Device Type** list, click **More options** and select **Add device type**.</span></span>  

### <span data-ttu-id="1b290-172">Mode d’affichage de l’appareil mobile</span><span class="sxs-lookup"><span data-stu-id="1b290-172">Mobile Device Viewport Mode</span></span>   

<span data-ttu-id="1b290-173">Pour simuler les dimensions d’un appareil mobile spécifique, sélectionnez-le dans la liste des **appareils** .</span><span class="sxs-lookup"><span data-stu-id="1b290-173">To simulate the dimensions of a specific mobile device, select the device from the **Device** list.</span></span>  

> ##### <span data-ttu-id="1b290-174">Figure 6</span><span class="sxs-lookup"><span data-stu-id="1b290-174">Figure 6</span></span>  
> <span data-ttu-id="1b290-175">La liste des appareils</span><span class="sxs-lookup"><span data-stu-id="1b290-175">The Device list</span></span>  
> ![La liste des appareils][ImageDeviceList]  

#### <span data-ttu-id="1b290-177">Faire pivoter la fenêtre d’affichage avec l’orientation paysage</span><span class="sxs-lookup"><span data-stu-id="1b290-177">Rotate the viewport to landscape orientation</span></span>   

<span data-ttu-id="1b290-178">Cliquez **sur faire** pivoter faire pivoter ![ ][ImageRotateIcon] pour faire pivoter la fenêtre d’affichage en orientation paysage.</span><span class="sxs-lookup"><span data-stu-id="1b290-178">Click **Rotate** ![Rotate][ImageRotateIcon] to rotate the viewport to landscape orientation.</span></span>  

> ##### <span data-ttu-id="1b290-179">Figure 7</span><span class="sxs-lookup"><span data-stu-id="1b290-179">Figure 7</span></span>  
> <span data-ttu-id="1b290-180">Orientation paysage</span><span class="sxs-lookup"><span data-stu-id="1b290-180">Landscape orientation</span></span>  
> ![Orientation paysage][ImageLandscape]  

> [!NOTE]
> <span data-ttu-id="1b290-182">Le bouton **faire pivoter** disparaît si la **barre d’outils** de votre appareil est étroite.</span><span class="sxs-lookup"><span data-stu-id="1b290-182">The **Rotate** button disappears if your **Device Toolbar** is narrow.</span></span>  

> ##### <span data-ttu-id="1b290-183">Figure8</span><span class="sxs-lookup"><span data-stu-id="1b290-183">Figure 8</span></span>  
> <span data-ttu-id="1b290-184">Barre d’outils de l’appareil</span><span class="sxs-lookup"><span data-stu-id="1b290-184">The Device Toolbar</span></span>  
> ![Barre d’outils de l’appareil][ImageDeviceToolbar2]  

<span data-ttu-id="1b290-186">Voir aussi [définir l’orientation](#set-orientation).</span><span class="sxs-lookup"><span data-stu-id="1b290-186">See also [Set orientation](#set-orientation).</span></span>  

#### <span data-ttu-id="1b290-187">Afficher le cadre de l’appareil</span><span class="sxs-lookup"><span data-stu-id="1b290-187">Show device frame</span></span>   

<span data-ttu-id="1b290-188">Lors de la simulation des dimensions d’un appareil mobile spécifique comme un iPhone 6, ouvrez **plus d’options** , puis sélectionnez Afficher l' **image** de l’appareil pour afficher l’image de l’appareil physique dans la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="1b290-188">When simulating the dimensions of a specific mobile device like an iPhone 6, open **More options** and then select **Show device frame** to show the physical device frame around the viewport.</span></span>  

> [!NOTE]
> <span data-ttu-id="1b290-189">Si vous ne voyez pas d’image d’appareil pour un appareil particulier, cela signifie probablement que DevTools n’a pas d’art pour cette option spécifique.</span><span class="sxs-lookup"><span data-stu-id="1b290-189">If you do not see a device frame for a particular device, it probably means that DevTools just does not have art for that specific option.</span></span>  

> ##### <span data-ttu-id="1b290-190">Figure9</span><span class="sxs-lookup"><span data-stu-id="1b290-190">Figure 9</span></span>  
> <span data-ttu-id="1b290-191">Afficher le cadre de l’appareil</span><span class="sxs-lookup"><span data-stu-id="1b290-191">Show device frame</span></span>  
> ![Afficher le cadre de l’appareil][ImageShowDeviceFrame]  

> ##### <span data-ttu-id="1b290-193">Figure10</span><span class="sxs-lookup"><span data-stu-id="1b290-193">Figure 10</span></span>  
> <span data-ttu-id="1b290-194">Le cadre de l’appareil pour l’iPhone 6</span><span class="sxs-lookup"><span data-stu-id="1b290-194">The device frame for the iPhone 6</span></span>  
> ![Le cadre de l’appareil pour l’iPhone 6][ImageIphoneFrame]  

#### <span data-ttu-id="1b290-196">Ajouter un appareil mobile personnalisé</span><span class="sxs-lookup"><span data-stu-id="1b290-196">Add a custom mobile device</span></span>   

<span data-ttu-id="1b290-197">Pour ajouter un appareil personnalisé:</span><span class="sxs-lookup"><span data-stu-id="1b290-197">To add a custom device:</span></span>  

1.  <span data-ttu-id="1b290-198">Cliquez sur la liste des **appareils** , puis sélectionnez **modifier**.</span><span class="sxs-lookup"><span data-stu-id="1b290-198">Click the **Device** list and then select **Edit**.</span></span>  

> ##### <span data-ttu-id="1b290-199">Figure11</span><span class="sxs-lookup"><span data-stu-id="1b290-199">Figure 11</span></span>  
> <span data-ttu-id="1b290-200">Sélectionner **modifier**la 
> ![ sélection modifier][ImageEdit]</span><span class="sxs-lookup"><span data-stu-id="1b290-200">Selecting **Edit**
![Selecting Edit][ImageEdit]</span></span>  

1.  <span data-ttu-id="1b290-201">Cliquez sur **Ajouter un appareil personnalisé**.</span><span class="sxs-lookup"><span data-stu-id="1b290-201">Click **Add custom device**.</span></span>  

1.  <span data-ttu-id="1b290-202">Entrez le nom, la largeur et la hauteur de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="1b290-202">Enter a name, width, and height for the device.</span></span>  <span data-ttu-id="1b290-203">Le [coefficient d’appareil][MDNWindowDevicePixelRatio], la [chaîne de l’agent utilisateur][MDNUserAgent]et les champs [type d’appareil](#set-the-device-type) sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="1b290-203">The [device pixel ratio][MDNWindowDevicePixelRatio], [user agent string][MDNUserAgent], and [device type](#set-the-device-type) fields are optional.</span></span>  <span data-ttu-id="1b290-204">Le champ type d’appareil est la liste qui est définie sur **mobile** par défaut.</span><span class="sxs-lookup"><span data-stu-id="1b290-204">The device type field is the list that is set to **Mobile** by default.</span></span>  

> ##### <span data-ttu-id="1b290-205">Figure12</span><span class="sxs-lookup"><span data-stu-id="1b290-205">Figure 12</span></span>  
> <span data-ttu-id="1b290-206">Création d’un appareil personnalisé</span><span class="sxs-lookup"><span data-stu-id="1b290-206">Creating a custom device</span></span>  
> ![Création d’un appareil personnalisé][ImageAddCustomDevice]  

### <span data-ttu-id="1b290-208">Afficher les règles</span><span class="sxs-lookup"><span data-stu-id="1b290-208">Show rulers</span></span>   

<span data-ttu-id="1b290-209">Cliquez sur **autres options** , puis sélectionnez **afficher les règles** pour afficher les règles au-dessus et à gauche de votre fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="1b290-209">Click **More options** and then select **Show rulers** to see rulers above and to the left of your viewport.</span></span>  <span data-ttu-id="1b290-210">L’unité de dimensionnement des règles est en pixels.</span><span class="sxs-lookup"><span data-stu-id="1b290-210">The sizing unit of the rulers is pixels.</span></span>  

> ##### <span data-ttu-id="1b290-211">Figure13</span><span class="sxs-lookup"><span data-stu-id="1b290-211">Figure 13</span></span>  
> <span data-ttu-id="1b290-212">Afficher les règles</span><span class="sxs-lookup"><span data-stu-id="1b290-212">Show rulers</span></span>  
> ![Afficher les règles][ImageShowRulers]  

> ##### <span data-ttu-id="1b290-214">Figure14</span><span class="sxs-lookup"><span data-stu-id="1b290-214">Figure 14</span></span>  
> <span data-ttu-id="1b290-215">Règles au-dessus et à gauche de la fenêtre d’affichage</span><span class="sxs-lookup"><span data-stu-id="1b290-215">Rulers above and to the left of the viewport</span></span>  
> ![Règles au-dessus et à gauche de la fenêtre d’affichage][ImageRulers]  

### <span data-ttu-id="1b290-217">Effectuer un zoom dans la fenêtre d’affichage</span><span class="sxs-lookup"><span data-stu-id="1b290-217">Zoom the viewport</span></span>   

<span data-ttu-id="1b290-218">Utilisez la liste **Zoom** pour effectuer un zoom avant ou arrière.</span><span class="sxs-lookup"><span data-stu-id="1b290-218">Use the **Zoom** list to zoom in or out.</span></span>  

> ##### <span data-ttu-id="1b290-219">Figure15</span><span class="sxs-lookup"><span data-stu-id="1b290-219">Figure 15</span></span>  
> <span data-ttu-id="1b290-220">Zoom</span><span class="sxs-lookup"><span data-stu-id="1b290-220">Zoom</span></span>  
> ![Zoom][ImageZoomViewport]  

## <span data-ttu-id="1b290-222">Limiter le réseau et le processeur</span><span class="sxs-lookup"><span data-stu-id="1b290-222">Throttle the network and CPU</span></span>   

<span data-ttu-id="1b290-223">Pour limiter le réseau et le processeur, sélectionnez mobile de **niveau moyen** ou **mobile** de niveau inférieur dans la liste **limitation** .</span><span class="sxs-lookup"><span data-stu-id="1b290-223">To throttle the network and CPU, select **Mid-tier mobile** or **Low-end mobile** from the **Throttle** list.</span></span>  

> ##### <span data-ttu-id="1b290-224">Figure16</span><span class="sxs-lookup"><span data-stu-id="1b290-224">Figure 16</span></span>  
> <span data-ttu-id="1b290-225">La liste des limitations</span><span class="sxs-lookup"><span data-stu-id="1b290-225">The Throttle list</span></span>  
> ![La liste des limitations][ImageThrottling]  

<span data-ttu-id="1b290-227">Le **mobile de niveau supérieur** simule un réseau 3G rapide et accélère votre processeur de manière à ce qu’il soit 4 fois plus lent qu’normal.</span><span class="sxs-lookup"><span data-stu-id="1b290-227">**Mid-tier mobile** simulates fast 3G and throttles your CPU so that it is 4 times slower than normal.</span></span>  <span data-ttu-id="1b290-228">Le **téléphone mobile de faible fin** simule un réseau 3G lent et limite votre UC de 6 temps de plus en plus lente.</span><span class="sxs-lookup"><span data-stu-id="1b290-228">**Low-end mobile** simulates slow 3G and throttles your CPU 6 times slower than normal.</span></span>  <span data-ttu-id="1b290-229">Gardez à l’esprit que la limitation dépend de la fonctionnalité normale de votre ordinateur portable ou de votre ordinateur de bureau.</span><span class="sxs-lookup"><span data-stu-id="1b290-229">Keep in mind that the throttling is relative to the normal capability of your laptop or desktop.</span></span>  

> [!NOTE]
> <span data-ttu-id="1b290-230">La liste des **limitations** sera masquée si la **barre d’outils** de votre appareil est étroite.</span><span class="sxs-lookup"><span data-stu-id="1b290-230">The **Throttle** list will be hidden if your **Device Toolbar** is narrow.</span></span>  

> ##### <span data-ttu-id="1b290-231">Figure17</span><span class="sxs-lookup"><span data-stu-id="1b290-231">Figure 17</span></span>  
> <span data-ttu-id="1b290-232">Barre d’outils de l’appareil</span><span class="sxs-lookup"><span data-stu-id="1b290-232">The Device Toolbar</span></span>  
> ![Barre d’outils de l’appareil][ImageDeviceToolbar3]  

### <span data-ttu-id="1b290-234">Limiter le processeur uniquement</span><span class="sxs-lookup"><span data-stu-id="1b290-234">Throttle the CPU only</span></span>   

<span data-ttu-id="1b290-235">Pour limiter le processeur uniquement, et non le réseau, accédez au panneau **performances** , cliquez sur paramètres de capture des **paramètres de capture** ![ ][ImageCaptureIcon] , puis sélectionnez **4x Slowdown** ou **6 ralentissement** dans la liste **processeur** .</span><span class="sxs-lookup"><span data-stu-id="1b290-235">To throttle the CPU only and not the network, go to the **Performance** panel, click **Capture Settings** ![Capture Settings][ImageCaptureIcon], and then select **4x slowdown** or **6x slowdown** from the **CPU** list.</span></span>  

> ##### <span data-ttu-id="1b290-236">Figure 18</span><span class="sxs-lookup"><span data-stu-id="1b290-236">Figure 18</span></span>  
> <span data-ttu-id="1b290-237">Liste UC</span><span class="sxs-lookup"><span data-stu-id="1b290-237">The CPU list</span></span>  
> ![Liste UC][ImageCPU]  

### <span data-ttu-id="1b290-239">Limiter le réseau uniquement</span><span class="sxs-lookup"><span data-stu-id="1b290-239">Throttle the network only</span></span>   

<span data-ttu-id="1b290-240">Pour limiter le réseau et non le processeur, accédez au panneau **réseau** et sélectionnez **Fast 3G** ou **lente 3G** dans la liste **limitation** .</span><span class="sxs-lookup"><span data-stu-id="1b290-240">To throttle the network only and not the CPU, go the **Network** panel and select **Fast 3G** or **Slow 3G** from the **Throttle** list.</span></span>  

> ##### <span data-ttu-id="1b290-241">Figure 19</span><span class="sxs-lookup"><span data-stu-id="1b290-241">Figure 19</span></span>  
> <span data-ttu-id="1b290-242">La liste des limitations</span><span class="sxs-lookup"><span data-stu-id="1b290-242">The Throttle list</span></span>  
> ![La liste des limitations][ImageNetwork]  

<span data-ttu-id="1b290-244">`Control` + `Shift` + `P` Vous pouvez appuyer sur \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le menu de commandes, taper `3G` , puis sélectionner **activer la limitation Fast 3G** ou **activer la limitation 3G lente**.</span><span class="sxs-lookup"><span data-stu-id="1b290-244">Or press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, type `3G`, and select **Enable fast 3G throttling** or **Enable slow 3G throttling**.</span></span>  

> ##### <span data-ttu-id="1b290-245">Figure 20</span><span class="sxs-lookup"><span data-stu-id="1b290-245">Figure 20</span></span>  
> <span data-ttu-id="1b290-246">Menu de commandes</span><span class="sxs-lookup"><span data-stu-id="1b290-246">The Command Menu</span></span>  
> ![Menu de commandes][ImageCommandMenu]  

<span data-ttu-id="1b290-248">Vous pouvez également définir la limitation du réseau dans le panneau **performances** .</span><span class="sxs-lookup"><span data-stu-id="1b290-248">You can also set network throttling from the **Performance** panel.</span></span>  <span data-ttu-id="1b290-249">Cliquez sur paramètres de capture **paramètres** ![ ][ImageCaptureIcon] de capture, puis sélectionnez **Fast 3G** ou **lente 3G** dans la liste **réseau** .</span><span class="sxs-lookup"><span data-stu-id="1b290-249">Click **Capture Settings** ![Capture Settings][ImageCaptureIcon] and then select **Fast 3G** or **Slow 3G** from the **Network** list.</span></span>  

> ##### <span data-ttu-id="1b290-250">Figure 21</span><span class="sxs-lookup"><span data-stu-id="1b290-250">Figure 21</span></span>  
> <span data-ttu-id="1b290-251">Configuration de la limitation du réseau à partir du panneau performances</span><span class="sxs-lookup"><span data-stu-id="1b290-251">Setting network throttling from the Performance panel</span></span>  
> ![Configuration de la limitation du réseau à partir du panneau performances][ImageNetwork2]  

## <span data-ttu-id="1b290-253">Remplacer la géolocalisation</span><span class="sxs-lookup"><span data-stu-id="1b290-253">Override geolocation</span></span>   

<span data-ttu-id="1b290-254">Pour ouvrir l’interface utilisateur de remplacement de géolocalisation cliquez sur **personnaliser et contrôler devtools** `...` , puis sélectionnez **autres**  >  **capteurs**d’outils.</span><span class="sxs-lookup"><span data-stu-id="1b290-254">To open the geolocation overriding UI click **Customize and control DevTools** `...` and then select **More tools** > **Sensors**.</span></span>  

> ##### <span data-ttu-id="1b290-255">Figure 22</span><span class="sxs-lookup"><span data-stu-id="1b290-255">Figure 22</span></span>  
> <span data-ttu-id="1b290-256">Capteurs</span><span class="sxs-lookup"><span data-stu-id="1b290-256">Sensors</span></span>  
> ![Capteurs][ImageSensors]  

<span data-ttu-id="1b290-258">Vous pouvez ou appuyer sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le menu de commandes, taper `Sensors` , puis sélectionner **afficher les capteurs**.</span><span class="sxs-lookup"><span data-stu-id="1b290-258">Or press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, type `Sensors`, and then select **Show Sensors**.</span></span>  

> ##### <span data-ttu-id="1b290-259">Figure 23</span><span class="sxs-lookup"><span data-stu-id="1b290-259">Figure 23</span></span>  
> <span data-ttu-id="1b290-260">Afficher les capteurs</span><span class="sxs-lookup"><span data-stu-id="1b290-260">Show Sensors</span></span>  
> ![Afficher les capteurs][ImageShowSensors]  

<span data-ttu-id="1b290-262">Sélectionnez l’une des présélections dans la liste **géolocalisation** ou sélectionnez **emplacement personnalisé** pour entrer vos propres coordonnées, ou sélectionnez **emplacement non disponible** pour tester le comportement de votre page lorsque la géolocalisation est dans un état d’erreur.</span><span class="sxs-lookup"><span data-stu-id="1b290-262">Select one of the presets from the **Geolocation** list, or select **Custom location** to enter your own coordinates, or select **Location unavailable** to test out how your page behaves when geolocation is in an error state.</span></span>  

> ##### <span data-ttu-id="1b290-263">Figure 24</span><span class="sxs-lookup"><span data-stu-id="1b290-263">Figure 24</span></span>  
> <span data-ttu-id="1b290-264">Géolocalisation</span><span class="sxs-lookup"><span data-stu-id="1b290-264">Geolocation</span></span>  
> ![Géolocalisation][ImageGeolocation]  

## <span data-ttu-id="1b290-266">Définir l’orientation</span><span class="sxs-lookup"><span data-stu-id="1b290-266">Set orientation</span></span>   

<span data-ttu-id="1b290-267">Pour ouvrir l’interface utilisateur d’orientation, cliquez sur **personnaliser et contrôler devtools** `...` puis sélectionnez **autres**  >  **capteurs**d’outils.</span><span class="sxs-lookup"><span data-stu-id="1b290-267">To open the orientation UI click **Customize and control DevTools** `...` and then select **More tools** > **Sensors**.</span></span>  

> ##### <span data-ttu-id="1b290-268">Figure 25</span><span class="sxs-lookup"><span data-stu-id="1b290-268">Figure 25</span></span>  
> <span data-ttu-id="1b290-269">Capteurs</span><span class="sxs-lookup"><span data-stu-id="1b290-269">Sensors</span></span>  
> ![Capteurs][ImageSensors2]  

<span data-ttu-id="1b290-271">Vous pouvez ou appuyer sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le menu de commandes, taper `Sensors` , puis sélectionner **afficher les capteurs**.</span><span class="sxs-lookup"><span data-stu-id="1b290-271">Or press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, type `Sensors`, and then select **Show Sensors**.</span></span>  

> ##### <span data-ttu-id="1b290-272">Figure 26</span><span class="sxs-lookup"><span data-stu-id="1b290-272">Figure 26</span></span>  
> <span data-ttu-id="1b290-273">Afficher les capteurs</span><span class="sxs-lookup"><span data-stu-id="1b290-273">Show Sensors</span></span>  
> ![Afficher les capteurs][ImageShowSensors2]  

<span data-ttu-id="1b290-275">Sélectionnez l’une des présélections dans la liste **orientation** ou sélectionnez **orientation personnalisée** pour définir vos propres valeurs alpha, bêta et gamma.</span><span class="sxs-lookup"><span data-stu-id="1b290-275">Select one of the presets from the **Orientation** list or select **Custom orientation** to set your own alpha, beta, and gamma values.</span></span>  

> ##### <span data-ttu-id="1b290-276">Figure 27</span><span class="sxs-lookup"><span data-stu-id="1b290-276">Figure 27</span></span>  
> <span data-ttu-id="1b290-277">Orientation</span><span class="sxs-lookup"><span data-stu-id="1b290-277">Orientation</span></span>  
> ![Orientation][ImageOrientation]  

 



<!--See [Join the DevTools community][DevToolsCommunity] for other ways to leave feedback.  -->  

<!-- image links -->  

[ImageCaptureIcon]: /microsoft-edge/devtools-guide-chromium/media/capture-settings-icon.msft.png  
[ImageCustomizeIcon]: /microsoft-edge/devtools-guide-chromium/media/customize-and-control-devtools-icon.msft.png  
[ImageDeviceToolbarIcon]: /microsoft-edge/devtools-guide-chromium/media/toggle-device-toolbar-dark-icon.msft.png  
[ImageRotateIcon]: /microsoft-edge/devtools-guide-chromium/media/rotate-dark-icon.msft.png  

[ImageDeviceToolbar]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-highlighted.msft.png "Figure 1: barre d’outils de l’appareil"  
[ImageResponsiveHandles]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png "Figure 2: poignées permettant de modifier les dimensions de la fenêtre d’affichage en mode de fenêtre d’affichage réactif"  
[ImageShowMediaQueries]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png "Figure 3: afficher les requêtes multimédias"  
[ImageBreakpoint]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png "Figure 4: cliquez sur un point d’arrêt pour modifier la largeur de la fenêtre d’affichage"  
[ImageDeviceType]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-device-type-list.msft.png "Figure 5: liste type d’appareil"  
[ImageDeviceList]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-device-list.msft.png "Figure 6: liste des appareils"  
[ImageLandscape]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-landscape.msft.png "Figure 7: orientation paysage"  
[ImageDeviceToolbar2]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-highlighted.msft.png "Figure 8: barre d’outils de l’appareil"  
[ImageShowDeviceFrame]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png "Figure 9: afficher le cadre de l’appareil"  
[ImageIphoneFrame]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png "Figure 10: cadre de l’appareil pour iPhone 6"  
[ImageEdit]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-device-list-edit.msft.png "Figure 11: sélectionner Modifier"  
[ImageAddCustomDevice]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png "Figure 12: création d’un appareil personnalisé"  
[ImageShowRulers]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png "Figure 13: afficher les règles"  
[ImageRulers]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-rulers.msft.png "Figure 14: règles au-dessus et à gauche de la fenêtre d’affichage"  
[ImageZoomViewport]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-zoom.msft.png "Figure 15: zoom"  
[ImageThrottling]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-throttle.msft.png "Figure 16: liste de limitation"  
[ImageDeviceToolbar3]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-highlighted.msft.png "Figure 17: barre d’outils de l’appareil"  
[ImageCPU]: /microsoft-edge/devtools-guide-chromium/media/device-mode-performance-cpu-throttle.msft.png "Figure 18: liste UC"  
[ImageNetwork]: /microsoft-edge/devtools-guide-chromium/media/device-mode-network-throttle.msft.png "Figure 19: liste de limitation"  
[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/device-mode-command-menu-throttle.msft.png "Figure 20: menu de commandes"  
[ImageNetwork2]: /microsoft-edge/devtools-guide-chromium/media/device-mode-performance-network-throttle.msft.png "Figure 21: configuration de la limitation du réseau à partir du panneau performances"  
[ImageSensors]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png "Figure 22: capteurs"  
[ImageShowSensors]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png "Figure 23: afficher les capteurs"  
[ImageGeolocation]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png "Figure 24: géolocalisation"  
[ImageSensors2]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png "Figure 25: capteurs"  
[ImageShowSensors2]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png "Figure 26: afficher les capteurs"  
[ImageOrientation]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png "Figure 27: orientation"  

<!-- links -->  

<!--[DevToolsCommunity]: ../index.md#community "Join the DevTools community"  -->
[DevToolsRemoteDebugging]:/Microsoft-Edge/devtools-Guide-Chromium/Remote-Debugging/index "prenez en main les appareils Android de débogage à distance"  

[MDNWindowDevicePixelRatio]: https://developer.mozilla.org/docs/Web/API/Window/devicePixelRatio "Window. devicePixelRatio | MDN"  
[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Agent utilisateur | MDN"  

[WikiApproximation]: https://en.wikipedia.org/wiki/Order_of_approximation#First-order "Ordre de rapprochement-premier-ordre-Wikipédia"  

> [!NOTE]
> <span data-ttu-id="1b290-310">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1b290-310">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="1b290-311">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="1b290-311">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="1b290-313">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1b290-313">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
