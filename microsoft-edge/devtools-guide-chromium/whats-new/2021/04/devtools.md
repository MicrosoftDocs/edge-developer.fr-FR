---
description: Les soulignements ondulés mettent en évidence les problèmes de code dans l’outil Éléments, la chronologie de mise à jour du service de travail, etc.
title: Nouveautés de DevTools (Microsoft Edge 91)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 5f499a6c9f1109f80a9d459edf94ed2226734f19
ms.sourcegitcommit: 87ba918b0910373bb645615377709bf140dc9b19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2021
ms.locfileid: "11583458"
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
# <a name="whats-new-in-devtools-microsoft-edge-91"></a><span data-ttu-id="e87cc-104">Nouveautés de DevTools (Microsoft Edge 91)</span><span class="sxs-lookup"><span data-stu-id="e87cc-104">What's New In DevTools (Microsoft Edge 91)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="wavy-underlines-highlight-code-issues-and-improvements-in-elements-tool"></a><span data-ttu-id="e87cc-105">Les soulignements ondulés mettent en évidence les problèmes de code et les améliorations apportées à l’outil Elements</span><span class="sxs-lookup"><span data-stu-id="e87cc-105">Wavy underlines highlight code issues and improvements in Elements tool</span></span>  

<!--  Title: Get code hints in Elements tool  -->  
<!--  Subtitle: Wavy underlines like the ones you see in Visual Studio Code now display in the Elements tool.  Underlines alert you to code issues related to accessibility, compatibility, security, performance, and  so on.  -->  

<span data-ttu-id="e87cc-106">Dans la plupart des IDE modernes, les soulignements ondulés sous le texte indiquent des erreurs de syntaxe.</span><span class="sxs-lookup"><span data-stu-id="e87cc-106">In most modern IDEs, wavy underlines under text indicate syntax errors.</span></span>   <span data-ttu-id="e87cc-107">Dans Microsoft Edge version 91 ou ultérieure, les soulignements ondulés s’affichent sous HTML dans la vue **DOM** de **l’outil Elements.**</span><span class="sxs-lookup"><span data-stu-id="e87cc-107">In Microsoft Edge version 91 or later, wavy underlines display under HTML in the **DOM** view of the **Elements** tool.</span></span>  <span data-ttu-id="e87cc-108">Les soulignements ondulés indiquent des problèmes de code et des suggestions liés à l’accessibilité, la compatibilité, les performances, etc.</span><span class="sxs-lookup"><span data-stu-id="e87cc-108">The wavy underlines indicate code issues and suggestions related to accessibility, compatibility, performance, and so on.</span></span>  <span data-ttu-id="e87cc-109">Pour plus d’informations sur la façon de passer en revue et de modifier les problèmes, accédez à Rechercher et résoudre les problèmes avec [l’outil Microsoft Edge DevTools Issues][DevtoolsIssuesIndex].</span><span class="sxs-lookup"><span data-stu-id="e87cc-109">For more information about how to review and edit issues, navigate to [Find and fix problems with the Microsoft Edge DevTools Issues tool][DevtoolsIssuesIndex].</span></span>  

<span data-ttu-id="e87cc-110">Pour ouvrir **l’outil Problèmes** et en savoir plus sur le problème et comment le résoudre, effectuer l’une des actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="e87cc-110">To open the **Issues** tool and learn more about the issue and how to fix it, complete one of the following actions.</span></span>  

*   <span data-ttu-id="e87cc-111">Sélectionnez et `Shift` maintenez, puis choisissez un soulignement ondulé.</span><span class="sxs-lookup"><span data-stu-id="e87cc-111">Select and hold `Shift`, and then choose any wavy underline.</span></span>  
*   <span data-ttu-id="e87cc-112">Effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="e87cc-112">Complete the following actions.</span></span>  
    1.  <span data-ttu-id="e87cc-113">Pointez sur n’importe quel soulignement ondulé.</span><span class="sxs-lookup"><span data-stu-id="e87cc-113">Hover on any wavy underline.</span></span>  
    1.  <span data-ttu-id="e87cc-114">Ouvrez le menu contextuel \(cliquez avec le bouton droit\).</span><span class="sxs-lookup"><span data-stu-id="e87cc-114">Open the contextual menu \(right-click\).</span></span>  
    1.  <span data-ttu-id="e87cc-115">Choose **Show in Issues**.</span><span class="sxs-lookup"><span data-stu-id="e87cc-115">Choose **Show in Issues**.</span></span>  
        
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/elements-iframe-highlight-issues.msft.png" alt-text="Choisir l’erreur soulignée dans l’outil Éléments" lightbox="../../media/2021/04/elements-iframe-highlight-issues.msft.png":::
         <span data-ttu-id="e87cc-117">Choisir l’erreur soulignée dans **l’outil Éléments**</span><span class="sxs-lookup"><span data-stu-id="e87cc-117">Choose the underlined error in the **Elements** tool</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/elements-iframe-highlight-issues-focus.msft.png" alt-text="Afficher les détails des erreurs dans l’outil Problèmes" lightbox="../../media/2021/04/elements-iframe-highlight-issues-focus.msft.png":::
         <span data-ttu-id="e87cc-119">Afficher les détails des erreurs dans **l’outil Problèmes**</span><span class="sxs-lookup"><span data-stu-id="e87cc-119">Display error details in the **Issues** tool</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="learn-about-devtools-with-informative-tooltips"></a><span data-ttu-id="e87cc-120">En savoir plus sur DevTools grâce à des infobulles informatives</span><span class="sxs-lookup"><span data-stu-id="e87cc-120">Learn about DevTools with informative tooltips</span></span>  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<!--  Title: Learn more about DevTools with DevTools Tooltips  -->  
<!--  Subtitle: Informative overlays are now available in the default DevTools interface.  -->  

<span data-ttu-id="e87cc-121">La fonctionnalité d’outils DevTools vous permet d’en savoir plus sur les différents outils et volets de DevTools.</span><span class="sxs-lookup"><span data-stu-id="e87cc-121">The DevTools Tooltips feature helps you learn about all the different tools and panes in DevTools.</span></span>  <span data-ttu-id="e87cc-122">Pour désactiver les bulles, sélectionnez `Esc` .</span><span class="sxs-lookup"><span data-stu-id="e87cc-122">To turn off Tooltips, select `Esc`.</span></span>  <span data-ttu-id="e87cc-123">Pour activer les bulles, effectuer l’une des actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="e87cc-123">To turn on Tooltips, complete one of the following actions.</span></span>  

*   <span data-ttu-id="e87cc-124">Sélectionnez `Ctrl` + `Shift` + `H` \(Windows/Linux\) ou `Cmd` + `Shift` + `H` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="e87cc-124">Select `Ctrl`+`Shift`+`H` \(Windows/Linux\) or `Cmd`+`Shift`+`H` \(macOS\).</span></span>  
*   <span data-ttu-id="e87cc-125">[Ouvrez le menu Commande,][DevtoolsCommandMenuIndexOpenCommandMenu] puis tapez `tooltips` .</span><span class="sxs-lookup"><span data-stu-id="e87cc-125">[Open the Command Menu][DevtoolsCommandMenuIndexOpenCommandMenu] and then type `tooltips`.</span></span>  
*   <span data-ttu-id="e87cc-126">Choose **Customize and control DevTools** \( `...` \) > **Help**  >  **Toggle the DevTools Tooltips**.</span><span class="sxs-lookup"><span data-stu-id="e87cc-126">Choose **Customize and control DevTools** \(`...`\) > **Help** > **Toggle the DevTools Tooltips**.</span></span>  

<span data-ttu-id="e87cc-127">En outre, si vous activer le mode Focus et l’expérience d’bulles d’outils [DevTools,][DevtoolsWhatsNew202102DevtoolsGroupToolsTogetherInFocusMode] vous pouvez également choisir le bouton Basculer le bouton d’outils **DevTools** \( \) en bas de la barre `?` d’activité. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="e87cc-127">Also, if you turn on the [Focus Mode and DevTools Tooltips][DevtoolsWhatsNew202102DevtoolsGroupToolsTogetherInFocusMode] experiment, you may also choose the **Toggle the DevTools Tooltips** \(`?`\) button at the bottom of the **Activity Bar**.</span></span>  

<span data-ttu-id="e87cc-128">Pour afficher plus d’informations sur l’utilisation de DevTools, allumez les info-bulles, puis pointez sur chaque région en plan des DevTools.</span><span class="sxs-lookup"><span data-stu-id="e87cc-128">To display more information about how to use the DevTools, turn on Tooltips, and then hover on each outlined region of the DevTools.</span></span>  

:::image type="complex" source="../../media/2021/04/elements-issues-focus-mode-tooltips.msft.png" alt-text="Pointez n’importe où dans la région mise en surbrillez de l’outil Problèmes pour afficher plus de détails" lightbox="../../media/2021/04/elements-issues-focus-mode-tooltips.msft.png":::
   <span data-ttu-id="e87cc-130">Pointez n’importe où dans \*\*\*\* la région mise en surbrillez de l’outil Problèmes pour afficher plus de détails</span><span class="sxs-lookup"><span data-stu-id="e87cc-130">Hover on anywhere in the highlighted region of the **Issues** tool to display more details</span></span>  
:::image-end:::  

## <a name="service-worker-update-timeline"></a><span data-ttu-id="e87cc-131">Chronologie de mise à jour du service de travail</span><span class="sxs-lookup"><span data-stu-id="e87cc-131">Service worker update timeline</span></span>  

<!--todo:  Update the linked [Service Worker improvements][DevtoolsServiceWorkerIndex] article.  -->  

<!--  Title: The tasks associated with your Service Worker  -->  
<!--  Subtitle: Debug with Service Worker Update Cycle  -->  

<span data-ttu-id="e87cc-132">Dans Microsoft Edge version 91 ou ultérieure, si vous êtes développeur Progressive Web App ou Service Worker, affichez le cycle de vie de mise à jour de vos employés de service sous forme de chronologie dans l’outil **Application.**</span><span class="sxs-lookup"><span data-stu-id="e87cc-132">In Microsoft Edge version 91 or later, if you're a Progressive Web App or Service Worker developer, display the update lifecycle of your Service Workers as a timeline in the **Application** tool.</span></span>  <span data-ttu-id="e87cc-133">Cette fonctionnalité vous permet de comprendre le temps que votre service de travail passe à chacune des étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="e87cc-133">This feature helps you understand the time your Service Worker spends in each of the following stages.</span></span>  

