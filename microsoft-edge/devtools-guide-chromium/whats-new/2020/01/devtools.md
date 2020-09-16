---
description: Affichage 3D, intégration de Visual Studio à Microsoft Edge, et bien plus encore.
title: Nouveautés de DevTools (Microsoft Edge 81)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 3081ebb256a9ede637aaaddc3c3cdf7a70a201bb
ms.sourcegitcommit: b337717957529239434b4e8e1e167aebf0543518
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015474"
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

# <span data-ttu-id="2deb7-104">Nouveautés de DevTools (Microsoft Edge 81)</span><span class="sxs-lookup"><span data-stu-id="2deb7-104">What's New In DevTools (Microsoft Edge 81)</span></span>  

## <span data-ttu-id="2deb7-105">Annonces de l’équipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="2deb7-105">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="2deb7-106">Les sections suivantes répertorient les annonces que vous pouvez avoir manquées de l’équipe Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="2deb7-106">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team!</span></span> <span data-ttu-id="2deb7-107">Découvrez-les pour essayer de nouvelles fonctionnalités dans le DevTools, les extensions de code Visual Studio, etc.</span><span class="sxs-lookup"><span data-stu-id="2deb7-107">Check them out to try new features in the DevTools, Visual Studio Code extensions, and more.</span></span>  <span data-ttu-id="2deb7-108">Pour vous tenir au courant de toutes les fonctionnalités les plus récentes et les plus récentes de vos outils de développement, téléchargez les [canaux Microsoft Edge Preview][MicrosoftEdgePreviewChannels] et [Suivez-nous sur Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="2deb7-108">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <span data-ttu-id="2deb7-109">Améliorations de l’accessibilité dans DevTools</span><span class="sxs-lookup"><span data-stu-id="2deb7-109">Accessibility improvements to the DevTools</span></span>  

<span data-ttu-id="2deb7-110">L’équipe DevTools a 170 contribué aux modifications apportées à Chrome pour répondre aux problèmes de contraste des couleurs, de clavier et de lecteur d’écran à forte incidence dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="2deb7-110">The DevTools team has contributed 170 changes to Chromium to address high-impact color contrast, keyboard, and screen reader issues in the DevTools.</span></span>  <span data-ttu-id="2deb7-111">Tout développeur bâtiment sur le Web doit être en mesure d’utiliser le DevTools.</span><span class="sxs-lookup"><span data-stu-id="2deb7-111">Every developer building the web should be able to use the DevTools.</span></span>  

:::image type="complex" source="../../images/2020/01/a11y-performance-tool.msft.gif" alt-text="Outil performance dans le DevTools avec les améliorations de la navigation au clavier et du lecteur d’écran" lightbox="../../images/2020/01/a11y-performance-tool.msft.gif":::
   <span data-ttu-id="2deb7-113">Outil **performance** dans le devtools avec les améliorations de la navigation au clavier et du lecteur d’écran</span><span class="sxs-lookup"><span data-stu-id="2deb7-113">The **Performance** tool in the DevTools with the keyboard navigation and screen reader improvements</span></span>  
:::image-end:::  

<span data-ttu-id="2deb7-114">Vous voulez savoir comment rendre votre page Web accessible à tous vos utilisateurs?</span><span class="sxs-lookup"><span data-stu-id="2deb7-114">Want to learn how to make your web page accessible to all of your users?</span></span>  <span data-ttu-id="2deb7-115">Téléchargez les informations [d’accessibilité][AccessibilityInsights] et les extensions [Webhint][WebhintBrowserExtension] pour Microsoft Edge pour commencer.</span><span class="sxs-lookup"><span data-stu-id="2deb7-115">Download the [Accessibility Insights][AccessibilityInsights] and [webhint][WebhintBrowserExtension] extensions for Microsoft Edge to get started.</span></span>  

<span data-ttu-id="2deb7-116">Si vous utilisez un lecteur d’écran ou le clavier pour naviguer dans DevTools, envoyez-nous vos commentaires en nous appuyant sur un [Tweet][PostTweetEdgeDevTools] ou en cliquant sur l’icône d' [envoi de commentaires](#getting-in-touch-with-microsoft-edge-devtools-team) .</span><span class="sxs-lookup"><span data-stu-id="2deb7-116">If you use screen readers or the keyboard to navigate around the DevTools, send us your feedback by [tweeting][PostTweetEdgeDevTools] at us or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="2deb7-117">[#963183][CR963183] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="2deb7-117">Chromium issue [#963183][CR963183]</span></span>  

### <span data-ttu-id="2deb7-118">Utiliser le DevTools dans d’autres langues</span><span class="sxs-lookup"><span data-stu-id="2deb7-118">Using the DevTools in other languages</span></span>  

