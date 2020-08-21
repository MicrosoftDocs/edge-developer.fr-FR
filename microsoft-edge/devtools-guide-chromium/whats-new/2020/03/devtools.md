---
title: Nouveautés de DevTools (Microsoft Edge 83)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: f1b5d147aac1b8b527cc7365f9f91a2a7974863e
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942224"
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

# <span data-ttu-id="71642-103">Nouveautés de DevTools (Microsoft Edge 83)</span><span class="sxs-lookup"><span data-stu-id="71642-103">What's New In DevTools (Microsoft Edge 83)</span></span>  

<span data-ttu-id="71642-104">Suite à la mise à jour de la planification de chrome, nous devons nous ajuster notre planning pour les versions à venir de Microsoft Edge et en annulant la version 82 de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="71642-104">Following the updated Chromium schedule, we are adjusting our schedule for upcoming Microsoft Edge releases and cancelling the Microsoft Edge 82 release.</span></span> <span data-ttu-id="71642-105">Pour plus d’informations, consultez le [billet de blog][WindowsBlogStableRelease] .</span><span class="sxs-lookup"><span data-stu-id="71642-105">Check out our [blog post][WindowsBlogStableRelease] for more info.</span></span>  

<span data-ttu-id="71642-106">Voici les nouvelles fonctionnalités disponibles dans le DevTools de Microsoft Edge 83.</span><span class="sxs-lookup"><span data-stu-id="71642-106">Here are the new features available in the DevTools in Microsoft Edge 83.</span></span>  

## <span data-ttu-id="71642-107">Annonces de l’équipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="71642-107">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="71642-108">Les sections suivantes répertorient les annonces que vous pouvez avoir manquées de l’équipe Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="71642-108">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team!</span></span> <span data-ttu-id="71642-109">Découvrez-les pour essayer de nouvelles fonctionnalités dans les extensions de code DevTools, VS, etc.</span><span class="sxs-lookup"><span data-stu-id="71642-109">Check them out to try new features in the DevTools, VS Code extensions, and more.</span></span>  <span data-ttu-id="71642-110">Pour vous tenir au courant de toutes les fonctionnalités les plus récentes et les plus récentes de vos outils de développement, téléchargez les [canaux Microsoft Edge Preview][MicrosoftEdgePreviewChannels] et [Suivez-nous sur Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="71642-110">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <span data-ttu-id="71642-111">Déboguer à distance Microsoft Edge sur les appareils Windows 10</span><span class="sxs-lookup"><span data-stu-id="71642-111">Remotely debug Microsoft Edge on Windows 10 Devices</span></span>  

<span data-ttu-id="71642-112">L’application [outils de contrôle à distance pour Microsoft Edge \ (Beta)][RemoteTools] est désormais disponible dans le [Microsoft Store][MicrosoftStore].</span><span class="sxs-lookup"><span data-stu-id="71642-112">The [Remote Tools for Microsoft Edge \(Beta\)][RemoteTools] app is now available in the [Microsoft Store][MicrosoftStore].</span></span>  <span data-ttu-id="71642-113">À l’aide de cette application, qui étend [Windows Device Portal][WindowsUwpDebugTestPerfDevicePortal], vous pouvez vous connecter à partir de l’instance de Microsoft Edge qui s’exécute sur votre ordinateur de développement sur un appareil Windows 10 distant, afficher une liste des cibles \ (tous les onglets dans Microsoft Edge et [PWAS][PprgressiveWebAppsChromiumIndex] s’ouvrent sur l’appareil Windows 10) et utiliser devtools sur votre ordinateur de développement sur une cible qui s’exécute sur</span><span class="sxs-lookup"><span data-stu-id="71642-113">Using this app, which extends the [Windows Device Portal][WindowsUwpDebugTestPerfDevicePortal], you are able to connect from the instance of Microsoft Edge running on your development machine to a remote Windows 10 device, see a list of targets \(all tabs in Microsoft Edge and [PWAs][PprgressiveWebAppsChromiumIndex] open on the Windows 10 device\), and use the DevTools on your development machine against a target running on the remote Windows 10 device.</span></span>  

:::image type="complex" source="../../media/2020/03/remote-tools.msft.png" alt-text="Application outils de contrôle à distance pour Microsoft Edge (Beta) disponible dans le Microsoft Store" lightbox="../../media/2020/03/remote-tools.msft.png":::
   <span data-ttu-id="71642-115">Figure 1: application [outils de contrôle à distance pour Microsoft Edge (Beta)][RemoteTools] disponible dans le [Microsoft Store][MicrosoftStore]</span><span class="sxs-lookup"><span data-stu-id="71642-115">Figure 1:  The [Remote Tools for Microsoft Edge (Beta)][RemoteTools] app available in the [Microsoft Store][MicrosoftStore]</span></span>  
:::image-end:::  

<span data-ttu-id="71642-116">[Consultez notre guide de configuration de votre appareil Windows 10 et de votre ordinateur de développement pour le débogage à distance][DevtoolsRemoteDebuggingWindows].</span><span class="sxs-lookup"><span data-stu-id="71642-116">[Read our guide for setting up your Windows 10 device and your development machine for remote debugging][DevtoolsRemoteDebuggingWindows].</span></span>  <span data-ttu-id="71642-117">Donnez-nous votre avis concernant le débogage à distance par le biais de [Tweet][PostTweetEdgeDevTools] ou en cliquant sur l’icône d' [envoi de commentaires](#getting-in-touch-with-microsoft-edge-devtools-team) .</span><span class="sxs-lookup"><span data-stu-id="71642-117">Let us know about your remote debugging experience by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

### <span data-ttu-id="71642-118">Nouvelles méthodes d’accès aux paramètres</span><span class="sxs-lookup"><span data-stu-id="71642-118">New ways to access Settings</span></span>  

<span data-ttu-id="71642-119">Il existe de nombreux paramètres pour le DevTools que vous pouvez personnaliser pour améliorer l’aspect et l’apparence de DevTools, ainsi que les tâches dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="71642-119">There are tons of settings for the DevTools that you are able to customize to make the DevTools look, feel, and work the way you need.</span></span> <span data-ttu-id="71642-120">Dans Microsoft Edge 83, il est désormais plus facile d’accéder aux [paramètres][DevtoolsCustomizeIndexSettings] dans le devtools.</span><span class="sxs-lookup"><span data-stu-id="71642-120">In Microsoft Edge 83, accessing [Settings][DevtoolsCustomizeIndexSettings] in the DevTools is now much easier.</span></span> <span data-ttu-id="71642-121">Ouvrez les paramètres à l’aide de l’icône d’engrenage en regard des alertes de console et du menu principal.</span><span class="sxs-lookup"><span data-stu-id="71642-121">Open Settings with the gear icon next to Console alerts and the main menu.</span></span>  

