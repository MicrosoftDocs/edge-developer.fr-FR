---
description: Modèles de contrôle de version utilisés pour Microsoft Edge WebView2
title: Version de Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/18/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 8463ce403af069cf25dbf7b08bb49d44c1e54501
ms.sourcegitcommit: f1aa8925f7985a2bbfd951f188a8c19c97e4ff6f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/18/2020
ms.locfileid: "10659566"
---
# <span data-ttu-id="574af-104">Présentation des versions de navigateur et de WebView2</span><span class="sxs-lookup"><span data-stu-id="574af-104">Understanding browser versions and WebView2</span></span>  

<span data-ttu-id="574af-105">WebView2 dépend de Microsoft Edge pour fonctionner.</span><span class="sxs-lookup"><span data-stu-id="574af-105">WebView2 depends on Microsoft Edge to function.</span></span>  <span data-ttu-id="574af-106">Chaque SDK WebView2 nécessite qu’une version de navigateur minimum soit installée.</span><span class="sxs-lookup"><span data-stu-id="574af-106">Each WebView2 SDK requires that a minimum browser version is installed.</span></span>  <span data-ttu-id="574af-107">Cette version de navigateur est spécifiée dans nos [notes de publication][Webview2Releasenotes].</span><span class="sxs-lookup"><span data-stu-id="574af-107">This browser version is specified in our [Release Notes][Webview2Releasenotes].</span></span>  <span data-ttu-id="574af-108">La version minimale est susceptible de apparaître dans la version de package du SDK.</span><span class="sxs-lookup"><span data-stu-id="574af-108">You may see the minimum version reflected in the package version of the SDK.</span></span>  <span data-ttu-id="574af-109">Par exemple, si vous utilisez la `SDK package version 0.9.488` , vous devez installer Microsoft Edge avec le numéro de build 488 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="574af-109">For example, if you use the `SDK package version 0.9.488`, then you must install Microsoft Edge with a build number of 488 or later.</span></span>  <span data-ttu-id="574af-110">Pour plus d’informations sur les dernières versions du navigateur, voir [canaux de navigateur][DeployedgeChannels].</span><span class="sxs-lookup"><span data-stu-id="574af-110">For more information on the latest releases of the browser, see [Browser Channels][DeployedgeChannels].</span></span>  

> [!NOTE]
> <span data-ttu-id="574af-111">WebView2 est actuellement en version preview.</span><span class="sxs-lookup"><span data-stu-id="574af-111">WebView2 is currently in Preview.</span></span>  <span data-ttu-id="574af-112">Même si l’équipe WebView de Microsoft Edge s’efforce de garantir la compatibilité descendante entre les versions de navigateur et les SDK, il n’est pas garanti que certaines versions plus récentes du navigateur ne prennent pas en charge les versions antérieures du SDK.</span><span class="sxs-lookup"><span data-stu-id="574af-112">While, the Microsoft Edge WebView team strives to ensure backward compatibility between browser versions and SDKs, it is not guaranteed as some newer versions of the browser may not support older SDK versions.</span></span>  <span data-ttu-id="574af-113">Si des modifications sont apportées [entre les versions][Webview2Releasenotes]de navigateur et les kits de développement logiciel (SDK) Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="574af-113">If there are breaking changes between browser versions and SDKs, the Microsoft Edge WebView team indicates the changes in the [release notes][Webview2Releasenotes].</span></span>  

<span data-ttu-id="574af-114">À l’avenir, l’équipe WebView Microsoft Edge doit changer le modèle de distribution.</span><span class="sxs-lookup"><span data-stu-id="574af-114">In the future, the Microsoft Edge WebView team plans to change the distribution model.</span></span>  <span data-ttu-id="574af-115">Les plans d’équipe de l’équipe Web Microsoft Edge pour supprimer la dépendance directe sur le navigateur Microsoft Edge à partir de WebView2.</span><span class="sxs-lookup"><span data-stu-id="574af-115">The Microsoft Edge WebView team plans to remove the direct dependency on the Microsoft Edge browser from WebView2.</span></span>  <!--To learn more, see [WebView2 Runtime][Webview2IndexEdgeRuntime] in the [Distribution][Webview2Distibution] section.  -->  

<!--todo: dd link to distribution.md after publication  -->  

## <span data-ttu-id="574af-116">API expérimentales</span><span class="sxs-lookup"><span data-stu-id="574af-116">Experimental APIs</span></span>  

<span data-ttu-id="574af-117">Si WebView2 est une version d’évaluation, les API du SDK sont censées rester les mêmes au niveau GA.</span><span class="sxs-lookup"><span data-stu-id="574af-117">While WebView2 is a preview, the APIs in the SDK are expected to remain the same at GA.</span></span>  <span data-ttu-id="574af-118">Il existe des [API expérimentales][Webview2ReferenceWin3209488Experimental] incluses dans le kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="574af-118">There are [experimental APIs][Webview2ReferenceWin3209488Experimental] included in the SDK.</span></span>  <span data-ttu-id="574af-119">Évaluez les API expérimentales et envoyez vos commentaires à l’aide de l' [référentiel samples de commentaires WebView][GithubMicrosoftedgeWebviewfeedback].</span><span class="sxs-lookup"><span data-stu-id="574af-119">Please evaluate the experimental APIs and send your feedback using the [WebView feedback repo][GithubMicrosoftedgeWebviewfeedback].</span></span>  

### <span data-ttu-id="574af-120">Feuille de route</span><span class="sxs-lookup"><span data-stu-id="574af-120">Roadmap</span></span>  

<span data-ttu-id="574af-121">Une fois que WebView2 atteint un état disponible général stable et que nous publions le kit de développement logiciel (SDK) 1.0.0, l’équipe WebView Microsoft Edge doit déplacer toutes les API expérimentales vers un package de version préliminaire.</span><span class="sxs-lookup"><span data-stu-id="574af-121">After WebView2 reaches a stable general available state and we release the 1.0.0 SDK, the Microsoft Edge WebView team plans to move all experimental APIs to a pre-release package.</span></span>  <span data-ttu-id="574af-122">La version préliminaire du package continue d’accepter les commentaires et de vous familiariser avec les fonctionnalités les plus récentes, tandis que la version stable conserve la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="574af-122">The pre-release package continues to allow for feedback and insight into the latest features, while the stable release version maintains backward compatibility.</span></span>  

<!--links -->

[Webview2Distibution]: ./distribution.md "n’existe pas | Documents Microsoft"  
[Webview2IndexEdgeRuntime]: ../index.md#microsoft-edge-webview2-runtime "Microsoft Edge WebView2 Runtime-Microsoft Edge WebView2 (version préliminaire du développeur) | Documents Microsoft"  
[Webview2ReferenceWin3209488Experimental]: ../reference/win32/0-9-488-reference-webview2.md#experimental "Expérimentation-référence (WebView2) | Documents Microsoft"  
[Webview2Releasenotes]: ../releasenotes.md "Notes de publication pour WebView2 SDK | Documents Microsoft"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Vue d’ensemble des canaux Microsoft Edge | Documents Microsoft"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires sur le WebView-MicrosoftEdge/WebViewFeedback | GitHub"  
