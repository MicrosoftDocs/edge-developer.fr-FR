---
description: Émuler les défaillances de la vision des couleurs, ancrer à gauche dans le menu commande, et bien plus encore.
title: Nouveautés de DevTools (Microsoft Edge 83)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 158d91e3d9c925beebe03a1baa8d6308b650262b
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398944"
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

# <a name="whats-new-in-devtools-microsoft-edge-83"></a><span data-ttu-id="246b3-104">Nouveautés de DevTools (Microsoft Edge 83)</span><span class="sxs-lookup"><span data-stu-id="246b3-104">What's New In DevTools (Microsoft Edge 83)</span></span>  

<span data-ttu-id="246b3-105">Après la mise à jour de la planification Chromium, nous ajustons notre planification pour les prochaines publication de Microsoft Edge et annulons la version Microsoft Edge 82.</span><span class="sxs-lookup"><span data-stu-id="246b3-105">Following the updated Chromium schedule, we are adjusting our schedule for upcoming Microsoft Edge releases and cancelling the Microsoft Edge 82 release.</span></span> <span data-ttu-id="246b3-106">Consultez notre [billet de blog pour][WindowsBlogStableRelease] plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="246b3-106">Check out our [blog post][WindowsBlogStableRelease] for more info.</span></span>  

<span data-ttu-id="246b3-107">Voici les nouvelles fonctionnalités disponibles dans DevTools dans Microsoft Edge 83.</span><span class="sxs-lookup"><span data-stu-id="246b3-107">Here are the new features available in the DevTools in Microsoft Edge 83.</span></span>  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a><span data-ttu-id="246b3-108">Annonces de l’équipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="246b3-108">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="246b3-109">Les sections suivantes sont une liste des annonces que vous avez peut-être manquées de l’équipe Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="246b3-109">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team.</span></span>  <span data-ttu-id="246b3-110">Consultez les annonces pour essayer les nouvelles fonctionnalités des extensions DevTools, Microsoft Visual Studio Code, etc.</span><span class="sxs-lookup"><span data-stu-id="246b3-110">Check out the announcements to try new features in the DevTools, Microsoft Visual Studio Code extensions, and more.</span></span>  <span data-ttu-id="246b3-111">Pour rester à jour sur toutes les fonctionnalités les plus récentes et les plus importantes de vos outils de développement, téléchargez les canaux d’aperçu [microsoft Edge][MicrosoftEdgePreviewChannels] et suivez-nous [sur Twitter.][EdgeDevToolsTwitterAccount]</span><span class="sxs-lookup"><span data-stu-id="246b3-111">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <a name="remotely-debug-microsoft-edge-on-windows-10-devices"></a><span data-ttu-id="246b3-112">Débogage à distance de Microsoft Edge sur les appareils Windows 10</span><span class="sxs-lookup"><span data-stu-id="246b3-112">Remotely debug Microsoft Edge on Windows 10 Devices</span></span>  

<span data-ttu-id="246b3-113">[L’application Outils à distance pour Microsoft Edge \(Bêta\)][RemoteTools] est désormais disponible dans le [Microsoft Store.][MicrosoftStore]</span><span class="sxs-lookup"><span data-stu-id="246b3-113">The [Remote Tools for Microsoft Edge \(Beta\)][RemoteTools] app is now available in the [Microsoft Store][MicrosoftStore].</span></span>  <span data-ttu-id="246b3-114">À l’aide de cette application, qui étend [Windows Device Portal,][WindowsUwpDebugTestPerfDevicePortal]vous pouvez vous connecter à partir de l’instance de Microsoft Edge en cours d’exécution sur votre ordinateur de développement à un appareil Windows 10 distant, afficher la liste des cibles \(tous les onglets de Microsoft Edge et [pwAs][ProgressiveWebAppsChromiumIndex] s’ouvrent sur l’appareil Windows 10\), et utiliser DevTools sur votre ordinateur de développement par rapport à une cible s’exécutant sur l’appareil Windows 10 distant.</span><span class="sxs-lookup"><span data-stu-id="246b3-114">Using this app, which extends the [Windows Device Portal][WindowsUwpDebugTestPerfDevicePortal], you are able to connect from the instance of Microsoft Edge running on your development machine to a remote Windows 10 device, display a list of targets \(all tabs in Microsoft Edge and [PWAs][ProgressiveWebAppsChromiumIndex] open on the Windows 10 device\), and use the DevTools on your development machine against a target running on the remote Windows 10 device.</span></span>  

:::image type="complex" source="../../media/2020/03/remote-tools.msft.png" alt-text="Application Outils à distance pour Microsoft Edge (bêta) disponible dans le Microsoft Store" lightbox="../../media/2020/03/remote-tools.msft.png":::
   <span data-ttu-id="246b3-116">Application [Outils à distance pour Microsoft Edge (bêta)][RemoteTools] disponible dans le [Microsoft Store][MicrosoftStore]</span><span class="sxs-lookup"><span data-stu-id="246b3-116">The [Remote Tools for Microsoft Edge (Beta)][RemoteTools] app available in the [Microsoft Store][MicrosoftStore]</span></span>  
:::image-end:::  

