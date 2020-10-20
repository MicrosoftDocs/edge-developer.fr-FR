---
description: En savoir plus sur les nouveautés à venir pour WebView2
title: Introduction à la WebView 2 de Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 52a2f6d9ef3447955554a5507c3eaab39e6b6a9e
ms.sourcegitcommit: af91bfc3e6d8afc51f0fbbc0fe392262f424225c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/19/2020
ms.locfileid: "11120367"
---
# <span data-ttu-id="c0acd-104">Introduction à Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="c0acd-104">Microsoft Edge WebView2 roadmap</span></span>  

##### <span data-ttu-id="c0acd-105">Dernière mise à jour: 2020 Oct</span><span class="sxs-lookup"><span data-stu-id="c0acd-105">Last Updated: Oct 2020</span></span>  

<span data-ttu-id="c0acd-106">Le contrôle WebView2 permet aux développeurs d’incorporer des technologies Web dans leurs applications natives.</span><span class="sxs-lookup"><span data-stu-id="c0acd-106">The WebView2 control allows developers to embed web technologies in their native applications.</span></span>  <span data-ttu-id="c0acd-107">La page suivante présente la procédure prospective pour WebView2.</span><span class="sxs-lookup"><span data-stu-id="c0acd-107">The following page outlines the prospective roadmap for WebView2.</span></span>  

> [!NOTE]
> <span data-ttu-id="c0acd-108">WebView2 est en cours de développement actif et la présentation continue à évoluer en fonction des variations du marché et des commentaires des clients. Veuillez noter que les plans décrits ici ne sont pas exhaustifs et peuvent faire l’objet de modifications.</span><span class="sxs-lookup"><span data-stu-id="c0acd-108">WebView2 is under active development and the roadmap continues to evolve based on market changes and customer feedback, so please note that the plans outlined here are not exhaustive and are subject to change.</span></span>  

<span data-ttu-id="c0acd-109">Si vous avez des inquiétudes ou des questions concernant la formule d’introduction, reportez-vous à la [référentiel Samples][GithubMicrosoftedgeWebviewfeedbackMain]de vos commentaires.</span><span class="sxs-lookup"><span data-stu-id="c0acd-109">If you have concerns or questions about the Roadmap, provide your feedback in the [feedback repo][GithubMicrosoftedgeWebviewfeedbackMain].</span></span>  

<span data-ttu-id="c0acd-110">L’équipe WebView2 planifie les efforts importants suivants pour les mises à jour ultérieures.</span><span class="sxs-lookup"><span data-stu-id="c0acd-110">The WebView2 team is planning the following major efforts for future updates.</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="c0acd-111">Programme d’installation d’WebView2 Runtime</span><span class="sxs-lookup"><span data-stu-id="c0acd-111">WebView2 Runtime Installer</span></span>  
   :::column-end:::
   :::column span="2":::
      *   <span data-ttu-id="c0acd-112">4e trimestre 2020</span><span class="sxs-lookup"><span data-stu-id="c0acd-112">Q4 2020</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      <span data-ttu-id="c0acd-113">Version corrigée</span><span class="sxs-lookup"><span data-stu-id="c0acd-113">Fixed Version</span></span>  
   :::column-end:::
   :::column span="2":::
      *   <span data-ttu-id="c0acd-114">4e trimestre 2020</span><span class="sxs-lookup"><span data-stu-id="c0acd-114">Q4 2020</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      <span data-ttu-id="c0acd-115">Disponibilité générale</span><span class="sxs-lookup"><span data-stu-id="c0acd-115">General Availability</span></span>  
   :::column-end:::
   :::column span="2":::
      *   <span data-ttu-id="c0acd-116">Win32 C/C++ \ (4e trim 2020 \)</span><span class="sxs-lookup"><span data-stu-id="c0acd-116">Win32 C/C++ \(Q4 2020\)</span></span>  
      *   <span data-ttu-id="c0acd-117">.NET \ (4E TRIM 2020 \)</span><span class="sxs-lookup"><span data-stu-id="c0acd-117">.NET \(Q4 2020\)</span></span>  
      *   [<span data-ttu-id="c0acd-118">WinUI 3.0</span><span class="sxs-lookup"><span data-stu-id="c0acd-118">WinUI 3.0</span></span>][GithubMicrosoftUiXamlRoadmap]  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="c0acd-119">Programme d’exécution et de WebView2</span><span class="sxs-lookup"><span data-stu-id="c0acd-119">WebView2 Runtime and Installer</span></span>  

