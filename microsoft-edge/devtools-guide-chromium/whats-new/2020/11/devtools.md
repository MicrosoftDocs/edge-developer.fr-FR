---
description: Microsoft Edge pour Linux, conseils d’amélioration de webhint dans l’outil problèmes, nouvelles fonctionnalités de débogage de travailleur de service, etc.
title: Nouveautés de DevTools (Microsoft Edge 88)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 500b64e7b51e0f02c9fcbcb7a83e8273b3a5a0d7
ms.sourcegitcommit: 3234b32e73c9f8362082d995296bd1c5e4286036
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/09/2020
ms.locfileid: "11205242"
---
# <span data-ttu-id="51a1b-104">Nouveautés de DevTools (Microsoft Edge 88)</span><span class="sxs-lookup"><span data-stu-id="51a1b-104">What's New in DevTools (Microsoft Edge 88)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <span data-ttu-id="51a1b-105">Le pilote Microsoft Edge et Microsoft Edge est désormais disponible sur Linux</span><span class="sxs-lookup"><span data-stu-id="51a1b-105">Microsoft Edge and Microsoft Edge Driver now available on Linux</span></span>  

<!-- Title: Microsoft Edge and Microsoft Edge Driver on Linux  -->  
<!-- Subtitle: Get Microsoft Edge Dev on Ubuntu, Debian, Fedora, and openSUSE distributions and start automating in CI/CD environments with Microsoft Edge Driver. -->  

<span data-ttu-id="51a1b-106">Microsoft Edge dev est désormais pris en charge sur les distributions Ubuntu, Debian, Fedora et openSUSE.</span><span class="sxs-lookup"><span data-stu-id="51a1b-106">Microsoft Edge Dev is now supported on Ubuntu, Debian, Fedora, and openSUSE distributions.</span></span>  <span data-ttu-id="51a1b-107">Téléchargez et installez le Microsoft Edge dev `.deb` ou le `.rpm` package directement à partir du [site Microsoft Edge Insider][MicrosoftinsiderDownloadPlatformLinux] ou utilisez les outils de gestion des packages standard de votre distribution Linux.</span><span class="sxs-lookup"><span data-stu-id="51a1b-107">Download and install the Microsoft Edge Dev `.deb` or `.rpm` package directly from the [Microsoft Edge Insider site][MicrosoftinsiderDownloadPlatformLinux] or use the standard package management tools of your Linux distribution.</span></span>  

<span data-ttu-id="51a1b-108">Si vous utilisez un environnement Linux dans vos solutions d’intégration et de remise en continu, vous pouvez également utiliser le pilote Microsoft Edge pour Linux.</span><span class="sxs-lookup"><span data-stu-id="51a1b-108">If you are using a Linux environment in your continuous integration and delivery \(CI/CD\) solutions, Microsoft Edge Driver is also available on Linux.</span></span>  <span data-ttu-id="51a1b-109">Pour commencer à automatiser Microsoft Edge dev avec le pilote Microsoft Edge, accédez à la [page téléchargements de pilotes Microsoft Edge][MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads].</span><span class="sxs-lookup"><span data-stu-id="51a1b-109">To get started automating Microsoft Edge Dev with Microsoft Edge Driver, navigate to [Microsoft Edge Driver Downloads page][MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads].</span></span>  <span data-ttu-id="51a1b-110">Pour obtenir de l’aide sur l’automatisation du développement Microsoft Edge avec le pilote Microsoft Edge, naviguez jusqu’à l' [utilisation de WebDriver (chrome) pour l’automatisation des tests][WebDriverChromiumMain].</span><span class="sxs-lookup"><span data-stu-id="51a1b-110">For help with automating Microsoft Edge Dev along with Microsoft Edge Driver, navigate to [Use WebDriver (Chromium) for test automation][WebDriverChromiumMain].</span></span>  

:::image type="complex" source="../../media/2020/11/edge-on-linux.msft.png" alt-text="DevTools dans Microsoft Edge sur Linux" lightbox="../../media/2020/11/edge-on-linux.msft.png":::
   <span data-ttu-id="51a1b-112">DevTools dans Microsoft Edge sur Linux</span><span class="sxs-lookup"><span data-stu-id="51a1b-112">DevTools in Microsoft Edge on Linux</span></span>  
:::image-end:::  

## <span data-ttu-id="51a1b-113">Amélioration de l’astuce et des conseils de plateforme dans l’outil problèmes</span><span class="sxs-lookup"><span data-stu-id="51a1b-113">Improved webhint and platform tips in the Issues tool</span></span>  

<!-- Title: Improvements to Issues tool and webhint integration  -->  
<!-- Subtitle: Categories and third-party filtering make it easier to survey issues in the Issues tool.  Issues surfaced by webhint now have improved code snippets and documentation links to help you fix problems in your website.  -->  

<span data-ttu-id="51a1b-114">Un outil open source, [webhint][WebhintMain], fournit des commentaires en temps réel sur les sites Web et les pages Web locales.</span><span class="sxs-lookup"><span data-stu-id="51a1b-114">An open-source tool, [webhint][WebhintMain], provides real-time feedback for websites and local webpages.</span></span>  <span data-ttu-id="51a1b-115">À partir de la [version 85 de Microsoft Edge][WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel], consultez les commentaires sur le webhint dans l’outil [problèmes][DevtoolsIssuesIndex] .</span><span class="sxs-lookup"><span data-stu-id="51a1b-115">Starting with [Microsoft Edge version 85][WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel], review webhint feedback in the [Issues][DevtoolsIssuesIndex] tool.</span></span>  <span data-ttu-id="51a1b-116">Il est désormais plus facile de passer en revue les problèmes qui s’affichent dans l’outil de **problèmes** en ajoutant les catégories suivantes.</span><span class="sxs-lookup"><span data-stu-id="51a1b-116">Issues that appear in the **Issues** tool are now easier to review with the addition of the following categories.</span></span>  

*   [<span data-ttu-id="51a1b-117">Accessibilité</span><span class="sxs-lookup"><span data-stu-id="51a1b-117">Accessibility</span></span>][WebhintUserGuideHintsAccessibility]  
*   [<span data-ttu-id="51a1b-118">Compatibilité</span><span class="sxs-lookup"><span data-stu-id="51a1b-118">Compatibility</span></span>][WebhintUserGuideHintsCompatibility]  
*   [<span data-ttu-id="51a1b-119">Niveau de performance</span><span class="sxs-lookup"><span data-stu-id="51a1b-119">Performance</span></span>][WebhintUserGuideHintsPerformance]  
*   [<span data-ttu-id="51a1b-120">Les pièges</span><span class="sxs-lookup"><span data-stu-id="51a1b-120">Pitfalls</span></span>][WebhintUserGuideHintsPitfalls]  
*   [<span data-ttu-id="51a1b-121">PWA</span><span class="sxs-lookup"><span data-stu-id="51a1b-121">PWA</span></span>][WebhintUserGuideHintsPwa]  
*   [<span data-ttu-id="51a1b-122">Sécurité</span><span class="sxs-lookup"><span data-stu-id="51a1b-122">Security</span></span>][WebhintUserGuideHintsSecurity]  
    
<span data-ttu-id="51a1b-123">Vous pouvez à présent filtrer les problèmes tiers à l’aide d’une nouvelle case à cocher.</span><span class="sxs-lookup"><span data-stu-id="51a1b-123">You are now able to filter out third-party issues using a new checkbox.</span></span>  <span data-ttu-id="51a1b-124">La fonctionnalité de filtre vous aide à masquer les problèmes liés au code de bibliothèques tierces ou d’autres sources.</span><span class="sxs-lookup"><span data-stu-id="51a1b-124">The filter functionality helps you hide issues related to code from third-party libraries or other sources.</span></span>  

