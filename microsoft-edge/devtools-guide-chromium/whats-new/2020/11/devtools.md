---
description: Microsoft Edge sur Linux, conseils d’amélioration de webhint dans l’outil problèmes, nouvelles fonctionnalités de débogage du worker du service et plus.
title: Nouveautés de DevTools (Microsoft Edge 88)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/15/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.localizationpriority: high
ms.openlocfilehash: 7f4f9e2602d26b09a8b52a570c4caaaccc4f04f1
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439274"
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
# <a name="whats-new-in-devtools-microsoft-edge-88"></a><span data-ttu-id="21db9-104">Nouveautés de DevTools (Microsoft Edge 88)</span><span class="sxs-lookup"><span data-stu-id="21db9-104">What's New in DevTools (Microsoft Edge 88)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="microsoft-edge-and-microsoft-edge-driver-now-available-on-linux"></a><span data-ttu-id="21db9-105">Microsoft Edge et le pilote Microsoft Edge désormais disponible sur Linux</span><span class="sxs-lookup"><span data-stu-id="21db9-105">Microsoft Edge and Microsoft Edge Driver now available on Linux</span></span>  

<!-- Title: Microsoft Edge and Microsoft Edge Driver on Linux  -->  
<!-- Subtitle: Get Microsoft Edge Dev on Ubuntu, Debian, Fedora, and openSUSE distributions and start automating in CI/CD environments with Microsoft Edge Driver. -->  

<span data-ttu-id="21db9-106">Microsoft Edge dev est désormais pris en charge sur les distributions Ubuntu, Debian, Fedora et openSUSE.</span><span class="sxs-lookup"><span data-stu-id="21db9-106">Microsoft Edge Dev is now supported on Ubuntu, Debian, Fedora, and openSUSE distributions.</span></span>  <span data-ttu-id="21db9-107">Téléchargez et installez le Microsoft Edge dev `.deb` ou le `.rpm` package directement à partir du [site Microsoft Edge Insider][MicrosoftinsiderDownloadPlatformLinux] ou utilisez les outils de gestion des packages standard de votre distribution Linux.</span><span class="sxs-lookup"><span data-stu-id="21db9-107">Download and install the Microsoft Edge Dev `.deb` or `.rpm` package directly from the [Microsoft Edge Insider site][MicrosoftinsiderDownloadPlatformLinux] or use the standard package management tools of your Linux distribution.</span></span>  

<span data-ttu-id="21db9-108">Si vous utilisez un environnement Linux dans vos solutions \(CI/CD\) d’intégration et de remise en continu, vous pouvez également utiliser le pilote Microsoft Edge sur Linux.</span><span class="sxs-lookup"><span data-stu-id="21db9-108">If you are using a Linux environment in your continuous integration and delivery \(CI/CD\) solutions, Microsoft Edge Driver is also available on Linux.</span></span>  <span data-ttu-id="21db9-109">Pour commencer à automatiser Microsoft Edge Dev avec le pilote Microsoft Edge, accédez à la [page de téléchargements de pilotes Microsoft Edge][MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads].</span><span class="sxs-lookup"><span data-stu-id="21db9-109">To get started automating Microsoft Edge Dev with Microsoft Edge Driver, navigate to [Microsoft Edge Driver Downloads page][MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads].</span></span>  <span data-ttu-id="21db9-110">Pour obtenir de l’aide sur l’automatisation de Microsoft Edge Dev avec le pilote Microsoft Edge, accédez à [utilisation de WebDriver (chrome) pour l’automatisation des tests][WebDriverChromiumMain].</span><span class="sxs-lookup"><span data-stu-id="21db9-110">For help with automating Microsoft Edge Dev along with Microsoft Edge Driver, navigate to [Use WebDriver (Chromium) for test automation][WebDriverChromiumMain].</span></span>  

:::image type="complex" source="../../media/2020/11/edge-on-linux.msft.png" alt-text="DevTools dans Microsoft Edge sur Linux" lightbox="../../media/2020/11/edge-on-linux.msft.png":::
   <span data-ttu-id="21db9-112">DevTools dans Microsoft Edge sur Linux</span><span class="sxs-lookup"><span data-stu-id="21db9-112">DevTools in Microsoft Edge on Linux</span></span>  
:::image-end:::  

## <a name="improved-webhint-and-platform-tips-in-the-issues-tool"></a><span data-ttu-id="21db9-113">Amélioration des conseils de webhint et de plateforme dans l’outil des problèmes</span><span class="sxs-lookup"><span data-stu-id="21db9-113">Improved webhint and platform tips in the Issues tool</span></span>  

<!-- Title: Improvements to Issues tool and webhint integration  -->  
<!-- Subtitle: Categories and third-party filtering make it easier to survey issues in the Issues tool.  Issues surfaced by webhint now have improved code snippets and documentation links to help you fix problems in your website.  -->  

<span data-ttu-id="21db9-114">Un outil open source, [webhint][WebhintMain], fournit des commentaires en temps réel sur les sites web et les pages web locales.</span><span class="sxs-lookup"><span data-stu-id="21db9-114">An open-source tool, [webhint][WebhintMain], provides real-time feedback for websites and local webpages.</span></span>  <span data-ttu-id="21db9-115">À partir de la [version 85 de Microsoft Edge][WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel], consultez les commentaires sur le webhint dans l’outil des [problèmes][DevtoolsIssuesIndex].</span><span class="sxs-lookup"><span data-stu-id="21db9-115">Starting with [Microsoft Edge version 85][WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel], review webhint feedback in the [Issues][DevtoolsIssuesIndex] tool.</span></span>  <span data-ttu-id="21db9-116">Il est désormais plus facile de passer en revue les problèmes qui s’affichent dans l’outil de **problèmes** en ajoutant ces catégories.</span><span class="sxs-lookup"><span data-stu-id="21db9-116">Issues that appear in the **Issues** tool are now easier to review with the addition of the following categories.</span></span>  

*   [<span data-ttu-id="21db9-117">Accessibilité</span><span class="sxs-lookup"><span data-stu-id="21db9-117">Accessibility</span></span>][WebhintUserGuideHintsAccessibility]  
*   [<span data-ttu-id="21db9-118">Compatibilité</span><span class="sxs-lookup"><span data-stu-id="21db9-118">Compatibility</span></span>][WebhintUserGuideHintsCompatibility]  
*   [<span data-ttu-id="21db9-119">Niveau de performance</span><span class="sxs-lookup"><span data-stu-id="21db9-119">Performance</span></span>][WebhintUserGuideHintsPerformance]  
*   [<span data-ttu-id="21db9-120">Les pièges</span><span class="sxs-lookup"><span data-stu-id="21db9-120">Pitfalls</span></span>][WebhintUserGuideHintsPitfalls]  
*   [<span data-ttu-id="21db9-121">PWA</span><span class="sxs-lookup"><span data-stu-id="21db9-121">PWA</span></span>][WebhintUserGuideHintsPwa]  
*   [<span data-ttu-id="21db9-122">Sécurité</span><span class="sxs-lookup"><span data-stu-id="21db9-122">Security</span></span>][WebhintUserGuideHintsSecurity]  
    
<span data-ttu-id="21db9-123">Vous pouvez à présent filtrer les problèmes tiers à l’aide d’une nouvelle case à cocher.</span><span class="sxs-lookup"><span data-stu-id="21db9-123">You are now able to filter out third-party issues using a new checkbox.</span></span>  <span data-ttu-id="21db9-124">La fonctionnalité de filtre vous aide à masquer les problèmes liés au code de bibliothèques tierces ou d’autres sources.</span><span class="sxs-lookup"><span data-stu-id="21db9-124">The filter functionality helps you hide issues related to code from third-party libraries or other sources.</span></span>  

<span data-ttu-id="21db9-125">Pour vous aider à passer en revue les problèmes détectés par [webhint][WebhintMain], l’outil des**problèmes** affiche désormais ces informations.</span><span class="sxs-lookup"><span data-stu-id="21db9-125">To help you review issues revealed by [webhint][WebhintMain], the **Issues** tool now displays the following information.</span></span>  

