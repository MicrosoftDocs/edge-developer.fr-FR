---
description: Modèle de processus
title: Modèle de | WebView 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, applications wpf, wpf, edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, edge html
ms.openlocfilehash: 95d0c53219114c47a781317ab4b2ee2028fc586f
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535614"
---
# <a name="process-model"></a><span data-ttu-id="38429-104">Modèle de processus</span><span class="sxs-lookup"><span data-stu-id="38429-104">Process model</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="38429-105">Plateformes pris en charge :</span><span class="sxs-lookup"><span data-stu-id="38429-105">Supported platforms:</span></span>
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="38429-106">Win32, Windows Forms, WinUi, WPF</span><span class="sxs-lookup"><span data-stu-id="38429-106">Win32, Windows Forms, WinUi, WPF</span></span>
   :::column-end:::
:::row-end:::  

<span data-ttu-id="38429-107">WebView2 utilise le même modèle de processus que le navigateur Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="38429-107">WebView2 uses the same process model as the Microsoft Edge browser.</span></span>  <span data-ttu-id="38429-108">Pour plus d’informations sur le modèle de processus de navigateur, accédez à Architecture du navigateur - À l’intérieur, regardez [le navigateur web moderne.][GoogleDeveloperWebUpdates201809InsideBrowserPart1BrowserArchitecture]</span><span class="sxs-lookup"><span data-stu-id="38429-108">For more information about the browser process model, navigate to [Browser Architecture - Inside look at modern web browser][GoogleDeveloperWebUpdates201809InsideBrowserPart1BrowserArchitecture].</span></span>  

<span data-ttu-id="38429-109">Un processus de navigateur est associé aux processus de rendu et à d’autres processus utilitaires, comme décrit dans cet article.</span><span class="sxs-lookup"><span data-stu-id="38429-109">One browser process is associated with the renderer processes and other utility processes as described in that article.</span></span>  <span data-ttu-id="38429-110">En outre, si WebView2 est spécifié, les processus de demande de l’application hôte utilisent WebView2.</span><span class="sxs-lookup"><span data-stu-id="38429-110">Additionally, if WebView2 is specified, the host app requesting processes use WebView2.</span></span>  

:::image type="complex" source="../media/process-model-1.png" alt-text="Processus 1" lightbox="../media/process-model-1.png":::
   <span data-ttu-id="38429-112">Processus 1</span><span class="sxs-lookup"><span data-stu-id="38429-112">Process 1</span></span>  
:::image-end:::    

<span data-ttu-id="38429-113">Un processus de navigateur est associé à un seul dossier de données utilisateur.</span><span class="sxs-lookup"><span data-stu-id="38429-113">A browser process is associated with only one user data folder.</span></span>  <span data-ttu-id="38429-114">Un processus de demande peut spécifier plusieurs dossiers de données utilisateur.</span><span class="sxs-lookup"><span data-stu-id="38429-114">A request process may specify more than one user data folder.</span></span>  <span data-ttu-id="38429-115">Un processus de demande qui spécifie plusieurs dossiers de données utilisateur est associé au même nombre de processus de navigateur.</span><span class="sxs-lookup"><span data-stu-id="38429-115">A request process that specifies more than one user data folder is associated with the same number of browser processes.</span></span>  
<span data-ttu-id="38429-116">Par exemple, un processus de demande qui demande l’accès à deux dossiers de données utilisateur utilise deux processus de navigateur.</span><span class="sxs-lookup"><span data-stu-id="38429-116">For example, a request process that requests access to two user data folders uses two browser processes.</span></span>  

:::image type="complex" source="../media/process-model-2.png" alt-text="Processus 2" lightbox="../media/process-model-2.png":::
   <span data-ttu-id="38429-118">Processus 2</span><span class="sxs-lookup"><span data-stu-id="38429-118">Process 2</span></span>  
:::image-end:::    

<span data-ttu-id="38429-119">Un processus de navigateur est associé à plusieurs processus de rendu.</span><span class="sxs-lookup"><span data-stu-id="38429-119">A browser process is associated with several renderer processes.</span></span>  <span data-ttu-id="38429-120">Une instance WebView 2 crée un processus de navigateur pour traiter les images.</span><span class="sxs-lookup"><span data-stu-id="38429-120">A WebView 2 instance creates a browser process to service frames.</span></span>  <span data-ttu-id="38429-121">Un processus de navigateur peut être associé à plusieurs images.</span><span class="sxs-lookup"><span data-stu-id="38429-121">A browser process may be associated with multiple frames.</span></span>  <span data-ttu-id="38429-122">Un processus de navigateur peut être associé à différentes instances de WebView2.</span><span class="sxs-lookup"><span data-stu-id="38429-122">A browser process may be associated with different instances of WebView2.</span></span>  <span data-ttu-id="38429-123">Le nombre de processus de rendu varie en fonction des conditions suivantes.</span><span class="sxs-lookup"><span data-stu-id="38429-123">The number of render processes varies based on the following conditions.</span></span>  

*   <span data-ttu-id="38429-124">Utilisation de la fonctionnalité d’isolation de site web dans votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="38429-124">Use of the website isolation feature in your browser.</span></span>  
*   <span data-ttu-id="38429-125">Nombre d’origines déconnectées distinctes rendues dans les instances associées de WebView2.</span><span class="sxs-lookup"><span data-stu-id="38429-125">The number of distinct disconnected origins rendered in associated instances of WebView2.</span></span>  
    
