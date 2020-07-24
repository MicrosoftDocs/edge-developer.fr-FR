---
description: Modèle de processus
title: Modèle de processus
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 8548308896815266fbd1e150da979b56cfb268e2
ms.sourcegitcommit: 553957c101f83681b363103cb6af56bf20173f23
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/24/2020
ms.locfileid: "10895545"
---
# <span data-ttu-id="cfd2d-104">Modèle de processus</span><span class="sxs-lookup"><span data-stu-id="cfd2d-104">Process model</span></span>  

<span data-ttu-id="cfd2d-105">WebView2 utilise le même modèle de processus que le navigateur Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="cfd2d-105">WebView2 uses the same process model as the Microsoft Edge browser.</span></span>  <span data-ttu-id="cfd2d-106">Pour plus d’informations sur le modèle de processus de navigateur, voir [architecture de navigateur-dans l’interface du navigateur Web moderne][GoogleDeveloperWebUpdates201809InsideBrowserPart1BrowserArchitecture].</span><span class="sxs-lookup"><span data-stu-id="cfd2d-106">For more information about the browser process model, see [Browser Architecture - Inside look at modern web browser][GoogleDeveloperWebUpdates201809InsideBrowserPart1BrowserArchitecture].</span></span> 

<span data-ttu-id="cfd2d-107">Un processus de navigateur est associé aux processus de convertisseur et aux autres processus d’utilitaire, comme décrit dans cet article.</span><span class="sxs-lookup"><span data-stu-id="cfd2d-107">One browser process is associated with the renderer processes and other utility processes as described in that article.</span></span>  <span data-ttu-id="cfd2d-108">Par ailleurs, dans le cas de WebView2, il existe une application hôte demandant des processus à l’aide de WebView2.</span><span class="sxs-lookup"><span data-stu-id="cfd2d-108">Additionally, in the case of WebView2, there are host app requesting processes using WebView2.</span></span>  

:::image type="complex" source="../media/process-model-1.png" alt-text="Processus 1" lightbox="../media/process-model-1.png":::
   <span data-ttu-id="cfd2d-110">Processus 1</span><span class="sxs-lookup"><span data-stu-id="cfd2d-110">Process 1</span></span>  
:::image-end:::  

<span data-ttu-id="cfd2d-111">Un processus de navigateur est spécifié par dossier de données utilisateur dans une session utilisateur qui répond à tous les processus de demande WebView2 qui spécifient ce dossier de données utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cfd2d-111">One browser process is specified per user data folder in a user session that serve any WebView2 requesting process that specifies that user data folder.</span></span>  <span data-ttu-id="cfd2d-112">Cela signifie qu’un processus de navigateur est susceptible de traiter plusieurs processus de demande et qu’un processus de requête est susceptible d’utiliser plusieurs processus de navigateur.</span><span class="sxs-lookup"><span data-stu-id="cfd2d-112">This means one browser process may be serving multiple requesting processes and one requesting process may be using multiple browser processes.</span></span>  

:::image type="complex" source="../media/process-model-2.png" alt-text="Processus 2" lightbox="../media/process-model-2.png":::
   <span data-ttu-id="cfd2d-114">Processus 2</span><span class="sxs-lookup"><span data-stu-id="cfd2d-114">Process 2</span></span>  
:::image-end:::  

<span data-ttu-id="cfd2d-115">Un processus de navigateur a un certain nombre de processus de rendu associés.</span><span class="sxs-lookup"><span data-stu-id="cfd2d-115">A browser process has some number of associated renderer processes.</span></span>  <span data-ttu-id="cfd2d-116">Les processus du navigateur sont créés selon les besoins pour traiter les trames éventuellement multiples dans différentes instances de WebView2.</span><span class="sxs-lookup"><span data-stu-id="cfd2d-116">The browser processes are created as required to service potentially multiple frames in different instances of WebView2.</span></span>  <span data-ttu-id="cfd2d-117">Le nombre de processus de rendu varie en fonction de la fonctionnalité du navigateur d’isolation de site et du nombre d’origines déconnectées distinctes rendues dans les instances associées de WebView2.</span><span class="sxs-lookup"><span data-stu-id="cfd2d-117">The number of renderer processes varies based on the site isolation browser feature and the number of distinct disconnected origins rendered in associated instances of WebView2.</span></span>  <span data-ttu-id="cfd2d-118">La fonctionnalité navigateur d’isolation du site est décrite dans le contenu précédent.</span><span class="sxs-lookup"><span data-stu-id="cfd2d-118">The site isolation browser feature is described in the previous content.</span></span>  

<span data-ttu-id="cfd2d-119">`CoreWebView2Environment`Représente un dossier de données utilisateur et un processus de navigateur.</span><span class="sxs-lookup"><span data-stu-id="cfd2d-119">The `CoreWebView2Environment` represents a user data folder and browser process.</span></span>  <span data-ttu-id="cfd2d-120">Le `CoreWebView2` ne correspond pas directement à un ensemble de processus, car divers processus de rendu sont utilisés par un WebView2, en fonction de l’isolement du site, comme décrit précédemment.</span><span class="sxs-lookup"><span data-stu-id="cfd2d-120">The `CoreWebView2` does not directly correspond to any one set of processes since various renderer processes are used by a WebView2 depending on site isolation as previously described.</span></span>  

<span data-ttu-id="cfd2d-121">Vous pouvez réagir aux blocages et se bloquer dans ces processus de navigateur et de convertisseur à l’aide `ProcessFailed` de l’événement de `CoreWebView2` .</span><span class="sxs-lookup"><span data-stu-id="cfd2d-121">You are able to react to crashes and hangs in these browser and renderer processes using the `ProcessFailed` event of `CoreWebView2`.</span></span>  

<span data-ttu-id="cfd2d-122">Vous pouvez arrêter en toute sécurité les processus de navigateur et de convertisseur associés à l’aide `Close` de la méthode de `CoreWebView2Controller` .</span><span class="sxs-lookup"><span data-stu-id="cfd2d-122">You are able to safely shutdown associated browser and renderer processes using the `Close` method of `CoreWebView2Controller`.</span></span>  

<span data-ttu-id="cfd2d-123">Pour ouvrir la fenêtre Gestionnaire des tâches du navigateur à partir de la fenêtre de **devtools** d’une instance de WebView2, vous pouvez sélectionner `Shift` + `Escape` la barre de titre de la fenêtre devtools, ouvrir le menu contextuel (cliquez avec le bouton droit de la souris \) et choisir `Browser task manager` .</span><span class="sxs-lookup"><span data-stu-id="cfd2d-123">To open the Browser Task Manager window from the **DevTools** window of a WebView2 instance, you are able to select `Shift`+`Escape` or hover on the DevTools window title bar, open the contextual menu \(right-click\), and choose `Browser task manager`.</span></span>  <span data-ttu-id="cfd2d-124">Tous les processus associés au processus de navigation de votre WebView2 sont affichés, y compris les objectifs associés.</span><span class="sxs-lookup"><span data-stu-id="cfd2d-124">All processes associated with the browser process of your WebView2 are displayed including associated purposes.</span></span>  

<!-- links -->  

[GoogleDeveloperWebUpdates201809InsideBrowserPart1BrowserArchitecture]: https://developers.google.com/web/updates/2018/09/inside-browser-part1#browser-architecture "Architecture de navigateur-dans l’interface du navigateur Web moderne (partie 1)"  