<span data-ttu-id="c0acd-120">Le [modèle de distribution persistant][ConceptDistributionEvergreenModel] vous permet de cibler ou de mettre en chaîne l’installation de WebView2 Runtime sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c0acd-120">[Evergreen distribution model][ConceptDistributionEvergreenModel] allows you to target or chain install the WebView2 Runtime onto your user's machine.</span></span>  <span data-ttu-id="c0acd-121">Le programme d’exécution et de programme d’installation de WebView2 a atteint une disponibilité générale (GA).</span><span class="sxs-lookup"><span data-stu-id="c0acd-121">The Evergreen WebView2 Runtime and installer has reached General Availability \(GA\).</span></span>  

## <span data-ttu-id="c0acd-122">Version corrigée</span><span class="sxs-lookup"><span data-stu-id="c0acd-122">Fixed version</span></span>  

<span data-ttu-id="c0acd-123">Le [modèle de distribution de version fixe][ConceptsDistributionFixedVersionModel] vous permet d’empaqueter les fichiers binaires Microsoft Edge dans votre application native.</span><span class="sxs-lookup"><span data-stu-id="c0acd-123">[Fixed version distribution model][ConceptsDistributionFixedVersionModel] allows you to package the Microsoft Edge binaries inside your native application.</span></span>  <span data-ttu-id="c0acd-124">Ce service est actuellement disponible en préversion et destiné à la disponibilité du 4e trimestre 2020.</span><span class="sxs-lookup"><span data-stu-id="c0acd-124">It is currently under preview and targeted to GA Q4 2020.</span></span>  

## <span data-ttu-id="c0acd-125">Disponibilité générale</span><span class="sxs-lookup"><span data-stu-id="c0acd-125">General availability</span></span>  

### <span data-ttu-id="c0acd-126">Win32 C/C++</span><span class="sxs-lookup"><span data-stu-id="c0acd-126">Win32 C/C++</span></span>  

<span data-ttu-id="c0acd-127">Le kit de développement logiciel (SDK) Win32 C/C++ a atteint la disponibilité.</span><span class="sxs-lookup"><span data-stu-id="c0acd-127">The Win32 C/C++ SDK has reached GA.</span></span>  

### <span data-ttu-id="c0acd-128">.NET</span><span class="sxs-lookup"><span data-stu-id="c0acd-128">.NET</span></span>  

<span data-ttu-id="c0acd-129">Le kit de développement logiciel (SDK) .NET englobe le SDK C/C++ Win32.</span><span class="sxs-lookup"><span data-stu-id="c0acd-129">The .NET SDK wraps the Win32 C/C++ SDK.</span></span>  <span data-ttu-id="c0acd-130">Le kit de développement logiciel (SDK) .NET est censé se produire sous la version de Win32 C/C++ GA du 4e trimestre 2020.</span><span class="sxs-lookup"><span data-stu-id="c0acd-130">The .NET SDK is expected to GA shortly after the Win32 C/C++ GA in Q4 2020.</span></span>  

### <span data-ttu-id="c0acd-131">WinUI 3.0</span><span class="sxs-lookup"><span data-stu-id="c0acd-131">WinUI 3.0</span></span>  

<span data-ttu-id="c0acd-132">Vous pouvez accéder à WebView2 dans vos applications UWP à l’aide de [Win interface 3,0][UwpToolkitsWinui3Index], actuellement en alpha.</span><span class="sxs-lookup"><span data-stu-id="c0acd-132">You are able to access WebView2 in your UWP applications using [Win UI 3.0][UwpToolkitsWinui3Index], currently in alpha.</span></span>  <span data-ttu-id="c0acd-133">Pour plus d’informations sur la façon de rester à jour, consultez la documentation de la [bibliothèque d’interface utilisateur Windows][GithubMicrosoftUiXamlRoadmap].</span><span class="sxs-lookup"><span data-stu-id="c0acd-133">For more information about keeping up to date, see [Windows UI Library Roadmap][GithubMicrosoftUiXamlRoadmap].</span></span>  

<!-- links -->  

[ConceptDistributionEvergreenModel]: ./concepts/distribution.md#evergreen-distribution-mode "Modèle de distribution persistant: distribution d’applications à l’aide de WebView2 | Documents Microsoft"  
[ConceptsDistributionFixedVersionModel]: ./concepts/distribution.md#fixed-version-distribution-mode "Modèle de distribution de version fixe: distribution d’applications à l’aide de WebView2 | Documents Microsoft"  

[UwpToolkitsWinui3Index]: /uwp/toolkits/winui3/index "Version d’évaluation de la bibliothèque d’interface utilisateur 3,0 Preview 1 (2020) | Documents Microsoft"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires sur le WebView-MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftUiXamlRoadmap]: https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md "Plan de la bibliothèque d’interface utilisateur Windows-Microsoft/Microsoft-UI-XAML | GitHub"  