*   **<span data-ttu-id="e87cc-134">Install</span><span class="sxs-lookup"><span data-stu-id="e87cc-134">Install</span></span>**  
*   **<span data-ttu-id="e87cc-135">Attendre</span><span class="sxs-lookup"><span data-stu-id="e87cc-135">Wait</span></span>**  
*   **<span data-ttu-id="e87cc-136">Activer</span><span class="sxs-lookup"><span data-stu-id="e87cc-136">Activate</span></span>**  
    
:::image type="complex" source="../../media/2021/04/application-service-workers-update-cycle-version-73-focus.msft.png" alt-text="Passer en revue la chronologie du cycle de mise à jour pour votre service de travail" lightbox="../../media/2021/04/application-service-workers-update-cycle-version-73-focus.msft.png":::
   <span data-ttu-id="e87cc-138">Passer en revue **la chronologie** du cycle de mise **à jour** pour votre service de travail</span><span class="sxs-lookup"><span data-stu-id="e87cc-138">Review the **Timeline** in the **Update Cycle** for your Service Worker</span></span>  
:::image-end:::  

<span data-ttu-id="e87cc-139">Pour plus d’informations sur le cycle de vie de vos employés de service, accédez au cycle de vie des travailleurs [de service.][ProgressiveWebAppsServiceworkerServiceWorkerLifecycle]</span><span class="sxs-lookup"><span data-stu-id="e87cc-139">For more information about the lifecycle of your Service Workers, navigate to [The Service Worker lifecycle][ProgressiveWebAppsServiceworkerServiceWorkerLifecycle].</span></span>  <span data-ttu-id="e87cc-140">Pour plus d’informations sur les outils de débogage pour les applications web progressives et les travailleurs de service dans DevTools, accédez aux améliorations apportées aux services [de travail.][DevtoolsServiceWorkerIndex]</span><span class="sxs-lookup"><span data-stu-id="e87cc-140">For more information about debugging tools for Progressive Web Apps and Service Workers in the DevTools, navigate to [Service Worker improvements][DevtoolsServiceWorkerIndex].</span></span>  <span data-ttu-id="e87cc-141">Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans Chromium projet open source, accédez au problème [1066604][CR1066604].</span><span class="sxs-lookup"><span data-stu-id="e87cc-141">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [1066604][CR1066604].</span></span>  

## <a name="progressive-web-apps-no-longer-display-warnings-for-non-square-icons"></a><span data-ttu-id="e87cc-142">Les applications web progressives n’affichent plus d’avertissements pour les icônes non carrées</span><span class="sxs-lookup"><span data-stu-id="e87cc-142">Progressive Web Apps no longer display warnings for non-square icons</span></span>  

<!--  Title: Non-square icons in app manifest no longer produce warnings  -->  
<!--  Subtitle: As long as square icons are included in the app manifest, non-square icons no longer produce warnings  -->  

<span data-ttu-id="e87cc-143">Dans [Microsoft Edge version 90][DevtoolsWhatsNew202102Devtools] ou antérieure, si le manifeste d’application web de votre PWA incluait une icône non carrée, un avertissement s’affichait dans la section Erreurs et **avertissements** pour chaque icône non carrée.</span><span class="sxs-lookup"><span data-stu-id="e87cc-143">In [Microsoft Edge version 90][DevtoolsWhatsNew202102Devtools] or earlier, if the Web App Manifest of your PWA included a non-square icon, a warning was displayed in the **Errors and Warnings**  section for each non-square icon.</span></span>  <span data-ttu-id="e87cc-144">Dans Microsoft Edge version 91 ou ultérieure, la **section** Manifeste de l’outil **Application** n’affiche aucun avertissement si vous fournissez au moins une icône carrée.</span><span class="sxs-lookup"><span data-stu-id="e87cc-144">In Microsoft Edge version 91 or later, the **Manifest** section in the **Application** tool displays no warnings if you provide at least one square icon.</span></span>  <span data-ttu-id="e87cc-145">Si vous ne fournissez aucune icône carrée, un avertissement affiche le message suivant.</span><span class="sxs-lookup"><span data-stu-id="e87cc-145">If you don't provide any square icons, a warning displays the following message.</span></span>  

```output
Most operating systems require square icons.  Please include at least one square icon in the array.  
```  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/edge89-application-manifest-errors-and-warnings.msft.png" alt-text="Dans Microsoft Edge version 90 ou antérieure, une erreur s’affiche pour chaque icône non carrée" lightbox="../../media/2021/04/edge89-application-manifest-errors-and-warnings.msft.png":::
         <span data-ttu-id="e87cc-147">Dans Microsoft Edge version 90 ou antérieure, une erreur s’affiche pour chaque icône non carrée</span><span class="sxs-lookup"><span data-stu-id="e87cc-147">In Microsoft Edge version 90 or earlier, an error displays for each icon that is non-square</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/edge91-application-manifest-errors-and-warnings.msft.png" alt-text="Dans Microsoft Edge version 91 ou ultérieure, aucune erreur ne s’affiche lorsque vous fournissez au moins une icône carrée" lightbox="../../media/2021/04/edge91-application-manifest-errors-and-warnings.msft.png":::
         <span data-ttu-id="e87cc-149">Dans Microsoft Edge version 91 ou ultérieure, aucune erreur ne s’affiche lorsque vous fournissez au moins une icône carrée</span><span class="sxs-lookup"><span data-stu-id="e87cc-149">In Microsoft Edge version 91 or later, no error displays when you provide at least one square icon</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="e87cc-150">Pour passer en revue les erreurs et les avertissements dans votre manifeste d’application web, accédez à l’outil **Application** et choisissez la section **Manifeste.**</span><span class="sxs-lookup"><span data-stu-id="e87cc-150">To review errors and warnings in your Web App Manifest, navigate to the **Application** tool and choose the **Manifest** section.</span></span>  <span data-ttu-id="e87cc-151">Les erreurs et avertissements sont répertoriés sous le titre **Erreurs et avertissements.**</span><span class="sxs-lookup"><span data-stu-id="e87cc-151">Errors and warnings are listed under the **Errors and Warnings** heading.</span></span>  <span data-ttu-id="e87cc-152">Pour plus d’informations sur le manifeste d’application web, accédez à Utiliser le manifeste d’application web pour intégrer votre application Web progressive [dans le système d’exploitation.][ProgressiveWebAppsWebappmanifests]</span><span class="sxs-lookup"><span data-stu-id="e87cc-152">For more information about the Web App Manifest, navigate to [Use the Web App Manifest to integrate your Progressive Web App into the Operating System][ProgressiveWebAppsWebappmanifests].</span></span>  <span data-ttu-id="e87cc-153">Pour créer des icônes à inclure dans votre manifeste d’application web, accédez au générateur [d’images PWABuilder.][PwabuilderImagegenerator]</span><span class="sxs-lookup"><span data-stu-id="e87cc-153">To create icons to include in your Web App Manifest, navigate to the [PWABuilder Image Generator][PwabuilderImagegenerator].</span></span>  <span data-ttu-id="e87cc-154">Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans le projet open source Chromium, accédez à Problème [1185945][CR1185945].</span><span class="sxs-lookup"><span data-stu-id="e87cc-154">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [1185945][CR1185945].</span></span>  

## <a name="localized-devtools-now-supported-in-chromium-based-browsers"></a><span data-ttu-id="e87cc-155">DevTools localisées désormais prise en charge dans Chromium navigateurs basés sur les navigateurs</span><span class="sxs-lookup"><span data-stu-id="e87cc-155">Localized DevTools now supported in Chromium-based browsers</span></span>  

<!--  Title: Localization for all  -->  
<!--  Subtitle: Match browser language enabled to all Chromium-based browsers  -->  

<span data-ttu-id="e87cc-156">À partir [Microsoft Edge version 81,][DevtoolsWhatsNew202001DevtoolsUsingDevtoolsInOtherLanguages]Microsoft Edge DevTools s’affiche dans votre propre langue.</span><span class="sxs-lookup"><span data-stu-id="e87cc-156">Starting in [Microsoft Edge version 81][DevtoolsWhatsNew202001DevtoolsUsingDevtoolsInOtherLanguages], Microsoft Edge DevTools displays in your own language.</span></span>  <span data-ttu-id="e87cc-157">De nombreux développeurs utilisent d’autres outils de développement tels que StackOverflow et Visual Studio Code dans leur langue native, et pas seulement en anglais.</span><span class="sxs-lookup"><span data-stu-id="e87cc-157">Many developers use other developer tools like StackOverflow and Visual Studio Code in their native language, not just in English.</span></span>  <span data-ttu-id="e87cc-158">L Microsoft Edge’équipe DevTools, l’équipe Chrome DevTools et l’équipe Google Chrome ont travaillé pour offrir la même expérience dans tous les navigateurs basés sur Chromium.</span><span class="sxs-lookup"><span data-stu-id="e87cc-158">The Microsoft Edge DevTools team, Chrome DevTools team, and the Google Lighthouse team collaborated to provide the same experience in all Chromium-based browsers.</span></span>  <span data-ttu-id="e87cc-159">Pour plus d’informations sur l’utilisation de DevTools dans votre langue, accédez à Modifier les paramètres de langue [de DevTools.][DevtoolsCustomizeLocalization]</span><span class="sxs-lookup"><span data-stu-id="e87cc-159">For more information about how to use DevTools in your language, navigate to [Change DevTools language settings][DevtoolsCustomizeLocalization].</span></span>  <span data-ttu-id="e87cc-160">Pour plus d’informations sur la collaboration sur cette fonctionnalité dans le projet open source Chromium, accédez à [1136655][CR1136655].</span><span class="sxs-lookup"><span data-stu-id="e87cc-160">For more information about the collaboration on this feature in the Chromium open-source project, navigate to [1136655][CR1136655].</span></span>  

:::image type="complex" source="../../media/2021/04/japanese-browser-japanese-navigation-elements-3d-view.msft.png" alt-text="Microsoft Edge navigateur et DevTools sont définies sur japonais" lightbox="../../media/2021/04/japanese-browser-japanese-navigation-elements-3d-view.msft.png":::
   <span data-ttu-id="e87cc-162">Microsoft Edge navigateur et DevTools sont définies sur japonais</span><span class="sxs-lookup"><span data-stu-id="e87cc-162">Microsoft Edge browser and DevTools set to Japanese</span></span>  
:::image-end:::  

## <a name="use-the-keyboard-to-navigate-to-css-variables"></a><span data-ttu-id="e87cc-163">Utiliser le clavier pour accéder aux variables CSS</span><span class="sxs-lookup"><span data-stu-id="e87cc-163">Use the keyboard to navigate to CSS variables</span></span>  

<!--  Title: Navigate to CSS variables with the arrow keys  -->  
<!--  Subtitle: In the Styles pane, use the arrow keys to choose CSS variables.  Select `Enter` to see the variable definition.  -->  

