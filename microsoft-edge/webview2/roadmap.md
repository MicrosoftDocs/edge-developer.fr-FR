---
description: En savoir plus sur les étapes suivantes pour WebView2
title: Feuille de route Microsoft Edge WebView 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html
ms.openlocfilehash: 7b67e4a6844ead0f845667a70df8657745ece938
ms.sourcegitcommit: 8f37c931ecde4d58223113f7e3b42d37cc3df97f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/10/2021
ms.locfileid: "11643419"
---
# <a name="microsoft-edge-webview2-roadmap"></a><span data-ttu-id="c5d0d-104">Microsoft Edge Feuille de route WebView2</span><span class="sxs-lookup"><span data-stu-id="c5d0d-104">Microsoft Edge WebView2 roadmap</span></span>  

> [!NOTE]
> <span data-ttu-id="c5d0d-105">Last Updated: July 2021</span><span class="sxs-lookup"><span data-stu-id="c5d0d-105">Last Updated:  July 2021</span></span>  

<span data-ttu-id="c5d0d-106">Le contrôle WebView2 permet aux développeurs d’incorporer des technologies web dans leurs applications natives.</span><span class="sxs-lookup"><span data-stu-id="c5d0d-106">The WebView2 control allows developers to embed web technologies in their native applications.</span></span>  <span data-ttu-id="c5d0d-107">La page suivante décrit la feuille de route prospective pour WebView2.</span><span class="sxs-lookup"><span data-stu-id="c5d0d-107">The following page outlines the prospective roadmap for WebView2.</span></span>  

> [!NOTE]
> <span data-ttu-id="c5d0d-108">WebView2 est en cours de développement actif et la feuille de route continue d’évoluer en fonction des changements de marché et des commentaires des clients. Notez donc que les plans présentés ici ne sont pas exhaustifs et peuvent faire l’objet de modifications.</span><span class="sxs-lookup"><span data-stu-id="c5d0d-108">WebView2 is under active development and the roadmap continues to evolve based on market changes and customer feedback, so please note that the plans outlined here are not exhaustive and are subject to change.</span></span>  

<span data-ttu-id="c5d0d-109">Si vous avez des préoccupations ou des questions sur la feuille de route, faites part de vos commentaires dans le [repo de commentaires.][GithubMicrosoftedgeWebviewfeedbackMain]</span><span class="sxs-lookup"><span data-stu-id="c5d0d-109">If you have concerns or questions about the Roadmap, provide your feedback in the [feedback repo][GithubMicrosoftedgeWebviewfeedbackMain].</span></span>  

<span data-ttu-id="c5d0d-110">L’équipe WebView2 planifie les efforts majeurs suivants pour les futures mises à jour.</span><span class="sxs-lookup"><span data-stu-id="c5d0d-110">The WebView2 team is planning the following major efforts for future updates.</span></span>  

* <span data-ttu-id="c5d0d-111">Aperçu UWP</span><span class="sxs-lookup"><span data-stu-id="c5d0d-111">UWP Preview</span></span>
* <span data-ttu-id="c5d0d-112">Aperçu MacOS</span><span class="sxs-lookup"><span data-stu-id="c5d0d-112">MacOS Preview</span></span>
* <span data-ttu-id="c5d0d-113">Aperçu Xbox</span><span class="sxs-lookup"><span data-stu-id="c5d0d-113">Xbox Preview</span></span>
* <span data-ttu-id="c5d0d-114">HoloLens Aperçu</span><span class="sxs-lookup"><span data-stu-id="c5d0d-114">HoloLens Preview</span></span>

## <a name="webview2-runtime-and-installer"></a><span data-ttu-id="c5d0d-115">Runtime et programme d’installation WebView2</span><span class="sxs-lookup"><span data-stu-id="c5d0d-115">WebView2 Runtime and Installer</span></span>  

<span data-ttu-id="c5d0d-116">[Un modèle de distribution persistant][ConceptDistributionEvergreenModel] vous permet de cibler ou d’installer le runtime WebView2 sur l’ordinateur de votre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c5d0d-116">[Evergreen distribution model][ConceptDistributionEvergreenModel] allows you to target or chain install the WebView2 Runtime onto your user's machine.</span></span>  <span data-ttu-id="c5d0d-117">Le runtime et le programme d’installation WebView2 persistants ont atteint la disponibilité générale \(GA\).</span><span class="sxs-lookup"><span data-stu-id="c5d0d-117">The Evergreen WebView2 Runtime and installer has reached General Availability \(GA\).</span></span>  

