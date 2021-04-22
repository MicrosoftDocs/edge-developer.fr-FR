---
description: Les soulignements ondulés mettent en évidence les problèmes de code dans l'outil Éléments, la chronologie de mise à jour du service de travail, etc.
title: Nouveautés de DevTools (Microsoft Edge 91)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/21/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 3a2be4d309432de4421af73ca7b4d21734ad5221
ms.sourcegitcommit: de75fda30bb8964e9a184228d068b4402ec59c3e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "11514445"
---
<!-- Copyright Jecelyn Yeen 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="whats-new-in-devtools-microsoft-edge-91"></a><span data-ttu-id="2f1dc-104">Nouveautés de DevTools (Microsoft Edge 91)</span><span class="sxs-lookup"><span data-stu-id="2f1dc-104">What's New In DevTools (Microsoft Edge 91)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="wavy-underlines-highlight-code-issues-and-improvements-in-elements-tool"></a><span data-ttu-id="2f1dc-105">Les soulignements ondulés mettent en évidence les problèmes de code et les améliorations apportées à l'outil Elements</span><span class="sxs-lookup"><span data-stu-id="2f1dc-105">Wavy underlines highlight code issues and improvements in Elements tool</span></span>  

<!--  Title: Get code hints in Elements tool  -->  
<!--  Subtitle: Wavy underlines like the ones you see in Visual Studio Code now display in the Elements tool.  Underlines alert you to code issues related to accessibility, compatibility, security, performance, and  so on.  -->  

<span data-ttu-id="2f1dc-106">Dans la plupart des IDE modernes, les soulignements ondulés sous le texte indiquent des erreurs de syntaxe.</span><span class="sxs-lookup"><span data-stu-id="2f1dc-106">In most modern IDEs, wavy underlines under text indicate syntax errors.</span></span>   <span data-ttu-id="2f1dc-107">Dans Microsoft Edge version 91 ou ultérieure, les soulignements ondulés s'affichent sous HTML dans la vue **DOM** de **l'outil Elements.**</span><span class="sxs-lookup"><span data-stu-id="2f1dc-107">In Microsoft Edge version 91 or later, wavy underlines display under HTML in the **DOM** view of the **Elements** tool.</span></span>  <span data-ttu-id="2f1dc-108">Les soulignements ondulés indiquent des problèmes de code et des suggestions liés à l'accessibilité, la compatibilité, les performances, etc.</span><span class="sxs-lookup"><span data-stu-id="2f1dc-108">The wavy underlines indicate code issues and suggestions related to accessibility, compatibility, performance, and so on.</span></span>  <span data-ttu-id="2f1dc-109">Pour plus d'informations sur la façon de passer en revue et de modifier les problèmes, accédez à Rechercher et résoudre les problèmes avec l'outil Problèmes [DevTools][DevtoolsIssuesIndex]de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2f1dc-109">For more information about how to review and edit issues, navigate to [Find and fix problems with the Microsoft Edge DevTools Issues tool][DevtoolsIssuesIndex].</span></span>  

<span data-ttu-id="2f1dc-110">Pour ouvrir **l'outil Problèmes** et en savoir plus sur le problème et comment le résoudre, effectuer l'une des actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="2f1dc-110">To open the **Issues** tool and learn more about the issue and how to fix it, complete one of the following actions.</span></span>  

*   <span data-ttu-id="2f1dc-111">Sélectionnez et `Shift` maintenez, puis choisissez un soulignement ondulé.</span><span class="sxs-lookup"><span data-stu-id="2f1dc-111">Select and hold `Shift`, and then choose any wavy underline.</span></span>  
*   <span data-ttu-id="2f1dc-112">Effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="2f1dc-112">Complete the following actions.</span></span>  
    1.  <span data-ttu-id="2f1dc-113">Pointez sur n'importe quel soulignement ondulé.</span><span class="sxs-lookup"><span data-stu-id="2f1dc-113">Hover on any wavy underline.</span></span>  
    1.  <span data-ttu-id="2f1dc-114">Ouvrez le menu contextuel \(cliquez avec le bouton droit\).</span><span class="sxs-lookup"><span data-stu-id="2f1dc-114">Open the contextual menu \(right-click\).</span></span>  
    1.  <span data-ttu-id="2f1dc-115">Choose **Show in Issues**.</span><span class="sxs-lookup"><span data-stu-id="2f1dc-115">Choose **Show in Issues**.</span></span>  
        
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/elements-iframe-highlight-issues.msft.png" alt-text="Choisir l'erreur soulignée dans l'outil Éléments" lightbox="../../media/2021/04/elements-iframe-highlight-issues.msft.png":::
         <span data-ttu-id="2f1dc-117">Choisir l'erreur soulignée dans **l'outil Éléments**</span><span class="sxs-lookup"><span data-stu-id="2f1dc-117">Choose the underlined error in the **Elements** tool</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/elements-iframe-highlight-issues-focus.msft.png" alt-text="Afficher les détails des erreurs dans l'outil Problèmes" lightbox="../../media/2021/04/elements-iframe-highlight-issues-focus.msft.png":::
         <span data-ttu-id="2f1dc-119">Afficher les détails des erreurs dans **l'outil Problèmes**</span><span class="sxs-lookup"><span data-stu-id="2f1dc-119">Display error details in the **Issues** tool</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="learn-about-devtools-with-informative-tooltips"></a><span data-ttu-id="2f1dc-120">En savoir plus sur DevTools grâce à des infobulles informatives</span><span class="sxs-lookup"><span data-stu-id="2f1dc-120">Learn about DevTools with informative tooltips</span></span>  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<!--  Title: Learn more about DevTools with DevTools Tooltips  -->  
