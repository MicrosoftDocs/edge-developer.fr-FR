---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs
ms.openlocfilehash: aaaad1f622887ed1c941a9cf12ee4c753b352286
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878882"
---
# <span data-ttu-id="b347b-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="b347b-104">Microsoft.Web.WebView2.Core.CoreWebView2NavigationCompletedEventArgs class</span></span> 

<span data-ttu-id="b347b-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="b347b-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="b347b-106">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="b347b-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="b347b-107">Arguments d’événement pour l’événement NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="b347b-107">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="b347b-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="b347b-108">Summary</span></span>

 <span data-ttu-id="b347b-109">Ses</span><span class="sxs-lookup"><span data-stu-id="b347b-109">Members</span></span>                        | <span data-ttu-id="b347b-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="b347b-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b347b-111">Propriétés IsSuccess</span><span class="sxs-lookup"><span data-stu-id="b347b-111">IsSuccess</span></span>](#issuccess) | <span data-ttu-id="b347b-112">True lorsque la navigation est réussie.</span><span class="sxs-lookup"><span data-stu-id="b347b-112">True when the navigation is successful.</span></span>
[<span data-ttu-id="b347b-113">NavigationId</span><span class="sxs-lookup"><span data-stu-id="b347b-113">NavigationId</span></span>](#navigationid) | <span data-ttu-id="b347b-114">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="b347b-114">The ID of the navigation.</span></span>
[<span data-ttu-id="b347b-115">WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="b347b-115">WebErrorStatus</span></span>](#weberrorstatus) | <span data-ttu-id="b347b-116">Code d’erreur en cas d’échec de la navigation.</span><span class="sxs-lookup"><span data-stu-id="b347b-116">The error code if the navigation failed.</span></span>

## <span data-ttu-id="b347b-117">Ses</span><span class="sxs-lookup"><span data-stu-id="b347b-117">Members</span></span>

#### <span data-ttu-id="b347b-118">Propriétés IsSuccess</span><span class="sxs-lookup"><span data-stu-id="b347b-118">IsSuccess</span></span> 

<span data-ttu-id="b347b-119">True lorsque la navigation est réussie.</span><span class="sxs-lookup"><span data-stu-id="b347b-119">True when the navigation is successful.</span></span>

> <span data-ttu-id="b347b-120">public bool [Propriétés IsSuccess](#issuccess)</span><span class="sxs-lookup"><span data-stu-id="b347b-120">public bool [IsSuccess](#issuccess)</span></span>

<span data-ttu-id="b347b-121">Il s’agit de la valeur false pour une navigation qui s’est produite dans une page d’erreur (échecs en raison d’un réseau, échec de recherche DNS, serveur HTTP répond avec 4xx), mais peut également avoir la valeur false pour des éléments supplémentaires tels que Window. Stop () appelé sur la page de navigation.</span><span class="sxs-lookup"><span data-stu-id="b347b-121">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="b347b-122">NavigationId</span><span class="sxs-lookup"><span data-stu-id="b347b-122">NavigationId</span></span> 

<span data-ttu-id="b347b-123">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="b347b-123">The ID of the navigation.</span></span>

> <span data-ttu-id="b347b-124">public ulong [NavigationId](#navigationid)</span><span class="sxs-lookup"><span data-stu-id="b347b-124">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="b347b-125">WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="b347b-125">WebErrorStatus</span></span> 

<span data-ttu-id="b347b-126">Code d’erreur en cas d’échec de la navigation.</span><span class="sxs-lookup"><span data-stu-id="b347b-126">The error code if the navigation failed.</span></span>

> <span data-ttu-id="b347b-127">public CoreWebView2WebErrorStatus [WebErrorStatus](#weberrorstatus)</span><span class="sxs-lookup"><span data-stu-id="b347b-127">public CoreWebView2WebErrorStatus [WebErrorStatus](#weberrorstatus)</span></span>

