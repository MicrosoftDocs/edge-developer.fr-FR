---
description: Déboguez à distance le contenu en direct sur un appareil Android à partir d’un ordinateur Windows ou macOS.
title: Découvrir les appareils Android de débogage à distance
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: c6bdb48460fb8f6ff26cbb02872e33cb50dd6e12
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125362"
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

# <span data-ttu-id="ccc49-104">Découvrir les appareils Android de débogage à distance</span><span class="sxs-lookup"><span data-stu-id="ccc49-104">Get started with remote debugging Android devices</span></span>  

<span data-ttu-id="ccc49-105">Déboguez à distance le contenu en direct sur un appareil Android à partir de votre ordinateur Windows ou macOS.</span><span class="sxs-lookup"><span data-stu-id="ccc49-105">Remote debug live content on an Android device from your Windows or macOS computer.</span></span>  <span data-ttu-id="ccc49-106">La page du didacticiel suivante vous explique comment effectuer les opérations suivantes.</span><span class="sxs-lookup"><span data-stu-id="ccc49-106">The following tutorial page teaches you how to complete the following actions.</span></span>  

*   <span data-ttu-id="ccc49-107">Configurez votre appareil Android pour le débogage à distance et découvrez-le à partir de votre ordinateur de développement.</span><span class="sxs-lookup"><span data-stu-id="ccc49-107">Set up your Android device for remote debugging, and discover it from your development machine.</span></span>  
*   <span data-ttu-id="ccc49-108">Inspectez et déboguez le contenu en direct sur votre appareil Android à partir de votre ordinateur de développement.</span><span class="sxs-lookup"><span data-stu-id="ccc49-108">Inspect and debug live content on your Android device from your development machine.</span></span>  
*   <span data-ttu-id="ccc49-109">Contenu Screencast de votre appareil Android sur une instance DevTools sur votre ordinateur de développement.</span><span class="sxs-lookup"><span data-stu-id="ccc49-109">Screencast content from your Android device onto a DevTools instance on your development machine.</span></span>  

<!--  
:::image type="complex" source="../media/remote-debugging--remote-debugging.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging--remote-debugging.msft.png":::
   old Figure 1.  Remote Debugging lets you inspect a page running on an Android device from your development machine  
:::image-end:::  
-->  

> [!NOTE]
> <span data-ttu-id="ccc49-110">Le débogage à distance de l’application Microsoft Edge sur les appareils iOS n’est pas pris en charge pour le moment.</span><span class="sxs-lookup"><span data-stu-id="ccc49-110">Remote debugging the Microsoft Edge app on iOS devices is not currently supported.</span></span>  <span data-ttu-id="ccc49-111">Le guide suivant est particulièrement axé sur le débogage à distance de Microsoft Edge sur les appareils Android.</span><span class="sxs-lookup"><span data-stu-id="ccc49-111">The following guide is specifically focused on remote debugging Microsoft Edge on Android devices.</span></span>
> <span data-ttu-id="ccc49-112">Si vous avez un appareil macOS, suivez le [Guide de débogage de Brightcove][BrightcoveSupportDebuggingMobileDevices] pour déboguer à distance Microsoft Edge sur un appareil iOS à l’aide de Safari.</span><span class="sxs-lookup"><span data-stu-id="ccc49-112">If you have a macOS device, follow the [Brightcove Debugging guide][BrightcoveSupportDebuggingMobileDevices] to remotely debug Microsoft Edge on an iOS device using Safari.</span></span>  <span data-ttu-id="ccc49-113">Pour plus d’informations sur l’outil inspecteur Web dans Safari, accédez à [outils de développement Web Safari][AppleDeveloperSafariTools].</span><span class="sxs-lookup"><span data-stu-id="ccc49-113">For more information about the Web Inspector tool in Safari, navigate to [Safari Web Development Tools][AppleDeveloperSafariTools].</span></span>  

