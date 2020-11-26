---
description: Modèles de contrôle de version utilisés pour Microsoft Edge WebView2
title: Version de Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/25/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 54d62de00a89a3c433fd77e9ec20945adbfc19c3
ms.sourcegitcommit: 2e14ff82350f700d7eabc8d33b3ec3e5fc8c61fa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "11191609"
---
# <span data-ttu-id="c8057-104">Comprendre les versions de kit de développement logiciel WebView2</span><span class="sxs-lookup"><span data-stu-id="c8057-104">Understand WebView2 SDK versions</span></span>  

<span data-ttu-id="c8057-105">Les nouvelles versions du kit de développement logiciel (SDK) WebView2 sont fournies à la même cadence générale que le navigateur Microsoft Edge \ (chrome \), qui est approximativement toutes les six semaines.</span><span class="sxs-lookup"><span data-stu-id="c8057-105">New versions of the WebView2 SDK are shipped at the same general cadence as the Microsoft Edge \(Chromium\) browser, which is approximately every six weeks.</span></span>  

## <span data-ttu-id="c8057-106">Package de mise à jour et version préliminaire</span><span class="sxs-lookup"><span data-stu-id="c8057-106">Release and prerelease package</span></span>  

<span data-ttu-id="c8057-107">Le package NuGet WebView2 contient à la fois une version de package et une version préliminaire.</span><span class="sxs-lookup"><span data-stu-id="c8057-107">The WebView2 NuGet package contains both a release and pre-release package.</span></span>  

<span data-ttu-id="c8057-108">Le **package de publication** est en transfert compatible et contient les composants suivants.</span><span class="sxs-lookup"><span data-stu-id="c8057-108">The **release package** is forward compatible and contains the following components.</span></span>  

*   [<span data-ttu-id="c8057-109">API C/C++ Win32</span><span class="sxs-lookup"><span data-stu-id="c8057-109">Win32 C/C++ APIs</span></span>][ReferenceWin32]
*   <span data-ttu-id="c8057-110">API .NET:  [WPF][DotnetMicrosoftWebWebview2WpfNamespace], [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace]et [Core][DotnetMicrosoftWebWebview2CoreNamespace].</span><span class="sxs-lookup"><span data-stu-id="c8057-110">.NET APIs:  [WPF][DotnetMicrosoftWebWebview2WpfNamespace], [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace], and [Core][DotnetMicrosoftWebWebview2CoreNamespace].</span></span>  
    
<span data-ttu-id="c8057-111">Les API du SDK sont entièrement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="c8057-111">APIs in the SDK are fully supported.</span></span>  

<span data-ttu-id="c8057-112">Le **package** de mise à jour est un sur-ensemble du package de publication doté d' [API expérimentales](#experimental-apis).</span><span class="sxs-lookup"><span data-stu-id="c8057-112">The **prerelease package** is a superset of the release package with [Experimental APIs](#experimental-apis).</span></span>  

### <span data-ttu-id="c8057-113">Feuille de route</span><span class="sxs-lookup"><span data-stu-id="c8057-113">Roadmap</span></span>  

<span data-ttu-id="c8057-114">Le package de publication contient toutes les API Win32 C/C++ et .NET stables et prises en charge.</span><span class="sxs-lookup"><span data-stu-id="c8057-114">The release package contains all of the stable, supported Win32 C/C++ and .NET APIs.</span></span>  <span data-ttu-id="c8057-115">Le package de mise à jour contient des API expérimentales susceptibles d’être modifiées en fonction de vos commentaires.</span><span class="sxs-lookup"><span data-stu-id="c8057-115">The prerelease package contains experimental APIs that are subject to change based on your feedback.</span></span>  

## <span data-ttu-id="c8057-116">API expérimentales</span><span class="sxs-lookup"><span data-stu-id="c8057-116">Experimental APIs</span></span>  

<span data-ttu-id="c8057-117">L’équipe WebView cherche des commentaires sur les API expérimentales qui pourront être incluses dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="c8057-117">The WebView team is seeking feedback on experimental APIs that may be included in future releases.</span></span>  <span data-ttu-id="c8057-118">Les API expérimentales sont marquées comme `experimental` dans le kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="c8057-118">The experimental APIs are marked as `experimental` in the SDK.</span></span>  <span data-ttu-id="c8057-119">Pour vous aider à évaluer les API expérimentales et à partager vos commentaires, accédez au [référentiel samples de commentaires WebView][GithubMicrosoftedgeWebviewfeedback].</span><span class="sxs-lookup"><span data-stu-id="c8057-119">To help you evaluate the Experimental APIs and share your feedback, navigate to the [WebView feedback repo][GithubMicrosoftedgeWebviewfeedback].</span></span>  