<!--  Subtitle: Informative overlays are now available in the default DevTools interface.  -->  

<span data-ttu-id="2f1dc-121">La fonctionnalité d'outils DevTools vous permet d'en savoir plus sur les différents outils et volets de DevTools.</span><span class="sxs-lookup"><span data-stu-id="2f1dc-121">The DevTools Tooltips feature helps you learn about all the different tools and panes in DevTools.</span></span>  <span data-ttu-id="2f1dc-122">Pour désactiver les bulles, sélectionnez `Esc` .</span><span class="sxs-lookup"><span data-stu-id="2f1dc-122">To turn off Tooltips, select `Esc`.</span></span>  <span data-ttu-id="2f1dc-123">Pour activer les bulles, effectuer l'une des actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="2f1dc-123">To turn on Tooltips, complete one of the following actions.</span></span>  

*   <span data-ttu-id="2f1dc-124">Sélectionnez `Ctrl` + `Shift` + `H` \(Windows/Linux\) ou `Cmd` + `Shift` + `H` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="2f1dc-124">Select `Ctrl`+`Shift`+`H` \(Windows/Linux\) or `Cmd`+`Shift`+`H` \(macOS\).</span></span>  
*   <span data-ttu-id="2f1dc-125">[Ouvrez le menu Commande,][DevtoolsCommandMenuIndexOpenCommandMenu] puis tapez `tooltips` .</span><span class="sxs-lookup"><span data-stu-id="2f1dc-125">[Open the Command Menu][DevtoolsCommandMenuIndexOpenCommandMenu] and then type `tooltips`.</span></span>  
*   <span data-ttu-id="2f1dc-126">Choose **Customize and control DevTools** \( `...` \) > **Help**  >  **Toggle the DevTools Tooltips**.</span><span class="sxs-lookup"><span data-stu-id="2f1dc-126">Choose **Customize and control DevTools** \(`...`\) > **Help** > **Toggle the DevTools Tooltips**.</span></span>  

<span data-ttu-id="2f1dc-127">En outre, si vous allumez l'expérience d'bulles d'outils Mode Focus et [DevTools,][DevtoolsWhatsNew202102DevtoolsGroupToolsTogetherInFocusMode] vous pouvez également choisir le bouton Basculer le bouton d'outils **DevTools** \( \) en bas de la barre `?` d'activité. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="2f1dc-127">Also, if you turn on the [Focus Mode and DevTools Tooltips][DevtoolsWhatsNew202102DevtoolsGroupToolsTogetherInFocusMode] experiment, you may also choose the **Toggle the DevTools Tooltips** \(`?`\) button at the bottom of the **Activity Bar**.</span></span>  

<span data-ttu-id="2f1dc-128">Pour afficher plus d'informations sur l'utilisation de DevTools, allumez les info-bulles, puis pointez sur chaque région en plan des DevTools.</span><span class="sxs-lookup"><span data-stu-id="2f1dc-128">To display more information about how to use the DevTools, turn on Tooltips, and then hover on each outlined region of the DevTools.</span></span>  

:::image type="complex" source="../../media/2021/04/elements-issues-focus-mode-tooltips.msft.png" alt-text="Pointez n'importe où dans la région mise en surbrillez de l'outil Problèmes pour afficher plus de détails" lightbox="../../media/2021/04/elements-issues-focus-mode-tooltips.msft.png":::
   <span data-ttu-id="2f1dc-130">Pointez n'importe où dans \*\*\*\* la région mise en surbrillez de l'outil Problèmes pour afficher plus de détails</span><span class="sxs-lookup"><span data-stu-id="2f1dc-130">Hover on anywhere in the highlighted region of the **Issues** tool to display more details</span></span>  
