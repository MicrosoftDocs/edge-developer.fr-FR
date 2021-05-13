---
description: Utilisez des périphériques virtuels dans Microsoft Edge pour créer des sites web d’abord mobiles.
title: Émuler des appareils mobiles dans Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft Edge, développement web, outils f12, devtools, émulation, appareil, simulation, mobile
ms.openlocfilehash: b62a1799b1707fc4c6890bb7ad9ad4aa9afab113
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564405"
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
# <a name="emulate-mobile-devices-in-microsoft-edge-devtools"></a><span data-ttu-id="61652-104">Émuler des appareils mobiles dans Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="61652-104">Emulate mobile devices in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="61652-105">Utilisez **l’émulation de l’appareil** pour approximativement l’apparence et la réponse de votre page sur un appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="61652-105">Use **Device emulation** to approximate how your page looks and responds on a mobile device.</span></span>  <span data-ttu-id="61652-106">Les Microsoft Edge DevTools fournissent un ensemble de fonctionnalités pour vous aider à émuler des appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="61652-106">The Microsoft Edge DevTools provide a collection of features to help you emulate mobile devices.</span></span>  <span data-ttu-id="61652-107">La collection inclut les fonctionnalités suivantes.</span><span class="sxs-lookup"><span data-stu-id="61652-107">The collection includes the following features.</span></span>  

