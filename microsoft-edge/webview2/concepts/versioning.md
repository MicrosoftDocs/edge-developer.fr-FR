---
description: Modèles de contrôle de version utilisés pour Microsoft Edge WebView2
title: Version de Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: a47c7295e87cf4295f8cdf898b62aa3b550aa9a5
ms.sourcegitcommit: af91bfc3e6d8afc51f0fbbc0fe392262f424225c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/19/2020
ms.locfileid: "11120338"
---
# <span data-ttu-id="1f1ca-104">Comprendre les versions de kit de développement logiciel WebView2</span><span class="sxs-lookup"><span data-stu-id="1f1ca-104">Understand WebView2 SDK versions</span></span>  

<span data-ttu-id="1f1ca-105">Pour développer une application WebView2, vous devez installer le [Runtime WebView2][MicrosoftDeveloperEdgeWebview2] ou un [canal Microsoft Edge non stable][MicrosoftedgeinsiderDownload].</span><span class="sxs-lookup"><span data-stu-id="1f1ca-105">To develop a WebView2 application, you must install either the [WebView2 Runtime][MicrosoftDeveloperEdgeWebview2] or a [non-stable Microsoft Edge channel][MicrosoftedgeinsiderDownload].</span></span>  <span data-ttu-id="1f1ca-106">La version minimale requise est incluse dans la version du package NuGet du SDK.</span><span class="sxs-lookup"><span data-stu-id="1f1ca-106">The minimum version that's required is included in the NuGet package version of the SDK.</span></span>  <span data-ttu-id="1f1ca-107">Par exemple, si vous utilisez la `SDK package version 0.9.488` , vous devez installer le [Runtime WebView2][MicrosoftDeveloperEdgeWebview2] ou un [canal Microsoft Edge non stable][MicrosoftedgeinsiderDownload] avec un numéro de version 488 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="1f1ca-107">For example, if you use the `SDK package version 0.9.488`, then you must install either the [WebView2 Runtime][MicrosoftDeveloperEdgeWebview2] or a [non-stable Microsoft Edge channel][MicrosoftedgeinsiderDownload] with a build number of 488 or later.</span></span>  <span data-ttu-id="1f1ca-108">La version minimale requise est également spécifiée dans les [notes de publication][Releasenotes]de WebView2.</span><span class="sxs-lookup"><span data-stu-id="1f1ca-108">The minimum version required is also specified in the WebView2 [Release Notes][Releasenotes].</span></span>  <span data-ttu-id="1f1ca-109">Les nouvelles versions du kit de développement logiciel (SDK) WebView2 sont fournies à la même cadence générale que le navigateur Microsoft Edge \ (chrome \), qui est approximativement toutes les six semaines.</span><span class="sxs-lookup"><span data-stu-id="1f1ca-109">New versions of the WebView2 SDK are shipped at the same general cadence as the Microsoft Edge \(Chromium\) browser, which is approximately every six weeks.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="1f1ca-110">Lorsque vous développez des applications WebView2 persistantes, testez régulièrement votre application par rapport aux dernières versions des navigateurs Microsoft Edge WebView2 Runtime et non stables.</span><span class="sxs-lookup"><span data-stu-id="1f1ca-110">When developing Evergreen WebView2 applications, regularly test your application against the latest versions of the WebView2 Runtime and non-stable Microsoft Edge browsers.</span></span>  <span data-ttu-id="1f1ca-111">Dans la mesure où la plateforme Web est en perpétuelle évolution, il est préférable de procéder au test régulier pour vous assurer que votre application s’exécute comme prévu.</span><span class="sxs-lookup"><span data-stu-id="1f1ca-111">Because the web platform is constantly evolving, regular testing is the best way to ensure your application performs as intended.</span></span>  

## <span data-ttu-id="1f1ca-112">Package de mise à jour et version préliminaire</span><span class="sxs-lookup"><span data-stu-id="1f1ca-112">Release and prerelease package</span></span>  

<span data-ttu-id="1f1ca-113">Le package NuGet WebView2 contient à la fois une version de package et une version préliminaire.</span><span class="sxs-lookup"><span data-stu-id="1f1ca-113">The WebView2 NuGet package contains both a release and pre-release package.</span></span>  

<span data-ttu-id="1f1ca-114">Le package de publication est en transfert compatible et contient les [API C/C++ Win32][ReferenceWin32].</span><span class="sxs-lookup"><span data-stu-id="1f1ca-114">The release package is forward compatible and contains the [Win32 C/C++ APIs][ReferenceWin32].</span></span>  <span data-ttu-id="1f1ca-115">Les API dans ce SDK sont entièrement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="1f1ca-115">APIs in this SDK are fully supported.</span></span>  

<span data-ttu-id="1f1ca-116">Le package de mise à jour est un sur-ensemble du package de publication avec les composants supplémentaires indiqués ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="1f1ca-116">The prerelease package is a superset of the release package with the additional components listed below.</span></span>  

