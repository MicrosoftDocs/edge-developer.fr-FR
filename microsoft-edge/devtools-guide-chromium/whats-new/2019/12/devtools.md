---
description: Améliorations en matière d’accessibilité, utilisation de DevTools dans d’autres langues, et bien plus encore.
title: Nouveautés de DevTools (Microsoft Edge 80)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 7758b7f8ed55bb766abc56d6dd29ec124617e7ff
ms.sourcegitcommit: e29cd1c393fc1f433dba8c3d8f260b425ade63a9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/13/2021
ms.locfileid: "11408310"
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
# <a name="whats-new-in-devtools-microsoft-edge-80"></a><span data-ttu-id="2bb90-104">Nouveautés de DevTools (Microsoft Edge 80)</span><span class="sxs-lookup"><span data-stu-id="2bb90-104">What's new in DevTools (Microsoft Edge 80)</span></span>  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a><span data-ttu-id="2bb90-105">Annonces de l’équipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="2bb90-105">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="2bb90-106">Les sections suivantes sont une liste des annonces que vous avez peut-être manquées de l’équipe Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="2bb90-106">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team.</span></span>  <span data-ttu-id="2bb90-107">Consultez les annonces pour essayer de nouvelles fonctionnalités des extensions DevTools, Microsoft Visual Studio Code, etc.</span><span class="sxs-lookup"><span data-stu-id="2bb90-107">Check out the announcements to try new features in the DevTools, Microsoft Visual Studio Code extensions, and more.</span></span>  <span data-ttu-id="2bb90-108">Pour rester à jour sur toutes les fonctionnalités les plus récentes et les plus importantes de vos outils de développement, téléchargez les canaux d’aperçu [Microsoft Edge][MicrosoftEdgePreviewChannels] et [suivez-nous sur Twitter.][EdgeDevToolsTwitterAccount]</span><span class="sxs-lookup"><span data-stu-id="2bb90-108">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <a name="accessibility-improvements-to-the-devtools"></a><span data-ttu-id="2bb90-109">Améliorations de l’accessibilité de DevTools</span><span class="sxs-lookup"><span data-stu-id="2bb90-109">Accessibility improvements to the DevTools</span></span>  

<span data-ttu-id="2bb90-110">L’équipe DevTools a apporté 170 modifications à Chromium pour résoudre les problèmes de contraste de couleur, de clavier et de lecteur d’écran à fort impact dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="2bb90-110">The DevTools team has contributed 170 changes to Chromium to address high-impact color contrast, keyboard, and screen reader issues in the DevTools.</span></span>  <span data-ttu-id="2bb90-111">Chaque développeur qui construit le web doit être en mesure d’utiliser DevTools.</span><span class="sxs-lookup"><span data-stu-id="2bb90-111">Every developer building the web should be able to use the DevTools.</span></span>  

:::image type="complex" source="../../images/2019/12/a11y-performance-tool.msft.gif" alt-text="L’outil Performances dans DevTools avec les améliorations apportées à la navigation au clavier et au lecteur d’écran" lightbox="../../images/2019/12/a11y-performance-tool.msft.gif":::
   <span data-ttu-id="2bb90-113">**L’outil Performances** dans DevTools avec les améliorations apportées à la navigation au clavier et au lecteur d’écran</span><span class="sxs-lookup"><span data-stu-id="2bb90-113">The **Performance** tool in the DevTools with the keyboard navigation and screen reader improvements</span></span>  
:::image-end:::  

<span data-ttu-id="2bb90-114">Vous souhaitez découvrir comment rendre votre page web accessible à tous vos utilisateurs ?</span><span class="sxs-lookup"><span data-stu-id="2bb90-114">Want to learn how to make your web page accessible to all of your users?</span></span>  <span data-ttu-id="2bb90-115">Téléchargez [les informations sur l’accessibilité][AccessibilityInsights] et les extensions web [pour][WebhintBrowserExtension] que Microsoft Edge commence.</span><span class="sxs-lookup"><span data-stu-id="2bb90-115">Download the [Accessibility Insights][AccessibilityInsights] and [webhint][WebhintBrowserExtension] extensions for Microsoft Edge to get started.</span></span>  