## <span data-ttu-id="ccc49-114">Étape 1: découvrir votre appareil Android</span><span class="sxs-lookup"><span data-stu-id="ccc49-114">Step 1: Discover your Android device</span></span>  

<span data-ttu-id="ccc49-115">Le flux de travail suivant fonctionne pour la plupart des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="ccc49-115">The workflow below works for most users.</span></span>  <span data-ttu-id="ccc49-116">Pour obtenir de l’aide, accédez à [résolution des problèmes: devtools ne détecte pas la section appareil Android](#troubleshooting-devtools-is-not-detecting-the-android-device) .</span><span class="sxs-lookup"><span data-stu-id="ccc49-116">For more help, navigate to [Troubleshooting: DevTools is not detecting the Android device](#troubleshooting-devtools-is-not-detecting-the-android-device) section.</span></span>  

1.  <span data-ttu-id="ccc49-117">Ouvrez l’écran **options de développement** sur votre téléphone Android.</span><span class="sxs-lookup"><span data-stu-id="ccc49-117">Open the **Developer Options** screen on your Android.</span></span>  <span data-ttu-id="ccc49-118">Pour plus d’informations, accédez à [configurer les options pour les développeurs dans l’appareil][AndroidDeveloperStudioDevOptions].</span><span class="sxs-lookup"><span data-stu-id="ccc49-118">For more information, navigate to [Configure On-Device Developer Options][AndroidDeveloperStudioDevOptions].</span></span>  
1.  <span data-ttu-id="ccc49-119">Sélectionnez **activer le débogage USB**.</span><span class="sxs-lookup"><span data-stu-id="ccc49-119">Choose **Enable USB Debugging**.</span></span>  
1.  <span data-ttu-id="ccc49-120">Sur votre ordinateur de développement, ouvrez Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ccc49-120">On your development machine, open Microsoft Edge.</span></span>  
1.  <span data-ttu-id="ccc49-121">Accédez à la `edge://inspect` page dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ccc49-121">Navigate to the `edge://inspect` page in Microsoft Edge.</span></span>  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-no-targets.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging-edge-inspect-no-targets.msft.png":::
       <span data-ttu-id="ccc49-123">Figure1.</span><span class="sxs-lookup"><span data-stu-id="ccc49-123">Figure 1.</span></span>  <span data-ttu-id="ccc49-124">`edge://inspect`Page dans Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ccc49-124">The `edge://inspect` page in Microsoft Edge</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ccc49-125">Connectez votre appareil Android directement à votre ordinateur de développement à l’aide d’un câble USB.</span><span class="sxs-lookup"><span data-stu-id="ccc49-125">Connect your Android device directly to your development machine using a USB cable.</span></span>  <span data-ttu-id="ccc49-126">La première fois que vous essayez de vous connecter, une invite s’affiche à propos de DevTools détection d’un périphérique inconnu.</span><span class="sxs-lookup"><span data-stu-id="ccc49-126">The first time you try to connect, a prompt should be displayed about DevTools detecting an unknown device.</span></span>  <span data-ttu-id="ccc49-127">Autorisez l’invite d’autorisation de **débogage USB** sur votre appareil Android.</span><span class="sxs-lookup"><span data-stu-id="ccc49-127">Accept the **Allow USB Debugging** permission prompt on your Android device.</span></span>  
    
    :::image type="complex" source="../media/remote-debugging-android-permissions-prompt.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging-android-permissions-prompt.msft.png":::
       <span data-ttu-id="ccc49-129">Figure2.</span><span class="sxs-lookup"><span data-stu-id="ccc49-129">Figure 2.</span></span>  <span data-ttu-id="ccc49-130">Invite **autoriser le débogage USB** sur un appareil Android</span><span class="sxs-lookup"><span data-stu-id="ccc49-130">The **Allow USB Debugging** permission prompt on an Android device</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ccc49-131">Si le nom de modèle de votre appareil Android est affiché, Microsoft Edge a correctement établi la connexion à votre appareil.</span><span class="sxs-lookup"><span data-stu-id="ccc49-131">If the model name of your Android device is displayed, then Microsoft Edge has successfully established the connection to your device.</span></span>  <span data-ttu-id="ccc49-132">Passez à la section [étape 2](#step-2-debug-content-on-your-android-device-from-your-development-machine) .</span><span class="sxs-lookup"><span data-stu-id="ccc49-132">Continue to the [Step 2](#step-2-debug-content-on-your-android-device-from-your-development-machine) section.</span></span>  
    
    <!--  
    :::image type="complex" source="../media/remote-debugging--unknown-device.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging--unknown-device.msft.png":::
       old Figure 4.  The **Remote Devices** tab has successfully detected an unknown device that is pending authorization  
    :::image-end:::
    -->  
    
### <span data-ttu-id="ccc49-133">Résolution des problèmes: DevTools ne détecte pas l’appareil Android</span><span class="sxs-lookup"><span data-stu-id="ccc49-133">Troubleshooting: DevTools is not detecting the Android device</span></span>  

<span data-ttu-id="ccc49-134">Les conseils suivants vous aideront à résoudre les problèmes liés à la configuration de votre matériel.</span><span class="sxs-lookup"><span data-stu-id="ccc49-134">Use the following tips to help you troubleshoot the correct settings for your hardware.</span></span>  

*   <span data-ttu-id="ccc49-135">Si vous utilisez un concentrateur USB, essayez de connecter votre appareil Android directement à votre ordinateur de développement.</span><span class="sxs-lookup"><span data-stu-id="ccc49-135">If you are using a USB hub, try connecting your Android device directly to your development machine.</span></span>  
*   <span data-ttu-id="ccc49-136">Essayez de débrancher le câble USB entre votre appareil et votre machine de développement Android, puis de reconnecter le câble USB.</span><span class="sxs-lookup"><span data-stu-id="ccc49-136">Try unplugging the USB cable between your Android device and development machine, and then re-plugging your USB cable.</span></span>  <span data-ttu-id="ccc49-137">Terminez la tâche lorsque les écrans de votre ordinateur Android et de développement sont déverrouillés.</span><span class="sxs-lookup"><span data-stu-id="ccc49-137">Complete the task while your Android and development machine screens are unlocked.</span></span>  
*   <span data-ttu-id="ccc49-138">Assurez-vous que le câble USB fonctionne.</span><span class="sxs-lookup"><span data-stu-id="ccc49-138">Make sure that your USB cable works.</span></span>  <span data-ttu-id="ccc49-139">Vous devriez être en mesure d’inspecter les fichiers sur votre appareil Android à partir de votre ordinateur de développement.</span><span class="sxs-lookup"><span data-stu-id="ccc49-139">You should be able to inspect files on your Android device from your development machine.</span></span>  

<span data-ttu-id="ccc49-140">Pour vérifier que votre logiciel est correctement configuré, suivez les conseils ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="ccc49-140">Use the following tips to help you verify that your software is set up correctly.</span></span>  

*   <span data-ttu-id="ccc49-141">Si votre ordinateur de développement exécute Windows, essayez d’installer manuellement les pilotes USB pour votre appareil Android.</span><span class="sxs-lookup"><span data-stu-id="ccc49-141">If your development machine is running Windows, try manually installing the USB drivers for your Android device.</span></span>  <span data-ttu-id="ccc49-142">Pour plus d’informations, accédez à [installer les pilotes USB du fabricant][AndroidDeveloperToolsOemUsb].</span><span class="sxs-lookup"><span data-stu-id="ccc49-142">For more information, navigate to [Install OEM USB Drivers][AndroidDeveloperToolsOemUsb].</span></span>  
*   <span data-ttu-id="ccc49-143">Quelques combinaisons de périphériques Windows et Android (en particulier Samsung \) requièrent des paramètres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="ccc49-143">Some combinations of Windows and Android devices \(especially Samsung\) require additional settings.</span></span>  <span data-ttu-id="ccc49-144">Pour plus d’informations, accédez à [devtools périphériques ne détecte pas le périphérique en cas de branchement][Stackoverflow21925992].</span><span class="sxs-lookup"><span data-stu-id="ccc49-144">For more information, navigate to [DevTools Devices does not detect device when plugged in][Stackoverflow21925992].</span></span>  

<span data-ttu-id="ccc49-145">Appliquez les conseils suivants pour vous aider à résoudre les problèmes d’affichage de l’invite de **débogage USB** sur votre appareil Android.</span><span class="sxs-lookup"><span data-stu-id="ccc49-145">Use the following tips to help you troubleshoot if the **Allow USB Debugging** prompt is not displayed on your Android device.</span></span>  

*   <span data-ttu-id="ccc49-146">En vous déconnectant puis en rouvrant le câble USB alors que DevTools est en focus sur votre ordinateur de développement et votre écran d’accueil Android s’affiche.</span><span class="sxs-lookup"><span data-stu-id="ccc49-146">Disconnecting and then re-connecting the USB cable while DevTools is in focus on your development machine and your Android homescreen is showing.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="ccc49-147">L’invite s’affiche si les écrans de votre ordinateur Android ou de développement sont verrouillés.</span><span class="sxs-lookup"><span data-stu-id="ccc49-147">The prompt is displayed if your Android or development machine screens are locked.</span></span>  

*   <span data-ttu-id="ccc49-148">Mise à jour des paramètres d’affichage de votre appareil et de votre appareil Android de sorte qu’ils ne soient jamais en veille.</span><span class="sxs-lookup"><span data-stu-id="ccc49-148">Updating the display settings for your Android device and development machine so that each never goes to sleep.</span></span>  
*   <span data-ttu-id="ccc49-149">Définir le mode USB pour Android sur la norme PTP.</span><span class="sxs-lookup"><span data-stu-id="ccc49-149">Setting the USB mode for Android to PTP.</span></span>  <span data-ttu-id="ccc49-150">Pour plus d’informations, accédez à [la boîte de dialogue autoriser le débogage USB ne s’affiche pas dans Galaxy S4][StackexchangeAndroid101933].</span><span class="sxs-lookup"><span data-stu-id="ccc49-150">For more information, navigate to [Galaxy S4 does not show Authorize USB debugging dialog box][StackexchangeAndroid101933].</span></span>  
*   <span data-ttu-id="ccc49-151">Sélectionnez **révoquer les autorisations de débogage USB** dans l’écran Options pour les **développeurs** de votre appareil Android pour le rétablir à un état frais.</span><span class="sxs-lookup"><span data-stu-id="ccc49-151">Choose **Revoke USB Debugging Authorizations** from the **Developer Options** screen on your Android device to reset it to a fresh state.</span></span>  

<span data-ttu-id="ccc49-152">Si vous trouvez une solution qui n’est pas mentionnée sur cette page ou dans devtools appareils, la détection de l' [appareil n’est pas détectée lors][Stackoverflow21925992] du dépassement de capacité de la pile.</span><span class="sxs-lookup"><span data-stu-id="ccc49-152">If you find a solution that is not mentioned on this page or in [DevTools Devices does not detect device when plugged in][Stackoverflow21925992] on Stack Overflow, please add your solution to the Stack Overflow question</span></span><!--, or [open an issue in the webfundamentals repository][GitHubWebFundamentalsNewIssue]--><span data-ttu-id="ccc49-153">!</span><span class="sxs-lookup"><span data-stu-id="ccc49-153">!</span></span>  

## <span data-ttu-id="ccc49-154">Étape 2: déboguer du contenu sur votre appareil Android à partir de votre ordinateur de développement</span><span class="sxs-lookup"><span data-stu-id="ccc49-154">Step 2: Debug content on your Android device from your development machine</span></span>  

1.  <span data-ttu-id="ccc49-155">Ouvrez Microsoft Edge sur votre appareil Android.</span><span class="sxs-lookup"><span data-stu-id="ccc49-155">Open Microsoft Edge on your Android device.</span></span>  
1.  <span data-ttu-id="ccc49-156">Accédez au `edge://inspect` nom de modèle de votre appareil Android qui s’affiche, suivi du numéro de série de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ccc49-156">Navigate to `edge://inspect`, the model name of your Android device is displayed, followed by the device serial number.</span></span>  <span data-ttu-id="ccc49-157">En dessous, la version de Microsoft Edge qui s’exécute sur l’appareil doit être affichée, avec le numéro de version entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="ccc49-157">Below that, the version of Microsoft Edge running on the device should be displayed, with the version number in parentheses.</span></span>  <span data-ttu-id="ccc49-158">Chaque onglet Microsoft Edge ouvert obtient une section unique.</span><span class="sxs-lookup"><span data-stu-id="ccc49-158">Each open Microsoft Edge tab gets a unique section.</span></span>  <span data-ttu-id="ccc49-159">Vous pouvez interagir avec cet onglet à partir d’une section.</span><span class="sxs-lookup"><span data-stu-id="ccc49-159">You may interact with that tab from a section.</span></span>  <!--If there are any apps using WebView, a section for each of those apps should be displayed, too.  --><!--In [**Figure 5**](#figure-5) there are no tabs or WebViews open.  -->  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging-edge-inspect-with-targets.msft.png":::
       <span data-ttu-id="ccc49-161">Figure3.</span><span class="sxs-lookup"><span data-stu-id="ccc49-161">Figure 3.</span></span>  <span data-ttu-id="ccc49-162">Un appareil distant connecté</span><span class="sxs-lookup"><span data-stu-id="ccc49-162">A connected remote device</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ccc49-163">Dans l' **onglet Ouvrir avec** la zone de texte URL, entrez une URL, puis choisissez **ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="ccc49-163">In the **Open tab with url** text box, enter a URL and then choose **Open**.</span></span>  <span data-ttu-id="ccc49-164">La page s’ouvre dans un nouvel onglet sur votre appareil Android.</span><span class="sxs-lookup"><span data-stu-id="ccc49-164">The page opens in a new tab on your Android device.</span></span>  
1.  <span data-ttu-id="ccc49-165">Sélectionnez **inspecter** en regard de l’URL que vous venez d’ouvrir.</span><span class="sxs-lookup"><span data-stu-id="ccc49-165">Choose **inspect** next to the URL that you just opened.</span></span>  <span data-ttu-id="ccc49-166">Une nouvelle instance de DevTools s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="ccc49-166">A new DevTools instance opens.</span></span>  

<!-- The version of Microsoft Edge running on your Android device determines the version of DevTools that opens on your development machine.  
    So, if your Android device is running a very old version of Microsoft Edge, the DevTools instance may look very different than what you are used to.   -->

### <span data-ttu-id="ccc49-167">Autres actions: mettre au point, recharger ou fermer un onglet</span><span class="sxs-lookup"><span data-stu-id="ccc49-167">More actions: focus, reload, or close a tab</span></span>  

<span data-ttu-id="ccc49-168">Sélectionnez l' **onglet Focus**, **Reload**ou **Fermer** en regard de l’onglet que vous voulez mettre au point, recharger ou fermer.</span><span class="sxs-lookup"><span data-stu-id="ccc49-168">Choose **focus tab**, **reload**, or **close** next to the tab that you want to focus, reload, or close.</span></span>  

:::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png":::
   <span data-ttu-id="ccc49-170">Figure4.</span><span class="sxs-lookup"><span data-stu-id="ccc49-170">Figure 4.</span></span>  <span data-ttu-id="ccc49-171">Boutons de focalisation, de rechargement et de fermeture d’un onglet</span><span class="sxs-lookup"><span data-stu-id="ccc49-171">The buttons for focusing, reloading, or closing a tab</span></span>  
:::image-end:::  

### <span data-ttu-id="ccc49-172">Inspecter les éléments</span><span class="sxs-lookup"><span data-stu-id="ccc49-172">Inspect elements</span></span>  

<span data-ttu-id="ccc49-173">Accédez au panneau **éléments** de votre instance devtools, puis pointez sur un élément pour le mettre en surbrillance dans la fenêtre d’affichage de votre appareil Android.</span><span class="sxs-lookup"><span data-stu-id="ccc49-173">Go to the **Elements** panel of your DevTools instance, and hover over an element to highlight it in the viewport of your Android device.</span></span>  

<span data-ttu-id="ccc49-174">Vous pouvez également sélectionner un élément sur l’écran de votre appareil Android pour le sélectionner dans le panneau **éléments** .</span><span class="sxs-lookup"><span data-stu-id="ccc49-174">You may also select an element on your Android device screen to select it in the **Elements** panel.</span></span>  <span data-ttu-id="ccc49-175">Sélectionnez l’icône **Sélectionner l’élément** \ ( ![ Sélectionner l’élément ][ImageSelectElementIcon] \) dans votre instance devtools, puis sélectionnez l’élément sur l’écran de votre appareil Android.</span><span class="sxs-lookup"><span data-stu-id="ccc49-175">Choose **Select Element** \(![Select Element][ImageSelectElementIcon]\) icon on your DevTools instance, and then select the element on your Android device screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="ccc49-176">**Sélectionner l’élément** est désactivé après la première sélection; vous devez donc le réactiver chaque fois que vous souhaitez utiliser la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="ccc49-176">**Select Element** is disabled after the first selection, so you must re-enable it every time you want to use the feature.</span></span>  

### <span data-ttu-id="ccc49-177">Capturez l’écran de votre téléphone Android sur votre ordinateur de développement.</span><span class="sxs-lookup"><span data-stu-id="ccc49-177">Screencast your Android screen to your development machine</span></span>  

<span data-ttu-id="ccc49-178">**Toggle Screencast** ![ ][ImageToggleScreencastIcon] Pour afficher le contenu de votre appareil Android dans votre instance devtools, sélectionnez l’icône activer/désactiver la vidéo.</span><span class="sxs-lookup"><span data-stu-id="ccc49-178">Choose **Toggle Screencast** \(![Toggle Screencast][ImageToggleScreencastIcon]\) icon to view the content of your Android device in your DevTools instance.</span></span>  

<span data-ttu-id="ccc49-179">Vous pouvez interagir avec la capture vidéo de l’une des manières suivantes.</span><span class="sxs-lookup"><span data-stu-id="ccc49-179">You are able to interact with the screencast in the following ways.</span></span>  

*   <span data-ttu-id="ccc49-180">Les clics sont convertis en pressions et déclenchent les événements d’effleurement appropriés sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ccc49-180">Clicks are translated into taps, firing proper touch events on the device.</span></span>  
*   <span data-ttu-id="ccc49-181">Les séquences de touches de votre ordinateur sont envoyées à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ccc49-181">Keystrokes on your computer are sent to the device.</span></span>  
*   <span data-ttu-id="ccc49-182">Pour simuler un mouvement de pincement, maintenez la touche enfoncée `Shift` pendant que vous faites glisser.</span><span class="sxs-lookup"><span data-stu-id="ccc49-182">To simulate a pinch gesture, hold `Shift` while dragging.</span></span>  
*   <span data-ttu-id="ccc49-183">Pour faire défiler, utilisez votre pavé tactile ou votre volant de souris, ou glissement rapide avec le pointeur de la souris.</span><span class="sxs-lookup"><span data-stu-id="ccc49-183">To scroll, use your trackpad or mouse wheel, or fling with your mouse pointer.</span></span>

> [!NOTE]
> <span data-ttu-id="ccc49-184">Pour plus d’informations, suivez les conseils ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="ccc49-184">Use the following tips to help you screencast.</span></span>  
> 
> *   <span data-ttu-id="ccc49-185">Les screencasts affichent uniquement le contenu de la page.</span><span class="sxs-lookup"><span data-stu-id="ccc49-185">Screencasts only display page content.</span></span>  <span data-ttu-id="ccc49-186">Les parties transparentes de l’enregistrement vidéo représentent des interfaces de périphériques, comme la barre d’adresses Microsoft Edge, la barre d’État Android ou le clavier Android.</span><span class="sxs-lookup"><span data-stu-id="ccc49-186">Transparent portions of the screencast represent device interfaces, such as the Microsoft Edge address bar, the Android status bar, or the Android keyboard.</span></span>  
> *   <span data-ttu-id="ccc49-187">Les screencasts ont un impact négatif sur les taux d’images.</span><span class="sxs-lookup"><span data-stu-id="ccc49-187">Screencasts negatively affect frame rates.</span></span>  <span data-ttu-id="ccc49-188">Désactivez la capture d’images lors du mesurage des défilement ou des animations pour obtenir une image plus précise des performances de votre page.</span><span class="sxs-lookup"><span data-stu-id="ccc49-188">Disable screencasting while measuring scrolls or animations to get a more accurate picture of the performance of your page.</span></span>  
> *   <span data-ttu-id="ccc49-189">Si l’écran de votre appareil Android est verrouillé, le contenu de votre screencast disparaît.</span><span class="sxs-lookup"><span data-stu-id="ccc49-189">If your Android device screen locks, the content of your screencast disappears.</span></span>  <span data-ttu-id="ccc49-190">Déverrouillez l’écran de votre appareil Android pour la reprise automatique.</span><span class="sxs-lookup"><span data-stu-id="ccc49-190">Unlock your Android device screen to automatically resume the screencast.</span></span>  

## <span data-ttu-id="ccc49-191">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="ccc49-191">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageSelectElementIcon]: /microsoft-edge/devtools-guide-chromium/media/select-element-icon.msft.png  
[ImageToggleScreencastIcon]: /microsoft-edge/devtools-guide-chromium/media/toggle-screencast-icon.msft.png  

<!-- links -->  

[AndroidDeveloperStudioDevOptions]: https://developer.android.com/studio/debug/dev-options "Configurer les options pour les développeurs sur un appareil Développeur pour Android"  
[AndroidDeveloperToolsOemUsb]: https://developer.android.com/tools/extras/oem-usb.html "Installer les pilotes USB OEM | Développeurs Android"  

[AppleDeveloperSafariTools]: https://developer.apple.com/safari/tools "Outils de développement Web Safari | Développeur Apple"  

[BrightcoveSupportDebuggingMobileDevices]: https://support.brightcove.com/debugging-mobile-devices "Débogage sur les appareils mobiles | Support Brightcove"  

<!-- [GitHubWebFundamentalsNewIssue]: https://github.com/Alphabet/webfundamentals/issues/new?title=[Remote%20Debugging] "GitHub - Web Fundamentals - New Issue"  -->  

[StackexchangeAndroid101933]: https://android.stackexchange.com/questions/101933 "ADB: échange d’une pile enthousiaste pour Android"  

[Stackoverflow21925992]: https://stackoverflow.com/questions/21925992 "DevToolsx XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX"  

> [!NOTE]
> <span data-ttu-id="ccc49-198">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ccc49-198">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="ccc49-199">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="ccc49-199">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="ccc49-201">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ccc49-201">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
