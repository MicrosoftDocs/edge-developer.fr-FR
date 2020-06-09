---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 11d7e5ffef11a445c55cd4a9d70fcbbb8087c024
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698694"
---
# <span data-ttu-id="06eeb-104">interface ICoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="06eeb-104">interface ICoreWebView2NavigationCompletedEventArgs</span></span> 

```
interface ICoreWebView2NavigationCompletedEventArgs
  : public IUnknown
```

<span data-ttu-id="06eeb-105">Arguments d’événement pour l’événement NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="06eeb-105">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="06eeb-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="06eeb-106">Summary</span></span>

 <span data-ttu-id="06eeb-107">Ses</span><span class="sxs-lookup"><span data-stu-id="06eeb-107">Members</span></span>                        | <span data-ttu-id="06eeb-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="06eeb-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="06eeb-109">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="06eeb-109">get_IsSuccess</span></span>](#get_issuccess) | <span data-ttu-id="06eeb-110">True lorsque la navigation est réussie.</span><span class="sxs-lookup"><span data-stu-id="06eeb-110">True when the navigation is successful.</span></span>
[<span data-ttu-id="06eeb-111">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="06eeb-111">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="06eeb-112">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="06eeb-112">The ID of the navigation.</span></span>
[<span data-ttu-id="06eeb-113">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="06eeb-113">get_WebErrorStatus</span></span>](#get_weberrorstatus) | <span data-ttu-id="06eeb-114">Code d’erreur en cas d’échec de la navigation.</span><span class="sxs-lookup"><span data-stu-id="06eeb-114">The error code if the navigation failed.</span></span>

## <span data-ttu-id="06eeb-115">Ses</span><span class="sxs-lookup"><span data-stu-id="06eeb-115">Members</span></span>

#### <span data-ttu-id="06eeb-116">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="06eeb-116">get_IsSuccess</span></span> 

<span data-ttu-id="06eeb-117">True lorsque la navigation est réussie.</span><span class="sxs-lookup"><span data-stu-id="06eeb-117">True when the navigation is successful.</span></span>

> <span data-ttu-id="06eeb-118">valeur publique HRESULT [get_IsSuccess](#get_issuccess)(bool \* propriétés IsSuccess)</span><span class="sxs-lookup"><span data-stu-id="06eeb-118">public HRESULT [get_IsSuccess](#get_issuccess)(BOOL \* isSuccess)</span></span>

<span data-ttu-id="06eeb-119">Il s’agit de la valeur false pour une navigation qui s’est produite dans une page d’erreur (échecs en raison d’un réseau, échec de recherche DNS, serveur HTTP répond avec 4xx), mais peut également avoir la valeur false pour des éléments supplémentaires tels que Window. Stop () appelé sur la page de navigation.</span><span class="sxs-lookup"><span data-stu-id="06eeb-119">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="06eeb-120">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="06eeb-120">get_NavigationId</span></span> 

<span data-ttu-id="06eeb-121">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="06eeb-121">The ID of the navigation.</span></span>

> <span data-ttu-id="06eeb-122">navigation_id [get_NavigationId](#get_navigationid)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="06eeb-122">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

#### <span data-ttu-id="06eeb-123">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="06eeb-123">get_WebErrorStatus</span></span> 

<span data-ttu-id="06eeb-124">Code d’erreur en cas d’échec de la navigation.</span><span class="sxs-lookup"><span data-stu-id="06eeb-124">The error code if the navigation failed.</span></span>

> <span data-ttu-id="06eeb-125">[get_WebErrorStatus](#get_weberrorstatus)par le biais du public HRESULT (COREWEBVIEW2_WEB_ERROR_STATUS \* COREWEBVIEW2_WEB_ERROR_STATUS)</span><span class="sxs-lookup"><span data-stu-id="06eeb-125">public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(COREWEBVIEW2_WEB_ERROR_STATUS \* COREWEBVIEW2_WEB_ERROR_STATUS)</span></span>

