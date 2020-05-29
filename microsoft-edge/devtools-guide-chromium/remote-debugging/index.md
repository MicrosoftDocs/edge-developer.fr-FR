---
title: Découvrir les appareils Android de débogage à distance
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: a9002ca82e6e0dcaf7f174b336e5c640929a561b
ms.sourcegitcommit: 33663cd7838dddee86228dde469a5e9551bddb02
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611818"
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




<!--
<style>
.devtools-inline {
  max-height: 1em;
  vertical-align: middle;
}
</style>
-->  
# <span data-ttu-id="75481-103">Découvrir les appareils Android de débogage à distance</span><span class="sxs-lookup"><span data-stu-id="75481-103">Get Started with Remote Debugging Android Devices</span></span>   



<span data-ttu-id="75481-104">Déboguez à distance le contenu en direct sur un appareil Android à partir de votre ordinateur Windows ou macOS.</span><span class="sxs-lookup"><span data-stu-id="75481-104">Remote debug live content on an Android device from your Windows or macOS computer.</span></span>  <span data-ttu-id="75481-105">Ce didacticiel vous explique comment:</span><span class="sxs-lookup"><span data-stu-id="75481-105">This tutorial teaches you how to:</span></span>  

*   <span data-ttu-id="75481-106">Configurez votre appareil Android pour le débogage à distance et découvrez-le à partir de votre ordinateur de développement.</span><span class="sxs-lookup"><span data-stu-id="75481-106">Set up your Android device for remote debugging, and discover it from your development machine.</span></span>  
*   <span data-ttu-id="75481-107">Inspectez et déboguez le contenu en direct sur votre appareil Android à partir de votre ordinateur de développement.</span><span class="sxs-lookup"><span data-stu-id="75481-107">Inspect and debug live content on your Android device from your development machine.</span></span>  
*   <span data-ttu-id="75481-108">Contenu Screencast de votre appareil Android sur une instance DevTools sur votre ordinateur de développement.</span><span class="sxs-lookup"><span data-stu-id="75481-108">Screencast content from your Android device onto a DevTools instance on your development machine.</span></span>  

<!--
> ##### Figure 1  
> Remote Debugging lets you inspect a page running on an Android device from your development machine  
> ![Remote Debugging lets you inspect a page running on an Android device from your development machine][ImageRemoteDebugging]  -->

## <span data-ttu-id="75481-109">Étape 1: découvrir votre appareil Android</span><span class="sxs-lookup"><span data-stu-id="75481-109">Step 1: Discover your Android device</span></span>   