<span data-ttu-id="51a1b-125">Pour vous aider à passer en revue les problèmes détectés par [webhint][WebhintMain], l’outil **problèmes** affiche désormais les informations suivantes.</span><span class="sxs-lookup"><span data-stu-id="51a1b-125">To help you review issues revealed by [webhint][WebhintMain], the **Issues** tool now displays the following information.</span></span>  

*   <span data-ttu-id="51a1b-126">Meilleurs extraits de code.</span><span class="sxs-lookup"><span data-stu-id="51a1b-126">Improved code snippets.</span></span>  
*   <span data-ttu-id="51a1b-127">Liens vers d’autres panneaux pertinents.</span><span class="sxs-lookup"><span data-stu-id="51a1b-127">Links to other relevant panels.</span></span>  
*   <span data-ttu-id="51a1b-128">Liens vers la documentation pour vous aider à résoudre les problèmes rencontrés sur votre site Web.</span><span class="sxs-lookup"><span data-stu-id="51a1b-128">Links to documentation to help you fix problems in your website.</span></span>  
    
:::image type="complex" source="../../media/2020/11/issues-webhints.msft.png" alt-text="Outil problèmes" lightbox="../../media/2020/11/issues-webhints.msft.png":::
   <span data-ttu-id="51a1b-130">Outil **problèmes**</span><span class="sxs-lookup"><span data-stu-id="51a1b-130">**Issues** tool</span></span>  
:::image-end:::  

## <span data-ttu-id="51a1b-131">Les couches composites sont désormais en vue 3D</span><span class="sxs-lookup"><span data-stu-id="51a1b-131">Composited Layers are now in 3D View</span></span>  

<!-- Title: 3D View is now integrated with Composited Layers  -->  
<!-- Subtitle: Composited Layers are now in 3D View.  -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::

<span data-ttu-id="51a1b-132">Il est possible que vous souhaitiez visualiser les contenus de **calques** avec les valeurs d’index z et le modèle d’objet document (DOM).</span><span class="sxs-lookup"><span data-stu-id="51a1b-132">You may now visualize **Layers** content alongside z-index values and the Document Object Model \(DOM\).</span></span>  <span data-ttu-id="51a1b-133">Cette fonctionnalité vous permet de déboguer sans basculer entre les outils d' [affichage 3D][Devtools3dViewIndex] et de **calques** .</span><span class="sxs-lookup"><span data-stu-id="51a1b-133">This feature helps you debug without switching between the [3D view][Devtools3dViewIndex] and **Layers** tools as often.</span></span>  <span data-ttu-id="51a1b-134">Pour une interface de débogage complète, l' [affichage 3D et les couches composites sont désormais combinés][DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView].</span><span class="sxs-lookup"><span data-stu-id="51a1b-134">For a comprehensive visual debugging experience, the [3D View and Composited Layers are now combined][DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView].</span></span>  

:::image type="complex" source="../../media/2020/11/experiments-layers.msft.png" alt-text="Volet couches composites" lightbox="../../media/2020/11/experiments-layers.msft.png":::
   <span data-ttu-id="51a1b-136">Volet **couches composites**</span><span class="sxs-lookup"><span data-stu-id="51a1b-136">**Composited Layers** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="51a1b-137">Définitions des variables CSS dans le volet styles</span><span class="sxs-lookup"><span data-stu-id="51a1b-137">CSS variable definitions in Styles pane</span></span>  

<!-- Title: Jump to CSS variable definitions  -->  
<!-- Subtitle: Choose any CSS variable to navigate directly to the definition in the Styles tool. -->  

<span data-ttu-id="51a1b-138">Dans le volet **styles** , les [variables CSS][MdnUsingCssCustomProperties] sont désormais liées directement à chaque définition.</span><span class="sxs-lookup"><span data-stu-id="51a1b-138">In the **Styles** pane, [CSS variables][MdnUsingCssCustomProperties] now link directly to each definition.</span></span>  <span data-ttu-id="51a1b-139">Choisissez la variable pour afficher ou modifier facilement la définition de variables CSS.</span><span class="sxs-lookup"><span data-stu-id="51a1b-139">Choose the variable to easily view or change the CSS variable definition.</span></span>  <span data-ttu-id="51a1b-140">Dans l’exemple, DevTools affiche les attributs CSS pour l' `body` élément.</span><span class="sxs-lookup"><span data-stu-id="51a1b-140">In the example, DevTools displays the CSS attributes for the `body` element.</span></span>  <span data-ttu-id="51a1b-141">Pour afficher la définition de variable pour la `--theme-body-background` variable CSS, effectuez les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="51a1b-141">To display the variable definition for the `--theme-body-background` CSS variable, complete the following actions.</span></span>  

1.  <span data-ttu-id="51a1b-142">Dans le volet **styles** , sélectionnez `var(--theme-body-background)` .</span><span class="sxs-lookup"><span data-stu-id="51a1b-142">In the **Styles** pane, choose `var(--theme-body-background)`.</span></span>  
1.  <span data-ttu-id="51a1b-143">Le volet **styles** affiche désormais la définition de la `--theme-body-background` variable CSS.</span><span class="sxs-lookup"><span data-stu-id="51a1b-143">The **Styles** pane now displays the definition of the `--theme-body-background` CSS variable.</span></span>  
    
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/css-variable-support.msft.png" alt-text="Variable CSS liée au style" lightbox="../../media/2020/11/css-variable-support.msft.png":::
         <span data-ttu-id="51a1b-145">Variable CSS liée au style</span><span class="sxs-lookup"><span data-stu-id="51a1b-145">CSS variable linked to the style</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/css-variable-support-target.msft.png" alt-text="Variable CSS liée à la cible de style" lightbox="../../media/2020/11/css-variable-support-target.msft.png":::
         <span data-ttu-id="51a1b-147">Variable CSS liée à la cible de style</span><span class="sxs-lookup"><span data-stu-id="51a1b-147">CSS variable linked to style target</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="51a1b-148">Améliorations du débogage des travailleurs de services</span><span class="sxs-lookup"><span data-stu-id="51a1b-148">Service worker debugging improvements</span></span>  

<!-- Title:  Service worker debugging improvements in the Network, Application, and Sources tools  -->  
<!-- Subtitle:  Making service workers easier to debug for progressive web applications and more.  -->  

