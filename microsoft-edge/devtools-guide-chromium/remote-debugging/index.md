---
title: Découvrir les appareils Android de débogage à distance
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: fc7450ba2b088eee8f4005216374980096cbb067
ms.sourcegitcommit: ba9f0ed77e84174b03262b17e62c6a7e26cfeb3d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/30/2020
ms.locfileid: "10688150"
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

# <span data-ttu-id="18b91-103">Découvrir les appareils Android de débogage à distance</span><span class="sxs-lookup"><span data-stu-id="18b91-103">Get started with remote debugging Android devices</span></span>  

<span data-ttu-id="18b91-104">Déboguez à distance le contenu en direct sur un appareil Android à partir de votre ordinateur Windows ou macOS.</span><span class="sxs-lookup"><span data-stu-id="18b91-104">Remote debug live content on an Android device from your Windows or macOS computer.</span></span>  <span data-ttu-id="18b91-105">Cette page de didacticiel vous explique comment effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="18b91-105">This tutorial page teaches you how to complete the following actions.</span></span>  

*   <span data-ttu-id="18b91-106">Configurez votre appareil Android pour le débogage à distance et découvrez-le à partir de votre ordinateur de développement.</span><span class="sxs-lookup"><span data-stu-id="18b91-106">Set up your Android device for remote debugging, and discover it from your development machine.</span></span>  
*   <span data-ttu-id="18b91-107">Inspectez et déboguez le contenu en direct sur votre appareil Android à partir de votre ordinateur de développement.</span><span class="sxs-lookup"><span data-stu-id="18b91-107">Inspect and debug live content on your Android device from your development machine.</span></span>  
*   <span data-ttu-id="18b91-108">Contenu Screencast de votre appareil Android sur une instance DevTools sur votre ordinateur de développement.</span><span class="sxs-lookup"><span data-stu-id="18b91-108">Screencast content from your Android device onto a DevTools instance on your development machine.</span></span>  

<!--  
:::image type="complex" source="../media/remote-debugging--remote-debugging.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging--remote-debugging.msft.png":::
   old Figure 1.  Remote Debugging lets you inspect a page running on an Android device from your development machine  
:::image-end:::  
-->  

## <span data-ttu-id="18b91-109">Étape 1: découvrir votre appareil Android</span><span class="sxs-lookup"><span data-stu-id="18b91-109">Step 1: Discover your Android device</span></span>  

