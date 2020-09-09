---
description: Utilisez des périphériques virtuels dans Microsoft Edge pour créer des sites Web de premier prénom.
title: Émuler des appareils mobiles dans Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/04/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, émulation, appareil, simulation, mobile
ms.openlocfilehash: c70b81eabb145461eac7d1b9a8f438d6a18fbc89
ms.sourcegitcommit: cc96ada9679b23feb841e46f19d8077251c4a4df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "10997061"
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

# <span data-ttu-id="71256-104">Émuler des appareils mobiles dans Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="71256-104">Emulate mobile devices in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="71256-105">Utilisez l' **émulation d’appareil** pour rapprocher l’apparence de votre page et la réponse sur un appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="71256-105">Use **Device emulation** to approximate how your page looks and responds on a mobile device.</span></span>  <span data-ttu-id="71256-106">Le Microsoft Edge DevTools fournit un ensemble de fonctionnalités pour vous aider à émuler les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="71256-106">The Microsoft Edge DevTools provide a collection of features to help you emulate mobile devices.</span></span>  <span data-ttu-id="71256-107">La collection inclut les fonctionnalités suivantes.</span><span class="sxs-lookup"><span data-stu-id="71256-107">The collection includes the following features.</span></span>  

*   [<span data-ttu-id="71256-108">Simuler une fenêtre d’affichage mobile</span><span class="sxs-lookup"><span data-stu-id="71256-108">Simulate a mobile viewport</span></span>](#simulate-a-mobile-viewport)  
*   [<span data-ttu-id="71256-109">Limiter le réseau</span><span class="sxs-lookup"><span data-stu-id="71256-109">Throttle the network</span></span>](#throttle-the-network-only)  
*   [<span data-ttu-id="71256-110">Limiter le processeur</span><span class="sxs-lookup"><span data-stu-id="71256-110">Throttle the CPU</span></span>](#throttle-the-cpu-only)  
*   [<span data-ttu-id="71256-111">Simuler géolocalisation</span><span class="sxs-lookup"><span data-stu-id="71256-111">Simulate geolocation</span></span>](#override-geolocation)  
*   [<span data-ttu-id="71256-112">Définir l’orientation</span><span class="sxs-lookup"><span data-stu-id="71256-112">Set orientation</span></span>](#set-orientation)  
*   [<span data-ttu-id="71256-113">Définir la chaîne de l’agent utilisateur</span><span class="sxs-lookup"><span data-stu-id="71256-113">Set the user agent string</span></span>](#set-user-agent-string)  

## <span data-ttu-id="71256-114">Limitations</span><span class="sxs-lookup"><span data-stu-id="71256-114">Limitations</span></span>  

<span data-ttu-id="71256-115">L' **émulation d’appareil** est une [approximation première commande][WikiApproximation] de l’apparence de votre page sur un appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="71256-115">**Device emulation** is a [first-order approximation][WikiApproximation] of the look and feel of your page on a mobile device.</span></span>  <span data-ttu-id="71256-116">L' **émulation d’appareil** n’exécute pas réellement votre code sur un appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="71256-116">**Device emulation** does not actually run your code on a mobile device.</span></span>  <span data-ttu-id="71256-117">À la place, vous simulez l’expérience utilisateur mobile sur votre ordinateur portable ou votre ordinateur de bureau.</span><span class="sxs-lookup"><span data-stu-id="71256-117">Instead you simulate the mobile user experience from your laptop or desktop.</span></span>  

<span data-ttu-id="71256-118">Certains aspects des appareils mobiles ne sont jamais émulés dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="71256-118">Some aspects of mobile devices are never emulated in DevTools.</span></span>  <span data-ttu-id="71256-119">Par exemple, l’architecture des UC mobiles est différente de l’architecture de l’ordinateur portable ou de l’UC de bureau.</span><span class="sxs-lookup"><span data-stu-id="71256-119">For example, the architecture of mobile CPUs is different than the architecture of laptop or desktop CPUs.</span></span>  <span data-ttu-id="71256-120">En cas de doute, il est préférable d’exécuter votre page sur un appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="71256-120">When in doubt, your best bet is to actually run your page on a mobile device.</span></span>  <span data-ttu-id="71256-121">Utilisez [débogage à distance] [DevToolsRemoteDebugging] pour interagir avec le code d’une page à partir de votre ordinateur, tandis que votre page s’exécute réellement sur un appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="71256-121">Use [Remote Debugging][DevToolsRemoteDebugging] to interact with the code of a page from your machine while your page actually runs on a mobile device.</span></span>  <span data-ttu-id="71256-122">Vous pouvez afficher, modifier, déboguer, profiler ou les quatre lorsque vous interagissez avec le code.</span><span class="sxs-lookup"><span data-stu-id="71256-122">You may view, change, debug, profile, or all four while you interact with the code.</span></span>  <span data-ttu-id="71256-123">Votre ordinateur est-il possible d’un bloc-notes ou d’un ordinateur de bureau.</span><span class="sxs-lookup"><span data-stu-id="71256-123">Your machine may be a notebook or desktop computer.</span></span>  

## <span data-ttu-id="71256-124">Simuler une fenêtre d’affichage mobile</span><span class="sxs-lookup"><span data-stu-id="71256-124">Simulate a mobile viewport</span></span>  

<span data-ttu-id="71256-125">Sélectionnez **basculer l’émulation d’appareil**  \ ( ![ activez la barre d’outils de l’appareil ][ImageDeviceToolbarIcon] \) ou sélectionnez **personnaliser et contrôler devtools** \ ( `...` \) > l' **émulation d’appareil** pour ouvrir l’interface utilisateur qui vous permet de simuler une fenêtre d’affichage mobile.</span><span class="sxs-lookup"><span data-stu-id="71256-125">Choose **Toggle device emulation**  \(![Toggle Device Toolbar][ImageDeviceToolbarIcon]\) or choose **Customize and control DevTools** \(`...`\) > **Device emulation** to open the UI that enables you to simulate a mobile viewport.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Barre d’outils de l’appareil" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
    <span data-ttu-id="71256-127">Barre d’outils de l’appareil</span><span class="sxs-lookup"><span data-stu-id="71256-127">The Device Toolbar</span></span>  
:::image-end:::  

<span data-ttu-id="71256-128">Par défaut, la barre d’outils de l’appareil s’ouvre en mode de fenêtre d’affichage réactif.</span><span class="sxs-lookup"><span data-stu-id="71256-128">By default the Device Toolbar opens in Responsive Viewport Mode.</span></span>  

### <span data-ttu-id="71256-129">Mode de fenêtre d’affichage réactif</span><span class="sxs-lookup"><span data-stu-id="71256-129">Responsive Viewport Mode</span></span>  

<span data-ttu-id="71256-130">Pour tester rapidement l’aspect de votre page sur plusieurs tailles d’écran, faites glisser les poignées pour redimensionner la fenêtre d’affichage selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="71256-130">To quickly test the look and feel of your page across multiple screen sizes, drag the handles to resize the viewport to your required dimensions.</span></span>  <span data-ttu-id="71256-131">Vous pouvez également entrer des valeurs spécifiques dans les zones largeur et hauteur.</span><span class="sxs-lookup"><span data-stu-id="71256-131">You may also enter specific values in the width and height boxes.</span></span>  <span data-ttu-id="71256-132">Dans l’illustration suivante, la largeur est définie sur `626` et la hauteur est définie sur `516` .</span><span class="sxs-lookup"><span data-stu-id="71256-132">In the following figure, the width is set to `626` and the height is set to `516`.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png" alt-text="Poignées permettant de modifier les dimensions de la fenêtre d’affichage en mode de fenêtre d’affichage réactif" lightbox="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png":::
    <span data-ttu-id="71256-134">Poignées permettant de modifier les dimensions de la fenêtre d’affichage en mode de fenêtre d’affichage réactif</span><span class="sxs-lookup"><span data-stu-id="71256-134">The handles for changing the dimensions of the viewport when in Responsive Viewport Mode</span></span>  
:::image-end:::  

#### <span data-ttu-id="71256-135">Afficher les requêtes multimédias</span><span class="sxs-lookup"><span data-stu-id="71256-135">Show media queries</span></span>  

<span data-ttu-id="71256-136">Si vous avez défini des requêtes multimédias sur votre page, accédez aux dimensions de la fenêtre d’affichage dans lesquelles ces requêtes multimédias sont prises en compte en affichant des points d’arrêt de requête multimédia au-dessus de votre fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="71256-136">If you have defined media queries on your page, jump to the viewport dimensions where those media queries take effect by showing media query breakpoints above your viewport.</span></span>  <span data-ttu-id="71256-137">Sélectionnez **autres options**  >  **afficher les requêtes multimédias**.</span><span class="sxs-lookup"><span data-stu-id="71256-137">Choose **More options** > **Show media queries**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png" alt-text="Afficher les requêtes multimédias" lightbox="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png":::
   **<span data-ttu-id="71256-139">Afficher les requêtes multimédias</span><span class="sxs-lookup"><span data-stu-id="71256-139">Show media queries</span></span>**  
:::image-end:::  

<span data-ttu-id="71256-140">Choisissez un point d’arrêt pour modifier la largeur de la fenêtre d’affichage de telle sorte que la requête multimédia soit déclenchée.</span><span class="sxs-lookup"><span data-stu-id="71256-140">Choose a breakpoint to change the width of the viewport so that the media query gets triggered.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png" alt-text="Sélectionner un point d’arrêt pour modifier la largeur de la fenêtre d’affichage" lightbox="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png":::
   <span data-ttu-id="71256-142">Sélectionner un point d’arrêt pour modifier la largeur de la fenêtre d’affichage</span><span class="sxs-lookup"><span data-stu-id="71256-142">Choose a breakpoint to change the width of the viewport</span></span>  
:::image-end:::  

#### <span data-ttu-id="71256-143">Définir le type d’appareil</span><span class="sxs-lookup"><span data-stu-id="71256-143">Set the device type</span></span>  

<span data-ttu-id="71256-144">Utilisez la liste **type d’appareil** pour simuler un appareil mobile ou un appareil de bureau.</span><span class="sxs-lookup"><span data-stu-id="71256-144">Use the **Device Type** list to simulate a mobile device or desktop device.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png" alt-text="Liste type d’appareil" lightbox="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png":::
   <span data-ttu-id="71256-146">Liste **type d’appareil**</span><span class="sxs-lookup"><span data-stu-id="71256-146">The **Device Type** list</span></span>  
:::image-end:::  

<span data-ttu-id="71256-147">Le tableau suivant décrit les différences entre les options de type d’appareil disponibles.</span><span class="sxs-lookup"><span data-stu-id="71256-147">The following table describes the differences between the available device type options.</span></span>  <span data-ttu-id="71256-148">La colonne méthode de rendu fait référence au rendu de la page par Microsoft Edge en tant qu’affichage mobile ou de bureau.</span><span class="sxs-lookup"><span data-stu-id="71256-148">The Rendering method column refers to whether Microsoft Edge renders the page as a mobile or desktop viewport.</span></span>  <span data-ttu-id="71256-149">La colonne icône du curseur fait référence au type de curseur qui s’affiche lorsque vous pointez sur la page.</span><span class="sxs-lookup"><span data-stu-id="71256-149">The Cursor icon column refers to what type of cursor you see when you hover on the page.</span></span>  <span data-ttu-id="71256-150">La colonne déclenchée Events indique si la page déclenche ou a des `touch` `click` événements lorsque vous interagissez avec la page.</span><span class="sxs-lookup"><span data-stu-id="71256-150">The Events triggered column refers to whether the page triggers `touch` or `click` events when you interact with the page.</span></span>  

| <span data-ttu-id="71256-151">Option</span><span class="sxs-lookup"><span data-stu-id="71256-151">Option</span></span> | <span data-ttu-id="71256-152">Méthode de rendu</span><span class="sxs-lookup"><span data-stu-id="71256-152">Rendering method</span></span> | <span data-ttu-id="71256-153">Icône du curseur</span><span class="sxs-lookup"><span data-stu-id="71256-153">Cursor icon</span></span> | <span data-ttu-id="71256-154">Événements déclenchés</span><span class="sxs-lookup"><span data-stu-id="71256-154">Events triggered</span></span> |  
|:--- |:--- |:--- |:--- |  
| <span data-ttu-id="71256-155">Appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="71256-155">Mobile</span></span> | <span data-ttu-id="71256-156">Appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="71256-156">Mobile</span></span> | <span data-ttu-id="71256-157">Cercle</span><span class="sxs-lookup"><span data-stu-id="71256-157">Circle</span></span> | <span data-ttu-id="71256-158">interface tactile</span><span class="sxs-lookup"><span data-stu-id="71256-158">touch</span></span> |  
| <span data-ttu-id="71256-159">Mobile \ (sans interaction</span><span class="sxs-lookup"><span data-stu-id="71256-159">Mobile \(no touch\)</span></span> | <span data-ttu-id="71256-160">Appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="71256-160">Mobile</span></span> | <span data-ttu-id="71256-161">Normal</span><span class="sxs-lookup"><span data-stu-id="71256-161">Normal</span></span> | <span data-ttu-id="71256-162"> cliquez sur </span><span class="sxs-lookup"><span data-stu-id="71256-162">click</span></span> |  
| <span data-ttu-id="71256-163">Bureau</span><span class="sxs-lookup"><span data-stu-id="71256-163">Desktop</span></span> | <span data-ttu-id="71256-164">Bureau</span><span class="sxs-lookup"><span data-stu-id="71256-164">Desktop</span></span> | <span data-ttu-id="71256-165">Normal</span><span class="sxs-lookup"><span data-stu-id="71256-165">Normal</span></span> | <span data-ttu-id="71256-166"> cliquez sur </span><span class="sxs-lookup"><span data-stu-id="71256-166">click</span></span> |  
| <span data-ttu-id="71256-167">Bureau \ (effleurement)</span><span class="sxs-lookup"><span data-stu-id="71256-167">Desktop \(touch\)</span></span> | <span data-ttu-id="71256-168">Bureau</span><span class="sxs-lookup"><span data-stu-id="71256-168">Desktop</span></span> | <span data-ttu-id="71256-169">Cercle</span><span class="sxs-lookup"><span data-stu-id="71256-169">Circle</span></span> | <span data-ttu-id="71256-170">interface tactile</span><span class="sxs-lookup"><span data-stu-id="71256-170">touch</span></span> |  

> [!NOTE]
> <span data-ttu-id="71256-171">Si la liste **type d’appareil** n’est pas affichée, sélectionnez **autres options**  >  **Ajouter un type d’appareil**.</span><span class="sxs-lookup"><span data-stu-id="71256-171">If the **Device Type** list is not displayed, choose **More options** > **Add device type**.</span></span>  

### <span data-ttu-id="71256-172">Mode d’affichage de l’appareil mobile</span><span class="sxs-lookup"><span data-stu-id="71256-172">Mobile Device Viewport Mode</span></span>  

<span data-ttu-id="71256-173">Pour simuler les dimensions d’un appareil mobile spécifique, sélectionnez-le dans la liste des **appareils** .</span><span class="sxs-lookup"><span data-stu-id="71256-173">To simulate the dimensions of a specific mobile device, select the device from the **Device** list.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list.msft.png" alt-text="La liste des appareils" lightbox="../media/device-mode-toggle-device-toolbar-device-list.msft.png":::
   <span data-ttu-id="71256-175">La liste des **appareils**</span><span class="sxs-lookup"><span data-stu-id="71256-175">The **Device** list</span></span>  
:::image-end:::  

#### <span data-ttu-id="71256-176">Faire pivoter la fenêtre d’affichage avec l’orientation paysage</span><span class="sxs-lookup"><span data-stu-id="71256-176">Rotate the viewport to landscape orientation</span></span>  

<span data-ttu-id="71256-177">Testez votre page Web en orientation paysage.</span><span class="sxs-lookup"><span data-stu-id="71256-177">Test your webpage in landscape orientation.</span></span>  

*   <span data-ttu-id="71256-178">Pour faire pivoter la fenêtre d’affichage en orientation paysage, sélectionnez **faire pivoter** \ ( ![ rotation ][ImageRotateIcon] \).</span><span class="sxs-lookup"><span data-stu-id="71256-178">To rotate the viewport to landscape orientation, choose **Rotate** \(![Rotate][ImageRotateIcon]\).</span></span>  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-landscape.msft.png" alt-text="Page affichée en orientation paysage" lightbox="../media/device-mode-toggle-device-toolbar-landscape.msft.png":::
       <span data-ttu-id="71256-180">Page affichée en orientation paysage</span><span class="sxs-lookup"><span data-stu-id="71256-180">Page displayed in landscape orientation</span></span>  
    :::image-end:::  
    
> [!NOTE]
> <span data-ttu-id="71256-181">Le bouton **faire pivoter** disparaît si la **barre d’outils** de votre appareil est étroite.</span><span class="sxs-lookup"><span data-stu-id="71256-181">The **Rotate** button disappears if your **Device Toolbar** is narrow.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Barre d’outils de l’appareil" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   <span data-ttu-id="71256-183">**Barre d’outils** de l’appareil</span><span class="sxs-lookup"><span data-stu-id="71256-183">The **Device Toolbar**</span></span>  
:::image-end:::  

<span data-ttu-id="71256-184">Pour plus d’informations, voir [définir l’orientation](#set-orientation).</span><span class="sxs-lookup"><span data-stu-id="71256-184">For more information, go to [Set orientation](#set-orientation).</span></span>  

#### <span data-ttu-id="71256-185">Afficher le cadre de l’appareil</span><span class="sxs-lookup"><span data-stu-id="71256-185">Show device frame</span></span>  

<span data-ttu-id="71256-186">Affichez le frame d’appareil physique à l’écran de la fenêtre d’affichage lorsque vous simulez les dimensions d’un appareil mobile spécifique tel qu’un iPhone 6.</span><span class="sxs-lookup"><span data-stu-id="71256-186">Display the physical device frame around the viewport when you simulate the dimensions of a specific mobile device such as an iPhone 6.</span></span>  

1.  <span data-ttu-id="71256-187">Ouvrez **plus d’options**.</span><span class="sxs-lookup"><span data-stu-id="71256-187">Open **More options**.</span></span>  
1.  <span data-ttu-id="71256-188">Sélectionnez **afficher le cadre**de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="71256-188">Choose **Show device frame**.</span></span>  

> [!NOTE]
> <span data-ttu-id="71256-189">Si vous ne voyez pas d’image d’appareil pour un appareil particulier, cela signifie que DevTools n’a pas d’image pour cette option.</span><span class="sxs-lookup"><span data-stu-id="71256-189">If you do not see a device frame for a particular device, it means that DevTools does not have art for that option.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png" alt-text="Afficher le cadre de l’appareil" lightbox="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png":::
         <span data-ttu-id="71256-191">Afficher le cadre de l’appareil</span><span class="sxs-lookup"><span data-stu-id="71256-191">Show device frame</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png" alt-text="Le cadre de l’appareil pour l’iPhone 6" lightbox="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png":::
         <span data-ttu-id="71256-193">Le cadre de l’appareil pour l’iPhone 6</span><span class="sxs-lookup"><span data-stu-id="71256-193">The device frame for the iPhone 6</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### <span data-ttu-id="71256-194">Ajouter un appareil mobile personnalisé</span><span class="sxs-lookup"><span data-stu-id="71256-194">Add a custom mobile device</span></span>  

<span data-ttu-id="71256-195">Si l’option d’appareil mobile dont vous avez besoin ne figure pas dans la liste par défaut, vous pouvez ajouter un appareil personnalisé.</span><span class="sxs-lookup"><span data-stu-id="71256-195">If the mobile device option that you need is not included on the default list, you may add a custom device.</span></span>  <span data-ttu-id="71256-196">Pour ajouter un appareil personnalisé, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="71256-196">To add a custom device, complete the following steps.</span></span>  

1.  <span data-ttu-id="71256-197">Choisissez la liste des **appareils** > **modifier**.</span><span class="sxs-lookup"><span data-stu-id="71256-197">Choose the **Device** list > **Edit**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png" alt-text="Sélectionnez Modifier." lightbox="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png":::
       <span data-ttu-id="71256-199">Sélectionnez **modifier** .</span><span class="sxs-lookup"><span data-stu-id="71256-199">Select **Edit**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="71256-200">Sélectionnez **Ajouter un appareil personnalisé**.</span><span class="sxs-lookup"><span data-stu-id="71256-200">Choose **Add custom device**.</span></span>  
1.  <span data-ttu-id="71256-201">Sur les **appareils émulés**, entrez le nom d’un appareil, la largeur de l’écran et la hauteur de l’écran de l’appareil personnalisé.</span><span class="sxs-lookup"><span data-stu-id="71256-201">On **Emulated Devices**, enter a device name, screen width, and screen height for the custom device.</span></span>  <span data-ttu-id="71256-202">Le [coefficient d’appareil][MDNWindowDevicePixelRatio], la [chaîne de l’agent utilisateur][MDNUserAgent]et les champs [type d’appareil](#set-the-device-type) sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="71256-202">The [device pixel ratio][MDNWindowDevicePixelRatio], [user agent string][MDNUserAgent], and [device type](#set-the-device-type) fields are optional.</span></span>  <span data-ttu-id="71256-203">Le champ type d’appareil utilise par défaut la valeur **mobile**.</span><span class="sxs-lookup"><span data-stu-id="71256-203">The device type field defaults to **Mobile**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png" alt-text="Créer un appareil personnalisé" lightbox="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png":::
       <span data-ttu-id="71256-205">Créer un appareil personnalisé</span><span class="sxs-lookup"><span data-stu-id="71256-205">Create a custom device</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="71256-206">Afficher les règles</span><span class="sxs-lookup"><span data-stu-id="71256-206">Show rulers</span></span>  

<span data-ttu-id="71256-207">Si vous avez besoin de mesurer les dimensions de l’écran, vous pouvez utiliser des règles pour mesurer la taille de l’écran en pixels.</span><span class="sxs-lookup"><span data-stu-id="71256-207">If you need to measure screen dimensions, you may use rulers to measure the screen size in pixels.</span></span>  <span data-ttu-id="71256-208">Sélectionnez **autres options**  >  **afficher les règles** pour afficher les règles au-dessus et à gauche de votre fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="71256-208">Choose **More options** > **Show rulers** to display rulers above and to the left of your viewport.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png" alt-text="Option de menu pour afficher les règles" lightbox="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png":::
         <span data-ttu-id="71256-210">Option de menu pour afficher les règles</span><span class="sxs-lookup"><span data-stu-id="71256-210">Menu item to display rulers</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-rulers.msft.png" alt-text="Règles au-dessus et à gauche de la fenêtre d’affichage" lightbox="../media/device-mode-toggle-device-toolbar-rulers.msft.png":::
         <span data-ttu-id="71256-212">Règles au-dessus et à gauche de la fenêtre d’affichage</span><span class="sxs-lookup"><span data-stu-id="71256-212">Rulers above and to the left of the viewport</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="71256-213">Effectuer un zoom dans la fenêtre d’affichage</span><span class="sxs-lookup"><span data-stu-id="71256-213">Zoom the viewport</span></span>  

<span data-ttu-id="71256-214">Pour tester l’apparence de votre page à plusieurs niveaux de zoom, utilisez la liste **Zoom** pour effectuer un zoom avant ou arrière.</span><span class="sxs-lookup"><span data-stu-id="71256-214">To test the look and feel of your page at multiple zoom levels, use the **Zoom** list to zoom in or out.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-zoom.msft.png" alt-text="Zoom" lightbox="../media/device-mode-toggle-device-toolbar-zoom.msft.png":::
   **<span data-ttu-id="71256-216">Zoom</span><span class="sxs-lookup"><span data-stu-id="71256-216">Zoom</span></span>**  
:::image-end:::  

## <span data-ttu-id="71256-217">Limiter le réseau et le processeur</span><span class="sxs-lookup"><span data-stu-id="71256-217">Throttle the network and CPU</span></span>  

<span data-ttu-id="71256-218">Les appareils mobiles sont souvent dotés de contraintes réseau et UC.</span><span class="sxs-lookup"><span data-stu-id="71256-218">Mobile devices often have network and CPU constraints.</span></span>  <span data-ttu-id="71256-219">Assurez-vous d’avoir testé la rapidité de chargement de la page et la manière dont elle réagit aux différentes vitesses d’utilisation de l’Internet et du processeur.</span><span class="sxs-lookup"><span data-stu-id="71256-219">Ensure you test how quickly your page loads and how it responds at different internet and CPU speeds.</span></span>  

<span data-ttu-id="71256-220">Limiter le réseau et le processeur.</span><span class="sxs-lookup"><span data-stu-id="71256-220">Throttle the network and CPU.</span></span>  

1.  <span data-ttu-id="71256-221">Choisissez liste de **limitations** et sélectionnez mobile de **niveau supérieur** ou mobile de niveau **inférieur**.</span><span class="sxs-lookup"><span data-stu-id="71256-221">Choose **Throttle** list and change the preset to **Mid-tier mobile** or **Low-end mobile**.</span></span>  
    *   <span data-ttu-id="71256-222">Le **mobile milieu de niveau** simule `fast 3G` et limite votre processeur.</span><span class="sxs-lookup"><span data-stu-id="71256-222">**Mid-tier mobile** simulates `fast 3G` and throttles your CPU.</span></span>  <span data-ttu-id="71256-223">Il est quatre fois plus lent qu’normal.</span><span class="sxs-lookup"><span data-stu-id="71256-223">It is four times slower than normal.</span></span>  
    *   <span data-ttu-id="71256-224">Un **mobile de bas de gamme** simule `slow 3G` et limite votre processeur.</span><span class="sxs-lookup"><span data-stu-id="71256-224">**Low-end mobile** simulates `slow 3G` and throttles your CPU.</span></span>  <span data-ttu-id="71256-225">Il est plus lent que le nombre normal.</span><span class="sxs-lookup"><span data-stu-id="71256-225">It is six times slower than normal.</span></span>  
    
<span data-ttu-id="71256-226">Toutes les limitations dépendent de la fonctionnalité normale de votre ordinateur portable ou de votre ordinateur de bureau.</span><span class="sxs-lookup"><span data-stu-id="71256-226">All of the throttling is based upon the normal capability of your laptop or desktop.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-throttle.msft.png" alt-text="Liste de limitations de la barre d’outils de l’appareil" lightbox="../media/device-mode-toggle-device-toolbar-throttle.msft.png":::
   <span data-ttu-id="71256-228">Liste de **limitations** de la barre d’outils de l’appareil</span><span class="sxs-lookup"><span data-stu-id="71256-228">The **Throttle** list in the Device Toolbar</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="71256-229">Si la **liste des limitations** est masquée, votre **barre d’outils** de l’appareil est trop étroite.</span><span class="sxs-lookup"><span data-stu-id="71256-229">If the **Throttle list** is hidden, your **Device Toolbar** is too narrow.</span></span>  <span data-ttu-id="71256-230">Pour accéder à la **liste de limitation**, augmentez la largeur de la **barre d’outils**de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="71256-230">To access the **Throttle list**, increase the width of the **Device Toolbar**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Barre d’outils de l’appareil" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   <span data-ttu-id="71256-232">**Barre d’outils** de l’appareil</span><span class="sxs-lookup"><span data-stu-id="71256-232">The **Device Toolbar**</span></span>  
:::image-end:::  

### <span data-ttu-id="71256-233">Limiter le processeur uniquement</span><span class="sxs-lookup"><span data-stu-id="71256-233">Throttle the CPU only</span></span>  

<span data-ttu-id="71256-234">Pour limiter le processeur et non le réseau, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="71256-234">To throttle the CPU only and not the network, complete the following steps.</span></span>

1.  <span data-ttu-id="71256-235">Sélectionnez le panneau **performances** , puis choisissez **paramètres de capture** \ ( ![ paramètres de capture ][ImageCaptureIcon] \).</span><span class="sxs-lookup"><span data-stu-id="71256-235">Choose the **Performance** panel, and choose **Capture Settings** \(![Capture Settings][ImageCaptureIcon]\).</span></span>
1.  <span data-ttu-id="71256-236">Sélectionnez **CPU**  >  **ralentissement** de l’UC 4x ou **6 ralentissements**.</span><span class="sxs-lookup"><span data-stu-id="71256-236">Choose **CPU** > **4x slowdown** or **6x slowdown**.</span></span>
    
    :::image type="complex" source="../media/device-mode-performance-cpu-throttle.msft.png" alt-text="Liste UC du panneau de performance" lightbox="../media/device-mode-performance-cpu-throttle.msft.png":::
       <span data-ttu-id="71256-238">Liste **UC** du panneau de **performance**</span><span class="sxs-lookup"><span data-stu-id="71256-238">The **CPU** list in the **Performance** panel</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="71256-239">Limiter le réseau uniquement</span><span class="sxs-lookup"><span data-stu-id="71256-239">Throttle the network only</span></span>  

<span data-ttu-id="71256-240">Pour limiter le réseau uniquement, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="71256-240">To throttle the network only, complete the following steps.</span></span>

1.  <span data-ttu-id="71256-241">Choisissez le panneau **réseau** .</span><span class="sxs-lookup"><span data-stu-id="71256-241">Choose the **Network** panel.</span></span>
1.  <span data-ttu-id="71256-242">Choisissez **connexion**  >  **Fast 3G** ou **lente 3G**.</span><span class="sxs-lookup"><span data-stu-id="71256-242">Choose **Online** > **Fast 3G** or **Slow 3G**.</span></span>
    
    :::image type="complex" source="../media/device-mode-network-throttle.msft.png" alt-text="Liste de limitations du panneau réseau" lightbox="../media/device-mode-network-throttle.msft.png":::
       <span data-ttu-id="71256-244">Liste de **limitations** du panneau réseau</span><span class="sxs-lookup"><span data-stu-id="71256-244">The **Throttle** list in the Network panel</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="71256-245">`Control` + `Shift` + `P` Vous pouvez sélectionner \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le **menu de commandes**, taper `3G` , puis sélectionner **activer la limitation Fast 3G** ou **activer la limitation 3G lente**.</span><span class="sxs-lookup"><span data-stu-id="71256-245">Or select `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**, type `3G`, and choose **Enable fast 3G throttling** or **Enable slow 3G throttling**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-command-menu-throttle.msft.png" alt-text="Menu de commandes" lightbox="../media/device-mode-command-menu-throttle.msft.png":::
       <span data-ttu-id="71256-247">**Menu de commandes**</span><span class="sxs-lookup"><span data-stu-id="71256-247">The **Command Menu**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="71256-248">Vous pouvez également définir la limitation du réseau dans le panneau **performances** .</span><span class="sxs-lookup"><span data-stu-id="71256-248">You may also set network throttling from the **Performance** panel.</span></span>  

1.  <span data-ttu-id="71256-249">Sélectionnez **paramètres de capture** \ ( ![ paramètres de capture ][ImageCaptureIcon] \), puis choisissez la liste des **réseaux** et définissez le paramètre prédéfini sur **Fast 3G** ou **lente 3G**.</span><span class="sxs-lookup"><span data-stu-id="71256-249">Choose **Capture Settings** \(![Capture Settings][ImageCaptureIcon]\) and choose the **Network** list and change the preset to **Fast 3G** or **Slow 3G**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-performance-network-throttle.msft.png" alt-text="Définir la limitation du réseau à partir du panneau performances" lightbox="../media/device-mode-performance-network-throttle.msft.png":::
       <span data-ttu-id="71256-251">Définir la limitation du réseau à partir du panneau **performances**</span><span class="sxs-lookup"><span data-stu-id="71256-251">Set network throttling from the **Performance** panel</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="71256-252">Remplacer la géolocalisation</span><span class="sxs-lookup"><span data-stu-id="71256-252">Override geolocation</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="71256-253">Si votre page dépend d’informations géolocalisation d’un appareil mobile pour s’afficher correctement, fournissez des géolocalisation différentes à l’aide de l’interface utilisateur de remplacement de géolocalisation.</span><span class="sxs-lookup"><span data-stu-id="71256-253">If your page depends on geolocation information from a mobile device to render properly, provide different geolocations using the geolocation overriding UI.</span></span>  

      1.  <span data-ttu-id="71256-254">Sélectionnez **personnaliser et contrôler devtools** \ ( `...` \) > **plus**de  >  **capteurs**d’outils.</span><span class="sxs-lookup"><span data-stu-id="71256-254">Choose **Customize and control DevTools** \(`...`\) > **More tools** > **Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Capteurs pour la géolocalisation" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         <span data-ttu-id="71256-256">**Capteurs** pour la géolocalisation</span><span class="sxs-lookup"><span data-stu-id="71256-256">**Sensors** for geolocation</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  <span data-ttu-id="71256-257">Ouvrir le menu de commandes.</span><span class="sxs-lookup"><span data-stu-id="71256-257">Open the Command Menu.</span></span>  
          *   <span data-ttu-id="71256-258">Sélectionnez `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="71256-258">Select `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  
      1. <span data-ttu-id="71256-259">Tapez `Sensors` , puis sélectionnez **afficher les capteurs**.</span><span class="sxs-lookup"><span data-stu-id="71256-259">Type `Sensors`, and choose **Show Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Afficher les capteurs pour la géolocalisation" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         <span data-ttu-id="71256-261">**Afficher les capteurs** pour la géolocalisation</span><span class="sxs-lookup"><span data-stu-id="71256-261">**Show Sensors** for geolocation</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="71256-262">Dans le panneau **capteurs** , vous pouvez sélectionner l’un des emplacements prédéfinis inclus dans devtools à l’aide du menu déroulant **emplacement** .</span><span class="sxs-lookup"><span data-stu-id="71256-262">On the **Sensors** panel, you may select one of the preset locations included in DevTools using the **Location** drop-down menu.</span></span>  <span data-ttu-id="71256-263">Pour entrer un emplacement personnalisé, sélectionnez **autres...**</span><span class="sxs-lookup"><span data-stu-id="71256-263">To enter a custom location, choose **Other…**</span></span> <span data-ttu-id="71256-264">et entrez les coordonnées de votre emplacement personnalisé.</span><span class="sxs-lookup"><span data-stu-id="71256-264">and enter the coordinates of your custom location.</span></span>  <span data-ttu-id="71256-265">Pour tester votre page dans un état d’erreur lorsque les informations de géolocalisation ne sont pas disponibles, sélectionnez **emplacement non disponible**.</span><span class="sxs-lookup"><span data-stu-id="71256-265">To test your page in an error state when location information is unavailable, choose **Location unavailable**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png" alt-text="Panneau capteurs avec une position prédéfinie sélectionnée" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png":::
    <span data-ttu-id="71256-267">Panneau **capteurs** avec une position prédéfinie sélectionnée</span><span class="sxs-lookup"><span data-stu-id="71256-267">**Sensors** panel with a preset location selected.</span></span>  
:::image-end:::

## <span data-ttu-id="71256-268">Définir l’orientation</span><span class="sxs-lookup"><span data-stu-id="71256-268">Set orientation</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="71256-269">Si votre page dépend des informations d’orientation d’un appareil mobile pour s’afficher correctement, ouvrez l’interface utilisateur d’orientation.</span><span class="sxs-lookup"><span data-stu-id="71256-269">If your page depends on orientation information from a mobile device to render properly, open the orientation UI.</span></span>  

      1.  <span data-ttu-id="71256-270">Sélectionnez **personnaliser et contrôler devtools** \ ( `...` \) > **plus**de  >  **capteurs**d’outils.</span><span class="sxs-lookup"><span data-stu-id="71256-270">Choose **Customize and control DevTools** \(`...`\) > **More tools** > **Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Capteurs d’orientation" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         <span data-ttu-id="71256-272">**Capteurs** d’orientation</span><span class="sxs-lookup"><span data-stu-id="71256-272">**Sensors** for orientation</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  <span data-ttu-id="71256-273">Ouvrir le menu de commandes.</span><span class="sxs-lookup"><span data-stu-id="71256-273">Open the Command Menu.</span></span>  
          *   <span data-ttu-id="71256-274">Sélectionnez `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="71256-274">Select `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  
      1. <span data-ttu-id="71256-275">Tapez `Sensors` , puis sélectionnez **afficher les capteurs**.</span><span class="sxs-lookup"><span data-stu-id="71256-275">Type `Sensors`, and choose **Show Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Afficher les capteurs d’orientation" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         <span data-ttu-id="71256-277">**Afficher les capteurs** d’orientation</span><span class="sxs-lookup"><span data-stu-id="71256-277">**Show Sensors** for orientation</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="71256-278">Dans le panneau **capteurs** , vous pouvez sélectionner une orientation prédéfinie dans le menu déroulant **orientation** .</span><span class="sxs-lookup"><span data-stu-id="71256-278">On the **Sensors** panel, you may select a preset orientation from the **Orientation** drop-down menu.</span></span>  <span data-ttu-id="71256-279">Pour entrer votre propre orientation, choisissez **orientation personnalisée**, puis entrez vos valeurs [alpha][MDNDeviceOrientaitonAlpha], [bêta][MDNDeviceOrientaitonBeta]et [gamma][MDNDeviceOrientaitonGamma] .</span><span class="sxs-lookup"><span data-stu-id="71256-279">To enter your own orientation, choose **Custom orientation**, and enter your own [alpha][MDNDeviceOrientaitonAlpha], [beta][MDNDeviceOrientaitonBeta], and [gamma][MDNDeviceOrientaitonGamma] values.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png" alt-text="Options d’orientation dans le panneau capteurs" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png":::
    <span data-ttu-id="71256-281">Options d' **orientation** dans le panneau **capteurs**</span><span class="sxs-lookup"><span data-stu-id="71256-281">**Orientation** options on the **Sensors** panel</span></span>  
:::image-end:::  

## <span data-ttu-id="71256-282">Définir une chaîne d’agent utilisateur</span><span class="sxs-lookup"><span data-stu-id="71256-282">Set user agent string</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="71256-283">Si votre page dépend de la chaîne de l’agent utilisateur d’un appareil mobile pour s’afficher correctement, utilisez le volet de **conditions réseau** pour fournir différentes chaînes d’agent utilisateur.</span><span class="sxs-lookup"><span data-stu-id="71256-283">If your page depends on the user agent string from a mobile device to render properly, use the **Network conditions** panel to provide different user agent strings.</span></span>  
      
      1.  <span data-ttu-id="71256-284">Sélectionnez **personnaliser et contrôler devtools** \ ( `...` \) > **plus d’outils**  >  **conditions réseau**.</span><span class="sxs-lookup"><span data-stu-id="71256-284">Choose **Customize and control DevTools** \(`...`\) > **More tools** > **Network conditions**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-network-conditions.msft.png" alt-text="Entrée conditions réseau dans le menu plus d’outils" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-network-conditions.msft.png":::
         <span data-ttu-id="71256-286">Entrée **conditions réseau** dans le menu **plus d’outils**</span><span class="sxs-lookup"><span data-stu-id="71256-286">**Network conditions** entry in the **More tools** menu</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  <span data-ttu-id="71256-287">Ouvrir le menu de commandes.</span><span class="sxs-lookup"><span data-stu-id="71256-287">Open the Command Menu.</span></span>  
          *   <span data-ttu-id="71256-288">Sélectionnez `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="71256-288">Select `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  
      1. <span data-ttu-id="71256-289">Tapez `Network conditions` , puis choisissez **afficher les conditions du réseau**.</span><span class="sxs-lookup"><span data-stu-id="71256-289">Type `Network conditions`, and choose **Show Network conditions**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-network-conditions.msft.png" alt-text="Afficher les conditions réseau" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-network-conditions.msft.png":::
         **<span data-ttu-id="71256-291">Afficher les conditions réseau</span><span class="sxs-lookup"><span data-stu-id="71256-291">Show Network conditions</span></span>**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="71256-292">En regard d' **agent utilisateur**, décochez la case **sélectionner automatiquement** .</span><span class="sxs-lookup"><span data-stu-id="71256-292">Next to **User agent**, clear the **Select automatically** checkbox.</span></span>  <span data-ttu-id="71256-293">Ensuite, sélectionnez **Custom (personnalisé)...** pour effectuer une sélection dans une liste de chaînes prédéfinies agent utilisateur.</span><span class="sxs-lookup"><span data-stu-id="71256-293">Then, select **Custom...** to select from a list of predefined user agent strings.</span></span>  <span data-ttu-id="71256-294">Pour entrer votre propre chaîne d’agent utilisateur, entrez la chaîne dans **entrer un agent utilisateur personnalisé**.</span><span class="sxs-lookup"><span data-stu-id="71256-294">To enter your own user agent string, enter the string in **Enter a custom user agent**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-network-conditions-macos.msft.png" alt-text="Définissez la chaîne de l’agent utilisateur sur Microsoft Edge sur macOS." lightbox="../media/device-mode-toggle-device-toolbar-network-conditions-macos.msft.png":::
    <span data-ttu-id="71256-296">Définissez la chaîne de l’agent utilisateur sur Microsoft Edge sur macOS.</span><span class="sxs-lookup"><span data-stu-id="71256-296">Set the user agent string to Microsoft Edge on macOS</span></span>  
:::image-end:::  

## <span data-ttu-id="71256-297">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="71256-297">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCaptureIcon]: ../media/capture-settings-icon.msft.png  
[ImageDeviceToolbarIcon]: ../media/toggle-device-toolbar-dark-icon.msft.png  
[ImageRotateIcon]: ../media/rotate-dark-icon.msft.png  

<!-- links -->  

<!--[DevToolsCommunity]: ../index.md#community "Join the DevTools community | Microsoft Docs"  -->
[DevToolsRemoteDebugging]: .. /Remote-Debugging/index.MD "mise en route des appareils Android de débogage à distance | Documents Microsoft  

[MDNWindowDevicePixelRatio]: https://developer.mozilla.org/docs/Web/API/Window/devicePixelRatio "Window. devicePixelRatio | MDN"  
[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Agent utilisateur | MDN"  
[MDNDeviceOrientaitonAlpha]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/alpha "DeviceOrientationEvent. alpha | MDN"  
[MDNDeviceOrientaitonBeta]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/beta "DeviceOrientationEvent. beta | MDN"  
[MDNDeviceOrientaitonGamma]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/gamma "DeviceOrientationEvent. gamma | MDN"  

[WikiApproximation]: https://en.wikipedia.org/wiki/Order_of_approximation#First-order "Ordre de rapprochement-premier-ordre-Wikipédia"  

> [!NOTE]
> <span data-ttu-id="71256-305">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="71256-305">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="71256-306">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="71256-306">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="71256-308">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="71256-308">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