*   <span data-ttu-id="1f1ca-117">API .NET: [WPF][DotnetMicrosoftWebWebview2WpfNamespace], [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace]et [Core][DotnetMicrosoftWebWebview2CoreNamespace]</span><span class="sxs-lookup"><span data-stu-id="1f1ca-117">.NET APIs: [WPF][DotnetMicrosoftWebWebview2WpfNamespace], [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace], and [Core][DotnetMicrosoftWebWebview2CoreNamespace]</span></span>  
*   <span data-ttu-id="1f1ca-118">API expérimentales: pour plus d’informations, accédez à la section [API expérimentales](#experimental-apis) .</span><span class="sxs-lookup"><span data-stu-id="1f1ca-118">Experimental APIs:  For more information, navigate to the [Experimental APIs](#experimental-apis) section.</span></span>  

## <span data-ttu-id="1f1ca-119">API expérimentales</span><span class="sxs-lookup"><span data-stu-id="1f1ca-119">Experimental APIs</span></span>  

<span data-ttu-id="1f1ca-120">L’équipe WebView teste les API d’expérimentation qui pourront être incluses dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="1f1ca-120">The WebView team is testing experimental APIs that may be included in future releases.</span></span>  <span data-ttu-id="1f1ca-121">Les API expérimentales sont marquées comme `experimental` dans le kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="1f1ca-121">The experimental APIs are marked as `experimental` in the SDK.</span></span>  <span data-ttu-id="1f1ca-122">Les API expérimentales pourront être fournies sous la forme d’API entièrement stables dans le package de publication.</span><span class="sxs-lookup"><span data-stu-id="1f1ca-122">Experimental APIs may ship as fully stable APIs in the release package.</span></span>  <span data-ttu-id="1f1ca-123">Vous pouvez évaluer les API expérimentales et partager des commentaires à l’aide de l' [référentiel samples de commentaires WebView][GithubMicrosoftedgeWebviewfeedback].</span><span class="sxs-lookup"><span data-stu-id="1f1ca-123">You can evaluate the Experimental APIs and share feedback using the [WebView feedback repo][GithubMicrosoftedgeWebviewfeedback].</span></span>  

> [!CAUTION]
> <span data-ttu-id="1f1ca-124">Évitez d’utiliser les API expérimentales dans les applications de production.</span><span class="sxs-lookup"><span data-stu-id="1f1ca-124">Avoid using the experimental APIs in production apps.</span></span>  

## <span data-ttu-id="1f1ca-125">Correspondance des versions du runtime WebView2</span><span class="sxs-lookup"><span data-stu-id="1f1ca-125">Matching WebView2 Runtime versions</span></span>  

<span data-ttu-id="1f1ca-126">Lors de l’écriture d’une application WebView2 à l’aide d’une version de kit de développement logiciel (SDK) spécifique, les utilisateurs de votre application peuvent l’exécuter avec plusieurs versions compatibles du runtime WebView2.</span><span class="sxs-lookup"><span data-stu-id="1f1ca-126">When writing a WebView2 app using a particular SDK version, users of your app may run it with several compatible versions of the WebView2 Runtime.</span></span>  <span data-ttu-id="1f1ca-127">L’équipe WebView travaille sur une version d’WebView2 Runtime compatible qui contient des API non expérimentales des versions précédentes du runtime et des nouvelles API non expérimentales.</span><span class="sxs-lookup"><span data-stu-id="1f1ca-127">The WebView team is working on a compatible WebView2 Runtime version that contains non-experimental APIs from previous versions of the Runtime and new non-experimental APIs.</span></span>  

<span data-ttu-id="1f1ca-128">En fonction du SDK que vous utilisez, prenez en compte les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="1f1ca-128">Depending on which SDK you use, consider the following items:</span></span> 

*   <span data-ttu-id="1f1ca-129">**Win32 C/C++**.</span><span class="sxs-lookup"><span data-stu-id="1f1ca-129">**Win32 C/C++**.</span></span>  <span data-ttu-id="1f1ca-130">Lors de l’utilisation `QueryInterface` pour obtenir une nouvelle interface, recherchez une valeur de retour de `E_NOINTERFACE` .</span><span class="sxs-lookup"><span data-stu-id="1f1ca-130">When using `QueryInterface` to obtain a new interface, check for a return value of `E_NOINTERFACE`.</span></span>  <span data-ttu-id="1f1ca-131">Cette valeur peut indiquer que le runtime WebView2 est une version antérieure et ne prend pas en charge cette interface.</span><span class="sxs-lookup"><span data-stu-id="1f1ca-131">This value may indicate that the WebView2 Runtime is a previous version, and doesn't support that interface.</span></span>  
*   <span data-ttu-id="1f1ca-132">**.Net et WinUI**.</span><span class="sxs-lookup"><span data-stu-id="1f1ca-132">**.NET and WinUI**.</span></span>  <span data-ttu-id="1f1ca-133">Recherchez une `No such interface supported` exception lors de l’utilisation des méthodes, propriétés et événements qui ont été ajoutés aux SDK plus récents.</span><span class="sxs-lookup"><span data-stu-id="1f1ca-133">Check for a `No such interface supported` exception when using methods, properties, and events that were added to more recent SDKs.</span></span>  <span data-ttu-id="1f1ca-134">Cette exception peut se produire lorsque le runtime WebView2 est une version antérieure et ne prend pas en charge ces API.</span><span class="sxs-lookup"><span data-stu-id="1f1ca-134">This exception may occur when the WebView2 Runtime is a previous version, and doesn't support those APIs.</span></span>  

<span data-ttu-id="1f1ca-135">Si une API n’est pas disponible, envisagez de supprimer la fonctionnalité associée ou Informez vos utilisateurs qu’ils ont besoin de mettre à jour leur version de WebView2 Runtime.</span><span class="sxs-lookup"><span data-stu-id="1f1ca-135">If an API is unavailable, consider removing the associated feature, or inform your users that they need to update their version of the WebView2 Runtime.</span></span>  

<span data-ttu-id="1f1ca-136">Il est possible de présenter, de modifier et de supprimer des API expérimentales du SDK au kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="1f1ca-136">Experimental APIs may be introduced, modified, and removed from SDK to SDK.</span></span>  <span data-ttu-id="1f1ca-137">Les API expérimentales peuvent ne pas être disponibles dans votre version installée de WebView2 Runtime.</span><span class="sxs-lookup"><span data-stu-id="1f1ca-137">Experimental APIs may not be available in your installed version of the WebView2 Runtime.</span></span>  

## <span data-ttu-id="1f1ca-138">Feuille de route</span><span class="sxs-lookup"><span data-stu-id="1f1ca-138">Roadmap</span></span>  

<span data-ttu-id="1f1ca-139">Le package de publication contient toutes les API Win32 C/C++ stables et prises en charge.</span><span class="sxs-lookup"><span data-stu-id="1f1ca-139">The release package contains all of the stable, supported Win32 C/C++ APIs.</span></span>  <span data-ttu-id="1f1ca-140">À l’avenir, le package de publication contient toutes les API .NET stables et prises en charge lorsqu’elles sont disponibles en général.</span><span class="sxs-lookup"><span data-stu-id="1f1ca-140">In the future, the release package will contain all stable, supported .NET APIs when they are made generally available.</span></span>  <span data-ttu-id="1f1ca-141">Le package de mise à jour contient des API expérimentales susceptibles d’être modifiées en fonction de vos commentaires et de vos informations de partage.</span><span class="sxs-lookup"><span data-stu-id="1f1ca-141">The prerelease package contains experimental APIs that are subject to change based upon your feedback and shared insights.</span></span>  

<!--## Versioning  

After you have used a particular version of the SDK to build your app, your app may end up running with an older or newer version of installed browser binaries.  Until version 1.0.0.0 of WebView2 there may be breaking changes during updates that prevent your SDK from working with different versions of installed browser binaries.  After version 1.0.0.0, different versions of the SDK may work with different versions of the installed browser by using the following best practices.  

1.  To account for breaking changes to the API be sure to check for failure when requesting the DLL export `CreateCoreWebView2Environment` and when running `QueryInterface` on any `CoreWebView2` object.  A return value of `E_NOINTERFACE` indicates that the SDK is not compatible with the Microsoft Edge browser binaries.  
1.  Checking for failure from `QueryInterface` also accounts for cases where the SDK is newer than the version of the Microsoft Edge browser and your app attempts to use an interface of which the Microsoft Edge browser is unaware.  

1.  When an interface is unavailable, you may consider disabling the associated feature if possible, or otherwise informing your users to update their browsers.  -->  

<!--links -->  

[Releasenotes]: ../releasenotes.md "Notes de publication pour WebView2 SDK | Documents Microsoft"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Vue d’ensemble des canaux Microsoft Edge | Documents Microsoft"  

[DotnetMicrosoftWebWebview2CoreNamespace]: /dotnet/api/microsoft.web.webview2.core "Espace de noms Microsoft. Web. WebView2. Core | Documents Microsoft"  
[DotnetMicrosoftWebWebview2WpfNamespace]: /dotnet/api/microsoft.web.webview2.wpf "Espace de noms Microsoft. Web. WebView2. WPF | Documents Microsoft"  
[DotnetMicrosoftWebWebview2WinformsNamespace]: /dotnet/api/microsoft.web.webview2.winforms "Espace de noms Microsoft. Web. WebView2. WinForms | Documents Microsoft"  
[ReferenceWin32]: /microsoft-edge/webview2/reference/win32 "Référence C++ Win32 WebView2 | Documents Microsoft"  

[MicrosoftDeveloperEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2/ "Microsoft Edge WebView2 | Développeur Microsoft"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires sur le WebView-MicrosoftEdge/WebViewFeedback | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Télécharger les canaux Microsoft Edge Insider"  