> [!CAUTION]
> <span data-ttu-id="c8057-120">Il est possible de présenter, de modifier et de supprimer des API expérimentales du SDK au kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="c8057-120">Experimental APIs may be introduced, modified, and removed from SDK to SDK.</span></span>  <span data-ttu-id="c8057-121">Évitez d’utiliser les API expérimentales dans les applications de production.</span><span class="sxs-lookup"><span data-stu-id="c8057-121">Avoid using the experimental APIs in production apps.</span></span>  

> [!NOTE]
> <span data-ttu-id="c8057-122">Les API expérimentales peuvent ne pas être disponibles dans votre version installée de WebView2 Runtime.</span><span class="sxs-lookup"><span data-stu-id="c8057-122">Experimental APIs may not be available in your installed version of the WebView2 Runtime.</span></span>  

## <span data-ttu-id="c8057-123">Correspondance des versions du runtime WebView2</span><span class="sxs-lookup"><span data-stu-id="c8057-123">Matching WebView2 Runtime versions</span></span>  
<span data-ttu-id="c8057-124">Les applications WebView2 requièrent que les utilisateurs installent un [WebView2 Runtime][MicrosoftDeveloperEdgeWebview2].</span><span class="sxs-lookup"><span data-stu-id="c8057-124">WebView2 apps require users to install a [WebView2 Runtime][MicrosoftDeveloperEdgeWebview2].</span></span>  <span data-ttu-id="c8057-125">L’exécution de WebView2 est automatiquement mise à jour vers la dernière version disponible.</span><span class="sxs-lookup"><span data-stu-id="c8057-125">The WebView2 Runtime automatically updates to the latest version available.</span></span>  <span data-ttu-id="c8057-126">Dans certains cas, il est possible que les utilisateurs puissent arrêter les mises à jour automatiques d’WebView2 Runtime, ce qui risque de provoquer des problèmes de compatibilité avec les applications.</span><span class="sxs-lookup"><span data-stu-id="c8057-126">In some scenarios, users may want to stop automatic WebView2 Runtime updates, which may cause app compatibility issues.</span></span>  

<span data-ttu-id="c8057-127">Si les mises à jour de l’application WebView2 sont arrêtées, vérifiez que vous comprenez la version minimale du [Runtime WebView2][MicrosoftDeveloperEdgeWebview2] requis par votre application.</span><span class="sxs-lookup"><span data-stu-id="c8057-127">If WebView2 Runtime updates are stopped, ensure you understand the minimum version of the [WebView2 Runtime][MicrosoftDeveloperEdgeWebview2] required by your app.</span></span>  <span data-ttu-id="c8057-128">Prenez en compte les deux éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="c8057-128">Consider the following two items:</span></span>  

