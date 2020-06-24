---
description: Modèles de contrôle de version utilisés pour Microsoft Edge WebView2
title: Version de Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/22/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 3862576134d1179fb24b2ce865f705b2bf1db8a6
ms.sourcegitcommit: de171a8e7ccd9f23846f3cd06519e4a0104f1c52
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/23/2020
ms.locfileid: "10757605"
---
# <span data-ttu-id="2a49b-104">Comprendre les versions de kit de développement logiciel WebView2</span><span class="sxs-lookup"><span data-stu-id="2a49b-104">Understand WebView2 SDK versions</span></span>  

<span data-ttu-id="2a49b-105">WebView2 dépend de Microsoft Edge pour fonctionner.</span><span class="sxs-lookup"><span data-stu-id="2a49b-105">WebView2 depends on Microsoft Edge to function.</span></span> <span data-ttu-id="2a49b-106">Chaque SDK WebView2 nécessite qu’une version de navigateur minimum soit installée.</span><span class="sxs-lookup"><span data-stu-id="2a49b-106">Each WebView2 SDK requires that a minimum browser version is installed.</span></span>  <span data-ttu-id="2a49b-107">La version minimale est répercutée dans la version du package du SDK.</span><span class="sxs-lookup"><span data-stu-id="2a49b-107">The minimum version is reflected in the package version of the SDK.</span></span>  <span data-ttu-id="2a49b-108">Par exemple, si vous utilisez la `SDK package version 0.9.488` , vous devez installer Microsoft Edge avec le numéro de build 488 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="2a49b-108">For example, if you use the `SDK package version 0.9.488`, then you must install Microsoft Edge with a build number of 488 or later.</span></span> <span data-ttu-id="2a49b-109">La version du navigateur est également spécifiée dans les [notes de publication][Webview2Releasenotes]de WebView2.</span><span class="sxs-lookup"><span data-stu-id="2a49b-109">The browser version is also specified in the WebView2 [Release Notes][Webview2Releasenotes].</span></span>  <span data-ttu-id="2a49b-110">Pour plus d’informations sur les dernières versions du navigateur, voir [canaux de navigateur][DeployedgeChannels].</span><span class="sxs-lookup"><span data-stu-id="2a49b-110">For more information on the latest releases of the browser, see [Browser Channels][DeployedgeChannels].</span></span>  

> [!NOTE]
> <span data-ttu-id="2a49b-111">WebView2 est actuellement en version preview.</span><span class="sxs-lookup"><span data-stu-id="2a49b-111">WebView2 is currently in preview.</span></span>  <span data-ttu-id="2a49b-112">Même si l’équipe WebView de Microsoft Edge s’efforce de garantir la compatibilité descendante entre les versions de navigateur et les SDK, il n’est pas garanti que certaines versions plus récentes du navigateur ne prennent pas en charge les versions antérieures du SDK.</span><span class="sxs-lookup"><span data-stu-id="2a49b-112">While, the Microsoft Edge WebView team strives to ensure backward compatibility between browser versions and SDKs, it is not guaranteed as some newer versions of the browser may not support older SDK versions.</span></span>  <span data-ttu-id="2a49b-113">Si des modifications sont apportées entre les versions de navigateur et les kits de développement logiciel (SDK), l’équipe WebView Microsoft Edge spécifie les modifications apportées aux [notes de publication][Webview2Releasenotes].</span><span class="sxs-lookup"><span data-stu-id="2a49b-113">If there are breaking changes between browser versions and SDKs, the Microsoft Edge WebView team specifies the changes in the [release notes][Webview2Releasenotes].</span></span>  

<span data-ttu-id="2a49b-114">À l’avenir, le modèle de distribution pour les applications WebView2 changera.</span><span class="sxs-lookup"><span data-stu-id="2a49b-114">In the future, the distribution model for WebView2 applications will change.</span></span> <span data-ttu-id="2a49b-115">Pour plus d’informations, consultez [WebView2 Runtime][Webview2IndexEdgeRuntime].</span><span class="sxs-lookup"><span data-stu-id="2a49b-115">For more information, see [WebView2 Runtime][Webview2IndexEdgeRuntime].</span></span>  
 
## <span data-ttu-id="2a49b-116">Package de publication et version préliminaire</span><span class="sxs-lookup"><span data-stu-id="2a49b-116">Release and pre-release package</span></span>  

<span data-ttu-id="2a49b-117">Dans Preview, le package de publication contient les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="2a49b-117">In preview, the release package contains the following.</span></span>  

*   <span data-ttu-id="2a49b-118">[API C/C++ Win32][Webview2ReferenceWin3209538]: les API du SDK qui doivent rester identiques à la disponibilité.</span><span class="sxs-lookup"><span data-stu-id="2a49b-118">[Win32 C/C++ APIs][Webview2ReferenceWin3209538]: APIs in the SDK that are expected to remain the same at GA.</span></span> 

<span data-ttu-id="2a49b-119">Dans Preview, le package de la version préliminaire contient les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="2a49b-119">In preview, the pre-release package contains the following.</span></span>  

