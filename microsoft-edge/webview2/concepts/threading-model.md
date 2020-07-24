---
description: Modèle de threads
title: Modèle de threads
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: ad51afee97d3cc3e913ecdd73c4f0c2a99c70564
ms.sourcegitcommit: 553957c101f83681b363103cb6af56bf20173f23
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/24/2020
ms.locfileid: "10895544"
---
# <span data-ttu-id="bea74-104">Modèle de threads</span><span class="sxs-lookup"><span data-stu-id="bea74-104">Threading model</span></span>  

## <span data-ttu-id="bea74-105">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="bea74-105">Thread safety</span></span>  

<span data-ttu-id="bea74-106">WebView2 doit être créé sur un thread d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bea74-106">The WebView2 must be created on a UI thread.</span></span>  <span data-ttu-id="bea74-107">Particulièrement un thread avec une pompe de messages.</span><span class="sxs-lookup"><span data-stu-id="bea74-107">Specifically a thread with a message pump.</span></span>  <span data-ttu-id="bea74-108">Tous les rappels se produisent sur ce thread et les requêtes dans le WebView2 doivent être effectuées sur ce thread.</span><span class="sxs-lookup"><span data-stu-id="bea74-108">All callbacks occur on that thread and requests into the WebView2 must be done on that thread.</span></span>  <span data-ttu-id="bea74-109">Il n’est pas sûr d’utiliser le WebView2 à partir d’un autre thread.</span><span class="sxs-lookup"><span data-stu-id="bea74-109">It is not safe to use the WebView2 from another thread.</span></span>  

<span data-ttu-id="bea74-110">La seule exception est pour la `Content` propriété de `CoreWebView2WebResourceRequest` .</span><span class="sxs-lookup"><span data-stu-id="bea74-110">The only exception is for the `Content` property of `CoreWebView2WebResourceRequest`.</span></span>  <span data-ttu-id="bea74-111">Le `Content` flux de propriété est lu à partir d’un thread d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="bea74-111">The `Content` property stream is read from a background thread.</span></span>  <span data-ttu-id="bea74-112">Le flux doit être une technologie agile ou être créé à partir d’une tâche STA d’arrière-plan pour éviter l’impact sur les performances du thread d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bea74-112">The stream should be agile or be created from a background STA to prevent performance impact to the UI thread.</span></span>  

## <span data-ttu-id="bea74-113">Entr</span><span class="sxs-lookup"><span data-stu-id="bea74-113">Reentrancy</span></span>  

<span data-ttu-id="bea74-114">Les rappels incluant des gestionnaires d’événements et des gestionnaires d’achèvement s’exécutent en série.</span><span class="sxs-lookup"><span data-stu-id="bea74-114">Callbacks including event handlers and completion handlers run serially.</span></span>  <span data-ttu-id="bea74-115">Si vous disposez d’un gestionnaire d’événements et commencez une boucle de messages, aucun gestionnaire d’événements ou aucun rappel d’achèvement ne peut commencer à s’exécuter dans une méthode réentrante.</span><span class="sxs-lookup"><span data-stu-id="bea74-115">If you have an event handler running and begin a message loop, no other event handlers or completion callbacks are able to begin running in a reentrant manner.</span></span>  

## <span data-ttu-id="bea74-116">Reports</span><span class="sxs-lookup"><span data-stu-id="bea74-116">Deferrals</span></span>  

<span data-ttu-id="bea74-117">Certains événements WebView2 lisent les valeurs définies sur leurs arguments d’événement ou effectuent une action après la fin du gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="bea74-117">Some WebView2 events read values set on their event args or perform some action after the event handler completes.</span></span>  <span data-ttu-id="bea74-118">Si vous devez également exécuter une opération asynchrone telle qu’un gestionnaire d’événements, vous pouvez utiliser la `GetDeferral` méthode sur les arguments d’événement des événements associés.</span><span class="sxs-lookup"><span data-stu-id="bea74-118">If you also need to run an asynchronous operation such an event handler, you may use the `GetDeferral` method on the event args of the associated events.</span></span>  <span data-ttu-id="bea74-119">L’objet de report retourné garantit que le gestionnaire d’événements n’est pas considéré comme complet tant que la `Complete` méthode de l' `Deferral` est demandée.</span><span class="sxs-lookup"><span data-stu-id="bea74-119">The returned Deferral object ensures the event handler is not considered complete until the `Complete` method of the `Deferral` is requested.</span></span>  

<span data-ttu-id="bea74-120">Par exemple, vous pouvez utiliser l' `NewWindowRequested` événement pour fournir une `CoreWebView2` connexion en tant que fenêtre enfant lorsque le gestionnaire d’événements est terminé.</span><span class="sxs-lookup"><span data-stu-id="bea74-120">For instance, you may use the `NewWindowRequested` event to provide a `CoreWebView2` to connect as a child window when the event handler completes.</span></span>  <span data-ttu-id="bea74-121">Mais si vous avez besoin de créer la `CoreWebView2` méthode de manière asynchrone, demandez la `GetDeferral` méthode sur le `NewWindowRequestedEventArgs` .</span><span class="sxs-lookup"><span data-stu-id="bea74-121">But if you need to asynchronously create the `CoreWebView2`, request the `GetDeferral` method on the `NewWindowRequestedEventArgs`.</span></span>  <span data-ttu-id="bea74-122">Une fois que vous avez créé le et que vous avez `CoreWebView2` défini la `NewWindow` propriété sur la `NewWindowRequestedEventArgs` requête, l' `Complete` objet est retourné de manière asynchrone `Deferral` à l’aide de la `GetDeferral` méthode.</span><span class="sxs-lookup"><span data-stu-id="bea74-122">After you have asynchronously created the `CoreWebView2` and set the `NewWindow` property on the `NewWindowRequestedEventArgs`, request `Complete` on the `Deferral` object be returned using the `GetDeferral` method.</span></span>  

<!-- links -->  
