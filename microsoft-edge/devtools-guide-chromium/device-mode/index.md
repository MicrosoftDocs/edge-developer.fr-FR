---
title: Simuler des appareils mobiles avec le mode appareil dans Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 6973f28a0cb530e8928976adb1354fa7471ee343
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10985260"
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





# <span data-ttu-id="8c967-103">Simuler des appareils mobiles avec le mode appareil dans Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="8c967-103">Simulate mobile devices with Device Mode in Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="8c967-104">Utilisez le mode appareil pour obtenir un aperçu de l’apparence de votre page et de son exécution sur un appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="8c967-104">Use Device Mode to approximate how your page looks and performs on a mobile device.</span></span>  

<span data-ttu-id="8c967-105">Le mode appareil est le nom de la collection libre de fonctionnalités dans Microsoft Edge DevTools qui vous permettent de simuler des appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="8c967-105">Device Mode is the name for the loose collection of features in Microsoft Edge DevTools that help you simulate mobile devices.</span></span>  <span data-ttu-id="8c967-106">Ces fonctionnalités incluent:</span><span class="sxs-lookup"><span data-stu-id="8c967-106">These features include:</span></span>  

*   [<span data-ttu-id="8c967-107">Simulation d’une fenêtre d’affichage mobile</span><span class="sxs-lookup"><span data-stu-id="8c967-107">Simulating a mobile viewport</span></span>](#simulate-a-mobile-viewport)  
*   [<span data-ttu-id="8c967-108">Limitation du réseau</span><span class="sxs-lookup"><span data-stu-id="8c967-108">Throttling the network</span></span>](#throttle-the-network-only)  
*   [<span data-ttu-id="8c967-109">Limitation de l’UC</span><span class="sxs-lookup"><span data-stu-id="8c967-109">Throttling the CPU</span></span>](#throttle-the-cpu-only)  
*   [<span data-ttu-id="8c967-110">Simulation de géolocalisation</span><span class="sxs-lookup"><span data-stu-id="8c967-110">Simulating geolocation</span></span>](#override-geolocation)  
*   [<span data-ttu-id="8c967-111">Définir l’orientation</span><span class="sxs-lookup"><span data-stu-id="8c967-111">Setting orientation</span></span>](#set-orientation)  

## <span data-ttu-id="8c967-112">Limitations</span><span class="sxs-lookup"><span data-stu-id="8c967-112">Limitations</span></span>   

<span data-ttu-id="8c967-113">Imaginez le mode appareil comme une [approximation prioritaire][WikiApproximation] de l’apparence de votre page sur un appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="8c967-113">Think of Device Mode as a [first-order approximation][WikiApproximation] of how your page looks and feels on a mobile device.</span></span>  <span data-ttu-id="8c967-114">Le mode appareil n’exécute pas réellement votre code sur un appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="8c967-114">With Device Mode you do not actually run your code on a mobile device.</span></span>  <span data-ttu-id="8c967-115">Vous simulez l’expérience utilisateur mobile sur votre ordinateur portable ou votre ordinateur de bureau.</span><span class="sxs-lookup"><span data-stu-id="8c967-115">You simulate the mobile user experience from your laptop or desktop.</span></span>  

<span data-ttu-id="8c967-116">Certains aspects des appareils mobiles qu’DevTools ne seront jamais en mesure de simuler.</span><span class="sxs-lookup"><span data-stu-id="8c967-116">There are some aspects of mobile devices that DevTools will never be able to simulate.</span></span>  <span data-ttu-id="8c967-117">Par exemple, l’architecture des UC mobiles est très différente de l’architecture de l’ordinateur portable ou de l’UC de bureau.</span><span class="sxs-lookup"><span data-stu-id="8c967-117">For example, the architecture of mobile CPUs is very different than the architecture of laptop or desktop CPUs.</span></span>  <span data-ttu-id="8c967-118">En cas de doute, il est préférable d’exécuter votre page sur un appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="8c967-118">When in doubt, your best bet is to actually run your page on a mobile device.</span></span>  <span data-ttu-id="8c967-119">Pour afficher, modifier, déboguer et profiler le code d’une page à partir de votre ordinateur portable ou de votre ordinateur de bureau, vous pouvez utiliser [Remote Debugger] [DevToolsRemoteDebugging].</span><span class="sxs-lookup"><span data-stu-id="8c967-119">Use [Remote Debugging][DevToolsRemoteDebugging] to view, change, debug, and profile the code of a page from your laptop or desktop while it actually runs on a mobile device.</span></span>  

## <span data-ttu-id="8c967-120">Simuler une fenêtre d’affichage mobile</span><span class="sxs-lookup"><span data-stu-id="8c967-120">Simulate a mobile viewport</span></span>   

<span data-ttu-id="8c967-121">Cliquez sur le **bouton bascule de la barre d’outils** de l’appareil \ ( ![ activez la barre d’outils de ][ImageDeviceToolbarIcon] l’appareil \) pour ouvrir l’interface utilisateur qui vous permet de simuler une fenêtre d’affichage mobile.</span><span class="sxs-lookup"><span data-stu-id="8c967-121">Click **Toggle Device Toolbar** \(![Toggle Device Toolbar][ImageDeviceToolbarIcon]\) to open the UI that enables you to simulate a mobile viewport.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Barre d’outils de l’appareil" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   <span data-ttu-id="8c967-123">Barre d’outils de l’appareil</span><span class="sxs-lookup"><span data-stu-id="8c967-123">The Device Toolbar</span></span>  
:::image-end:::  

<span data-ttu-id="8c967-124">Par défaut, la barre d’outils de l’appareil s’ouvre en mode de fenêtre d’affichage réactif.</span><span class="sxs-lookup"><span data-stu-id="8c967-124">By default the Device Toolbar opens in Responsive Viewport Mode.</span></span>  

### <span data-ttu-id="8c967-125">Mode de fenêtre d’affichage réactif</span><span class="sxs-lookup"><span data-stu-id="8c967-125">Responsive Viewport Mode</span></span>   

<span data-ttu-id="8c967-126">Faites glisser les poignées pour redimensionner la fenêtre d’affichage en fonction des dimensions dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="8c967-126">Drag the handles to resize the viewport to whatever dimensions you need.</span></span>  <span data-ttu-id="8c967-127">Vous avez d’autres valeurs dans les zones largeur et hauteur.</span><span class="sxs-lookup"><span data-stu-id="8c967-127">Or, enter specific values in the width and height boxes.</span></span>  <span data-ttu-id="8c967-128">Dans l’illustration suivante, la largeur est définie sur `626` et la hauteur est définie sur `516` .</span><span class="sxs-lookup"><span data-stu-id="8c967-128">In the following figure, the width is set to `626` and the height is set to `516`.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png" alt-text="Poignées permettant de modifier les dimensions de la fenêtre d’affichage en mode de fenêtre d’affichage réactif" lightbox="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png":::
   <span data-ttu-id="8c967-130">Poignées permettant de modifier les dimensions de la fenêtre d’affichage en mode de fenêtre d’affichage réactif</span><span class="sxs-lookup"><span data-stu-id="8c967-130">The handles for changing the dimensions of the viewport when in Responsive Viewport Mode</span></span>  
:::image-end:::  

#### <span data-ttu-id="8c967-131">Afficher les requêtes multimédias</span><span class="sxs-lookup"><span data-stu-id="8c967-131">Show media queries</span></span>   

<span data-ttu-id="8c967-132">Pour afficher les points d’arrêt de requête multimédias au-dessus de votre fenêtre d’affichage, cliquez sur **plus d’options** , puis sélectionnez **afficher les requêtes multimédias**.</span><span class="sxs-lookup"><span data-stu-id="8c967-132">To show media query breakpoints above your viewport, click **More options** and then select **Show media queries**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png" alt-text="Afficher les requêtes multimédias" lightbox="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png":::
   **<span data-ttu-id="8c967-134">Afficher les requêtes multimédias</span><span class="sxs-lookup"><span data-stu-id="8c967-134">Show media queries</span></span>**  
:::image-end:::  

<span data-ttu-id="8c967-135">Cliquez sur un point d’arrêt pour modifier la largeur de la fenêtre d’affichage de telle sorte que le point d’arrêt soit déclenché.</span><span class="sxs-lookup"><span data-stu-id="8c967-135">Click a breakpoint to change the width of the viewport so that the breakpoint gets triggered.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png" alt-text="Cliquez sur un point d’arrêt pour modifier la largeur de la fenêtre d’affichage" lightbox="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png":::
   <span data-ttu-id="8c967-137">Cliquez sur un point d’arrêt pour modifier la largeur de la fenêtre d’affichage</span><span class="sxs-lookup"><span data-stu-id="8c967-137">Click a breakpoint to change the width of the viewport</span></span>  
:::image-end:::  

#### <span data-ttu-id="8c967-138">Définir le type d’appareil</span><span class="sxs-lookup"><span data-stu-id="8c967-138">Set the device type</span></span>   

<span data-ttu-id="8c967-139">Utilisez la liste **type d’appareil** pour simuler un appareil mobile ou un appareil de bureau.</span><span class="sxs-lookup"><span data-stu-id="8c967-139">Use the **Device Type** list to simulate a mobile device or desktop device.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png" alt-text="Liste type d’appareil" lightbox="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png":::
   <span data-ttu-id="8c967-141">Liste **type d’appareil**</span><span class="sxs-lookup"><span data-stu-id="8c967-141">The **Device Type** list</span></span>  
:::image-end:::  

<span data-ttu-id="8c967-142">Le tableau ci-dessous décrit les différences entre les options.</span><span class="sxs-lookup"><span data-stu-id="8c967-142">The table below describes the differences between the options.</span></span>  <span data-ttu-id="8c967-143">La **méthode de rendu** fait référence à la façon dont Microsoft Edge effectue le rendu de la page en tant que fenêtre d’affichage mobile ou de bureau.</span><span class="sxs-lookup"><span data-stu-id="8c967-143">**Rendering method** refers to whether Microsoft Edge renders the page as a mobile or desktop viewport.</span></span>  <span data-ttu-id="8c967-144">**Icône du curseur** désigne le type de curseur qui s’affiche lorsque vous survolez la page.</span><span class="sxs-lookup"><span data-stu-id="8c967-144">**Cursor icon** refers to what type of cursor you see when you hover over the page.</span></span>  <span data-ttu-id="8c967-145">Les **événements déclenchés** font référence au déclenchement de la page `touch` ou aux `click` événements lorsque vous interagissez avec la page.</span><span class="sxs-lookup"><span data-stu-id="8c967-145">**Events fired** refers to whether the page fires `touch` or `click` events when you interact with the page.</span></span>  

| <span data-ttu-id="8c967-146">Option</span><span class="sxs-lookup"><span data-stu-id="8c967-146">Option</span></span> | <span data-ttu-id="8c967-147">Méthode de rendu</span><span class="sxs-lookup"><span data-stu-id="8c967-147">Rendering method</span></span> | <span data-ttu-id="8c967-148">Icône du curseur</span><span class="sxs-lookup"><span data-stu-id="8c967-148">Cursor icon</span></span> | <span data-ttu-id="8c967-149">Événements déclenchés</span><span class="sxs-lookup"><span data-stu-id="8c967-149">Events fired</span></span> |  
|:--- |:--- |:--- |:--- |  
| <span data-ttu-id="8c967-150">Appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="8c967-150">Mobile</span></span> | <span data-ttu-id="8c967-151">Appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="8c967-151">Mobile</span></span> | <span data-ttu-id="8c967-152">Cercle</span><span class="sxs-lookup"><span data-stu-id="8c967-152">Circle</span></span> | <span data-ttu-id="8c967-153">interface tactile</span><span class="sxs-lookup"><span data-stu-id="8c967-153">touch</span></span> |  
| <span data-ttu-id="8c967-154">Mobile \ (sans interaction</span><span class="sxs-lookup"><span data-stu-id="8c967-154">Mobile \(no touch\)</span></span> | <span data-ttu-id="8c967-155">Appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="8c967-155">Mobile</span></span> | <span data-ttu-id="8c967-156">Normal</span><span class="sxs-lookup"><span data-stu-id="8c967-156">Normal</span></span> | <span data-ttu-id="8c967-157"> cliquez sur </span><span class="sxs-lookup"><span data-stu-id="8c967-157">click</span></span> |  
| <span data-ttu-id="8c967-158">Bureau</span><span class="sxs-lookup"><span data-stu-id="8c967-158">Desktop</span></span> | <span data-ttu-id="8c967-159">Bureau</span><span class="sxs-lookup"><span data-stu-id="8c967-159">Desktop</span></span> | <span data-ttu-id="8c967-160">Normal</span><span class="sxs-lookup"><span data-stu-id="8c967-160">Normal</span></span> | <span data-ttu-id="8c967-161"> cliquez sur </span><span class="sxs-lookup"><span data-stu-id="8c967-161">click</span></span> |  
| <span data-ttu-id="8c967-162">Bureau \ (effleurement)</span><span class="sxs-lookup"><span data-stu-id="8c967-162">Desktop \(touch\)</span></span> | <span data-ttu-id="8c967-163">Bureau</span><span class="sxs-lookup"><span data-stu-id="8c967-163">Desktop</span></span> | <span data-ttu-id="8c967-164">Cercle</span><span class="sxs-lookup"><span data-stu-id="8c967-164">Circle</span></span> | <span data-ttu-id="8c967-165">interface tactile</span><span class="sxs-lookup"><span data-stu-id="8c967-165">touch</span></span> |  

> [!NOTE]
> <span data-ttu-id="8c967-166">Si vous ne voyez pas la liste **type d’appareil** , cliquez sur plus d' **options** , puis sélectionnez Ajouter un **type d’appareil**.</span><span class="sxs-lookup"><span data-stu-id="8c967-166">If you do not see the **Device Type** list, click **More options** and select **Add device type**.</span></span>  

### <span data-ttu-id="8c967-167">Mode d’affichage de l’appareil mobile</span><span class="sxs-lookup"><span data-stu-id="8c967-167">Mobile Device Viewport Mode</span></span>   

<span data-ttu-id="8c967-168">Pour simuler les dimensions d’un appareil mobile spécifique, sélectionnez-le dans la liste des **appareils** .</span><span class="sxs-lookup"><span data-stu-id="8c967-168">To simulate the dimensions of a specific mobile device, select the device from the **Device** list.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list.msft.png" alt-text="La liste des appareils" lightbox="../media/device-mode-toggle-device-toolbar-device-list.msft.png":::
   <span data-ttu-id="8c967-170">La liste des **appareils**</span><span class="sxs-lookup"><span data-stu-id="8c967-170">The **Device** list</span></span>  
:::image-end:::  

#### <span data-ttu-id="8c967-171">Faire pivoter la fenêtre d’affichage avec l’orientation paysage</span><span class="sxs-lookup"><span data-stu-id="8c967-171">Rotate the viewport to landscape orientation</span></span>   

<span data-ttu-id="8c967-172">Cliquez sur **faire pivoter** \ ( ![ faire pivoter ][ImageRotateIcon] ) pour faire pivoter la fenêtre d’affichage en orientation paysage.</span><span class="sxs-lookup"><span data-stu-id="8c967-172">Click **Rotate** \(![Rotate][ImageRotateIcon]\) to rotate the viewport to landscape orientation.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-landscape.msft.png" alt-text="Orientation paysage" lightbox="../media/device-mode-toggle-device-toolbar-landscape.msft.png":::
   <span data-ttu-id="8c967-174">Orientation paysage</span><span class="sxs-lookup"><span data-stu-id="8c967-174">Landscape orientation</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="8c967-175">Le bouton **faire pivoter** disparaît si la **barre d’outils** de votre appareil est étroite.</span><span class="sxs-lookup"><span data-stu-id="8c967-175">The **Rotate** button disappears if your **Device Toolbar** is narrow.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Barre d’outils de l’appareil" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   <span data-ttu-id="8c967-177">**Barre d’outils** de l’appareil</span><span class="sxs-lookup"><span data-stu-id="8c967-177">The **Device Toolbar**</span></span>  
:::image-end:::  

<span data-ttu-id="8c967-178">Voir aussi [définir l’orientation](#set-orientation).</span><span class="sxs-lookup"><span data-stu-id="8c967-178">See also [Set orientation](#set-orientation).</span></span>  

#### <span data-ttu-id="8c967-179">Afficher le cadre de l’appareil</span><span class="sxs-lookup"><span data-stu-id="8c967-179">Show device frame</span></span>   

<span data-ttu-id="8c967-180">Lors de la simulation des dimensions d’un appareil mobile spécifique comme un iPhone 6, ouvrez **plus d’options** , puis sélectionnez Afficher l' **image** de l’appareil pour afficher l’image de l’appareil physique dans la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="8c967-180">When simulating the dimensions of a specific mobile device like an iPhone 6, open **More options** and then select **Show device frame** to show the physical device frame around the viewport.</span></span>  

> [!NOTE]
> <span data-ttu-id="8c967-181">Si vous ne voyez pas d’image d’appareil pour un appareil particulier, cela signifie probablement que DevTools n’a pas d’art pour cette option spécifique.</span><span class="sxs-lookup"><span data-stu-id="8c967-181">If you do not see a device frame for a particular device, it probably means that DevTools just does not have art for that specific option.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png" alt-text="Afficher le cadre de l’appareil" lightbox="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png":::
         <span data-ttu-id="8c967-183">Afficher le cadre de l’appareil</span><span class="sxs-lookup"><span data-stu-id="8c967-183">Show device frame</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png" alt-text="Le cadre de l’appareil pour l’iPhone 6" lightbox="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png":::
         <span data-ttu-id="8c967-185">Le cadre de l’appareil pour l’iPhone 6</span><span class="sxs-lookup"><span data-stu-id="8c967-185">The device frame for the iPhone 6</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

#### <span data-ttu-id="8c967-186">Ajouter un appareil mobile personnalisé</span><span class="sxs-lookup"><span data-stu-id="8c967-186">Add a custom mobile device</span></span>   

<span data-ttu-id="8c967-187">Pour ajouter un appareil personnalisé:</span><span class="sxs-lookup"><span data-stu-id="8c967-187">To add a custom device:</span></span>  

1.  <span data-ttu-id="8c967-188">Cliquez sur la liste des **appareils** , puis sélectionnez **modifier**.</span><span class="sxs-lookup"><span data-stu-id="8c967-188">Click the **Device** list and then select **Edit**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png" alt-text="Sélectionnez Modifier." lightbox="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png":::
       <span data-ttu-id="8c967-190">Sélectionnez **modifier** .</span><span class="sxs-lookup"><span data-stu-id="8c967-190">Select **Edit**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="8c967-191">Cliquez sur **Ajouter un appareil personnalisé**.</span><span class="sxs-lookup"><span data-stu-id="8c967-191">Click **Add custom device**.</span></span>  
1.  <span data-ttu-id="8c967-192">Entrez le nom, la largeur et la hauteur de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8c967-192">Enter a name, width, and height for the device.</span></span>  <span data-ttu-id="8c967-193">Le [coefficient d’appareil][MDNWindowDevicePixelRatio], la [chaîne de l’agent utilisateur][MDNUserAgent]et les champs [type d’appareil](#set-the-device-type) sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="8c967-193">The [device pixel ratio][MDNWindowDevicePixelRatio], [user agent string][MDNUserAgent], and [device type](#set-the-device-type) fields are optional.</span></span>  <span data-ttu-id="8c967-194">Le champ type d’appareil est la liste qui est définie sur **mobile** par défaut.</span><span class="sxs-lookup"><span data-stu-id="8c967-194">The device type field is the list that is set to **Mobile** by default.</span></span>  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png" alt-text="Créer un appareil personnalisé" lightbox="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png":::
       <span data-ttu-id="8c967-196">Appareil personnalisé de création</span><span class="sxs-lookup"><span data-stu-id="8c967-196">Createa custom device</span></span>  
    :::image-end:::  

### <span data-ttu-id="8c967-197">Afficher les règles</span><span class="sxs-lookup"><span data-stu-id="8c967-197">Show rulers</span></span>   

<span data-ttu-id="8c967-198">Cliquez sur **autres options** , puis sélectionnez **afficher les règles** pour afficher les règles au-dessus et à gauche de votre fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="8c967-198">Click **More options** and then select **Show rulers** to see rulers above and to the left of your viewport.</span></span>  <span data-ttu-id="8c967-199">L’unité de dimensionnement des règles est en pixels.</span><span class="sxs-lookup"><span data-stu-id="8c967-199">The sizing unit of the rulers is pixels.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png" alt-text="Afficher les règles" lightbox="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png":::
         **<span data-ttu-id="8c967-201">Afficher les règles</span><span class="sxs-lookup"><span data-stu-id="8c967-201">Show rulers</span></span>**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-rulers.msft.png" alt-text="Règles au-dessus et à gauche de la fenêtre d’affichage" lightbox="../media/device-mode-toggle-device-toolbar-rulers.msft.png":::
         <span data-ttu-id="8c967-203">Règles au-dessus et à gauche de la fenêtre d’affichage</span><span class="sxs-lookup"><span data-stu-id="8c967-203">Rulers above and to the left of the viewport</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

### <span data-ttu-id="8c967-204">Effectuer un zoom dans la fenêtre d’affichage</span><span class="sxs-lookup"><span data-stu-id="8c967-204">Zoom the viewport</span></span>   

<span data-ttu-id="8c967-205">Utilisez la liste **Zoom** pour effectuer un zoom avant ou arrière.</span><span class="sxs-lookup"><span data-stu-id="8c967-205">Use the **Zoom** list to zoom in or out.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-zoom.msft.png" alt-text="Zoom" lightbox="../media/device-mode-toggle-device-toolbar-zoom.msft.png":::
   **<span data-ttu-id="8c967-207">Zoom</span><span class="sxs-lookup"><span data-stu-id="8c967-207">Zoom</span></span>**  
:::image-end:::  

## <span data-ttu-id="8c967-208">Limiter le réseau et le processeur</span><span class="sxs-lookup"><span data-stu-id="8c967-208">Throttle the network and CPU</span></span>   

<span data-ttu-id="8c967-209">Pour limiter le réseau et le processeur, sélectionnez mobile de **niveau moyen** ou **mobile** de niveau inférieur dans la liste **limitation** .</span><span class="sxs-lookup"><span data-stu-id="8c967-209">To throttle the network and CPU, select **Mid-tier mobile** or **Low-end mobile** from the **Throttle** list.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-throttle.msft.png" alt-text="La liste des limitations" lightbox="../media/device-mode-toggle-device-toolbar-throttle.msft.png":::
   <span data-ttu-id="8c967-211">La liste des **limitations**</span><span class="sxs-lookup"><span data-stu-id="8c967-211">The **Throttle** list</span></span>  
:::image-end:::  

<span data-ttu-id="8c967-212">Le **mobile de niveau supérieur** simule un réseau 3G rapide et accélère votre processeur de manière à ce qu’il soit 4 fois plus lent qu’normal.</span><span class="sxs-lookup"><span data-stu-id="8c967-212">**Mid-tier mobile** simulates fast 3G and throttles your CPU so that it is 4 times slower than normal.</span></span>  <span data-ttu-id="8c967-213">Le **téléphone mobile de faible fin** simule un réseau 3G lent et limite votre UC de 6 temps de plus en plus lente.</span><span class="sxs-lookup"><span data-stu-id="8c967-213">**Low-end mobile** simulates slow 3G and throttles your CPU 6 times slower than normal.</span></span>  <span data-ttu-id="8c967-214">Gardez à l’esprit que la limitation dépend de la fonctionnalité normale de votre ordinateur portable ou de votre ordinateur de bureau.</span><span class="sxs-lookup"><span data-stu-id="8c967-214">Keep in mind that the throttling is relative to the normal capability of your laptop or desktop.</span></span>  

> [!NOTE]
> <span data-ttu-id="8c967-215">La liste des **limitations** est cachée si la **barre d’outils** de votre appareil est étroite.</span><span class="sxs-lookup"><span data-stu-id="8c967-215">The **Throttle** list is hidden if your **Device Toolbar** is narrow.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Barre d’outils de l’appareil" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   <span data-ttu-id="8c967-217">**Barre d’outils** de l’appareil</span><span class="sxs-lookup"><span data-stu-id="8c967-217">The **Device Toolbar**</span></span>  
:::image-end:::  

### <span data-ttu-id="8c967-218">Limiter le processeur uniquement</span><span class="sxs-lookup"><span data-stu-id="8c967-218">Throttle the CPU only</span></span>   

<span data-ttu-id="8c967-219">Pour limiter le processeur uniquement, et non le réseau, accédez au panneau **performance** , cliquez sur **paramètres de capture** \ ( ![ paramètres de capture ][ImageCaptureIcon] \), puis sélectionnez **4x Slowdown** ou en 6 points de **ralentissement** dans la liste **processeur** .</span><span class="sxs-lookup"><span data-stu-id="8c967-219">To throttle the CPU only and not the network, go to the **Performance** panel, click **Capture Settings** \(![Capture Settings][ImageCaptureIcon]\), and then select **4x slowdown** or **6x slowdown** from the **CPU** list.</span></span>  

:::image type="complex" source="../media/device-mode-performance-cpu-throttle.msft.png" alt-text="Liste UC" lightbox="../media/device-mode-performance-cpu-throttle.msft.png":::
   <span data-ttu-id="8c967-221">Liste **UC**</span><span class="sxs-lookup"><span data-stu-id="8c967-221">The **CPU** list</span></span>  
:::image-end:::  

### <span data-ttu-id="8c967-222">Limiter le réseau uniquement</span><span class="sxs-lookup"><span data-stu-id="8c967-222">Throttle the network only</span></span>   

<span data-ttu-id="8c967-223">Pour limiter le réseau et non le processeur, accédez au panneau **réseau** et sélectionnez **Fast 3G** ou **lente 3G** dans la liste **limitation** .</span><span class="sxs-lookup"><span data-stu-id="8c967-223">To throttle the network only and not the CPU, go the **Network** panel and select **Fast 3G** or **Slow 3G** from the **Throttle** list.</span></span>  

:::image type="complex" source="../media/device-mode-network-throttle.msft.png" alt-text="La liste des limitations" lightbox="../media/device-mode-network-throttle.msft.png":::
   <span data-ttu-id="8c967-225">La liste des **limitations**</span><span class="sxs-lookup"><span data-stu-id="8c967-225">The **Throttle** list</span></span>  
:::image-end:::  

<span data-ttu-id="8c967-226">`Control` + `Shift` + `P` Vous pouvez appuyer sur \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le **menu de commandes**, taper `3G` , puis sélectionner **activer la limitation Fast 3G** ou **activer la limitation 3G lente**.</span><span class="sxs-lookup"><span data-stu-id="8c967-226">Or press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**, type `3G`, and select **Enable fast 3G throttling** or **Enable slow 3G throttling**.</span></span>  

:::image type="complex" source="../media/device-mode-command-menu-throttle.msft.png" alt-text="Menu de commandes" lightbox="../media/device-mode-command-menu-throttle.msft.png":::
   <span data-ttu-id="8c967-228">**Menu de commandes**</span><span class="sxs-lookup"><span data-stu-id="8c967-228">The **Command Menu**</span></span>  
:::image-end:::  

<span data-ttu-id="8c967-229">Vous pouvez également définir la limitation du réseau dans le panneau **performances** .</span><span class="sxs-lookup"><span data-stu-id="8c967-229">You can also set network throttling from the **Performance** panel.</span></span>  <span data-ttu-id="8c967-230">Cliquez sur **paramètres de capture** \ (paramètres de ![ capture ][ImageCaptureIcon] \), puis sélectionnez **Fast 3G** ou **lente 3G** dans la liste **réseau** .</span><span class="sxs-lookup"><span data-stu-id="8c967-230">Click **Capture Settings** \(![Capture Settings][ImageCaptureIcon]\) and then select **Fast 3G** or **Slow 3G** from the **Network** list.</span></span>  

:::image type="complex" source="../media/device-mode-performance-network-throttle.msft.png" alt-text="Définir la limitation du réseau à partir du panneau performances" lightbox="../media/device-mode-performance-network-throttle.msft.png":::
   <span data-ttu-id="8c967-232">Définir la limitation du réseau à partir du panneau **performances**</span><span class="sxs-lookup"><span data-stu-id="8c967-232">Set network throttling from the **Performance** panel</span></span>  
:::image-end:::  

## <span data-ttu-id="8c967-233">Remplacer la géolocalisation</span><span class="sxs-lookup"><span data-stu-id="8c967-233">Override geolocation</span></span>   

<span data-ttu-id="8c967-234">Pour ouvrir l’interface utilisateur de remplacement de géolocalisation cliquez sur **personnaliser et contrôler devtools** \ ( `...` \), puis sélectionnez **autres**  >  **capteurs**d’outils.</span><span class="sxs-lookup"><span data-stu-id="8c967-234">To open the geolocation overriding UI click **Customize and control DevTools** \(`...`\) and then select **More tools** > **Sensors**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Capteurs" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
   **<span data-ttu-id="8c967-236">Capteurs</span><span class="sxs-lookup"><span data-stu-id="8c967-236">Sensors</span></span>**  
:::image-end:::  

<span data-ttu-id="8c967-237">Vous pouvez ou appuyer sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le menu de commandes, taper `Sensors` , puis sélectionner **afficher les capteurs**.</span><span class="sxs-lookup"><span data-stu-id="8c967-237">Or press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, type `Sensors`, and then select **Show Sensors**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Afficher les capteurs" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
   **<span data-ttu-id="8c967-239">Afficher les capteurs</span><span class="sxs-lookup"><span data-stu-id="8c967-239">Show Sensors</span></span>**  
:::image-end:::  

<span data-ttu-id="8c967-240">Sélectionnez l’une des présélections dans la liste **géolocalisation** ou sélectionnez **emplacement personnalisé** pour entrer vos propres coordonnées, ou sélectionnez **emplacement non disponible** pour tester le comportement de votre page lorsque la géolocalisation est dans un état d’erreur.</span><span class="sxs-lookup"><span data-stu-id="8c967-240">Select one of the presets from the **Geolocation** list, or select **Custom location** to enter your own coordinates, or select **Location unavailable** to test out how your page behaves when geolocation is in an error state.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png" alt-text="Géolocalisation" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png":::
   **<span data-ttu-id="8c967-242">Géolocalisation</span><span class="sxs-lookup"><span data-stu-id="8c967-242">Geolocation</span></span>**  
:::image-end:::  

## <span data-ttu-id="8c967-243">Définir l’orientation</span><span class="sxs-lookup"><span data-stu-id="8c967-243">Set orientation</span></span>   

:::row:::
   :::column span="":::
      <span data-ttu-id="8c967-244">Pour ouvrir l’interface utilisateur d’orientation, cliquez sur **personnaliser et contrôler devtools** `...` puis sélectionnez **autres**  >  **capteurs**d’outils.</span><span class="sxs-lookup"><span data-stu-id="8c967-244">To open the orientation UI click **Customize and control DevTools** `...` and then select **More tools** > **Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Capteurs" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         **<span data-ttu-id="8c967-246">Capteurs</span><span class="sxs-lookup"><span data-stu-id="8c967-246">Sensors</span></span>**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="8c967-247">Vous pouvez ou appuyer sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le menu de commandes, taper `Sensors` , puis sélectionner **afficher les capteurs**.</span><span class="sxs-lookup"><span data-stu-id="8c967-247">Or press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, type `Sensors`, and then select **Show Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Afficher les capteurs" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         **<span data-ttu-id="8c967-249">Afficher les capteurs</span><span class="sxs-lookup"><span data-stu-id="8c967-249">Show Sensors</span></span>**  
      :::image-end:::  
   :::column-end:::
:::row-end:::

<span data-ttu-id="8c967-250">Sélectionnez l’une des présélections dans la liste **orientation** ou sélectionnez **orientation personnalisée** pour définir vos propres valeurs alpha, bêta et gamma.</span><span class="sxs-lookup"><span data-stu-id="8c967-250">Select one of the presets from the **Orientation** list or select **Custom orientation** to set your own alpha, beta, and gamma values.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png" alt-text="Orientation" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png":::
   **<span data-ttu-id="8c967-252">Orientation</span><span class="sxs-lookup"><span data-stu-id="8c967-252">Orientation</span></span>**  
:::image-end:::  

<!--  
 


-->  

<!--See [Join the DevTools community][DevToolsCommunity] for other ways to leave feedback.  -->  

<!-- image links -->  

[ImageCaptureIcon]: ../media/capture-settings-icon.msft.png  
[ImageDeviceToolbarIcon]: ../media/toggle-device-toolbar-dark-icon.msft.png  
[ImageRotateIcon]: ../media/rotate-dark-icon.msft.png  

<!-- links -->  

<!--[DevToolsCommunity]: ../index.md#community "Join the DevTools community | Microsoft Docs"  -->
[DevToolsRemoteDebugging]: .. /Remote-Debugging/index.MD "mise en route des appareils Android de débogage à distance | Documents Microsoft  

[MDNWindowDevicePixelRatio]: https://developer.mozilla.org/docs/Web/API/Window/devicePixelRatio "Window. devicePixelRatio | MDN"  
[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Agent utilisateur | MDN"  

[WikiApproximation]: https://en.wikipedia.org/wiki/Order_of_approximation#First-order "Ordre de rapprochement-premier-ordre-Wikipédia"  

> [!NOTE]
> <span data-ttu-id="8c967-257">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8c967-257">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="8c967-258">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="8c967-258">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="8c967-260">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8c967-260">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
