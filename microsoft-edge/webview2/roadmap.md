---
description: En savoir plus sur les étapes suivantes pour WebView2
title: Feuille de route pour Microsoft Edge WebView 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html
ms.openlocfilehash: 0f51b5cab32bdb9b9aa9b6baceef5fe5a17eea54
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398412"
---
# <a name="microsoft-edge-webview2-roadmap"></a><span data-ttu-id="636d4-104">Feuille de route Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="636d4-104">Microsoft Edge WebView2 roadmap</span></span>  

> [!NOTE]
> <span data-ttu-id="636d4-105">Last Updated: November 2020</span><span class="sxs-lookup"><span data-stu-id="636d4-105">Last Updated:  November 2020</span></span>  

<span data-ttu-id="636d4-106">Le contrôle WebView2 permet aux développeurs d’incorporer des technologies web dans leurs applications natives.</span><span class="sxs-lookup"><span data-stu-id="636d4-106">The WebView2 control allows developers to embed web technologies in their native applications.</span></span>  <span data-ttu-id="636d4-107">La page suivante décrit la feuille de route prospective pour WebView2.</span><span class="sxs-lookup"><span data-stu-id="636d4-107">The following page outlines the prospective roadmap for WebView2.</span></span>  

> [!NOTE]
> <span data-ttu-id="636d4-108">WebView2 est en cours de développement actif et la feuille de route continue d’évoluer en fonction des changements de marché et des commentaires des clients. Notez donc que les plans présentés ici ne sont pas exhaustifs et peuvent faire l’objet de modifications.</span><span class="sxs-lookup"><span data-stu-id="636d4-108">WebView2 is under active development and the roadmap continues to evolve based on market changes and customer feedback, so please note that the plans outlined here are not exhaustive and are subject to change.</span></span>  

<span data-ttu-id="636d4-109">Si vous avez des préoccupations ou des questions sur la feuille de route, faites part de vos commentaires dans le [repo de commentaires.][GithubMicrosoftedgeWebviewfeedbackMain]</span><span class="sxs-lookup"><span data-stu-id="636d4-109">If you have concerns or questions about the Roadmap, provide your feedback in the [feedback repo][GithubMicrosoftedgeWebviewfeedbackMain].</span></span>  

<span data-ttu-id="636d4-110">L’équipe WebView2 planifie les efforts majeurs suivants pour les futures mises à jour.</span><span class="sxs-lookup"><span data-stu-id="636d4-110">The WebView2 team is planning the following major efforts for future updates.</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="636d4-111">Programme d’installation Runtime WebView2</span><span class="sxs-lookup"><span data-stu-id="636d4-111">WebView2 Runtime Installer</span></span>  
   :::column-end:::
   :::column span="2":::
      *   <span data-ttu-id="636d4-112">T4 2020</span><span class="sxs-lookup"><span data-stu-id="636d4-112">Q4 2020</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      <span data-ttu-id="636d4-113">Version corrigée</span><span class="sxs-lookup"><span data-stu-id="636d4-113">Fixed Version</span></span>  
   :::column-end:::
   :::column span="2":::
      *   <span data-ttu-id="636d4-114">T4 2020</span><span class="sxs-lookup"><span data-stu-id="636d4-114">Q4 2020</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      <span data-ttu-id="636d4-115">Disponibilité générale</span><span class="sxs-lookup"><span data-stu-id="636d4-115">General Availability</span></span>  
   :::column-end:::
   :::column span="2":::
      *   <span data-ttu-id="636d4-116">Win32 C/C++ \(Q4 2020\)</span><span class="sxs-lookup"><span data-stu-id="636d4-116">Win32 C/C++ \(Q4 2020\)</span></span>  
      *   <span data-ttu-id="636d4-117">.NET \(Q4 2020\)</span><span class="sxs-lookup"><span data-stu-id="636d4-117">.NET \(Q4 2020\)</span></span>  
      *   [<span data-ttu-id="636d4-118">WinUI 3.0</span><span class="sxs-lookup"><span data-stu-id="636d4-118">WinUI 3.0</span></span>][GithubMicrosoftUiXamlRoadmap]  
   :::column-end:::
:::row-end:::  

## <a name="webview2-runtime-and-installer"></a><span data-ttu-id="636d4-119">Runtime et programme d’installation WebView2</span><span class="sxs-lookup"><span data-stu-id="636d4-119">WebView2 Runtime and Installer</span></span>  

