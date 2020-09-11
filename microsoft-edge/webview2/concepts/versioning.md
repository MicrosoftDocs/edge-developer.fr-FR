---
description: Modèles de contrôle de version utilisés pour Microsoft Edge WebView2
title: Version de Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 3ce1f0653a14d92571f1365cbfebc8bb2215ecbe
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010676"
---
# <span data-ttu-id="5e3af-104">Comprendre les versions de kit de développement logiciel WebView2</span><span class="sxs-lookup"><span data-stu-id="5e3af-104">Understand WebView2 SDK versions</span></span>  

<span data-ttu-id="5e3af-105">WebView2 dépend de Microsoft Edge pour fonctionner.</span><span class="sxs-lookup"><span data-stu-id="5e3af-105">WebView2 depends on Microsoft Edge to function.</span></span>  <span data-ttu-id="5e3af-106">Chaque SDK WebView2 nécessite qu’une version de navigateur minimum soit installée.</span><span class="sxs-lookup"><span data-stu-id="5e3af-106">Each WebView2 SDK requires that a minimum browser version is installed.</span></span>  <span data-ttu-id="5e3af-107">La version minimale est répercutée dans la version du package du SDK.</span><span class="sxs-lookup"><span data-stu-id="5e3af-107">The minimum version is reflected in the package version of the SDK.</span></span>  <span data-ttu-id="5e3af-108">Par exemple, si vous utilisez la `SDK package version 0.9.488` , vous devez installer Microsoft Edge avec le numéro de build 488 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="5e3af-108">For example, if you use the `SDK package version 0.9.488`, then you must install Microsoft Edge with a build number of 488 or later.</span></span>  <span data-ttu-id="5e3af-109">La version du navigateur est également spécifiée dans les [notes de publication][Releasenotes]de WebView2.</span><span class="sxs-lookup"><span data-stu-id="5e3af-109">The browser version is also specified in the WebView2 [Release Notes][Releasenotes].</span></span>  <span data-ttu-id="5e3af-110">Pour plus d’informations sur la dernière version du navigateur Microsoft Edge, voir [canaux du navigateur][DeployedgeChannels].</span><span class="sxs-lookup"><span data-stu-id="5e3af-110">For more information about the latest release of the Microsoft Edge browser, navigate to [Browser Channels][DeployedgeChannels].</span></span>  

> [!NOTE]
> <span data-ttu-id="5e3af-111">WebView2 est actuellement en version preview.</span><span class="sxs-lookup"><span data-stu-id="5e3af-111">WebView2 is currently in preview.</span></span>  <span data-ttu-id="5e3af-112">Même si l’équipe WebView s’efforce de garantir la compatibilité descendante entre les versions de navigateur et les kits de développement logiciel (SDK), il n’est pas garanti que les versions plus récentes du navigateur ne prennent pas en charge les versions antérieures du SDK.</span><span class="sxs-lookup"><span data-stu-id="5e3af-112">While the WebView team strives to ensure backward compatibility between browser versions and SDKs, it is not guaranteed because newer versions of the browser may not support previous SDK versions.</span></span>  <span data-ttu-id="5e3af-113">Si des modifications sont apportées entre les versions de navigateur et les kits de développement logiciel (SDK), les modifications sont indiquées dans les [notes de publication][Releasenotes].</span><span class="sxs-lookup"><span data-stu-id="5e3af-113">If there are breaking changes between browser versions and SDKs, the changes are specified in the [Release Notes][Releasenotes].</span></span>  

<span data-ttu-id="5e3af-114">À l’avenir, l’équipe WebView planifie le changement du modèle de distribution pour les applications WebView2.</span><span class="sxs-lookup"><span data-stu-id="5e3af-114">In the future, the WebView team plans to change the distribution model for WebView2 apps.</span></span>  <span data-ttu-id="5e3af-115">Pour plus d’informations, accédez au [mode de distribution persistant][DistributionEvergreenMode].</span><span class="sxs-lookup"><span data-stu-id="5e3af-115">For more information, navigate to [Evergreen distribution mode][DistributionEvergreenMode].</span></span>  

## <span data-ttu-id="5e3af-116">Package de mise à jour et version préliminaire</span><span class="sxs-lookup"><span data-stu-id="5e3af-116">Release and prerelease package</span></span>  

<span data-ttu-id="5e3af-117">Dans Preview, le package de publication contient les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="5e3af-117">In preview, the release package contains the following.</span></span>  

*   <span data-ttu-id="5e3af-118">[API C/C++ Win32][ReferenceWin3209622]: les API du SDK qui doivent rester identiques à la disponibilité.</span><span class="sxs-lookup"><span data-stu-id="5e3af-118">[Win32 C/C++ APIs][ReferenceWin3209622]: APIs in the SDK that are expected to remain the same at GA.</span></span>  