<span data-ttu-id="e87cc-164">À partir [Microsoft Edge version 88,][DevtoolsWhatsNew202011DevtoolsCssVariableDefinitionsInStylesPane]le volet **Styles** affiche les variables CSS et fournit un lien directement vers la définition de chaque variable.</span><span class="sxs-lookup"><span data-stu-id="e87cc-164">Starting in [Microsoft Edge version 88][DevtoolsWhatsNew202011DevtoolsCssVariableDefinitionsInStylesPane], the **Styles** pane displays CSS variables and provides a link directly to the definition of each variable.</span></span>  <span data-ttu-id="e87cc-165">Dans Microsoft Edge version 91 ou ultérieure, vous pouvez utiliser les touches de direction pour accéder facilement aux variables CSS.</span><span class="sxs-lookup"><span data-stu-id="e87cc-165">In Microsoft Edge version 91 or later, you may use the arrow keys to easily navigate to CSS variables.</span></span>  <span data-ttu-id="e87cc-166">Pour ouvrir la définition dans le volet **Styles,** pointez sur une variable, puis sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="e87cc-166">To open the definition in the **Styles** pane, hover on a variable, and then select `Enter`.</span></span>  <span data-ttu-id="e87cc-167">Pour plus d’informations sur les variables CSS, accédez à [l’utilisation de propriétés personnalisées CSS (variables).][MdnDocsWebCssUsingCssCustomProperties]</span><span class="sxs-lookup"><span data-stu-id="e87cc-167">For more information about CSS variables, navigate to [Using CSS custom properties (variables)][MdnDocsWebCssUsingCssCustomProperties].</span></span>  <span data-ttu-id="e87cc-168">Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans le projet open source Chromium, accédez à Problème [1187735][CR1187735].</span><span class="sxs-lookup"><span data-stu-id="e87cc-168">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [1187735][CR1187735].</span></span>  

:::image type="complex" source="../../media/2021/04/elements-styles-body-background-color-theme-body-background.msft.png" alt-text="Variable CSS --theme-body-background mise en évidence dans le volet Styles" lightbox="../../media/2021/04/elements-styles-body-background-color-theme-body-background.msft.png":::
   <span data-ttu-id="e87cc-170">Variable `--theme-body-background` CSS mise en évidence dans le **volet Styles**</span><span class="sxs-lookup"><span data-stu-id="e87cc-170">The `--theme-body-background` CSS variable highlighted in the **Styles** pane</span></span>  
:::image-end:::  

## <a name="issues-are-automatically-sorted-by-severity"></a><span data-ttu-id="e87cc-171">Les problèmes sont automatiquement triés par gravité</span><span class="sxs-lookup"><span data-stu-id="e87cc-171">Issues are automatically sorted by severity</span></span>  

<!-- Title: Display Issues in severity order  -->  
<!-- Subtitle: Entries in the Issues tool now display in severity order and allow you to focus your updates on the most important issues. -->  

<span data-ttu-id="e87cc-172">**L’outil Problèmes** affiche des recommandations pour améliorer votre site web, notamment l’accessibilité, les performances, la sécurité, etc.</span><span class="sxs-lookup"><span data-stu-id="e87cc-172">The **Issues** tool displays recommendations to improve your website, including accessibility, performance, security, and so on.</span></span> <span data-ttu-id="e87cc-173">En fonction de vos commentaires, les problèmes sont désormais automatiquement triés par gravité.</span><span class="sxs-lookup"><span data-stu-id="e87cc-173">Based on your feedback, issues are now automatically sorted by severity.</span></span>  <span data-ttu-id="e87cc-174">Dans chaque catégorie de commentaires, \*\*\*\* chaque problème marqué comme erreur apparaît en premier, suivi de chaque problème marqué comme **avertissement,** puis de chaque problème marqué comme **conseil.**</span><span class="sxs-lookup"><span data-stu-id="e87cc-174">In each feedback category, each issue marked as an **Error** appears first, followed each issue marked as a **Warning**, then each issue marked as a **Tip**.</span></span>  <span data-ttu-id="e87cc-175">Pour vous aider à affiner vos problèmes, des options de filtre supplémentaires sont prévues pour une prochaine mise à jour.</span><span class="sxs-lookup"><span data-stu-id="e87cc-175">To help you refine your issues, extra filter options are planned for a future update.</span></span>  <span data-ttu-id="e87cc-176">Pour plus d’informations sur la façon de passer en revue les problèmes, accédez à Rechercher et résoudre les problèmes avec [l’outil Microsoft Edge DevTools Issues][DevtoolsIssuesIndex].</span><span class="sxs-lookup"><span data-stu-id="e87cc-176">For more information about how to review issues, navigate to [Find and fix problems with the Microsoft Edge DevTools Issues tool][DevtoolsIssuesIndex].</span></span>  

:::image type="complex" source="../../media/2021/04/elements-issues-ordered-issues.msft.png" alt-text="L’outil Problèmes affiche les problèmes triés par gravité" lightbox="../../media/2021/04/elements-issues-ordered-issues.msft.png":::
   <span data-ttu-id="e87cc-178">**L’outil Problèmes** affiche les problèmes triés par gravité</span><span class="sxs-lookup"><span data-stu-id="e87cc-178">The **Issues** tool displays sorted issues by severity</span></span>  
:::image-end:::  

## <a name="microsoft-edge-developer-tools-for-visual-studio-code-version-117"></a><span data-ttu-id="e87cc-179">Microsoft Edge Outils de développement Visual Studio Code version 1.1.7</span><span class="sxs-lookup"><span data-stu-id="e87cc-179">Microsoft Edge Developer Tools for Visual Studio Code version 1.1.7</span></span>  

<!-- Title: Microsoft Edge DevTools for Visual Studio version 1.1.7  -->  
<!-- Subtitle: Increased target closure reliability, automatically update the side panel, new contextual menu for settings and Changelog, and more. -->  

<span data-ttu-id="e87cc-180">Les [outils][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] Microsoft Edge pour Visual Studio Code version 1.1.7 fournissent les outils DevTools de [Microsoft Edge version 88.][DevtoolsWhatsNew202011Devtools]</span><span class="sxs-lookup"><span data-stu-id="e87cc-180">The [Microsoft Edge Tools for Visual Studio Code extension][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] version 1.1.7 provides the DevTools from [Microsoft Edge version 88][DevtoolsWhatsNew202011Devtools].</span></span>  <span data-ttu-id="e87cc-181">Cette extension prend désormais en charge ARM et ne dépend plus du débogger [pour Microsoft Edge][VisualstudioMarketplaceMsjsdiagDebuggerForEdge] extension.</span><span class="sxs-lookup"><span data-stu-id="e87cc-181">This extension now supports ARM devices and no longer depends on the [Debugger for Microsoft Edge][VisualstudioMarketplaceMsjsdiagDebuggerForEdge] extension.</span></span>  <span data-ttu-id="e87cc-182">La version 1.1.7 inclut les correctifs et améliorations de bogue suivants.</span><span class="sxs-lookup"><span data-stu-id="e87cc-182">Version 1.1.7 includes the following bug fixes and improvements.</span></span>  

*   <span data-ttu-id="e87cc-183">Mise à jour de la fiabilité de la fermeture cible.</span><span class="sxs-lookup"><span data-stu-id="e87cc-183">Updated the reliability of target closure.</span></span>  
*   <span data-ttu-id="e87cc-184">Mise à jour du panneau latéral pour qu’il soit actualisé automatiquement lorsque vous déboguer des cibles créées ou détruites.</span><span class="sxs-lookup"><span data-stu-id="e87cc-184">Updated the side panel to automatically refreshes when you debug targets that are created or destroyed.</span></span>  
*   <span data-ttu-id="e87cc-185">Ajout d’un nouveau menu contextuel qui vous permet d’accéder plus rapidement aux paramètres d’extension et au dernier changelog.</span><span class="sxs-lookup"><span data-stu-id="e87cc-185">Added a new contextual menu that gives you faster access to the extension settings and the latest Changelog.</span></span>  
*   <span data-ttu-id="e87cc-186">Mise à jour et simplification de la publication de la documentation d’extension, y compris les fonctionnalités les plus nouvelles.</span><span class="sxs-lookup"><span data-stu-id="e87cc-186">Updated and simplified the release of extension documentation including the newest features.</span></span>  
    
<span data-ttu-id="e87cc-187">Pour mettre à jour manuellement la version 1.1.7, accédez à Mettre à jour [une extension manuellement.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]</span><span class="sxs-lookup"><span data-stu-id="e87cc-187">To manually update to version 1.1.7, navigate to [Update an extension manually][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually].</span></span>  <span data-ttu-id="e87cc-188">Vous pouvez signaler des problèmes, puis contribuer à l’extension sur le référentiel [GitHub vscode-edge-devtools][GithubMicrosoftVscodeEdgeDevtools].</span><span class="sxs-lookup"><span data-stu-id="e87cc-188">You may file issues and contribute to the extension on the [vscode-edge-devtools GitHub repo][GithubMicrosoftVscodeEdgeDevtools].</span></span>  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="e87cc-189">Annonces du projet de Chromium</span><span class="sxs-lookup"><span data-stu-id="e87cc-189">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="visualize-css-scroll-snap"></a><span data-ttu-id="e87cc-190">Afficher l’achemin de défilement CSS</span><span class="sxs-lookup"><span data-stu-id="e87cc-190">Visualize CSS scroll-snap</span></span>  

