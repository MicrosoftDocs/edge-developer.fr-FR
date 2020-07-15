---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: c13d0625669d6303c115c3d415d12278cfbe8320
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880499"
---
# <span data-ttu-id="5d4e3-104">0.9.515-interface ICoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="5d4e3-104">0.9.515 - interface ICoreWebView2NavigationCompletedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="5d4e3-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="5d4e3-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="5d4e3-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="5d4e3-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NavigationCompletedEventArgs
  : public IUnknown
```

<span data-ttu-id="5d4e3-107">Arguments d’événement pour l’événement NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="5d4e3-107">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="5d4e3-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="5d4e3-108">Summary</span></span>

 <span data-ttu-id="5d4e3-109">Ses</span><span class="sxs-lookup"><span data-stu-id="5d4e3-109">Members</span></span>                        | <span data-ttu-id="5d4e3-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="5d4e3-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5d4e3-111">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="5d4e3-111">get_IsSuccess</span></span>](#get_issuccess) | <span data-ttu-id="5d4e3-112">True lorsque la navigation est réussie.</span><span class="sxs-lookup"><span data-stu-id="5d4e3-112">True when the navigation is successful.</span></span>
[<span data-ttu-id="5d4e3-113">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="5d4e3-113">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="5d4e3-114">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="5d4e3-114">The ID of the navigation.</span></span>
[<span data-ttu-id="5d4e3-115">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="5d4e3-115">get_WebErrorStatus</span></span>](#get_weberrorstatus) | <span data-ttu-id="5d4e3-116">Code d’erreur en cas d’échec de la navigation.</span><span class="sxs-lookup"><span data-stu-id="5d4e3-116">The error code if the navigation failed.</span></span>

## <span data-ttu-id="5d4e3-117">Ses</span><span class="sxs-lookup"><span data-stu-id="5d4e3-117">Members</span></span>

#### <span data-ttu-id="5d4e3-118">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="5d4e3-118">get_IsSuccess</span></span> 

<span data-ttu-id="5d4e3-119">True lorsque la navigation est réussie.</span><span class="sxs-lookup"><span data-stu-id="5d4e3-119">True when the navigation is successful.</span></span>

> <span data-ttu-id="5d4e3-120">valeur publique HRESULT [get_IsSuccess](#get_issuccess)(bool \* propriétés IsSuccess)</span><span class="sxs-lookup"><span data-stu-id="5d4e3-120">public HRESULT [get_IsSuccess](#get_issuccess)(BOOL \* isSuccess)</span></span>

<span data-ttu-id="5d4e3-121">Il s’agit de la valeur false pour une navigation qui s’est produite dans une page d’erreur (échecs en raison d’un réseau, échec de recherche DNS, serveur HTTP répond avec 4xx), mais peut également avoir la valeur false pour des éléments supplémentaires tels que Window. Stop () appelé sur la page de navigation.</span><span class="sxs-lookup"><span data-stu-id="5d4e3-121">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="5d4e3-122">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="5d4e3-122">get_NavigationId</span></span> 

<span data-ttu-id="5d4e3-123">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="5d4e3-123">The ID of the navigation.</span></span>

> <span data-ttu-id="5d4e3-124">navigation_id [get_NavigationId](#get_navigationid)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="5d4e3-124">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

#### <span data-ttu-id="5d4e3-125">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="5d4e3-125">get_WebErrorStatus</span></span> 

<span data-ttu-id="5d4e3-126">Code d’erreur en cas d’échec de la navigation.</span><span class="sxs-lookup"><span data-stu-id="5d4e3-126">The error code if the navigation failed.</span></span>

> <span data-ttu-id="5d4e3-127">[get_WebErrorStatus](#get_weberrorstatus)par le biais du public HRESULT (COREWEBVIEW2_WEB_ERROR_STATUS \* COREWEBVIEW2_WEB_ERROR_STATUS)</span><span class="sxs-lookup"><span data-stu-id="5d4e3-127">public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(COREWEBVIEW2_WEB_ERROR_STATUS \* COREWEBVIEW2_WEB_ERROR_STATUS)</span></span>