:::image-end:::  

## <a name="service-worker-update-timeline"></a><span data-ttu-id="2f1dc-131">Chronologie de mise à jour du service de travail</span><span class="sxs-lookup"><span data-stu-id="2f1dc-131">Service worker update timeline</span></span>  

<!--todo:  Update the linked [Service Worker improvements][DevtoolsServiceWorkerIndex] article.  -->  

<!--  Title: The tasks associated with your Service Worker  -->  
<!--  Subtitle: Debug with Service Worker Update Cycle  -->  

<span data-ttu-id="2f1dc-132">Dans Microsoft Edge version 91 ou ultérieure, si vous êtes développeur Progressive Web App ou Service Worker, vous pouvez afficher le cycle de vie des mises à jour de vos employés de service sous forme de chronologie dans l'outil **Application.**</span><span class="sxs-lookup"><span data-stu-id="2f1dc-132">In Microsoft Edge version 91 or later, if you are a Progressive Web App or Service Worker developer, you may display the update lifecycle of your Service Workers as a timeline in the **Application** tool.</span></span>  <span data-ttu-id="2f1dc-133">Cette fonctionnalité vous permet de comprendre le temps que votre service de travail passe à chacune des étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="2f1dc-133">This feature helps you understand the time your Service Worker spends in each of the following stages.</span></span>  

*   **<span data-ttu-id="2f1dc-134">Install</span><span class="sxs-lookup"><span data-stu-id="2f1dc-134">Install</span></span>**  
*   **<span data-ttu-id="2f1dc-135">Attendre</span><span class="sxs-lookup"><span data-stu-id="2f1dc-135">Wait</span></span>**  
*   **<span data-ttu-id="2f1dc-136">Activer</span><span class="sxs-lookup"><span data-stu-id="2f1dc-136">Activate</span></span>**  
    
:::image type="complex" source="../../media/2021/04/application-service-workers-update-cycle-version-73-focus.msft.png" alt-text="Passer en revue la chronologie du cycle de mise à jour pour votre service de travail" lightbox="../../media/2021/04/application-service-workers-update-cycle-version-73-focus.msft.png":::
   <span data-ttu-id="2f1dc-138">Passer en revue **la chronologie** du cycle de mise **à jour** pour votre service de travail</span><span class="sxs-lookup"><span data-stu-id="2f1dc-138">Review the **Timeline** in the **Update Cycle** for your Service Worker</span></span>  
:::image-end:::  

<span data-ttu-id="2f1dc-139">Pour plus d'informations sur le cycle de vie de vos employés de service, accédez au cycle de vie des travailleurs [de service.][ProgressiveWebAppsServiceworkerServiceWorkerLifecycle]</span><span class="sxs-lookup"><span data-stu-id="2f1dc-139">For more information about the lifecycle of your Service Workers, navigate to [The Service Worker lifecycle][ProgressiveWebAppsServiceworkerServiceWorkerLifecycle].</span></span>  <span data-ttu-id="2f1dc-140">Pour plus d'informations sur les outils de débogage pour les applications web progressives et les travailleurs de service dans DevTools, accédez aux améliorations apportées aux services [de travail.][DevtoolsServiceWorkerIndex]</span><span class="sxs-lookup"><span data-stu-id="2f1dc-140">For more information about debugging tools for Progressive Web Apps and Service Workers in the DevTools, navigate to [Service Worker improvements][DevtoolsServiceWorkerIndex].</span></span>  <span data-ttu-id="2f1dc-141">Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans le projet open source Chromium, accédez à Problème [1066604][CR1066604].</span><span class="sxs-lookup"><span data-stu-id="2f1dc-141">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [1066604][CR1066604].</span></span>  

## <a name="progressive-web-apps-no-longer-display-warnings-for-non-square-icons"></a><span data-ttu-id="2f1dc-142">Les applications web progressives n'affichent plus d'avertissements pour les icônes non carrées</span><span class="sxs-lookup"><span data-stu-id="2f1dc-142">Progressive Web Apps no longer display warnings for non-square icons</span></span>  

<!--  Title: Non-square icons in app manifest no longer produce warnings  -->  
<!--  Subtitle: As long as square icons are included in the app manifest, non-square icons no longer produce warnings  -->  

