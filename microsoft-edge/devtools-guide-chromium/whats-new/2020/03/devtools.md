---
title: Nouveautés de DevTools (Microsoft Edge 83)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: ab3df52708febd4928c7e4ac41a77713370b9fa1
ms.sourcegitcommit: a34858dd3260967ba9699842fa839c7a94775fe4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/12/2020
ms.locfileid: "10710377"
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

# <span data-ttu-id="c9d0c-103">Nouveautés de DevTools (Microsoft Edge 83)</span><span class="sxs-lookup"><span data-stu-id="c9d0c-103">What's New In DevTools (Microsoft Edge 83)</span></span>  

<span data-ttu-id="c9d0c-104">Suite à la mise à jour de la planification de chrome, nous devons nous ajuster notre planning pour les versions à venir de Microsoft Edge et en annulant la version 82 de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-104">Following the updated Chromium schedule, we are adjusting our schedule for upcoming Microsoft Edge releases and cancelling the Microsoft Edge 82 release.</span></span> <span data-ttu-id="c9d0c-105">Pour plus d’informations, consultez le [billet de blog][WindowsBlogStableRelease] .</span><span class="sxs-lookup"><span data-stu-id="c9d0c-105">Check out our [blog post][WindowsBlogStableRelease] for more info.</span></span>  

<span data-ttu-id="c9d0c-106">Voici les nouvelles fonctionnalités disponibles dans le DevTools de Microsoft Edge 83.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-106">Here are the new features available in the DevTools in Microsoft Edge 83.</span></span>  

## <span data-ttu-id="c9d0c-107">Annonces de l’équipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="c9d0c-107">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="c9d0c-108">Les sections suivantes répertorient les annonces que vous pouvez avoir manquées de l’équipe Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-108">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team!</span></span> <span data-ttu-id="c9d0c-109">Découvrez-les pour essayer de nouvelles fonctionnalités dans les extensions de code DevTools, VS, etc.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-109">Check them out to try new features in the DevTools, VS Code extensions, and more.</span></span>  <span data-ttu-id="c9d0c-110">Pour vous tenir au courant de toutes les fonctionnalités les plus récentes et les plus récentes de vos outils de développement, téléchargez les [canaux Microsoft Edge Preview][MicrosoftEdgePreviewChannels] et [Suivez-nous sur Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="c9d0c-110">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <span data-ttu-id="c9d0c-111">Déboguer à distance Microsoft Edge sur les appareils Windows 10</span><span class="sxs-lookup"><span data-stu-id="c9d0c-111">Remotely debug Microsoft Edge on Windows 10 Devices</span></span>  

<span data-ttu-id="c9d0c-112">L’application [outils de contrôle à distance pour Microsoft Edge \ (Beta)][RemoteTools] est désormais disponible dans le [Microsoft Store][MicrosoftStore].</span><span class="sxs-lookup"><span data-stu-id="c9d0c-112">The [Remote Tools for Microsoft Edge \(Beta\)][RemoteTools] app is now available in the [Microsoft Store][MicrosoftStore].</span></span>  <span data-ttu-id="c9d0c-113">À l’aide de cette application, qui étend [Windows Device Portal][WindowsDevicePortal], vous pouvez vous connecter à partir de l’instance de Microsoft Edge qui s’exécute sur votre ordinateur de développement sur un appareil Windows 10 distant, afficher une liste des cibles \ (tous les onglets dans Microsoft Edge et [PWAS][PWADoc] s’ouvrent sur l’appareil Windows 10) et utiliser devtools sur votre ordinateur de développement sur une cible qui s’exécute sur</span><span class="sxs-lookup"><span data-stu-id="c9d0c-113">Using this app, which extends the [Windows Device Portal][WindowsDevicePortal], you are able to connect from the instance of Microsoft Edge running on your development machine to a remote Windows 10 device, see a list of targets \(all tabs in Microsoft Edge and [PWAs][PWADoc] open on the Windows 10 device\), and use the DevTools on your development machine against a target running on the remote Windows 10 device.</span></span>  

:::image type="complex" source="../../media/2020/03/remote-tools.msft.png" alt-text="Application outils de contrôle à distance pour Microsoft Edge (Beta) disponible dans le Microsoft Store" lightbox="../../media/2020/03/remote-tools.msft.png":::
   <span data-ttu-id="c9d0c-115">Figure 1: application [outils de contrôle à distance pour Microsoft Edge (Beta)][RemoteTools] disponible dans le [Microsoft Store][MicrosoftStore]</span><span class="sxs-lookup"><span data-stu-id="c9d0c-115">Figure 1:  The [Remote Tools for Microsoft Edge (Beta)][RemoteTools] app available in the [Microsoft Store][MicrosoftStore]</span></span>  
:::image-end:::  

