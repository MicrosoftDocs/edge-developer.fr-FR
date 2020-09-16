---
description: Amélioration de l’accessibilité, utilisation du DevTools dans d’autres langues, etc.
title: Nouveautés de DevTools (Microsoft Edge 80)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 8f82f46cd683433a37614bcf15745e1de9f31ffb
ms.sourcegitcommit: b337717957529239434b4e8e1e167aebf0543518
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015467"
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

# <span data-ttu-id="b614b-104">Nouveautés de DevTools (Microsoft Edge 80)</span><span class="sxs-lookup"><span data-stu-id="b614b-104">What's new in DevTools (Microsoft Edge 80)</span></span>  

## <span data-ttu-id="b614b-105">Annonces de l’équipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="b614b-105">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="b614b-106">Les sections suivantes répertorient les annonces que vous pouvez avoir manquées de l’équipe Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="b614b-106">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team!</span></span> <span data-ttu-id="b614b-107">Découvrez-les pour essayer de nouvelles fonctionnalités dans le DevTools, les extensions de code Visual Studio, etc.</span><span class="sxs-lookup"><span data-stu-id="b614b-107">Check them out to try new features in the DevTools, Visual Studio Code extensions, and more.</span></span>  <span data-ttu-id="b614b-108">Pour vous tenir au courant de toutes les fonctionnalités les plus récentes et les plus récentes de vos outils de développement, téléchargez les [canaux Microsoft Edge Preview][MicrosoftEdgePreviewChannels] et [Suivez-nous sur Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="b614b-108">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <span data-ttu-id="b614b-109">Améliorations de l’accessibilité dans DevTools</span><span class="sxs-lookup"><span data-stu-id="b614b-109">Accessibility improvements to the DevTools</span></span>  

<span data-ttu-id="b614b-110">L’équipe DevTools a 170 contribué aux modifications apportées à Chrome pour répondre aux problèmes de contraste des couleurs, de clavier et de lecteur d’écran à forte incidence dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="b614b-110">The DevTools team has contributed 170 changes to Chromium to address high-impact color contrast, keyboard, and screen reader issues in the DevTools.</span></span>  <span data-ttu-id="b614b-111">Tout développeur bâtiment sur le Web doit être en mesure d’utiliser le DevTools.</span><span class="sxs-lookup"><span data-stu-id="b614b-111">Every developer building the web should be able to use the DevTools.</span></span>  

:::image type="complex" source="../../images/2019/12/a11y-performance-tool.msft.gif" alt-text="Outil performance dans le DevTools avec les améliorations de la navigation au clavier et du lecteur d’écran" lightbox="../../images/2019/12/a11y-performance-tool.msft.gif":::
   <span data-ttu-id="b614b-113">Outil **performance** dans le devtools avec les améliorations de la navigation au clavier et du lecteur d’écran</span><span class="sxs-lookup"><span data-stu-id="b614b-113">The **Performance** tool in the DevTools with the keyboard navigation and screen reader improvements</span></span>  
:::image-end:::  

<span data-ttu-id="b614b-114">Vous voulez savoir comment rendre votre page Web accessible à tous vos utilisateurs?</span><span class="sxs-lookup"><span data-stu-id="b614b-114">Want to learn how to make your web page accessible to all of your users?</span></span>  <span data-ttu-id="b614b-115">Téléchargez les informations [d’accessibilité][AccessibilityInsights] et les extensions [Webhint][WebhintBrowserExtension] pour Microsoft Edge pour commencer.</span><span class="sxs-lookup"><span data-stu-id="b614b-115">Download the [Accessibility Insights][AccessibilityInsights] and [webhint][WebhintBrowserExtension] extensions for Microsoft Edge to get started.</span></span>  

<span data-ttu-id="b614b-116">Si vous utilisez un lecteur d’écran ou le clavier pour naviguer dans le DevTools, envoyez-nous vos commentaires en nous appuyant sur un [Tweet][PostTweetEdgeDevTools] ou en cliquant sur l’icône d' [envoi de commentaires](#getting-in-touch-with-microsoft-edge-devtools-team) .</span><span class="sxs-lookup"><span data-stu-id="b614b-116">If you use screen readers or the keyboard to navigate around the DevTools, send your feedback by [tweeting][PostTweetEdgeDevTools] at us or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="b614b-117">[#963183][CR963183] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="b614b-117">Chromium issue [#963183][CR963183]</span></span>  

### <span data-ttu-id="b614b-118">Utiliser le DevTools dans d’autres langues</span><span class="sxs-lookup"><span data-stu-id="b614b-118">Using the DevTools in other languages</span></span>  

<span data-ttu-id="b614b-119">De nombreux développeurs utilisent d’autres outils de développement tels que StackOverflow et Visual Studio, dans leur langue maternelle, et non uniquement en anglais.</span><span class="sxs-lookup"><span data-stu-id="b614b-119">Many developers use other developer tools, like StackOverflow and Visual Studio Code, in their native language, not just in English.</span></span>  <span data-ttu-id="b614b-120">Nous sommes heureux d’annoncer la localisation de DevTools, que vous pouvez désormais utiliser dans l’un des 10 langues autres que l’anglais:</span><span class="sxs-lookup"><span data-stu-id="b614b-120">We’re excited to announce localization for the DevTools, which you are now able to use in one of 10 languages besides English:</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="b614b-121">Chinois (simplifié)- &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span><span class="sxs-lookup"><span data-stu-id="b614b-121">Chinese \(Simplified\) - &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="b614b-122">Chinois (traditionnel)- &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span><span class="sxs-lookup"><span data-stu-id="b614b-122">Chinese \(Traditional\) - &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="b614b-123">Français-Fran&#231;AIS</span><span class="sxs-lookup"><span data-stu-id="b614b-123">French – fran&#231;ais</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="b614b-124">Allemand-Deutsch</span><span class="sxs-lookup"><span data-stu-id="b614b-124">German - deutsch</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="b614b-125">Italien-Italiano</span><span class="sxs-lookup"><span data-stu-id="b614b-125">Italian - italiano</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="b614b-126">Japonais- &#26085;&#26412;&#35486;</span><span class="sxs-lookup"><span data-stu-id="b614b-126">Japanese - &#26085;&#26412;&#35486;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="b614b-127">Coréen- &#54620;&#44397;&#50612;</span><span class="sxs-lookup"><span data-stu-id="b614b-127">Korean - &#54620;&#44397;&#50612;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="b614b-128">Portugais-portugu&#234;s</span><span class="sxs-lookup"><span data-stu-id="b614b-128">Portuguese - portugu&#234;s</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="b614b-129">Russe- &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span><span class="sxs-lookup"><span data-stu-id="b614b-129">Russian – &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="b614b-130">Espagnol-ESPA&#241;ol</span><span class="sxs-lookup"><span data-stu-id="b614b-130">Spanish - espa&#241;ol</span></span>
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