:::image type="complex" source="../../media/2020/03/settings.msft.png" alt-text="L’icône d’engrenage s’ouvre pour afficher les paramètres dans le DevTools" lightbox="../../media/2020/03/settings.msft.png":::
   <span data-ttu-id="71642-123">Figure 2: l’icône d’engrenage s’ouvre pour afficher les **paramètres** dans le devtools</span><span class="sxs-lookup"><span data-stu-id="71642-123">Figure 2:  The gear icon opens **Settings** in the DevTools</span></span>  
:::image-end:::  

<span data-ttu-id="71642-124">Vous pouvez également ouvrir les [paramètres][DevtoolsCustomizeIndexSettings] à partir du **menu principal** sous **autres outils**.</span><span class="sxs-lookup"><span data-stu-id="71642-124">You are also able to open [Settings][DevtoolsCustomizeIndexSettings] from the **Main Menu** under **More tools**.</span></span>

:::image type="complex" source="../../media/2020/03/settings2.msft.png" alt-text="Menu principal > plus d’outils > paramètres" lightbox="../../media/2020/03/settings2.msft.png":::
   <span data-ttu-id="71642-126">Figure 3: **menu principal**  >  **plus**  >  **paramètres** d’outils</span><span class="sxs-lookup"><span data-stu-id="71642-126">Figure 3:  **Main Menu** > **More tools** > **Settings**</span></span>  
:::image-end:::  