<span data-ttu-id="2bb90-116">Si vous utilisez des lecteurs d’écran ou le clavier pour naviguer dans DevTools, envoyez vos commentaires en nous faisant un [tweet][PostTweetEdgeDevTools] ou en criant l’icône Envoyer [des](#getting-in-touch-with-microsoft-edge-devtools-team) commentaires !</span><span class="sxs-lookup"><span data-stu-id="2bb90-116">If you use screen readers or the keyboard to navigate around the DevTools, send your feedback by [tweeting][PostTweetEdgeDevTools] at us orchoosing the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="2bb90-117">Problème de chrome [#963183][CR963183]</span><span class="sxs-lookup"><span data-stu-id="2bb90-117">Chromium issue [#963183][CR963183]</span></span>  

### <a name="using-the-devtools-in-other-languages"></a><span data-ttu-id="2bb90-118">Utilisation de DevTools dans d’autres langues</span><span class="sxs-lookup"><span data-stu-id="2bb90-118">Using the DevTools in other languages</span></span>  

<span data-ttu-id="2bb90-119">De nombreux développeurs utilisent d’autres outils de développement, tels que StackOverflow et Visual Studio Code, dans leur langue native, et pas seulement en anglais.</span><span class="sxs-lookup"><span data-stu-id="2bb90-119">Many developers use other developer tools, like StackOverflow and Visual Studio Code, in their native language, not just in English.</span></span>  <span data-ttu-id="2bb90-120">Nous sommes ravis d’annoncer la localisation de DevTools, que vous pouvez désormais utiliser dans l’une des 10 langues en plus de l’anglais :</span><span class="sxs-lookup"><span data-stu-id="2bb90-120">We’re excited to announce localization for the DevTools, which you are now able to use in one of 10 languages besides English:</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="2bb90-121">Chinois \(Simplifié\) - &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span><span class="sxs-lookup"><span data-stu-id="2bb90-121">Chinese \(Simplified\) - &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="2bb90-122">Chinois \(Traditionnel\) - &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span><span class="sxs-lookup"><span data-stu-id="2bb90-122">Chinese \(Traditional\) - &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="2bb90-123">Français –&#231;ais</span><span class="sxs-lookup"><span data-stu-id="2bb90-123">French – fran&#231;ais</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="2bb90-124">Allemand - deu deutsche</span><span class="sxs-lookup"><span data-stu-id="2bb90-124">German - deutsch</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="2bb90-125">Italien - italiano</span><span class="sxs-lookup"><span data-stu-id="2bb90-125">Italian - italiano</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="2bb90-126">Japonais - &#26085;&#26412;&#35486;</span><span class="sxs-lookup"><span data-stu-id="2bb90-126">Japanese - &#26085;&#26412;&#35486;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="2bb90-127">Coréen - &#54620;&#44397;&#50612;</span><span class="sxs-lookup"><span data-stu-id="2bb90-127">Korean - &#54620;&#44397;&#50612;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="2bb90-128">Portugais - portugu&#234;s</span><span class="sxs-lookup"><span data-stu-id="2bb90-128">Portuguese - portugu&#234;s</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="2bb90-129">Russe – &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span><span class="sxs-lookup"><span data-stu-id="2bb90-129">Russian – &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="2bb90-130">Espagnol - espa&#241;ol</span><span class="sxs-lookup"><span data-stu-id="2bb90-130">Spanish - espa&#241;ol</span></span>
   :::column-end:::
:::row-end:::

<!--  
|  |  |  
|:--- |:--- |  
| Chinese (Simplified) - 中文（简体）| Chinese (Traditional) - 中文（繁體）|  
| French – français | German - deutsch |  
| Italian - italiano | Portuguese - português |  
| Korean - 한국어 | Japanese - 日本語 |  
| Russian – русский | Spanish - español |  
-->  

<span data-ttu-id="2bb90-131">Accédez à l’indicateur Activer les outils de développement localisées et `edge://flags` définissez-le **sur Activé.** </span><span class="sxs-lookup"><span data-stu-id="2bb90-131">Navigate to `edge://flags` and set the **Enable localized Developer Tools** flag to **Enabled**.</span></span>  <span data-ttu-id="2bb90-132">Définissez également **l’indicateur d’expériences Outils** de développement **sur Activé.**</span><span class="sxs-lookup"><span data-stu-id="2bb90-132">Also set the **Developer Tools experiments** flag to **Enabled**.</span></span>  <span data-ttu-id="2bb90-133">Redémarrez Microsoft Edge et ouvrez DevTools.</span><span class="sxs-lookup"><span data-stu-id="2bb90-133">Restart Microsoft Edge and open the DevTools.</span></span>  <!-- Select `F1` in the DevTools or navigate to Settings > Experiments and check the **Match browser language** checkbox.  -->  <span data-ttu-id="2bb90-134">Les DevTools correspondent à la langue que vous utilisez pour Microsoft Edge dans `edge://settings/languages` .</span><span class="sxs-lookup"><span data-stu-id="2bb90-134">The DevTools match the language you use for Microsoft Edge in `edge://settings/languages`.</span></span>  

:::image type="complex" source="../../images/2019/12/localized-devtools.msft.png" alt-text="DevTools en allemand" lightbox="../../images/2019/12/localized-devtools.msft.png":::
   <span data-ttu-id="2bb90-136">DevTools en allemand</span><span class="sxs-lookup"><span data-stu-id="2bb90-136">The DevTools in German</span></span>  
:::image-end:::  

<span data-ttu-id="2bb90-137">Si vous souhaitez utiliser les DevTools dans une autre langue que celles [disponibles,][PostTweetEdgeDevTools] tweetez-nous ou sélectionnez l’icône Envoyer [des](#getting-in-touch-with-microsoft-edge-devtools-team) commentaires.</span><span class="sxs-lookup"><span data-stu-id="2bb90-137">If you want to use the DevTools in a different language than the ones that are available, [tweet][PostTweetEdgeDevTools] at us or choose the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon.</span></span>  

<span data-ttu-id="2bb90-138">Problème de chrome [#941561][CR941561]</span><span class="sxs-lookup"><span data-stu-id="2bb90-138">Chromium issue [#941561][CR941561]</span></span>  

### <a name="webhint-microsoft-edge-extension"></a><span data-ttu-id="2bb90-139">extension Webhint Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2bb90-139">webhint Microsoft Edge extension</span></span>  

<span data-ttu-id="2bb90-140">L’extension Microsoft Edge webhint vous permet d’analyser facilement votre page web et d’obtenir des commentaires sur l’accessibilité, la compatibilité du navigateur, la sécurité, les performances et bien plus encore dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="2bb90-140">The webhint Microsoft Edge extension allows you to easily scan your web page and get feedback on accessibility, browser compatibility, security, performance, and more within the DevTools.</span></span>  <span data-ttu-id="2bb90-141">Pour plus d’informations, [https://webhint.io][Webhint] voir .</span><span class="sxs-lookup"><span data-stu-id="2bb90-141">Read more at [https://webhint.io][Webhint].</span></span>  

:::image type="complex" source="../../images/2019/12/webhint-browser-extension.msft.png" alt-text="Outil Hints dans DevTools lors de l’installation de l’extension de navigateur webhint" lightbox="../../images/2019/12/webhint-browser-extension.msft.png":::
   <span data-ttu-id="2bb90-143">Outil **Hints** dans DevTools lors de l’installation de l’extension de navigateur webhint</span><span class="sxs-lookup"><span data-stu-id="2bb90-143">The **Hints** tool in the DevTools when the webhint browser extension is installed</span></span>  
:::image-end:::  

<span data-ttu-id="2bb90-144">[Essayez l’extension de navigateur webhint dans Microsoft Edge.][MicrosoftEdgeInsiderAddons]</span><span class="sxs-lookup"><span data-stu-id="2bb90-144">[Try the webhint browser extension in Microsoft Edge][MicrosoftEdgeInsiderAddons].</span></span>  <span data-ttu-id="2bb90-145">Une fois l’extension installée, ouvrez DevTools et choisissez **l’outil Hints.**</span><span class="sxs-lookup"><span data-stu-id="2bb90-145">Once you install the extension, open the DevTools and choose the **Hints** tool.</span></span>  <span data-ttu-id="2bb90-146">À partir de là, exécutez une analyse de site personnalisable.</span><span class="sxs-lookup"><span data-stu-id="2bb90-146">From here, run a customizable site scan.</span></span>  <span data-ttu-id="2bb90-147">Pour en savoir [plus, webhint.io][WebhintBrowserExtension] plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="2bb90-147">Head over to [webhint.io][WebhintBrowserExtension] to learn more.</span></span>

### <a name="3d-view"></a><span data-ttu-id="2bb90-148">Vue 3D</span><span class="sxs-lookup"><span data-stu-id="2bb90-148">3D View</span></span>  

<span data-ttu-id="2bb90-149">Utilisez la vue **3D** pour déboguer votre application web en naviguant dans le modèle objet de document [\(DOM\)][MDNDocumentObjectModel] ou le contexte d’empilement [d’index z.][MDNZIndex]</span><span class="sxs-lookup"><span data-stu-id="2bb90-149">Use the **3D View** to debug your web application by navigating through the [Document Object Model \(DOM\)][MDNDocumentObjectModel] or the [z-index][MDNZIndex] stacking context.</span></span>  

:::image type="complex" source="../../images/2019/12/3dview.msft.png" alt-text="Affichage 3D dans devTools" lightbox="../../images/2019/12/3dview.msft.png":::
   <span data-ttu-id="2bb90-151">Affichage **3D** dans devTools</span><span class="sxs-lookup"><span data-stu-id="2bb90-151">The **3D View** in the DevTools</span></span>  
:::image-end:::  

<span data-ttu-id="2bb90-152">Pour accéder à la vue 3D, accédez à l’indicateur d’expériences Outils de développement et assurez-vous qu’il `edge://flags` est activé.  </span><span class="sxs-lookup"><span data-stu-id="2bb90-152">To access the 3D View, navigate to `edge://flags` and ensure that the **Developer Tools experiments** flag is set to **Enabled**.</span></span>  <span data-ttu-id="2bb90-153">Redémarrez Microsoft Edge et ouvrez DevTools.</span><span class="sxs-lookup"><span data-stu-id="2bb90-153">Restart Microsoft Edge and open the DevTools.</span></span>  <span data-ttu-id="2bb90-154">Sélectionnez dans DevTools ou ouvrez la section Expériences de `F1` **paramètres,** puis activez la case à cocher Activer l’affichage  >   **3D.**</span><span class="sxs-lookup"><span data-stu-id="2bb90-154">Select `F1` in the DevTools or open the **Settings** > **Experiments** section, and turn on the **Enable 3D View** checkbox.</span></span>  <span data-ttu-id="2bb90-155">Maintenant, `Ctrl`  +  `Shift`  +  `P` sélectionnez , tapez **en mode 3D et** **sélectionnez Afficher la vue 3D**.</span><span class="sxs-lookup"><span data-stu-id="2bb90-155">Now, select `Ctrl` + `Shift` + `P`, type in **3D View** and select **Show 3D View**.</span></span>  

<span data-ttu-id="2bb90-156">Nous travaillons sur l’interface utilisateur et ajoutons des fonctionnalités à l’affichage 3D. Veuillez donc nous envoyer vos [commentaires.](#getting-in-touch-with-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="2bb90-156">We're working on the UI and adding more functionality to the 3D View so please send us your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team).</span></span>  

<span data-ttu-id="2bb90-157">Problème de chrome [#987787][CR987787]</span><span class="sxs-lookup"><span data-stu-id="2bb90-157">Chromium issue [#987787][CR987787]</span></span>

### <a name="visual-studio-code-extensions"></a><span data-ttu-id="2bb90-158">Visual Studio extensions de code</span><span class="sxs-lookup"><span data-stu-id="2bb90-158">Visual Studio Code extensions</span></span>  

<span data-ttu-id="2bb90-159">L’équipe DevTools a également publié certaines extensions pour [Visual Studio Code][VisualStudioCode] qui vous permet d’utiliser la puissance de DevTools directement à partir de votre éditeur de texte.</span><span class="sxs-lookup"><span data-stu-id="2bb90-159">The DevTools team has also released some extensions for [Visual Studio Code][VisualStudioCode] that let you use the power of the DevTools directly from your text editor.</span></span> <span data-ttu-id="2bb90-160">Consultez les extensions suivantes.</span><span class="sxs-lookup"><span data-stu-id="2bb90-160">Check out the following extensions.</span></span>  

#### <a name="elements-for-microsoft-edge"></a><span data-ttu-id="2bb90-161">Éléments pour Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2bb90-161">Elements for Microsoft Edge</span></span>  

<span data-ttu-id="2bb90-162">Utilisez l’outil Elements à partir Visual Studio Code en ajoutant l’extension de code éléments pour [Microsoft Edge (Chromium)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] Visual Studio code.</span><span class="sxs-lookup"><span data-stu-id="2bb90-162">Use the Elements tool from within Visual Studio Code by adding the [Elements for Microsoft Edge (Chromium)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] Visual Studio Code extension.</span></span>  

:::image type="complex" source="../../images/2019/12/elements-for-edge.msft.png" alt-text="L’outil Elements dans Visual Studio Code à l’aide de l’extension Elements pour Microsoft Edge" lightbox="../../images/2019/12/elements-for-edge.msft.png":::
   <span data-ttu-id="2bb90-164">**L’outil Elements** dans Visual Studio Code à l’aide de l’extension Elements pour Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2bb90-164">The **Elements** tool in Visual Studio Code using the Elements for Microsoft Edge extension</span></span>  
:::image-end:::  

<span data-ttu-id="2bb90-165">Pour plus d’informations, consultez [Éléments pour l’extension][VisualStudioCodeElementEdgeExtension]de code Visual Studio Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2bb90-165">For more information, check out [Elements for Microsoft Edge Visual Studio Code extension][VisualStudioCodeElementEdgeExtension].</span></span>  

#### <a name="debugger-for-microsoft-edge"></a><span data-ttu-id="2bb90-166">Débogger pour Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2bb90-166">Debugger for Microsoft Edge</span></span>  

<span data-ttu-id="2bb90-167">Avec le [déboguer pour l’extension][VisualStudioMarketplaceDebuggerEdge] de code Visual Studio Microsoft Edge, déboguer JavaScript en cours d’exécution dans Microsoft Edge directement à partir Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="2bb90-167">With the [Debugger for Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] Visual Studio Code extension, debug JavaScript running in Microsoft Edge directly from Visual Studio Code.</span></span>  

:::image type="complex" source="../../images/2019/12/vscode-debugger.msft.png" alt-text="Débogger pour l’extension Microsoft Edge dans Visual Studio Code" lightbox="../../images/2019/12/vscode-debugger.msft.png":::
   <span data-ttu-id="2bb90-169">Débogger pour l’extension Microsoft Edge dans Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="2bb90-169">The Debugger for Microsoft Edge Extension in Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="2bb90-170">Pour plus d’informations, [découvrez comment déboguer Microsoft Edge][VisualStudioCodeDebuggerEdgeExtension]à partir de Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="2bb90-170">For more information, check out [how to debug Microsoft Edge from Visual Studio Code][VisualStudioCodeDebuggerEdgeExtension].</span></span>  

#### <a name="webhint"></a><span data-ttu-id="2bb90-171">webhint</span><span class="sxs-lookup"><span data-stu-id="2bb90-171">webhint</span></span>  

<span data-ttu-id="2bb90-172">[L’extension de Visual Studio][VisualStudioMarketplaceWebhintExtension] web utilise l’extension de code pour améliorer votre page web pendant que vous `webhint` l’écrivez !</span><span class="sxs-lookup"><span data-stu-id="2bb90-172">The [webhint][VisualStudioMarketplaceWebhintExtension] Visual Studio Code extension uses `webhint` to improve your web page while you're writing it!</span></span> <span data-ttu-id="2bb90-173">Cette extension s’exécute et signale les diagnostics sur vos fichiers d’espace de travail en fonction de `webhint` l’analyse.</span><span class="sxs-lookup"><span data-stu-id="2bb90-173">This extension runs and reports diagnostics on your workspace files based on `webhint` analysis.</span></span>  

:::image type="complex" source="../../images/2019/12/webhint-vscode-extension.msft.png" alt-text="The webhint Visual Studio Code extension analyzing a .tsx file in Visual Studio Code" lightbox="../../images/2019/12/webhint-vscode-extension.msft.png":::
   <span data-ttu-id="2bb90-175">La Visual Studio l’extension de code qui analyse un `.tsx` fichier dans Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="2bb90-175">The webhint Visual Studio Code extension analyzing a `.tsx` file in Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="2bb90-176">[En savoir plus sur l Visual Studio’extension web code.][WebhintVisualStudioCodeExtension]</span><span class="sxs-lookup"><span data-stu-id="2bb90-176">[Learn more about the Visual Studio Code webhint extension][WebhintVisualStudioCodeExtension].</span></span>  

### <a name="visual-studio-integration"></a><span data-ttu-id="2bb90-177">Visual Studio’intégration</span><span class="sxs-lookup"><span data-stu-id="2bb90-177">Visual Studio integration</span></span>  

<span data-ttu-id="2bb90-178">Dans Visual Studio version 2019 16.2 ou ultérieure, utilisez le déboguer Visual Studio déboguer JavaScript en cours d’exécution dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2bb90-178">In Visual Studio 2019 version 16.2 or later, use the Visual Studio debugger to debug JavaScript running in Microsoft Edge.</span></span>  <span data-ttu-id="2bb90-179">[Téléchargez Visual Studio 2019][MicrosoftVisualStudioDownloads] pour tester cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="2bb90-179">[Download Visual Studio 2019][MicrosoftVisualStudioDownloads] to try this feature out.</span></span>  

:::image type="complex" source="../../images/2019/12/vs.msft.png" alt-text="Visual Studio avec la possibilité de lancer votre application web dans Microsoft Edge Canary, Dev ou Beta" lightbox="../../images/2019/12/vs.msft.png":::
   <span data-ttu-id="2bb90-181">Visual Studio avec la possibilité de lancer votre application web dans Microsoft Edge Canary, Dev ou Beta</span><span class="sxs-lookup"><span data-stu-id="2bb90-181">Visual Studio with the option to launch your web app in Microsoft Edge Canary, Dev, or Beta</span></span>  
:::image-end:::  

<span data-ttu-id="2bb90-182">[Lisez notre billet de blog pour découvrir comment déboguer Microsoft Edge à partir de Visual Studio][MicrosoftVisualStudioBlogDebugJavascript].</span><span class="sxs-lookup"><span data-stu-id="2bb90-182">[Read our blog post to learn how to debug Microsoft Edge from Visual Studio][MicrosoftVisualStudioBlogDebugJavascript].</span></span>  

### <a name="tracking-prevention-console-messages"></a><span data-ttu-id="2bb90-183">Suivi des messages de la console de prévention</span><span class="sxs-lookup"><span data-stu-id="2bb90-183">Tracking prevention Console messages</span></span>  

<span data-ttu-id="2bb90-184">La prévention du suivi est une fonctionnalité unique de Microsoft Edge qui vous empêche d’être suivi par un site web avant de le visiter.</span><span class="sxs-lookup"><span data-stu-id="2bb90-184">Tracking prevention is a unique feature in Microsoft Edge that blocks you from being tracked by a website before you visited it.</span></span>  <span data-ttu-id="2bb90-185">Le paramètre de prévention du suivi par défaut est le mode équilibré, qui bloque les suivis tiers et les suivis malveillants connus pour une expérience qui équilibre la confidentialité et la compatibilité web.</span><span class="sxs-lookup"><span data-stu-id="2bb90-185">The default tracking prevention setting is Balanced mode, which blocks 3rd party trackers and known malicious trackers for an experience that balances privacy and web compatibility.</span></span>  <span data-ttu-id="2bb90-186">Pour vous donner plus d’informations sur la compatibilité de votre page web lorsque certains suivis sont bloqués, l’équipe Microsoft Edge a ajouté des messages d’avertissement dans la **console** lorsqu’un suivi est bloqué.</span><span class="sxs-lookup"><span data-stu-id="2bb90-186">To give you more insight into the compatibility of your web page when certain trackers are blocked, The Microsoft Edge team added warning messages in the **Console** when a tracker is blocked.</span></span>  

:::image type="complex" source="../../images/2019/12/tracking-prevention.msft.png" alt-text="Messages dans la console lorsque la prévention du suivi bloque l’accès au stockage pour un suivi" lightbox="../../images/2019/12/tracking-prevention.msft.png":::
   <span data-ttu-id="2bb90-188">Messages dans la **console lorsque la prévention** du suivi bloque l’accès au stockage pour un suivi</span><span class="sxs-lookup"><span data-stu-id="2bb90-188">Messages in the **Console** when tracking prevention blocks access to storage for a tracker</span></span>  
:::image-end:::  

<span data-ttu-id="2bb90-189">[En savoir plus sur la prévention du suivi et l’équilibre entre la confidentialité et la compatibilité web.][TrackingPrevention]</span><span class="sxs-lookup"><span data-stu-id="2bb90-189">[Read more about tracking prevention and the balance between privacy and web compatibility][TrackingPrevention].</span></span>  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="2bb90-190">Annonces du projet de Chromium</span><span class="sxs-lookup"><span data-stu-id="2bb90-190">Announcements from the Chromium project</span></span>  

<span data-ttu-id="2bb90-191">Les sections suivantes annoncent des fonctionnalités supplémentaires disponibles dans Microsoft Edge 80 qui ont été contribués au projet open source Chromium.</span><span class="sxs-lookup"><span data-stu-id="2bb90-191">The following sections announce additional features available in Microsoft Edge 80 that were contributed to the open source Chromium project.</span></span>  

### <a name="support-for-let-and-class-redeclarations-in-the-console"></a><span data-ttu-id="2bb90-192">Prise en charge des redéclarations de classes et de let dans la console</span><span class="sxs-lookup"><span data-stu-id="2bb90-192">Support for let and class redeclarations in the Console</span></span>  

<span data-ttu-id="2bb90-193">La **console prend** désormais en charge les déclarations et les `let` `class` instructions.</span><span class="sxs-lookup"><span data-stu-id="2bb90-193">The **Console** now supports redeclarations of `let` and `class` statements.</span></span>  <span data-ttu-id="2bb90-194">L’incapacité à redéclarer était une gêne courante pour les développeurs web qui utilisent la console pour expérimenter du nouveau code JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2bb90-194">The inability to redeclare was a common annoyance for web developers who use the Console to experiment with new JavaScript code.</span></span>  

> [!WARNING]
> <span data-ttu-id="2bb90-195">La déclaration d’une `let` ou `class` d’une instruction dans un script en dehors de la console ou au sein d’une seule entrée de console provoque toujours une `SyntaxError` .</span><span class="sxs-lookup"><span data-stu-id="2bb90-195">Redeclaring a `let` or `class` statement in a script outside of the Console or within a single Console input still causes a `SyntaxError`.</span></span>  

<span data-ttu-id="2bb90-196">Par exemple, précédemment, lors de la nouvelle déclaration d’une variable locale avec `let` , la console a lancé une erreur :</span><span class="sxs-lookup"><span data-stu-id="2bb90-196">For example, previously, when re-declaring a local variable with `let`, the Console threw an error:</span></span>  

:::image type="complex" source="../../images/2019/12/letbefore.msft.png" alt-text="Console dans Microsoft Edge 79 indiquant que la déclaration d’échec de la déclaration" lightbox="../../images/2019/12/letbefore.msft.png":::
   <span data-ttu-id="2bb90-198">Console **dans** Microsoft Edge 79 indiquant que la nouvelle déclaration échoue</span><span class="sxs-lookup"><span data-stu-id="2bb90-198">The **Console** in Microsoft Edge 79 showing that the let re-declaration fails</span></span>  
:::image-end:::  

<span data-ttu-id="2bb90-199">À présent, la console autorise la déclaration :</span><span class="sxs-lookup"><span data-stu-id="2bb90-199">Now, the Console allows the redeclaration:</span></span>  

:::image type="complex" source="../../images/2019/12/letafter.msft.png" alt-text="Console dans Microsoft Edge 80 indiquant que la redéclaration a réussi" lightbox="../../images/2019/12/letafter.msft.png":::
   <span data-ttu-id="2bb90-201">Console **dans** Microsoft Edge 80 indiquant que la nouvelle déclaration réussit</span><span class="sxs-lookup"><span data-stu-id="2bb90-201">The **Console** in Microsoft Edge 80 showing that the let re-declaration succeeds</span></span>  
:::image-end:::  

<span data-ttu-id="2bb90-202">Problème de chrome [#1004193][CR1004193]</span><span class="sxs-lookup"><span data-stu-id="2bb90-202">Chromium issue [#1004193][CR1004193]</span></span>  

### <a name="improved-webassembly-debugging"></a><span data-ttu-id="2bb90-203">Débogage WebAssembly amélioré</span><span class="sxs-lookup"><span data-stu-id="2bb90-203">Improved WebAssembly debugging</span></span>  

<span data-ttu-id="2bb90-204">DevTools a commencé à prendre en charge la norme DE DÉBOGAGE [DNS,][DwarfHome]ce qui signifie une prise en charge accrue du pas à pas sur le code, de la définition de points d’arrêt et de la résolution des traces de pile dans vos langues sources dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="2bb90-204">DevTools has started to support the [DWARF Debugging Standard][DwarfHome], which means increased support for stepping over code, setting breakpoints, and resolving stack traces in your source languages within DevTools.</span></span>  

<!-- [TODO: Add this link back] -->  
<!--Check out [Improved WebAssembly debugging in Microsoft Edge DevTools][201912Webassembly] for the full story.  -->  

<!-- [TODO: Replace this image with screenshot in Edge] -->  
<!--
:::image type="complex" source="../../images/2019/12/wasm.msft.png" alt-text="The new DWARF-powered WebAssembly debugging" lightbox="../../images/2019/12/wasm.msft.png":::
   The new DWARF-powered WebAssembly debugging  
:::image-end:::  
-->  

### <a name="network-panel-updates"></a><span data-ttu-id="2bb90-205">Mises à jour du panneau réseau</span><span class="sxs-lookup"><span data-stu-id="2bb90-205">Network panel updates</span></span>  

#### <a name="request-initiator-chains-in-the-initiator-panel"></a><span data-ttu-id="2bb90-206">Chaînes d’initiateur de demande dans le panneau Initiateur</span><span class="sxs-lookup"><span data-stu-id="2bb90-206">Request Initiator Chains in the Initiator panel</span></span>  

<span data-ttu-id="2bb90-207">Vous pouvez désormais afficher les initiateurs et les dépendances d’une demande réseau en tant que liste imbriée.</span><span class="sxs-lookup"><span data-stu-id="2bb90-207">You are now able to view the initiators and dependencies of a network request as a nested list.</span></span>  <span data-ttu-id="2bb90-208">Cela peut vous aider à comprendre pourquoi une ressource a été demandée ou l’activité réseau qu’une certaine ressource \(par exemple, un script\) a provoqué.</span><span class="sxs-lookup"><span data-stu-id="2bb90-208">This may help you understand why a resource was requested, or what network activity a certain resource \(such as a script\) caused.</span></span>  

:::image type="complex" source="../../images/2019/12/initiators.msft.png" alt-text="Chaîne de l’initiateur de la demande dans le panneau Initiateur" lightbox="../../images/2019/12/initiators.msft.png":::
   <span data-ttu-id="2bb90-210">Chaîne de l’initiateur de la demande dans le **panneau Initiateur**</span><span class="sxs-lookup"><span data-stu-id="2bb90-210">A Request Initiator Chain in the **Initiator** panel</span></span>  
:::image-end:::  

<span data-ttu-id="2bb90-211">Après [avoir consigné l’activité][DevToolsNetworkIndex]réseau dans le  panneau Réseau, choisissez une ressource, puis accédez au panneau Initiateur pour afficher la chaîne de **l’initiateur de demande**:</span><span class="sxs-lookup"><span data-stu-id="2bb90-211">After [logging network activity in the Network panel][DevToolsNetworkIndex], choose a resource and then navigate to the **Initiator** panel to view the **Request Initiator Chain**:</span></span>  

*   <span data-ttu-id="2bb90-212">La **ressource inspectée est** en gras.</span><span class="sxs-lookup"><span data-stu-id="2bb90-212">The **inspected resource** is bold.</span></span>  <span data-ttu-id="2bb90-213">Dans la capture d’écran `ai.2.min.js` ci-dessus, se trouve la ressource inspectée.</span><span class="sxs-lookup"><span data-stu-id="2bb90-213">In the screenshot above, `ai.2.min.js` is the inspected resource.</span></span>  
*   <span data-ttu-id="2bb90-214">Les ressources au-dessus de la ressource inspectée sont **les initiateurs.**</span><span class="sxs-lookup"><span data-stu-id="2bb90-214">The resources above the inspected resource are the **initiators**.</span></span>  <span data-ttu-id="2bb90-215">Dans la capture d’écran `https://www.microsoftedgeinsider.com` ci-dessus, est l’initiateur de `ai.2.min.js` .</span><span class="sxs-lookup"><span data-stu-id="2bb90-215">In the screenshot above, `https://www.microsoftedgeinsider.com` is the initiator of `ai.2.min.js`.</span></span>  <span data-ttu-id="2bb90-216">En d’autres termes, `https://www.microsoftedgeinsider.com` a provoqué la demande réseau pour `ai.2.min.js` .</span><span class="sxs-lookup"><span data-stu-id="2bb90-216">In other words, `https://www.microsoftedgeinsider.com` caused the network request for `ai.2.min.js`.</span></span>  
*   <span data-ttu-id="2bb90-217">Les ressources sous la ressource inspectée sont **les dépendances.**</span><span class="sxs-lookup"><span data-stu-id="2bb90-217">The resources below the inspected resource are the **dependencies**.</span></span>  <span data-ttu-id="2bb90-218">Dans la capture d’écran `https://dc.services.visualstudio.com/v2/track` ci-dessus, est une dépendance de `ai.2.min.js` .</span><span class="sxs-lookup"><span data-stu-id="2bb90-218">In the screenshot above, `https://dc.services.visualstudio.com/v2/track` is a dependency of `ai.2.min.js`.</span></span>  <span data-ttu-id="2bb90-219">En d’autres termes, `ai.2.min.js` a provoqué la demande réseau pour `https://dc.services.visualstudio.com/v2/track` .</span><span class="sxs-lookup"><span data-stu-id="2bb90-219">In other words, `ai.2.min.js` caused the network request for `https://dc.services.visualstudio.com/v2/track`.</span></span>  

> [!NOTE]
> <span data-ttu-id="2bb90-220">Les informations d’initiateur et de dépendance peuvent également être accessibles en maintenant les ressources réseau en place, `Shift` puis en pointant dessus.</span><span class="sxs-lookup"><span data-stu-id="2bb90-220">Initiator and dependency information may also be accessed by holding `Shift` and then hovering over network resources.</span></span>  <span data-ttu-id="2bb90-221">Accédez à [Afficher les initiateurs et les dépendances.][DevToolsNetworkReferenceViewInitiatorsDependencies]</span><span class="sxs-lookup"><span data-stu-id="2bb90-221">Navigate to [View initiators and dependencies][DevToolsNetworkReferenceViewInitiatorsDependencies].</span></span>  

<span data-ttu-id="2bb90-222">Problème de chrome [#842488][CR842488]</span><span class="sxs-lookup"><span data-stu-id="2bb90-222">Chromium issue [#842488][CR842488]</span></span>  

#### <a name="highlight-the-selected-network-request-in-the-overview"></a><span data-ttu-id="2bb90-223">Mettre en évidence la demande réseau sélectionnée dans la vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="2bb90-223">Highlight the selected network request in the Overview</span></span>  

<span data-ttu-id="2bb90-224">Une fois que vous avez choisi une ressource réseau pour l’inspecter, le panneau Réseau place maintenant une bordure bleue autour de cette ressource dans la vue **d’ensemble.**</span><span class="sxs-lookup"><span data-stu-id="2bb90-224">After you choose a network resource in order to inspect it, the Network panel now puts a blue border around that resource in the **Overview**.</span></span>  <span data-ttu-id="2bb90-225">Cela vous permet de détecter si la demande réseau se produit plus tôt ou plus tard que prévu.</span><span class="sxs-lookup"><span data-stu-id="2bb90-225">This is able to help you detect if the network request is happening earlier or later than expected.</span></span>  

:::image type="complex" source="../../images/2019/12/overview.msft.png" alt-text="Volet Vue d’ensemble mettant en surbrillance la ressource inspectée" lightbox="../../images/2019/12/overview.msft.png":::
   <span data-ttu-id="2bb90-227">Volet **Vue d’ensemble** mettant en surbrillance la ressource inspectée</span><span class="sxs-lookup"><span data-stu-id="2bb90-227">The **Overview** pane highlighting the inspected resource</span></span>  
:::image-end:::  

<span data-ttu-id="2bb90-228">Problème de chrome [#988253][CR988253]</span><span class="sxs-lookup"><span data-stu-id="2bb90-228">Chromium issue [#988253][CR988253]</span></span>  

#### <a name="url-and-path-columns-in-the-network-panel"></a><span data-ttu-id="2bb90-229">Colonnes d’URL et de chemin d’accès dans le panneau Réseau</span><span class="sxs-lookup"><span data-stu-id="2bb90-229">URL and path columns in the Network panel</span></span>  

<span data-ttu-id="2bb90-230">Utilisez les nouvelles **colonnes**  Chemin d’accès et **URL** dans l’outil Réseau pour afficher le chemin d’accès absolu ou l’URL complète de chaque ressource réseau.</span><span class="sxs-lookup"><span data-stu-id="2bb90-230">Use the new **Path** and **URL** columns in the **Network** tool to display the absolute path or full URL of each network resource.</span></span>  

:::image type="complex" source="../../images/2019/12/columns.msft.png" alt-text="Les nouvelles colonnes Chemin d’accès et URL dans le panneau Réseau" lightbox="../../images/2019/12/columns.msft.png":::
   <span data-ttu-id="2bb90-232">Les nouvelles colonnes Chemin d’accès et URL dans **l’outil** Réseau</span><span class="sxs-lookup"><span data-stu-id="2bb90-232">The new Path and URL columns in the **Network** tool</span></span>  
:::image-end:::  

<span data-ttu-id="2bb90-233">Pour afficher les nouvelles colonnes, pointez sur l’en-tête du tableau **Cascade,** ouvrez le menu contextuel \(righ-click\), puis choisissez Chemin d’accès **ou** **URL.**</span><span class="sxs-lookup"><span data-stu-id="2bb90-233">To display the new columns, hover on the **Waterfall** table header, open the contextual menu \(righ-click\), and choose **Path** or **URL**.</span></span>  

<span data-ttu-id="2bb90-234">Problème de chrome [#993366][CR993366]</span><span class="sxs-lookup"><span data-stu-id="2bb90-234">Chromium issue [#993366][CR993366]</span></span>  

#### <a name="updated-user-agent-strings"></a><span data-ttu-id="2bb90-235">Mise à jour User-Agent chaînes</span><span class="sxs-lookup"><span data-stu-id="2bb90-235">Updated User-Agent strings</span></span>  

<span data-ttu-id="2bb90-236">DevTools prend en charge la définition d’une chaîne User-Agent personnalisée via le **panneau Conditions réseau.**</span><span class="sxs-lookup"><span data-stu-id="2bb90-236">DevTools supports setting a custom User-Agent string through the **Network Conditions** panel.</span></span>  <span data-ttu-id="2bb90-237">La User-Agent affecte l’en-tête HTTP attaché aux ressources réseau, ainsi que la `User-Agent` valeur de `navigator.userAgent` .</span><span class="sxs-lookup"><span data-stu-id="2bb90-237">The User-Agent string affects the `User-Agent` HTTP header attached to network resources, and also the value of `navigator.userAgent`.</span></span>  

<span data-ttu-id="2bb90-238">Les chaînes de User-Agent prédéfines ont été mises à jour pour refléter les versions modernes du navigateur.</span><span class="sxs-lookup"><span data-stu-id="2bb90-238">The predefined User-Agent strings have been updated to reflect modern browser versions.</span></span>  

:::image type="complex" source="../../images/2019/12/useragent.msft.png" alt-text="Menu Agent utilisateur dans le panneau Conditions réseau" lightbox="../../images/2019/12/useragent.msft.png":::
   <span data-ttu-id="2bb90-240">Menu Agent utilisateur dans le **panneau Conditions réseau**</span><span class="sxs-lookup"><span data-stu-id="2bb90-240">The User Agent menu in the **Network Conditions** panel</span></span>  
:::image-end:::  

<span data-ttu-id="2bb90-241">Pour accéder **aux conditions réseau,** [ouvrez le menu Commande][DevToolsCommandMenuIndex] et exécutez la `Show Network Conditions` commande.</span><span class="sxs-lookup"><span data-stu-id="2bb90-241">To access **Network Conditions**, [open the Command Menu][DevToolsCommandMenuIndex] and run the `Show Network Conditions` command.</span></span>  

> [!NOTE]
> <span data-ttu-id="2bb90-242">Vous pouvez également [définir User-Agent chaînes en mode appareil.][DevToolsDeviceModeIndex]</span><span class="sxs-lookup"><span data-stu-id="2bb90-242">You may also [set User-Agent strings in Device Mode][DevToolsDeviceModeIndex].</span></span>  

<span data-ttu-id="2bb90-243">Problème de chrome [#1029031][CR1029031]</span><span class="sxs-lookup"><span data-stu-id="2bb90-243">Chromium issue [#1029031][CR1029031]</span></span>  

### <a name="audits-panel-updates"></a><span data-ttu-id="2bb90-244">Audits panel updates</span><span class="sxs-lookup"><span data-stu-id="2bb90-244">Audits panel updates</span></span>  

#### <a name="new-configuration-ui"></a><span data-ttu-id="2bb90-245">Nouvelle interface utilisateur de configuration</span><span class="sxs-lookup"><span data-stu-id="2bb90-245">New configuration UI</span></span>  

<span data-ttu-id="2bb90-246">L’interface utilisateur de configuration a une nouvelle conception réactive et les options de configuration de limitation ont été simplifiées.</span><span class="sxs-lookup"><span data-stu-id="2bb90-246">The configuration UI has a new, responsive design, and the throttling configuration options have been simplified.</span></span>  <span data-ttu-id="2bb90-247">Pour plus d’informations sur les modifications apportées à l’interface utilisateur de limitation, accédez à Limitation du panneau [Audits.][GitHubGoogleChromeDevToolsAuditsPanelThrottling]</span><span class="sxs-lookup"><span data-stu-id="2bb90-247">For more information on the throttling UI changes, navigate to [Audits Panel Throttling][GitHubGoogleChromeDevToolsAuditsPanelThrottling].</span></span>  

:::image type="complex" source="../../images/2019/12/start.msft.png" alt-text="Nouvelle interface utilisateur de configuration" lightbox="../../images/2019/12/start.msft.png":::
   <span data-ttu-id="2bb90-249">Nouvelle interface utilisateur de configuration</span><span class="sxs-lookup"><span data-stu-id="2bb90-249">The new configuration UI</span></span>  
:::image-end:::  

### <a name="coverage-tool-updates"></a><span data-ttu-id="2bb90-250">Mises à jour de l’outil de couverture</span><span class="sxs-lookup"><span data-stu-id="2bb90-250">Coverage tool updates</span></span>  

#### <a name="per-function-or-per-block-coverage-modes"></a><span data-ttu-id="2bb90-251">Modes de couverture par fonction ou par bloc</span><span class="sxs-lookup"><span data-stu-id="2bb90-251">Per-function or per-block coverage modes</span></span>  

<span data-ttu-id="2bb90-252">[L’outil][DevToolsCoverageIndex] Couverture propose un nouveau menu déroulant qui vous permet de spécifier si les données de couverture de code doivent être collectées **par** fonction ou **par bloc.**</span><span class="sxs-lookup"><span data-stu-id="2bb90-252">The [Coverage][DevToolsCoverageIndex] tool has a new dropdown menu that lets you specify whether code coverage data should be collected **per function** or **per block**.</span></span>  <span data-ttu-id="2bb90-253">**La couverture** par bloc est plus détaillée, mais elle est également beaucoup plus coûteuse à collecter.</span><span class="sxs-lookup"><span data-stu-id="2bb90-253">**Per block** coverage is more detailed but also far more expensive to collect.</span></span>  <span data-ttu-id="2bb90-254">DevTools utilise désormais **la couverture par** fonction par défaut.</span><span class="sxs-lookup"><span data-stu-id="2bb90-254">DevTools uses **per function** coverage by default now.</span></span>  

> [!CAUTION]
> <span data-ttu-id="2bb90-255">Vous remarquerez peut-être des différences importantes de couverture de code dans les fichiers HTML selon que vous utilisez **par** fonction ou **par** mode bloc.</span><span class="sxs-lookup"><span data-stu-id="2bb90-255">You may notice large code coverage differences in HTML files depending on whether you use **per function** or **per block** mode.</span></span>  <span data-ttu-id="2bb90-256">Lors de **l’utilisation par** mode fonction, les scripts en ligne dans les fichiers HTML sont traités comme des fonctions.</span><span class="sxs-lookup"><span data-stu-id="2bb90-256">When using **per function** mode, inline scripts in HTML files are treated as functions.</span></span>  <span data-ttu-id="2bb90-257">Si le script s’exécute, DevTools marque l’intégralité du script en tant que code utilisé.</span><span class="sxs-lookup"><span data-stu-id="2bb90-257">If the script runs at all then DevTools marks the entire script as used code.</span></span>  <span data-ttu-id="2bb90-258">C’est seulement si le script ne s’exécute pas du tout que DevTools marque le script comme du code inutilisé.</span><span class="sxs-lookup"><span data-stu-id="2bb90-258">Only if the script does not run at all does DevTools mark the script as unused code.</span></span>  

:::image type="complex" source="../../images/2019/12/modes.msft.png" alt-text="Menu déroulant du mode couverture" lightbox="../../images/2019/12/modes.msft.png":::
   <span data-ttu-id="2bb90-260">Menu déroulant du mode couverture</span><span class="sxs-lookup"><span data-stu-id="2bb90-260">The coverage mode dropdown menu</span></span>  
:::image-end:::  

#### <a name="coverage-must-now-be-initiated-by-a-page-refresh"></a><span data-ttu-id="2bb90-261">La couverture doit maintenant être lancée par une actualisation de page</span><span class="sxs-lookup"><span data-stu-id="2bb90-261">Coverage must now be initiated by a page refresh</span></span>  

<span data-ttu-id="2bb90-262">Le basculement de la couverture de code sans actualisation de page a été supprimé car les données de couverture n’étaient pas fiables.</span><span class="sxs-lookup"><span data-stu-id="2bb90-262">Toggling code coverage without a page refresh has been removed because the coverage data was unreliable.</span></span>  <span data-ttu-id="2bb90-263">Par exemple, une fonction peut être signalée comme inutilisée si le runtime date d’il y a longtemps et si le garbage collector V8 l’a nettoyé.</span><span class="sxs-lookup"><span data-stu-id="2bb90-263">For example, a function may be reported as unused if the runtime was a long time ago and the V8 garbage collector has cleaned it up.</span></span>  

<span data-ttu-id="2bb90-264">Problème de chrome [#1004203][CR1004203]</span><span class="sxs-lookup"><span data-stu-id="2bb90-264">Chromium issue [#1004203][CR1004203]</span></span>  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="2bb90-265">Télécharger les canaux d’aperçu Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2bb90-265">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="2bb90-266">Si vous utilisez Windows ou macOS, envisagez d’utiliser les canaux d’aperçu [Microsoft Edge][MicrosoftEdgePreviewChannels] comme navigateur de développement par défaut.</span><span class="sxs-lookup"><span data-stu-id="2bb90-266">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="2bb90-267">Les canaux d’aperçu vous permettent d’accéder aux dernières fonctionnalités de DevTools.</span><span class="sxs-lookup"><span data-stu-id="2bb90-267">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="2bb90-268">Contacter l’équipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="2bb90-268">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- image links -->  

<!--[../../images/2019/12/wasm.msft.png]: ../../images/2019/12/wasm.msft.png "Figure: The new DWARF-powered WebAssembly debugging"  -->

<!-- links -->  

[DevToolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Exécuter des commandes avec le menu de commandes Microsoft Edge DevTools | Documents Microsoft"  
[DevToolsCoverageIndex]: /microsoft-edge/devtools-guide-chromium/coverage/index "Recherchez du code JavaScript et CSS inutilisé à l’aide de l’outil Couverture dans Microsoft Edge DevTools | Documents Microsoft"  
[DevToolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index#simulate-a-mobile-viewport "Simuler une port d’affichage mobile : simuler des appareils mobiles avec le mode appareil dans Microsoft Edge DevTools | Documents Microsoft"  
[DevToolsNetworkIndex]: /microsoft-edge/devtools-guide-chromium/network/index "Inspecter l’activité réseau dans microsoft Edge DevTools | Documents Microsoft"  
[DevToolsNetworkReferenceViewInitiatorsDependencies]: /microsoft-edge/devtools-guide-chromium/network/reference#view-initiators-and-dependencies "Afficher les initiateurs et les dépendances - Référence de l’analyse réseau | Documents Microsoft"  
[DevGuideEdgeHtmlWhatsNew]: /microsoft-edge/dev-guide/whats-new "Nouveautés de l'| EdgeHTML Documents Microsoft"  
[VisualStudioCodeDebuggerEdgeExtension]: /microsoft-edge/visual-studio-code/debugger-for-edge "Débogger pour l’extension de code Visual Studio Microsoft Edge | Documents Microsoft"  
[VisualStudioCodeElementEdgeExtension]: /microsoft-edge/visual-studio-code/elements-for-edge "Éléments de l’extension de code Visual Studio Microsoft Edge | Documents Microsoft"  

<!--  [201912Webassembly]: webassembly.md "Improved WebAssembly debugging in Microsoft Edge DevTools"  -->  

[CR842488]: https://crbug.com/842488 "Ajoutez le champ Initiateur à l’onglet En-têtes | Bogues Chromium"  
[CR988253]: https://crbug.com/988253 "Bug DevTools - Aucune association entre la demande réseau et le graphique de chronologie | Bogues Chromium"  
[CR993366]: https://crbug.com/993366 "Veuillez afficher la partie du chemin d’accès de l’URL dans les listes de demandes du panneau réseau | Bogues Chromium"  
[CR1004193]: https://crbug.com/1004193 "Mode REPL pour les | V8 Bogues Chromium"  
[CR1004203]: https://crbug.com/1004203 "Faire en sorte que la couverture de code soit | Bogues Chromium"  
[CR1029031]: https://crbug.com/1029031 "Les chaînes UA sont obsolètes | Bogues Chromium" 
[CR963183]: https://crbug.com/963183 "DevTools ne sont pas conformes WCAG | Bogues Chromium"
[CR941561]: https://crbug.com/941561 "Localisabilité du | DevTools Bogues Chromium"
[CR987787]: https://crbug.com/987787 "Vue Dom 3D | Bogues Chromium"

[AccessibilityInsights]: https://aka.ms/a11yinsights "Informations sur l’accessibilité"  

[DwarfHome]: https://dwarfstd.org "Accueil en maison de famille"  
[GitHubGoogleChromeDevToolsAuditsPanelThrottling]: https://github.com/GoogleChrome/lighthouse/blob/master/docs/throttling.md#devtools-audits-panel-throttling "Limitation du panneau Audits de DevTools - GoogleChrome/| GitHub"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Nouveau problème : MicrosoftDocs/edge-developer"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Canaux d’aperçu Microsoft Edge"  
[MicrosoftEdgeInsiderAddons]: https://aka.ms/webhint/edge-extension "Microsoft Edge Insider Addons"  
[MicrosoftVisualStudio]: https://aka.ms/vs "Visual Studio"  
[MicrosoftVisualStudioBlogDebugJavascript]: https://aka.ms/vs/debug-edge "Déboguer JavaScript dans Microsoft Edge à partir de Visual Studio | Visual Studio Blog"  
[MicrosoftVisualStudioDownloads]: https://aka.ms/vs/download "Télécharger Visual Studio 2019 pour Windows \& Mac"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Document Object Model (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "z-index | MDN"  
[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Publier un Tweet"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools compte Twitter"
[VisualStudioCode]: https://aka.ms/vscode "Visual Studio Code"  
[VisualStudioMarketplaceDebuggerEdge]: https://aka.ms/debugger4code "Débogger pour Microsoft Edge - Visual Studio Marketplace"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://aka.ms/elements4code "Éléments pour Microsoft Edge \(Chromium\) - Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://aka.ms/webhint4code "webhint - Visual Studio Marketplace"
[Webhint]: https://aka.ms/webhint "webhint"  
[WebhintBrowserExtension]: https://aka.ms/webhint/browser-extension "Webhint Browser Extension | documentation webhint"  
[WebhintVisualStudioCodeExtension]: https://aka.ms/webhint/code-extension "Webhint Visual Studio extension de code | documentation webhint"  
[TrackingPrevention]: https://aka.ms/microsoftedge/tracking-prevention-blog "Amélioration de la prévention du suivi dans le billet de blog de Microsoft Edge"
[TheWebWeWant]: https://aka.ms/webwewant "Le site Web de votre choix"

> [!NOTE]
> <span data-ttu-id="2bb90-308">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2bb90-308">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="2bb90-309">La page d’origine est disponible [ici](https://developers.google.com/web/updates/2019/12/devtools/index) et est créée par [Kayce Basques][KayceBasques] \(Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="2bb90-309">The original page is found [here](https://developers.google.com/web/updates/2019/12/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="2bb90-311">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2bb90-311">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
