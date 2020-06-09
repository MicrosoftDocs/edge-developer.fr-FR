---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/28/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 83f55e19c8c8c0f2fb075ff47e95e34be27c6602
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697335"
---
# <span data-ttu-id="908b7-104">interface ICoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="908b7-104">interface ICoreWebView2NavigationCompletedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="908b7-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="908b7-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="908b7-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="908b7-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NavigationCompletedEventArgs
  : public IUnknown
```

<span data-ttu-id="908b7-107">Arguments d’événement pour l’événement NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="908b7-107">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="908b7-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="908b7-108">Summary</span></span>

 <span data-ttu-id="908b7-109">Ses</span><span class="sxs-lookup"><span data-stu-id="908b7-109">Members</span></span>                        | <span data-ttu-id="908b7-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="908b7-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="908b7-111">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="908b7-111">get_IsSuccess</span></span>](#get_issuccess) | <span data-ttu-id="908b7-112">True lorsque la navigation est réussie.</span><span class="sxs-lookup"><span data-stu-id="908b7-112">True when the navigation is successful.</span></span>
[<span data-ttu-id="908b7-113">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="908b7-113">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="908b7-114">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="908b7-114">The ID of the navigation.</span></span>
[<span data-ttu-id="908b7-115">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="908b7-115">get_WebErrorStatus</span></span>](#get_weberrorstatus) | <span data-ttu-id="908b7-116">Code d’erreur en cas d’échec de la navigation.</span><span class="sxs-lookup"><span data-stu-id="908b7-116">The error code if the navigation failed.</span></span>

## <span data-ttu-id="908b7-117">Ses</span><span class="sxs-lookup"><span data-stu-id="908b7-117">Members</span></span>

#### <span data-ttu-id="908b7-118">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="908b7-118">get_IsSuccess</span></span> 

<span data-ttu-id="908b7-119">True lorsque la navigation est réussie.</span><span class="sxs-lookup"><span data-stu-id="908b7-119">True when the navigation is successful.</span></span>

> <span data-ttu-id="908b7-120">valeur publique HRESULT [get_IsSuccess](#get_issuccess)(bool \* propriétés IsSuccess)</span><span class="sxs-lookup"><span data-stu-id="908b7-120">public HRESULT [get_IsSuccess](#get_issuccess)(BOOL \* isSuccess)</span></span>

<span data-ttu-id="908b7-121">Il s’agit de la valeur false pour une navigation qui s’est produite dans une page d’erreur (échecs en raison d’un réseau, échec de recherche DNS, serveur HTTP répond avec 4xx), mais peut également avoir la valeur false pour des éléments supplémentaires tels que Window. Stop () appelé sur la page de navigation.</span><span class="sxs-lookup"><span data-stu-id="908b7-121">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="908b7-122">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="908b7-122">get_NavigationId</span></span> 

<span data-ttu-id="908b7-123">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="908b7-123">The ID of the navigation.</span></span>

> <span data-ttu-id="908b7-124">navigation_id [get_NavigationId](#get_navigationid)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="908b7-124">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

#### <span data-ttu-id="908b7-125">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="908b7-125">get_WebErrorStatus</span></span> 

<span data-ttu-id="908b7-126">Code d’erreur en cas d’échec de la navigation.</span><span class="sxs-lookup"><span data-stu-id="908b7-126">The error code if the navigation failed.</span></span>

> <span data-ttu-id="908b7-127">[get_WebErrorStatus](#get_weberrorstatus)par le biais du public HRESULT (COREWEBVIEW2_WEB_ERROR_STATUS \* COREWEBVIEW2_WEB_ERROR_STATUS)</span><span class="sxs-lookup"><span data-stu-id="908b7-127">public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(COREWEBVIEW2_WEB_ERROR_STATUS \* COREWEBVIEW2_WEB_ERROR_STATUS)</span></span>

