---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 215297bf56234452aad33e135cfb03ec079a049b
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877972"
---
# <span data-ttu-id="e2d9c-104">0.9.430-interface ICoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="e2d9c-104">0.9.430 - interface ICoreWebView2NavigationCompletedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="e2d9c-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="e2d9c-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="e2d9c-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="e2d9c-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NavigationCompletedEventArgs
  : public IUnknown
```

<span data-ttu-id="e2d9c-107">Arguments d’événement pour l’événement NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="e2d9c-107">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="e2d9c-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="e2d9c-108">Summary</span></span>

 <span data-ttu-id="e2d9c-109">Ses</span><span class="sxs-lookup"><span data-stu-id="e2d9c-109">Members</span></span>                        | <span data-ttu-id="e2d9c-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="e2d9c-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e2d9c-111">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="e2d9c-111">get_IsSuccess</span></span>](#get_issuccess) | <span data-ttu-id="e2d9c-112">True lorsque la navigation est réussie.</span><span class="sxs-lookup"><span data-stu-id="e2d9c-112">True when the navigation is successful.</span></span>
[<span data-ttu-id="e2d9c-113">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="e2d9c-113">get_WebErrorStatus</span></span>](#get_weberrorstatus) | <span data-ttu-id="e2d9c-114">Code d’erreur en cas d’échec de la navigation.</span><span class="sxs-lookup"><span data-stu-id="e2d9c-114">The error code if the navigation failed.</span></span>
[<span data-ttu-id="e2d9c-115">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="e2d9c-115">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="e2d9c-116">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="e2d9c-116">The ID of the navigation.</span></span>

## <span data-ttu-id="e2d9c-117">Ses</span><span class="sxs-lookup"><span data-stu-id="e2d9c-117">Members</span></span>

#### <span data-ttu-id="e2d9c-118">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="e2d9c-118">get_IsSuccess</span></span> 

<span data-ttu-id="e2d9c-119">True lorsque la navigation est réussie.</span><span class="sxs-lookup"><span data-stu-id="e2d9c-119">True when the navigation is successful.</span></span>

> <span data-ttu-id="e2d9c-120">valeur publique HRESULT [get_IsSuccess](#get_issuccess)(bool \* propriétés IsSuccess)</span><span class="sxs-lookup"><span data-stu-id="e2d9c-120">public HRESULT [get_IsSuccess](#get_issuccess)(BOOL \* isSuccess)</span></span>

<span data-ttu-id="e2d9c-121">Il s’agit de la valeur false pour une navigation qui s’est produite dans une page d’erreur (échecs en raison d’un réseau, échec de recherche DNS, serveur HTTP répond avec 4xx), mais peut également avoir la valeur false pour des éléments supplémentaires tels que Window. Stop () appelé sur la page de navigation.</span><span class="sxs-lookup"><span data-stu-id="e2d9c-121">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="e2d9c-122">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="e2d9c-122">get_WebErrorStatus</span></span> 

<span data-ttu-id="e2d9c-123">Code d’erreur en cas d’échec de la navigation.</span><span class="sxs-lookup"><span data-stu-id="e2d9c-123">The error code if the navigation failed.</span></span>

> <span data-ttu-id="e2d9c-124">[get_WebErrorStatus](#get_weberrorstatus)par le biais du public HRESULT (CORE_WEBVIEW2_WEB_ERROR_STATUS \* CORE_WEBVIEW2_WEB_ERROR_STATUS)</span><span class="sxs-lookup"><span data-stu-id="e2d9c-124">public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(CORE_WEBVIEW2_WEB_ERROR_STATUS \* CORE_WEBVIEW2_WEB_ERROR_STATUS)</span></span>

#### <span data-ttu-id="e2d9c-125">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="e2d9c-125">get_NavigationId</span></span> 

<span data-ttu-id="e2d9c-126">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="e2d9c-126">The ID of the navigation.</span></span>

> <span data-ttu-id="e2d9c-127">navigation_id [get_NavigationId](#get_navigationid)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="e2d9c-127">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