<span data-ttu-id="e87cc-191">Vous pouvez maintenant faire bascule le badge dans l’outil Elements pour inspecter l’alignement de l’alignement en `scroll-snap` défilement CSS. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="e87cc-191">You may now toggle the `scroll-snap` badge in the **Elements** tool to inspect the CSS scroll-snap alignment.</span></span>  <span data-ttu-id="e87cc-192">Lorsqu’un élément HTML de votre page web s’y est appliqué, un badge s’affiche à côté de `scroll-snap-type` `scroll-snap` celui-ci dans **l’outil Elements.**</span><span class="sxs-lookup"><span data-stu-id="e87cc-192">When an HTML element on your webpage has `scroll-snap-type` applied to it, a `scroll-snap` badge displays next to it in the **Elements** tool.</span></span>  <span data-ttu-id="e87cc-193">Choisissez le badge pour activer \(ou désactiver\) l’affichage d’une superposition d’un défilement sur la page web.</span><span class="sxs-lookup"><span data-stu-id="e87cc-193">Choose the badge to turn on \(or off\) the display of a scroll-snap overlay on the webpage.</span></span>  <span data-ttu-id="e87cc-194">Pour consulter un exemple de page web, [accédez à Scroll Ancrer Demo][GlitchMicrosoftEdgeChromiumDevtoolsCssDbgStoriesCssScrollSnapHtml].</span><span class="sxs-lookup"><span data-stu-id="e87cc-194">To review an example webpage, navigate to [Scroll Snap Demo][GlitchMicrosoftEdgeChromiumDevtoolsCssDbgStoriesCssScrollSnapHtml].</span></span>  <span data-ttu-id="e87cc-195">Dans l’exemple, les points s’affichent sur les bords en snap.</span><span class="sxs-lookup"><span data-stu-id="e87cc-195">In the example, dots display on snap edges.</span></span>  <span data-ttu-id="e87cc-196">Le port de défilement a un plan plein tandis que les éléments d’a snap ont des tirets.</span><span class="sxs-lookup"><span data-stu-id="e87cc-196">The scroll port has a solid outline while the snap items have dash outlines.</span></span>  <span data-ttu-id="e87cc-197">Le remplissage de défilement est rempli en vert tandis que la marge de défilement est remplie en orange.</span><span class="sxs-lookup"><span data-stu-id="e87cc-197">The scroll padding is filled in green while the scroll margin is filled in orange.</span></span>  <span data-ttu-id="e87cc-198">Pour passer en revue l’historique de cette fonctionnalité dans Chromium projet open source, accédez au problème [862450][CR862450].</span><span class="sxs-lookup"><span data-stu-id="e87cc-198">To review the history of this feature in the Chromium open-source project, navigate to Issue [862450][CR862450].</span></span>  

:::image type="complex" source="../../media/2021/04/elements-scroll-snap-highlight.msft.png" alt-text="CSS scroll-snap" lightbox="../../media/2021/04/elements-scroll-snap-highlight.msft.png":::
   <span data-ttu-id="e87cc-200">CSS scroll-snap</span><span class="sxs-lookup"><span data-stu-id="e87cc-200">CSS scroll-snap</span></span>  
:::image-end:::  

### <a name="new-memory-inspector-tool"></a><span data-ttu-id="e87cc-201">Nouvel outil Inspecteur de mémoire</span><span class="sxs-lookup"><span data-stu-id="e87cc-201">New Memory Inspector tool</span></span>  

<span data-ttu-id="e87cc-202">Utilisez le nouvel outil **Inspecteur de** mémoire pour inspecter une `ArrayBuffer` mémoire JavaScript et Wasm.</span><span class="sxs-lookup"><span data-stu-id="e87cc-202">Use the new **Memory Inspector** tool to inspect an `ArrayBuffer` in JavaScript and Wasm memory.</span></span>  <span data-ttu-id="e87cc-203">Ouvrez la [page web de démonstration Mémoire dans JS.][GlitchMemoryInspectorDemoJsHtml]</span><span class="sxs-lookup"><span data-stu-id="e87cc-203">Open the [Memory in JS][GlitchMemoryInspectorDemoJsHtml] demo webpage.</span></span>  <span data-ttu-id="e87cc-204">Dans **l’outil Sources,** ouvrez `memory-write-wasm` le fichier et définissez un point d’arrêt à la `0x03c` ligne.</span><span class="sxs-lookup"><span data-stu-id="e87cc-204">In the **Sources** tool, open the `memory-write-wasm` file, and set a breakpoint at line `0x03c`.</span></span>  <span data-ttu-id="e87cc-205">Actualisez la page web.</span><span class="sxs-lookup"><span data-stu-id="e87cc-205">Refresh the webpage.</span></span>  <span data-ttu-id="e87cc-206">Développez la section **Étendue** dans le volet débogger.</span><span class="sxs-lookup"><span data-stu-id="e87cc-206">Expand the **Scope** section in the debugger pane.</span></span>  <span data-ttu-id="e87cc-207">La nouvelle icône s’affiche à côté de la valeur **de la mémoire** tampon.</span><span class="sxs-lookup"><span data-stu-id="e87cc-207">The new icon is displayed next to the **buffer** value.</span></span>  <span data-ttu-id="e87cc-208">Choisissez-le pour ouvrir le nouvel outil **Inspecteur de** mémoire.</span><span class="sxs-lookup"><span data-stu-id="e87cc-208">Choose it to open the new **Memory Inspector** tool.</span></span>  

<span data-ttu-id="e87cc-209">Pour en savoir plus sur le débogage dans l’outil **Sources,** accédez au volet Utilisation du déboguer pour déboguer du [code JavaScript.][DevtoolsSourcesUsingDebuggerPaneToDebugJavascriptCode]</span><span class="sxs-lookup"><span data-stu-id="e87cc-209">To learn more about debugging in the **Sources** tool, navigate to [Using the Debugger pane to debug JavaScript code][DevtoolsSourcesUsingDebuggerPaneToDebugJavascriptCode].</span></span>  <span data-ttu-id="e87cc-210">Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez à Problème [1166577][CR1166577].</span><span class="sxs-lookup"><span data-stu-id="e87cc-210">To review the history of this feature in the Chromium open-source project, navigate to Issue [1166577][CR1166577].</span></span>  

:::image type="complex" source="../../media/2021/04/sources-memory-write-wasm-breakpoint-scope-reveal-in-memory-inspector-panel.msft.png" alt-text="Outil Inspecteur de mémoire" lightbox="../../media/2021/04/sources-memory-write-wasm-breakpoint-scope-reveal-in-memory-inspector-panel.msft.png":::
   <span data-ttu-id="e87cc-212">**Outil Inspecteur de** mémoire</span><span class="sxs-lookup"><span data-stu-id="e87cc-212">**Memory inspector** tool</span></span>  
:::image-end:::  

### <a name="new-badge-settings-pane-in-the-elements-tool"></a><span data-ttu-id="e87cc-213">Volet Nouveaux paramètres de badge dans l’outil Éléments</span><span class="sxs-lookup"><span data-stu-id="e87cc-213">New Badge settings pane in the Elements tool</span></span>  

<span data-ttu-id="e87cc-214">À présent, utilisez les **paramètres de badge dans** l’outil **Éléments** pour activer \(ou désactiver\) les badges individuels.</span><span class="sxs-lookup"><span data-stu-id="e87cc-214">Now, use the **Badge settings** in the **Elements** tool to turn on \(or off\) individual badges.</span></span>  <span data-ttu-id="e87cc-215">Utilisez cette fonctionnalité pour personnaliser et rester concentré sur les badges importants pendant que vous inspectez les pages web.</span><span class="sxs-lookup"><span data-stu-id="e87cc-215">Use this feature to customize and stay focused on important badges while you inspect webpages.</span></span>  <span data-ttu-id="e87cc-216">Pour afficher le volet des paramètres de badge en haut de l’outil **Éléments,** effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="e87cc-216">To display the badge settings pane at the top of the **Elements** tool, complete the following actions.</span></span>  

1.  <span data-ttu-id="e87cc-217">Pointez sur n’importe quel élément.</span><span class="sxs-lookup"><span data-stu-id="e87cc-217">Hover on any element.</span></span>  
1.  <span data-ttu-id="e87cc-218">Ouvrez le menu contextuel \(cliquez avec le bouton droit\).</span><span class="sxs-lookup"><span data-stu-id="e87cc-218">Open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="e87cc-219">Choisissez **les paramètres de badge...**.</span><span class="sxs-lookup"><span data-stu-id="e87cc-219">Choose **Badge settings...**.</span></span>  
    
<span data-ttu-id="e87cc-220">Pour afficher \(ou masquer\) les badges, sélectionnez \(ou supprimez\) la case à cocher en regard du nom du badge.</span><span class="sxs-lookup"><span data-stu-id="e87cc-220">To display \(or hide\) the badges, choose \(or remove\) the checkbox next to the badge name.</span></span>  

<!--  To review the history of this feature in the Chromium open-source project, navigate to Issue [1066772][CR1066772].  -->  

:::image type="complex" source="../../media/2021/04/elements-contextual-menu-badge-settings.msft.png" alt-text="Volet Paramètres du badge dans l’outil Éléments" lightbox="../../media/2021/04/elements-contextual-menu-badge-settings.msft.png":::
   <span data-ttu-id="e87cc-222">**Volet Paramètres du** badge dans l’outil **Éléments**</span><span class="sxs-lookup"><span data-stu-id="e87cc-222">**Badge settings** pane in the **Elements** tool</span></span>  
:::image-end:::  

### <a name="enhanced-image-preview-with-aspect-ratio-information"></a><span data-ttu-id="e87cc-223">Aperçu d’image amélioré avec des informations sur les proportions</span><span class="sxs-lookup"><span data-stu-id="e87cc-223">Enhanced image preview with aspect ratio information</span></span>  

<span data-ttu-id="e87cc-224">Les aperçus d’image dans devTools ont été améliorés pour afficher plus d’informations, notamment les détails suivants.</span><span class="sxs-lookup"><span data-stu-id="e87cc-224">Image previews in the DevTools have been enhanced to display more information, including the following details.</span></span>  

*   <span data-ttu-id="e87cc-225">Taille rendue</span><span class="sxs-lookup"><span data-stu-id="e87cc-225">Rendered size</span></span>  
*   <span data-ttu-id="e87cc-226">Proportions rendues</span><span class="sxs-lookup"><span data-stu-id="e87cc-226">Rendered aspect ratio</span></span>  
*   <span data-ttu-id="e87cc-227">Taille intrinsèque</span><span class="sxs-lookup"><span data-stu-id="e87cc-227">Intrinsic size</span></span>  
*   <span data-ttu-id="e87cc-228">Proportions intrinsèques</span><span class="sxs-lookup"><span data-stu-id="e87cc-228">Intrinsic aspect ratio</span></span>  
*   <span data-ttu-id="e87cc-229">Taille du fichier</span><span class="sxs-lookup"><span data-stu-id="e87cc-229">File size</span></span>  
    
