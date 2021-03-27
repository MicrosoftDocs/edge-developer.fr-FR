---
description: Débogage à distance du contenu en direct sur un appareil Android à partir d’un ordinateur Windows ou macOS.
title: Prise en main du débogage à distance des appareils Android
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/25/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: d69fd4832991826c76f47daea399bdd89e981bb4
ms.sourcegitcommit: bff24ab1f0a66aaf4c7f5ff81cea3eb28c6d8380
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/26/2021
ms.locfileid: "11461212"
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
# <a name="get-started-with-remote-debugging-android-devices"></a><span data-ttu-id="6f50a-104">Prise en main du débogage à distance des appareils Android</span><span class="sxs-lookup"><span data-stu-id="6f50a-104">Get started with remote debugging Android devices</span></span>  

<span data-ttu-id="6f50a-105">Déboguer à distance du contenu en direct sur un appareil Android à partir de votre ordinateur Windows ou macOS.</span><span class="sxs-lookup"><span data-stu-id="6f50a-105">Remote debug live content on an Android device from your Windows or macOS computer.</span></span>  <span data-ttu-id="6f50a-106">La page de didacticiel suivante vous apprend à effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="6f50a-106">The following tutorial page teaches you how to complete the following actions.</span></span>  

*   <span data-ttu-id="6f50a-107">Configurer votre appareil Android pour le débogage à distance et le découvrir à partir de votre ordinateur de développement.</span><span class="sxs-lookup"><span data-stu-id="6f50a-107">Set up your Android device for remote debugging, and discover it from your development machine.</span></span>  
*   <span data-ttu-id="6f50a-108">Inspectez et déboguer le contenu en direct sur votre appareil Android à partir de votre ordinateur de développement.</span><span class="sxs-lookup"><span data-stu-id="6f50a-108">Inspect and debug live content on your Android device from your development machine.</span></span>  
*   <span data-ttu-id="6f50a-109">Capture vidéo du contenu de votre appareil Android sur une instance DevTools sur votre ordinateur de développement.</span><span class="sxs-lookup"><span data-stu-id="6f50a-109">Screencast content from your Android device onto a DevTools instance on your development machine.</span></span>  

<!--  
:::image type="complex" source="../media/remote-debugging--remote-debugging.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging--remote-debugging.msft.png":::
   old Figure 1.  Remote Debugging lets you inspect a page running on an Android device from your development machine  
:::image-end:::  
-->  

> [!NOTE]
> <span data-ttu-id="6f50a-110">Le débogage à distance de l’application Microsoft Edge sur les appareils iOS n’est actuellement pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="6f50a-110">Remote debugging the Microsoft Edge app on iOS devices is not currently supported.</span></span>  <span data-ttu-id="6f50a-111">Le guide suivant est spécifiquement axé sur le débogage à distance de Microsoft Edge sur les appareils Android.</span><span class="sxs-lookup"><span data-stu-id="6f50a-111">The following guide is specifically focused on remote debugging Microsoft Edge on Android devices.</span></span>
> <span data-ttu-id="6f50a-112">Si vous avez un appareil macOS, suivez le guide de [débogage Brightcove][BrightcoveSupportDebuggingMobileDevices] pour déboguer Microsoft Edge à distance sur un appareil iOS à l’aide de Safari.</span><span class="sxs-lookup"><span data-stu-id="6f50a-112">If you have a macOS device, follow the [Brightcove Debugging guide][BrightcoveSupportDebuggingMobileDevices] to remotely debug Microsoft Edge on an iOS device using Safari.</span></span>  <span data-ttu-id="6f50a-113">Pour plus d’informations sur l’outil Inspecteur web dans Safari, accédez à [Safari Web Development Tools][AppleDeveloperSafariTools].</span><span class="sxs-lookup"><span data-stu-id="6f50a-113">For more information about the Web Inspector tool in Safari, navigate to [Safari Web Development Tools][AppleDeveloperSafariTools].</span></span>  