*   <span data-ttu-id="21db9-126">Meilleurs extraits de code.</span><span class="sxs-lookup"><span data-stu-id="21db9-126">Improved code snippets.</span></span>  
*   <span data-ttu-id="21db9-127">Liens vers d’autres panneaux pertinents.</span><span class="sxs-lookup"><span data-stu-id="21db9-127">Links to other relevant panels.</span></span>  
*   <span data-ttu-id="21db9-128">Liens vers la documentation pour vous aider à résoudre les problèmes rencontrés sur votre site Web.</span><span class="sxs-lookup"><span data-stu-id="21db9-128">Links to documentation to help you fix problems in your website.</span></span>  
    
:::image type="complex" source="../../media/2020/11/issues-webhints.msft.png" alt-text="Outil des problèmes" lightbox="../../media/2020/11/issues-webhints.msft.png":::
   <span data-ttu-id="21db9-130">Outil des **problèmes**</span><span class="sxs-lookup"><span data-stu-id="21db9-130">**Issues** tool</span></span>  
:::image-end:::  

## <a name="composited-layers-are-now-in-3d-view"></a><span data-ttu-id="21db9-131">Les couches composites sont désormais en affichage 3D</span><span class="sxs-lookup"><span data-stu-id="21db9-131">Composited Layers are now in 3D View</span></span>  

<!-- Title: 3D View is now integrated with Composited Layers  -->  
<!-- Subtitle: Composited Layers are now in 3D View.  -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="21db9-132">Vous avez désormais la possibilité de visualiser les contenus de **calques** avec les valeurs d’index z et le modèle d’objet du document (DOM).</span><span class="sxs-lookup"><span data-stu-id="21db9-132">You may now visualize **Layers** content alongside z-index values and the Document Object Model \(DOM\).</span></span>  <span data-ttu-id="21db9-133">Cette fonctionnalité vous permet de déboguer sans basculer entre les outils d’[affichage 3D][Devtools3dViewIndex] et de **calques** .</span><span class="sxs-lookup"><span data-stu-id="21db9-133">This feature helps you debug without switching between the [3D view][Devtools3dViewIndex] and **Layers** tools as often.</span></span>  <span data-ttu-id="21db9-134">Pour une expérience complète de débogage, [l’affichage 3D et les couches composites sont désormais combinés][DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView].</span><span class="sxs-lookup"><span data-stu-id="21db9-134">For a comprehensive visual debugging experience, the [3D View and Composited Layers are now combined][DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView].</span></span>  

:::image type="complex" source="../../media/2020/11/experiments-layers.msft.png" alt-text="Volet des couches composites" lightbox="../../media/2020/11/experiments-layers.msft.png":::
   <span data-ttu-id="21db9-136">Volet des **couches composites**</span><span class="sxs-lookup"><span data-stu-id="21db9-136">**Composited Layers** pane</span></span>  
:::image-end:::  

## <a name="css-variable-definitions-in-styles-pane"></a><span data-ttu-id="21db9-137">Définitions des variables CSS dans le volet styles</span><span class="sxs-lookup"><span data-stu-id="21db9-137">CSS variable definitions in Styles pane</span></span>  

<!-- Title: Jump to CSS variable definitions  -->  
<!-- Subtitle: Choose any CSS variable to navigate directly to the definition in the Styles tool. -->  

<span data-ttu-id="21db9-138">Dans le volet **styles** , les [variables CSS][MdnUsingCssCustomProperties] sont désormais liées directement à chaque définition.</span><span class="sxs-lookup"><span data-stu-id="21db9-138">In the **Styles** pane, [CSS variables][MdnUsingCssCustomProperties] now link directly to each definition.</span></span>  <span data-ttu-id="21db9-139">Choisissez la variable pour afficher ou modifier facilement la définition de variables CSS.</span><span class="sxs-lookup"><span data-stu-id="21db9-139">Choose the variable to easily view or change the CSS variable definition.</span></span>  <span data-ttu-id="21db9-140">Dans l’exemple, DevTools affiche les attributs CSS pour `body` l’élément.</span><span class="sxs-lookup"><span data-stu-id="21db9-140">In the example, DevTools displays the CSS attributes for the `body` element.</span></span>  <span data-ttu-id="21db9-141">Pour afficher la définition de variable pour la `--theme-body-background` variable CSS, effectuez ces actions.</span><span class="sxs-lookup"><span data-stu-id="21db9-141">To display the variable definition for the `--theme-body-background` CSS variable, complete the following actions.</span></span>  

1.  <span data-ttu-id="21db9-142">Dans le volet **styles** , choisissez `var(--theme-body-background)` .</span><span class="sxs-lookup"><span data-stu-id="21db9-142">In the **Styles** pane, choose `var(--theme-body-background)`.</span></span>  
1.  <span data-ttu-id="21db9-143">Le volet **styles** affiche désormais la définition de la variable CSS `--theme-body-background`.</span><span class="sxs-lookup"><span data-stu-id="21db9-143">The **Styles** pane now displays the definition of the `--theme-body-background` CSS variable.</span></span>  
    
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/css-variable-support.msft.png" alt-text="Variable CSS liée au style" lightbox="../../media/2020/11/css-variable-support.msft.png":::
         <span data-ttu-id="21db9-145">Variable CSS liée au style</span><span class="sxs-lookup"><span data-stu-id="21db9-145">CSS variable linked to the style</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/css-variable-support-target.msft.png" alt-text="Variable CSS liée à la cible de style" lightbox="../../media/2020/11/css-variable-support-target.msft.png":::
         <span data-ttu-id="21db9-147">Variable CSS liée à la cible de style</span><span class="sxs-lookup"><span data-stu-id="21db9-147">CSS variable linked to style target</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="service-worker-debugging-improvements"></a><span data-ttu-id="21db9-148">Améliorations du débogage du worker du service</span><span class="sxs-lookup"><span data-stu-id="21db9-148">Service worker debugging improvements</span></span>  

<!-- Title:  Service worker debugging improvements in the Network, Application, and Sources tools  -->  
<!-- Subtitle:  Making service workers easier to debug for progressive web applications and more.  -->  