<span data-ttu-id="71642-127">[#1050855][CR1050855] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="71642-127">Chromium issue [#1050855][CR1050855]</span></span>

### <span data-ttu-id="71642-128">Infobars nouveau et amélioré</span><span class="sxs-lookup"><span data-stu-id="71642-128">New and improved infobars</span></span>

<span data-ttu-id="71642-129">Les barres de notification d’information \ (infobars \) dans DevTools présentent désormais une meilleure interface et de nouvelles fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="71642-129">Informational notification bars \(infobars\) in DevTools now have an improved look and more functionality.</span></span> <span data-ttu-id="71642-130">Dans Microsoft Edge 83, infobars est plus facile à lire et à proposer des boutons pour vous permettre d’effectuer l’action appropriée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="71642-130">In Microsoft Edge 83, infobars are easier to read and provide buttons so you are able to take the relevant action right away.</span></span>  

:::image type="complex" source="../../media/2020/03/infobar.msft.png" alt-text="Barre d’informations pour l’impression d’un fichier minified dans Microsoft Edge 83" lightbox="../../media/2020/03/infobar.msft.png":::
   <span data-ttu-id="71642-132">Figure 4: barre d’informations pour l’impression d’un fichier minified dans Microsoft Edge version 83</span><span class="sxs-lookup"><span data-stu-id="71642-132">Figure 4:  Infobar for pretty-printing a minified file in Microsoft Edge Version 83</span></span>  
:::image-end:::  

<span data-ttu-id="71642-133">[#1056348][CR1056348] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="71642-133">Chromium issue [#1056348][CR1056348]</span></span>

### <span data-ttu-id="71642-134">Parcourir le sélecteur de couleurs à l’aide du clavier</span><span class="sxs-lookup"><span data-stu-id="71642-134">Navigate the Color Picker with your keyboard</span></span>  

<span data-ttu-id="71642-135">Le [Sélecteur de couleurs][DevtoolsCssReferenceColorPicker] est une interface utilisateur du [panneau éléments][DevtoolsCssIndex] permettant de changer et de faire des `color` `background-color` déclarations.</span><span class="sxs-lookup"><span data-stu-id="71642-135">The [Color Picker][DevtoolsCssReferenceColorPicker] is a GUI in the [Elements panel][DevtoolsCssIndex] for changing `color` and `background-color` declarations.</span></span>  <span data-ttu-id="71642-136">Dans les versions précédentes de Microsoft Edge, vous ne parvenez pas à naviguer dans la section **nuances** du [Sélecteur de couleur][DevtoolsCssReferenceColorPicker] à l’aide du clavier.</span><span class="sxs-lookup"><span data-stu-id="71642-136">In previous versions of Microsoft Edge, you were not able to navigate the **Shades** section of the [Color Picker][DevtoolsCssReferenceColorPicker] with the keyboard.</span></span>  

:::image type="complex" source="../../media/2020/03/color-picker.msft.png" alt-text="Vous pouvez maintenant utiliser votre clavier pour déplacer le sélecteur dans la section nuances du sélecteur de couleurs." lightbox="../../media/2020/03/color-picker.msft.png":::
   <span data-ttu-id="71642-138">Figure 5: vous pouvez maintenant utiliser votre clavier pour déplacer le sélecteur dans la section **tons** du [Sélecteur de couleurs][DevtoolsCssReferenceColorPicker]</span><span class="sxs-lookup"><span data-stu-id="71642-138">Figure 5:  You are now able to use your keyboard to move the selector in the **Shades** section of the [Color Picker][DevtoolsCssReferenceColorPicker]</span></span>  
:::image-end:::  

<span data-ttu-id="71642-139">Dans Microsoft Edge 83, vous pouvez maintenant utiliser le clavier pour déplacer le sélecteur dans la section **tons** du sélecteur de couleurs.</span><span class="sxs-lookup"><span data-stu-id="71642-139">In Microsoft Edge 83, you are now able to use the keyboard to move the selector in the **Shades** section of the Color Picker.</span></span>  

<span data-ttu-id="71642-140">[#963183][CR963183] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="71642-140">Chromium issue [#963183][CR963183]</span></span>  

### <span data-ttu-id="71642-141">L’onglet Propriétés est désormais rempli après une actualisation de page</span><span class="sxs-lookup"><span data-stu-id="71642-141">Properties tab now populates after a page refresh</span></span>  

<span data-ttu-id="71642-142">Dans Microsoft Edge 81 et les versions antérieures, l' **onglet Propriétés** dans le [panneau éléments][DevtoolsCssIndex] a été rompu par l’actualisation de la page.</span><span class="sxs-lookup"><span data-stu-id="71642-142">In Microsoft Edge 81 and earlier, the **Properties tab** in the [Elements panel][DevtoolsCssIndex] was broken by page refreshes.</span></span>  <span data-ttu-id="71642-143">Lorsque vous actualisez la page, l' **onglet Propriétés** ne remplissait pas les propriétés de l’élément actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="71642-143">When you refreshed the page, the **Properties tab** did not populate the properties of the currently-selected element.</span></span>  

:::image type="complex" source="../../media/2020/03/properties-in-81.msft.png" alt-text="Dans Microsoft Edge 81 et versions antérieures, l’onglet Propriétés était vide après une actualisation de page" lightbox="../../media/2020/03/properties-in-81.msft.png":::
   <span data-ttu-id="71642-145">Figure 6: image de l' **onglet Propriétés** dans Microsoft Edge 81 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="71642-145">Figure 6:  In Microsoft Edge 81 and earlier, the **Properties tab** was blank after a page refresh</span></span>  
:::image-end:::  

<span data-ttu-id="71642-146">Dans Microsoft Edge 83, vous pouvez désormais voir les propriétés de l’élément actuellement sélectionné après une actualisation de page dans l' **onglet Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="71642-146">In Microsoft Edge 83, you are now able to see the properties of the currently-selected element after a page refresh in the **Properties tab**.</span></span>  

:::image type="complex" source="../../media/2020/03/properties-in-82.msft.png" alt-text="Dans Microsoft Edge 83, l’onglet Propriétés affiche les propriétés de l’élément actuellement sélectionné après une actualisation de la page" lightbox="../../media/2020/03/properties-in-82.msft.png":::
   <span data-ttu-id="71642-148">Figure 7: dans le 83 Microsoft Edge, l' **onglet Propriétés** affiche les propriétés de l’élément actuellement sélectionné après une actualisation de la page</span><span class="sxs-lookup"><span data-stu-id="71642-148">Figure 7:  In Microsoft Edge 83, the **Properties tab** displays the properties of the currently-selected element after a page refresh</span></span>  
:::image-end:::  

<span data-ttu-id="71642-149">[#1050999][CR1050999] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="71642-149">Chromium issue [#1050999][CR1050999]</span></span>  

### <span data-ttu-id="71642-150">Utiliser les touches de direction pour faire défiler l’outil modifications</span><span class="sxs-lookup"><span data-stu-id="71642-150">Use the arrow keys to scroll in the Changes tool</span></span>  

<span data-ttu-id="71642-151">L' **outil modifications** effectue le suivi des modifications que vous avez apportées à CSS ou JavaScript dans le devtools.</span><span class="sxs-lookup"><span data-stu-id="71642-151">The **Changes tool** tracks any changes you have made to CSS or JavaScript in the DevTools.</span></span>  <span data-ttu-id="71642-152">Vous pouvez utiliser l' **outil modifications** pour afficher rapidement toutes vos modifications et revenir à votre éditeur/IDE.</span><span class="sxs-lookup"><span data-stu-id="71642-152">You are able to use the **Changes tool** to quickly see all your changes and take those back to your editor/IDE.</span></span>  

<span data-ttu-id="71642-153">Ouvrez l' **outil modifications** en appuyant sur `Ctrl` + `Shift` + `P` la devtools pour ouvrir le [menu de commandes][DevToolsCommandMenuIndex] et en tapant `changes` .</span><span class="sxs-lookup"><span data-stu-id="71642-153">Open the **Changes tool** by pressing `Ctrl`+`Shift`+`P` in the DevTools to open the [Command Menu][DevToolsCommandMenuIndex] and typing `changes`.</span></span>  <span data-ttu-id="71642-154">Activez et exécutez la commande **afficher les modifications** pour ouvrir l' **outil modifications** dans le tiroir devtools.</span><span class="sxs-lookup"><span data-stu-id="71642-154">Select and run the **Show Changes** command to open the **Changes tool** in the DevTools drawer.</span></span>  

<span data-ttu-id="71642-155">Lorsque vous avez apporté une modification à un fichier minified, l' **outil modifications** vous permet de faire défiler horizontalement pour afficher l’ensemble de votre code minified.</span><span class="sxs-lookup"><span data-stu-id="71642-155">When you have made a change to a minified file, the **Changes tool** enables you to scroll horizontally to see all of your minified code.</span></span>  <span data-ttu-id="71642-156">À partir de Microsoft Edge 83, vous pouvez à présent faire défiler les touches de direction de votre clavier.</span><span class="sxs-lookup"><span data-stu-id="71642-156">Starting in Microsoft Edge 83, you may now scroll horizontally using the arrow keys on your keyboard.</span></span>  

:::image type="complex" source="../../media/2020/03/changes.msft.png" alt-text="Dans Microsoft Edge 83, vous pouvez faire défiler horizontalement avec les touches de direction pour afficher votre code minified dans l’outil modifications." lightbox="../../media/2020/03/changes.msft.png":::
   <span data-ttu-id="71642-158">Figure 8: dans Microsoft Edge 83, vous pouvez faire défiler horizontalement avec les touches de direction pour voir les modifications que vous avez apportées à votre code minified dans l' **outil modifications** .</span><span class="sxs-lookup"><span data-stu-id="71642-158">Figure 8:  In Microsoft Edge 83, you may scroll horizontally with the arrow keys to see the changes you made to your minified code in the **Changes tool**</span></span>  
:::image-end:::  

<span data-ttu-id="71642-159">Si vous utilisez un lecteur d’écran ou le clavier pour naviguer dans DevTools, envoyez-nous vos commentaires en nous appuyant sur un [Tweet][PostTweetEdgeDevTools] ou en cliquant sur l’icône d' [envoi de commentaires](#getting-in-touch-with-microsoft-edge-devtools-team) .</span><span class="sxs-lookup"><span data-stu-id="71642-159">If you use screen readers or the keyboard to navigate around the DevTools, send us your feedback by [tweeting][PostTweetEdgeDevTools] at us or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="71642-160">[#963183][CR963183] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="71642-160">Chromium issue [#963183][CR963183]</span></span>  

## <span data-ttu-id="71642-161">Annonces du projet de chrome</span><span class="sxs-lookup"><span data-stu-id="71642-161">Announcements from the Chromium project</span></span>  

<span data-ttu-id="71642-162">Les sections suivantes annoncent des fonctionnalités supplémentaires disponibles dans Microsoft Edge 83 qui ont été fournies au projet de chrome Open source.</span><span class="sxs-lookup"><span data-stu-id="71642-162">The following sections announce additional features available in Microsoft Edge 83 that were contributed to the open source Chromium project.</span></span>  

### <span data-ttu-id="71642-163">Émuler les déficiences de la vision</span><span class="sxs-lookup"><span data-stu-id="71642-163">Emulate vision deficiencies</span></span>  

<span data-ttu-id="71642-164">Ouvrez l' [onglet rendu][DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab] , puis utilisez la nouvelle fonctionnalité **émuler les déficiences** de la vision pour mieux comprendre comment les personnes présentant différents types d’déficiences de la vision connaissent votre site.</span><span class="sxs-lookup"><span data-stu-id="71642-164">Open the [Rendering tab][DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab] and use the new **Emulate vision deficiencies** feature to get a better idea of how people with different types of vision deficiencies experience your site.</span></span>  

:::image type="complex" source="../../media/2020/03/vision.msft.png" alt-text="Émulation d’une vision floue" lightbox="../../media/2020/03/vision.msft.png":::
   <span data-ttu-id="71642-166">Figure 9: émulation d’une vision floue</span><span class="sxs-lookup"><span data-stu-id="71642-166">Figure 9:  Emulating blurred vision</span></span>  
:::image-end:::  

<span data-ttu-id="71642-167">DevTools est en mesure d’émuler une vision floue et des [types de troubles de la vision couleur][ColorBlindnessTypes]suivants.</span><span class="sxs-lookup"><span data-stu-id="71642-167">DevTools is able to emulate blurred vision and the following [types of color vision deficiencies][ColorBlindnessTypes].</span></span>  

| <span data-ttu-id="71642-168">Déficience de la vision couleur</span><span class="sxs-lookup"><span data-stu-id="71642-168">Color Vision Deficiency</span></span> | <span data-ttu-id="71642-169">Détails</span><span class="sxs-lookup"><span data-stu-id="71642-169">Details</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="71642-170">Protanopia</span><span class="sxs-lookup"><span data-stu-id="71642-170">Protanopia</span></span> | <span data-ttu-id="71642-171">L’impossibilité de percevoir des lumières rouges.</span><span class="sxs-lookup"><span data-stu-id="71642-171">The inability to perceive any red light.</span></span> |  
| <span data-ttu-id="71642-172">Deuteranopia</span><span class="sxs-lookup"><span data-stu-id="71642-172">Deuteranopia</span></span> | <span data-ttu-id="71642-173">L’impossibilité de percevoir une lumière verte.</span><span class="sxs-lookup"><span data-stu-id="71642-173">The inability to perceive any green light.</span></span> |  
| <span data-ttu-id="71642-174">Tritanopia</span><span class="sxs-lookup"><span data-stu-id="71642-174">Tritanopia</span></span> | <span data-ttu-id="71642-175">L’impossibilité de percevoir une lumière bleue.</span><span class="sxs-lookup"><span data-stu-id="71642-175">The inability to perceive any blue light.</span></span> |  
| <span data-ttu-id="71642-176">Achromatopsia</span><span class="sxs-lookup"><span data-stu-id="71642-176">Achromatopsia</span></span> | <span data-ttu-id="71642-177">L’impossibilité de percevoir une couleur, à l’exception des nuances de gris.</span><span class="sxs-lookup"><span data-stu-id="71642-177">The inability to perceive any color, except for shades of grey \(extremely rare\).</span></span> |  

<span data-ttu-id="71642-178">Il existe des versions moins extrêmes de ces déficiences de vision couleur, et en fait, elles sont plus courantes.</span><span class="sxs-lookup"><span data-stu-id="71642-178">Less extreme versions of these color vision deficiencies exist, and in fact they are more common.</span></span>  
<span data-ttu-id="71642-179">Par exemple, protanomaly est une sensibilité réduite de l’éclairage rouge (par opposition à protanopia, qui est la possibilité d’obtenir une lumière rouge).</span><span class="sxs-lookup"><span data-stu-id="71642-179">For example, protanomaly is a reduced sensitivity to red light (as opposed to protanopia, which is the complete inability to perceive red light).</span></span> <span data-ttu-id="71642-180">Toutefois, ces déficiences en matière de vision omaly n’ont pas été aussi clairement définies: chaque personne ayant une déficience de la vision est différente et peut voir ce qui se passe d’un point de vue différent (il est en mesure de percevoir plus ou moins des couleurs pertinentes).</span><span class="sxs-lookup"><span data-stu-id="71642-180">However, these -omaly vision deficiencies are not as clearly defined: every person with such a vision deficiency is different and might see things differently (being able to perceive more/less of the relevant colors).</span></span>  

<span data-ttu-id="71642-181">En concevant des simulations plus extrêmes dans DevTools, il est garanti que les applications Web sont accessibles aux personnes utilisant protanomaly, Deuteranomaly, tritanomaly et achromatomaly.</span><span class="sxs-lookup"><span data-stu-id="71642-181">By designing for the more extreme simulations in DevTools, your web apps are guaranteed to be accessible to people with protanomaly, deuteranomaly, tritanomaly, and achromatomaly as well.</span></span>  

<span data-ttu-id="71642-182">Envoyez vos commentaires en utilisant un [tweetation][PostTweetEdgeDevTools] ou en cliquant sur l’icône d' [envoi de commentaires](#getting-in-touch-with-microsoft-edge-devtools-team) .</span><span class="sxs-lookup"><span data-stu-id="71642-182">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="71642-183">[#1003700][CR1003700] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="71642-183">Chromium issue [#1003700][CR1003700]</span></span>  

### <span data-ttu-id="71642-184">Émuler des paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="71642-184">Emulate locales</span></span>  

<span data-ttu-id="71642-185">Émulez des paramètres régionaux en définissant un **Sensors**emplacement dans la  >  **zone**capteurs.</span><span class="sxs-lookup"><span data-stu-id="71642-185">Emulate locales by setting a location in **Sensors** > **Location**.</span></span> <span data-ttu-id="71642-186">[Ouvrez le **menu de commandes** ][DevToolsCommandMenuIndex] et tapez `Sensors` pour accéder à l’onglet **capteurs** .  Après avoir effectué ces actions, DevTools modifie les paramètres régionaux par défaut actuels en affectant le code suivant.</span><span class="sxs-lookup"><span data-stu-id="71642-186">[Open the **Command Menu**][DevToolsCommandMenuIndex] and type `Sensors` to access the **Sensors** tab.  After performing these actions, DevTools modifies the current default locale, affecting the following code.</span></span>  

*   `Intl.*` <span data-ttu-id="71642-187">Par exemple:</span><span class="sxs-lookup"><span data-stu-id="71642-187">APIs, for example:</span></span> `new Intl.NumberFormat().resolvedOptions().locale`  
*   <span data-ttu-id="71642-188">Autres API JavaScript prenant en charge des paramètres régionaux tels que `String.prototype.localeCompare` et `*.prototype.toLocaleString` , par exemple:</span><span class="sxs-lookup"><span data-stu-id="71642-188">Other locale-aware JavaScript APIs such as `String.prototype.localeCompare` and `*.prototype.toLocaleString`, for example:</span></span> `123_456..toLocaleString()`  
*   <span data-ttu-id="71642-189">API DOM telles que `navigator.language` et</span><span class="sxs-lookup"><span data-stu-id="71642-189">DOM APIs such as `navigator.language` and</span></span> `navigator.languages`  
*   <span data-ttu-id="71642-190">[`Accept-Language`][MDNAcceptLanguage]En-tête de requête http</span><span class="sxs-lookup"><span data-stu-id="71642-190">The [`Accept-Language`][MDNAcceptLanguage] HTTP request header</span></span>  

> [!NOTE]
> <span data-ttu-id="71642-191">Les mises à jour de `navigator.language` et ne `navigator.languages` sont pas visibles immédiatement, mais uniquement après la prochaine navigation ou actualisation de page.</span><span class="sxs-lookup"><span data-stu-id="71642-191">Updates to `navigator.language` and `navigator.languages` are not visible immediately, but only after the next navigation or page refresh.</span></span>  <span data-ttu-id="71642-192">Les modifications apportées à l' `Accept-Language` en-tête http sont uniquement répercutées pour les demandes suivantes.</span><span class="sxs-lookup"><span data-stu-id="71642-192">Changes to the `Accept-Language` HTTP header are only reflected for subsequent requests.</span></span>  

:::image type="complex" source="../../media/2020/03/locale.msft.png" alt-text="Émulation d’un paramètre régional" lightbox="../../media/2020/03/locale.msft.png":::
   <span data-ttu-id="71642-194">Figure 10: émulation d’un paramètre régional</span><span class="sxs-lookup"><span data-stu-id="71642-194">Figure 10:  Emulating a locale</span></span>  
:::image-end:::  

<span data-ttu-id="71642-195">Pour essayer une démonstration, voir [exemple de code dépendant des paramètres régionaux][MathiasByensLocaleDemo].</span><span class="sxs-lookup"><span data-stu-id="71642-195">To try a demo, see [Locale-dependent code example][MathiasByensLocaleDemo].</span></span>

<span data-ttu-id="71642-196">[#1051822][CR1051822] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="71642-196">Chromium issue [#1051822][CR1051822]</span></span>

### <span data-ttu-id="71642-197">Débogage de la stratégie d’intégration COEP (Cross-Origin)</span><span class="sxs-lookup"><span data-stu-id="71642-197">Cross-Origin Embedder Policy (COEP) debugging</span></span>  

<span data-ttu-id="71642-198">Le panneau réseau fournit désormais des informations de débogage de la [stratégie d’incorporation][COEP] à l’origine.</span><span class="sxs-lookup"><span data-stu-id="71642-198">The Network panel now provides [Cross-Origin Embedder Policy][COEP] debugging information.</span></span>  

<span data-ttu-id="71642-199">La colonne **État** donne désormais une explication rapide de la raison pour laquelle une requête a été bloquée ainsi qu’un lien pour afficher les en-têtes de cette requête pour un débogage supplémentaire:</span><span class="sxs-lookup"><span data-stu-id="71642-199">The **Status** column now provides a quick explanation of why a request was blocked as well as a link to view the headers of that request for further debugging:</span></span>  

:::image type="complex" source="../../media/2020/03/status.msft.png" alt-text="Demandes bloquées dans la colonne \* \* Status \* \*" lightbox="../../media/2020/03/status.msft.png":::
   <span data-ttu-id="71642-201">Figure 11: demandes bloquées dans la colonne État</span><span class="sxs-lookup"><span data-stu-id="71642-201">Figure 11:  Blocked requests in the Status column</span></span>  
:::image-end:::  

<span data-ttu-id="71642-202">La section **en-têtes de réponse** de l’onglet **en-têtes** fournit davantage d’instructions pour résoudre les problèmes:</span><span class="sxs-lookup"><span data-stu-id="71642-202">The **Response Headers** section of the **Headers** tab provides more guidance on how to resolve the issues:</span></span>  

:::image type="complex" source="../../media/2020/03/guidance.msft.png" alt-text="Conseils supplémentaires dans la section en-têtes de réponse" lightbox="../../media/2020/03/guidance.msft.png":::
   <span data-ttu-id="71642-204">Figure 12: conseils supplémentaires dans la section en-têtes de réponse</span><span class="sxs-lookup"><span data-stu-id="71642-204">Figure 12:  More guidance in the Response Headers section</span></span>  
:::image-end:::  

<span data-ttu-id="71642-205">Envoyez vos commentaires en utilisant un [tweetation][PostTweetEdgeDevTools] ou en cliquant sur l’icône d' [envoi de commentaires](#getting-in-touch-with-microsoft-edge-devtools-team) .</span><span class="sxs-lookup"><span data-stu-id="71642-205">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="71642-206">[#1051466][CR1051466] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="71642-206">Chromium issue [#1051466][CR1051466]</span></span>  

### <span data-ttu-id="71642-207">Nouvelles icônes pour les points d’arrêt, les points d’arrêt conditionnel et la logpoints</span><span class="sxs-lookup"><span data-stu-id="71642-207">New icons for breakpoints, conditional breakpoints, and logpoints</span></span>  

<span data-ttu-id="71642-208">Le panneau sources comporte de nouvelles icônes pour les points d’arrêt, les points d’arrêt conditionnel et logpoints:</span><span class="sxs-lookup"><span data-stu-id="71642-208">The Sources panel has new icons for breakpoints, conditional breakpoints, and logpoints:</span></span>  

*   <span data-ttu-id="71642-209">Points d’arrêt \ (</span><span class="sxs-lookup"><span data-stu-id="71642-209">Breakpoints \(</span></span>![Interruption](../../media/2020/03/breakpoint.msft.png)<span data-ttu-id="71642-211">\) sont représentés par des cercles rouges.</span><span class="sxs-lookup"><span data-stu-id="71642-211">\) are represented by red circles.</span></span>  
*   <span data-ttu-id="71642-212">Points d’arrêt conditionnels</span><span class="sxs-lookup"><span data-stu-id="71642-212">Conditional Breakpoints \(</span></span>![Point d’arrêt conditionnel](../../media/2020/03/conditional.msft.png)<span data-ttu-id="71642-214">\) sont représentés par des cercles demi-rouges.</span><span class="sxs-lookup"><span data-stu-id="71642-214">\) are represented by half-red half-white circles.</span></span>  
*   <span data-ttu-id="71642-215">Logpoints \(</span><span class="sxs-lookup"><span data-stu-id="71642-215">Logpoints \(</span></span>![Logpoint](../../media/2020/03/logpoint.msft.png)<span data-ttu-id="71642-217">\) sont représentés par des cercles rouges grâce aux icônes de la console.</span><span class="sxs-lookup"><span data-stu-id="71642-217">\) are represented by red circles with Console icons.</span></span>  

<span data-ttu-id="71642-218">La motivation des nouvelles icônes fut de rendre l’interface utilisateur plus cohérente avec les autres outils de débogage de l’interface utilisateur (qui sont généralement des points d’arrêt de couleur rouges \) et de faciliter la distinction entre les trois fonctionnalités en un clin d’œil.</span><span class="sxs-lookup"><span data-stu-id="71642-218">The motivation for the new icons was to make the UI more consistent with other GUI debugging tools \(which usually color breakpoints red\) and to make it easier to distinguish between the 3 features at a glance.</span></span>  

<span data-ttu-id="71642-219">[#1041830][CR1041830] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="71642-219">Chromium issue [#1041830][CR1041830]</span></span>  

### <span data-ttu-id="71642-220">Afficher les requêtes réseau qui définissent un chemin de cookie spécifique</span><span class="sxs-lookup"><span data-stu-id="71642-220">View network requests that set a specific cookie path</span></span>  

<span data-ttu-id="71642-221">Utilisez le nouveau `cookie-path` mot clé de filtre dans le panneau **réseau** pour vous concentrer sur les requêtes réseau qui définissent un [chemin de cookie][MDNCookiePath]spécifique.</span><span class="sxs-lookup"><span data-stu-id="71642-221">Use the new `cookie-path` filter keyword in the **Network** panel to focus on the network requests that set a specific [cookie path][MDNCookiePath].</span></span>  

<span data-ttu-id="71642-222">Consultez les [demandes de filtre par propriétés][DevtoolsNetworkReferenceFilterRequestsProperties] pour découvrir d’autres mots clés comme `cookie-path` .</span><span class="sxs-lookup"><span data-stu-id="71642-222">Check out [Filter requests by properties][DevtoolsNetworkReferenceFilterRequestsProperties] to discover more keywords like `cookie-path`.</span></span>

### <span data-ttu-id="71642-223">Ancrer à gauche à partir du menu de commandes</span><span class="sxs-lookup"><span data-stu-id="71642-223">Dock to left from the Command Menu</span></span>  

<span data-ttu-id="71642-224">Ouvrez le [menu de commandes][DevToolsCommandMenuIndex] et exécutez la `Dock to left` commande pour déplacer devtools à gauche de votre fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="71642-224">Open the [Command Menu][DevToolsCommandMenuIndex] and run the `Dock to left` command to move DevTools to the left of your viewport.</span></span>  

:::image type="complex" source="../../media/2020/03/dock-to-left.msft.png" alt-text="DevTools ancré à gauche de la fenêtre d’affichage" lightbox="../../media/2020/03/dock-to-left.msft.png":::
   <span data-ttu-id="71642-226">Figure 13: DevTools fixé à gauche de la fenêtre d’affichage</span><span class="sxs-lookup"><span data-stu-id="71642-226">Figure 13:  DevTools docked to the left of the viewport</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="71642-227">La fonctionnalité **ancrer à gauche** est disponible depuis Microsoft Edge 75, mais elle n’est auparavant accessible qu’à partir du [**menu principal**][DevtoolsCustomizePlacementsChangeMainMenu].</span><span class="sxs-lookup"><span data-stu-id="71642-227">The **Dock to left** feature has been available since Microsoft Edge 75, but it was previously only accessible from the [**Main Menu**][DevtoolsCustomizePlacementsChangeMainMenu].</span></span>  <span data-ttu-id="71642-228">La nouvelle fonctionnalité de Microsoft Edge 83 est que vous pouvez maintenant accéder à cette fonctionnalité à partir du menu de commandes.</span><span class="sxs-lookup"><span data-stu-id="71642-228">The new feature in Microsoft Edge 83 is that you may now access this feature from the Command Menu.</span></span>  

<span data-ttu-id="71642-229">Envoyez vos commentaires en utilisant un [tweetation][PostTweetEdgeDevTools] ou en cliquant sur l’icône d' [envoi de commentaires](#getting-in-touch-with-microsoft-edge-devtools-team) .</span><span class="sxs-lookup"><span data-stu-id="71642-229">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="71642-230">[#1011679][CR1011679] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="71642-230">Chromium issue [#1011679][CR1011679]</span></span>  

### <span data-ttu-id="71642-231">Le panneau d’audit est désormais le panneau de signalisation.</span><span class="sxs-lookup"><span data-stu-id="71642-231">The Audits panel is now the Lighthouse panel</span></span>  

<span data-ttu-id="71642-232">L’équipe DevTools a fréquemment reçu des commentaires de la part des développeurs Web, alors qu’il était possible d’exécuter un [phare][GithubGoogleChromeLighthouse] à partir de devtools, **lorsque l’utilisateur** a essayé le panneau de configuration, il n’a pas été en mesure de trouver le panneau de **signalisation.**</span><span class="sxs-lookup"><span data-stu-id="71642-232">The DevTools team frequently got feedback from web developers that while it was possible to run [Lighthouse][GithubGoogleChromeLighthouse] from DevTools, when they tried it out they were not able to find the "Lighthouse" panel, so the **Audits** panel is now the **Lighthouse** panel.</span></span>  

:::image type="complex" source="../../media/2020/03/lighthouse.msft.png" alt-text="Panneau de signalisation" lightbox="../../media/2020/03/lighthouse.msft.png":::
   <span data-ttu-id="71642-234">Figure 14: panneau de signalisation</span><span class="sxs-lookup"><span data-stu-id="71642-234">Figure 14:  The Lighthouse panel</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="71642-235">Le panneau de **signalisation** comporte des liens vers du contenu hébergé sur des sites Web tiers.</span><span class="sxs-lookup"><span data-stu-id="71642-235">The **Lighthouse** panel provides links to content hosted on third-party websites.</span></span>  <span data-ttu-id="71642-236">Microsoft n’est pas responsable et n’a aucun contrôle sur le contenu de ces sites et sur les données qu’ils peuvent recueillir.</span><span class="sxs-lookup"><span data-stu-id="71642-236">Microsoft is not responsible for and has no control over the content of these sites and any data they may collect.</span></span>  

### <span data-ttu-id="71642-237">Supprimer tous les remplacements locaux dans un dossier</span><span class="sxs-lookup"><span data-stu-id="71642-237">Delete all Local Overrides in a folder</span></span>  

<span data-ttu-id="71642-238">Après avoir configuré les **remplacements locaux** , vous pouvez cliquer avec le bouton droit sur un dossier et sélectionner l’option **supprimer toutes les substitutions** dans ce dossier.</span><span class="sxs-lookup"><span data-stu-id="71642-238">After setting up **Local Overrides** you may right-click a folder and select the new **Delete all overrides** option to delete all Local Overrides in that folder.</span></span>  

:::image type="complex" source="../../media/2020/03/overrides.msft.png" alt-text="Supprimer tous les remplacements" lightbox="../../media/2020/03/overrides.msft.png":::
   <span data-ttu-id="71642-240">Figure 15: supprimer tous les remplacements</span><span class="sxs-lookup"><span data-stu-id="71642-240">Figure 15:  Delete all overrides</span></span>  
:::image-end:::  

<span data-ttu-id="71642-241">Envoyez vos commentaires en utilisant un [tweetation][PostTweetEdgeDevTools] ou en cliquant sur l’icône d' [envoi de commentaires](#getting-in-touch-with-microsoft-edge-devtools-team) .</span><span class="sxs-lookup"><span data-stu-id="71642-241">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="71642-242">[#1016501][CR1016501] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="71642-242">Chromium issue [#1016501][CR1016501]</span></span>  

### <span data-ttu-id="71642-243">Interface utilisateur de tâches longues mise à jour</span><span class="sxs-lookup"><span data-stu-id="71642-243">Updated Long tasks UI</span></span>  

<span data-ttu-id="71642-244">Une **tâche longue** correspond à du code JavaScript qui monopolit le thread principal pendant un certain temps, provoquant le gel d’une page Web.</span><span class="sxs-lookup"><span data-stu-id="71642-244">A **Long Task** is JavaScript code that monopolizes the main thread for a long time, causing a web page to freeze.</span></span>  

<span data-ttu-id="71642-245">Vous avez la possibilité de [visualiser de longs tâches dans le panneau de performance][DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity] pour un certain temps, mais dans Microsoft Edge 83, l’interface utilisateur d’une visualisation de tâches longues du panneau de performance a été mise à jour.</span><span class="sxs-lookup"><span data-stu-id="71642-245">You have been able to [visualize Long Tasks in the Performance panel][DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity] for a while now, but in Microsoft Edge 83 the Long Task visualization UI in the Performance panel has been updated.</span></span>  <span data-ttu-id="71642-246">La partie tâches longues d’une tâche est désormais colorée avec un arrière-plan rouge rayé.</span><span class="sxs-lookup"><span data-stu-id="71642-246">The Long Task portion of a task is now colored with a striped red background.</span></span>  

:::image type="complex" source="../../media/2020/03/long-task.msft.png" alt-text="Nouvelle interface utilisateur de tâche longue" lightbox="../../media/2020/03/long-task.msft.png":::
   <span data-ttu-id="71642-248">Figure 16: interface utilisateur de nouvelle tâche longue</span><span class="sxs-lookup"><span data-stu-id="71642-248">Figure 16:  The new Long Task UI</span></span>  
:::image-end:::  

<span data-ttu-id="71642-249">Envoyez vos commentaires en utilisant un [tweetation][PostTweetEdgeDevTools] ou en cliquant sur l’icône d' [envoi de commentaires](#getting-in-touch-with-microsoft-edge-devtools-team) .</span><span class="sxs-lookup"><span data-stu-id="71642-249">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="71642-250">[#1054447][CR1054447] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="71642-250">Chromium issue [#1054447][CR1054447]</span></span>  

### <span data-ttu-id="71642-251">Icône masquable dans le volet manifeste</span><span class="sxs-lookup"><span data-stu-id="71642-251">Maskable icon support in the Manifest pane</span></span>  

<span data-ttu-id="71642-252">Android Oreo introduit des icônes adaptatives qui affichent des icônes d’application dans différentes formes sur différents modèles d’appareil.</span><span class="sxs-lookup"><span data-stu-id="71642-252">Android Oreo introduced adaptive icons, which display app icons in a variety of shapes across different device models.</span></span>  <span data-ttu-id="71642-253">Les icônes qui peuvent être **masquées** sont un nouveau format d’icône qui prend en charge les icônes adaptatives, qui vous permettent de vous assurer que votre icône [PWA][PprgressiveWebAppsChromiumIndex] fonctionne correctement sur les appareils qui prennent en charge la norme d’icônes masquées.</span><span class="sxs-lookup"><span data-stu-id="71642-253">**Maskable icons** are a new icon format that support adaptive icons, which enable you to ensure that your [PWA][PprgressiveWebAppsChromiumIndex] icon looks good on devices that support the maskable icons standard.</span></span>  

<span data-ttu-id="71642-254">Activez la case à cocher nouveau **afficher uniquement la zone sécurisée minimum pour les icônes masquées** dans le volet **manifeste** pour vérifier que votre icône MASKABLE fonctionne correctement sur les appareils Android Oreo.</span><span class="sxs-lookup"><span data-stu-id="71642-254">Enable the new **Show only the minimum safe area for maskable icons** checkbox in the **Manifest** pane to check that your maskable icon looks good on Android Oreo devices.</span></span>  

<!-- Check out [Are my current icons ready?] to learn more.  -->  

:::image type="complex" source="../../media/2020/03/maskable-icons.msft.png" alt-text="Case à cocher Afficher uniquement la zone sécurisée minimum pour les icônes masquées" lightbox="../../media/2020/03/maskable-icons.msft.png":::
   <span data-ttu-id="71642-256">Figure 17: activez la case à cocher **afficher uniquement la zone sécurisée minimum pour les icônes masquées** .</span><span class="sxs-lookup"><span data-stu-id="71642-256">Figure 17:  The **Show only the minimum safe area for maskable icons** checkbox</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="71642-257">Cette fonctionnalité est lancée dans Microsoft Edge 81.</span><span class="sxs-lookup"><span data-stu-id="71642-257">This feature launched in Microsoft Edge 81.</span></span>  <span data-ttu-id="71642-258">Les mises à jour abordées ici dans Microsoft Edge 83 n’ont pas été abordées dans [les nouveautés de devtools (Microsoft edge 81)][WhatsNew81].</span><span class="sxs-lookup"><span data-stu-id="71642-258">The updates covered here in Microsoft Edge 83 were not covered in [What's New In DevTools (Microsoft Edge 81)][WhatsNew81].</span></span>  

## <span data-ttu-id="71642-259">Télécharger les canaux Microsoft Edge preview</span><span class="sxs-lookup"><span data-stu-id="71642-259">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="71642-260">Si vous utilisez Windows ou macOS, envisagez d’utiliser les [canaux Microsoft Edge Preview][MicrosoftEdgePreviewChannels] comme navigateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="71642-260">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="71642-261">Les canaux d’aperçu vous permettent d’accéder aux dernières fonctionnalités de DevTools.</span><span class="sxs-lookup"><span data-stu-id="71642-261">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="71642-262">Contacter l’équipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="71642-262">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Publiez un tweet"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools compte Twitter"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[DevTools%20Docs%20Feedback] "Nouveau problème-MicrosoftDocs/Edge-développeur-GitHub"  
[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canaux Microsoft Edge preview"  
[TheWebWeWant]: https://webwewant.fyi "Le site Web de votre choix"  

[WhatsNew81]: ../01/devtools.md "Nouveautés de DevTools (Microsoft Edge 81) | Documents Microsoft"  

[DevToolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Exécuter des commandes à l’aide du menu de commandes de Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsCssReferenceColorPicker]: /microsoft-edge/devtools-guide-chromium/css/reference#change-colors-with-the-color-picker "Changer les couleurs avec le sélecteur de couleurs | Documents Microsoft"  
[DevtoolsCssIndex]: /microsoft-edge/devtools-guide-chromium/css/index "Découvrir comment afficher et modifier des feuilles CSS | Documents Microsoft"  
[DevtoolsCustomizePlacementsChangeMainMenu]: /microsoft-edge/devtools-guide-chromium/customize/placement#change-placement-from-the-main-menu "Changer le positionnement dans le menu principal | Documents Microsoft"  
[DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#view-main-thread-activity "Afficher l’activité du thread principal | Documents Microsoft"  
[DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Analyser les performances de rendu à l’aide de l’onglet rendu | Documents Microsoft"  
[PprgressiveWebAppsChromiumIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Applications Web progressives sur Windows | Documents Microsoft"  
[DevtoolsRemoteDebuggingWindows]: /microsoft-edge/devtools-guide-chromium/remote-debugging/windows "Commencer à utiliser le débogage à distance des appareils Windows 10 | Documents Microsoft"  
[DevtoolsJavascriptBreakpointsLineCode]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints#line-of-code-breakpoints "Points d’arrêt de la ligne de code: comment mettre en pause votre code avec des points d’arrêt dans Microsoft Edge DevTools | Documents Microsoft"
[DevtoolsNetworkReferenceFilterRequestsProperties]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties "Demandes de filtre par propriétés-référence d’analyse du réseau | Documents Microsoft"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Paramètres-personnaliser Microsoft Edge DevTools | Documents Microsoft"  

[WindowsUwpDebugTestPerfDevicePortal]: /windows/uwp/debug-test-perf/device-portal "Vue d’ensemble de Windows Device Portal"  

[RemoteTools]: https://www.microsoft.com/store/apps/9P6CMFV44ZLT "Outils de contrôle à distance pour Microsoft Edge (bêta)"  
[MicrosoftStore]: https://www.microsoft.com/store/apps/windows "Microsoft Store"  

[WindowsBlogStableRelease]: https://blogs.windows.com/msedgedev/2020/03/20 "Mise à jour sur les versions de canal stable pour Microsoft Edge"

[MicrosoftVisualstudio]: https://visualstudio.microsoft.com "Visual Studio"  

[VisualstudioCode]: https://code.visualstudio.com "Code Visual Studio"  

[ColorBlindnessTypes]: http://www.colourblindawareness.org/colour-blindness/types-of-colour-blindness "Types de cécité du Colour"  
[MDNAcceptLanguage]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Accept-Language "Accept-Language"
[MathiasByensLocaleDemo]: https://mathiasbynens.be/demo/locale "Exemple de code dépendant des paramètres régionaux"
[MDNCookiePath]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie#Directives

[CR963183]: https://crbug.com/963183 "Problème 963183: DevTools n’est pas conforme à la norme WCAG"  
[CR1003700]: https://crbug.com/1003700 "Problème 1003700: ajout de la prise en charge de DevTools pour la simulation d’déficience de vision couleur"  
[CR1011679]: https://crbug.com/1011679 "Problème 1011679: Introduisez l’option ancrer à gauche dans le menu de commandes"  
[CR1016501]: https://crbug.com/1016501 "Problème 1016501: demande de fonctionnalité: bouton permettant de supprimer tous les remplacements locaux"  
[CR1050999]: https://crbug.com/1050999 "Problème 1050999: onglet Propriétés"  
[CR1051466]: https://crbug.com/1051466 "Problème 1051466: prendre en charge le débogage de COOP/COEP dans DevTools"  
[CR1054447]: https://crbug.com/1054447 "Problème 1054447: mettre à jour les métriques de performance dans DevTools Timeline"  
[CR1051822]: https://crbug.com/1051822 "Problème 1051822: DevTools: ajouter une interface utilisateur pour émuler des paramètres régionaux"
[CR1041830]: https://crbug.com/1041830 "Problème 1041830: améliorer les couleurs pour les points d’arrêt"
[CR1050855]: https://crbug.com/1050855 "Problème 1050855: l’affichage des paramètres est difficile à découvrir"
[CR1056348]: https://crbug.com/1056348 "Problème 1056348: actualisation du composant barre d’informations"

[COOP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.tu4hyy6v12wn "Explication de COOP et de COEP-explication-la politique d’ouverture"  
[COEP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.uo6kivyh0ge2 "Explication de la stratégie d’intégration de COOP et COEP"  

[GithubGoogleChromeLighthouse]: https://github.com/GoogleChrome/lighthouse "Phare GitHub référentiel Samples"  

> [!NOTE]
> <span data-ttu-id="71642-303">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="71642-303">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="71642-304">La page d’origine est disponible [ici](https://developers.google.com/web/updates/2020/03/devtools/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="71642-304">The original page is found [here](https://developers.google.com/web/updates/2020/03/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="71642-306">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="71642-306">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
