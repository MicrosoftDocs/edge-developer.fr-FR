---
title: Nouveautés de DevTools (Microsoft Edge 81)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 10696a49a833475d59a6be1189362fdb0c26a96d
ms.sourcegitcommit: 2fa65cca74c5214601900579c0ce9f946ad8a27e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "10991155"
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

# <span data-ttu-id="bf1bf-103">Nouveautés de DevTools (Microsoft Edge 81)</span><span class="sxs-lookup"><span data-stu-id="bf1bf-103">What's New In DevTools (Microsoft Edge 81)</span></span>  

## <span data-ttu-id="bf1bf-104">Annonces de l’équipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="bf1bf-104">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="bf1bf-105">Les sections suivantes répertorient les annonces que vous pouvez avoir manquées de l’équipe Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="bf1bf-105">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team!</span></span> <span data-ttu-id="bf1bf-106">Découvrez-les pour essayer de nouvelles fonctionnalités dans les extensions de code DevTools, VS, etc.</span><span class="sxs-lookup"><span data-stu-id="bf1bf-106">Check them out to try new features in the DevTools, VS Code extensions, and more.</span></span>  <span data-ttu-id="bf1bf-107">Pour vous tenir au courant de toutes les fonctionnalités les plus récentes et les plus récentes de vos outils de développement, téléchargez les [canaux Microsoft Edge Preview][MicrosoftEdgePreviewChannels] et [Suivez-nous sur Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="bf1bf-107">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <span data-ttu-id="bf1bf-108">Améliorations de l’accessibilité dans DevTools</span><span class="sxs-lookup"><span data-stu-id="bf1bf-108">Accessibility improvements to the DevTools</span></span>  

<span data-ttu-id="bf1bf-109">L’équipe DevTools a 170 contribué aux modifications apportées à Chrome pour répondre aux problèmes de contraste des couleurs, de clavier et de lecteur d’écran à forte incidence dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="bf1bf-109">The DevTools team has contributed 170 changes to Chromium to address high-impact color contrast, keyboard, and screen reader issues in the DevTools.</span></span>  <span data-ttu-id="bf1bf-110">Tout développeur bâtiment sur le Web doit être en mesure d’utiliser le DevTools.</span><span class="sxs-lookup"><span data-stu-id="bf1bf-110">Every developer building the web should be able to use the DevTools.</span></span>  

> ##### <span data-ttu-id="bf1bf-111">Figure1</span><span class="sxs-lookup"><span data-stu-id="bf1bf-111">Figure 1</span></span>  
> <span data-ttu-id="bf1bf-112">Outil performance dans le DevTools avec les améliorations de la navigation au clavier et du lecteur d’écran</span><span class="sxs-lookup"><span data-stu-id="bf1bf-112">The Performance tool in the DevTools with the keyboard navigation and screen reader improvements</span></span>  
> ![Outil performance dans le DevTools avec les améliorations de la navigation au clavier et du lecteur d’écran][ImagePerformanceToolKeyboardReaderImprovements]  

<span data-ttu-id="bf1bf-114">Vous voulez savoir comment rendre votre page Web accessible à tous vos utilisateurs?</span><span class="sxs-lookup"><span data-stu-id="bf1bf-114">Want to learn how to make your web page accessible to all of your users?</span></span>  <span data-ttu-id="bf1bf-115">Téléchargez les informations [d’accessibilité][AccessibilityInsights] et les extensions [Webhint][WebhintBrowserExtension] pour Microsoft Edge pour commencer.</span><span class="sxs-lookup"><span data-stu-id="bf1bf-115">Download the [Accessibility Insights][AccessibilityInsights] and [webhint][WebhintBrowserExtension] extensions for Microsoft Edge to get started.</span></span>  

<span data-ttu-id="bf1bf-116">Si vous utilisez un lecteur d’écran ou le clavier pour naviguer dans DevTools, envoyez-nous vos commentaires en nous appuyant sur un [Tweet][PostTweetEdgeDevTools] ou en cliquant sur l’icône d' [envoi de commentaires](#getting-in-touch-with-microsoft-edge-devtools-team) .</span><span class="sxs-lookup"><span data-stu-id="bf1bf-116">If you use screen readers or the keyboard to navigate around the DevTools, send us your feedback by [tweeting][PostTweetEdgeDevTools] at us or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="bf1bf-117">[#963183][crbug963183] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="bf1bf-117">Chromium issue [#963183][crbug963183]</span></span>  

### <span data-ttu-id="bf1bf-118">Utiliser le DevTools dans d’autres langues</span><span class="sxs-lookup"><span data-stu-id="bf1bf-118">Using the DevTools in other languages</span></span>  

<span data-ttu-id="bf1bf-119">De nombreux développeurs utilisent d’autres outils de développement tels que StackOverflow et le code VS, dans leur langue maternelle, et pas seulement en anglais.</span><span class="sxs-lookup"><span data-stu-id="bf1bf-119">Many developers use other developer tools, like StackOverflow and VS Code, in their native language, not just in English.</span></span>  <span data-ttu-id="bf1bf-120">Nous sommes heureux d’annoncer la localisation de DevTools, que vous pouvez désormais utiliser dans l’un des 10 langues autres que l’anglais:</span><span class="sxs-lookup"><span data-stu-id="bf1bf-120">We’re excited to announce localization for the DevTools, which you are now able to use in one of 10 languages besides English:</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="bf1bf-121">Chinois (simplifié)- &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span><span class="sxs-lookup"><span data-stu-id="bf1bf-121">Chinese \(Simplified\) - &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="bf1bf-122">Chinois (traditionnel)- &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span><span class="sxs-lookup"><span data-stu-id="bf1bf-122">Chinese \(Traditional\) - &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="bf1bf-123">Français-Fran&#231;AIS</span><span class="sxs-lookup"><span data-stu-id="bf1bf-123">French – fran&#231;ais</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="bf1bf-124">Allemand-Deutsch</span><span class="sxs-lookup"><span data-stu-id="bf1bf-124">German - deutsch</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="bf1bf-125">Italien-Italiano</span><span class="sxs-lookup"><span data-stu-id="bf1bf-125">Italian - italiano</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="bf1bf-126">Japonais- &#26085;&#26412;&#35486;</span><span class="sxs-lookup"><span data-stu-id="bf1bf-126">Japanese - &#26085;&#26412;&#35486;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="bf1bf-127">Coréen- &#54620;&#44397;&#50612;</span><span class="sxs-lookup"><span data-stu-id="bf1bf-127">Korean - &#54620;&#44397;&#50612;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="bf1bf-128">Portugais-portugu&#234;s</span><span class="sxs-lookup"><span data-stu-id="bf1bf-128">Portuguese - portugu&#234;s</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="bf1bf-129">Russe- &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span><span class="sxs-lookup"><span data-stu-id="bf1bf-129">Russian – &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="bf1bf-130">Espagnol-ESPA&#241;ol</span><span class="sxs-lookup"><span data-stu-id="bf1bf-130">Spanish - espa&#241;ol</span></span>
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