<span data-ttu-id="636d4-120">[Un modèle de distribution persistant][ConceptDistributionEvergreenModel] vous permet de cibler ou d’installer le runtime WebView2 sur l’ordinateur de votre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="636d4-120">[Evergreen distribution model][ConceptDistributionEvergreenModel] allows you to target or chain install the WebView2 Runtime onto your user's machine.</span></span>  <span data-ttu-id="636d4-121">Le programme d’installation et le runtime WebView2 persistants ont atteint la disponibilité générale \(GA\).</span><span class="sxs-lookup"><span data-stu-id="636d4-121">The Evergreen WebView2 Runtime and installer has reached General Availability \(GA\).</span></span>  

## <a name="fixed-version"></a><span data-ttu-id="636d4-122">Version fixe</span><span class="sxs-lookup"><span data-stu-id="636d4-122">Fixed version</span></span>  

<span data-ttu-id="636d4-123">[Le modèle de distribution de version][ConceptsDistributionFixedVersionModel] fixe vous permet de mettre en package les binaires Microsoft Edge à l’intérieur de votre application native.</span><span class="sxs-lookup"><span data-stu-id="636d4-123">[Fixed version distribution model][ConceptsDistributionFixedVersionModel] allows you to package the Microsoft Edge binaries inside your native application.</span></span>  <span data-ttu-id="636d4-124">La version fixe a atteint la disponibilité générale \(GA\).</span><span class="sxs-lookup"><span data-stu-id="636d4-124">The Fixed Version has reached General Availability \(GA\).</span></span>  

## <a name="general-availability"></a><span data-ttu-id="636d4-125">Disponibilité générale</span><span class="sxs-lookup"><span data-stu-id="636d4-125">General availability</span></span>  

### <a name="win32-cc"></a><span data-ttu-id="636d4-126">Win32 C/C++</span><span class="sxs-lookup"><span data-stu-id="636d4-126">Win32 C/C++</span></span>  

<span data-ttu-id="636d4-127">Le SDK Win32 C/C++ a atteint la ga.</span><span class="sxs-lookup"><span data-stu-id="636d4-127">The Win32 C/C++ SDK has reached GA.</span></span>  

### <a name="net"></a><span data-ttu-id="636d4-128">.NET</span><span class="sxs-lookup"><span data-stu-id="636d4-128">.NET</span></span>  

<span data-ttu-id="636d4-129">Le SDK .NET a atteint la ga.</span><span class="sxs-lookup"><span data-stu-id="636d4-129">The .NET SDK has reached GA.</span></span> 

### <a name="winui-30"></a><span data-ttu-id="636d4-130">WinUI 3.0</span><span class="sxs-lookup"><span data-stu-id="636d4-130">WinUI 3.0</span></span>  

<span data-ttu-id="636d4-131">Vous pouvez accéder à WebView2 dans vos applications UWP à l’aide de [Win UI 3.0,][UwpToolkitsWinui3Index]actuellement en alpha.</span><span class="sxs-lookup"><span data-stu-id="636d4-131">You can access WebView2 in your UWP applications using [Win UI 3.0][UwpToolkitsWinui3Index], currently in alpha.</span></span>  <span data-ttu-id="636d4-132">Pour plus d’informations sur la mise à jour, accédez à la feuille de route de la bibliothèque [d’interface utilisateur Windows.][GithubMicrosoftUiXamlRoadmap]</span><span class="sxs-lookup"><span data-stu-id="636d4-132">For more information about keeping up to date, navigate to [Windows UI Library Roadmap][GithubMicrosoftUiXamlRoadmap].</span></span>  

<!-- links -->  

[ConceptDistributionEvergreenModel]: ./concepts/distribution.md#evergreen-distribution-mode "Modèle de distribution persistant : distribution d’applications à l’aide de WebView2 | Documents Microsoft"  
[ConceptsDistributionFixedVersionModel]: ./concepts/distribution.md#fixed-version-distribution-mode "Modèle de distribution de version fixe : distribution d’applications à l’aide de WebView2 | Documents Microsoft"  

[UwpToolkitsWinui3Index]: /uwp/toolkits/winui3/index "Windows UI Library 3.0 Preview 1 (mai 2020) | Documents Microsoft"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires WebView - MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftUiXamlRoadmap]: https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md "Feuille de route de la bibliothèque d’interface utilisateur Windows - Microsoft/microsoft-ui-xaml | GitHub"  