<span data-ttu-id="5e3af-119">Dans Preview, le package de mise à jour contient les composants suivants.</span><span class="sxs-lookup"><span data-stu-id="5e3af-119">In preview, the prerelease package contains the following components.</span></span>  

*   <span data-ttu-id="5e3af-120">API .NET: [WPF][ReferenceWpf09515], [WinForms][ReferenceWinforms09515]et [Core][ReferenceDotnet09628]</span><span class="sxs-lookup"><span data-stu-id="5e3af-120">.NET APIs: [WPF][ReferenceWpf09515], [WinForms][ReferenceWinforms09515], and [Core][ReferenceDotnet09628]</span></span>  
*   <span data-ttu-id="5e3af-121">API expérimentales.</span><span class="sxs-lookup"><span data-stu-id="5e3af-121">Experimental APIs.</span></span>  <span data-ttu-id="5e3af-122">Pour plus d’informations, consultez la section [API expérimentales](#experimental-apis) .</span><span class="sxs-lookup"><span data-stu-id="5e3af-122">For more information, see the [Experimental APIs](#experimental-apis) section.</span></span>  

## <span data-ttu-id="5e3af-123">API expérimentales</span><span class="sxs-lookup"><span data-stu-id="5e3af-123">Experimental APIs</span></span>  

<span data-ttu-id="5e3af-124">L’équipe WebView teste les API expérimentales qui pourraient représenter de nouvelles fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="5e3af-124">The WebView team is testing experimental APIs that may represent future functionality.</span></span>  <span data-ttu-id="5e3af-125">Les API expérimentales sont marquées comme `experimental` dans le kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="5e3af-125">The experimental APIs are marked as `experimental` in the SDK.</span></span>  <span data-ttu-id="5e3af-126">Les API expérimentales pourront être fournies sous la forme d’API entièrement stables dans le package de publication.</span><span class="sxs-lookup"><span data-stu-id="5e3af-126">Experimental APIs may ship as fully stable APIs in the release package.</span></span>  <span data-ttu-id="5e3af-127">Vous devez vous attendre à ce que toutes les API expérimentales soient modifiées avant leur publication.</span><span class="sxs-lookup"><span data-stu-id="5e3af-127">You should expect all experimental APIs to change before release.</span></span>  <span data-ttu-id="5e3af-128">Évaluez les API expérimentales et partagez des commentaires à l’aide de la [référentiel samples de commentaires WebView][GithubMicrosoftedgeWebviewfeedback].</span><span class="sxs-lookup"><span data-stu-id="5e3af-128">Please evaluate the Experimental APIs and share feedback using the [WebView feedback repo][GithubMicrosoftedgeWebviewfeedback].</span></span>  

> [!CAUTION]
> <span data-ttu-id="5e3af-129">Évitez d’utiliser les API expérimentales dans les applications de production.</span><span class="sxs-lookup"><span data-stu-id="5e3af-129">Avoid using the experimental APIs in production apps.</span></span>  

## <span data-ttu-id="5e3af-130">Correspondance des versions du runtime WebView2</span><span class="sxs-lookup"><span data-stu-id="5e3af-130">Matching WebView2 Runtime versions</span></span>  

<span data-ttu-id="5e3af-131">Lors de l’écriture d’une application WebView2 à l’aide d’une version de kit de développement logiciel (SDK) spécifique, les utilisateurs de votre application peuvent l’exécuter avec différentes versions compatibles du runtime WebView2.</span><span class="sxs-lookup"><span data-stu-id="5e3af-131">When writing a WebView2 app using a particular SDK version, the users fo you app may run your it with various compatible versions of the WebView2 Runtime.</span></span>  <span data-ttu-id="5e3af-132">À l’avenir, une nouvelle version du runtime WebView2 compatible plus récente contient toutes les API non expérimentales d’une ancienne version du runtime WebView2 compatible, ainsi que d’autres API non expérimentales.</span><span class="sxs-lookup"><span data-stu-id="5e3af-132">In the future, a newer compatible WebView2 Runtime version contains all the non-experimental APIs from an older compatible WebView2 Runtime version plus additional new non-experimental APIs.</span></span>  

*   <span data-ttu-id="5e3af-133">Les développeurs en **C/C++ Win32** , lors de l’utilisation `QueryInterface` pour obtenir une nouvelle interface, doivent vérifier la valeur de retour `E_NOINTERFACE` , qui peut indiquer que le runtime WebView2 est antérieur et ne prend pas en charge cette interface particulière.</span><span class="sxs-lookup"><span data-stu-id="5e3af-133">**Win32 C/C++** developers, when using `QueryInterface` to obtain a new interface, should check for a return value of `E_NOINTERFACE`, which may indicate that the WebView2 Runtime is older and does not support that particular interface.</span></span>  
*   <span data-ttu-id="5e3af-134">Les développeurs **.net et WinUI** doivent vérifier une `No such interface supported` exception lors de l’utilisation des méthodes, des propriétés et des événements ajoutés dans les SDK ultérieurs, qui peuvent se produire lorsque le runtime WebView2 est antérieur et ne prend pas en charge ces API spécifiques.</span><span class="sxs-lookup"><span data-stu-id="5e3af-134">**.NET and WinUI** developers should check for a `No such interface supported` exception when using methods, properties, and events added in later SDKs which may occur when the WebView2 Runtime is older and does not support those particular APIs.</span></span>  

<span data-ttu-id="5e3af-135">Si une API n’est pas disponible, envisagez de désactiver la fonctionnalité associée, le cas échéant, ou d’informer l’utilisateur final qu’il doit mettre à jour sa version d’exécution WebView2.</span><span class="sxs-lookup"><span data-stu-id="5e3af-135">If an API is unavailable, consider disabling the associated feature, if possible, or otherwise informing the end user they need to update their WebView2 Runtime version.</span></span>  

<span data-ttu-id="5e3af-136">Il est possible de présenter, de modifier et de supprimer des API expérimentales du SDK au kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="5e3af-136">Experimental APIs may be introduced, modified, and removed from SDK to SDK.</span></span>  <span data-ttu-id="5e3af-137">Lorsque vous tentez d’utiliser une API expérimentale qui n’est pas disponible dans le runtime WebView2, vous pouvez observer le même comportement décrit précédemment.</span><span class="sxs-lookup"><span data-stu-id="5e3af-137">When attempting to use an experimental API that is not available in the WebView2 Runtime you may observe the same previously described behavior.</span></span>  

## <span data-ttu-id="5e3af-138">Feuille de route</span><span class="sxs-lookup"><span data-stu-id="5e3af-138">Roadmap</span></span>  

<span data-ttu-id="5e3af-139">Lorsque WebView2 atteint un état disponible général stable, le package de publication contient toutes les API Win32 C/C++ et .NET stables et prises en charge.</span><span class="sxs-lookup"><span data-stu-id="5e3af-139">After WebView2 reaches a stable general available state, the release package contains all of the stable, supported Win32 C/C++ and .NET APIs.</span></span>  <span data-ttu-id="5e3af-140">Le package de mise à jour contient des API expérimentales susceptibles d’être modifiées en fonction de vos commentaires et de vos informations de partage.</span><span class="sxs-lookup"><span data-stu-id="5e3af-140">The prerelease package contains experimental APIs that are subject to change based upon your feedback and shared insights.</span></span>  

<!--## Versioning  

After you have used a particular version of the SDK to build your app, your app may end up running with an older or newer version of installed browser binaries.  Until version 1.0.0.0 of WebView2 there may be breaking changes during updates that prevent your SDK from working with different versions of installed browser binaries.  After version 1.0.0.0, different versions of the SDK may work with different versions of the installed browser by using the following best practices.  

1.  To account for breaking changes to the API be sure to check for failure when requesting the DLL export `CreateCoreWebView2Environment` and when running `QueryInterface` on any `CoreWebView2` object.  A return value of `E_NOINTERFACE` indicates that the SDK is not compatible with the Microsoft Edge browser binaries.  
1.  Checking for failure from `QueryInterface` also accounts for cases where the SDK is newer than the version of the Microsoft Edge browser and your app attempts to use an interface of which the Microsoft Edge browser is unaware.  

1.  When an interface is unavailable, you may consider disabling the associated feature if possible, or otherwise informing your users to update their browsers.  -->  

<!--links -->

[DistributionEvergreenMode]: ./distribution.md#evergreen-distribution-mode "Mode de distribution persistant: distribution d’applications à l’aide de WebView2 | Documents Microsoft"  
[ReferenceDotnet09628]: ../reference/dotnet/0-9-628-reference-webview2.md "Référence (WebView2) | Documents Microsoft"  
[ReferenceWinforms09515]: ../reference/winforms/0-9-515-reference-webview2.md "Référence (WebView2) | Documents Microsoft"  
[ReferenceWin3209622]: ../reference/win32/0-9-622-reference-webview2.md "Référence (WebView2) | Documents Microsoft"  
[ReferenceWpf09515]: ../reference/wpf/0-9-515-reference-webview2.md "Référence (WebView2) | Documents Microsoft"  
[Releasenotes]: ../releasenotes.md "Notes de publication pour WebView2 SDK | Documents Microsoft"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Vue d’ensemble des canaux Microsoft Edge | Documents Microsoft"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires sur le WebView-MicrosoftEdge/WebViewFeedback | GitHub"  