<span data-ttu-id="51a1b-149">Les nouvelles fonctionnalités suivantes dans les outils [réseau](#network-tool), [application](#application-tool)et [sources](#sources-tool) vous aident à créer votre [PWA][ProgressiveWebAppsChromiumIndex].</span><span class="sxs-lookup"><span data-stu-id="51a1b-149">The following new features in the [Network](#network-tool), [Application](#application-tool), and [Sources](#sources-tool) tools help you build your [PWA][ProgressiveWebAppsChromiumIndex].</span></span>  <span data-ttu-id="51a1b-150">Si vous éprouvez des difficultés à déboguer votre travailleur de service, utilisez les fonctionnalités suivantes.</span><span class="sxs-lookup"><span data-stu-id="51a1b-150">Use the following features when you have difficulty debugging your service worker.</span></span>  

<span data-ttu-id="51a1b-151">Demander le routage affiche `startup` les `fetch` événements et en fonction des requêtes réseau qui s’exécutent par le biais des travailleurs de service.</span><span class="sxs-lookup"><span data-stu-id="51a1b-151">Request routing displays the `startup` and `fetch` events based on the network requests that run through service workers.</span></span>  <span data-ttu-id="51a1b-152">Les chronologies sont accessibles à partir de l’outil de l' **application** ou du **réseau** .</span><span class="sxs-lookup"><span data-stu-id="51a1b-152">The timelines are accessed from either the **Application** or **Network** tool.</span></span>  <span data-ttu-id="51a1b-153">Les chronologies sont là lorsque vous rencontrez des problèmes avec les travailleurs de service et que vous souhaitez voir s’il y a un problème avec l' `startup` `fetch` événement ou.</span><span class="sxs-lookup"><span data-stu-id="51a1b-153">The timelines help when you are having trouble with service workers and want to see if something is wrong with the `startup` or `fetch` event.</span></span>  

### <span data-ttu-id="51a1b-154">Outil de l’application</span><span class="sxs-lookup"><span data-stu-id="51a1b-154">Application tool</span></span>  

<!-- Title: Open Network tool from the Service Workers pane  -->  
<!-- Subtitle: Display additional context when debugging a service worker.  -->  

<span data-ttu-id="51a1b-155">Affichez les informations de routage de toutes les demandes de service d’appel avec le nouveau lien **demandes réseau** .</span><span class="sxs-lookup"><span data-stu-id="51a1b-155">View all service worker request routing information with the new **Network requests** link.</span></span>  <span data-ttu-id="51a1b-156">Pour afficher un contexte supplémentaire lors du débogage du travailleur de service, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="51a1b-156">To display additional context when debugging the service worker, complete the following actions.</span></span>  

1.  <span data-ttu-id="51a1b-157">Accédez aux \*\*\*\*  >  **travailleurs de services**d’application.</span><span class="sxs-lookup"><span data-stu-id="51a1b-157">Navigate to **Application** > **Service Workers**.</span></span>  
1.  <span data-ttu-id="51a1b-158">Sélectionnez **requêtes réseau**.</span><span class="sxs-lookup"><span data-stu-id="51a1b-158">Choose **Network requests**.</span></span>  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-requests.msft.png" alt-text="Ouvrir l’outil réseau via le volet travailleurs de service" lightbox="../../media/2020/11/service-worker-application-network-requests.msft.png":::
       <span data-ttu-id="51a1b-160">Ouvrir l’outil **réseau** via le volet **travailleurs de service**</span><span class="sxs-lookup"><span data-stu-id="51a1b-160">Open **Network** tool from the **Service Workers** pane</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="51a1b-161">L’outil **réseau** s’ouvre dans le **tiroir** et affiche toutes les demandes réseau associées au travailleur du service.</span><span class="sxs-lookup"><span data-stu-id="51a1b-161">The **Network** tool opens in the **drawer** and displays all service worker-related network requests.</span></span>  <span data-ttu-id="51a1b-162">Les requêtes réseau sont filtrées à l’aide de `is:service-worker-intercepted` .</span><span class="sxs-lookup"><span data-stu-id="51a1b-162">The network requests are filtered using `is:service-worker-intercepted`.</span></span>  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-drawer.msft.png" alt-text="Outil réseau dans un tiroir" lightbox="../../media/2020/11/service-worker-application-network-drawer.msft.png":::
       <span data-ttu-id="51a1b-164">Outil **réseau** dans un **tiroir**</span><span class="sxs-lookup"><span data-stu-id="51a1b-164">**Network** tool in **drawer**</span></span>  
    :::image-end:::
    
1. <span data-ttu-id="51a1b-165">Pour rétablir le panneau supérieur de l’outil **réseau** , fermez le **tiroir**.</span><span class="sxs-lookup"><span data-stu-id="51a1b-165">To return the **Network** tool to the top panel, close the **drawer**.</span></span>  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-return.msft.png" alt-text="Fermez le tiroir de votre tiroir pour retourner le panneau de connexion." lightbox="../../media/2020/11/service-worker-application-network-return.msft.png":::
       <span data-ttu-id="51a1b-167">Fermez le **tiroir** de votre tiroir pour retourner le panneau de **connexion** .</span><span class="sxs-lookup"><span data-stu-id="51a1b-167">Close the **drawer** to return **Network** tool</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="51a1b-168">Outil réseau</span><span class="sxs-lookup"><span data-stu-id="51a1b-168">Network tool</span></span>  

<span data-ttu-id="51a1b-169">Déboguer les requêtes réseau qui s’exécutent par le biais des travailleurs de service.</span><span class="sxs-lookup"><span data-stu-id="51a1b-169">Debug network requests that run through service workers.</span></span>  <span data-ttu-id="51a1b-170">Vous pouvez également ouvrir des requêtes réseau à partir de l’outil de l' **application** .</span><span class="sxs-lookup"><span data-stu-id="51a1b-170">You may also open network requests from the **Application** tool.</span></span>  <span data-ttu-id="51a1b-171">Pour chaque demande, DevTools affiche les informations suivantes dans le volet [minutage][DevtoolsNetworkReferenceViewTimingBreakdownRequest] .</span><span class="sxs-lookup"><span data-stu-id="51a1b-171">For each request, DevTools display the following information in the [Timing][DevtoolsNetworkReferenceViewTimingBreakdownRequest] pane.</span></span>  

*   <span data-ttu-id="51a1b-172">Le début d’une demande et la durée de l’amorce.</span><span class="sxs-lookup"><span data-stu-id="51a1b-172">The start of a request and duration of the bootstrap.</span></span>  
*   <span data-ttu-id="51a1b-173">Modification apportée à l’inscription des travailleurs de service.</span><span class="sxs-lookup"><span data-stu-id="51a1b-173">Changes to service worker registration.</span></span>  
*   <span data-ttu-id="51a1b-174">Exécution d’un `fetch` Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="51a1b-174">The runtime of a `fetch` event handler.</span></span>  
*   <span data-ttu-id="51a1b-175">Exécution de tous les `fetch` événements de chargement d’un client.</span><span class="sxs-lookup"><span data-stu-id="51a1b-175">The runtime of all `fetch` events for loading a client.</span></span>  
    
:::image type="complex" source="../../media/2020/11/network-timing-service-worker.msft.png" alt-text="Volet minutage" lightbox="../../media/2020/11/network-timing-service-worker.msft.png":::
   <span data-ttu-id="51a1b-177">Volet **minutage**</span><span class="sxs-lookup"><span data-stu-id="51a1b-177">**Timing** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="51a1b-178">Outil sources</span><span class="sxs-lookup"><span data-stu-id="51a1b-178">Sources tool</span></span>  

<span data-ttu-id="51a1b-179">Dans les versions précédentes de Microsoft Edge, le niveau de profondeur de la pile d’appels était limité au code JavaScript de votre travailleur de service.</span><span class="sxs-lookup"><span data-stu-id="51a1b-179">In previous versions of Microsoft Edge, the level of depth in the call stack was limited to the JavaScript code in your service worker.</span></span>  <span data-ttu-id="51a1b-180">Dans Microsoft Edge 88, la pile d’appels affiche désormais l’initiateur de demandes qui s’exécutent par le biais de votre travailleur de service.</span><span class="sxs-lookup"><span data-stu-id="51a1b-180">In Microsoft Edge 88, the call stack now displays the initiator of requests that run through your service worker.</span></span>  

<span data-ttu-id="51a1b-181">Pour localiser l’initiateur de la requête, utilisez la pile d’appels de votre code JavaScript dans le travailleur de service.</span><span class="sxs-lookup"><span data-stu-id="51a1b-181">To locate the initiator of the request, use the call stack of your JavaScript code in the service worker.</span></span>  <span data-ttu-id="51a1b-182">La pile d’appels dans les figures suivantes commence par le code JavaScript de votre travailleur de service et affiche une référence à la demande de page Web d’origine `(index):157` .</span><span class="sxs-lookup"><span data-stu-id="51a1b-182">The call stack in the following figures starts with the JavaScript code in your service worker and displays a reference to the original webpage request as `(index):157`.</span></span>  <span data-ttu-id="51a1b-183">Dans la deuxième figure, la référence est choisie et a ouvert l’initiateur qui a créé la demande.</span><span class="sxs-lookup"><span data-stu-id="51a1b-183">In the second figure, the reference is chosen and opened the initiator that made the request.</span></span>  <span data-ttu-id="51a1b-184">Dans la deuxième figure, l’initiateur est la page Web.</span><span class="sxs-lookup"><span data-stu-id="51a1b-184">The initiator in the second figure is the webpage.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/service-worker-sources-stopped-at-breakpoint.msft.png" alt-text="Le fichier service-worker.js et la mise en surbrillance de la pile d’appels" lightbox="../../media/2020/11/service-worker-sources-stopped-at-breakpoint.msft.png":::
         <span data-ttu-id="51a1b-186">L' `service-worker.js` émetteur de la demande de mise en surbrillance des piles de fichiers et d’appels</span><span class="sxs-lookup"><span data-stu-id="51a1b-186">The `service-worker.js` file and call stack highlighting request originator</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/service-worker-sources-call-stack-target.msft.png" alt-text="La page Web (index) est l’initiateur de la requête" lightbox="../../media/2020/11/service-worker-sources-call-stack-target.msft.png":::
         <span data-ttu-id="51a1b-188">La `(index)` page Web est l’initiateur de la requête</span><span class="sxs-lookup"><span data-stu-id="51a1b-188">The `(index)` webpage is the request initiator</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="51a1b-189">Copier la valeur de la propriété d’une demande réseau</span><span class="sxs-lookup"><span data-stu-id="51a1b-189">Copy property value of a network request</span></span>  

<!-- Title: Copy response JSON in Network tool using the contextual menu  -->  
<!-- Subtitle:  The Network tool now has a more consistent UX.  Easily copy the JSON response using the contextual menu.  -->  

<span data-ttu-id="51a1b-190">Dans l’outil **réseau** , copiez la valeur de la propriété d’une demande réseau à l’aide de la nouvelle option **copier la valeur** .</span><span class="sxs-lookup"><span data-stu-id="51a1b-190">In the **Network** tool, copy the property value of a network request using the new **Copy value** option.</span></span>  <span data-ttu-id="51a1b-191">La valeur de la propriété est copiée en tant que valeur JSON décodée.</span><span class="sxs-lookup"><span data-stu-id="51a1b-191">The property value is copied as a decoded JSON value.</span></span>  <span data-ttu-id="51a1b-192">Dans les versions précédentes de Microsoft Edge, vous deviez copier une valeur à l’aide de l’une des actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="51a1b-192">In previous versions of Microsoft Edge, you had to copy a value using one of the following actions.</span></span>  

*   <span data-ttu-id="51a1b-193">Mettez en surbrillance l’intégralité du texte et copiez-le.</span><span class="sxs-lookup"><span data-stu-id="51a1b-193">Highlight the entire text and copy it.</span></span>  
*   <span data-ttu-id="51a1b-194">Stockez la valeur en tant que variable globale, le cas échéant, puis copiez-la à partir de la [console][DevtoolsConsoleIndex]devtools.</span><span class="sxs-lookup"><span data-stu-id="51a1b-194">Store the value as global variable, as applicable, and copy it from the DevTools [Console][DevtoolsConsoleIndex].</span></span>  
    
<span data-ttu-id="51a1b-195">Pour copier la valeur de la propriété dans le presse-papiers, accédez à [copier la réponse mise en forme JSON dans le presse-papiers][DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard].</span><span class="sxs-lookup"><span data-stu-id="51a1b-195">To copy the property value to your clipboard, navigate to [Copy formatted response JSON to the clipboard][DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard].</span></span>  <span data-ttu-id="51a1b-196">Pour passer en revue l’historique de cette fonctionnalité dans le projet open-source de chrome, accédez à la section problème [1132084][CR1132084].</span><span class="sxs-lookup"><span data-stu-id="51a1b-196">To review the history of this feature in the Chromium open-source project, navigate to Issue [1132084][CR1132084].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/copy-property-value.msft.png" alt-text="Copier la valeur de la propriété dans DevTools" lightbox="../../media/2020/11/copy-property-value.msft.png":::
         <span data-ttu-id="51a1b-198">Copier la valeur de la propriété dans DevTools</span><span class="sxs-lookup"><span data-stu-id="51a1b-198">Copy property value in DevTools</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/paste-property-value.msft.png" alt-text="Valeur de la propriété Paste dans le code Visual Studio" lightbox="../../media/2020/11/paste-property-value.msft.png":::
         <span data-ttu-id="51a1b-200">Valeur de la propriété Paste dans le code Visual Studio</span><span class="sxs-lookup"><span data-stu-id="51a1b-200">Paste property value in Visual Studio Code</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="51a1b-201">Personnaliser les raccourcis clavier à plusieurs pression</span><span class="sxs-lookup"><span data-stu-id="51a1b-201">Customize multi-press keyboard shortcuts</span></span>  

<!-- Title: Customize multi-press keyboard shortcuts  -->  
<!-- Subtitle: Create custom multi-press keyboard shortcuts in the shortcut editor.  -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::

<span data-ttu-id="51a1b-202">[Depuis la version 87 de Microsoft Edge][WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings], vous pouvez personnaliser les raccourcis clavier pour n’importe quelle action dans devtools.</span><span class="sxs-lookup"><span data-stu-id="51a1b-202">[Since Microsoft Edge version 87][WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings], you may customize keyboard shortcuts for any action in DevTools.</span></span>  <span data-ttu-id="51a1b-203">Dans la version 88 de Microsoft Edge, vous pouvez désormais créer des raccourcis clavier à plusieurs pression.</span><span class="sxs-lookup"><span data-stu-id="51a1b-203">In Microsoft Edge version 88, you may now create multi-press keyboard shortcuts.</span></span>  <span data-ttu-id="51a1b-204">Pour définir un raccourci pour une action dans le devtools, accédez à la [section][DevtoolsCustomizeIndexSettings]expériences de paramètres,  >  \*\*\*\* puis cochez la case en regard de activer l' **éditeur de raccourcis clavier**.</span><span class="sxs-lookup"><span data-stu-id="51a1b-204">To set a shortcut for an action in the DevTools, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments**  and choose the checkbox next to **Enable keyboard shortcut editor**.</span></span>  <span data-ttu-id="51a1b-205">Pour plus d’informations sur la personnalisation et la modification des raccourcis, accédez à [activer la fonctionnalité expérience de l’éditeur de raccourcis clavier][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span><span class="sxs-lookup"><span data-stu-id="51a1b-205">For more information about customizing and editing shortcuts, navigate to [Enable keyboard shortcut editor Experimental feature][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span></span>  

<span data-ttu-id="51a1b-206">Par exemple, la mise en surbrillance rouge affiche un raccourci clavier à plusieurs pression personnalisé pour l’action **commencer l’enregistrement des événements** .</span><span class="sxs-lookup"><span data-stu-id="51a1b-206">For example, the red highlight displays a multi-press keyboard shortcut customized for the **Start recording events** action.</span></span>  <span data-ttu-id="51a1b-207">Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de chrome, accédez à l' [#174309 du problème][CR174309].</span><span class="sxs-lookup"><span data-stu-id="51a1b-207">To review real-time updates on this feature in the Chromium open-source project, navigate to [Issue #174309][CR174309].</span></span>  

:::image type="complex" source="../../media/2020/11/multi-press-keyboard-shortcuts.msft.png" alt-text="Raccourcis clavier de cordes" lightbox="../../media/2020/11/multi-press-keyboard-shortcuts.msft.png":::
   <span data-ttu-id="51a1b-209">Raccourcis clavier à plusieurs pression</span><span class="sxs-lookup"><span data-stu-id="51a1b-209">Multi-press keyboard shortcuts</span></span>  
:::image-end:::  

## <span data-ttu-id="51a1b-210">Annonces du projet de chrome</span><span class="sxs-lookup"><span data-stu-id="51a1b-210">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <span data-ttu-id="51a1b-211">Nouveaux outils de visualisation d’angle CSS</span><span class="sxs-lookup"><span data-stu-id="51a1b-211">New CSS angle visualization tools</span></span>  

<span data-ttu-id="51a1b-212">DevTools dispose désormais d’une meilleure prise en charge du débogage d’angle CSS.</span><span class="sxs-lookup"><span data-stu-id="51a1b-212">DevTools now have better support for CSS angle debugging.</span></span>  <span data-ttu-id="51a1b-213">Lorsqu’un élément HTML de votre page est doté d’un angle CSS appliqué, une icône d’horloge s’affiche à côté de l’angle dans l’outil **styles** .</span><span class="sxs-lookup"><span data-stu-id="51a1b-213">When an HTML element on your page has CSS angle applied to it, a clock icon is displayed next to the angle in the **Styles** tool.</span></span>  <span data-ttu-id="51a1b-214">Pour activer ou désactiver la superposition de l’horloge, sélectionnez l’icône d’horloge.</span><span class="sxs-lookup"><span data-stu-id="51a1b-214">To toggle the clock overlay, choose the clock icon.</span></span>  <span data-ttu-id="51a1b-215">Pour modifier l’angle, sélectionnez un emplacement quelconque dans l’horloge ou faites glisser l’aiguille.</span><span class="sxs-lookup"><span data-stu-id="51a1b-215">To change the angle, choose anywhere in the clock or drag the needle.</span></span>  <span data-ttu-id="51a1b-216">Pour modifier la valeur de l’angle, vous pouvez également utiliser la souris et les raccourcis clavier.</span><span class="sxs-lookup"><span data-stu-id="51a1b-216">To change the angle value, you may also use mouse and keyboard shortcuts.</span></span>  <!--  To learn more, navigate to [Angle Clock][DevtoolsCssReferenceChangeAngleValueWithAngleClock].  -->  <span data-ttu-id="51a1b-217">Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de chrome, accédez à problèmes [1126178][CR1126178] et [1138633][CR1138633].</span><span class="sxs-lookup"><span data-stu-id="51a1b-217">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [1126178][CR1126178] and [1138633][CR1138633].</span></span>  

<!--todo:  add link when css angle clock section exists.  -->  

<span data-ttu-id="51a1b-218">L’angle CSS suivant est utilisé pour l’exemple.</span><span class="sxs-lookup"><span data-stu-id="51a1b-218">The following CSS angle is used for the example.</span></span>  

```css
background: linear-gradient(100deg, lightblue, pink);
```  

:::image type="complex" source="../../media/2020/11/css-angle.msft.png" alt-text="Angle CSS" lightbox="../../media/2020/11/css-angle.msft.png":::
   <span data-ttu-id="51a1b-220">Angle CSS</span><span class="sxs-lookup"><span data-stu-id="51a1b-220">CSS angle</span></span>  
:::image-end:::  

### <span data-ttu-id="51a1b-221">Simuler une taille de quota de stockage dans le volet stockage</span><span class="sxs-lookup"><span data-stu-id="51a1b-221">Simulate storage quota size in the Storage pane</span></span>  

<span data-ttu-id="51a1b-222">Vous pouvez à présent ignorer la taille de quota de stockage dans le volet **stockage** .</span><span class="sxs-lookup"><span data-stu-id="51a1b-222">You may now override storage quota size in the **Storage** pane.</span></span>  <span data-ttu-id="51a1b-223">Cette fonctionnalité permet de simuler différents appareils et de tester le comportement de votre site Web ou de votre application dans des scénarios de disponibilité du disque faible.</span><span class="sxs-lookup"><span data-stu-id="51a1b-223">This feature allows you to simulate different devices and test the behavior of your website or app in low disk availability scenarios.</span></span>  <span data-ttu-id="51a1b-224">Pour simuler le quota de stockage, effectuez les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="51a1b-224">To simulate the storage quota, complete the following actions.</span></span>  

1.  <span data-ttu-id="51a1b-225">Naviguez jusqu’à stockage d' **applications**  >  \*\*\*\*.</span><span class="sxs-lookup"><span data-stu-id="51a1b-225">Navigate to **Application** > **Storage**.</span></span>  
1.  <span data-ttu-id="51a1b-226">Activez la case à cocher **simuler le quota de stockage personnalisé** .</span><span class="sxs-lookup"><span data-stu-id="51a1b-226">Turn on the **Simulate custom storage quota** checkbox.</span></span>  
1.  <span data-ttu-id="51a1b-227">Entrez un numéro valide.</span><span class="sxs-lookup"><span data-stu-id="51a1b-227">Enter a valid number.</span></span>  
    
<span data-ttu-id="51a1b-228">Pour plus d’informations sur la façon d’émuler des appareils mobiles et d’autres fonctionnalités dans le DevTools, accédez à la section [émuler des appareils mobiles dans Microsoft Edge devtools ][DevtoolsDeviceModeIndex].</span><span class="sxs-lookup"><span data-stu-id="51a1b-228">For more information about how to emulate mobile devices and other features in the DevTools, navigate to [Emulate mobile devices in Microsoft Edge DevTools ][DevtoolsDeviceModeIndex].</span></span>  <span data-ttu-id="51a1b-229">Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de chrome, accédez à problèmes [945786][CR945786] et [1146985][CR1146985].</span><span class="sxs-lookup"><span data-stu-id="51a1b-229">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [945786][CR945786] and [1146985][CR1146985].</span></span>  

:::image type="complex" source="../../media/2020/11/storage-quota.msft.png" alt-text="Simuler la taille de quota de stockage" lightbox="../../media/2020/11/storage-quota.msft.png":::
   <span data-ttu-id="51a1b-231">Simuler la taille de quota de stockage</span><span class="sxs-lookup"><span data-stu-id="51a1b-231">Simulate storage quota size</span></span>  
:::image-end:::  

### <span data-ttu-id="51a1b-232">Signaler les erreurs CORS dans l’outil réseau</span><span class="sxs-lookup"><span data-stu-id="51a1b-232">Report CORS errors in the Network tool</span></span>  

<span data-ttu-id="51a1b-233">Évaluez cette fonctionnalité en accédant à [démonstration d’erreur cors][GlitchCorsErrors].</span><span class="sxs-lookup"><span data-stu-id="51a1b-233">Try out this feature by navigating to [CORS error demo][GlitchCorsErrors].</span></span>  <span data-ttu-id="51a1b-234">Ouvrez l’outil **réseau** , actualisez la page et observez la demande de réseau de l’échec.</span><span class="sxs-lookup"><span data-stu-id="51a1b-234">Open the **Network** tool, refresh the page, and observe the failed CORS network request.</span></span>  <span data-ttu-id="51a1b-235">La colonne État affiche l' **erreur cors**.</span><span class="sxs-lookup"><span data-stu-id="51a1b-235">The status column displays the **CORS error**.</span></span>  <span data-ttu-id="51a1b-236">Lorsque vous pointez sur l’erreur, l’info-bulle affiche maintenant le code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="51a1b-236">When you hover on the error, the tooltip now displays the error code.</span></span>  <span data-ttu-id="51a1b-237">Dans la version 87 et les versions antérieures de Microsoft Edge, DevTools affichait uniquement le statut generic **(Failed)** pour les erreurs cors.</span><span class="sxs-lookup"><span data-stu-id="51a1b-237">In Microsoft Edge version 87 and earlier, DevTools only displayed generic **(failed)** status for CORS errors.</span></span>  <span data-ttu-id="51a1b-238">Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de chrome, accédez à la section problème [1141824][CR1141824].</span><span class="sxs-lookup"><span data-stu-id="51a1b-238">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [1141824][CR1141824].</span></span>  

:::image type="complex" source="../../media/2020/11/cors-err.msft.png" alt-text="Erreurs CORS" lightbox="../../media/2020/11/cors-err.msft.png":::
   <span data-ttu-id="51a1b-240">Erreurs CORS</span><span class="sxs-lookup"><span data-stu-id="51a1b-240">CORS errors</span></span>  
:::image-end:::  

### <span data-ttu-id="51a1b-241">Mises à jour de l’affichage des détails du cadre</span><span class="sxs-lookup"><span data-stu-id="51a1b-241">Frame details view updates</span></span>  

#### <span data-ttu-id="51a1b-242">Informations d’isolement sur une origine dans l’affichage des détails du cadre</span><span class="sxs-lookup"><span data-stu-id="51a1b-242">Cross-origin isolation information in the Frame details view</span></span>  

<span data-ttu-id="51a1b-243">Le statut isolé entre l’origine est désormais affiché dans la section **isolement du & de sécurité** .</span><span class="sxs-lookup"><span data-stu-id="51a1b-243">The cross-origin isolated status is now displayed under the **Security & Isolation** section.</span></span>  <span data-ttu-id="51a1b-244">La nouvelle section disponibilité de l' **API** affiche la disponibilité du `SharedArrayBuffer` s \ (SAB \) et si les mémoires tampons pourraient être partagées en utilisant `postMessage()` .</span><span class="sxs-lookup"><span data-stu-id="51a1b-244">The new **API availability** section displays the availability of `SharedArrayBuffer`s \(SAB\) and whether the buffers may be shared using `postMessage()`.</span></span>  <span data-ttu-id="51a1b-245">Un avertissement de dépréciation s’affiche si le SAB et `postMessage()` est actuellement disponible, mais que le contexte n’est pas isolé.</span><span class="sxs-lookup"><span data-stu-id="51a1b-245">A deprecation warning displays if the SAB and `postMessage()` is currently available, but the context is not cross-origin isolated.</span></span>  <span data-ttu-id="51a1b-246">Pour plus d’informations sur l’isolement entre les origines et sur les raisons de leur nécessité `SharedArrayBuffers` , accédez à [WindowOrWorkerGlobalScope. crossOriginIsolated][MdnWindoworworkerglobalscopeCrossoriginisolated].</span><span class="sxs-lookup"><span data-stu-id="51a1b-246">For more information about cross-origin isolation and why it is required for features like `SharedArrayBuffers`, navigate to [WindowOrWorkerGlobalScope.crossOriginIsolated][MdnWindoworworkerglobalscopeCrossoriginisolated].</span></span>  <span data-ttu-id="51a1b-247">Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de chrome, accédez à la section problème [1139899][CR1139899].</span><span class="sxs-lookup"><span data-stu-id="51a1b-247">To review real-time updates of this feature in the Chromium open-source project, navigate to Issue [1139899][CR1139899].</span></span>  

:::image type="complex" source="../../media/2020/11/frame-cross-origin-isolated-api.msft.png" alt-text="Informations sur l’origine" lightbox="../../media/2020/11/frame-cross-origin-isolated-api.msft.png":::
   <span data-ttu-id="51a1b-249">Informations sur l’origine</span><span class="sxs-lookup"><span data-stu-id="51a1b-249">Cross-origin information</span></span>  
:::image-end:::  

#### <span data-ttu-id="51a1b-250">Nouvelles informations des travailleurs sur le Web dans l’affichage Détails du cadre</span><span class="sxs-lookup"><span data-stu-id="51a1b-250">New Web Workers information in the Frame details view</span></span>  

<span data-ttu-id="51a1b-251">DevTools organise désormais les travailleurs sur le Web au cadre du cadre parent approprié.</span><span class="sxs-lookup"><span data-stu-id="51a1b-251">DevTools now organizes web workers under the relevant parent frame.</span></span>  <span data-ttu-id="51a1b-252">Par exemple, si le `someName` cadre est créé `worker.js` , il `worker.js` apparaît `someName` dans la liste **trames** .</span><span class="sxs-lookup"><span data-stu-id="51a1b-252">For example, if the `someName` frame creates `worker.js`, then `worker.js` appears under `someName` in the **Frames** list.</span></span>  <span data-ttu-id="51a1b-253">Pour afficher les détails du travailleur Web, effectuez les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="51a1b-253">To view the details of the web worker, complete the following actions.</span></span>  

1.  <span data-ttu-id="51a1b-254">Ouvrir l’outil de l' **application** .</span><span class="sxs-lookup"><span data-stu-id="51a1b-254">Open **Application** tool.</span></span>  
1.  <span data-ttu-id="51a1b-255">Développez un cadre qui contient des travailleurs Web.</span><span class="sxs-lookup"><span data-stu-id="51a1b-255">Expand a frame that contains web workers.</span></span>  
1.  <span data-ttu-id="51a1b-256">Développez l’arborescence **travailleurs** .</span><span class="sxs-lookup"><span data-stu-id="51a1b-256">Expand the **Workers** tree.</span></span>  
1.  <span data-ttu-id="51a1b-257">Choisissez un travailleur.</span><span class="sxs-lookup"><span data-stu-id="51a1b-257">Choose a worker.</span></span>  
    
<span data-ttu-id="51a1b-258">Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de chrome, accédez à problèmes [1122507][CR1122507] et [1051466][CR1051466].</span><span class="sxs-lookup"><span data-stu-id="51a1b-258">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [1122507][CR1122507] and [1051466][CR1051466].</span></span>  

:::image type="complex" source="../../media/2020/11/application-frames-service-workers.msft.png" alt-text="Informations des travailleurs Web" lightbox="../../media/2020/11/application-frames-service-workers.msft.png":::
   <span data-ttu-id="51a1b-260">Informations des travailleurs Web</span><span class="sxs-lookup"><span data-stu-id="51a1b-260">Web workers information</span></span>  
:::image-end:::  

#### <span data-ttu-id="51a1b-261">Afficher les détails d’un cadre ouvrant pour les fenêtres ouvertes</span><span class="sxs-lookup"><span data-stu-id="51a1b-261">Display opener frame details for opened windows</span></span>  

<span data-ttu-id="51a1b-262">DevTools organise désormais les [fenêtres][MdnWindowConstructors] ouvertes sous le [Frame][MdnWindowFrames]parent approprié.</span><span class="sxs-lookup"><span data-stu-id="51a1b-262">DevTools now organizes opened [Windows][MdnWindowConstructors] under the relevant parent [frame][MdnWindowFrames].</span></span>  <span data-ttu-id="51a1b-263">Par exemple, si le `top` cadre ouvre a `Window` à `https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium` , la `Window` figure située sous `top` dans la liste des **cadres** .</span><span class="sxs-lookup"><span data-stu-id="51a1b-263">For example, if the `top` frame opens a `Window` to `https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium`, then the `Window` appears under `top` in the **Frames** list.</span></span>  

<span data-ttu-id="51a1b-264">Pour afficher le cadre responsable de l’ouverture d’une autre fenêtre dans l’outil **éléments** , effectuez les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="51a1b-264">To reveal the frame responsible for opening another Window in the **Elements** tool, complete the following actions.</span></span>  

1.  <span data-ttu-id="51a1b-265">Ouvrez l’arborescence des **cadres** .</span><span class="sxs-lookup"><span data-stu-id="51a1b-265">Open the **Frames** tree.</span></span>  
1.  <span data-ttu-id="51a1b-266">Développez **fenêtres ouvertes** et choisissez le `Window` cadre parent que vous voulez connaître.</span><span class="sxs-lookup"><span data-stu-id="51a1b-266">Expand **Opened Windows** and choose the `Window` for the parent frame you want to know.</span></span>  
1.  <span data-ttu-id="51a1b-267">Cliquez sur le lien d' **encadrement d’ouverture** .</span><span class="sxs-lookup"><span data-stu-id="51a1b-267">Choose the **Opener Frame** link.</span></span>  

<span data-ttu-id="51a1b-268">Les détails sont affichés sur l’image à l’origine de l’ouverture d’une autre `Window` .</span><span class="sxs-lookup"><span data-stu-id="51a1b-268">The details are displayed about which frame caused the opening of another `Window`.</span></span>  <span data-ttu-id="51a1b-269">Pour afficher l’outil d’ouverture dans l’outil **éléments** , effectuez les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="51a1b-269">To reveal the opener in the **Elements** tool, complete the following actions.</span></span>  

1.  <span data-ttu-id="51a1b-270">Ouvrez l’arborescence des **cadres** .</span><span class="sxs-lookup"><span data-stu-id="51a1b-270">Open the **Frames** tree.</span></span>  
1.  <span data-ttu-id="51a1b-271">Choisissez une fenêtre ouverte pour ouvrir les `Window` Détails.</span><span class="sxs-lookup"><span data-stu-id="51a1b-271">Choose an opened window to open the `Window` details.</span></span>  
1.  <span data-ttu-id="51a1b-272">Cliquez sur le lien d' **encadrement d’ouverture** .</span><span class="sxs-lookup"><span data-stu-id="51a1b-272">Choose the **Opener Frame** link.</span></span>  
    
<span data-ttu-id="51a1b-273">Pour passer en revue l’historique de cette fonctionnalité dans le projet open-source de chrome, accédez à la section problème [1107766][CR1107766].</span><span class="sxs-lookup"><span data-stu-id="51a1b-273">To review the history of this feature in the Chromium open-source project, navigate to Issue [1107766][CR1107766].</span></span>  

:::image type="complex" source="../../media/2020/11/application-frames-opened-windows-security-opener-frame.msft.png" alt-text="Informations de trames ouvertes" lightbox="../../media/2020/11/application-frames-opened-windows-security-opener-frame.msft.png":::
   <span data-ttu-id="51a1b-275">Informations de trames ouvertes</span><span class="sxs-lookup"><span data-stu-id="51a1b-275">Opened frame details</span></span>  
:::image-end:::  

### <span data-ttu-id="51a1b-276">Copy StackTrace pour l’initiateur réseau</span><span class="sxs-lookup"><span data-stu-id="51a1b-276">Copy stacktrace for network initiator</span></span>  

<span data-ttu-id="51a1b-277">Pour copier le StackTrace dans le presse-papiers, effectuez les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="51a1b-277">To copy the stacktrace to your clipboard, complete the following actions.</span></span>  

1.  <span data-ttu-id="51a1b-278">Ouvrir le menu contextuel \ (cliquez avec le bouton droit sur \).</span><span class="sxs-lookup"><span data-stu-id="51a1b-278">Open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="51a1b-279">Choisissez **copier**le  >  **StackTrace**.</span><span class="sxs-lookup"><span data-stu-id="51a1b-279">Choose **Copy** > **Copy stacktrace**.</span></span>  
    
<span data-ttu-id="51a1b-280">Pour passer en revue l’historique de cette fonctionnalité dans le projet open-source de chrome, accédez à la section problème [1139615][CR1139615].</span><span class="sxs-lookup"><span data-stu-id="51a1b-280">To review the history of this feature in the Chromium open-source project, navigate to Issue [1139615][CR1139615].</span></span>

:::image type="complex" source="../../media/2020/11/copy-stacktrace.msft.png" alt-text="Copier StackTrace" lightbox="../../media/2020/11/copy-stacktrace.msft.png":::
   <span data-ttu-id="51a1b-282">Copier StackTrace</span><span class="sxs-lookup"><span data-stu-id="51a1b-282">Copy stacktrace</span></span>  
:::image-end:::  

### <span data-ttu-id="51a1b-283">Aperçu de la valeur de la variable WASM sur mouseover</span><span class="sxs-lookup"><span data-stu-id="51a1b-283">Preview Wasm variable value on mouseover</span></span>  

<span data-ttu-id="51a1b-284">Utilisez cette fonction pour vérifier la valeur d’une variable webassembly \ (WASM \) lorsque votre code est en pause.</span><span class="sxs-lookup"><span data-stu-id="51a1b-284">Use this feature to review the value of a WebAssembly \(Wasm\) variable when your code is paused.</span></span>  <span data-ttu-id="51a1b-285">Pour afficher la valeur actuelle d’une variable, pointez sur une variable.</span><span class="sxs-lookup"><span data-stu-id="51a1b-285">To display the current value of a variable, hover on a variable.</span></span>  <span data-ttu-id="51a1b-286">Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de chrome, accédez à problèmes [1058836][CR1058836] et [1071432][CR1071432].</span><span class="sxs-lookup"><span data-stu-id="51a1b-286">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [1058836][CR1058836] and [1071432][CR1071432].</span></span>  

:::image type="complex" source="../../media/2020/11/wasm-mouseover.msft.png" alt-text="Prévisualiser la variable WASM sur mouseover" lightbox="../../media/2020/11/wasm-mouseover.msft.png":::
   <span data-ttu-id="51a1b-288">Prévisualiser la variable WASM sur mouseover</span><span class="sxs-lookup"><span data-stu-id="51a1b-288">Preview Wasm variable on mouseover</span></span>  
:::image-end:::  

### <span data-ttu-id="51a1b-289">Unités de mesure cohérentes pour la taille des fichiers et de la mémoire</span><span class="sxs-lookup"><span data-stu-id="51a1b-289">Consistent units of measurement for sizes of files and memory</span></span>  

<span data-ttu-id="51a1b-290">DevTools est désormais toujours utilisé `kB` pour l’affichage des tailles de fichiers et de mémoire.</span><span class="sxs-lookup"><span data-stu-id="51a1b-290">DevTools now consistently use `kB` for displaying sizes of files and memory.</span></span>  <span data-ttu-id="51a1b-291">Auparavant DevTools mélangées `kB` et `KiB` .</span><span class="sxs-lookup"><span data-stu-id="51a1b-291">Previously DevTools mixed `kB` and `KiB`.</span></span>

*   `kB` <span data-ttu-id="51a1b-292">ou kilo-octets \ (10 ^ 3 ou 1000 octets \)</span><span class="sxs-lookup"><span data-stu-id="51a1b-292">or kilobyte \(10^3 or 1000 bytes\)</span></span>  
*   `KiB` <span data-ttu-id="51a1b-293">ou kibibyte \ (2 ^ 10 ou 1024 octets \)</span><span class="sxs-lookup"><span data-stu-id="51a1b-293">or kibibyte \(2^10 or 1024 bytes\)</span></span>  
    
<span data-ttu-id="51a1b-294">Par exemple, l’outil **réseau** précédemment utilisé `kB` dans les étiquettes, mais utilisé `KiB` dans les calculs.</span><span class="sxs-lookup"><span data-stu-id="51a1b-294">For example, the **Network** tool previously used `kB` in the labels, but used `KiB` in calculations.</span></span>  <span data-ttu-id="51a1b-295">Votre avis a démontré que cette incohérence a causé une confusion.</span><span class="sxs-lookup"><span data-stu-id="51a1b-295">Your feedback showed that this inconsistency caused confusion.</span></span>  <span data-ttu-id="51a1b-296">Pour passer en revue l’historique de cette fonctionnalité dans le projet open-source de chrome, accédez à la section problème [1035309][CR1035309].</span><span class="sxs-lookup"><span data-stu-id="51a1b-296">To review the history of this feature in the Chromium open-source project, navigate to Issue [1035309][CR1035309].</span></span>  

## <span data-ttu-id="51a1b-297">Télécharger les canaux Microsoft Edge preview</span><span class="sxs-lookup"><span data-stu-id="51a1b-297">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="51a1b-298">Si vous utilisez Windows, Linux ou macOS, envisagez d’utiliser [Microsoft Edge Preview] [MicrosoftEdgePreviewChannels] en tant que navigateur de développement par défaut.</span><span class="sxs-lookup"><span data-stu-id="51a1b-298">If you are on Windows, Linux, or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="51a1b-299">Les canaux d’aperçu vous permettent d’accéder aux dernières fonctionnalités de DevTools.</span><span class="sxs-lookup"><span data-stu-id="51a1b-299">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="51a1b-300">Contacter l’équipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="51a1b-300">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[Devtools3dViewIndex]: /microsoft-edge/devtools-guide-chromium/3d-view/index "Affichage 3D | Documents Microsoft"  
[DevtoolsConsoleIndex]: /microsoft-edge/devtools-guide-chromium/console/index "Présentation de la console | Documents Microsoft"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Paramètres-personnaliser Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Émuler des appareils mobiles dans Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-keyboard-shortcut-editor "Activer l’éditeur de raccourcis clavier-fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-composited-layers-in-3d-view "Activer les couches composites dans l’affichage 3D-fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsIssuesIndex]: /microsoft-edge/devtools-guide-chromium/issues/index "Recherchez et corrigez les problèmes liés à l’outil problèmes dans Microsoft Edge DevTools Documents Microsoft"  
[DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard]: /microsoft-edge/devtools-guide-chromium/network/reference#copy-formatted-response-json-to-the-clipboard "Copier la réponse mise en forme JSON dans le presse-papiers-référence d’analyse du réseau | Documents Microsoft"  
[DevtoolsNetworkReferenceViewTimingBreakdownRequest]: /microsoft-edge/devtools-guide-chromium/network/reference#view-the-timing-breakdown-of-a-request "Afficher la répartition du temps d’une demande de référence d’analyse du réseau | Documents Microsoft"  
[WebDriverChromiumMain]: /microsoft-edge/webdriver-chromium "Utiliser le WebDriver (chrome) pour l’automatisation des tests | Documents Microsoft"  