<span data-ttu-id="2f1dc-143">Dans [Microsoft Edge version 90][DevtoolsWhatsNew202102Devtools] ou antérieure, si vous avez inclus une icône non carrée dans le manifeste d'application web de votre application PWA, la section Manifeste de l'outil **Application** a affiché un avertissement sous Erreurs et \*\*\*\* **avertissements** pour chaque icône non carrée.</span><span class="sxs-lookup"><span data-stu-id="2f1dc-143">In [Microsoft Edge version 90][DevtoolsWhatsNew202102Devtools] or earlier, if you included a non-square icon in the Web App Manifest of your PWA, the **Manifest** section in the **Application** tool displayed a warning under **Errors and Warnings** for each non-square icon.</span></span>  <span data-ttu-id="2f1dc-144">Dans Microsoft Edge version 91 ou ultérieure, la **section** Manifeste de l'outil **Application** n'affiche aucun avertissement si vous fournissez au moins une icône carrée.</span><span class="sxs-lookup"><span data-stu-id="2f1dc-144">In Microsoft Edge version 91 or later, the **Manifest** section in the **Application** tool displays no warnings if you provide at least one square icon.</span></span>  <span data-ttu-id="2f1dc-145">Si vous ne fournissez aucune icône carrée, un avertissement affiche le message suivant.</span><span class="sxs-lookup"><span data-stu-id="2f1dc-145">If you don't provide any square icons, a warning displays the following message.</span></span>  