<span data-ttu-id="246b3-117">Lisez notre guide pour la configuration de votre appareil Windows 10 et de votre ordinateur de [développement pour le débogage à distance.][DevtoolsRemoteDebuggingWindows]</span><span class="sxs-lookup"><span data-stu-id="246b3-117">[Read our guide for setting up your Windows 10 device and your development machine for remote debugging][DevtoolsRemoteDebuggingWindows].</span></span>  <span data-ttu-id="246b3-118">Faites-nous part de votre expérience de débogage à distance en [tweetant][PostTweetEdgeDevTools] ou en déconant l’icône [Envoyer des](#getting-in-touch-with-microsoft-edge-devtools-team) commentaires !</span><span class="sxs-lookup"><span data-stu-id="246b3-118">Let us know about your remote debugging experience by [tweeting][PostTweetEdgeDevTools] orchoosing the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

### <a name="new-ways-to-access-settings"></a><span data-ttu-id="246b3-119">Nouvelles façons d’accéder aux paramètres</span><span class="sxs-lookup"><span data-stu-id="246b3-119">New ways to access Settings</span></span>  

<span data-ttu-id="246b3-120">Il existe des milliers de paramètres pour devTools que vous pouvez personnaliser pour donner à DevTools l’apparence, l’apparence et le travail dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="246b3-120">There are tons of settings for the DevTools that you are able to customize to make the DevTools look, feel, and work the way you need.</span></span> <span data-ttu-id="246b3-121">Dans Microsoft Edge 83, l’accès aux [paramètres][DevtoolsCustomizeIndexSettings] dans DevTools est désormais beaucoup plus facile.</span><span class="sxs-lookup"><span data-stu-id="246b3-121">In Microsoft Edge 83, accessing [Settings][DevtoolsCustomizeIndexSettings] in the DevTools is now much easier.</span></span>  <span data-ttu-id="246b3-122">Ouvrez Paramètres avec l’icône d’engrenage en face des alertes de la console et du menu principal.</span><span class="sxs-lookup"><span data-stu-id="246b3-122">Open Settings with the gear icon next to Console alerts and the main menu.</span></span>  

:::image type="complex" source="../../media/2020/03/settings.msft.png" alt-text="L’icône d’engrenage ouvre paramètres dans DevTools" lightbox="../../media/2020/03/settings.msft.png":::
   <span data-ttu-id="246b3-124">L’icône d’engrenage ouvre **paramètres** dans DevTools</span><span class="sxs-lookup"><span data-stu-id="246b3-124">The gear icon opens **Settings** in the DevTools</span></span>  
:::image-end:::  

<span data-ttu-id="246b3-125">Vous pouvez également ouvrir [Paramètres à][DevtoolsCustomizeIndexSettings] partir du **menu principal** sous **Plus d’outils.**</span><span class="sxs-lookup"><span data-stu-id="246b3-125">You are also able to open [Settings][DevtoolsCustomizeIndexSettings] from the **Main Menu** under **More tools**.</span></span>

:::image type="complex" source="../../media/2020/03/settings2.msft.png" alt-text="Menu principal > plus d’outils > paramètres" lightbox="../../media/2020/03/settings2.msft.png":::
   <span data-ttu-id="246b3-127">**Menu principal**  >  **Autres outils**  >  **Paramètres**</span><span class="sxs-lookup"><span data-stu-id="246b3-127">**Main Menu** > **More tools** > **Settings**</span></span>  
:::image-end:::  

<span data-ttu-id="246b3-128">Problème de chrome [#1050855][CR1050855]</span><span class="sxs-lookup"><span data-stu-id="246b3-128">Chromium issue [#1050855][CR1050855]</span></span>

### <a name="new-and-improved-infobars"></a><span data-ttu-id="246b3-129">Barres d’informations nouvelles et améliorées</span><span class="sxs-lookup"><span data-stu-id="246b3-129">New and improved infobars</span></span>

<span data-ttu-id="246b3-130">Les barres de notification d’information \(infobars\) dans DevTools ont désormais une apparence améliorée et des fonctionnalités supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="246b3-130">Informational notification bars \(infobars\) in DevTools now have an improved look and more functionality.</span></span> <span data-ttu-id="246b3-131">Dans Microsoft Edge 83, les barres d’informations sont plus faciles à lire et fournissent des boutons afin que vous pouvez immédiatement prendre l’action pertinente.</span><span class="sxs-lookup"><span data-stu-id="246b3-131">In Microsoft Edge 83, infobars are easier to read and provide buttons so you are able to take the relevant action right away.</span></span>  

:::image type="complex" source="../../media/2020/03/infobar.msft.png" alt-text="Barre d’informations pour l’impression d’un fichier minifié dans Microsoft Edge 83" lightbox="../../media/2020/03/infobar.msft.png":::
   <span data-ttu-id="246b3-133">Barre d’informations pour l’impression d’un fichier minifié dans Microsoft Edge Version 83</span><span class="sxs-lookup"><span data-stu-id="246b3-133">Infobar for pretty-printing a minified file in Microsoft Edge Version 83</span></span>  
:::image-end:::  

<span data-ttu-id="246b3-134">Problème de chrome [#1056348][CR1056348]</span><span class="sxs-lookup"><span data-stu-id="246b3-134">Chromium issue [#1056348][CR1056348]</span></span>

### <a name="navigate-the-color-picker-with-your-keyboard"></a><span data-ttu-id="246b3-135">Naviguer dans le s sélectionneur de couleurs avec votre clavier</span><span class="sxs-lookup"><span data-stu-id="246b3-135">Navigate the Color Picker with your keyboard</span></span>  

<span data-ttu-id="246b3-136">Le [s sélectionneur de couleurs][DevtoolsCssReferenceColorPicker] est une interface graphique graphique dans le panneau [Éléments pour][DevtoolsCssIndex] la modification et les `color` `background-color` déclarations.</span><span class="sxs-lookup"><span data-stu-id="246b3-136">The [Color Picker][DevtoolsCssReferenceColorPicker] is a GUI in the [Elements panel][DevtoolsCssIndex] for changing `color` and `background-color` declarations.</span></span>  <span data-ttu-id="246b3-137">Dans les versions précédentes de Microsoft Edge, vous n’étiez pas en mesure de naviguer dans la section **Nuances** du s [picker][DevtoolsCssReferenceColorPicker] de couleurs avec le clavier.</span><span class="sxs-lookup"><span data-stu-id="246b3-137">In previous versions of Microsoft Edge, you were not able to navigate the **Shades** section of the [Color Picker][DevtoolsCssReferenceColorPicker] with the keyboard.</span></span>  

:::image type="complex" source="../../media/2020/03/color-picker.msft.png" alt-text="Vous pouvez désormais utiliser votre clavier pour déplacer le sélecteur dans la section Nuances du sélecteur de couleurs" lightbox="../../media/2020/03/color-picker.msft.png":::
   <span data-ttu-id="246b3-139">Vous pouvez désormais utiliser votre clavier pour déplacer le sélecteur dans la section **Nuances** du [sélecteur de couleurs][DevtoolsCssReferenceColorPicker]</span><span class="sxs-lookup"><span data-stu-id="246b3-139">You are now able to use your keyboard to move the selector in the **Shades** section of the [Color Picker][DevtoolsCssReferenceColorPicker]</span></span>  
:::image-end:::  

<span data-ttu-id="246b3-140">Dans Microsoft Edge 83, vous pouvez désormais utiliser le clavier pour déplacer le sélecteur dans la section **Nuances** du sélecteur de couleurs.</span><span class="sxs-lookup"><span data-stu-id="246b3-140">In Microsoft Edge 83, you are now able to use the keyboard to move the selector in the **Shades** section of the Color Picker.</span></span>  

<span data-ttu-id="246b3-141">Problème de chrome [#963183][CR963183]</span><span class="sxs-lookup"><span data-stu-id="246b3-141">Chromium issue [#963183][CR963183]</span></span>  

### <a name="properties-tab-now-populates-after-a-page-refresh"></a><span data-ttu-id="246b3-142">L’onglet Propriétés se remplit maintenant après l’actualisation d’une page</span><span class="sxs-lookup"><span data-stu-id="246b3-142">Properties tab now populates after a page refresh</span></span>  

<span data-ttu-id="246b3-143">Dans Microsoft Edge 81 et \*\*\*\* les antérieures, l’onglet Propriétés du panneau [Éléments][DevtoolsCssIndex] a été rompu par des actualisations de page.</span><span class="sxs-lookup"><span data-stu-id="246b3-143">In Microsoft Edge 81 and earlier, the **Properties tab** in the [Elements panel][DevtoolsCssIndex] was broken by page refreshes.</span></span>  <span data-ttu-id="246b3-144">Lorsque vous avez actualisé la page, **l’onglet Propriétés** n’a pas rempli les propriétés de l’élément actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="246b3-144">When you refreshed the page, the **Properties tab** did not populate the properties of the currently-selected element.</span></span>  

:::image type="complex" source="../../media/2020/03/properties-in-81.msft.png" alt-text="Dans Microsoft Edge 81 et les précédentes, l’onglet Propriétés était vide après l’actualisation d’une page" lightbox="../../media/2020/03/properties-in-81.msft.png":::
   <span data-ttu-id="246b3-146">Dans Microsoft Edge 81 et les précédentes, **l’onglet Propriétés** était vide après l’actualisation d’une page</span><span class="sxs-lookup"><span data-stu-id="246b3-146">In Microsoft Edge 81 and earlier, the **Properties tab** was blank after a page refresh</span></span>  
:::image-end:::  

<span data-ttu-id="246b3-147">Dans Microsoft Edge 83, vous pouvez désormais afficher les propriétés de l’élément actuellement sélectionné après une actualisation de page dans l’onglet **Propriétés.**</span><span class="sxs-lookup"><span data-stu-id="246b3-147">In Microsoft Edge 83, you are now able to display the properties of the currently-selected element after a page refresh in the **Properties tab**.</span></span>  

:::image type="complex" source="../../media/2020/03/properties-in-82.msft.png" alt-text="Dans Microsoft Edge 83, l’onglet Propriétés affiche les propriétés de l’élément actuellement sélectionné après l’actualisation d’une page" lightbox="../../media/2020/03/properties-in-82.msft.png":::
   <span data-ttu-id="246b3-149">Dans Microsoft Edge 83, l’onglet Propriétés affiche les propriétés de l’élément actuellement sélectionné après l’actualisation d’une page \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="246b3-149">In Microsoft Edge 83, the **Properties tab** displays the properties of the currently-selected element after a page refresh</span></span>  
:::image-end:::  

<span data-ttu-id="246b3-150">Problème de chrome [#1050999][CR1050999]</span><span class="sxs-lookup"><span data-stu-id="246b3-150">Chromium issue [#1050999][CR1050999]</span></span>  

### <a name="use-the-arrow-keys-to-scroll-in-the-changes-tool"></a><span data-ttu-id="246b3-151">Utiliser les touches de direction pour faire défiler l’outil Modifications</span><span class="sxs-lookup"><span data-stu-id="246b3-151">Use the arrow keys to scroll in the Changes tool</span></span>  

<span data-ttu-id="246b3-152">**L’outil Changes** suit toutes les modifications que vous avez apportées à CSS ou JavaScript dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="246b3-152">The **Changes tool** tracks any changes you have made to CSS or JavaScript in the DevTools.</span></span>  <span data-ttu-id="246b3-153">Vous pouvez utiliser l’outil **Modifications** pour afficher rapidement toutes vos modifications et les remettre à votre éditeur/IDE.</span><span class="sxs-lookup"><span data-stu-id="246b3-153">You are able to use the **Changes tool** to quickly display all your changes and take those back to your editor/IDE.</span></span>  

<span data-ttu-id="246b3-154">Pour ouvrir **l’outil Modifications,** sélectionnez `Ctrl` + `Shift` + `P` dans DevTools pour ouvrir le [menu commande][DevToolsCommandMenuIndex] et tapez `changes` .</span><span class="sxs-lookup"><span data-stu-id="246b3-154">To open the **Changes tool**, select `Ctrl`+`Shift`+`P` in the DevTools to open the [Command Menu][DevToolsCommandMenuIndex] and type `changes`.</span></span>  <span data-ttu-id="246b3-155">choisissez et exécutez la **commande Afficher les modifications** pour ouvrir **l’outil Modifications** dans le caisse DevTools.</span><span class="sxs-lookup"><span data-stu-id="246b3-155">choose and run the **Show Changes** command to open the **Changes tool** in the DevTools drawer.</span></span>  

<span data-ttu-id="246b3-156">Lorsque vous avez apporté une modification à un fichier minifié, l’outil **Changes** vous permet de faire défiler horizontalement pour afficher l’ensemble de votre code minifié.</span><span class="sxs-lookup"><span data-stu-id="246b3-156">When you have made a change to a minified file, the **Changes tool** enables you to scroll horizontally to display all of your minified code.</span></span>  <span data-ttu-id="246b3-157">À partir de Microsoft Edge 83, vous pouvez maintenant faire défiler horizontalement à l’aide des touches de direction de votre clavier.</span><span class="sxs-lookup"><span data-stu-id="246b3-157">Starting in Microsoft Edge 83, you may now scroll horizontally using the arrow keys on your keyboard.</span></span>  

:::image type="complex" source="../../media/2020/03/changes.msft.png" alt-text="Dans Microsoft Edge 83, vous pouvez faire défiler horizontalement avec les touches de direction pour afficher votre code minifié dans l’outil Modifications" lightbox="../../media/2020/03/changes.msft.png":::
   <span data-ttu-id="246b3-159">Dans Microsoft Edge 83, vous pouvez faire défiler horizontalement avec les touches de direction pour afficher les modifications apportées à votre code minifié dans l’outil **Modifications**</span><span class="sxs-lookup"><span data-stu-id="246b3-159">In Microsoft Edge 83, you may scroll horizontally with the arrow keys to display the changes you made to your minified code in the **Changes tool**</span></span>  
:::image-end:::  

<span data-ttu-id="246b3-160">Si vous utilisez des lecteurs d’écran ou le clavier pour naviguer dans DevTools, envoyez-nous vos commentaires en nous faisant part de vos [commentaires][PostTweetEdgeDevTools] ou en criant l’icône Envoyer [des](#getting-in-touch-with-microsoft-edge-devtools-team) commentaires !</span><span class="sxs-lookup"><span data-stu-id="246b3-160">If you use screen readers or the keyboard to navigate around the DevTools, send us your feedback by [tweeting][PostTweetEdgeDevTools] at us orchoosing the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="246b3-161">Problème de chrome [#963183][CR963183]</span><span class="sxs-lookup"><span data-stu-id="246b3-161">Chromium issue [#963183][CR963183]</span></span>  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="246b3-162">Annonces du projet de Chromium</span><span class="sxs-lookup"><span data-stu-id="246b3-162">Announcements from the Chromium project</span></span>  

<span data-ttu-id="246b3-163">Les sections suivantes annoncent des fonctionnalités supplémentaires disponibles dans Microsoft Edge 83 qui ont été contribués au projet Chromium open source.</span><span class="sxs-lookup"><span data-stu-id="246b3-163">The following sections announce additional features available in Microsoft Edge 83 that were contributed to the open source Chromium project.</span></span>  

### <a name="emulate-vision-deficiencies"></a><span data-ttu-id="246b3-164">Émuler les faiblesses de la vision</span><span class="sxs-lookup"><span data-stu-id="246b3-164">Emulate vision deficiencies</span></span>  

<span data-ttu-id="246b3-165">Ouvrez [l’onglet][DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab] Rendu et utilisez la nouvelle fonctionnalité Émuler les défauts de **vision** pour avoir une meilleure idée de la façon dont les personnes ayant différents types de problèmes de vision rencontrent votre site.</span><span class="sxs-lookup"><span data-stu-id="246b3-165">Open the [Rendering tab][DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab] and use the new **Emulate vision deficiencies** feature to get a better idea of how people with different types of vision deficiencies experience your site.</span></span>  

:::image type="complex" source="../../media/2020/03/vision.msft.png" alt-text="Émulation d’une vision floue" lightbox="../../media/2020/03/vision.msft.png":::
   <span data-ttu-id="246b3-167">Émulation d’une vision floue</span><span class="sxs-lookup"><span data-stu-id="246b3-167">Emulating blurred vision</span></span>  
:::image-end:::  

<span data-ttu-id="246b3-168">DevTools est en mesure d’émuler la vision floue et les types suivants de [défauts de vision de couleur.][ColorBlindnessTypes]</span><span class="sxs-lookup"><span data-stu-id="246b3-168">DevTools is able to emulate blurred vision and the following [types of color vision deficiencies][ColorBlindnessTypes].</span></span>  

| <span data-ttu-id="246b3-169">Problèmes de vision des couleurs</span><span class="sxs-lookup"><span data-stu-id="246b3-169">Color Vision Deficiency</span></span> | <span data-ttu-id="246b3-170">Détails</span><span class="sxs-lookup"><span data-stu-id="246b3-170">Details</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="246b3-171">Protanopia</span><span class="sxs-lookup"><span data-stu-id="246b3-171">Protanopia</span></span> | <span data-ttu-id="246b3-172">L’incapacité à percevoir toute lumière rouge.</span><span class="sxs-lookup"><span data-stu-id="246b3-172">The inability to perceive any red light.</span></span> |  
| <span data-ttu-id="246b3-173">Deuteranopia</span><span class="sxs-lookup"><span data-stu-id="246b3-173">Deuteranopia</span></span> | <span data-ttu-id="246b3-174">L’incapacité à percevoir toute lumière verte.</span><span class="sxs-lookup"><span data-stu-id="246b3-174">The inability to perceive any green light.</span></span> |  
| <span data-ttu-id="246b3-175">Tritanopia</span><span class="sxs-lookup"><span data-stu-id="246b3-175">Tritanopia</span></span> | <span data-ttu-id="246b3-176">L’incapacité à percevoir la lumière bleue.</span><span class="sxs-lookup"><span data-stu-id="246b3-176">The inability to perceive any blue light.</span></span> |  
| <span data-ttu-id="246b3-177">Achromatopsia</span><span class="sxs-lookup"><span data-stu-id="246b3-177">Achromatopsia</span></span> | <span data-ttu-id="246b3-178">L’incapacité à percevoir n’importe quelle couleur, à l’exception des nuances de gris \(extrêmement rares\).</span><span class="sxs-lookup"><span data-stu-id="246b3-178">The inability to perceive any color, except for shades of grey \(extremely rare\).</span></span> |  

<span data-ttu-id="246b3-179">Il existe des versions moins extrêmes de ces insuffisances de vision des couleurs et, en fait, elles sont plus courantes.</span><span class="sxs-lookup"><span data-stu-id="246b3-179">Less extreme versions of these color vision deficiencies exist, and in fact they are more common.</span></span>  
<span data-ttu-id="246b3-180">Par exemple, le protanomaly est une sensibilité réduite à la lumière rouge (par opposition à la protanopie, qui est l’incapacité totale à percevoir la lumière rouge).</span><span class="sxs-lookup"><span data-stu-id="246b3-180">For example, protanomaly is a reduced sensitivity to red light (as opposed to protanopia, which is the complete inability to perceive red light).</span></span> <span data-ttu-id="246b3-181">Toutefois, ces défaillances visuelles **-omaly** ne sont pas aussi clairement définies : chaque personne atteinte d’une telle défaillance visuelle est différente et peut voir les choses différemment \(être en mesure de percevoir plus/moins les couleurs pertinentes\).</span><span class="sxs-lookup"><span data-stu-id="246b3-181">However, these **-omaly** vision deficiencies are not as clearly defined:  every person with such a vision deficiency is different and may see things differently \(being able to perceive more/less of the relevant colors\).</span></span>  

<span data-ttu-id="246b3-182">En concevant des simulations plus extrêmes dans DevTools, vos applications web sont garanties d’être accessibles aux personnes avec protanomaly, deuteranomaly, tritanomaly et achromatomaly également.</span><span class="sxs-lookup"><span data-stu-id="246b3-182">By designing for the more extreme simulations in DevTools, your web apps are guaranteed to be accessible to people with protanomaly, deuteranomaly, tritanomaly, and achromatomaly as well.</span></span>  

<span data-ttu-id="246b3-183">Envoyez vos commentaires en [tweetant][PostTweetEdgeDevTools] ou en cinglant [l’icône Envoyer des](#getting-in-touch-with-microsoft-edge-devtools-team) commentaires !</span><span class="sxs-lookup"><span data-stu-id="246b3-183">Send your feedback by [tweeting][PostTweetEdgeDevTools] orchoosing the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="246b3-184">Problème de chrome [#1003700][CR1003700]</span><span class="sxs-lookup"><span data-stu-id="246b3-184">Chromium issue [#1003700][CR1003700]</span></span>  

### <a name="emulate-locales"></a><span data-ttu-id="246b3-185">Émuler les paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="246b3-185">Emulate locales</span></span>  

<span data-ttu-id="246b3-186">Émuler les paramètres régionaux en définir un emplacement dans **l’emplacement des**  >  **capteurs.**</span><span class="sxs-lookup"><span data-stu-id="246b3-186">Emulate locales by setting a location in **Sensors** > **Location**.</span></span> <span data-ttu-id="246b3-187">[Ouvrez le **menu Commande et** ][DevToolsCommandMenuIndex] tapez pour accéder à `Sensors` **l’onglet Capteurs.**  Après avoir effectué ces actions, DevTools modifie les paramètres régionaux par défaut actuels, ce qui affecte le code suivant.</span><span class="sxs-lookup"><span data-stu-id="246b3-187">[Open the **Command Menu**][DevToolsCommandMenuIndex] and type `Sensors` to access the **Sensors** tab.  After performing these actions, DevTools modifies the current default locale, affecting the following code.</span></span>  

*   `Intl.*` <span data-ttu-id="246b3-188">LES API, par exemple :</span><span class="sxs-lookup"><span data-stu-id="246b3-188">APIs, for example:</span></span> `new Intl.NumberFormat().resolvedOptions().locale`  
*   <span data-ttu-id="246b3-189">Autres API JavaScript sensibles aux paramètres régionaux telles `String.prototype.localeCompare` que `*.prototype.toLocaleString` et, par exemple :</span><span class="sxs-lookup"><span data-stu-id="246b3-189">Other locale-aware JavaScript APIs such as `String.prototype.localeCompare` and `*.prototype.toLocaleString`, for example:</span></span> `123_456..toLocaleString()`  
*   <span data-ttu-id="246b3-190">API DOM telles que `navigator.language` et</span><span class="sxs-lookup"><span data-stu-id="246b3-190">DOM APIs such as `navigator.language` and</span></span> `navigator.languages`  
*   <span data-ttu-id="246b3-191">En-tête de requête HTTP [accept-Language][MDNAcceptLanguage]</span><span class="sxs-lookup"><span data-stu-id="246b3-191">The [Accept-Language][MDNAcceptLanguage] HTTP request header</span></span>  

> [!NOTE]
> <span data-ttu-id="246b3-192">Mises à jour pour `navigator.language` et ne sont pas `navigator.languages` visibles immédiatement, mais uniquement après la navigation suivante ou l’actualisation de la page.</span><span class="sxs-lookup"><span data-stu-id="246b3-192">Updates to `navigator.language` and `navigator.languages` are not visible immediately, but only after the next navigation or page refresh.</span></span>  <span data-ttu-id="246b3-193">Les modifications apportées à `Accept-Language` l’en-tête HTTP ne sont reflétées que pour les demandes suivantes.</span><span class="sxs-lookup"><span data-stu-id="246b3-193">Changes to the `Accept-Language` HTTP header are only reflected for subsequent requests.</span></span>  

:::image type="complex" source="../../media/2020/03/locale.msft.png" alt-text="Émulation d’un paramètres régionaux" lightbox="../../media/2020/03/locale.msft.png":::
   <span data-ttu-id="246b3-195">Émulation d’un paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="246b3-195">Emulating a locale</span></span>  
:::image-end:::  

<span data-ttu-id="246b3-196">Pour essayer une démonstration, accédez à [l’exemple de code dépendant des paramètres régionaux.][MathiasByensLocaleDemo]</span><span class="sxs-lookup"><span data-stu-id="246b3-196">To try a demo, navigate to [Locale-dependent code example][MathiasByensLocaleDemo].</span></span>

<span data-ttu-id="246b3-197">Problème de chrome [#1051822][CR1051822]</span><span class="sxs-lookup"><span data-stu-id="246b3-197">Chromium issue [#1051822][CR1051822]</span></span>

### <a name="cross-origin-embedder-policy-coep-debugging"></a><span data-ttu-id="246b3-198">Débogage de la stratégie d’incorporation d’origine croisée (COEP)</span><span class="sxs-lookup"><span data-stu-id="246b3-198">Cross-Origin Embedder Policy (COEP) debugging</span></span>  

<span data-ttu-id="246b3-199">Le panneau Réseau fournit désormais [des informations de débogage][COEP] de stratégie d’incorporation d’origine croisée.</span><span class="sxs-lookup"><span data-stu-id="246b3-199">The Network panel now provides [Cross-Origin Embedder Policy][COEP] debugging information.</span></span>  

<span data-ttu-id="246b3-200">La **colonne État** fournit désormais une explication rapide de la raison pour laquelle une demande a été bloquée, ainsi qu’un lien pour afficher les en-têtes de cette demande pour un débogage supplémentaire :</span><span class="sxs-lookup"><span data-stu-id="246b3-200">The **Status** column now provides a quick explanation of why a request was blocked as well as a link to view the headers of that request for further debugging:</span></span>  

:::image type="complex" source="../../media/2020/03/status.msft.png" alt-text="Demandes bloquées dans la colonne **État**" lightbox="../../media/2020/03/status.msft.png":::
   <span data-ttu-id="246b3-202">Demandes bloquées dans la **colonne État**</span><span class="sxs-lookup"><span data-stu-id="246b3-202">Blocked requests in the **Status** column</span></span>  
:::image-end:::  

<span data-ttu-id="246b3-203">La section **En-têtes de** réponse de l’onglet **En-têtes** fournit davantage d’instructions sur la résolution des problèmes :</span><span class="sxs-lookup"><span data-stu-id="246b3-203">The **Response Headers** section of the **Headers** tab provides more guidance on how to resolve the issues:</span></span>  

:::image type="complex" source="../../media/2020/03/guidance.msft.png" alt-text="Plus d’instructions dans la section En-têtes de réponse" lightbox="../../media/2020/03/guidance.msft.png":::
   <span data-ttu-id="246b3-205">Plus d’instructions dans la section **En-têtes de** réponse</span><span class="sxs-lookup"><span data-stu-id="246b3-205">More guidance in the **Response Headers** section</span></span>  
:::image-end:::  

<span data-ttu-id="246b3-206">Envoyez vos commentaires en [tweetant][PostTweetEdgeDevTools] ou en cinglant [l’icône Envoyer des](#getting-in-touch-with-microsoft-edge-devtools-team) commentaires !</span><span class="sxs-lookup"><span data-stu-id="246b3-206">Send your feedback by [tweeting][PostTweetEdgeDevTools] orchoosing the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="246b3-207">Problème de chrome [#1051466][CR1051466]</span><span class="sxs-lookup"><span data-stu-id="246b3-207">Chromium issue [#1051466][CR1051466]</span></span>  

### <a name="new-icons-for-breakpoints-conditional-breakpoints-and-logpoints"></a><span data-ttu-id="246b3-208">Nouvelles icônes pour les points d’arrêt, les points d’arrêt conditionnels et les points d’accès</span><span class="sxs-lookup"><span data-stu-id="246b3-208">New icons for breakpoints, conditional breakpoints, and logpoints</span></span>  

<span data-ttu-id="246b3-209">Le panneau Sources possède de nouvelles icônes pour les points d’arrêt, les points d’arrêt conditionnels et les points d’accès :</span><span class="sxs-lookup"><span data-stu-id="246b3-209">The Sources panel has new icons for breakpoints, conditional breakpoints, and logpoints:</span></span>  

*   <span data-ttu-id="246b3-210">Points d’arrêt \(</span><span class="sxs-lookup"><span data-stu-id="246b3-210">Breakpoints \(</span></span>![Point d’arrêt](../../media/2020/03/breakpoint.msft.png)<span data-ttu-id="246b3-212">\) sont représentés par des cercles rouges.</span><span class="sxs-lookup"><span data-stu-id="246b3-212">\) are represented by red circles.</span></span>  
*   <span data-ttu-id="246b3-213">Points d’arrêt conditionnels \(</span><span class="sxs-lookup"><span data-stu-id="246b3-213">Conditional Breakpoints \(</span></span>![Point d’arrêt conditionnel](../../media/2020/03/conditional.msft.png)<span data-ttu-id="246b3-215">\) sont représentés par des cercles demi-rouges demi-blancs.</span><span class="sxs-lookup"><span data-stu-id="246b3-215">\) are represented by half-red half-white circles.</span></span>  
*   <span data-ttu-id="246b3-216">Logpoints \(</span><span class="sxs-lookup"><span data-stu-id="246b3-216">Logpoints \(</span></span>![Logpoint](../../media/2020/03/logpoint.msft.png)<span data-ttu-id="246b3-218">\) sont représentés par des cercles rouges avec des icônes de console.</span><span class="sxs-lookup"><span data-stu-id="246b3-218">\) are represented by red circles with Console icons.</span></span>  

<span data-ttu-id="246b3-219">La motivation des nouvelles icônes était de rendre l’interface utilisateur plus cohérente avec les autres outils de débogage de l’interface utilisateur graphique \(qui colorent généralement les points d’arrêt en rouge\) et de faciliter la distinction entre les 3 fonctionnalités en un coup d’œil.</span><span class="sxs-lookup"><span data-stu-id="246b3-219">The motivation for the new icons was to make the UI more consistent with other GUI debugging tools \(which usually color breakpoints red\) and to make it easier to distinguish between the 3 features at a glance.</span></span>  

<span data-ttu-id="246b3-220">Problème de chrome [#1041830][CR1041830]</span><span class="sxs-lookup"><span data-stu-id="246b3-220">Chromium issue [#1041830][CR1041830]</span></span>  

### <a name="view-network-requests-that-set-a-specific-cookie-path"></a><span data-ttu-id="246b3-221">Afficher les demandes réseau qui définissent un chemin d’accès de cookie spécifique</span><span class="sxs-lookup"><span data-stu-id="246b3-221">View network requests that set a specific cookie path</span></span>  

<span data-ttu-id="246b3-222">Utilisez le nouveau mot clé de filtre dans l’outil Réseau pour vous concentrer sur les demandes réseau qui définissent `cookie-path` un chemin d’accès [de cookie spécifique.][MDNCookiePath] \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="246b3-222">Use the new `cookie-path` filter keyword in the **Network** tool to focus on the network requests that set a specific [cookie path][MDNCookiePath].</span></span>  

<span data-ttu-id="246b3-223">Consultez [filtrer les demandes par propriétés][DevtoolsNetworkReferenceFilterRequestsProperties] pour découvrir d’autres mots clés tels que `cookie-path` .</span><span class="sxs-lookup"><span data-stu-id="246b3-223">Check out [Filter requests by properties][DevtoolsNetworkReferenceFilterRequestsProperties] to discover more keywords like `cookie-path`.</span></span>

### <a name="dock-to-left-from-the-command-menu"></a><span data-ttu-id="246b3-224">Ancrer à gauche à partir du menu Commande</span><span class="sxs-lookup"><span data-stu-id="246b3-224">Dock to left from the Command Menu</span></span>  

<span data-ttu-id="246b3-225">Ouvrez [le menu Commande][DevToolsCommandMenuIndex] et exécutez la commande pour déplacer `Dock to left` DevTools à gauche de votreport d’affichage.</span><span class="sxs-lookup"><span data-stu-id="246b3-225">Open the [Command Menu][DevToolsCommandMenuIndex] and run the `Dock to left` command to move DevTools to the left of your viewport.</span></span>  

:::image type="complex" source="../../media/2020/03/dock-to-left.msft.png" alt-text="DevTools docked to the left of the viewport" lightbox="../../media/2020/03/dock-to-left.msft.png":::
   <span data-ttu-id="246b3-227">DevTools docked to the left of the viewport</span><span class="sxs-lookup"><span data-stu-id="246b3-227">DevTools docked to the left of the viewport</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="246b3-228">La fonctionnalité Station **d’accueil** vers la gauche est disponible depuis Microsoft Edge 75, mais elle était auparavant accessible uniquement à partir du [menu principal.][DevtoolsCustomizePlacementsChangeMainMenu]</span><span class="sxs-lookup"><span data-stu-id="246b3-228">The **Dock to left** feature has been available since Microsoft Edge 75, but it was previously only accessible from the [Main Menu][DevtoolsCustomizePlacementsChangeMainMenu].</span></span>  <span data-ttu-id="246b3-229">La nouvelle fonctionnalité de Microsoft Edge 83 est que vous pouvez désormais accéder à cette fonctionnalité à partir du menu Commande.</span><span class="sxs-lookup"><span data-stu-id="246b3-229">The new feature in Microsoft Edge 83 is that you may now access this feature from the Command Menu.</span></span>  

<span data-ttu-id="246b3-230">Envoyez vos commentaires en [tweetant][PostTweetEdgeDevTools] ou en cinglant [l’icône Envoyer des](#getting-in-touch-with-microsoft-edge-devtools-team) commentaires !</span><span class="sxs-lookup"><span data-stu-id="246b3-230">Send your feedback by [tweeting][PostTweetEdgeDevTools] orchoosing the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="246b3-231">Problème de chrome [#1011679][CR1011679]</span><span class="sxs-lookup"><span data-stu-id="246b3-231">Chromium issue [#1011679][CR1011679]</span></span>  

### <a name="the-audits-panel-is-now-the-lighthouse-panel"></a><span data-ttu-id="246b3-232">Le panneau Audits est désormais le panneau Panneau de sélection</span><span class="sxs-lookup"><span data-stu-id="246b3-232">The Audits panel is now the Lighthouse panel</span></span>  

<span data-ttu-id="246b3-233">L’équipe DevTools a fréquemment reçu des commentaires des développeurs web qui ont dit que même s’il était possible d’exécuter [Lasser][GithubGoogleChromeLighthouse] à partir de DevTools, lorsqu’ils l’ont essayé, ils n’ont pas pu trouver le panneau « Course », de sorte que le panneau **Audits** est désormais le panneau DevTools. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="246b3-233">The DevTools team frequently got feedback from web developers that while it was possible to run [Lighthouse][GithubGoogleChromeLighthouse] from DevTools, when they tried it out they were not able to find the "Lighthouse" panel, so the **Audits** panel is now the **Lighthouse** panel.</span></span>  

:::image type="complex" source="../../media/2020/03/lighthouse.msft.png" alt-text="Panneau de sélection" lightbox="../../media/2020/03/lighthouse.msft.png":::
   <span data-ttu-id="246b3-235">Panneau de sélection</span><span class="sxs-lookup"><span data-stu-id="246b3-235">The Lighthouse panel</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="246b3-236">Le **panneau Panneau de** panneau fournit des liens vers du contenu hébergé sur des sites web tiers.</span><span class="sxs-lookup"><span data-stu-id="246b3-236">The **Lighthouse** panel provides links to content hosted on third-party websites.</span></span>  <span data-ttu-id="246b3-237">Microsoft n’est pas responsable et n’a aucun contrôle sur le contenu de ces sites et les données qu’ils peuvent collecter.</span><span class="sxs-lookup"><span data-stu-id="246b3-237">Microsoft is not responsible for and has no control over the content of these sites and any data they may collect.</span></span>  

### <a name="delete-all-local-overrides-in-a-folder"></a><span data-ttu-id="246b3-238">Supprimer toutes les substitutions locales dans un dossier</span><span class="sxs-lookup"><span data-stu-id="246b3-238">Delete all Local Overrides in a folder</span></span>  

<span data-ttu-id="246b3-239">Après avoir mis en place les **substitutions locales,** vous pouvez pointer sur un répertoire, ouvrir le menu contextuel \(clic droit\) et choisir la nouvelle option Supprimer toutes les substitutions pour supprimer toutes les **substitutions** locales dans ce dossier.</span><span class="sxs-lookup"><span data-stu-id="246b3-239">After setting up **Local Overrides** you may hover on a directory, open the contextual menu \(right-click\), and choose the new **Delete all overrides** option to delete all Local Overrides in that folder.</span></span>  

:::image type="complex" source="../../media/2020/03/overrides.msft.png" alt-text="Supprimer toutes les substitutions" lightbox="../../media/2020/03/overrides.msft.png":::
   <span data-ttu-id="246b3-241">Supprimer toutes les substitutions</span><span class="sxs-lookup"><span data-stu-id="246b3-241">Delete all overrides</span></span>  
:::image-end:::  

<span data-ttu-id="246b3-242">Envoyez vos commentaires en [tweetant][PostTweetEdgeDevTools] ou en cinglant [l’icône Envoyer des](#getting-in-touch-with-microsoft-edge-devtools-team) commentaires !</span><span class="sxs-lookup"><span data-stu-id="246b3-242">Send your feedback by [tweeting][PostTweetEdgeDevTools] orchoosing the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="246b3-243">Problème de chrome [#1016501][CR1016501]</span><span class="sxs-lookup"><span data-stu-id="246b3-243">Chromium issue [#1016501][CR1016501]</span></span>  

### <a name="updated-long-tasks-ui"></a><span data-ttu-id="246b3-244">Interface utilisateur des tâches longues mise à jour</span><span class="sxs-lookup"><span data-stu-id="246b3-244">Updated Long tasks UI</span></span>  

<span data-ttu-id="246b3-245">Une **tâche longue** est du code JavaScript qui a pour effet de bloquer le thread principal pendant une longue période, ce qui entraîne le blocage d’une page web.</span><span class="sxs-lookup"><span data-stu-id="246b3-245">A **Long Task** is JavaScript code that monopolizes the main thread for a long time, causing a web page to freeze.</span></span>  

<span data-ttu-id="246b3-246">Vous pouvez visualiser [][DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity] les tâches longues dans le panneau Performances depuis un certain temps, mais dans Microsoft Edge 83, l’interface utilisateur de visualisation des tâches longues dans le panneau Performances a été mise à jour.</span><span class="sxs-lookup"><span data-stu-id="246b3-246">You have been able to [visualize Long Tasks in the Performance panel][DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity] for a while now, but in Microsoft Edge 83 the Long Task visualization UI in the Performance panel has been updated.</span></span>  <span data-ttu-id="246b3-247">La partie Tâche longue d’une tâche est maintenant colorée avec un arrière-plan rouge à bandes.</span><span class="sxs-lookup"><span data-stu-id="246b3-247">The Long Task portion of a task is now colored with a striped red background.</span></span>  

:::image type="complex" source="../../media/2020/03/long-task.msft.png" alt-text="Nouvelle interface utilisateur de tâche longue" lightbox="../../media/2020/03/long-task.msft.png":::
   <span data-ttu-id="246b3-249">Nouvelle interface utilisateur de tâche longue</span><span class="sxs-lookup"><span data-stu-id="246b3-249">The new Long Task UI</span></span>  
:::image-end:::  

<span data-ttu-id="246b3-250">Envoyez vos commentaires en [tweetant][PostTweetEdgeDevTools] ou en cinglant [l’icône Envoyer des](#getting-in-touch-with-microsoft-edge-devtools-team) commentaires !</span><span class="sxs-lookup"><span data-stu-id="246b3-250">Send your feedback by [tweeting][PostTweetEdgeDevTools] orchoosing the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="246b3-251">Problème de chrome [#1054447][CR1054447]</span><span class="sxs-lookup"><span data-stu-id="246b3-251">Chromium issue [#1054447][CR1054447]</span></span>  

### <a name="maskable-icon-support-in-the-manifest-pane"></a><span data-ttu-id="246b3-252">Prise en charge des icônes masquées dans le volet manifeste</span><span class="sxs-lookup"><span data-stu-id="246b3-252">Maskable icon support in the Manifest pane</span></span>  

<span data-ttu-id="246b3-253">Android Oreo a introduit des icônes adaptatives, qui affichent les icônes d’application sous différentes formes sur différents modèles d’appareil.</span><span class="sxs-lookup"><span data-stu-id="246b3-253">Android Oreo introduced adaptive icons, which display app icons in a variety of shapes across different device models.</span></span>  <span data-ttu-id="246b3-254">**Les icônes masquées** sont un nouveau format d’icône qui permet de prendre en charge les icônes adaptatives, ce qui vous permet de vous assurer que votre icône [PWA][ProgressiveWebAppsChromiumIndex] s’adapte bien sur les appareils qui assurent la prise en charge de la norme des icônes masquées.</span><span class="sxs-lookup"><span data-stu-id="246b3-254">**Maskable icons** are a new icon format that support adaptive icons, which enable you to ensure that your [PWA][ProgressiveWebAppsChromiumIndex] icon looks good on devices that support the maskable icons standard.</span></span>  

<span data-ttu-id="246b3-255">Activez la nouvelle case à cocher Afficher uniquement \*\*\*\* la zone sécurisée minimale pour les **icônes** masquées dans le volet manifeste pour vérifier que votre icône masquée s’affiche bien sur les appareils Android Oreo.</span><span class="sxs-lookup"><span data-stu-id="246b3-255">Enable the new **Show only the minimum safe area for maskable icons** checkbox in the **Manifest** pane to check that your maskable icon looks good on Android Oreo devices.</span></span>  

<!-- Check out [Are my current icons ready?] to learn more.  -->  

:::image type="complex" source="../../media/2020/03/maskable-icons.msft.png" alt-text="Afficher uniquement la zone sécurisée minimale pour la case à cocher des icônes masquées" lightbox="../../media/2020/03/maskable-icons.msft.png":::
   <span data-ttu-id="246b3-257">La case à cocher Afficher uniquement **la zone sécurisée minimale pour les icônes masquées**</span><span class="sxs-lookup"><span data-stu-id="246b3-257">The **Show only the minimum safe area for maskable icons** checkbox</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="246b3-258">Cette fonctionnalité a été lancée dans Microsoft Edge 81.</span><span class="sxs-lookup"><span data-stu-id="246b3-258">This feature launched in Microsoft Edge 81.</span></span>  <span data-ttu-id="246b3-259">Les mises à jour couvertes ici dans Microsoft Edge 83 n’ont pas été couvertes dans [Nouveautés de DevTools (Microsoft Edge 81).][WhatsNew81]</span><span class="sxs-lookup"><span data-stu-id="246b3-259">The updates covered here in Microsoft Edge 83 were not covered in [What's New In DevTools (Microsoft Edge 81)][WhatsNew81].</span></span>  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="246b3-260">Télécharger les canaux d’aperçu Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="246b3-260">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="246b3-261">Si vous utilisez Windows ou macOS, envisagez d’utiliser les canaux d’aperçu [Microsoft Edge][MicrosoftEdgePreviewChannels] comme navigateur de développement par défaut.</span><span class="sxs-lookup"><span data-stu-id="246b3-261">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="246b3-262">Les canaux d’aperçu vous permettent d’accéder aux dernières fonctionnalités de DevTools.</span><span class="sxs-lookup"><span data-stu-id="246b3-262">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="246b3-263">Contacter l’équipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="246b3-263">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[WhatsNew81]: ../01/devtools.md "Nouveautés de DevTools (Microsoft Edge 81) | Documents Microsoft"  

[DevToolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Exécuter des commandes avec le menu de commandes Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsCssReferenceColorPicker]: /microsoft-edge/devtools-guide-chromium/css/reference#change-colors-with-the-color-picker "Modifier les couleurs à l'| Documents Microsoft"  
[DevtoolsCssIndex]: /microsoft-edge/devtools-guide-chromium/css/index "Mise en place de l’affichage et de la modification des | Documents Microsoft"  
[DevtoolsCustomizePlacementsChangeMainMenu]: /microsoft-edge/devtools-guide-chromium/customize/placement#change-placement-from-the-main-menu "Modifier l’emplacement à partir du menu | Documents Microsoft"  
[DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#view-main-thread-activity "Afficher l’activité du thread principal | Documents Microsoft"  
[DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Analyser les performances de rendu à l'| Documents Microsoft"  
[ProgressiveWebAppsChromiumIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Applications web progressives sur Windows | Documents Microsoft"  
[DevtoolsRemoteDebuggingWindows]: /microsoft-edge/devtools-guide-chromium/remote-debugging/windows "Mise en place du débogage à distance des appareils Windows 10 | Documents Microsoft"  
[DevtoolsJavascriptBreakpointsLineCode]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints#line-of-code-breakpoints "Points d’arrêt de ligne de code : comment suspendre votre code avec des points d’arrêt dans Microsoft Edge DevTools | Documents Microsoft"
[DevtoolsNetworkReferenceFilterRequestsProperties]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties "Filtrer les demandes par propriétés : référence de l’analyse réseau | Documents Microsoft"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Paramètres : personnaliser l'| Microsoft Edge DevTools Documents Microsoft"  

[WindowsUwpDebugTestPerfDevicePortal]: /windows/uwp/debug-test-perf/device-portal "Vue d’ensemble de Windows Device Portal"  

[RemoteTools]: https://www.microsoft.com/store/apps/9P6CMFV44ZLT "Outils à distance pour Microsoft Edge (bêta)"  
[MicrosoftStore]: https://www.microsoft.com/store/apps/windows "Microsoft Store"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canaux d’aperçu Microsoft Edge"  

[WindowsBlogStableRelease]: https://blogs.windows.com/msedgedev/2020/03/20 "Mise à jour sur les canaux stables pour Microsoft Edge"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[DevTools%20Docs%20Feedback] "Nouveau problème - MicrosoftDocs/Edge-développeur-GitHub"  

[MicrosoftVisualstudio]: https://visualstudio.microsoft.com "Visual Studio"  

[VisualstudioCode]: https://code.visualstudio.com "Code Visual Studio"  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Publier un Tweet"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools Twitter"  
[TheWebWeWant]: https://webwewant.fyi "Le site Web de votre choix"  

[ColorBlindnessTypes]: http://www.colourblindawareness.org/colour-blindness/types-of-colour-blindness "Types de daltonisme"  

[MDNAcceptLanguage]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Accept-Language "Accept-Language | MDN"  
[MDNCookiePath]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie#Directives "Set-Cookie | MDN"  

[MathiasByensLocaleDemo]: https://mathiasbynens.be/demo/locale "Exemple de code dépendant des paramètres régionaux"  

[CR963183]: https://crbug.com/963183 "Problème 963183 : Les devTools ne sont pas conformes WCAG"  
[CR1003700]: https://crbug.com/1003700 "Problème 1003700 : ajout de la prise en charge de DevTools pour la simulation de problèmes de vision des couleurs"  
[CR1011679]: https://crbug.com/1011679 "Problème 1011679 : introduire « Ancrer à gauche » à l’aide du menu Commande"  
[CR1016501]: https://crbug.com/1016501 "Problème 1016501 : Demande de fonctionnalité : bouton pour supprimer toutes les substitutions locales"  
[CR1050999]: https://crbug.com/1050999 "Problème 1050999 : onglet Propriétés"  
[CR1051466]: https://crbug.com/1051466 "Problème 1051466 : prise en charge du débogage BIP/COEP dans DevTools"  
[CR1054447]: https://crbug.com/1054447 "Problème 1054447 : mettre à jour les mesures de performances dans la chronologie DevTools"  
[CR1051822]: https://crbug.com/1051822 "Problème 1051822 : DevTools : ajouter une interface utilisateur pour émuler les paramètres régionaux"
[CR1041830]: https://crbug.com/1041830 "Problème 1041830 : Améliorer les couleurs des points d’arrêt"
[CR1050855]: https://crbug.com/1050855 "Problème 1050855 : l’affichage Paramètres est difficile à découvrir"
[CR1056348]: https://crbug.com/1056348 "Problème 1056348 : Actualisation des composants de la barre d’informations"

[COOP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.tu4hyy6v12wn "EXPLICATION ET COEP - Stratégie d’ouverture d’origine croisée"  
[COEP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.uo6kivyh0ge2 "EXPLICATION ET COEP - Stratégie d’incorporation d’origine croisée"  

[GithubGoogleChromeLighthouse]: https://github.com/GoogleChrome/lighthouse "| GitHub"  

> [!NOTE]
> <span data-ttu-id="246b3-305">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="246b3-305">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="246b3-306">La page d’origine est disponible [ici](https://developers.google.com/web/updates/2020/03/devtools/index) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="246b3-306">The original page is found [here](https://developers.google.com/web/updates/2020/03/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="246b3-308">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="246b3-308">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