<span data-ttu-id="e87cc-230">Ces informations vous aident à mieux comprendre vos images et à appliquer l’optimisation.</span><span class="sxs-lookup"><span data-stu-id="e87cc-230">The  information helps you better understand your images and apply optimization.</span></span>  <span data-ttu-id="e87cc-231">Les informations sur les proportions d’image sont également disponibles dans l’outil **Réseau,** lorsque vous choisissez un aperçu d’image.</span><span class="sxs-lookup"><span data-stu-id="e87cc-231">The image aspect ratio information is also available in the **Network** tool, when you choose an image preview.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="e87cc-232">Dans **l’outil Éléments,** l’aperçu d’image affiche désormais plus d’informations sur l’image.</span><span class="sxs-lookup"><span data-stu-id="e87cc-232">In the **Elements** tool, image preview now displays more information about the image.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="e87cc-233">En outre, les informations sur les proportions d’image sont disponibles dans l’outil **Réseau,** lorsque vous choisissez un aperçu d’image.</span><span class="sxs-lookup"><span data-stu-id="e87cc-233">Also, the image aspect ratio information is available in the **Network** tool, when you choose an image preview.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/elements-inspect-image-src-hover-preview.msft.png" alt-text="Aperçu d’image avec des informations sur les proportions dans l’outil Element" lightbox="../../media/2021/04/elements-inspect-image-src-hover-preview.msft.png":::
         <span data-ttu-id="e87cc-235">Aperçu d’image avec des informations sur les proportions dans **l’outil Element**</span><span class="sxs-lookup"><span data-stu-id="e87cc-235">Image preview with aspect ratio information in the **Element** tool</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/network-img-name-filters-preview.msft.png" alt-text="Informations sur les proportions d’image dans l’outil Réseau" lightbox="../../media/2021/04/network-img-name-filters-preview.msft.png":::
         <span data-ttu-id="e87cc-237">Informations sur les proportions d’image dans **l’outil** Réseau</span><span class="sxs-lookup"><span data-stu-id="e87cc-237">Image aspect ratio information in the **Network** tool</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="e87cc-238">Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez à Problèmes [1149832][CR1149832] et [1170656][CR1170656].</span><span class="sxs-lookup"><span data-stu-id="e87cc-238">To review the history of this feature in the Chromium open-source project, navigate to Issues [1149832][CR1149832] and [1170656][CR1170656].</span></span>  

### <a name="new-options-to-configure-content-encodings-in-the-network-conditions-tool"></a><span data-ttu-id="e87cc-239">Nouvelles options de configuration des codages de contenu dans l’outil Conditions réseau</span><span class="sxs-lookup"><span data-stu-id="e87cc-239">New options to configure Content-Encodings in the Network conditions tool</span></span> 

<span data-ttu-id="e87cc-240">Dans **l’outil** Réseau, sélectionnez le nouveau \*\*\*\* bouton Plus **de conditions réseau...** en haut du menu déroulant Limitation pour ouvrir l’outil **Conditions réseau.**</span><span class="sxs-lookup"><span data-stu-id="e87cc-240">In the **Network** tool, choose the new **More network conditions...** button next to the **Throttling** dropdown menu to open the **Network conditions** tool.</span></span>  <span data-ttu-id="e87cc-241">Pour tester si les réponses du serveur sont correctement codées pour les navigateurs qui ne peuvent pas prendre en charge [gzip,][GnuSoftwareGzipManual] [brotli][|::ref1::|Main]ou un autre futur, effectuer les `Content-Encoding` actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="e87cc-241">To test if server responses are correctly encoded for browsers that don't support [gzip][GnuSoftwareGzipManual], [brotli][|::ref1::|Main], or another future `Content-Encoding`, complete the following actions.</span></span>  

1.  <span data-ttu-id="e87cc-242">Ouvrir **l’outil Conditions réseau**</span><span class="sxs-lookup"><span data-stu-id="e87cc-242">Open the **Network conditions** tool</span></span>
1.  <span data-ttu-id="e87cc-243">Accédez **à Encodages de contenu acceptés.**</span><span class="sxs-lookup"><span data-stu-id="e87cc-243">Navigate to **Accepted Content-Encodings**.</span></span> 
1.  <span data-ttu-id="e87cc-244">Supprimez la case à cocher en regard `Content-Encoding` de la case à cocher que vous souhaitez tester.</span><span class="sxs-lookup"><span data-stu-id="e87cc-244">Remove the checkbox next to the `Content-Encoding` you want to test.</span></span>  
    
<span data-ttu-id="e87cc-245">Pour passer en revue l’historique de cette fonctionnalité dans Chromium projet open source, accédez à Problème [1162042][CR1162042].</span><span class="sxs-lookup"><span data-stu-id="e87cc-245">To review the history of this feature in the Chromium open-source project, navigate to Issue [1162042][CR1162042].</span></span>  

:::image type="complex" source="../../media/2021/04/network-more-network-conditions-accepted-content-encodings.msft.png" alt-text="Nouvelles conditions réseau... ouvre l’outil Conditions réseau pour configurer l’encodage de contenu" lightbox="../../media/2021/04/network-more-network-conditions-accepted-content-encodings.msft.png":::
   <span data-ttu-id="e87cc-247">Le **bouton Nouvelles conditions réseau...** ouvre l’outil **Conditions** réseau à configurer</span><span class="sxs-lookup"><span data-stu-id="e87cc-247">New **More network conditions...** button opens the **Network conditions** tool to configure</span></span> `Content-Encoding`  
:::image-end:::  

### <a name="styles-pane-enhancements"></a><span data-ttu-id="e87cc-248">Améliorations apportées au volet Styles</span><span class="sxs-lookup"><span data-stu-id="e87cc-248">Styles pane enhancements</span></span>  

#### <a name="new-shortcut-to-display-computed-value-in-the-styles-pane"></a><span data-ttu-id="e87cc-249">Nouveau raccourci pour afficher la valeur calculée dans le volet Styles</span><span class="sxs-lookup"><span data-stu-id="e87cc-249">New shortcut to display computed value in the Styles pane</span></span>  

<span data-ttu-id="e87cc-250">Maintenant, pour afficher la valeur CSS calculée dans le volet **Styles,** effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="e87cc-250">Now, to display the computed CSS value in the **Styles** pane, complete the following actions.</span></span>  

1.  <span data-ttu-id="e87cc-251">Pointez sur une propriété CSS.</span><span class="sxs-lookup"><span data-stu-id="e87cc-251">Hover on a CSS property.</span></span>  
1.  <span data-ttu-id="e87cc-252">Ouvrez le menu contextuel \(cliquez avec le bouton droit\).</span><span class="sxs-lookup"><span data-stu-id="e87cc-252">Open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="e87cc-253">Choose **View computed value**.</span><span class="sxs-lookup"><span data-stu-id="e87cc-253">Choose **View computed value**.</span></span>  
    
<span data-ttu-id="e87cc-254">Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez à Problème [1076198][CR1076198].</span><span class="sxs-lookup"><span data-stu-id="e87cc-254">To review the history of this feature in the Chromium open-source project, navigate to Issue [1076198][CR1076198].</span></span>  

:::image type="complex" source="../../media/2021/04/elements-styles-highlight-view-computed-value.msft.png" alt-text="Nouveau raccourci pour afficher la valeur calculée" lightbox="../../media/2021/04/elements-styles-highlight-view-computed-value.msft.png":::
   <span data-ttu-id="e87cc-256">Nouveau raccourci pour afficher la valeur calculée</span><span class="sxs-lookup"><span data-stu-id="e87cc-256">New shortcut to display computed value</span></span>  
:::image-end:::  

#### <a name="support-for-the-accent-color-keyword"></a><span data-ttu-id="e87cc-257">Prise en charge du mot clé accent-color</span><span class="sxs-lookup"><span data-stu-id="e87cc-257">Support for the accent-color keyword</span></span>  

<span data-ttu-id="e87cc-258">L’interface utilisateur de la mise à jour automatique du volet **Styles** détecte désormais le mot clé CSS, qui vous permet de spécifier la couleur d’accentuence pour les contrôles d’interface utilisateur générés par `accent-color` l’élément.</span><span class="sxs-lookup"><span data-stu-id="e87cc-258">The autocomplete UI of the **Styles** pane now detects the `accent-color` CSS keyword, which allows you to specify the accent color for UI controls generated by the element.</span></span>  <span data-ttu-id="e87cc-259">Les contrôles d’interface utilisateur générés par un élément sont, par exemple, des case à cocher ou des boutons d’radio.</span><span class="sxs-lookup"><span data-stu-id="e87cc-259">Examples of UI controls that are generated by an element include checkboxes or radio buttons.</span></span> <span data-ttu-id="e87cc-260">Pour plus d’informations sur l’état de l Chromium l’implémentation, accédez à Fonctionnalité : propriété CSS de couleur [accentuée.][ChromestatusFeature4752739957473280]</span><span class="sxs-lookup"><span data-stu-id="e87cc-260">For more information about the status of the Chromium implementation, navigate to [Feature: accent-color CSS property][ChromestatusFeature4752739957473280].</span></span>  <span data-ttu-id="e87cc-261">Pour activer cette fonctionnalité, accédez à la case à cocher et définissez-la `edge://flags#enable-experimental-web-platform-features` **sur Activé.**</span><span class="sxs-lookup"><span data-stu-id="e87cc-261">To turn on this feature, navigate to `edge://flags#enable-experimental-web-platform-features` and set the checkbox to **Enabled**.</span></span>  <span data-ttu-id="e87cc-262">Pour passer en revue l’historique de cette fonctionnalité dans le Chromium open source, accédez à Problème [1092093][CR1092093].</span><span class="sxs-lookup"><span data-stu-id="e87cc-262">To review the history of this feature in the Chromium open-source project, navigate to Issue [1092093][CR1092093].</span></span>  

:::image type="complex" source="../../media/2021/04/elements-styles-accent-color.msft.png" alt-text="mot clé CSS de couleur d’accent" lightbox="../../media/2021/04/elements-styles-accent-color.msft.png":::
   `accent-color` <span data-ttu-id="e87cc-264">Mot clé CSS</span><span class="sxs-lookup"><span data-stu-id="e87cc-264">CSS keyword</span></span>
:::image-end:::  

### <a name="display-details-about-blocked-features-in-the-frame-details-view"></a><span data-ttu-id="e87cc-265">Afficher les détails sur les fonctionnalités bloquées dans l’affichage Détails de l’image</span><span class="sxs-lookup"><span data-stu-id="e87cc-265">Display details about blocked features in the Frame details view</span></span>  

<span data-ttu-id="e87cc-266">La stratégie d’autorisations est une API de plateforme web qui permet à un site web d’autoriser ou de bloquer l’utilisation des fonctionnalités de navigateur dans une image individuelle ou dans un site qu’il `iframe` incorpore.</span><span class="sxs-lookup"><span data-stu-id="e87cc-266">Permissions Policy is a web platform API that gives a website the ability to allow or block the use of browser features in an individual frame or in an `iframe` that it embeds.</span></span> <span data-ttu-id="e87cc-267">Pour plus d’informations, [accédez à l’Explication de la stratégie d’autorisations.][GithubW3cWebappsecPermissionsPolicyPermissionsPolicyExplainerMd]</span><span class="sxs-lookup"><span data-stu-id="e87cc-267">For more information, navigate to [Permissions Policy Explainer][GithubW3cWebappsecPermissionsPolicyPermissionsPolicyExplainerMd].</span></span>  <span data-ttu-id="e87cc-268">Pour afficher les détails sur la raison pour laquelle une fonctionnalité est bloquée, effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="e87cc-268">To display the details on why a feature is blocked, complete the following actions.</span></span>  