```output
Most operating systems require square icons.  Please include at least one square icon in the array.  
```  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/edge89-application-manifest-errors-and-warnings.msft.png" alt-text="Dans Microsoft Edge version 90 ou antérieure, une erreur s'affiche pour chaque icône non carrée" lightbox="../../media/2021/04/edge89-application-manifest-errors-and-warnings.msft.png":::
         <span data-ttu-id="2f1dc-147">Dans Microsoft Edge version 90 ou antérieure, une erreur s'affiche pour chaque icône non carrée</span><span class="sxs-lookup"><span data-stu-id="2f1dc-147">In Microsoft Edge version 90 or earlier, an error displays for each icon that is non-square</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/edge91-application-manifest-errors-and-warnings.msft.png" alt-text="Dans Microsoft Edge version 91 ou ultérieure, aucune erreur ne s'affiche lorsque vous fournissez au moins une icône carrée" lightbox="../../media/2021/04/edge91-application-manifest-errors-and-warnings.msft.png":::
         <span data-ttu-id="2f1dc-149">Dans Microsoft Edge version 91 ou ultérieure, aucune erreur ne s'affiche lorsque vous fournissez au moins une icône carrée</span><span class="sxs-lookup"><span data-stu-id="2f1dc-149">In Microsoft Edge version 91 or later, no error displays when you provide at least one square icon</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="2f1dc-150">Pour passer en revue les erreurs et les avertissements dans votre manifeste d'application web, accédez à l'outil **Application** et choisissez la section **Manifeste.**</span><span class="sxs-lookup"><span data-stu-id="2f1dc-150">To review errors and warnings in your Web App Manifest, navigate to the **Application** tool and choose the **Manifest** section.</span></span>  <span data-ttu-id="2f1dc-151">Les erreurs et avertissements sont répertoriés sous le titre **Erreurs et avertissements.**</span><span class="sxs-lookup"><span data-stu-id="2f1dc-151">Errors and warnings are listed under the **Errors and Warnings** heading.</span></span>  <span data-ttu-id="2f1dc-152">Pour plus d'informations sur le manifeste de l'application Web, accédez à Utiliser le manifeste d'application web pour intégrer votre application Web progressive [dans le système d'exploitation.][ProgressiveWebAppsWebappmanifests]</span><span class="sxs-lookup"><span data-stu-id="2f1dc-152">For more information about the Web App Manifest, navigate to [Use the Web App Manifest to integrate your Progressive Web App into the Operating System][ProgressiveWebAppsWebappmanifests].</span></span>  <span data-ttu-id="2f1dc-153">Pour créer des icônes à inclure dans votre manifeste d'application web, accédez au générateur [d'images PWABuilder.][PwabuilderImagegenerator]</span><span class="sxs-lookup"><span data-stu-id="2f1dc-153">To create icons to include in your Web App Manifest, navigate to the [PWABuilder Image Generator][PwabuilderImagegenerator].</span></span>  <span data-ttu-id="2f1dc-154">Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1185945][CR1185945].</span><span class="sxs-lookup"><span data-stu-id="2f1dc-154">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [1185945][CR1185945].</span></span>  

## <a name="localized-devtools-now-supported-in-chromium-based-browsers"></a><span data-ttu-id="2f1dc-155">DevTools localisée désormais prise en charge dans les navigateurs basés sur Chromium</span><span class="sxs-lookup"><span data-stu-id="2f1dc-155">Localized DevTools now supported in Chromium-based browsers</span></span>  

<!--  Title: Localization for all  -->  
<!--  Subtitle: Match browser language enabled to all Chromium-based browsers  -->  

<span data-ttu-id="2f1dc-156">À partir [de Microsoft Edge version 81,][DevtoolsWhatsNew202001DevtoolsUsingDevtoolsInOtherLanguages]Microsoft Edge DevTools s'affiche dans votre propre langue.</span><span class="sxs-lookup"><span data-stu-id="2f1dc-156">Starting in [Microsoft Edge version 81][DevtoolsWhatsNew202001DevtoolsUsingDevtoolsInOtherLanguages], Microsoft Edge DevTools displays in your own language.</span></span>  <span data-ttu-id="2f1dc-157">De nombreux développeurs utilisent d'autres outils de développement tels que StackOverflow et Visual Studio code dans leur langue native, et pas seulement en anglais.</span><span class="sxs-lookup"><span data-stu-id="2f1dc-157">Many developers use other developer tools like StackOverflow and Visual Studio Code in their native language, not just in English.</span></span>  <span data-ttu-id="2f1dc-158">L'équipe Microsoft Edge DevTools, l'équipe Chrome DevTools et l'équipe Google Chrome ont travaillé pour offrir la même expérience dans tous les navigateurs basés sur Chromium.</span><span class="sxs-lookup"><span data-stu-id="2f1dc-158">The Microsoft Edge DevTools team, Chrome DevTools team, and the Google Lighthouse team collaborated to provide the same experience in all Chromium-based browsers.</span></span>  <span data-ttu-id="2f1dc-159">Pour plus d'informations sur l'utilisation de DevTools dans votre langue, accédez à Modifier les paramètres de langue [de DevTools.][DevtoolsCustomizeLocalization]</span><span class="sxs-lookup"><span data-stu-id="2f1dc-159">For more information about how to use DevTools in your language, navigate to [Change DevTools language settings][DevtoolsCustomizeLocalization].</span></span>  <span data-ttu-id="2f1dc-160">Pour plus d'informations sur la collaboration sur cette fonctionnalité dans le projet open source Chromium, accédez à [1136655.][CR1136655]</span><span class="sxs-lookup"><span data-stu-id="2f1dc-160">For more information about the collaboration on this feature in the Chromium open-source project, navigate to [1136655][CR1136655].</span></span>  

:::image type="complex" source="../../media/2021/04/japanese-browser-japanese-navigation-elements-3d-view.msft.png" alt-text="Navigateur Microsoft Edge et DevTools en japonais" lightbox="../../media/2021/04/japanese-browser-japanese-navigation-elements-3d-view.msft.png":::
   <span data-ttu-id="2f1dc-162">Navigateur Microsoft Edge et DevTools en japonais</span><span class="sxs-lookup"><span data-stu-id="2f1dc-162">Microsoft Edge browser and DevTools set to Japanese</span></span>  
:::image-end:::  

## <a name="use-the-keyboard-to-navigate-to-css-variables"></a><span data-ttu-id="2f1dc-163">Utiliser le clavier pour accéder aux variables CSS</span><span class="sxs-lookup"><span data-stu-id="2f1dc-163">Use the keyboard to navigate to CSS variables</span></span>  

<!--  Title: Navigate to CSS variables with the arrow keys  -->  
<!--  Subtitle: In the Styles pane, use the arrow keys to choose CSS variables.  Select `Enter` to see the variable definition.  -->  

<span data-ttu-id="2f1dc-164">À partir [de la version 88][DevtoolsWhatsNew202011DevtoolsCssVariableDefinitionsInStylesPane]de Microsoft Edge, le volet **Styles** affiche les variables CSS et fournit un lien directement vers la définition de chaque variable.</span><span class="sxs-lookup"><span data-stu-id="2f1dc-164">Starting in [Microsoft Edge version 88][DevtoolsWhatsNew202011DevtoolsCssVariableDefinitionsInStylesPane], the **Styles** pane displays CSS variables and provides a link directly to the definition of each variable.</span></span>  <span data-ttu-id="2f1dc-165">Dans Microsoft Edge version 91 ou ultérieure, vous pouvez utiliser les touches de direction pour accéder facilement aux variables CSS.</span><span class="sxs-lookup"><span data-stu-id="2f1dc-165">In Microsoft Edge version 91 or later, you may use the arrow keys to easily navigate to CSS variables.</span></span>  <span data-ttu-id="2f1dc-166">Pour ouvrir la définition dans le volet **Styles,** pointez sur une variable, puis sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="2f1dc-166">To open the definition in the **Styles** pane, hover on a variable, and then select `Enter`.</span></span>  <span data-ttu-id="2f1dc-167">Pour plus d'informations sur les variables CSS, accédez à [l'utilisation de propriétés personnalisées CSS (variables).][MdnDocsWebCssUsingCssCustomProperties]</span><span class="sxs-lookup"><span data-stu-id="2f1dc-167">For more information about CSS variables, navigate to [Using CSS custom properties (variables)][MdnDocsWebCssUsingCssCustomProperties].</span></span>  <span data-ttu-id="2f1dc-168">Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1187735.][CR1187735]</span><span class="sxs-lookup"><span data-stu-id="2f1dc-168">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [1187735][CR1187735].</span></span>  