1.  <span data-ttu-id="c8057-129">La version minimale requise du kit de développement logiciel (SDK), dans les [notes de publication][Webview2Releasenotes] de WebView2, sous **version d’WebView2 Runtime minimum**.</span><span class="sxs-lookup"><span data-stu-id="c8057-129">The minimum required version of the SDK, in found in the WebView2 [Release Notes][Webview2Releasenotes] under **minimum WebView2 Runtime version**.</span></span>  <span data-ttu-id="c8057-130">Par exemple, pour la version SDK version [1.0.622.22][Webview2Releasenotes1062222], vous devez installer le [WebView2 Runtime][MicrosoftDeveloperEdgeWebview2] ou un [canal Microsoft Edge non stable][MicrosoftedgeinsiderDownload] dont le numéro de version est `86.0.616.0` ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="c8057-130">For example, for SDK version [1.0.622.22][Webview2Releasenotes1062222], you must install either the [WebView2 Runtime][MicrosoftDeveloperEdgeWebview2] or a [non-stable Microsoft Edge channel][MicrosoftedgeinsiderDownload] with a build number of `86.0.616.0` or later.</span></span>  <span data-ttu-id="c8057-131">La version minimale requise par le SDK est modifiée uniquement en cas de changement de rupture dans la plateforme Web.</span><span class="sxs-lookup"><span data-stu-id="c8057-131">The minimum version required by the SDK only changes when a breaking change occurs in the web platform.</span></span>  
1.  <span data-ttu-id="c8057-132">La version minimale requise du package NuGet requis pour prendre en charge les interfaces et les API que vous utilisez dans votre application.</span><span class="sxs-lookup"><span data-stu-id="c8057-132">The minimum required version of the NuGet package required to support the interfaces and APIs that you use in your app.</span></span>  <span data-ttu-id="c8057-133">Les nouvelles interfaces et API sont ajoutées périodiquement à WebView2.</span><span class="sxs-lookup"><span data-stu-id="c8057-133">New interfaces and APIs are added periodically to WebView2.</span></span>  <span data-ttu-id="c8057-134">Les API et interfaces intégrées dans un kit de développement logiciel (SDK) nécessitent différentes versions du runtime WebView2, car les API et l’interface sont ajoutées au kit de développement logiciel à différents moments.</span><span class="sxs-lookup"><span data-stu-id="c8057-134">APIs and interfaces bundled in an SDK require different versions of the WebView2 Runtime, because APIs and interface are added to the SDK at different times.</span></span>  <span data-ttu-id="c8057-135">La version du runtime WebView2 requise correspond au numéro de la build, le troisième numéro, de la version du SDK dans laquelle l’API a été introduite pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="c8057-135">The required WebView2 Runtime version matches the build number, the third number, of the SDK version the API was first introduced in.</span></span>  <span data-ttu-id="c8057-136">Par exemple, une nouvelle API ou interface ajoutée dans SDK version [1.0.622.22][Webview2Releasenotes1062222] nécessite la version du runtime WebView2:  `86.0.622.0`  une API ou une interface ajoutée à une version ultérieure du SDK nécessite le runtime WebView2 portant le même numéro de version que le kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="c8057-136">For example, a new API or interface added in SDK version [1.0.622.22][Webview2Releasenotes1062222] requires the WebView2 Runtime version:  `86.0.622.0`  An API or interface added in a later SDK release requires the WebView2 Runtime that has the same version number as the SDK.</span></span>  <span data-ttu-id="c8057-137">Pour vous aider à déterminer si la version Runtime WebView2 prend en charge une interface ou une API, naviguez pour [déterminer la configuration requise pour le runtime WebView2](#determine-webview2-runtime-requirement).</span><span class="sxs-lookup"><span data-stu-id="c8057-137">To help you determine if the WebView2 Runtime version supports an interface or API, navigate to [Determine WebView2 Runtime requirement](#determine-webview2-runtime-requirement).</span></span>  
    
> [!IMPORTANT]
> <span data-ttu-id="c8057-138">Lorsque vous développez des [applications WebView2 persistantes][Webview2ConceptsDistributionEvergreenDistributionMode], testez régulièrement votre application par rapport aux dernières versions des navigateurs Microsoft Edge WebView2 Runtime et non stables.</span><span class="sxs-lookup"><span data-stu-id="c8057-138">When developing [Evergreen WebView2 apps][Webview2ConceptsDistributionEvergreenDistributionMode], regularly test your app against the latest versions of the WebView2 Runtime and non-stable Microsoft Edge browsers.</span></span>  <span data-ttu-id="c8057-139">Dans la mesure où la plateforme Web est en perpétuelle évolution, il est préférable de procéder au test régulier pour vous assurer que votre application fonctionne comme prévu.</span><span class="sxs-lookup"><span data-stu-id="c8057-139">Because the web platform is constantly evolving, regular testing is the best way to ensure your app performs as intended.</span></span>  

### <span data-ttu-id="c8057-140">Déterminer la configuration requise pour WebView2 Runtime</span><span class="sxs-lookup"><span data-stu-id="c8057-140">Determine WebView2 Runtime requirement</span></span>  

<span data-ttu-id="c8057-141">En fonction du SDK que vous utilisez, prenez en compte les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="c8057-141">Depending on which SDK you use, consider the following items:</span></span>  

*   <span data-ttu-id="c8057-142">**Win32 C/C++**.</span><span class="sxs-lookup"><span data-stu-id="c8057-142">**Win32 C/C++**.</span></span>  <span data-ttu-id="c8057-143">Lors de l’utilisation `QueryInterface` pour obtenir une nouvelle interface, vérifiez la valeur de retour de `E_NOINTERFACE` .</span><span class="sxs-lookup"><span data-stu-id="c8057-143">When using `QueryInterface` to obtain a new interface, verify a return value of `E_NOINTERFACE`.</span></span>  <span data-ttu-id="c8057-144">La valeur peut indiquer que le runtime WebView2 est une version antérieure et ne prend pas en charge cette interface.</span><span class="sxs-lookup"><span data-stu-id="c8057-144">The value may indicate that the WebView2 Runtime is a previous version, and doesn't support that interface.</span></span>  <span data-ttu-id="c8057-145">Pour obtenir un exemple de fonctionnement, accédez à la [ligne 622-AppWindow. cpp][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisampleAppwindowCppL622].</span><span class="sxs-lookup"><span data-stu-id="c8057-145">For an example of how it works, navigate to [Line 622 - AppWindow.cpp][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisampleAppwindowCppL622].</span></span>  
*   <span data-ttu-id="c8057-146">**.Net et WinUI**.</span><span class="sxs-lookup"><span data-stu-id="c8057-146">**.NET and WinUI**.</span></span>  <span data-ttu-id="c8057-147">Recherchez une `No such interface supported` exception lors de l’utilisation des méthodes, propriétés et événements qui ont été ajoutés aux SDK plus récents.</span><span class="sxs-lookup"><span data-stu-id="c8057-147">Check for a `No such interface supported` exception when using methods, properties, and events that were added to more recent SDKs.</span></span>  <span data-ttu-id="c8057-148">L’exception peut se produire lorsque le runtime WebView2 est une version antérieure et ne prend pas en charge les API.</span><span class="sxs-lookup"><span data-stu-id="c8057-148">The exception may occur when the WebView2 Runtime is a previous version, and does not support the APIs.</span></span>  
    
<span data-ttu-id="c8057-149">Si une API n’est pas disponible, envisagez de supprimer la fonctionnalité associée ou Informez vos utilisateurs qu’une mise à jour du runtime WebView2 est requise.</span><span class="sxs-lookup"><span data-stu-id="c8057-149">If an API is unavailable, consider removing the associated feature, or inform your users that an update to the WebView2 Runtime is required.</span></span>  

<!--
## Versioning  

After you have used a particular version of the SDK to build your app, your app may end up running with an older or newer version of installed browser binaries.  Until version 1.0.0.0 of WebView2 there may be breaking changes during updates that prevent your SDK from working with different versions of installed browser binaries.  After version 1.0.0.0, different versions of the SDK may work with different versions of the installed browser by using the following best practices.  

1.  To account for breaking changes to the API be sure to check for failure when requesting the DLL export `CreateCoreWebView2Environment` and when running `QueryInterface` on any `CoreWebView2` object.  A return value of `E_NOINTERFACE` indicates that the SDK is not compatible with the Microsoft Edge browser binaries.  
1.  Checking for failure from `QueryInterface` also accounts for cases where the SDK is newer than the version of the Microsoft Edge browser and your app attempts to use an interface of which the Microsoft Edge browser is unaware.  
1.  When an interface is unavailable, you may consider disabling the associated feature if possible, or otherwise informing your users to update their browsers.  
    -->  

<!--links -->  

[Webview2ConceptsDistributionEvergreenDistributionMode]: ./distribution.md#evergreen-distribution-mode "Mode de distribution persistant: distribution d’applications à l’aide de WebView2 | Documents Microsoft"  
[Webview2Releasenotes]: ../releasenotes.md "Notes de publication pour WebView2 SDK | Documents Microsoft"  
[Webview2Releasenotes1062222]: ../releasenotes.md#1062222 "1.0.622.22-notes de publication pour WebView2 SDK | Documents Microsoft"   

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Vue d’ensemble des canaux Microsoft Edge | Documents Microsoft"  

[DotnetMicrosoftWebWebview2CoreNamespace]: /dotnet/api/microsoft.web.webview2.core "Espace de noms Microsoft. Web. WebView2. Core | Documents Microsoft"  
[DotnetMicrosoftWebWebview2WpfNamespace]: /dotnet/api/microsoft.web.webview2.wpf "Espace de noms Microsoft. Web. WebView2. WPF | Documents Microsoft"  
[DotnetMicrosoftWebWebview2WinformsNamespace]: /dotnet/api/microsoft.web.webview2.winforms "Espace de noms Microsoft. Web. WebView2. WinForms | Documents Microsoft"  
[ReferenceWin32]: /microsoft-edge/webview2/reference/win32 "Référence C++ Win32 WebView2 | Documents Microsoft"  

[MicrosoftDeveloperEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2/ "Microsoft Edge WebView2 | Développeur Microsoft"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires sur le WebView-MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisampleAppwindowCppL622]: https://github.com/MicrosoftEdge/WebView2Samples/blob/8ec7de9d3e80a942bc7025cffad98eee75e11e64/SampleApps/WebView2APISample/AppWindow.cpp#L622 "Ligne 622-AppWindow. cpp-MicrosoftEdge/WebView2Samples | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Télécharger les canaux Microsoft Edge Insider"  