<span data-ttu-id="2deb7-119">De nombreux développeurs utilisent d’autres outils de développement tels que StackOverflow et Visual Studio, dans leur langue maternelle, et non uniquement en anglais.</span><span class="sxs-lookup"><span data-stu-id="2deb7-119">Many developers use other developer tools, like StackOverflow and Visual Studio Code, in their native language, not just in English.</span></span>  <span data-ttu-id="2deb7-120">Nous sommes heureux d’annoncer la localisation de DevTools, que vous pouvez désormais utiliser dans l’un des 10 langues autres que l’anglais:</span><span class="sxs-lookup"><span data-stu-id="2deb7-120">We’re excited to announce localization for the DevTools, which you are now able to use in one of 10 languages besides English:</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="2deb7-121">Chinois (simplifié)- &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span><span class="sxs-lookup"><span data-stu-id="2deb7-121">Chinese \(Simplified\) - &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="2deb7-122">Chinois (traditionnel)- &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span><span class="sxs-lookup"><span data-stu-id="2deb7-122">Chinese \(Traditional\) - &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="2deb7-123">Français-Fran&#231;AIS</span><span class="sxs-lookup"><span data-stu-id="2deb7-123">French – fran&#231;ais</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="2deb7-124">Allemand-Deutsch</span><span class="sxs-lookup"><span data-stu-id="2deb7-124">German - deutsch</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="2deb7-125">Italien-Italiano</span><span class="sxs-lookup"><span data-stu-id="2deb7-125">Italian - italiano</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="2deb7-126">Japonais- &#26085;&#26412;&#35486;</span><span class="sxs-lookup"><span data-stu-id="2deb7-126">Japanese - &#26085;&#26412;&#35486;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="2deb7-127">Coréen- &#54620;&#44397;&#50612;</span><span class="sxs-lookup"><span data-stu-id="2deb7-127">Korean - &#54620;&#44397;&#50612;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="2deb7-128">Portugais-portugu&#234;s</span><span class="sxs-lookup"><span data-stu-id="2deb7-128">Portuguese - portugu&#234;s</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="2deb7-129">Russe- &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span><span class="sxs-lookup"><span data-stu-id="2deb7-129">Russian – &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="2deb7-130">Espagnol-ESPA&#241;ol</span><span class="sxs-lookup"><span data-stu-id="2deb7-130">Spanish - espa&#241;ol</span></span>
   :::column-end:::
:::row-end:::

<!--  
|  |  |  
|:--- |:--- |  
| Chinese (Simplified) - 中文(简体)（简体）| Chinese (Traditional) - 中文(繁體)（繁體）|  
| French – français | German - deutsch |  
| Italian - italiano | Portuguese - português |  
| Korean - 한국어 | Japanese - 日本語 |  
| Russian – русский | Spanish - español |  
-->  

<span data-ttu-id="2deb7-131">Le DevTools correspond automatiquement à la langue que vous utilisez pour Microsoft Edge dans `edge://settings/languages` .</span><span class="sxs-lookup"><span data-stu-id="2deb7-131">The DevTools automatically match the language you use for Microsoft Edge in `edge://settings/languages`.</span></span>  

<span data-ttu-id="2deb7-132">Si vous voulez que Microsoft Edge soit dans une langue et que votre DevTools reste en anglais, appuyez sur `F1` la devtools pour ouvrir les [paramètres][Settings] et désactiver respecter la **langue du navigateur**.</span><span class="sxs-lookup"><span data-stu-id="2deb7-132">If you want Microsoft Edge to be in one language and your DevTools to remain in English, press `F1` in the DevTools to open [Settings][Settings] and disable **Match browser language**.</span></span>  

:::image type="complex" source="../../images/2020/01/localized-devtools.msft.png" alt-text="DevTools en allemand" lightbox="../../images/2020/01/localized-devtools.msft.png":::
   <span data-ttu-id="2deb7-134">DevTools en allemand</span><span class="sxs-lookup"><span data-stu-id="2deb7-134">The DevTools in German</span></span>  
:::image-end:::  

<span data-ttu-id="2deb7-135">Les messages de **console** ne sont pas localisés.</span><span class="sxs-lookup"><span data-stu-id="2deb7-135">**Console** messages are not localized.</span></span>  <span data-ttu-id="2deb7-136">Seules les chaînes utilisées dans l’interface utilisateur DevTools sont affichées dans la langue que vous utilisez pour Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2deb7-136">Only the strings used in the DevTools UI are displayed in the language you use for Microsoft Edge.</span></span>  

<span data-ttu-id="2deb7-137">Si vous souhaitez utiliser le DevTools dans une autre langue que celle proposée, vous pouvez utiliser le [Tweet][PostTweetEdgeDevTools] ou cliquez sur l’icône d' [envoi de commentaires](#getting-in-touch-with-microsoft-edge-devtools-team) .</span><span class="sxs-lookup"><span data-stu-id="2deb7-137">If you want to use the DevTools in a different language than the ones that are available, [tweet][PostTweetEdgeDevTools] at us or click the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon.</span></span>  