1.  <span data-ttu-id="e87cc-269">Accédez à [stratégie d’autorisations OOPIF.][GlitchPermissionPolicyDemoMain]</span><span class="sxs-lookup"><span data-stu-id="e87cc-269">Navigate to [OOPIF Permissions Policy][GlitchPermissionPolicyDemoMain].</span></span>  
1.  <span data-ttu-id="e87cc-270">Accédez à **l’outil Application.**</span><span class="sxs-lookup"><span data-stu-id="e87cc-270">Navigate to the **Application** tool.</span></span>  
1.  <span data-ttu-id="e87cc-271">Choisissez un cadre.</span><span class="sxs-lookup"><span data-stu-id="e87cc-271">Choose a frame.</span></span>  
1.  <span data-ttu-id="e87cc-272">Accédez à la section **Stratégie des autorisations.**</span><span class="sxs-lookup"><span data-stu-id="e87cc-272">Navigate to the **Permissions Policy** section.</span></span>  
1.  <span data-ttu-id="e87cc-273">Accédez à la **propriété Fonctionnalités désactivées.**</span><span class="sxs-lookup"><span data-stu-id="e87cc-273">Navigate to the **Disabled Features** property.</span></span>  
1.  <span data-ttu-id="e87cc-274">Choose **Show details**.</span><span class="sxs-lookup"><span data-stu-id="e87cc-274">Choose **Show details**.</span></span>  
1.  <span data-ttu-id="e87cc-275">Sélectionnez l’icône en fonction de chaque stratégie pour accéder à la demande réseau qui `iframe` a bloqué la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="e87cc-275">Choose the icon next to each policy to navigate to the `iframe` or network request that blocked the feature.</span></span>  
    
<span data-ttu-id="e87cc-276">Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez à Problème [1158827][CR1158827].</span><span class="sxs-lookup"><span data-stu-id="e87cc-276">To review the history of this feature in the Chromium open-source project, navigate to Issue [1158827][CR1158827].</span></span>  

:::image type="complex" source="../../media/2021/04/application-frames-top-permission-policy-disabled-features-show-details-highlight.msft.png" alt-text="Fonctionnalités bloquées dans l’affichage Détails de l’image" lightbox="../../media/2021/04/application-frames-top-permission-policy-disabled-features-show-details-highlight.msft.png":::
   <span data-ttu-id="e87cc-278">Fonctionnalités bloquées dans l’affichage Détails de l’image</span><span class="sxs-lookup"><span data-stu-id="e87cc-278">Blocked features in the Frame details view</span></span>  
:::image-end:::  

### <a name="filter-experiments-in-the-experiments-setting"></a><span data-ttu-id="e87cc-279">Filtrer les expériences dans le paramètre Expériences</span><span class="sxs-lookup"><span data-stu-id="e87cc-279">Filter experiments in the Experiments setting</span></span>  

<span data-ttu-id="e87cc-280">Recherchez des expériences plus rapidement avec le nouveau filtre d’expérience.</span><span class="sxs-lookup"><span data-stu-id="e87cc-280">Find experiments quicker with the new experiment filter.</span></span>  <span data-ttu-id="e87cc-281">Par exemple, pour activer de nouvelles expériences pour les problèmes de code, effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="e87cc-281">For example, to turn on new experiments for code issues, complete the following actions.</span></span>
``

1.  <span data-ttu-id="e87cc-282">Accédez **à Paramètres**  >  **expériences.**</span><span class="sxs-lookup"><span data-stu-id="e87cc-282">Navigate to **Settings** > **Experiments**.</span></span>  
1.  <span data-ttu-id="e87cc-283">Accédez à la **boîte de** texte Filtrer.</span><span class="sxs-lookup"><span data-stu-id="e87cc-283">Navigate to the **Filter** textbox.</span></span>  
1.  <span data-ttu-id="e87cc-284">Tapez `issues`.</span><span class="sxs-lookup"><span data-stu-id="e87cc-284">Type `issues`.</span></span>  
    
:::image type="complex" source="../../media/2021/04/settings-experiments-filter-by-issues.msft.png" alt-text="Filtrer les expériences dans le paramètre Expériences" lightbox="../../media/2021/04/settings-experiments-filter-by-issues.msft.png":::
   <span data-ttu-id="e87cc-286">Filtrer les expériences dans le **paramètre Expériences**</span><span class="sxs-lookup"><span data-stu-id="e87cc-286">Filter experiments in the **Experiments** setting</span></span>  
:::image-end:::  

### <a name="new-vary-header-column-in-the-cache-storage-pane"></a><span data-ttu-id="e87cc-287">Nouvelle colonne d’en-tête Vary dans le volet de stockage du cache</span><span class="sxs-lookup"><span data-stu-id="e87cc-287">New Vary Header column in the Cache storage pane</span></span>  

<span data-ttu-id="e87cc-288">Utilisez la nouvelle colonne dans le volet Stockage cache pour afficher les valeurs d’en-tête de réponse `Vary Header` HTTP [Vary.][HttpwgSpecsRfc7231HtmlHeaderVary] \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="e87cc-288">Use the new `Vary Header` column in the **Cache Storage** pane to display the [Vary][HttpwgSpecsRfc7231HtmlHeaderVary] HTTP response header values.</span></span>  <span data-ttu-id="e87cc-289">Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez à Problème [1186049][CR1186049].</span><span class="sxs-lookup"><span data-stu-id="e87cc-289">To review the history of this feature in the Chromium open-source project, navigate to Issue [1186049][CR1186049].</span></span>  

:::image type="complex" source="../../media/2021/04/application-cache-cache-storage-highlighted-vary-header.msft.png" alt-text="Colonne d’en-tête Vary" lightbox="../../media/2021/04/application-cache-cache-storage-highlighted-vary-header.msft.png":::
   <span data-ttu-id="e87cc-291">Colonne d’en-tête Vary</span><span class="sxs-lookup"><span data-stu-id="e87cc-291">Vary Header column</span></span>  
:::image-end:::  

### <a name="sources-tool-improvements"></a><span data-ttu-id="e87cc-292">Améliorations apportées à l’outil Sources</span><span class="sxs-lookup"><span data-stu-id="e87cc-292">Sources tool improvements</span></span>  

#### <a name="support-for-new-javascript-features"></a><span data-ttu-id="e87cc-293">Prise en charge des nouvelles fonctionnalités JavaScript</span><span class="sxs-lookup"><span data-stu-id="e87cc-293">Support for new JavaScript features</span></span>  

<span data-ttu-id="e87cc-294">DevTools désormais prise en charge de la nouvelle marque privée [contrôles a.k.a.][V8DevFeaturesPrivateBrandChecks] #foo en javaScript obj fonctionnalité de langage.</span><span class="sxs-lookup"><span data-stu-id="e87cc-294">DevTools now support the new [Private brand checks a.k.a. #foo in obj][V8DevFeaturesPrivateBrandChecks] JavaScript language feature.</span></span>  <span data-ttu-id="e87cc-295">La fonctionnalité de vérification de marque privée étend [l’opérateur in][MdnDocsWebJavascriptReferenceOperatorsIn] pour prendre en charge [les champs de classe Privé][V8DevFeaturesClassFieldsPrivateClassFields] sur un objet spécifique.</span><span class="sxs-lookup"><span data-stu-id="e87cc-295">The private brand checks feature extends the [in operator][MdnDocsWebJavascriptReferenceOperatorsIn] to support [Private class fields][V8DevFeaturesClassFieldsPrivateClassFields] on a specific object.</span></span>  <span data-ttu-id="e87cc-296">Essayez-le dans les **outils Console** **et Sources.**</span><span class="sxs-lookup"><span data-stu-id="e87cc-296">Try it in the **Console** and **Sources** tools.</span></span>  <span data-ttu-id="e87cc-297">En outre, pour inspecter les champs privés, effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="e87cc-297">Also, to inspect the private fields, complete the following actions.</span></span>  

1.  <span data-ttu-id="e87cc-298">Accédez **au volet débogger.**</span><span class="sxs-lookup"><span data-stu-id="e87cc-298">Navigate to **debugger** pane.</span></span>  
1.  <span data-ttu-id="e87cc-299">Accédez à la section **Étendue.**</span><span class="sxs-lookup"><span data-stu-id="e87cc-299">Navigate to the **Scope** section.</span></span>  
    
<span data-ttu-id="e87cc-300">Pour passer en revue l’historique de cette fonctionnalité dans Chromium projet open source, accédez au problème [11374][CR11374].</span><span class="sxs-lookup"><span data-stu-id="e87cc-300">To review the history of this feature in the Chromium open-source project, navigate to Issue [11374][CR11374].</span></span>  

:::image type="complex" source="../../media/2021/04/sources-page-pen-js-breakpoint-scope-script-dog.msft.png" alt-text="Vérifications de marque privée JavaScript" lightbox="../../media/2021/04/sources-page-pen-js-breakpoint-scope-script-dog.msft.png":::
   <span data-ttu-id="e87cc-302">Vérifications de marque privée JavaScript</span><span class="sxs-lookup"><span data-stu-id="e87cc-302">JavaScript private brand checks</span></span>  
:::image-end:::  

#### <a name="enhanced-support-for-breakpoints-debugging"></a><span data-ttu-id="e87cc-303">Prise en charge améliorée du débogage des points d’arrêt</span><span class="sxs-lookup"><span data-stu-id="e87cc-303">Enhanced support for breakpoints debugging</span></span>  

<span data-ttu-id="e87cc-304">Les bundlers JavaScript modernes tels que [Webpack][WebpackJsMain]et [Rollup][RollupjsMain] prise en charge le fractionnement de code.</span><span class="sxs-lookup"><span data-stu-id="e87cc-304">Modern JavaScript bundlers like [Webpack][WebpackJsMain], and [Rollup][RollupjsMain] support code splitting.</span></span>  <span data-ttu-id="e87cc-305">Pour en savoir plus sur le fractionnement de code, accédez [au fractionnement de code.][JsWebpackGuidesCodeSplittingTextThereAreThreeGeneralApproachesToCodeSplittingSplitCodeViaInlineFunctionCallsWithinModules]</span><span class="sxs-lookup"><span data-stu-id="e87cc-305">To learn more about code splitting, navigate to [Code splitting][JsWebpackGuidesCodeSplittingTextThereAreThreeGeneralApproachesToCodeSplittingSplitCodeViaInlineFunctionCallsWithinModules].</span></span>  <span data-ttu-id="e87cc-306">Dans Microsoft Edge version 90 ou antérieure, DevTools ne définisse les points d’arrêt que dans un seul ensemble.</span><span class="sxs-lookup"><span data-stu-id="e87cc-306">In Microsoft Edge version 90 or earlier, DevTools only set breakpoints in a single bundle.</span></span>  <span data-ttu-id="e87cc-307">Dans Microsoft Edge version 91 ou ultérieure, DevTools définit correctement les points d’arrêt dans plusieurs groupes lorsque vous déboguer un composant partagé.</span><span class="sxs-lookup"><span data-stu-id="e87cc-307">In Microsoft Edge version 91 or later, DevTools properly sets breakpoints in multiple bundles when you debug a shared component.</span></span>  <span data-ttu-id="e87cc-308">Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez à Problèmes [1142705][CR1142705], [979000][CR979000]et [1180794][CR1180794].</span><span class="sxs-lookup"><span data-stu-id="e87cc-308">To review the history of this feature in the Chromium open-source project, navigate to Issues [1142705][CR1142705], [979000][CR979000], and [1180794][CR1180794].</span></span>  