:::image type="complex" source="../../media/2021/04/elements-styles-body-background-color-theme-body-background.msft.png" alt-text="Variable CSS --theme-body-background mise en évidence dans le volet Styles" lightbox="../../media/2021/04/elements-styles-body-background-color-theme-body-background.msft.png":::
   <span data-ttu-id="2f1dc-170">Variable `--theme-body-background` CSS mise en évidence dans le **volet Styles**</span><span class="sxs-lookup"><span data-stu-id="2f1dc-170">The `--theme-body-background` CSS variable highlighted in the **Styles** pane</span></span>  
:::image-end:::  

## <a name="issues-are-automatically-sorted-by-severity"></a><span data-ttu-id="2f1dc-171">Les problèmes sont automatiquement triés par gravité</span><span class="sxs-lookup"><span data-stu-id="2f1dc-171">Issues are automatically sorted by severity</span></span>  

<!-- Title: Display Issues in severity order  -->  
<!-- Subtitle: Entries in the Issues tool now display in severity order and allow you to focus your updates on the most important issues. -->  

<span data-ttu-id="2f1dc-172">**L'outil Problèmes** affiche des recommandations pour améliorer votre site web, notamment l'accessibilité, les performances, la sécurité, etc.</span><span class="sxs-lookup"><span data-stu-id="2f1dc-172">The **Issues** tool displays recommendations to improve your website, including accessibility, performance, security, and so on.</span></span> <span data-ttu-id="2f1dc-173">En fonction de vos commentaires, les problèmes sont désormais automatiquement triés par gravité.</span><span class="sxs-lookup"><span data-stu-id="2f1dc-173">Based on your feedback, issues are now automatically sorted by severity.</span></span>  <span data-ttu-id="2f1dc-174">Dans chaque catégorie de commentaires, \*\*\*\* chaque problème marqué comme erreur apparaît en premier, suivi de chaque problème marqué comme **avertissement,** puis de chaque problème marqué comme **conseil.**</span><span class="sxs-lookup"><span data-stu-id="2f1dc-174">In each feedback category, each issue marked as an **Error** appears first, followed each issue marked as a **Warning**, then each issue marked as a **Tip**.</span></span>  <span data-ttu-id="2f1dc-175">Pour vous aider à affiner vos problèmes, des options de filtre supplémentaires sont prévues pour une prochaine mise à jour.</span><span class="sxs-lookup"><span data-stu-id="2f1dc-175">To help you refine your issues, extra filter options are planned for a future update.</span></span>  <span data-ttu-id="2f1dc-176">Pour plus d'informations sur la façon de passer en revue les problèmes, accédez à Rechercher et résoudre les problèmes avec l'outil Problèmes [DevTools][DevtoolsIssuesIndex]de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2f1dc-176">For more information about how to review issues, navigate to [Find and fix problems with the Microsoft Edge DevTools Issues tool][DevtoolsIssuesIndex].</span></span>  

:::image type="complex" source="../../media/2021/04/elements-issues-ordered-issues.msft.png" alt-text="L'outil Problèmes affiche les problèmes triés par gravité" lightbox="../../media/2021/04/elements-issues-ordered-issues.msft.png":::
   <span data-ttu-id="2f1dc-178">**L'outil Problèmes** affiche les problèmes triés par gravité</span><span class="sxs-lookup"><span data-stu-id="2f1dc-178">The **Issues** tool displays sorted issues by severity</span></span>  
:::image-end:::  

## <a name="microsoft-edge-developer-tools-for-visual-studio-code-version-117"></a><span data-ttu-id="2f1dc-179">Outils de développement Microsoft Edge Visual Studio Code version 1.1.7</span><span class="sxs-lookup"><span data-stu-id="2f1dc-179">Microsoft Edge Developer Tools for Visual Studio Code version 1.1.7</span></span>  