<span data-ttu-id="75481-110">Le flux de travail suivant fonctionne pour la plupart des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="75481-110">The workflow below works for most users.</span></span>  <span data-ttu-id="75481-111">Pour plus d’informations, reportez-vous à [la rubrique résolution des problèmes: devtools ne détecte pas l’appareil Android](#troubleshooting-devtools-is-not-detecting-the-android-device) .</span><span class="sxs-lookup"><span data-stu-id="75481-111">See [Troubleshooting: DevTools is not detecting the Android device](#troubleshooting-devtools-is-not-detecting-the-android-device) for more help.</span></span>  

1.  <span data-ttu-id="75481-112">Ouvrez l’écran **options de développement** sur votre téléphone Android.</span><span class="sxs-lookup"><span data-stu-id="75481-112">Open the **Developer Options** screen on your Android.</span></span>  <span data-ttu-id="75481-113">Voir [configurer les options pour les développeurs sur un appareil](https://developer.android.com/studio/debug/dev-options.html).</span><span class="sxs-lookup"><span data-stu-id="75481-113">See [Configure On-Device Developer Options](https://developer.android.com/studio/debug/dev-options.html).</span></span>  
1.  <span data-ttu-id="75481-114">Sélectionnez **activer le débogage USB**.</span><span class="sxs-lookup"><span data-stu-id="75481-114">Select **Enable USB Debugging**.</span></span>  
1.  <span data-ttu-id="75481-115">Sur votre ordinateur de développement, ouvrez Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="75481-115">On your development machine, open Microsoft Edge.</span></span>  
1.  <span data-ttu-id="75481-116">[Ouvrez devtools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="75481-116">[Open DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="75481-117">Dans devtools, sélectionnez le **menu principal** , `...` puis sélectionnez **plus d’outils**  >  **distants de périphériques distants**.</span><span class="sxs-lookup"><span data-stu-id="75481-117">In DevTools, select the **Main Menu** `...` then select **More tools** > **Remote devices**.</span></span>  
    
    > ##### <span data-ttu-id="75481-118">Figure1</span><span class="sxs-lookup"><span data-stu-id="75481-118">Figure 1</span></span>  
    > <span data-ttu-id="75481-119">Ouverture de l’onglet **équipements distants** par le biais du **menu principal**</span><span class="sxs-lookup"><span data-stu-id="75481-119">Opening the **Remote Devices** tab via the **Main Menu**</span></span>  
    > <span data-ttu-id="75481-120">! [Ouverture de l’onglet équipements distants par le biais du menu principal] [ImageOpenRemoteDevices]</span><span class="sxs-lookup"><span data-stu-id="75481-120">![Opening the Remote Devices tab via the Main Menu][ImageOpenRemoteDevices]</span></span>  

1.  <span data-ttu-id="75481-121">Dans DevTools, ouvrez l’onglet **paramètres** .</span><span class="sxs-lookup"><span data-stu-id="75481-121">In DevTools, open the **Settings** tab.</span></span>  

1.  <span data-ttu-id="75481-122">Vérifiez que la case **détecter les périphériques USB** est activée.</span><span class="sxs-lookup"><span data-stu-id="75481-122">Make sure that the **Discover USB devices** checkbox is enabled.</span></span>  
    
    > ##### <span data-ttu-id="75481-123">Figure 2</span><span class="sxs-lookup"><span data-stu-id="75481-123">Figure 2</span></span>  
    > <span data-ttu-id="75481-124">La case **détecter les périphériques USB** est activée</span><span class="sxs-lookup"><span data-stu-id="75481-124">The **Discover USB Devices** checkbox is enabled</span></span>  
    > <span data-ttu-id="75481-125">! [La case détecter les périphériques USB est activée] [ImageDiscoverUSBDevices]</span><span class="sxs-lookup"><span data-stu-id="75481-125">![The Discover USB Devices checkbox is enabled][ImageDiscoverUSBDevices]</span></span>  

1.  <span data-ttu-id="75481-126">Connectez votre appareil Android directement à votre ordinateur de développement à l’aide d’un câble USB.</span><span class="sxs-lookup"><span data-stu-id="75481-126">Connect your Android device directly to your development machine using a USB cable.</span></span>  <span data-ttu-id="75481-127">La première fois que vous effectuez cette opération, vous observez généralement que DevTools a détecté un appareil inconnu.</span><span class="sxs-lookup"><span data-stu-id="75481-127">The first time you do this, you usually see that DevTools has detected an unknown device.</span></span>  <span data-ttu-id="75481-128">Si vous voyez un point vert et le texte **connecté** sous le nom de modèle de votre appareil Android, devtools a correctement établi la connexion à votre appareil.</span><span class="sxs-lookup"><span data-stu-id="75481-128">If you see a green dot and the text **Connected** below the model name of your Android device, then DevTools has successfully established the connection to your device.</span></span>  <span data-ttu-id="75481-129">Passez à l' [étape 2](#step-2-debug-content-on-your-android-device-from-your-development-machine).</span><span class="sxs-lookup"><span data-stu-id="75481-129">Continue to [Step 2](#step-2-debug-content-on-your-android-device-from-your-development-machine).</span></span>  
    <!--
    > ##### Figure 4  
    > The **Remote Devices** tab has successfully detected an unknown device that is pending authorization  
    > ![The Remote Devices tab has successfully detected an unknown device that is pending authorization][ImageUnknownDevice]  -->

1.  <span data-ttu-id="75481-130">Si votre appareil s’affiche comme **inconnu**, acceptez l’invite d’autorisation de **débogage USB** sur votre appareil Android.</span><span class="sxs-lookup"><span data-stu-id="75481-130">If your device is showing up as **Unknown**, accept the **Allow USB Debugging** permission prompt on your Android device.</span></span>  

### <span data-ttu-id="75481-131">Résolution des problèmes: DevTools ne détecte pas l’appareil Android</span><span class="sxs-lookup"><span data-stu-id="75481-131">Troubleshooting: DevTools is not detecting the Android device</span></span>   

<span data-ttu-id="75481-132">Assurez-vous que votre matériel est correctement configuré:</span><span class="sxs-lookup"><span data-stu-id="75481-132">Make sure that your hardware is set up correctly:</span></span>  

*   <span data-ttu-id="75481-133">Si vous utilisez un concentrateur USB, essayez plutôt de connecter votre appareil Android directement à votre ordinateur de développement.</span><span class="sxs-lookup"><span data-stu-id="75481-133">If you are using a USB hub, try connecting your Android device directly to your development machine instead.</span></span>  
*   <span data-ttu-id="75481-134">Essayez de débrancher le câble USB de votre appareil et de votre ordinateur de développement Android, puis de le réactiver.</span><span class="sxs-lookup"><span data-stu-id="75481-134">Try unplugging the USB cable between your Android device and development machine, and then plugging it back in.</span></span>  <span data-ttu-id="75481-135">Faites-le pendant que vos écrans d’appareil Android et de développement sont déverrouillés.</span><span class="sxs-lookup"><span data-stu-id="75481-135">Do it while your Android and development machine screens are unlocked.</span></span>  
*   <span data-ttu-id="75481-136">Assurez-vous que le câble USB fonctionne.</span><span class="sxs-lookup"><span data-stu-id="75481-136">Make sure that your USB cable works.</span></span>  <span data-ttu-id="75481-137">Vous devriez être en mesure d’inspecter les fichiers sur votre appareil Android à partir de votre ordinateur de développement.</span><span class="sxs-lookup"><span data-stu-id="75481-137">You should be able to inspect files on your Android device from your development machine.</span></span>  

<span data-ttu-id="75481-138">Assurez-vous que votre logiciel est correctement configuré:</span><span class="sxs-lookup"><span data-stu-id="75481-138">Make sure that your software is set up correctly:</span></span>  

*   <span data-ttu-id="75481-139">Si votre ordinateur de développement exécute Windows, essayez d’installer manuellement les pilotes USB pour votre appareil Android.</span><span class="sxs-lookup"><span data-stu-id="75481-139">If your development machine is running Windows, try manually installing the USB drivers for your Android device.</span></span>  <span data-ttu-id="75481-140">Voir [installer les pilotes USB OEM][AndroidUSBDrivers].</span><span class="sxs-lookup"><span data-stu-id="75481-140">See [Install OEM USB Drivers][AndroidUSBDrivers].</span></span>  
    
*   <span data-ttu-id="75481-141">Quelques combinaisons de périphériques Windows et Android (en particulier, Samsung) nécessitent une configuration supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="75481-141">Some combinations of Windows and Android devices (especially Samsung) require extra set up.</span></span>  <span data-ttu-id="75481-142">Reportez-vous à la section [DevTools appareils ne détecte pas le périphérique connecté] [StackOverflowDevicesNotDetected].</span><span class="sxs-lookup"><span data-stu-id="75481-142">See [DevTools Devices does not detect device when plugged in][StackOverflowDevicesNotDetected].</span></span>  
    
<span data-ttu-id="75481-143">Si vous ne voyez pas l’invite **autoriser le débogage USB** sur votre appareil Android, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="75481-143">If you do not see the **Allow USB Debugging** prompt on your Android device try:</span></span>  

*   <span data-ttu-id="75481-144">En vous déconnectant puis en rouvrant le câble USB alors que DevTools est en focus sur votre ordinateur de développement et votre écran d’accueil Android s’affiche.</span><span class="sxs-lookup"><span data-stu-id="75481-144">Disconnecting and then re-connecting the USB cable while DevTools is in focus on your development machine and your Android homescreen is showing.</span></span>  <span data-ttu-id="75481-145">En d’autres termes, il est possible que l’invite ne s’affiche pas lorsque les écrans de votre ordinateur Android ou de développement sont verrouillés.</span><span class="sxs-lookup"><span data-stu-id="75481-145">In other words, sometimes the prompt does not show up when your Android or development machine screens are locked.</span></span>
*   <span data-ttu-id="75481-146">Mise à jour des paramètres d’affichage de votre appareil et de votre ordinateur de développement Android pour qu’ils ne soient jamais en veille.</span><span class="sxs-lookup"><span data-stu-id="75481-146">Updating the display settings for your Android device and development machine so that they never go to sleep.</span></span>  
*   <span data-ttu-id="75481-147">Définir le mode USB pour Android sur la norme PTP.</span><span class="sxs-lookup"><span data-stu-id="75481-147">Setting the USB mode for Android to PTP.</span></span>  <span data-ttu-id="75481-148">Reportez-vous à [la section Galaxy S4 ne pas afficher la boîte de dialogue autoriser le débogage USB][StackExchangeGalaxyS4DoesNotShowDialogBox].</span><span class="sxs-lookup"><span data-stu-id="75481-148">See [Galaxy S4 does not show Authorize USB debugging dialog box][StackExchangeGalaxyS4DoesNotShowDialogBox].</span></span>  
*   <span data-ttu-id="75481-149">Sélectionnez **révoquer les autorisations de débogage USB** à partir de l’écran Options pour les **développeurs** sur votre appareil Android pour rétablir l’état de votre choix.</span><span class="sxs-lookup"><span data-stu-id="75481-149">Select **Revoke USB Debugging Authorizations** from the **Developer Options** screen on your Android device to reset it to a fresh state.</span></span>  

<span data-ttu-id="75481-150">Si vous trouvez une solution qui n’est pas mentionnée dans cette section ou dans [DevTools appareils ne détecte aucun appareil lorsque branché] [StackOverflowDevicesNotDetected] ou ajoutez une réponse à cette question de dépassement de pile</span><span class="sxs-lookup"><span data-stu-id="75481-150">If you find a solution that is not mentioned in this section or in [DevTools Devices does not detect device when plugged in][StackOverflowDevicesNotDetected] or please add an answer to that Stack Overflow question</span></span><!--, or [open an issue in the webfundamentals repository][GitHubWebFundamentalsNewIssue]--><span data-ttu-id="75481-151">!</span><span class="sxs-lookup"><span data-stu-id="75481-151">!</span></span>  

## <span data-ttu-id="75481-152">Étape 2: déboguer du contenu sur votre appareil Android à partir de votre ordinateur de développement</span><span class="sxs-lookup"><span data-stu-id="75481-152">Step 2: Debug content on your Android device from your development machine</span></span>   

1.  <span data-ttu-id="75481-153">Ouvrez Microsoft Edge sur votre appareil Android.</span><span class="sxs-lookup"><span data-stu-id="75481-153">Open Microsoft Edge on your Android device.</span></span>  

1.  <span data-ttu-id="75481-154">Dans l’onglet **équipements distants** , sélectionnez l’onglet qui correspond à votre nom de modèle d’appareil Android.</span><span class="sxs-lookup"><span data-stu-id="75481-154">In the **Remote Devices** tab, select the tab that matches your Android device model name.</span></span>  
    <span data-ttu-id="75481-155">Dans la partie supérieure de cette page, vous pouvez voir le nom du modèle de votre appareil Android, puis son numéro de série.</span><span class="sxs-lookup"><span data-stu-id="75481-155">At the top of this page, you see the model name of your Android device, followed by its serial number.</span></span>  <span data-ttu-id="75481-156">En dessous, vous devez voir la version de Microsoft Edge en cours d’exécution sur l’appareil, avec le numéro de version entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="75481-156">Below that, you should see the version of Microsoft Edge running on the device, with the version number in parentheses.</span></span>  <span data-ttu-id="75481-157">Chaque onglet Microsoft Edge ouvert dispose de sa propre section.</span><span class="sxs-lookup"><span data-stu-id="75481-157">Each open Microsoft Edge tab gets its own section.</span></span>  <span data-ttu-id="75481-158">Vous pouvez interagir avec cet onglet à partir de cette section.</span><span class="sxs-lookup"><span data-stu-id="75481-158">You may interact with that tab from this section.</span></span>  <!--If there are any apps using WebView, you see a section for each of those apps, too.  --><!--In [**Figure 5**](#figure-5) there are no tabs or WebViews open.  -->
    <!--
    > ##### Figure 5  
    > A connected remote device  
    > ![A connected remote device][ImageConnectedRemoteDevice]  -->

1.  <span data-ttu-id="75481-159">Dans la zone de texte **nouvel onglet** , entrez une URL, puis sélectionnez **ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="75481-159">In the **New tab** text box, enter a URL and then select **Open**.</span></span>  <span data-ttu-id="75481-160">La page s’ouvre dans un nouvel onglet sur votre appareil Android.</span><span class="sxs-lookup"><span data-stu-id="75481-160">The page opens in a new tab on your Android device.</span></span>  

1.  <span data-ttu-id="75481-161">Sélectionnez **inspecter** en regard de l’URL que vous venez d’ouvrir.</span><span class="sxs-lookup"><span data-stu-id="75481-161">Select **Inspect** next to the URL that you just opened.</span></span>  <span data-ttu-id="75481-162">Une nouvelle instance de DevTools s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="75481-162">A new DevTools instance opens.</span></span>  <span data-ttu-id="75481-163">La version de Microsoft Edge qui s’exécute sur votre appareil Android détermine la version d’DevTools qui s’ouvre sur votre ordinateur de développement.</span><span class="sxs-lookup"><span data-stu-id="75481-163">The version of Microsoft Edge running on your Android device determines the version of DevTools that opens on your development machine.</span></span>  
    <span data-ttu-id="75481-164">Par conséquent, si votre appareil Android exécute une vieille version de Microsoft Edge, l’instance DevTools peut s’avérer très différente de celle utilisée.</span><span class="sxs-lookup"><span data-stu-id="75481-164">So, if your Android device is running a very old version of Microsoft Edge, the DevTools instance may look very different than what you are used to.</span></span>  

### <span data-ttu-id="75481-165">Autres actions: recharger, mettre au point ou fermer un onglet</span><span class="sxs-lookup"><span data-stu-id="75481-165">More actions: reload, focus, or close a tab</span></span>   

<span data-ttu-id="75481-166">Sélectionnez **autres options** `...` en regard de l’onglet à recharger, mettre au point ou fermer.</span><span class="sxs-lookup"><span data-stu-id="75481-166">Select **More Options** `...` next to the tab that you want to reload, focus, or close.</span></span>  
<!--
> ##### Figure 6  
> The menu for reloading, focusing, or closing a tab  
> ![The menu for reloading, focusing, or closing a tab][ImageReload]  -->

### <span data-ttu-id="75481-167">Inspecter les éléments</span><span class="sxs-lookup"><span data-stu-id="75481-167">Inspect elements</span></span>   

<span data-ttu-id="75481-168">Accédez au panneau **éléments** de votre instance devtools, puis pointez sur un élément pour le mettre en surbrillance dans la fenêtre d’affichage de votre appareil Android.</span><span class="sxs-lookup"><span data-stu-id="75481-168">Go to the **Elements** panel of your DevTools instance, and hover over an element to highlight it in the viewport of your Android device.</span></span>  

<span data-ttu-id="75481-169">Vous pouvez également sélectionner un élément sur l’écran de votre appareil Android pour le sélectionner dans le panneau **éléments** .</span><span class="sxs-lookup"><span data-stu-id="75481-169">You may also select an element on your Android device screen to select it in the **Elements** panel.</span></span>  <span data-ttu-id="75481-170">Sélectionnez **Sélectionner** ![ l’élément sélectionner ][ImageSelectElementIcon] l’élément dans votre instance de devtools, puis sélectionnez l’élément sur l’écran de votre appareil Android.</span><span class="sxs-lookup"><span data-stu-id="75481-170">Select **Select Element** ![Select Element][ImageSelectElementIcon] on your DevTools instance, and then select the element on your Android device screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="75481-171">**Sélectionner l’élément** est désactivé après la première sélection; vous devez donc le réactiver chaque fois que vous souhaitez utiliser cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="75481-171">**Select Element** is disabled after the first selection, so you must re-enable it every time you want to use this feature.</span></span>  

### <span data-ttu-id="75481-172">Capturez l’écran de votre téléphone Android sur votre ordinateur de développement.</span><span class="sxs-lookup"><span data-stu-id="75481-172">Screencast your Android screen to your development machine</span></span>   

<span data-ttu-id="75481-173">Sélectionnez activer **/** désactiver ![ le bouton bascule capture ][ImageToggleScreencastIcon] d’écran pour afficher le contenu de votre appareil Android dans votre instance devtools.</span><span class="sxs-lookup"><span data-stu-id="75481-173">Select **Toggle Screencast** ![Toggle Screencast][ImageToggleScreencastIcon] to view the content of your Android device in your DevTools instance.</span></span>  

<span data-ttu-id="75481-174">Vous pouvez interagir avec le screencast de plusieurs manières:</span><span class="sxs-lookup"><span data-stu-id="75481-174">You are able to interact with the screencast in multiple ways:</span></span>  

*   <span data-ttu-id="75481-175">Les clics sont convertis en pressions et déclenchent les événements d’effleurement appropriés sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="75481-175">Clicks are translated into taps, firing proper touch events on the device.</span></span>  
*   <span data-ttu-id="75481-176">Les séquences de touches de votre ordinateur sont envoyées à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="75481-176">Keystrokes on your computer are sent to the device.</span></span>  
*   <span data-ttu-id="75481-177">Pour simuler un mouvement de pincement, maintenez la touche enfoncée `Shift` pendant que vous faites glisser.</span><span class="sxs-lookup"><span data-stu-id="75481-177">To simulate a pinch gesture, hold `Shift` while dragging.</span></span>  
*   <span data-ttu-id="75481-178">Pour faire défiler, utilisez votre pavé tactile ou votre volant de souris, ou glissement rapide avec le pointeur de la souris.</span><span class="sxs-lookup"><span data-stu-id="75481-178">To scroll, use your trackpad or mouse wheel, or fling with your mouse pointer.</span></span>

<span data-ttu-id="75481-179">Quelques remarques sur les screencasts:</span><span class="sxs-lookup"><span data-stu-id="75481-179">Some notes on screencasts:</span></span>  

*   <span data-ttu-id="75481-180">Les screencasts affichent uniquement le contenu de la page.</span><span class="sxs-lookup"><span data-stu-id="75481-180">Screencasts only display page content.</span></span>  <span data-ttu-id="75481-181">Les parties transparentes de l’enregistrement vidéo représentent des interfaces de périphériques, comme la barre d’adresses Microsoft Edge, la barre d’État Android ou le clavier Android.</span><span class="sxs-lookup"><span data-stu-id="75481-181">Transparent portions of the screencast represent device interfaces, such as the Microsoft Edge address bar, the Android status bar, or the Android keyboard.</span></span>  
*   <span data-ttu-id="75481-182">Les screencasts ont un impact négatif sur les taux d’images.</span><span class="sxs-lookup"><span data-stu-id="75481-182">Screencasts negatively affect frame rates.</span></span>  <span data-ttu-id="75481-183">Désactivez la capture d’images lors du mesurage des défilement ou des animations pour obtenir une image plus précise des performances de votre page.</span><span class="sxs-lookup"><span data-stu-id="75481-183">Disable screencasting while measuring scrolls or animations to get a more accurate picture of the performance of your page.</span></span>  
*   <span data-ttu-id="75481-184">Si l’écran de votre appareil Android est verrouillé, le contenu de votre screencast disparaît.</span><span class="sxs-lookup"><span data-stu-id="75481-184">If your Android device screen locks, the content of your screencast disappears.</span></span>  <span data-ttu-id="75481-185">Déverrouillez l’écran de votre appareil Android pour la reprise automatique.</span><span class="sxs-lookup"><span data-stu-id="75481-185">Unlock your Android device screen to automatically resume the screencast.</span></span>  





<!-- image links -->  

[ImageSelectElementIcon]: /microsoft-edge/devtools-guide-chromium/media/select-element-icon.msft.png  
[ImageToggleScreencastIcon]: /microsoft-edge/devtools-guide-chromium/media/toggle-screencast-icon.msft.png  

<!--[ImageRemoteDebugging]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging--remote-debugging.msft.png "old Figure 1:  Remote Debugging lets you inspect a page running on an Android device from your development machine"  -->  
[ImageOpenRemoteDevices]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Remote-Debugging-More-Tools-Remote-Devices.msft.png "figure 1: ouverture de l’onglet équipements distants par le biais du menu principal"  
[ImageDiscoverUSBDevices]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Remote-Debugging-Remote-Devices-Tab.msft.png "figure 2: la case à cocher découvrir les appareils USB est activée"  
<!--[ImageUnknownDevice]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging--unknown-device.msft.png "old Figure 4:  The Remote Devices tab has successfully detected an unknown device that is pending authorization"  -->  
<!--[ImageConnectedRemoteDevice]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging--connected-remote-device.msft.png "old Figure 5:  A connected remote device"  -->
<!--[ImageReload]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging--reload.msft.png "old Figure 6: The menu for reloading, focusing, or closing a tab"  -->

<!-- links -->  

[DevToolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Ouvrir Microsoft Edge DevTools"  

[AndroidUSBDrivers]: https://developer.android.com/tools/extras/oem-usb.html "Installer les pilotes USB OEM | Développeurs Android"  

<!-- [GitHubWebFundamentalsNewIssue]: https://github.com/Alphabet/webfundamentals/issues/new?title=[Remote%20Debugging] "GitHub - Web Fundamentals - New Issue"  -->  
[StackOverflowDevicesNotDetected]: https://stackoverflow.com/questions/21925992 «les appareils devtools ne détectent pas l’appareil en cas de dépassement de la pile connectée»  

[StackExchangeGalaxyS4DoesNotShowDialogBox]: https://android.stackexchange.com/questions/101933 "ADB: échange d’une pile enthousiaste pour Android"  

> [!NOTE]
> <span data-ttu-id="75481-192">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="75481-192">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="75481-193">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="75481-193">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="75481-195">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="75481-195">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