<span data-ttu-id="bf1bf-131">Le DevTools correspond automatiquement à la langue que vous utilisez pour Microsoft Edge dans `edge://settings/languages` .</span><span class="sxs-lookup"><span data-stu-id="bf1bf-131">The DevTools automatically match the language you use for Microsoft Edge in `edge://settings/languages`.</span></span>  

<span data-ttu-id="bf1bf-132">Si vous voulez que Microsoft Edge soit dans une langue et que votre DevTools reste en anglais, appuyez sur `F1` la devtools pour ouvrir les [paramètres][Settings] et désactiver respecter la **langue du navigateur**.</span><span class="sxs-lookup"><span data-stu-id="bf1bf-132">If you want Microsoft Edge to be in one language and your DevTools to remain in English, press `F1` in the DevTools to open [Settings][Settings] and disable **Match browser language**.</span></span>  

> ##### <span data-ttu-id="bf1bf-133">Figure 2</span><span class="sxs-lookup"><span data-stu-id="bf1bf-133">Figure 2</span></span>  
> <span data-ttu-id="bf1bf-134">DevTools en allemand</span><span class="sxs-lookup"><span data-stu-id="bf1bf-134">The DevTools in German</span></span>  
> ![DevTools en allemand][ImageLocalizedGerman]  

<span data-ttu-id="bf1bf-136">Les messages de **console** ne sont pas localisés.</span><span class="sxs-lookup"><span data-stu-id="bf1bf-136">**Console** messages are not localized.</span></span>  <span data-ttu-id="bf1bf-137">Seules les chaînes utilisées dans l’interface utilisateur DevTools sont affichées dans la langue que vous utilisez pour Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="bf1bf-137">Only the strings used in the DevTools UI are displayed in the language you use for Microsoft Edge.</span></span>  

<span data-ttu-id="bf1bf-138">Si vous souhaitez utiliser le DevTools dans une autre langue que celle proposée, vous pouvez utiliser le [Tweet][PostTweetEdgeDevTools] ou cliquez sur l’icône d' [envoi de commentaires](#getting-in-touch-with-microsoft-edge-devtools-team) .</span><span class="sxs-lookup"><span data-stu-id="bf1bf-138">If you want to use the DevTools in a different language than the ones that are available, [tweet][PostTweetEdgeDevTools] at us or click the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon.</span></span>  

