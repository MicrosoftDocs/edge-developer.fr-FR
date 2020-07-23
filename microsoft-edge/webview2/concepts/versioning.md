---
description: Modèles de contrôle de version utilisés pour Microsoft Edge WebView2
title: Version de Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/22/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: acf3103f39d33586ee0614aeb0f10de0ab71c89a
ms.sourcegitcommit: b3555043e9d5aefa5a9e36ba4d73934d41559f49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/23/2020
ms.locfileid: "10894311"
---
# <span data-ttu-id="c4a75-104">Comprendre les versions de kit de développement logiciel WebView2</span><span class="sxs-lookup"><span data-stu-id="c4a75-104">Understand WebView2 SDK versions</span></span>  

<span data-ttu-id="c4a75-105">WebView2 dépend de Microsoft Edge pour fonctionner.</span><span class="sxs-lookup"><span data-stu-id="c4a75-105">WebView2 depends on Microsoft Edge to function.</span></span>  <span data-ttu-id="c4a75-106">Chaque SDK WebView2 nécessite qu’une version de navigateur minimum soit installée.</span><span class="sxs-lookup"><span data-stu-id="c4a75-106">Each WebView2 SDK requires that a minimum browser version is installed.</span></span>  <span data-ttu-id="c4a75-107">La version minimale est répercutée dans la version du package du SDK.</span><span class="sxs-lookup"><span data-stu-id="c4a75-107">The minimum version is reflected in the package version of the SDK.</span></span>  <span data-ttu-id="c4a75-108">Par exemple, si vous utilisez la `SDK package version 0.9.488` , vous devez installer Microsoft Edge avec le numéro de build 488 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="c4a75-108">For example, if you use the `SDK package version 0.9.488`, then you must install Microsoft Edge with a build number of 488 or later.</span></span>  <span data-ttu-id="c4a75-109">La version du navigateur est également spécifiée dans les [notes de publication][Releasenotes]de WebView2.</span><span class="sxs-lookup"><span data-stu-id="c4a75-109">The browser version is also specified in the WebView2 [Release Notes][Releasenotes].</span></span>  <span data-ttu-id="c4a75-110">Pour plus d’informations sur les dernières versions du navigateur, voir [canaux de navigateur][DeployedgeChannels].</span><span class="sxs-lookup"><span data-stu-id="c4a75-110">For more information on the latest releases of the browser, see [Browser Channels][DeployedgeChannels].</span></span>  

> [!NOTE]
> <span data-ttu-id="c4a75-111">WebView2 est actuellement en version preview.</span><span class="sxs-lookup"><span data-stu-id="c4a75-111">WebView2 is currently in preview.</span></span>  <span data-ttu-id="c4a75-112">Même si l’équipe WebView s’efforce de garantir la compatibilité descendante entre les versions de navigateur et les kits de développement logiciel (SDK), il n’est pas garanti que les versions plus récentes du navigateur ne prennent pas en charge les versions antérieures du SDK.</span><span class="sxs-lookup"><span data-stu-id="c4a75-112">While the WebView team strives to ensure backward compatibility between browser versions and SDKs, it is not guaranteed because newer versions of the browser may not support previous SDK versions.</span></span>  <span data-ttu-id="c4a75-113">S’il existe des modifications apportées entre les versions de navigateur et les kits de développement logiciel (SDK), nous indiquons les changements dans les [notes de publication][Releasenotes].</span><span class="sxs-lookup"><span data-stu-id="c4a75-113">If there are breaking changes between browser versions and SDKs, we specify the changes in the [Release Notes][Releasenotes].</span></span>  

<span data-ttu-id="c4a75-114">À l’avenir, nous prévoyons de changer le modèle de distribution pour les applications WebView2.</span><span class="sxs-lookup"><span data-stu-id="c4a75-114">In the future, we plan to change the distribution model for WebView2 applications.</span></span>  <span data-ttu-id="c4a75-115">Pour plus d’informations, reportez-vous à la section [mode de distribution persistant][DistributionEvergreenMode].</span><span class="sxs-lookup"><span data-stu-id="c4a75-115">For more information, see [Evergreen distribution mode][DistributionEvergreenMode].</span></span>  
 
## <span data-ttu-id="c4a75-116">Package de publication et version préliminaire</span><span class="sxs-lookup"><span data-stu-id="c4a75-116">Release and pre-release package</span></span>  

<span data-ttu-id="c4a75-117">Dans Preview, le package de publication contient les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="c4a75-117">In preview, the release package contains the following.</span></span>  

*   <span data-ttu-id="c4a75-118">[API C/C++ Win32][ReferenceWin3209538]: les API du SDK qui doivent rester identiques à la disponibilité.</span><span class="sxs-lookup"><span data-stu-id="c4a75-118">[Win32 C/C++ APIs][ReferenceWin3209538]: APIs in the SDK that are expected to remain the same at GA.</span></span>  

<span data-ttu-id="c4a75-119">Dans Preview, la version préliminaire du package contient les composants suivants.</span><span class="sxs-lookup"><span data-stu-id="c4a75-119">In preview, the pre-release package contains the following components.</span></span>  

