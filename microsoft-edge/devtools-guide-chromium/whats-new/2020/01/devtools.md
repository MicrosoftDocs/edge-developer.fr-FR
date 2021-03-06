---
description: Affichage 3D, Visual Studio’intégration à Microsoft Edge, et bien plus encore.
title: Nouveautés de DevTools (Microsoft Edge 81)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: a60be4d55d7f6152ed7ce7afd24049f0f5909a4b
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398244"
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

# <a name="whats-new-in-devtools-microsoft-edge-81"></a><span data-ttu-id="a5c99-104">Nouveautés de DevTools (Microsoft Edge 81)</span><span class="sxs-lookup"><span data-stu-id="a5c99-104">What's New In DevTools (Microsoft Edge 81)</span></span>  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a><span data-ttu-id="a5c99-105">Annonces de l’équipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="a5c99-105">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="a5c99-106">Les sections suivantes sont une liste des annonces que vous avez peut-être manquées de l’équipe Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="a5c99-106">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team.</span></span>  <span data-ttu-id="a5c99-107">Consultez les annonces pour essayer les nouvelles fonctionnalités des extensions DevTools, Microsoft Visual Studio Code, etc.</span><span class="sxs-lookup"><span data-stu-id="a5c99-107">Check out the announcements to try new features in the DevTools, Microsoft Visual Studio Code extensions, and more.</span></span>  <span data-ttu-id="a5c99-108">Pour rester à jour sur toutes les fonctionnalités les plus récentes et les plus importantes de vos outils de développement, téléchargez les canaux d’aperçu [Microsoft Edge][MicrosoftEdgePreviewChannels] et [suivez-nous sur Twitter.][EdgeDevToolsTwitterAccount]</span><span class="sxs-lookup"><span data-stu-id="a5c99-108">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <a name="accessibility-improvements-to-the-devtools"></a><span data-ttu-id="a5c99-109">Améliorations de l’accessibilité de DevTools</span><span class="sxs-lookup"><span data-stu-id="a5c99-109">Accessibility improvements to the DevTools</span></span>  

<span data-ttu-id="a5c99-110">L’équipe DevTools a apporté 170 modifications à Chromium pour résoudre les problèmes de contraste de couleur, de clavier et de lecteur d’écran à fort impact dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="a5c99-110">The DevTools team has contributed 170 changes to Chromium to address high-impact color contrast, keyboard, and screen reader issues in the DevTools.</span></span>  <span data-ttu-id="a5c99-111">Chaque développeur qui construit le web doit être en mesure d’utiliser DevTools.</span><span class="sxs-lookup"><span data-stu-id="a5c99-111">Every developer building the web should be able to use the DevTools.</span></span>  

:::image type="complex" source="../../images/2020/01/a11y-performance-tool.msft.gif" alt-text="L’outil Performances dans DevTools avec les améliorations apportées à la navigation au clavier et au lecteur d’écran" lightbox="../../images/2020/01/a11y-performance-tool.msft.gif":::
   <span data-ttu-id="a5c99-113">**L’outil Performances** dans DevTools avec les améliorations apportées à la navigation au clavier et au lecteur d’écran</span><span class="sxs-lookup"><span data-stu-id="a5c99-113">The **Performance** tool in the DevTools with the keyboard navigation and screen reader improvements</span></span>  
:::image-end:::  

<span data-ttu-id="a5c99-114">Vous souhaitez découvrir comment rendre votre page web accessible à tous vos utilisateurs ?</span><span class="sxs-lookup"><span data-stu-id="a5c99-114">Want to learn how to make your web page accessible to all of your users?</span></span>  <span data-ttu-id="a5c99-115">Téléchargez [les informations sur l’accessibilité][AccessibilityInsights] et les extensions web [pour][WebhintBrowserExtension] que Microsoft Edge commence.</span><span class="sxs-lookup"><span data-stu-id="a5c99-115">Download the [Accessibility Insights][AccessibilityInsights] and [webhint][WebhintBrowserExtension] extensions for Microsoft Edge to get started.</span></span>  