## <a name="fixed-version"></a><span data-ttu-id="c5d0d-118">Version fixe</span><span class="sxs-lookup"><span data-stu-id="c5d0d-118">Fixed version</span></span>  

<span data-ttu-id="c5d0d-119">[Le modèle de distribution de version][ConceptsDistributionFixedVersionModel] fixe vous permet de mettre en package les Microsoft Edge binaires à l’intérieur de votre application native.</span><span class="sxs-lookup"><span data-stu-id="c5d0d-119">[Fixed version distribution model][ConceptsDistributionFixedVersionModel] allows you to package the Microsoft Edge binaries inside your native application.</span></span>  <span data-ttu-id="c5d0d-120">La version fixe a atteint la disponibilité générale \(GA\).</span><span class="sxs-lookup"><span data-stu-id="c5d0d-120">The Fixed Version has reached General Availability \(GA\).</span></span>  

## <a name="general-availability"></a><span data-ttu-id="c5d0d-121">Disponibilité générale</span><span class="sxs-lookup"><span data-stu-id="c5d0d-121">General availability</span></span>  

### <a name="win32-cc"></a><span data-ttu-id="c5d0d-122">Win32 C/C++</span><span class="sxs-lookup"><span data-stu-id="c5d0d-122">Win32 C/C++</span></span>  

<span data-ttu-id="c5d0d-123">Le SDK Win32 C/C++ a atteint la ga.</span><span class="sxs-lookup"><span data-stu-id="c5d0d-123">The Win32 C/C++ SDK has reached GA.</span></span>  

### <a name="net"></a><span data-ttu-id="c5d0d-124">.NET</span><span class="sxs-lookup"><span data-stu-id="c5d0d-124">.NET</span></span>  

<span data-ttu-id="c5d0d-125">Le SDK .NET a atteint la ga.</span><span class="sxs-lookup"><span data-stu-id="c5d0d-125">The .NET SDK has reached GA.</span></span> 

### <a name="windows-ui-library-3"></a><span data-ttu-id="c5d0d-126">Windows Bibliothèque d’interface utilisateur 3</span><span class="sxs-lookup"><span data-stu-id="c5d0d-126">Windows UI Library 3</span></span>

<span data-ttu-id="c5d0d-127">Vous pouvez accéder aux contrôles WebView2 dans vos applications en utilisant [Windows UI Library 3 (WinUI3)][UwpToolkitsWinui3Index] avec le SDK Windows App.</span><span class="sxs-lookup"><span data-stu-id="c5d0d-127">You can access WebView2 controls in your applications using [Windows UI Library 3 (WinUI3)][UwpToolkitsWinui3Index] with the Windows App SDK.</span></span> <span data-ttu-id="c5d0d-128">Il est actuellement en prévisualisation.</span><span class="sxs-lookup"><span data-stu-id="c5d0d-128">This is currently in preview.</span></span> <span data-ttu-id="c5d0d-129">Pour plus d’informations, accédez à la [feuille de route Windows SDK de l’application.][WindowsAppSDK|::ref1::|]</span><span class="sxs-lookup"><span data-stu-id="c5d0d-129">For more information, navigate to the [Windows App SDK roadmap][WindowsAppSDK|::ref1::|].</span></span>

 
<!-- links -->  

[WindowsAppSDKRoadmap]: https://github.com/microsoft/WindowsAppSDK/blob/main/docs/roadmap.md "Feuille de route"
[ConceptDistributionEvergreenModel]: ./concepts/distribution.md#evergreen-distribution-mode "Modèle de distribution persistant : distribution d’applications à l’aide de WebView2 | Documents Microsoft"  
[ConceptsDistributionFixedVersionModel]: ./concepts/distribution.md#fixed-version-distribution-mode "Modèle de distribution de version fixe : distribution d’applications à l’aide de WebView2 | Documents Microsoft"  

[UwpToolkitsWinui3Index]: /uwp/toolkits/winui3/index "Windows UI Library 3.0 Preview 1 (mai 2020) | Documents Microsoft"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires WebView - MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftUiXamlRoadmap]: https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md "Windows Feuille de route de la bibliothèque d’interface utilisateur : microsoft/microsoft-ui-xaml | GitHub"  