## <a name="step-1-discover-your-android-device"></a><span data-ttu-id="6f50a-114">Étape 1 : Découvrir votre appareil Android</span><span class="sxs-lookup"><span data-stu-id="6f50a-114">Step 1: Discover your Android device</span></span>  

<span data-ttu-id="6f50a-115">Le flux de travail ci-dessous fonctionne pour la plupart des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="6f50a-115">The workflow below works for most users.</span></span>  <span data-ttu-id="6f50a-116">Pour plus d’aide, accédez à Résolution des problèmes [: DevTools](#troubleshooting-devtools-is-not-detecting-the-android-device) ne détecte pas la section d’appareil Android.</span><span class="sxs-lookup"><span data-stu-id="6f50a-116">For more help, navigate to [Troubleshooting: DevTools is not detecting the Android device](#troubleshooting-devtools-is-not-detecting-the-android-device) section.</span></span>  

1.  <span data-ttu-id="6f50a-117">Ouvrez **l’écran Options du** développeur sur votre android.</span><span class="sxs-lookup"><span data-stu-id="6f50a-117">Open the **Developer Options** screen on your Android.</span></span>  <span data-ttu-id="6f50a-118">Pour plus d’informations, [accédez à Configurer les options du développeur sur appareil.][AndroidDeveloperStudioDevOptions]</span><span class="sxs-lookup"><span data-stu-id="6f50a-118">For more information, navigate to [Configure On-Device Developer Options][AndroidDeveloperStudioDevOptions].</span></span>  
1.  <span data-ttu-id="6f50a-119">Choisissez **Activer le débogage USB.**</span><span class="sxs-lookup"><span data-stu-id="6f50a-119">Choose **Enable USB Debugging**.</span></span>  
1.  <span data-ttu-id="6f50a-120">Sur votre ordinateur de développement, ouvrez Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6f50a-120">On your development machine, open Microsoft Edge.</span></span>  
1.  <span data-ttu-id="6f50a-121">Accédez à `edge://inspect` la page dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6f50a-121">Navigate to the `edge://inspect` page in Microsoft Edge.</span></span>  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-no-targets.msft.png" alt-text="Page de edge://inspect dans Microsoft Edge" lightbox="../media/remote-debugging-edge-inspect-no-targets.msft.png":::
       <span data-ttu-id="6f50a-123">Figure1.</span><span class="sxs-lookup"><span data-stu-id="6f50a-123">Figure 1.</span></span>  <span data-ttu-id="6f50a-124">Page `edge://inspect` dans Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="6f50a-124">The `edge://inspect` page in Microsoft Edge</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="6f50a-125">Connectez votre appareil Android directement à votre ordinateur de développement à l’aide d’un câble USB.</span><span class="sxs-lookup"><span data-stu-id="6f50a-125">Connect your Android device directly to your development machine using a USB cable.</span></span>  <span data-ttu-id="6f50a-126">La première fois que vous essayez de vous connecter, une invite doit s’afficher sur DevTools détectant un appareil inconnu.</span><span class="sxs-lookup"><span data-stu-id="6f50a-126">The first time you try to connect, a prompt should be displayed about DevTools detecting an unknown device.</span></span>  <span data-ttu-id="6f50a-127">Acceptez **l’invite d’autorisation Autoriser le débogage USB** sur votre appareil Android.</span><span class="sxs-lookup"><span data-stu-id="6f50a-127">Accept the **Allow USB Debugging** permission prompt on your Android device.</span></span>  
    
    :::image type="complex" source="../media/remote-debugging-android-permissions-prompt.msft.png" alt-text="Invite d’autorisation Autoriser le débogage USB sur un appareil Android" lightbox="../media/remote-debugging-android-permissions-prompt.msft.png":::
       <span data-ttu-id="6f50a-129">Figure2.</span><span class="sxs-lookup"><span data-stu-id="6f50a-129">Figure 2.</span></span>  <span data-ttu-id="6f50a-130">Invite **d’autorisation Autoriser le débogage USB** sur un appareil Android</span><span class="sxs-lookup"><span data-stu-id="6f50a-130">The **Allow USB Debugging** permission prompt on an Android device</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="6f50a-131">Si le nom de modèle de votre appareil Android est affiché, Microsoft Edge a correctement établi la connexion à votre appareil.</span><span class="sxs-lookup"><span data-stu-id="6f50a-131">If the model name of your Android device is displayed, then Microsoft Edge has successfully established the connection to your device.</span></span>  <span data-ttu-id="6f50a-132">Continuez [jusqu’à la section Étape 2.](#step-2-debug-content-on-your-android-device-from-your-development-machine)</span><span class="sxs-lookup"><span data-stu-id="6f50a-132">Continue to the [Step 2](#step-2-debug-content-on-your-android-device-from-your-development-machine) section.</span></span>  
    
    <!--  
    :::image type="complex" source="../media/remote-debugging--unknown-device.msft.png" alt-text="The Remote Devices tab has successfully detected an unknown device that is pending authorization" lightbox="../media/remote-debugging--unknown-device.msft.png":::
       old Figure 4.  The **Remote Devices** tab has successfully detected an unknown device that is pending authorization  
    :::image-end:::
    -->  
    
### <a name="troubleshooting-devtools-is-not-detecting-the-android-device"></a><span data-ttu-id="6f50a-133">Résolution des problèmes : DevTools ne détecte pas l’appareil Android</span><span class="sxs-lookup"><span data-stu-id="6f50a-133">Troubleshooting: DevTools is not detecting the Android device</span></span>  

<span data-ttu-id="6f50a-134">Utilisez les conseils suivants pour vous aider à résoudre les problèmes de paramètres corrects pour votre matériel.</span><span class="sxs-lookup"><span data-stu-id="6f50a-134">Use the following tips to help you troubleshoot the correct settings for your hardware.</span></span>  

*   <span data-ttu-id="6f50a-135">Si vous utilisez un concentrateur USB, essayez de connecter votre appareil Android directement à votre ordinateur de développement.</span><span class="sxs-lookup"><span data-stu-id="6f50a-135">If you are using a USB hub, try connecting your Android device directly to your development machine.</span></span>  
*   <span data-ttu-id="6f50a-136">Essayez de débrancher le câble USB entre votre appareil Android et votre ordinateur de développement, puis de le brancher à nouveau.</span><span class="sxs-lookup"><span data-stu-id="6f50a-136">Try unplugging the USB cable between your Android device and development machine, and then re-plugging your USB cable.</span></span>  <span data-ttu-id="6f50a-137">Terminez la tâche pendant que vos écrans d’ordinateur android et de développement sont déverrouillés.</span><span class="sxs-lookup"><span data-stu-id="6f50a-137">Complete the task while your Android and development machine screens are unlocked.</span></span>  
*   <span data-ttu-id="6f50a-138">Assurez-vous que votre câble USB fonctionne.</span><span class="sxs-lookup"><span data-stu-id="6f50a-138">Make sure that your USB cable works.</span></span>  <span data-ttu-id="6f50a-139">Vous devriez être en mesure d’inspecter les fichiers sur votre appareil Android à partir de votre ordinateur de développement.</span><span class="sxs-lookup"><span data-stu-id="6f50a-139">You should be able to inspect files on your Android device from your development machine.</span></span>  

<span data-ttu-id="6f50a-140">Utilisez les conseils suivants pour vérifier que votre logiciel est correctement installé.</span><span class="sxs-lookup"><span data-stu-id="6f50a-140">Use the following tips to help you verify that your software is set up correctly.</span></span>  

*   <span data-ttu-id="6f50a-141">Si votre ordinateur de développement exécute Windows, essayez d’installer manuellement les pilotes USB de votre appareil Android.</span><span class="sxs-lookup"><span data-stu-id="6f50a-141">If your development machine is running Windows, try manually installing the USB drivers for your Android device.</span></span>  <span data-ttu-id="6f50a-142">Pour plus d’informations, [accédez à Installer des pilotes USB OEM.][AndroidDeveloperToolsOemUsb]</span><span class="sxs-lookup"><span data-stu-id="6f50a-142">For more information, navigate to [Install OEM USB Drivers][AndroidDeveloperToolsOemUsb].</span></span>  
*   <span data-ttu-id="6f50a-143">Certaines combinaisons d’appareils Windows et Android \(notamment Samsung\) nécessitent des paramètres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="6f50a-143">Some combinations of Windows and Android devices \(especially Samsung\) require additional settings.</span></span>  <span data-ttu-id="6f50a-144">Pour plus d’informations, accédez [à DevTools Devices does not detect device when plugged in][Stackoverflow21925992].</span><span class="sxs-lookup"><span data-stu-id="6f50a-144">For more information, navigate to [DevTools Devices does not detect device when plugged in][Stackoverflow21925992].</span></span>  

<span data-ttu-id="6f50a-145">Utilisez les conseils suivants pour vous aider à résoudre les problèmes si l’invite Autoriser le **débogage USB** n’est pas affichée sur votre appareil Android.</span><span class="sxs-lookup"><span data-stu-id="6f50a-145">Use the following tips to help you troubleshoot if the **Allow USB Debugging** prompt is not displayed on your Android device.</span></span>  

*   <span data-ttu-id="6f50a-146">Déconnexion, puis nouvelle connexion du câble USB pendant que DevTools est en focus sur votre ordinateur de développement et que votre écran d’accueil Android s’affiche.</span><span class="sxs-lookup"><span data-stu-id="6f50a-146">Disconnecting and then re-connecting the USB cable while DevTools is in focus on your development machine and your Android homescreen is showing.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="6f50a-147">L’invite s’affiche si vos écrans d’ordinateur Android ou de développement sont verrouillés.</span><span class="sxs-lookup"><span data-stu-id="6f50a-147">The prompt is displayed if your Android or development machine screens are locked.</span></span>  

*   <span data-ttu-id="6f50a-148">Mise à jour des paramètres d’affichage de votre appareil Android et de votre ordinateur de développement afin que chacun ne soit jamais mis en veille.</span><span class="sxs-lookup"><span data-stu-id="6f50a-148">Updating the display settings for your Android device and development machine so that each never goes to sleep.</span></span>  
*   <span data-ttu-id="6f50a-149">Définition du mode USB pour Android sur PTP.</span><span class="sxs-lookup"><span data-stu-id="6f50a-149">Setting the USB mode for Android to PTP.</span></span>  <span data-ttu-id="6f50a-150">Pour plus d’informations, accédez à La boîte de dialogue Autoriser le débogage USB n’apparaît pas dans La boîte de dialogue Autoriser le [débogage USB.][StackexchangeAndroid101933]</span><span class="sxs-lookup"><span data-stu-id="6f50a-150">For more information, navigate to [Galaxy S4 does not show Authorize USB debugging dialog box][StackexchangeAndroid101933].</span></span>  
*   <span data-ttu-id="6f50a-151">Choose **Revoke USB Debugging Authorizations** from the **Developer Options** screen on your Android device to reset it to a fresh state.</span><span class="sxs-lookup"><span data-stu-id="6f50a-151">Choose **Revoke USB Debugging Authorizations** from the **Developer Options** screen on your Android device to reset it to a fresh state.</span></span>  

<span data-ttu-id="6f50a-152">Si vous trouvez une solution qui n’est pas mentionnée sur cette page ou dans [DevTools Devices][Stackoverflow21925992] ne détecte pas l’appareil lorsqu’il est branché sur Stack Overflow, ajoutez votre solution à la question Stack Overflow.</span><span class="sxs-lookup"><span data-stu-id="6f50a-152">If you find a solution that is not mentioned on this page or in [DevTools Devices does not detect device when plugged in][Stackoverflow21925992] on Stack Overflow, please add your solution to the Stack Overflow question</span></span><!--, or [open an issue in the webfundamentals repository][GitHubWebFundamentalsNewIssue]--><span data-ttu-id="6f50a-153">.</span><span class="sxs-lookup"><span data-stu-id="6f50a-153">.</span></span>  

## <a name="step-2-debug-content-on-your-android-device-from-your-development-machine"></a><span data-ttu-id="6f50a-154">Étape 2 : Déboguer le contenu de votre appareil Android à partir de votre ordinateur de développement</span><span class="sxs-lookup"><span data-stu-id="6f50a-154">Step 2: Debug content on your Android device from your development machine</span></span>  

1.  <span data-ttu-id="6f50a-155">Ouvrez Microsoft Edge sur votre appareil Android.</span><span class="sxs-lookup"><span data-stu-id="6f50a-155">Open Microsoft Edge on your Android device.</span></span>  
1.  <span data-ttu-id="6f50a-156">Accédez `edge://inspect` à , le nom de modèle de votre appareil Android s’affiche, suivi du numéro de série de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6f50a-156">Navigate to `edge://inspect`, the model name of your Android device is displayed, followed by the device serial number.</span></span>  <span data-ttu-id="6f50a-157">En dessous de cela, la version de Microsoft Edge en cours d’exécution sur l’appareil doit être affichée, avec le numéro de version entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="6f50a-157">Below that, the version of Microsoft Edge running on the device should be displayed, with the version number in parentheses.</span></span>  <span data-ttu-id="6f50a-158">Chaque onglet Microsoft Edge ouvert obtient une section unique.</span><span class="sxs-lookup"><span data-stu-id="6f50a-158">Each open Microsoft Edge tab gets a unique section.</span></span>  <span data-ttu-id="6f50a-159">Vous pouvez interagir avec cet onglet à partir d’une section.</span><span class="sxs-lookup"><span data-stu-id="6f50a-159">You may interact with that tab from a section.</span></span>  <!--If there are any apps using WebView, a section for each of those apps should be displayed, too.  --><!--In [**Figure 5**](#figure-5) there are no tabs or WebViews open.  -->  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets.msft.png" alt-text="Un appareil distant connecté" lightbox="../media/remote-debugging-edge-inspect-with-targets.msft.png":::
       <span data-ttu-id="6f50a-161">Figure3.</span><span class="sxs-lookup"><span data-stu-id="6f50a-161">Figure 3.</span></span>  <span data-ttu-id="6f50a-162">Un appareil distant connecté</span><span class="sxs-lookup"><span data-stu-id="6f50a-162">A connected remote device</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="6f50a-163">Dans **l’onglet Ouvrir avec une zone** de texte d’URL, entrez une URL, puis choisissez **Ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="6f50a-163">In the **Open tab with url** text box, enter a URL and then choose **Open**.</span></span>  <span data-ttu-id="6f50a-164">La page s’ouvre dans un nouvel onglet sur votre appareil Android.</span><span class="sxs-lookup"><span data-stu-id="6f50a-164">The page opens in a new tab on your Android device.</span></span>  
1.  <span data-ttu-id="6f50a-165">Sélectionnez **Inspecter** en côté de l’URL que vous ouvrez.</span><span class="sxs-lookup"><span data-stu-id="6f50a-165">Choose **inspect** next to the URL that you just opened.</span></span>  <span data-ttu-id="6f50a-166">Une nouvelle instance DevTools s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="6f50a-166">A new DevTools instance opens.</span></span>  

<!-- The version of Microsoft Edge running on your Android device determines the version of DevTools that opens on your development machine.  
    So, if your Android device is running a very old version of Microsoft Edge, the DevTools instance may look very different than what you are used to.   -->

### <a name="more-actions-focus-refresh-or-close-a-tab"></a><span data-ttu-id="6f50a-167">Autres actions : mise au point, actualisation ou fermeture d’un onglet</span><span class="sxs-lookup"><span data-stu-id="6f50a-167">More actions: focus, refresh, or close a tab</span></span>  

<span data-ttu-id="6f50a-168">Choisissez **l’onglet Focus,** **rechargez**ou fermez-le à côté de l’onglet que vous souhaitez mettre au point, actualiser ou fermer. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="6f50a-168">Choose **focus tab**, **reload**, or **close** next to the tab that you want to focus, refresh, or close.</span></span>  

:::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png" alt-text="Boutons de mise au point, d’actualisation ou de fermeture d’un onglet" lightbox="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png":::
   <span data-ttu-id="6f50a-170">Figure4.</span><span class="sxs-lookup"><span data-stu-id="6f50a-170">Figure 4.</span></span>  <span data-ttu-id="6f50a-171">Boutons de mise au point, d’actualisation ou de fermeture d’un onglet</span><span class="sxs-lookup"><span data-stu-id="6f50a-171">The buttons for focusing, refreshing, or closing a tab</span></span>  
:::image-end:::  

### <a name="inspect-elements"></a><span data-ttu-id="6f50a-172">Inspecter les éléments</span><span class="sxs-lookup"><span data-stu-id="6f50a-172">Inspect elements</span></span>  

<span data-ttu-id="6f50a-173">Accédez à **l’outil Elements** de votre instance DevTools, puis pointez sur un élément pour le mettre en surbrillation dans laport d’affichage de votre appareil Android.</span><span class="sxs-lookup"><span data-stu-id="6f50a-173">Navigate to the **Elements** tool of your DevTools instance, and hover on an element to highlight it in the viewport of your Android device.</span></span>  

<span data-ttu-id="6f50a-174">Vous pouvez également sélectionner un élément sur l’écran de votre appareil Android pour le sélectionner dans **l’outil Éléments.**</span><span class="sxs-lookup"><span data-stu-id="6f50a-174">You may also select an element on your Android device screen to select it in the **Elements** tool.</span></span>  <span data-ttu-id="6f50a-175">Sélectionnez **l’icône** Select Element \( Select Element \) sur votre ![ instance DevTools, puis sélectionnez l’élément sur l’écran de ](../media/select-element-icon.msft.png) votre appareil Android.</span><span class="sxs-lookup"><span data-stu-id="6f50a-175">Choose **Select Element** \(![Select Element](../media/select-element-icon.msft.png)\) icon on your DevTools instance, and then select the element on your Android device screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="6f50a-176">**Select Element** est désactivé après la première sélection. Vous devez donc le réactiver chaque fois que vous souhaitez utiliser la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="6f50a-176">**Select Element** is disabled after the first selection, so you must re-enable it every time you want to use the feature.</span></span>  

### <a name="screencast-your-android-screen-to-your-development-machine"></a><span data-ttu-id="6f50a-177">Capture d’écran de votre écran Android sur votre ordinateur de développement</span><span class="sxs-lookup"><span data-stu-id="6f50a-177">Screencast your Android screen to your development machine</span></span>  

<span data-ttu-id="6f50a-178">Choisissez **l’icône Deggle Screencast** \( Toggle Screencast \) pour afficher le contenu de votre appareil Android dans votre ![ instance ](../media/toggle-screencast-icon.msft.png) DevTools.</span><span class="sxs-lookup"><span data-stu-id="6f50a-178">Choose **Toggle Screencast** \(![Toggle Screencast](../media/toggle-screencast-icon.msft.png)\) icon to view the content of your Android device in your DevTools instance.</span></span>  

<span data-ttu-id="6f50a-179">Vous pouvez interagir avec la capture vidéo des manières suivantes.</span><span class="sxs-lookup"><span data-stu-id="6f50a-179">You are able to interact with the screencast in the following ways.</span></span>  

*   <span data-ttu-id="6f50a-180">Les choix sont convertis en pressions, ce qui permet de tirer les événements tactiles appropriés sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6f50a-180">Chooses are translated into taps, firing proper touch events on the device.</span></span>  
*   <span data-ttu-id="6f50a-181">Les frappes de touches sur votre ordinateur sont envoyées à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6f50a-181">Keystrokes on your computer are sent to the device.</span></span>  
*   <span data-ttu-id="6f50a-182">Pour simuler un mouvement de pincement, maintenez le doigt `Shift` en cours de glissement.</span><span class="sxs-lookup"><span data-stu-id="6f50a-182">To simulate a pinch gesture, hold `Shift` while dragging.</span></span>  
*   <span data-ttu-id="6f50a-183">Pour faire défiler la souris, utilisez votre trackpad ou votre roulette de souris, ou fling avec votre pointeur de souris.</span><span class="sxs-lookup"><span data-stu-id="6f50a-183">To scroll, use your trackpad or mouse wheel, or fling with your mouse pointer.</span></span>

> [!NOTE]
> <span data-ttu-id="6f50a-184">Utilisez les conseils suivants pour vous aider à faire une capture vidéo.</span><span class="sxs-lookup"><span data-stu-id="6f50a-184">Use the following tips to help you screencast.</span></span>  
> 
> *   <span data-ttu-id="6f50a-185">Les captures d’écran affichent uniquement le contenu de la page.</span><span class="sxs-lookup"><span data-stu-id="6f50a-185">Screencasts only display page content.</span></span>  <span data-ttu-id="6f50a-186">Les parties transparentes de la capture vidéo représentent des interfaces d’appareil, telles que la barre d’adresses Microsoft Edge, la barre d’état Android ou le clavier Android.</span><span class="sxs-lookup"><span data-stu-id="6f50a-186">Transparent portions of the screencast represent device interfaces, such as the Microsoft Edge address bar, the Android status bar, or the Android keyboard.</span></span>  
> *   <span data-ttu-id="6f50a-187">Les captures vidéo affectent négativement les taux d’images.</span><span class="sxs-lookup"><span data-stu-id="6f50a-187">Screencasts negatively affect frame rates.</span></span>  <span data-ttu-id="6f50a-188">Désactivez la capture vidéo lors de la mesure des défilements ou des animations pour obtenir une image plus précise des performances de votre page.</span><span class="sxs-lookup"><span data-stu-id="6f50a-188">Disable screencasting while measuring scrolls or animations to get a more accurate picture of the performance of your page.</span></span>  
> *   <span data-ttu-id="6f50a-189">Si l’écran de votre appareil Android se verrouille, le contenu de votre capture vidéo disparaît.</span><span class="sxs-lookup"><span data-stu-id="6f50a-189">If your Android device screen locks, the content of your screencast disappears.</span></span>  <span data-ttu-id="6f50a-190">Déverrouillez l’écran de votre appareil Android pour reprendre automatiquement la capture vidéo.</span><span class="sxs-lookup"><span data-stu-id="6f50a-190">Unlock your Android device screen to automatically resume the screencast.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="6f50a-191">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="6f50a-191">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[AndroidDeveloperStudioDevOptions]: https://developer.android.com/studio/debug/dev-options "Configurer les options du développeur sur l’appareil | Développeur Android"  
[AndroidDeveloperToolsOemUsb]: https://developer.android.com/tools/extras/oem-usb.html "Installer les pilotes USB OEM | Développeurs Android"  

[AppleDeveloperSafariTools]: https://developer.apple.com/safari/tools "Outils de développement web Safari | Développeur Apple"  

[BrightcoveSupportDebuggingMobileDevices]: https://support.brightcove.com/debugging-mobile-devices "Débogage sur les appareils mobiles | Prise en charge de Brightcove"  

<!-- [GitHubWebFundamentalsNewIssue]: https://github.com/Alphabet/webfundamentals/issues/new?title=[Remote%20Debugging] "GitHub - Web Fundamentals - New Issue"  -->  

[StackexchangeAndroid101933]: https://android.stackexchange.com/questions/101933 "adb - Android Enthusiast Stack Exchange"  

[Stackoverflow21925992]: https://stackoverflow.com/questions/21925992 "DevTools Devices does not detect device when plugged in - Stack Overflow"  

> [!NOTE]
> <span data-ttu-id="6f50a-198">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6f50a-198">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="6f50a-199">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="6f50a-199">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="6f50a-201">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6f50a-201">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