*   <span data-ttu-id="2a49b-120">API .NET: [WPF][Webview2ReferenceWpf09515], [WinForms][Webview2ReferenceWinforms09515]et [Core][Webview2ReferenceDotnet09538]</span><span class="sxs-lookup"><span data-stu-id="2a49b-120">.NET APIs: [WPF][Webview2ReferenceWpf09515], [WinForms][Webview2ReferenceWinforms09515], and [Core][Webview2ReferenceDotnet09538]</span></span>
*   <span data-ttu-id="2a49b-121">API expérimentales.</span><span class="sxs-lookup"><span data-stu-id="2a49b-121">Experimental APIs.</span></span>  <span data-ttu-id="2a49b-122">Pour plus d’informations, consultez la section [API Experimantal](#experimental-apis) .</span><span class="sxs-lookup"><span data-stu-id="2a49b-122">For more information, see the [Experimantal APIs](#experimental-apis) section.</span></span>  

### <span data-ttu-id="2a49b-123">API expérimentales</span><span class="sxs-lookup"><span data-stu-id="2a49b-123">Experimental APIs</span></span>  

<span data-ttu-id="2a49b-124">L’équipe WebView teste des API qui représentent de nouvelles fonctionnalités intitulées API expérimentales.</span><span class="sxs-lookup"><span data-stu-id="2a49b-124">The WebView Team is testing APIs that represent future functionality named Experimental APIs.</span></span>  <span data-ttu-id="2a49b-125">Les API expérimentales sont marquées comme `experimental` dans le kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="2a49b-125">The Experimental APIs are marked as `experimental` in the SDK.</span></span>  <span data-ttu-id="2a49b-126">Certaines API expérimentales pourront être fournies sous la forme d’API entièrement stables dans le package de publication.</span><span class="sxs-lookup"><span data-stu-id="2a49b-126">Some Experimental APIs may ship as fully stable APIs in the release package.</span></span>  <span data-ttu-id="2a49b-127">Vous devez vous attendre à ce que toutes les API expérimentales soient modifiées avant leur publication.</span><span class="sxs-lookup"><span data-stu-id="2a49b-127">You should expect all experimental APIs to change before release.</span></span>  <span data-ttu-id="2a49b-128">Évaluez les API expérimentales et partagez des commentaires à l’aide de la [référentiel samples de commentaires WebView][GithubMicrosoftedgeWebviewfeedback].</span><span class="sxs-lookup"><span data-stu-id="2a49b-128">Please evaluate the Experimental APIs and share feedback using the [WebView feedback repo][GithubMicrosoftedgeWebviewfeedback].</span></span>   

> [!CAUTION]
> <span data-ttu-id="2a49b-129">Évitez d’utiliser les API expérimentales dans les applications de production.</span><span class="sxs-lookup"><span data-stu-id="2a49b-129">Avoid using the experimental APIs in production applications.</span></span>  

### <span data-ttu-id="2a49b-130">Feuille de route</span><span class="sxs-lookup"><span data-stu-id="2a49b-130">Roadmap</span></span>  

<span data-ttu-id="2a49b-131">Lorsque WebView2 atteint un état disponible général stable, le package de publication contient toutes les API Win32 C/C++ et .NET stables et prises en charge.</span><span class="sxs-lookup"><span data-stu-id="2a49b-131">After WebView2 reaches a stable general available state, the release package contains all of the stable, supported Win32 C/C++ and .NET APIs.</span></span>  <span data-ttu-id="2a49b-132">Le package de la version préliminaire contient des API expérimentales susceptibles d’être modifiées en fonction des commentaires du développeur et des informations partagées.</span><span class="sxs-lookup"><span data-stu-id="2a49b-132">The pre-release package contains experimental APIs that are subject to change based upon developer feedback and shared insights.</span></span>  

<!--links -->

[Webview2IndexEdgeRuntime]: ./distribution.md#microsoft-edge-webview2-runtime "Microsoft Edge WebView2-distribution d’applications à l’aide de WebView2 | Documents Microsoft"  
[Webview2ReferenceDotnet09538]: ../reference/dotnet/0-9-538-reference-webview2.md "Référence (WebView2) | Documents Microsoft"  
[Webview2ReferenceWinforms09515]: ../reference/winforms/0-9-515-reference-webview2.md "Référence (WebView2) | Documents Microsoft"  
[Webview2ReferenceWin3209538]: ../reference/win32/0-9-538-reference-webview2.md "Référence (WebView2) | Documents Microsoft"  
[Webview2ReferenceWpf09515]: ../reference/wpf/0-9-515-reference-webview2.md "Référence (WebView2) | Documents Microsoft"  
[Webview2Releasenotes]: ../releasenotes.md "Notes de publication pour WebView2 SDK | Documents Microsoft"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Vue d’ensemble des canaux Microsoft Edge | Documents Microsoft"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires sur le WebView-MicrosoftEdge/WebViewFeedback | GitHub"  