<span data-ttu-id="21db9-149">Ces nouvelles fonctionnalités dans les outils [réseau](#network-tool), [application](#application-tool)et [sources](#sources-tool) vous aident à créer votre [PWA][ProgressiveWebAppsIndex].</span><span class="sxs-lookup"><span data-stu-id="21db9-149">The following new features in the [Network](#network-tool), [Application](#application-tool), and [Sources](#sources-tool) tools help you build your [PWA][ProgressiveWebAppsIndex].</span></span>  <span data-ttu-id="21db9-150">Si vous éprouvez des difficultés à déboguer votre worker du service, utilisez ces fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="21db9-150">Use the following features when you have difficulty debugging your service worker.</span></span>  

<span data-ttu-id="21db9-151">Le routage de demande affiche les événements de `startup` et de `fetch` basés sur les requêtes réseau exécutées par le biais des workers du service.</span><span class="sxs-lookup"><span data-stu-id="21db9-151">Request routing displays the `startup` and `fetch` events based on the network requests that run through service workers.</span></span>  <span data-ttu-id="21db9-152">Les chronologies sont accessibles à partir de l'outil **Application** ou **Réseau**.</span><span class="sxs-lookup"><span data-stu-id="21db9-152">The timelines are accessed from either the **Application** or **Network** tool.</span></span>  <span data-ttu-id="21db9-153">Les chronologies sont utiles lorsque vous avez des problèmes avec les travailleurs de service et que vous voulez afficher si quelque chose ne va pas avec`startup` l'événement`fetch`.</span><span class="sxs-lookup"><span data-stu-id="21db9-153">The timelines help when you are having trouble with service workers and want to display if something is wrong with the `startup` or `fetch` event.</span></span>  

### <a name="application-tool"></a><span data-ttu-id="21db9-154">Outil de l’application</span><span class="sxs-lookup"><span data-stu-id="21db9-154">Application tool</span></span>  

<!-- Title: Open Network tool from the Service Workers pane  -->  
<!-- Subtitle: Display additional context when debugging a service worker.  -->  

<span data-ttu-id="21db9-155">Affichez les informations de routage de demande des workers du service avec le nouveau lien **demandes de réseau**.</span><span class="sxs-lookup"><span data-stu-id="21db9-155">View all service worker request routing information with the new **Network requests** link.</span></span>  <span data-ttu-id="21db9-156">Pour afficher un contexte supplémentaire lors du débogage du worker du service, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="21db9-156">To display additional context when debugging the service worker, complete the following actions.</span></span>  

1.  <span data-ttu-id="21db9-157">Accédez aux **workers du service**  >  **de l’application**.</span><span class="sxs-lookup"><span data-stu-id="21db9-157">Navigate to **Application** > **Service Workers**.</span></span>  
1.  <span data-ttu-id="21db9-158">Sélectionnez **demandes de réseau**.</span><span class="sxs-lookup"><span data-stu-id="21db9-158">Choose **Network requests**.</span></span>  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-requests.msft.png" alt-text="Ouvrir l’outil réseau à partir du volet workers du service" lightbox="../../media/2020/11/service-worker-application-network-requests.msft.png":::
       <span data-ttu-id="21db9-160">Ouvrir l’outil **réseau** à partir du volet **workers du service**</span><span class="sxs-lookup"><span data-stu-id="21db9-160">Open **Network** tool from the **Service Workers** pane</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="21db9-161">L’outil **réseau** s’ouvre dans le **tiroir** et affiche toutes les demandes réseau associées au worker du service.</span><span class="sxs-lookup"><span data-stu-id="21db9-161">The **Network** tool opens in the **drawer** and displays all service worker-related network requests.</span></span>  <span data-ttu-id="21db9-162">Les requêtes réseau sont filtrées à l’aide de `is:service-worker-intercepted`.</span><span class="sxs-lookup"><span data-stu-id="21db9-162">The network requests are filtered using `is:service-worker-intercepted`.</span></span>  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-drawer.msft.png" alt-text="Outil réseau dans un tiroir" lightbox="../../media/2020/11/service-worker-application-network-drawer.msft.png":::
       <span data-ttu-id="21db9-164">Outil **réseau** dans un **tiroir**</span><span class="sxs-lookup"><span data-stu-id="21db9-164">**Network** tool in **drawer**</span></span>  
    :::image-end:::
    
1. <span data-ttu-id="21db9-165">Pour rétablir le panneau supérieur de l’outil **réseau** , fermez le **tiroir**.</span><span class="sxs-lookup"><span data-stu-id="21db9-165">To return the **Network** tool to the top panel, close the **drawer**.</span></span>  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-return.msft.png" alt-text="Fermer le tiroir pour renvoyer l’outil réseau" lightbox="../../media/2020/11/service-worker-application-network-return.msft.png":::
       <span data-ttu-id="21db9-167">Fermez le **tiroir** pour renvoyer l’outil **réseau**.</span><span class="sxs-lookup"><span data-stu-id="21db9-167">Close the **drawer** to return **Network** tool</span></span>  
    :::image-end:::  
    
### <a name="network-tool"></a><span data-ttu-id="21db9-168">Outil réseau</span><span class="sxs-lookup"><span data-stu-id="21db9-168">Network tool</span></span>  

<span data-ttu-id="21db9-169">Déboguer les requêtes réseau qui s’exécutent par le biais des workersdu service.</span><span class="sxs-lookup"><span data-stu-id="21db9-169">Debug network requests that run through service workers.</span></span>  <span data-ttu-id="21db9-170">Vous pouvez également ouvrir des requêtes réseau à partir de l’outil de **l’application**.</span><span class="sxs-lookup"><span data-stu-id="21db9-170">You may also open network requests from the **Application** tool.</span></span>  <span data-ttu-id="21db9-171">Pour chaque demande, DevTools affiche ces informations dans le volet [chronométrage][DevtoolsNetworkReferenceViewTimingBreakdownRequest].</span><span class="sxs-lookup"><span data-stu-id="21db9-171">For each request, DevTools display the following information in the [Timing][DevtoolsNetworkReferenceViewTimingBreakdownRequest] pane.</span></span>  

*   <span data-ttu-id="21db9-172">Le début d’une demande et la durée du démarrage.</span><span class="sxs-lookup"><span data-stu-id="21db9-172">The start of a request and duration of the bootstrap.</span></span>  
*   <span data-ttu-id="21db9-173">Modification apportée à l’inscription du worker du service.</span><span class="sxs-lookup"><span data-stu-id="21db9-173">Changes to service worker registration.</span></span>  
*   <span data-ttu-id="21db9-174">Exécution d’un gestionnaire d’événements `fetch`.</span><span class="sxs-lookup"><span data-stu-id="21db9-174">The runtime of a `fetch` event handler.</span></span>  
*   <span data-ttu-id="21db9-175">Exécution de tous les événements `fetch` de chargement d’un client.</span><span class="sxs-lookup"><span data-stu-id="21db9-175">The runtime of all `fetch` events for loading a client.</span></span>  
    
:::image type="complex" source="../../media/2020/11/network-timing-service-worker.msft.png" alt-text="Volet chronométrage" lightbox="../../media/2020/11/network-timing-service-worker.msft.png":::
   <span data-ttu-id="21db9-177">Volet **chronométrage**</span><span class="sxs-lookup"><span data-stu-id="21db9-177">**Timing** pane</span></span>  
:::image-end:::  

### <a name="sources-tool"></a><span data-ttu-id="21db9-178">Outil sources</span><span class="sxs-lookup"><span data-stu-id="21db9-178">Sources tool</span></span>  

<span data-ttu-id="21db9-179">Dans les versions précédentes de Microsoft Edge, le niveau de profondeur de la pile d’appels était limité au code JavaScript de votre worker du service.</span><span class="sxs-lookup"><span data-stu-id="21db9-179">In previous versions of Microsoft Edge, the level of depth in the call stack was limited to the JavaScript code in your service worker.</span></span>  <span data-ttu-id="21db9-180">Dans Microsoft Edge 88, la pile d’appels affiche désormais l’initiateur de demandes qui s’exécutent par le biais de votre worker du service.</span><span class="sxs-lookup"><span data-stu-id="21db9-180">In Microsoft Edge 88, the call stack now displays the initiator of requests that run through your service worker.</span></span>  

<span data-ttu-id="21db9-181">Pour localiser l’initiateur de la requête, utilisez la pile d’appels de votre code JavaScript dans le worker du service.</span><span class="sxs-lookup"><span data-stu-id="21db9-181">To locate the initiator of the request, use the call stack of your JavaScript code in the service worker.</span></span>  <span data-ttu-id="21db9-182">La pile d’appels dans ces illustrations commence par le code JavaScript de votre worker du service et affiche une référence à la demande de page Web d’origine en tant que `(index):157`.</span><span class="sxs-lookup"><span data-stu-id="21db9-182">The call stack in the following figures starts with the JavaScript code in your service worker and displays a reference to the original webpage request as `(index):157`.</span></span>  <span data-ttu-id="21db9-183">Dans la deuxième illustration, la référence est choisie et a ouvert l’initiateur qui a créé la demande.</span><span class="sxs-lookup"><span data-stu-id="21db9-183">In the second figure, the reference is chosen and opened the initiator that made the request.</span></span>  <span data-ttu-id="21db9-184">Dans la deuxième illustration, l’initiateur est la page web.</span><span class="sxs-lookup"><span data-stu-id="21db9-184">The initiator in the second figure is the webpage.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/service-worker-sources-stopped-at-breakpoint.msft.png" alt-text="Le fichier service-worker.js et la mise en surbrillance de la pile d’appels nécessitent un émetteur." lightbox="../../media/2020/11/service-worker-sources-stopped-at-breakpoint.msft.png":::
         <span data-ttu-id="21db9-186">Le fichier `service-worker.js` et la mise en surbrillance de la pile d’appels nécessitent un émetteur. </span><span class="sxs-lookup"><span data-stu-id="21db9-186">The `service-worker.js` file and call stack highlighting request originator</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/service-worker-sources-call-stack-target.msft.png" alt-text="La page web (index) est l’initiateur de la requête" lightbox="../../media/2020/11/service-worker-sources-call-stack-target.msft.png":::
         <span data-ttu-id="21db9-188">La page web `(index)` est l’initiateur de la requête</span><span class="sxs-lookup"><span data-stu-id="21db9-188">The `(index)` webpage is the request initiator</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="copy-property-value-of-a-network-request"></a><span data-ttu-id="21db9-189">Copier la valeur de la propriété d’une demande réseau</span><span class="sxs-lookup"><span data-stu-id="21db9-189">Copy property value of a network request</span></span>  

<!-- Title: Copy response JSON in Network tool using the contextual menu  -->  
<!-- Subtitle:  The Network tool now has a more consistent UX.  Easily copy the JSON response using the contextual menu.  -->  

<span data-ttu-id="21db9-190">Dans l’outil **réseau** , copiez la valeur de la propriété d’une demande réseau à l’aide de la nouvelle option **copier la valeur**.</span><span class="sxs-lookup"><span data-stu-id="21db9-190">In the **Network** tool, copy the property value of a network request using the new **Copy value** option.</span></span>  <span data-ttu-id="21db9-191">La valeur de la propriété est copiée en tant que valeur JSON décodée.</span><span class="sxs-lookup"><span data-stu-id="21db9-191">The property value is copied as a decoded JSON value.</span></span>  <span data-ttu-id="21db9-192">Dans les versions précédentes de Microsoft Edge, vous deviez copier une valeur à l’aide de l’une de ces actions.</span><span class="sxs-lookup"><span data-stu-id="21db9-192">In previous versions of Microsoft Edge, you had to copy a value using one of the following actions.</span></span>  

*   <span data-ttu-id="21db9-193">Mettez en surbrillance l’intégralité du texte et copiez-le.</span><span class="sxs-lookup"><span data-stu-id="21db9-193">Highlight the entire text and copy it.</span></span>  
*   <span data-ttu-id="21db9-194">Stockez la valeur en tant que variable globale, le cas échéant, puis copiez-la à partir de la [console][DevtoolsConsoleIndex]DevTools.</span><span class="sxs-lookup"><span data-stu-id="21db9-194">Store the value as global variable, as applicable, and copy it from the DevTools [Console][DevtoolsConsoleIndex].</span></span>  
    
<span data-ttu-id="21db9-195">Pour copier la valeur de la propriété dans le presse-papiers, accédez à [copier la valeur JSON de la réponse mise en forme dans le presse-papiers][DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard].</span><span class="sxs-lookup"><span data-stu-id="21db9-195">To copy the property value to your clipboard, navigate to [Copy formatted response JSON to the clipboard][DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard].</span></span>  <span data-ttu-id="21db9-196">Pour passer en revue l’historique de cette fonctionnalité dans le projet open-source Chromium, accédez à la section problème [1132084][CR1132084].</span><span class="sxs-lookup"><span data-stu-id="21db9-196">To review the history of this feature in the Chromium open-source project, navigate to Issue [1132084][CR1132084].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/copy-property-value.msft.png" alt-text="Copier la valeur de la propriété dans DevTools" lightbox="../../media/2020/11/copy-property-value.msft.png":::
         <span data-ttu-id="21db9-198">Copier la valeur d'une propriété dans DevTools</span><span class="sxs-lookup"><span data-stu-id="21db9-198">Copy property value in DevTools</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/paste-property-value.msft.png" alt-text="Coller la valeur d'une propriété dans Microsoft Visual Studio Code" lightbox="../../media/2020/11/paste-property-value.msft.png":::
         <span data-ttu-id="21db9-200">Coller la valeur d'une propriété dans Microsoft Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="21db9-200">Paste property value in Microsoft Visual Studio Code</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="customize-multi-press-keyboard-shortcuts"></a><span data-ttu-id="21db9-201">Personnaliser les raccourcis clavier multi-presses</span><span class="sxs-lookup"><span data-stu-id="21db9-201">Customize multi-press keyboard shortcuts</span></span>  

<!-- Title: Customize multi-press keyboard shortcuts  -->  
<!-- Subtitle: Create custom multi-press keyboard shortcuts in the shortcut editor.  -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::

<span data-ttu-id="21db9-202">[Depuis la version 87 de Microsoft Edge][WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings], vous pouvez personnaliser les raccourcis clavier pour n’importe quelle action dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="21db9-202">[Since Microsoft Edge version 87][WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings], you may customize keyboard shortcuts for any action in DevTools.</span></span>  <span data-ttu-id="21db9-203">Dans la version 88 de Microsoft Edge, vous pouvez désormais créer des raccourcis clavier à plusieurs clics.</span><span class="sxs-lookup"><span data-stu-id="21db9-203">In Microsoft Edge version 88, you may now create multi-press keyboard shortcuts.</span></span>  <span data-ttu-id="21db9-204">Pour définir un raccourci vers une action dans la DevTools, accédez à [paramètres][DevtoolsCustomizeIndexSettings] > **expérimentations** et cochez la case en regard de **activer l’éditeur de raccourcis clavier**.</span><span class="sxs-lookup"><span data-stu-id="21db9-204">To set a shortcut for an action in the DevTools, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments**  and choose the checkbox next to **Enable keyboard shortcut editor**.</span></span>  <span data-ttu-id="21db9-205">Pour plus d’informations sur la personnalisation et la modification des raccourcis, accédez à [activer la fonctionnalité expérimentale de l’éditeur de raccourcis clavier][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span><span class="sxs-lookup"><span data-stu-id="21db9-205">For more information about customizing and editing shortcuts, navigate to [Enable keyboard shortcut editor Experimental feature][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span></span>  

<span data-ttu-id="21db9-206">Par exemple, la mise en surbrillance rouge affiche un raccourci clavier à plusieurs clics personnalisé pour l’action **commencer l’enregistrement des événements**.</span><span class="sxs-lookup"><span data-stu-id="21db9-206">For example, the red highlight displays a multi-press keyboard shortcut customized for the **Start recording events** action.</span></span>  <span data-ttu-id="21db9-207">Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de Chromium, accédez à [problème #174309][CR174309].</span><span class="sxs-lookup"><span data-stu-id="21db9-207">To review real-time updates on this feature in the Chromium open-source project, navigate to [Issue #174309][CR174309].</span></span>  

:::image type="complex" source="../../media/2020/11/multi-press-keyboard-shortcuts.msft.png" alt-text="Raccourcis clavier des cordes" lightbox="../../media/2020/11/multi-press-keyboard-shortcuts.msft.png":::
   <span data-ttu-id="21db9-209">Raccourcis clavier à plusieurs clics</span><span class="sxs-lookup"><span data-stu-id="21db9-209">Multi-press keyboard shortcuts</span></span>  
:::image-end:::  

## <a name="devtools-now-match-browser-language"></a><span data-ttu-id="21db9-210">DevTools correspond désormais à la langue du navigateur</span><span class="sxs-lookup"><span data-stu-id="21db9-210">DevTools now match browser language</span></span>  

<span data-ttu-id="21db9-211">Dans Microsoft Edge version 87, si vous activiez le paramètre **respecter la langue du navigateur** dans [paramètres DevTools][DevtoolsCustomizeIndexSettings], DevTools ne correspondait pas à la langue du navigateur.</span><span class="sxs-lookup"><span data-stu-id="21db9-211">In Microsoft Edge version 87, if you turned on the **Match browser language** setting in [DevTools Settings][DevtoolsCustomizeIndexSettings], DevTools did not match the browser language.</span></span>  <span data-ttu-id="21db9-212">Dans Microsoft Edge version 88, DevTools correspond désormais à la langue du navigateur si vous activez le paramètre **respecter la langue du navigateur**.</span><span class="sxs-lookup"><span data-stu-id="21db9-212">In Microsoft Edge version 88, DevTools now matches the browser language if you turn on the **Match browser language** setting.</span></span>  <span data-ttu-id="21db9-213">Pour plus d’informations sur le paramètre **respecter la langue du navigateur** DevTools, accédez à [modifier les paramètres de langue DevTools][DevtoolsCustomizeLocalization].</span><span class="sxs-lookup"><span data-stu-id="21db9-213">For more information about the **Match browser language** DevTools Setting, navigate to [Change DevTools language settings][DevtoolsCustomizeLocalization].</span></span>  

:::image type="complex" source="../../media/2020/11/startpage-devtools-settings-japanese.msft.png" alt-text="Faire correspondre le paramètre DevTools de la langue du navigateur au japonais" lightbox="../../media/2020/11/startpage-devtools-settings-japanese.msft.png":::
   <span data-ttu-id="21db9-215">**Faire correspondre la langue du navigateur**relative au paramètre DevTools au japonais</span><span class="sxs-lookup"><span data-stu-id="21db9-215">**Match browser language** DevTools setting in Japanese</span></span>  
:::image-end:::  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="21db9-216">Annonces du projet de Chromium</span><span class="sxs-lookup"><span data-stu-id="21db9-216">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="new-css-angle-visualization-tools"></a><span data-ttu-id="21db9-217">Nouveaux outils de visualisation d’angle CSS</span><span class="sxs-lookup"><span data-stu-id="21db9-217">New CSS angle visualization tools</span></span>  

<span data-ttu-id="21db9-218">DevTools dispose désormais d’une meilleure prise en charge du débogage d’angle CSS.</span><span class="sxs-lookup"><span data-stu-id="21db9-218">DevTools now have better support for CSS angle debugging.</span></span>  <span data-ttu-id="21db9-219">Lorsqu’un élément HTML de votre page est doté d’un angle CSS appliqué, une icône d’horloge s’affiche à côté de l’angle dans l’outil **styles**.</span><span class="sxs-lookup"><span data-stu-id="21db9-219">When an HTML element on your page has CSS angle applied to it, a clock icon is displayed next to the angle in the **Styles** tool.</span></span>  <span data-ttu-id="21db9-220">Pour activer ou désactiver la superposition de l’horloge, sélectionnez l’icône d’horloge.</span><span class="sxs-lookup"><span data-stu-id="21db9-220">To toggle the clock overlay, choose the clock icon.</span></span>  <span data-ttu-id="21db9-221">Pour modifier l’angle, sélectionnez un emplacement quelconque dans l’horloge ou faites glisser l’aiguille.</span><span class="sxs-lookup"><span data-stu-id="21db9-221">To change the angle, choose anywhere in the clock or drag the needle.</span></span>  <span data-ttu-id="21db9-222">Pour modifier la valeur de l’angle, vous pouvez également utiliser la souris et les raccourcis clavier.</span><span class="sxs-lookup"><span data-stu-id="21db9-222">To change the angle value, you may also use mouse and keyboard shortcuts.</span></span>  <!--  To learn more, navigate to [Angle Clock][DevtoolsCssReferenceChangeAngleValueWithAngleClock].  -->  <span data-ttu-id="21db9-223">Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de Chromium, accédez aux problèmes [1126178][CR1126178] et [1138633][CR1138633].</span><span class="sxs-lookup"><span data-stu-id="21db9-223">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [1126178][CR1126178] and [1138633][CR1138633].</span></span>  

<!--todo:  add link when css angle clock section exists.  -->  

<span data-ttu-id="21db9-224">Cet angle CSS est utilisé pour l’exemple.</span><span class="sxs-lookup"><span data-stu-id="21db9-224">The following CSS angle is used for the example.</span></span>  

```css
background: linear-gradient(100deg, lightblue, pink);
```  

:::image type="complex" source="../../media/2020/11/css-angle.msft.png" alt-text="Angle CSS" lightbox="../../media/2020/11/css-angle.msft.png":::
   <span data-ttu-id="21db9-226">Angle CSS</span><span class="sxs-lookup"><span data-stu-id="21db9-226">CSS angle</span></span>  
:::image-end:::  

### <a name="simulate-storage-quota-size-in-the-storage-pane"></a><span data-ttu-id="21db9-227">Simuler une taille de quota de stockage dans le volet stockage</span><span class="sxs-lookup"><span data-stu-id="21db9-227">Simulate storage quota size in the Storage pane</span></span>  

<span data-ttu-id="21db9-228">Vous pouvez à présent remplacer la taille de quota de stockage dans le volet **stockage**.</span><span class="sxs-lookup"><span data-stu-id="21db9-228">You may now override storage quota size in the **Storage** pane.</span></span>  <span data-ttu-id="21db9-229">Cette fonctionnalité permet de simuler différents appareils et de tester le comportement de votre site web ou de votre application dans des scénarios de disponibilité du disque faible.</span><span class="sxs-lookup"><span data-stu-id="21db9-229">This feature allows you to simulate different devices and test the behavior of your website or app in low disk availability scenarios.</span></span>  <span data-ttu-id="21db9-230">Pour simuler le quota de stockage, effectuez ces actions.</span><span class="sxs-lookup"><span data-stu-id="21db9-230">To simulate the storage quota, complete the following actions.</span></span>  

1.  <span data-ttu-id="21db9-231">Accédez au **stockage** > **de l’application**.</span><span class="sxs-lookup"><span data-stu-id="21db9-231">Navigate to **Application** > **Storage**.</span></span>  
1.  <span data-ttu-id="21db9-232">Activez la case à cocher **simuler le quota de stockage personnalisé**.</span><span class="sxs-lookup"><span data-stu-id="21db9-232">Turn on the **Simulate custom storage quota** checkbox.</span></span>  
1.  <span data-ttu-id="21db9-233">Entrez un numéro valide.</span><span class="sxs-lookup"><span data-stu-id="21db9-233">Enter a valid number.</span></span>  
    
<span data-ttu-id="21db9-234">Pour plus d’informations sur la façon d’émuler des appareils mobiles et d’autres fonctionnalités dans le DevTools, accédez à la section [émuler des appareils mobiles dans Microsoft Edge DevTools ][DevtoolsDeviceModeIndex].</span><span class="sxs-lookup"><span data-stu-id="21db9-234">For more information about how to emulate mobile devices and other features in the DevTools, navigate to [Emulate mobile devices in Microsoft Edge DevTools ][DevtoolsDeviceModeIndex].</span></span>  <span data-ttu-id="21db9-235">Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de Chromium, accédez aux problèmes [945786][CR945786] et [1146985][CR1146985].</span><span class="sxs-lookup"><span data-stu-id="21db9-235">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [945786][CR945786] and [1146985][CR1146985].</span></span>  

:::image type="complex" source="../../media/2020/11/storage-quota.msft.png" alt-text="Simuler la taille de quota de stockage" lightbox="../../media/2020/11/storage-quota.msft.png":::
   <span data-ttu-id="21db9-237">Simuler la taille de quota de stockage</span><span class="sxs-lookup"><span data-stu-id="21db9-237">Simulate storage quota size</span></span>  
:::image-end:::  

### <a name="report-cors-errors-in-the-network-tool"></a><span data-ttu-id="21db9-238">Signaler les erreurs CORS dans l’outil réseau</span><span class="sxs-lookup"><span data-stu-id="21db9-238">Report CORS errors in the Network tool</span></span>  

<span data-ttu-id="21db9-239">Évaluez cette fonctionnalité en accédant à [version de démonstration d’erreur CORS][GlitchCorsErrors].</span><span class="sxs-lookup"><span data-stu-id="21db9-239">Try out this feature by navigating to [CORS error demo][GlitchCorsErrors].</span></span>  <span data-ttu-id="21db9-240">Ouvrez l’outil de **réseau** , actualisez la page et observez la requête de réseau CORS ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="21db9-240">Open the **Network** tool, refresh the page, and observe the failed CORS network request.</span></span>  <span data-ttu-id="21db9-241">La colonne état affiche **l’erreur CORS**.</span><span class="sxs-lookup"><span data-stu-id="21db9-241">The status column displays the **CORS error**.</span></span>  <span data-ttu-id="21db9-242">Lorsque vous placer le curseur sur l’erreur, l’info-bulle affiche maintenant le code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="21db9-242">When you hover on the error, the tooltip now displays the error code.</span></span>  <span data-ttu-id="21db9-243">Dans la version 87 et les versions antérieures de Microsoft Edge, DevTools affichait uniquement le statut générique **(échec)** pour les erreurs CORS.</span><span class="sxs-lookup"><span data-stu-id="21db9-243">In Microsoft Edge version 87 and earlier, DevTools only displayed generic **(failed)** status for CORS errors.</span></span>  <span data-ttu-id="21db9-244">Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de chrome, accédez au problème [1141824][CR1141824].</span><span class="sxs-lookup"><span data-stu-id="21db9-244">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [1141824][CR1141824].</span></span>  

:::image type="complex" source="../../media/2020/11/cors-err.msft.png" alt-text="Erreurs CORS" lightbox="../../media/2020/11/cors-err.msft.png":::
   <span data-ttu-id="21db9-246">Erreurs CORS</span><span class="sxs-lookup"><span data-stu-id="21db9-246">CORS errors</span></span>  
:::image-end:::  

### <a name="frame-details-view-updates"></a><span data-ttu-id="21db9-247">Mises à jour de l’affichage des détails du cadre</span><span class="sxs-lookup"><span data-stu-id="21db9-247">Frame details view updates</span></span>  

#### <a name="cross-origin-isolation-information-in-the-frame-details-view"></a><span data-ttu-id="21db9-248">Informations d’isolation de l’origine croisée dans l’affichage des détails du cadre</span><span class="sxs-lookup"><span data-stu-id="21db9-248">Cross-origin isolation information in the Frame details view</span></span>  

<span data-ttu-id="21db9-249">L’état isolé de l’origine croisée s’affiche désormais sous la section **sécurité & isolation**.</span><span class="sxs-lookup"><span data-stu-id="21db9-249">The cross-origin isolated status is now displayed under the **Security & Isolation** section.</span></span>  <span data-ttu-id="21db9-250">La nouvelle section **disponibilité de l’API** affiche la disponibilité de (SAB \) `SharedArrayBuffer` et si les mémoires tampons pourraient être partagées en utilisant `postMessage()`.</span><span class="sxs-lookup"><span data-stu-id="21db9-250">The new **API availability** section displays the availability of `SharedArrayBuffer`s \(SAB\) and whether the buffers may be shared using `postMessage()`.</span></span>  <span data-ttu-id="21db9-251">Un avertissement de dépréciation s’affiche si le SAB et `postMessage()` sont actuellement disponibles, mais que le contexte n’est pas isolé par origine croisée.</span><span class="sxs-lookup"><span data-stu-id="21db9-251">A deprecation warning displays if the SAB and `postMessage()` is currently available, but the context is not cross-origin isolated.</span></span>  <span data-ttu-id="21db9-252">Pour plus d’informations sur l’isolement entre les origines et sur les raisons de leur nécessité comme `SharedArrayBuffers` , accédez à [WindowOrWorkerGlobalScope.crossOriginIsolated][MdnWindoworworkerglobalscopeCrossoriginisolated].</span><span class="sxs-lookup"><span data-stu-id="21db9-252">For more information about cross-origin isolation and why it is required for features like `SharedArrayBuffers`, navigate to [WindowOrWorkerGlobalScope.crossOriginIsolated][MdnWindoworworkerglobalscopeCrossoriginisolated].</span></span>  <span data-ttu-id="21db9-253">Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de Chromium, accédez au problème [1139899][CR1139899].</span><span class="sxs-lookup"><span data-stu-id="21db9-253">To review real-time updates of this feature in the Chromium open-source project, navigate to Issue [1139899][CR1139899].</span></span>  

:::image type="complex" source="../../media/2020/11/frame-cross-origin-isolated-api.msft.png" alt-text="Informations sur l’origine croisée" lightbox="../../media/2020/11/frame-cross-origin-isolated-api.msft.png":::
   <span data-ttu-id="21db9-255">Informations sur l’origine croisée</span><span class="sxs-lookup"><span data-stu-id="21db9-255">Cross-origin information</span></span>  
:::image-end:::  

#### <a name="new-web-workers-information-in-the-frame-details-view"></a><span data-ttu-id="21db9-256">Nouvelles informations des travailleurs web dans l’affichage des détails du cadre</span><span class="sxs-lookup"><span data-stu-id="21db9-256">New Web Workers information in the Frame details view</span></span>  

<span data-ttu-id="21db9-257">DevTools organise désormais les travailleurs web sous le cadre du parent approprié.</span><span class="sxs-lookup"><span data-stu-id="21db9-257">DevTools now organizes web workers under the relevant parent frame.</span></span>  <span data-ttu-id="21db9-258">Par exemple, si le cadre `someName` crée `worker.js` , `worker.js` s’affiche sous `someName` dans la liste des **cadres**.</span><span class="sxs-lookup"><span data-stu-id="21db9-258">For example, if the `someName` frame creates `worker.js`, then `worker.js` appears under `someName` in the **Frames** list.</span></span>  <span data-ttu-id="21db9-259">Pour afficher les détails du travailleur web, effectuez ces actions.</span><span class="sxs-lookup"><span data-stu-id="21db9-259">To view the details of the web worker, complete the following actions.</span></span>  

1.  <span data-ttu-id="21db9-260">Ouvrir l’outil de **l’application**.</span><span class="sxs-lookup"><span data-stu-id="21db9-260">Open **Application** tool.</span></span>  
1.  <span data-ttu-id="21db9-261">Développer un cadre qui contient des travailleurs web.</span><span class="sxs-lookup"><span data-stu-id="21db9-261">Expand a frame that contains web workers.</span></span>  
1.  <span data-ttu-id="21db9-262">Développer l’arborescence **travailleurs**.</span><span class="sxs-lookup"><span data-stu-id="21db9-262">Expand the **Workers** tree.</span></span>  
1.  <span data-ttu-id="21db9-263">Choisir un travailleur.</span><span class="sxs-lookup"><span data-stu-id="21db9-263">Choose a worker.</span></span>  
    
<span data-ttu-id="21db9-264">Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de Chromium, accédez aux problèmes [1122507][CR1122507] et [1051466][CR1051466].</span><span class="sxs-lookup"><span data-stu-id="21db9-264">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [1122507][CR1122507] and [1051466][CR1051466].</span></span>  

:::image type="complex" source="../../media/2020/11/application-frames-service-workers.msft.png" alt-text="Informations sur les travailleurs web" lightbox="../../media/2020/11/application-frames-service-workers.msft.png":::
   <span data-ttu-id="21db9-266">Informations sur les travailleurs web</span><span class="sxs-lookup"><span data-stu-id="21db9-266">Web workers information</span></span>  
:::image-end:::  

#### <a name="display-opener-frame-details-for-opened-windows"></a><span data-ttu-id="21db9-267">Afficher les détails d’un cadre ouvrant pour les fenêtres ouvertes</span><span class="sxs-lookup"><span data-stu-id="21db9-267">Display opener frame details for opened windows</span></span>  

<span data-ttu-id="21db9-268">DevTools organise désormais les [fenêtres][MdnWindowConstructors] ouvertes sous le [cadre][MdnWindowFrames]parent approprié.</span><span class="sxs-lookup"><span data-stu-id="21db9-268">DevTools now organizes opened [Windows][MdnWindowConstructors] under the relevant parent [frame][MdnWindowFrames].</span></span>  <span data-ttu-id="21db9-269">Par exemple, si le cadre `top` ouvre une `Window` à `https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium` , la `Window` s’affiche sous `top` dans la liste des **cadres** .</span><span class="sxs-lookup"><span data-stu-id="21db9-269">For example, if the `top` frame opens a `Window` to `https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium`, then the `Window` appears under `top` in the **Frames** list.</span></span>  

<span data-ttu-id="21db9-270">Pour afficher le cadre responsable de l’ouverture d’une autre fenêtre dans l’outil des **éléments** , effectuez ces actions.</span><span class="sxs-lookup"><span data-stu-id="21db9-270">To reveal the frame responsible for opening another Window in the **Elements** tool, complete the following actions.</span></span>  

1.  <span data-ttu-id="21db9-271">Ouvrez l’arborescence des **cadres**.</span><span class="sxs-lookup"><span data-stu-id="21db9-271">Open the **Frames** tree.</span></span>  
1.  <span data-ttu-id="21db9-272">Développez les**fenêtres ouvertes** et choisissez le `Window` pour le cadre parent que vous voulez connaître.</span><span class="sxs-lookup"><span data-stu-id="21db9-272">Expand **Opened Windows** and choose the `Window` for the parent frame you want to know.</span></span>  
1.  <span data-ttu-id="21db9-273">Sélectionnez le lien du **cadre d’ouverture**.</span><span class="sxs-lookup"><span data-stu-id="21db9-273">Choose the **Opener Frame** link.</span></span>  

<span data-ttu-id="21db9-274">Les détails sur le cadre à l’origine de l’ouverture d’une autre `Window` sont affichés.</span><span class="sxs-lookup"><span data-stu-id="21db9-274">The details are displayed about which frame caused the opening of another `Window`.</span></span>  <span data-ttu-id="21db9-275">Pour afficher la l’élément responsable de l’ouverture dans l’outil **éléments** , effectuez ces actions..</span><span class="sxs-lookup"><span data-stu-id="21db9-275">To reveal the opener in the **Elements** tool, complete the following actions.</span></span>  

1.  <span data-ttu-id="21db9-276">Ouvrez l’arborescence des **cadres**.</span><span class="sxs-lookup"><span data-stu-id="21db9-276">Open the **Frames** tree.</span></span>  
1.  <span data-ttu-id="21db9-277">Choisissez une fenêtre ouverte pour ouvrir les détails de `Window`.</span><span class="sxs-lookup"><span data-stu-id="21db9-277">Choose an opened window to open the `Window` details.</span></span>  
1.  <span data-ttu-id="21db9-278">Sélectionnez le lien du **cadre d’ouverture**.</span><span class="sxs-lookup"><span data-stu-id="21db9-278">Choose the **Opener Frame** link.</span></span>  
    
<span data-ttu-id="21db9-279">Pour passer en revue l’historique de cette fonctionnalité dans le projet open-source de Chromium, accédez au problème [1107766][CR1107766].</span><span class="sxs-lookup"><span data-stu-id="21db9-279">To review the history of this feature in the Chromium open-source project, navigate to Issue [1107766][CR1107766].</span></span>  

:::image type="complex" source="../../media/2020/11/application-frames-opened-windows-security-opener-frame.msft.png" alt-text="Informations de cadre ouvert" lightbox="../../media/2020/11/application-frames-opened-windows-security-opener-frame.msft.png":::
   <span data-ttu-id="21db9-281">Informations de cadre ouvert</span><span class="sxs-lookup"><span data-stu-id="21db9-281">Opened frame details</span></span>  
:::image-end:::  

### <a name="copy-stacktrace-for-network-initiator"></a><span data-ttu-id="21db9-282">Copier le StackTrace pour l’initiateur réseau</span><span class="sxs-lookup"><span data-stu-id="21db9-282">Copy stacktrace for network initiator</span></span>  

<span data-ttu-id="21db9-283">Pour copier le StackTrace dans le presse-papiers, effectuez ces actions.</span><span class="sxs-lookup"><span data-stu-id="21db9-283">To copy the stacktrace to your clipboard, complete the following actions.</span></span>  

1.  <span data-ttu-id="21db9-284">Ouvrez le menu contextuel \(cliquez avec le bouton droit\).</span><span class="sxs-lookup"><span data-stu-id="21db9-284">Open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="21db9-285">Choisissez **copier**le  >  **StackTrace**.</span><span class="sxs-lookup"><span data-stu-id="21db9-285">Choose **Copy** > **Copy stacktrace**.</span></span>  
    
<span data-ttu-id="21db9-286">Pour passer en revue l’historique de cette fonctionnalité dans le projet open-source de Chromium, accédez au problème [1139615][CR1139615].</span><span class="sxs-lookup"><span data-stu-id="21db9-286">To review the history of this feature in the Chromium open-source project, navigate to Issue [1139615][CR1139615].</span></span>

:::image type="complex" source="../../media/2020/11/copy-stacktrace.msft.png" alt-text="Copier le StackTrace" lightbox="../../media/2020/11/copy-stacktrace.msft.png":::
   <span data-ttu-id="21db9-288">Copier le StackTrace</span><span class="sxs-lookup"><span data-stu-id="21db9-288">Copy stacktrace</span></span>  
:::image-end:::  

### <a name="preview-wasm-variable-value-on-mouseover"></a><span data-ttu-id="21db9-289">Afficher un aperçu de la valeur de la variable WASM sur mouseover</span><span class="sxs-lookup"><span data-stu-id="21db9-289">Preview Wasm variable value on mouseover</span></span>  

<span data-ttu-id="21db9-290">Utilisez cette fonction pour afficher un aperçu de la valeur d’une variable webassembly \ (WASM \) lorsque votre code est en pause.</span><span class="sxs-lookup"><span data-stu-id="21db9-290">Use this feature to review the value of a WebAssembly \(Wasm\) variable when your code is paused.</span></span>  <span data-ttu-id="21db9-291">Pour afficher la valeur actuelle d’une variable, pointez sur une variable.</span><span class="sxs-lookup"><span data-stu-id="21db9-291">To display the current value of a variable, hover on a variable.</span></span>  <span data-ttu-id="21db9-292">Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de Chromium, accédez aux problèmes [1058836][CR1058836] et [1071432][CR1071432].</span><span class="sxs-lookup"><span data-stu-id="21db9-292">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [1058836][CR1058836] and [1071432][CR1071432].</span></span>  

:::image type="complex" source="../../media/2020/11/wasm-mouseover.msft.png" alt-text="Afficher un aperçu de la variable WASM sur mouseover" lightbox="../../media/2020/11/wasm-mouseover.msft.png":::
   <span data-ttu-id="21db9-294">Afficher un aperçu de la variable WASM sur mouseover</span><span class="sxs-lookup"><span data-stu-id="21db9-294">Preview Wasm variable on mouseover</span></span>  
:::image-end:::  

### <a name="consistent-units-of-measurement-for-sizes-of-files-and-memory"></a><span data-ttu-id="21db9-295">Unités de mesure cohérentes pour la taille des fichiers et de la mémoire</span><span class="sxs-lookup"><span data-stu-id="21db9-295">Consistent units of measurement for sizes of files and memory</span></span>  

<span data-ttu-id="21db9-296">Désormais DevTools utilise `kB` pour l’affichage des tailles de fichiers et de mémoire.</span><span class="sxs-lookup"><span data-stu-id="21db9-296">DevTools now consistently use `kB` for displaying sizes of files and memory.</span></span>  <span data-ttu-id="21db9-297">Auparavant DevTools combinait `kB` et `KiB` .</span><span class="sxs-lookup"><span data-stu-id="21db9-297">Previously DevTools mixed `kB` and `KiB`.</span></span>

*   `kB` <span data-ttu-id="21db9-298">ou kilo-octets \ (10^3 ou 1000 octets \)</span><span class="sxs-lookup"><span data-stu-id="21db9-298">or kilobyte \(10^3 or 1000 bytes\)</span></span>  
*   `KiB` <span data-ttu-id="21db9-299">ou kibibyte \ (2^10 ou 1024 octets \)</span><span class="sxs-lookup"><span data-stu-id="21db9-299">or kibibyte \(2^10 or 1024 bytes\)</span></span>  
    
<span data-ttu-id="21db9-300">Par exemple, l’outil **réseau** utilisait `kB` dans les étiquettes, mais utilisait `KiB` dans les calculs.</span><span class="sxs-lookup"><span data-stu-id="21db9-300">For example, the **Network** tool previously used `kB` in the labels, but used `KiB` in calculations.</span></span>  <span data-ttu-id="21db9-301">Votre commentaire a démontré que cette incohérence a causé une confusion.</span><span class="sxs-lookup"><span data-stu-id="21db9-301">Your feedback showed that this inconsistency caused confusion.</span></span>  <span data-ttu-id="21db9-302">Pour passer en revue l’historique de cette fonctionnalité dans le projet open-source de Chromium, accédez au problème [1035309][CR1035309].</span><span class="sxs-lookup"><span data-stu-id="21db9-302">To review the history of this feature in the Chromium open-source project, navigate to Issue [1035309][CR1035309].</span></span>  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="21db9-303">Téléchargez les canaux de l'aperçu de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="21db9-303">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="21db9-304">Si vous êtes sous Windows, Linux ou macOS, envisagez d'utiliser les [canaux d'aperçu de Microsoft Edge][MicrosoftEdgePreviewChannels] comme navigateur de développement par défaut.</span><span class="sxs-lookup"><span data-stu-id="21db9-304">If you are on Windows, Linux, or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="21db9-305">Les canaux de prévisualisation vous donnent accès aux dernières fonctionnalités de DevTools.</span><span class="sxs-lookup"><span data-stu-id="21db9-305">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="21db9-306">Contacter l’équipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="21db9-306">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[Devtools3dViewIndex]: /microsoft-edge/devtools-guide-chromium/3d-view/index "Affichage 3D | Documents Microsoft"  
[DevtoolsConsoleIndex]: /microsoft-edge/devtools-guide-chromium/console/index "Présentation de la console | Documents Microsoft"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Paramètres-personnaliser Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsCustomizeLocalization]: /microsoft-edge/devtools-guide-chromium/customize/localization "Modifier les paramètres de langue de DevTools | Documents Microsoft"  
[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Émuler des appareils mobiles dans Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-keyboard-shortcut-editor "Activer l’éditeur de raccourcis clavier-fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-composited-layers-in-3d-view "Activer les couches composites dans l’affichage 3D - fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsIssuesIndex]: /microsoft-edge/devtools-guide-chromium/issues/index "Recherchez et corrigez les problèmes liés à l’outil des problèmes de Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard]: /microsoft-edge/devtools-guide-chromium/network/reference#copy-formatted-response-json-to-the-clipboard "Copier la valeur JSON de la réponse mise en forme dans le presse-papiers - référence d’analyse du réseau | Documents Microsoft"  
[DevtoolsNetworkReferenceViewTimingBreakdownRequest]: /microsoft-edge/devtools-guide-chromium/network/reference#view-the-timing-breakdown-of-a-request "Afficher la répartition du chronométrage d’une demande - référence d’analyse du réseau | Documents Microsoft"  
[WebDriverChromiumMain]: /microsoft-edge/webdriver-chromium "Utiliser le WebDriver (Chromium) pour l’automatisation des tests | Documents Microsoft"  

<!--  [DevtoolsCssReferenceChangeAngleValueWithAngleClock]: /microsoft-edge/devtools-guide-chromium/css/reference#change-angle-value-with-the-angle-clock "Change angle value with the Angle Clock - CSS reference | Microsoft Docs"  -->  

[ProgressiveWebAppsIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Applications web progressives sur Windows | Documents Microsoft"  

[WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings]: ../10/devtools.md#customize-keyboard-shortcuts-in-settings "Personnaliser les raccourcis clavier dans les paramètres - nouveautés de DevTools (Microsoft Edge 87) | Documents Microsoft"  
[WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel]: ../06/devtools.md#webhint-feedback-in-the-issues-panel "Commentaires sur les webhint dans le panneau des problèmes - nouveautés de DevTools (Microsoft Edge 85) | Documents Microsoft"  

[MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver#downloads "Télécharger WebDriver | Développeur Microsoft"  

[MicrosoftinsiderDownloadPlatformLinux]: https://www.microsoftedgeinsider.com/download?platform=linux "Télécharger les canaux Microsoft Edge Insider"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canaux d’aperçu Microsoft Edge"  

[VisualStudioCode]: https://code.visualstudio.com "Code Visual Studio"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Bogues Chromium"  

[CR174309]: https://crbug.com/174309 "Problème 174309: DevTools: Autoriser la personnalisation des raccourcis clavier/les combinaisons de touches | Bogues Chromium"  
[CR945786]: https://crbug.com/945786 "Problème 945786: DevTools: Autoriser le remplacement de navigator.storage.estimate() | Bogues Chromium"  
[CR1029427]: https://crbug.com/1029427 "Problème 1029427: Réduire la surcharge des performances de l’envoi de messages de protocole frontal | Bogues Chromium"  
[CR1035309]: https://crbug.com/1035309 "Problème 1035309: DevTools doit utiliser de manière cohérente Mo pour signifier mégaoctets, pas mebibyte | Bogues Chromium"  
[CR1051466]: https://crbug.com/1051466 "Problème 1051466: Prendre en charge le débogage COOP/COEP dans DevTools | Bogues Chromium"  
[CR1058836]: https://crbug.com/1058836 "Problème 1058836: Problèmes UX liés au débogage de WASM | Bogues Chromium"  
[CR1071432]: https://crbug.com/1071432 "Problème 1071432: ☂️ Experience de développeur de base WASM | Bogues Chromium"  
[CR1107766]: https://crbug.com/1107766 "Problème 1107766: Affichez des informations sur les cadres générées par ’window.open()' dans l’arborescence de cadre | Bogues Chromium"  
[CR1122507]: https://crbug.com/1122507 "Problème 1122507: Informations sur le travailleur de surface dans l’affichage de l’arborescence de cadre | Bogues Chromium"  
[CR1126178]: https://crbug.com/1126178 "Problème 1126178: ☂ DevTools: CSS <type> composants | Bogues Chromium"  
[CR1130556]: https://crbug.com/1130556 "Problème 1130556: DevTools: tester l’image de retour (émulation) | Bogues Chromium"  
[CR1132084]: https://crbug.com/1132084 "Problème 1132084: il n’y a pas de moyen simple de copier la charge utile de la requête JSON | Bogues Chromium"  
[CR1136394]: https://crbug.com/1136394 "Problème 1136394: outils Flexbox | Bogues Chromium"  
[CR1138633]: https://crbug.com/1138633 "Problème 1138633: DevTools: CSS <angle> le composant doit refléter son apparence de propriété dans l’arrière-plan d’horloge | Bogues Chromium"  
[CR1139615]: https://crbug.com/1139615 "Problème 1139615: L’initiateur réseau doit permettre de copier le rapport des appels de procédure | Bogues Chromium"  
[CR1139899]: https://crbug.com/1139899 "Problème 1139899: Signaler la disponibilité des API contrôlées dans l’affichage des détails du cadre | Bogues Chromium"  
[CR1139945]: https://crbug.com/1139945 "Problème 1139945: icônes des propriétés CSS de Flexbox dans le panneau styles | Bogues Chromium"  
[CR1141824]: https://crbug.com/1141824 "Problème 1141824: améliorer le signalement des erreurs CORS dans DevTools | Bogues Chromium"  
[CR1144090]: https://crbug.com/1144090 "Problème 1144090: Ajouter des ornements de style flex à l’arborescence des éléments | Bogues Chromium"  
[CR1146985]: https://crbug.com/1146985 "Problème 1146985: le texte supprimé reste affiché dans le champ de texte de la section «stockage» de la fenêtre « outils de développement » | Bogues Chromium"  

[GlitchCorsErrors]: https://cors-errors.glitch.me "Erreurs CORS | Problème"  

[MdnCors]: https://developer.mozilla.org/docs/Web/HTTP/CORS "Partage de ressources d’origine croisée (CORS) | MDN"  
[MdnUsingCssCustomProperties]: https://developer.mozilla.org/docs/Web/CSS/Using_CSS_custom_properties "Utilisation des propriétés personnalisées CSS (variables) | MDN"  
[MdnWindowConstructors]: https://developer.mozilla.org/docs/Web/API/Window#Constructors "Constructeurs - fenêtre | MDN"  
[MdnWindowFrames]: https://developer.mozilla.org/docs/Web/API/Window/frames "Window.frames | MDN"  
[MdnWindoworworkerglobalscopeCrossoriginisolated]: https://developer.mozilla.org/docs/Web/API/WindowOrWorkerGlobalScope/crossOriginIsolated "WindowOrWorkerGlobalScope.crossOriginIsolated | MDN"  

[WebhintMain]: https://webhint.io "webhint"  
[WebhintUserGuideHintsAccessibility]: https://webhint.io/docs/user-guide/hints/accessibility "Accessibilité | Webhint"  
[WebhintUserGuideHintsCompatibility]: https://webhint.io/docs/user-guide/hints/compatibility "Compatibilité | Webhint"  
[WebhintUserGuideHintsPerformance]: https://webhint.io/docs/user-guide/hints/performance "Performance | Webhint"  
[WebhintUserGuideHintsPitfalls]: https://webhint.io/docs/user-guide/hints/pitfalls "Pièges | Webhint"  
[WebhintUserGuideHintsPwa]: https://webhint.io/docs/user-guide/hints/pwa "PWA | Webhint"  
[WebhintUserGuideHintsSecurity]: https://webhint.io/docs/user-guide/hints/security "Sécurité | Webhint"  

> [!NOTE]
> <span data-ttu-id="21db9-359">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="21db9-359">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="21db9-360">La page d’origine est disponible [ici](https://developers.google.com/web/updates/2020/11/devtools/index) et est créée par [Jecelyn Yeen][JecelynYeen] \(Appui au développeur, Chrome DevTools\)</span><span class="sxs-lookup"><span data-stu-id="21db9-360">The original page is found [here](https://developers.google.com/web/updates/2020/11/devtools/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="21db9-362">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="21db9-362">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