*   <span data-ttu-id="c4a75-120">API .NET: [WPF][ReferenceWpf09515], [WinForms][ReferenceWinforms09515]et [Core][ReferenceDotnet09538]</span><span class="sxs-lookup"><span data-stu-id="c4a75-120">.NET APIs: [WPF][ReferenceWpf09515], [WinForms][ReferenceWinforms09515], and [Core][ReferenceDotnet09538]</span></span>  
*   <span data-ttu-id="c4a75-121">API expérimentales.</span><span class="sxs-lookup"><span data-stu-id="c4a75-121">Experimental APIs.</span></span>  <span data-ttu-id="c4a75-122">Pour plus d’informations, consultez la section [API expérimentales](#experimental-apis) .</span><span class="sxs-lookup"><span data-stu-id="c4a75-122">For more information, see the [Experimental APIs](#experimental-apis) section.</span></span>  

## <span data-ttu-id="c4a75-123">API expérimentales</span><span class="sxs-lookup"><span data-stu-id="c4a75-123">Experimental APIs</span></span>  

<span data-ttu-id="c4a75-124">Nous testons des API d’expérimentation qui peuvent représenter de nouvelles fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="c4a75-124">We are testing experimental APIs that may represent future functionality.</span></span>  <span data-ttu-id="c4a75-125">Les API expérimentales sont marquées comme `experimental` dans le kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="c4a75-125">The experimental APIs are marked as `experimental` in the SDK.</span></span>  <span data-ttu-id="c4a75-126">Les API expérimentales pourront être fournies sous la forme d’API entièrement stables dans le package de publication.</span><span class="sxs-lookup"><span data-stu-id="c4a75-126">Experimental APIs may ship as fully stable APIs in the release package.</span></span>  <span data-ttu-id="c4a75-127">Vous devez vous attendre à ce que toutes les API expérimentales soient modifiées avant leur publication.</span><span class="sxs-lookup"><span data-stu-id="c4a75-127">You should expect all experimental APIs to change before release.</span></span>  <span data-ttu-id="c4a75-128">Évaluez les API expérimentales et partagez des commentaires à l’aide de la [référentiel samples de commentaires WebView][GithubMicrosoftedgeWebviewfeedback].</span><span class="sxs-lookup"><span data-stu-id="c4a75-128">Please evaluate the Experimental APIs and share feedback using the [WebView feedback repo][GithubMicrosoftedgeWebviewfeedback].</span></span>   

> [!CAUTION]
> <span data-ttu-id="c4a75-129">Évitez d’utiliser les API expérimentales dans les applications de production.</span><span class="sxs-lookup"><span data-stu-id="c4a75-129">Avoid using the experimental APIs in production applications.</span></span>  

## <span data-ttu-id="c4a75-130">Feuille de route</span><span class="sxs-lookup"><span data-stu-id="c4a75-130">Roadmap</span></span>  

<span data-ttu-id="c4a75-131">Lorsque WebView2 atteint un état disponible général stable, le package de publication contient toutes les API Win32 C/C++ et .NET stables et prises en charge.</span><span class="sxs-lookup"><span data-stu-id="c4a75-131">After WebView2 reaches a stable general available state, the release package contains all of the stable, supported Win32 C/C++ and .NET APIs.</span></span>  <span data-ttu-id="c4a75-132">Le package de la version préliminaire contient des API expérimentales susceptibles d’être modifiées en fonction des commentaires du développeur et des informations partagées.</span><span class="sxs-lookup"><span data-stu-id="c4a75-132">The pre-release package contains experimental APIs that are subject to change based upon developer feedback and shared insights.</span></span>  

<!--## Versioning  

After you have used a particular version of the SDK to build your app, your app may end up running with an older or newer version of installed browser binaries.  Until version 1.0.0.0 of WebView2 there may be breaking changes during updates that prevent your SDK from working with different versions of installed browser binaries.  After version 1.0.0.0, different versions of the SDK may work with different versions of the installed browser by using the following best practices.  

1.  To account for breaking changes to the API be sure to check for failure when requesting the DLL export `CreateCoreWebView2Environment` and when running `QueryInterface` on any `CoreWebView2` object.  A return value of `E_NOINTERFACE` indicates that the SDK is not compatible with the Microsoft Edge browser binaries.  
1.  Checking for failure from `QueryInterface` also accounts for cases where the SDK is newer than the version of the Microsoft Edge browser and your app attempts to use an interface of which the Microsoft Edge browser is unaware.  

1.  When an interface is unavailable, you may consider disabling the associated feature if possible, or otherwise informing your users to update their browsers.  -->  

<!--links -->

[DistributionEvergreenMode]: ./distribution.md#evergreen-distribution-mode "Mode de distribution persistant: distribution d’applications à l’aide de WebView2 | Documents Microsoft"  
[ReferenceDotnet09538]: ../reference/dotnet/0-9-538-reference-webview2.md "Référence (WebView2) | Documents Microsoft"  
[ReferenceWinforms09515]: ../reference/winforms/0-9-515-reference-webview2.md "Référence (WebView2) | Documents Microsoft"  
[ReferenceWin3209538]: ../reference/win32/0-9-538-reference-webview2.md "Référence (WebView2) | Documents Microsoft"  
[ReferenceWpf09515]: ../reference/wpf/0-9-515-reference-webview2.md "Référence (WebView2) | Documents Microsoft"  
[Releasenotes]: ../releasenotes.md "Notes de publication pour WebView2 SDK | Documents Microsoft"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Vue d’ensemble des canaux Microsoft Edge | Documents Microsoft"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires sur le WebView-MicrosoftEdge/WebViewFeedback | GitHub"  
