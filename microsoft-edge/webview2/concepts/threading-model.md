---
description: Modèle de thread
title: Modèle de thread
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 61e3b7fc8d25e2a1ce9c60fb84f5f39ba43f281b
ms.sourcegitcommit: efdc6369c48942bfa39e45c713300ed70f0e3655
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/12/2020
ms.locfileid: "11013736"
---
# <span data-ttu-id="59f38-104">Modèle de thread</span><span class="sxs-lookup"><span data-stu-id="59f38-104">Threading model</span></span> 

<span data-ttu-id="59f38-105">Le contrôle WebView2 est basé sur le [modèle COM (Component Object Model)](https://docs.microsoft.com/windows/win32/com/the-component-object-model) et doit être exécuté sur un thread de type [thread unique cloisonné (STA)](https://docs.microsoft.com/windows/win32/com/single-threaded-apartments) .</span><span class="sxs-lookup"><span data-stu-id="59f38-105">The WebView2 control is based on the [Component Object Model (COM)](https://docs.microsoft.com/windows/win32/com/the-component-object-model) and must run on a [Single Threaded Apartments (STA)](https://docs.microsoft.com/windows/win32/com/single-threaded-apartments) thread.</span></span>

## <span data-ttu-id="59f38-106">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="59f38-106">Thread safety</span></span>  

<span data-ttu-id="59f38-107">WebView2 doit être créé sur un thread d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="59f38-107">The WebView2 must be created on a UI thread.</span></span>  <span data-ttu-id="59f38-108">Particulièrement un thread avec une pompe de messages.</span><span class="sxs-lookup"><span data-stu-id="59f38-108">Specifically a thread with a message pump.</span></span>  <span data-ttu-id="59f38-109">Tous les rappels se produisent sur ce thread et les requêtes dans le WebView2 doivent être effectuées sur ce thread.</span><span class="sxs-lookup"><span data-stu-id="59f38-109">All callbacks occur on that thread and requests into the WebView2 must be done on that thread.</span></span>  <span data-ttu-id="59f38-110">Il n’est pas sûr d’utiliser le WebView2 à partir d’un autre thread.</span><span class="sxs-lookup"><span data-stu-id="59f38-110">It is not safe to use the WebView2 from another thread.</span></span>  

<span data-ttu-id="59f38-111">La seule exception est pour la `Content` propriété de `CoreWebView2WebResourceRequest` .</span><span class="sxs-lookup"><span data-stu-id="59f38-111">The only exception is for the `Content` property of `CoreWebView2WebResourceRequest`.</span></span>  <span data-ttu-id="59f38-112">Le `Content` flux de propriété est lu à partir d’un thread d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="59f38-112">The `Content` property stream is read from a background thread.</span></span>  <span data-ttu-id="59f38-113">Le flux doit être une technologie agile ou être créé à partir d’une tâche STA d’arrière-plan pour éviter l’impact sur les performances du thread d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="59f38-113">The stream should be agile or be created from a background STA to prevent performance impact to the UI thread.</span></span>  

## <span data-ttu-id="59f38-114">Entr</span><span class="sxs-lookup"><span data-stu-id="59f38-114">Reentrancy</span></span>  

<span data-ttu-id="59f38-115">Les rappels incluant des gestionnaires d’événements et des gestionnaires d’achèvement s’exécutent en série.</span><span class="sxs-lookup"><span data-stu-id="59f38-115">Callbacks including event handlers and completion handlers run serially.</span></span>  <span data-ttu-id="59f38-116">Si vous disposez d’un gestionnaire d’événements et commencez une boucle de messages, aucun gestionnaire d’événements ou aucun rappel d’achèvement ne peut commencer à s’exécuter dans une méthode réentrante.</span><span class="sxs-lookup"><span data-stu-id="59f38-116">If you have an event handler running and begin a message loop, no other event handlers or completion callbacks are able to begin running in a reentrant manner.</span></span>  

## <span data-ttu-id="59f38-117">Reports</span><span class="sxs-lookup"><span data-stu-id="59f38-117">Deferrals</span></span>  

<span data-ttu-id="59f38-118">Certains événements WebView2 lisent les valeurs définies sur leurs arguments d’événement ou effectuent une action après la fin du gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="59f38-118">Some WebView2 events read values set on their event args or perform some action after the event handler completes.</span></span>  <span data-ttu-id="59f38-119">Si vous devez également exécuter une opération asynchrone telle qu’un gestionnaire d’événements, vous pouvez utiliser la `GetDeferral` méthode sur les arguments d’événement des événements associés.</span><span class="sxs-lookup"><span data-stu-id="59f38-119">If you also need to run an asynchronous operation such an event handler, you may use the `GetDeferral` method on the event args of the associated events.</span></span>  <span data-ttu-id="59f38-120">L’objet de report retourné garantit que le gestionnaire d’événements n’est pas considéré comme complet tant que la `Complete` méthode de l' `Deferral` est demandée.</span><span class="sxs-lookup"><span data-stu-id="59f38-120">The returned Deferral object ensures the event handler is not considered complete until the `Complete` method of the `Deferral` is requested.</span></span>  

<span data-ttu-id="59f38-121">Par exemple, vous pouvez utiliser l' `NewWindowRequested` événement pour fournir une `CoreWebView2` connexion en tant que fenêtre enfant lorsque le gestionnaire d’événements est terminé.</span><span class="sxs-lookup"><span data-stu-id="59f38-121">For instance, you may use the `NewWindowRequested` event to provide a `CoreWebView2` to connect as a child window when the event handler completes.</span></span>  <span data-ttu-id="59f38-122">Mais si vous avez besoin de créer la `CoreWebView2` méthode de manière asynchrone, demandez la `GetDeferral` méthode sur le `NewWindowRequestedEventArgs` .</span><span class="sxs-lookup"><span data-stu-id="59f38-122">But if you need to asynchronously create the `CoreWebView2`, request the `GetDeferral` method on the `NewWindowRequestedEventArgs`.</span></span>  <span data-ttu-id="59f38-123">Une fois que vous avez créé le et que vous avez `CoreWebView2` défini la `NewWindow` propriété sur la `NewWindowRequestedEventArgs` requête, l' `Complete` objet est retourné de manière asynchrone `Deferral` à l’aide de la `GetDeferral` méthode.</span><span class="sxs-lookup"><span data-stu-id="59f38-123">After you have asynchronously created the `CoreWebView2` and set the `NewWindow` property on the `NewWindowRequestedEventArgs`, request `Complete` on the `Deferral` object be returned using the `GetDeferral` method.</span></span>  

<!-- links -->  
