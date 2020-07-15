---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 3a15232a7fe2ddf230d0463069052c55f7abc843
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879134"
---
# <span data-ttu-id="d7c7a-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="d7c7a-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2NavigationCompletedEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="d7c7a-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="d7c7a-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="d7c7a-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="d7c7a-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="d7c7a-107">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="d7c7a-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="d7c7a-108">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="d7c7a-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="d7c7a-109">Arguments d’événement pour l’événement NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="d7c7a-109">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="d7c7a-110">Résumé</span><span class="sxs-lookup"><span data-stu-id="d7c7a-110">Summary</span></span>

 <span data-ttu-id="d7c7a-111">Ses</span><span class="sxs-lookup"><span data-stu-id="d7c7a-111">Members</span></span>                        | <span data-ttu-id="d7c7a-112">Descriptions</span><span class="sxs-lookup"><span data-stu-id="d7c7a-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d7c7a-113">Propriétés IsSuccess</span><span class="sxs-lookup"><span data-stu-id="d7c7a-113">IsSuccess</span></span>](#issuccess) | <span data-ttu-id="d7c7a-114">True lorsque la navigation est réussie.</span><span class="sxs-lookup"><span data-stu-id="d7c7a-114">True when the navigation is successful.</span></span>
[<span data-ttu-id="d7c7a-115">NavigationId</span><span class="sxs-lookup"><span data-stu-id="d7c7a-115">NavigationId</span></span>](#navigationid) | <span data-ttu-id="d7c7a-116">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="d7c7a-116">The ID of the navigation.</span></span>
[<span data-ttu-id="d7c7a-117">WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="d7c7a-117">WebErrorStatus</span></span>](#weberrorstatus) | <span data-ttu-id="d7c7a-118">Code d’erreur en cas d’échec de la navigation.</span><span class="sxs-lookup"><span data-stu-id="d7c7a-118">The error code if the navigation failed.</span></span>

## <span data-ttu-id="d7c7a-119">Ses</span><span class="sxs-lookup"><span data-stu-id="d7c7a-119">Members</span></span>

#### <span data-ttu-id="d7c7a-120">Propriétés IsSuccess</span><span class="sxs-lookup"><span data-stu-id="d7c7a-120">IsSuccess</span></span> 

<span data-ttu-id="d7c7a-121">True lorsque la navigation est réussie.</span><span class="sxs-lookup"><span data-stu-id="d7c7a-121">True when the navigation is successful.</span></span>

> <span data-ttu-id="d7c7a-122">public bool [Propriétés IsSuccess](#issuccess)</span><span class="sxs-lookup"><span data-stu-id="d7c7a-122">public bool [IsSuccess](#issuccess)</span></span>

<span data-ttu-id="d7c7a-123">Il s’agit de la valeur false pour une navigation qui s’est produite dans une page d’erreur (échecs en raison d’un réseau, échec de recherche DNS, serveur HTTP répond avec 4xx), mais peut également avoir la valeur false pour des éléments supplémentaires tels que Window. Stop () appelé sur la page de navigation.</span><span class="sxs-lookup"><span data-stu-id="d7c7a-123">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="d7c7a-124">NavigationId</span><span class="sxs-lookup"><span data-stu-id="d7c7a-124">NavigationId</span></span> 

<span data-ttu-id="d7c7a-125">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="d7c7a-125">The ID of the navigation.</span></span>

> <span data-ttu-id="d7c7a-126">public ulong [NavigationId](#navigationid)</span><span class="sxs-lookup"><span data-stu-id="d7c7a-126">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="d7c7a-127">WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="d7c7a-127">WebErrorStatus</span></span> 

<span data-ttu-id="d7c7a-128">Code d’erreur en cas d’échec de la navigation.</span><span class="sxs-lookup"><span data-stu-id="d7c7a-128">The error code if the navigation failed.</span></span>

> <span data-ttu-id="d7c7a-129">public CoreWebView2WebErrorStatus [WebErrorStatus](#weberrorstatus)</span><span class="sxs-lookup"><span data-stu-id="d7c7a-129">public CoreWebView2WebErrorStatus [WebErrorStatus](#weberrorstatus)</span></span>