<span data-ttu-id="b614b-131">Accédez à `edge://flags` l’indicateur d' **activation des outils de développement localisé** et définissez-le sur **activé**.</span><span class="sxs-lookup"><span data-stu-id="b614b-131">Navigate to `edge://flags` and set the **Enable localized Developer Tools** flag to **Enabled**.</span></span>  <span data-ttu-id="b614b-132">Définissez également l’indicateur **expériences des outils de développement** sur **activé**.</span><span class="sxs-lookup"><span data-stu-id="b614b-132">Also set the **Developer Tools experiments** flag to **Enabled**.</span></span>  <span data-ttu-id="b614b-133">Redémarrez Microsoft Edge et ouvrez le DevTools.</span><span class="sxs-lookup"><span data-stu-id="b614b-133">Restart Microsoft Edge and open the DevTools.</span></span>  <!-- Press `F1` in the DevTools or go to Settings > Experiments and check the **Match browser language** checkbox.  -->  <span data-ttu-id="b614b-134">Le DevTools correspond à la langue que vous utilisez pour Microsoft Edge dans `edge://settings/languages` .</span><span class="sxs-lookup"><span data-stu-id="b614b-134">The DevTools match the language you use for Microsoft Edge in `edge://settings/languages`.</span></span>  

:::image type="complex" source="../../images/2019/12/localized-devtools.msft.png" alt-text="DevTools en allemand" lightbox="../../images/2019/12/localized-devtools.msft.png":::
   <span data-ttu-id="b614b-136">DevTools en allemand</span><span class="sxs-lookup"><span data-stu-id="b614b-136">The DevTools in German</span></span>  
:::image-end:::  

<span data-ttu-id="b614b-137">Si vous souhaitez utiliser le DevTools dans une autre langue que celle proposée, vous pouvez utiliser le [Tweet][PostTweetEdgeDevTools] ou cliquez sur l’icône d' [envoi de commentaires](#getting-in-touch-with-microsoft-edge-devtools-team) .</span><span class="sxs-lookup"><span data-stu-id="b614b-137">If you want to use the DevTools in a different language than the ones that are available, [tweet][PostTweetEdgeDevTools] at us or click the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon.</span></span>  