#### <a name="support-hover-preview-with-bracket-notation"></a><span data-ttu-id="e87cc-309">Prise en charge de l’aperçu de pointage avec une notation entre crochets</span><span class="sxs-lookup"><span data-stu-id="e87cc-309">Support hover preview with bracket notation</span></span>  

<span data-ttu-id="e87cc-310">DevTools désormais la prise en charge de l’aperçu de pointage sur les expressions de membre JavaScript qui utilisent la `[]` notation dans **l’outil Sources.**</span><span class="sxs-lookup"><span data-stu-id="e87cc-310">DevTools now support hover preview on JavaScript member expressions that use the `[]` notation in the **Sources** tool.</span></span>  <span data-ttu-id="e87cc-311">Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez à Problème [1178305][CR1178305].</span><span class="sxs-lookup"><span data-stu-id="e87cc-311">To review the history of this feature in the Chromium open-source project, navigate to Issue [1178305][CR1178305].</span></span>  

:::image type="complex" source="../../media/2021/04/sources-page-pen.js-breakpoint-arr-i-a.msft.png" alt-text="Prise en charge de l’aperçu de pointage avec notation []" lightbox="../../media/2021/04/sources-page-pen.js-breakpoint-arr-i-a.msft.png":::
   <span data-ttu-id="e87cc-313">Prise en charge de l’aperçu de pointage avec `[]` notation</span><span class="sxs-lookup"><span data-stu-id="e87cc-313">Support hover preview with `[]` notation</span></span>  
:::image-end:::  

#### <a name="improved-outline-of-html-files"></a><span data-ttu-id="e87cc-314">Amélioration du plan des fichiers HTML</span><span class="sxs-lookup"><span data-stu-id="e87cc-314">Improved outline of HTML files</span></span>  

<span data-ttu-id="e87cc-315">DevTools dispose désormais d’une meilleure prise en charge de plan pour les `.html` fichiers.</span><span class="sxs-lookup"><span data-stu-id="e87cc-315">DevTools now has better outline support for `.html` files.</span></span>  <span data-ttu-id="e87cc-316">Dans **l’outil Sources,** ouvrez le `.html` fichier.</span><span class="sxs-lookup"><span data-stu-id="e87cc-316">In the **Sources** tool, open the `.html` file.</span></span>  <span data-ttu-id="e87cc-317">Pour activer \(ou désactiver\) le plan de code, sélectionnez `Ctrl` + `Shift` + `O` Windows/Linux `Cmd` + `Shift` + `O` ou sur macOS.</span><span class="sxs-lookup"><span data-stu-id="e87cc-317">To turn on \(or off\) the code outline, select `Ctrl`+`Shift`+`O` on Windows/Linux or `Cmd`+`Shift`+`O` on macOS.</span></span>  <span data-ttu-id="e87cc-318">Dans la figure suivante, DevTools liste maintenant correctement toutes les fonctions dans le plan.</span><span class="sxs-lookup"><span data-stu-id="e87cc-318">In the following figure, DevTools now correctly list all functions in the outline.</span></span>  <span data-ttu-id="e87cc-319">Auparavant, DevTools affichait uniquement certaines fonctions.</span><span class="sxs-lookup"><span data-stu-id="e87cc-319">Previously, DevTools only displayed some of the functions.</span></span>  <span data-ttu-id="e87cc-320">Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez à Problèmes [761019][CR761019] et [1191465][CR1191465].</span><span class="sxs-lookup"><span data-stu-id="e87cc-320">To review the history of this feature in the Chromium open-source project, navigate to Issues [761019][CR761019] and [1191465][CR1191465].</span></span>  

:::image type="complex" source="../../media/2021/04/sources-page-jobobbx-at.msft.png" alt-text=" Amélioration du plan des fichiers HTML" lightbox="../../media/2021/04/sources-page-jobobbx-at.msft.png":::
   <span data-ttu-id="e87cc-322">Amélioration du plan des fichiers HTML</span><span class="sxs-lookup"><span data-stu-id="e87cc-322">Improved outline of HTML files</span></span>  
:::image-end:::  

#### <a name="proper-error-stack-traces-for-wasm-debugging"></a><span data-ttu-id="e87cc-323">Traces de pile d’erreurs correctes pour le débogage Wasm</span><span class="sxs-lookup"><span data-stu-id="e87cc-323">Proper error stack traces for Wasm debugging</span></span>  

<span data-ttu-id="e87cc-324">Dans Microsoft Edge version 90 ou antérieure, DevTools affichait uniquement des références Wasm génériques dans les traces de pile d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="e87cc-324">In Microsoft Edge version 90 or earlier, DevTools only displayed generic Wasm references in Error stack traces.</span></span>  <span data-ttu-id="e87cc-325">Dans Microsoft Edge version 91 ou ultérieure, DevTools résout les demandes de fonction en ligne et affiche l’emplacement source dans les traces de pile d’erreurs pour le débogage Wasm.</span><span class="sxs-lookup"><span data-stu-id="e87cc-325">In Microsoft Edge version 91 or later, DevTools resolves inline function requests and displays the source location in Error stack traces for Wasm debugging.</span></span>  <span data-ttu-id="e87cc-326">Pour en savoir plus sur les traces de pile d’erreurs dans la **console,** accédez à [erreur.][DevtoolsConsoleApiError]</span><span class="sxs-lookup"><span data-stu-id="e87cc-326">To learn more about Error stack traces in the **Console**, navigate to [error][DevtoolsConsoleApiError].</span></span>  

<span data-ttu-id="e87cc-327">Dans Microsoft Edge version 91 ou ultérieure, DevTools résout les demandes de fonction en ligne et affiche les traces de pile d’erreurs correctes pour le débogage Wasm.</span><span class="sxs-lookup"><span data-stu-id="e87cc-327">In Microsoft Edge version 91 or later, DevTools resolves inline function requests and displays proper error stack traces for Wasm debugging.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="e87cc-328">Dans Microsoft Edge version 90 et antérieures, l’emplacement source ne s’affiche pas dans les traces de pile d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="e87cc-328">In Microsoft Edge version 90 and earlier, the source location doesn't display in the Error stack traces.</span></span>  <span data-ttu-id="e87cc-329">Les emplacements sources incluent `dsquare` .</span><span class="sxs-lookup"><span data-stu-id="e87cc-329">Source locations include `dsquare`.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="e87cc-330">Dans Microsoft Edge version 91 et ultérieures, l’emplacement source s’affiche dans les traces de pile d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="e87cc-330">In Microsoft Edge version 91 and later, the source location displays in the Error stack traces.</span></span>
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/sources-page-inlining-dwarf-wasm-breakpoint-console-new-error-old.msft.png" alt-text="Traces de pile d’erreurs précédentes pour le débogage Wasm" lightbox="../../media/2021/04/sources-page-inlining-dwarf-wasm-breakpoint-console-new-error-old.msft.png":::
         <span data-ttu-id="e87cc-332">Traces de pile d’erreurs correctes pour le débogage Wasm</span><span class="sxs-lookup"><span data-stu-id="e87cc-332">Proper error stack traces for Wasm debugging</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/sources-page-inlining-dwarf-wasm-breakpoint-console-new-error.msft.png" alt-text="Traces de pile d’erreurs correctes pour le débogage Wasm" lightbox="../../media/2021/04/sources-page-inlining-dwarf-wasm-breakpoint-console-new-error.msft.png":::
         <span data-ttu-id="e87cc-334">Traces de pile d’erreurs correctes pour le débogage Wasm</span><span class="sxs-lookup"><span data-stu-id="e87cc-334">Proper error stack traces for Wasm debugging</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="e87cc-335">Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez à Problème [1189161][CR1189161].</span><span class="sxs-lookup"><span data-stu-id="e87cc-335">To review the history of this feature in the Chromium open-source project, navigate to Issue [1189161][CR1189161].</span></span>  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="e87cc-336">Télécharger les canaux d’aperçu Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e87cc-336">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="e87cc-337">Si vous êtes sous Windows, Linux ou macOS, envisagez d'utiliser les [canaux d'aperçu de Microsoft][MicrosoftEdgePreviewChannels] Edge comme navigateur de développement par défaut.</span><span class="sxs-lookup"><span data-stu-id="e87cc-337">If you are on Windows, Linux, or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="e87cc-338">Les canaux de prévisualisation vous donnent accès aux dernières fonctionnalités de DevTools.</span><span class="sxs-lookup"><span data-stu-id="e87cc-338">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="e87cc-339">Contacter l’équipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="e87cc-339">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsWhatsNew202001DevtoolsUsingDevtoolsInOtherLanguages]: ../../2020/01/devtools.md#using-the-devtools-in-other-languages "Utilisation de DevTools dans d’autres langues : nouveautés de DevTools (Microsoft Edge 81) | Documents Microsoft"  
[DevtoolsWhatsNew202011Devtools]: ../../2020/11/devtools.md "Nouveautés de DevTools (Microsoft Edge 88) | Documents Microsoft"  
[DevtoolsWhatsNew202011DevtoolsCssVariableDefinitionsInStylesPane]: ../../2020/11/devtools.md#css-variable-definitions-in-styles-pane "Définitions de variables CSS dans le volet Styles - Nouveautés de DevTools (Microsoft Edge 88) | Documents Microsoft"  
[DevtoolsWhatsNew202102Devtools]: ../02/devtools.md "Nouveautés de DevTools (Microsoft Edge 90) | Documents Microsoft"  
[DevtoolsWhatsNew202102DevtoolsGroupToolsTogetherInFocusMode]: ../02/devtools.md#group-tools-together-in-focus-mode "Group tools together in Focus Mode - What’s New In DevTools (Microsoft Edge 90) | Documents Microsoft"  