<span data-ttu-id="2deb7-138">[#941561][CR941561] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="2deb7-138">Chromium issue [#941561][CR941561]</span></span>  

### <span data-ttu-id="2deb7-139">extension Microsoft Edge de webhint</span><span class="sxs-lookup"><span data-stu-id="2deb7-139">webhint Microsoft Edge extension</span></span>  

<span data-ttu-id="2deb7-140">L’extension Microsoft Edge de Microsoft vous permet d’analyser facilement votre page Web et de faire des commentaires sur l’accessibilité, la compatibilité avec les navigateurs, la sécurité et les performances, etc., dans le DevTools.</span><span class="sxs-lookup"><span data-stu-id="2deb7-140">The webhint Microsoft Edge extension allows you to easily scan your web page and get feedback on accessibility, browser compatibility, security, performance, and more within the DevTools.</span></span>  <span data-ttu-id="2deb7-141">Pour en savoir plus [https://webhint.io][Webhint] , voir.</span><span class="sxs-lookup"><span data-stu-id="2deb7-141">Read more at [https://webhint.io][Webhint].</span></span>  

:::image type="complex" source="../../images/2020/01/webhint-browser-extension.msft.png" alt-text="Onglet Hints dans le DevTools lorsque l’extension de navigateur webhint est installée" lightbox="../../images/2020/01/webhint-browser-extension.msft.png":::
   <span data-ttu-id="2deb7-143">Onglet **Hints** dans le devtools lorsque l’extension de navigateur webhint est installée</span><span class="sxs-lookup"><span data-stu-id="2deb7-143">The **Hints** tab in the DevTools when the webhint browser extension is installed</span></span>  
:::image-end:::  

<span data-ttu-id="2deb7-144">[Essayez l’extension de navigateur webhint dans Microsoft Edge][MicrosoftEdgeInsiderAddons].</span><span class="sxs-lookup"><span data-stu-id="2deb7-144">[Try the webhint browser extension in Microsoft Edge][MicrosoftEdgeInsiderAddons].</span></span>  <span data-ttu-id="2deb7-145">Une fois l’extension installée, ouvrez le DevTools et sélectionnez l’onglet conseils.  À partir de là, effectuez une analyse de site personnalisable.</span><span class="sxs-lookup"><span data-stu-id="2deb7-145">Once you install the extension, open the DevTools and select the Hints tab.  From here, run a customizable site scan.</span></span>  <span data-ttu-id="2deb7-146">Accédez à [webhint.IO][WebhintBrowserExtension] pour en savoir plus.</span><span class="sxs-lookup"><span data-stu-id="2deb7-146">Head over to [webhint.io][WebhintBrowserExtension] to learn more.</span></span>  

### <span data-ttu-id="2deb7-147">Vue 3D</span><span class="sxs-lookup"><span data-stu-id="2deb7-147">3D View</span></span>  

<span data-ttu-id="2deb7-148">Utilisez la **vue 3D** pour déboguer votre application Web en naviguant dans le [modèle d’objet de document \ (DOM \)][MDNDocumentObjectModel] ou le contexte de pile [de l’index z][MDNZIndex] .</span><span class="sxs-lookup"><span data-stu-id="2deb7-148">Use the **3D View** to debug your web application by navigating through the [Document Object Model \(DOM\)][MDNDocumentObjectModel] or the [z-index][MDNZIndex] stacking context.</span></span>  

:::image type="complex" source="../../images/2020/01/3dview.msft.png" alt-text="Affichage 3D dans le DevTools" lightbox="../../images/2020/01/3dview.msft.png":::
   <span data-ttu-id="2deb7-150">Affichage 3D dans le DevTools</span><span class="sxs-lookup"><span data-stu-id="2deb7-150">The 3D View in the DevTools</span></span>  
:::image-end:::  

<span data-ttu-id="2deb7-151">Pour accéder à l’affichage 3D, appuyez sur la touche `Ctrl`  +  `Shift`  +  `P` **affichage** 3D et sélectionnez **afficher la vue 3D**.</span><span class="sxs-lookup"><span data-stu-id="2deb7-151">To access the 3D View, press `Ctrl` + `Shift` + `P`, type in **3D View** and select **Show 3D View**.</span></span>  

<span data-ttu-id="2deb7-152">Nous travaillons sur l’interface utilisateur et nous ajoutons d’autres fonctionnalités à l’affichage 3D; nous vous envoyons donc votre [avis](#getting-in-touch-with-microsoft-edge-devtools-team).</span><span class="sxs-lookup"><span data-stu-id="2deb7-152">We're working on the UI and adding more functionality to the 3D View, so please send us your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team).</span></span>  

<span data-ttu-id="2deb7-153">[#987787][CR987787] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="2deb7-153">Chromium issue [#987787][CR987787]</span></span>  

### <span data-ttu-id="2deb7-154">Extensions de code Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2deb7-154">Visual Studio Code extensions</span></span>  

<span data-ttu-id="2deb7-155">L’équipe DevTools a également émis quelques extensions pour le [code Visual Studio][VisualStudioCode] qui vous permettent d’utiliser la puissance de devtools directement à partir de votre éditeur de texte.</span><span class="sxs-lookup"><span data-stu-id="2deb7-155">The DevTools team has also released some extensions for [Visual Studio Code][VisualStudioCode] that let you use the power of the DevTools directly from your text editor!</span></span> <span data-ttu-id="2deb7-156">Consultez les extensions suivantes:</span><span class="sxs-lookup"><span data-stu-id="2deb7-156">Check out the extensions below:</span></span>  

#### <span data-ttu-id="2deb7-157">Éléments pour Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2deb7-157">Elements for Microsoft Edge</span></span>  

<span data-ttu-id="2deb7-158">Pour ce faire, utilisez l’outil éléments dans le code Visual Studio en ajoutant les éléments pour l’extension de code Visual Studio [Microsoft Edge \ (chrome \)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] .</span><span class="sxs-lookup"><span data-stu-id="2deb7-158">Use the Elements tool from within Visual Studio Code by adding the [Elements for Microsoft Edge \(Chromium\)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] Visual Studio Code extension.</span></span>  

:::image type="complex" source="../../images/2020/01/elements-for-edge.msft.png" alt-text="Outil éléments dans le code Visual Studio utilisant les éléments de l’extension Microsoft Edge" lightbox="../../images/2020/01/elements-for-edge.msft.png":::
   <span data-ttu-id="2deb7-160">Outil **éléments** dans le code Visual Studio utilisant les éléments de l’extension Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2deb7-160">The **Elements** tool in Visual Studio Code using the Elements for Microsoft Edge extension</span></span>  
:::image-end:::  

<span data-ttu-id="2deb7-161">Pour plus d’informations, consultez les [éléments pour l’extension de code Visual Studio Visual Studio][VisualStudioCodeElementEdgeExtension].</span><span class="sxs-lookup"><span data-stu-id="2deb7-161">For more information, check out [Elements for Microsoft Edge Visual Studio Code extension][VisualStudioCodeElementEdgeExtension].</span></span>  

#### <span data-ttu-id="2deb7-162">Débogueur pour Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2deb7-162">Debugger for Microsoft Edge</span></span>  

<span data-ttu-id="2deb7-163">Avec le [débogueur pour][VisualStudioMarketplaceDebuggerEdge] l’extension de code Visual Studio Visual Studio, déboguez JavaScript en cours d’exécution dans Microsoft Edge directement à partir de code Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="2deb7-163">With the [Debugger for Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] Visual Studio Code extension, debug JavaScript running in Microsoft Edge directly from Visual Studio Code.</span></span>  

:::image type="complex" source="../../images/2020/01/vscode-debugger.msft.png" alt-text="Le débogueur pour l’extension Microsoft Edge dans le code Visual Studio" lightbox="../../images/2020/01/vscode-debugger.msft.png":::
   <span data-ttu-id="2deb7-165">Le débogueur pour l’extension Microsoft Edge dans le code Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2deb7-165">The Debugger for Microsoft Edge Extension in Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="2deb7-166">Pour plus d’informations, voir [Comment déboguer Microsoft Edge à partir de code Visual Studio][VisualStudioCodeDebuggerEdgeExtension].</span><span class="sxs-lookup"><span data-stu-id="2deb7-166">For more information, check out [how to debug Microsoft Edge from Visual Studio Code][VisualStudioCodeDebuggerEdgeExtension].</span></span>  

#### <span data-ttu-id="2deb7-167">webhint</span><span class="sxs-lookup"><span data-stu-id="2deb7-167">webhint</span></span>  

<span data-ttu-id="2deb7-168">L’extension de code [webhint][VisualStudioMarketplaceWebhintExtension] Visual Studio utilise `webhint` pour améliorer votre page Web pendant que vous rédigez un message.</span><span class="sxs-lookup"><span data-stu-id="2deb7-168">The [webhint][VisualStudioMarketplaceWebhintExtension] Visual Studio Code extension uses `webhint` to improve your web page while you're writing it!</span></span> <span data-ttu-id="2deb7-169">Cette extension exécute et signale les diagnostics de vos fichiers d’espace de travail en fonction de l' `webhint` analyse.</span><span class="sxs-lookup"><span data-stu-id="2deb7-169">This extension runs and reports diagnostics on your workspace files based on `webhint` analysis.</span></span>  

:::image type="complex" source="../../images/2020/01/webhint-vscode-extension.msft.png" alt-text="Extension de code Visual Studio webhint qui analyse un fichier. TSX dans le code Visual Studio" lightbox="../../images/2020/01/webhint-vscode-extension.msft.png":::
   <span data-ttu-id="2deb7-171">Extension de code Visual Studio webhint qui analyse un `.tsx` fichier dans le code Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2deb7-171">The webhint Visual Studio Code extension analyzing a `.tsx` file in Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="2deb7-172">[En savoir plus sur l’extension Visual Studio code webhint][WebhintVisualStudioCodeExtension].</span><span class="sxs-lookup"><span data-stu-id="2deb7-172">[Learn more about the Visual Studio Code webhint extension][WebhintVisualStudioCodeExtension].</span></span>  

### <span data-ttu-id="2deb7-173">Intégration de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2deb7-173">Visual Studio integration</span></span>  

<span data-ttu-id="2deb7-174">Dans Visual Studio 2019 version 16,2 ou ultérieure, utilisez le débogueur Visual Studio pour déboguer JavaScript en cours d’exécution dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2deb7-174">In Visual Studio 2019 version 16.2 or later, use the Visual Studio debugger to debug JavaScript running in Microsoft Edge.</span></span>  <span data-ttu-id="2deb7-175">[Téléchargez Visual Studio 2019][MicrosoftVisualStudioDownloads] pour essayer cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="2deb7-175">[Download Visual Studio 2019][MicrosoftVisualStudioDownloads] to try this feature out!</span></span>  

:::image type="complex" source="../../images/2020/01/vs.msft.png" alt-text="Visual Studio avec l’option de lancement de votre application Web dans Microsoft Edge Canaries, dev ou Beta" lightbox="../../images/2020/01/vs.msft.png":::
   <span data-ttu-id="2deb7-177">Visual Studio avec l’option de lancement de votre application Web dans Microsoft Edge Canaries, dev ou Beta</span><span class="sxs-lookup"><span data-stu-id="2deb7-177">Visual Studio with the option to launch your web app in Microsoft Edge Canary, Dev, or Beta</span></span>  
:::image-end:::  

<span data-ttu-id="2deb7-178">[Apprenez-en davantage sur le débogage de Microsoft Edge à partir de Visual Studio][MicrosoftVisualStudio].</span><span class="sxs-lookup"><span data-stu-id="2deb7-178">[Learn more about debugging Microsoft Edge from Visual Studio][MicrosoftVisualStudio].</span></span>  

### <span data-ttu-id="2deb7-179">Suivi des messages de la console de prévention</span><span class="sxs-lookup"><span data-stu-id="2deb7-179">Tracking prevention Console messages</span></span>  

<span data-ttu-id="2deb7-180">La prévention de suivi est une fonctionnalité unique de Microsoft Edge qui vous protège du suivi par des sites Web que vous n’avez pas encore visités.</span><span class="sxs-lookup"><span data-stu-id="2deb7-180">Tracking prevention is a unique feature in Microsoft Edge that protects you from being tracked by websites you haven't visited before.</span></span>  <span data-ttu-id="2deb7-181">Le paramètre de prévention du suivi par défaut est le mode équilibré, qui permet de bloquer des suivis tiers et des pistes malveillantes connues pour une interface qui équilibre la confidentialité et la compatibilité Web.</span><span class="sxs-lookup"><span data-stu-id="2deb7-181">The default tracking prevention setting is Balanced mode, which blocks 3rd party trackers and known malicious trackers for an experience that balances privacy and web compatibility.</span></span>  <span data-ttu-id="2deb7-182">Pour plus d’informations sur la compatibilité de votre page Web lorsque certains suivis sont bloqués, nous avons également ajouté des messages d’avertissement dans la console lorsqu’un suivi est bloqué.</span><span class="sxs-lookup"><span data-stu-id="2deb7-182">To give you more insight into the compatibility of your web page when certain trackers are blocked, we've also added warning messages in the Console when a tracker is blocked.</span></span>  

:::image type="complex" source="../../images/2020/01/tracking-prevention.msft.png" alt-text="Messages dans la console lors du suivi de la prévention bloquer l’accès au stockage pour un suivi" lightbox="../../images/2020/01/tracking-prevention.msft.png":::
   <span data-ttu-id="2deb7-184">Messages dans la console lors du suivi de la prévention bloquer l’accès au stockage pour un suivi</span><span class="sxs-lookup"><span data-stu-id="2deb7-184">Messages in the Console when tracking prevention blocks access to storage for a tracker</span></span>  
:::image-end:::  

<span data-ttu-id="2deb7-185">[En savoir plus sur la prévention de suivi et le compromis entre la confidentialité et la compatibilité Web][TrackingPrevention].</span><span class="sxs-lookup"><span data-stu-id="2deb7-185">[Read more about tracking prevention and the balance between privacy and web compatibility][TrackingPrevention].</span></span>  

## <span data-ttu-id="2deb7-186">Annonces du projet de chrome</span><span class="sxs-lookup"><span data-stu-id="2deb7-186">Announcements from the Chromium project</span></span>  

<span data-ttu-id="2deb7-187">Les sections suivantes annoncent des fonctionnalités supplémentaires disponibles dans Microsoft Edge 81 qui ont été fournies au projet de chrome Open source.</span><span class="sxs-lookup"><span data-stu-id="2deb7-187">The following sections announce additional features available in Microsoft Edge 81 that were contributed to the open source Chromium project.</span></span>  

### <span data-ttu-id="2deb7-188">Prise en charge de moto G4 en mode appareil</span><span class="sxs-lookup"><span data-stu-id="2deb7-188">Moto G4 support in Device Mode</span></span>  

<span data-ttu-id="2deb7-189">Après l' [activation de la barre d’outils de l’appareil][DeviceToolbar], simulez les dimensions d’une fenêtre d’affichage moto G4 de la liste des **appareils** .</span><span class="sxs-lookup"><span data-stu-id="2deb7-189">After [enabling the Device Toolbar][DeviceToolbar], simulate the dimensions of a Moto G4 viewport from the **Device** list.</span></span>  

:::image type="complex" source="../../images/2020/01/motog4.msft.png" alt-text="Simulation d’une fenêtre d’affichage moto G4" lightbox="../../images/2020/01/motog4.msft.png":::
   <span data-ttu-id="2deb7-191">Simulation d’une fenêtre d’affichage moto G4</span><span class="sxs-lookup"><span data-stu-id="2deb7-191">Simulating a Moto G4 viewport</span></span>  
:::image-end:::  

<span data-ttu-id="2deb7-192">Cliquez sur [afficher le cadre][DeviceFrame] de l’appareil pour afficher le matériel moto G4 dans la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="2deb7-192">Click [Show Device Frame][DeviceFrame] to show the Moto G4 hardware around the viewport.</span></span>  

:::image type="complex" source="../../images/2020/01/motog4frame.msft.png" alt-text="Affichage du matériel moto G4" lightbox="../../images/2020/01/motog4frame.msft.png":::
   <span data-ttu-id="2deb7-194">Affichage du matériel moto G4</span><span class="sxs-lookup"><span data-stu-id="2deb7-194">Showing the Moto G4 hardware</span></span>  
:::image-end:::  

<span data-ttu-id="2deb7-195">Fonctionnalités connexes:</span><span class="sxs-lookup"><span data-stu-id="2deb7-195">Related features:</span></span>  

*   <span data-ttu-id="2deb7-196">Ouvrez le [menu de commandes][CommandMenu] et exécutez la `Capture screenshot` commande pour effectuer une capture d’écran de la fenêtre d’affichage qui inclut le matériel moto G4 (après avoir activé l’option **afficher le cadre**de l’appareil).</span><span class="sxs-lookup"><span data-stu-id="2deb7-196">Open the [Command Menu][CommandMenu] and run the `Capture screenshot` command to take a screenshot of the viewport that includes the Moto G4 hardware (after enabling **Show Device Frame**).</span></span>  
*   <span data-ttu-id="2deb7-197">[Limitez le réseau et le processeur][ThrottleNetworkAndCpu] pour simuler plus précisément les conditions de navigation sur le Web des utilisateurs mobiles.</span><span class="sxs-lookup"><span data-stu-id="2deb7-197">[Throttle the network and CPU][ThrottleNetworkAndCpu] to more accurately simulate a mobile user's web browsing conditions.</span></span>  

<span data-ttu-id="2deb7-198">[#924693][CR924693] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="2deb7-198">Chromium issue [#924693][CR924693]</span></span>  

### <span data-ttu-id="2deb7-199">Mises à jour associées au cookie;</span><span class="sxs-lookup"><span data-stu-id="2deb7-199">Cookie-related updates</span></span>  

#### <span data-ttu-id="2deb7-200">Cookies bloqués dans le volet cookies</span><span class="sxs-lookup"><span data-stu-id="2deb7-200">Blocked cookies in the Cookies pane</span></span>  

<span data-ttu-id="2deb7-201">Le volet cookies du panneau application affiche désormais les cookies bloqués avec un arrière-plan jaune.</span><span class="sxs-lookup"><span data-stu-id="2deb7-201">The Cookies pane in the Application panel now displays blocked cookies with a yellow background.</span></span>  

:::image type="complex" source="../../images/2020/01/blockedcookies.msft.png" alt-text="Cookies bloqués dans le volet cookies du panneau application" lightbox="../../images/2020/01/blockedcookies.msft.png":::
   <span data-ttu-id="2deb7-203">Cookies bloqués dans le volet cookies du panneau application</span><span class="sxs-lookup"><span data-stu-id="2deb7-203">Blocked cookies in the Cookies pane of the Application panel</span></span>  
:::image-end:::  

<span data-ttu-id="2deb7-204">[#1030258][CR1030258] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="2deb7-204">Chromium issue [#1030258][CR1030258]</span></span>  <!-- inaccessible  -->  

#### <span data-ttu-id="2deb7-205">Priorité de cookie dans le volet cookie</span><span class="sxs-lookup"><span data-stu-id="2deb7-205">Cookie priority in the Cookie pane</span></span>  

<span data-ttu-id="2deb7-206">Les tables cookies dans les panneaux réseau et application incluent désormais une colonne de **priorité** .</span><span class="sxs-lookup"><span data-stu-id="2deb7-206">The Cookies tables in the Network and Application panels now include a **Priority** column.</span></span>  

> [!CAUTION]
> <span data-ttu-id="2deb7-207">Les navigateurs de type chrome, tels que Microsoft Edge, sont les seuls navigateurs qui prennent en charge la priorité des cookies.</span><span class="sxs-lookup"><span data-stu-id="2deb7-207">Chromium-based browsers, like Microsoft Edge, are the only browsers that support cookie priority.</span></span>  

<span data-ttu-id="2deb7-208">[#1026879][CR1026879] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="2deb7-208">Chromium issue [#1026879][CR1026879]</span></span>  

#### <span data-ttu-id="2deb7-209">Modifier toutes les valeurs de cookie</span><span class="sxs-lookup"><span data-stu-id="2deb7-209">Edit all cookie values</span></span>  

<span data-ttu-id="2deb7-210">Toutes les cellules des tables cookie sont modifiables, à l’exception des cellules de la colonne **taille** , car cette colonne représente la taille du réseau du cookie, en octets.</span><span class="sxs-lookup"><span data-stu-id="2deb7-210">All cells in the Cookie tables are editable now, except cells in the **Size** column because that column represents the network size of the cookie, in bytes.</span></span>  <span data-ttu-id="2deb7-211">Pour obtenir une description de chaque colonne, voir [champs][CookiesFields] .</span><span class="sxs-lookup"><span data-stu-id="2deb7-211">See [Fields][CookiesFields] for an explanation of each column.</span></span>  

:::image type="complex" source="../../images/2020/01/editcookie.msft.png" alt-text="Modification d’une valeur de cookie" lightbox="../../images/2020/01/editcookie.msft.png":::
   <span data-ttu-id="2deb7-213">Modification d’une valeur de cookie</span><span class="sxs-lookup"><span data-stu-id="2deb7-213">Editing a cookie value</span></span>  
:::image-end:::  

#### <span data-ttu-id="2deb7-214">Copy As Node.js FETCH pour inclure des données de cookie</span><span class="sxs-lookup"><span data-stu-id="2deb7-214">Copy as Node.js fetch to include cookie data</span></span>  

<span data-ttu-id="2deb7-215">Cliquez avec le bouton droit sur une demande réseau et sélectionnez **copier**la  >  **copie sous Node.js récupérer** pour obtenir une `fetch` expression incluant des données de cookie.</span><span class="sxs-lookup"><span data-stu-id="2deb7-215">Right-click a network request and select **Copy** > **Copy as Node.js fetch** to get a `fetch` expression that includes cookie data.</span></span>  

:::image type="complex" source="../../images/2020/01/fetchcookies.msft.png" alt-text="Copy As Node.js Fetch" lightbox="../../images/2020/01/fetchcookies.msft.png":::
   <span data-ttu-id="2deb7-217">Copy As Node.js Fetch</span><span class="sxs-lookup"><span data-stu-id="2deb7-217">Copy as Node.js fetch</span></span>  
:::image-end:::  

<span data-ttu-id="2deb7-218">[#1029826][CR1029826] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="2deb7-218">Chromium issue [#1029826][CR1029826]</span></span>  

### <span data-ttu-id="2deb7-219">Icônes de manifeste d’application Web plus précises</span><span class="sxs-lookup"><span data-stu-id="2deb7-219">More accurate web app manifest icons</span></span>  

<span data-ttu-id="2deb7-220">Auparavant, le volet manifeste du panneau d’application a envoyé ses propres demandes pour afficher les icônes du manifeste de l’application Web.</span><span class="sxs-lookup"><span data-stu-id="2deb7-220">Previously, the Manifest pane in the Application panel sent its own requests in order to display web app manifest icons.</span></span>  <span data-ttu-id="2deb7-221">DevTools affiche maintenant la même icône de manifeste que celle utilisée par Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2deb7-221">DevTools now shows the exact same manifest icon that Microsoft Edge uses.</span></span>  

:::image type="complex" source="../../images/2020/01/manifesticons.msft.png" alt-text="Icônes du volet manifeste" lightbox="../../images/2020/01/manifesticons.msft.png":::
   <span data-ttu-id="2deb7-223">Icônes du volet manifeste</span><span class="sxs-lookup"><span data-stu-id="2deb7-223">Icons in the Manifest pane</span></span>  
:::image-end:::  

<span data-ttu-id="2deb7-224">[#985402][CR985402] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="2deb7-224">Chromium issue [#985402][CR985402]</span></span>  

### <span data-ttu-id="2deb7-225">Survol des propriétés de contenu CSS pour afficher les valeurs sans échappement</span><span class="sxs-lookup"><span data-stu-id="2deb7-225">Hover over CSS content properties to see unescaped values</span></span>  

<span data-ttu-id="2deb7-226">Placez le pointeur de la souris sur la valeur d’une `content` propriété pour afficher la version sans échappement de la valeur.</span><span class="sxs-lookup"><span data-stu-id="2deb7-226">Hover over the value of a `content` property to see the unescaped version of the value.</span></span>  

<span data-ttu-id="2deb7-227">Par exemple, dans cette [démonstration][CSSContentDemo] , lorsque vous examinez le `p::after` Pseudo-élément, vous voyez une chaîne d’échappement dans le volet styles:</span><span class="sxs-lookup"><span data-stu-id="2deb7-227">For example, in this [demo][CSSContentDemo] when you inspect the `p::after` pseudo-element you see an escaped string in the Styles pane:</span></span>  

:::image type="complex" source="../../images/2020/01/escapedstring.msft.png" alt-text="Chaîne d’échappement" lightbox="../../images/2020/01/escapedstring.msft.png":::
   <span data-ttu-id="2deb7-229">Chaîne d’échappement</span><span class="sxs-lookup"><span data-stu-id="2deb7-229">The escaped string</span></span>  
:::image-end:::  

<span data-ttu-id="2deb7-230">Lorsque vous pointez sur la `content` valeur, vous voyez la valeur sans séquence d’échappement:</span><span class="sxs-lookup"><span data-stu-id="2deb7-230">When you hover over the `content` value you see the unescaped value:</span></span>  

:::image type="complex" source="../../images/2020/01/unescapedstring.msft.png" alt-text="Valeur sans échappement" lightbox="../../images/2020/01/unescapedstring.msft.png":::
   <span data-ttu-id="2deb7-232">Valeur sans échappement</span><span class="sxs-lookup"><span data-stu-id="2deb7-232">The unescaped value</span></span>  
:::image-end:::  

### <span data-ttu-id="2deb7-233">Erreurs de carte source plus détaillées dans la console</span><span class="sxs-lookup"><span data-stu-id="2deb7-233">More detailed source map errors in the Console</span></span>  

<span data-ttu-id="2deb7-234">La console donne désormais plus de détails sur la raison pour laquelle une table source n’a pas pu être chargée ou analysée.</span><span class="sxs-lookup"><span data-stu-id="2deb7-234">The Console now provides more detail on why a source map failed to load or parse.</span></span>  <span data-ttu-id="2deb7-235">Auparavant, il vous suffit de fournir une erreur sans expliquer ce qui s’est passé.</span><span class="sxs-lookup"><span data-stu-id="2deb7-235">Previously it just provided an error without explaining what went wrong.</span></span>  

:::image type="complex" source="../../images/2020/01/sourcemap.msft.png" alt-text="Erreur de chargement du mappage source dans la console" lightbox="../../images/2020/01/sourcemap.msft.png":::
   <span data-ttu-id="2deb7-237">Erreur de chargement du mappage source dans la console</span><span class="sxs-lookup"><span data-stu-id="2deb7-237">A source map loading error in the Console</span></span>  
:::image-end:::  

### <span data-ttu-id="2deb7-238">Paramètre permettant de désactiver le défilement au-delà de la fin d’un fichier</span><span class="sxs-lookup"><span data-stu-id="2deb7-238">Setting for disabling scrolling past the end of a file</span></span>  

<span data-ttu-id="2deb7-239">Ouvrez [paramètres][Settings] , puis désactivez l’option les sources de **Préférences**  >  **Sources**  >  **autorisent le défilement au-delà de la fin du fichier** pour désactiver le comportement de l’interface utilisateur par défaut qui vous permet de faire défiler le fichier dans le volet **sources** .</span><span class="sxs-lookup"><span data-stu-id="2deb7-239">Open [Settings][Settings] and then disable **Preferences** > **Sources** > **Allow scrolling past end of file** to disable the default UI behavior that allows you to scroll well past the end of a file in the **Sources** panel.</span></span>  

:::image type="complex" source="../../images/2020/01/settings.msft.png" alt-text="Désactivation de l’option autoriser le défilement au-delà de la fin du fichier" lightbox="../../images/2020/01/settings.msft.png":::
   <span data-ttu-id="2deb7-241">Désactivation de l’option autoriser le défilement au- **delà de la fin du fichier** dans les paramètres</span><span class="sxs-lookup"><span data-stu-id="2deb7-241">Disabling **Allow scrolling past end of file** in Settings</span></span>  
:::image-end:::  

:::image type="complex" source="../../images/2020/01/scrollingsources.msft.png" alt-text="Le défilement au-delà de la fin d’un fichier est désormais désactivé dans le panneau sources" lightbox="../../images/2020/01/scrollingsources.msft.png":::
   <span data-ttu-id="2deb7-243">Le défilement au-delà de la fin d’un fichier est désormais désactivé dans le panneau sources</span><span class="sxs-lookup"><span data-stu-id="2deb7-243">Scrolling past the end of a file is now disabled in the Sources panel</span></span>  
:::image-end:::  

## <span data-ttu-id="2deb7-244">Télécharger les canaux Microsoft Edge preview</span><span class="sxs-lookup"><span data-stu-id="2deb7-244">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="2deb7-245">Si vous utilisez Windows ou macOS, envisagez d’utiliser les [canaux Microsoft Edge Preview][MicrosoftEdgePreviewChannels] comme navigateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="2deb7-245">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="2deb7-246">Les canaux d’aperçu vous permettent d’accéder aux dernières fonctionnalités de DevTools.</span><span class="sxs-lookup"><span data-stu-id="2deb7-246">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="2deb7-247">Contacter l’équipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="2deb7-247">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DeviceToolbar]: /microsoft-edge/devtools-guide-chromium/device-mode/index#simulate-a-mobile-viewport "Simuler une fenêtre d’affichage mobile-simuler des appareils mobiles avec le mode appareil dans Microsoft Edge DevTools | Documents Microsoft"
[DeviceFrame]: /microsoft-edge/devtools-guide-chromium/device-mode/index#show-device-frame "Afficher le cadre de l’appareil: simuler les appareils mobiles avec le mode appareil dans Microsoft Edge DevTools | Documents Microsoft"
[CommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Exécuter des commandes à l’aide du menu de commandes de Microsoft Edge DevTools | Documents Microsoft"  
[ThrottleNetworkAndCpu]: /microsoft-edge/devtools-guide-chromium/device-mode/index#throttle-the-network-and-cpu "Limiter la vitesse du réseau et de l’UC-simuler les appareils mobiles avec le mode périphérique dans Microsoft Edge DevTools | Documents Microsoft"
[Settings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Paramètres-personnaliser Microsoft Edge DevTools | Documents Microsoft"
[MicrosoftVisualStudio]: /microsoft-edge/visual-studio/index "Visual Studio | Documents Microsoft"  
[CookiesFields]: /microsoft-edge/devtools-guide-chromium/storage/cookies#fields "Champs: afficher, modifier et supprimer des cookies avec Microsoft Edge DevTools | Documents Microsoft"  

[VisualStudioCodeDebuggerEdgeExtension]: /microsoft-edge/visual-studio-code/debugger-for-edge "Débogueur de l’extension de code Visual Studio Visual Studio"  
[VisualStudioCodeElementEdgeExtension]: /microsoft-edge/visual-studio-code/elements-for-edge "Éléments de l’extension de code Visual Studio Visual Studio"  

[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Canaux Microsoft Edge preview"  

[VisualStudioCode]: https://aka.ms/vscode "Code Visual Studio"  
[VisualStudioMarketplaceDebuggerEdge]: https://aka.ms/debugger4code "Débogueur pour Microsoft Edge-Visual Studio Marketplace"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://aka.ms/elements4code "Éléments pour Microsoft Edge \ (chrome \)-Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://aka.ms/webhint4code "webhint-Visual Studio Marketplace"

[TrackingPrevention]: https://aka.ms/microsoftedge/tracking-prevention-blog "Amélioration de la prévention du suivi dans le billet de blog Microsoft Edge"

[MicrosoftEdgeInsiderAddons]: https://aka.ms/webhint/edge-extension "Compléments Microsoft Edge Insider"  
[MicrosoftVisualStudioDownloads]: https://aka.ms/vs/download "Télécharger Visual Studio 2019 pour Windows & Mac"  

[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Publiez un tweet"  

[CR924693]: https://crbug.com/924693 "Demande de fonctionnalité: Ajouter moto G4 à la liste du mode appareil | Bugs du chrome"  
[CR1030258]: https://crbug.com/1030258 "CR 1030258 | Bugs du chrome"  
[CR1026879]: https://crbug.com/1026879 "L’onglet cookie dans la console de développement ne montre plus de priorité | Bugs du chrome"  
[CR1029826]: https://crbug.com/1029826 "onglet réseau-> cliquez avec le bouton droit pour demander-> copier-> copier comme FETCH ne copie pas les cookies | Bugs du chrome"  
[CR985402]: https://crbug.com/985402 "les chaînes d’erreur d’icône du manifeste de l’application Web sont confuses | Bugs du chrome"  
[CR963183]: https://crbug.com/963183 "DevTools ne respectent pas la norme WCAG | Bugs du chrome"  
[CR941561]: https://crbug.com/941561 "Localization du DevTools | Bugs du chrome"  
[CR987787]: https://crbug.com/987787 "Affichage 3D DOM | Bugs du chrome"  

[CSSContentDemo]: https://mathiasbynens.github.io/css-dbg-stories/css-escapes.html "Démo pour le contenu CSS sans échappement"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Nouveau problème-MicrosoftDocs/Edge-développeur"  

[TheWebWeWant]: https://aka.ms/webwewant "Le site Web de votre choix"  
[AccessibilityInsights]: https://aka.ms/a11yinsights "Insights sur l’accessibilité"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "DOM (Document Object Model) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "index z | MDN"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools compte Twitter"  

[Webhint]: https://aka.ms/webhint "Astuce"  

[WebhintBrowserExtension]: https://aka.ms/webhint/browser-extension "Extension du navigateur webhint | documentation webhint"  
[WebhintVisualStudioCodeExtension]: https://aka.ms/webhint/code-extension "Extension de code Visual Studio webhint | documentation webhint"  

> [!NOTE]
> <span data-ttu-id="2deb7-284">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2deb7-284">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="2deb7-285">La page d’origine est disponible [ici](https://developers.google.com/web/updates/2020/01/devtools/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="2deb7-285">The original page is found [here](https://developers.google.com/web/updates/2020/01/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="2deb7-287">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2deb7-287">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  