<span data-ttu-id="b614b-138">[#941561][CR941561] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="b614b-138">Chromium issue [#941561][CR941561]</span></span>  

### <span data-ttu-id="b614b-139">extension Microsoft Edge de webhint</span><span class="sxs-lookup"><span data-stu-id="b614b-139">webhint Microsoft Edge extension</span></span>  

<span data-ttu-id="b614b-140">L’extension Microsoft Edge de Microsoft vous permet d’analyser facilement votre page Web et de faire des commentaires sur l’accessibilité, la compatibilité avec les navigateurs, la sécurité et les performances, etc., dans le DevTools.</span><span class="sxs-lookup"><span data-stu-id="b614b-140">The webhint Microsoft Edge extension allows you to easily scan your web page and get feedback on accessibility, browser compatibility, security, performance, and more within the DevTools.</span></span>  <span data-ttu-id="b614b-141">Pour en savoir plus [https://webhint.io][Webhint] , voir.</span><span class="sxs-lookup"><span data-stu-id="b614b-141">Read more at [https://webhint.io][Webhint].</span></span>  

:::image type="complex" source="../../images/2019/12/webhint-browser-extension.msft.png" alt-text="Onglet Hints dans le DevTools lorsque l’extension de navigateur webhint est installée" lightbox="../../images/2019/12/webhint-browser-extension.msft.png":::
   <span data-ttu-id="b614b-143">Onglet **Hints** dans le devtools lorsque l’extension de navigateur webhint est installée</span><span class="sxs-lookup"><span data-stu-id="b614b-143">The **Hints** tab in the DevTools when the webhint browser extension is installed</span></span>  
:::image-end:::  

<span data-ttu-id="b614b-144">[Essayez l’extension de navigateur webhint dans Microsoft Edge][MicrosoftEdgeInsiderAddons].</span><span class="sxs-lookup"><span data-stu-id="b614b-144">[Try the webhint browser extension in Microsoft Edge][MicrosoftEdgeInsiderAddons].</span></span>  <span data-ttu-id="b614b-145">Une fois l’extension installée, ouvrez le DevTools et sélectionnez l’onglet conseils.  À partir de là, effectuez une analyse de site personnalisable.</span><span class="sxs-lookup"><span data-stu-id="b614b-145">Once you install the extension, open the DevTools and select the Hints tab.  From here, run a customizable site scan.</span></span>  <span data-ttu-id="b614b-146">Accédez à [webhint.IO][WebhintBrowserExtension] pour en savoir plus.</span><span class="sxs-lookup"><span data-stu-id="b614b-146">Head over to [webhint.io][WebhintBrowserExtension] to learn more.</span></span>

### <span data-ttu-id="b614b-147">Vue 3D</span><span class="sxs-lookup"><span data-stu-id="b614b-147">3D View</span></span>  

<span data-ttu-id="b614b-148">Utilisez la **vue 3D** pour déboguer votre application Web en naviguant dans le [modèle d’objet de document \ (DOM \)][MDNDocumentObjectModel] ou le contexte de pile [de l’index z][MDNZIndex] .</span><span class="sxs-lookup"><span data-stu-id="b614b-148">Use the **3D View** to debug your web application by navigating through the [Document Object Model \(DOM\)][MDNDocumentObjectModel] or the [z-index][MDNZIndex] stacking context.</span></span>  

:::image type="complex" source="../../images/2019/12/3dview.msft.png" alt-text="Affichage 3D dans le DevTools" lightbox="../../images/2019/12/3dview.msft.png":::
   <span data-ttu-id="b614b-150">**Affichage 3D** dans le devtools</span><span class="sxs-lookup"><span data-stu-id="b614b-150">The **3D View** in the DevTools</span></span>  
:::image-end:::  

<span data-ttu-id="b614b-151">Pour accéder à la vue 3D, accédez à l' `edge://flags` indicateur d' **expériences outils de développement** et vérifiez qu’il est défini sur **activé**.</span><span class="sxs-lookup"><span data-stu-id="b614b-151">To access the 3D View, navigate to `edge://flags` and ensure that the **Developer Tools experiments** flag is set to **Enabled**.</span></span>  <span data-ttu-id="b614b-152">Redémarrez Microsoft Edge et ouvrez le DevTools.</span><span class="sxs-lookup"><span data-stu-id="b614b-152">Restart Microsoft Edge and open the DevTools.</span></span>  <span data-ttu-id="b614b-153">Appuyez sur `F1` le devtools ou accédez à **paramètres**, accédez à la section **expériences** , puis activez la case à cocher **activer le mode 3D** .</span><span class="sxs-lookup"><span data-stu-id="b614b-153">Press `F1` in the DevTools or go to **Settings**, navigate to **Experiments** section, and check the **Enable 3D View** checkbox.</span></span>  <span data-ttu-id="b614b-154">À présent, appuyez sur la touche `Ctrl`  +  `Shift`  +  `P` **affichage 3D** et sélectionnez **afficher la vue 3D**.</span><span class="sxs-lookup"><span data-stu-id="b614b-154">Now, press `Ctrl` + `Shift` + `P`, type in **3D View** and select **Show 3D View**.</span></span>  

<span data-ttu-id="b614b-155">Nous travaillons sur l’interface utilisateur et nous ajoutons d’autres fonctionnalités à la vue 3D; nous vous envoyons donc votre [avis](#getting-in-touch-with-microsoft-edge-devtools-team).</span><span class="sxs-lookup"><span data-stu-id="b614b-155">We're working on the UI and adding more functionality to the 3D View so please send us your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team).</span></span>  

<span data-ttu-id="b614b-156">[#987787][CR987787] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="b614b-156">Chromium issue [#987787][CR987787]</span></span>

### <span data-ttu-id="b614b-157">Extensions de code Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b614b-157">Visual Studio Code extensions</span></span>  

<span data-ttu-id="b614b-158">L’équipe DevTools a également émis quelques extensions pour le [code Visual Studio][VisualStudioCode] qui vous permettent d’utiliser la puissance de devtools directement à partir de votre éditeur de texte.</span><span class="sxs-lookup"><span data-stu-id="b614b-158">The DevTools team has also released some extensions for [Visual Studio Code][VisualStudioCode] that let you use the power of the DevTools directly from your text editor.</span></span> <span data-ttu-id="b614b-159">Consultez les extensions suivantes.</span><span class="sxs-lookup"><span data-stu-id="b614b-159">Check out the following extensions.</span></span>  

#### <span data-ttu-id="b614b-160">Éléments pour Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b614b-160">Elements for Microsoft Edge</span></span>  

<span data-ttu-id="b614b-161">Utilisez l’outil éléments dans le code Visual Studio en ajoutant les éléments de l’extension de code Visual Studio [(chrome)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] .</span><span class="sxs-lookup"><span data-stu-id="b614b-161">Use the Elements tool from within Visual Studio Code by adding the [Elements for Microsoft Edge (Chromium)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] Visual Studio Code extension.</span></span>  

:::image type="complex" source="../../images/2019/12/elements-for-edge.msft.png" alt-text="Outil éléments dans le code Visual Studio utilisant les éléments de l’extension Microsoft Edge" lightbox="../../images/2019/12/elements-for-edge.msft.png":::
   <span data-ttu-id="b614b-163">Outil **éléments** dans le code Visual Studio utilisant les éléments de l’extension Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b614b-163">The **Elements** tool in Visual Studio Code using the Elements for Microsoft Edge extension</span></span>  
:::image-end:::  

<span data-ttu-id="b614b-164">Pour plus d’informations, consultez les [éléments pour l’extension de code Visual Studio Visual Studio][VisualStudioCodeElementEdgeExtension].</span><span class="sxs-lookup"><span data-stu-id="b614b-164">For more information, check out [Elements for Microsoft Edge Visual Studio Code extension][VisualStudioCodeElementEdgeExtension].</span></span>  

#### <span data-ttu-id="b614b-165">Débogueur pour Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b614b-165">Debugger for Microsoft Edge</span></span>  

<span data-ttu-id="b614b-166">Avec le [débogueur pour][VisualStudioMarketplaceDebuggerEdge] l’extension de code Visual Studio Visual Studio, déboguez JavaScript en cours d’exécution dans Microsoft Edge directement à partir de code Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b614b-166">With the [Debugger for Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] Visual Studio Code extension, debug JavaScript running in Microsoft Edge directly from Visual Studio Code.</span></span>  

:::image type="complex" source="../../images/2019/12/vscode-debugger.msft.png" alt-text="Le débogueur pour l’extension Microsoft Edge dans le code Visual Studio" lightbox="../../images/2019/12/vscode-debugger.msft.png":::
   <span data-ttu-id="b614b-168">Le débogueur pour l’extension Microsoft Edge dans le code Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b614b-168">The Debugger for Microsoft Edge Extension in Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="b614b-169">Pour plus d’informations, voir [Comment déboguer Microsoft Edge à partir de code Visual Studio][VisualStudioCodeDebuggerEdgeExtension].</span><span class="sxs-lookup"><span data-stu-id="b614b-169">For more information, check out [how to debug Microsoft Edge from Visual Studio Code][VisualStudioCodeDebuggerEdgeExtension].</span></span>  

#### <span data-ttu-id="b614b-170">webhint</span><span class="sxs-lookup"><span data-stu-id="b614b-170">webhint</span></span>  

<span data-ttu-id="b614b-171">L’extension de code [webhint][VisualStudioMarketplaceWebhintExtension] Visual Studio utilise `webhint` pour améliorer votre page Web pendant que vous rédigez un message.</span><span class="sxs-lookup"><span data-stu-id="b614b-171">The [webhint][VisualStudioMarketplaceWebhintExtension] Visual Studio Code extension uses `webhint` to improve your web page while you're writing it!</span></span> <span data-ttu-id="b614b-172">Cette extension exécute et signale les diagnostics de vos fichiers d’espace de travail en fonction de l' `webhint` analyse.</span><span class="sxs-lookup"><span data-stu-id="b614b-172">This extension runs and reports diagnostics on your workspace files based on `webhint` analysis.</span></span>  

:::image type="complex" source="../../images/2019/12/webhint-vscode-extension.msft.png" alt-text="Extension de code Visual Studio webhint qui analyse un fichier. TSX dans le code Visual Studio" lightbox="../../images/2019/12/webhint-vscode-extension.msft.png":::
   <span data-ttu-id="b614b-174">Extension de code Visual Studio webhint qui analyse un `.tsx` fichier dans le code Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b614b-174">The webhint Visual Studio Code extension analyzing a `.tsx` file in Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="b614b-175">[En savoir plus sur l’extension Visual Studio code webhint][WebhintVisualStudioCodeExtension].</span><span class="sxs-lookup"><span data-stu-id="b614b-175">[Learn more about the Visual Studio Code webhint extension][WebhintVisualStudioCodeExtension].</span></span>  

### <span data-ttu-id="b614b-176">Intégration de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b614b-176">Visual Studio integration</span></span>
<span data-ttu-id="b614b-177">Dans Visual Studio 2019 version 16,2 ou ultérieure, utilisez le débogueur Visual Studio pour déboguer JavaScript en cours d’exécution dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b614b-177">In Visual Studio 2019 version 16.2 or later, use the Visual Studio debugger to debug JavaScript running in Microsoft Edge.</span></span>  <span data-ttu-id="b614b-178">[Téléchargez Visual Studio 2019][MicrosoftVisualStudioDownloads] pour essayer cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="b614b-178">[Download Visual Studio 2019][MicrosoftVisualStudioDownloads] to try this feature out!</span></span>  

:::image type="complex" source="../../images/2019/12/vs.msft.png" alt-text="Visual Studio avec l’option de lancement de votre application Web dans Microsoft Edge Canaries, dev ou Beta" lightbox="../../images/2019/12/vs.msft.png":::
   <span data-ttu-id="b614b-180">Visual Studio avec l’option de lancement de votre application Web dans Microsoft Edge Canaries, dev ou Beta</span><span class="sxs-lookup"><span data-stu-id="b614b-180">Visual Studio with the option to launch your web app in Microsoft Edge Canary, Dev, or Beta</span></span>  
:::image-end:::  

<span data-ttu-id="b614b-181">[Pour plus d’informations sur le débogage de Microsoft Edge à partir de Visual Studio, consultez notre billet de blog][MicrosoftVisualStudioBlogDebugJavascript].</span><span class="sxs-lookup"><span data-stu-id="b614b-181">[Read our blog post to learn how to debug Microsoft Edge from Visual Studio][MicrosoftVisualStudioBlogDebugJavascript].</span></span>  

### <span data-ttu-id="b614b-182">Suivi des messages de la console de prévention</span><span class="sxs-lookup"><span data-stu-id="b614b-182">Tracking prevention Console messages</span></span>  

<span data-ttu-id="b614b-183">La prévention de suivi est une fonctionnalité unique de Microsoft Edge qui vous protège du suivi par des sites Web que vous n’avez pas encore visités.</span><span class="sxs-lookup"><span data-stu-id="b614b-183">Tracking prevention is a unique feature in Microsoft Edge that protects you from being tracked by websites you haven't visited before.</span></span>  <span data-ttu-id="b614b-184">Le paramètre de prévention du suivi par défaut est le mode équilibré, qui permet de bloquer des suivis tiers et des pistes malveillantes connues pour une interface qui équilibre la confidentialité et la compatibilité Web.</span><span class="sxs-lookup"><span data-stu-id="b614b-184">The default tracking prevention setting is Balanced mode, which blocks 3rd party trackers and known malicious trackers for an experience that balances privacy and web compatibility.</span></span>  <span data-ttu-id="b614b-185">Pour plus d’informations sur la compatibilité de votre page Web lorsque certains suivis sont bloqués, nous avons également ajouté des messages d’avertissement dans la console lorsqu’un suivi est bloqué.</span><span class="sxs-lookup"><span data-stu-id="b614b-185">To give you more insight into the compatibility of your web page when certain trackers are blocked, we've also added warning messages in the Console when a tracker is blocked.</span></span>  

:::image type="complex" source="../../images/2019/12/tracking-prevention.msft.png" alt-text="Messages dans la console lors du suivi de la prévention bloquer l’accès au stockage pour un suivi" lightbox="../../images/2019/12/tracking-prevention.msft.png":::
   <span data-ttu-id="b614b-187">Messages dans la **console** lors du suivi de la prévention bloquer l’accès au stockage pour un suivi</span><span class="sxs-lookup"><span data-stu-id="b614b-187">Messages in the **Console** when tracking prevention blocks access to storage for a tracker</span></span>  
:::image-end:::  

<span data-ttu-id="b614b-188">[En savoir plus sur la prévention de suivi et le compromis entre la confidentialité et la compatibilité Web][TrackingPrevention].</span><span class="sxs-lookup"><span data-stu-id="b614b-188">[Read more about tracking prevention and the balance between privacy and web compatibility][TrackingPrevention].</span></span>  

## <span data-ttu-id="b614b-189">Annonces du projet de chrome</span><span class="sxs-lookup"><span data-stu-id="b614b-189">Announcements from the Chromium project</span></span>  

<span data-ttu-id="b614b-190">Les sections suivantes annoncent des fonctionnalités supplémentaires disponibles dans Microsoft Edge 80 qui ont été fournies au projet de chrome Open source.</span><span class="sxs-lookup"><span data-stu-id="b614b-190">The following sections announce additional features available in Microsoft Edge 80 that were contributed to the open source Chromium project.</span></span>  

### <span data-ttu-id="b614b-191">Prise en charge de la redéclaration de la classe et des classes dans la console</span><span class="sxs-lookup"><span data-stu-id="b614b-191">Support for let and class redeclarations in the Console</span></span>  

<span data-ttu-id="b614b-192">La **console** prend désormais en charge les redéclarations `let` et les `class` instructions.</span><span class="sxs-lookup"><span data-stu-id="b614b-192">The **Console** now supports redeclarations of `let` and `class` statements.</span></span>  <span data-ttu-id="b614b-193">L’impossibilité de redéclarer est une gêne pour les développeurs Web qui utilisent la console pour tester le nouveau code JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b614b-193">The inability to redeclare was a common annoyance for web developers who use the Console to experiment with new JavaScript code.</span></span>  

> [!WARNING]
> <span data-ttu-id="b614b-194">La redéclaration d’une `let` instruction ou d’un `class` script en dehors de la console, ou au sein d’une seule et même entrée de console entraîne une `SyntaxError` .</span><span class="sxs-lookup"><span data-stu-id="b614b-194">Redeclaring a `let` or `class` statement in a script outside of the Console or within a single Console input still causes a `SyntaxError`.</span></span>  

<span data-ttu-id="b614b-195">Par exemple, auparavant, lors de la redéclaration d’une variable locale avec `let` , la console a renvoyé une erreur:</span><span class="sxs-lookup"><span data-stu-id="b614b-195">For example, previously, when re-declaring a local variable with `let`, the Console threw an error:</span></span>  

:::image type="complex" source="../../images/2019/12/letbefore.msft.png" alt-text="La console dans Microsoft Edge 79 indiquant l’échec de la redéclaration" lightbox="../../images/2019/12/letbefore.msft.png":::
   <span data-ttu-id="b614b-197">La **console** dans Microsoft Edge 79 indiquant que la redéclaration de l’option ne fonctionne pas</span><span class="sxs-lookup"><span data-stu-id="b614b-197">The **Console** in Microsoft Edge 79 showing that the let re-declaration fails</span></span>  
:::image-end:::  

<span data-ttu-id="b614b-198">À présent, la console autorise la redéclaration:</span><span class="sxs-lookup"><span data-stu-id="b614b-198">Now, the Console allows the redeclaration:</span></span>  

:::image type="complex" source="../../images/2019/12/letafter.msft.png" alt-text="Console dans Microsoft Edge 80 indiquant que la redéclaration de réussite est réussie" lightbox="../../images/2019/12/letafter.msft.png":::
   <span data-ttu-id="b614b-200">**Console** dans Microsoft Edge 80 indiquant que la redéclaration de réussite a réussi</span><span class="sxs-lookup"><span data-stu-id="b614b-200">The **Console** in Microsoft Edge 80 showing that the let re-declaration succeeds</span></span>  
:::image-end:::  

<span data-ttu-id="b614b-201">[#1004193][CR1004193] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="b614b-201">Chromium issue [#1004193][CR1004193]</span></span>  

### <span data-ttu-id="b614b-202">Débogage d’assembly améliorée</span><span class="sxs-lookup"><span data-stu-id="b614b-202">Improved WebAssembly debugging</span></span>  

<span data-ttu-id="b614b-203">DevTools a commencé à prendre en charge la [norme de débogage de nain][DwarfHome], ce qui signifie qu’il s’agit d’une prise en charge accrue pour le code pas à pas, la définition de points d’arrêt et la résolution de traces de pile dans vos langages sources dans devtools.</span><span class="sxs-lookup"><span data-stu-id="b614b-203">DevTools has started to support the [DWARF Debugging Standard][DwarfHome], which means increased support for stepping over code, setting breakpoints, and resolving stack traces in your source languages within DevTools.</span></span>  

<!-- [TODO: Add this link back] -->  
<!--Check out [Improved WebAssembly debugging in Microsoft Edge DevTools][201912Webassembly] for the full story.  -->  

<!-- [TODO: Replace this image with screenshot in Edge] -->  
<!--
:::image type="complex" source="../../images/2019/12/wasm.msft.png" alt-text="The new DWARF-powered WebAssembly debugging" lightbox="../../images/2019/12/wasm.msft.png":::
   The new DWARF-powered WebAssembly debugging  
:::image-end:::  
-->  

### <span data-ttu-id="b614b-204">Mises à jour du panneau réseau</span><span class="sxs-lookup"><span data-stu-id="b614b-204">Network panel updates</span></span>  

#### <span data-ttu-id="b614b-205">Chaînes d’initiateur de requête dans l’onglet initiateur</span><span class="sxs-lookup"><span data-stu-id="b614b-205">Request Initiator Chains in the Initiator tab</span></span>  

<span data-ttu-id="b614b-206">Vous pouvez à présent afficher les initiateurs et les dépendances d’une demande réseau en tant que liste imbriquée.</span><span class="sxs-lookup"><span data-stu-id="b614b-206">You are now able to view the initiators and dependencies of a network request as a nested list.</span></span>  <span data-ttu-id="b614b-207">Cela risque de vous aider à comprendre la raison pour laquelle une ressource a été demandée ou l’activité réseau pour laquelle une ressource (par exemple, un script) a été créée.</span><span class="sxs-lookup"><span data-stu-id="b614b-207">This may help you understand why a resource was requested, or what network activity a certain resource \(such as a script\) caused.</span></span>  

:::image type="complex" source="../../images/2019/12/initiators.msft.png" alt-text="Chaîne d’initiateur de requête dans l’onglet initiateur" lightbox="../../images/2019/12/initiators.msft.png":::
   <span data-ttu-id="b614b-209">Chaîne d’initiateur de requête dans l’onglet **initiateur**</span><span class="sxs-lookup"><span data-stu-id="b614b-209">A Request Initiator Chain in the **Initiator** tab</span></span>  
:::image-end:::  

<span data-ttu-id="b614b-210">Après la [journalisation de l’activité réseau dans le panneau réseau][DevToolsNetworkIndex], cliquez sur une ressource, puis accédez à l’onglet **initiateur** pour afficher la chaîne d’initiateur de la **requête**:</span><span class="sxs-lookup"><span data-stu-id="b614b-210">After [logging network activity in the Network panel][DevToolsNetworkIndex], click a resource and then go to the **Initiator** tab to view the **Request Initiator Chain**:</span></span>  

*   <span data-ttu-id="b614b-211">La **ressource inspectée** est en gras.</span><span class="sxs-lookup"><span data-stu-id="b614b-211">The **inspected resource** is bold.</span></span>  <span data-ttu-id="b614b-212">Dans la capture d’écran ci-dessus, `ai.2.min.js` figure la ressource inspectée.</span><span class="sxs-lookup"><span data-stu-id="b614b-212">In the screenshot above, `ai.2.min.js` is the inspected resource.</span></span>  
*   <span data-ttu-id="b614b-213">Les ressources au-dessus de la ressource inspectée sont les **initiateurs**.</span><span class="sxs-lookup"><span data-stu-id="b614b-213">The resources above the inspected resource are the **initiators**.</span></span>  <span data-ttu-id="b614b-214">Dans la capture d’écran ci-dessus, `https://www.microsoftedgeinsider.com` est l’initiateur de `ai.2.min.js` .</span><span class="sxs-lookup"><span data-stu-id="b614b-214">In the screenshot above, `https://www.microsoftedgeinsider.com` is the initiator of `ai.2.min.js`.</span></span>  <span data-ttu-id="b614b-215">En d’autres termes, à `https://www.microsoftedgeinsider.com` l’origine de la demande de réseau `ai.2.min.js` .</span><span class="sxs-lookup"><span data-stu-id="b614b-215">In other words, `https://www.microsoftedgeinsider.com` caused the network request for `ai.2.min.js`.</span></span>  
*   <span data-ttu-id="b614b-216">Les ressources sous la ressource inspectée sont les **dépendances**.</span><span class="sxs-lookup"><span data-stu-id="b614b-216">The resources below the inspected resource are the **dependencies**.</span></span>  <span data-ttu-id="b614b-217">Dans la capture d’écran ci-dessus, `https://dc.services.visualstudio.com/v2/track` il existe une dépendance `ai.2.min.js` .</span><span class="sxs-lookup"><span data-stu-id="b614b-217">In the screenshot above, `https://dc.services.visualstudio.com/v2/track` is a dependency of `ai.2.min.js`.</span></span>  <span data-ttu-id="b614b-218">En d’autres termes, à `ai.2.min.js` l’origine de la demande de réseau `https://dc.services.visualstudio.com/v2/track` .</span><span class="sxs-lookup"><span data-stu-id="b614b-218">In other words, `ai.2.min.js` caused the network request for `https://dc.services.visualstudio.com/v2/track`.</span></span>  

> [!NOTE]
> <span data-ttu-id="b614b-219">Il est également possible d’accéder à des informations d’initiateur et de dépendance en Holding `Shift` puis en pointant sur les ressources réseau.</span><span class="sxs-lookup"><span data-stu-id="b614b-219">Initiator and dependency information may also be accessed by holding `Shift` and then hovering over network resources.</span></span>  <span data-ttu-id="b614b-220">Voir [les initiateurs de vues et les dépendances][DevToolsNetworkReferenceViewInitiatorsDependencies].</span><span class="sxs-lookup"><span data-stu-id="b614b-220">See [View initiators and dependencies][DevToolsNetworkReferenceViewInitiatorsDependencies].</span></span>  

<span data-ttu-id="b614b-221">[#842488][CR842488] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="b614b-221">Chromium issue [#842488][CR842488]</span></span>  

#### <span data-ttu-id="b614b-222">Mettre en surbrillance la demande réseau sélectionnée dans la vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="b614b-222">Highlight the selected network request in the Overview</span></span>  

<span data-ttu-id="b614b-223">Après avoir cliqué sur une ressource réseau pour la vérifier, le panneau réseau place désormais une bordure bleue autour de celle-ci dans la **vue d’ensemble**.</span><span class="sxs-lookup"><span data-stu-id="b614b-223">After you click a network resource in order to inspect it, the Network panel now puts a blue border around that resource in the **Overview**.</span></span>  <span data-ttu-id="b614b-224">Cela peut vous aider à détecter si la demande de réseau se produit avant ou après la fin prévue.</span><span class="sxs-lookup"><span data-stu-id="b614b-224">This is able to help you detect if the network request is happening earlier or later than expected.</span></span>  

:::image type="complex" source="../../images/2019/12/overview.msft.png" alt-text="Volet vue d’ensemble mettant en évidence la ressource inspectée" lightbox="../../images/2019/12/overview.msft.png":::
   <span data-ttu-id="b614b-226">Volet **vue d’ensemble** mettant en évidence la ressource inspectée</span><span class="sxs-lookup"><span data-stu-id="b614b-226">The **Overview** pane highlighting the inspected resource</span></span>  
:::image-end:::  

<span data-ttu-id="b614b-227">[#988253][CR988253] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="b614b-227">Chromium issue [#988253][CR988253]</span></span>  

#### <span data-ttu-id="b614b-228">Colonnes d’URL et de chemin d’accès dans le panneau réseau</span><span class="sxs-lookup"><span data-stu-id="b614b-228">URL and path columns in the Network panel</span></span>  

<span data-ttu-id="b614b-229">Utilisez les nouvelles colonnes **path** et **URL** du panneau **réseau** pour afficher le chemin d’accès absolu ou l’URL complète de chaque ressource réseau.</span><span class="sxs-lookup"><span data-stu-id="b614b-229">Use the new **Path** and **URL** columns in the **Network** panel to see the absolute path or full URL of each network resource.</span></span>  

:::image type="complex" source="../../images/2019/12/columns.msft.png" alt-text="Les nouvelles colonnes Path et URL du panneau réseau" lightbox="../../images/2019/12/columns.msft.png":::
   <span data-ttu-id="b614b-231">Les nouvelles colonnes Path et URL du panneau **réseau**</span><span class="sxs-lookup"><span data-stu-id="b614b-231">The new Path and URL columns in the **Network** panel</span></span>  
:::image-end:::  

<span data-ttu-id="b614b-232">Cliquez avec le bouton droit sur l’en-tête de tableau en **cascade** , puis sélectionnez **chemin** ou **URL** pour afficher les nouvelles colonnes.</span><span class="sxs-lookup"><span data-stu-id="b614b-232">Right-click the **Waterfall** table header and select **Path** or **URL** to show the new columns.</span></span>  

<span data-ttu-id="b614b-233">[#993366][CR993366] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="b614b-233">Chromium issue [#993366][CR993366]</span></span>  

#### <span data-ttu-id="b614b-234">Chaînes d’agent utilisateur mises à jour</span><span class="sxs-lookup"><span data-stu-id="b614b-234">Updated User-Agent strings</span></span>  

<span data-ttu-id="b614b-235">DevTools prend en charge la définition d’une chaîne d’agent utilisateur personnalisée par le biais de l’onglet **conditions réseau** .  La chaîne de l’agent utilisateur affecte l' `User-Agent` en-tête http attaché aux ressources réseau, ainsi que la valeur de `navigator.userAgent` .</span><span class="sxs-lookup"><span data-stu-id="b614b-235">DevTools supports setting a custom User-Agent string through the **Network Conditions** tab.  The User-Agent string affects the `User-Agent` HTTP header attached to network resources, and also the value of `navigator.userAgent`.</span></span>  

<span data-ttu-id="b614b-236">Les chaînes d’agent utilisateur prédéfinies ont été mises à jour pour refléter les versions modernes du navigateur.</span><span class="sxs-lookup"><span data-stu-id="b614b-236">The predefined User-Agent strings have been updated to reflect modern browser versions.</span></span>  

:::image type="complex" source="../../images/2019/12/useragent.msft.png" alt-text="Menu agent utilisateur de l’onglet conditions réseau" lightbox="../../images/2019/12/useragent.msft.png":::
   <span data-ttu-id="b614b-238">Menu agent utilisateur de l’onglet **conditions réseau**</span><span class="sxs-lookup"><span data-stu-id="b614b-238">The User Agent menu in the **Network Conditions** tab</span></span>  
:::image-end:::  

<span data-ttu-id="b614b-239">Pour accéder aux **conditions du réseau**, [Ouvrez le menu de commandes][DevToolsCommandMenuIndex] et exécutez la `Show Network Conditions` commande.</span><span class="sxs-lookup"><span data-stu-id="b614b-239">To access **Network Conditions**, [open the Command Menu][DevToolsCommandMenuIndex] and run the `Show Network Conditions` command.</span></span>  

> [!NOTE]
> <span data-ttu-id="b614b-240">Vous pouvez également [définir des chaînes d’agent utilisateur en mode appareil][DevToolsDeviceModeIndex].</span><span class="sxs-lookup"><span data-stu-id="b614b-240">You may also [set User-Agent strings in Device Mode][DevToolsDeviceModeIndex].</span></span>  

<span data-ttu-id="b614b-241">[#1029031][CR1029031] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="b614b-241">Chromium issue [#1029031][CR1029031]</span></span>  

### <span data-ttu-id="b614b-242">Mises à jour du volet d’audit</span><span class="sxs-lookup"><span data-stu-id="b614b-242">Audits panel updates</span></span>  

#### <span data-ttu-id="b614b-243">Nouvelle interface utilisateur de configuration</span><span class="sxs-lookup"><span data-stu-id="b614b-243">New configuration UI</span></span>  

<span data-ttu-id="b614b-244">L’interface utilisateur de configuration dispose d’une nouvelle conception réactive, et les options de configuration de limitation ont été simplifiées.</span><span class="sxs-lookup"><span data-stu-id="b614b-244">The configuration UI has a new, responsive design, and the throttling configuration options have been simplified.</span></span>  <span data-ttu-id="b614b-245">Pour plus d’informations sur les modifications de l’interface utilisateur de limitation, voir [limitation du panneau d’audit][GitHubGoogleChromeDevToolsAuditsPanelThrottling] .</span><span class="sxs-lookup"><span data-stu-id="b614b-245">See [Audits Panel Throttling][GitHubGoogleChromeDevToolsAuditsPanelThrottling] for more information on the throttling UI changes.</span></span>  

:::image type="complex" source="../../images/2019/12/start.msft.png" alt-text="Nouvelle interface utilisateur de configuration" lightbox="../../images/2019/12/start.msft.png":::
   <span data-ttu-id="b614b-247">Nouvelle interface utilisateur de configuration</span><span class="sxs-lookup"><span data-stu-id="b614b-247">The new configuration UI</span></span>  
:::image-end:::  

### <span data-ttu-id="b614b-248">Mises à jour de l’onglet couverture</span><span class="sxs-lookup"><span data-stu-id="b614b-248">Coverage tab updates</span></span>  

#### <span data-ttu-id="b614b-249">Modes de couverture par fonction ou par bloc</span><span class="sxs-lookup"><span data-stu-id="b614b-249">Per-function or per-block coverage modes</span></span>  

<span data-ttu-id="b614b-250">Dans le menu déroulant de l' [onglet couverture][DevToolsCoverageIndex] , vous pouvez spécifier si les données de couverture du code doivent être collectées **par fonction** ou **par bloc**.</span><span class="sxs-lookup"><span data-stu-id="b614b-250">The [Coverage tab][DevToolsCoverageIndex] has a new dropdown menu that lets you specify whether code coverage data should be collected **per function** or **per block**.</span></span>  <span data-ttu-id="b614b-251">La couverture **par bloc** est plus détaillée, mais aussi bien plus coûteuse à rassembler.</span><span class="sxs-lookup"><span data-stu-id="b614b-251">**Per block** coverage is more detailed but also far more expensive to collect.</span></span>  <span data-ttu-id="b614b-252">DevTools utilise par défaut une couverture par **fonction** .</span><span class="sxs-lookup"><span data-stu-id="b614b-252">DevTools uses **per function** coverage by default now.</span></span>  

> [!CAUTION]
> <span data-ttu-id="b614b-253">Il est possible que vous voyiez des différences de couverture de code importantes dans les fichiers HTML selon que vous utilisez la **fonction par fonction** ou **par bloc** .</span><span class="sxs-lookup"><span data-stu-id="b614b-253">You may see large code coverage differences in HTML files depending on whether you use **per function** or **per block** mode.</span></span>  <span data-ttu-id="b614b-254">Lorsque vous utilisez le mode **par fonction** , les scripts inline dans les fichiers HTML sont traités en tant que fonctions.</span><span class="sxs-lookup"><span data-stu-id="b614b-254">When using **per function** mode, inline scripts in HTML files are treated as functions.</span></span>  <span data-ttu-id="b614b-255">Si le script s’exécute tout de même, DevTools marque tout le script en tant que code utilisé.</span><span class="sxs-lookup"><span data-stu-id="b614b-255">If the script runs at all then DevTools marks the entire script as used code.</span></span>  <span data-ttu-id="b614b-256">Par exemple, si le script n’est pas exécuté, DevTools le marquer comme étant du code inutilisé.</span><span class="sxs-lookup"><span data-stu-id="b614b-256">Only if the script does not run at all does DevTools mark the script as unused code.</span></span>  

:::image type="complex" source="../../images/2019/12/modes.msft.png" alt-text="Menu déroulant du mode couverture" lightbox="../../images/2019/12/modes.msft.png":::
   <span data-ttu-id="b614b-258">Menu déroulant du mode couverture</span><span class="sxs-lookup"><span data-stu-id="b614b-258">The coverage mode dropdown menu</span></span>  
:::image-end:::  

#### <span data-ttu-id="b614b-259">La couverture doit maintenant être initiée par un recharge de page</span><span class="sxs-lookup"><span data-stu-id="b614b-259">Coverage must now be initiated by a page reload</span></span>  

<span data-ttu-id="b614b-260">Le basculement de la couverture du code sans recharge de page a été supprimé car les données de couverture étaient instables.</span><span class="sxs-lookup"><span data-stu-id="b614b-260">Toggling code coverage without a page reload has been removed because the coverage data was unreliable.</span></span>  <span data-ttu-id="b614b-261">Par exemple, une fonction peut être signalée comme n’étant pas utilisée si le runtime était depuis longtemps et si le nettoyage de la mémoire a nettoyé celle-ci.</span><span class="sxs-lookup"><span data-stu-id="b614b-261">For example, a function may be reported as unused if the runtime was a long time ago and the V8 garbage collector has cleaned it up.</span></span>  

<span data-ttu-id="b614b-262">[#1004203][CR1004203] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="b614b-262">Chromium issue [#1004203][CR1004203]</span></span>  

## <span data-ttu-id="b614b-263">Télécharger les canaux Microsoft Edge preview</span><span class="sxs-lookup"><span data-stu-id="b614b-263">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="b614b-264">Si vous utilisez Windows ou macOS, envisagez d’utiliser les [canaux Microsoft Edge Preview][MicrosoftEdgePreviewChannels] comme navigateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="b614b-264">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="b614b-265">Les canaux d’aperçu vous permettent d’accéder aux dernières fonctionnalités de DevTools.</span><span class="sxs-lookup"><span data-stu-id="b614b-265">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="b614b-266">Contacter l’équipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="b614b-266">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!--<<../../_shared/devtools-feedback.md>> -->

<!--<<../../_shared/canary.md>> -->

<!--<<../../_shared/discover.md>> -->

<!-- image links -->  

<!--[../../images/2019/12/wasm.msft.png]: ../../images/2019/12/wasm.msft.png "Figure: The new DWARF-powered WebAssembly debugging"  -->

<!-- links -->  

[DevToolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Exécuter des commandes à l’aide du menu de commandes de Microsoft Edge DevTools | Documents Microsoft"  
[DevToolsCoverageIndex]: /microsoft-edge/devtools-guide-chromium/coverage/index "Recherchez du code JavaScript et CSS inutilisé avec l’onglet couverture dans Microsoft Edge DevTools | Documents Microsoft"  
[DevToolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index#simulate-a-mobile-viewport "Simuler une fenêtre d’affichage mobile-simuler des appareils mobiles avec le mode appareil dans Microsoft Edge DevTools | Documents Microsoft"  
[DevToolsNetworkIndex]: /microsoft-edge/devtools-guide-chromium/network/index "Examiner l’activité réseau dans Microsoft Edge DevTools | Documents Microsoft"  
[DevToolsNetworkReferenceViewInitiatorsDependencies]: /microsoft-edge/devtools-guide-chromium/network/reference#view-initiators-and-dependencies "Afficher les initiateurs et les dépendances-référence d’analyse du réseau | Documents Microsoft"  
[DevGuideEdgeHtmlWhatsNew]: /microsoft-edge/dev-guide/whats-new "Nouveautés de EdgeHTML | Documents Microsoft"  
[VisualStudioCodeDebuggerEdgeExtension]: /microsoft-edge/visual-studio-code/debugger-for-edge "Débogueur de l’extension de code Visual Studio Microsoft Edge | Documents Microsoft"  
[VisualStudioCodeElementEdgeExtension]: /microsoft-edge/visual-studio-code/elements-for-edge "Éléments de l’extension de code Visual Studio Visual Studio | Documents Microsoft"  

<!--  [201912Webassembly]: webassembly.md "Improved WebAssembly debugging in Microsoft Edge DevTools"  -->  

[CR842488]: https://crbug.com/842488 "Ajoutez le champ Initiator à l’onglet en-têtes | Bugs du chrome"  
[CR988253]: https://crbug.com/988253 "Erreur DevTools-aucune association entre la demande réseau et le graphique de chronologie | Bugs du chrome"  
[CR993366]: https://crbug.com/993366 "Affichez la partie Path de l’URL dans la liste des demandes du panneau réseau | Bugs du chrome"  
[CR1004193]: https://crbug.com/1004193 "Mode REPL pour V8 | Bugs du chrome"  
[CR1004203]: https://crbug.com/1004203 "Rendre votre couverture du code géniale | Bugs du chrome"  
[CR1029031]: https://crbug.com/1029031 "Les chaînes UA sont obsolètes | Bugs du chrome" 
[CR963183]: https://crbug.com/963183 "DevTools ne respectent pas la norme WCAG | Bugs du chrome"
[CR941561]: https://crbug.com/941561 "Localization du DevTools | Bugs du chrome"
[CR987787]: https://crbug.com/987787 "Affichage 3D DOM | Bugs du chrome"

[AccessibilityInsights]: https://aka.ms/a11yinsights "Insights sur l’accessibilité"  

[DwarfHome]: https://dwarfstd.org "Onglet Accueil"  
[GitHubGoogleChromeDevToolsAuditsPanelThrottling]: https://github.com/GoogleChrome/lighthouse/blob/master/docs/throttling.md#devtools-audits-panel-throttling "DevTools’limitation du panneau d’audit-GoogleChrome/phare | GitHub"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Nouveau problème-MicrosoftDocs/Edge-développeur"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Canaux Microsoft Edge preview"  
[MicrosoftEdgeInsiderAddons]: https://aka.ms/webhint/edge-extension "Compléments Microsoft Edge Insider"  
[MicrosoftVisualStudio]: https://aka.ms/vs "Visual Studio"  
[MicrosoftVisualStudioBlogDebugJavascript]: https://aka.ms/vs/debug-edge "Déboguer JavaScript dans Microsoft Edge à partir de Visual Studio | Blog Visual Studio"  
[MicrosoftVisualStudioDownloads]: https://aka.ms/vs/download "Télécharger Visual Studio 2019 pour Windows \ & Mac"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "DOM (Document Object Model) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "index z | MDN"  
[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Publiez un tweet"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools compte Twitter"
[VisualStudioCode]: https://aka.ms/vscode "Code Visual Studio"  
[VisualStudioMarketplaceDebuggerEdge]: https://aka.ms/debugger4code "Débogueur pour Microsoft Edge-Visual Studio Marketplace"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://aka.ms/elements4code "Éléments pour Microsoft Edge \ (chrome \)-Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://aka.ms/webhint4code "webhint-Visual Studio Marketplace"
[Webhint]: https://aka.ms/webhint "Astuce"  
[WebhintBrowserExtension]: https://aka.ms/webhint/browser-extension "Extension du navigateur webhint | documentation webhint"  
[WebhintVisualStudioCodeExtension]: https://aka.ms/webhint/code-extension "Extension de code Visual Studio webhint | documentation webhint"  
[TrackingPrevention]: https://aka.ms/microsoftedge/tracking-prevention-blog "Amélioration de la prévention du suivi dans le billet de blog Microsoft Edge"
[TheWebWeWant]: https://aka.ms/webwewant "Le site Web de votre choix"

> [!NOTE]
> <span data-ttu-id="b614b-306">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b614b-306">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b614b-307">La page d’origine est disponible [ici](https://developers.google.com/web/updates/2019/12/devtools/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="b614b-307">The original page is found [here](https://developers.google.com/web/updates/2019/12/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="b614b-309">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b614b-309">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