[DevtoolsCommandMenuIndexOpenCommandMenu]: ../../../command-menu/index.md#open-the-command-menu "Ouvrez le menu Commande - Exécutez les commandes avec le menu Microsoft Edge commande DevTools | Documents Microsoft"  
[DevtoolsConsoleApiError]: ../../../console/api.md#error "error - Console API reference | Documents Microsoft"  
[DevtoolsCustomizeLocalization]: ../../../customize/localization.md "Modifier les paramètres de langue de DevTools | Microsoft Docs"  
[DevtoolsIssuesIndex]: ../../../issues/index.md "Recherchez et corrigez les problèmes liés à l’outil des problèmes de Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsServiceWorkerIndex]: ../../../service-workers/index.md "Améliorations apportées aux services | Documents Microsoft"  
[DevtoolsSourcesUsingDebuggerPaneToDebugJavascriptCode]: ../../../sources/index.md#using-the-debugger-pane-to-debug-javascript-code "Utilisation du volet Déboguer le code JavaScript - Sources : vue d’ensemble de l’outil | Documents Microsoft"  

[ProgressiveWebAppsServiceworkerServiceWorkerLifecycle]: ../../../../progressive-web-apps-chromium/serviceworker.md#the-service-worker-lifecycle "Cycle de vie des travailleurs du service : utiliser les travailleurs de service pour gérer les demandes réseau et les notifications Push | Documents Microsoft"  
[ProgressiveWebAppsWebappmanifests]: ../../../../progressive-web-apps-chromium/webappmanifests.md "Utiliser le manifeste d’application web pour intégrer votre application Web progressive au système d’exploitation | Documents Microsoft"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
<!--[GithubMicrosoftVscodeEdgeDevtoolsPullxxx]: https://github.com/microsoft/vscode-edge-devtools/pull/xxx "Pull xxx: Lorem al Ipsum | GitHub"  -->  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canaux de préversion de Microsoft Edge"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Mettre à jour une extension manuellement - Extension Marketplace | Visual Studio Code"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Outils Microsoft Edge pour Visual Studio Code | Visual Studio Marketplace"  
[VisualstudioMarketplaceMsjsdiagDebuggerForEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Débogueur pour Microsoft Edge | Visual Studio Marketplace"  

[BrotliMain]: https://www.brotli.org "Brotli"  

[ChromestatusFeature4752739957473280]: https://chromestatus.com/feature/4752739957473280 "Fonctionnalité : propriété CSS de couleur d’accentu | État de la plateforme Chrome"  

[CsswgDraftsCssUi4WidgetAccent]: https://drafts.csswg.org/css-ui-4/#widget-accent "Couleurs d’accentuage de widget : propriété couleur d’accentuage - Module d’interface utilisateur de base CSS niveau 4 | Brouillons de l’éditeur de groupe de travail CSS"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Bogues Chromium"  
[CR11374]: https://crbug.com/v8/11374 "Problème 11374 : implémenter la vérification de marque d’une marque d’une marque pour les champs privés"  
[CR761019]: https://crbug.com/761019 "Problème 761019 : « Passer au symbole » rate la première fonction et préfère une correspondance pire si elle contient tous les caractères tapés"  
[CR862450]: https://crbug.com/862450 "Problème 862450 : [css-scroll-snap] Envisagez d’ajouter la fonctionnalité Devtools pour l’snap de défilement css"  
[CR979000]: https://crbug.com/979000 "Problème 979000 : les cartes sources avec des chemins d’accès aux sources entrent en conflit ne fonctionnent pas."  
[CR1066604]: https://crbug.com/1066604 "Problème 1066604 : DevTools : voir les détails sur l’installation et l’activation des événements par ServiceWorker | Chromium bogues"  
<!--  [CR1066772]: https://crbug.com/1066772 "Issue 1066772: "  locked  -->  
[CR1076198]: https://crbug.com/1076198 «Problème 1076198: [Feature Request] Jump to computed property from `styles` tab»  
[CR1092093]: «Problème 1092093 : rendre les contrôles de formulaire plus color-stylables en appuyant sur la propriété CSS « accent-color » » https://crbug.com/1092093  
<span data-ttu-id="e87cc-369">[CR1136655] : « Problème https://crbug.com/1136655 1136655 : Devtools : localisation v2 | Chromium bogues »</span><span class="sxs-lookup"><span data-stu-id="e87cc-369">[CR1136655]: https://crbug.com/1136655 "Issue 1136655: Devtools: Localization V2 | Chromium bugs"</span></span>  
[CR1142705]: «Problème 1142705 : les points d’arrêt cessent de fonctionner lorsque 2 sourcesmaps pointent vers le même fichier virtuel lors de l’utilisation de https://crbug.com/1142705 webpack»  
[CR1149832]: «Problème 1149832 : Demande de fonctionnalité : l’aperçu d’image doit également afficher la taille https://crbug.com/1149832 du fichier»  
[CR1158827]: «Problème 1158827 : [Stratégie d’autorisations] Implémenter la prise en charge de devtool pour la stratégie https://crbug.com/1158827 d’autorisations»  
[CR1162042]: «Problème 1162042 : DevTools : prise en charge de la désactivation du codage de contenu https://crbug.com/1162042 gzip/brotli/jxl»  
[CR1166577]: https://crbug.com/1166577 «Problème 1166577 : ☂️ Linear Memory Inspector 1.0»  
[CR1170656]: https://crbug.com/1170656 «Problème 1170656 : afficher les proportions intrinsèques»  
[CR1178305]: «Problème 1178305 : le débogger n’affiche pas la valeur de propriété https://crbug.com/1178305 d’un élément indexé lorsqu’il est survolé»  
<span data-ttu-id="e87cc-377">[CR1180794] : « Problème 1180794 : les points d’arrêt ne fonctionnent pas avec l’optimisation du compilateur de https://crbug.com/1180794 fermeture »</span><span class="sxs-lookup"><span data-stu-id="e87cc-377">[CR1180794]: https://crbug.com/1180794 "Issue 1180794: Breakpoints don't work with Closure Compiler inlining optimization"</span></span>  
[CR1185945]: «Problème 1185945 : l’avertissement de manifeste implique que toutes les icônes doivent être https://crbug.com/1185945 carrées | Chromium bogues »  
<span data-ttu-id="e87cc-379">[CR1186049] : « Problème 1186049 : Colonne pour Vary : en-tête dans la visionneuse Stockage https://crbug.com/1186049 cache »</span><span class="sxs-lookup"><span data-stu-id="e87cc-379">[CR1186049]: https://crbug.com/1186049 "Issue 1186049: Column for Vary: header in Cache Storage viewer"</span></span>  
[CR1187735]: https://crbug.com/1187735 «Problème 1187735 : Accessibilité : MAS2.1.1 : Clavier : Impossible d’appeler la fonction « Var(..) » à l’aide du clavier | Chromium bogues »  
[CR1189161]: https://crbug.com/1189161 «Problème 1189161 : les stacktraces ne sont pas `new Error` transformés via LAXIT»  
[CR1191465]: https://crbug.com/1191465 «Problème 1191465 : Ctrl+Shift+O rompu sur HTML»  

[GithubW3cWebappsecPermissionsPolicyPermissionsPolicyExplainerMd]: https://github.com/w3c/webappsec-permissions-policy/blob/main/permissions-policy-explainer.md "Explication de la stratégie d'autorisation | GitHub"  

[GlitchMemoryInspectorDemoJsHtml]: https://memory-inspector.glitch.me/demo-js.html "Mémoire dans les | JS Glitch"  
[GlitchMemoryInspectorDemoWasmHtml]: https://memory-inspector.glitch.me/demo-wasm.html "Mémoire dans wasm | Glitch"  

[GlitchMicrosoftEdgeChromiumDevtoolsCssDbgStoriesCssScrollSnapHtml]: https://microsoft-edge-chromium-devtools.glitch.me/css-dbg-stories/css-scroll-snap.html "Scroll Ancrer Demo | Glitch"  

[GlitchPermissionPolicyDemoMain]: http://permission-policy-demo.glitch.me "Stratégie d’autorisations OOPIF | Glitch"  

[GnuSoftwareGzipManual]: https://www.gnu.org/software/gzip/manual "gzip : programme de compression de | Système d’exploitation GNU"  

[HttpwgSpecsRfc7231HtmlHeaderVary]: https://httpwg.org/specs/rfc7231.html#header.vary "Vary - Protocole HTTP (Hypertext Transfer Protocol) : sémantique et contenu | Groupe de travail HTTP IETF"  

[JsWebpackGuidesCodeSplittingTextThereAreThreeGeneralApproachesToCodeSplittingSplitCodeViaInlineFunctionCallsWithinModules]: https://webpack.js.org/guides/code-splitting/#:~:text=There%20are%20three%20general%20approaches%20to%20code%20splitting,Split%20code%20via%20inline%20function%20calls%20within%20modules. "Il existe trois approches générales pour le fractionnement de code : points d’entrée : fractionner manuellement le code à l’aide de la configuration d’entrée.  Empêcher la duplication : utilisez des dépendances d’entrée ou SplitChunksPlugin pour dédupliquer et fractionner des blocs.  Importations dynamiques : fractionnement de code via des appels de fonction inline au sein de modules. - Partage de code | webpack"  

[MdnDocsWebCssUsingCssCustomProperties]: https://developer.mozilla.org/docs/Web/CSS/Using_CSS_custom_properties "Utilisation des propriétés personnalisées CSS (variables) | MDN"  

[MdnDocsWebJavascriptReferenceOperatorsIn]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Operators/in "dans l’opérateur | MDN"  

[PwabuilderImagegenerator]: https://www.pwabuilder.com/imageGenerator "Image Generator | PWABuilder"  

[RollupjsMain]: https://rollupjs.org "rollup.js"  

[V8DevFeaturesPrivateBrandChecks]: https://v8.dev/features/private-brand-checks "La marque privée vérifie l’identité #foo dans obj | V8"  
[V8DevFeaturesClassFieldsPrivateClassFields]: https://v8.dev/features/class-fields#private-class-fields "Champs de classe privés : champs de classes publiques et privées | V8"  

[WebpackJsMain]: https://webpack.js.org "webpack"  

> [!NOTE]
> <span data-ttu-id="e87cc-398">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e87cc-398">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e87cc-399">La page d’origine est disponible [ici](https://developer.chrome.com/blog/new-in-devtools-91) et est créée par [Jecelyn Yeen][JecelynYeen] \(Appui au développeur, Chrome DevTools\)</span><span class="sxs-lookup"><span data-stu-id="e87cc-399">The original page is found [here](https://developer.chrome.com/blog/new-in-devtools-91) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="e87cc-401">Ce travail est sous [licence internationale Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e87cc-401">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  