<!-- Title: Microsoft Edge DevTools for Visual Studio version 1.1.7  -->  
<!-- Subtitle: Increased target closure reliability, automatically update the side panel, new contextual menu for settings and Changelog, and more. -->  

<span data-ttu-id="2f1dc-180">Microsoft [Edge Tools for Visual Studio Code extension][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] version 1.1.7 fournit devTools de Microsoft Edge version [88][DevtoolsWhatsNew202011Devtools].</span><span class="sxs-lookup"><span data-stu-id="2f1dc-180">The [Microsoft Edge Tools for Visual Studio Code extension][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] version 1.1.7 provides the DevTools from [Microsoft Edge version 88][DevtoolsWhatsNew202011Devtools].</span></span>  <span data-ttu-id="2f1dc-181">Cette extension prend désormais en charge ARM et ne dépend plus [de l'extension Debugger pour Microsoft Edge.][VisualstudioMarketplaceMsjsdiagDebuggerForEdge]</span><span class="sxs-lookup"><span data-stu-id="2f1dc-181">This extension now supports ARM devices and no longer depends on the [Debugger for Microsoft Edge][VisualstudioMarketplaceMsjsdiagDebuggerForEdge] extension.</span></span>  <span data-ttu-id="2f1dc-182">La version 1.1.7 inclut les correctifs et améliorations de bogue suivants.</span><span class="sxs-lookup"><span data-stu-id="2f1dc-182">Version 1.1.7 includes the following bug fixes and improvements.</span></span>  

*   <span data-ttu-id="2f1dc-183">Mise à jour de la fiabilité de la fermeture cible.</span><span class="sxs-lookup"><span data-stu-id="2f1dc-183">Updated the reliability of target closure.</span></span>  
*   <span data-ttu-id="2f1dc-184">Mise à jour du panneau latéral pour qu'il soit actualisé automatiquement lorsque vous déboguer des cibles créées ou détruites.</span><span class="sxs-lookup"><span data-stu-id="2f1dc-184">Updated the side panel to automatically refreshes when you debug targets that are created or destroyed.</span></span>  
*   <span data-ttu-id="2f1dc-185">Ajout d'un nouveau menu contextuel qui vous permet d'accéder plus rapidement aux paramètres d'extension et au dernier changelog.</span><span class="sxs-lookup"><span data-stu-id="2f1dc-185">Added a new contextual menu that gives you faster access to the extension settings and the latest Changelog.</span></span>  
*   <span data-ttu-id="2f1dc-186">Mise à jour et simplification de la publication de la documentation d'extension, y compris les fonctionnalités les plus nouvelles.</span><span class="sxs-lookup"><span data-stu-id="2f1dc-186">Updated and simplified the release of extension documentation including the newest features.</span></span>  
    
<span data-ttu-id="2f1dc-187">Pour mettre à jour manuellement la version 1.1.7, accédez à Mettre à jour [une extension manuellement.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]</span><span class="sxs-lookup"><span data-stu-id="2f1dc-187">To manually update to version 1.1.7, navigate to [Update an extension manually][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually].</span></span>  <span data-ttu-id="2f1dc-188">Vous pouvez signaler des problèmes, puis contribuer à l’extension sur le référentiel [GitHub vscode-edge-devtools][GithubMicrosoftVscodeEdgeDevtools].</span><span class="sxs-lookup"><span data-stu-id="2f1dc-188">You may file issues and contribute to the extension on the [vscode-edge-devtools GitHub repo][GithubMicrosoftVscodeEdgeDevtools].</span></span>  

<!--## Announcements from the Chromium project  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### Ipsum et Chromium  

Lorem al lorem et Chromium  To review the history of this feature in the Chromium open-source project, navigate to Issue [xxxxxxx][CRxxxxxxx].  

:::image type="complex" source="../../media/2021/04/lorem-et-chromium.msft.png" alt-text="Ipsum et Chromium" lightbox="../../media/2021/04/lorem-et-chromium.msft.png":::
   Ipsum et Chromium  
:::image-end:::  -->  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="2f1dc-189">Télécharger les canaux d’aperçu Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2f1dc-189">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="2f1dc-190">Si vous êtes sous Windows, Linux ou macOS, envisagez d'utiliser les [canaux d'aperçu de Microsoft][MicrosoftEdgePreviewChannels] Edge comme navigateur de développement par défaut.</span><span class="sxs-lookup"><span data-stu-id="2f1dc-190">If you are on Windows, Linux, or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="2f1dc-191">Les canaux de prévisualisation vous donnent accès aux dernières fonctionnalités de DevTools.</span><span class="sxs-lookup"><span data-stu-id="2f1dc-191">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="2f1dc-192">Contacter l’équipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="2f1dc-192">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsWhatsNew202001DevtoolsUsingDevtoolsInOtherLanguages]: ../../2020/01/devtools.md#using-the-devtools-in-other-languages "Utilisation de DevTools dans d'autres langues : nouveautés de DevTools (Microsoft Edge 81) | Documents Microsoft"  
[DevtoolsWhatsNew202011Devtools]: ../../2020/11/devtools.md "Nouveautés de DevTools (Microsoft Edge 88) | Documents Microsoft"  
[DevtoolsWhatsNew202011DevtoolsCssVariableDefinitionsInStylesPane]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/11/devtools#css-variable-definitions-in-styles-pane "Définitions de variables CSS dans le volet Styles - Nouveautés de DevTools (Microsoft Edge 88) | Documents Microsoft"  
[DevtoolsWhatsNew202102Devtools]: ../02/devtools.md "Nouveautés de DevTools (Microsoft Edge 90) | Documents Microsoft"  
[DevtoolsWhatsNew202102DevtoolsGroupToolsTogetherInFocusMode]: ../02/devtools.md#group-tools-together-in-focus-mode "Group tools together in Focus Mode - What's New In DevTools (Microsoft Edge 90) | Documents Microsoft"  

[DevtoolsCommandMenuIndexOpenCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index#open-the-command-menu "Ouvrez le menu Commande - Exécutez des commandes avec le menu DevTools Command de Microsoft Edge | Documents Microsoft"  
[DevtoolsCustomizeLocalization]: /microsoft-edge/devtools-guide-chromium/customize/localization "Modifier les paramètres de langue de DevTools | Documents Microsoft"  
[DevtoolsIssuesIndex]: /microsoft-edge/devtools-guide-chromium/issues/index "Recherchez et corrigez les problèmes liés à l’outil des problèmes de Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsServiceWorkerIndex]: /microsoft-edge/devtools-guide-chromium/service-workers/index "Améliorations apportées aux services | Documents Microsoft"  

[ProgressiveWebAppsServiceworkerServiceWorkerLifecycle]: /microsoft-edge/progressive-web-apps-chromium/serviceworker#the-service-worker-lifecycle "Cycle de vie des travailleurs du service : utiliser les travailleurs de service pour gérer les demandes réseau et les notifications Push | Documents Microsoft"  
[ProgressiveWebAppsWebappmanifests]: /microsoft-edge/progressive-web-apps-chromium/webappmanifests "Utiliser le manifeste de l'application Web pour intégrer votre application Web progressive au système d'exploitation | Documents Microsoft"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
<!--[GithubMicrosoftVscodeEdgeDevtoolsPullxxx]: https://github.com/microsoft/vscode-edge-devtools/pull/xxx "Pull xxx: Lorem al Ipsum | GitHub"  -->  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canaux de préversion de Microsoft Edge"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Mettre à jour une extension manuellement - Extension Marketplace | Visual Studio Code"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Outils Microsoft Edge pour Visual Studio Code | Visual Studio Marketplace"  
[VisualstudioMarketplaceMsjsdiagDebuggerForEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Débogueur pour Microsoft Edge | Visual Studio Marketplace"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Bogues Chromium"  
[CR1066604]: https://crbug.com/1066604 "Problème 1066604 : DevTools : voir les détails sur l'installation et l'activation des événements par ServiceWorker | Bogues Chromium"  
[CR1136655]: https://crbug.com/1136655 "Problème 1136655 : Devtools : localisation v2 | Bogues Chromium"  
[CR1185945]: https://crbug.com/1185945 "Problème 1185945 : l'avertissement de manifeste implique que toutes les icônes doivent être carrées | Bogues Chromium"  
[CR1187735]: https://crbug.com/1187735 "Problème 1187735 : Accessibilité : MAS2.1.1 : Clavier : Impossible d'appeler la fonction « Var(..) » à l'aide du clavier | Bogues Chromium"  

[MdnDocsWebCssUsingCssCustomProperties]: https://developer.mozilla.org/docs/Web/CSS/Using_CSS_custom_properties "Utilisation des propriétés personnalisées CSS (variables) | MDN"  

[PwabuilderImagegenerator]: https://www.pwabuilder.com/imageGenerator "Image Generator | PWABuilder"  

<!--  > [!NOTE]
> Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].  
> The original page is found [here](https://developer.chrome.com/blog/new-in-devtools-91) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen
-->