<span data-ttu-id="18b91-110">Le flux de travail suivant fonctionne pour la plupart des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="18b91-110">The workflow below works for most users.</span></span>  <span data-ttu-id="18b91-111">Pour plus d’informations, reportez-vous à [la rubrique résolution des problèmes: devtools ne détecte pas l’appareil Android](#troubleshooting-devtools-is-not-detecting-the-android-device) .</span><span class="sxs-lookup"><span data-stu-id="18b91-111">See [Troubleshooting: DevTools is not detecting the Android device](#troubleshooting-devtools-is-not-detecting-the-android-device) for more help.</span></span>  

1.  <span data-ttu-id="18b91-112">Ouvrez l’écran **options de développement** sur votre téléphone Android.</span><span class="sxs-lookup"><span data-stu-id="18b91-112">Open the **Developer Options** screen on your Android.</span></span>  <span data-ttu-id="18b91-113">Pour plus d’informations, reportez-vous à [configurer les options pour les développeurs dans l’appareil](https://developer.android.com/studio/debug/dev-options.html).</span><span class="sxs-lookup"><span data-stu-id="18b91-113">For more information, see [Configure On-Device Developer Options](https://developer.android.com/studio/debug/dev-options.html).</span></span>  
1.  <span data-ttu-id="18b91-114">Sélectionnez **activer le débogage USB**.</span><span class="sxs-lookup"><span data-stu-id="18b91-114">Select **Enable USB Debugging**.</span></span>  
1.  <span data-ttu-id="18b91-115">Sur votre ordinateur de développement, ouvrez Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="18b91-115">On your development machine, open Microsoft Edge.</span></span>  
1.  <span data-ttu-id="18b91-116">Accédez à la `edge://inspect` page dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="18b91-116">Navigate to the `edge://inspect` page in Microsoft Edge.</span></span>  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-no-targets.msft.png" alt-text="Page edge://inspect dans Microsoft Edge" lightbox="../media/remote-debugging-edge-inspect-no-targets.msft.png":::
       <span data-ttu-id="18b91-118">Figure1.</span><span class="sxs-lookup"><span data-stu-id="18b91-118">Figure 1.</span></span>  <span data-ttu-id="18b91-119">`edge://inspect`Page dans Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="18b91-119">The `edge://inspect` page in Microsoft Edge</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="18b91-120">Connectez votre appareil Android directement à votre ordinateur de développement à l’aide d’un câble USB.</span><span class="sxs-lookup"><span data-stu-id="18b91-120">Connect your Android device directly to your development machine using a USB cable.</span></span>  <span data-ttu-id="18b91-121">Lorsque vous tentez de vous connecter pour la première fois, vous êtes généralement invité à DevTools détecter un appareil inconnu.</span><span class="sxs-lookup"><span data-stu-id="18b91-121">The first time you try to connect, you usually see prompt about DevTools detecting an unknown device.</span></span>  <span data-ttu-id="18b91-122">Autorisez l’invite d’autorisation de **débogage USB** sur votre appareil Android.</span><span class="sxs-lookup"><span data-stu-id="18b91-122">Accept the **Allow USB Debugging** permission prompt on your Android device.</span></span>  
    
    :::image type="complex" source="../media/remote-debugging-android-permissions-prompt.msft.png" alt-text="Invite autoriser le débogage USB sur un appareil Android" lightbox="../media/remote-debugging-android-permissions-prompt.msft.png":::
       <span data-ttu-id="18b91-124">Figure2.</span><span class="sxs-lookup"><span data-stu-id="18b91-124">Figure 2.</span></span>  <span data-ttu-id="18b91-125">Invite **autoriser le débogage USB** sur un appareil Android</span><span class="sxs-lookup"><span data-stu-id="18b91-125">The **Allow USB Debugging** permission prompt on an Android device</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="18b91-126">Si vous voyez le nom de modèle de votre appareil Android, Microsoft Edge a correctement établi la connexion à votre appareil.</span><span class="sxs-lookup"><span data-stu-id="18b91-126">If you see the model name of your Android device, then Microsoft Edge has successfully established the connection to your device.</span></span>  <span data-ttu-id="18b91-127">Passez à l' [étape 2](#step-2-debug-content-on-your-android-device-from-your-development-machine).</span><span class="sxs-lookup"><span data-stu-id="18b91-127">Continue to [Step 2](#step-2-debug-content-on-your-android-device-from-your-development-machine).</span></span>  
    
    <!--  
    :::image type="complex" source="../media/remote-debugging--unknown-device.msft.png" alt-text="The Remote Devices tab has successfully detected an unknown device that is pending authorization" lightbox="../media/remote-debugging--unknown-device.msft.png":::
       old Figure 4.  The **Remote Devices** tab has successfully detected an unknown device that is pending authorization  
    :::image-end:::
    -->  
    
### <span data-ttu-id="18b91-128">Résolution des problèmes: DevTools ne détecte pas l’appareil Android</span><span class="sxs-lookup"><span data-stu-id="18b91-128">Troubleshooting: DevTools is not detecting the Android device</span></span>  

<span data-ttu-id="18b91-129">Les conseils suivants vous aideront à résoudre les problèmes liés à la configuration de votre matériel.</span><span class="sxs-lookup"><span data-stu-id="18b91-129">Use the following tips to help you troubleshoot the correct settings for your hardware.</span></span>  

*   <span data-ttu-id="18b91-130">Si vous utilisez un concentrateur USB, essayez de connecter votre appareil Android directement à votre ordinateur de développement.</span><span class="sxs-lookup"><span data-stu-id="18b91-130">If you are using a USB hub, try connecting your Android device directly to your development machine.</span></span>  
*   <span data-ttu-id="18b91-131">Essayez de débrancher le câble USB entre votre appareil et votre machine de développement Android, puis de reconnecter le câble USB.</span><span class="sxs-lookup"><span data-stu-id="18b91-131">Try unplugging the USB cable between your Android device and development machine, and then re-plugging your USB cable.</span></span>  <span data-ttu-id="18b91-132">Terminez la tâche lorsque les écrans de votre ordinateur Android et de développement sont déverrouillés.</span><span class="sxs-lookup"><span data-stu-id="18b91-132">Complete the task while your Android and development machine screens are unlocked.</span></span>  
*   <span data-ttu-id="18b91-133">Assurez-vous que le câble USB fonctionne.</span><span class="sxs-lookup"><span data-stu-id="18b91-133">Make sure that your USB cable works.</span></span>  <span data-ttu-id="18b91-134">Vous devriez être en mesure d’inspecter les fichiers sur votre appareil Android à partir de votre ordinateur de développement.</span><span class="sxs-lookup"><span data-stu-id="18b91-134">You should be able to inspect files on your Android device from your development machine.</span></span>  

<span data-ttu-id="18b91-135">Pour vérifier que votre logiciel est correctement configuré, suivez les conseils ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="18b91-135">Use the following tips to help you verify that your software is set up correctly.</span></span>  

*   <span data-ttu-id="18b91-136">Si votre ordinateur de développement exécute Windows, essayez d’installer manuellement les pilotes USB pour votre appareil Android.</span><span class="sxs-lookup"><span data-stu-id="18b91-136">If your development machine is running Windows, try manually installing the USB drivers for your Android device.</span></span>  <span data-ttu-id="18b91-137">Pour plus d’informations, voir [installer les pilotes USB du fabricant][AndroidUSBDrivers].</span><span class="sxs-lookup"><span data-stu-id="18b91-137">For more information, see [Install OEM USB Drivers][AndroidUSBDrivers].</span></span>  
*   <span data-ttu-id="18b91-138">Quelques combinaisons de périphériques Windows et Android (en particulier Samsung \) requièrent des paramètres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="18b91-138">Some combinations of Windows and Android devices \(especially Samsung\) require additional settings.</span></span>  <span data-ttu-id="18b91-139">Pour plus d’informations, reportez-vous à la section [DevTools appareils ne détecte pas le périphérique connecté] [StackOverflowDevicesNotDetected].</span><span class="sxs-lookup"><span data-stu-id="18b91-139">For more information, see [DevTools Devices does not detect device when plugged in][StackOverflowDevicesNotDetected].</span></span>  

<span data-ttu-id="18b91-140">Pour résoudre les problèmes liés à l’invite de **débogage USB** sur votre appareil Android, suivez les conseils ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="18b91-140">Use the following tips to help you troubleshoot not seeing the **Allow USB Debugging** prompt on your Android device.</span></span>  

*   <span data-ttu-id="18b91-141">En vous déconnectant puis en rouvrant le câble USB alors que DevTools est en focus sur votre ordinateur de développement et votre écran d’accueil Android s’affiche.</span><span class="sxs-lookup"><span data-stu-id="18b91-141">Disconnecting and then re-connecting the USB cable while DevTools is in focus on your development machine and your Android homescreen is showing.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="18b91-142">L’invite risque de ne pas s’afficher si l’écran de votre appareil Android ou de développement est verrouillé.</span><span class="sxs-lookup"><span data-stu-id="18b91-142">You may not see the prompt if your Android or development machine screens are locked.</span></span>  

*   <span data-ttu-id="18b91-143">Mise à jour des paramètres d’affichage de votre appareil et de votre appareil Android de sorte qu’ils ne soient jamais en veille.</span><span class="sxs-lookup"><span data-stu-id="18b91-143">Updating the display settings for your Android device and development machine so that each never goes to sleep.</span></span>  
*   <span data-ttu-id="18b91-144">Définir le mode USB pour Android sur la norme PTP.</span><span class="sxs-lookup"><span data-stu-id="18b91-144">Setting the USB mode for Android to PTP.</span></span>  <span data-ttu-id="18b91-145">Pour plus d’informations, reportez-vous à [la section Galaxy S4 ne pas afficher la boîte de dialogue autoriser le débogage USB][StackExchangeGalaxyS4DoesNotShowDialogBox].</span><span class="sxs-lookup"><span data-stu-id="18b91-145">For more information, see [Galaxy S4 does not show Authorize USB debugging dialog box][StackExchangeGalaxyS4DoesNotShowDialogBox].</span></span>  
*   <span data-ttu-id="18b91-146">Sélectionnez **révoquer les autorisations de débogage USB** à partir de l’écran Options pour les **développeurs** sur votre appareil Android pour rétablir l’état de votre choix.</span><span class="sxs-lookup"><span data-stu-id="18b91-146">Select **Revoke USB Debugging Authorizations** from the **Developer Options** screen on your Android device to reset it to a fresh state.</span></span>  

<span data-ttu-id="18b91-147">Si vous trouvez une solution qui n’est pas mentionnée sur cette page ou dans [DevTools appareils ne détecte aucun appareil lorsque branché] [StackOverflowDevicesNotDetected] en cas de dépassement de pile, ajoutez votre solution à la question de dépassement de pile.</span><span class="sxs-lookup"><span data-stu-id="18b91-147">If you find a solution that is not mentioned on this page or in [DevTools Devices does not detect device when plugged in][StackOverflowDevicesNotDetected] on Stack Overflow, please add your solution to the Stack Overflow question</span></span><!--, or [open an issue in the webfundamentals repository][GitHubWebFundamentalsNewIssue]--><span data-ttu-id="18b91-148">!</span><span class="sxs-lookup"><span data-stu-id="18b91-148">!</span></span>  

## <span data-ttu-id="18b91-149">Étape 2: déboguer du contenu sur votre appareil Android à partir de votre ordinateur de développement</span><span class="sxs-lookup"><span data-stu-id="18b91-149">Step 2: Debug content on your Android device from your development machine</span></span>  

1.  <span data-ttu-id="18b91-150">Ouvrez Microsoft Edge sur votre appareil Android.</span><span class="sxs-lookup"><span data-stu-id="18b91-150">Open Microsoft Edge on your Android device.</span></span>  
1.  <span data-ttu-id="18b91-151">À partir de la `edge://inspect` page, vous pouvez voir le nom du modèle de votre appareil Android, puis le numéro de série de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="18b91-151">From the `edge://inspect` page, you see the model name of your Android device, followed by the device serial number.</span></span>  <span data-ttu-id="18b91-152">En dessous, vous devez voir la version de Microsoft Edge en cours d’exécution sur l’appareil, avec le numéro de version entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="18b91-152">Below that, you should see the version of Microsoft Edge running on the device, with the version number in parentheses.</span></span>  <span data-ttu-id="18b91-153">Chaque onglet Microsoft Edge ouvert obtient une section unique.</span><span class="sxs-lookup"><span data-stu-id="18b91-153">Each open Microsoft Edge tab gets a unique section.</span></span>  <span data-ttu-id="18b91-154">Vous pouvez interagir avec cet onglet à partir d’une section.</span><span class="sxs-lookup"><span data-stu-id="18b91-154">You may interact with that tab from a section.</span></span>  <!--If there are any apps using WebView, you see a section for each of those apps, too.  --><!--In [**Figure 5**](#figure-5) there are no tabs or WebViews open.  -->  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets.msft.png" alt-text="Un appareil distant connecté" lightbox="../media/remote-debugging-edge-inspect-with-targets.msft.png":::
       <span data-ttu-id="18b91-156">Figure3.</span><span class="sxs-lookup"><span data-stu-id="18b91-156">Figure 3.</span></span>  <span data-ttu-id="18b91-157">Un appareil distant connecté</span><span class="sxs-lookup"><span data-stu-id="18b91-157">A connected remote device</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="18b91-158">Dans l' **onglet Ouvrir avec** la zone de texte URL, entrez une URL, puis sélectionnez **ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="18b91-158">In the **Open tab with url** text box, enter a URL and then select **Open**.</span></span>  <span data-ttu-id="18b91-159">La page s’ouvre dans un nouvel onglet sur votre appareil Android.</span><span class="sxs-lookup"><span data-stu-id="18b91-159">The page opens in a new tab on your Android device.</span></span>  
1.  <span data-ttu-id="18b91-160">Sélectionnez **inspecter** en regard de l’URL que vous venez d’ouvrir.</span><span class="sxs-lookup"><span data-stu-id="18b91-160">Select **inspect** next to the URL that you just opened.</span></span>  <span data-ttu-id="18b91-161">Une nouvelle instance de DevTools s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="18b91-161">A new DevTools instance opens.</span></span>  

<!-- The version of Microsoft Edge running on your Android device determines the version of DevTools that opens on your development machine.  
    So, if your Android device is running a very old version of Microsoft Edge, the DevTools instance may look very different than what you are used to.   -->

### <span data-ttu-id="18b91-162">Autres actions: mettre au point, recharger ou fermer un onglet</span><span class="sxs-lookup"><span data-stu-id="18b91-162">More actions: focus, reload, or close a tab</span></span>  

<span data-ttu-id="18b91-163">Sélectionnez l' **onglet Focus**, **Reload**ou **Fermer** en regard de l’onglet que vous voulez mettre au point, recharger ou fermer.</span><span class="sxs-lookup"><span data-stu-id="18b91-163">Select **focus tab**, **reload**, or **close** next to the tab that you want to focus, reload, or close.</span></span>  

:::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png" alt-text="Boutons de focalisation, de rechargement et de fermeture d’un onglet" lightbox="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png":::
   <span data-ttu-id="18b91-165">Figure4.</span><span class="sxs-lookup"><span data-stu-id="18b91-165">Figure 4.</span></span>  <span data-ttu-id="18b91-166">Boutons de focalisation, de rechargement et de fermeture d’un onglet</span><span class="sxs-lookup"><span data-stu-id="18b91-166">The buttons for focusing, reloading, or closing a tab</span></span>  
:::image-end:::  

### <span data-ttu-id="18b91-167">Inspecter les éléments</span><span class="sxs-lookup"><span data-stu-id="18b91-167">Inspect elements</span></span>  

<span data-ttu-id="18b91-168">Accédez au panneau **éléments** de votre instance devtools, puis pointez sur un élément pour le mettre en surbrillance dans la fenêtre d’affichage de votre appareil Android.</span><span class="sxs-lookup"><span data-stu-id="18b91-168">Go to the **Elements** panel of your DevTools instance, and hover over an element to highlight it in the viewport of your Android device.</span></span>  

<span data-ttu-id="18b91-169">Vous pouvez également sélectionner un élément sur l’écran de votre appareil Android pour le sélectionner dans le panneau **éléments** .</span><span class="sxs-lookup"><span data-stu-id="18b91-169">You may also select an element on your Android device screen to select it in the **Elements** panel.</span></span>  <span data-ttu-id="18b91-170">Sélectionnez **Select Element** ![ l’icône sélectionner un élément ][ImageSelectElementIcon] de votre instance devtools, puis sélectionnez l’élément sur l’écran de votre appareil Android.</span><span class="sxs-lookup"><span data-stu-id="18b91-170">Select **Select Element** ![Select Element][ImageSelectElementIcon] icon on your DevTools instance, and then select the element on your Android device screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="18b91-171">**Sélectionner l’élément** est désactivé après la première sélection; vous devez donc le réactiver chaque fois que vous souhaitez utiliser la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="18b91-171">**Select Element** is disabled after the first selection, so you must re-enable it every time you want to use the feature.</span></span>  

### <span data-ttu-id="18b91-172">Capturez l’écran de votre téléphone Android sur votre ordinateur de développement.</span><span class="sxs-lookup"><span data-stu-id="18b91-172">Screencast your Android screen to your development machine</span></span>  

<span data-ttu-id="18b91-173">**Toggle Screencast** ![ ][ImageToggleScreencastIcon] Pour afficher le contenu de votre appareil Android dans votre instance devtools, sélectionnez l’icône d’activation/désactivation de la capture d’écran.</span><span class="sxs-lookup"><span data-stu-id="18b91-173">Select **Toggle Screencast** ![Toggle Screencast][ImageToggleScreencastIcon] icon to view the content of your Android device in your DevTools instance.</span></span>  

<span data-ttu-id="18b91-174">Vous pouvez interagir avec la capture vidéo de l’une des manières suivantes.</span><span class="sxs-lookup"><span data-stu-id="18b91-174">You are able to interact with the screencast in the following ways.</span></span>  

*   <span data-ttu-id="18b91-175">Les clics sont convertis en pressions et déclenchent les événements d’effleurement appropriés sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="18b91-175">Clicks are translated into taps, firing proper touch events on the device.</span></span>  
*   <span data-ttu-id="18b91-176">Les séquences de touches de votre ordinateur sont envoyées à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="18b91-176">Keystrokes on your computer are sent to the device.</span></span>  
*   <span data-ttu-id="18b91-177">Pour simuler un mouvement de pincement, maintenez la touche enfoncée `Shift` pendant que vous faites glisser.</span><span class="sxs-lookup"><span data-stu-id="18b91-177">To simulate a pinch gesture, hold `Shift` while dragging.</span></span>  
*   <span data-ttu-id="18b91-178">Pour faire défiler, utilisez votre pavé tactile ou votre volant de souris, ou glissement rapide avec le pointeur de la souris.</span><span class="sxs-lookup"><span data-stu-id="18b91-178">To scroll, use your trackpad or mouse wheel, or fling with your mouse pointer.</span></span>

> [!NOTE]
> <span data-ttu-id="18b91-179">Pour plus d’informations, suivez les conseils ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="18b91-179">Use the following tips to help you screencast.</span></span>  
> 
> *   <span data-ttu-id="18b91-180">Les screencasts affichent uniquement le contenu de la page.</span><span class="sxs-lookup"><span data-stu-id="18b91-180">Screencasts only display page content.</span></span>  <span data-ttu-id="18b91-181">Les parties transparentes de l’enregistrement vidéo représentent des interfaces de périphériques, comme la barre d’adresses Microsoft Edge, la barre d’État Android ou le clavier Android.</span><span class="sxs-lookup"><span data-stu-id="18b91-181">Transparent portions of the screencast represent device interfaces, such as the Microsoft Edge address bar, the Android status bar, or the Android keyboard.</span></span>  
> *   <span data-ttu-id="18b91-182">Les screencasts ont un impact négatif sur les taux d’images.</span><span class="sxs-lookup"><span data-stu-id="18b91-182">Screencasts negatively affect frame rates.</span></span>  <span data-ttu-id="18b91-183">Désactivez la capture d’images lors du mesurage des défilement ou des animations pour obtenir une image plus précise des performances de votre page.</span><span class="sxs-lookup"><span data-stu-id="18b91-183">Disable screencasting while measuring scrolls or animations to get a more accurate picture of the performance of your page.</span></span>  
> *   <span data-ttu-id="18b91-184">Si l’écran de votre appareil Android est verrouillé, le contenu de votre screencast disparaît.</span><span class="sxs-lookup"><span data-stu-id="18b91-184">If your Android device screen locks, the content of your screencast disappears.</span></span>  <span data-ttu-id="18b91-185">Déverrouillez l’écran de votre appareil Android pour la reprise automatique.</span><span class="sxs-lookup"><span data-stu-id="18b91-185">Unlock your Android device screen to automatically resume the screencast.</span></span>  

<!-- image links -->  

[ImageSelectElementIcon]: /microsoft-edge/devtools-guide-chromium/media/select-element-icon.msft.png  
[ImageToggleScreencastIcon]: /microsoft-edge/devtools-guide-chromium/media/toggle-screencast-icon.msft.png  

<!--[ImageRemoteDebugging]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging--remote-debugging.msft.png "old Figure 1:  Remote Debugging lets you inspect a page running on an Android device from your development machine"  -->  
<!--[ImageEdgeInspect]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-edge-inspect-no-targets.msft.png "Figure 1: The edge://inspect page in Microsoft Edge"  -->  
<!--[ImageAndroidPermissionPrompt]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-android-permissions-prompt.msft.png "Figure 2: The Allow USB Debugging permission prompt on an Android device"  -->  
<!--[ImageConnectedRemoteDevice]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-edge-inspect-with-targets.msft.png "Figure 3: A connected remote device"  -->  
<!-- [ImageReload]:  /microsoft-edge/devtools-guide-chromium/media/remote-debugging-edge-inspect-with-targets-buttons.msft.png "Figure 4: The buttons for focusing, reloading, or closing a tab"  -->  
<!--[ImageUnknownDevice]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging--unknown-device.msft.png "old Figure 4:  The Remote Devices tab has successfully detected an unknown device that is pending authorization"  -->  

<!-- links -->  

[AndroidUSBDrivers]: https://developer.android.com/tools/extras/oem-usb.html "Installer les pilotes USB OEM | Développeurs Android"  

<!-- [GitHubWebFundamentalsNewIssue]: https://github.com/Alphabet/webfundamentals/issues/new?title=[Remote%20Debugging] "GitHub - Web Fundamentals - New Issue"  -->  
[StackOverflowDevicesNotDetected]: https://stackoverflow.com/questions/21925992 «les appareils devtools ne détectent pas l’appareil en cas de dépassement de la pile connectée»  

[StackExchangeGalaxyS4DoesNotShowDialogBox]: https://android.stackexchange.com/questions/101933 "ADB: échange d’une pile enthousiaste pour Android"  

> [!NOTE]
> <span data-ttu-id="18b91-189">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="18b91-189">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="18b91-190">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="18b91-190">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="18b91-192">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="18b91-192">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