<span data-ttu-id="38429-126">La fonctionnalité de navigateur d’isolation de site web est décrite dans le contenu précédent.</span><span class="sxs-lookup"><span data-stu-id="38429-126">The website isolation browser feature is described in the previous content.</span></span> 
<!--todo:  which previous content?  -->  

<span data-ttu-id="38429-127">Représente `CoreWebView2Environment` un dossier de données utilisateur et un processus de navigateur.</span><span class="sxs-lookup"><span data-stu-id="38429-127">The `CoreWebView2Environment` represents a user data folder and browser process.</span></span>  <span data-ttu-id="38429-128">Il ne correspond directement à aucun ensemble de processus, car différents processus de rendu sont utilisés par un contrôle WebView2 en fonction de l’isolation du site web, comme décrit `CoreWebView2` précédemment.</span><span class="sxs-lookup"><span data-stu-id="38429-128">The `CoreWebView2` does not directly correspond to any one set of processes since various renderer processes are used by a WebView2 depending on website isolation as previously described.</span></span>  

<span data-ttu-id="38429-129">Pour réagir aux incidents et se bloque dans le navigateur et les processus de rendu, utilisez `ProcessFailed` l’événement de `CoreWebView2` .</span><span class="sxs-lookup"><span data-stu-id="38429-129">To react to crashes and hangs in the browser and renderer processes, use the `ProcessFailed` event of `CoreWebView2`.</span></span>  

<span data-ttu-id="38429-130">Pour arrêter en toute sécurité les processus de navigateur et de rendu associés, utilisez `Close` la méthode de `CoreWebView2Controller` .</span><span class="sxs-lookup"><span data-stu-id="38429-130">To safely shut down associated browser and renderer processes, use the `Close` method of `CoreWebView2Controller`.</span></span>  

<span data-ttu-id="38429-131">Pour ouvrir la fenêtre Gestionnaire des tâches du navigateur à partir **de la fenêtre DevTools** d’une instance WebView2, terminez l’opération sur les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="38429-131">To open the Browser Task Manager window from the **DevTools** window of a WebView2 instance, complete on of the following actions.</span></span>  

*   <span data-ttu-id="38429-132">Sélectionnez `Shift` + `Escape` .</span><span class="sxs-lookup"><span data-stu-id="38429-132">Select `Shift`+`Escape`.</span></span>  
*   <span data-ttu-id="38429-133">Pointez sur la barre de titre de la fenêtre DevTools, ouvrez le menu contextuel \(clic droit\), puis choisissez `Browser task manager` .</span><span class="sxs-lookup"><span data-stu-id="38429-133">Hover on the DevTools window title bar, open the contextual menu \(right-click\), and choose `Browser task manager`.</span></span>  
    
<span data-ttu-id="38429-134">Tous les processus associés au processus de navigateur de votre WebView2 sont affichés, y compris les objectifs associés.</span><span class="sxs-lookup"><span data-stu-id="38429-134">All processes associated with the browser process of your WebView2 are displayed including associated purposes.</span></span>  

## <a name="see-also"></a><span data-ttu-id="38429-135">Voir également</span><span class="sxs-lookup"><span data-stu-id="38429-135">See also</span></span>  

*   <span data-ttu-id="38429-136">To Get Started using WebView2, navigate to [WebView2 Get Started Guides.][Webview2IndexGetStarted]</span><span class="sxs-lookup"><span data-stu-id="38429-136">To Get Started using WebView2, navigate to [WebView2 Get Started Guides][Webview2IndexGetStarted] guides.</span></span>  
*   <span data-ttu-id="38429-137">Pour obtenir un exemple complet des fonctionnalités WebView2, accédez au référentiel [WebView2Samples][GithubMicrosoftedgeWebview2samples] sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="38429-137">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples repo][GithubMicrosoftedgeWebview2samples] on GitHub.</span></span>  
*   <span data-ttu-id="38429-138">Pour plus d’informations sur les API WebView2, accédez à la référence [d’API.][DotnetApiMicrosoftWebWebview2WpfWebview2]</span><span class="sxs-lookup"><span data-stu-id="38429-138">For more detailed information about WebView2 APIs, navigate to [API reference][DotnetApiMicrosoftWebWebview2WpfWebview2].</span></span>  
*   <span data-ttu-id="38429-139">Pour plus d’informations sur WebView2, accédez [à Ressources WebView2.][Webview2IndexNextSteps]</span><span class="sxs-lookup"><span data-stu-id="38429-139">For more information about WebView2, navigate to [WebView2 Resources][Webview2IndexNextSteps].</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="38429-140">Entrer en contact avec l’équipe Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="38429-140">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2IndexGetStarted]: ../index.md#get-started "Get started - Introduction to Microsoft Edge WebView2 | Documents Microsoft"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Étapes suivantes : présentation de Microsoft Edge WebView2 | Documents Microsoft"  

[DotnetApiMicrosoftWebWebview2WpfWebview2]: /dotnet/api/microsoft.web.webview2.wpf.webview2 "Classe WebView2 | Documents Microsoft"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples - MicrosoftEdge/WebView2Samples | GitHub"  

[GoogleDeveloperWebUpdates201809InsideBrowserPart1BrowserArchitecture]: https://developers.google.com/web/updates/2018/09/inside-browser-part1#browser-architecture "Architecture du navigateur : examiner le navigateur web moderne (partie 1)"  