<span data-ttu-id="bf1bf-139">[#941561][crbug941561] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="bf1bf-139">Chromium issue [#941561][crbug941561]</span></span>  

### <span data-ttu-id="bf1bf-140">extension Microsoft Edge de webhint</span><span class="sxs-lookup"><span data-stu-id="bf1bf-140">webhint Microsoft Edge extension</span></span>  

<span data-ttu-id="bf1bf-141">L’extension Microsoft Edge de Microsoft vous permet d’analyser facilement votre page Web et de faire des commentaires sur l’accessibilité, la compatibilité avec les navigateurs, la sécurité et les performances, etc., dans le DevTools.</span><span class="sxs-lookup"><span data-stu-id="bf1bf-141">The webhint Microsoft Edge extension allows you to easily scan your web page and get feedback on accessibility, browser compatibility, security, performance, and more within the DevTools.</span></span>  <span data-ttu-id="bf1bf-142">Pour en savoir plus [https://webhint.io][Webhint] , voir.</span><span class="sxs-lookup"><span data-stu-id="bf1bf-142">Read more at [https://webhint.io][Webhint].</span></span>  

> ##### <span data-ttu-id="bf1bf-143">Figure3</span><span class="sxs-lookup"><span data-stu-id="bf1bf-143">Figure 3</span></span>  
> <span data-ttu-id="bf1bf-144">Onglet Hints dans le DevTools lorsque l’extension de navigateur webhint est installée</span><span class="sxs-lookup"><span data-stu-id="bf1bf-144">The Hints tab in the DevTools when the webhint browser extension is installed</span></span>  
> ![Onglet Hints dans le DevTools lorsque l’extension de navigateur webhint est installée][ImageHintsTabWebhintExtension]  

<span data-ttu-id="bf1bf-146">[Essayez l’extension de navigateur webhint dans Microsoft Edge][MicrosoftEdgeInsiderAddons].</span><span class="sxs-lookup"><span data-stu-id="bf1bf-146">[Try the webhint browser extension in Microsoft Edge][MicrosoftEdgeInsiderAddons].</span></span>  <span data-ttu-id="bf1bf-147">Une fois l’extension installée, ouvrez le DevTools et sélectionnez l’onglet conseils.  À partir de là, effectuez une analyse de site personnalisable.</span><span class="sxs-lookup"><span data-stu-id="bf1bf-147">Once you install the extension, open the DevTools and select the Hints tab.  From here, run a customizable site scan.</span></span>  <span data-ttu-id="bf1bf-148">Accédez à [webhint.IO][WebhintBrowserExtension] pour en savoir plus.</span><span class="sxs-lookup"><span data-stu-id="bf1bf-148">Head over to [webhint.io][WebhintBrowserExtension] to learn more.</span></span>  

### <span data-ttu-id="bf1bf-149">Vue 3D</span><span class="sxs-lookup"><span data-stu-id="bf1bf-149">3D View</span></span>  

<span data-ttu-id="bf1bf-150">Utilisez la **vue 3D** pour déboguer votre application Web en naviguant dans le [modèle d’objet de document \ (DOM \)][MDNDocumentObjectModel] ou le contexte de pile [de l’index z][MDNZIndex] .</span><span class="sxs-lookup"><span data-stu-id="bf1bf-150">Use the **3D View** to debug your web application by navigating through the [Document Object Model \(DOM\)][MDNDocumentObjectModel] or the [z-index][MDNZIndex] stacking context.</span></span>  

> ##### <span data-ttu-id="bf1bf-151">Figure 4</span><span class="sxs-lookup"><span data-stu-id="bf1bf-151">Figure 4</span></span>  
> <span data-ttu-id="bf1bf-152">Affichage 3D dans le DevTools</span><span class="sxs-lookup"><span data-stu-id="bf1bf-152">The 3D View in the DevTools</span></span>  
> ![Affichage 3D dans le DevTools][Image3DView]  

<span data-ttu-id="bf1bf-154">Pour accéder à l’affichage 3D, appuyez sur la touche `Ctrl`  +  `Shift`  +  `P` **affichage** 3D et sélectionnez **afficher la vue 3D**.</span><span class="sxs-lookup"><span data-stu-id="bf1bf-154">To access the 3D View, press `Ctrl` + `Shift` + `P`, type in **3D View** and select **Show 3D View**.</span></span>  

<span data-ttu-id="bf1bf-155">Nous travaillons sur l’interface utilisateur et nous ajoutons d’autres fonctionnalités à l’affichage 3D; nous vous envoyons donc votre [avis](#getting-in-touch-with-microsoft-edge-devtools-team).</span><span class="sxs-lookup"><span data-stu-id="bf1bf-155">We're working on the UI and adding more functionality to the 3D View, so please send us your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team).</span></span>  

<span data-ttu-id="bf1bf-156">[#987787][crbug987787] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="bf1bf-156">Chromium issue [#987787][crbug987787]</span></span>  

### <span data-ttu-id="bf1bf-157">Extensions de code Visual Studio</span><span class="sxs-lookup"><span data-stu-id="bf1bf-157">Visual Studio Code extensions</span></span>  

<span data-ttu-id="bf1bf-158">L’équipe DevTools a également émis certaines extensions pour le [code Visual Studio \ (vs code \)][VisualStudioCode] qui vous permettent d’utiliser la puissance de devtools directement à partir de votre éditeur de texte.</span><span class="sxs-lookup"><span data-stu-id="bf1bf-158">The DevTools team has also released some extensions for [Visual Studio Code \(VS Code\)][VisualStudioCode] that let you use the power of the DevTools directly from your text editor!</span></span> <span data-ttu-id="bf1bf-159">Consultez les extensions suivantes:</span><span class="sxs-lookup"><span data-stu-id="bf1bf-159">Check out the extensions below:</span></span>  

#### <span data-ttu-id="bf1bf-160">Éléments pour Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="bf1bf-160">Elements for Microsoft Edge</span></span>  

<span data-ttu-id="bf1bf-161">Utilisez l’outil éléments du code VS, en ajoutant les éléments de l’extension du code [Microsoft Edge \ (chrome \)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] .</span><span class="sxs-lookup"><span data-stu-id="bf1bf-161">Use the Elements tool from within VS Code by adding the [Elements for Microsoft Edge \(Chromium\)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] VS Code extension.</span></span>  

> ##### <span data-ttu-id="bf1bf-162">Figure 5</span><span class="sxs-lookup"><span data-stu-id="bf1bf-162">Figure 5</span></span>  
> <span data-ttu-id="bf1bf-163">L’outil éléments dans le code VS en utilisant les éléments pour l’extension Microsoft Edge et l' ![ outil éléments en utilisant les éléments de l’extension Microsoft Edge][ImageElementsVisualStudioCode]</span><span class="sxs-lookup"><span data-stu-id="bf1bf-163">The Elements tool in VS Code using the Elements for Microsoft Edge extension ![The Elements tool in VS Code using the Elements for Microsoft Edge extension][ImageElementsVisualStudioCode]</span></span>  

<span data-ttu-id="bf1bf-164">Pour plus d’informations, consultez les [éléments pour l’extension de code Microsoft Edge vs][VisualStudioCodeElementEdgeExtension].</span><span class="sxs-lookup"><span data-stu-id="bf1bf-164">For more information, check out [Elements for Microsoft Edge VS Code extension][VisualStudioCodeElementEdgeExtension].</span></span>  

#### <span data-ttu-id="bf1bf-165">Débogueur pour Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="bf1bf-165">Debugger for Microsoft Edge</span></span>  

<span data-ttu-id="bf1bf-166">Avec le [débogueur pour l’extension de code Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] vs, déboguez JavaScript en cours d’exécution dans Microsoft Edge directement à partir du code vs.</span><span class="sxs-lookup"><span data-stu-id="bf1bf-166">With the [Debugger for Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] VS Code extension, debug JavaScript running in Microsoft Edge directly from VS Code!</span></span>  

> ##### <span data-ttu-id="bf1bf-167">Figure 6</span><span class="sxs-lookup"><span data-stu-id="bf1bf-167">Figure 6</span></span>  
> <span data-ttu-id="bf1bf-168">Débogueur de l’extension Microsoft Edge dans le code VS</span><span class="sxs-lookup"><span data-stu-id="bf1bf-168">The Debugger for Microsoft Edge Extension in VS Code</span></span>  
> ![Débogueur de l’extension Microsoft Edge dans le code VS][ImageDebuggerExtensionVisualStudioCode]  

<span data-ttu-id="bf1bf-170">Pour plus d’informations, voir [Comment déboguer Microsoft Edge du code vs][VisualStudioCodeDebuggerEdgeExtension].</span><span class="sxs-lookup"><span data-stu-id="bf1bf-170">For more information, check out [how to debug Microsoft Edge from VS Code][VisualStudioCodeDebuggerEdgeExtension].</span></span>  

#### <span data-ttu-id="bf1bf-171">webhint</span><span class="sxs-lookup"><span data-stu-id="bf1bf-171">webhint</span></span>  

<span data-ttu-id="bf1bf-172">L’extension de code [webhint][VisualStudioMarketplaceWebhintExtension] et `webhint` de code vous permet d’améliorer votre page Web lorsque vous rédigez un message.</span><span class="sxs-lookup"><span data-stu-id="bf1bf-172">The [webhint][VisualStudioMarketplaceWebhintExtension] VS Code extension uses `webhint` to improve your web page while you're writing it!</span></span> <span data-ttu-id="bf1bf-173">Cette extension exécute et signale les diagnostics de vos fichiers d’espace de travail en fonction de l' `webhint` analyse.</span><span class="sxs-lookup"><span data-stu-id="bf1bf-173">This extension runs and reports diagnostics on your workspace files based on `webhint` analysis.</span></span>  

> ##### <span data-ttu-id="bf1bf-174">Figure 7</span><span class="sxs-lookup"><span data-stu-id="bf1bf-174">Figure 7</span></span>  
> <span data-ttu-id="bf1bf-175">Extension de code webhint et analyse d’un fichier. TSX dans le code VS</span><span class="sxs-lookup"><span data-stu-id="bf1bf-175">The webhint VS Code extension analyzing a .tsx file in VS Code</span></span>  
> ![Extension de code webhint et analyse d’un fichier. TSX dans le code VS][ImageWebhintVisualStudioCodeExtensionWorkspace]  

<span data-ttu-id="bf1bf-177">[En savoir plus sur l’extension du webhint code vs][WebhintVisualStudioCodeExtension].</span><span class="sxs-lookup"><span data-stu-id="bf1bf-177">[Learn more about the VS Code webhint extension][WebhintVisualStudioCodeExtension].</span></span>  

### <span data-ttu-id="bf1bf-178">Intégration de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="bf1bf-178">Visual Studio integration</span></span>  

<span data-ttu-id="bf1bf-179">Dans Visual Studio 2019 version 16,2 ou ultérieure, utilisez le débogueur Visual Studio pour déboguer JavaScript en cours d’exécution dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="bf1bf-179">In Visual Studio 2019 version 16.2 or later, use the Visual Studio debugger to debug JavaScript running in Microsoft Edge.</span></span>  <span data-ttu-id="bf1bf-180">[Téléchargez Visual Studio 2019][MicrosoftVisualStudioDownloads] pour essayer cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="bf1bf-180">[Download Visual Studio 2019][MicrosoftVisualStudioDownloads] to try this feature out!</span></span>  

> ##### <span data-ttu-id="bf1bf-181">Figure8</span><span class="sxs-lookup"><span data-stu-id="bf1bf-181">Figure 8</span></span>  
> <span data-ttu-id="bf1bf-182">Visual Studio avec l’option de lancement de votre application Web dans Microsoft Edge Canaries, dev ou Beta</span><span class="sxs-lookup"><span data-stu-id="bf1bf-182">Visual Studio with the option to launch your web app in Microsoft Edge Canary, Dev, or Beta</span></span>  
> ![Visual Studio avec l’option de lancement de votre application Web dans Microsoft Edge Canaries, dev ou Beta][ImageVisualStudioLaunchWebApp]  

<span data-ttu-id="bf1bf-184">[Apprenez-en davantage sur le débogage de Microsoft Edge à partir de Visual Studio][MicrosoftVisualStudio].</span><span class="sxs-lookup"><span data-stu-id="bf1bf-184">[Learn more about debugging Microsoft Edge from Visual Studio][MicrosoftVisualStudio].</span></span>  

### <span data-ttu-id="bf1bf-185">Suivi des messages de la console de prévention</span><span class="sxs-lookup"><span data-stu-id="bf1bf-185">Tracking prevention Console messages</span></span>  

<span data-ttu-id="bf1bf-186">La prévention de suivi est une fonctionnalité unique de Microsoft Edge qui vous protège du suivi par des sites Web que vous n’avez pas encore visités.</span><span class="sxs-lookup"><span data-stu-id="bf1bf-186">Tracking prevention is a unique feature in Microsoft Edge that protects you from being tracked by websites you haven't visited before.</span></span>  <span data-ttu-id="bf1bf-187">Le paramètre de prévention du suivi par défaut est le mode équilibré, qui permet de bloquer des suivis tiers et des pistes malveillantes connues pour une interface qui équilibre la confidentialité et la compatibilité Web.</span><span class="sxs-lookup"><span data-stu-id="bf1bf-187">The default tracking prevention setting is Balanced mode, which blocks 3rd party trackers and known malicious trackers for an experience that balances privacy and web compatibility.</span></span>  <span data-ttu-id="bf1bf-188">Pour plus d’informations sur la compatibilité de votre page Web lorsque certains suivis sont bloqués, nous avons également ajouté des messages d’avertissement dans la console lorsqu’un suivi est bloqué.</span><span class="sxs-lookup"><span data-stu-id="bf1bf-188">To give you more insight into the compatibility of your web page when certain trackers are blocked, we've also added warning messages in the Console when a tracker is blocked.</span></span>  

> ##### <span data-ttu-id="bf1bf-189">Figure9</span><span class="sxs-lookup"><span data-stu-id="bf1bf-189">Figure 9</span></span>  
> <span data-ttu-id="bf1bf-190">Messages dans la console lors du suivi de la prévention bloquer l’accès au stockage pour un suivi</span><span class="sxs-lookup"><span data-stu-id="bf1bf-190">Messages in the Console when tracking prevention blocks access to storage for a tracker</span></span>  
> ![Messages dans la console lors du suivi de la prévention bloquer l’accès au stockage pour un suivi][ImageTrackingPrevention]  

<span data-ttu-id="bf1bf-192">[En savoir plus sur la prévention de suivi et le compromis entre la confidentialité et la compatibilité Web][TrackingPrevention].</span><span class="sxs-lookup"><span data-stu-id="bf1bf-192">[Read more about tracking prevention and the balance between privacy and web compatibility][TrackingPrevention].</span></span>  

## <span data-ttu-id="bf1bf-193">Annonces du projet de chrome</span><span class="sxs-lookup"><span data-stu-id="bf1bf-193">Announcements from the Chromium project</span></span>  

<span data-ttu-id="bf1bf-194">Les sections suivantes annoncent des fonctionnalités supplémentaires disponibles dans Microsoft Edge 81 qui ont été fournies au projet de chrome Open source.</span><span class="sxs-lookup"><span data-stu-id="bf1bf-194">The following sections announce additional features available in Microsoft Edge 81 that were contributed to the open source Chromium project.</span></span>  

### <span data-ttu-id="bf1bf-195">Prise en charge de moto G4 en mode appareil</span><span class="sxs-lookup"><span data-stu-id="bf1bf-195">Moto G4 support in Device Mode</span></span>  

<span data-ttu-id="bf1bf-196">Après l' [activation de la barre d’outils de l’appareil][DeviceToolbar], simulez les dimensions d’une fenêtre d’affichage moto G4 de la liste des **appareils** .</span><span class="sxs-lookup"><span data-stu-id="bf1bf-196">After [enabling the Device Toolbar][DeviceToolbar], simulate the dimensions of a Moto G4 viewport from the **Device** list.</span></span>  

> ##### <span data-ttu-id="bf1bf-197">Figure10</span><span class="sxs-lookup"><span data-stu-id="bf1bf-197">Figure 10</span></span>  
> <span data-ttu-id="bf1bf-198">Simulation d’une fenêtre d’affichage moto G4</span><span class="sxs-lookup"><span data-stu-id="bf1bf-198">Simulating a Moto G4 viewport</span></span>  
> ![Simulation d’une fenêtre d’affichage moto G4][ImageMotoG4]  

<span data-ttu-id="bf1bf-200">Cliquez sur [afficher le cadre][DeviceFrame] de l’appareil pour afficher le matériel moto G4 dans la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="bf1bf-200">Click [Show Device Frame][DeviceFrame] to show the Moto G4 hardware around the viewport.</span></span>  

> ##### <span data-ttu-id="bf1bf-201">Figure11</span><span class="sxs-lookup"><span data-stu-id="bf1bf-201">Figure 11</span></span>  
> <span data-ttu-id="bf1bf-202">Affichage du matériel moto G4</span><span class="sxs-lookup"><span data-stu-id="bf1bf-202">Showing the Moto G4 hardware</span></span>  
> ![Affichage du matériel moto G4][ImageMotoG4Frame]  

<span data-ttu-id="bf1bf-204">Fonctionnalités connexes:</span><span class="sxs-lookup"><span data-stu-id="bf1bf-204">Related features:</span></span>  

*   <span data-ttu-id="bf1bf-205">Ouvrez le [menu de commandes][CommandMenu] et exécutez la `Capture screenshot` commande pour effectuer une capture d’écran de la fenêtre d’affichage qui inclut le matériel moto G4 (après avoir activé l’option **afficher le cadre**de l’appareil).</span><span class="sxs-lookup"><span data-stu-id="bf1bf-205">Open the [Command Menu][CommandMenu] and run the `Capture screenshot` command to take a screenshot of the viewport that includes the Moto G4 hardware (after enabling **Show Device Frame**).</span></span>  
*   <span data-ttu-id="bf1bf-206">[Limitez le réseau et le processeur][ThrottleNetworkAndCpu] pour simuler plus précisément les conditions de navigation sur le Web des utilisateurs mobiles.</span><span class="sxs-lookup"><span data-stu-id="bf1bf-206">[Throttle the network and CPU][ThrottleNetworkAndCpu] to more accurately simulate a mobile user's web browsing conditions.</span></span>  

<span data-ttu-id="bf1bf-207">[#924693][crbug924693] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="bf1bf-207">Chromium issue [#924693][crbug924693]</span></span>  

### <span data-ttu-id="bf1bf-208">Mises à jour associées au cookie;</span><span class="sxs-lookup"><span data-stu-id="bf1bf-208">Cookie-related updates</span></span>  

#### <span data-ttu-id="bf1bf-209">Cookies bloqués dans le volet cookies</span><span class="sxs-lookup"><span data-stu-id="bf1bf-209">Blocked cookies in the Cookies pane</span></span>  

<span data-ttu-id="bf1bf-210">Le volet cookies du panneau application affiche désormais les cookies bloqués avec un arrière-plan jaune.</span><span class="sxs-lookup"><span data-stu-id="bf1bf-210">The Cookies pane in the Application panel now displays blocked cookies with a yellow background.</span></span>  

> ##### <span data-ttu-id="bf1bf-211">Figure12</span><span class="sxs-lookup"><span data-stu-id="bf1bf-211">Figure 12</span></span>  
> <span data-ttu-id="bf1bf-212">Cookies bloqués dans le volet cookies du panneau application</span><span class="sxs-lookup"><span data-stu-id="bf1bf-212">Blocked cookies in the Cookies pane of the Application panel</span></span>  
> ![Cookies bloqués dans le volet cookies du panneau application][ImageBlockedCookies]  

<span data-ttu-id="bf1bf-214">[#1030258][crbug|::ref1::|] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="bf1bf-214">Chromium issue [#1030258][crbug|::ref1::|]</span></span>  

#### <span data-ttu-id="bf1bf-215">Priorité de cookie dans le volet cookie</span><span class="sxs-lookup"><span data-stu-id="bf1bf-215">Cookie priority in the Cookie pane</span></span>  

<span data-ttu-id="bf1bf-216">Les tables cookies dans les panneaux réseau et application incluent désormais une colonne de **priorité** .</span><span class="sxs-lookup"><span data-stu-id="bf1bf-216">The Cookies tables in the Network and Application panels now include a **Priority** column.</span></span>  

> [!CAUTION]
> <span data-ttu-id="bf1bf-217">Les navigateurs de type chrome, tels que Microsoft Edge, sont les seuls navigateurs qui prennent en charge la priorité des cookies.</span><span class="sxs-lookup"><span data-stu-id="bf1bf-217">Chromium-based browsers, like Microsoft Edge, are the only browsers that support cookie priority.</span></span>  

<span data-ttu-id="bf1bf-218">[#1026879][crbug1026879] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="bf1bf-218">Chromium issue [#1026879][crbug1026879]</span></span>  

#### <span data-ttu-id="bf1bf-219">Modifier toutes les valeurs de cookie</span><span class="sxs-lookup"><span data-stu-id="bf1bf-219">Edit all cookie values</span></span>  

<span data-ttu-id="bf1bf-220">Toutes les cellules des tables cookie sont modifiables, à l’exception des cellules de la colonne **taille** , car cette colonne représente la taille du réseau du cookie, en octets.</span><span class="sxs-lookup"><span data-stu-id="bf1bf-220">All cells in the Cookie tables are editable now, except cells in the **Size** column because that column represents the network size of the cookie, in bytes.</span></span>  <span data-ttu-id="bf1bf-221">Pour obtenir une description de chaque colonne, voir [champs][CookiesFields] .</span><span class="sxs-lookup"><span data-stu-id="bf1bf-221">See [Fields][CookiesFields] for an explanation of each column.</span></span>  

> ##### <span data-ttu-id="bf1bf-222">Figure13</span><span class="sxs-lookup"><span data-stu-id="bf1bf-222">Figure 13</span></span>  
> <span data-ttu-id="bf1bf-223">Modification d’une valeur de cookie</span><span class="sxs-lookup"><span data-stu-id="bf1bf-223">Editing a cookie value</span></span>  
> ![Modification d’une valeur de cookie][ImageEditCookie]  

#### <span data-ttu-id="bf1bf-225">Copy As Node.js FETCH pour inclure des données de cookie</span><span class="sxs-lookup"><span data-stu-id="bf1bf-225">Copy as Node.js fetch to include cookie data</span></span>  

<span data-ttu-id="bf1bf-226">Cliquez avec le bouton droit sur une demande réseau et sélectionnez **copier**la  >  **copie sous Node.js récupérer** pour obtenir une `fetch` expression incluant des données de cookie.</span><span class="sxs-lookup"><span data-stu-id="bf1bf-226">Right-click a network request and select **Copy** > **Copy as Node.js fetch** to get a `fetch` expression that includes cookie data.</span></span>  

> ##### <span data-ttu-id="bf1bf-227">Figure14</span><span class="sxs-lookup"><span data-stu-id="bf1bf-227">Figure 14</span></span>  
> <span data-ttu-id="bf1bf-228">Copy As Node.js Fetch</span><span class="sxs-lookup"><span data-stu-id="bf1bf-228">Copy as Node.js fetch</span></span>  
> ![Copy As Node.js Fetch][ImageCopyFetch]  

<span data-ttu-id="bf1bf-230">[#1029826][crbug1029826] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="bf1bf-230">Chromium issue [#1029826][crbug1029826]</span></span>  

### <span data-ttu-id="bf1bf-231">Icônes de manifeste d’application Web plus précises</span><span class="sxs-lookup"><span data-stu-id="bf1bf-231">More accurate web app manifest icons</span></span>  

<span data-ttu-id="bf1bf-232">Auparavant, le volet manifeste du panneau d’application a envoyé ses propres demandes pour afficher les icônes du manifeste de l’application Web.</span><span class="sxs-lookup"><span data-stu-id="bf1bf-232">Previously, the Manifest pane in the Application panel sent its own requests in order to display web app manifest icons.</span></span>  <span data-ttu-id="bf1bf-233">DevTools affiche maintenant la même icône de manifeste que celle utilisée par Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="bf1bf-233">DevTools now shows the exact same manifest icon that Microsoft Edge uses.</span></span>  

> ##### <span data-ttu-id="bf1bf-234">Figure15</span><span class="sxs-lookup"><span data-stu-id="bf1bf-234">Figure 15</span></span>  
> <span data-ttu-id="bf1bf-235">Icônes du volet manifeste</span><span class="sxs-lookup"><span data-stu-id="bf1bf-235">Icons in the Manifest pane</span></span>  
> ![Icônes du volet manifeste][ImageManifestIcon]  

<span data-ttu-id="bf1bf-237">[#985402][crbug985402] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="bf1bf-237">Chromium issue [#985402][crbug985402]</span></span>  

### <span data-ttu-id="bf1bf-238">Survol des propriétés de contenu CSS pour afficher les valeurs sans échappement</span><span class="sxs-lookup"><span data-stu-id="bf1bf-238">Hover over CSS content properties to see unescaped values</span></span>  

<span data-ttu-id="bf1bf-239">Placez le pointeur de la souris sur la valeur d’une `content` propriété pour afficher la version sans échappement de la valeur.</span><span class="sxs-lookup"><span data-stu-id="bf1bf-239">Hover over the value of a `content` property to see the unescaped version of the value.</span></span>  

<span data-ttu-id="bf1bf-240">Par exemple, dans cette [démonstration][CSSContentDemo] , lorsque vous examinez le `p::after` Pseudo-élément, vous voyez une chaîne d’échappement dans le volet styles:</span><span class="sxs-lookup"><span data-stu-id="bf1bf-240">For example, in this [demo][CSSContentDemo] when you inspect the `p::after` pseudo-element you see an escaped string in the Styles pane:</span></span>  

> ##### <span data-ttu-id="bf1bf-241">Figure16</span><span class="sxs-lookup"><span data-stu-id="bf1bf-241">Figure 16</span></span>  
> <span data-ttu-id="bf1bf-242">Chaîne d’échappement</span><span class="sxs-lookup"><span data-stu-id="bf1bf-242">The escaped string</span></span>  
> ![Chaîne d’échappement][ImageEscapedString]  

<span data-ttu-id="bf1bf-244">Lorsque vous pointez sur la `content` valeur, vous voyez la valeur sans séquence d’échappement:</span><span class="sxs-lookup"><span data-stu-id="bf1bf-244">When you hover over the `content` value you see the unescaped value:</span></span>  

> ##### <span data-ttu-id="bf1bf-245">Figure17</span><span class="sxs-lookup"><span data-stu-id="bf1bf-245">Figure 17</span></span>  
> <span data-ttu-id="bf1bf-246">Valeur sans échappement</span><span class="sxs-lookup"><span data-stu-id="bf1bf-246">The unescaped value</span></span>  
> ![Valeur sans échappement][ImageUnescapedString]  

### <span data-ttu-id="bf1bf-248">Erreurs de carte source plus détaillées dans la console</span><span class="sxs-lookup"><span data-stu-id="bf1bf-248">More detailed source map errors in the Console</span></span>  

<span data-ttu-id="bf1bf-249">La console donne désormais plus de détails sur la raison pour laquelle une table source n’a pas pu être chargée ou analysée.</span><span class="sxs-lookup"><span data-stu-id="bf1bf-249">The Console now provides more detail on why a source map failed to load or parse.</span></span>  <span data-ttu-id="bf1bf-250">Auparavant, il vous suffit de fournir une erreur sans expliquer ce qui s’est passé.</span><span class="sxs-lookup"><span data-stu-id="bf1bf-250">Previously it just provided an error without explaining what went wrong.</span></span>  

> ##### <span data-ttu-id="bf1bf-251">Figure 18</span><span class="sxs-lookup"><span data-stu-id="bf1bf-251">Figure 18</span></span>  
> <span data-ttu-id="bf1bf-252">Erreur de chargement du mappage source dans la console</span><span class="sxs-lookup"><span data-stu-id="bf1bf-252">A source map loading error in the Console</span></span>  
> ![Erreur de chargement du mappage source dans la console][ImageSourcemapError]  

### <span data-ttu-id="bf1bf-254">Paramètre permettant de désactiver le défilement au-delà de la fin d’un fichier</span><span class="sxs-lookup"><span data-stu-id="bf1bf-254">Setting for disabling scrolling past the end of a file</span></span>  

<span data-ttu-id="bf1bf-255">Ouvrez [paramètres][Settings] , puis désactivez l’option les sources de **Préférences**  >  **Sources**  >  **autorisent le défilement au-delà de la fin du fichier** pour désactiver le comportement de l’interface utilisateur par défaut qui vous permet de faire défiler le fichier dans le volet **sources** .</span><span class="sxs-lookup"><span data-stu-id="bf1bf-255">Open [Settings][Settings] and then disable **Preferences** > **Sources** > **Allow scrolling past end of file** to disable the default UI behavior that allows you to scroll well past the end of a file in the **Sources** panel.</span></span>  

> ##### <span data-ttu-id="bf1bf-256">Figure 19</span><span class="sxs-lookup"><span data-stu-id="bf1bf-256">Figure 19</span></span>  
> <span data-ttu-id="bf1bf-257">Désactivation de l’option autoriser le défilement au- **delà de la fin du fichier** dans les paramètres</span><span class="sxs-lookup"><span data-stu-id="bf1bf-257">Disabling **Allow scrolling past end of file** in Settings</span></span>  
> ![Désactivation de l’option autoriser le défilement au-delà de la fin du fichier][ImageSettings]  

> ##### <span data-ttu-id="bf1bf-259">Figure 20</span><span class="sxs-lookup"><span data-stu-id="bf1bf-259">Figure 20</span></span>  
> <span data-ttu-id="bf1bf-260">Le défilement au-delà de la fin d’un fichier est désormais désactivé dans le panneau sources</span><span class="sxs-lookup"><span data-stu-id="bf1bf-260">Scrolling past the end of a file is now disabled in the Sources panel</span></span>  
> ![Le défilement au-delà de la fin d’un fichier est désormais désactivé dans le panneau sources][ImageScroll]  

## <span data-ttu-id="bf1bf-262">Télécharger les canaux Microsoft Edge preview</span><span class="sxs-lookup"><span data-stu-id="bf1bf-262">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="bf1bf-263">Si vous utilisez Windows ou macOS, envisagez d’utiliser les [canaux Microsoft Edge Preview][MicrosoftEdgePreviewChannels] comme navigateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="bf1bf-263">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="bf1bf-264">Les canaux d’aperçu vous permettent d’accéder aux dernières fonctionnalités de DevTools.</span><span class="sxs-lookup"><span data-stu-id="bf1bf-264">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="bf1bf-265">Contacter l’équipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="bf1bf-265">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- <<../../_shared/devtools-feedback.md>>  

<<../../_shared/canary.md>>  

<<../../_shared/discover.md>> -->  

<!-- image links -->  

[ImagePerformanceToolKeyboardReaderImprovements]: ../../images/2020/01/a11y-performance-tool.msft.gif "Figure 1: l’outil performance dans le DevTools avec les améliorations de la navigation au clavier et du lecteur d’écran"  
[ImageLocalizedGerman]: ../../images/2020/01/localized-devtools.msft.png "Figure 2: DevTools en allemand"  
[ImageHintsTabWebhintExtension]: ../../images/2020/01/webhint-browser-extension.msft.png "Figure 3: onglet hints de Microsoft Edge DevTools lorsque l’extension de navigateur webhint est installée"  
[Image3DView]: ../../images/2020/01/3dview.msft.png "Figure 4: affichage 3D dans Microsoft Edge DevTools"  
[ImageElementsVisualStudioCode]: ../../images/2020/01/elements-for-edge.msft.png "Figure 5: outil éléments du code VS utilisant les éléments de l’extension Microsoft Edge"  
[ImageDebuggerExtensionVisualStudioCode]: ../../images/2020/01/vscode-debugger.msft.png "Figure 6: débogueur de l’extension Microsoft Edge dans le code VS"  
[ImageWebhintVisualStudioCodeExtensionWorkspace]: ../../images/2020/01/webhint-vscode-extension.msft.png "Figure 7: l’extension de code webhint VS analyse des fichiers. TSX dans le code VS"  
[ImageVisualStudioLaunchWebApp]: ../../images/2020/01/vs.msft.png "Figure 8: Visual Studio avec l’option de lancement de votre application Web dans Microsoft Edge Canaries, dev ou Beta"  
[ImageTrackingPrevention]: ../../images/2020/01/tracking-prevention.msft.png "Figure 9: messages dans la console lors du suivi de la prévention blocage de l’accès au stockage pour un suivi" 
[ImageMotoG4]: ../../images/2020/01/motog4.msft.png "Figure 10: simulation d’une fenêtre d’affichage moto G4" 
[ImageMotoG4Frame]: ../../images/2020/01/motog4frame.msft.png "Figure 11: affichage du matériel moto G4" 
[ImageBlockedCookies]: ../../images/2020/01/blockedcookies.msft.png "Figure 12: cookies bloqués dans le volet cookies du panneau application"
[ImageEditCookie]: ../../images/2020/01/editcookie.msft.png "Figure 13: modification d’une valeur de cookie"
[ImageCopyFetch]: ../../images/2020/01/fetchcookies.msft.png "Figure 14: copier en tant que Node.js récupérer"
[ImageManifestIcon]: ../../images/2020/01/manifesticons.msft.png "Figure 15: icônes dans le volet manifeste"
[ImageEscapedString]: ../../images/2020/01/escapedstring.msft.png "Figure 16: chaîne d’échappement"
[ImageUnescapedString]: ../../images/2020/01/unescapedstring.msft.png "Figure 17: valeur sans échappement"
[ImageSourcemapError]: ../../images/2020/01/sourcemap.msft.png "Figure 18: erreur de chargement d’une carte source dans la console"
[ImageSettings]: ../../images/2020/01/settings.msft.png "Figure 19: désactivation de l’option autoriser le défilement au-delà de la fin du fichier dans les paramètres"
[ImageScroll]: ../../images/2020/01/scrollingsources.msft.png "Figure 20: le défilement au-delà de la fin d’un fichier est désormais désactivé dans le panneau sources"

<!-- links -->  

[DeviceToolbar]: ../../../device-mode/index.md#simulate-a-mobile-viewport "Simuler une fenêtre d’affichage mobile avec le mode appareil dans Microsoft Edge DevTools"
[DeviceFrame]: ../../../device-mode/index.md#show-device-frame "Sélectionnez Afficher l’image de l’appareil pour afficher l’image de l’appareil physique à l’intérieur de la fenêtre d’affichage."
[CommandMenu]: ../../../command-menu/index.md "Exécuter des commandes à l’aide du menu de commande de Microsoft Edge DevTools"  
[ThrottleNetworkAndCpu]: ../../../device-mode/index.md#throttle-the-network-and-cpu "Limitation du réseau et du processeur pour simuler plus précisément les conditions de navigation sur le Web des utilisateurs mobiles."
[crbug924693]: https://crbug.com/924693 "924693: demande de fonctionnalité: Ajouter moto G4 à la liste du mode appareil"
[crbug1030258]: https://crbug.com/1030258 "1030258"
[crbug1026879]: https://crbug.com/1026879 "1026879: l’onglet cookie de la console dev ne montre plus de priorité"
[CookiesFields]: ../../../storage/cookies.md#fields "Les champs de la table cookies"
[crbug1029826]: https://crbug.com/1029826 "1029826: onglet réseau-> cliquez avec le bouton droit pour demander-> copier-> Copy en tant que FETCH ne copie aucun cookie"
[crbug985402]: https://crbug.com/985402 "985402: les chaînes d’erreur d’icône de manifeste Web App sont confuses"
[CSSContentDemo]: https://mathiasbynens.github.io/css-dbg-stories/css-escapes.html "Démo pour le contenu CSS sans échappement"
[Settings]: ../../../customize/index.md#settings "Personnaliser Microsoft Edge DevTools avec des paramètres"
[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Publiez un tweet"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Nouveau problème-MicrosoftDocs/Edge-développeur"  
[TheWebWeWant]: https://aka.ms/webwewant "Le site Web de votre choix"
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Canaux Microsoft Edge preview"  
[VisualStudioCodeDebuggerEdgeExtension]: ../../../../visual-studio-code/debugger-for-edge.md "Débogueur pour l’extension de code Microsoft Edge VS"  
[VisualStudioCodeElementEdgeExtension]: ../../../../visual-studio-code/elements-for-edge.md "Éléments pour l’extension de code Microsoft Edge VS"  
[crbug963183]: https://crbug.com/963183 "963183-DevTools n’est pas conforme à la norme WCAG"
[crbug941561]: https://crbug.com/941561 "941561-localization du DevTools"
[crbug987787]: https://crbug.com/987787 "987787-affichage 3D de Dom"
[AccessibilityInsights]: https://aka.ms/a11yinsights "Insights sur l’accessibilité"  
[MicrosoftEdgeInsiderAddons]: https://aka.ms/webhint/edge-extension "Compléments Microsoft Edge Insider"  
[MicrosoftVisualStudio]: ../../../../visual-studio/index.md "Visual Studio"  
[MicrosoftVisualStudioDownloads]: https://aka.ms/vs/download "Télécharger Visual Studio 2019 pour Windows \ & Mac"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "DOM (Document Object Model) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "index z | MDN"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools compte Twitter"
[VisualStudioCode]: https://aka.ms/vscode "Code Visual Studio"  
[VisualStudioMarketplaceDebuggerEdge]: https://aka.ms/debugger4code "Débogueur pour Microsoft Edge-Visual Studio Marketplace"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://aka.ms/elements4code "Éléments pour Microsoft Edge \ (chrome \)-Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://aka.ms/webhint4code "webhint-Visual Studio Marketplace"
[Webhint]: https://aka.ms/webhint "Astuce"  
[WebhintBrowserExtension]: https://aka.ms/webhint/browser-extension "Extension du navigateur webhint | documentation webhint"  
[WebhintVisualStudioCodeExtension]: https://aka.ms/webhint/code-extension "Extension de code webhint et documentation webhint"  
[TrackingPrevention]: https://aka.ms/microsoftedge/tracking-prevention-blog "Amélioration de la prévention du suivi dans le billet de blog Microsoft Edge"

> [!NOTE]
> <span data-ttu-id="bf1bf-322">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="bf1bf-322">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="bf1bf-323">La page d’origine est disponible [ici](https://developers.google.com/web/updates/2020/01/devtools/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="bf1bf-323">The original page is found [here](https://developers.google.com/web/updates/2020/01/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="bf1bf-325">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="bf1bf-325">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  