<!--  [DevtoolsCssReferenceChangeAngleValueWithAngleClock]: /microsoft-edge/devtools-guide-chromium/css/reference#change-angle-value-with-the-angle-clock "Change angle value with the Angle Clock - CSS reference | Microsoft Docs"  -->  

[ProgressiveWebAppsChromiumIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Applications Web progressives sur Windows | Documents Microsoft"  

[WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/10/devtools#customize-keyboard-shortcuts-in-settings "Personnaliser les raccourcis clavier dans les paramètres-nouveautés de DevTools (Microsoft Edge 87) | Documents Microsoft"  
[WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/06/devtools#webhint-feedback-in-the-issues-panel "Commentaires sur les webhint dans le volet problèmes-nouveautés de DevTools (Microsoft Edge 85) | Documents Microsoft"  

[MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver#downloads "Télécharger WebDriver | Développeur Microsoft"  

[MicrosoftinsiderDownloadPlatformLinux]: https://www.microsoftedgeinsider.com/download?platform=linux "Télécharger les canaux Microsoft Edge Insider"  

[VisualStudioCode]: https://code.visualstudio.com "Code Visual Studio"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Bugs du chrome"  

[CR174309]: https://crbug.com/174309 "Problème 174309: DevTools: autoriser pour personnaliser les raccourcis clavier/les combinaisons de touches | Bugs du chrome"  
[CR945786]: https://crbug.com/945786 "Problème 945786: DevTools: autoriser le remplacement de Navigator. Storage. Estimate () | Bugs du chrome"  
[CR1029427]: https://crbug.com/1029427 "Problème 1029427: réduisez la surcharge des performances de l’envoi de messages de protocole au premier plan | Bugs du chrome"  
[CR1035309]: https://crbug.com/1035309 "Problème 1035309: DevTools doit utiliser de manière cohérente Mo pour signifier mégaoctets, pas mebibyte | Bugs du chrome"  
[CR1051466]: https://crbug.com/1051466 "Problème 1051466: prendre en charge le débogage COOP/COEP dans DevTools | Bugs du chrome"  
[CR1058836]: https://crbug.com/1058836 "Problème 1058836: UX problèmes liés au débogage de WASM Bugs du chrome"  
[CR1071432]: https://crbug.com/1071432 "Problème 1071432: ☂️ WASM basique pour les développeurs | Bugs du chrome"  
[CR1107766]: https://crbug.com/1107766 "Problème 1107766: Affichez des informations sur les trames générées par’Window. Open () 'dans l’arborescence de trames | Bugs du chrome"  
[CR1122507]: https://crbug.com/1122507 "Problème 1122507: informations sur le travailleur de surface dans l’arborescence d’images | Bugs du chrome"  
[CR1126178]: https://crbug.com/1126178 "Problème 1126178: ☂ DevTools: CSS <type> composants | Bugs du chrome"  
[CR1130556]: https://crbug.com/1130556 "Problème 1130556: DevTools: test de substitution d’image (émulation) | Bugs du chrome"  
[CR1132084]: https://crbug.com/1132084 "Problème 1132084: il n’y a pas de moyen simple de copier la charge utile de requête JSON | Bugs du chrome"  
[CR1136394]: https://crbug.com/1136394 "Problème 1136394: outils Flexbox | Bugs du chrome"  
[CR1138633]: https://crbug.com/1138633 "Problème 1138633: DevTools: CSS <angle> le composant doit refléter son apparence de propriété dans l’arrière-plan d’horloge | Bugs du chrome"  
[CR1139615]: https://crbug.com/1139615 "Problème 1139615: l’initiateur réseau doit permettre de copier la trace de pile | Bugs du chrome"  
[CR1139899]: https://crbug.com/1139899 "Problème 1139899: signaler la disponibilité des API contrôlées dans l’affichage Détails de la trame | Bugs du chrome"  
[CR1139945]: https://crbug.com/1139945 "Problème 1139945: icônes pour les propriétés CSS de Flexbox dans le panneau Styles | Bugs du chrome"  
[CR1141824]: https://crbug.com/1141824 "Problème 1141824: améliorer le signalement des erreurs CORS dans DevTools | Bugs du chrome"  
[CR1144090]: https://crbug.com/1144090 "Problème 1144090: ajoutez des ornements de style Flex à l’arborescence des éléments | Bugs du chrome"  
[CR1146985]: https://crbug.com/1146985 "Problème 1146985: le texte supprimé reste affiché dans le champ texte de la section «stockage» de la fenêtre outils de développement | Bugs du chrome"  

[GlitchCorsErrors]: https://cors-errors.glitch.me "Erreurs CORS | Problème"  

[MdnCors]: https://developer.mozilla.org/docs/Web/HTTP/CORS "Partage de ressources à l’origine (CORS) | MDN"  
[MdnUsingCssCustomProperties]: https://developer.mozilla.org/docs/Web/CSS/Using_CSS_custom_properties "Utilisation de propriétés personnalisées CSS (variables) | MDN"  
[MdnWindowConstructors]: https://developer.mozilla.org/docs/Web/API/Window#Constructors "Constructeurs-fenêtre | MDN"  
[MdnWindowFrames]: https://developer.mozilla.org/docs/Web/API/Window/frames "Fenêtre. frames | MDN"  
[MdnWindoworworkerglobalscopeCrossoriginisolated]: https://developer.mozilla.org/docs/Web/API/WindowOrWorkerGlobalScope/crossOriginIsolated "WindowOrWorkerGlobalScope. crossOriginIsolated | MDN"  

[WebhintMain]: https://webhint.io "Astuce"  
[WebhintUserGuideHintsAccessibility]: https://webhint.io/docs/user-guide/hints/accessibility "Accessibilité | Astuce"  
[WebhintUserGuideHintsCompatibility]: https://webhint.io/docs/user-guide/hints/compatibility "Compatibilité | Astuce"  
[WebhintUserGuideHintsPerformance]: https://webhint.io/docs/user-guide/hints/performance "Performance | Astuce"  
[WebhintUserGuideHintsPitfalls]: https://webhint.io/docs/user-guide/hints/pitfalls "Pièges | Astuce"  
[WebhintUserGuideHintsPwa]: https://webhint.io/docs/user-guide/hints/pwa "PWA | Astuce"  
[WebhintUserGuideHintsSecurity]: https://webhint.io/docs/user-guide/hints/security "Sécurité | Astuce"  

> [!NOTE]
> <span data-ttu-id="51a1b-351">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="51a1b-351">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="51a1b-352">La page d’origine est disponible [ici](https://developers.google.com/web/updates/2020/11/devtools/index) et est créée par [Jecelyn Yeen][JecelynYeen] \ (développeurs, chrome devtools \).</span><span class="sxs-lookup"><span data-stu-id="51a1b-352">The original page is found [here](https://developers.google.com/web/updates/2020/11/devtools/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="51a1b-354">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="51a1b-354">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