<span data-ttu-id="c9d0c-116">[Consultez notre guide de configuration de votre appareil Windows 10 et de votre ordinateur de développement pour le débogage à distance][RemoteDebuggingWin10].</span><span class="sxs-lookup"><span data-stu-id="c9d0c-116">[Read our guide for setting up your Windows 10 device and your development machine for remote debugging][RemoteDebuggingWin10].</span></span>  <span data-ttu-id="c9d0c-117">Donnez-nous votre avis concernant le débogage à distance par le biais du [Tweet][PostTweetEdgeDevTools] ou en cliquant sur l’icône de [Commentaires](#feedback) .</span><span class="sxs-lookup"><span data-stu-id="c9d0c-117">Let us know about your remote debugging experience by [tweeting][PostTweetEdgeDevTools] or clicking the [Feedback](#feedback) icon!</span></span>  

### <span data-ttu-id="c9d0c-118">Nouvelles méthodes d’accès aux paramètres</span><span class="sxs-lookup"><span data-stu-id="c9d0c-118">New ways to access Settings</span></span>  

<span data-ttu-id="c9d0c-119">Il existe de nombreux paramètres pour le DevTools que vous pouvez personnaliser pour améliorer l’aspect et l’apparence de DevTools, ainsi que les tâches dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-119">There are tons of settings for the DevTools that you are able to customize to make the DevTools look, feel, and work the way you need.</span></span> <span data-ttu-id="c9d0c-120">Dans Microsoft Edge 83, il est désormais plus facile d’accéder aux [paramètres][OverviewSettings] dans le devtools.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-120">In Microsoft Edge 83, accessing [Settings][OverviewSettings] in the DevTools is now much easier.</span></span> <span data-ttu-id="c9d0c-121">Ouvrez les paramètres à l’aide de l’icône d’engrenage en regard des alertes de console et du menu principal.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-121">Open Settings with the gear icon next to Console alerts and the main menu.</span></span>  

:::image type="complex" source="../../media/2020/03/settings.msft.png" alt-text="L’icône d’engrenage s’ouvre pour afficher les paramètres dans le DevTools" lightbox="../../media/2020/03/settings.msft.png":::
   <span data-ttu-id="c9d0c-123">Figure 2: l’icône d’engrenage s’ouvre pour afficher les **paramètres** dans le devtools</span><span class="sxs-lookup"><span data-stu-id="c9d0c-123">Figure 2:  The gear icon opens **Settings** in the DevTools</span></span>  
:::image-end:::  

<span data-ttu-id="c9d0c-124">Vous pouvez également ouvrir les [paramètres][OverviewSettings] à partir du **menu principal** sous **autres outils**.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-124">You are also able to open [Settings][OverviewSettings] from the **Main Menu** under **More tools**.</span></span>

:::image type="complex" source="../../media/2020/03/settings2.msft.png" alt-text="Menu principal > plus d’outils > paramètres" lightbox="../../media/2020/03/settings2.msft.png":::
   <span data-ttu-id="c9d0c-126">Figure 3: **menu principal**  >  **plus**  >  **paramètres** d’outils</span><span class="sxs-lookup"><span data-stu-id="c9d0c-126">Figure 3:  **Main Menu** > **More tools** > **Settings**</span></span>  
:::image-end:::  

<span data-ttu-id="c9d0c-127">[#1050855][crbug1050855] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="c9d0c-127">Chromium issue [#1050855][crbug1050855]</span></span>

### <span data-ttu-id="c9d0c-128">Infobars nouveau et amélioré</span><span class="sxs-lookup"><span data-stu-id="c9d0c-128">New and improved infobars</span></span>

<span data-ttu-id="c9d0c-129">Les barres de notification d’information \ (infobars \) dans DevTools présentent désormais une meilleure interface et de nouvelles fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-129">Informational notification bars \(infobars\) in DevTools now have an improved look and more functionality.</span></span> <span data-ttu-id="c9d0c-130">Dans Microsoft Edge 83, infobars est plus facile à lire et à proposer des boutons pour vous permettre d’effectuer l’action appropriée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-130">In Microsoft Edge 83, infobars are easier to read and provide buttons so you are able to take the relevant action right away.</span></span>  

:::image type="complex" source="../../media/2020/03/infobar.msft.png" alt-text="Barre d’informations pour l’impression d’un fichier minified dans Microsoft Edge 83" lightbox="../../media/2020/03/infobar.msft.png":::
   <span data-ttu-id="c9d0c-132">Figure 4: barre d’informations pour l’impression d’un fichier minified dans Microsoft Edge version 83</span><span class="sxs-lookup"><span data-stu-id="c9d0c-132">Figure 4:  Infobar for pretty-printing a minified file in Microsoft Edge Version 83</span></span>  
:::image-end:::  

<span data-ttu-id="c9d0c-133">[#1056348][crbug1056348] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="c9d0c-133">Chromium issue [#1056348][crbug1056348]</span></span>

### <span data-ttu-id="c9d0c-134">Parcourir le sélecteur de couleurs à l’aide du clavier</span><span class="sxs-lookup"><span data-stu-id="c9d0c-134">Navigate the Color Picker with your keyboard</span></span>  

<span data-ttu-id="c9d0c-135">Le [Sélecteur de couleurs][ColorPicker] est une interface utilisateur du [panneau éléments][ElementsDoc] permettant de changer et de faire des `color` `background-color` déclarations.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-135">The [Color Picker][ColorPicker] is a GUI in the [Elements panel][ElementsDoc] for changing `color` and `background-color` declarations.</span></span>  <span data-ttu-id="c9d0c-136">Dans les versions précédentes de Microsoft Edge, vous ne parvenez pas à naviguer dans la section **nuances** du [Sélecteur de couleur][ColorPicker] à l’aide du clavier.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-136">In previous versions of Microsoft Edge, you were not able to navigate the **Shades** section of the [Color Picker][ColorPicker] with the keyboard.</span></span>  

:::image type="complex" source="../../media/2020/03/color-picker.msft.png" alt-text="Vous pouvez maintenant utiliser votre clavier pour déplacer le sélecteur dans la section nuances du sélecteur de couleurs." lightbox="../../media/2020/03/color-picker.msft.png":::
   <span data-ttu-id="c9d0c-138">Figure 5: vous pouvez maintenant utiliser votre clavier pour déplacer le sélecteur dans la section **tons** du [Sélecteur de couleurs][ColorPicker]</span><span class="sxs-lookup"><span data-stu-id="c9d0c-138">Figure 5:  You are now able to use your keyboard to move the selector in the **Shades** section of the [Color Picker][ColorPicker]</span></span>  
:::image-end:::  

<span data-ttu-id="c9d0c-139">Dans Microsoft Edge 83, vous pouvez maintenant utiliser le clavier pour déplacer le sélecteur dans la section **tons** du sélecteur de couleurs.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-139">In Microsoft Edge 83, you are now able to use the keyboard to move the selector in the **Shades** section of the Color Picker.</span></span>  

<span data-ttu-id="c9d0c-140">[#963183][crbug963183] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="c9d0c-140">Chromium issue [#963183][crbug963183]</span></span>  

### <span data-ttu-id="c9d0c-141">L’onglet Propriétés est désormais rempli après une actualisation de page</span><span class="sxs-lookup"><span data-stu-id="c9d0c-141">Properties tab now populates after a page refresh</span></span>  

<span data-ttu-id="c9d0c-142">Dans Microsoft Edge 81 et les versions antérieures, l' **onglet Propriétés** dans le [panneau éléments][ElementsDoc] a été rompu par l’actualisation de la page.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-142">In Microsoft Edge 81 and earlier, the **Properties tab** in the [Elements panel][ElementsDoc] was broken by page refreshes.</span></span>  <span data-ttu-id="c9d0c-143">Lorsque vous actualisez la page, l' **onglet Propriétés** ne remplissait pas les propriétés de l’élément actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-143">When you refreshed the page, the **Properties tab** did not populate the properties of the currently-selected element.</span></span>  

:::image type="complex" source="../../media/2020/03/properties-in-81.msft.png" alt-text="Dans Microsoft Edge 81 et versions antérieures, l’onglet Propriétés était vide après une actualisation de page" lightbox="../../media/2020/03/properties-in-81.msft.png":::
   <span data-ttu-id="c9d0c-145">Figure 6: image de l' **onglet Propriétés** dans Microsoft Edge 81 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="c9d0c-145">Figure 6:  In Microsoft Edge 81 and earlier, the **Properties tab** was blank after a page refresh</span></span>  
:::image-end:::  

<span data-ttu-id="c9d0c-146">Dans Microsoft Edge 83, vous pouvez désormais voir les propriétés de l’élément actuellement sélectionné après une actualisation de page dans l' **onglet Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-146">In Microsoft Edge 83, you are now able to see the properties of the currently-selected element after a page refresh in the **Properties tab**.</span></span>  

:::image type="complex" source="../../media/2020/03/properties-in-82.msft.png" alt-text="Dans Microsoft Edge 83, l’onglet Propriétés affiche les propriétés de l’élément actuellement sélectionné après une actualisation de la page" lightbox="../../media/2020/03/properties-in-82.msft.png":::
   <span data-ttu-id="c9d0c-148">Figure 7: dans le 83 Microsoft Edge, l' **onglet Propriétés** affiche les propriétés de l’élément actuellement sélectionné après une actualisation de la page</span><span class="sxs-lookup"><span data-stu-id="c9d0c-148">Figure 7:  In Microsoft Edge 83, the **Properties tab** displays the properties of the currently-selected element after a page refresh</span></span>  
:::image-end:::  

<span data-ttu-id="c9d0c-149">[#1050999][crbug1050999] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="c9d0c-149">Chromium issue [#1050999][crbug1050999]</span></span>  

### <span data-ttu-id="c9d0c-150">Utiliser les touches de direction pour faire défiler l’outil modifications</span><span class="sxs-lookup"><span data-stu-id="c9d0c-150">Use the arrow keys to scroll in the Changes tool</span></span>  

<span data-ttu-id="c9d0c-151">L' **outil modifications** effectue le suivi des modifications que vous avez apportées à CSS ou JavaScript dans le devtools.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-151">The **Changes tool** tracks any changes you have made to CSS or JavaScript in the DevTools.</span></span>  <span data-ttu-id="c9d0c-152">Vous pouvez utiliser l' **outil modifications** pour afficher rapidement toutes vos modifications et revenir à votre éditeur/IDE.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-152">You are able to use the **Changes tool** to quickly see all your changes and take those back to your editor/IDE.</span></span>  

<span data-ttu-id="c9d0c-153">Ouvrez l' **outil modifications** en appuyant sur `Ctrl` + `Shift` + `P` la devtools pour ouvrir le [menu de commandes][DevToolsCommandMenuIndex] et en tapant `changes` .</span><span class="sxs-lookup"><span data-stu-id="c9d0c-153">Open the **Changes tool** by pressing `Ctrl`+`Shift`+`P` in the DevTools to open the [Command Menu][DevToolsCommandMenuIndex] and typing `changes`.</span></span>  <span data-ttu-id="c9d0c-154">Activez et exécutez la commande **afficher les modifications** pour ouvrir l' **outil modifications** dans le tiroir devtools.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-154">Select and run the **Show Changes** command to open the **Changes tool** in the DevTools drawer.</span></span>  

<span data-ttu-id="c9d0c-155">Lorsque vous avez apporté une modification à un fichier minified, l' **outil modifications** vous permet de faire défiler horizontalement pour afficher l’ensemble de votre code minified.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-155">When you have made a change to a minified file, the **Changes tool** enables you to scroll horizontally to see all of your minified code.</span></span>  <span data-ttu-id="c9d0c-156">À partir de Microsoft Edge 83, vous pouvez à présent faire défiler les touches de direction de votre clavier.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-156">Starting in Microsoft Edge 83, you may now scroll horizontally using the arrow keys on your keyboard.</span></span>  

:::image type="complex" source="../../media/2020/03/changes.msft.png" alt-text="Dans Microsoft Edge 83, vous pouvez faire défiler horizontalement avec les touches de direction pour afficher votre code minified dans l’outil modifications." lightbox="../../media/2020/03/changes.msft.png":::
   <span data-ttu-id="c9d0c-158">Figure 8: dans Microsoft Edge 83, vous pouvez faire défiler horizontalement avec les touches de direction pour voir les modifications que vous avez apportées à votre code minified dans l' **outil modifications** .</span><span class="sxs-lookup"><span data-stu-id="c9d0c-158">Figure 8:  In Microsoft Edge 83, you may scroll horizontally with the arrow keys to see the changes you made to your minified code in the **Changes tool**</span></span>  
:::image-end:::  

<span data-ttu-id="c9d0c-159">Si vous utilisez un lecteur d’écran ou le clavier pour naviguer dans DevTools, envoyez-nous vos commentaires en nous appuyant sur un [Tweet][PostTweetEdgeDevTools] ou en cliquant sur l’icône de [Commentaires](#feedback) .</span><span class="sxs-lookup"><span data-stu-id="c9d0c-159">If you use screen readers or the keyboard to navigate around the DevTools, send us your feedback by [tweeting][PostTweetEdgeDevTools] at us or clicking the [Feedback](#feedback) icon!</span></span>  

<span data-ttu-id="c9d0c-160">[#963183][crbug963183] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="c9d0c-160">Chromium issue [#963183][crbug963183]</span></span>  

## <span data-ttu-id="c9d0c-161">Annonces du projet de chrome</span><span class="sxs-lookup"><span data-stu-id="c9d0c-161">Announcements from the Chromium project</span></span>  

<span data-ttu-id="c9d0c-162">Les sections suivantes annoncent des fonctionnalités supplémentaires disponibles dans Microsoft Edge 83 qui ont été fournies au projet de chrome Open source.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-162">The following sections announce additional features available in Microsoft Edge 83 that were contributed to the open source Chromium project.</span></span>  

### <span data-ttu-id="c9d0c-163">Émuler les déficiences de la vision</span><span class="sxs-lookup"><span data-stu-id="c9d0c-163">Emulate vision deficiencies</span></span>  

<span data-ttu-id="c9d0c-164">Ouvrez l' [onglet rendu][RenderingDoc] , puis utilisez la nouvelle fonctionnalité **émuler les déficiences** de la vision pour mieux comprendre comment les personnes présentant différents types d’déficiences de la vision connaissent votre site.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-164">Open the [Rendering tab][RenderingDoc] and use the new **Emulate vision deficiencies** feature to get a better idea of how people with different types of vision deficiencies experience your site.</span></span>  

:::image type="complex" source="../../media/2020/03/vision.msft.png" alt-text="Émulation d’une vision floue" lightbox="../../media/2020/03/vision.msft.png":::
   <span data-ttu-id="c9d0c-166">Figure 9: émulation d’une vision floue</span><span class="sxs-lookup"><span data-stu-id="c9d0c-166">Figure 9:  Emulating blurred vision</span></span>  
:::image-end:::  

<span data-ttu-id="c9d0c-167">DevTools est en mesure d’émuler une vision floue et des [types de troubles de la vision couleur][ColorBlindnessTypes]suivants.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-167">DevTools is able to emulate blurred vision and the following [types of color vision deficiencies][ColorBlindnessTypes].</span></span>  

| <span data-ttu-id="c9d0c-168">Déficience de la vision couleur</span><span class="sxs-lookup"><span data-stu-id="c9d0c-168">Color Vision Deficiency</span></span> | <span data-ttu-id="c9d0c-169">Détails</span><span class="sxs-lookup"><span data-stu-id="c9d0c-169">Details</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="c9d0c-170">Protanopia</span><span class="sxs-lookup"><span data-stu-id="c9d0c-170">Protanopia</span></span> | <span data-ttu-id="c9d0c-171">L’impossibilité de percevoir des lumières rouges.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-171">The inability to perceive any red light.</span></span> |  
| <span data-ttu-id="c9d0c-172">Deuteranopia</span><span class="sxs-lookup"><span data-stu-id="c9d0c-172">Deuteranopia</span></span> | <span data-ttu-id="c9d0c-173">L’impossibilité de percevoir une lumière verte.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-173">The inability to perceive any green light.</span></span> |  
| <span data-ttu-id="c9d0c-174">Tritanopia</span><span class="sxs-lookup"><span data-stu-id="c9d0c-174">Tritanopia</span></span> | <span data-ttu-id="c9d0c-175">L’impossibilité de percevoir une lumière bleue.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-175">The inability to perceive any blue light.</span></span> |  
| <span data-ttu-id="c9d0c-176">Achromatopsia</span><span class="sxs-lookup"><span data-stu-id="c9d0c-176">Achromatopsia</span></span> | <span data-ttu-id="c9d0c-177">L’impossibilité de percevoir une couleur, à l’exception des nuances de gris.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-177">The inability to perceive any color, except for shades of grey \(extremely rare\).</span></span> |  

<span data-ttu-id="c9d0c-178">Il existe des versions moins extrêmes de ces déficiences de vision couleur, et en fait, elles sont plus courantes.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-178">Less extreme versions of these color vision deficiencies exist, and in fact they are more common.</span></span>  
<span data-ttu-id="c9d0c-179">Par exemple, protanomaly est une sensibilité réduite de l’éclairage rouge (par opposition à protanopia, qui est la possibilité d’obtenir une lumière rouge).</span><span class="sxs-lookup"><span data-stu-id="c9d0c-179">For example, protanomaly is a reduced sensitivity to red light (as opposed to protanopia, which is the complete inability to perceive red light).</span></span> <span data-ttu-id="c9d0c-180">Toutefois, ces déficiences en matière de vision omaly n’ont pas été aussi clairement définies: chaque personne ayant une déficience de la vision est différente et peut voir ce qui se passe d’un point de vue différent (il est en mesure de percevoir plus ou moins des couleurs pertinentes).</span><span class="sxs-lookup"><span data-stu-id="c9d0c-180">However, these -omaly vision deficiencies are not as clearly defined: every person with such a vision deficiency is different and might see things differently (being able to perceive more/less of the relevant colors).</span></span>  

<span data-ttu-id="c9d0c-181">En concevant des simulations plus extrêmes dans DevTools, il est garanti que les applications Web sont accessibles aux personnes utilisant protanomaly, Deuteranomaly, tritanomaly et achromatomaly.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-181">By designing for the more extreme simulations in DevTools, your web apps are guaranteed to be accessible to people with protanomaly, deuteranomaly, tritanomaly, and achromatomaly as well.</span></span>  

<span data-ttu-id="c9d0c-182">Envoyez-nous vos commentaires en le [tweetant][PostTweetEdgeDevTools] ou en cliquant sur l’icône de [Commentaires](#feedback) .</span><span class="sxs-lookup"><span data-stu-id="c9d0c-182">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Feedback](#feedback) icon!</span></span>  

<span data-ttu-id="c9d0c-183">[#1003700][crbug1003700] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="c9d0c-183">Chromium issue [#1003700][crbug1003700]</span></span>  

### <span data-ttu-id="c9d0c-184">Émuler des paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="c9d0c-184">Emulate locales</span></span>  

<span data-ttu-id="c9d0c-185">Émulez des paramètres régionaux en définissant un **Sensors**emplacement dans la  >  **zone**capteurs.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-185">Emulate locales by setting a location in **Sensors** > **Location**.</span></span> <span data-ttu-id="c9d0c-186">[Ouvrez le **menu de commandes** ][DevToolsCommandMenuIndex] et tapez `Sensors` pour accéder à l’onglet **capteurs** .  Après avoir effectué ces actions, DevTools modifie les paramètres régionaux par défaut actuels en affectant le code suivant.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-186">[Open the **Command Menu**][DevToolsCommandMenuIndex] and type `Sensors` to access the **Sensors** tab.  After performing these actions, DevTools modifies the current default locale, affecting the following code.</span></span>  

*   `Intl.*` <span data-ttu-id="c9d0c-187">Par exemple:</span><span class="sxs-lookup"><span data-stu-id="c9d0c-187">APIs, for example:</span></span> `new Intl.NumberFormat().resolvedOptions().locale`  
*   <span data-ttu-id="c9d0c-188">Autres API JavaScript prenant en charge des paramètres régionaux tels que `String.prototype.localeCompare` et `*.prototype.toLocaleString` , par exemple:</span><span class="sxs-lookup"><span data-stu-id="c9d0c-188">Other locale-aware JavaScript APIs such as `String.prototype.localeCompare` and `*.prototype.toLocaleString`, for example:</span></span> `123_456..toLocaleString()`  
*   <span data-ttu-id="c9d0c-189">API DOM telles que `navigator.language` et</span><span class="sxs-lookup"><span data-stu-id="c9d0c-189">DOM APIs such as `navigator.language` and</span></span> `navigator.languages`  
*   <span data-ttu-id="c9d0c-190">[`Accept-Language`][MDNAcceptLanguage]En-tête de requête http</span><span class="sxs-lookup"><span data-stu-id="c9d0c-190">The [`Accept-Language`][MDNAcceptLanguage] HTTP request header</span></span>  

> [!NOTE]
> <span data-ttu-id="c9d0c-191">Les mises à jour de `navigator.language` et ne `navigator.languages` sont pas visibles immédiatement, mais uniquement après la prochaine navigation ou actualisation de page.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-191">Updates to `navigator.language` and `navigator.languages` are not visible immediately, but only after the next navigation or page refresh.</span></span>  <span data-ttu-id="c9d0c-192">Les modifications apportées à l' `Accept-Language` en-tête http sont uniquement répercutées pour les demandes suivantes.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-192">Changes to the `Accept-Language` HTTP header are only reflected for subsequent requests.</span></span>  

:::image type="complex" source="../../media/2020/03/locale.msft.png" alt-text="Émulation d’un paramètre régional" lightbox="../../media/2020/03/locale.msft.png":::
   <span data-ttu-id="c9d0c-194">Figure 10: émulation d’un paramètre régional</span><span class="sxs-lookup"><span data-stu-id="c9d0c-194">Figure 10:  Emulating a locale</span></span>  
:::image-end:::  

<span data-ttu-id="c9d0c-195">Pour essayer une démonstration, voir [exemple de code dépendant des paramètres régionaux][MathiasByensLocaleDemo].</span><span class="sxs-lookup"><span data-stu-id="c9d0c-195">To try a demo, see [Locale-dependent code example][MathiasByensLocaleDemo].</span></span>

<span data-ttu-id="c9d0c-196">[#1051822][crbug1051822] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="c9d0c-196">Chromium issue [#1051822][crbug1051822]</span></span>

### <span data-ttu-id="c9d0c-197">Débogage de la stratégie d’intégration COEP (Cross-Origin)</span><span class="sxs-lookup"><span data-stu-id="c9d0c-197">Cross-Origin Embedder Policy (COEP) debugging</span></span>  

<span data-ttu-id="c9d0c-198">Le panneau réseau fournit désormais des informations de débogage de la [stratégie d’incorporation][COEP] à l’origine.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-198">The Network panel now provides [Cross-Origin Embedder Policy][COEP] debugging information.</span></span>  

<span data-ttu-id="c9d0c-199">La colonne **État** donne désormais une explication rapide de la raison pour laquelle une requête a été bloquée ainsi qu’un lien pour afficher les en-têtes de cette requête pour un débogage supplémentaire:</span><span class="sxs-lookup"><span data-stu-id="c9d0c-199">The **Status** column now provides a quick explanation of why a request was blocked as well as a link to view the headers of that request for further debugging:</span></span>  

:::image type="complex" source="../../media/2020/03/status.msft.png" alt-text="Demandes bloquées dans la colonne \* \* Status \* \*" lightbox="../../media/2020/03/status.msft.png":::
   <span data-ttu-id="c9d0c-201">Figure 11: demandes bloquées dans la colonne État</span><span class="sxs-lookup"><span data-stu-id="c9d0c-201">Figure 11:  Blocked requests in the Status column</span></span>  
:::image-end:::  

<span data-ttu-id="c9d0c-202">La section **en-têtes de réponse** de l’onglet **en-têtes** fournit davantage d’instructions pour résoudre les problèmes:</span><span class="sxs-lookup"><span data-stu-id="c9d0c-202">The **Response Headers** section of the **Headers** tab provides more guidance on how to resolve the issues:</span></span>  

:::image type="complex" source="../../media/2020/03/guidance.msft.png" alt-text="Conseils supplémentaires dans la section en-têtes de réponse" lightbox="../../media/2020/03/guidance.msft.png":::
   <span data-ttu-id="c9d0c-204">Figure 12: conseils supplémentaires dans la section en-têtes de réponse</span><span class="sxs-lookup"><span data-stu-id="c9d0c-204">Figure 12:  More guidance in the Response Headers section</span></span>  
:::image-end:::  

<span data-ttu-id="c9d0c-205">Envoyez-nous vos commentaires en le [tweetant][PostTweetEdgeDevTools] ou en cliquant sur l’icône de [Commentaires](#feedback) .</span><span class="sxs-lookup"><span data-stu-id="c9d0c-205">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Feedback](#feedback) icon!</span></span>  

<span data-ttu-id="c9d0c-206">[#1051466][crbug1051466] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="c9d0c-206">Chromium issue [#1051466][crbug1051466]</span></span>  

### <span data-ttu-id="c9d0c-207">Afficher les requêtes réseau qui définissent un chemin de cookie spécifique</span><span class="sxs-lookup"><span data-stu-id="c9d0c-207">View network requests that set a specific cookie path</span></span>  

<span data-ttu-id="c9d0c-208">Utilisez le nouveau `cookie-path` mot clé de filtre dans le panneau **réseau** pour vous concentrer sur les requêtes réseau qui définissent un [chemin de cookie][MDNCookiePath]spécifique.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-208">Use the new `cookie-path` filter keyword in the **Network** panel to focus on the network requests that set a specific [cookie path][MDNCookiePath].</span></span>  

<span data-ttu-id="c9d0c-209">Consultez les [demandes de filtre par propriétés][NetworkProperties] pour découvrir d’autres mots clés comme `cookie-path` .</span><span class="sxs-lookup"><span data-stu-id="c9d0c-209">Check out [Filter requests by properties][NetworkProperties] to discover more keywords like `cookie-path`.</span></span>

### <span data-ttu-id="c9d0c-210">Ancrer à gauche à partir du menu de commandes</span><span class="sxs-lookup"><span data-stu-id="c9d0c-210">Dock to left from the Command Menu</span></span>  

<span data-ttu-id="c9d0c-211">Ouvrez le [menu de commandes][DevToolsCommandMenuIndex] et exécutez la `Dock to left` commande pour déplacer devtools à gauche de votre fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-211">Open the [Command Menu][DevToolsCommandMenuIndex] and run the `Dock to left` command to move DevTools to the left of your viewport.</span></span>  

:::image type="complex" source="../../media/2020/03/dock-to-left.msft.png" alt-text="DevTools ancré à gauche de la fenêtre d’affichage" lightbox="../../media/2020/03/dock-to-left.msft.png":::
   <span data-ttu-id="c9d0c-213">Figure 13: DevTools fixé à gauche de la fenêtre d’affichage</span><span class="sxs-lookup"><span data-stu-id="c9d0c-213">Figure 13:  DevTools docked to the left of the viewport</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="c9d0c-214">La fonctionnalité **ancrer à gauche** est disponible depuis Microsoft Edge 75, mais elle n’est auparavant accessible qu’à partir du [**menu principal**][MainMenuDoc].</span><span class="sxs-lookup"><span data-stu-id="c9d0c-214">The **Dock to left** feature has been available since Microsoft Edge 75, but it was previously only accessible from the [**Main Menu**][MainMenuDoc].</span></span>  <span data-ttu-id="c9d0c-215">La nouvelle fonctionnalité de Microsoft Edge 83 est que vous pouvez maintenant accéder à cette fonctionnalité à partir du menu de commandes.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-215">The new feature in Microsoft Edge 83 is that you may now access this feature from the Command Menu.</span></span>  

<span data-ttu-id="c9d0c-216">Envoyez-nous vos commentaires en le [tweetant][PostTweetEdgeDevTools] ou en cliquant sur l’icône de [Commentaires](#feedback) .</span><span class="sxs-lookup"><span data-stu-id="c9d0c-216">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Feedback](#feedback) icon!</span></span>  

<span data-ttu-id="c9d0c-217">[#1011679][crbug1011679] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="c9d0c-217">Chromium issue [#1011679][crbug1011679]</span></span>  

### <span data-ttu-id="c9d0c-218">Le panneau d’audit est désormais le panneau de signalisation.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-218">The Audits panel is now the Lighthouse panel</span></span>  

<span data-ttu-id="c9d0c-219">L’équipe DevTools a fréquemment reçu des commentaires de la part des développeurs Web, alors qu’il était possible d’exécuter un [phare][GithubGoogleChromeLighthouse] à partir de devtools, **lorsque l’utilisateur** a essayé le panneau de configuration, il n’a pas été en mesure de trouver le panneau de **signalisation.**</span><span class="sxs-lookup"><span data-stu-id="c9d0c-219">The DevTools team frequently got feedback from web developers that while it was possible to run [Lighthouse][GithubGoogleChromeLighthouse] from DevTools, when they tried it out they were not able to find the "Lighthouse" panel, so the **Audits** panel is now the **Lighthouse** panel.</span></span>  

:::image type="complex" source="../../media/2020/03/lighthouse.msft.png" alt-text="Panneau de signalisation" lightbox="../../media/2020/03/lighthouse.msft.png":::
   <span data-ttu-id="c9d0c-221">Figure 14: panneau de signalisation</span><span class="sxs-lookup"><span data-stu-id="c9d0c-221">Figure 14:  The Lighthouse panel</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="c9d0c-222">Le panneau de **signalisation** comporte des liens vers du contenu hébergé sur des sites Web tiers.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-222">The **Lighthouse** panel provides links to content hosted on third-party websites.</span></span>  <span data-ttu-id="c9d0c-223">Microsoft n’est pas responsable et n’a aucun contrôle sur le contenu de ces sites et sur les données qu’ils peuvent recueillir.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-223">Microsoft is not responsible for and has no control over the content of these sites and any data they may collect.</span></span>  

### <span data-ttu-id="c9d0c-224">Supprimer tous les remplacements locaux dans un dossier</span><span class="sxs-lookup"><span data-stu-id="c9d0c-224">Delete all Local Overrides in a folder</span></span>  

<span data-ttu-id="c9d0c-225">Après avoir configuré les **remplacements locaux** , vous pouvez cliquer avec le bouton droit sur un dossier et sélectionner l’option **supprimer toutes les substitutions** dans ce dossier.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-225">After setting up **Local Overrides** you may right-click a folder and select the new **Delete all overrides** option to delete all Local Overrides in that folder.</span></span>  

:::image type="complex" source="../../media/2020/03/overrides.msft.png" alt-text="Supprimer tous les remplacements" lightbox="../../media/2020/03/overrides.msft.png":::
   <span data-ttu-id="c9d0c-227">Figure 15: supprimer tous les remplacements</span><span class="sxs-lookup"><span data-stu-id="c9d0c-227">Figure 15:  Delete all overrides</span></span>  
:::image-end:::  

<span data-ttu-id="c9d0c-228">Envoyez-nous vos commentaires en le [tweetant][PostTweetEdgeDevTools] ou en cliquant sur l’icône de [Commentaires](#feedback) .</span><span class="sxs-lookup"><span data-stu-id="c9d0c-228">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Feedback](#feedback) icon!</span></span>  

<span data-ttu-id="c9d0c-229">[#1016501][crbug1016501] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="c9d0c-229">Chromium issue [#1016501][crbug1016501]</span></span>  

### <span data-ttu-id="c9d0c-230">Interface utilisateur de tâches longues mise à jour</span><span class="sxs-lookup"><span data-stu-id="c9d0c-230">Updated Long tasks UI</span></span>  

<span data-ttu-id="c9d0c-231">Une **tâche longue** correspond à du code JavaScript qui monopolit le thread principal pendant un certain temps, provoquant le gel d’une page Web.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-231">A **Long Task** is JavaScript code that monopolizes the main thread for a long time, causing a web page to freeze.</span></span>  

<span data-ttu-id="c9d0c-232">Vous avez la possibilité de [visualiser de longs tâches dans le panneau de performance][LongTasksInPerformancePanel] pour un certain temps, mais dans Microsoft Edge 83, l’interface utilisateur d’une visualisation de tâches longues du panneau de performance a été mise à jour.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-232">You have been able to [visualize Long Tasks in the Performance panel][LongTasksInPerformancePanel] for a while now, but in Microsoft Edge 83 the Long Task visualization UI in the Performance panel has been updated.</span></span>  <span data-ttu-id="c9d0c-233">La partie tâches longues d’une tâche est désormais colorée avec un arrière-plan rouge rayé.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-233">The Long Task portion of a task is now colored with a striped red background.</span></span>  

:::image type="complex" source="../../media/2020/03/long-task.msft.png" alt-text="Nouvelle interface utilisateur de tâche longue" lightbox="../../media/2020/03/long-task.msft.png":::
   <span data-ttu-id="c9d0c-235">Figure 16: interface utilisateur de nouvelle tâche longue</span><span class="sxs-lookup"><span data-stu-id="c9d0c-235">Figure 16:  The new Long Task UI</span></span>  
:::image-end:::  

<span data-ttu-id="c9d0c-236">Envoyez-nous vos commentaires en le [tweetant][PostTweetEdgeDevTools] ou en cliquant sur l’icône de [Commentaires](#feedback) .</span><span class="sxs-lookup"><span data-stu-id="c9d0c-236">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Feedback](#feedback) icon!</span></span>  

<span data-ttu-id="c9d0c-237">[#1054447][crbug1054447] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="c9d0c-237">Chromium issue [#1054447][crbug1054447]</span></span>  

### <span data-ttu-id="c9d0c-238">Icône masquable dans le volet manifeste</span><span class="sxs-lookup"><span data-stu-id="c9d0c-238">Maskable icon support in the Manifest pane</span></span>  

<span data-ttu-id="c9d0c-239">Android Oreo introduit des icônes adaptatives qui affichent des icônes d’application dans différentes formes sur différents modèles d’appareil.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-239">Android Oreo introduced adaptive icons, which display app icons in a variety of shapes across different device models.</span></span>  <span data-ttu-id="c9d0c-240">Les icônes qui peuvent être **masquées** sont un nouveau format d’icône qui prend en charge les icônes adaptatives, qui vous permettent de vous assurer que votre icône [PWA][PWADoc] fonctionne correctement sur les appareils qui prennent en charge la norme d’icônes masquées.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-240">**Maskable icons** are a new icon format that support adaptive icons, which enable you to ensure that your [PWA][PWADoc] icon looks good on devices that support the maskable icons standard.</span></span>  

<span data-ttu-id="c9d0c-241">Activez la case à cocher nouveau **afficher uniquement la zone sécurisée minimum pour les icônes masquées** dans le volet **manifeste** pour vérifier que votre icône MASKABLE fonctionne correctement sur les appareils Android Oreo.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-241">Enable the new **Show only the minimum safe area for maskable icons** checkbox in the **Manifest** pane to check that your maskable icon looks good on Android Oreo devices.</span></span>  

<!-- Check out [Are my current icons ready?] to learn more.  -->  

:::image type="complex" source="../../media/2020/03/maskable-icons.msft.png" alt-text="Case à cocher Afficher uniquement la zone sécurisée minimum pour les icônes masquées" lightbox="../../media/2020/03/maskable-icons.msft.png":::
   <span data-ttu-id="c9d0c-243">Figure 17: activez la case à cocher **afficher uniquement la zone sécurisée minimum pour les icônes masquées** .</span><span class="sxs-lookup"><span data-stu-id="c9d0c-243">Figure 17:  The **Show only the minimum safe area for maskable icons** checkbox</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="c9d0c-244">Cette fonctionnalité est lancée dans Microsoft Edge 81.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-244">This feature launched in Microsoft Edge 81.</span></span>  <span data-ttu-id="c9d0c-245">Les mises à jour abordées ici dans Microsoft Edge 83 n’ont pas été abordées dans [les nouveautés de devtools (Microsoft edge 81)][WhatsNew81].</span><span class="sxs-lookup"><span data-stu-id="c9d0c-245">The updates covered here in Microsoft Edge 83 were not covered in [What's New In DevTools (Microsoft Edge 81)][WhatsNew81].</span></span>  

## <span data-ttu-id="c9d0c-246">Commentaires</span><span class="sxs-lookup"><span data-stu-id="c9d0c-246">Feedback</span></span>  

<span data-ttu-id="c9d0c-247">Découvrir les nouvelles fonctionnalités et les modifications de cette publication ou tout autre sujet lié à DevTools:</span><span class="sxs-lookup"><span data-stu-id="c9d0c-247">To discuss the new features and changes in this post, or anything else related to DevTools:</span></span>  

*   <span data-ttu-id="c9d0c-248">Envoyez vos commentaires à l’aide de l’icône de **Commentaires** dans le devtools</span><span class="sxs-lookup"><span data-stu-id="c9d0c-248">Send your feedback using the **Feedback** icon in the DevTools</span></span>  
*   <span data-ttu-id="c9d0c-249">Tweeter sur [@EdgeDevTools][PostTweetEdgeDevTools]</span><span class="sxs-lookup"><span data-stu-id="c9d0c-249">Tweet at [@EdgeDevTools][PostTweetEdgeDevTools]</span></span>  
*   <span data-ttu-id="c9d0c-250">Envoyez une suggestion au [site Web de votre choix][TheWebWeWant]</span><span class="sxs-lookup"><span data-stu-id="c9d0c-250">Submit a suggestion to [The Web We Want][TheWebWeWant]</span></span>  
*   <span data-ttu-id="c9d0c-251">Classer des bogues sur ce document dans le référentiel [Edge-développeurs][GitHubMicrosoftDocsEdgeDeveloperNewIssue]</span><span class="sxs-lookup"><span data-stu-id="c9d0c-251">File bugs on this document in the [edge-developer][GitHubMicrosoftDocsEdgeDeveloperNewIssue] repository</span></span>  

:::image type="complex" source="../../media/2020/03/feedback-icon.msft.png" alt-text="L’icône \* \* Feedback \* \* dans Microsoft Edge DevTools" lightbox="../../media/2020/03/feedback-icon.msft.png":::
   <span data-ttu-id="c9d0c-253">Figure 18: icône de **Commentaires** dans le Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="c9d0c-253">Figure 18:  The **Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

## <span data-ttu-id="c9d0c-254">Télécharger les canaux Microsoft Edge preview</span><span class="sxs-lookup"><span data-stu-id="c9d0c-254">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="c9d0c-255">Si vous utilisez Windows ou macOS, envisagez d’utiliser les [canaux Microsoft Edge Preview][MicrosoftEdgePreviewChannels] comme navigateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-255">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="c9d0c-256">Les canaux d’aperçu vous permettent d’accéder aux dernières fonctionnalités de DevTools.</span><span class="sxs-lookup"><span data-stu-id="c9d0c-256">The preview channels give you access to the latest DevTools features.</span></span>  

<!-- links -->  

[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Publiez un tweet"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools compte Twitter"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Nouveau problème-MicrosoftDocs/Edge-développeur"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Canaux Microsoft Edge preview"  
[TheWebWeWant]: https://aka.ms/webwewant "Le site Web de votre choix"  

[WhatsNew81]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/01/devtools "Nouveautés de DevTools (Microsoft Edge 81)"  

[DevToolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Exécuter des commandes à l’aide du menu de commande de Microsoft Edge DevTools"  
[ColorPicker]: /microsoft-edge/devtools-guide-chromium/css/reference#change-colors-with-the-color-picker "Changer les couleurs à l’aide du sélecteur de couleurs"  
[ElementsDoc]: /microsoft-edge/devtools-guide-chromium/css/index "Découvrir comment afficher et modifier des feuilles CSS"  
[MainMenuDoc]: /microsoft-edge/devtools-guide-chromium/customize/placement#change-placement-from-the-main-menu "Changer la position dans le menu principal"  
[LongTasksInPerformancePanel]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#view-main-thread-activity "Afficher l’activité du thread principal"  
[RenderingDoc]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Analyser les performances de rendu à l’aide de l’onglet rendu"  
[PWADoc]: /microsoft-edge/progressive-web-apps-chromium/index "Applications Web progressives sur Windows"  
[RemoteDebuggingWin10]: /microsoft-edge/devtools-guide-chromium/remote-debugging/windows "Prendre en main les appareils Windows 10 de débogage à distance"  
[LineOfCodeBreakpoints]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints#line-of-code-breakpoints "Points d’arrêt de code de ligne"
[NetworkProperties]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties
[OverviewSettings]: /microsoft-edge/devtools-guide-chromium/customize/#settings

[WindowsDevicePortal]: /windows/uwp/debug-test-perf/device-portal "Vue d’ensemble de Windows Device Portal"  

[RemoteTools]: https://www.microsoft.com/store/apps/9P6CMFV44ZLT "Outils de contrôle à distance pour Microsoft Edge (bêta)"  
[MicrosoftStore]: https://www.microsoft.com/store/apps/windows "Microsoft Store"  
[WindowsBlogStableRelease]: https://blogs.windows.com/msedgedev/2020/03/20/update-stable-channel-releases/ "Mise à jour sur les versions de canal stable pour Microsoft Edge"

[ColorBlindnessTypes]: http://www.colourblindawareness.org/colour-blindness/types-of-colour-blindness/ "Types de cécité du Colour"  
[MDNAcceptLanguage]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Accept-Language "Accept-Language"
[MathiasByensLocaleDemo]: https://mathiasbynens.be/demo/locale "Exemple de code dépendant des paramètres régionaux"
[MDNCookiePath]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie#Directives

[crbug963183]: https://crbug.com/963183 "Problème 963183: DevTools n’est pas conforme à la norme WCAG"  
[crbug1003700]: https://crbug.com/1003700 "Problème 1003700: ajout de la prise en charge de DevTools pour la simulation d’déficience de vision couleur"  
[crbug1011679]: https://crbug.com/1011679 "Problème 1011679: Introduisez l’option ancrer à gauche dans le menu de commandes"  
[crbug1016501]: https://crbug.com/1016501 "Problème 1016501: demande de fonctionnalité: bouton permettant de supprimer tous les remplacements locaux"  
[crbug1050999]: https://crbug.com/1050999 "Problème 1050999: onglet Propriétés"  
[crbug1051466]: https://crbug.com/1051466 "Problème 1051466: prendre en charge le débogage de COOP/COEP dans DevTools"  
[crbug1054447]: https://crbug.com/1054447 "Problème 1054447: mettre à jour les métriques de performance dans DevTools Timeline"  
[crbug1051822]: https://crbug.com/1051822 "Problème 1051822: DevTools: ajouter une interface utilisateur pour émuler des paramètres régionaux"
[crbug1041830]: https://crbug.com/1041830 "Problème 1041830: améliorer les couleurs pour les points d’arrêt"
[crbug1050855]: https://crbug.com/1050855 "Problème 1050855: l’affichage des paramètres est difficile à découvrir"
[crbug1056348]: https://crbug.com/1056348 "Problème 1056348: actualisation du composant barre d’informations"

[COOP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.tu4hyy6v12wn "Explication de COOP et de COEP-explication-la politique d’ouverture"  
[COEP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.uo6kivyh0ge2 "Explication de la stratégie d’intégration de COOP et COEP"  

[GithubGoogleChromeLighthouse]: https://github.com/GoogleChrome/lighthouse "Phare GitHub référentiel Samples"  

> [!NOTE]
> <span data-ttu-id="c9d0c-293">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c9d0c-293">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c9d0c-294">La page d’origine est disponible [ici](https://developers.google.com/web/updates/2020/03/devtools/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="c9d0c-294">The original page is found [here](https://developers.google.com/web/updates/2020/03/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="c9d0c-296">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c9d0c-296">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