<span data-ttu-id="a5c99-116">Si vous utilisez des lecteurs d’écran ou le clavier pour naviguer dans DevTools, envoyez-nous vos commentaires en nous faisant part de vos [commentaires][PostTweetEdgeDevTools] ou en criant l’icône Envoyer [des](#getting-in-touch-with-microsoft-edge-devtools-team) commentaires !</span><span class="sxs-lookup"><span data-stu-id="a5c99-116">If you use screen readers or the keyboard to navigate around the DevTools, send us your feedback by [tweeting][PostTweetEdgeDevTools] at us orchoosing the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="a5c99-117">Problème de chrome [#963183][CR963183]</span><span class="sxs-lookup"><span data-stu-id="a5c99-117">Chromium issue [#963183][CR963183]</span></span>  

### <a name="using-the-devtools-in-other-languages"></a><span data-ttu-id="a5c99-118">Utilisation de DevTools dans d’autres langues</span><span class="sxs-lookup"><span data-stu-id="a5c99-118">Using the DevTools in other languages</span></span>  

<span data-ttu-id="a5c99-119">De nombreux développeurs utilisent d’autres outils de développement, tels que StackOverflow et Visual Studio Code, dans leur langue native, et pas seulement en anglais.</span><span class="sxs-lookup"><span data-stu-id="a5c99-119">Many developers use other developer tools, like StackOverflow and Visual Studio Code, in their native language, not just in English.</span></span>  <span data-ttu-id="a5c99-120">Nous sommes ravis d’annoncer la localisation de DevTools, que vous pouvez désormais utiliser dans l’une des 10 langues en plus de l’anglais :</span><span class="sxs-lookup"><span data-stu-id="a5c99-120">We’re excited to announce localization for the DevTools, which you are now able to use in one of 10 languages besides English:</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="a5c99-121">Chinois \(Simplifié\) - &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span><span class="sxs-lookup"><span data-stu-id="a5c99-121">Chinese \(Simplified\) - &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="a5c99-122">Chinois \(Traditionnel\) - &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span><span class="sxs-lookup"><span data-stu-id="a5c99-122">Chinese \(Traditional\) - &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="a5c99-123">Français –&#231;ais</span><span class="sxs-lookup"><span data-stu-id="a5c99-123">French – fran&#231;ais</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="a5c99-124">Allemand - deu deutsche</span><span class="sxs-lookup"><span data-stu-id="a5c99-124">German - deutsch</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="a5c99-125">Italien - italiano</span><span class="sxs-lookup"><span data-stu-id="a5c99-125">Italian - italiano</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="a5c99-126">Japonais - &#26085;&#26412;&#35486;</span><span class="sxs-lookup"><span data-stu-id="a5c99-126">Japanese - &#26085;&#26412;&#35486;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="a5c99-127">Coréen - &#54620;&#44397;&#50612;</span><span class="sxs-lookup"><span data-stu-id="a5c99-127">Korean - &#54620;&#44397;&#50612;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="a5c99-128">Portugais - portugu&#234;s</span><span class="sxs-lookup"><span data-stu-id="a5c99-128">Portuguese - portugu&#234;s</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="a5c99-129">Russe – &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span><span class="sxs-lookup"><span data-stu-id="a5c99-129">Russian – &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="a5c99-130">Espagnol - espa&#241;ol</span><span class="sxs-lookup"><span data-stu-id="a5c99-130">Spanish - espa&#241;ol</span></span>
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

<span data-ttu-id="a5c99-131">DevTools correspond automatiquement à la langue que vous utilisez pour Microsoft Edge dans `edge://settings/languages` .</span><span class="sxs-lookup"><span data-stu-id="a5c99-131">The DevTools automatically match the language you use for Microsoft Edge in `edge://settings/languages`.</span></span>  

<span data-ttu-id="a5c99-132">Si vous souhaitez que Microsoft Edge soit dans une langue et que vos DevTools restent en anglais, sélectionnez `F1` Dans DevTools pour ouvrir [Paramètres][Settings] et désactiver la langue du navigateur Match . \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="a5c99-132">If you want Microsoft Edge to be in one language and your DevTools to remain in English, select `F1` in the DevTools to open [Settings][Settings] and disable **Match browser language**.</span></span>  

:::image type="complex" source="../../images/2020/01/localized-devtools.msft.png" alt-text="DevTools en allemand" lightbox="../../images/2020/01/localized-devtools.msft.png":::
   <span data-ttu-id="a5c99-134">DevTools en allemand</span><span class="sxs-lookup"><span data-stu-id="a5c99-134">The DevTools in German</span></span>  
:::image-end:::  

<span data-ttu-id="a5c99-135">**Les** messages de la console ne sont pas localisées.</span><span class="sxs-lookup"><span data-stu-id="a5c99-135">**Console** messages are not localized.</span></span>  <span data-ttu-id="a5c99-136">Seules les chaînes utilisées dans l’interface utilisateur de DevTools sont affichées dans la langue que vous utilisez pour Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a5c99-136">Only the strings used in the DevTools UI are displayed in the language you use for Microsoft Edge.</span></span>  

<span data-ttu-id="a5c99-137">Si vous souhaitez utiliser les DevTools dans une autre langue que celles [disponibles,][PostTweetEdgeDevTools] tweetez-nous ou sélectionnez l’icône Envoyer [des](#getting-in-touch-with-microsoft-edge-devtools-team) commentaires.</span><span class="sxs-lookup"><span data-stu-id="a5c99-137">If you want to use the DevTools in a different language than the ones that are available, [tweet][PostTweetEdgeDevTools] at us or choose the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon.</span></span>  

<span data-ttu-id="a5c99-138">Problème de chrome [#941561][CR941561]</span><span class="sxs-lookup"><span data-stu-id="a5c99-138">Chromium issue [#941561][CR941561]</span></span>  

### <a name="webhint-microsoft-edge-extension"></a><span data-ttu-id="a5c99-139">extension Webhint Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a5c99-139">webhint Microsoft Edge extension</span></span>  

<span data-ttu-id="a5c99-140">L’extension Microsoft Edge webhint vous permet d’analyser facilement votre page web et d’obtenir des commentaires sur l’accessibilité, la compatibilité du navigateur, la sécurité, les performances et bien plus encore dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="a5c99-140">The webhint Microsoft Edge extension allows you to easily scan your web page and get feedback on accessibility, browser compatibility, security, performance, and more within the DevTools.</span></span>  <span data-ttu-id="a5c99-141">Pour plus d’informations, [https://webhint.io][Webhint] voir .</span><span class="sxs-lookup"><span data-stu-id="a5c99-141">Read more at [https://webhint.io][Webhint].</span></span>  

:::image type="complex" source="../../images/2020/01/webhint-browser-extension.msft.png" alt-text="Outil Hints dans DevTools lors de l’installation de l’extension de navigateur webhint" lightbox="../../images/2020/01/webhint-browser-extension.msft.png":::
   <span data-ttu-id="a5c99-143">Outil **Hints** dans DevTools lors de l’installation de l’extension de navigateur webhint</span><span class="sxs-lookup"><span data-stu-id="a5c99-143">The **Hints** tool in the DevTools when the webhint browser extension is installed</span></span>  
:::image-end:::  

<span data-ttu-id="a5c99-144">[Essayez l’extension de navigateur webhint dans Microsoft Edge.][MicrosoftEdgeInsiderAddons]</span><span class="sxs-lookup"><span data-stu-id="a5c99-144">[Try the webhint browser extension in Microsoft Edge][MicrosoftEdgeInsiderAddons].</span></span>  <span data-ttu-id="a5c99-145">Une fois l’extension installée, ouvrez DevTools et choisissez **l’outil Hints.**</span><span class="sxs-lookup"><span data-stu-id="a5c99-145">Once you install the extension, open the DevTools and choose the **Hints** tool.</span></span>  <span data-ttu-id="a5c99-146">À partir de là, exécutez une analyse de site personnalisable.</span><span class="sxs-lookup"><span data-stu-id="a5c99-146">From here, run a customizable site scan.</span></span>  <span data-ttu-id="a5c99-147">Pour en savoir [plus, webhint.io][WebhintBrowserExtension] plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="a5c99-147">Head over to [webhint.io][WebhintBrowserExtension] to learn more.</span></span>  

### <a name="3d-view"></a><span data-ttu-id="a5c99-148">Vue 3D</span><span class="sxs-lookup"><span data-stu-id="a5c99-148">3D View</span></span>  

<span data-ttu-id="a5c99-149">Utilisez la vue **3D** pour déboguer votre application web en naviguant dans le modèle objet de document [\(DOM\)][MDNDocumentObjectModel] ou le contexte d’empilement [d’index z.][MDNZIndex]</span><span class="sxs-lookup"><span data-stu-id="a5c99-149">Use the **3D View** to debug your web application by navigating through the [Document Object Model \(DOM\)][MDNDocumentObjectModel] or the [z-index][MDNZIndex] stacking context.</span></span>  

:::image type="complex" source="../../images/2020/01/3dview.msft.png" alt-text="Affichage 3D dans devTools" lightbox="../../images/2020/01/3dview.msft.png":::
   <span data-ttu-id="a5c99-151">Affichage 3D dans devTools</span><span class="sxs-lookup"><span data-stu-id="a5c99-151">The 3D View in the DevTools</span></span>  
:::image-end:::  

<span data-ttu-id="a5c99-152">Pour accéder à la vue 3D, sélectionnez , tapez en mode `Ctrl`  +  `Shift`  +  `P` **3D** et **sélectionnez Afficher la vue 3D.**</span><span class="sxs-lookup"><span data-stu-id="a5c99-152">To access the 3D View, select `Ctrl` + `Shift` + `P`, type in **3D View** and select **Show 3D View**.</span></span>  

<span data-ttu-id="a5c99-153">L’équipe Microsoft Edge travaille avec l’équipe Chromium sur l’interface utilisateur et ajoute des fonctionnalités à la vue 3D. Par ailleurs, envoyez vos [commentaires.](#getting-in-touch-with-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="a5c99-153">The Microsoft Edge team is working with the Chromium team on the UI and adding more functionality to the 3D View, so please send your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team).</span></span>  

<span data-ttu-id="a5c99-154">Problème de chrome [#987787][CR987787]</span><span class="sxs-lookup"><span data-stu-id="a5c99-154">Chromium issue [#987787][CR987787]</span></span>  

### <a name="visual-studio-code-extensions"></a><span data-ttu-id="a5c99-155">Visual Studio extensions de code</span><span class="sxs-lookup"><span data-stu-id="a5c99-155">Visual Studio Code extensions</span></span>  

<span data-ttu-id="a5c99-156">L’équipe DevTools a également publié certaines extensions pour [Visual Studio Code][VisualStudioCode] qui vous permet d’utiliser la puissance de DevTools directement à partir de votre éditeur de texte !</span><span class="sxs-lookup"><span data-stu-id="a5c99-156">The DevTools team has also released some extensions for [Visual Studio Code][VisualStudioCode] that let you use the power of the DevTools directly from your text editor!</span></span> <span data-ttu-id="a5c99-157">Consultez les extensions ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="a5c99-157">Check out the extensions below:</span></span>  

#### <a name="elements-for-microsoft-edge"></a><span data-ttu-id="a5c99-158">Éléments pour Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a5c99-158">Elements for Microsoft Edge</span></span>  

<span data-ttu-id="a5c99-159">Utilisez l’outil Elements à partir Visual Studio Code en ajoutant les éléments pour [Microsoft Edge \(Chromium\)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] Visual Studio l’extension de code.</span><span class="sxs-lookup"><span data-stu-id="a5c99-159">Use the Elements tool from within Visual Studio Code by adding the [Elements for Microsoft Edge \(Chromium\)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] Visual Studio Code extension.</span></span>  

:::image type="complex" source="../../images/2020/01/elements-for-edge.msft.png" alt-text="L’outil Elements dans Visual Studio Code à l’aide de l’extension Elements pour Microsoft Edge" lightbox="../../images/2020/01/elements-for-edge.msft.png":::
   <span data-ttu-id="a5c99-161">**L’outil Elements** dans Visual Studio Code à l’aide de l’extension Elements pour Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a5c99-161">The **Elements** tool in Visual Studio Code using the Elements for Microsoft Edge extension</span></span>  
:::image-end:::  

<span data-ttu-id="a5c99-162">Pour plus d’informations, consultez [Éléments pour l’extension][VisualStudioCodeElementEdgeExtension]de code Visual Studio Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a5c99-162">For more information, check out [Elements for Microsoft Edge Visual Studio Code extension][VisualStudioCodeElementEdgeExtension].</span></span>  

#### <a name="debugger-for-microsoft-edge"></a><span data-ttu-id="a5c99-163">Débogger pour Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a5c99-163">Debugger for Microsoft Edge</span></span>  

<span data-ttu-id="a5c99-164">Avec le [déboguer pour l’extension][VisualStudioMarketplaceDebuggerEdge] de code Visual Studio Microsoft Edge, déboguer JavaScript en cours d’exécution dans Microsoft Edge directement à partir Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="a5c99-164">With the [Debugger for Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] Visual Studio Code extension, debug JavaScript running in Microsoft Edge directly from Visual Studio Code.</span></span>  

:::image type="complex" source="../../images/2020/01/vscode-debugger.msft.png" alt-text="Débogger pour l’extension Microsoft Edge dans Visual Studio Code" lightbox="../../images/2020/01/vscode-debugger.msft.png":::
   <span data-ttu-id="a5c99-166">Débogger pour l’extension Microsoft Edge dans Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="a5c99-166">The Debugger for Microsoft Edge Extension in Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="a5c99-167">Pour plus d’informations, [découvrez comment déboguer Microsoft Edge][VisualStudioCodeDebuggerEdgeExtension]à partir de Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="a5c99-167">For more information, check out [how to debug Microsoft Edge from Visual Studio Code][VisualStudioCodeDebuggerEdgeExtension].</span></span>  

#### <a name="webhint"></a><span data-ttu-id="a5c99-168">webhint</span><span class="sxs-lookup"><span data-stu-id="a5c99-168">webhint</span></span>  

<span data-ttu-id="a5c99-169">La [Visual Studio][VisualStudioMarketplaceWebhintExtension] l’extension de code utilise pour améliorer votre page web pendant `webhint` que vous l’écrivez.</span><span class="sxs-lookup"><span data-stu-id="a5c99-169">The [webhint][VisualStudioMarketplaceWebhintExtension] Visual Studio Code extension uses `webhint` to improve your web page while you are writing it.</span></span>  <span data-ttu-id="a5c99-170">Cette extension s’exécute et signale les diagnostics sur vos fichiers d’espace de travail en fonction de `webhint` l’analyse.</span><span class="sxs-lookup"><span data-stu-id="a5c99-170">This extension runs and reports diagnostics on your workspace files based on `webhint` analysis.</span></span>  

:::image type="complex" source="../../images/2020/01/webhint-vscode-extension.msft.png" alt-text="The webhint Visual Studio Code extension analyzing a .tsx file in Visual Studio Code" lightbox="../../images/2020/01/webhint-vscode-extension.msft.png":::
   <span data-ttu-id="a5c99-172">La page web Visual Studio’extension de code analysant un `.tsx` fichier dans Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="a5c99-172">The webhint Visual Studio Code extension analyzing a `.tsx` file in Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="a5c99-173">[En savoir plus sur l Visual Studio’extension web code.][WebhintVisualStudioCodeExtension]</span><span class="sxs-lookup"><span data-stu-id="a5c99-173">[Learn more about the Visual Studio Code webhint extension][WebhintVisualStudioCodeExtension].</span></span>  

### <a name="visual-studio-integration"></a><span data-ttu-id="a5c99-174">Visual Studio’intégration</span><span class="sxs-lookup"><span data-stu-id="a5c99-174">Visual Studio integration</span></span>  

<span data-ttu-id="a5c99-175">Dans Visual Studio version 2019 16.2 ou ultérieure, utilisez le déboguer Visual Studio déboguer JavaScript en cours d’exécution dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a5c99-175">In Visual Studio 2019 version 16.2 or later, use the Visual Studio debugger to debug JavaScript running in Microsoft Edge.</span></span>  <span data-ttu-id="a5c99-176">[Téléchargez Visual Studio 2019][MicrosoftVisualStudioDownloads] pour tester cette fonctionnalité !</span><span class="sxs-lookup"><span data-stu-id="a5c99-176">[Download Visual Studio 2019][MicrosoftVisualStudioDownloads] to try this feature out!</span></span>  

:::image type="complex" source="../../images/2020/01/vs.msft.png" alt-text="Visual Studio avec la possibilité de lancer votre application web dans Microsoft Edge Canary, Dev ou Beta" lightbox="../../images/2020/01/vs.msft.png":::
   <span data-ttu-id="a5c99-178">Visual Studio avec la possibilité de lancer votre application web dans Microsoft Edge Canary, Dev ou Beta</span><span class="sxs-lookup"><span data-stu-id="a5c99-178">Visual Studio with the option to launch your web app in Microsoft Edge Canary, Dev, or Beta</span></span>  
:::image-end:::  

<span data-ttu-id="a5c99-179">[En savoir plus sur le débogage de Microsoft Edge à partir Visual Studio][MicrosoftVisualStudio].</span><span class="sxs-lookup"><span data-stu-id="a5c99-179">[Learn more about debugging Microsoft Edge from Visual Studio][MicrosoftVisualStudio].</span></span>  

### <a name="tracking-prevention-console-messages"></a><span data-ttu-id="a5c99-180">Suivi des messages de la console de prévention</span><span class="sxs-lookup"><span data-stu-id="a5c99-180">Tracking prevention Console messages</span></span>  

<span data-ttu-id="a5c99-181">La prévention du suivi est une fonctionnalité unique de Microsoft Edge qui vous empêche d’être suivi par des sites web que vous n’avez pas visités auparavant.</span><span class="sxs-lookup"><span data-stu-id="a5c99-181">Tracking prevention is a unique feature in Microsoft Edge that protects you from being tracked by websites you have not visited before.</span></span>  <span data-ttu-id="a5c99-182">Le paramètre de prévention du suivi par défaut est le mode équilibré, qui bloque les suivis tiers et les suivis malveillants connus pour une expérience qui équilibre la confidentialité et la compatibilité web.</span><span class="sxs-lookup"><span data-stu-id="a5c99-182">The default tracking prevention setting is Balanced mode, which blocks 3rd party trackers and known malicious trackers for an experience that balances privacy and web compatibility.</span></span>  <span data-ttu-id="a5c99-183">Pour vous donner plus d’informations sur la compatibilité de votre page web lorsque certains suivis sont bloqués, des messages d’avertissement ont été ajoutés dans la **console** lorsqu’un suivi est bloqué.</span><span class="sxs-lookup"><span data-stu-id="a5c99-183">To give you more insight into the compatibility of your web page when certain trackers are blocked, warning messages were added in the **Console** when a tracker is blocked.</span></span>  

:::image type="complex" source="../../images/2020/01/tracking-prevention.msft.png" alt-text="Messages dans la console lorsque la prévention du suivi bloque l’accès au stockage pour un suivi" lightbox="../../images/2020/01/tracking-prevention.msft.png":::
   <span data-ttu-id="a5c99-185">Messages dans la **console lorsque la prévention** du suivi bloque l’accès au stockage pour un suivi</span><span class="sxs-lookup"><span data-stu-id="a5c99-185">Messages in the **Console** when tracking prevention blocks access to storage for a tracker</span></span>  
:::image-end:::  

<span data-ttu-id="a5c99-186">[En savoir plus sur la prévention du suivi et l’équilibre entre la confidentialité et la compatibilité web.][TrackingPrevention]</span><span class="sxs-lookup"><span data-stu-id="a5c99-186">[Read more about tracking prevention and the balance between privacy and web compatibility][TrackingPrevention].</span></span>  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="a5c99-187">Annonces du projet de Chromium</span><span class="sxs-lookup"><span data-stu-id="a5c99-187">Announcements from the Chromium project</span></span>  

<span data-ttu-id="a5c99-188">Les sections suivantes annoncent des fonctionnalités supplémentaires disponibles dans Microsoft Edge 81 qui ont été contribués au projet Chromium open source.</span><span class="sxs-lookup"><span data-stu-id="a5c99-188">The following sections announce additional features available in Microsoft Edge 81 that were contributed to the open source Chromium project.</span></span>  

### <a name="moto-g4-support-in-device-mode"></a><span data-ttu-id="a5c99-189">Prise en charge du G4 dans le mode appareil</span><span class="sxs-lookup"><span data-stu-id="a5c99-189">Moto G4 support in Device Mode</span></span>  

<span data-ttu-id="a5c99-190">Après [avoir activé la barre d’outils][DeviceToolbar]de l’appareil, simulez les dimensions d’uneport d’affichage g4 à partir de la liste **des** appareils.</span><span class="sxs-lookup"><span data-stu-id="a5c99-190">After [enabling the Device Toolbar][DeviceToolbar], simulate the dimensions of a Moto G4 viewport from the **Device** list.</span></span>  

:::image type="complex" source="../../images/2020/01/motog4.msft.png" alt-text="Simulation d’uneport d’affichage G4" lightbox="../../images/2020/01/motog4.msft.png":::
   <span data-ttu-id="a5c99-192">Simulation d’uneport d’affichage G4</span><span class="sxs-lookup"><span data-stu-id="a5c99-192">Simulating a Moto G4 viewport</span></span>  
:::image-end:::  

<span data-ttu-id="a5c99-193">Sélectionnez [Afficher le cadre de][DeviceFrame] l’appareil pour afficher le matériel de LaG4 autour de la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="a5c99-193">Choose [Show Device Frame][DeviceFrame] to show the Moto G4 hardware around the viewport.</span></span>  

:::image type="complex" source="../../images/2020/01/motog4frame.msft.png" alt-text="Affichage du matériel Du G4" lightbox="../../images/2020/01/motog4frame.msft.png":::
   <span data-ttu-id="a5c99-195">Affichage du matériel Du G4</span><span class="sxs-lookup"><span data-stu-id="a5c99-195">Showing the Moto G4 hardware</span></span>  
:::image-end:::  

<span data-ttu-id="a5c99-196">Fonctionnalités connexes :</span><span class="sxs-lookup"><span data-stu-id="a5c99-196">Related features:</span></span>  

*   <span data-ttu-id="a5c99-197">Ouvrez [le menu De][CommandMenu] commande et exécutez la commande pour prendre une capture d’écran de la fenêtre d’affichage qui inclut le matériel de Contrôle G4 (après l’activation de l’activation de l’affichage du cadre de `Capture screenshot` **périphérique).**</span><span class="sxs-lookup"><span data-stu-id="a5c99-197">Open the [Command Menu][CommandMenu] and run the `Capture screenshot` command to take a screenshot of the viewport that includes the Moto G4 hardware (after enabling **Show Device Frame**).</span></span>  
*   <span data-ttu-id="a5c99-198">[Limiter le réseau et le processeur][ThrottleNetworkAndCpu] pour simuler plus précisément les conditions de navigation web d’un utilisateur mobile.</span><span class="sxs-lookup"><span data-stu-id="a5c99-198">[Throttle the network and CPU][ThrottleNetworkAndCpu] to more accurately simulate a mobile user's web browsing conditions.</span></span>  

<span data-ttu-id="a5c99-199">Problème de chrome [#924693][CR924693]</span><span class="sxs-lookup"><span data-stu-id="a5c99-199">Chromium issue [#924693][CR924693]</span></span>  

### <a name="cookie-related-updates"></a><span data-ttu-id="a5c99-200">Mises à jour relatives aux cookies</span><span class="sxs-lookup"><span data-stu-id="a5c99-200">Cookie-related updates</span></span>  

#### <a name="blocked-cookies-in-the-cookies-pane"></a><span data-ttu-id="a5c99-201">Cookies bloqués dans le volet Cookies</span><span class="sxs-lookup"><span data-stu-id="a5c99-201">Blocked cookies in the Cookies pane</span></span>  

<span data-ttu-id="a5c99-202">Le volet Cookies du panneau Application affiche désormais les cookies bloqués avec un arrière-plan jaune.</span><span class="sxs-lookup"><span data-stu-id="a5c99-202">The Cookies pane in the Application panel now displays blocked cookies with a yellow background.</span></span>  

:::image type="complex" source="../../images/2020/01/blockedcookies.msft.png" alt-text="Cookies bloqués dans le volet Cookies du panneau Application" lightbox="../../images/2020/01/blockedcookies.msft.png":::
   <span data-ttu-id="a5c99-204">Cookies bloqués dans le volet Cookies du panneau Application</span><span class="sxs-lookup"><span data-stu-id="a5c99-204">Blocked cookies in the Cookies pane of the Application panel</span></span>  
:::image-end:::  

<span data-ttu-id="a5c99-205">Problème de chrome [#1030258][CR1030258]</span><span class="sxs-lookup"><span data-stu-id="a5c99-205">Chromium issue [#1030258][CR1030258]</span></span>  <!-- inaccessible  -->  

#### <a name="cookie-priority-in-the-cookie-pane"></a><span data-ttu-id="a5c99-206">Priorité des cookies dans le volet Cookie</span><span class="sxs-lookup"><span data-stu-id="a5c99-206">Cookie priority in the Cookie pane</span></span>  

<span data-ttu-id="a5c99-207">Les tableaux Cookies des **outils** Réseau et **Application** incluent désormais une **colonne** Priorité.</span><span class="sxs-lookup"><span data-stu-id="a5c99-207">The Cookies tables in the **Network** and **Application** tools now include a **Priority** column.</span></span>  

> [!CAUTION]
> <span data-ttu-id="a5c99-208">Les navigateurs basés sur Chromium, tels que Microsoft Edge, sont les seuls à la prise en charge de la priorité des cookies.</span><span class="sxs-lookup"><span data-stu-id="a5c99-208">Chromium-based browsers, like Microsoft Edge, are the only browsers that support cookie priority.</span></span>  

<span data-ttu-id="a5c99-209">Problème de chrome [#1026879][CR1026879]</span><span class="sxs-lookup"><span data-stu-id="a5c99-209">Chromium issue [#1026879][CR1026879]</span></span>  

#### <a name="edit-all-cookie-values"></a><span data-ttu-id="a5c99-210">Modifier toutes les valeurs de cookie</span><span class="sxs-lookup"><span data-stu-id="a5c99-210">Edit all cookie values</span></span>  

<span data-ttu-id="a5c99-211">Toutes les cellules des tableaux cookies sont modifiables maintenant, à l’exception des cellules de la colonne **Size,** car cette colonne représente la taille réseau du cookie, en octets.</span><span class="sxs-lookup"><span data-stu-id="a5c99-211">All cells in the Cookie tables are editable now, except cells in the **Size** column because that column represents the network size of the cookie, in bytes.</span></span>  <span data-ttu-id="a5c99-212">Pour obtenir une explication de chaque colonne, accédez à [Champs.][CookiesFields]</span><span class="sxs-lookup"><span data-stu-id="a5c99-212">For an explanation of each column, navigate to [Fields][CookiesFields].</span></span>  

:::image type="complex" source="../../images/2020/01/editcookie.msft.png" alt-text="Modification d’une valeur de cookie" lightbox="../../images/2020/01/editcookie.msft.png":::
   <span data-ttu-id="a5c99-214">Modification d’une valeur de cookie</span><span class="sxs-lookup"><span data-stu-id="a5c99-214">Editing a cookie value</span></span>  
:::image-end:::  

#### <a name="copy-as-nodejs-fetch-to-include-cookie-data"></a><span data-ttu-id="a5c99-215">Copier en tant que Node.js pour inclure des données de cookie</span><span class="sxs-lookup"><span data-stu-id="a5c99-215">Copy as Node.js fetch to include cookie data</span></span>  

<span data-ttu-id="a5c99-216">Pour obtenir une expression qui inclut des données de cookie, pointez sur une demande réseau, ouvrez le menu contextuel `fetch` \(clic droit\), puis choisissez Copier comme Node.js \*\*\*\*  >  **récupérer.**</span><span class="sxs-lookup"><span data-stu-id="a5c99-216">To get a `fetch` expression that includes cookie data, hover on a network request, open the contextual menu \(right-click\), and choose **Copy** > **Copy as Node.js fetch**.</span></span>  

:::image type="complex" source="../../images/2020/01/fetchcookies.msft.png" alt-text="Copier en tant Node.js récupérer" lightbox="../../images/2020/01/fetchcookies.msft.png":::
   <span data-ttu-id="a5c99-218">Copier en tant Node.js récupérer</span><span class="sxs-lookup"><span data-stu-id="a5c99-218">Copy as Node.js fetch</span></span>  
:::image-end:::  

<span data-ttu-id="a5c99-219">Problème de chrome [#1029826][CR1029826]</span><span class="sxs-lookup"><span data-stu-id="a5c99-219">Chromium issue [#1029826][CR1029826]</span></span>  

### <a name="more-accurate-web-app-manifest-icons"></a><span data-ttu-id="a5c99-220">Icônes de manifeste d’application web plus précises</span><span class="sxs-lookup"><span data-stu-id="a5c99-220">More accurate web app manifest icons</span></span>  

<span data-ttu-id="a5c99-221">Auparavant, le volet Manifeste du panneau Application envoyait ses propres demandes afin d’afficher les icônes de manifeste d’application web.</span><span class="sxs-lookup"><span data-stu-id="a5c99-221">Previously, the Manifest pane in the Application panel sent its own requests in order to display web app manifest icons.</span></span>  <span data-ttu-id="a5c99-222">DevTools affiche désormais la même icône de manifeste que Microsoft Edge utilise.</span><span class="sxs-lookup"><span data-stu-id="a5c99-222">DevTools now shows the exact same manifest icon that Microsoft Edge uses.</span></span>  

:::image type="complex" source="../../images/2020/01/manifesticons.msft.png" alt-text="Icônes dans le volet manifeste" lightbox="../../images/2020/01/manifesticons.msft.png":::
   <span data-ttu-id="a5c99-224">Icônes dans le volet manifeste</span><span class="sxs-lookup"><span data-stu-id="a5c99-224">Icons in the Manifest pane</span></span>  
:::image-end:::  

<span data-ttu-id="a5c99-225">Problème de chrome [#985402][CR985402]</span><span class="sxs-lookup"><span data-stu-id="a5c99-225">Chromium issue [#985402][CR985402]</span></span>  

### <a name="hover-on-css-content-properties-to-display-unescaped-values"></a><span data-ttu-id="a5c99-226">Pointer sur les propriétés de contenu CSS pour afficher des valeurs non scaped</span><span class="sxs-lookup"><span data-stu-id="a5c99-226">Hover on CSS content properties to display unescaped values</span></span>  

<span data-ttu-id="a5c99-227">Pointez sur la valeur d’une propriété pour afficher la `content` version sans paysage de la valeur.</span><span class="sxs-lookup"><span data-stu-id="a5c99-227">Hover on the value of a `content` property to display the unescaped version of the value.</span></span>  

<span data-ttu-id="a5c99-228">Par exemple, dans cette [démonstration,][CSSContentDemo] lorsque vous examinez le pseudo-élément, une chaîne d’échappée s’affiche `p::after` dans le volet **Styles** :</span><span class="sxs-lookup"><span data-stu-id="a5c99-228">For example, in this [demo][CSSContentDemo] when you inspect the `p::after` pseudo-element an escaped string is displayed in the **Styles** pane:</span></span>  

:::image type="complex" source="../../images/2020/01/escapedstring.msft.png" alt-text="Chaîne d’échadé" lightbox="../../images/2020/01/escapedstring.msft.png":::
   <span data-ttu-id="a5c99-230">Chaîne d’échadé</span><span class="sxs-lookup"><span data-stu-id="a5c99-230">The escaped string</span></span>  
:::image-end:::  

<span data-ttu-id="a5c99-231">Lorsque vous pointez sur la `content` valeur, la valeur non érosée s’affiche.</span><span class="sxs-lookup"><span data-stu-id="a5c99-231">When you hover on the `content` value, the unescaped value is displayed.</span></span>  

:::image type="complex" source="../../images/2020/01/unescapedstring.msft.png" alt-text="Valeur non scaped" lightbox="../../images/2020/01/unescapedstring.msft.png":::
   <span data-ttu-id="a5c99-233">Valeur non scaped</span><span class="sxs-lookup"><span data-stu-id="a5c99-233">The unescaped value</span></span>  
:::image-end:::  

### <a name="more-detailed-source-map-errors-in-the-console"></a><span data-ttu-id="a5c99-234">Erreurs de carte source plus détaillées dans la console</span><span class="sxs-lookup"><span data-stu-id="a5c99-234">More detailed source map errors in the Console</span></span>  

<span data-ttu-id="a5c99-235">La console fournit désormais plus de détails sur les raisons pour lesquelles un MAP source n’a pas pu être chargé ou l’analyse.</span><span class="sxs-lookup"><span data-stu-id="a5c99-235">The Console now provides more detail on why a source map failed to load or parse.</span></span>  <span data-ttu-id="a5c99-236">Auparavant, il a simplement fourni une erreur sans expliquer ce qui s’est passé.</span><span class="sxs-lookup"><span data-stu-id="a5c99-236">Previously it just provided an error without explaining what went wrong.</span></span>  

:::image type="complex" source="../../images/2020/01/sourcemap.msft.png" alt-text="Erreur de chargement d’une carte source dans la console" lightbox="../../images/2020/01/sourcemap.msft.png":::
   <span data-ttu-id="a5c99-238">Erreur de chargement d’une carte source dans la console</span><span class="sxs-lookup"><span data-stu-id="a5c99-238">A source map loading error in the Console</span></span>  
:::image-end:::  

### <a name="setting-for-disabling-scrolling-past-the-end-of-a-file"></a><span data-ttu-id="a5c99-239">Paramètre de désactivation du défilement au-delà de la fin d’un fichier</span><span class="sxs-lookup"><span data-stu-id="a5c99-239">Setting for disabling scrolling past the end of a file</span></span>  

<span data-ttu-id="a5c99-240">Ouvrez [Paramètres,][Settings] \*\*\*\* puis désactivez Préférences Sources Autoriser le défilement au-delà de la fin du fichier pour désactiver le comportement de l’interface utilisateur par défaut qui vous permet de faire défiler bien au-delà de la fin d’un fichier dans le panneau  >  \*\*\*\*  >  \*\*\*\* **Sources.**</span><span class="sxs-lookup"><span data-stu-id="a5c99-240">Open [Settings][Settings] and then disable **Preferences** > **Sources** > **Allow scrolling past end of file** to disable the default UI behavior that allows you to scroll well past the end of a file in the **Sources** panel.</span></span>  

:::image type="complex" source="../../images/2020/01/settings.msft.png" alt-text="Désactivation de l’utilisation du défilement au-delà de la fin du fichier" lightbox="../../images/2020/01/settings.msft.png":::
   <span data-ttu-id="a5c99-242">Désactivation de **l’utilisation du défilement au-delà de la fin du fichier** dans paramètres</span><span class="sxs-lookup"><span data-stu-id="a5c99-242">Disabling **Allow scrolling past end of file** in Settings</span></span>  
:::image-end:::  

:::image type="complex" source="../../images/2020/01/scrollingsources.msft.png" alt-text="Le défilement au-delà de la fin d’un fichier est désormais désactivé dans le panneau Sources" lightbox="../../images/2020/01/scrollingsources.msft.png":::
   <span data-ttu-id="a5c99-244">Le défilement au-delà de la fin d’un fichier est désormais désactivé dans le panneau Sources</span><span class="sxs-lookup"><span data-stu-id="a5c99-244">Scrolling past the end of a file is now disabled in the Sources panel</span></span>  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="a5c99-245">Télécharger les canaux d’aperçu Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a5c99-245">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="a5c99-246">Si vous utilisez Windows ou macOS, envisagez d’utiliser les canaux d’aperçu [Microsoft Edge][MicrosoftEdgePreviewChannels] comme navigateur de développement par défaut.</span><span class="sxs-lookup"><span data-stu-id="a5c99-246">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="a5c99-247">Les canaux d’aperçu vous permettent d’accéder aux dernières fonctionnalités de DevTools.</span><span class="sxs-lookup"><span data-stu-id="a5c99-247">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="a5c99-248">Contacter l’équipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="a5c99-248">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DeviceToolbar]: /microsoft-edge/devtools-guide-chromium/device-mode/index#simulate-a-mobile-viewport "Simuler une port d’affichage mobile : simuler des appareils mobiles avec le mode appareil dans Microsoft Edge DevTools | Documents Microsoft"
[DeviceFrame]: /microsoft-edge/devtools-guide-chromium/device-mode/index#show-device-frame "Afficher l’image de l’appareil : simuler des appareils mobiles avec le mode appareil dans Microsoft Edge DevTools | Documents Microsoft"
[CommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Exécuter des commandes avec le menu de commandes Microsoft Edge DevTools | Documents Microsoft"  
[ThrottleNetworkAndCpu]: /microsoft-edge/devtools-guide-chromium/device-mode/index#throttle-the-network-and-cpu "Limiter le réseau et le processeur : simuler des appareils mobiles en mode appareil dans Microsoft Edge DevTools | Documents Microsoft"
[Settings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Paramètres-personnaliser Microsoft Edge DevTools | Documents Microsoft"
[MicrosoftVisualStudio]: /microsoft-edge/visual-studio/index "Visual Studio | Documents Microsoft"  
[CookiesFields]: /microsoft-edge/devtools-guide-chromium/storage/cookies#fields "Champs : afficher, modifier et supprimer des cookies avec Microsoft Edge DevTools | Documents Microsoft"  

[VisualStudioCodeDebuggerEdgeExtension]: /microsoft-edge/visual-studio-code/debugger-for-edge "Débogger pour l’extension de code Visual Studio Microsoft Edge"  
[VisualStudioCodeElementEdgeExtension]: /microsoft-edge/visual-studio-code/elements-for-edge "Éléments de l’extension de code Visual Studio Microsoft Edge"  

[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Canaux d’aperçu Microsoft Edge"  

[VisualStudioCode]: https://aka.ms/vscode "Visual Studio Code"  
[VisualStudioMarketplaceDebuggerEdge]: https://aka.ms/debugger4code "Débogger pour Microsoft Edge - Visual Studio Marketplace"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://aka.ms/elements4code "Éléments pour Microsoft Edge \(Chromium\) - Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://aka.ms/webhint4code "webhint - Visual Studio Marketplace"

[TrackingPrevention]: https://aka.ms/microsoftedge/tracking-prevention-blog "Amélioration de la prévention du suivi dans le billet de blog de Microsoft Edge"

[MicrosoftEdgeInsiderAddons]: https://aka.ms/webhint/edge-extension "Microsoft Edge Insider Addons"  
[MicrosoftVisualStudioDownloads]: https://aka.ms/vs/download "Télécharger Visual Studio 2019 pour Windows & Mac"  

[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Publier un tweet"  

[CR924693]: https://crbug.com/924693 "Demande de fonctionnalité : ajouter Le G4 à la liste des modes d’appareil | Bogues Chromium"  
[CR1030258]: https://crbug.com/1030258 "Cr 1030258 | Bogues Chromium"  
[CR1026879]: https://crbug.com/1026879 "L’onglet Cookie de la console dev n’affiche plus la priorité | Bogues Chromium"  
[CR1029826]: https://crbug.com/1029826 "onglet réseau -> choisir de demander -> copie -> copie, car l’extraction ne copie pas les cookies | Bogues Chromium"  
[CR985402]: https://crbug.com/985402 "Les chaînes d’erreur d’icône de manifeste d’application web | Bogues Chromium"  
[CR963183]: https://crbug.com/963183 "DevTools ne sont pas conformes WCAG | Bogues Chromium"  
[CR941561]: https://crbug.com/941561 "Localisabilité de l'| Bogues Chromium"  
[CR987787]: https://crbug.com/987787 "Vue Dom 3D | Bogues Chromium"  

[CSSContentDemo]: https://mathiasbynens.github.io/css-dbg-stories/css-escapes.html "Démonstration du contenu CSS sans paysage"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Nouveau problème : MicrosoftDocs/edge-developer"  

[TheWebWeWant]: https://aka.ms/webwewant "Le site web que nous voulons"  
[AccessibilityInsights]: https://aka.ms/a11yinsights "Informations sur l’accessibilité"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Modèle objet de document (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "z-index | MDN"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools compte Twitter"  

[Webhint]: https://aka.ms/webhint "webhint"  

[WebhintBrowserExtension]: https://aka.ms/webhint/browser-extension "Webhint Browser Extension | documentation webhint"  
[WebhintVisualStudioCodeExtension]: https://aka.ms/webhint/code-extension "Webhint Visual Studio extension de code | documentation webhint"  

> [!NOTE]
> <span data-ttu-id="a5c99-285">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a5c99-285">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="a5c99-286">La page d’origine est disponible [ici](https://developers.google.com/web/updates/2020/01/devtools/index) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="a5c99-286">The original page is found [here](https://developers.google.com/web/updates/2020/01/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="a5c99-288">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a5c99-288">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  