*   [<span data-ttu-id="61652-108">Simuler une vue mobile</span><span class="sxs-lookup"><span data-stu-id="61652-108">Simulate a mobile viewport</span></span>](#simulate-a-mobile-viewport)  
*   [<span data-ttu-id="61652-109">Limiter le réseau</span><span class="sxs-lookup"><span data-stu-id="61652-109">Throttle the network</span></span>](#throttle-the-network-only)  
*   [<span data-ttu-id="61652-110">Limiter l’UC</span><span class="sxs-lookup"><span data-stu-id="61652-110">Throttle the CPU</span></span>](#throttle-the-cpu-only)  
*   [<span data-ttu-id="61652-111">Simuler la géolocalisation</span><span class="sxs-lookup"><span data-stu-id="61652-111">Simulate geolocation</span></span>](#override-geolocation)  
*   [<span data-ttu-id="61652-112">Définir l’orientation</span><span class="sxs-lookup"><span data-stu-id="61652-112">Set orientation</span></span>](#set-orientation)  
*   [<span data-ttu-id="61652-113">Définir la chaîne de l’agent utilisateur</span><span class="sxs-lookup"><span data-stu-id="61652-113">Set the user agent string</span></span>](#set-user-agent-string)  

## <a name="limitations"></a><span data-ttu-id="61652-114">Limitations</span><span class="sxs-lookup"><span data-stu-id="61652-114">Limitations</span></span>  

<span data-ttu-id="61652-115">**L’émulation d’appareil** est une [approximation][WikiApproximation] de premier ordre de l’apparence de votre page sur un appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="61652-115">**Device emulation** is a [first-order approximation][WikiApproximation] of the look and feel of your page on a mobile device.</span></span>  <span data-ttu-id="61652-116">**L’émulation d’appareil** n’exécute pas réellement votre code sur un appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="61652-116">**Device emulation** does not actually run your code on a mobile device.</span></span>  <span data-ttu-id="61652-117">Au lieu de cela, vous simulez l’expérience utilisateur mobile à partir de votre ordinateur portable ou de bureau.</span><span class="sxs-lookup"><span data-stu-id="61652-117">Instead you simulate the mobile user experience from your laptop or desktop.</span></span>  

<span data-ttu-id="61652-118">Certains aspects des appareils mobiles ne sont jamais émulés dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="61652-118">Some aspects of mobile devices are never emulated in DevTools.</span></span>  <span data-ttu-id="61652-119">Par exemple, l’architecture des processeurs mobiles est différente de celle des processeurs d’ordinateur portable ou de bureau.</span><span class="sxs-lookup"><span data-stu-id="61652-119">For example, the architecture of mobile CPUs is different than the architecture of laptop or desktop CPUs.</span></span>  <span data-ttu-id="61652-120">En cas de doute, votre meilleur objectif est d’exécuter réellement votre page sur un appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="61652-120">When in doubt, your best bet is to actually run your page on a mobile device.</span></span>  <span data-ttu-id="61652-121">Utilisez [Débogage à distance][DevToolsRemoteDebugging] pour interagir avec le code d’une page à partir de votre ordinateur pendant que votre page s’exécute réellement sur un appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="61652-121">Use [Remote Debugging][DevToolsRemoteDebugging] to interact with the code of a page from your machine while your page actually runs on a mobile device.</span></span>  <span data-ttu-id="61652-122">Vous pouvez afficher, modifier, déboguer, profiler ou les quatre pendant que vous interagissez avec le code.</span><span class="sxs-lookup"><span data-stu-id="61652-122">You may view, change, debug, profile, or all four while you interact with the code.</span></span>  <span data-ttu-id="61652-123">Votre ordinateur peut être un ordinateur de bureau ou un bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="61652-123">Your machine may be a notebook or desktop computer.</span></span>  

## <a name="simulate-a-mobile-viewport"></a><span data-ttu-id="61652-124">Simuler une vue mobile</span><span class="sxs-lookup"><span data-stu-id="61652-124">Simulate a mobile viewport</span></span>  

<span data-ttu-id="61652-125">Choose **Toggle device emulation**  \( ![ Toggle Device Toolbar ](../media/toggle-device-toolbar-dark-icon.msft.png) \) or choose **Customize and control DevTools** \( `...` \) > Device **emulation** to open the UI that enables you to simulate a mobile viewport.</span><span class="sxs-lookup"><span data-stu-id="61652-125">Choose **Toggle device emulation**  \(![Toggle Device Toolbar](../media/toggle-device-toolbar-dark-icon.msft.png)\) or choose **Customize and control DevTools** \(`...`\) > **Device emulation** to open the UI that enables you to simulate a mobile viewport.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Barre d’outils Appareil" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
    <span data-ttu-id="61652-127">Barre d’outils Appareil</span><span class="sxs-lookup"><span data-stu-id="61652-127">The Device Toolbar</span></span>  
:::image-end:::  

<span data-ttu-id="61652-128">Par défaut, la barre d’outils de l’appareil s’ouvre en mode Deport réactif.</span><span class="sxs-lookup"><span data-stu-id="61652-128">By default the Device Toolbar opens in Responsive Viewport Mode.</span></span>  

### <a name="responsive-viewport-mode"></a><span data-ttu-id="61652-129">Mode d’affichage réactif</span><span class="sxs-lookup"><span data-stu-id="61652-129">Responsive Viewport Mode</span></span>  

<span data-ttu-id="61652-130">Pour tester rapidement l’apparence de votre page sur plusieurs tailles d’écran, faites glisser les poignées pour resizer laport d’affichage à vos dimensions requises.</span><span class="sxs-lookup"><span data-stu-id="61652-130">To quickly test the look and feel of your page across multiple screen sizes, drag the handles to resize the viewport to your required dimensions.</span></span>  <span data-ttu-id="61652-131">Vous pouvez également entrer des valeurs spécifiques dans les zones de largeur et de hauteur.</span><span class="sxs-lookup"><span data-stu-id="61652-131">You may also enter specific values in the width and height boxes.</span></span>  <span data-ttu-id="61652-132">Dans la figure suivante, la largeur est définie sur `626` et la hauteur sur `516` .</span><span class="sxs-lookup"><span data-stu-id="61652-132">In the following figure, the width is set to `626` and the height is set to `516`.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png" alt-text="Poignées de modification des dimensions de laport d’affichage en mode d’affichage réactif" lightbox="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png":::
    <span data-ttu-id="61652-134">Poignées de modification des dimensions de laport d’affichage en mode d’affichage réactif</span><span class="sxs-lookup"><span data-stu-id="61652-134">The handles for changing the dimensions of the viewport when in Responsive Viewport Mode</span></span>  
:::image-end:::  

#### <a name="show-media-queries"></a><span data-ttu-id="61652-135">Afficher les requêtes multimédias</span><span class="sxs-lookup"><span data-stu-id="61652-135">Show media queries</span></span>  

<span data-ttu-id="61652-136">Si vous avez défini des requêtes multimédias sur votre page, vous pouvez passer aux dimensions de laport d’affichage dans laquelle ces requêtes multimédias prennent effet en affichant les points d’arrêt des requêtes multimédias au-dessus de votreport d’affichage.</span><span class="sxs-lookup"><span data-stu-id="61652-136">If you have defined media queries on your page, jump to the viewport dimensions where those media queries take effect by showing media query breakpoints above your viewport.</span></span>  <span data-ttu-id="61652-137">Choose **More options**Show media  >  **queries**.</span><span class="sxs-lookup"><span data-stu-id="61652-137">Choose **More options** > **Show media queries**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png" alt-text="Afficher les requêtes multimédias" lightbox="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png":::
   **<span data-ttu-id="61652-139">Afficher les requêtes multimédias</span><span class="sxs-lookup"><span data-stu-id="61652-139">Show media queries</span></span>**  
:::image-end:::  

<span data-ttu-id="61652-140">Choisissez un point d’arrêt pour modifier la largeur de laport d’affichage afin que la requête multimédia soit déclenchée.</span><span class="sxs-lookup"><span data-stu-id="61652-140">Choose a breakpoint to change the width of the viewport so that the media query gets triggered.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png" alt-text="Choisir un point d’arrêt pour modifier la largeur de laport d’affichage" lightbox="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png":::
   <span data-ttu-id="61652-142">Choisir un point d’arrêt pour modifier la largeur de laport d’affichage</span><span class="sxs-lookup"><span data-stu-id="61652-142">Choose a breakpoint to change the width of the viewport</span></span>  
:::image-end:::  

#### <a name="set-the-device-type"></a><span data-ttu-id="61652-143">Définir le type d’appareil</span><span class="sxs-lookup"><span data-stu-id="61652-143">Set the device type</span></span>  

<span data-ttu-id="61652-144">Utilisez la liste **Type d’appareil** pour simuler un appareil mobile ou un appareil de bureau.</span><span class="sxs-lookup"><span data-stu-id="61652-144">Use the **Device Type** list to simulate a mobile device or desktop device.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png" alt-text="Liste des types d’appareils" lightbox="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png":::
   <span data-ttu-id="61652-146">Liste **des types d’appareils**</span><span class="sxs-lookup"><span data-stu-id="61652-146">The **Device Type** list</span></span>  
:::image-end:::  

<span data-ttu-id="61652-147">Le tableau suivant décrit les différences entre les options de type d’appareil disponibles.</span><span class="sxs-lookup"><span data-stu-id="61652-147">The following table describes the differences between the available device type options.</span></span>  <span data-ttu-id="61652-148">La colonne Méthode de rendu indique si Microsoft Edge rendu de la page en tant que port d’affichage mobile ou de bureau.</span><span class="sxs-lookup"><span data-stu-id="61652-148">The Rendering method column refers to whether Microsoft Edge renders the page as a mobile or desktop viewport.</span></span>  <span data-ttu-id="61652-149">La colonne d’icône curseur fait référence au type de curseur qui s’affiche lorsque vous pointez sur la page.</span><span class="sxs-lookup"><span data-stu-id="61652-149">The Cursor icon column refers to what type of cursor is displayed when you hover on the page.</span></span>  <span data-ttu-id="61652-150">La colonne Événements déclenchés indique si la page se déclenche ou s’il s’agit d’événements lorsque `touch` `click` vous interagissez avec la page.</span><span class="sxs-lookup"><span data-stu-id="61652-150">The Events triggered column refers to whether the page triggers `touch` or `click` events when you interact with the page.</span></span>  

| <span data-ttu-id="61652-151">Option</span><span class="sxs-lookup"><span data-stu-id="61652-151">Option</span></span> | <span data-ttu-id="61652-152">Méthode de rendu</span><span class="sxs-lookup"><span data-stu-id="61652-152">Rendering method</span></span> | <span data-ttu-id="61652-153">Icône curseur</span><span class="sxs-lookup"><span data-stu-id="61652-153">Cursor icon</span></span> | <span data-ttu-id="61652-154">Événements déclenchés</span><span class="sxs-lookup"><span data-stu-id="61652-154">Events triggered</span></span> |  
|:--- |:--- |:--- |:--- |  
| <span data-ttu-id="61652-155">Appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="61652-155">Mobile</span></span> | <span data-ttu-id="61652-156">Appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="61652-156">Mobile</span></span> | <span data-ttu-id="61652-157">Cercle</span><span class="sxs-lookup"><span data-stu-id="61652-157">Circle</span></span> | <span data-ttu-id="61652-158">interface tactile</span><span class="sxs-lookup"><span data-stu-id="61652-158">touch</span></span> |  
| <span data-ttu-id="61652-159">Mobile \(aucune touche\)</span><span class="sxs-lookup"><span data-stu-id="61652-159">Mobile \(no touch\)</span></span> | <span data-ttu-id="61652-160">Appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="61652-160">Mobile</span></span> | <span data-ttu-id="61652-161">Normal</span><span class="sxs-lookup"><span data-stu-id="61652-161">Normal</span></span> | <span data-ttu-id="61652-162"> choisissez</span><span class="sxs-lookup"><span data-stu-id="61652-162">choose</span></span> |  
| <span data-ttu-id="61652-163">Bureau</span><span class="sxs-lookup"><span data-stu-id="61652-163">Desktop</span></span> | <span data-ttu-id="61652-164">Bureau</span><span class="sxs-lookup"><span data-stu-id="61652-164">Desktop</span></span> | <span data-ttu-id="61652-165">Normal</span><span class="sxs-lookup"><span data-stu-id="61652-165">Normal</span></span> | <span data-ttu-id="61652-166"> choisissez</span><span class="sxs-lookup"><span data-stu-id="61652-166">choose</span></span> |  
| <span data-ttu-id="61652-167">Bureau \(tactile\)</span><span class="sxs-lookup"><span data-stu-id="61652-167">Desktop \(touch\)</span></span> | <span data-ttu-id="61652-168">Bureau</span><span class="sxs-lookup"><span data-stu-id="61652-168">Desktop</span></span> | <span data-ttu-id="61652-169">Cercle</span><span class="sxs-lookup"><span data-stu-id="61652-169">Circle</span></span> | <span data-ttu-id="61652-170">interface tactile</span><span class="sxs-lookup"><span data-stu-id="61652-170">touch</span></span> |  

> [!NOTE]
> <span data-ttu-id="61652-171">Si la liste **Type d’appareil** n’est pas affichée, sélectionnez **Autres options**Ajouter un type  >  **d’appareil.**</span><span class="sxs-lookup"><span data-stu-id="61652-171">If the **Device Type** list is not displayed, choose **More options** > **Add device type**.</span></span>  

### <a name="mobile-device-viewport-mode"></a><span data-ttu-id="61652-172">Mode d’affichage d’appareil mobile</span><span class="sxs-lookup"><span data-stu-id="61652-172">Mobile Device Viewport Mode</span></span>  

<span data-ttu-id="61652-173">Pour simuler les dimensions d’un appareil mobile spécifique, sélectionnez l’appareil dans la liste **Des** appareils.</span><span class="sxs-lookup"><span data-stu-id="61652-173">To simulate the dimensions of a specific mobile device, select the device from the **Device** list.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list.msft.png" alt-text="Liste des appareils" lightbox="../media/device-mode-toggle-device-toolbar-device-list.msft.png":::
   <span data-ttu-id="61652-175">Liste **des appareils**</span><span class="sxs-lookup"><span data-stu-id="61652-175">The **Device** list</span></span>  
:::image-end:::  

#### <a name="rotate-the-viewport-to-landscape-orientation"></a><span data-ttu-id="61652-176">Faire pivoter laport d’affichage vers l’orientation paysage</span><span class="sxs-lookup"><span data-stu-id="61652-176">Rotate the viewport to landscape orientation</span></span>  

<span data-ttu-id="61652-177">Testez votre page web en orientation paysage.</span><span class="sxs-lookup"><span data-stu-id="61652-177">Test your webpage in landscape orientation.</span></span>  

*   <span data-ttu-id="61652-178">Pour faire pivoter la vue vers l’orientation paysage, choisissez **Rotation** \( ![ Rotation ](../media/rotate-dark-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="61652-178">To rotate the viewport to landscape orientation, choose **Rotate** \(![Rotate](../media/rotate-dark-icon.msft.png)\).</span></span>  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-landscape.msft.png" alt-text="Page affichée en orientation paysage" lightbox="../media/device-mode-toggle-device-toolbar-landscape.msft.png":::
       <span data-ttu-id="61652-180">Page affichée en orientation paysage</span><span class="sxs-lookup"><span data-stu-id="61652-180">Page displayed in landscape orientation</span></span>  
    :::image-end:::  
    
> [!NOTE]
> <span data-ttu-id="61652-181">Le **bouton Pivoter** disparaît si la barre d’outils de **votre** appareil est étroite.</span><span class="sxs-lookup"><span data-stu-id="61652-181">The **Rotate** button disappears if your **Device Toolbar** is narrow.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Barre d’outils Appareil" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   <span data-ttu-id="61652-183">Barre **d’outils Appareil**</span><span class="sxs-lookup"><span data-stu-id="61652-183">The **Device Toolbar**</span></span>  
:::image-end:::  

<span data-ttu-id="61652-184">Pour plus d’informations, accédez à [Définir l’orientation.](#set-orientation)</span><span class="sxs-lookup"><span data-stu-id="61652-184">For more information, navigate to [Set orientation](#set-orientation).</span></span>  

#### <a name="show-device-frame"></a><span data-ttu-id="61652-185">Afficher le cadre de l’appareil</span><span class="sxs-lookup"><span data-stu-id="61652-185">Show device frame</span></span>  

<span data-ttu-id="61652-186">Affichez le cadre de l’appareil physique autour de la fenêtre d’affichage lorsque vous simulez les dimensions d’un appareil mobile spécifique, tel qu’un iPhone 6.</span><span class="sxs-lookup"><span data-stu-id="61652-186">Display the physical device frame around the viewport when you simulate the dimensions of a specific mobile device such as an iPhone 6.</span></span>  

1.  <span data-ttu-id="61652-187">Ouvrez **plus d’options.**</span><span class="sxs-lookup"><span data-stu-id="61652-187">Open **More options**.</span></span>  
1.  <span data-ttu-id="61652-188">Choose **Show device frame**.</span><span class="sxs-lookup"><span data-stu-id="61652-188">Choose **Show device frame**.</span></span>  

> [!NOTE]
> <span data-ttu-id="61652-189">Si un cadre d’appareil pour un appareil particulier n’est pas affiché, cela signifie que DevTools n’a pas d’image pour l’option.</span><span class="sxs-lookup"><span data-stu-id="61652-189">If a device frame for a particular device is not displayed, it means that DevTools does not have art for the option.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png" alt-text="Afficher le cadre de l’appareil" lightbox="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png":::
         <span data-ttu-id="61652-191">Afficher le cadre de l’appareil</span><span class="sxs-lookup"><span data-stu-id="61652-191">Show device frame</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png" alt-text="Image de l’appareil iPhone 6" lightbox="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png":::
         <span data-ttu-id="61652-193">Image de l’appareil iPhone 6</span><span class="sxs-lookup"><span data-stu-id="61652-193">The device frame for the iPhone 6</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### <a name="add-a-custom-mobile-device"></a><span data-ttu-id="61652-194">Ajouter un appareil mobile personnalisé</span><span class="sxs-lookup"><span data-stu-id="61652-194">Add a custom mobile device</span></span>  

<span data-ttu-id="61652-195">Si l’option d’appareil mobile dont vous avez besoin n’est pas incluse dans la liste par défaut, vous pouvez ajouter un appareil personnalisé.</span><span class="sxs-lookup"><span data-stu-id="61652-195">If the mobile device option that you need is not included on the default list, you may add a custom device.</span></span>  <span data-ttu-id="61652-196">Pour ajouter un appareil personnalisé, complétez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="61652-196">To add a custom device, complete the following steps.</span></span>  

1.  <span data-ttu-id="61652-197">Choose the **Device** list > **Edit**.</span><span class="sxs-lookup"><span data-stu-id="61652-197">Choose the **Device** list > **Edit**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png" alt-text="Choose Edit" lightbox="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png":::
       <span data-ttu-id="61652-199">Choose **Edit**</span><span class="sxs-lookup"><span data-stu-id="61652-199">Choose **Edit**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="61652-200">Choisissez **Ajouter un appareil personnalisé.**</span><span class="sxs-lookup"><span data-stu-id="61652-200">Choose **Add custom device**.</span></span>  
1.  <span data-ttu-id="61652-201">Sur **les appareils émulés,** entrez un nom d’appareil, la largeur de l’écran et la hauteur de l’écran pour l’appareil personnalisé.</span><span class="sxs-lookup"><span data-stu-id="61652-201">On **Emulated Devices**, enter a device name, screen width, and screen height for the custom device.</span></span>  <span data-ttu-id="61652-202">Les champs [Ratio de pixels de][MDNWindowDevicePixelRatio]l’appareil, chaîne [d’agent utilisateur][MDNUserAgent]et [type](#set-the-device-type) d’appareil sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="61652-202">The [device pixel ratio][MDNWindowDevicePixelRatio], [user agent string][MDNUserAgent], and [device type](#set-the-device-type) fields are optional.</span></span>  <span data-ttu-id="61652-203">Par défaut, le champ De type d’appareil est **Mobile.**</span><span class="sxs-lookup"><span data-stu-id="61652-203">The device type field defaults to **Mobile**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png" alt-text="Créer un appareil personnalisé" lightbox="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png":::
       <span data-ttu-id="61652-205">Créer un appareil personnalisé</span><span class="sxs-lookup"><span data-stu-id="61652-205">Create a custom device</span></span>  
    :::image-end:::  
    
### <a name="show-rulers"></a><span data-ttu-id="61652-206">Afficher les règles</span><span class="sxs-lookup"><span data-stu-id="61652-206">Show rulers</span></span>  

<span data-ttu-id="61652-207">Si vous devez mesurer les dimensions de l’écran, vous pouvez utiliser des règles pour mesurer la taille de l’écran en pixels.</span><span class="sxs-lookup"><span data-stu-id="61652-207">If you need to measure screen dimensions, you may use rulers to measure the screen size in pixels.</span></span>  <span data-ttu-id="61652-208">Choose **More options**Show  >  **rulers** to display rulers above and to the left of your viewport.</span><span class="sxs-lookup"><span data-stu-id="61652-208">Choose **More options** > **Show rulers** to display rulers above and to the left of your viewport.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png" alt-text="Élément de menu pour afficher les règles" lightbox="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png":::
         <span data-ttu-id="61652-210">Élément de menu pour afficher les règles</span><span class="sxs-lookup"><span data-stu-id="61652-210">Menu item to display rulers</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-rulers.msft.png" alt-text="Règles au-dessus et à gauche de la vue" lightbox="../media/device-mode-toggle-device-toolbar-rulers.msft.png":::
         <span data-ttu-id="61652-212">Règles au-dessus et à gauche de la vue</span><span class="sxs-lookup"><span data-stu-id="61652-212">Rulers above and to the left of the viewport</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="zoom-the-viewport"></a><span data-ttu-id="61652-213">Zoomer la vue</span><span class="sxs-lookup"><span data-stu-id="61652-213">Zoom the viewport</span></span>  

<span data-ttu-id="61652-214">Pour tester l’apparence de votre page à plusieurs niveaux de zoom, utilisez la liste **Zoom** pour effectuer un zoom avant ou arrière.</span><span class="sxs-lookup"><span data-stu-id="61652-214">To test the look and feel of your page at multiple zoom levels, use the **Zoom** list to zoom in or out.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-zoom.msft.png" alt-text="Zoom" lightbox="../media/device-mode-toggle-device-toolbar-zoom.msft.png":::
   **<span data-ttu-id="61652-216">Zoom</span><span class="sxs-lookup"><span data-stu-id="61652-216">Zoom</span></span>**  
:::image-end:::  

## <a name="throttle-the-network-and-cpu"></a><span data-ttu-id="61652-217">Limiter le réseau et le processeur</span><span class="sxs-lookup"><span data-stu-id="61652-217">Throttle the network and CPU</span></span>  

<span data-ttu-id="61652-218">Les appareils mobiles ont souvent des contraintes de réseau et de processeur.</span><span class="sxs-lookup"><span data-stu-id="61652-218">Mobile devices often have network and CPU constraints.</span></span>  <span data-ttu-id="61652-219">Veillez à tester la rapidité de chargement de votre page et la façon dont elle répond à différentes vitesses internet et processeur.</span><span class="sxs-lookup"><span data-stu-id="61652-219">Ensure you test how quickly your page loads and how it responds at different internet and CPU speeds.</span></span>  

<span data-ttu-id="61652-220">Limiter le réseau et le processeur.</span><span class="sxs-lookup"><span data-stu-id="61652-220">Throttle the network and CPU.</span></span>  

1.  <span data-ttu-id="61652-221">Choose **Throttle** list and change the preset to **Mid-tier mobile** or **Low-end mobile**.</span><span class="sxs-lookup"><span data-stu-id="61652-221">Choose **Throttle** list and change the preset to **Mid-tier mobile** or **Low-end mobile**.</span></span>  
    *   <span data-ttu-id="61652-222">**Un appareil mobile de niveau intermédiaire** simule et limitation votre `fast 3G` processeur.</span><span class="sxs-lookup"><span data-stu-id="61652-222">**Mid-tier mobile** simulates `fast 3G` and throttles your CPU.</span></span>  <span data-ttu-id="61652-223">Elle est quatre fois plus lente que la normale.</span><span class="sxs-lookup"><span data-stu-id="61652-223">It is four times slower than normal.</span></span>  
    *   <span data-ttu-id="61652-224">**Un appareil mobile bas de gamme** simule et limitation votre `slow 3G` processeur.</span><span class="sxs-lookup"><span data-stu-id="61652-224">**Low-end mobile** simulates `slow 3G` and throttles your CPU.</span></span>  <span data-ttu-id="61652-225">Elle est six fois plus lente que la normale.</span><span class="sxs-lookup"><span data-stu-id="61652-225">It is six times slower than normal.</span></span>  
    
<span data-ttu-id="61652-226">Toutes les limitations sont basées sur les fonctionnalités normales de votre ordinateur portable ou de votre bureau.</span><span class="sxs-lookup"><span data-stu-id="61652-226">All of the throttling is based upon the normal capability of your laptop or desktop.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-throttle.msft.png" alt-text="Liste Limitation dans la barre d’outils de l’appareil" lightbox="../media/device-mode-toggle-device-toolbar-throttle.msft.png":::
   <span data-ttu-id="61652-228">Liste **Limitation dans** la barre d’outils de l’appareil</span><span class="sxs-lookup"><span data-stu-id="61652-228">The **Throttle** list in the Device Toolbar</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="61652-229">Si la liste **Throttle est** masquée, votre **barre d’outils d’appareil** est trop étroite.</span><span class="sxs-lookup"><span data-stu-id="61652-229">If the **Throttle list** is hidden, your **Device Toolbar** is too narrow.</span></span>  <span data-ttu-id="61652-230">Pour accéder à la liste **Limitation,** augmentez la largeur de la barre d’outils **de l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="61652-230">To access the **Throttle list**, increase the width of the **Device Toolbar**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Barre d’outils Appareil" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   <span data-ttu-id="61652-232">Barre **d’outils Appareil**</span><span class="sxs-lookup"><span data-stu-id="61652-232">The **Device Toolbar**</span></span>  
:::image-end:::  

### <a name="throttle-the-cpu-only"></a><span data-ttu-id="61652-233">Limiter l’UC uniquement</span><span class="sxs-lookup"><span data-stu-id="61652-233">Throttle the CPU only</span></span>  

<span data-ttu-id="61652-234">Pour limiter l’UC uniquement et non le réseau, complétez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="61652-234">To throttle the CPU only and not the network, complete the following steps.</span></span>

1.  <span data-ttu-id="61652-235">Choisissez le **panneau Performances,** puis **sélectionnez Capturer Paramètres** \( Capturer Paramètres ![ ](../media/capture-settings-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="61652-235">Choose the **Performance** panel, and choose **Capture Settings** \(![Capture Settings](../media/capture-settings-icon.msft.png)\).</span></span>
1.  <span data-ttu-id="61652-236">Choisissez **le**  >  **ralentissement 4x du** processeur ou le ralentissement **6x.**</span><span class="sxs-lookup"><span data-stu-id="61652-236">Choose **CPU** > **4x slowdown** or **6x slowdown**.</span></span>
    
    :::image type="complex" source="../media/device-mode-performance-cpu-throttle.msft.png" alt-text="Liste du processeur dans le panneau Performances" lightbox="../media/device-mode-performance-cpu-throttle.msft.png":::
       <span data-ttu-id="61652-238">Liste **du processeur** dans le panneau **Performances**</span><span class="sxs-lookup"><span data-stu-id="61652-238">The **CPU** list in the **Performance** panel</span></span>  
    :::image-end:::  
    
### <a name="throttle-the-network-only"></a><span data-ttu-id="61652-239">Limiter le réseau uniquement</span><span class="sxs-lookup"><span data-stu-id="61652-239">Throttle the network only</span></span>  

<span data-ttu-id="61652-240">Pour limiter le réseau uniquement, complétez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="61652-240">To throttle the network only, complete the following steps.</span></span>

1.  <span data-ttu-id="61652-241">Choisissez **l’outil** Réseau.</span><span class="sxs-lookup"><span data-stu-id="61652-241">Choose the **Network** tool.</span></span>
1.  <span data-ttu-id="61652-242">Choisissez **En ligne**Fast  >  **3G** ou Slow **3G**.</span><span class="sxs-lookup"><span data-stu-id="61652-242">Choose **Online** > **Fast 3G** or **Slow 3G**.</span></span>
    
    :::image type="complex" source="../media/device-mode-network-throttle.msft.png" alt-text="Liste De limitation dans le panneau Réseau" lightbox="../media/device-mode-network-throttle.msft.png":::
       <span data-ttu-id="61652-244">Liste **De limitation** dans le panneau Réseau</span><span class="sxs-lookup"><span data-stu-id="61652-244">The **Throttle** list in the Network panel</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="61652-245">Ou sélectionnez `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\) \*\*\*\* `3G` \*\*\*\* \*\*\*\* pour ouvrir le menu commande, tapez et choisissez Activer la limitation 3G rapide ou Activer la limitation de 3G lente.</span><span class="sxs-lookup"><span data-stu-id="61652-245">Or select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**, type `3G`, and choose **Enable fast 3G throttling** or **Enable slow 3G throttling**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-command-menu-throttle.msft.png" alt-text="Menu Commande" lightbox="../media/device-mode-command-menu-throttle.msft.png":::
       <span data-ttu-id="61652-247">Menu **Commande**</span><span class="sxs-lookup"><span data-stu-id="61652-247">The **Command Menu**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="61652-248">Vous pouvez également définir la limitation du réseau à partir du **panneau Performances.**</span><span class="sxs-lookup"><span data-stu-id="61652-248">You may also set network throttling from the **Performance** panel.</span></span>  

1.  <span data-ttu-id="61652-249">Choose **Capture Paramètres** \( Capture Paramètres ![ ](../media/capture-settings-icon.msft.png) \) and choose the **Network** list and change the preset to **Fast 3G** or Slow **3G**.</span><span class="sxs-lookup"><span data-stu-id="61652-249">Choose **Capture Settings** \(![Capture Settings](../media/capture-settings-icon.msft.png)\) and choose the **Network** list and change the preset to **Fast 3G** or **Slow 3G**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-performance-network-throttle.msft.png" alt-text="Définir la limitation du réseau à partir du panneau Performances" lightbox="../media/device-mode-performance-network-throttle.msft.png":::
       <span data-ttu-id="61652-251">Définir la limitation du réseau à partir du panneau **Performances**</span><span class="sxs-lookup"><span data-stu-id="61652-251">Set network throttling from the **Performance** panel</span></span>  
    :::image-end:::  
    
## <a name="override-geolocation"></a><span data-ttu-id="61652-252">Remplacer la géolocalisation</span><span class="sxs-lookup"><span data-stu-id="61652-252">Override geolocation</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="61652-253">Si votre page dépend des informations de géolocalisation d’un appareil mobile pour un rendu correct, fournissez différentes géolocalisations à l’aide de l’interface utilisateur de remplacement de la géolocalisation.</span><span class="sxs-lookup"><span data-stu-id="61652-253">If your page depends on geolocation information from a mobile device to render properly, provide different geolocations using the geolocation overriding UI.</span></span>  

      1.  <span data-ttu-id="61652-254">Choose **Customize and control DevTools** \( `...` \) > More **tools**  >  **Sensors**.</span><span class="sxs-lookup"><span data-stu-id="61652-254">Choose **Customize and control DevTools** \(`...`\) > **More tools** > **Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Capteurs pour la géolocalisation" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         <span data-ttu-id="61652-256">**Capteurs** pour la géolocalisation</span><span class="sxs-lookup"><span data-stu-id="61652-256">**Sensors** for geolocation</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  <span data-ttu-id="61652-257">Ouvrez le menu Commande.</span><span class="sxs-lookup"><span data-stu-id="61652-257">Open the Command Menu.</span></span>  
          *   <span data-ttu-id="61652-258">Sélectionnez `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="61652-258">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  
      1. <span data-ttu-id="61652-259">Tapez `Sensors` et choisissez Afficher les **capteurs.**</span><span class="sxs-lookup"><span data-stu-id="61652-259">Type `Sensors`, and choose **Show Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Afficher les capteurs pour la géolocalisation" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         <span data-ttu-id="61652-261">**Afficher les capteurs** pour la géolocalisation</span><span class="sxs-lookup"><span data-stu-id="61652-261">**Show Sensors** for geolocation</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="61652-262">Dans le **panneau Capteurs,** vous pouvez sélectionner l’un des emplacements prédéfinés inclus dans DevTools à l’aide du menu déroulant Emplacement. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="61652-262">On the **Sensors** panel, you may select one of the preset locations included in DevTools using the **Location** drop-down menu.</span></span>  <span data-ttu-id="61652-263">Pour entrer un emplacement personnalisé, choisissez **Autre...**</span><span class="sxs-lookup"><span data-stu-id="61652-263">To enter a custom location, choose **Other…**</span></span> <span data-ttu-id="61652-264">et entrez les coordonnées de votre emplacement personnalisé.</span><span class="sxs-lookup"><span data-stu-id="61652-264">and enter the coordinates of your custom location.</span></span>  <span data-ttu-id="61652-265">Pour tester votre page dans un état d’erreur lorsque les informations d’emplacement ne sont pas disponibles, choisissez **Emplacement indisponible.**</span><span class="sxs-lookup"><span data-stu-id="61652-265">To test your page in an error state when location information is unavailable, choose **Location unavailable**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png" alt-text="Panneau capteurs avec un emplacement prédéfiny sélectionné" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png":::
    <span data-ttu-id="61652-267">**Panneau capteurs** avec un emplacement prédéfiny sélectionné.</span><span class="sxs-lookup"><span data-stu-id="61652-267">**Sensors** panel with a preset location selected.</span></span>  
:::image-end:::

## <a name="set-orientation"></a><span data-ttu-id="61652-268">Définir l’orientation</span><span class="sxs-lookup"><span data-stu-id="61652-268">Set orientation</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="61652-269">Si votre page dépend des informations d’orientation d’un appareil mobile pour un rendu correct, ouvrez l’interface utilisateur d’orientation.</span><span class="sxs-lookup"><span data-stu-id="61652-269">If your page depends on orientation information from a mobile device to render properly, open the orientation UI.</span></span>  

      1.  <span data-ttu-id="61652-270">Choose **Customize and control DevTools** \( `...` \) > More **tools**  >  **Sensors**.</span><span class="sxs-lookup"><span data-stu-id="61652-270">Choose **Customize and control DevTools** \(`...`\) > **More tools** > **Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Capteurs d’orientation" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         <span data-ttu-id="61652-272">**Capteurs d’orientation**</span><span class="sxs-lookup"><span data-stu-id="61652-272">**Sensors** for orientation</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  <span data-ttu-id="61652-273">Ouvrez le menu Commande.</span><span class="sxs-lookup"><span data-stu-id="61652-273">Open the Command Menu.</span></span>  
          *   <span data-ttu-id="61652-274">Sélectionnez `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="61652-274">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  
      1. <span data-ttu-id="61652-275">Tapez `Sensors` et choisissez Afficher les **capteurs.**</span><span class="sxs-lookup"><span data-stu-id="61652-275">Type `Sensors`, and choose **Show Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Afficher les capteurs pour l’orientation" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         <span data-ttu-id="61652-277">**Afficher les capteurs pour** l’orientation</span><span class="sxs-lookup"><span data-stu-id="61652-277">**Show Sensors** for orientation</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="61652-278">Dans le **panneau Capteurs,** vous pouvez sélectionner une orientation prédéfinë dans le menu déroulant **Orientation.**</span><span class="sxs-lookup"><span data-stu-id="61652-278">On the **Sensors** panel, you may select a preset orientation from the **Orientation** drop-down menu.</span></span>  <span data-ttu-id="61652-279">Pour entrer votre propre orientation, choisissez **l’orientation**personnalisée, puis entrez vos propres valeurs [alpha,][MDNDeviceOrientaitonAlpha] [bêta][MDNDeviceOrientaitonBeta]et [gamma.][MDNDeviceOrientaitonGamma]</span><span class="sxs-lookup"><span data-stu-id="61652-279">To enter your own orientation, choose **Custom orientation**, and enter your own [alpha][MDNDeviceOrientaitonAlpha], [beta][MDNDeviceOrientaitonBeta], and [gamma][MDNDeviceOrientaitonGamma] values.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png" alt-text="Options d’orientation sur le panneau Capteurs" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png":::
    <span data-ttu-id="61652-281">**Options d’orientation** sur le **panneau Capteurs**</span><span class="sxs-lookup"><span data-stu-id="61652-281">**Orientation** options on the **Sensors** panel</span></span>  
:::image-end:::  

## <a name="set-user-agent-string"></a><span data-ttu-id="61652-282">Définir la chaîne de l’agent utilisateur</span><span class="sxs-lookup"><span data-stu-id="61652-282">Set user agent string</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="61652-283">Si votre page dépend de la chaîne d’agent utilisateur d’un appareil mobile pour un rendu correct, utilisez le panneau **Conditions** réseau pour fournir différentes chaînes d’agent utilisateur.</span><span class="sxs-lookup"><span data-stu-id="61652-283">If your page depends on the user agent string from a mobile device to render properly, use the **Network conditions** panel to provide different user agent strings.</span></span>  
      
      1.  <span data-ttu-id="61652-284">Choose **Customize and control DevTools** \( `...` \) > More **tools**  >  **Network conditions**.</span><span class="sxs-lookup"><span data-stu-id="61652-284">Choose **Customize and control DevTools** \(`...`\) > **More tools** > **Network conditions**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-network-conditions.msft.png" alt-text="Entrée des conditions réseau dans le menu Plus d’outils" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-network-conditions.msft.png":::
         <span data-ttu-id="61652-286">**Entrée des conditions réseau** dans le menu **Plus d’outils**</span><span class="sxs-lookup"><span data-stu-id="61652-286">**Network conditions** entry in the **More tools** menu</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  <span data-ttu-id="61652-287">Ouvrez le menu Commande.</span><span class="sxs-lookup"><span data-stu-id="61652-287">Open the Command Menu.</span></span>  
          *   <span data-ttu-id="61652-288">Sélectionnez `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="61652-288">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  
      1. <span data-ttu-id="61652-289">Tapez `Network conditions` et choisissez Afficher les conditions **réseau.**</span><span class="sxs-lookup"><span data-stu-id="61652-289">Type `Network conditions`, and choose **Show Network conditions**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-network-conditions.msft.png" alt-text="Afficher les conditions réseau" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-network-conditions.msft.png":::
         **<span data-ttu-id="61652-291">Afficher les conditions réseau</span><span class="sxs-lookup"><span data-stu-id="61652-291">Show Network conditions</span></span>**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="61652-292">En regard de **l’agent utilisateur,** cochez la **case** Sélectionner automatiquement.</span><span class="sxs-lookup"><span data-stu-id="61652-292">Next to **User agent**, clear the **Select automatically** checkbox.</span></span>  <span data-ttu-id="61652-293">Ensuite, choisissez **Personnalisé...** pour sélectionner dans une liste de chaînes d’agent utilisateur prédéfinées.</span><span class="sxs-lookup"><span data-stu-id="61652-293">Then, choose **Custom...** to select from a list of predefined user agent strings.</span></span>  <span data-ttu-id="61652-294">Pour entrer votre propre chaîne d’agent utilisateur, entrez la chaîne **dans Entrer un agent utilisateur personnalisé.**</span><span class="sxs-lookup"><span data-stu-id="61652-294">To enter your own user agent string, enter the string in **Enter a custom user agent**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-network-conditions-macos.msft.png" alt-text="Définir la chaîne de l’agent utilisateur sur Microsoft Edge sur macOS" lightbox="../media/device-mode-toggle-device-toolbar-network-conditions-macos.msft.png":::
    <span data-ttu-id="61652-296">Définir la chaîne de l’agent utilisateur sur Microsoft Edge sur macOS</span><span class="sxs-lookup"><span data-stu-id="61652-296">Set the user agent string to Microsoft Edge on macOS</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="61652-297">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="61652-297">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

<!--[DevToolsCommunity]: ../index.md#community "Join the DevTools community | Microsoft Docs"  -->
[DevToolsRemoteDebugging]: .. /remote-debugging/index.md " Get started with remote debugging Android devices | Microsoft Docs »  

[MDNWindowDevicePixelRatio]: https://developer.mozilla.org/docs/Web/API/Window/devicePixelRatio "Window.devicePixelRatio | MDN"  
[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Agent utilisateur | MDN"  
[MDNDeviceOrientaitonAlpha]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/alpha "DeviceOrientationEvent.alpha, | MDN"  
[MDNDeviceOrientaitonBeta]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/beta "DeviceOrientationEvent.beta, | MDN"  
[MDNDeviceOrientaitonGamma]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/gamma "DeviceOrientationEvent.gamma, | MDN"  

[WikiApproximation]: https://en.wikipedia.org/wiki/Order_of_approximation#First-order "Order of Approximation - First-order - Wikipedia"  

> [!NOTE]
> <span data-ttu-id="61652-305">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="61652-305">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="61652-306">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="61652-306">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="61652-308">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="61652-308">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
